---
name: bom-teardown
description: Build a layered supply-chain Bill-of-Materials MAP upstream from a downstream end-market and rank candidate bottleneck nodes (the narrow pipes the market under-owns). Use when the user wants to MAP a supply chain's structure from scratch for an AI/space/robotics theme (e.g. "AI data center capex", "humanoid actuation", "LEO constellations", "HBM", "CPO") — who controls the key parts, not who sells shovels.
when_to_use: Use to construct or refresh the supply-chain map and bottleneck shortlist for a theme. Do NOT use for recent news / leading indicators on a name (that is narrative-lag-scan) or for due diligence on one ticker (that is bottleneck-dd).
argument-hint: "<theme-or-end-market>"
allowed-tools: WebSearch WebFetch Read Write Bash
---

# BOM Teardown

Theme / end-market: **$ARGUMENTS**

Implements the top-down teardown from the Serenity framework. **First read
`reference/serenity-framework.md`** (relative to the ASBOM project root — this skill
assumes that working directory). It holds the BOM layer taxonomies, the *corrected*
bottleneck-scoring rubric (do NOT use downstream$/market-cap), and the cyclicality
note. If no theme was given, ask which of the three domains and how far upstream.

## Procedure
0. **Ensure `maps/` exists** (`mkdir -p maps`) before writing.
1. **Anchor the downstream.** Quantify the capex/demand with current data
   (WebSearch latest hyperscaler capex, launch cadence, unit forecasts). Cite it.
2. **Decompose into BOM layers** using the matching taxonomy table. List real
   players per layer (annotate listing venue — not everything is US-listed; verify
   each ticker, they are author inferences). Keep peeling the tightest layer deeper.
3. **Score each candidate node 1–5** on the framework's independent axes — **TAM
   capture** (node revenue from this downstream ÷ that spend), **moat/replaceability**
   (one combined axis), **pricing power**, **bottleneck durability/half-life**, and
   **liquidity/investability**. Evidence per score. Weight TAM-capture + durability
   highest. A high moat score with weak TAM capture or incoming glut = false positive.
4. **Cyclicality check.** For each tightness thesis, note *announced* capacity
   additions across all suppliers — broad expansion is a thesis-killer, not bullish.
5. **Shortlist the narrowest, most durable pipes (3–6).** For each: one-line thesis,
   closest small/mid-cap names (with venue), milestone to watch, and the single
   biggest risk (incl. single-country/export-control exposure).

## Output
Write `maps/<theme-slug>-<YYYY-MM-DD>.md`: the anchored downstream (sourced), the
layered table, the scored ranking, and the shortlist. Append shortlisted names to
`watchlist.md` (use the `watchlist` schema; conviction = `candidate — needs DD`).
Tag **fact vs. inference** and **source `[S]` vs. author `[A]`**. Hand each candidate
to `bottleneck-dd`. End with **NFA**.
