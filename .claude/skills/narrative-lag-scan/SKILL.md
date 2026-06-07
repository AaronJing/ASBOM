---
name: narrative-lag-scan
description: Hunt leading indicators that move before the price — conference talks, partner/customer/ecosystem pages, supplier & foundry announcements, capacity expansions, job postings, product roadmaps, datasheets, qualification/sampling news, patents and government awards. Use when the user wants to find signals that institutions/sell-side haven't absorbed yet for a ticker or theme, or to refresh signals on a watchlist name. Estimates the absorption-lag window. NFA.
---

# Narrative-Lag Scan

Implements habit #3 of the Serenity framework: conferences, partner pages,
supplier announcements, hiring, and roadmaps change *first*; sell-side reacts
*later*, and that window is the alpha. Read the "Narrative-lag source list" in
`reference/serenity-framework.md`.

## Inputs
- A ticker, company, or theme (required). Optional: a "since" date to scan from
  (default: last review date in `signals/<TICKER>.md`, else last 6 months).

## Procedure
1. **Sweep the leading-indicator sources** (WebSearch/WebFetch each; capture the
   date and a primary-source link for every hit):
   - Earnings calls / 10-Q/10-K/8-K supply-chain & capex commentary
   - Conference talks & technical sessions (OFC, ISSCC, Hot Chips, GTC, SC, IEDM,
     Space Symposium, etc.) relevant to the name
   - Partner / customer / "ecosystem" pages on the company & its customers' sites
   - Supplier / foundry / capacity-expansion announcements
   - Job postings (roles that reveal roadmap & ramp)
   - Product roadmaps, datasheets, qualification / sampling announcements
   - Trade press / teardown reports; patents; government grants (CHIPS, DoD, NASA/ESA)
2. **Log each new signal**: date · source (with link) · one-line what-it-implies ·
   **fact vs. inference** tag · which BOM node/thesis it touches.
3. **Assess absorption.** For each material signal, judge whether sell-side /
   consensus has already reflected it (any analyst notes, price reaction, guidance
   change?). Mark `un-priced` / `partially priced` / `priced`.
4. **Estimate the lag window** — the gap between the leading signal and likely
   broad recognition (next earnings, revenue inflection, index/coverage pickup).
   Note the catalyst that would close it.

## Output
Append to `signals/<TICKER-or-theme-slug>.md` a dated scan block: the signal log
table, the absorption assessment, and the lag-window estimate. Surface the top
`un-priced` signals at the top. If a signal materially changes a thesis, note that
the ticker's `watchlist.md` row and `research/<TICKER>.md` should be refreshed.
Distinguish **fact** from **inference**. End with **NFA**.
