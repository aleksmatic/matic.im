
# matic.im — static site

This repo contains a ultra‑light, accessible static site with two pages:
- `/index.html` (About Me)
- `/publications.html`

## How to deploy (pick one)

### A) GitHub Pages (free, simple)

1. Create a new repo, e.g., `matic.im`. Upload all files from this folder.
2. In repo Settings → Pages → set **Source** to `Deploy from a branch`, branch `main`, folder `/root` (or use `GitHub Actions`).
3. Add a file named `CNAME` in the repo root with a single line: `matic.im` (already included here).
4. In your domain DNS (registrar), set:
   - **A** records for apex `matic.im` to: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
   - **CNAME** for `www` → `<your-username>.github.io`.
5. Wait a bit, then in GitHub Pages, enable HTTPS. Make sure both apex and `www` resolve before certificate is issued.

### B) Netlify (free, drag‑and‑drop)

1. Drag this folder into Netlify app, or connect the repo.
2. In **Domain management**, add `matic.im`.
3. Either use **Netlify DNS** (switch nameservers) or keep your registrar and set:
   - **ALIAS/ANAME** (preferred) for apex `matic.im` → `apex-loadbalancer.netlify.com`, or fallback **A** to `75.2.60.5`.
   - **CNAME** for `www` → your Netlify subdomain.
4. Netlify will provision HTTPS automatically when DNS is correct.

## Customize

- Put your headshot at `/assets/profile.jpg` (create the folder).
- Update email, links, and add more publications as `<li>` items.
- Styles live in `styles.css`. No JS, no frameworks.

