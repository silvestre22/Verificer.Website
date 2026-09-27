# Verificer website (static, for GitHub Pages)

A static rebuild of verificer.com. No build step: plain HTML, CSS and a small script.

## Files
```
index.html                     home page
privacy/index.html             Privacy Policy   (keeps the old /privacy URL)
terms-of-service/index.html    Terms of Service (keeps the old /terms-of-service URL)
assets/css/styles.css          all styles; colours and fonts are tokens at the top
assets/js/main.js              header, mobile menu, scroll reveal
assets/img/                    logos, client logos, team photo, cloud partner logos
assets/images/                 Unsplash photos, saved locally (named by photo ID)
CNAME                          custom domain (verificer.com)
.nojekyll                      tells GitHub Pages to serve files as they are
```

All links are relative, so the site works both on the custom domain and at
`username.github.io/repo/` before the domain is connected.

## Publish to GitHub Pages
1. Move the contents of this `docs/` folder into the repository you will publish from
   (or keep it here and publish this repo's `docs/` folder).
2. Repository **Settings → Pages → Build and deployment**: Source "Deploy from a branch",
   pick the branch and the folder (`/docs` here, or `/ (root)` if you moved the files).
3. Under **Custom domain** enter `verificer.com`, then point the domain's DNS at GitHub Pages
   (A records to 185.199.108.153, .109.153, .110.153, .111.153, or a CNAME for `www`).
4. Tick **Enforce HTTPS** once the certificate is issued.

GitHub Pages on a private repository needs a paid GitHub plan; a public repository works on the free plan.

## Editing content
- Contact details are in the `#contact` section of `index.html`.
- The carbon project summary is in the `#carbon` section.
- Client logos: add the file to `assets/img/clients/` and a `<li>` in the `logo-wall` list.

## Photos
Photos are free to use under the Unsplash License (unsplash.com/license). They are saved in
`assets/images/` as `photo-<ID>.jpg` (1600px wide), so the site does not depend on Unsplash's servers.To use your own photo, save it in `assets/images/` and change that image's `src="..."` in `index.html`.
The hero and forest backgrounds are set by `--hero-img` and `--flagship-img` in `assets/css/styles.css`;
those paths are relative to the stylesheet (`../images/...`).

| Where | Unsplash photo ID |
|---|---|
| Hero background (server rack) | 1680992046626-418f7e910589 |
| Forward deployed engineers | 1581091877018-dac6a371d50f |
| Custom AI agents | 1555066931-4365d14bab8c |
| MCP servers (network cables) | 1744868562210-fffb7fa882d9 |
| On-premise LLM (server rack) | 1680992046626-418f7e910589 |
| AI governance (padlock) | 1614064548237-096f735f344f |
| Manufacturing | 1647427060118-4911c9821b82 |
| Banking (KL Twin Towers) | 1508062878650-88b52897f298 |
| Healthcare | 1777269749032-d8d458ae594d |
| Government (Putrajaya) | 1686242143315-a3c9cdc731f5 |
| Logistics | 1578575437130-527eed3abbec |
| Energy | 1508514177221-188b1cf16e9d |
| Carbon flagship (forest aerial) | 1593069567131-53a0614dde1d |
