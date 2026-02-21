# Pregnancy & Birth Guide — PWA

An evidence-based, fully offline-capable Progressive Web App (PWA) for pregnant patients. Covers prenatal visits, labor & delivery, postpartum recovery, newborn care, FAQ, and personal contact storage.

## Features

- ✅ **Works 100% offline** — Service worker caches everything after first load
- ✅ **Installable to home screen** — iOS and Android
- ✅ **Full-text search** across all content
- ✅ **Tap-to-call and tap-to-text** saved care team contacts
- ✅ **Persistent contact storage** — saved to the device, no server needed
- ✅ **High school reading level** — plain language, evidence-based (ACOG guidelines)
- ✅ **No ads, no tracking, no data collection**

## Files

```
index.html      ← The entire app
manifest.json   ← PWA metadata (name, icons, theme color)
sw.js           ← Service worker (offline caching)
README.md       ← This file
```

## Deploy to GitHub Pages (3 minutes)

1. Create a new GitHub repository (can be public or private)
2. Upload these three files: `index.html`, `manifest.json`, `sw.js`
3. In the repo, go to **Settings → Pages**
4. Under **Source**, select **Deploy from a branch**, choose `main`, folder `/ (root)`
5. Click **Save**
6. Your app will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

That's it. Share the URL with your patients.

## iOS Install Instructions (for patients)

1. Open the link in **Safari** (must be Safari on iPhone)
2. Tap the **Share** button (box with arrow)
3. Scroll down and tap **Add to Home Screen**
4. Tap **Add**

The app will now appear on the home screen and work completely offline.

## Android Install Instructions (for patients)

1. Open the link in **Chrome**
2. Tap the three-dot menu (⋮)
3. Tap **Add to Home Screen** or **Install App**
4. Tap **Install**

## Updating Content

All content is inside `index.html` in the `CONTENT` JavaScript object (around line 400). Each topic has:
- `id` — unique identifier
- `title` — displayed in the card header
- `sub` — subtitle
- `body` — HTML content of the accordion panel

After editing, increment the cache version in `sw.js` (`const CACHE_NAME = 'birth-guide-v2'`) so patients get the updated version.

## Customization Ideas

- Add your practice name and logo to the header
- Add a "Prepared by [Your Practice]" footer
- Pre-fill your office phone number in the My Info section
- Add a link to your patient portal
- Translate to Spanish (the content structure makes this straightforward)

## Evidence Base

Content is based on:
- ACOG (American College of Obstetricians and Gynecologists) clinical guidance
- AAP (American Academy of Pediatrics) safe sleep and newborn care guidelines
- WHO delayed cord clamping and first bath recommendations
- Published evidence on epidurals, VBAC, and induction of labor

---

*This app provides general health education. It is not a substitute for individualized medical advice from a licensed provider.*
