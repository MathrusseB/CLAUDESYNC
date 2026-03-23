# CHANGELOG
**Most recent first. Each entry: date, what changed, which pages affected.**

---

## March 22, 2026 (TFP Session — Evening)
- TFP website V2 fully redesigned and deployed to Railway (taskforceprotection-production.up.railway.app)
- Aventura-inspired cinematic scroll redesign launched with real client data
- Five visual patches applied post-launch: spacing, typography weight, section transitions, visual consistency
- Bo's Spartan helmet logo integrated across nav, hero, print overlay, and favicon
- Logo bible entry created documenting tfp-logo-pdf4.png (1635×2037px) and usage locations
- Chrome Claude audit initiated: Pass 1 (Aventura scroll inventory) complete, Pass 2 in progress
- Video hosting solution identified: Cloudflare R2 via MCP for hero video integration
- Sidearm photo saved in build/hero_photo_old.txt for future second photo break section
- Pages affected: kleos/clients.md, changelog.md

## March 22, 2026 (PSO Session)
- Supabase startup queries reduced from 7,503 to 5 (lazy loading architecture)
- 1,204 waterfowl harvest records imported from 3 seasons of spreadsheet data
- Chart.js integrated via CDN with MRChart wrapper component
- Guest Reporting overlay built with season filtering, harvest summary bars, chart context switching
- Season definition standardized: April 1 - March 31, displayed as "YYYY-YY", getSeasonLabel() utility
- Outfitting Log: read-only protection on waterfowl historical records, independent scroll areas, entry reset
- Custom Report scroll bug architecturally fixed (state lifted, scroll uses refs not useState)
- Room names cleaned up (Building + Number only)
- Guest Log renamed from Room Assignments
- Login screen updated with Blue Maple Ranch logo, "Designed by Kleos." positioning
- Daily Visit Diary spec document completed (8 pages, 3 new Supabase tables designed)
- CC instruction doc created for outfitting log redesign + audit fixes (12 items, not yet executed)
- Memory rule added: always prioritize accuracy over speed, never guess
- Pages affected: This would be a new page — suggest creating pso/status.md

## March 22, 2026 (Evening)
- **CLAUDESYNC knowledge base launched and verified live**
- **Instructions distributed to all projects**
- **Rules 039-041 added** (CLAUDESYNC operations, CC-only updates, no slash branches)
- No revenue changes
- Pages affected: changelog.md, rules.md

## March 22, 2026
- **Corporate structure finalized.** RanchRock Holdings LLC chosen as holding company name. Operating agreement drafted with d/b/a provisions for Calamityville and Kleos. IP assignment covers all projects including speaking materials.
- **Calamityville concept pivoted.** Expanded from crime-only to all historical events (disasters, scandals, tragedies). Name changed from MurderHouse GO! to Calamityville. Dual-mode gameplay: Discovery (remote) + Explorer (physical visit). Historical events only (decades old minimum) to solve player safety.
- **Monetization strategy expanded.** Premium content tiers, sponsored locations, media licensing, educational licensing, merchandise, advertising.
- **CLAUDESYNC knowledge base created.** Replaces the Holy Text as the primary context delivery method for Claude instances. Holy Text continues as archive.
- Pages affected: ALL (initial population)

## March 20, 2026
- **KIN central feed deployed.** kleosdesign.com/insights/feed.json live. CORS resolved via _headers file. Source 2 operational. Source 3 cross-links active between AA and TFP.
- **TFP V2 mockup approved.** Aventura-inspired redesign. CC build attempted, stalled on file I/O. Rules 028/029 established for large file builds.
- Pages affected: kleos/status.md, kleos/kin.md

## March 19, 2026
- **Allegiance Armory content-complete.** Cale's questionnaire processed, 5 blog articles live, lightbox built, mobile nav fixed, ambient canvas working. In client review.
- **Task Force Protection built.** Full site, blog infrastructure, KIN integration. Email sent to Bo at $4,000.
- **Common Ground Coffee KIN-integrated.** Mobile fixes, blog infrastructure, 3 seed articles. Live on Railway.
- Pages affected: kleos/clients.md, kleos/kin.md, revenue.md
