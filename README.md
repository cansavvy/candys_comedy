# Candy's Comedy

Single-page marketing site for **Candy's Comedy** (standup, Baltimore). Built with [Quarto](https://quarto.org) using the [OTTR](https://www.ottrproject.org/) automation template: spelling and URL checks on pull requests, and rendering on push to `main` / `staging`.

## Edit the site

- **Page content:** [`index.qmd`](index.qmd)
- **Styles:** [`styles.css`](styles.css)
- **Site config:** [`_quarto.yml`](_quarto.yml)
- **Images:** [`resources/images/`](resources/images/) — headshot (`profile.png`), on-stage (`standup.png`)

Local preview:

```sh
quarto render
# open docs/index.html
```

## Publish on GitHub Pages

1. Push to **`main`** (or `staging`). The **Render all** workflow builds the site into **`docs/`**.
2. In the repo on GitHub: **Settings → Pages → Build and deployment**
   - **Branch:** `main`
   - **Folder:** `/docs`
3. **Custom domain:** [`CNAME`](CNAME) is set to `candyscomedy.com` and copied into `docs/` on render. In **Pages**, enter the same custom domain and turn on **Enforce HTTPS** after DNS validates.
4. **DNS** (at your registrar): point the apex and/or `www` to GitHub Pages per [GitHub’s custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## Automation secrets

If the render workflow cannot push commits, add a `repo`-scoped **Personal Access Token** as repository secret `GH_PAT` (see OTTR docs).

## License

See [`LICENSE`](LICENSE).
