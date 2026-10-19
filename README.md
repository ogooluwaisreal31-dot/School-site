# School website template
Static HTML/CSS/JS. No build step. Works on sample content until Supabase is connected.

## Run locally
`python3 -m http.server 8000` then open http://localhost:8000

## Publish on GitHub Pages
1. Create an empty repo on github.com (no README).
2. In a terminal in this folder: `git init`, `git add .`, `git commit -m "School site"`, `git branch -M main`, `git remote add origin <repo-url>`, `git push -u origin main`.
3. Repo > Settings > Pages > Source: "Deploy from a branch", Branch: main, Folder: / (root) > Save.
4. After a minute the site is live at https://<username>.github.io/<repo>/
5. Custom domain: Settings > Pages > Custom domain, then add the DNS records GitHub shows; tick "Enforce HTTPS" when available.
6. Replace YOUR-DOMAIN in `sitemap.xml` and `robots.txt` with the real domain.

## Customise a school
Edit `assets/js/config.js`: name, colours, `fontPreset` (modern, classic, friendly, formal, clean), contact, sections and content.

## Later: Supabase (not required to publish)
Run `supabase/migrations/001_schema.sql`, `002_editable_extras.sql`, `supabase/seed.sql`, then fill `assets/js/supabase-config.js` (anon key only, never service_role). `supabase/tests.sql` has security checks.
