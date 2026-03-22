# CLAUDESYNC — RanchRock Holdings Knowledge Base

This repo is a structured knowledge base for all RanchRock Holdings operations. It is read by Claude instances across multiple projects via raw GitHub URLs.

## How It Works

- **Claude reads** specific pages at the start of a session using web_fetch
- **Brian or CC updates** pages when things change, via normal git commits
- **Claude never writes** to this repo directly from a conversation

## URL Pattern

All files are accessible at:
```
https://raw.githubusercontent.com/MathrusseB/CLAUDESYNC/claude/main/[path]
```
Example: `https://raw.githubusercontent.com/MathrusseB/CLAUDESYNC/claude/main/kleos/status.md`

## For Claude Instances

When starting a session, fetch `state.md` first. It will tell you which other pages are relevant. Only fetch what you need — don't load everything.

## For Brian

At the end of any session that changes project status, revenue, rules, or dependencies:
1. Ask Claude to generate the updates as markdown
2. Hand the updates to CC or paste them yourself
3. CC pushes to main

## Page Index

|Page                     |What It Contains                                                           |
|-------------------------|---------------------------------------------------------------------------|
|system.md                |System instructions — how CLAUDESYNC works, query formats, update protocols|
|state.md                 |Master snapshot of everything — start here                                 |
|rules.md                 |All operational rules (design, content, technical, process)                |
|revenue.md               |Revenue across all brands                                                  |
|legal.md                 |Corporate structure, filings, IP                                           |
|changelog.md             |Reverse-chronological update log                                           |
|kleos/status.md          |Kleos overview and priorities                                              |
|kleos/clients.md         |All Kleos client projects                                                  |
|kleos/kin.md             |KIN architecture details                                                   |
|kleos/pipeline.md        |Revenue pipeline                                                           |
|calamityville/concept.md |Game concept and mechanics                                                 |
|calamityville/spec.md    |Prototype technical spec                                                   |
|calamityville/business.md|Monetization, funding, team                                                |
|calamityville/roadmap.md |Development phases                                                         |
|speaking/status.md       |Speaking career                                                            |
|employment/status.md     |Current job, opportunities                                                 |
