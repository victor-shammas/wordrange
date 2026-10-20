# Wordrange website (GitHub Pages, custom domain)

The static marketing, support and privacy pages for Wordrange, a Mac app that counts the words in a
manuscript the way journals count them. Plain HTML and one stylesheet (shared with the other apps at
victorshammas.com), with no build step, external fonts, scripts or trackers. The app's source lives in a
private repo.

| File | Published URL |
|---|---|
| `index.html` | https://victorshammas.com/wordrange/ (Marketing URL) |
| `support.html` | https://victorshammas.com/wordrange/support.html (Support URL; the app's Help menu opens it) |
| `privacy.html` | https://victorshammas.com/wordrange/privacy.html (Privacy Policy URL) |
| `style.css`, `icon.png`, `favicon.png`, `apple-touch-icon.png` | assets (the icons come from `Design/make-icon.swift` in the app repo) |
| `.nojekyll` | tells Pages to serve files as-is |

Keep these paths stable: the app links to `support.html`, and App Store Connect to all three.

## How the URL works

The user site (`victor-shammas.github.io`) has the custom domain `victorshammas.com`, so every public
project repo with Pages turned on is served at `https://victorshammas.com/<repo-name>/`. This repo must be
named `wordrange` and needs no `CNAME` file. Pages: Settings › Pages › Deploy from a branch › `main`, `/ (root)`.

## At launch

- Replace the "Coming soon" span in `index.html` with the App Store link in the comment above it
  (`https://apps.apple.com/app/idPLACEHOLDER`, with the numeric Apple ID from App Store Connect). Optionally
  use Apple's official "Download on the Mac App Store" badge, following Apple's badge rules.
- Add Wordrange to https://victorshammas.com/apps/ (`static/apps/index.html` in `victor-shammas.github.io`)
  and to the app bar of the other apps' sites.
