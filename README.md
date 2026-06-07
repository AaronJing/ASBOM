# ASBOM — AI Supply-chain BOM research

A personal research workspace built around the **Serenity framework**: tear down
the Bill of Materials upstream from downstream capex to find the *narrowest pipe* —
the small/mid-cap node with no short-term substitute that the market hasn't priced.

Focus domains: **AI hardware** (materials → chips, not flooded software), **Space**,
and **Physical AI / robotics**.

> **NFA.** Everything here produces a *watchlist*, not a buy list.

## The four skills (in `.claude/skills/`)

| Skill | Trigger | Writes to |
|---|---|---|
| **bom-teardown** | name a theme/end-market → layered supply-chain map + bottleneck shortlist | `maps/` |
| **bottleneck-dd** | name a ticker → 4-question gauntlet + financial red-flag screen → verdict | `research/` |
| **narrative-lag-scan** | name a ticker/theme → leading-indicator sweep + absorption-lag estimate | `signals/` |
| **watchlist** | add/update/review/prune the list; the spine the others feed | `watchlist.md` |

## Typical flow

1. `/bom-teardown AI data center optical` → shortlist of bottleneck nodes/tickers.
2. `/bottleneck-dd <TICKER>` → does the thesis hold? fatal flaws? → watchlist verdict.
3. `/narrative-lag-scan <TICKER>` → what's moving that consensus hasn't absorbed?
4. `/watchlist review` → what's stale or has a catalyst coming → re-run 2/3.
5. `/watchlist score` → grade graduated names at +90/+180d, so the method's own
   hit rate gets measured (survivorship-bias guard), not assumed.

(Tickers in the reference are *author inferences* — verify each; venues vary, e.g.
Soitec is `SOI.PA` (Paris), not US `$SOI` which is now `SEI`.)

## Layout

```
reference/serenity-framework.md   methodology + BOM taxonomies (read by every skill)
maps/        teardown outputs       research/   per-ticker DD
signals/     narrative-lag logs     watchlist.md  the spine
```

The framework is replicable; the *positions are not*. Watchlist, then do the real
financial/valuation/liquidity/positioning work yourself.
