# CleverTap Field Guides — Deploy Pack

Two things in this pack:
1. **index.html** — the fully upgraded Linked Content gallery (Field Guide 06)
2. **suite-index.html** — a landing hub that links all 10 galleries

## 1. Deploy the updated Linked Content gallery
Repo: `ct-linked-content-gallery` → https://shijunneo-bot.github.io/ct-linked-content-gallery/
- Open the repo → replace `index.html` on `main` with the one in this pack (upload → commit).
- Pages redeploys automatically in ~1 minute.

What changed in this version (world-class UAT pass):
- **SEO:** meta description, keywords, canonical, Open Graph + Twitter cards, JSON-LD WebApplication schema.
- **AEO (AI search):** a semantic content summary crawlers and AI engines can read (the cards are JS-rendered, so bots previously saw almost nothing).
- **Performance:** Google Fonts moved from render-blocking `@import` to preconnect + non-blocking load (better LCP/Core Web Vitals).
- **Light + dark mode:** a theme toggle (bottom-right), remembered per visitor, both themes WCAG AA on every text token. No flash on load.
- **Family strip:** now links all 10 live galleries.
- **Favicon:** official CleverTap mark (embedded, so it travels with the file).

## 2. Deploy the suite landing hub (optional but recommended)
Pick ONE approach:

**Option A — a dedicated repo (cleanest URL):**
- New repo `ct-field-guides` → upload `suite-index.html`, rename it to `index.html` → enable Pages.
- Lives at https://shijunneo-bot.github.io/ct-field-guides/

**Option B — add to an existing repo:**
- Drop `suite-index.html` into any gallery repo; it's reachable at `.../suite-index.html`.

## 3. Favicon consistency across ALL galleries (one-time task)
You asked that every gallery use the same CleverTap icon. The favicon is one line in each `index.html` `<head>`. In each of the other repos, ensure this line is present (replace any existing `<link rel="icon">`):

```html
<link rel="icon" type="image/png" href="https://docs.clevertap.com/favicon.ico">
<meta name="theme-color" content="#0B0D1C">
```

(Using CleverTap's hosted favicon URL keeps every gallery identical and is the simplest one-line edit. The Linked Content gallery in this pack embeds the same icon as base64 so it works even offline — either approach shows the same mark.)

Repos to update: amp-email-gallery · rich-push-gallery · ct-sms-field-guide · whatsapp-addon-gallery · ct-template-gallery · ct-recommendations-gallery · ct-geofencing-gallery · ct-reminders-gallery · ct-promos-gallery

## Notes
- Both files are self-contained (no build step, no dependencies beyond Google Fonts).
- The gallery is one ~510KB HTML file with all 120 examples, mockups, and setup recipes embedded.
