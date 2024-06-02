## Merge from remote:

https://stackoverflow.com/questions/41283955/github-keeps-saying-this-branch-is-x-commits-ahead-y-commits-behind

## Regenerate minified javascripts

```
NODE_ENV=production npx rollup -c --bundleConfigAsCjs
```

## Minify all jpges

```
mogrify -define jpeg:extent=800kb -resize 1000 */*.jpg
```
