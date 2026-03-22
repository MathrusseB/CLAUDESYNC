# KIN ARCHITECTURE
**Last Updated:** March 22, 2026

## The Six Sources
1. **Source 1:** Dedicated client articles on THEIR domain (maintenance agreement)
2. **Source 2:** Central JSON feed at kleosdesign.com/insights/feed.json — ✅ LIVE
3. **Source 3:** Cross-links between same-vertical clients — ✅ OPERATIONAL (AA ↔ TFP)
4. **Source 4:** KIN Broadcast — biweekly industry analysis (needs 3+ nodes/vertical)
5. **Source 5:** KIN Quarterly — synthesizes 6 broadcasts
6. **Source 6:** KIN Year in Review — annual authority piece

## Feed Schema (LOCKED — Rule 035)
```json
{
  "title": "",
  "tag": "",
  "tags": [],
  "excerpt": "",
  "date": "",
  "slug": "",
  "author": "",
  "url": ""
}
```

## Three-Tier Client Feed Fallback
1. Fetch central feed (kleosdesign.com/insights/feed.json) filtered by tag
2. Fall back to local blog.json
3. Fall back to embedded seed array in JavaScript

All failures silent. When central feed is live, client sites auto-connect with zero code changes.

## Current Feed Contents
- 5 Private Service articles (URLs → Insights hub)
- 5 Firearms/Tactical articles (URLs → AA Railway)
- 5 Security articles (URLs → "#" — full pages NOT WRITTEN)

## Active Verticals
| Vertical | Tag | Nodes | Status |
|----------|-----|-------|--------|
| Firearms/Tactical | tactical | 1 (AA) | Active |
| Security | security | 1 (TFP) | Active |
| Food & Bev | food-beverage | 1 (CG) | Active |
| Private Service | private-service | 0 | Pipeline (PSG) |

## Content Flywheel
```
Source 1 builds client authority → Source 2 auto-populates blogs → Source 3 cross-links build network authority → Source 4 harvests breadcrumbs into analysis → Source 5 quarterly synthesis → Source 6 annual → trade publication citations → inbound clients
```
