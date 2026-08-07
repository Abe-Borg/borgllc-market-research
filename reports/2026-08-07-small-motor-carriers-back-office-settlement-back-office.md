# Small Motor Carriers (5–50 Trucks) — Back Office and Settlement

**Market research cycle · back-office angle**

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market claimed** | Small motor carriers (5–50 trucks) — back office and settlement |
| **Angle claimed** | back-office |
| **Claim ID** | `6449b7ae` |
| **Date** | 2026-08-07 |
| **Backlog remaining after this claim** | 239 assignments across 122 markets |
| **Ledger state at claim time** | 13 completed reports, 0 outstanding claims |

### Why this assignment over the others available

Three filters were applied to the 240-item backlog in order.

**First, market breadth over depth.** The ledger's completed set contains exactly one report per market — thirteen markets, thirteen reports. Every market in the backlog with an untouched entry was therefore equally "new" by the zero-completed test, so the tiebreaker moved to the angle distribution: `core-practitioner-workflow` had five completed reports, `narrow-subspecialty` and `handoffs-and-qa` three each, and **`back-office` only two**. The catalog's thinnest angle is the one where the drudgery lives, which is where a catalog of small focused tools should be strongest. That eliminated roughly three quarters of the backlog.

**Second, evidence density.** The remaining candidates were screened for whether a substantial primary-evidence trail plausibly exists online. Small motor carriers are unusual in that nearly every obligation the back office carries is written down in a public federal or interstate-compact document — 49 CFR Parts 376, 382, 386, 390, 391, 395, 396; the IFTA Articles of Agreement, Procedures Manual and Audit Manual; the IRP Audit Reference; FMCSA's Uniform Fine Assessment manual — *and* FMCSA publishes actual violation counts and penalty amounts. That combination (a written obligation plus a published price for failing it) is rare and makes the ROI arithmetic checkable rather than asserted. It is also a market with an unusually active public practitioner forum (TruckersReport) whose threads are indexed and fetchable.

**Third, catalog diversity.** The completed set clusters heavily in AEC (fire protection, HVAC, land surveying, geotech) and in insurance/real-estate/healthcare-billing adjacencies. Freight brokerage appears once, but at the `handoffs-and-qa` angle, which covers load tendering, BOL/POD exchange and cargo claims — the *broker's* side of the transaction. An **asset-based motor carrier's back office** is a different business with a different regulatory surface: it employs drivers, owns vehicles, files fuel taxes, and produces settlement statements, none of which a broker does. Overlap risk was judged low.

Two candidates were seriously considered and rejected. *Community association (HOA/condominium) management back office* is a large and painful market but sits adjacent to the already-completed *Commercial property management / back-office* report, and its opportunity set (AP, work orders, owner statements, delinquency tracking) would likely duplicate it. *Independent pharmacy third-party reconciliation and PBM claw-backs* is genuinely narrow and painful but has poor prospects for realistic test data, since PBM remittance files are contractually restricted.

---

## 1. Market examined

### The industry and the addressable population

US motor carriers registered with FMCSA number **2,085,534** as of the May 2026 operating-authority snapshot ([FMCSA A&I Registration Statistics](https://ai.fmcsa.dot.gov/RegistrationStatistics)), but that figure counts every USDOT registrant including private, intrastate and dormant entities. Direct aggregation of the FMCSA SMS Motor Carrier Census file (Socrata resource `kjg3-diqy`, data updated 2026-07-13) gives the distribution:

| Power units | Carriers | Share of all registrants |
|---|---:|---:|
| 1 | 1,169,530 | 56.1% |
| 2–6 | 622,252 | 29.8% |
| 7–20 | 113,505 | 5.4% |
| 21–50 | 28,173 | 1.4% |
| 51–100 | 9,486 | 0.5% |
| 101+ | 8,103 | 0.4% |

Filtering to carriers holding for-hire authority **and** reporting mileage for 2024 or later yields 436,124 active for-hire carriers, of which the **5–50 power-unit band contains 69,511 carriers operating roughly 878,851 power units**. Of those 69,511, **68,186 (98.1%) have an email address on file with FMCSA** — the segment is directly reachable without a channel partner. Top states: California 7,210, Texas 6,735, Illinois 4,675, Ohio 3,679, Pennsylvania 3,219.

Published cross-checks are consistent once definitions are reconciled. ATA reports "almost 580,000 active US motor carriers... that own or lease at least one tractor," of which **91.5% operate 10 or fewer trucks and 99.3% operate 100 or fewer** ([ATA Economics and Industry Data](https://www.trucking.org/economics-and-industry-data)). FMCSA's own [Pocket Guide 2024](https://www.fmcsa.dot.gov/sites/fmcsa.dot.gov/files/2025-09/FMCSA%20Pocket%20Guide%202024-v6%20508%20.pdf) counts 787,189 interstate + intrastate-HM carriers with recent activity, 53.1% of them single-truck. FreightWaves puts it at **97% of for-hire carriers at ≤10 trucks, 70% single-truck** ([FreightWaves](https://www.freightwaves.com/news/there-are-292000-shippers-in-america-and-97-of-carriers-have-10-trucks-or-less-the-match-has-been-right-in-front-of-you-the-whole-time)).

**The honest denominator for a back-office tool aimed at this band is 60,000–70,000 companies, not 580,000 and not 2 million.**

### The organizations

An active for-hire carrier with 7–20 power units averages **11.07 drivers**; a 21–50 unit carrier averages **32.02 drivers** (computed from the FMCSA census). A "10–30 truck carrier" is therefore a **10–35 person company**, of which 1–3 people do not drive.

ATRI's 2026 report (2025 data) found carriers cut **non-driver staff by 7.8%** in 2025 while cutting truck count only 2.4% — the back office was cut harder than the fleet ([ATRI](https://truckingresearch.org/2026/07/new-atri-report-details-accelerating-costs-and-low-profitability-despite-cuts/)).

### The user

The buyer and the user are the same person, and it is one of two people:

- **The owner.** Does sales, dispatch, banking and whatever else is left. Practitioner voice, verbatim: *"I run 7 trucks with no fleet management software. If your accounting is set up properly you should have access to anything you need right there."* — kranky1, [TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/management-software.2418884/), 29 Mar 2022.
- **The office manager / settlement clerk / safety administrator** — one title, all three jobs. ZipRecruiter (7 Aug 2026): "Trucking Company Office Manager" averages **$51,476/yr ($24.70/hr)**, typical $40k–$59k, with 1,000+ open postings ([ZipRecruiter](https://www.ziprecruiter.com/Jobs/Trucking-Company-Office-Manager)). "Settlement Clerk" averages **$19.77/hr**, and the listed software skills are **Microsoft Excel/Office and QuickBooks** — not a TMS ([ZipRecruiter](https://www.ziprecruiter.com/Jobs/Settlement-Clerk)).

A dedicated safety-and-compliance head appears around 30–50 trucks: Frasier Dedicated Services, Dallas TX, "Safety & Compliance Fleet Manager (DOT/FMCSA)," **$60,000–$70,000**, posted 5 Aug 2026 ([Indeed](https://to.indeed.com/aaprw97ddsgc)). Below that, the archetype is Building Products Inc., Sioux Falls SD, "Safety and Compliance Supervisor," $65,109–$83,968, where DOT compliance is *one of four portfolios* and the stated required toolchain is **"Strong working knowledge of Microsoft Office applications and Tenstreet"** ([Indeed](https://to.indeed.com/aappsbcpvpnp)).

### The economics that gate every pricing decision

ATRI's 2026 update (released 15 Jul 2026, 2025 data) puts **average marginal cost at $2.336/mile**, up 3.4%:

| Line item | ¢/mile 2025 | YoY |
|---|---:|---:|
| Driver wages | 81.8 | +2.5% |
| Driver benefits | 21.0 | +6.6% |
| Fuel | 48.0 | flat |
| Truck/trailer payments | 40.4 | +3.6% |
| Repair & maintenance | 21.5 | **+8.6%** |
| Insurance premiums | 10.6 | +3.9% |
| Tires | 5.0 | +6.4% |
| Tolls | 4.3 | **+13.2%** |
| Permits & licenses | 0.8 | *decreased* |
| **Total** | **233.6** | **+3.4%** |

Operating margins in 2025: **truckload and refrigerated below 1.0%; flatbed at −0.5% (an operating loss)**; only tank came in around 4% ([FreightWaves](https://www.freightwaves.com/news/trucking-costs-outpaced-consumer-inflation-in-25-atri), [FleetOwner](https://www.fleetowner.com/operations/article/55392569/atri-report-breaks-down-class-8-truck-operating-costs-by-region-and-expense-category)). Utilization has collapsed from a 125,000 mi/truck/yr historical average to roughly **86,000 today** ([FleetOwner IdeaXchange](https://www.fleetowner.com/perspectives/ideaxchange/blog/55395622/three-takeaways-from-atris-2026-trucking-cost-analysis-for-fleet-operators)).

The arithmetic that follows is the single most important constraint in this report. At 86,000 mi × $2.336/mi, a truck consumes **~$201,000/yr**, i.e. ~$16,750/truck/month. At a 0.5–1.0% operating margin, **gross profit per truck is roughly $1,000–$2,000 per year.** A $100/truck/month software stack costs $1,200/yr — **60% to 120% of the entire per-truck profit.**

Against that, a single average FMCSA civil penalty of **$5,959** ([My Safety Manager](https://www.mysafetymanager.com/driver-qualification-file-cost/)) equals three to six trucks' worth of annual profit.

> **This is why compliance spend survives cuts that TMS spend does not, and it is the pricing thesis for everything in section 4.** Time-saving arguments do not clear the bar. Fine-avoidance and revenue-recovery arguments do.

Churn is also severe. Authority exits ran **1,500+/week through 2025, 8% above 2024** ([FreightWaves](https://www.freightwaves.com/news/trucking-company-exits-reach-12-month-high)); ~88,000 authorities were revoked in 2023 ([Commercial Factor](https://magazine.factoring.org/magazine-articles/carrier-amp-broker-failures-in-20242025-and-why-2026-may-bring-one-last-wave)). Q1 2026 was the first net-gain quarter since Q2 2025 ([Trucking Dive](https://www.truckingdive.com/news/carrier-population-shifts-back-toward-growth-quarterly-fmcsa-data-shows/817176/)). Gross logo churn in the addressable base plausibly runs 12–18%/yr regardless of product quality — which argues for a free open-source base with paid customization rather than a subscription that must survive a renewal cycle.

---

## 2. How the work is performed

The back office at a 5–50 truck carrier runs four clocks simultaneously. They are almost entirely disjoint systems, and nobody sells one product that spans them.

### Clock 1 — the weekly settlement and billing cycle

**Monday–Friday, driven by load completion.**

A load arrives as a **rate confirmation** (PDF from a broker, or a customer contract). Dispatch assigns it. The driver runs it and produces a **signed bill of lading / proof of delivery**, plus incidental paper: scale tickets, lumper receipts, toll charges, detention timestamps, fuel-card transactions, and possibly a **Comcheck or fuel advance** drawn against the load before delivery.

Two documents get produced from that pile, on two different clocks:

- **The customer invoice**, which needs invoice + signed POD + rate confirmation at minimum, plus load-specific extras (scale tickets, lumper receipts, appointment confirmations). Payment terms start *"when the broker receives a complete, correct invoice"* with a signed POD — **not on the delivery date** ([O Trucking](https://otrucking.com/resources/guides/broker-payment-terms/)). Net 30 is used by 70%+ of brokers; **average broker days-to-pay is about 33.**
- **The driver settlement statement**, which for a leased owner-operator must be paid **within 15 days after submission of the necessary delivery documents** under [49 CFR 376.12(f)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-376/subpart-B/section-376.12).

**The carrier finances the ~18-day gap between those two clocks.** That is the structural reason freight factoring is near-universal at this fleet size: recourse factoring runs **1–5% per invoice cycle**, non-recourse **3–7%**, with a **5–20% reserve holdback**, and chargebacks trigger when an invoice ages past the recourse period, **often 90 days** ([FreightWaves Checkpoint](https://www.freightwaves.com/checkpoint/recourse-vs-non-recourse-factoring/)). Broker quick-pay is the alternative at **1.5–5%, most commonly 2–3%** ([FreightWaves](https://www.freightwaves.com/news/the-broker-offers-you-quick-pay-and-it-sounds-like-free-money-read-this-before-you-take-it)).

The settlement statement itself assembles from **seven independent input streams that live in seven different systems**: rate confirmations (email/broker portal), fuel card statements (Comdata/EFS/WEX/Pilot/TCH web export), lumper receipts (paper photos), ELD records (Motive/Samsara cloud), toll invoices (state toll authority), insurance documents (agent), and dispatch/load records (spreadsheet or TMS). *"No single system holds all the information"* ([Invoice Data Extraction](https://invoicedataextraction.com/blog/driver-settlement-statement-processing)).

The output is a document with a legally specified shape. Under [49 CFR 376.12](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-376/subpart-B/section-376.12):

| Cite | Requirement |
|---|---|
| **376.12(g)** | If paid on **percentage**, the carrier must give the lessor **a copy of the rated freight bill** at or before settlement. |
| **376.12(h)** | The lease must specify **all chargeback items and how each is computed**, and *"the lessor shall be afforded copies of those documents which are necessary to determine the validity of the charge."* |
| **376.12(k)(1)–(2)** | The lease must state the escrow amount and **the specific items escrow may be applied to**. |
| **376.12(k)(3)** | Escrow accounting either **itemized on individual settlement sheets** or as a **separate monthly accounting**. |
| **376.12(k)(5)** | Carrier must pay escrow interest **at least quarterly**, at a rate ≥ the average yield on **91-day, 13-week Treasury bills**. |
| **376.12(k)(6)** | Escrow returned **no later than 45 days from termination**, with a final accounting. |

### Clock 2 — the quarterly and annual filing calendar

| Filing | Cadence | Consequence of missing |
|---|---|---|
| **IFTA quarterly return** | Last day of the month after quarter close (Apr 30 / Jul 31 / Oct 31 / Jan 31) | **$50 or 10% of net tax due, whichever is greater**, plus interest at IRS §6621(a)(2) + 2 pts (**9%/yr, .0075/mo for 2025 and 2026**), charged **per jurisdiction**; ultimately license revocation |
| **IRP apportioned renewal** | Annual, off a **July 1 – June 30** distance reporting period | Plates not issued |
| **Form 2290 HVUT** | Last day of month following first use (Aug 31 for July) | 4.5%/mo up to 5 months; no stamped Schedule 1 = no registration |
| **UCR** | Annual, opens Oct 1 | Roadside enforcement |
| **MCS-150 biennial update** | Every 24 months keyed to USDOT number digits, **plus within 30 days of a name/address/entity change** | USDOT deactivation; FMCSA cites up to $1,000/day to $10,000 |
| **NY HUT / KY KYU / NM WDT** | Quarterly | State penalties |
| **OR weight-mile** | **Monthly** | State penalties |

A real small-carrier owner's own enumeration of the treadmill: *"Quarterly IFTA filings, NM, NY, KY permits, once a year 2290, UCR, IFTA Renewal IRP, bienial MCS-150"* — TallJoe, [TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/how-come-no-one-mentioned-how-much-work-is-involved-for-authority-audit.1294107/page-6), 22 Nov 2018. In the same thread, TruckRunner on giving up his authority: *"I really just didnt feel like filling out all of that paperwork and jumping through hoops."*

**2026 wrinkle:** FMCSA replaced its legacy registration systems with **Motus** (motus.dot.gov) starting 14 May 2026. Every registrant must re-claim their profile via login.gov identity proofing plus Thomson Reuters CLEAR business verification. It went badly enough that FMCSA **suspended inactivation of USDOT numbers for entities that hadn't completed the biennial update since 1 June 2026**; reported failures include three months of impossible MCS-150 updates and Motus issuing a **brand-new DOT number** to a 24-year-old carrier trying to claim its existing one ([Overdrive](https://www.overdriveonline.com/regulations/article/15828482/fmcsa-suspends-usdot-deactivations-as-motus-issues-mount-for-carriers)).

### Clock 3 — the rolling driver-and-vehicle compliance calendar

Per driver, continuously: CDL expiry; **medical examiner's certificate, max 24 months** (12 for certain conditions); **annual MVR** under 391.25(a) plus a dated **annual review note naming the reviewer** under 391.25(c)(2); the **within-30-days-of-hire** MVR and safety-performance-history investigation under 391.23; the National Registry verification note under 391.23(m); **at least one Clearinghouse query per driver per 12 months** plus a **full pre-employment query** under [49 CFR Part 382 Subpart G](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-382/subpart-G); and inclusion in a random drug/alcohol pool at **50% controlled substances / 10% alcohol for 2026** — unchanged for a sixth year ([Trucksafe](https://www.trucksafe.com/post/fmcsa-keeps-random-drug-alcohol-testing-rates-the-same-for-2026)).

Per vehicle: **396.3(b)(2) requires "a schedule of inspections to be performed, including nature and due date"** — a forward-looking schedule, not a repair history — plus DVIRs retained 3 months, annual 396.17 inspections, and 396.21(b) inspection reports retained 14 months.

FMCSA's own Paperwork Reduction Act estimate for DQ files alone (OMB 2126-0004, [Federal Register 15 Apr 2025](https://www.federalregister.gov/documents/2025/04/15/2025-06345/agency-information-collection-activities-renewal-of-a-currently-approved-collection-driver)): **0.81 million carrier respondents, 14.15 million annual burden hours — about 17.5 hours per carrier per year for driver qualification files by themselves.**

The baseline storage system, described by a compliance vendor without irony: *"everything lives in binders, sticky notes, or someone's head"* ([Fleet Regulators](https://fleetregulators.com/blog/how-to-stay-compliant-without-losing-your-mind)).

### Clock 4 — the four-year evidence archive

Nothing above is finished when it is filed. IFTA requires records **four years following the date the return was due or filed, whichever is later**, plus any period covered by waivers or jeopardy assessments (Procedures Manual P510, [IFTA Procedures Manual eff. Jan 2026](https://www.iftach.org/manuals/2026/PM/Procedures%20Manual%20-%2001-01-26.pdf)). IRP distance records run three years past the close of the registration year, which Minnesota states plainly as **5½ years in practice** ([MN DPS](https://dps.mn.gov/divisions/dvs/business/irp-and-ifta/irp-and-ifta-audit/irp-and-ifta-audit-record-keeping-requirements)). DQ files: employment + 3 years. Drug/alcohol positives and refusals plus **random selection records: 5 years**. RODS and supporting documents: 6 months.

And the burden of proof is explicit — IFTA P520: *"In an IFTA audit, the burden of proof is on the licensee. The audit will be completed using the best information available to the base jurisdiction."*

### Software actually in use

| Category | What small carriers pay | Source |
|---|---|---|
| **ELD (mandatory)** | Motive ~$20–50/veh/mo + ~$150 hardware, 12-mo min; Samsara ~$27–33/veh/mo + $99–548 hardware, **36-month term typical with auto-renewal**; Matrack $14.95–19.95 month-to-month | [Small Fleet HQ](https://smallfleethq.com/elds/motive-vs-samsara), [AI-ELD](https://ai-eld.com/insights/how-much-does-an-eld-cost-2026) |
| **TMS (discretionary)** | TruckingOffice **$25 (1–2 trucks) / $55 (3–7) / $90 (8+)** per month, no per-user fee; TruckLogics $36–225/mo by band; Tailwind $99/user/mo; Truckbase **$290/mo minimum billed annually**; Q7 $49–129/user/mo + $1,000–5,000 implementation; McLeod five- to six-figure annual | [TruckingOffice](https://www.truckingoffice.com/pricing/), [Truckbase](https://www.truckbase.com/trucking-software-pricing), [ITQlick](https://www.itqlick.com/q7-trucking-business-software/pricing), [BestCarrierTMS](https://bestcarriertms.com/tms-pricing-guide.php) |
| **Accounting** | QuickBooks Online $38 / $85 / $140 / $340 per month | [QuickBooks](https://quickbooks.intuit.com/pricing/) |
| **Compliance** | J.J. Keller Encompass **$25.50/truck/mo** BYOD, **$59** on their tablet, DQ/D&A/training quoted separately; DOTDriverFiles **$50/driver/yr**; My Safety Manager managed **$49/driver/mo**; category average **$300/mo for 1–19 drivers** | [Dockex](https://dockex.io/vs/jj-keller), [DOTDriverFiles](https://dotdriverfiles.com/pricing/), [AvatarFleet](https://www.avatarfleet.com/blog/how-much-does-driver-compliance-software-cost) |
| **IFTA filing service** | $30–100 per truck per quarter (Motor Carrier HQ $320/yr all four); IFTA Plus **$39/$69/$99/$129 per quarterly filing** by fleet band | [Motor Carrier HQ](https://www.motorcarrierhq.com/ifta/), [IFTA Plus](https://www.iftaplus.com/pricing) |
| **Fuel/D&A** | DOT drug-testing consortium ~$55.95/driver; MVRs ~$10 median, $3–$25 by state; **Clearinghouse queries $1.25 flat** | [Consortium Pool](https://consortiumpool.com/cdl-drug-testing/), [FMCSA Clearinghouse](https://clearinghouse.fmcsa.dot.gov/Resource/Index/Query-Plan) |

A realistic 15-truck stack runs **$1,000–$1,500/month, or $67–$100 per truck per month** — which, per the margin arithmetic above, is the entire per-truck profit.

The competition is therefore not another TMS. **It is a spreadsheet plus QuickBooks plus a CPA**, and that position is publicly defended by practitioners and by trade press: Adam Wingfield in FreightWaves, 9 Aug 2025, *"How to Use a Single Spreadsheet to Manage 90 Percent of Your Trucking Business"* — **"You don't need ten apps, a TMS subscription, or another software pitch to get your trucking business in order."** ([FreightWaves](https://www.freightwaves.com/news/how-to-use-a-single-spreadsheet-to-manage-90-percent-of-your-trucking-business))

---

## 3. Most important problems, ranked

### Problem 1 — Two Clearinghouse queries per driver per year, at $1.25 each, are the #1 and #2 most expensive routine audit findings in the country

**Who:** the office manager or owner, for every driver hire and on each driver's annual anniversary.
**When:** pre-employment (before the driver performs any safety-sensitive function) and at least once per 12 months thereafter.
**Currently handled:** manually, on a calendar reminder or not at all. Query results must be retained **3 years**; reporting deadlines run to close of business on the **third business day**.
**Why inadequate:** it is a pure calendar-and-evidence task with no natural forcing function. Nothing breaks when it is missed. It surfaces only at audit.

**Evidence — this is the strongest quantified finding in the report.** Analysis of **>50,000 FMCSA violations through June 2025** ([US Compliance Services](https://uscomplianceservices.org/what-50000-fmcsa-violations-tell-us-about-carrier-compliance-in-2025/)):

| Violation | Count (H1 2025) | Average penalty |
|---|---:|---:|
| §382.701(b)(1) **no annual Clearinghouse query** | 2,471 | **$10,278** |
| §382.701(a) **no pre-employment Clearinghouse query** | 2,696 | $7,736 |
| §382.301(a) used driver before pre-employment result | 1,050 | $10,654 |
| §395.8(e)(1) false RODS | 2,241 | $9,018 |
| §382.711(b) carrier not registered in Clearinghouse | 1,057 | $5,072 |
| §396.3(b)(2) **no system showing when maintenance is due** | 1,204 | $2,040 |

J.J. Keller, analyzing FMCSA audit data 2021–2025: *"failing to request a Clearinghouse query when required accounted for almost 10 percent of all audit violations cited by the FMCSA since 2021"* — pre-employment query, annual query, and registration are the **#3, #4 and #5 most-cited audit violations**. Their stated cause: *"The administrative tasks…can fall through the cracks."* ([J.J. Keller DataSense](https://www.jjkellerdatasense.com/driver-insights/clearinghouse-violations-during-audits))

**Frequency:** twice per driver-year minimum, so 20–60 events/yr at this fleet size.
**Cost:** $7,736–$10,654 per finding, against a $1.25 task and roughly 5 minutes of labor. Enforcement is aimed directly at this segment: in FY2020, **over 80% of all FMCSA audits hit carriers with ≤20 trucks and 53.6% hit carriers with ≤6 trucks**, with offsite audits rising from 0.5% of audits in 2017 to 50.3% in 2020 and **documents due within 48 hours** ([Overdrive](https://www.overdriveonline.com/regulations/article/15063877/owneroperators-remain-in-crosshairs-of-dots-offsite-reviews)).

There is a compounding pressure: as of 2 January 2026, **328,431 CDL/CLP holders have violations on record and 202,345 are in "prohibited" status**, of whom **159,226 (78.7%) have never started return-to-duty** ([FreightWaves](https://www.freightwaves.com/news/the-industry-is-focused-on-200000-non-domiciled-cdls-but-there-is-another-200000-driver-story-nobody-is-covering)). A practitioner reports roughly **15% of former-CDL applicants come back "prohibited"** (brian991219, [TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/driver-qualification-file.2504647/), 22 Mar 2024). Since 18 November 2024, Clearinghouse-II requires state licensing agencies to **downgrade the CDL** of any prohibited driver.

### Problem 2 — IFTA/IRP records that were never audit-grade, and the 4 MPG default assessment

**Who:** whoever files the quarterly return — owner, office manager, or a $30–100/quarter outside service.
**When:** quarterly, with a four-year lookback.
**Currently handled:** trip envelopes and Excel, handwritten odometer readings at state lines, consumer GPS, or an ELD vendor's IFTA report — plus a fuel-card quarterly export for gallons. Verbatim from [TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/anyone-have-a-good-program-or-spreadsheet-for-ifta-irp-miles.332629/page-2): *"I use trip envelopes and add up state mileages on the back... Enter those into excel"* (gokiddogo, 14 Jan 2017); *"use google sheets, then its already in a spreadsheet...Cost 0$"* (skallagrime, 7 Feb 2024).

**Why inadequate — the non-obvious structural finding:** an HOS-compliant ELD record is **legally incapable** of satisfying IFTA's GPS record specification.

| | IFTA P540.200 / IRP (2024) | 49 CFR 395 App. A (ELD) |
|---|---|---|
| Lat/long precision | **≥4 decimal places (~11 m)** | **hundreds of a degree** (2 decimals, ~1 mi) — §4.3.1.6 |
| Precision during personal conveyance | (no relief) | **tenths of a degree** (~10 mi) — §4.7.3 |
| Recording cadence | **every 10 min** (IFTA) / **15 min** (IRP), engine on | duty-status changes + intermediate log **once per hour** in motion |
| Odometer | **ECM odometer at each reading** | accumulated miles since power-on, whole miles |

Sources: [IFTA Procedures Manual 2026](https://www.iftach.org/manuals/2026/PM/Procedures%20Manual%20-%2001-01-26.pdf), [IRP Audit Reference & Best Practices 1/10/24](https://cdn.ymaws.com/www.irponline.org/resource/resmgr/audit_prog2/audit_best_practices_1_10_24.pdf), [eCFR 49 CFR 395 App. A](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-395/appendix-Appendix%20A%20to%20Subpart%20B%20of%20Part%20395). J.J. Keller translates ELD precision to *"approximately within a one-mile radius"* on duty, *"approximately within a 10-mile radius"* on personal conveyance ([J.J. Keller](https://jjkellercompliancenetwork.com/regsense/what-is-the-level-of-precision-for-commercial-motor-vehicle-cmv-location-information-recorded-by-an-electronic-logging-device-eld)). The IRP audit guide also explicitly **rejects PDF, JPEG, PNG and Word** as acceptable record formats — a screenshot of an ELD IFTA screen is not a record.

**Cost of failure.** IFTA Audit Manual A550.100: *"in the absence of adequate records, a standard of 4 MPG/1.7KPL will be used"* ([Kansas IFTA Audit Manual](https://www.ksrevenue.gov/pdf/mfiftaam.pdf)). Indiana states the practical form: *"Miles per gallon reduced to 4.0 or by 20%"* plus *"Tax-paid fuel credits disallowed without receipts"* plus a *"20% of registration fees"* assessment ([Indiana DOR](https://www.in.gov/dor/motor-carrier-services/files/audit-tips.pdf)). A truck actually getting 6.5 MPG reassessed at 4.0 has its taxable gallons inflated ~62% while credits stay flat. IRP's inadequate-records ladder is **20% of apportionable fees (1st offense), 50% (2nd), 100% (3rd)** ([CA DMV IRP Ch.9](https://www.dmv.ca.gov/portal/handbook/irp/chapter-9-audits)). Minnesota's warning: *"Assessments for inadequate or unavailable records may exceed $10,000 per vehicle."*

**Frequency of exposure.** Jurisdictions must audit **an average of 3% of accounts per year** for both IFTA and IRP (A310), with sub-quotas of ≥15% low-distance and ≥25% high-distance accounts. In practice they under-deliver: Connecticut's [2024 Finding of Non-Compliance](https://www.iftach.org/committee/CT%202024%20Final%20Determination%20Finding%20of%20Non-Compliance.pdf) shows 239 of 357 required audits completed 2019–2023 (**2.01%**). So a given carrier's annual audit probability is on the order of 1-in-40 to 1-in-50 — but the lookback when it comes is four years.

**The audit-selection algorithm is public, and a clean spreadsheet is itself a flag.** A poster claiming to have written Indiana's audit-selection software listed the criteria ([TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/criteria-used-for-ifta-irp-audit-selection.213213/), 14 May 2013): everything ending in 5 or 0; identical reported miles/gallons quarter to quarter; **MPG over 7**; MPG not following a seasonal pattern; **MPG varying more than 1.0 between quarters**; sudden drops or zero returns; non-taxable miles; not filing. In the same thread another poster observed of carriers using reporting services that *"many of them have the same MPG from quarter to quarter."*

Real assessments: PSM379 reported an initial **$9,000** reduced to **$4,200** after producing debit-card fuel statements; Ruthless reported an auditor who called his records *"the best records he had seen in 20+ years"* and still assessed, *"in the state's favor for a modest sum, with no way for me to prove otherwise"* ([TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/ifta-irp-audit.2344493/), 6 Sep 2021).

And the ELD vendor's report is widely reported as unusable: *"Mine aren't even close to reality. Between states not even listed on the report, to wild discrepancies in actual miles driven in any particular state…always short miles. I'm talking thousands of miles missing over a 30,500 mile quarter."* (Concorde, 28 Jul 2022, [TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/big-road-%E2%80%9Cfleet-complete%E2%80%9D-ifta-mileage-report.2436550/)). And from an actual audit: *"elog data wasn't able to be used and the auditor allowed me to recover data from my old gps unit"* (dirthaller, 7 Feb 2024).

Samsara's own documentation confirms silent failure modes: *"By default, vehicle fuel type is Unspecified until you Edit Fuel Type"*, reports available only on the second day of the following month, and **DC excluded** ([Samsara KB](https://kb.samsara.com/hc/en-us/articles/360046354291-IFTA-Report)). Motive states plainly: *"Motive doesn't automate IFTA fuel tax filing"* ([Motive](https://gomotive.com/products/features/ifta-reporting-automation/)).

### Problem 3 — The settlement statement is a regulated legal artifact that no affordable product produces

**Who:** the settlement clerk or owner, weekly.
**When:** every pay cycle, for every leased owner-operator and driver.
**Currently handled:** Excel or Google Sheets. The archetypal thread: a carrier asks for settlement software, cites that *"QuickBooks requires significant setup time"* and that payroll companies charge fees, and **accepts a free Google Sheets template instead** ([TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/settlement-software.292165/)). The QuickBooks community's own answer to an owner-operator asking how to enter weekly settlements: *"if you are an OTR owner/operator you really need specialized software"* ([Intuit Community](https://quickbooks.intuit.com/learn-support/en-us/reports-and-accounting/i-am-an-owner-operator-simi-truck-driver-i-need-to-enter-weekly/00/485796)) — QuickBooks has no concept of a settlement, a single document bundling multiple load revenues against multiple vendor deductions.

**Why inadequate:** the statement carries federal obligations a spreadsheet cannot enforce, and the failures are litigated. *OOIDA v. Landstar* (11th Cir.) held that catch-all lease language like "third party fees" gives insufficient notice under 376.12(h), and drew the operative distinction: flat-fee chargebacks need only be verifiable on the statement, but **variable-rate chargebacks with markup require disclosing the third-party cost** ([Benesch](https://www.beneschlaw.com/insight/interconnect-flash-no-6-ooida-landstar-upon-further-review/)). *OOIDA v. Swift* produced declared violations of **376.12(h)** (deductions exceeding carrier cost, undisclosed) and **376.12(k)(2)** (unspecified escrow application) ([FMCSA final order](https://www.fmcsa.dot.gov/sites/fmcsa.dot.gov/files/2024-10/OOIDA%20v%20Swift%20Final%20Order.pdf)).

OOIDA practitioner commentary ([Land Line](https://landline.media/magazine/your-rights-regs/)): Tom Crowley on escrow — *"some will fabricate some deductions from that escrow fund"*; on chargebacks — *"The carrier just says 'hey we paid for this we're going to charge you for this'"*; on the 15-day rule — *"Any time the carrier is going past the 15 days to get paid, those are the flags to look for."*

**The market evidence is unusually clean.** Rigbooks is the cheapest, most small-fleet-focused accounting product in the category at $19–$149/mo — and its pricing page states: *"Do you need **1099 Driver Settlements, Fuel Card Imports, Bank Statement Imports**, or Scheduled Maintenance Plans? Please contact sales"* ([Rigbooks](https://www.rigbooks.com/pricing)). Customer *invoicing* is included in every published tier. **Driver settlement is not.**

**Frequency:** 52 cycles/yr × 8–35 drivers.
**Cost:** the enumerated error taxonomy is specific — missing loads at period boundaries; linehaul not matching the rate con; practical-vs-shortest mileage gaps; **one driver's fuel purchase appearing on another driver's settlement**; lumper deductions posted without the offsetting reimbursement; detention collected from the broker but not passed through; recurring deductions charged after the contract changed; and vague *"miscellaneous deductions"* — which is itself a direct 376.12(h) violation ([Invoice Data Extraction](https://invoicedataextraction.com/blog/driver-settlement-statement-processing)).

The mileage-basis dispute alone is worth 8–10%: odometer miles exceed paid miles by that margin, and a Wisconsin→New York load short by **100 miles ≈ $250** ([Overdrive](https://www.overdriveonline.com/overdrive-extra/article/15768772/why-are-carriers-shippers-still-using-short-miles-to-pay-truckers)). On percentage pay, drivers report an inability to verify at all: *"Really easy to photoshop a rate con to show lower rate to driver than actual rate. This happened to me at multiple carriers."* (Kenworth6969) and *"Yes they have to show you what they billed the customer... Keep in mind they do nt like that and it will most likely result in your dismissal"* (NightWind), with gentleroger quantifying the skim at **$1,000–1,500 per truck per year** for a 1% shave ([TruckersReport 1](https://www.thetruckersreport.com/truckingindustryforum/threads/percentage-pay-how-to-know-if-they-are-cheating-you.2504427/), [TruckersReport 2](https://www.thetruckersreport.com/truckingindustryforum/threads/rates-legality-of-disclosure.2493787/)).

There is also a hard state-law layer nobody appears to serve. **California Labor Code 226** requires wage statements to separately identify, for piece-rate/mileage drivers, **productive time, non-productive time (inspections, waiting, fueling, paperwork), and paid rest-break time** — *"A pay stub that shows only a mileage total does not meet this requirement"* ([Trucking Payroll](https://www.truckingpayroll.com/2026/06/19/california-truck-driver-pay-stub/)). California also holds the largest concentration of target carriers (7,210 of 69,511).

### Problem 4 — Accessorial charges, especially detention, are earned and then never collected

**Who:** driver in the field, office manager at invoicing.
**When:** every load with a wait.
**Currently handled:** the driver texts a photo or writes times on the BOL; the office manager may or may not invoice it; the broker may or may not pay.
**Why inadequate:** ATRI data via [Innovative Small Carrier Services](https://innovativelogisticsgroup.io/profitability-and-cost-control/driver-detention-costs-the-industry-15-billion-a-year-how-small-carriers-build-a-real-accessorial-strategy-in-2026/): detention costs the industry **$15.1B/year** and **less than half of detention invoices actually get paid**. Disciplined process moves recovery to **75–85% within three months**. Free time is 2–3 hours; detention runs **$25–$100/hr**; the documentation burden is **10–15 minutes per load**. A **five-truck fleet example recovers ~$18,000/yr** at two events/truck/month × three excess hours.

**Frequency:** ATRI's 2026 data puts truckload dwell at **1.71 hours per stop** — this is a per-load event.
**Cost/evidence:** brokers reject on documentation. ZVar: brokers claim *"the bond only covers cartage fees. It doesn't cover accessorial fees like detention, tonu, etc."*; Judge describes keeping **a printer in the truck** to staple a rate con copy to every invoice; DUNE-T: *"I was screwed on detention quite a few times by XPO brokers, they simply said customer did not approve the detention."* ([TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/how-to-get-brokers-to-actually-pay-detention.2145331/page-2))

### Problem 5 — Document-expiry and filing-calendar tracking across drivers, vehicles and jurisdictions

**Who:** office manager. **When:** continuously.
**Currently handled:** spreadsheets, binders, calendar reminders, sticky notes.
**Why inadequate:** existing DQ software *"struggles to integrate expiration tracking with missing document alerts simultaneously"* — it tells you a med card expires but not that the road-test certificate was never collected ([My Safety Manager](https://www.mysafetymanager.com/driver-qualification-file-software/)).

**Cost:** at a compliance review, a "critical" violation requires a pattern of **≥10% of records examined**, which for a 10-truck carrier is **one driver's file out of ten** ([Idealease](https://www.idealease.com/safety-bulletins/fmcsa-has-contacted-me-compliance-review-0)). Foley calls the 391.23 previous-employer investigation *"the single most common DQF finding"* and reports **3,172 FMCSA violations in 2025 for expired or missing DOT medical certificates** ([Foley](https://www.foleyservices.com/articles/dqf-audit-checklist/)).

**Two live 2026 complications.** First, **391.27 (the driver's annual certificate of violations) has been removed** — the section is `[Reserved]` as of the Record of Violations final rule effective 9 May 2022 ([Federal Register](https://www.federalregister.gov/documents/2022/03/09/2022-04930/record-of-violations)) — yet a large fraction of 2026 checklists and vendor templates still list it. Second, the **NRII rule (effective 23 June 2025)** makes the CDLIS MVR, not the paper card, the source of truth for CDL holders' medical certification; because states lagged, FMCSA has issued serial paper-MEC waivers, the current one **effective 11 April 2026 and expiring 11 October 2026**, allowing paper reliance for up to 60 days from issuance, with **Alaska, California, Kentucky, Louisiana and New Hampshire still non-compliant** and FMCSA warning states not to expect further nationwide waivers ([FMCSA NRII waiver notice](https://nationalregistry.fmcsa.dot.gov/assets/documents/nriilearningcenter/NRII%20Waiver%20Oct%2011%202026.pdf)).

A 10-truck carrier now has to know, per driver, which state issued the CDL, whether that state is NRII-compliant, and therefore whether the paper card is acceptable evidence and for how many more days. That is a versioned rules table, not a reminder.

**How the penalty is computed** — the most useful and least-known primary document is FMCSA's **Uniform Fine Assessment 4.0** manual: `[(Range Max − Range Min) × Violation Factor + Range Min] × (1 + Case Factor) × 80% if small business`, capped at 2% of gross revenue, where Case Factor includes **−20 if corrected before investigation** and −10 if corrected before Notice of Claim ([UFA User Manual](https://www.fmcsa.dot.gov/sites/fmcsa.dot.gov/files/docs/ATTACHMENT-A_UFA-UserManual%20508%20compliant_0.pdf)). **That −20 credit is a direct, quantified economic argument for self-audit tooling.**

### Problem 6 — Fuel surcharge schedules go stale and nobody can audit the pass-through

**Who:** owner (negotiating), office manager (applying), driver (disputing).
**When:** every load, recalculated weekly.
**Currently handled:** a number typed into a rate sheet years ago, or a per-customer bracket table read off a PDF.
**Why inadequate:** FSC is a **per-carrier, per-week, per-lane bracket lookup**, not one formula. The live artifact: the [Estes/EFW Weekly Fuel Surcharge Letter for 08/05/2026–08/11/2026](https://efwnow.com/wp-content/uploads/2026/08/Weekly-Fuel-Surcharge-Letter-08.05.2026-08.11.2026.pdf) references DOE diesel at **$5.348**, sets Economy FSC at **46.50%**, and publishes a bracket table spanning $1.10–$7.00+/gal mapping to 4.50%–63.00%.

The index is the **EIA/DOE Weekly U.S. No. 2 Diesel Retail On-Highway price**, released Mondays ([EIA](https://www.eia.gov/petroleum/gasdiesel/)). Current level and recent volatility: **$5.348 (8/3/2026)**, $5.313 (7/27), $5.134 (7/20), **$4.796 (7/13)**, $4.578 (7/06). A **$0.77 swing in four weeks.**

OOIDA's formula: `FSC/mi = (current DOE price − base/peg) ÷ assumed MPG`, with ~6 MPG loaded, and the position that *"good carriers will typically pass through 100% of the fuel surcharge to their leased-on owner-operators"* — *"Make sure your lease-agreement includes the 100% pass through"* ([OOIDA](https://www.ooida.com/trucking-tools/fuel-surcharge-calculator/)).

**Cost:** a formula built at $3.50 diesel adding $0.30/mi leaves a **$0.20+/mi gap** at today's prices — **$100 on a 500-mile load** ([Truckstop](https://truckstop.com/blog/how-to-negotiate-fuel-surcharges/)). At 86,000 mi/truck/yr that is on the order of **$17,000 per truck per year**, though real exposure is lower since not all miles are loaded and revenue-generating. Even a fraction of that dwarfs any software cost in this market.

Drivers cannot audit it and default to assuming theft — instructively, in one dispute the driver's suspicion was arithmetically *wrong*: griemar suspected his carrier of skimming by computing `Load Pay = Truck Gross ÷ 1.12` rather than subtracting 12%, and another poster demonstrated the divisor method actually **favored** the driver ([TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/fsc-is-this-legal.298781/)). The problem is verifiability, not necessarily fraud.

### Problem 7 — Fuel-card CSV exports are non-standard and lose exactly the fields IFTA and settlement need

**Who:** office manager, weekly and quarterly.
**Currently handled:** copy-paste between the fuel network's export and whatever template downstream.
**Evidence:** in TruckingOffice's own support forum, Roy Sansbury: *"Having to copy and paste from the pilot excel to the tms template is very tedious"* — the vendor had to hand-build a Pilot-specific importer. Chuck Brewster separately complained the standard import template **drops invoice numbers, price per gallon, DEF, oil, anti-freeze and transaction details**, and asked for customizable column mapping across vendors ([TruckingOffice support](https://help.truckingoffice.com/hc/en-us/community/posts/4404375840276-PILOT-FUEL-CARD-CSV)).

**Why it matters twice:** the dropped fields are exactly the ones IFTA cares about (jurisdiction of purchase, fuel type separating taxable diesel from DEF and reefer fuel, unit number) and exactly the ones settlement cares about (which driver, which truck, price per gallon for chargeback verification under 376.12(h)). Off-road diesel, reefer fuel and APU fuel wrongly claimed as tax-paid gallons is a named audit finding ([CNRG Fleet](https://cnrgfleet.com/ifta-reporting-guide-what-to-do-when-your-mileage-and-fuel-records-dont-match-up/)).

### Problem 8 — Invoice packets get rejected, and non-recourse factoring does not cover the common causes

**Who:** office manager. **When:** every invoice.
**Evidence:** ten enumerated causes of billing delay — missing POD; illegible/incomplete POD images; rate mismatch vs. the broker confirmation; manual rekeying errors; **accessorial charges not documented**; missing customer-specific documents (scale tickets, appointment confirmations); late driver paperwork; loads parked in an undefined "problem loads" queue; disconnected systems; end-of-period backlogs ([Carrier1](https://carrier1.com/blog/faster-billing-for-carriers-10-reasons-invoices-get-delayed)).

**Why it costs more than it looks:** non-recourse factoring's coverage is narrow — it covers debtor insolvency during the contracted window and **explicitly excludes "Disputes, short-pays, offsets, missing or late proof of delivery, delivery errors, and fraud"** ([FreightWaves Checkpoint](https://www.freightwaves.com/checkpoint/recourse-vs-non-recourse-factoring/)). So the most common rejection causes revert to the carrier regardless of program type, the reserve holdback (5–20%) stays trapped, and an invoice aging past the ~90-day recourse window becomes a full chargeback against the next funding.

*Evidence gap: I could not find a primary source putting a dollar figure on a single rejected freight invoice. This is inferred cost, not measured cost.*

### Problem 9 — Preventive maintenance schedules that satisfy the letter of 396.3(b)(2)

**Evidence:** **1,204 violations of §396.3(b)(2) — "no system showing when maintenance is due" — in the first half of 2025 alone, averaging $2,040.** The regulation demands a *forward-looking schedule with due dates*, not a repair history; break-fix records plus a shoebox of invoices satisfy 396.3(b)(3) and fail 396.3(b)(2). An FMCSA investigator's actual finding, quoted by the carrier: the *"maintenance program only fixed broken items rather than following preventative protocols"* (Riprap, [TruckersReport](https://www.thetruckersreport.com/truckingindustryforum/threads/compliance-review-not-new-entrant.352105/page-2), 10 Mar 2017).

This one is notable because **Fleetio exists at $4/vehicle/month and Whip Around at $5/asset/month** and the market is still failing at it — which suggests the barrier is adoption friction and setup, not price.

### Problem 10 — Random drug/alcohol selection evidence the carrier does not hold

Small carriers must join a consortium/C-TPA because a 50% annual rate on a 5-driver pool is arithmetically absurd; the rate applies to the **consortium pool**, not the member. But the evidentiary burden stays with the carrier: *"You need your own retrievable copy of every random selection record, or a written agreement confirming your C/TPA will produce records on request"* ([Foley](https://www.foleyservices.com/articles/basics-of-drug-alcohol-testing-recordkeeping/)). Random selection records are a **5-year retention** item under Part 382 Subpart D. Named audit findings: below-rate testing; **year-end clustering** (bunching selections into one quarter violates the "spread reasonably throughout the year" rule *even if the annual total is met* — "auditors specifically look for it"); new hires not added to the pool on day one; selected-then-separated drivers never tested ([Foley](https://www.foleyservices.com/articles/dot-random-drug-test-frequency/)).

---

## 4. Application opportunities

Nine focused concepts, plus two deferred. Pricing context throughout: the ceiling is roughly **$25–$40 per truck per month for anything discretionary**, and higher only where the product displaces a named line item or avoids a named fine.

---

### 4.1 QueryGuard — Clearinghouse and DQ obligation ledger with evidence attachment

**Intended user:** office manager or owner at a 5–50 truck carrier.
**Problem solved:** Problems 1 and 5 — the two cheapest tasks in trucking ($1.25 Clearinghouse queries) are the two most expensive audit findings, and DQ software tracks expiry but not completeness.

**Current workflow:** a spreadsheet with driver names and med-card expiry dates, a calendar reminder for annual queries, and a filing cabinet or shared folder of scanned PDFs. At audit, the office manager assembles a packet by hand under a 48-hour clock.

**Proposed workflow:** one driver record per driver. The tool holds the **current** 391.51(b) obligation list (correctly omitting the removed 391.27), computes each obligation's next-due date from its own recurrence rule, and requires an attached file as evidence of completion. It distinguishes three states per obligation — *satisfied with evidence*, *due*, and **never collected** — which is precisely the gap the incumbents leave. It generates a dated, indexed audit packet on demand and a per-driver completeness report.

**Inputs:** driver roster (name, hire date, CDL number, issuing state, CDL expiry); uploaded PDFs/images of MVRs, med certs, road test certs, applications, Clearinghouse query confirmations, annual review notes.
**Outputs:** a rolling deadline list; a per-driver completeness report; an audit packet (indexed PDF or zip with a manifest); a CSV export.

**Essential features:** the 391.51(b) obligation model with recurrence rules; the 391.23 **30-day-from-hire** clock for the MVR and safety-performance-history investigation; the 391.25(c)(2) annual review note requiring a named reviewer and date; the 391.23(m) National Registry verification note; the **391.53 Driver Investigation History File as a separate, access-restricted store** (insurers may see most of it but not the alcohol/controlled-substances data); Clearinghouse pre-employment and annual query tracking with the 3-year retention clock; retention-clock enforcement including the 391.51(d) three-year purge allowance; and the **NRII paper-MEC acceptability table keyed to CDL issuing state and current waiver expiry**.

**Deliberately excluded from v1:** MVR ordering (that is a paid data integration and a licensing question); Clearinghouse API integration (FMCSA requires per-employer accounts and C/TPAs cannot buy queries on the employer's behalf); driver recruiting/applicant tracking; training/LMS; anything touching vehicles.

**AI:** **inappropriate.** Every rule here is a deterministic date computation from a published regulation. Adding a model would introduce non-determinism into an audit artifact. The one defensible optional use is OCR to read an expiry date off a scanned med card, and even that should be operator-confirmed.

**Why a spreadsheet won't do:** a spreadsheet can hold expiry dates. It cannot enforce that the road-test certificate was ever collected, cannot maintain two files with different access rules and different retention triggers, cannot evaluate paper-MEC acceptability against a state-by-state waiver table, and cannot produce a manifest proving what existed on what date.

**Complexity:** small. **Learning difficulty:** under 30 minutes — it looks like a checklist.
**Value:** avoids findings averaging **$7,736–$10,654** each, plus the UFA **−20 "corrected before investigation"** credit. At 20 drivers the annual DQ burden is a meaningful fraction of FMCSA's 17.5 hrs/carrier/yr estimate.
**Risks and constraints:** this stores driver PII including medical certification. **49 CFR §40.321 prohibits releasing individual drug/alcohol test results or medical information to third parties without the employee's specific written consent** — a SaaS handling this data is a "service agent" and inherits that obligation directly, making any casual "share driver files with your broker" feature a federal violation rather than a privacy-policy question. California's CCPA/CPRA is the binding state regime because it is the only comprehensive state law covering employees, and California holds the largest concentration of target carriers. **Design implication: local-first or self-hosted by default, encrypted at rest, no third-party sharing surface.**
**Existing substitutes:** Foley (no published pricing), J.J. Keller Encompass ($25.50–$59/truck/mo plus quoted modules), Tenstreet (which acquired DriverReach in March 2025 — the two named competitors are now one company; benchmarked at $300–$2,500+/mo), DOTDriverFiles ($50/driver/yr — the clearest low-end price), My Safety Manager ($49/driver/mo managed).
**Why still attractive:** the incumbents split into person-side and asset-side silos and price for 50+ trucks; the category average is $300/mo for 1–19 drivers. A free, local-first, correctness-first tool that ships the *current* rule list (no 391.27) and models NRII state acceptability is differentiated on accuracy, not features.
**Paid customization:** per-carrier obligation sets for HM, passenger, or intrastate operations; state-specific additions; integration with an existing C-TPA's export format; branded audit packets; migration from binders.

---

### 4.2 MileVault — compliance-grade distance archive and multi-jurisdiction filing pack

**Intended user:** owner or office manager who files IFTA/IRP in-house, or the outside filing service that serves 20 such carriers.
**Problem solved:** Problem 2 — the source records that survive an audit live in an ELD vendor's cloud on the ELD vendor's retention schedule, at a precision the regulation does not accept, while the carrier owes four years (IFTA) to 5½ years (IRP) of defensible records with the burden of proof on itself.

**Current workflow:** pull the ELD vendor's IFTA report each quarter, pull the fuel card's quarterly export, key both into a spreadsheet or a $39–$129 filing service, file, and hope.

**Proposed workflow:** ingest the raw telematics ping stream (not the derived report) on a schedule; store it locally in a normalized archive with the elements the regulation names — **date/time, latitude and longitude to ≥4 decimal places, ECM odometer reading, vehicle unit number**; classify each ping to a jurisdiction; produce per-vehicle monthly summaries by jurisdiction; and generate, from that one dataset, the several filings that need it.

**Inputs:** telematics/GPS export (vendor CSV or API); fuel-card transaction file; vehicle roster with fuel type and weight; the IFTA quarterly tax-rate matrix.
**Outputs:** IFTA quarterly return worksheet with total/non-IFTA/IFTA/taxable mile buckets and separate surcharge lines; **IRP renewal distance schedule on the July 1–June 30 reporting period, organized by equipment number and jurisdiction**; NY HUT, KY KYU, NM WDT quarterly worksheets and OR monthly; and an **auditor export in XLS/XLSX/CSV** — the exact deliverable the IRP audit guide demands and the format in which it explicitly rejects PDF, JPEG, PNG and Word.

**Essential features:** the four-bucket mile taxonomy (total / non-IFTA / IFTA / taxable) with the rule that exempt miles stay in *total* miles even when out of *taxable* miles; surcharge-jurisdiction handling where no tax-paid-gallon credit is allowed against the surcharge; per-jurisdiction bulk-fuel and receipt tracking; retention-clock enforcement to 4 and 5½ years; and the correct IRP reporting period, since **"use of incorrect reporting period" is its own audit finding code (11.015)** and **"IFTA Quarterly Fuel Use Tax Schedules are not acceptable summaries for IRP audit purposes"** ([CA DMV IRP Ch.10](https://www.dmv.ca.gov/portal/handbook/irp/chapter-10-recordkeeping/), [Ch.11](https://www.dmv.ca.gov/portal/handbook/irp/chapter-11-common-errors-found-in-audits/)).

**Deliberately excluded:** actually e-filing with any jurisdiction; route optimization; dispatch; anything resembling a TMS; real-time tracking.

**AI:** **inappropriate** for the core. Jurisdiction assignment from coordinates is a geospatial point-in-polygon problem with a right answer. The one place a model could earn its place is reconciling ambiguous fuel receipts (faded scans, missing jurisdiction) — and that is better framed as an optional OCR assist with mandatory human confirmation.

**Why a spreadsheet won't do:** the volume is wrong by orders of magnitude. A 10-minute ping cadence on 20 trucks running 10 hours a day generates ~1.2 million rows per year, and it must be queryable four years later.

**Complexity:** medium — the hardest build in this set. **Learning difficulty:** a few hours, mostly one-time setup of vehicle and vendor mappings.
**Value:** avoids assessments that Minnesota warns "may exceed $10,000 per vehicle," 4 MPG default recomputation across a 4-year lookback, and the IRP 20/50/100% fee-assessment ladder. Displaces $30–$100 per truck per quarter of filing-service fees.
**Risks:** telematics vendor export formats change and some vendors do not expose raw pings at all — that is the central feasibility risk and must be validated first (see section 6). Storage of position data is itself a privacy consideration; drivers' location histories are sensitive.
**Existing substitutes:** ELD vendor IFTA modules (Motive explicitly *"doesn't automate IFTA fuel tax filing"*; Samsara's report has documented default-misconfiguration and stale-data issues); ExpressIFTA ($14.90/filing, but *"does not track your miles or fuel purchases"*); IFTA Plus (which prices NY HUT and NM WDT as **separate SKUs at $15–$47 each**); ProMiles, which practitioners identify as the tool auditors themselves use.
**Why still attractive:** nothing surveyed advertises **retaining the raw ping stream for the full retention period and exporting it in the format an auditor demands.** TMS vendors store derived jurisdiction totals; the source records live in a vendor cloud, and carriers churn ELD vendors. The audit-survival artifact is the raw archive, and it is the thing most likely to be lost.
**Paid customization:** vendor-specific ingest adapters; multi-carrier tenancy for filing services; state-specific worksheet formats; historical backfill and archive migration.

---

### 4.3 IFTA Pre-Filing Linter — anomaly check against the auditor's own selection criteria

**Intended user:** anyone about to file an IFTA return — carrier, bookkeeper, or filing service.
**Problem solved:** Problem 2's selection layer. Audit selection is algorithmic and the criteria are known, but no surveyed tool checks a return against them before submission.

**Current workflow:** file and hope.

**Proposed workflow:** paste or upload the return's per-jurisdiction miles and gallons for this quarter and the prior four to eight quarters. The tool runs a fixed rule set and returns a ranked list of flags with the reason each one is a flag.

**Inputs:** a CSV or paste of jurisdiction / miles / gallons by quarter, plus optional per-vehicle detail.
**Outputs:** a flag report, each item naming the trigger, the specific numbers involved, and a suggested reconciliation step.

**Essential features — the rule set, taken directly from the audit-selection criteria and the audit manual's most-frequent-errors list:**

- values ending in 5 or 0 across the board (fabricated-looking rounding)
- identical reported miles or gallons across consecutive quarters
- fleet MPG above 7 or below 4
- quarter-over-quarter MPG variance greater than 1.0
- MPG not following a seasonal pattern
- non-taxable miles reported without a corresponding exemption basis
- zero returns
- **total miles less than the sum of jurisdiction miles**, or an odometer-derived total disagreeing with the sum
- missing base-jurisdiction distance
- deadhead/bobtail distance apparently omitted
- adjacent-jurisdiction pairs with implausible mile ratios
- surcharge-jurisdiction lines missing where the jurisdiction requires one
- fuel-type mix implying DEF or reefer gallons claimed as taxable diesel

**Deliberately excluded:** filing, mileage capture, fuel-card ingest. This tool takes a finished return as input and criticizes it. That narrowness is the point.

**AI:** **inappropriate.** These are arithmetic and threshold rules. A model would make the output less auditable, not more.

**Why a spreadsheet won't do:** a spreadsheet *could* implement these rules — but nobody has, because the value is in knowing which rules to encode, and that knowledge is buried in an audit manual and a 2013 forum post. The tool's value is the encoded rule set plus the explanation of each flag, not the computation.

**Complexity:** small — this is a weekend build with a static rules file and a table.
**Learning difficulty:** ten minutes.
**Value:** reduces audit probability, which against a 4-year lookback and $4,200–$9,000 observed assessments is worth far more than the build cost. Secondarily, it catches genuine data errors before they become a filed position that must be defended.
**Risks:** the rule set is derived partly from a forum account of one state's selection software. It should be presented as *heuristics consistent with the published audit manual*, not as a claim about any jurisdiction's current algorithm. Overstating that would be both wrong and reputationally risky.
**Existing substitutes:** none found. The prep services do not advertise this.
**Why attractive:** it is the cleanest possible catalog entry — narrow, explainable in one sentence, zero setup, no data integration, no PII, and it makes an invisible risk visible. It is also an excellent free lead-in to 4.2.
**Paid customization:** carrier-specific baselines (a reefer fleet's seasonal MPG pattern differs from a dry van's); multi-client dashboards for a filing service; jurisdiction-specific rule additions.

---

### 4.4 SettleSheet — Part 376.12-compliant settlement statement generator

**Intended user:** settlement clerk or owner at a carrier with leased owner-operators.
**Problem solved:** Problem 3 — the weekly statement is a regulated artifact, spreadsheets are the norm, and the cheapest small-fleet accounting product puts settlements behind "contact sales."

**Current workflow:** a spreadsheet per pay period, hand-assembled from seven systems, emailed or printed.

**Proposed workflow:** define each contractor's lease terms once — pay basis (percentage / per-mile with a named mileage basis / flat / hourly), recurring deductions with their computation method, escrow terms. Each cycle, load the period's loads and transactions, review exceptions, and generate a statement that is compliant by construction.

**Inputs:** lease terms per contractor; load list with revenue and mileage; deduction transactions (fuel card, insurance, lease, advances); accessorial records; supporting documents.
**Outputs:** a per-contractor settlement statement PDF with an itemized chargeback section referencing the backup document for each charge; a **running escrow ledger** with additions, deductions, description per movement, and **quarterly interest accrued at the 91-day Treasury bill average yield**; a rated-freight-bill attachment for percentage-pay contractors; a period summary for the accounting system; and, on termination, a **45-day escrow return clock with final accounting**.

**Essential features:** the 376.12(h) requirement that every chargeback names its computation method and links to the document proving validity; 376.12(g)'s rated freight bill for percentage pay; 376.12(k)(3)'s escrow itemization; 376.12(k)(5)'s quarterly T-bill interest; 376.12(k)(6)'s 45-day return; a **named mileage basis per lease** (hub / practical / shortest) recorded on the statement so the 8–10% dispute is at least explicit; advance recovery tracking with a **three-leg reconciliation** (broker advance → factor remittance → settlement deduction) to catch duplicate recovery; and a **California Labor Code 226 mode** decomposing piece-rate pay into productive time, non-productive time and paid rest breaks.

**Deliberately excluded:** payroll tax filing, W-2/1099 issuance, banking/ACH, general ledger. This produces the statement and an export; it is not an accounting system.

**AI:** **optional and peripheral.** Extracting rate and accessorial amounts from a broker's rate-confirmation PDF is a genuine document-understanding problem where formats vary per broker and rules break down — a reasonable AI use with human confirmation. The pay arithmetic and the compliance structure must be deterministic.

**Why a spreadsheet won't do:** a spreadsheet cannot enforce that every chargeback has attached backup, cannot maintain an escrow ledger with quarterly interest accrual, cannot detect that an advance was recovered twice across three systems, and cannot produce the evidence trail that 376.12(h) contemplates. The Landstar and Swift cases are about exactly these failures.

**Complexity:** medium. **Learning difficulty:** 1–2 hours, mostly one-time lease setup.
**Value:** removes a recurring weekly production task; the duplicated-advance and stale-recurring-deduction error classes each recover real money; and the compliance structure is genuine liability reduction against a litigated regulation. A 1% linehaul error is worth **$1,000–1,500 per truck per year**.
**Risks:** this produces a document a contractor may later use as evidence. Correctness matters more than convenience. Wage-statement requirements vary by state beyond California. The T-bill rate source must be reliable and dated.
**Existing substitutes:** Excel and Google Sheets templates (free, in wide use); Rigbooks (settlements behind "contact sales"); Truckbase ($290/mo minimum); Axon; McLeod. QuickBooks has no settlement concept at all.
**Why attractive:** the compliance framing is the wedge. Every competitor sells "driver settlements" as an accounting feature. None sells the statement as the legal artifact 376.12 describes, and none appears to compute the escrow interest the regulation mandates.
**Paid customization:** carrier-specific lease term modeling; state wage-statement variants; integration with a specific fuel card or factoring company; branded statements; contractor self-service portal.

---

### 4.5 FuelCard Normalizer — a community-maintained fuel transaction mapping layer

**Intended user:** office manager; also a building block for 4.2 and 4.4.
**Problem solved:** Problem 7 — every fuel network exports a different CSV, importers are hand-written per vendor, and the fields dropped in normalization are exactly the ones IFTA and settlement need.

**Current workflow:** download the export, copy-paste columns into whatever template is downstream, lose some fields, repeat weekly.

**Proposed workflow:** drop the export in; the tool detects the network from the header signature, applies the mapping, and emits a canonical transaction file. Unknown formats fall back to an interactive column mapper that saves a reusable, shareable mapping.

**Inputs:** any fuel-card CSV/XLS export (Comdata, EFS, WEX, Pilot/Flying J, TCH, Love's, TA, and bank/debit statements).
**Outputs:** a canonical transaction file — date/time, unit number, driver, jurisdiction, product code with **diesel / DEF / reefer / oil separated**, gallons, price per gallon, total, invoice number, location — plus an exception list for rows that failed validation.

**Essential features:** header-signature detection; a versioned mapping file format that users can contribute back; product-code taxonomy mapping (the DEF-as-diesel misclassification is a real audit exposure); jurisdiction derivation from location where the export omits it; unit-number normalization; and validation rules (negative gallons, duplicate transactions, transactions on a truck that was not in service, purchases in a jurisdiction with no corresponding miles).

**Deliberately excluded:** fuel-purchase optimization, price comparison, card management, anything requiring a login to a fuel network.

**AI:** **optional, narrow, and honest about it.** Suggesting column mappings for an unseen format is a reasonable model use. Applying a saved mapping must be deterministic.

**Why a spreadsheet won't do:** the mapping knowledge is the asset, and it needs to be versioned and shared across users rather than re-derived by each carrier. That is a repository, not a workbook.

**Complexity:** small. **Learning difficulty:** minutes.
**Value:** removes a weekly copy-paste task; more importantly it prevents the two error classes with real downstream cost — misallocated fuel on the wrong driver's settlement, and DEF/reefer gallons claimed as taxable diesel.
**Risks:** low. Transaction data is business data, not driver PII, though card numbers must be masked.
**Existing substitutes:** each TMS's own importer, which is the problem being solved.
**Why attractive:** it is the classic open-source shape — a data-normalization layer whose value grows with contributors, useful standalone, and a dependency for two other concepts in this catalog.
**Paid customization:** building and maintaining a mapping for a carrier's specific card program; automated retrieval where a network offers an API.

---

### 4.6 FSC Keeper — effective-dated fuel surcharge schedules with pass-through audit

**Intended user:** owner (negotiating and reviewing), office manager (applying), and by extension the contractor receiving the pass-through.
**Problem solved:** Problem 6 — FSC is a per-customer, per-week bracket lookup that goes stale silently, and nobody can audit whether the pass-through actually happened.

**Current workflow:** a peg price and cents-per-mile typed into a rate sheet at some point in the past, applied by memory.

**Proposed workflow:** store each customer's FSC schedule as an effective-dated object — either a formula (peg price, assumed MPG, index basis: national vs. PADD region) or a **bracket table**, which is what real published schedules actually are. Each Monday, ingest the EIA weekly diesel release, recompute every active schedule, and report the week's rate per customer. Separately, reconcile FSC billed to FSC paid through to contractors.

**Inputs:** per-customer FSC schedules (formula or bracket table); the EIA weekly diesel series; load records with miles and customer; settlement records showing FSC paid out.
**Outputs:** this week's FSC by customer; a staleness report showing which schedules have not been revised as the index moved and the implied per-mile gap; a pass-through reconciliation (FSC billed vs. FSC paid to contractors); and a negotiation worksheet showing what a given peg and MPG assumption is worth at the current index.

**Essential features:** effective-dated schedule versioning (so a historical load can be re-priced at the schedule in force that week); bracket-table support; PADD-region basis as well as national; the OOIDA `(index − peg) ÷ MPG` formula; and a **100% pass-through check** against the lease term OOIDA advises contractors to insist on.

**Deliberately excluded:** rate negotiation with brokers, load boards, invoicing.

**AI:** **inappropriate.** This is arithmetic against a published weekly number.

**Why a spreadsheet won't do:** a spreadsheet handles one schedule adequately. It handles effective-dating across a dozen customers, weekly index ingestion, and historical re-pricing badly — and the staleness detection, which is where the money is, requires comparing schedule vintage to index movement over time.

**Complexity:** small. **Learning difficulty:** 30 minutes.
**Value:** the Truckstop example puts a stale peg at **$0.20+/mi**, or $100 on a 500-mile load. Even a fraction of the naive annualization is orders of magnitude above any plausible price. The pass-through audit also protects against the contractor disputes documented in section 3.
**Risks:** low. The main caution is that FSC is contractual — the tool reports what a schedule *says* and what the index *is*; it cannot unilaterally change a customer's terms. It should be framed as a negotiation and verification aid, not a billing authority.
**Existing substitutes:** spreadsheets; TMS FSC modules in the mid-market products; the carrier reading a weekly PDF.
**Why attractive:** the input is a free, public, weekly, machine-readable government series; test data is trivially available; the arithmetic is simple; and diesel is currently volatile enough ($4.58 → $5.35 in five weeks) that stale schedules are actively lossy right now.
**Paid customization:** modeling a specific customer's unusual schedule; integration with an invoicing system; lane-specific or regional schedules.

---

### 4.7 DetentionDesk — accessorial evidence capture and 48-hour invoice builder

**Intended user:** driver (capture) and office manager (invoice).
**Problem solved:** Problem 4 — less than half of detention invoices get paid, against a $15.1B industry-wide pool, and the failure is documentary.

**Current workflow:** the driver texts times or writes them on the BOL; the office manager invoices it if she remembers and has enough to justify it; the broker denies it.

**Proposed workflow:** on arrival the driver records gate-in, dock-in, work start/finish, and gate-out, with photographs carrying visible timestamps and, where obtainable, a dock supervisor signature. The office manager reviews the event against the rate confirmation's free-time terms and the ELD duty-status record, and generates an accessorial invoice with the evidence attached — **within 48 hours**, which is the practice associated with 75–85% recovery.

**Inputs:** load reference and rate-confirmation terms (free time, detention rate, whether accessorials are excluded); driver-captured timestamps and photos; ELD duty-status export for cross-reference.
**Outputs:** a detention invoice with a computed chargeable-hours calculation and an attached evidence packet; an aging report of unbilled and unpaid accessorials; and a per-customer scorecard of average dwell and payment rate.

**Essential features:** a fast driver capture flow (this must take well under the 10–15 minutes per load the documentation burden currently costs); free-time and rate terms per customer; **ELD duty-status cross-reference**, which is what turns a driver's claim into corroborated evidence; the 48-hour submission clock; and detection of rate confirmations that carry explicit no-accessorial clauses, so the office manager knows before the driver waits.

**Deliberately excluded:** dispute escalation, collections, legal action, broker communication. The tool builds an invoice with evidence; it does not chase it.

**AI:** **optional.** Reading a timestamp off a gate photo, or extracting free-time terms from a rate confirmation PDF, are reasonable model uses with confirmation. The hours computation must be deterministic.

**Why a spreadsheet won't do:** the capture happens in a truck cab, not at a desk, and the evidence is photographic. A spreadsheet cannot hold the artifacts or enforce the 48-hour clock.

**Complexity:** small-to-medium (the driver-side capture is the complexity).
**Learning difficulty:** 15 minutes for the driver, an hour for the office.
**Value:** the cited five-truck example recovers ~$18,000/yr. Even at half that, this is the highest raw-dollar concept in the set for the smallest fleets.
**Risks:** driver adoption is the binding constraint, and drivers correctly resent unpaid administrative work. Any design that adds friction without visibly paying the driver a share of what it recovers will fail. Photographic evidence at customer facilities may raise facility-policy objections.
**Existing substitutes:** TMS accessorial modules; manual process; nothing purpose-built at this price point that was found.
**Why attractive:** the ROI is directly measurable in dollars recovered, which is the only argument that clears the margin bar in this market.
**Paid customization:** customer-specific term libraries; integration with a factoring company's document submission; branded evidence packets.

---

### 4.8 PacketCheck — invoice packet completeness linter

**Intended user:** office manager, at invoicing.
**Problem solved:** Problem 8 — invoices are rejected or delayed for documentary reasons, and non-recourse factoring explicitly does not cover the most common causes.

**Current workflow:** assemble the packet, submit it to the broker or factor, wait, get it kicked back, rework it, resubmit — with the invoice's clock restarting and the reserve holdback staying trapped.

**Proposed workflow:** before submission, run the packet through a per-customer requirement profile. The tool checks that every required document is present, that the amounts on the invoice reconcile to the rate confirmation plus documented accessorials, that reference numbers match, and that the POD is legible and signed.

**Inputs:** the assembled packet (invoice, POD, rate confirmation, scale tickets, lumper receipts, accessorial evidence); a per-customer/per-factor requirement profile.
**Outputs:** a pass/fail checklist with specific defects named; a corrected reference-number report; an assembled, correctly ordered submission file.

**Essential features:** per-customer and per-factor requirement profiles (they differ, and the factor's requirements are contractual); amount reconciliation between invoice, rate confirmation and accessorial documentation; reference-number consistency across documents; **POD legibility and signature presence check**; and a rejection-reason log that feeds back into the profiles over time.

**Deliberately excluded:** submitting to anyone; factoring; collections; AR aging (that is accounting's job).

**AI:** **justified here, unusually.** Determining whether a scanned POD is legible and actually bears a signature is a perception problem that rules cannot solve well — a photograph of a dark, crumpled, partially-cut-off delivery receipt is exactly the case conventional code handles badly. Amount and reference-number extraction from varied broker documents is likewise a genuine document-understanding task. Everything downstream of extraction should be deterministic and every extraction should be operator-confirmable.

**Why a spreadsheet won't do:** the inputs are images and PDFs, not numbers.

**Complexity:** small-to-medium. **Learning difficulty:** 20 minutes.
**Value:** each avoided rejection moves an invoice from day 60+ back to day 33, keeps the reserve holdback moving, and avoids the chargeback risk of aging past the ~90-day recourse window. *The per-rejection dollar cost is inferred, not measured — this is the weakest-evidenced value claim in the set.*
**Risks:** an AI legibility check that produces false confidence is worse than no check. It must fail loudly and default to flagging. Handling customer documents raises no unusual privacy issue but does raise fraud-surface concerns given the FBI's April 2026 warning that threat actors specifically **manipulate FMCSA records, insurance information, and billing documentation** ([IC3 PSA I-043026-PSA](https://www.ic3.gov/PSA/2026/PSA260430)).
**Existing substitutes:** the factoring company's own intake review, which happens *after* submission and is the rejection itself.
**Why attractive:** it moves a check that currently happens at the counterparty to before submission, which is where it is worth something.
**Paid customization:** building requirement profiles for a carrier's specific customer set; integration with a specific factor's portal format.

---

### 4.9 PM-Due — a maintenance schedule that satisfies 396.3(b)(2) literally

**Intended user:** owner or office manager.
**Problem solved:** Problem 9 — 1,204 violations in half a year for having no system showing when maintenance is due, averaging $2,040.

**Current workflow:** a shoebox of repair invoices, plus whatever the shop remembers.

**Proposed workflow:** define a PM schedule per vehicle class (interval by miles, engine hours, or elapsed time), attach it to each vehicle, and let the tool compute and display next-due dates. Record completions with the invoice attached.

**Inputs:** vehicle roster with the 396.3(b)(1) identification elements (company number, make, serial number, year, tire size); PM interval definitions; odometer/hour readings; completed service records.
**Outputs:** a forward-looking due schedule per vehicle stating the **nature and due date** of each inspection — the literal wording of 396.3(b)(2); a completion history satisfying 396.3(b)(3); an annual 396.17 inspection tracker; and a DVIR-defect-to-repair-certification link satisfying 396.11.

**Essential features:** the forward schedule (the thing being violated), retention clocks (**1 year where housed plus 6 months after the vehicle leaves control** for maintenance records; **3 months** for DVIRs; **14 months** for 396.21(b) inspection reports), and defect-to-repair certification.

**Deliberately excluded:** work orders, parts inventory, purchase orders, shop scheduling, telematics fault codes. Those are Fleetio's business and Fleetio does them well for $4/vehicle/month.

**AI:** **inappropriate.**

**Why a spreadsheet won't do:** honestly, a well-built spreadsheet nearly does — which is why this concept scores lower on differentiation. What it adds is the retention clocks, the DVIR linkage, and a schedule shaped to the regulation's exact wording rather than to a fleet manager's intuition.

**Complexity:** small. **Learning difficulty:** 30 minutes.
**Value:** avoids a $2,040-average finding that FMCSA cites over a thousand times per half-year.
**Risks:** low.
**Existing substitutes:** Fleetio ($4/veh/mo), Whip Around ($5/asset/mo, free for one asset), and a large ecosystem of free Excel maintenance-log templates. **This is the most contested space in the set.**
**Why still attractive despite that:** the violation count proves the market is failing at this *despite* cheap tools existing, which points at adoption friction rather than price — a tool that requires no account, no per-vehicle fee, and ten minutes of setup, and that names the regulation it satisfies, addresses a different barrier than Fleetio does. But this should be treated as the weakest differentiation case in the set and validated before building.
**Paid customization:** manufacturer-specific PM interval libraries; integration with an existing shop's system.

---

### Deferred candidates (documented, not scored)

**ELD Revoked-Device Watcher.** FMCSA publishes registered and revoked ELD device lists as machine-fetchable files and is de-listing devices in continuous batches — 56+ devices removed since January 2025. Carriers get up to 60 days to install a compliant replacement; after that they are cited under 395.8(a)(1) and placed out of service. A script that diffs the published revoked list against your device model and emails you is perhaps thirty lines of code, and nothing on the market appears to do it. It is deferred here only because it is too small to be a standalone catalog entry — it belongs as a feature of 4.1 or as a free utility.

**DataQs Case Manager.** FMCSA's [15 April 2026 DataQs overhaul](https://www.fmcsa.dot.gov/newsroom/fmcsa-upgrades-dataqs-program-improve-efficiency-and-transparency-safety-record) creates a mandatory three-stage independent review with hard deadlines (**initial ≤21 days, reconsideration ≤21 days, final ≤45 days**), eligibility windows of 3 years for inspections and 5 years for crashes, documented denial reasoning, and **publicly published state performance data**. States have 120 days to finalize implementation plans, with requirements effective around September 2026. Small carriers are hit hardest by CSA volatility because their denominators are tiny — one bad inspection can move a percentile 20–40 points — and 2–5 truck fleets historically had the *lowest* DataQs success rate at 51%. This is a brand-new, deadline-driven, evidence-attached workflow with zero incumbent tooling and a forthcoming public benchmarking dataset. **It is deferred only because the state implementations are not yet in force; it should be re-examined in the next cycle covering this market.**

---

## 5. Opportunity ranking

Each concept scored 1–5 on ten criteria. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of implementation | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 4.1 | **QueryGuard** — Clearinghouse & DQ obligation ledger | 5 | 5 | 5 | 5 | 4 | 4 | 4 | 4 | 4 | 5 | **45** |
| 4.6 | **FSC Keeper** — effective-dated fuel surcharge schedules | 4 | 5 | 4 | 5 | 5 | 5 | 3 | 4 | 5 | 4 | **44** |
| 4.3 | **IFTA Pre-Filing Linter** | 4 | 4 | 4 | 5 | 5 | 5 | 5 | 3 | 4 | 4 | **43** |
| 4.5 | **FuelCard Normalizer** | 3 | 5 | 3 | 5 | 5 | 5 | 4 | 4 | 4 | 4 | **42** |
| 4.4 | **SettleSheet** — 376.12 settlement generator | 4 | 5 | 4 | 4 | 3 | 3 | 4 | 5 | 3 | 5 | **40** |
| 4.9 | **PM-Due** — 396.3(b)(2) schedule | 3 | 4 | 3 | 5 | 5 | 5 | 3 | 3 | 4 | 5 | **40** |
| 4.8 | **PacketCheck** — invoice packet linter | 4 | 5 | 4 | 5 | 3 | 4 | 4 | 4 | 3 | 3 | **39** |
| 4.2 | **MileVault** — IFTA/IRP distance archive | 5 | 4 | 4 | 3 | 2 | 2 | 5 | 5 | 3 | 5 | **38** |
| 4.7 | **DetentionDesk** — accessorial capture | 4 | 4 | 5 | 4 | 3 | 3 | 3 | 4 | 3 | 4 | **37** |

### The top three

**1. QueryGuard (45).** This is the clearest opportunity in the report and it is not close on evidence. The problem is quantified by FMCSA's own violation data rather than by a vendor's marketing: the #1 and #2 most expensive routine audit findings for a small carrier are the **absence of two calendar events that cost $1.25 each**, at average penalties of **$10,278 and $7,736**. J.J. Keller's independent read — Clearinghouse query failures account for nearly 10% of all audit violations cited since 2021 — corroborates it from a second direction. The task requires no hardware, no telematics, no integration, and no AI; it requires a correct obligation model, a date computation, and an evidence store. The incumbents charge $300/month for 1–19 drivers and still leave the completeness gap that My Safety Manager names explicitly. And the segment is reachable: 68,186 of the 69,511 target carriers have an email address on file with FMCSA.

The build is small; the differentiation is *accuracy*, which is unusual and defensible. Shipping the current 391.51(b) list without the removed 391.27, and modeling NRII paper-MEC acceptability by CDL issuing state against a waiver clock that expires 11 October 2026, are both things much of the existing checklist ecosystem gets wrong today.

**2. FSC Keeper (44).** This ranks second on a combination of near-perfect buildability and a live, currently-worsening problem. Its severity is genuinely lower than MileVault's or SettleSheet's, and it ranks above them because the scoring rewards ease of implementation and narrowness — which is the correct bias for this catalog. The input is a free weekly government series; test data is a public CSV; the arithmetic is subtraction and division; there is no PII; and diesel moved $0.77 in four weeks this summer, which means every schedule pegged before 2022 is actively bleeding money right now. The staleness report — "this customer's schedule was set at a $3.50 peg, the index is $5.35, your implied gap is $0.20/mi" — is a one-screen output that a carrier can act on in a negotiation the same day.

**3. IFTA Pre-Filing Linter (43).** The purest catalog entry in the set: one input, one output, no integration, no setup, no stored data, explainable in a sentence. Its differentiation score is the highest in the table because nothing comparable was found — the filing services sell the filing, not a critique of it. Its value proposition is unusual and appealing: it does not save time, it reduces the probability of a four-year-lookback audit by catching the exact patterns the selection criteria reward. It is also the natural free front door to MileVault, which is the harder and more valuable build behind it.

### What to investigate next

**Build QueryGuard first.** It has the strongest evidence, the clearest ROI, the smallest build, and the least dependency on anything outside the carrier's own knowledge. Ship it with the ELD Revoked-Device Watcher folded in as a free utility.

**Prototype the IFTA Pre-Filing Linter in parallel** — it is small enough to be a side output of the same effort and serves as the acquisition channel for the IFTA work.

**Validate MileVault's central feasibility question before committing to it.** Despite ranking eighth, it addresses the single highest-severity problem in the market and has the strongest differentiation and customization potential. It is ranked low almost entirely on implementation risk, and that risk resolves to one question: *can a small carrier actually obtain the raw ≤10-minute, 4-decimal, ECM-odometer ping stream from the ELD/telematics vendors they use?* If the answer is yes for two or three major vendors, MileVault's score rises substantially and it becomes the flagship. If the answer is no, the concept is dead and should be removed from the catalog rather than half-built. **That question is the highest-value thing to answer in the next cycle.**

---

## 6. Validation plan

### Questions to ask practitioners

*For QueryGuard, ask an owner or office manager at a 5–25 truck carrier:*

1. Walk me through what happened the last time you hired a driver. What did you collect, in what order, and how did you know you were done?
2. How do you know when a driver's annual Clearinghouse query is due? Show me.
3. Have you ever been through a new-entrant safety audit or a compliance review? What did they ask for, how long did you have, and how did you assemble it?
4. If FMCSA emailed you tomorrow asking for all driver files within 48 hours, how long would that take you and what would you be missing?
5. Do you know whether your drivers' CDL-issuing states are NRII-compliant? Do you still accept paper medical cards?
6. Who holds your random drug-test selection records — you or your consortium? If your consortium disappeared tomorrow, could you prove your selections were spread across the year?

*For MileVault, the feasibility questions matter more than the pain questions:*

7. Which ELD/telematics vendor are you on, and can you export raw GPS pings — not the IFTA summary report? At what interval and what coordinate precision?
8. Have you ever been IFTA- or IRP-audited? What exactly did the auditor ask for, and what could you not produce?
9. Where do your IFTA records from four years ago live right now?
10. Do you file NY HUT, KYU, NM, or Oregon? Off what data?

*For SettleSheet:*

11. Show me a settlement statement you produced last week. (Then check it against 376.12(h) and (k) line by line.)
12. Do you hold escrow for any contractor? When did you last pay escrow interest, and at what rate?
13. Has a contractor ever disputed a deduction? What did you have to produce?

### Who to interview

- **Small carrier owners, 5–30 trucks**, reachable directly: 68,186 of the 69,511 target carriers have email on file with FMCSA, and the census file is public. California (7,210), Texas (6,735) and Illinois (4,675) have the deepest concentrations.
- **Settlement clerks and trucking office managers** — 1,000+ open "Trucking Company Office Manager" postings on ZipRecruiter alone; hiring managers at those companies are approachable.
- **Third-party compliance service providers** (Foley, My Safety Manager, Simplex, Dockex, DOTDriverFiles) — they see the failure patterns across hundreds of carriers and their pricing pages reveal what the market will pay.
- **IFTA/IRP filing services** (Motor Carrier HQ, IFTA Plus, Start4Truckers) — they receive whatever the carrier can produce and know exactly where the inputs break.
- **A former or current state IFTA/IRP auditor.** This is the single highest-value interview in the plan. State revenue departments and DMVs employ them; several have written publicly.
- **OOIDA** — the Land Line reporting on 376.12 violations indicates staff with direct case knowledge.
- **A freight factoring company's intake desk** — they hold the actual rejection-reason distribution that section 3, Problem 8 is missing.

### Further search terms

`IFTA audit assessment appeal` · `IRP records review findings` · `individual vehicle distance record requirements` · `new entrant safety audit failed corrective action plan` · `FMCSA notice of claim settlement small carrier` · `Clearinghouse annual query violation penalty` · `owner operator settlement statement dispute 376.12` · `escrow return 45 days owner operator` · `detention invoice denied broker` · `fuel surcharge schedule bracket table carrier` · `motor carrier office manager job description` · site-restricted searches on `thetruckersreport.com`, `landline.media`, `overdriveonline.com`, `ccjdigital.com`, `truckingdive.com`. **Reddit (r/Truckers, r/TruckingIndustry, r/smallbusiness) was unreachable from this environment across all four research streams — every practitioner quote in this report comes from TruckersReport, Land Line, FreightWaves or Overdrive. Reddit coverage is a genuine gap and should be gathered from a different network path.**

### Sample files and data needed

| For | Need |
|---|---|
| QueryGuard | A real (redacted) driver qualification file; a real audit document-request letter; a C-TPA random selection report; the NRII state-compliance list |
| MileVault | Raw telematics ping exports from Motive, Samsara and one budget ELD; a filed IFTA return with its worksheets; an IRP renewal distance schedule; an actual auditor document request |
| IFTA Linter | Eight consecutive quarters of filed returns from two or three carriers (jurisdiction / miles / gallons only — no PII needed) |
| SettleSheet | Three or four real settlement statements from different carriers; an owner-operator lease agreement; a fuel card export |
| FuelCard Normalizer | One export each from Comdata, EFS, WEX, Pilot and TCH — headers and a few rows suffice |
| FSC Keeper | Three or four real customer FSC schedules (the [EFW weekly letter](https://efwnow.com/wp-content/uploads/2026/08/Weekly-Fuel-Surcharge-Letter-08.05.2026-08.11.2026.pdf) is a public one); the EIA weekly series is already public |
| PacketCheck | A set of rejected invoice packets with the stated rejection reasons |

### Prototypes that would validate

- **QueryGuard, one week:** a single-file local web app holding a driver roster and an obligation table, computing next-due dates and rendering a completeness matrix. No file storage in v0 — just show a carrier their own gaps and watch their reaction. If the matrix shows nothing they didn't already know, the premise is wrong.
- **IFTA Linter, two days:** a form that accepts pasted quarterly figures and runs the rule set. Test against real returns from three carriers. If it flags nothing on returns that were never audited and flags something on a return that *was* audited, that is meaningful signal.
- **FSC Keeper, three days:** fetch the EIA weekly series, accept one customer schedule, output the current rate and the staleness gap. Show it to five carriers and ask what their peg price is. If most cannot answer, the problem is confirmed.
- **MileVault, one week of pure feasibility work, no product:** attempt to export raw ping data from two ELD vendors and measure the actual interval and coordinate precision against IFTA P540.200. **This is a go/no-go gate, not a prototype.**

### Assumptions most likely to make these fail

1. **That carriers believe they have a compliance gap.** The most likely failure across the whole set is not that the problem is unreal but that carriers do not perceive it until an auditor arrives. The violation data proves the gap exists; it does not prove anyone will act before the fine. **Every product here needs to make the gap visible in under a minute.**
2. **That raw telematics pings are obtainable.** MileVault dies without this.
3. **That the office manager, not a service provider, is the buyer.** Many carriers have outsourced IFTA and DQ management entirely. If so, the customer is the service provider — which changes the product (multi-tenant, higher price tolerance, different feature set) but may improve the economics.
4. **That "free open-source with paid customization" survives contact with this market.** These are companies with no IT function whose stated toolchain is Microsoft Office. Self-hosting anything may be a non-starter, and a hosted version raises the Part 40 §40.321 and CCPA obligations described in 4.1.
5. **That drivers will cooperate with DetentionDesk.** Unpaid administrative work imposed on drivers has an extremely poor adoption history.
6. **That the margin math permits any price at all.** At $1,000–$2,000 gross profit per truck per year, several of these concepts may only ever be free tools with services attached. That is a viable model for this catalog, but it should be an explicit choice rather than a discovery.

---

## 7. Cross-industry patterns

Six patterns from this market that transfer to named backlog assignments.

### Pattern A — Regulatory obligation ledger with mandatory evidence attachment

An obligation set defined by public regulation, each item with a recurrence rule, a retention clock, and a required proving document; the tool's distinguishing feature is tracking *never-collected* separately from *expired*.

**Transfers to:** *Fire protection inspection, testing and maintenance (ITM) contractors under NFPA 25* (inspection frequencies and deficiency records by system type); *Radiation safety officer services and portable gauge licensee compliance* (NRC/agreement-state licence conditions, leak tests, dosimetry); *Special inspection agency accreditation consultants (IAS AC291, ANAB, WABO)* (inspector qualification records and their expiry); *Provider credentialing and payer enrollment services* (per-payer, per-provider recurring attestations); *Calibration and metrology service providers / in-house gage management* (calibration intervals and traceability certificates); *Multi-state charitable solicitation registration compliance* (40+ jurisdictions on different renewal cycles).

### Pattern B — Pre-submission linter modeled on the reviewer's own selection or rejection logic

Take a finished deliverable, run it against the criteria the receiving authority is known to apply, and return ranked flags before submission rather than after rejection.

**Transfers to:** *Small third-party medical billing companies* (claim scrubbing is the mature analogue — the pattern generalizes to less-served submissions); *Environmental laboratories producing regulator EDD deliverables (EQuIS and state formats)*, where rejected loads are a known cost; *Premium audit and payroll classification consulting*; *Property tax consulting and assessment appeal firms*; *Building permit expediting and code consulting firms* (plan-check rejection patterns are jurisdiction-specific and knowable).

### Pattern C — Community-maintained vendor-export normalization layer

Every counterparty exports a different file; the mapping knowledge is the asset; it should be versioned, shared, and contributed back rather than re-derived per customer.

**Transfers to:** *Independent pharmacy third-party reconciliation and PBM claw-backs* (remittance formats differ per PBM); *Freight bill audit and payment for small shippers*; *Submetering and utility expense recovery service providers* (utility bill formats); *Industrial distributors and metal service centers issuing material test reports*; *Outsourced real-estate accounting and lease administration service providers*.

### Pattern D — Compliance-grade source archive held independently of the vendor cloud that produced it

The regulator requires the raw source record for years; the vendor that produced it retains it on its own schedule; the practitioner churns vendors. The archive, not the derived report, is the audit-survival artifact.

**Transfers to:** *Environmental laboratories producing regulator EDD deliverables* (raw instrument data vs. reported results); *Geotechnical and environmental consulting / materials testing labs* (already covered at narrow-subspecialty — this is a distinct back-office angle); *Title abstracting and independent title search contractors*; *UAS / drone mapping and reality-capture service providers* (raw imagery and flight logs vs. delivered orthomosaics); *Deep foundation testing specialists (CSL, PIT, PDA)*.

### Pattern E — Effective-dated rate or schedule table driving a recurring computed pass-through

A published index or fee schedule changes on a fixed cadence; a per-counterparty table converts it to a charge; the table goes stale silently and nobody can audit whether the pass-through occurred.

**Transfers to:** *Workers' compensation medical billing and state fee schedule compliance* (state fee schedules update annually and vary by jurisdiction); *Retail shopping center management — percentage rent and gross sales reporting*; *Submetering and utility expense recovery service providers* (utility tariff changes); *Employee benefits brokerage and benefits administration* (rate tables by plan year); *Tenant-side lease audit and occupancy cost consulting* (CAM escalation formulas).

### Pattern F — The statement as a regulated legal artifact, not an accounting output

A recurring document whose itemization, backup-document linkage, and interest computation are mandated by regulation and litigated when wrong — and which the affordable software tier treats as a mere report.

**Transfers to:** *Real estate brokerage trust and escrow account compliance administration* (trust accounting rules are state-mandated and audited); *Independent escrow companies (California DFPI-licensed, non-title)*; *Third-party claims administration (TPA) and self-insured program operations* (loss run and claim statement requirements); *HOA and condominium management companies — estoppel and demand response desk* (statutory content and response deadlines per state); *1031 exchange qualified intermediaries* (fund-holding and accounting obligations).

---

## 8. Sources and confidence

### Verified findings — read directly on a primary or credible named source

**Regulation and standards (primary text):**
[49 CFR 376.12 (truth-in-leasing)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-376/subpart-B/section-376.12) · [49 CFR 391.51 (DQ file)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-391/subpart-C/section-391.51) · [49 CFR 391.23](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-391/subpart-C/section-391.23) · [49 CFR 391.53](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-391/subpart-C/section-391.53) · [49 CFR 382 Subpart G (Clearinghouse)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-382/subpart-G) · [49 CFR 382.305 (random testing)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-382/subpart-C/section-382.305) · [49 CFR 40.321 (confidentiality)](https://www.ecfr.gov/current/title-49/subtitle-A/part-40/subpart-P/section-40.321) · [49 CFR 395 Appendix A (ELD spec)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-395/appendix-Appendix%20A%20to%20Subpart%20B%20of%20Part%20395) · [49 CFR 395.11 (supporting documents)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-395/subpart-A/section-395.11) · [49 CFR 395.32 (unidentified driving)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-395/subpart-B/section-395.32) · [49 CFR Part 396](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-396) · [49 CFR 385 Appendix B (violation severity)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-385/appendix-Appendix%20B%20to%20Part%20385) · [49 CFR 390.201 (biennial update)](https://www.ecfr.gov/current/title-49/subtitle-B/chapter-III/subchapter-B/part-390/subpart-E/section-390.201) · [Record of Violations final rule removing 391.27](https://www.federalregister.gov/documents/2022/03/09/2022-04930/record-of-violations) · [FMCSA UFA 4.0 User Manual](https://www.fmcsa.dot.gov/sites/fmcsa.dot.gov/files/docs/ATTACHMENT-A_UFA-UserManual%20508%20compliant_0.pdf) · [FMCSA DQ Files ICR renewal, 15 Apr 2025](https://www.federalregister.gov/documents/2025/04/15/2025-06345/agency-information-collection-activities-renewal-of-a-currently-approved-collection-driver) · [FMCSA NRII paper-MEC waiver to 11 Oct 2026](https://nationalregistry.fmcsa.dot.gov/assets/documents/nriilearningcenter/NRII%20Waiver%20Oct%2011%202026.pdf) · [FMCSA DataQs overhaul, 15 Apr 2026](https://www.fmcsa.dot.gov/newsroom/fmcsa-upgrades-dataqs-program-improve-efficiency-and-transparency-safety-record) · [FMCSA Clearinghouse query pricing](https://clearinghouse.fmcsa.dot.gov/Resource/Index/Query-Plan) · [SMS Methodology](https://csa.fmcsa.dot.gov/Documents/SMSMethodology.pdf) · [Enhanced SMS notice, 20 Nov 2024](https://www.federalregister.gov/documents/2024/11/20/2024-27087/enhanced-carrier-safety-measurement-system-sms)

**IFTA / IRP (primary):**
[IFTA Procedures Manual, eff. Jan 2026](https://www.iftach.org/manuals/2026/PM/Procedures%20Manual%20-%2001-01-26.pdf) · [IFTA Articles of Agreement, eff. Jan 2026](https://www.iftach.org/manuals/2026/AA/Articles%20of%20Agreement%20-%2001-01-26.pdf) · [IFTA Best Practices Audit Guide](https://www.iftach.org/committee/ac/Best%20Practices%20Guide.pdf) · [Kansas IFTA Audit Manual](https://www.ksrevenue.gov/pdf/mfiftaam.pdf) · [Connecticut 2024 Finding of Non-Compliance](https://www.iftach.org/committee/CT%202024%20Final%20Determination%20Finding%20of%20Non-Compliance.pdf) · [IRP Audit Reference & Best Practices, 10 Jan 2024](https://cdn.ymaws.com/www.irponline.org/resource/resmgr/audit_prog2/audit_best_practices_1_10_24.pdf) · [CA DMV IRP Handbook Ch.9](https://www.dmv.ca.gov/portal/handbook/irp/chapter-9-audits), [Ch.10](https://www.dmv.ca.gov/portal/handbook/irp/chapter-10-recordkeeping/), [Ch.11](https://www.dmv.ca.gov/portal/handbook/irp/chapter-11-common-errors-found-in-audits/) · [Iowa DOT IRP Carrier Manual](https://iowadot.gov/media/1144/download?inline=) · [Indiana DOR audit tips](https://www.in.gov/dor/motor-carrier-services/files/audit-tips.pdf) · [Illinois MFUT-53](https://tax.illinois.gov/content/dam/soi/en/web/tax/research/publications/documents/motorfuel/mfut-53.pdf) · [Minnesota DPS recordkeeping](https://dps.mn.gov/divisions/dvs/business/irp-and-ifta/irp-and-ifta-audit/irp-and-ifta-audit-record-keeping-requirements) · [SC DMV IFTA returns](https://dmv.sc.gov/Business-Customers/Motor-Carriers/International-Fuel-Tax-Agreement/IFTA-Tax-Returns) · [Idaho STC revoked IFTA licenses](https://tax.idaho.gov/taxes/product-excise-taxes/fuels-taxes-and-fees/consumer-fuels/ifta-licenses/revoked-idaho-ifta-license/) · [CDTFA IFTA interest rates](https://cdtfa.ca.gov/taxes-and-fees/ifta-interest-rates.htm) · [NY IFTA-101-I instructions](https://www7b.tax.ny.gov/pdfs/IFTA/Ifta101_i_CA.pdf)

**Market and economic data:**
[FMCSA SMS Motor Carrier Census, data.transportation.gov](https://data.transportation.gov/resource/kjg3-diqy.json) (aggregated directly; data updated 2026-07-13) · [FMCSA A&I Registration Statistics](https://ai.fmcsa.dot.gov/RegistrationStatistics) · [FMCSA Pocket Guide 2024](https://www.fmcsa.dot.gov/sites/fmcsa.dot.gov/files/2025-09/FMCSA%20Pocket%20Guide%202024-v6%20508%20.pdf) · [ATA Economics and Industry Data](https://www.trucking.org/economics-and-industry-data) · [ATRI 2026 Operational Costs release, 15 Jul 2026](https://truckingresearch.org/2026/07/new-atri-report-details-accelerating-costs-and-low-profitability-despite-cuts/) · [FreightWaves on ATRI 2026](https://www.freightwaves.com/news/trucking-costs-outpaced-consumer-inflation-in-25-atri) · [FleetOwner ATRI regional breakdown](https://www.fleetowner.com/operations/article/55392569/atri-report-breaks-down-class-8-truck-operating-costs-by-region-and-expense-category) · [FleetOwner IdeaXchange on utilization](https://www.fleetowner.com/perspectives/ideaxchange/blog/55395622/three-takeaways-from-atris-2026-trucking-cost-analysis-for-fleet-operators) · [Trucking Dive Q1 2026 carrier population](https://www.truckingdive.com/news/carrier-population-shifts-back-toward-growth-quarterly-fmcsa-data-shows/817176/) · [FreightWaves carrier exits 12-month high](https://www.freightwaves.com/news/trucking-company-exits-reach-12-month-high) · [EIA weekly diesel prices](https://www.eia.gov/petroleum/gasdiesel/)

**Violation and enforcement data:**
[US Compliance Services — analysis of >50,000 FMCSA violations through June 2025](https://uscomplianceservices.org/what-50000-fmcsa-violations-tell-us-about-carrier-compliance-in-2025/) · [J.J. Keller DataSense on Clearinghouse audit violations](https://www.jjkellerdatasense.com/driver-insights/clearinghouse-violations-during-audits) · [Overdrive on offsite audits targeting small carriers](https://www.overdriveonline.com/regulations/article/15063877/owneroperators-remain-in-crosshairs-of-dots-offsite-reviews) · [Foley DQF audit checklist](https://www.foleyservices.com/articles/dqf-audit-checklist/) · [Trucksafe on 2026 random testing rates](https://www.trucksafe.com/post/fmcsa-keeps-random-drug-alcohol-testing-rates-the-same-for-2026) · [Overdrive on Motus problems](https://www.overdriveonline.com/regulations/article/15828482/fmcsa-suspends-usdot-deactivations-as-motus-issues-mount-for-carriers) · [FBI IC3 PSA I-043026-PSA on cargo theft](https://www.ic3.gov/PSA/2026/PSA260430)

**Practitioner voice (all verbatim, all TruckersReport unless noted):**
[IFTA/IRP audit experiences](https://www.thetruckersreport.com/truckingindustryforum/threads/ifta-irp-audit.2344493/) · [Audit selection criteria](https://www.thetruckersreport.com/truckingindustryforum/threads/criteria-used-for-ifta-irp-audit-selection.213213/) · [BigRoad/Fleet Complete IFTA report accuracy](https://www.thetruckersreport.com/truckingindustryforum/threads/big-road-%E2%80%9Cfleet-complete%E2%80%9D-ifta-mileage-report.2436550/) · [IFTA tracking methods](https://www.thetruckersreport.com/truckingindustryforum/threads/ifta-tracking.2501385/) · [Settlement software](https://www.thetruckersreport.com/truckingindustryforum/threads/settlement-software.292165/) · [Percentage pay transparency](https://www.thetruckersreport.com/truckingindustryforum/threads/percentage-pay-how-to-know-if-they-are-cheating-you.2504427/) · [Rate disclosure legality](https://www.thetruckersreport.com/truckingindustryforum/threads/rates-legality-of-disclosure.2493787/) · [Getting brokers to pay detention](https://www.thetruckersreport.com/truckingindustryforum/threads/how-to-get-brokers-to-actually-pay-detention.2145331/page-2) · [Management software / "I run 7 trucks with no software"](https://www.thetruckersreport.com/truckingindustryforum/threads/management-software.2418884/) · [Compliance review experience](https://www.thetruckersreport.com/truckingindustryforum/threads/compliance-review-not-new-entrant.352105/page-2) · [Authority audit workload](https://www.thetruckersreport.com/truckingindustryforum/threads/how-come-no-one-mentioned-how-much-work-is-involved-for-authority-audit.1294107/page-6) · [Driver qualification file](https://www.thetruckersreport.com/truckingindustryforum/threads/driver-qualification-file.2504647/) · [OOIDA Land Line "Your rights in the regs"](https://landline.media/magazine/your-rights-regs/) · [Overdrive on short miles](https://www.overdriveonline.com/overdrive-extra/article/15768772/why-are-carriers-shippers-still-using-short-miles-to-pay-truckers) · [TruckingOffice Pilot fuel card CSV thread](https://help.truckingoffice.com/hc/en-us/community/posts/4404375840276-PILOT-FUEL-CARD-CSV)

**Vendor pricing (verified to the cited page):**
[TruckingOffice](https://www.truckingoffice.com/pricing/) · [Truckbase](https://www.truckbase.com/trucking-software-pricing) · [Rigbooks](https://www.rigbooks.com/pricing) · [TruckLogics](https://www.trucklogics.com/pricing) · [IFTA Plus](https://www.iftaplus.com/pricing) · [Fleetio](https://www.fleetio.com/pricing) · [Whip Around](https://whiparound.com/pricing/) · [DOTDriverFiles](https://dotdriverfiles.com/pricing/) · [Dockex vs J.J. Keller](https://dockex.io/vs/jj-keller) · [My Safety Manager DQ cost](https://www.mysafetymanager.com/driver-qualification-file-cost/) · [QuickBooks](https://quickbooks.intuit.com/pricing/) · [Motor Carrier HQ](https://www.motorcarrierhq.com/ifta/) · [EFW weekly fuel surcharge letter, 8/5–8/11/2026](https://efwnow.com/wp-content/uploads/2026/08/Weekly-Fuel-Surcharge-Letter-08.05.2026-08.11.2026.pdf)

**Case law and legal analysis:**
[Benesch on OOIDA v. Landstar](https://www.beneschlaw.com/insight/interconnect-flash-no-6-ooida-landstar-upon-further-review/) · [FMCSA OOIDA v. Swift final order](https://www.fmcsa.dot.gov/sites/fmcsa.dot.gov/files/2024-10/OOIDA%20v%20Swift%20Final%20Order.pdf) · [DOL Fact Sheet #19 (motor carrier exemption)](https://www.dol.gov/agencies/whd/fact-sheets/19-flsa-motor-carrier) · [California Labor Code 226 for truck drivers](https://www.truckingpayroll.com/2026/06/19/california-truck-driver-pay-stub/)

### Strong inferences — reasoned from verified facts, not directly stated by a source

- **The per-truck margin ceiling on software spend.** The $1,000–$2,000 gross profit per truck per year figure is derived (86,000 mi × $2.336/mi × 0.5–1.0% margin), not published. ATRI publishes the cost per mile and the margin separately; the multiplication is mine. The conclusion — that a $100/truck/month stack consumes the entire margin — follows arithmetically but should be sanity-checked against a real carrier's P&L.
- **That ELD records are legally insufficient for IFTA.** The regulatory texts are verified and their requirements are plainly different. What is inferred is the *consequence*: that ELD vendors offering IFTA modules must be running a separate, denser telematics feed alongside the HOS record, and that personal-conveyance segments at 10-mile precision are effectively unallocatable to a jurisdiction. No source states this conclusion; it follows from comparing the two specs.
- **That the addressable population is ~69,500 carriers.** The FMCSA census aggregation is verified arithmetic, but the "active for-hire" filter (authority + mileage reported 2024 or later) is a definitional choice, not FMCSA's.
- **That advances are structurally prone to duplicate recovery.** The three-leg reconciliation problem (broker advance → factor remittance → settlement deduction) is logically implied by the documented mechanics and supported by one practitioner account of a $400 dispute, but no source enumerates it as a known error class.
- **That the gap between silos is where the cheap failures happen.** The market splits into asset-side (Fleetio, Whip Around, Motive, Samsara), person-side (Foley, J.J. Keller, Tenstreet) and filings (Simplex, permit services). That the cheapest failures — a $1.25 query at $10,278/violation, a maintenance-due schedule at $2,040/violation — fall between them is my read of the violation data, not a claim any source makes.

### Tentative hypotheses requiring practitioner validation

- **That raw ≤10-minute, 4-decimal, ECM-odometer ping data is actually obtainable** from the ELD/telematics vendors small carriers use. MileVault's entire viability rests on this and it is unverified.
- **The dollar cost of a single rejected freight invoice.** No primary source was found. PacketCheck's value claim is inferred from payment-timing mechanics and factoring terms, not measured.
- **That carriers will act on a compliance gap before an auditor arrives.** The violation data proves the gap; nothing proves the willingness.
- **Whether "the owner's spouse does the books" is real.** Widely repeated as folklore; TruckersReport threads consistently show the owner personally doing it. No citable primary source was found either way.
- **Exact 2026 Part 386 Appendix B civil penalty figures.** Sources conflict on whether a 2026 inflation adjustment published. The eCFR render referenced adjustments "through July 21, 2026" while a secondary source reported no separate 2026 adjustment as of May 2026. **Re-pull Appendix B directly before quoting a dollar figure.**
- **Whether the enhanced SMS has launched.** The November 2024 Federal Register notice promised a follow-up notice announcing the launch date. That follow-up was not located. Multiple 2026 blogs assert a March 2026 go-live, but several of those same sources conflate Motus with SMS, which marks them as unreliable. **Do not publish a go-live date without the follow-up notice.**
- **The Clearinghouse-II 60-day CDL downgrade clock.** Commonly cited but not stated on either FMCSA page examined. Needs the final rule text.
- **UCR 2027 fee levels** (reported as rising ~20% to $55/$167/$333/$1,163/$5,548/$54,165 with collection from 1 Oct 2026) — one source describes the rule as proposed rather than final.

### Coverage gap to disclose

**Reddit was unreachable from this environment across all four research streams** — `reddit.com` and `old.reddit.com` returned 403/ROBOTS_DISALLOWED, domain-scoped searches were rejected, and pushshift mirrors were down. r/Truckers and r/TruckingIndustry are the largest practitioner communities in this market. Every practitioner quote in this report comes from TruckersReport, Land Line, Overdrive, FreightWaves or vendor support forums. This is a real sampling bias — TruckersReport skews toward long-tenured owner-operators and small-fleet owners, which is arguably the right population for this report, but it is not the whole population.

The session also exhausted its web-search budget before two flagged items (enhanced SMS launch status, 2026 Part 386 penalty figures) could be independently re-verified. Both are marked tentative above.
