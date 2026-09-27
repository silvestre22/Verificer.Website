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
