# Deploying to GitHub Pages

1. Use your PERSONAL GitHub account (not the work one). Create a public repo named
   `<username>.github.io` (gives you https://<username>.github.io with no extra config).
2. GitHub and LinkedIn links are set. A public email button was left off for now; add
   `<a class="btn" href="mailto:...">Email</a>` in the Contact section when ready.
3. Add `assets/photo.jpg` (square, ~600px).
4. From this folder:
   ```
   git init -b main
   git add .
   git commit -m "Initial site"
   git remote add origin https://github.com/<username>/<username>.github.io.git
   git push -u origin main
   ```
5. Repo Settings > Pages > Deploy from branch > `main` / root. Live in ~1 minute.

## Custom domain (optional)
- Keep the domain: transfer it OUT of WordPress.com to a registrar (Cloudflare, Porkbun,
  Namecheap, about $10-15/yr), cancel the WordPress plan afterward.
- Add a file named `CNAME` containing just the domain, then at the registrar add four A
  records for the apex (185.199.108.153, .109.153, .110.153, .111.153) and a CNAME
  `www` -> `<username>.github.io`. Tick "Enforce HTTPS" in Pages settings.
- Or let it go: the free github.io URL works fine.
- Before cancelling WordPress, export your content (Tools > Export) and check the
  domain's renewal/transfer lock status.
