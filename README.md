# naveed.dev / naveed.sh

A plain, dependency-free static blog. **Just HTML, CSS, and (optionally) JS** —
no framework, no build step, no `node_modules`. Every page is hand-editable HTML
that GitHub Pages serves directly.

## Structure

```
index.html                     Home page (list of posts)
404.html                       Not-found page
style.css                      All styling (single file)
avatar.png                     Profile photo / favicon
CNAME                          Custom domain for GitHub Pages
.nojekyll                      Tell GitHub Pages not to run Jekyll
robots.txt / sitemap.xml / rss.xml
media/                         Images used by posts
posts/<slug>/index.html        One folder per post  -> /posts/<slug>/
pages/about/index.html         Static pages          -> /pages/about/
category/<name>/index.html     Category index pages  -> /category/<name>/
tag/<name>/index.html          Tag index pages       -> /tag/<name>/
```

The URL layout matches the old Gatsby site (`/posts/<slug>/`, `/pages/about/`,
`/category/<name>/`, `/tag/<name>/`), so existing links keep working.

## Editing

- **Edit a post:** open the relevant `posts/<slug>/index.html` and edit the
  markup inside `<div class="post-body"> … </div>`.
- **Add a post:** copy an existing `posts/<slug>/` folder to a new slug, edit the
  title/date/content, then add a matching `<article class="post-preview">` entry
  near the top of `index.html` (and, if you want, to the relevant category/tag
  pages). That's it — no build to run.
- **Restyle:** everything lives in `style.css`.

## Deployment (GitHub Pages)

Deployment is automatic via `.github/workflows/deploy.yml`: every push to the
default branch uploads this repo to GitHub Pages (no build, just an upload).

One-time setup in the repo's **Settings → Pages**:

1. Set **Source** to **GitHub Actions**.
2. Under **Custom domain**, confirm `www.naveed.dev` (matches the `CNAME` file).

### Pointing both naveed.dev and naveed.sh at the site

GitHub Pages can only have **one** custom domain in `CNAME` (currently
`www.naveed.dev`). Configure DNS at your registrar like this:

**Primary domain — naveed.dev (served by Pages):**

| Record | Host  | Value                                                            |
| ------ | ----- | --------------------------------------------------------------- |
| CNAME  | `www` | `naveedn.github.io`                                             |
| A      | `@`   | `185.199.108.153` `185.199.109.153` `185.199.110.153` `185.199.111.153` |
| AAAA   | `@`   | `2606:50c0:8000::153` `2606:50c0:8001::153` `2606:50c0:8002::153` `2606:50c0:8003::153` |

(The apex `naveed.dev` then redirects to `www.naveed.dev` automatically.)

**Secondary domain — naveed.sh (redirects to naveed.dev):**

GitHub Pages won't serve a second domain, so redirect it at the registrar /
DNS provider. Most registrars (Cloudflare, Namecheap, Porkbun, etc.) offer a
free **URL/redirect record** — point `naveed.sh` and `www.naveed.sh` with a
301 redirect to `https://www.naveed.dev`. If your registrar lacks redirect
records, use a Cloudflare "Redirect Rule" (free) on the naveed.sh zone.

> If you'd rather serve from `naveed.sh` instead, swap the value in `CNAME` and
> flip the DNS roles above.
