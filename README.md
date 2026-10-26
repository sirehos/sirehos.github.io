# SirehOS Lite — Homepage v0.2

Static, dependency-free landing page for `sirehos.org`.

## Local preview
Open `index.html` in a browser.

## Publish on GitHub Pages
1. Create a GitHub organization `sirehos` (if available).
2. Create a **public** repository named `sirehos.github.io` in that organization.
3. Upload `index.html` and the entire `assets/` folder to the repository root.
4. Repository **Settings → Pages → Build and deployment → Deploy from a branch**, select `main` and `/ (root)`, then save.
5. Wait until the site works at `https://sirehos.github.io`.
6. In Pages settings set **Custom domain** to `sirehos.org`, then save. GitHub may create the CNAME file automatically; keep it committed.
7. At Porkbun DNS for `sirehos.org`, remove conflicting A/AAAA/ALIAS records for the root and add the four GitHub Pages A records:
   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153
   Each uses Host blank or `@` (as Porkbun accepts), Type A.
8. Optional `www`: CNAME `www` → `sirehos.github.io` (not `sirehos.org`).
9. Allow DNS/HTTPS provisioning time; verify `https://sirehos.org`, then enable **Enforce HTTPS** in GitHub Pages settings when available.

If you choose a different GitHub owner/repository, substitute its actual Pages hostname. Avoid wildcard DNS records; never remove MX/TXT records used by email. Keep domain registration at Porkbun; no transfer required.

## Contents
- `index.html` — complete responsive page
- `assets/sirehos-emblem.webp` — approved provisional emblem, optimized for web
- `assets/favicon.svg` — simple leaf favicon

The site accurately labels capabilities as *planned* and does not claim a release is available.
