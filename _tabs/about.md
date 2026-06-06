---
# the default layout is 'page'
icon: fas fa-info-circle
order: 1
---

<style>
  .follow-links {
    margin: 1.5rem 0;
    border: 1px solid var(--tb-border-color);
    border-radius: 12px;
    overflow: hidden;
  }
  .follow-links a {
    display: flex;
    align-items: center;
    gap: 1rem;
    padding: 0.9rem 1.1rem;
    text-decoration: none;
    color: var(--text-color);
    background: var(--card-bg);
    transition: background-color 0.18s cubic-bezier(0.22, 1, 0.36, 1);
  }
  .follow-links a + a {
    border-top: 1px solid var(--tb-border-color);
  }
  .follow-links a:hover {
    background: color-mix(in srgb, var(--link-color) 6%, var(--card-bg));
  }
  .follow-links .fl-icon {
    flex: 0 0 2.6rem;
    height: 2.6rem;
    display: grid;
    place-items: center;
    border-radius: 9px;
    font-size: 1.3rem;
    color: #fff;
  }
  .follow-links .fl-title {
    font-weight: 600;
    line-height: 1.2;
  }
  .follow-links .fl-sub {
    font-size: 0.85rem;
    color: var(--text-muted-color);
  }
  .follow-links .fl-arrow {
    margin-left: auto;
    color: var(--text-muted-color);
    transition: transform 0.18s cubic-bezier(0.22, 1, 0.36, 1);
  }
  .follow-links a:hover .fl-arrow {
    transform: translateX(3px);
    color: var(--link-color);
  }
  .fl-disclaimer {
    margin-top: 2.5rem;
    padding-top: 1rem;
    border-top: 1px solid var(--tb-border-color);
    font-size: 0.82rem;
    line-height: 1.5;
    color: var(--text-muted-color);
  }
</style>

# Building an airplane in my garage

I'm **Fan**, and I'm assembling a [Sling Tsi](https://www.airplanefactory.com/aircraft/sling-tsi/), a sleek four-seat aircraft, from a box of parts in the San Francisco Bay Area.

This is my build log. Thousands of rivets, miles of wire, and a fair amount of patience, slowly turning into a flying machine. The good days and the head-scratchers are all here.

## Follow along

<div class="follow-links">
  <a href="https://youtube.com/@fanflynorcal?si=xHDwt0aCdQs9oAYJ" target="_blank" rel="noopener noreferrer">
    <span class="fl-icon" style="background:#ff0033;"><i class="fab fa-youtube"></i></span>
    <span>
      <span class="fl-title">YouTube</span><br>
      <span class="fl-sub">Video build logs from the hangar</span>
    </span>
    <i class="fas fa-arrow-right fl-arrow"></i>
  </a>
  <a href="https://photos.app.goo.gl/oAyhZDqKqAVYoPcz5" target="_blank" rel="noopener noreferrer">
    <span class="fl-icon" style="background:#1a73e8;"><i class="fas fa-camera-retro"></i></span>
    <span>
      <span class="fl-title">Photo album</span><br>
      <span class="fl-sub">Real-time photos as the build happens</span>
    </span>
    <i class="fas fa-arrow-right fl-arrow"></i>
  </a>
</div>

Prefer the written word? The [posts]({{ site.url }}) here cover each step in detail.

<p class="fl-disclaimer">I'm not a professional builder, and this site only documents my own experience. Please do your own research before applying anything here to your own build.</p>
