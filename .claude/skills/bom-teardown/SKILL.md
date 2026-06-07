---
name: bom-teardown
description: Tear down the supply-chain Bill of Materials upstream from a downstream end-market to find bottleneck nodes — the narrowest pipes where downstream spends huge capex but the upstream supplier is small-cap with no short-term substitute. Use when the user names an AI/space/robotics theme or end-market (e.g. "AI data center capex", "humanoid robots", "LEO constellations", "HBM", "CPO") and wants to map who controls the key parts, not who sells the shovels.
---

# BOM Teardown

Implements the top-down teardown from the Serenity framework. Read
`reference/serenity-framework.md` first — it holds the BOM layer taxonomies for
AI / space / robotics and the bottleneck-scoring rubric.

## Inputs
- A theme or end-market (required). If vague, ask which of the three domains
  (AI hardware, space, Physical AI) and how far upstream to go.

## Procedure
1. **Anchor the downstream.** Quantify the capex/demand magnitude with current
   data (WebSearch the latest hyperscaler capex guides, launch cadence, unit
   forecasts). State the number and source. This is the "$100B downstream" anchor.
2. **Decompose into BOM layers.** Use the matching taxonomy table in the reference
   doc. For each layer, list the real players (tickers where public). Keep peeling
   the layer that looks tightest one level deeper (e.g. optical → laser → InP
   substrate → InP feedstock).
3. **Score each node for bottleneck-ness** (1–5 each, note the evidence):
   - *Downstream $ ÷ upstream market cap* (higher = narrower pipe)
   - *Substitutability* (sole/dual-source vs. commodity; switching cost)
   - *Lead time / capacity tightness* (qual time, fab/tool constraints)
   - *Concentration* (few suppliers control the node)
   - *Pricing power* (tiny % of system BOM but a hard gate)
4. **Shortlist the narrowest pipes.** Pick the top 3–6 nodes. For each: one-line
   bottleneck thesis, the closest small/mid-cap names, and the *milestone to watch*
   (qualification / design win / capacity / customer mapping).
5. **Flag what to verify next** — hand each candidate to `bottleneck-dd` for the
   4-question gauntlet and red-flag screen.

## Output
Write `maps/<theme-slug>-<YYYY-MM-DD>.md` containing: the downstream anchor (with
source), the layered table, the scored node ranking, and the shortlist with
tickers + milestones. Then append/refresh the shortlisted tickers in
`watchlist.md` (use the `watchlist` skill's schema; mark conviction as "candidate
— needs DD"). Distinguish **fact** (filed/announced) from **inference**. End with **NFA**.
