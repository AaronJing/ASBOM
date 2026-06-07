---
name: watchlist
description: Maintain the ASBOM watchlist.md and outcomes ledger — the spine that ties together bom-teardown, bottleneck-dd, and narrative-lag-scan. Use when the user wants to add/update/review/prune a watchlist name, see what's stale or has a catalyst coming, score graduated names at +90/+180 days, or get the current state of the list. Holds the canonical row schema. A research watchlist, not a buy list. NFA.
when_to_use: Use to manage the watchlist file itself (add/update/review/prune/show) and the outcomes ledger. Not for generating new research (use bom-teardown / bottleneck-dd / narrative-lag-scan).
argument-hint: "<add|update|review|prune|show|score> [ticker]"
allowed-tools: Read Write Bash
---

# Watchlist Manager

Request: **$ARGUMENTS**

Owns `watchlist.md` (relative to the ASBOM project root), the canonical table all
other ASBOM skills feed. Read `reference/serenity-framework.md` for the discipline
(watchlist ≠ buy list; survivorship bias; NFA; fact vs. inference; the verdict set).

## Row schema (one row per ticker)
`| Ticker | Domain | Chain node | Bottleneck thesis (1 line) | Conviction | Catalyst (+date) | Key risk | Kill criterion | Stage | Last reviewed | Links |`

- **Domain:** AI-HW / Space / Physical-AI
- **Chain node:** the BOM layer it bottlenecks (e.g. "InP substrate", "harmonic reducer")
- **Conviction:** `candidate — needs DD` / `watchlist` / `high conviction` /
  `too early` / `thesis true but un-investable` / `pass`. Cap conviction while the
  thesis rests on inference; `high conviction` needs an evidentiary bar (qualified &
  ramping, named backer, priced-in case rebutted).
- **Kill criterion:** the pre-registered "wrong if X by date Y".
- **Stage:** qualification / design win / capacity tight / revenue ramp
- **Links:** repo-root-relative, e.g. `[research/AXTI.md](research/AXTI.md)`; use `—`
  when a file doesn't exist yet.

## Operations (infer from $ARGUMENTS)
- **add / update:** upsert one row (never duplicate). If `candidate — needs DD`,
  suggest running `bottleneck-dd`. A row with no `research/` link hasn't passed the
  gauntlet — flag it.
- **review:** list rows whose *Last reviewed* is older than ~30 days (or given window)
  and any with imminent catalysts; recommend `narrative-lag-scan` / `bottleneck-dd`
  refreshes and offer to run them.
- **prune:** move `pass` rows to `## Archive` (keep the reasoning/lesson, don't delete).
- **score (outcomes ledger):** for graduated names past +90 / +180 days, record the
  price/return move vs. entry **regardless of current opinion**, so the method's own
  hit rate is measured, not assumed. This is the survivorship-bias guard.
- **show:** render the current table, optionally filtered by domain/conviction.

## Rules
- Ensure `watchlist.md` exists (create from the schema if missing).
- Sort active rows by conviction then domain; keep `## Archive` and `## Outcomes
  ledger` sections below the active table.
- Every row links back to its evidence. Never imply a recommendation; keep the **NFA**
  banner in the file header.
