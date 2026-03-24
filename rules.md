# RANCHROCK RULES
**Last Updated:** March 22, 2026

These rules apply to ALL projects under RanchRock. Every Claude instance must follow them.

## Design
- 001: No default dark backgrounds. Design for the client's audience.
- 002: Don't write clever taglines. Confident businesses state what they are.
- 003: One font family per site. Get out of the way.
- 004: Reference real sites before designing. Find proof, don't guess.
- 005: Study Awwwards winners for interaction patterns.
- 013: Two-audience architecture — institutional buyers get hard data first.
- 026: Nav elements must use discrete background states, not semi-transparent compositing.
- 027: Study reference sites by reading source code, not just screenshots.
- 044: Every Kleos client proposal must be a printed document matching the client site's design language (colors, typography feel, tone). Coil-bound at Staples. Slide it across the table.

## Content
- 011: Every blog article must contain breadcrumbs (harvestable data points for KIN).
- 014: Scrub pitch-specific content from public sites.
- 015: Spell out every acronym.
- 030: Blog articles must sound like the client, not a content farm.
- 033: Footer attribution: "Built by Kleos." with link to kleosdesign.com.

## Technical
- 006: DNS — always verify SPF, DKIM, and DMARC.
- 007: Don't fix blind — diagnose first.
- 012: Canonical domain established before deployment. One serves, one redirects.
- 017: Embed assets as base64 for single-file delivery (when asset count is low).
- 018: Private repos for all client sites.
- 019: Default branch is "main", not "master".
- 020: Don't use display:none for animated elements. Use visibility/opacity.
- 021: CC prompts must include exact file paths.
- 023: @media print must default to printable profile, not full site.
- 024: Canvas particles use viewport dimensions, not document dimensions.
- 028: Hard-clear mobile Safari cache between major CSS changes.
- 031: isMobile must account for touch devices in landscape (pointer: coarse + height check).
- 035: feed.json schema is LOCKED (title, tag, tags[], excerpt, date, slug, author, url).
- 037: Always deploy _headers file with CORS rules for feed.json on Cloudflare.
- 042: Wheel handlers must accumulate delta for touchpad compatibility. Never set cooldown before confirming navigation threshold is met.
- 043: Custom cursors must use transform:translate() not left/top. Add will-change:transform. left/top triggers layout recalc every frame; transform is GPU-composited.

## Process
- 008: Claude architects. Chrome Claude builds.
- 009: The $500 is not the win. The yes is the win.
- 010: First site in any vertical sets the quality floor for every site after it.
- 025: Kill cosmetic elements that don't justify debugging cost.
- 029: Silencer Shop dealer URLs are self-attributing (/dealername path).
- 032: Every client site must have blog infrastructure at build time.
- 034: Claude architects, CC builds. No exceptions.
- 036: Never overwrite the Cloudflare community subfolder when deploying.
- 038: Platform before clients. Kleos platform must never fall behind its client sites.

## Holy Text
- 016/022: Entry format: NEW ENTRY — [Date], [Time] [Timezone]. End with END OF ENTRY.

## CLAUDESYNC
- 039: CLAUDESYNC is the primary context delivery method. Fetch from GitHub, not the Holy Text.
- 040: CLAUDESYNC pages are updated via CC, never by Claude directly.
- 041: Raw GitHub URLs require branch names without forward slashes. Default branch is `main`.
