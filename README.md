# claude-artifacts

Static HTML artifacts built with Claude, published via GitHub Pages.

**Live site:** https://bryanhirsch.github.io/primers/

## Artifacts

| Directory | Page | Live URL |
| --- | --- | --- |
| `midsummer-nights-dream/` | A Midsummer Night's Dream — Pocket Companion | [/midsummer-nights-dream/](https://bryanhirsch.github.io/claude-artifacts/midsummer-nights-dream/) |
| `spain-argentina-final-primer/` | Spain ✕ Argentina — The World Cup Final, Explained | [/spain-argentina-final-primer/](https://bryanhirsch.github.io/claude-artifacts/spain-argentina-final-primer/) |
| `spain-france-primer/` | Spain ✕ France — Your Watch-Party Primer | [/spain-france-primer/](https://bryanhirsch.github.io/claude-artifacts/spain-france-primer/) |
| `england-mexico-primer/` | England ✕ Mexico — Your Watch-Party Primer | [/england-mexico-primer/](https://bryanhirsch.github.io/claude-artifacts/england-mexico-primer/) |
| `boston-legacy-primer/` | Boston Legacy ✕ Washington Spirit — Your Primer | [/boston-legacy-primer/](https://bryanhirsch.github.io/claude-artifacts/boston-legacy-primer/) |

Each artifact is one self-contained `index.html` — inline CSS and JS, no build
step, no local assets. The only external requests are Google Fonts and outbound
YouTube links.

## Layout

```
.
├── index.html                        # landing page linking to each artifact
├── .nojekyll                         # serve files as-is, no Jekyll processing
├── .github/workflows/pages.yml       # deploys the repo root to Pages on push to main
└── <artifact-name>/index.html
```

## Enabling Pages

The deploy workflow is committed, but the repository setting has to be flipped
once by hand:

**Settings → Pages → Build and deployment → Source → GitHub Actions**

After that, every push to `main` publishes the site. You can also trigger a
deploy manually from the **Actions** tab (*Deploy to GitHub Pages* →
*Run workflow*).

## Adding another artifact

1. Create a directory named after the artifact.
2. Save the artifact HTML inside it as `index.html`.
3. Add a card for it in the root `index.html` and a row in the table above.

## Local preview

```sh
python3 -m http.server 8000
# then open http://localhost:8000/
```
