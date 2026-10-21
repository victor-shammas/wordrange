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

## The free download

The download button links to `https://github.com/victor-shammas/wordrange/releases/latest/download/Wordrange.dmg`:
the latest release of this repo. Releases hold only the notarized DMG, never source code (that's in the private
repo `wordrange-app`). To publish a new version, in the app repo: `scripts/release-direct.sh`, then
`gh release create v<version> build/direct/Wordrange.dmg -R victor-shammas/wordrange --title "Wordrange <version>"`,
and update the version in the hero's fine print.

## At the App Store launch

- Add the App Store button from the comment under the download button in `index.html`
  (`https://apps.apple.com/app/id6825066145`). Optionally use Apple's official "Download on the Mac App Store"
  badge, following Apple's badge rules.
- Change the "Coming soon" pill on https://victorshammas.com/apps/ and the Apps board card.
