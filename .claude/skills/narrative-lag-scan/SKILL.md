---
name: narrative-lag-scan
description: Sweep leading indicators that move BEFORE the price for a named ticker/theme — conference talks, partner/customer pages, supplier & foundry announcements, capacity expansions, job postings, roadmaps, datasheets, qualification/sampling, patents, government awards — then judge whether sell-side has absorbed them and estimate the lag window. Use when the user wants recent signals/news on a name that consensus may not have priced. NFA.
when_to_use: Use to find recent leading-indicator signals on a specific ticker/theme and gauge what's un-priced. Not for building a supply-chain map (bom-teardown) or full financial DD/verdict on a ticker (bottleneck-dd).
argument-hint: "<ticker-or-theme> [since-date]"
allowed-tools: WebSearch WebFetch Read Write Bash
---

# Narrative-Lag Scan

Target: **$ARGUMENTS**

Implements habit #3 of the Serenity framework — signals change first, sell-side
reacts later. **First read `reference/serenity-framework.md`** (relative to the ASBOM
project root) for the source list and the cyclicality caveat. The "lag = alpha"
premise is *asserted, not proven*, so every call gets a post-hoc check.

## Procedure
0. **Ensure `signals/` exists** (`mkdir -p signals`). Default scan window: the last
   review date in `signals/<TICKER>.md` if present, else last 6 months.
1. **Sweep the leading-indicator sources** (WebSearch/WebFetch each; capture date +
   primary-source link for every hit): filings/calls supply-chain & capex commentary;
   relevant conference talks; partner/customer/ecosystem pages; supplier/foundry &
   **capacity-expansion** announcements; job postings; roadmaps/datasheets/
   qualification; trade press/teardowns; patents; gov grants.
2. **Log each new signal:** date · source (link) · one-line implication · **fact vs.
   inference** tag · which BOM node/thesis it touches.
3. **Cyclicality flag.** A capacity-expansion signal is **bearish** for a tightness
   thesis (today's tightness → next year's glut) — mark it as such, don't log it bullish.
4. **Assess absorption.** For each material signal judge `un-priced` / `partially
   priced` / `priced` (any analyst notes, price reaction, guidance change?).
5. **Estimate the lag window** to broad recognition (next earnings, revenue inflection,
   coverage pickup) + the catalyst that closes it.
6. **Post-hoc check.** For prior signals in the log, did the signal actually precede
   the move? Feed the answer to the outcomes ledger so the lag-alpha claim is tested.

## Output
Append a dated scan block to `signals/<TICKER-or-theme-slug>.md`: the signal log
table, the absorption assessment, the lag-window estimate, and the post-hoc results.
Surface top `un-priced` signals first. If a signal materially changes a thesis, note
that `watchlist.md` and `research/<TICKER>.md` need a refresh. Tag **fact vs.
inference**. End with **NFA**.
