# AI Digest

Personal weekly AI developments digest. Generated automatically every Sunday by a Cowork scheduled task.

- **Live site:** https://&lt;your-username&gt;.github.io/ai-digest/
- **Archive:** https://&lt;your-username&gt;.github.io/ai-digest/archive/
- **Source markdown:** the scheduled task also produces a markdown file in the Cowork outputs folder.

## Repo layout

```
/
├── index.html                  ← latest week (overwritten each Sunday)
├── archive/
│   ├── index.html              ← list of past weeks (regenerated each Sunday)
│   └── YYYY-MM-DD.html         ← permanent per-week archive
├── manifest.json               ← PWA manifest (iOS home-screen install)
├── sw.js                       ← service worker, offline caching
├── icon.svg / icon-*.png       ← icons
├── .nojekyll                   ← skip Jekyll, serve files as-is
└── README.md
```

## How updates land here

The scheduled task in Cowork (file: `weekly-ai-developments-digest.SKILL.md`) does:

1. Research the past 7 days of AI news.
2. Generate the new digest as HTML.
3. `git clone` this repo with a fine-grained PAT, write the new files, `git commit`, `git push`.
4. GitHub Pages rebuilds within a few minutes.

## Adding past weeks

To backfill an old week as an archive entry, drop the HTML at `archive/YYYY-MM-DD.html` and add an entry to `archive/index.html`. The deploy script does both automatically each week.
