---
name: bottleneck-dd
description: Run due diligence on ONE ticker/company using the Serenity four-question gauntlet (with pass bars) plus the full financial AND market-structure red-flag screen — ATM/dilution, customer concentration, financing & runway, GAAP margin, yield, insider/lockup, going-concern, liquidity/float, short interest, promotion, valuation already-priced-in, and geopolitical/export-control. Use when the user names a single ticker and wants a watchlist verdict. Produces a watchlist candidate, not a recommendation. NFA.
when_to_use: Use to vet ONE named ticker/company in depth. Not for mapping a whole supply chain (bom-teardown) or sweeping recent news/leading indicators (narrative-lag-scan).
argument-hint: "<ticker-or-company>"
allowed-tools: WebSearch WebFetch Read Write Bash
---

# Bottleneck Due Diligence

Target: **$ARGUMENTS**

Implements the gauntlet + red-flag guardrail + anti-bias discipline from the Serenity
framework. **First read `reference/serenity-framework.md`** (relative to the ASBOM
project root — this skill assumes that working directory) for the pass bars, the full
red-flag screen, and the verdict set.

## Procedure
0. **Ensure `research/` exists** (`mkdir -p research`).
1. **Locate it in the chain.** Which BOM layer/node, what the downstream pays for,
   listing venue. Pull latest business description (WebSearch / investor site).
2. **The four questions, with pass bars** (evidence + fact-vs-inference tag each).
   Each needs its *disconfirming* check, not just a story:
   1. What's truly in short supply it controls? + who can supply it within 18 months?
   2. How much will downstream pay? (BOM % vs. gate-ness, margin/pricing-power) +
      is it commoditizing?
   3. Is it the closest small/mid-cap *not yet priced*? Requires **positive** evidence
      it's unpriced (valuation vs comps, low coverage, no recent re-rate) — not mere
      absence of evidence. Demand the priced-in case too.
   4. Fatal flaws → run the full red-flag screen below.
3. **Red-flag screen** — pull receipts from latest 10-Q/10-K/8-K and reputable data
   (WebSearch/WebFetch; never assert numbers from memory — cite each):
   - **Capital structure:** ATM/dilution, share-count trend, convertibles/warrants;
     going-concern, auditor quality/changes, restatements, SPAC/reverse-merger lineage,
     related-party deals; **insider Form-4 selling, lockup/warrant expiry**.
   - **Demand:** customer concentration (top 1–3 %); contract backer quality.
   - **Solvency:** cash runway (quarters), debt maturities & rate, off-B/S/SPV/leases.
   - **Margin/execution:** GAAP vs non-GAAP; qualified-and-ramping vs roadmap promise.
   - **Market structure (CRITICAL for anon-sourced microcaps):** float/ADV (can you
     exit?), short interest & borrow, **promotion check** (paid/coordinated pump; what
     is the source's own position — am I exit liquidity?), **already-priced-in**
     (EV/S vs comps, recent re-rate).
   - **Geopolitical:** single-country/export-control exposure (InP/GaAs/rare-earths).
4. **Anti-bias:** write the **bear case/steelman**, a **pre-registered kill criterion**
   ("wrong if X by date Y"), and **P(this inference is wrong)** given the microcap base
   rate. Note the milestone/stage and next catalyst + date.
5. **Verdict** (one): `watchlist` / `high conviction` / `too early — watch milestone` /
   `thesis true but un-investable` (priced-in/illiquid/overvalued) / `pass`, with the
   single biggest reason. State the conviction cap while thesis rests on inference.

## Output
Write `research/<TICKER>.md` (append a new dated block on re-runs; keep history).
Update the ticker's `watchlist.md` row (conviction, catalyst, key risk, kill
criterion, last-reviewed, link) and add it to the outcomes ledger if it graduates.
Tag every number with its source and **fact vs. inference**. End with **NFA**.
