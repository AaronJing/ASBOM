# The Serenity Framework — Shared Reference

> Distilled from an analysis of ~5,577 tweets by Serenity (@aleabitoreddit).
> This is a **research framework that produces a watchlist, not a buy list**. NFA.

The one-sentence thesis: **Don't just look at who is selling shovels — find who
controls the key parts of the shovels.** Tear down the Bill of Materials (BOM)
upstream from downstream capex until you reach the *narrowest pipe*: a node where
the downstream spends hundreds of billions, but the upstream supplier is a small/
mid cap with no short-term substitute.

---

## The four core judgment habits

1. **Hunt small upstream segments institutions haven't fully understood.** While the
   crowd stares at GPUs, look upstream: optical modules → lasers → InP substrate →
   SOI/epi wafer → feedstock.
2. **Distrust simple stories; interrogate quality.** Customer quality, contract
   structure, financing structure, ATM dilution, GAAP margin. Especially in
   neocloud / AI data-center financing.
3. **Exploit narrative absorption lag.** Conferences, partner pages, supplier
   announcements, job postings, product roadmaps change *first*; sell-side and
   institutional positioning react *later*. That window is the alpha.
4. **Get on early, at the right milestone.** The biggest moves are caught at
   *qualification / design win / capacity tightness / customer mapping* — not when
   revenue is fully realized. This is also where the biggest risk lives, because
   the reasoning is a jigsaw of public info, not company announcements.

---

## The four bottleneck questions (the gauntlet)

Run these on any candidate before it earns a watchlist slot:

1. **What is truly in short supply in this chain?** (capacity, IP, a process step,
   a raw input, a qualification)
2. **How high a price is the downstream willing to pay for this bottleneck?**
   (Is the node a tiny % of system BOM but a hard gate? Pricing power follows.)
3. **Which small company is closest to this bottleneck, and is the market *not yet*
   pricing it in?** (design wins, sole/dual-source status, lead times)
4. **Does it have fatal flaws?** financing need · ATM/share dilution · customer
   concentration · mass-production / yield failure · weak GAAP margin · high-
   interest debt.

Pass all four → graduate to financial/valuation/liquidity/positioning research.

---

## Financial red-flag checklist (the "don't blindly follow" guardrail)

His style is high-volatility, high-concentration, small-cap, cross-market,
event-driven, options/leverage. Public tweets are not a full ledger. So always
pull the receipts:

- **Dilution / ATM:** Is there an active at-the-market program? Share count trend
  over 4–8 quarters. Convertibles, warrants.
- **Customer concentration:** % revenue from top 1–3 customers. Single-program risk.
- **Financing structure:** Cash runway (quarters at current burn), debt maturities,
  interest rate on debt, lease/SPV/off-balance-sheet structures (esp. neocloud).
- **Margin quality:** GAAP gross/operating margin vs. non-GAAP. One-offs.
- **Execution / yield:** Is the bottleneck product actually qualified and ramping,
  or still a roadmap promise? Mass-production track record.
- **Contract quality:** Who is the backer? (MSFT/META/GOOGL/AMZN/ORCL-backed
  contracts vs. an OpenAI-risk single-thread vs. unnamed).

---

## Narrative-lag source list (where signals appear *before* the price)

- Earnings calls & 10-Q/10-K/8-K (read the supply-chain commentary, capex guides)
- Conference talks & technical sessions (OFC, ISSCC, Hot Chips, GTC, SC, IEDM,
  Space Symposium, etc.)
- Partner / customer / "ecosystem" pages on company websites
- Supplier & foundry announcements; capacity-expansion / capex press releases
- Job postings (roles reveal roadmap & ramp before products ship)
- Product roadmaps, datasheets, qualification / sampling announcements
- Industry trade press & teardown reports
- Patent filings, government grants (CHIPS, DoD, ESA/NASA awards)

---

## BOM layer taxonomies (the maps to peel)

### A. AI data-center capex (downstream: hyperscaler capex, $100B+/yr each)

| Layer | What's in it | Watch-for bottleneck nodes |
|---|---|---|
| Power generation | utilities, gas turbines, nuclear/SMR, gensets | $XLU $VST $CEG; turbine/SMR supply |
| Power delivery | grid, transformers, switchgear, power semis | transformer lead times, SiC/GaN |
| Cooling | liquid cooling, CDUs, cold plates, immersion | coolant, quick-disconnects |
| Compute | GPUs, AI ASICs, CPUs | $NVDA $TSM; custom ASIC ($MRVL) |
| Networking / optical | switches, optical modules, CPO, DSP, lasers | $SIVE $LITE $COHR $AAOI $MRVL |
| Memory | HBM, DRAM, NAND | $MU $SNDK $WDC; HBM tightness |
| Substrate / packaging | CoWoS, ABF substrate, advanced packaging | packaging capacity |
| Materials / wafers | InP, SOI, epi wafer, GaAs, compound semi | $AXTI $SOI $IQE $TSEM |
| Feedstock | InP/GaAs feedstock, specialty gases, photoresist | sole-source feedstock |
| Neocloud / financing | GPU clouds & their capital quality | $NBIS $IREN $CRWV $CIFR $ORCL |

The deeper you go (optical → laser → InP substrate → InP feedstock), the smaller
the cap and the fewer the substitutes — i.e., the narrower the pipe.

### B. Space (downstream: launch cadence, constellations, defense/gov budgets)

| Layer | What's in it | Watch-for bottleneck nodes |
|---|---|---|
| Launch | vehicles, engines, propulsion | reusability, engine throughput |
| Satellite bus | structures, ADCS, reaction wheels | actuator/wheel supply |
| Payload — comms | phased arrays, RF, optical inter-sat links | space-grade lasers/optics |
| Payload — EO/SAR | sensors, optics, focal planes | rad-hard detectors |
| Power | solar cells (III-V), batteries | space-grade III-V cells |
| Electronics | rad-hard ICs, FPGAs, ADC/DAC | rad-hard / qualified parts |
| Ground segment | antennas, gateways, modems | scaling teleports |
| Materials | rad-hard substrates, composites, propellant | specialty materials |

### C. Physical AI / robotics (downstream: humanoids, autonomy, automation)

| Layer | What's in it | Watch-for bottleneck nodes |
|---|---|---|
| Actuation | motors, harmonic/cycloidal reducers, ball screws | precision reducers, gearing |
| Sensing | lidar, depth cameras, tactile, IMU, force-torque | tactile / FT sensors |
| Compute | edge AI SoCs, GPUs | edge inference silicon |
| Power | batteries, BMS, power electronics | high-density cells |
| Magnets / materials | rare-earth magnets (NdFeB), specialty alloys | magnet supply / China dep. |
| Connectivity | low-latency links, slip rings | — |
| Software/sim (deprioritized — "software is flooded") | — | — |

---

## Output discipline

- Every artifact this framework produces is a **watchlist candidate**, not a
  recommendation. End reports with **NFA**.
- Prefer primary sources (filings, datasheets, conference decks) over headlines.
- Record *what would change your mind* and the *catalyst + date* to re-check.
- Distinguish **fact** (filed/announced) from **inference** (jigsaw of public info).
