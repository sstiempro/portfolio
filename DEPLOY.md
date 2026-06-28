# Portfolio site — status & deploy

## ✅ It's LIVE right now (temporary preview, deployed with no login)
**https://portfolio-tth.voltaic-garden.workers.dev**

This was deployed to a Cloudflare **temporary preview account** (`wrangler deploy --temporary`) — no credentials needed. Both the main page and `case-studies/adisa.html` are verified rendering.

## To make it permanent on **portfolio.sstiem.com**
The site is built, deployed, and verified. The only remaining step touches *your Cloudflare account* — which, for security, only you can authenticate. Two ways:

### Option A — Claim the live deploy (fastest, ~60-min window)
Open the **claim URL** from the deploy output (expires 60 min after deploy) → log into your Cloudflare account → the Worker `portfolio-tth` moves under your account permanently. Then: Workers & Pages → `portfolio-tth` → **Settings → Domains & Routes → Add → Custom domain** → `portfolio.sstiem.com`. *(If the window lapsed, just use Option B — I can redeploy instantly.)*

### Option B — You log in once, I finish it
```
cd ~/Developer/job-search/portfolio-site
npx wrangler login        # one browser click on YOUR account
```
Then tell me **"logged in"** and I'll run the deploy to your account and wire up `portfolio.sstiem.com` for you. (`.assetsignore` already excludes the config/docs so only the site ships.)

## To edit & redeploy
Edit `index.html` / `case-studies/adisa.html`, then re-run the deploy command. Tell me any change and I'll do it.
