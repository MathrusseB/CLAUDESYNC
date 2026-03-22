# CALAMITYVILLE — PROTOTYPE SPEC
**Last Updated:** March 22, 2026

## What We're Building
Browser-based interactive prototype. React app, map-based (no AR), single-player, demonstrates core game loop with real historical event data. $0 cost. Runs in any browser.

## Data Strategy
- **Prototype:** Curated dataset of 50–100 famous historical events, hand-researched with locations, dates, descriptions, story hooks
- **Production (later):** City open data portals (Chicago Socrata API), CrimeoMeter API, FBI Crime Data Explorer, plus curated historical database
- Content is the moat — every token is editorially curated

## Tech Stack
- **Frontend:** React (Vite), Leaflet.js + OpenStreetMap (free) or Mapbox GL JS
- **Styling:** Tailwind CSS
- **Animations:** Framer Motion
- **Data:** Client-side fetch from curated JSON dataset, no backend needed
- **Hosting:** Vercel or Netlify (free)
- **Cost:** $0–$15 (domain only)

## Build Sessions
1. **Data Pipeline:** Curate 50–100 historical events, build token transform (type mapping, rarity, points, buffer zone offsets)
2. **Map + Tokens:** React app, map rendering, custom token markers by rarity, clustering, player position, detection radius
3. **Collection Mechanics:** Token state machine (locked→available→collected), detail card, collection animation, inventory, scoring
4. **Game Layer + Polish:** Weekly theme system, simulated leaderboard, event timer, home screen, mobile-responsive, dark mode map

## Success Criteria
- Opens in browser, tokens on real map
- Tokens color-coded by rarity
- Moving player pin makes nearby tokens collectible
- Collecting shows detail card with event info + adds to score
- Weekly theme filter changes visible tokens
- Simulated leaderboard shows player position
- Loads in <3 seconds
- Feels like a game, not a data dashboard
