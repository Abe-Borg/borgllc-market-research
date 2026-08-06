# Commercial Property Management — Back Office

**Market:** Commercial property management
**Angle:** back-office
**Claim ID:** `3dee0a20`
**Date:** 2026-08-06

---

## 0. Cycle header

### Why this assignment

The ledger held 191 open assignments across 71 markets at the start of this cycle, with 8 reports completed. Commercial property management had **zero completed entries**, which satisfied the first stated preference (breadth over depth). Among the untouched markets I weighed it against structural engineering, general contractor preconstruction, small CPA practices, title/escrow, and medical billing.

I chose commercial property management / back-office for four reasons:

1. **Angle diversity.** Completed reports skew heavily toward `core-practitioner-workflow` (4 of 8). `back-office` had exactly one prior entry (independent insurance agencies). Taking a second back-office assignment in a completely different vertical materially widens the catalog.
2. **The back-office here is not generic admin.** In commercial property management the back office *is* where money is made and lost. Operating-expense recovery, escalations, percentage rent and billbacks are revenue-recognition functions dressed as clerical work. That is unusual and it means the ROI story for a tool is a dollar figure rather than a time saving.
3. **The problems are arithmetic on documents.** Nearly every pain point reduces to "apply a per-counterparty rule set, stored in prose, to a column of numbers, and be able to prove it later." That is precisely the shape of software this catalog is trying to build, and it does not require integrations to be useful.
4. **Existing tooling is genuinely bifurcated.** Enterprise platforms (Yardi Voyager, MRI) are expensive, modular-priced, and hard to learn; small-firm platforms (Buildium, AppFolio) were built residential-first and treat commercial recovery as an add-on. The gap between them is wide and populated by Excel.

I deliberately kept **certificate-of-insurance tracking** out of the centerpiece position even though it surfaced repeatedly in research. The ledger already carries `Certificate-of-insurance compliance from the holder side (GCs, property managers, municipalities)` as its own market, and an existing pattern (`Requirement-profile document parser`) already names commercial property management as a transfer target. Duplicating it here would waste a future cycle. It appears in this report only as context.

**Backlog remaining after this claim: 190 assignments.**

---

## 1. Market examined

### The industry

Commercial property management is the operation of income-producing non-residential real estate — office buildings, retail centers, industrial and flex parks, medical office, and mixed-use — on behalf of owners. IBISWorld tracks property management in the US as a large, highly fragmented industry; the fragmentation is the relevant fact. Below the national service firms (CBRE, JLL, Cushman & Wakefield, Colliers, Newmark, Lincoln, Hines) sits a very long tail of regional and local firms, plus owner-operators who self-manage.

### The organizations that matter for this catalog

The buyer profile is not the national firm. It is:

- **Third-party regional management firms, roughly 5–60 employees**, managing between 15 and 200 commercial properties for multiple ownership entities. These firms carry property managers, property administrators, and one to four property accountants. They typically run one platform (Yardi Breeze/Voyager, MRI, Rent Manager, Re-Leased, or QuickBooks plus Excel) and a great deal of Excel around it.
- **Owner-operators / private landlords with in-house management**, often family offices or local development companies holding 5–40 assets. These are the most Excel-dependent of all and frequently have one person who "does CAM."
- **Outsourced real-estate accounting shops** (a growing category — Keystone, Madras, Analytix, RE BackOffice, Springbord and similar) that perform reconciliation, AP and lease administration as a service for the two groups above. These are excellent early customers for tooling because their margin is directly a function of hours per reconciliation.
- **Retail-focused managers** of strip centers, power centers and small malls, where percentage rent and sales reporting add an entire additional workflow.

### The users

- **Property Administrator / Assistant Property Manager** — the highest-volume user. The Indeed posting reviewed for this report ([Equitable Real Estate Partners, Henrico VA, $60–67k, posted 2026-07-27](https://to.indeed.com/aa7kdjq647yr)) lists, in one role: AP invoice coding and PO/contract matching, tenant bill-backs and miscellaneous invoicing, delinquency monitoring and past-due notices, budget assembly and bid collection, CAM reconciliation assistance, maintenance of lease documents, vendor contracts, **certificates of insurance, permits and regulatory documentation**, vendor W-9 and licensing files, and work-order tracking. Required experience: 5 years property management, 5 years AP, 5 years AR, **3 years MRI**. That single job description is the best available map of this market's back office.
- **Property Accountant** — owns the general ledger, month-end close, recovery calculations, and the reconciliation packages.
- **Lease Administrator** — at firms large enough to have one. Abstracts leases, maintains critical dates, sets up billing schedules, handles estoppels. The [Turnberry Senior Lease Administrator posting](https://to.indeed.com/aamv8v8x2bqg) ($64k–$97k, Aventura FL) confirms the role exists at mid-size operators.
- **Property Manager** — reviews and signs off, handles tenant disputes, owns the owner relationship.
- **Controller / owner principal** — reviews reconciliations before release, signs the management-fee invoice, faces the owner's auditor.

### Organization size sweet spot

Firms with **20–150 commercial tenants under management** are the target. Below that, a single spreadsheet genuinely suffices. Above roughly 400 tenants, the firm has usually bought a full enterprise stack and hired consultants to configure it, which changes the buying decision from "does this tool help" to "does it integrate with Voyager."

---

## 2. How the work is performed

The commercial property back office runs on a calendar with a monthly loop, an annual loop, and an event-driven loop. Understanding which loop a problem sits in determines whether a tool gets used twelve times a year, once a year, or on demand.

### 2a. Lease intake and abstraction (event-driven)

A signed lease or amendment arrives — often as a scanned PDF, sometimes 60–120 pages with exhibits. Someone must extract the terms that drive money:

- Premises rentable square feet and the **denominator** used for pro-rata share (building RSF vs. leasable RSF vs. occupied RSF — the choice is lease-specific and is a frequent error source)
- Base rent schedule and step increases by date
- Escalation method: fixed percentage, fixed dollar, or CPI (which index, which base month, which lag, floors and ceilings)
- Recovery structure: triple net, modified gross, base-year stop, or fully gross
- Expense pool membership (a retail center may have separate CAM, insurance, tax, and marketing/promo pools, plus an anchor-excluded pool)
- Caps: annual vs. cumulative vs. compounding, controllable vs. all
- Exclusions: the negotiated carve-out list, often a full page of prose
- Gross-up permission and threshold (typically 90–100% occupancy)
- Reconciliation delivery deadline (commonly 60–180 days after year end; one source puts the practical norm at 90–120 days)
- Audit rights: window, cost-shifting threshold, notice requirements
- Percentage rent terms: rate, natural or artificial breakpoint, whether the breakpoint escalates with base rent, sales-reporting frequency, exclusions from gross sales
- Critical dates: renewal option windows, termination options, expansion/ROFO/ROFR notice windows, security deposit burn-downs, TI allowance draw deadlines

That abstract is then keyed into the property management system as a set of billing schedules and recovery setups, and — nearly always — copied again into an Excel workbook that the property accountant actually trusts. Published lease-abstraction pricing sits in the range of low-tens of dollars per lease for offshore services to a few hundred for domestic specialist work, with turnaround measured in days; that market exists precisely because doing it in-house is slow.

**This is the single most consequential step in the entire back office, and it is performed once, by one person, usually under time pressure, and rarely re-verified.** Every downstream calculation inherits its errors.

### 2b. Monthly loop

1. **Recurring charges post.** Base rent, estimated CAM/opex, insurance and tax escalations, storage, parking, after-hours HVAC.
2. **AP intake.** Vendor invoices arrive by email, mail and portal. The administrator codes each to a GL account and a property, matches to a PO, service contract or work order, routes for approval, and files it. Industry benchmarking cited by PredictAP puts average cost per invoice at **$12.88 against a best-in-class $2.78**, with **9.2-day average cycle time vs. 3.1 days** for leaders.
3. **Coding decisions with recovery consequences.** Each invoice implicitly answers: is this operating or capital? Is it recoverable? Which pool? Is it tenant-specific and therefore billable directly? Those answers are made in seconds by a $60k administrator and are not revisited until the annual reconciliation eleven months later.
4. **Billbacks.** Tenant-caused or tenant-requested work — after-hours HVAC, lock changes, tenant-side plumbing, sign installs, damage repair — must be identified, marked up per the lease or management agreement, invoiced and collected.
5. **Utility rebilling.** Where the building has submeters, reads are collected (often manually), converted to consumption, allocated, and billed. Where it has no submeters, consumption is allocated by RSF or by a negotiated formula.
6. **AR and delinquency.** Aging is reviewed; late fees are assessed per lease-specific grace periods and rates; past-due notices go out; default notices with lease-specific cure periods are prepared, sometimes with counsel.
7. **Month-end close and owner reporting.** GL close, accruals, variance narrative against budget, owner statement package, distribution calculation, management-fee calculation.
8. **Management fee.** Almost always a percentage of collected revenue — but *which* revenue is defined in the management agreement, and definitions vary (does it include CAM reimbursements? percentage rent? termination fees? insurance proceeds?). This is computed by hand at many firms.

### 2c. Annual loop

- **Budget season** (roughly August–November). Vendor bids collected, contracts repriced, capital plan assembled, next-year CAM estimates derived from the budget and re-billed to tenants as new monthly estimates.
- **Reconciliation season** (January–April). The main event, described below.
- **Percentage rent settlement** for retail, typically 60–90 days after lease-year end.
- **Insurance renewal**: statement of values, square footage, replacement cost, loss runs.
- **Property tax**: assessment notices arrive on jurisdiction-specific dates, appeal windows are short and vary by state and county (Texas alone has county-by-county protest deadlines), and tax is usually a recoverable expense so an appeal outcome flows straight into tenant billing.
- **1099 filing** for vendors and, where the manager collects rent for owners, for owners as well — requiring current W-9s and correct TINs.
- **Trust/escrow account compliance** where the firm holds client funds under a real estate broker license. Several states mandate three-way reconciliation and prescribe record retention (Arizona A.R.S. §32-2175 is an explicit example; Colorado DRE publishes three-way reconciliation guidance; California DRE sets broker record retention).

### 2d. The annual reconciliation, in detail

This is the workflow the rest of the report keeps returning to.

1. **Close the year and pull the GL** for each property, by expense account.
2. **Classify every expense**: recoverable vs. non-recoverable, operating vs. capital, which pool, and any tenant-specific carve-out. Roof replacement and HVAC unit replacement are the canonical capital-vs-operating traps.
3. **Gross up occupancy-sensitive expenses** where the lease permits — utilities, janitorial, waste, sometimes management fee. Fixed costs like taxes and insurance should *not* be grossed up; misclassifying a fixed cost as variable is described by Baker Tilly as the most frequent gross-up error.
4. **Apply per-tenant lease terms**: pro-rata share using the correct denominator, exclusions, caps (annual, cumulative, compounding, controllable-only), base-year stops, admin fee percentages, and any negotiated cap on the admin fee itself.
5. **Compute the true-up**: (adjusted pool × share) − amounts already billed = owed or credit.
6. **Build the backup package**: expense summary by category, calculation detail, and enough invoice-level support to survive an audit request.
7. **Deliver by the lease deadline**, which differs per tenant. Late delivery can, under some lease language, waive the landlord's right to collect.
8. **Reset next year's estimates** and post the new monthly billing.
9. **Defend disputes and audits.** Tenants — especially national retail and office tenants with lease-audit firms on contingency — request backup, question classifications, and negotiate.

Portfolio size drives the tooling: 1–3 properties on QuickBooks plus Excel; 4–25 on Buildium/AppFolio CAM modules; 25+ on Yardi or MRI. Reconciliation completion runs **60–90 days for typical operators vs. 30–45 days for top performers**.

---

## 3. Most important problems, ranked

### P1 — The recovery calculation is a per-tenant rule set stored in prose, executed in Excel, and never verified against the lease again

**Who:** property accountants and property administrators at firms of every size, and the outsourced accounting shops serving them.
**When:** annually at reconciliation, and monthly whenever estimates are reset.
**Currently handled by:** a per-property Excel workbook, hand-built, inherited from a predecessor, with tenant columns and expense rows; or a Yardi/MRI recovery setup configured once at lease commencement and thereafter trusted.
**Why inadequate:** the workbook encodes lease terms as formulas with no link back to the lease language, so nobody can answer "why is this tenant's cap 4% cumulative" without reopening a 90-page PDF. The enterprise systems encode the same terms as configuration fields that are equally invisible and equally unverified. When a lease is amended — a very common event — the amendment updates the PDF and, often, nothing else.
**Frequency:** every reconciliation, every tenant. A 40-tenant portfolio is 40 independent rule executions.
**Cost:** Tango Analytics' 2023 analysis is cited for **40% of CAM reconciliations containing material errors**; JLL 2023 is cited for **28% of tenants independently finding discrepancies**; specialist auditors claim recovery of **15–20% of billed charges** when engaged. PredictAP frames the industry-wide leakage at **$5–15 billion annually**, **$100k–$400k per property**, and notes the valuation multiplier: a $100k recurring CAM recovery loss reduces asset value by $1–2M at typical cap rates. These figures come from vendors with an interest in the number being large and should be treated as directional, not precise — but the direction is consistent across independent sources and matches the existence of an entire contingency-fee lease-audit industry.
**Evidence quality:** strong. Multiple independent sources (law firms, accounting firms, software vendors on both the landlord and tenant side) describe the same failure modes: wrong pro-rata denominator, missing caps, missing exclusions, capital treated as operating, no gross-up or wrong gross-up, late delivery.

### P2 — Expense classification decisions are made monthly at AP and audited annually, eleven months too late

**Who:** property administrators coding AP; property accountants who inherit the coding.
**When:** every invoice, every month.
**Currently handled by:** the administrator's judgment plus a GL chart of accounts, with a property manager approving.
**Why inadequate:** the person coding does not have the lease exclusion lists in front of them and generally could not apply them if they did — exclusions are per-tenant, not per-property, and a single invoice may be recoverable for one tenant and excluded for another. The recoverability question is therefore deferred to reconciliation, when the person answering it is looking at a GL line item like "ABC Mechanical — 4,820.00" with no memory of what it was.
**Frequency:** continuous. AP volume for a 20-property portfolio is easily several hundred invoices monthly.
**Cost:** the $12.88 average per-invoice processing cost is the visible part; the invisible part is that reconciliation season is spent re-deriving classification decisions from vendor names, which is the direct cause of P1's error rate. It also produces the reconciliation's longest pole: sources cite 60–90 days typical vs. 30–45 for leaders, a difference substantially attributable to whether classification was done as you go.
**Evidence quality:** strong for the process description (job postings, accounting-firm guides), moderate for the cost attribution.

### P3 — Escalations and rent steps are date-triggered obligations with no failure signal

**Who:** lease administrators, property administrators, small owner-operators.
**When:** on each lease's anniversary or step date, scattered across the calendar.
**Currently handled by:** billing schedules entered once into the PMS, an Outlook reminder, or a "rent roll" spreadsheet with a step column.
**Why inadequate:** a fixed step usually gets entered correctly because it is a known number. **CPI escalations do not**, because they require pulling the correct index series (CPI-U, which area, which base month), applying the lease's lag and rounding, respecting floors and ceilings, and documenting the vintage used. Missing an escalation is a silent failure — the tenant does not complain, the GL balances, and the shortfall compounds for the remaining lease term. Recovering it later is a negotiation, not a right, and many landlords simply eat it.
**Frequency:** each tenant, annually.
**Cost:** a missed 3% escalation on a $180k/yr lease is $5,400 in year one and roughly $28k over a five-year remaining term, plus the permanently lower base that flows into every subsequent renewal and into the asset's valuation.
**Evidence quality:** strong on mechanics (multiple legal and vendor sources describe CPI escalation disputes and the index-selection problem); the frequency of *missed* escalations is a strong inference rather than a measured figure.

### P4 — Percentage rent and tenant sales reporting is an unenforced obligation

**Who:** retail property managers and administrators.
**When:** monthly or quarterly sales reports, plus annual certification.
**Currently handled by:** a spreadsheet of who reported what, chased by email.
**Why inadequate:** tenants under-report or simply stop reporting; nobody notices until year-end. Breakpoints must escalate in parallel with base rent in stepped leases and frequently do not get updated. Exclusion definitions (returns, employee discounts, inter-store transfers, and now BOPIS/e-commerce fulfilled from the store) are contested and inconsistently applied. Multi-location tenants report on their own format.
**Frequency:** monthly for every retail tenant with a percentage clause.
**Cost:** unbilled percentage rent is pure lost revenue. The occupancy-cost-ratio analysis that sales data enables (total occupancy cost ÷ gross sales, with 12–15% signalling distress) is also lost, which removes an early-warning signal on tenant credit.
**Evidence quality:** strong on mechanics and disputes; magnitude is property-specific.

### P5 — Billbacks are identified by memory

**Who:** property administrators and building engineers.
**When:** whenever chargeable work occurs.
**Currently handled by:** the work-order system records the work; a human later decides whether it was chargeable and to whom, then creates a miscellaneous invoice.
**Why inadequate:** the decision requires the lease (is this landlord's or tenant's obligation?), the management agreement (what markup is permitted?), and the work order (what actually happened?) simultaneously. When the administrator is busy, work simply does not get billed. Building Engines frames the metric set — total expected recovery, disputes, days-to-collect, error count — which implies these are commonly not tracked at all.
**Frequency:** continuous; concentrated in office and medical office.
**Cost:** small per event ($150–$2,500 typical), large in aggregate, and 100% margin when captured.
**Evidence quality:** moderate. The problem is well described by vendors; independent practitioner quantification is thin.

### P6 — Critical dates are known but not converted into landlord action dates

**Who:** lease administrators, property managers, owners.
**When:** option windows, which are typically 6–12 months before expiration and often only 30–60 days wide.
**Currently handled by:** a critical-date spreadsheet or the PMS's date fields, reviewed in a monthly meeting.
**Why inadequate:** a spreadsheet stores the tenant's deadline. It does not store the landlord's *preparation* deadline — the date by which market rent must be determined, an offer prepared, or a notice mailed under the lease's specific delivery method. Landlord-side obligations (responding to an exercised option within N days, delivering a market-rent determination, honoring a ROFR within N days of receiving a third-party offer) are conditional and event-triggered, which spreadsheets handle badly.
**Frequency:** several times per year per portfolio.
**Cost:** an unexercised or badly handled option can mean a vacancy, or a below-market renewal locked in for five years.
**Evidence quality:** strong on the workflow, moderate on the failure rate.

### P7 — Reconciliation backup packages are assembled by hand under deadline

**Who:** property accountants.
**When:** at delivery and again whenever a tenant disputes or audits.
**Currently handled by:** exporting a GL detail, printing a workbook tab, and attaching invoice PDFs pulled one by one.
**Why inadequate:** the statement the tenant receives and the workbook the accountant used are separate artifacts with no enforced tie. When a tenant asks "show me the invoices behind line 6420," it is a manual retrieval exercise months after the fact. Landlords are obligated under most leases to provide supporting documentation on request, and unclear statements are named by accounting-firm sources as a leading contributor to landlord-tenant disputes.
**Frequency:** every reconciliation for statement production; a subset trigger full audits.
**Cost:** days of accountant time per contested reconciliation, plus negotiated concessions made because backup could not be produced quickly.
**Evidence quality:** strong.

### P8 — Trust-account and records compliance is a licensing risk handled informally

**Who:** broker-licensed management firms holding client funds.
**When:** monthly reconciliation; on audit.
**Currently handled by:** the bookkeeper's bank reconciliation, sometimes without the third leg.
**Why inadequate:** several states require a **three-way** reconciliation (bank balance = book balance = sum of individual owner/tenant ledgers) and prescribe record retention. Arizona codifies property-management record requirements and audit authority at A.R.S. §32-2175; Colorado's Division of Real Estate publishes three-way reconciliation guidance; California sets broker record-retention obligations. Commingling and unreconciled trust accounts are among the most common findings in broker audits.
**Frequency:** monthly.
**Cost:** license discipline is existential for the firm; the routine cost is the hours spent proving the third leg by hand.
**Evidence quality:** strong on the legal requirement; moderate on how many small firms actually skip it.

### P9 — Property tax assessment and appeal deadlines are jurisdiction-specific and short

**Who:** property managers and asset managers.
**When:** assessment notices arrive on a jurisdiction calendar.
**Currently handled by:** the tax consultant, if one is engaged, or an annual reminder.
**Why inadequate:** deadlines vary by state and, in states like Texas, by county. Tax is normally a recoverable expense, so a successful appeal reduces tenant billing and an unappealed over-assessment is billed straight through to tenants — who may then dispute it.
**Frequency:** annual, per parcel.
**Cost:** a missed appeal window is a full year of over-assessment.
**Evidence quality:** strong on the deadline variance, weak on how often small managers actually miss it.

---

## 4. Application opportunities

### O1 — RecoveryLedger: lease-rule-driven operating expense reconciliation engine

**Intended user:** property accountant, outsourced real-estate accounting shop, owner-operator doing their own CAM.

**Problem solved:** P1, P7. The reconciliation calculation lives in a hand-built workbook with no traceability to lease language and no reusability across years.

**Current workflow:** export GL → open last year's workbook → update the expense column → hope the tenant formulas are still right → paste into a statement template → email PDFs.

**Proposed workflow:** define each tenant once as a structured **recovery profile** (pool memberships, share numerator/denominator, exclusion list, cap type and history, base-year amount, gross-up permission and threshold, admin fee, deadline). Import the GL as CSV. Map accounts to pools. Run. Output is a per-tenant statement, a per-tenant calculation trace showing every rule applied with the lease section cited, and a portfolio summary.

**Inputs:** GL export (CSV/XLSX), a recovery profile per tenant (YAML/JSON, editable in a form), occupancy by month, prior-year billed amounts.

**Outputs:** tenant statements (PDF/XLSX), calculation trace per tenant, portfolio true-up summary, next-year estimate schedule, an exceptions list (missing profile, unmapped GL account, cap breached, deadline within N days).

**Essential features:** cap arithmetic that handles annual / cumulative / compounding and controllable-only variants with multi-year carryforward; correct gross-up restricted to accounts flagged variable; base-year stop; explicit denominator selection; deadline tracking per tenant; a full trace of every arithmetic step.

**Deliberately excluded:** general ledger accounting, AP, tenant portal, e-signature, integration with Yardi/MRI at v1 (CSV in, CSV out).

**AI:** inappropriate for the calculation. Optional for a separate assist that proposes a recovery profile from a lease PDF (see O2) — but the calculation itself must be deterministic, auditable, and reproducible. An AI-computed CAM statement is unusable in a dispute.

**Why not a spreadsheet:** a spreadsheet can do the arithmetic. It cannot version the rule set, carry a cap forward across years with an audit trail, cite a lease section, or produce a defensible trace. And in practice every property's workbook is different, so knowledge does not transfer between properties or staff.

**Complexity:** medium. **Learning difficulty:** moderate — the concepts are the user's own domain; the work is defining profiles once.

**Value:** compresses the 60–90-day reconciliation cycle toward the 30–45-day leader benchmark; directly attacks a 40%-material-error rate; makes the tenant-audit response a report rather than a project.

**Risks:** financial calculations that go into billing carry real liability if wrong — the tool must be extensively tested and must never silently guess. Lease interpretation remains the user's responsibility and the UI must say so. Tenant financial data is confidential.

**Existing products/substitutes:** Yardi and MRI recovery modules (powerful, expensive, opaque, configured by consultants); Buildium/AppFolio CAM features (residential-first, thin on caps/gross-up/base-year); CapVeri, Stratafolio, Re-Leased, Rioo (commercial SaaS, subscription, cloud-hosted); outsourced services (RE BackOffice, Springbord, Keystone, Madras).

**Why still attractive:** none of these give a small firm a *free, local, auditable* engine whose rules are readable text a controller can review. The market is bifurcated between expensive platforms and Excel; the open-source middle is empty. Owner-side confidentiality also argues for a local tool.

**Paid customization:** very high. Every firm's GL chart differs, every portfolio has odd pools (retail promo funds, anchor exclusions, parking decks, multi-parcel allocations). Profile authoring, GL mapping, and statement branding are natural paid engagements, as is a Yardi/MRI export adapter.

---

### O2 — LeaseProfile: lease-to-recovery-profile extractor with mandatory human confirmation

**Intended user:** lease administrator, property accountant onboarding a new asset.

**Problem solved:** the abstraction bottleneck feeding P1, P3, P4, P6.

**Current workflow:** read the lease PDF, type terms into a form or spreadsheet, key them again into the PMS.

**Proposed workflow:** drop the lease PDF in. The tool locates and quotes the candidate provisions (premises RSF, pro-rata definition, recovery structure, caps, exclusions, gross-up, escalation method, percentage rent, option windows, reconciliation deadline, audit rights), presents each as *quoted lease text plus a proposed structured value*, and requires the user to confirm or correct each field before it is written. Output is the recovery profile consumed by O1 and the critical-date set consumed by O5.

**Inputs:** lease PDF (and amendments, processed as a chain).

**Outputs:** structured profile (JSON/YAML), a side-by-side confirmation sheet showing quote → value → page reference, an "unfound" list for provisions it could not locate.

**Essential features:** amendment chaining (amendment 3 supersedes amendment 1 on the same term); page/section citation for every extracted value; explicit "not found" rather than a guessed default; export to O1 and O5.

**Deliberately excluded:** full lease abstract for legal purposes; clause risk scoring; anything that writes to the PMS unattended.

**AI:** **appropriate and materially advantageous.** Locating a gross-up provision in unstructured legal prose across wildly varying lease forms is exactly what conventional parsing fails at. But the design must be extract-and-cite, never extract-and-assume: the human confirms every field, and the citation makes confirmation fast.

**Why not a spreadsheet:** the input is a PDF; there is nothing to formula against.

**Complexity:** medium. **Learning difficulty:** low — it is a review-and-confirm screen.

**Value:** replaces a 1–3 hour manual abstraction per lease with a 20–30 minute confirmation, and — more importantly — produces a structured artifact where today the output is prose in someone's head.

**Risks:** hallucinated values are the central risk; mitigated by mandatory confirmation and by refusing to output unconfirmed fields. Leases are confidential — a local-model or bring-your-own-key design matters. Do not market it as legal review.

**Existing products/substitutes:** Lextract, Prophia, Leasecake, Occupier, DDee, plus offshore abstraction services at low per-lease pricing.

**Why still attractive:** the commercial products sell portfolio-management platforms with abstraction attached; nobody sells a small, local, confirm-every-field extractor whose output is a file you own. The offshore services are cheap but slow and produce a PDF abstract, not machine-readable rules.

**Paid customization:** high — landlord-form-specific extraction tuning, and integration of the profile output into a firm's existing workbook.

---

### O3 — RecoverySetup Auditor: drift detector between the lease abstract and the billing configuration

**Intended user:** controller, property accountant, or an owner's asset manager doing a health check.

**Problem solved:** P1 and P3, from the other direction — not "compute the reconciliation" but "is what we have been billing all year actually what the lease says?"

**Current workflow:** nobody checks. The setup was done at commencement; drift is discovered when a tenant audits.

**Proposed workflow:** feed the tool (a) the structured lease profiles and (b) an export of the current billing/recovery setup from the PMS or the rent roll. It produces a mismatch report: pro-rata share differs from lease-computed share; escalation date passed with no rate change; cap not configured though the lease has one; recovery structure mismatch; RSF differs between rent roll and lease; deadline configured beyond the lease's limit; percentage rent breakpoint not escalated with base rent.

**Inputs:** lease profiles (from O2 or hand-entered), rent roll / billing schedule export, recovery setup export.

**Outputs:** ranked mismatch report with dollar impact estimate where computable, and a remediation checklist.

**Essential features:** tolerant field matching across differing export formats; dollar-impact estimation; suppress-with-reason so known intentional deviations stop reappearing.

**Deliberately excluded:** writing corrections back to the PMS; anything requiring live API access.

**AI:** inappropriate. This is set comparison with domain rules.

**Why not a spreadsheet:** a VLOOKUP compares two columns. It cannot recompute a pro-rata share from a lease definition, apply a cap history, or decide that a passed escalation date with an unchanged rate is a finding.

**Complexity:** small-to-medium. **Learning difficulty:** low.

**Value:** finds silent revenue leakage — the highest-value category, because missed escalations and wrong shares compound. Also the natural due-diligence tool at acquisition, which is a second market.

**Risks:** false positives will erode trust; the suppress-with-reason feature is essential, not optional.

**Existing products/substitutes:** lease-audit consultants (tenant side, contingency); internal audit; nothing packaged on the landlord side for small firms.

**Why still attractive:** it is the cheapest possible version of the expensive thing (a lease audit), aimed at the party who would rather find the error first.

**Paid customization:** high — export-format adapters per PMS.

---

### O4 — EscalationRun: annual rent step and CPI escalation batch calculator with notice generation

**Intended user:** property administrator, lease administrator, small owner-operator.

**Problem solved:** P3.

**Current workflow:** a rent-roll tab with a step column, worked manually each anniversary; CPI escalations computed by looking up an index on the BLS site and doing the math in a corner of the sheet, with the vintage undocumented.

**Proposed workflow:** load the lease profiles and a date range. The tool lists every escalation event due in the window, computes the new rate — fixed, fixed-dollar, or CPI with the lease's specified index, area, base month, lag, rounding, floor and ceiling — shows the arithmetic, and generates the tenant notice letter with the index values and publication dates stated.

**Inputs:** lease profiles, CPI series values (a maintained local data file, refreshed by download; BLS series are public), effective date range.

**Outputs:** escalation schedule with old/new rates, per-lease calculation trace, tenant notice letters (DOCX/PDF), and a CSV to key into the PMS.

**Essential features:** all three escalation methods; correct handling of "greater of CPI or 3%, not to exceed 5%" compound language; explicit statement of which index vintage was used (this is what wins the dispute); a look-back mode that flags escalations that should already have happened and didn't.

**Deliberately excluded:** live BLS API dependency (ship a data file and a refresh script — a fragile integration would break the tool at exactly the wrong moment); invoicing; PMS write-back.

**AI:** inappropriate. This is arithmetic on a published index.

**Why not a spreadsheet:** it could be one — and this is the concept where that objection has the most force. The differentiator is the look-back audit, the correct handling of floor/ceiling compound language, the documented index vintage, and the generated notice. A firm's spreadsheet does none of those and, critically, does not tell you about the escalation you forgot two years ago.

**Complexity:** small. **Learning difficulty:** low — under an hour.

**Value:** each caught escalation is worth thousands to tens of thousands over the remaining term, at essentially zero marginal cost. The clearest ROI story in this report.

**Risks:** using the wrong CPI series is the failure mode; the tool must force explicit series selection rather than defaulting. Index revisions must be handled (BLS revises some series).

**Existing products/substitutes:** PMS billing schedules (handle fixed steps well, CPI poorly); free CPI calculators (single-lease, no notice, no audit); Lextract/LeasePilot calculators.

**Why still attractive:** the batch + look-back + notice-generation combination does not exist in a free tool, and CPI escalation is the specific case every platform handles badly.

**Paid customization:** moderate — letter templates, unusual index bases, non-US indices.

---

### O5 — OptionClock: critical-date register with back-solved landlord action dates

**Intended user:** lease administrator, property manager, owner principal.

**Problem solved:** P6.

**Current workflow:** a critical-date spreadsheet listing tenant deadlines, reviewed monthly.

**Proposed workflow:** ingest the critical dates from the lease profile. For each, back-solve the *landlord's* action dates using configurable lead times: market-rent determination due, offer package due, notice-mailing date accounting for the lease's required delivery method and any deemed-receipt rule, and the landlord's own response deadline once a tenant exercises. Produce a rolling action calendar, not a date list.

**Inputs:** lease profiles or a manual date entry form; firm-level lead-time policy.

**Outputs:** action calendar (ICS export, HTML view, printable), a 90-day action list, and an event log recording what was done and when — which is itself the evidence if a dispute arises.

**Essential features:** back-solving with configurable lead times; conditional/event-triggered obligations (ROFR clock starts when a third-party offer is received, not on a fixed date); the event log; ICS export so it lands in the calendar the user already reads.

**Deliberately excluded:** email sending, task assignment, anything resembling a project management tool. It writes to a calendar and prints a list.

**AI:** inappropriate for the clock. Optional upstream via O2 to find the dates.

**Why not a spreadsheet:** conditional and event-triggered obligations, delivery-method arithmetic, and an immutable action log are all things spreadsheets model badly. The deeper reason: a spreadsheet stores the tenant's deadline, and the tenant's deadline is not an action item for the landlord.

**Complexity:** small. **Learning difficulty:** low.

**Value:** one preserved above-market renewal or one avoided vacancy pays for years of use.

**Risks:** miscalculating a notice date is worse than not having the tool; delivery-method rules must be per-lease and conservative. The tool must not be presented as legal advice on notice sufficiency.

**Existing products/substitutes:** PMS date fields, Occupier, Leasecake, LeaseCommand, Outlook reminders.

**Why still attractive:** every existing product stores dates. Almost none convert them into the landlord's own dated tasks, and none of the small ones are free.

**Paid customization:** moderate.

---

### O6 — SalesLedger: retail gross-sales reporting register and percentage rent calculator

**Intended user:** retail property manager or administrator at a center with 10–80 tenants.

**Problem solved:** P4.

**Current workflow:** a spreadsheet of monthly sales by tenant, populated from emailed reports in whatever format the tenant sends, chased by email; percentage rent computed at year end, sometimes.

**Proposed workflow:** define each tenant's reporting obligation (frequency, due date, breakpoint type, rate, exclusions, escalation linkage to base rent). The tool maintains the register, produces a **delinquent-reporting chase list** with pre-written reminder text, ingests reports (CSV, or manual entry, or a simple email-parsed format), computes percentage rent against a breakpoint that escalates with base rent, and reports occupancy-cost ratio per tenant.

**Inputs:** tenant obligation definitions, monthly sales figures, base rent schedule.

**Outputs:** reporting compliance status, chase list, percentage rent calculation with trace, occupancy-cost-ratio table with a configurable distress threshold, annual settlement statements.

**Essential features:** escalating breakpoint tied to base rent steps (the specific thing that breaks in long leases); missing-report tracking with an age; exclusion categories applied per lease definition; occupancy-cost ratio flagging.

**Deliberately excluded:** POS integration; sales forecasting; anything requiring the tenant to log into something.

**AI:** optional and narrow — normalizing inconsistent tenant-submitted sales report formats. Rules and a per-tenant mapping handle most of it; AI is a fallback for the tail.

**Why not a spreadsheet:** it usually is one, and it fails at exactly two points: nobody notices non-reporting, and the breakpoint does not escalate. Both are structural, not effort, problems.

**Complexity:** medium. **Learning difficulty:** low-to-moderate.

**Value:** recovers percentage rent that is currently not billed, and surfaces tenant distress months before a default.

**Risks:** tenant sales data is highly confidential and often protected by lease confidentiality clauses — local-only storage is close to mandatory. Do not aggregate across landlords.

**Existing products/substitutes:** Yardi/MRI retail modules; Nakisa; spreadsheets.

**Why still attractive:** small retail landlords are the most spreadsheet-bound segment in this market and the percentage-rent leakage is direct revenue.

**Paid customization:** high — per-tenant report format mapping is inherently bespoke.

---

### O7 — BillbackGate: chargeable-work determination and billback invoice builder

**Intended user:** property administrator; building engineer as a data source.

**Problem solved:** P5.

**Current workflow:** work orders close in the maintenance system; someone remembers to bill some of them.

**Proposed workflow:** import closed work orders (CSV export from any system). For each, the tool applies a rules table derived from the lease and management agreement — work category × tenant × premises location → chargeable / not chargeable / needs review — and computes the billable amount with the permitted markup. It produces a review queue and, on approval, a billback invoice with a lease-clause citation on the face of it.

**Inputs:** work-order export, vendor cost or labor hours and rates, per-tenant chargeability rules, markup policy.

**Outputs:** review queue, billback invoices (PDF), a monthly unbilled-recovery report showing what was closed and never billed.

**Essential features:** the unbilled report (this is the actual product — the invoice is easy, noticing the omission is the value); citation on the invoice, which reduces disputes; markup rules per management agreement.

**Deliberately excluded:** being a work-order or CMMS system; field mobile app; payment processing.

**AI:** optional — classifying free-text work-order descriptions into categories. A keyword rules table plus a review queue gets most of the way; AI is a convenience.

**Why not a spreadsheet:** the volume and the cross-referencing (work order × lease obligation × markup policy) exceed comfortable spreadsheet use, and the unbilled report requires reconciling two sets.

**Complexity:** small-to-medium. **Learning difficulty:** low.

**Value:** captured billbacks are near-100% margin. Even modest capture improvement across a portfolio is meaningful.

**Risks:** billing a tenant for landlord-obligation work damages the relationship — the review queue must be mandatory, never auto-send.

**Existing products/substitutes:** Building Engines, Prism, Yardi Maintenance billbacks — all bundled into platforms.

**Why still attractive:** it works alongside whatever CMMS the firm already has, needs only a CSV, and is the only piece of the platform they actually wanted.

**Paid customization:** moderate — the rules table is firm-specific.

---

### O8 — ReconPacket: audit-ready reconciliation backup binder assembler

**Intended user:** property accountant responding to a tenant CAM audit or a routine backup request.

**Problem solved:** P7.

**Current workflow:** pull GL detail, find invoices one at a time, assemble a PDF, redact what shouldn't be shared, send.

**Proposed workflow:** given a reconciliation output (from O1 or from the firm's own workbook, as CSV) and a folder of AP invoice PDFs indexed by invoice number or vendor+date, assemble a bookmarked binder: statement, expense summary by pool, GL detail per pool, and the underlying invoices, with a cover index and a completeness report naming every GL line for which no supporting document could be located.

**Inputs:** reconciliation detail CSV, invoice PDF folder, a mapping of GL line to invoice reference.

**Outputs:** single bookmarked PDF binder, index CSV, missing-support exception list.

**Essential features:** the missing-support list (find out before the tenant does); bookmarking by pool and account; scope control (only the pools this tenant participates in — do not hand a tenant another tenant's data).

**Deliberately excluded:** OCR of unsearchable scans at v1; redaction automation (flag, don't auto-redact); document management.

**AI:** optional, for matching invoice PDFs to GL lines when no invoice number is recorded. Deterministic matching on invoice number + amount + vendor covers most.

**Why not a spreadsheet:** the deliverable is a PDF binder.

**Complexity:** small-to-medium. **Learning difficulty:** low.

**Value:** converts a multi-day scramble into a run; the missing-support report is a pre-emptive risk finding.

**Risks:** over-disclosure — sending a tenant documents outside their pools, or unredacted third-party pricing, is a real hazard. Scope control must be explicit and default-restrictive.

**Existing products/substitutes:** Yardi/MRI document attachments; manual assembly.

**Why still attractive:** this pattern (bookmarked evidence binder from a structured index) is already recorded in the ledger from the fire-protection cycle and transfers cleanly; the CRE-specific part is the pool-scoped disclosure control.

**Paid customization:** moderate.

---

### O9 — TrustCheck: three-way trust account reconciliation and exception report

**Intended user:** broker-licensed management firm's bookkeeper or controller.

**Problem solved:** P8.

**Current workflow:** a two-way bank reconciliation; the third leg (sum of individual ledgers) proved by hand or not at all.

**Proposed workflow:** import bank statement, book balance, and the individual owner/tenant ledger balances. The tool performs the three-way match, lists variances by ledger, flags negative individual ledgers (a classic commingling indicator), flags stale outstanding items, and produces a dated, signable reconciliation report formatted for an examiner.

**Inputs:** bank statement CSV/OFX, GL trust account detail, individual ledger balances export.

**Outputs:** three-way reconciliation report (PDF), variance list, negative-ledger and stale-item exception lists, a retained history.

**Essential features:** the three-way match itself; negative individual ledger detection; a retained monthly history, since the examiner asks for the last N months.

**Deliberately excluded:** being an accounting system; bank connectivity (CSV import only — bank integrations are the fragile-dependency trap).

**AI:** inappropriate.

**Why not a spreadsheet:** it can be, and some firms do it. The value is the enforced monthly artifact with retained history and the specific exception rules an examiner looks for. Jurisdictional variance in requirements is the part a spreadsheet never encodes.

**Complexity:** small. **Learning difficulty:** low.

**Value:** licensing risk reduction, which is hard to price but existential; plus an hour or two monthly.

**Risks:** state requirements vary meaningfully; the tool must ship jurisdiction rule packs and be explicit that it does not constitute compliance certification. Bank and client-fund data is sensitive — local-only.

**Existing products/substitutes:** Rentec Direct, AppFolio, Buildium and Propertyware all have trust accounting; the gap is firms on QuickBooks or on commercial-only platforms without a trust module.

**Why still attractive:** narrowly scoped, legally motivated, and aimed at the specific firms whose software does not do it. Weakest differentiation of the nine, which the scoring reflects.

**Paid customization:** low-to-moderate — jurisdiction packs.

---

## 5. Opportunity ranking

Scored 1–5 on each of ten criteria. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of build | Narrow scope | Differentiation | Customization | Test data | Evidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| O1 | RecoveryLedger | 5 | 4 | 5 | 4 | 3 | 3 | 5 | 5 | 4 | 5 | **43** |
| O4 | EscalationRun | 4 | 4 | 5 | 5 | 5 | 5 | 4 | 3 | 5 | 4 | **44** |
| O3 | RecoverySetup Auditor | 5 | 3 | 5 | 5 | 4 | 4 | 5 | 5 | 4 | 4 | **44** |
| O2 | LeaseProfile | 4 | 4 | 4 | 5 | 3 | 4 | 4 | 5 | 4 | 5 | **42** |
| O6 | SalesLedger | 4 | 5 | 4 | 4 | 4 | 4 | 4 | 5 | 3 | 4 | **41** |
| O5 | OptionClock | 4 | 3 | 4 | 5 | 5 | 5 | 3 | 3 | 4 | 4 | **40** |
| O8 | ReconPacket | 3 | 3 | 4 | 5 | 4 | 5 | 3 | 3 | 4 | 4 | **38** |
| O7 | BillbackGate | 3 | 5 | 4 | 5 | 4 | 4 | 3 | 4 | 3 | 3 | **38** |
| O9 | TrustCheck | 4 | 5 | 3 | 5 | 5 | 5 | 2 | 2 | 3 | 4 | **38** |

### The top three

**O3 — RecoverySetup Auditor (44).** The highest-leverage concept per unit of build effort. It does not have to compute a correct reconciliation; it only has to notice that the billing configuration and the lease disagree. That is a comparison problem, which means it is buildable in weeks rather than months, and its output is a list of dollar-denominated findings — the easiest ROI conversation in this entire report. It also has a second market at acquisition due diligence, where a buyer wants exactly this report on a seller's rent roll. Its weakness is frequency: it is run a few times a year, not continuously.

**O4 — EscalationRun (44).** Ties on score with a very different profile: small, fast to build, immediately understandable, and attacking a failure mode (the silently missed CPI escalation) that is pure permanent revenue loss and compounds into asset valuation. The look-back mode — "here are escalations that should have happened and didn't" — is the feature that makes it a discovery tool rather than a calculator, and that is what earns the differentiation score. Its scope is genuinely narrow enough to finish. Realistic test data is trivially available (public CPI series plus synthetic lease terms).

**O1 — RecoveryLedger (43).** The most valuable and the most demanding. It attacks the largest documented problem in the market, and a deterministic, auditable, locally-run recovery engine with lease-cited traces has no free equivalent. It scores lower only on ease of build and narrowness — cap arithmetic, gross-up, base-year stops and multi-year carryforward are a lot of correctness surface, and the temptation to grow it into a platform is severe. It is the strongest *product* here but the riskiest first build.

### What to investigate next

**Start with O4 (EscalationRun).** It is small, it is finishable, it produces a dollar figure in the first session, and building it forces the creation of the lease-profile data model that O1, O3, O5 and O6 all depend on. It is the cheapest way to validate whether practitioners will maintain structured lease profiles at all — which is the assumption the entire suite rests on.

**Then O3 (RecoverySetup Auditor)**, which reuses that model and adds only a comparison layer, and is the natural door-opener at firms that will not buy a reconciliation engine until they believe they have a problem.

**O1 last**, funded by the credibility the first two build.

---

## 6. Validation plan

### Questions to ask practitioners

For property accountants and outsourced accounting shops:

- Walk me through your last reconciliation for one property. What did you open first?
- Where do the tenant-specific caps and exclusions actually live — in the workbook, in Yardi, or in your head?
- When was the last time you re-read a lease to check a recovery setup? What triggered it?
- How many tenants disputed last year's reconciliation? What did they ask for, and how long did it take to produce?
- Have you ever discovered an escalation that should have been billed and wasn't? How far back had it gone? Did you recover it?
- What happens when a lease is amended mid-year — who updates the recovery setup, and how do you know it happened?
- How do you determine which CPI series and base month to use? Where is that written down after the fact?
- What did you do the last time a tenant simply stopped sending sales reports?
- Which parts of Yardi/MRI/Buildium do you deliberately not use, and what did you replace them with?
- If I gave you a report saying "these 6 tenants are being billed on terms that don't match their leases," what would you do with it?

For controllers and owner principals:

- What is your exposure if a reconciliation is delivered after the lease deadline?
- Has an owner or a buyer's diligence team ever found a billing error you didn't know about?

### Who to interview

- Property accountants and lease administrators at regional firms (BOMA and IREM local chapters are the access route; IREM's ARM/CPM and BOMA's RPA credential holders are the exact population).
- Outsourced real-estate accounting providers — they will talk about hours-per-reconciliation openly because it is their unit economics.
- Tenant-side lease auditors. They are adversarial to the customer but they know the error taxonomy better than anyone and will describe it freely.
- Small owner-operators with 5–20 assets and no lease administrator. Most likely to adopt a free tool.
- Yardi/MRI implementation consultants, on what clients configure wrong.

### Search terms for further research

`CAM reconciliation workbook template`, `operating expense recovery setup Yardi`, `MRI recoveries module cap carryforward`, `base year stop calculation office lease`, `controllable CAM cap cumulative compounding`, `CPI escalation lease dispute index series`, `percentage rent breakpoint escalation amendment`, `commercial lease audit findings landlord`, `three-way reconciliation property management state`, `tenant billback markup management agreement`, `estoppel certificate turnaround property manager`, `BOMA operating expense study`, `IREM income expense analysis`, plus r/CommercialRealEstate, r/PropertyManagement, r/Accounting, BiggerPockets commercial forums, and the AppFolio/Yardi/Buildium user communities.

### Sample files and data needed

- 5–10 real commercial leases across office, retail and industrial, with amendments, redacted — the single most important asset. Public REIT filings contain lease exhibits; SEC EDGAR is a usable free source for realistic lease language.
- A real (anonymized) property GL export with a full year of expense detail.
- A completed reconciliation workbook from a practicing accountant, with the statement it produced.
- A rent roll and a PMS recovery-setup export.
- BLS CPI-U series for several metro areas (public).
- A retail center's sales reporting spreadsheet.

### Prototype that would validate the idea

Build **EscalationRun** against 20 synthetic-plus-real lease profiles covering fixed steps, fixed dollar, straight CPI, CPI with floor, CPI with floor and ceiling, and "greater of CPI or fixed." Run it in look-back mode over three prior years. Hand the output to two practicing property accountants and ask one question: *did we find anything you didn't know about?* A single confirmed missed escalation validates the entire suite's premise.

For **RecoverySetup Auditor**, the prototype is even cheaper: take one firm's rent roll and five leases, hand-build the profiles, and produce the mismatch report manually first. If a manual version finds nothing, the software version will not either.

### Assumptions most likely to make this fail

1. **That practitioners will author structured lease profiles.** This is the load-bearing assumption for six of the nine concepts. If entering a profile takes as long as doing the reconciliation by hand, nothing else matters. Mitigation: O2, and a profile format simple enough to fill from a lease abstract in ten minutes.
2. **That the errors are actually there.** The 40% figure comes from a vendor. If a competent firm's setups are basically right, O3's value collapses. The manual pilot above tests this cheaply.
3. **That local/desktop is a feature, not a defect.** I believe confidentiality favors local tools here, but the market may simply expect cloud and treat a local tool as dated.
4. **That firms will trust a free tool with a billing calculation.** They may run it as a check against their workbook forever and never adopt it as the source. That is still a viable product — but it is a *verification* product, not a *production* one, which changes the positioning of O1 substantially.
5. **That CSV export is available.** Yardi and MRI exports are usually obtainable but sometimes gated behind a module the client did not buy. If a firm cannot get a GL export, half these tools are dead on arrival at that firm.
6. **That leases are consistent enough to model.** Recovery structures vary more than any schema anticipates. The escape hatch — a free-text override with a manual amount — must exist from day one or the tool will be abandoned at the first weird lease.

---

## 7. Cross-industry patterns

**1. Per-counterparty rule set extracted from prose, executed as versioned code, with the source clause cited in the output.**
The defining pattern of this market. Each tenant's lease encodes a distinct calculation, the calculation is executed in a spreadsheet with no link to its source, and the resulting number must later be defended clause by clause. The generalization: wherever a contract governs an amount you bill, the contract terms should be structured data and the bill should carry its own citations.
*Transfers to:* Independent insurance agencies – commercial lines (policy terms driving premium allocation); Freight brokerage (accessorial charges per customer contract); Machine shop / job shop quoting (PO terms driving price adjustment); Marketing and creative agency account and production management (retainer and overage terms); Third-party claims administration (TPA) and self-insured program operations.

**2. Silent revenue leakage detector: compare what you are billing against what you are entitled to bill, and report the delta.**
Distinct from an error-checker because the failure produces no error message — the counterparty is happy, the ledger balances, and the loss compounds. The output is a dollar-denominated findings list, not a validation pass/fail.
*Transfers to:* Medical billing and revenue cycle for small practices (undercoding, unbilled encounters); Freight bill audit and payment for small shippers; Premium audit and payroll classification consulting; Bookkeeping and outsourced accounting firms; Small motor carriers (5–50 trucks) back office and settlement.

**3. Configuration-drift auditor between a source document and the system configured from it.**
Someone reads a document once and types its terms into a system; the document is later amended; nobody re-verifies. A comparison tool that recomputes the configuration from the document and reports mismatches is cheap to build and finds real money. This is meaningfully different from the ledger's existing "reconciling an artifact against the instructions that produced it" pattern because here both sides persist and drift apart over years.
*Transfers to:* HR and benefits administration in companies under 200 employees (plan documents vs. payroll deduction setup); Employee benefits brokerage and benefits administration; Nonprofit grant management and compliance (award terms vs. accounting setup); Staffing and recruiting agency operations (client rate agreements vs. billing rates); Managing general agents (MGAs), wholesale brokers, and program administrators.

**4. Published-index escalation calculator with documented vintage.**
A contract references an external published index; someone must select the right series, apply lag and rounding and floors and ceilings, and — critically — record which vintage of the index was used, because the index is revised and the dispute happens later. The recorded provenance is the deliverable, not the arithmetic.
*Transfers to:* General contractor preconstruction and estimating (material price escalation clauses); Freight brokerage (fuel surcharge indices); Right-of-way and easement acquisition consulting; Training organizations and continuing-education providers (multi-year contract escalators); Commercial property management.

**5. Counterparty reporting-obligation register with a non-reporting chase list.**
When the counterparty owes *you* a periodic report, the failure mode is silence. A register that tracks who owes what by when and generates the chase list turns an invisible omission into a visible queue.
*Transfers to:* Nonprofit grant management and compliance (subrecipient reports); Independent insurance agencies (loss runs and payroll reports for audits); Fiscal sponsorship organizations administering awards for sponsored projects; Workforce development boards and WIOA subrecipients; Supplier quality engineering at OEMs and primes.

**6. Scope-controlled disclosure packet: assemble supporting evidence for one counterparty without exposing another's.**
Assembling a backup binder is easy; assembling one that provably contains only what this counterparty is entitled to see is the hard and valuable part.
*Transfers to:* Small-firm litigation support and paralegal work; Independent property and casualty claims adjusting; Medical billing and revenue cycle for small practices; Third-party claims administration (TPA) and self-insured program operations.

---

## 8. Sources and confidence

### Verified findings (multiple independent sources, or primary documents)

- The commercial property back-office role combines AP coding, tenant billbacks, CAM reconciliation support, delinquency, budget assembly, COI/W-9/permit file maintenance and work-order coordination in a single position requiring 5 years' experience and MRI proficiency — [Property Administrator, Equitable Real Estate Partners, Henrico VA (Indeed, 2026-07-27)](https://to.indeed.com/aa7kdjq647yr); [Senior Lease Administrator, Turnberry, Aventura FL (Indeed, 2026-08-05)](https://to.indeed.com/aamv8v8x2bqg).
- The CAM reconciliation workflow — GL classification, gross-up, per-tenant lease application, true-up, backup package, deadline delivery, estimate reset — and its canonical error set (wrong pro-rata denominator, capital treated as operating, missed caps and exclusions, absent or wrong gross-up, late delivery): [Keystone Property Accounting](https://www.keystonepropertyaccounting.com/cam-reconciliation-property-managers-guide/); [G-Squared CFO](https://www.gsquaredcfo.com/blog/cam-reconciliation-accounting); [Harvest LLP (legal perspective)](https://harvestllp.com/articles/reconciliation-of-cam-expenses-a-guide-from-landlord-and-tenant-perspectives/).
- Gross-up mechanics: 90–95% occupancy thresholds, variable-only application, and expense misclassification as the most frequent error — [Baker Tilly](https://www.bakertilly.com/insights/start-with-the-lease-agreement).
- Reconciliation delivery deadlines cluster at 60–180 days after year end, with 90–120 days the practical norm, and tenant audit rights are lease-defined with statute-of-limitations limits on look-back — [Keystone](https://www.keystonepropertyaccounting.com/cam-reconciliation-property-managers-guide/); [Harvest LLP](https://harvestllp.com/articles/reconciliation-of-cam-expenses-a-guide-from-landlord-and-tenant-perspectives/).
- Percentage rent operations: monthly/quarterly certifications, 60–90 day annual reconciliation, 2–3 year audit look-back, 2–5% material-underpayment cost-shifting thresholds, breakpoints that must escalate in parallel with base rent, occupancy-cost ratios of 12–15% signalling distress, and unresolved e-commerce/BOPIS inclusion disputes — [Bryckel](https://www.bryckel.ai/resources/percentage-rent-gross-sales-reporting).
- Yardi Voyager user complaints: two-month onboarding, navigation difficulty, report accuracy and blank-report issues, crashes and month-end slowness, and à-la-carte module pricing that "nickel and dimes you for every function," with implementation cost potentially equal to license cost — [Capterra verified reviews](https://www.capterra.com/p/33832/Yardi-Voyager/reviews/).
- Tooling tiers by portfolio size (QuickBooks+Excel → Buildium/AppFolio → Yardi/MRI) — [Keystone](https://www.keystonepropertyaccounting.com/cam-reconciliation-property-managers-guide/).
- Trust-account and record-keeping obligations for licensed managers are state-specific and include three-way reconciliation in several jurisdictions — [Arizona A.R.S. §32-2175](https://www.azleg.gov/ars/32/02175.htm); [Colorado Division of Real Estate three-way reconciliation guidance](https://content.govdelivery.com/accounts/CODORA/bulletins/26401da); [Colorado DRE broker financial audit process](https://dre.colorado.gov/division-programs/real-estate-broker/broker-practice-guidance/broker-financial-audit-process).
- Property tax appeal deadlines vary by state and by county within states — [Texas Comptroller](https://comptroller.texas.gov/taxes/property-tax/protests/); [Texas county-by-county deadlines](https://www.propertytaxes.law/property-tax-appeal-deadlines-in-texas-by-county/).
- Critical-date categories and the notice-window problem — [Lextract critical dates guide](https://lextract.io/resources/articles/critical-dates-tracking-guide); [Occupier](https://www.occupier.com/blog/critical-date-management); [LeaseCommand](https://leasecommand.com/critical-date-tracking-for-lease-portfolios/).
- Billback tracking metrics (expected recovery, disputes, days-to-collect, error count) as the industry's own framing of what goes wrong — [Building Engines](https://www.buildingengines.com/blog/how-to-track-work-orders-billbacks/).

### Strong inferences (single source, or vendor-supplied figures that are directionally corroborated)

- **40% of CAM reconciliations contain material errors** (attributed to Tango Analytics 2023); **28% of tenants find discrepancies independently** (attributed to JLL 2023); professional audits recover **15–20% of billed charges**; industry leakage **$5–15B/yr**, **$100k–400k per property**; **$12.88 average cost per AP invoice vs. $2.78 best-in-class**; **9.2 vs. 3.1 day cycle times**; **60–90 day reconciliation completion vs. 30–45 for leaders** — all via [PredictAP](https://blog.predictap.com/cam-reconciliations-the-15-billion-problem-hiding-in-plain-sight). These come from parties selling solutions to the problem. The existence of a contingency-fee lease-audit industry, tenant-side audit tooling ([CAMAudit](https://www.camaudit.io/resources/cam-audits/commercial-lease-audit-guide)), and outsourced reconciliation services ([Springbord](https://www.springbord.com/blog/what-a-cam-recovery-audit-reviews-and-why-most-cam-overcharges-go-undetected/), [RE BackOffice](https://www.rebolease.com/cam-reconciliation-services-faq)) independently corroborates that the error rate is materially above zero, but the specific percentages should be re-derived before being used in any pitch.
- Missed CPI escalations are common and rarely recovered. The mechanics of the problem are well documented ([Norris McLaughlin on CPI in commercial leases](https://norrismclaughlin.com/articles/client-alert-commercial-leases-cpi-revisited/); [Stratafolio](https://stratafolio.com/blog/what-are-lease-rate-escalations/)); the *frequency* of the miss is inferred from the pattern of tooling built to address it and is not directly measured.
- Submetered utility rebilling produces recurring allocation errors — [Genea](https://www.getgenea.com/blog/the-4-most-common-submeter-billing-mistakes/); [Conservice](https://www.conservice.com/blog/the-noi-drain-you-cant-see-how-utility-billing-errors-quietly-undermine-portfolio-performance/). Vendor sources; treat magnitude with caution.
- Lease abstraction cost and turnaround (low-tens of dollars offshore to a few hundred domestic, days of turnaround) — inferred from the pricing pages of [Lextract](https://lextract.io/resources/articles/how-much-does-lease-abstraction-cost) and [CapVeri](https://www.capveri.com/blog/lease-abstraction-services-guide) and the volume of firms offering the service. Not independently verified.

### Tentative hypotheses requiring practitioner validation

- That small commercial managers will maintain a structured lease-profile file rather than reverting to their existing workbook. **This is the assumption the whole suite rests on and it is unvalidated.**
- That local-only operation is perceived as a confidentiality advantage rather than as a limitation. Plausible given tenant sales data and lease confidentiality clauses, but untested.
- That GL and rent-roll CSV exports are reliably obtainable from Yardi Breeze, Voyager, MRI and Buildium in the tiers small firms actually buy.
- That the missed-escalation look-back finds something at a typical, competently run firm. If it does not, O4's differentiation collapses to "a calculator."
- That billback capture rates are materially below 100% at small firms. Widely implied by vendor marketing; no independent measurement located.
- That firms would accept an AI-assisted lease extractor for confidential lease documents at all. Some owners' policies may forbid it outright, in which case O2 must ship a local-model option or be dropped.

### Note on evidence gaps

Direct practitioner voice — forum threads, Reddit discussions, conference Q&A — proved difficult to surface for this market through available search. Almost every high-ranking source is a vendor or a service provider with a commercial interest in the problem being severe. The two Indeed job descriptions are the most trustworthy artifacts in this report precisely because they were written to hire someone, not to sell something, and they corroborate the workflow description in detail. **Before building anything here, talk to three property accountants.** The problem shape is well established; the magnitude is not.

---

*Cycle `3dee0a20` — Commercial property management / back-office — 2026-08-06.*
