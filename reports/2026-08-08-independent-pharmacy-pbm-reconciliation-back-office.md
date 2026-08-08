# Independent Pharmacy Third-Party Reconciliation and PBM Claw-Backs — Back Office

**Market research cycle report — Borg LLC free/open-source business application catalog**

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market claimed** | Independent pharmacy third-party reconciliation and PBM claw-backs |
| **Angle claimed** | back-office |
| **Claim ID** | `0d33e95c` |
| **Date** | 2026-08-08 |
| **Report** | `reports/2026-08-08-independent-pharmacy-pbm-reconciliation-back-office.md` |
| **Backlog remaining after this claim** | 363 assignments |
| **Completed reports before this one** | 30 (30 distinct markets) |

### Why this assignment was chosen over the others available

The ledger had 363 available assignments across 221 markets with zero completed coverage. The selection rule that dominates right now is breadth, so anything in a market already touched (fire protection, MEP, land surveying, machine shops, insurance, title/escrow, legal, medical billing) was set aside. From the remaining fresh markets I applied three filters:

1. **Sector never touched by the catalog.** Thirty completed reports cluster into roughly eight sectors: AEC/construction, insurance, legal, accounting/tax, healthcare billing, transportation, manufacturing quality, and nonprofit/HR back office. **Retail pharmacy is absent entirely.** Adding it widens the catalog's sector footprint more than another AEC or another accounting sub-market would.
2. **Evidence density.** Pharmacy reimbursement is one of the most heavily documented small-business finance problems in the United States right now — NCPA publishes annual audited-style Digest statistics and member surveys with hard percentages, health-care law firms publish detailed audit-procedure guides because it is a live practice area, CMS publishes the underlying acquisition-cost benchmark for free, and thirteen-plus states passed reimbursement-floor statutes in 2024–2026 that create a brand-new compliance-verification workload. That is far more verifiable practitioner evidence than most backlog entries would yield.
3. **Structural fit to the catalog thesis.** The work in question is file-in, file-out: a claims extract, an X12 835 remittance, a bank statement, a public price file. Narrow deterministic tools operating on those files can produce measurable dollars. That is exactly the shape of application the catalog is meant to hold, and almost none of it needs AI.

Candidates seriously considered and passed over: *Print brokers and prepress service bureaus / handoffs-and-qa* (equally fresh sector and excellent standards evidence via the Ghent Workgroup, but a structurally shrinking industry with thin margins — weaker economic case); *Calibration and metrology service providers / core-practitioner-workflow* (clean spreadsheet-bound workflow, but adjacent to two already-completed manufacturing-quality markets); *Test, adjust and balance contractors* and *Backflow prevention testers* (both adjacent to already-completed HVAC-design and fire-ITM markets); *Non-emergency medical transportation* (fresh, but evidence is thinner and the pain is scheduling rather than document work).

The **back-office** angle was the one available on this market in the backlog and is the correct one regardless — the entire subject is the money desk behind the counter, not the dispensing workflow.

---

## 1. Market examined

### Industry and role

Independent community pharmacy — retail pharmacies not owned by a national chain, mass merchant, supermarket, or PBM affiliate. The specific role under examination is the **third-party / accounts-receivable desk**: the owner-pharmacist, bookkeeper, or lead technician responsible for making sure the pharmacy is actually paid what it was promised at the point of sale, and for defending the money already received against retroactive recovery.

### Size of the market

- **18,960 independent pharmacy locations** in the United States as of July 2025, roughly **36% of all retail pharmacies** — a $103 billion marketplace in 2024. ([NCPA 2025 Digest](https://ncpa.org/newsroom/news-releases/2025/10/19/ncpa-releases-2025-digest-report))
- Average store dispensed **67,601 prescriptions in 2024**, up sharply from 59,644 in 2023 — volume per surviving store is rising because stores are closing around them. 84% generic; 52% of volume is Medicare Part D plus Medicaid combined.
- Community pharmacies employ **more than 235,000 people** nationally. The typical independent is a single location with 5–15 employees; multi-store groups of 2–15 locations are common and are the segment most likely to hire dedicated back-office staff.
- Financial condition is severe: **80.3%** of surveyed independents reported declining financial health, **30.3%** were considering closing, and **96.5%** said Part D reimbursement threatened their viability. ([NCPA January 2025 member survey](https://ncpa.org/sites/default/files/2025-01/1.27.2025-FinalExecSummary.NCPA_.MemberSurvey.pdf))

### Type of user for the software

Not a developer, not an analyst. Realistically:

- **Owner-pharmacist** doing back-office work in the evening, Excel-literate but not a modeler.
- **Certified pharmacy technician** promoted to "third-party technician" — comfortable with the pharmacy management system, payer portals, and spreadsheets.
- **Part-time bookkeeper** or the pharmacy's outside CPA firm, working from exports.
- In 2–15 store groups, a **single central biller** covering all locations.

All of them are working on Windows desktops inside a HIPAA-covered entity, usually with no IT department and often with the pharmacy management system (PMS) locked down by the vendor.

---

## 2. How the work is performed

### The financial pipeline of one prescription

1. **Adjudication.** At fill time the pharmacy transmits an NCPDP claim to the PBM through a switch and receives back a *promise to pay*: ingredient cost, dispensing fee, patient pay amount, and any point-of-sale price concession. Nothing is verified at this moment; the number on the screen is a representation, not a payment.
2. **Dispense and pickup.** The patient pays the copay. If the patient never picks up, the claim must be reversed within the PBM's return-to-stock window or the payment becomes recoverable.
3. **Payment cycle.** The PBM pays on a contracted cycle — typically twice monthly, sometimes 30+ days. Payment arrives as an ACH deposit, and separately an **X12 835 electronic remittance advice** should arrive no later than three business days after the corresponding EFT. Some payers send only paper EOBs; some send 835s in a week, others take 30 days. ([Sykes CPA / Econcile](https://www.sykes-cpa.com/third-party-reconciliation-for-independent-pharmacies/))
4. **Adjustments.** The remittance carries claim-level adjustments (CAS segments mapped to NCPDP reason codes) and, critically, **provider-level adjustments in the PLB segment** — fees, prior-period recoupments, and forwarding balances that are *not* tied to any claim in that file. When recoveries exceed new payments the payer zeroes the check and carries the deficit forward with a `FB` forwarding-balance code. ([NCPDP X12N 835 Payment Reference Guide](https://www.ncpdp.org/NCPDP/media/pdf/X12N835_5010PaymentReferenceGuide.pdf))
5. **Reconciliation.** Someone must match three things: what was adjudicated (PMS claim data), what the remittance says was paid (835/EOB), and what actually landed in the bank. Anything unmatched is a receivable to chase.
6. **Retroactive recovery.** Months later, three separate mechanisms can take the money back: **effective-rate true-ups** (GER/BER), **PBM audits**, and **invoice reconciliation audits**.

### Who does what

| Actor | Role in the back office |
|---|---|
| Owner-pharmacist | Owns the P&L; signs audit responses; decides which fights to pick |
| Third-party technician | Posts payments, chases unpaid claims, files MAC appeals, assembles audit documents |
| Bookkeeper / outside CPA | Reconciles deposits to the general ledger, monitors AR aging |
| PSAO | Negotiates network contracts on the pharmacy's behalf; often the counterparty on effective-rate true-ups; the effective rate is measured **at the aggregate PSAO level, not per pharmacy or per claim** ([GNP](https://www.wearegnp.com/insights/what-pharmacies-should-know-about-dir-fees-and-ger-and-ber-recoupments)) |
| Wholesaler | Must send purchase histories directly to the PBM during invoice reconciliation audits |
| PBM audit vendor | Issues discrepancy reports, sets response and appeal deadlines |

### Documents and systems in play

- **PMS claim exports** — PioneerRx, Liberty, Rx30, QS/1, BestRx, Computer-Rx, Micro Merchant PrimeRx. Every one exports differently; most export CSV.
- **X12 835 files**, downloaded from PBM provider portals or delivered to a clearinghouse mailbox. Pharmacy 835s identify the claim by prescription/service reference number, sometimes concatenated with a fill number prefixed `FILL`, with the product identified by an `N4`-qualified NDC.
- **Paper EOBs** for smaller payers, requiring manual entry.
- **Bank statements / ACH detail.**
- **PBM provider manuals** — the binding source for return-to-stock windows, documentation requirements, and appeal procedures; each PBM's is different and they change without much notice.
- **NADAC** — CMS's free weekly National Average Drug Acquisition Cost survey file, now with a three-month moving average on generics since December 2024. ([Medicaid.gov NADAC](https://www.medicaid.gov/medicaid/nadac))
- **AWP** — proprietary, licensed from Medi-Span or First Databank; used as the denominator in effective-rate math.
- **Spreadsheets** — the actual system of record in most stores. Practitioner accounts describe pharmacists hand-tracking **7,000+ claims per month** in spreadsheets.

### Software currently used

The reconciliation software market exists and is mature at the top: **Outcomes/Net-Rx RecRx**, **FDS eConcile**, **EnlivenHealth**, **PBA Health EnsurePay**, **AlignRx eRecon**, **Cardinal Health Reconciliation**, plus PSAO-bundled services (APCI ResolveRx, Pharmacy First). They are largely subscription or full-service offerings; Outcomes describes a "flat monthly fee" with an assigned account manager and payment posting done on the pharmacy's behalf. An EnlivenHealth case study reports an 11-store group reducing reconciliation to **1–2 hours per month across all 11 pharmacies**, framed as an 88% reduction against the industry average.

What these products do well is the **three-way match and the chasing of unpaid claims**. What they consistently do *not* advertise is: below-cost detection against NADAC and the new state floors, MAC appeal packaging and deadline tracking, running effective-rate exposure, will-call/return-to-stock compliance, audit-response assembly, and dispensed-vs-purchased NDC proofing. Those are the gaps this report targets.

---

## 3. Most important problems, ranked

### P1 — Money is promised at adjudication and never actually arrives, and nobody notices

**Who:** Every independent, most acutely those without reconciliation software.
**When:** Continuously; discovered (if ever) weeks later.
**Currently handled by:** "Fill and pray" — dispense and assume payment. Where it is handled at all, a technician compares deposits to a spreadsheet.
**Why inadequate:** Claim volume defeats manual matching. Even a small pharmacy has hundreds of claims a week; the average store now fills ~5,600 prescriptions a month. Vendors report that **after 60 days over 4% of a pharmacy's receivables remain unpaid**, and that a typical store carries a **$250,000–$300,000 receivable balance in any given month** ([Net-Rx](https://net-rx.com/identify-missing-pharmacy-payments/), [Sykes CPA](https://www.sykes-cpa.com/third-party-reconciliation-for-independent-pharmacies/)). Causes are mundane — stale address on file with the payer, wrong bank routing detail, a claim simply "missed for whatever reason."
**Frequency:** Weekly, unending.
**Cost:** If 1–4% of a $250k monthly receivable is genuinely lost, that is $30k–$120k a year of already-earned revenue on a business whose gross profit is at a ten-year low.
**Evidence:** Verified — multiple independent vendor and CPA sources, consistent numbers, and an industry benchmark (AR should be 50–70% of monthly sales; days-in-AR 10–15) that owners are told to measure against ([Independent Rx Consulting](https://independentrxconsulting.com/pharmacy-accounts-receivable-what-they-tell-you/)).

### P2 — Claims are paid *below acquisition cost* and the pharmacy cannot see it at the claim level in time to appeal

**Who:** Every independent, disproportionately on Part D and Medicaid managed care.
**When:** At adjudication; the appeal window is short.
**Currently handled by:** Gut feel, occasional spot checks, or a technician eyeballing the paid amount against the invoice.
**Why inadequate:** The numbers are stark — **40.8% of surveyed pharmacies were paid below NADAC on more than 40% of their Medicare Part D prescriptions**, and 29.2% were below NADAC on more than half. Meanwhile the appeal right exists and is time-boxed: a representative PBM MAC appeal process gives **60 calendar days from date of service** to appeal, with a decision in 10 days and 60 days to resubmit after a favorable determination ([IPM](https://ipm.rxipm.com/mac-appeals-specific-state-requirements/)). Thirty-six states have MAC statutes; Georgia-style laws require the PBM to adjust the MAC prospectively and allow reversal/rebill of the appealed claim, or to name an NDC actually purchasable at or below the MAC ([Frier Levitt](https://www.frierlevitt.com/articles/why-filing-mac-appeals-should-be-a-win-win-for-pharmacies/)). Pharmacies leave this on the table because identifying the underwater claims inside the 60-day window is manual work nobody has time for.
**Frequency:** Daily, at scale.
**Cost:** Directly the difference between surviving and closing. This is the single most cited cause of the closure wave.
**Evidence:** Verified — CMS-published NADAC, NCPA survey percentages, PBM-published appeal procedures.

### P3 — A new statutory reimbursement floor exists in a growing list of states, and nobody is checking whether PBMs actually honor it

**Who:** Independents in the thirteen-plus states that adopted NADAC-plus-dispensing-fee floors.
**When:** Every claim, from each state's effective date.
**Currently handled by:** Essentially not at all, or by a state association fielding anecdotes.
**Why inadequate:** The laws are new, specific, and *checkable arithmetic*: Kentucky $10.64 (Jan 1, 2025), Nebraska $10.38, California SB 41 $10.05 (Oct 2025), Arkansas / Georgia / Tennessee / West Virginia / Iowa tied to the state Medicaid rate, with Alabama, Louisiana, and Montana adding 2025 provisions ([Frier Levitt, 2026 state PBM reform](https://www.frierlevitt.com/articles/2026-state-pbm-reform-nadac-reimbursement-spread-pricing-bans/)). Enforcement depends on the pharmacy noticing and documenting a shortfall — Frier Levitt explicitly lists *tracking NADAC weekly, verifying reimbursement calculations, and documenting claims paid below the minimum* as pharmacy obligations. A pharmacy that cannot produce a claim-level shortfall list has no complaint to file with its insurance department.
**Frequency:** Every claim in a covered state.
**Cost:** In a state with a $10.05 floor, a systematic $3 shortfall across 5,600 monthly claims is $200k a year — recoverable only with evidence.
**Evidence:** Verified — statutes and effective dates are public; Arkansas is documented as the most aggressive enforcement state.

### P4 — Retroactive claw-backs arrive as opaque lump sums that cannot be traced to claims

**Who:** Every independent.
**When:** Effective-rate true-ups typically annually after calendar year-end; DIR-style recoveries at unpredictable intervals — "some plans may take these recoupments from the next payment, while others take recoupments six months or more after the initial transaction."
**Currently handled by:** Accepting the invoice. Practitioner-facing legal commentary is blunt that independents have "zero bargaining power" against PBMs covering ~95% of the population.
**Why inadequate:** The pharmacy is charged based on an aggregate computation performed on the PBM's data, at the **PSAO aggregate level**, using AWP as the denominator: `Actual Effective Rate = 1 − (ingredient cost paid ÷ AWP)`, with per-claim variance `= (contract rate − actual rate) × AWP` ([Pharmacy First effective-rate guide](https://www.pharmacyfirst.com/wp-content/uploads/2021/02/Pharmacy-First_Effective-Rate-User-Guide_CEO.pdf)). The pharmacy can in principle compute its own running position and does not. Compounding this, the 2024 move of Part D price concessions to the point of sale destroyed the float that used to cushion these recoveries — pharmacies now absorb the margin hit immediately ([Pharmacy Times](https://www.pharmacytimes.com/view/it-s-crunch-time-for-cash-flow-and-closures-what-s-on-the-other-side-)).
**Frequency:** Continuous fees; annual or semi-annual true-ups.
**Cost:** True-up invoices are described as having "caused grave financial harm" and forced closures. Even absent a dispute, not forecasting the liability is a cash-flow failure.
**Evidence:** Verified mechanism and formula; specific dollar magnitudes are firm-specific and not publicly reported.

### P5 — PBM audits are escalating, are documentation-driven, and are lost on deadlines and paperwork rather than on facts

**Who:** Every independent; specialty and high-cost dispensers most heavily.
**When:** Desk audits at any time; on-site audits with notice.
**Currently handled by:** Panic, a fax machine, and a paid audit-assistance membership (PAAS National) or outside counsel.
**Why inadequate:** PBMs "dramatically increased the number of audits conducted in 2025" and now use analytics on prescriber patterns and high-cost drug activity to target ([Buchanan Ingersoll & Rooney](https://www.bipc.com/pbm-audits-assessment-of-escalating-trends-and-strategies-for-pharmacies), [Health Law Alliance](https://www.healthlawalliance.com/blog/pbm-enforcement-trends-independent-pharmacies-must-prepare-for-in-2026)). The published top-ten discrepancy list is almost entirely clerical: non-calculable directions, undocumented DAW, miscalculated day supply, early refills, missing patient signatures, inadequate patient account collections, undocumented quantity reductions, unrecorded rejection overrides, incomplete transfer information, and **missed audit response deadlines** ([PBA Health](https://www.pbahealth.com/elements/how-to-minimize-financial-losses-from-pbm-pharmacy-audits/)). Recoupments are typically the *full* claim amount. Deadlines are hard: a representative PBM completes desk review in 14 calendar days and allows **30 days from the final audit report to appeal**, after which findings become final ([Health Law Alliance, Prime audit guide](https://www.healthlawalliance.com/blog/prime-therapeutics-audit-defense-guide)). Unresolved audits lead to network termination, which is existential.
**Frequency:** Several per year per store is typical; escalating.
**Cost:** Thousands to six figures per audit, plus the termination tail risk.
**Evidence:** Verified — multiple law-firm practice guides with concrete procedural detail.

### P6 — Unclaimed prescriptions sit in will-call past the PBM's return-to-stock window and convert into full-claim recoupments

**Who:** Every pharmacy.
**When:** Constantly; the exposure is invisible until an audit.
**Currently handled by:** A weekly walk of the will-call bins, or a PMS report nobody runs.
**Why inadequate:** The industry-average return-to-stock rate is around **5.1%** of fills; one high-performing independent published its own rate at **0.56% (20 of 3,558 fills)**, which is itself evidence of how much variance is operationally controllable ([Blueberry Pharmacy](https://blueberrypharmacy.medium.com/ghosted-at-the-counter-how-return-to-stock-impacts-pharmacy-operations-and-patient-care-e4dcd3dc739a)). PBM manuals impose windows — commonly around 10 days — and "a PBM will recoup a claim in full if a medication is picked up after their required return to stock timeframes" ([PAAS National](https://paasnational.com/pbm-enforcement-of-return-to-stock-policies/)). The windows differ per PBM and live behind paywalled provider manuals. RTS also doubles labor per affected prescription and distorts on-hand inventory counts.
**Frequency:** Daily.
**Cost:** At 5% of 5,600 monthly fills, ~280 prescriptions a month are in play; even a small fraction picked up late or never reversed is direct recoupment exposure plus dead inventory.
**Evidence:** Verified rates and mechanism; exact per-PBM day counts are paywalled and must be confirmed per contract.

### P7 — Invoice reconciliation audits compare *dispensed* NDC quantities to *purchased* quantities, and pharmacies cannot pre-check themselves

**Who:** Independents, especially those buying from secondary suppliers.
**When:** On PBM demand, looking back over a defined window; records must be kept six years.
**Currently handled by:** Reactively, after the demand letter, by pulling wholesaler reports.
**Why inadequate:** Wholesalers submit purchase summaries **directly to the PBM**, and may inadvertently omit purchases; buying from a non-NABP-accredited distributor results in automatic rejection regardless of whether the inventory physically existed. Shortages "frequently result in PBM terminations" ([Frier Levitt](https://www.frierlevitt.com/articles/setting-up-your-pharmacy-for-success-preparing-for-and-responding-to-invoice-reconciliation-audits/)). A related and increasingly cited finding is submitting a claim under an NDC different from the one purchased, even for a therapeutically identical product.
**Frequency:** Occasional but high-severity.
**Cost:** Existential when it goes wrong.
**Evidence:** Verified.

### P8 — Payer rates drift downward on repeat business and the change is invisible

**Who:** Every independent.
**When:** Whenever a PBM changes a MAC list or a plan's rate.
**Currently handled by:** Anecdote — "this one feels like it's paying worse."
**Why inadequate:** The pharmacy has the data to detect it (same NDC, same payer, same quantity, lower ingredient cost this month than last) but no routine that surfaces it. Detecting a rate change early is what makes a MAC appeal or a purchasing change possible while it still matters.
**Frequency:** Continuous.
**Cost:** Diffuse but compounding.
**Evidence:** Strong inference from the claim-data structure and from vendor "profit leakage" messaging; not directly quantified in a published source.

---

## 4. Application opportunities

> Design constraint applying to all ten: pharmacy claim data is PHI. Every concept below is specified as a **local, single-machine, no-cloud, no-telemetry desktop application** operating on files the pharmacy already possesses. This is not a limitation to work around — it is the primary differentiator against subscription SaaS and full-service reconciliation bureaus, and it makes a free open-source base version credible in a HIPAA-covered entity.

---

### 4.1 RemitMatch — three-way claim / remittance / deposit reconciler

- **User:** Third-party technician or bookkeeper.
- **Problem:** P1.
- **Current workflow:** Spreadsheet of claims, manual comparison against 835 downloads and bank deposits; hundreds to thousands of rows a week.
- **Proposed workflow:** Drop in the PMS claim export, a folder of 835 files, and a bank CSV. The tool matches on prescription/fill reference and NDC, applies CAS adjustments, allocates PLB provider-level amounts, and produces three outputs: matched-and-correct, short-paid, and never-paid-and-aging.
- **Inputs:** PMS claim CSV; X12 835 files; bank transaction CSV.
- **Outputs:** Reconciliation workbook; aging report bucketed 0/30/60/90/120+; a "chase list" with payer contact and claim identifiers; a GL-ready deposit summary.
- **Essential features:** X12 835 parser handling `FILL`-suffixed reference numbers and `FB` forwarding balances; configurable per-payer tolerance; persistent match state across runs so a claim resolved last month is not re-chased.
- **Excluded from v1:** Payment posting back into the PMS; payer portal scraping; multi-store consolidation.
- **AI:** Inappropriate. This is deterministic matching.
- **Why not a spreadsheet:** 835 is a segmented EDI format, not tabular; PLB allocation and forwarding balances cannot be expressed cleanly in formulas; and the job requires state that persists across weekly runs.
- **Complexity:** Medium. **Learning:** ~1 hour.
- **Value:** Recovering even 1% of a $250k monthly receivable is $30k/yr.
- **Risks:** PHI at rest; must ship with no network calls. Timely-filing limits vary by contract.
- **Substitutes:** Outcomes/Net-Rx, FDS eConcile, EnlivenHealth, AlignRx, PSAO services — a genuinely crowded segment.
- **Why still attractive:** It is the necessary data foundation for concepts 4.2, 4.4, 4.5, and 4.10, and a free local parser removes the reason a small single-store owner declines a subscription. But on its own merits this is the *least* differentiated idea in the list, and it is ranked accordingly.
- **Paid customization:** PMS-specific import mappings; multi-store rollups; QuickBooks/Sage export.

---

### 4.2 NADACGuard — below-cost and state-floor shortfall detector

- **User:** Owner-pharmacist; third-party technician.
- **Problem:** P2 and P3.
- **Current workflow:** Nothing systematic. Occasional spot-checks against invoices.
- **Proposed workflow:** Load the claim export; the tool joins each claim's NDC and quantity to the CMS NADAC file for the effective week, computes `paid ingredient cost − (NADAC × quantity)` and, if a state floor applies, `paid total − (NADAC × qty + statutory dispensing fee)`. It outputs a ranked shortfall list by dollars, by payer, and by NDC, and flags which shortfalls are still inside the 60-day MAC appeal window.
- **Inputs:** PMS claim export; CMS NADAC weekly/monthly CSV (free, public, auto-refreshable); a small state-rules table (state → floor formula → dispensing fee → effective date).
- **Outputs:** Shortfall register; appeal-eligible worklist with days remaining; per-payer summary suitable for a state insurance department complaint or a PSAO escalation; trend chart of below-cost percentage over time.
- **Essential features:** NDC-11 normalization; NADAC effective-dating (the *right* week's price, not today's); explicit "no NADAC available for this NDC" bucket rather than silent omission; state rules shipped as an editable data file so the community can maintain them.
- **Excluded from v1:** Actual invoice-cost matching (wholesaler invoice ingestion), AWP-based math, appeal submission.
- **AI:** Inappropriate for the calculation. *Optional, narrowly:* extracting a statutory formula from a newly passed bill into the state-rules file — but a human should approve every entry.
- **Why not a spreadsheet:** NADAC is ~30k+ rows refreshed weekly with effective-date ranges; NDC formats differ between the PMS export and CMS; a VLOOKUP against a stale file silently produces wrong answers on a legally consequential number.
- **Complexity:** Medium. **Learning:** ~30–60 minutes.
- **Value:** Converts P2/P3 from a grievance into an evidence file. In a $10.05-floor state a systematic shortfall across 5,600 monthly claims is six figures annually.
- **Risks:** NADAC is a *survey average*, not this pharmacy's acquisition cost — the tool must label it as a benchmark, not proof of loss, or it will overstate claims. State statutes change; the rules file must be dated and versioned.
- **Substitutes:** Reconciliation vendors report "underpaid" against the *adjudicated* amount, which is a different and much weaker test — it catches the PBM paying less than it promised, not the PBM promising less than the law requires. No mainstream product is positioned on the 2025–2026 state floors.
- **Why still attractive:** The regulatory change is 12–24 months old, the benchmark data is free and public, and the arithmetic is trivial. This is the clearest gap found in the cycle.
- **Paid customization:** A specific state's complaint-form output; PSAO-format escalation exports; wholesaler invoice-cost overlay so the tool compares against *real* acquisition cost.

---

### 4.3 AppealDesk — MAC appeal packager and deadline tracker

- **User:** Third-party technician.
- **Problem:** P2, execution half.
- **Current workflow:** Each PBM publishes its own appeal form — some fillable PDF, some Excel template — with different required fields; the technician retypes claim data into whichever form applies, emails or faxes it, and then loses track of the outcome.
- **Proposed workflow:** Select claims from a shortfall list (hand-entered or imported from 4.2), pick the PBM, and the tool renders the completed appeal in that PBM's required format, logs the submission date, computes the decision-due date and the resubmission deadline, and nags on the dashboard when a response is overdue or a favorable determination has an unexercised reversal/rebill window closing.
- **Inputs:** Claim rows (Rx number, NDC, date of service, quantity, paid amount, acquisition or NADAC reference, NPI/NCPDP); a per-PBM form template pack.
- **Outputs:** Filled PDF or Excel appeal per PBM; a submission log; a deadline calendar; an outcome ledger showing dollars appealed, won, and lost by PBM.
- **Essential features:** Template pack as plain data (community-maintainable); jurisdiction-aware deadline math (default 60 days from date of service, overridable per state/contract); tamper-evident submission log for later disputes.
- **Excluded from v1:** Direct portal submission, e-fax, automated outcome scraping.
- **AI:** Inappropriate. Form-filling and date arithmetic.
- **Why not a spreadsheet:** The deliverable is a specific PBM's PDF/XLSX form, and the value is in the deadline state machine, not the data.
- **Complexity:** Small. **Learning:** ~30 minutes.
- **Value:** Converts an unexercised legal right into recovered dollars and prospective price corrections that benefit every subsequent fill of that drug.
- **Risks:** Template drift — PBMs change forms; the pack needs a version and a "last verified" date. Not legal advice.
- **Substitutes:** PBM portals and PSAO appeal desks. Neither gives the pharmacy its own outcome ledger.
- **Why still attractive:** Smallest build in the list with a direct dollar outcome, and it composes with 4.2 into a two-step "find it, file it" workflow.
- **Paid customization:** Templates for a specific PBM mix; state-specific procedural variants; a firm-branded outcome report for the owner's monthly review.

---

### 4.4 EffectiveRateWatch — running GER/BER position and true-up forecaster

- **User:** Owner-pharmacist; PSAO liaison.
- **Problem:** P4.
- **Current workflow:** Wait for the year-end invoice and hope.
- **Proposed workflow:** After each reconciliation run the tool computes actual effective rate per claim as `1 − (ingredient cost paid ÷ AWP)`, aggregates by contract/PBM/drug class, compares to the contracted target, and reports the cumulative variance — i.e. the dollar amount the pharmacy should expect to owe or be owed at true-up — plus the drugs and payers driving it.
- **Inputs:** Claim export including ingredient cost paid and quantity; an AWP price file; a contract table (PBM → generic target → brand target → measurement period).
- **Outputs:** Running effective-rate position by contract; forecast true-up liability; top-variance NDC list; a month-over-month trend so a deteriorating position is visible in April rather than the following February.
- **Essential features:** Correct handling of reversals and partial fills; separate generic and brand pools; an "unpriced claim" exception bucket.
- **Excluded from v1:** Disputing the PBM's own calculation line by line; PSAO-level aggregation across other pharmacies (the pharmacy does not have that data).
- **AI:** Inappropriate.
- **Why not a spreadsheet:** It could be one, at small volume — but the AWP join across tens of thousands of monthly claims with effective-dated prices is where spreadsheets fail quietly.
- **Complexity:** Medium. **Learning:** ~1 hour, and requires the user to understand their own contract terms, which many do not.
- **Value:** Turns a year-end surprise into a monitored, budgetable liability, and identifies which drugs to stop dispensing at a loss.
- **Risks:** **AWP is proprietary** (Medi-Span / First Databank). An open-source tool cannot ship AWP data; it must accept a file the pharmacy already licenses through its PMS. This is a real adoption barrier and the main reason this concept scores below 4.2. Also: because the true-up is computed at the PSAO aggregate level, the pharmacy's own position is an *indicator*, not the invoice — the tool must say so plainly.
- **Substitutes:** PSAO periodic reporting (Pharmacy First and others explicitly provide claim-level effective-rate reporting to members). Pharmacies not in such a PSAO have nothing.
- **Why still attractive:** Highest differentiation score in the list — no small-tool product addresses it — and the formula is published.
- **Paid customization:** Contract-specific term modeling; escrow-position reporting; wholesaler-cost overlay to convert variance into true margin.

---

### 4.5 OffsetLedger — plain-English decoder for fees, recoupments, and forwarding balances

- **User:** Bookkeeper; owner.
- **Problem:** P4, visibility half.
- **Current workflow:** A deposit is smaller than expected; nobody can explain why; the difference is booked to a miscellaneous expense account or ignored.
- **Proposed workflow:** Parse every 835's PLB and CAS content into a dated register: fee type, amount, the reference the payer supplied, and — where the reference permits — the original claim and date of service it traces back to. Unattributable amounts are reported as unattributable rather than hidden.
- **Inputs:** 835 files.
- **Outputs:** Fee-and-recoupment register by payer and month; a "what happened to this deposit" reconciliation for any single ACH; forwarding-balance carry tracking; an annual fee-burden summary by category.
- **Essential features:** Full PLB reason-code dictionary in plain language; `FB` forwarding-balance chain tracking across files; CAS-to-NCPDP reason-code mapping; explicit unattributed bucket.
- **Excluded from v1:** Disputing fees; contract-legality analysis.
- **AI:** Inappropriate — this is a code lookup against a published standard.
- **Why not a spreadsheet:** PLB is a repeating segment with paired reason/amount fields inside a non-tabular EDI file. It is not spreadsheet-shaped.
- **Complexity:** Small-to-medium. **Learning:** ~30 minutes.
- **Value:** Makes the true cost of each PBM relationship visible for the first time; supplies the numbers for contract decisions and for the pharmacy's CPA.
- **Risks:** Payers populate PLB references inconsistently; the tool must not fabricate traceability it cannot prove.
- **Substitutes:** Outcomes advertises "transparent reports on DIR fees, transaction charges, and third-party payer adjustments" — the closest existing competitor to this concept specifically.
- **Why still attractive:** As a standalone free utility it has near-zero adoption friction — one file in, one register out — and it is the natural on-ramp to the rest of the suite.
- **Paid customization:** GL mapping and journal-entry export; multi-store consolidated fee reporting.

---

### 4.6 WillCallWatchdog — unclaimed prescription aging and reversal worklist

- **User:** Lead technician; pharmacist-in-charge.
- **Problem:** P6.
- **Current workflow:** Weekly bin walk, or an unread PMS report.
- **Proposed workflow:** Load the will-call / not-picked-up export daily or weekly. The tool ages each item against **that claim's PBM's** return-to-stock window from an editable rules table, produces a prioritized reversal worklist (past due, due in 2 days, watch), and writes an **Unclaimed Prescription Reversal Log** entry when the user confirms a reversal.
- **Inputs:** PMS unclaimed/will-call export (Rx number, patient, fill date, payer/BIN-PCN, drug, quantity, value); a per-PBM RTS window table.
- **Outputs:** Dated reversal worklist; retained reversal log for FWA compliance and audit defense; dollar value of inventory sitting in will-call; RTS rate trend against the ~5.1% industry benchmark.
- **Essential features:** Per-payer window rules the pharmacy can edit from its own provider manuals; a hard "reversed on / by whom" audit trail; refrigerated and controlled-substance flags for physical handling.
- **Excluded from v1:** Patient outreach/texting (a crowded category), PMS write-back, inventory adjustment.
- **AI:** Inappropriate.
- **Why not a spreadsheet:** It is *almost* a spreadsheet — but the retained, dated, per-item compliance log is precisely the artifact a spreadsheet does not produce credibly, and per-payer windows make the aging non-uniform.
- **Complexity:** Small. **Learning:** ~20 minutes.
- **Value:** Prevents full-claim recoupments, frees will-call inventory, and produces the exact log PAAS-style compliance programs require.
- **Risks:** RTS windows come from paywalled provider manuals — the tool must ship *empty* with a clear "enter your contracted windows" step rather than shipping guessed values. State return-to-stock rules also vary (Pennsylvania, Texas, and Florida each have specific provisions).
- **Substitutes:** PMS unclaimed-prescription reports (present but passive); patient-engagement platforms (solve pickup, not reversal compliance).
- **Why still attractive:** Cheapest build with the tightest before/after story, and it touches a 5% -of-fills problem every single day.
- **Paid customization:** Multi-store bin reporting; delivery/mail-order variants; integration with the pharmacy's own SOP document set.

---

### 4.7 AuditPack — PBM audit response assembler and deadline clock

- **User:** Owner-pharmacist, usually under time pressure.
- **Problem:** P5.
- **Current workflow:** Print, hand-collate, hand-number, fax; hope nothing is missing; frequently miss a deadline.
- **Proposed workflow:** Enter or import the PBM's discrepancy list. For each finding code the tool presents the required document checklist, accepts scanned or exported documents per claim, and assembles a single indexed PDF with **NPI and NCPDP on every page**, sequential page numbers, a cover index, and a claim-by-claim response table. It runs a deadline clock for the response date, the appeal window (commonly 30 days from the final audit report), and any third-party review window.
- **Inputs:** Discrepancy list (CSV or manual entry); scanned hard copies, signature logs, invoices; a per-PBM finding-code → required-documents map.
- **Outputs:** Submission-ready indexed PDF; a per-claim response matrix; a deadline dashboard; a retained copy of exactly what was sent and when.
- **Essential features:** Page-level stamping; completeness check ("3 of 14 claims have no signature log attached"); immutable submission archive.
- **Excluded from v1:** Legal argument drafting, extrapolation modeling, direct portal upload.
- **AI:** **Optional and genuinely useful, but strictly assistive** — classifying a pile of scans by claim number, or extracting an Rx number from a scanned hard copy. Never for deciding whether a document satisfies a finding. Must run locally (PHI) and must be overridable.
- **Why not a spreadsheet:** The deliverable is a paginated, stamped, indexed evidence package.
- **Complexity:** Medium. **Learning:** ~1 hour under stress — the UI must assume a panicking user.
- **Value:** "Missed audit response deadlines" is on the published top-ten discrepancy list; the tool removes an entire category of self-inflicted loss, and recoupments are full-claim.
- **Risks:** PHI-heavy; local-only is mandatory. It must be clearly framed as document assembly, not audit defense advice — the market for the latter belongs to counsel and PAAS.
- **Substitutes:** PAAS National membership and law-firm engagements (advice, not assembly); generic PDF tools (assembly, not domain structure).
- **Why still attractive:** Complementary to, rather than competitive with, the paid advisors — which makes them plausible channel partners.
- **Paid customization:** Per-PBM finding-code maps; integration with a specific scanner workflow; multi-store audit tracking.

---

### 4.8 InvoiceProof — dispensed-versus-purchased NDC reconciliation

- **User:** Owner-pharmacist; purchasing technician.
- **Problem:** P7.
- **Current workflow:** Reactive; pull wholesaler reports after the demand arrives.
- **Proposed workflow:** Load a period's dispensing data and the same period's wholesaler purchase history. The tool computes, per NDC, units dispensed versus units purchased (plus opening inventory where known), and flags negative coverage — the exact test the PBM will run — plus claims billed under an NDC never purchased.
- **Inputs:** PMS dispensing export; wholesaler purchase history CSV (primary and secondary suppliers); optional opening inventory.
- **Outputs:** Per-NDC coverage report with shortages ranked by dollar exposure; NDC-mismatch list; a supplier-source summary flagging purchases from suppliers the pharmacy has not marked as accredited.
- **Essential features:** NDC-11 normalization and package-size-to-unit conversion (the hard part); multi-supplier merge; period selection matching a typical audit lookback.
- **Excluded from v1:** Perpetual inventory management; DSCSA transaction-record handling; automated wholesaler API pulls.
- **AI:** Inappropriate.
- **Why not a spreadsheet:** Unit-of-measure normalization across package sizes and suppliers is where hand-built sheets produce confidently wrong answers.
- **Complexity:** Medium. **Learning:** ~1 hour.
- **Value:** Turns the highest-severity audit into something the pharmacy has already run on itself. Shortages "frequently result in PBM terminations."
- **Risks:** Requires accurate package-size reference data; misconfiguration produces false shortages and unnecessary alarm. Accreditation status of a supplier must be user-asserted, not inferred.
- **Substitutes:** Inventory modules in PMS platforms (perpetual inventory, a different and heavier problem); nothing focused on the audit test itself.
- **Why still attractive:** Narrow, defensive, and directly mirrors a published audit procedure.
- **Paid customization:** Wholesaler-specific import mappings; scheduled quarterly self-audit reporting.

---

### 4.9 RateDriftSentinel — payer reimbursement change detector

- **User:** Owner-pharmacist.
- **Problem:** P8.
- **Current workflow:** Anecdote.
- **Proposed workflow:** Across successive claim exports, group by NDC + payer + normalized quantity and detect statistically meaningful drops in ingredient cost paid. Report the top drifts by annualized dollar impact, with the date the change first appeared.
- **Inputs:** Claim exports over time (the tool keeps its own local history).
- **Outputs:** Ranked drift report; per-payer trend; a feed of appeal candidates into 4.3 and shortfall confirmation against 4.2.
- **Essential features:** Robust grouping (quantity normalization, generic substitution awareness); minimum-occurrence threshold to suppress noise; first-observed dating so the 60-day appeal clock is visible.
- **Excluded from v1:** Cross-pharmacy benchmarking (requires data the pharmacy does not have and should not share).
- **AI:** Inappropriate — a threshold comparison, not a prediction problem.
- **Why not a spreadsheet:** Requires retained multi-period history and grouping logic that resets whenever a new export lands.
- **Complexity:** Small-to-medium. **Learning:** ~30 minutes.
- **Value:** Early warning is what makes an appeal or a purchasing change possible while the window is open.
- **Risks:** Legitimate reasons for rate changes exist (plan change, different BIN/PCN); the tool must present candidates, not verdicts.
- **Substitutes:** Vendor "profit leakage" analytics bundled into paid platforms.
- **Why still attractive:** Pure derived value from data the pharmacy already owns, zero external dependencies, and it makes the whole suite feel proactive.
- **Paid customization:** Alert thresholds by drug class; scheduled email-free local report generation.

---

### 4.10 CopayGap — uncollected patient-responsibility finder

- **User:** Front-end manager; bookkeeper.
- **Problem:** Audit discrepancy category "inadequate patient account collections," plus ordinary AR leakage on house charge accounts.
- **Current workflow:** House accounts tracked in the PMS or on paper; collections chased sporadically, if at all.
- **Proposed workflow:** Compare the patient-pay amount reported on each claim to amounts actually collected in the POS/house-account export; age the gaps; produce a statement worklist and a documented waiver log for the genuinely uncollectible.
- **Inputs:** Claim export with patient pay amount; POS/house account export.
- **Outputs:** Uncollected-copay aging; per-patient statement worklist; a dated waiver/write-off log defensible in an audit.
- **Essential features:** Aging buckets aligned to the 60-day escalation convention; explicit waiver documentation (routine copay waivers are an audit finding, so the log matters as much as the collection).
- **Excluded from v1:** Payment processing, statement mailing, collections agency handoff.
- **AI:** Inappropriate.
- **Why not a spreadsheet:** Two-source matching plus a retained waiver log.
- **Complexity:** Small. **Learning:** ~20 minutes.
- **Value:** Recovers small-dollar-but-high-count revenue and removes a named audit discrepancy category.
- **Risks:** Copay waiver rules are a compliance minefield (federal anti-kickback exposure on routine waivers). The tool documents; it must not advise.
- **Substitutes:** PMS AR modules of varying quality.
- **Why still attractive:** Cheap, and it addresses a *published* audit finding rather than a generic AR complaint. Lowest score in the list, included because it is nearly free once 4.1 exists.
- **Paid customization:** POS-specific import mappings; statement template branding.

---

## 5. Opportunity ranking

Scored 1–5 on each of ten criteria. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of implementation | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 4.2 | **NADACGuard** — below-cost & state-floor detector | 5 | 5 | 5 | 4 | 4 | 4 | 4 | 4 | 4 | 5 | **44** |
| 4.3 | **AppealDesk** — MAC appeal packager + deadlines | 4 | 4 | 4 | 5 | 5 | 5 | 4 | 5 | 3 | 4 | **43** |
| 4.6 | **WillCallWatchdog** — RTS aging & reversal log | 4 | 5 | 4 | 5 | 5 | 5 | 3 | 3 | 4 | 4 | **42** |
| 4.5 | **OffsetLedger** — PLB/CAS fee & recoupment register | 4 | 5 | 4 | 5 | 4 | 5 | 4 | 3 | 3 | 4 | **41** |
| 4.1 | **RemitMatch** — three-way reconciler | 5 | 5 | 5 | 4 | 3 | 3 | 2 | 4 | 3 | 5 | **39** |
| 4.9 | **RateDriftSentinel** — payer rate change detector | 4 | 5 | 4 | 5 | 4 | 4 | 3 | 3 | 4 | 3 | **39** |
| 4.4 | **EffectiveRateWatch** — GER/BER position & forecast | 5 | 3 | 4 | 3 | 4 | 4 | 5 | 4 | 2 | 4 | **38** |
| 4.8 | **InvoiceProof** — dispensed vs purchased NDC | 5 | 3 | 4 | 4 | 3 | 4 | 4 | 4 | 3 | 4 | **38** |
| 4.7 | **AuditPack** — audit response assembler | 5 | 2 | 4 | 4 | 3 | 4 | 4 | 5 | 2 | 4 | **37** |
| 4.10 | **CopayGap** — uncollected patient responsibility | 3 | 4 | 3 | 5 | 4 | 5 | 3 | 3 | 3 | 3 | **36** |

### The top three explained

**1. NADACGuard (44).** This wins because a regulatory change created a checkable arithmetic obligation faster than the software market responded to it. Thirteen-plus states now mandate NADAC-plus-a-dispensing-fee floors with dates and dollar amounts published in statute; the benchmark file is free, public, and refreshed weekly by CMS; and 40.8% of surveyed pharmacies are being paid below NADAC on more than 40% of their Part D claims. The existing reconciliation vendors measure *promised versus paid*, which is a different question — none of them are positioned on *paid versus legally required*. The tool is a join, a subtraction, and a sort. The honest weakness is that NADAC is a national survey average rather than this pharmacy's invoice cost, so the output is an evidence file and a prioritized list, not proof of loss; the paid customization path (overlay actual wholesaler invoice cost) is exactly how that weakness converts into revenue.

**2. AppealDesk (43).** The pharmacy already has the legal right, the PBM already publishes the form, and the deadline is already fixed at roughly 60 days from date of service. What is missing is a thing that fills the form and runs the clock. This scores highly on the criteria that matter most for a first shipped product — smallest build, fastest to learn, hardest to scope-creep, and highest customization potential, since every pharmacy's PBM mix and state procedure differs. It is weaker on independent ROI because it depends on someone having already identified the underwater claims, which is precisely why it should ship alongside NADACGuard.

**3. WillCallWatchdog (42).** The least glamorous and the most certain. A ~5.1% industry-average return-to-stock rate against a documented per-PBM reversal deadline and a full-claim recoupment penalty is about as clean a before/after as this catalog will find, and one published independent runs at 0.56%, which proves the gap is operational rather than inevitable. It is a small build with a daily touchpoint, and the retained reversal log is a compliance artifact a spreadsheet cannot credibly produce. It loses points only on differentiation, since PMS platforms do surface unclaimed-prescription reports — they simply do not age them against per-payer contractual windows or log the reversal.

### What should be investigated next

**NADACGuard and AppealDesk together, as a single two-step validation.** They share the same input file, the same user, and the same 60-day clock, and the pair produces a complete story: *here are your underwater claims, here is the filed appeal, here is what came back.* Build the NADAC join first as a throwaway script against one real claim export — if the shortfall list does not surprise the pharmacist who supplied the data, the whole thesis is wrong and the cycle cost is one afternoon.

The second investigation, in parallel and cheap, is **WillCallWatchdog**, because it needs no external data source at all and can be validated with a single day's will-call export.

---

## 6. Validation plan

### Questions to ask practitioners

*On reconciliation generally:*
1. Do you reconcile at the claim level, at the deposit level, or not at all? If you use a vendor, what does it still not tell you?
2. What is your current AR balance and your days-in-AR? Do you know how much of it is genuinely uncollectible?
3. When a deposit is smaller than you expected, how do you find out why — and how often do you simply give up?

*On below-cost claims and appeals:*
4. Roughly what share of your Part D claims do you believe are paid below your acquisition cost? How do you know?
5. How many MAC appeals did you file last year? If none or few — was it because you could not identify the claims, could not spare the time, or did not believe it would work?
6. Are you in a state with a NADAC-plus-dispensing-fee floor? Have you ever checked whether a PBM actually paid it? Would you file a complaint if you had a claim-level shortfall list?

*On claw-backs:*
7. Do you know your current effective-rate position against your contract, or do you find out at true-up?
8. Do you have AWP pricing available in a file you can export, or only inside your PMS screens?

*On audits and will-call:*
9. How many audits did you respond to in the last 12 months, and what did they cost you? Did you ever lose a claim purely on a deadline or a missing page?
10. What is your return-to-stock rate, and do you know each PBM's reversal window off the top of your head?

*On tooling reality:*
11. Can you export claim data from your PMS yourself, or must you call the vendor? What format?
12. Would your compliance posture permit installing a local desktop application that reads exported PHI, and who decides?

### Who to interview

- **Owner-pharmacists of 1–3 store independents**, ideally split between a state with a new reimbursement floor (Kentucky, Nebraska, California, Iowa, Arkansas) and one without.
- **Central billers at 5–15 store groups** — the highest-volume users and the most likely to pay for customization.
- **PSAO field representatives** (APCI, Pharmacy First, EPIC, AlignRx) — they see the aggregate and know which complaints recur.
- **State pharmacy associations** — they collect member reimbursement complaints and would immediately understand the shortfall-register output.
- **PAAS National and pharmacy-side law firms** (Frier Levitt, Health Law Alliance, Buchanan) — potential channel partners for AuditPack, and the most reliable source on current audit procedure.
- **Independent pharmacy CPAs** (e.g. the Sykes-type niche practices) — they already see the reconciliation gap across dozens of clients.

### Search terms for further research

`NADAC below cost claim state floor complaint form` · `MAC appeal deadline [state] statute pharmacy` · `PBM provider manual return to stock days` · `835 PLB WO forwarding balance pharmacy` · `generic effective rate true-up invoice dispute` · `invoice reconciliation audit shortage NDC mismatch` · `PMS name + export claims CSV` · `NCPA member survey reimbursement below NADAC` · `pharmacy audit finding codes full recovery` · `[PBM name] audit appeal 30 days final report`

### Sample files and data needed

1. A real (or realistically synthesized) **PMS claim export** from at least two different systems — PioneerRx and one of Liberty/Rx30/BestRx — to learn how much column layouts differ.
2. **Two or three 835 files** from different PBMs, including at least one with PLB recoupments and one with a forwarding balance.
3. A **CMS NADAC weekly CSV** (already public — download today, no permission needed).
4. A **will-call / unclaimed export**.
5. A **PBM discrepancy report** and one **final audit report** with finding codes, ideally supplied by a law firm or PAAS in redacted form.
6. A **wholesaler purchase history CSV**.

Items 1, 2, 4, 5, and 6 all contain PHI or commercially sensitive terms and will require either a cooperating pharmacy under an agreement or careful synthesis. **Item 3 is free and public and should be pulled first.**

### The prototype that would validate this

A single Python script, run once, on one real claim export plus that week's NADAC file, that prints: the count and dollar value of claims paid below NADAC, the same below NADAC-plus-the-state-dispensing-fee, the top 20 by dollar exposure, and how many are still inside a 60-day appeal window. Nothing else. No UI. If a pharmacist looks at that output and immediately asks "can you do last quarter too," the concept is validated. If they say "I already knew that and it doesn't help," the differentiation thesis has failed and the effort should move to WillCallWatchdog.

### Assumptions most likely to make this fail

1. **That pharmacies can get their own claim data out.** If PMS exports are locked, incomplete (missing ingredient cost paid), or vendor-gated, the entire suite has no input. *This is the single highest-risk assumption and must be tested first.*
2. **That NADAC is close enough to actual acquisition cost** to be persuasive. If pharmacists dismiss it as "not my cost," the shortfall register becomes noise and the tool must ingest wholesaler invoices instead — a materially bigger build.
3. **That appeals actually recover money.** Published success rates are absent from the sources reviewed. If PBMs deny routinely and the recovery is only prospective, the ROI argument shifts from "recover dollars" to "correct future pricing," which is real but slower to sell.
4. **That a free local tool is adoptable in a HIPAA-covered entity.** Some pharmacies will require a BAA or a vendor security review even for a local install; some corporate-owned groups will refuse unsigned binaries outright.
5. **That the incumbent vendors do not simply add the feature.** NADAC comparison is not hard for Outcomes or FDS to ship. The defensible position is local-first, free, and community-maintained state rules — not the arithmetic.
6. **That the segment can pay for customization.** With 30% of independents considering closure, the paid-tier buyer may be the PSAO, the state association, or the accounting firm rather than the pharmacy itself.

---

## 7. Cross-industry patterns

Patterns from this cycle that should transfer to named markets still in the backlog:

**A. Public benchmark file versus paid amount — the "free-reference-data shortfall detector."** A government or standards body publishes a free reference price/rate; a payer pays something else; nobody joins the two at line-item level. Transfers directly to: *Workers' compensation medical billing and state fee schedule compliance* (state fee schedules are public), *Ambulance and EMS billing*, *Independent pharmacy* (here), *Certified payroll and prevailing wage compliance service providers* (published wage determinations), and *Freight bill audit and payment for small shippers* (contracted tariff versus invoiced).

**B. Statutory floor enacted faster than software adapted — the "new-law arithmetic verifier."** A wave of state legislation creates a checkable numeric obligation 12–24 months before any vendor productizes the check. Transfers to: *Community floodplain administration at small municipalities*, *Multi-state charitable solicitation registration compliance*, *Multi-state income and franchise tax nexus monitoring for small businesses*, and *Patient financial counseling and No Surprises Act Good Faith Estimate compliance*.

**C. Provider-level adjustment opacity — the "why is this deposit short" decoder.** Remittances carry aggregate deductions untraceable to the transactions that caused them. Transfers to: *Small motor carriers back office and settlement* (settlement deductions), *Staffing back-office service bureaus and payroll funders*, *Freight factoring companies*, *Independent pharmacy* (here), and *Small third-party medical billing companies*.

**D. Deadline-clock-as-product.** The right exists, the form exists, the deadline is fixed, and the loss is caused by the clock rather than the merits. Transfers to: *Legal document preparers and registered LDAs*, *Provider credentialing and payer enrollment services*, *Unclaimed property and escheat compliance service providers*, *HOA and condominium management estoppel and demand response desks*, and *Government contracts administration at small govcons*.

**E. Pre-run the auditor's own test.** The audit procedure is published; the pharmacy can execute it on itself before the demand letter arrives. Transfers to: *Small defense suppliers navigating CMMC Level 2* (already completed — worth cross-referencing), *DCAA-audit-ready incurred cost submissions at small government contractors*, *ERISA employee benefit plan auditors at small CPA firms*, *Metal finishing and special-process suppliers*, and *Premium audit and payroll classification consulting*.

**F. Aging-with-per-counterparty-rules.** Generic aging is a solved commodity; aging where the deadline differs per counterparty and is buried in a contract is not. Transfers to: *Certificate-of-insurance compliance from the holder side*, *Mortgage servicer payoff and lien release departments*, *Cargo claims and OS&D handling*, and *Third-party COBRA administrators*.

**G. Local-only desktop as the differentiator, not the compromise.** In regulated small businesses, "runs on your machine, sends nothing anywhere" defeats a better-featured SaaS product. Transfers to essentially every healthcare and legal market in the backlog, and should be treated as a default architectural stance for the catalog rather than a per-product decision.

---

## 8. Sources and confidence

### Verified findings (multiple independent sources, or primary/official documents)

- Market size, store count, volume, and financial condition — [NCPA 2025 Digest release](https://ncpa.org/newsroom/news-releases/2025/10/19/ncpa-releases-2025-digest-report); [NCPA January 2025 member survey executive summary (PDF)](https://ncpa.org/sites/default/files/2025-01/1.27.2025-FinalExecSummary.NCPA_.MemberSurvey.pdf)
- NADAC availability, weekly cadence, and the December 2024 three-month-moving-average change — [Medicaid.gov NADAC](https://www.medicaid.gov/medicaid/nadac); [data.medicaid.gov NADAC 2025 dataset](https://data.medicaid.gov/dataset/f38d0706-1239-442c-a3cc-40ef1b686ac0)
- State NADAC-plus-dispensing-fee floors, states, dates, and dollar amounts — [Frier Levitt, 2026 State PBM Reform](https://www.frierlevitt.com/articles/2026-state-pbm-reform-nadac-reimbursement-spread-pricing-bans/); [MultiState, State PBM Reform in 2025](https://www.multistate.us/insider/2025/10/23/state-pharmacy-benefit-management-reform-in-2025)
- Pharmacy 835 structure — claim identification by prescription/fill reference, `N4` NDC qualifier, CAS adjustments, PLB provider-level adjustments, `FB` forwarding balance, three-business-day EFT/835 rule — [NCPDP Pharmacy Reference Guide to the X12N 835 v5010 (PDF)](https://www.ncpdp.org/NCPDP/media/pdf/X12N835_5010PaymentReferenceGuide.pdf)
- MAC appeal mechanics: 60 days from date of service, 10-day decision, 60-day resubmission, PDF and Excel form formats — [IPM MAC Appeals](https://ipm.rxipm.com/mac-appeals-specific-state-requirements/); [OptumRx appeals submission guide](https://professionals.optumrx.com/resources/manuals-guides/appeals-submission-guide.html); 36 states with MAC statutes and the Georgia remedy structure — [Frier Levitt](https://www.frierlevitt.com/articles/why-filing-mac-appeals-should-be-a-win-win-for-pharmacies/)
- Effective rate formula and mechanics, PSAO-aggregate measurement, annual true-up — [Pharmacy First Effective Rate User Guide (PDF)](https://www.pharmacyfirst.com/wp-content/uploads/2021/02/Pharmacy-First_Effective-Rate-User-Guide_CEO.pdf); [GNP on DIRs, GERs, BERs](https://www.wearegnp.com/insights/what-pharmacies-should-know-about-dir-fees-and-ger-and-ber-recoupments); [Frier Levitt on GER claw-backs](https://www.frierlevitt.com/articles/generic-effective-rate-ger-a-new-type-of-post-sale-clawback-by-pbms/)
- Audit procedure: 14-day desk review, 30-day appeal from final report, finding codes tied to partial or full recovery, documentation requested — [Health Law Alliance, Prime Therapeutics audit guide](https://www.healthlawalliance.com/blog/prime-therapeutics-audit-defense-guide); top-ten discrepancy list and full-claim recoupment — [PBA Health](https://www.pbahealth.com/elements/how-to-minimize-financial-losses-from-pbm-pharmacy-audits/); 2025 audit escalation and NDC-mismatch findings — [Buchanan Ingersoll & Rooney](https://www.bipc.com/pbm-audits-assessment-of-escalating-trends-and-strategies-for-pharmacies); 2026 enforcement trends — [Health Law Alliance](https://www.healthlawalliance.com/blog/pbm-enforcement-trends-independent-pharmacies-must-prepare-for-in-2026)
- Invoice reconciliation audits: wholesaler-direct purchase histories, accreditation requirement, six-year retention, termination risk — [Frier Levitt](https://www.frierlevitt.com/articles/setting-up-your-pharmacy-for-success-preparing-for-and-responding-to-invoice-reconciliation-audits/)
- Return-to-stock: full-claim recoupment past the PBM window, ~10-day reference point, reversal log as a compliance artifact — [PAAS National](https://paasnational.com/pbm-enforcement-of-return-to-stock-policies/); RTS rates (5.1% industry average, 0.56% at one independent) and operational impact — [Blueberry Pharmacy](https://blueberrypharmacy.medium.com/ghosted-at-the-counter-how-return-to-stock-impacts-pharmacy-operations-and-patient-care-e4dcd3dc739a)
- Reconciliation workflow, receivable magnitudes, and the >4%-unpaid-at-60-days figure — [Net-Rx, identifying missing payments](https://net-rx.com/identify-missing-pharmacy-payments/); [Net-Rx, what is pharmacy reconciliation](https://net-rx.com/pharmacy-reconciliation/); [Sykes CPA / Econcile](https://www.sykes-cpa.com/third-party-reconciliation-for-independent-pharmacies/)
- Existing tool landscape — [Outcomes Reconciliation](https://www.outcomes.com/reconciliation); [Net-Rx RecRx](https://net-rx.com/products/recrx/); [Pharmacy Times, three third-party claims tools](https://www.pharmacytimes.com/view/3-third-party-claims-tools-pharmacy-technicians-can-use); [EnlivenHealth 11-store case study](https://enlivenhealth.co/case-studies/independent-pharmacy-group-reduces-claims-reconciliation-time-by-88-with-help-from-enlivenhealth)
- Point-of-sale price concession change and the loss of float — [Pharmacy Times](https://www.pharmacytimes.com/view/it-s-crunch-time-for-cash-flow-and-closures-what-s-on-the-other-side-); [Epstein Becker Green on CY2024 Part D DIR changes](https://www.ebglaw.com/insights/publications/cms-finalizes-changes-to-pharmacy-dir-in-part-d-starting-with-contract-year-2024)
- AR benchmarks (AR 50–70% of monthly sales; 10–15 days in AR; escalate at 60 days) — [Independent Rx Consulting](https://independentrxconsulting.com/pharmacy-accounts-receivable-what-they-tell-you/)
- Proposed federal PBM fee-disclosure rule, comment period closing March 31 2026, and the fact that it obligates disclosure **to plan fiduciaries, not to pharmacies** — [Federal Register, Jan 30 2026](https://www.federalregister.gov/documents/2026/01/30/2026-01907/improving-transparency-into-pharmacy-benefit-manager-fee-disclosure)

### Strong inferences (well-supported by the above, but not stated as such in any single source)

- The dollar magnitude of P3 in a floor state (~$200k/yr on a $3 systematic shortfall at average volume) is my arithmetic from published volume and statutory fee figures, not a published finding.
- That existing reconciliation vendors do not cover below-cost detection against NADAC/state floors, MAC appeal packaging, effective-rate position, will-call compliance, or audit assembly. This is inferred from the absence of those capabilities in their public marketing — a reasonable but not conclusive test, and the first thing to verify in a vendor demo.
- That PMS claim exports contain ingredient cost paid, NDC, quantity, and payer identifiers in usable form across the major systems. Highly likely given the vendor ecosystem that consumes them, but unverified per system.
- That AWP licensing is the binding constraint on an open-source effective-rate tool. AWP's proprietary status is well established; whether a typical pharmacy can export it from its PMS is not.
- That MAC appeal filing rates among independents are low. Strongly implied by the "should be a win-win" framing of the legal commentary, but no survey figure was found.

### Tentative hypotheses requiring practitioner validation

- That a 60-day-from-date-of-service appeal window is the general norm. One PBM's published process says so; others may differ materially, and state law overrides in several jurisdictions.
- That ~10 days is a representative return-to-stock window. PAAS states the figure but the per-PBM detail is paywalled; every window must be read from the pharmacy's own provider manuals.
- That pharmacies will install and trust an unsigned open-source desktop application handling PHI. Untested, and it is the assumption that most cleanly kills the entire suite if wrong.
- That the paid-customization buyer is the pharmacy. Given 30% of independents are considering closure, the PSAO, state association, or specialist CPA firm may be the more realistic customer.
- That MAC appeals produce meaningful recovery rather than prospective-only correction. No success-rate data was located in any public source; this is the largest unquantified variable in the top-ranked concept pair.

### A note on what could not be reached

Practitioner forum evidence (Reddit r/pharmacy and similar) was not retrievable in this environment — the fetch was rejected. The practitioner voice in this report therefore comes from trade press, vendor case studies, CPA and law-firm practice guides, and association surveys rather than from unfiltered peer discussion. That is a real gap: it means the *reported* pain points are ones with a commercial or professional advocate behind them, and genuinely unserved complaints with no advocate may be underrepresented here. Direct practitioner interviews per section 6 are the correction.

---

*End of report — cycle `0d33e95c`, 2026-08-08.*
