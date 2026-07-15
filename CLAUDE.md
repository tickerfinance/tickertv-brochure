# tickertv-brochure

Standalone static brochure site for **Ticker TV** (Copia's IR video & social media package).
Single [`index.html`](index.html) + [`assets/`](assets/). No build, no framework, no dependencies.

## Deployments — Cloudflare Pages, automatic, git-driven

Everything is on **Cloudflare Pages** (connected to this repo; no build command, output dir = repo
root). No manual deploys, and no GitHub Pages.

- **`main` → production** at **https://tv.ticker.app**. Pushing to `main` deploys production.
- **Any other branch → its own preview**, Vercel-style: `https://<branch>.tickertv-brochure.pages.dev`,
  plus a unique per-commit `https://<hash>.tickertv-brochure.pages.dev`. PRs get the preview link
  commented automatically.

To preview before shipping: push any branch, check its preview URL, then merge to `main`.

## Editing notes

- Everything is in one `index.html` (inline styles/scripts). Keep it self-contained.
- Media/logos/team images live under `assets/`; reference with relative paths.
- The GitHub org is **tickerfinance** (dir is named `irdataservices` for historical reasons).
- Production domain is **tv.ticker.app**; OG/social meta in `index.html` points there.
