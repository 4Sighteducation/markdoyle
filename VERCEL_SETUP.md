# Vercel Deployment & CMS Setup (MarkDoyle.me)

## Part 1 — Deploy to Vercel

1. Import the repo `4Sighteducation/markdoyle` into Vercel
2. Framework preset should auto-detect **Astro**
3. Build command: `npm run build`
4. Output directory: `dist`

## Part 2 — Set up Decap CMS login (Netlify Identity + Git Gateway)

This site is hosted on **Vercel**, but editor login is handled by a small **Netlify** site.

1. Create a new Netlify site (can be any placeholder site)
2. Netlify → **Identity**:
   - Enable Identity
   - Registration: **Invite only**
3. Netlify → **Identity → Services → Git Gateway**:
   - Enable Git Gateway
   - If prompted, add a GitHub token that can write to `4Sighteducation/markdoyle`
4. Update these two files with your Netlify site URL:
   - `public/admin/config.yml` → `identity_url`, `gateway_url`
   - `public/admin/index.html` → `NETLIFY_IDENTITY_API_URL`
   - `public/admin/invite.html` → `NETLIFY_IDENTITY_API_URL`

## Part 3 — Connect domain `markdoyle.me`

1. In Vercel project → Settings → Domains
2. Add `markdoyle.me` (and optionally `www.markdoyle.me`)
3. Follow Vercel’s DNS instructions in your registrar

## Printing

The homepage includes a **Print / Save as PDF** button.
The CSS uses `@page` + `@media print` so the printed output matches the on-screen A4-like layout.

