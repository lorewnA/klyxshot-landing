# Klyxshot Landing

Static landing page for klyxshot.com. Pure HTML/CSS, no build step.

## Deploy on Vercel (free, 5 min)

1. **Sign up:** https://vercel.com (Login with GitHub).

2. **Push this folder to a GitHub repo:**
   ```bash
   cd klyxshot-landing
   git init
   git add .
   git commit -m "Landing page"
   gh repo create klyxshot-landing --public --source=. --push
   ```
   Or create manually on github.com and push.

3. **Import to Vercel:**
   - Vercel dashboard → "Add New" → Project
   - Import the `klyxshot-landing` repo
   - Framework preset: **Other**
   - Root directory: leave empty
   - Build & Output: leave empty (Vercel auto-detects static)
   - Click Deploy

4. **Connect domain klyxshot.com:**
   - Vercel project → Settings → Domains → Add `klyxshot.com`
   - Vercel will give you DNS records to add
   - Go to Cloudflare DNS for klyxshot.com and add the records they show
   - Wait ~5 min for DNS to propagate
   - Done

## Pages

| URL | File |
|---|---|
| `/` | `index.html` — main landing |
| `/download` | `download.html` — download page |
| `/privacy` | `privacy.html` — GDPR privacy policy |
| `/terms` | `terms.html` — terms of service |

## What to update later

- **Download link** in `download.html` — currently points to a placeholder GitHub release URL. Replace with your actual `Klyxshot-Setup.exe` URL once you have a build.
- **Pricing checkout URL** in `index.html` — already wired to your Lemon Squeezy URL.
- **Email** `support@klyxshot.com` — make sure Cloudflare Email Routing is set up for this address.

## Local preview

Just open `index.html` in a browser — no server needed.
Or `python3 -m http.server 8080` for localhost preview.
