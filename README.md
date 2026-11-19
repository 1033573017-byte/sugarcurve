# SugarCurve — Sugar Control Companion

A sugar-control companion web app built for a health & wellness creator's audience (Douyin, 10,371 followers, anti-aging / sugar-control niche).

**Live v0 is in this repo:** open `index.html` in any browser — no build step, no dependencies.

## What v0 already does
- Meal logging against a starter food database (sugar grams per 100g, 25 common foods)
- Daily sugar total against a 50g/day goal, with on-track / over states
- Estimated post-meal glucose curve chart (canvas, illustrative model — baseline 5.2 mmol/L, GI-speed-weighted peaks)
- Day streaks for staying under goal, persisted in localStorage

## The pitch
My followers ask how to control sugar without giving up real food. SugarCurve answers in one glance per meal: log what you ate, see the sugar load and the curve it likely causes, keep the streak alive. I promote it natively inside my Douyin content — every video on sugar control ends with the tool I actually use.

## What the Devin Bot builds next (scoped slices, one PR each)
1. Full food database (300+ foods, sugar + GI), barcode/photo meal entry
2. Accounts + cloud sync, history and weekly reports
3. Personalized goals (weight, fasting glucose context), reminders before typical snack times
4. PWA packaging for home-screen install, share-card export for social posts

## Architecture
- v0: single-file HTML/CSS/JS, canvas charting, localStorage — deliberately zero-dependency so it runs anywhere
- Product build: TypeScript + Vite PWA, IndexedDB local-first with optional sync, food data as versioned JSON, chart module shared between web and share-card renderer
- Content loop: creator dashboard showing which foods the audience logs most, feeding the next video topics
