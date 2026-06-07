---
name: bottleneck-dd
description: Run due diligence on a single ticker/company using the Serenity four-question bottleneck gauntlet plus the financial red-flag screen (ATM/dilution, customer concentration, financing structure & cash runway, GAAP margin, mass-production/yield risk, contract quality). Use when the user names a ticker or company and wants a watchlist verdict — whether the bottleneck thesis holds and whether there are fatal flaws. Produces a watchlist candidate, not a recommendation. NFA.
---

# Bottleneck Due Diligence

Implements the bottleneck gauntlet + red-flag guardrail from the Serenity
framework. Read `reference/serenity-framework.md` first (the four questions and
the financial red-flag checklist).

## Inputs
- A ticker or company name (required). Optionally the supply-chain node it sits in
  (from a prior `bom-teardown`).

## Procedure
1. **Locate it in the chain.** State which BOM layer/node it occupies and what the
   downstream is paying for. Pull the latest business description (WebSearch /
   investor site).
2. **The four questions** (answer each with evidence + fact-vs-inference tag):
   1. What is truly in short supply that this company controls?
   2. How much is the downstream willing to pay for that bottleneck? (BOM % vs.
      gate-ness, pricing power signals)
   3. Is it the closest small/mid-cap to the bottleneck, and is the market *not yet*
      pricing it? (design wins, sole/dual-source, lead times, recent re-rating)
   4. Fatal flaws? → run the red-flag screen below.
3. **Financial red-flag screen** — pull the receipts from the latest 10-Q/10-K/8-K
   and reputable data (WebSearch/WebFetch; never assert numbers from memory — cite):
   - **Dilution / ATM:** active ATM program? share-count trend (4–8 q), convertibles/warrants.
   - **Customer concentration:** % revenue top 1–3 customers; single-program risk.
   - **Financing / runway:** cash, quarterly burn → runway in quarters; debt
     maturities & interest rate; lease/SPV/off-balance-sheet (esp. neocloud).
   - **Margin quality:** GAAP gross/op margin vs. non-GAAP; one-offs.
   - **Execution / yield:** qualified & ramping vs. roadmap promise; mass-prod record.
   - **Contract quality:** who's the backer (MSFT/META/GOOGL/AMZN/ORCL vs. OpenAI-
     single-thread vs. unnamed).
4. **Milestone & catalyst.** What stage is it at (qualification / design win /
   capacity / revenue)? Next catalyst + expected date. What would change the thesis.
5. **Verdict:** one of `watchlist` / `too early — watch milestone` / `pass` with the
   single biggest reason. Note valuation/liquidity caveats.

## Output
Write `research/<TICKER>.md` with all sections above and a dated header (append a
new dated block on re-runs; keep history). Update the ticker's row in
`watchlist.md` (conviction, catalyst, key risk, last-reviewed date, link to this
file). Tag every number with its source and **fact vs. inference**. End with **NFA**.
