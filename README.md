# jessrudder.com

Plain HTML/CSS academic site hosted on GitHub Pages. No build step, no Jekyll.

## Files
```
index.html              <- all page content (edit this)
assets/css/style.css    <- colors, fonts, layout (colors are at the top)
assets/img/rudder.jpg   <- your headshot (add it)
assets/pdf/Rudder_CV.pdf <- your CV (add it; same name = link always works)
CNAME                   <- tells GitHub Pages to serve jessrudder.com
```

## 1. Put it on GitHub
1. Create a new **public** repo named `jessrudder.github.io` (or any name).
2. Upload everything in this folder (Add file → Upload files), keeping the folder structure.
3. Add your photo as `assets/img/rudder.jpg` and CV as `assets/pdf/Rudder_CV.pdf`.
4. Repo **Settings → Pages** → Source: *Deploy from a branch* → `main` / `(root)` → Save.
   The site appears at `https://<username>.github.io` within a minute or two.

## 2. Point jessrudder.com at GitHub (instead of Google Sites)
At your domain registrar (Google Domains moved to Squarespace — check there), edit DNS:

| Type  | Host | Value |
|-------|------|-------|
| A     | @    | 185.199.108.153 |
| A     | @    | 185.199.109.153 |
| A     | @    | 185.199.110.153 |
| A     | @    | 185.199.111.153 |
| CNAME | www  | `<username>.github.io` |

Delete the old records pointing to Google Sites (usually a `CNAME www → ghs.googlehosted.com`).
Then in **Settings → Pages**, enter `jessrudder.com` as the custom domain and tick **Enforce HTTPS**
once it's available (DNS can take up to a day). Also remove the custom URL from Google Sites settings.

## 3. Updating
- New paper: copy a `<div class="paper"> ... </div>` block in `index.html` and edit.
- New CV: upload a file with the same name, `Rudder_CV.pdf`, overwriting the old one.
- Edit on github.com directly (pencil icon) — changes go live in ~1 minute.
