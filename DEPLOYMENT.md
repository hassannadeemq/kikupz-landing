# Kikupz Landing Page — Deployment Guide

## Files

- **index.html** — Main landing page (fully self-contained, no build step needed)
- **assets/** — Images and icons (all linked from index.html)
- **netlify.toml** — Netlify configuration

## Deploy to Netlify

### Option 1: Drag & Drop (Quickest)
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag this entire folder onto the Netlify drop zone
3. Done — your site is live

### Option 2: Git + Auto-Deploy
1. Push this folder to a GitHub repo
2. In Netlify, connect the repo
3. Set publish directory to `.` (the root)
4. Netlify auto-deploys on every push

### Option 3: Netlify CLI
```bash
npm install -g netlify-cli
netlify deploy --prod
```

## Testing Locally

```bash
# Python 3
python3 -m http.server 8000

# Or Node
npx http-server
```

Then visit `http://localhost:8000`

## Key Points

- All images are in the `assets/` folder — make sure it's included in deployment
- All CSS is inline (no external stylesheets)
- Google Fonts load from CDN (no build step)
- All CTA buttons link to `https://kikupz.glide.page`
- The page is fully responsive (mobile, tablet, desktop)

## Updating Content

Edit `index.html` directly:
- Change app URL: search for `https://kikupz.glide.page` and replace
- Change copy: edit text in the HTML sections
- Change colors: edit hex values in the `<style>` block
- Change images: replace files in `assets/` folder and update `src` attributes

No build step needed — changes are live immediately after pushing.
