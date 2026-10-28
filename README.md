# Game Legal Pages

Public legal pages for games published by PanJung99.

## Pages

- 银河火线 TapTap 隐私政策: `docs/galactic-fireline/taptap/privacy/index.html`
- 银河火线 Google Play 隐私政策: `docs/galactic-fireline/google-play/privacy/index.html`
- 银河火线 Google Play 发布核对（不发布到网页）: `sources/galactic-fireline/google-play/release-review.md`

After enabling GitHub Pages with branch `main` and folder `/docs`, the public URL will be:

```text
https://panjung99.github.io/game-legal-pages/galactic-fireline/taptap/privacy/
```

## Structure

Use one directory per game and platform:

```text
docs/
  <game-slug>/
    taptap/
      privacy/
        index.html
    google-play/
      privacy/
        index.html

sources/
  <game-slug>/
    taptap/
      privacy.md
    google-play/
      privacy.md
```

Keep `docs/` for rendered HTML pages and `sources/` for editable Markdown drafts.
