# CT Linked Content Gallery · Field Guide 06

A single-file interactive field guide for CleverTap Linked Content and Custom KVP:
120 send-time personalization plays across 15 verticals, with channel-true mockups,
a developer setup docs tab, and a 3D sphere cover built from the gallery's own renders.

**Live URL after deploy:** https://shijunneo-bot.github.io/ct-linked-content-gallery/

## What's inside (one file, no dependencies)
- Sphere cover intro (16 real mockup tiles, hover to pause and inspect, tap or Enter to open)
- 120 use-case cards, 8 per vertical, emoji-hinted titles, deliverability stamps
- Vertical index cards with live counts, collapsible sticky filters, API-family filters (15+ each)
- Channel-true modals: lockscreen push, full email with product cards, SMS and WhatsApp frames, web push, webhook ops card
- Developer Setup Docs tab: Linked Content setup, Catalog STP, Campaign ID, Recommendations, the External Trigger stack, 12 Liquid hacks, TAM talking points per section
- Living gradient wordmark, film grain, aurora background; full keyboard support, WCAG-checked contrast, reduced-motion safe, mobile bottom-sheet modals

## Deploy (GitHub web UI, ~2 minutes)
1. github.com → New repository → name: `ct-linked-content-gallery` → Public → Create
2. "uploading an existing file" → drop `index.html` → Commit to `main`
3. Settings → Pages → Source: Deploy from a branch → Branch: `main`, folder `/ (root)` → Save
4. Wait ~1 minute; the site is live at the URL above.

## Deploy (git CLI)
```bash
git init ct-linked-content-gallery && cd ct-linked-content-gallery
cp /path/to/index.html .
git add index.html && git commit -m "FG06: Linked Content gallery v1"
git branch -M main
git remote add origin git@github.com:shijunneo-bot/ct-linked-content-gallery.git
git push -u origin main
# then enable Pages: Settings → Pages → main / root
```

## Updating later
Replace `index.html` on `main` (web UI: open file → edit/upload → commit). Pages redeploys automatically.

## After deploy
The other five galleries can add this to their family strips as
`06 · Linked Content → https://shijunneo-bot.github.io/ct-linked-content-gallery/`.
