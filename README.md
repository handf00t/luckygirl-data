# luckygirl — content

Published daily content for the **luckygirl** app. Served over GitHub Pages at:

```
https://handf00t.github.io/luckygirl-data/v1/<YYYY-MM-DD>-<digest>.json
https://handf00t.github.io/luckygirl-data/v1/latest.json
```

The digest in the filename is not decoration. Readers span time zones and each
should get *their* local date, so a day's file has to be live before that day
begins anywhere — at UTC+14. The app is built on a closed day and a reveal, and
a plainly dated file published that early would let anyone read tomorrow by
editing a digit. With a digest there is nothing to increment.

Obscurity, not security: the salt lives in the app binary. It raises the bar
from typing a URL to reverse-engineering a build, which is the right bar here.

`latest.json` is the one guessable name, so it deliberately holds the newest day
that has already begun *everywhere* (UTC-12). It is a fallback for a CDN miss,
not the leading edge.

Everything here is generated — see `pipeline/` in the app repo. Do not hand-edit:
the next run overwrites it, and the ranking is reproducible from the date alone,
so an edit here would disagree with what the pipeline believes it published.

No personal data. The app sends no identifiers; it performs a plain GET.
