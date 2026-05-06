# talkimal-site

Static landing + legal pages for **Talkimal** (https://talkimal.com).

## Structure

```
talkimal-site/
├── index.html       Landing
├── privacy.html     Privacy Policy
├── terms.html       Terms of Service
├── support.html     Support / FAQ
├── style.css        Shared styles
├── _redirects       Clean-URL rewrites for Cloudflare Pages
└── README.md
```

## Deploy (Cloudflare Pages)

1. Connect this repo to a new Cloudflare Pages project.
2. Build settings:
   - Framework preset: **None**
   - Build command: (leave empty)
   - Build output directory: `/`
3. Add custom domain: `talkimal.com` (Cloudflare auto-creates DNS records).
4. Push to `main` to deploy.

## Update

Edit the relevant `.html` and `git push`. Cloudflare Pages redeploys automatically on every commit.

Source-of-truth markdown for legal text lives in `../docs/legal/` of the parent project. When changing legal content, update both the markdown and the HTML.

## Local preview

```bash
python3 -m http.server 8000
# open http://localhost:8000
```
