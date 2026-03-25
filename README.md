# Nanusense Discover

A Netflix-style content discovery page for [nanusense.com](https://nanusense.com).

Live at: **discover.nanusense.com**

## What it is

Single-page static site that fetches all posts from the Nanusense WordPress REST API and presents them as:
- A rotating hero banner (Featured posts)
- Netflix-style horizontal category rows with featured images
- A shuffle button per category that opens a full reading modal
- Light / dark theme toggle

## Deploy

This is a single static HTML file. Vercel serves it automatically with zero config.

1. Push to GitHub
2. Import repo in [vercel.com](https://vercel.com)
3. Add custom domain `discover.nanusense.com`
4. Add DNS record at your registrar:
   ```
   Type:  CNAME
   Name:  discover
   Value: cname.vercel-dns.com
   ```

## Update content

Content is fetched live from the WordPress API on every page load — no rebuild needed when new posts are published.

To update the UI, edit `index.html` and push to main. Vercel deploys in ~30 seconds.

## Files

```
index.html    ← the entire app (HTML + CSS + JS)
vercel.json   ← cache + security headers
```
