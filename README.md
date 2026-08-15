# luckygirl — content

Published daily content for the **luckygirl** app. Served over GitHub Pages at:

```
https://handf00t.github.io/luckygirl-data/v1/<YYYY-MM-DD>.json
https://handf00t.github.io/luckygirl-data/v1/latest.json
```

The app asks for the exact day first and falls back to `latest.json`, which
matters at a time-zone edge: a reader west of UTC can ask for a date the
pipeline has published but this CDN edge has not yet picked up, and serving
something current beats an error screen.

Everything here is generated — see `pipeline/` in the app repo. Do not hand-edit:
the next run overwrites it, and the ranking is reproducible from the date alone,
so an edit here would disagree with what the pipeline believes it published.

No personal data. The app sends no identifiers; it performs a plain GET.
