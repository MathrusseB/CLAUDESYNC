# CLAUDESYNC — System Instructions

**Last Updated:** March 22, 2026

> This page is read by every Claude instance at the start of every session. It defines how the knowledge base works, how to request historical detail, and how to generate updates.

-----

## What CLAUDESYNC Is

A structured knowledge base of markdown files on GitHub that holds the current operating state of all IXK Holdings projects. Claude reads from it. Claude never writes to it directly.

**Base URL:** `https://raw.githubusercontent.com/MathrusseB/CLAUDESYNC/claude/main/`

## Tools in the Ecosystem

|Tool                |What It Is                  |What It Does                                                                            |
|--------------------|----------------------------|----------------------------------------------------------------------------------------|
|**CLAUDESYNC**      |GitHub repo (markdown files)|Holds current state. Claude reads via web_fetch.                                        |
|**Holy Text**       |Google Doc (Brian's browser)|Full chronological archive. Every session entry, every technical detail, every decision.|
|**Chrome Claude**   |Browser-based Claude        |Can read the Holy Text when open in a tab. Bridge between archive and active sessions.  |
|**CC (Claude Code)**|Command line tool           |Pushes code, updates files, deploys. Updates CLAUDESYNC pages on GitHub.                |

## How to Start a Session

1. Brian pastes the CLAUDESYNC base URL and tells Claude which project the session is about.
1. Claude fetches `state.md` and `system.md` first.
1. Based on the project, Claude fetches only the relevant pages (e.g., a Kleos session fetches `kleos/status.md` and `kleos/clients.md` — not the Calamityville pages).
1. Claude confirms it has context and begins work.

**Never fetch all pages.** Only fetch what the session needs.

## Page Index

|Page                  |Path                     |Contents                           |
|----------------------|-------------------------|-----------------------------------|
|System Instructions   |system.md                |THIS PAGE — how CLAUDESYNC works   |
|Master State          |state.md                 |Snapshot of everything — start here|
|Rules                 |rules.md                 |All operational rules              |
|Revenue               |revenue.md               |Revenue across all brands          |
|Legal                 |legal.md                 |Corporate structure, filings, IP   |
|Changelog             |changelog.md             |Reverse-chronological update log   |
|Kleos Status          |kleos/status.md          |Kleos overview and priorities      |
|Kleos Clients         |kleos/clients.md         |All client projects                |
|Kleos KIN             |kleos/kin.md             |KIN architecture details           |
|Kleos Pipeline        |kleos/pipeline.md        |Revenue pipeline                   |
|Calamityville Concept |calamityville/concept.md |Game concept and mechanics         |
|Calamityville Spec    |calamityville/spec.md    |Prototype technical spec           |
|Calamityville Business|calamityville/business.md|Monetization, funding, team        |
|Calamityville Roadmap |calamityville/roadmap.md |Development phases                 |
|Speaking Status       |speaking/status.md       |Speaking career                    |
|Employment Status     |employment/status.md     |Current job, opportunities         |

-----

## When Claude Needs Historical Detail

CLAUDESYNC only holds current state. It does not hold session history, exact technical implementations, or the full story behind past decisions. That lives in the **Holy Text** (Google Doc).

When a session needs detail that isn't in CLAUDESYNC, Claude generates a **Holy Text Query** for Chrome Claude in this exact format:

```
HOLY TEXT QUERY
───────────────
Question: [specific question — what you need to know]
Context: [why you need it — what the current session is working on]
Format: [how the answer should come back]
  Options: "exact quote" | "summary under 200 words" | "list of steps" | "full passage"
```

### How Brian Executes It

1. Copy the Holy Text Query from the project chat
1. Open the Holy Text Google Doc in a browser tab
1. Open Chrome Claude (browser-based Claude)
1. Paste the query into Chrome Claude
1. Chrome Claude reads the Holy Text, finds the answer, returns it in the requested format
1. Copy Chrome Claude's answer back into the project chat
1. Tell project Claude: "Here's what Chrome Claude found:" and paste the answer

-----

## When a Session Ends — Generating Updates

At the end of any session that changes project status, revenue, rules, dependencies, or priorities, Claude generates two outputs:

### Output 1: Holy Text Entry

A full session entry for the archive, in this format:

```
NEW ENTRY — [Date], [Time] [Timezone]

FILED BY: Claude ([Project Name] Session — [Brief Description])

---

SESSION SUMMARY
[What was accomplished in plain English]

WHAT CHANGED
[Bulleted list of specific changes]

NEW RULES (if any)
[Rule number and description]

OUTSTANDING ITEMS
[What's still pending]

---

END OF ENTRY
```

Brian pastes this into the Holy Text Google Doc.

### Output 2: CLAUDESYNC Update

A set of page updates for CC to push to the GitHub repo, in this format:

```
CLAUDESYNC UPDATE
─────────────────
Repo: github.com/MathrusseB/CLAUDESYNC
Branch: claude/main

Files to update:
- [path.md]: [one-line description of what changed]
- [path.md]: [one-line description of what changed]
- changelog.md: [add new entry at top]

── FILE: [path.md] ──
[full replacement content for the file]

── FILE: [path.md] ──
[full replacement content for the file]

── FILE: changelog.md (PREPEND — do not replace, add to top) ──
## [Date]
- [What changed]
- Pages affected: [list]
```

Brian hands this to CC (Claude Code). CC pushes directly to claude/main. Next session, every project sees the updates.

### What Triggers an Update

Generate both outputs when ANY of the following happened in the session:

- A project status changed (started, completed, blocked, live)
- Revenue changed (payment received, invoice sent, deal closed or lost)
- A new rule was established
- A dependency shifted
- A priority order changed
- A new document or artifact was created
- A strategic decision was made
- A concept pivoted or evolved

If nothing changed (e.g., a pure Q&A session), no update is needed. Say so explicitly: "No CLAUDESYNC updates needed from this session."

-----

## Rules for All Claude Instances

1. **Never hallucinate state.** If CLAUDESYNC doesn't have the answer, say so and generate a Holy Text Query. Don't guess.
1. **Never load unnecessary pages.** A Kleos build session doesn't need Calamityville pages. A Calamityville strategy session doesn't need Kleos client details.
1. **Always check changelog.md if unsure whether information is current.** The changelog shows what changed and when.
1. **Rules in rules.md are permanent and universal.** Every Claude instance follows them regardless of project.
1. **CLAUDESYNC pages replace, not append.** When updating a page, write the full new version. Old content is overwritten. The Holy Text is where history lives.
1. **The changelog is the one exception** — new entries are prepended to the top, not replaced.
