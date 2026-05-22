# Root Crate · getrootcrate.com

The marketing landing page for [Root Crate](https://getrootcrate.com), curators of cultural boxes from countries around the world. Our first box celebrates Pakistan.

## Stack

A static HTML site. No build step, no framework, no dependencies (Google Fonts is loaded from a CDN). Everything renders directly from the files in this repo.

## Local preview

Open `index.html` directly in a browser, or run any static server from this folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deployment: Cloudflare Pages

1. Push this repo to GitHub.
2. In Cloudflare Pages, click **Create a project** and connect this repo.
3. **Framework preset:** None
4. **Build command:** _(leave empty)_
5. **Build output directory:** `/`
6. Click **Save and Deploy**. The first deploy takes about a minute.
7. In the Pages project settings, bind the custom domain `getrootcrate.com`.

`_headers` sets sensible security and caching defaults that Cloudflare picks up automatically.

## Repo layout

```
.
├── index.html         The landing page (all content and styles are inline)
├── 404.html           Fallback page for unknown paths
├── _headers           Cloudflare Pages header rules (security + caching)
├── robots.txt         Crawler hints
├── sitemap.xml        Site map for search engines
├── README.md          You are here
├── .gitignore         Excludes uploads/, OS junk, editor files
└── img/               All web-ready imagery
    ├── crate-closed.jpg   Hero shot of the closed box
    ├── crate-flatlay.jpg  Reveal shot (also the social-share image)
    ├── rooh-afza.jpg
    ├── nimco.jpg
    ├── chili-mili.jpg
    ├── sooper.jpg
    ├── pakola.jpg
    ├── logo-mark.png        Header/footer logo
    ├── logo-mark-large.png  Apple touch icon (home-screen save)
    └── favicon-128.png      Browser tab icon
```

## Editing content

All copy lives in plain text inside `index.html`. Search for the section comments (e.g. `<!-- ===== STORY ===== -->`) to find what you want to change.

If you swap a product photo, drop the new file into `img/` with the same name and refresh.
