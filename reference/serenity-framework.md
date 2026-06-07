# The Serenity Framework — Shared Reference

> Distilled from a third-party summary of ~5,577 tweets by Serenity
> (@aleabitoreddit). **This is a research framework that produces a *watchlist*, not
> a buy list.** NFA.
>
> **Provenance tags.** This doc preaches "fact vs. inference," so it tags itself:
> `[S]` = asserted in the source summary · `[A]` = author inference/addition (added
> to operationalize the method; verify independently). The source gave the *method*
> and a *ticker cloud*; the **layer-by-layer placement of specific tickers, the
> conference list, the scoring metric, and the risk screens below are largely `[A]`**
> — treat them as a starting hypothesis, not gospel.

The one-sentence thesis `[S]`: **Don't just look at who sells shovels — find who
controls the key parts of the shovels.** Tear down the Bill of Materials (BOM)
upstream from downstream capex until you reach a *narrow pipe*: a node where the
downstream spends heavily but the supplier is hard to replace in the short term.

---

## The four core judgment habits `[S]`

1. **Hunt small upstream segments institutions haven't fully understood.** While the
   crowd stares at GPUs, look upstream: optical modules → lasers → InP substrate →
   SOI/epi wafer → feedstock.
2. **Distrust simple stories; interrogate quality.** Customer quality, contract
   structure, financing structure, ATM dilution, GAAP margin.
3. **Exploit narrative absorption lag.** Conferences, partner pages, supplier
   announcements, hiring, roadmaps change *first*; sell-side reacts *later*.
4. **Get on early, at the right milestone** (qualification / design win / capacity
   tightness / customer mapping) — *before* revenue is fully realized. The source
   itself flags this as where the **biggest risk** lives, because the reasoning is a
   jigsaw of public info, not company announcements. Early = higher loss
   probability, not just higher upside. Treat it as such.

---

## The four bottleneck questions (the gauntlet) `[S]` — with pass bars `[A]`

The source lists four questions; the source did **not** give thresholds. The bars
below are `[A]` to stop the gauntlet from being unfalsifiable (anything can pass a
vibes test). Each question needs a *disconfirming* check, not just a story.

1. **What is truly in short supply that this node controls?**
   Bar: name the specific constraint (capacity / IP / a process step / a raw input /
   a qualification) **and** the evidence it's binding (lead times, allocation,
   sole/dual-source status). Disconfirm: who else can supply it within 18 months?
2. **How much will the downstream pay for this bottleneck?**
   Bar: the node is a small % of system BOM but a hard gate → show pricing power
   (gross margin trend, price increases sticking). Disconfirm: is it actually
   commoditizing?
3. **Is the closest small/mid-cap *not yet* priced in?**
   Bar: requires *positive* evidence it's unpriced (valuation vs. comps, no/low
   sell-side coverage, no recent re-rate) — **not** mere absence of evidence.
   This question is a confirmation-bias magnet; demand the priced-in case too.
4. **Fatal flaws?** → run the full red-flag screen below. Any unmitigated CRITICAL
   flag = does not graduate, regardless of how good 1–3 look.

Graduating the gauntlet earns a *watchlist slot*, not conviction.

---

## Bottleneck scoring `[A]` (used by `bom-teardown`)

⚠️ **Do not use "downstream $ ÷ upstream market cap."** It's a trap: downstream
capex is always huge and any small-cap is tiny, so the ratio always looks huge and
"higher = better" degenerates to *smaller cap = better* — steering you into the most
illiquid, most pumpable names while measuring nothing about real value capture.

Score each candidate node 1–5 on **independent** axes (avoid double-counting the
same moat four times), require evidence per score, and set a graduation threshold:

- **TAM capture** — node revenue *from this downstream* ÷ that downstream's spend.
  (How much of the $ actually reaches this node? This is the real "narrow pipe.")
- **Moat / replaceability** — one combined axis: substitutability + switching cost +
  qualification time + supplier concentration (HHI). High = few alternatives, long
  to qualify.
- **Pricing power** — gross-margin level/trend; price increases sticking.
- **Bottleneck durability (half-life)** — see cyclicality note below. How long does
  the pipe stay narrow given *announced* capacity additions across **all** suppliers?
- **Liquidity/investability** — float, ADV, listing venue (penalize names you can't
  size or exit; see red flags).

Weight TAM-capture and durability highest. A high score on moat alone, with weak
TAM capture or a glut incoming, is a false positive.

---

## Financial / risk red-flag screen — the "don't blindly follow" guardrail

The source style is high-volatility, high-concentration, small-cap, cross-market,
event-driven, options/leverage; tweets are **not** a full ledger and returns are
self-reported/unaudited. So pull the receipts. `[S]` = source-named, `[A]` = added.

**Capital structure & dilution**
- ATM program active? share-count trend (4–8 q); convertibles/warrants. `[S]`
- Going-concern language; auditor quality/changes; restatements; reverse-merger/
  SPAC lineage; related-party transactions. `[A]` (microcaps are where fraud hides)
- Insider behavior: Form 4 selling, lockup/warrant expiry schedule, insider-
  ownership trend. `[A]`

**Demand & contract quality**
- Customer concentration: % revenue top 1–3; single-program risk. `[S]`
- Contract backer: MSFT/META/GOOGL/AMZN/ORCL-backed vs. OpenAI-single-thread vs.
  unnamed. `[S]`

**Financing & solvency**
- Cash runway (quarters at current burn); debt maturities & interest rate;
  lease/SPV/off-balance-sheet (esp. neocloud). `[S]`

**Margin & execution**
- GAAP gross/op margin vs. non-GAAP; one-offs. `[S]`
- Qualified & ramping vs. roadmap promise; mass-production / yield track record. `[S]`

**Market structure & promotion (CRITICAL for anon-sourced microcaps)** `[A]`
- **Liquidity:** float, average daily volume — *can you actually exit?* Penalize.
- **Short interest** & days-to-cover / borrow cost (squeeze vs. crowded-short).
- **Promotion check:** is this name being pumped (paid promo, coordinated social)?
  *What is the source account's own position — am I the exit liquidity?*
- **Already priced in:** EV/S vs. comps, implied TAM capture, recent re-rate. Being
  right on the bottleneck and wrong on the price is the main way to lose here.

**Geopolitical / single-country / export-control** `[A]`
- InP, GaAs, rare earths, photoresist, specialty gases concentrate in China/Japan.
  Single-country sourcing is a bottleneck *and* a risk — policy can ban, nationalize,
  or subsidize the pipe away overnight. Score it as risk, not just moat.

---

## Anti-bias discipline `[A]`

The method is reverse-engineered from one anonymous account's *visible* calls —
textbook survivorship bias, and theses assembled from a "jigsaw of public info" are
exactly how you cherry-pick. Counter it:

- **Pre-register a kill criterion** before researching ("I'm wrong if X by date Y").
- **Write the bear case / steelman** for every graduating name.
- **State a base rate** ("most pre-revenue microcap bottleneck plays de-rate or go
  to zero — assume the base rate is low") and an explicit P(this inference is wrong).
- **Keep an outcomes ledger** (see `watchlist.md`): every graduated name is scored at
  +90/+180 days regardless of current opinion, so the method's *own* hit rate gets
  measured instead of assumed. The source's claimed returns are unverified.

---

## Verdict set `[A]`

The method must be able to say "great bottleneck, terrible stock." Allowed verdicts:
`watchlist` · `high conviction` (needs evidentiary bar, capped while thesis rests on
inference) · `too early — watch milestone` · **`thesis true but un-investable`**
(priced-in / illiquid / overvalued) · `pass`.

---

## Narrative-lag source list `[S]` core, `[A]` specifics

- Earnings calls & 10-Q/10-K/8-K (supply-chain commentary, capex guides) `[S]`
- Conference talks & technical sessions — e.g. OFC, ISSCC, Hot Chips, GTC, SC, IEDM,
  Space Symposium `[A]` (verify which matter per name)
- Partner / customer / "ecosystem" pages `[S]`
- Supplier & foundry announcements; **capacity-expansion** press releases `[S]`
  — ⚠️ capacity expansion is *bearish* for a tightness thesis (see cyclicality).
- Job postings `[S]` · product roadmaps, datasheets, qualification/sampling `[S]`
- Trade press & teardown reports `[A]` · patents, gov grants (CHIPS, DoD, NASA/ESA) `[A]`

The "lag = alpha" premise assumes retail reading partner pages front-runs sell-side.
That edge is **asserted, not proven** — every lag call must be checked post-hoc (did
the signal actually precede the move?) and fed to the outcomes ledger.

---

## Cyclicality / bottleneck half-life `[A]`

Memory, optical, and wafers are violently cyclical: today's tightness is next year's
glut. **Capacity expansion announced across the supplier base is a thesis-killer, not
a bullish tell.** For every tightness thesis, track aggregate *announced* capacity
additions and estimate how long the pipe stays narrow.

---

## BOM layer taxonomies `[A]` — ticker placement is author inference; verify each

Tickers below are placed by the author to operationalize the source's ticker cloud;
some may be mis-assigned. **Venue matters** — not everything is US-listed.

### A. AI data-center capex (downstream: hyperscaler capex, $100B+/yr each)

| Layer | What's in it | Candidate names (verify) |
|---|---|---|
| Power generation | utilities, gas turbines, nuclear/SMR, gensets | XLU, VST (Vistra), CEG (Constellation) |
| Power delivery | grid, transformers, switchgear, power semis | transformer lead times; SiC/GaN |
| Cooling | liquid cooling, CDUs, cold plates, immersion | coolant, quick-disconnects |
| Compute | GPUs, AI ASICs, CPUs | NVDA, TSM; custom ASIC (MRVL) |
| Networking / optical | switches, optical modules, CPO, DSP, lasers | LITE (Lumentum), COHR (Coherent), AAOI, MRVL, **SIVE.ST** (Sivers, Stockholm; OTC SIVEF) |
| Memory | HBM, DRAM, NAND | MU (DRAM/HBM/NAND), SNDK (NAND). *Only MU makes HBM among US lines; SK Hynix/Samsung are the HBM oligopoly — Korea proxy EWY if exposure wanted.* |
| Substrate / packaging | CoWoS (TSMC Si-interposer) **and** ABF organic substrate (Ibiden/Unimicron/Shinko) — distinct nodes | packaging/CoWoS capacity. **TSEM** (Tower) = analog/SiPho **foundry**, belongs here not in wafers |
| Materials / wafers | InP, SOI, epi wafer, GaAs, compound semi | AXTI (AXT — InP/GaAs substrate), **Soitec (SOI.PA / OTC SLOIF)** = SOI-wafer ~90% share *(NOT US `$SOI`, which is the renamed oilfield/power co. now `SEI`)*, **IQE.L** (IQE — epi wafer; London AIM, OTC IQEPY) |
| Feedstock | InP/GaAs feedstock, specialty gases, photoresist | sole-source feedstock; export-control exposed |
| Neocloud / financing | GPU clouds & their capital quality | NBIS (Nebius), IREN, CRWV (CoreWeave), CIFR (Cipher), ORCL |

The deeper you go (optical → laser → InP substrate → InP feedstock), the smaller and
fewer the substitutes — but also the less liquid and more single-country-exposed.

> Removed/corrected vs. earlier draft: `$SOI` (US ticker is Solaris **Energy** Infra
> `SEI`, not SOI wafers) → use Soitec `SOI.PA`. `$WDC` dropped from Memory (NAND was
> spun out as `SNDK` Feb 2025; WDC is now HDD-only). `TSEM` moved from wafers to
> foundry/packaging. `SIVE`/`IQE` annotated as non-US listings.

### B. Space (downstream: launch cadence, constellations, defense/gov budgets)

| Layer | What's in it | Watch-for bottleneck |
|---|---|---|
| Launch | vehicles, engines, propulsion | reusability, engine throughput |
| Satellite bus | structures, ADCS, reaction wheels | actuator/wheel supply |
| Payload — comms | phased arrays, RF, optical inter-sat links | space-grade lasers/optics |
| Payload — EO/SAR | sensors, optics, focal planes | rad-hard detectors |
| Power | III-V solar cells, batteries | space-grade III-V cells |
| Electronics | rad-hard ICs, FPGAs, ADC/DAC | rad-hard / qualified parts |
| Ground segment | antennas, gateways, modems | teleport scaling |
| Materials | rad-hard substrates, composites, propellant | specialty materials |

### C. Physical AI / robotics (downstream: humanoids, autonomy, automation)

| Layer | What's in it | Watch-for bottleneck |
|---|---|---|
| Actuation | motors, harmonic/cycloidal reducers, ball screws | precision reducers (Harmonic Drive dominance), gearing |
| Sensing | lidar, depth cameras, tactile, IMU, force-torque | tactile / FT sensors |
| Compute | edge AI SoCs, GPUs | edge inference silicon |
| Power | batteries, BMS, power electronics | high-density cells |
| Magnets / materials | rare-earth magnets (NdFeB), specialty alloys | magnet supply / China dependence (export-control) |
| Connectivity | low-latency links, slip rings | — |
| Software/sim | deprioritized — "software is flooded" | — |

---

## Output discipline

- Every artifact is a **watchlist candidate**, not a recommendation. End with **NFA**.
- Prefer primary sources (filings, datasheets, conference decks) over headlines.
- Tag **fact vs. inference** and **source vs. author** on every claim that matters.
- Record the **kill criterion**, the **catalyst + date** to re-check, and feed
  outcomes back to the ledger so the method audits itself.
