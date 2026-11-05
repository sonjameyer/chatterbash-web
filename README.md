# chatterbash-web

The marketing website for **ChatterBash**, a party game of explaining, hinting,
and miming by Bouncy Wizard. Live at [chatterbash.com](https://chatterbash.com).

Get the app:

- [Google Play](https://play.google.com/store/apps/details?id=com.bouncywizard.chatterbash)
- [App Store](https://apps.apple.com/app/id6808120869)

## Contents

This is a plain static site: no build step, no dependencies.

| File | Purpose |
| --- | --- |
| `index.html` | Landing page: game overview, the three rounds, store links |
| `privacy.html` | Privacy policy (linked from the app store listings) |
| `style.css` | Shared stylesheet for both pages |
| `logo.png`, `favicon.png`, `apple-touch-icon.png` | Branding and icons |
| `google-play-badge.png`, `app-store-badge.svg` | Store badges |
| `CNAME` | Custom domain for GitHub Pages |

## Local preview

Open `index.html` directly in a browser, or serve the folder so relative links
behave exactly as they do in production:

```sh
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment

The site is hosted on GitHub Pages from the `main` branch, served at
`chatterbash.com` via the `CNAME` file. Pushing to `main` publishes changes.

When you change `style.css`, bump the cache-buster query string in the
`<link rel="stylesheet" href="style.css?v=N">` tag in each HTML page so
visitors pick up the new styles.

## Contact

Bouncy Wizard · [bouncywizardapps@gmail.com](mailto:bouncywizardapps@gmail.com)
