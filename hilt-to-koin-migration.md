# Hilt to Koin Migration — Feasibility Review & Implementation Plan

## Feasibility: High (moderate effort)

Both are mature DI frameworks for Android/Kotlin. Migration is well-documented and concepts map 1:1, but the scope of changes depends on project size.

### Key Differences

| Aspect | Hilt | Koin |
|---|---|---|
| Type | Compile-time (codegen) | Runtime (service locator) |
| Build speed | Slower (kapt/ksp) | Faster |
| Error detection | Compile-time | Runtime |
| Boilerplate | More (annotations) | Less |
| Test setup | Complex | Simpler |
| Multiplatform | Android only | KMP-ready |

### Risks

- **Runtime errors**: Koin catches missing dependencies at runtime, not compile-time — requires thorough testing
- **Scope mapping**: Hilt's `@InstallIn` components map to Koin's scopes but not identically
- **Hilt-specific integrations**: `@HiltWorker` (WorkManager), `@HiltNavGraphViewModel`, Navigation component bindings need manual wiring

---

## Implementation Plan

### Phase 1: Preparation

1. Audit all Hilt usages: `@HiltAndroidApp`, `@AndroidEntryPoint`, `@HiltViewModel`, `@Module`, `@InstallIn`, `@Provides`, `@Binds`, `@Inject`, `@EntryPoint`
2. Map Hilt components to Koin scopes:
   - `SingletonComponent` → `single { }` in root module
   - `ActivityRetainedComponent` → `viewModel { }`
   - `ActivityComponent` → `scope<Activity> { }`
   - `FragmentComponent` → `scope<Fragment> { }`
   - `ViewModelScoped` → `viewModel { }` with scoped deps
3. Identify any `@EntryPoint` usages (need special handling)

---

### Phase 2: Dependency Swap

```kotlin
// Remove:
plugins { id("com.google.dagger.hilt.android") }
kapt("com.google.dagger:hilt-android-compiler:2.x")
implementation("com.google.dagger:hilt-android:2.x")

// Add:
implementation("io.insert-koin:koin-android:3.5.x")
implementation("io.insert-koin:koin-androidx-viewmodel:3.5.x")
// Optional for Compose:
implementation("io.insert-koin:koin-androidx-compose:3.5.x")
```

---

### Phase 3: Application Class

```kotlin
// Before (Hilt):
@HiltAndroidApp
class App : Application()

// After (Koin):
class App : Application() {
    override fun onCreate() {
        super.onCreate()
        startKoin {
            androidLogger()
            androidContext(this@App)
            modules(appModule, networkModule, repositoryModule)
        }
    }
}
```

---

### Phase 4: Convert Modules

```kotlin
// Before (Hilt):
@Module
@InstallIn(SingletonComponent::class)
object NetworkModule {
    @Provides @Singleton
    fun provideRetrofit(): Retrofit = Retrofit.Builder()...build()

    @Provides @Singleton
    fun provideApiService(retrofit: Retrofit): ApiService =
        retrofit.create(ApiService::class.java)
}

// After (Koin):
val networkModule = module {
    single { Retrofit.Builder()...build() }
    single { get<Retrofit>().create(ApiService::class.java) }
}
```

---

### Phase 5: Convert ViewModels

```kotlin
// Before (Hilt):
@HiltViewModel
class MainViewModel @Inject constructor(
    private val repo: UserRepository
) : ViewModel()

// After (Koin):
class MainViewModel(
    private val repo: UserRepository
) : ViewModel()

// In module:
val viewModelModule = module {
    viewModel { MainViewModel(get()) }
}

// In Fragment/Activity:
val vm: MainViewModel by viewModel()
```

---

### Phase 6: Remove `@AndroidEntryPoint`

```kotlin
// Before:
@AndroidEntryPoint
class MainActivity : AppCompatActivity() {
    @Inject lateinit var analytics: Analytics
}

// After:
class MainActivity : AppCompatActivity() {
    private val analytics: Analytics by inject()
}
```

---

### Phase 7: Testing

```kotlin
// Before (Hilt test):
@HiltAndroidTest
class MainActivityTest { ... }

// After (Koin test):
class MainActivityTest : KoinTest {
    @get:Rule val koinRule = KoinTestRule.create {
        modules(testModule)
    }
    val analytics: Analytics by inject()
}
```

---

### Phase 8: Cleanup

- Remove all Hilt annotations (`@HiltAndroidApp`, `@AndroidEntryPoint`, `@HiltViewModel`, `@Inject` field injections)
- Remove Hilt Gradle plugin
- Remove `hilt-android-compiler` kapt dependency
- Remove `@Module`/`@InstallIn`/`@Provides`/`@Binds` classes (replaced by Koin modules)
- Run full test suite

---

## Effort Estimate by Project Size

| Project size | Estimated effort |
|---|---|
| Small (<10 modules, <20 ViewModels) | 1–2 days |
| Medium (10–30 modules, 20–50 ViewModels) | 3–5 days |
| Large (30+ modules, 50+ ViewModels) | 1–2 weeks |

---

## Recommendation

Proceed — Koin offers simpler syntax, faster builds, and KMP readiness. The main tradeoff is losing compile-time safety, which you mitigate with solid unit tests and `checkModules()` in CI:

```kotlin
// Verify all Koin bindings resolve at test time:
class KoinModuleTest : KoinTest {
    @Test
    fun verifyKoinModules() {
        androidApplication().checkModules()
    }
}
```
