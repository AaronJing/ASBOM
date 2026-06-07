---
name: watchlist
description: Maintain the ASBOM watchlist.md — the spine that ties together bom-teardown, bottleneck-dd, and narrative-lag-scan. Use when the user wants to add/update/review/prune a watchlist name, see what's stale and needs re-checking, or get the current state of the list. Holds the canonical row schema other skills write to. It is a research watchlist, not a buy list. NFA.
---

# Watchlist Manager

Owns `watchlist.md`, the canonical table all other ASBOM skills feed. Read
`reference/serenity-framework.md` for the discipline (watchlist ≠ buy list, NFA,
fact vs. inference).

## Row schema (one row per ticker)
`| Ticker | Domain | Chain node | Bottleneck thesis (1 line) | Conviction | Catalyst (+date) | Key risk | Stage | Last reviewed | Links |`

- **Domain:** AI-HW / Space / Physical-AI
- **Chain node:** the BOM layer it bottlenecks (e.g. "InP substrate", "harmonic reducer")
- **Conviction:** `candidate — needs DD` / `watchlist` / `high` / `too early` / `pass`
- **Stage:** qualification / design win / capacity tight / revenue ramp
- **Links:** relative paths to `research/<TICKER>.md`, `signals/<…>.md`, `maps/<…>.md`

## Operations (infer from the request)
- **add / update:** upsert a row. If conviction is `candidate — needs DD`, suggest
  running `bottleneck-dd`. Keep one row per ticker; never duplicate.
- **review:** list rows whose *Last reviewed* is older than ~30 days (or user-given
  window) and any with imminent catalysts; recommend `narrative-lag-scan` /
  `bottleneck-dd` refreshes. Offer to run them.
- **prune:** move `pass` rows to a `## Archive` section at the bottom (don't delete
  the reasoning — keep the lesson).
- **show:** render the current table, optionally filtered by domain/conviction.

## Rules
- Sort active rows by conviction then domain. Keep an `## Archive` section below.
- Every row links back to its evidence files. If a row has no `research/` link,
  it hasn't passed the gauntlet — flag it.
- Never imply a recommendation. The file header carries an **NFA** banner.
