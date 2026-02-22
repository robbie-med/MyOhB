# Pregnancy & Birth Guide — PWA

An evidence-based, fully offline-capable Progressive Web App for pregnant patients. Covers prenatal visits, labor & delivery, postpartum recovery, newborn care, FAQ, and 10 interactive clinical tools — all stored privately on the patient's device.

## Features

- **Works 100% offline** — service worker caches everything after first load
- **Installable** — iOS and Android home screen
- **10 interactive tools** — kick counter, contraction timer, feeding log, diaper log, jaundice tracker, blood pressure log, weight tracker, mood check-in (EPDS), birth plan builder, visit notes
- **Dark mode** — respects system preference, user-toggleable
- **Full-text search** across all content
- **Data export** — download all your data as a JSON file
- **Print-ready birth plan** — clean layout for printing or saving as PDF
- **Tap-to-call / tap-to-text** saved care team contacts
- **No ads, no tracking, no data collection** — everything stays on the device

## File Structure

```
index.html      HTML shell — all pages and modals, no inline JS or CSS
styles.css      All styles, including tool UI and dark mode
content.js      Guide content, navigation, search, My Info, PWA logic
tools.js        All 10 interactive tools
sw.js           Service worker (offline caching, cache-first strategy)
manifest.json   PWA metadata (name, icons, theme color)
README.md       This file
```

To update content, edit `content.js` (the `CONTENT` object at the top).
After any change, bump the cache version in `sw.js` (`CACHE_NAME = 'birth-guide-v3'` etc.) so users get the update.

## Deploy to GitHub Pages

1. Push all files to a GitHub repository
2. Go to **Settings → Pages**
3. Source: **Deploy from a branch**, branch `main`, folder `/ (root)`
4. Save — live in ~2 minutes at `https://YOUR-USERNAME.github.io/YOUR-REPO/`

## iOS Install (share with patients)

1. Open the link in **Safari**
2. Tap the Share button → **Add to Home Screen**
3. Tap **Add**

## Android Install

1. Open in **Chrome**
2. Tap ⋮ → **Add to Home Screen** or **Install App**

## Interactive Tools

| Tool | Purpose |
|---|---|
| Kick Counter | Sessions, 10-in-2-hour goal, history |
| Contraction Timer | 5-1-1 detection, "time to go in" alert |
| Feeding Log | Breast/bottle, 24-hr count, flags <8/day |
| Diaper Log | Wet and dirty counts by day |
| Jaundice Tracker | Birth-date-based day-by-day guidance |
| Blood Pressure Log | Flags ≥140/90, color-coded history |
| Weight Tracker | IOM guidelines by pre-pregnancy BMI |
| Mood Check-In | Edinburgh Postnatal Depression Scale (EPDS) |
| Birth Plan Builder | Guided choices, multi-select, notes, copy/print |
| Visit Notes | Pre-visit questions and post-visit notes |

## Evidence Base

- ACOG clinical guidance (prenatal care, labor, postpartum)
- AAP safe sleep and newborn care guidelines
- WHO recommendations (delayed cord clamping, first bath timing)
- Published evidence on epidurals, VBAC, and labor induction

---

*This app provides general health education and is not a substitute for individualized medical advice.*
