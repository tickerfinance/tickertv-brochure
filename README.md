# Ticker TV brochure

Standalone marketing/brochure site for **Ticker TV** — Copia's IR video & social media package
(CEO interviews, Fireside Chats, Town Hall Q&As, event coverage for listed companies and fund
managers).

Plain static site: a single [`index.html`](index.html) plus [`assets/`](assets/) (media, logos,
team, patterns). No build step, no framework, no dependencies.

## Deployments

Hosted entirely on **Cloudflare Pages**, connected to this GitHub repo. There is no build command;
the output directory is the repo root. All deploys are automatic — never a manual step.

| Push to | Deploys to | URL |
|---|---|---|
| **`main`** | Production | https://tv.ticker.app |
| **any other branch** | Preview | `https://<branch>.tickertv-brochure.pages.dev` |

Cloudflare gives Vercel-style previews out of the box: **every non-`main` branch gets its own live
URL**, and every individual commit gets a unique `https://<hash>.tickertv-brochure.pages.dev`.
Open a PR and Cloudflare comments the preview link on it.

### Typical flow

```bash
git switch -c my-change      # any branch name
# ...edit...
git commit -am "..." && git push -u origin my-change
# → live at https://my-change.tickertv-brochure.pages.dev

# ship it
git switch main && git merge my-change && git push
# → production deploy
```

## Local preview

No server needed; open `index.html` directly, or:

```bash
python3 -m http.server 8000   # http://localhost:8000
```
