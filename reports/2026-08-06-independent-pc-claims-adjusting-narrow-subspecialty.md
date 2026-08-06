# Market Research Cycle — Independent P&C Claims Adjusting

## Narrow subspecialty: the 1099 field property adjuster writing Xactimate estimates on carrier fee schedules

---

## 0. Cycle header

| | |
|---|---|
| **Market** | Independent property and casualty claims adjusting |
| **Angle** | narrow-subspecialty |
| **Named subspecialty** | Independent (1099) **field property** adjusters — daily-territory and catastrophe (CAT) deployment — who personally scope losses, write their own Xactimate estimates, and are paid per claim on an IA-firm fee schedule |
| **Claim ID** | `1c0329d5` |
| **Date** | 2026-08-06 |
| **Report** | `reports/2026-08-06-independent-pc-claims-adjusting-narrow-subspecialty.md` |
| **Backlog remaining after this claim** | 230 assignments |

### Why this assignment over the others available

The ledger held 231 open assignments across 113 markets at the start of this cycle. Selection followed the stated priority order:

1. **Zero completed coverage.** "Independent property and casualty claims adjusting" had no completed entries. Insurance appears once in the catalog so far — *Independent insurance agencies, commercial lines / back-office* (2026-08-03) — and that is the **distribution** side of insurance. Claims adjusting is a structurally different business with different software, different economics, and a different buyer. Choosing it adds a genuinely new vertical rather than deepening one.
2. **Strong expected practitioner evidence.** Adjusting has an unusually visible practitioner culture: a 25-year-old dedicated forum (CatAdjuster.org), several full-time training businesses that publish operational detail (IA Path, AdjusterPro, Adjuster Authority, Actionable/AdjustingExpectations), a first-person practitioner Substack, and — most usefully — a dense field of small commercial tools whose marketing copy *quotes the exact friction their buyers report*. That last category is strong triangulating evidence: nobody builds a $149/month product to solve an imaginary problem.
3. **Angle diversity.** The catalog was skewed toward `core-practitioner-workflow` (5 of 12 completed) with only 2 `narrow-subspecialty` reports. Taking the narrow-subspecialty angle rebalances the mix and forces a tighter, more actionable scope than a whole-market survey.
4. **The buyer is an individual, not a committee.** The 1099 IA buys their own tools with their own money and can adopt something the same afternoon. For a free-open-source-base / paid-customization catalog, that is a materially better adoption profile than software that needs an enterprise procurement cycle.

**Scope discipline for the narrow-subspecialty angle.** This report deliberately stays inside one niche and excludes: auto/casualty/liability IAs, desk and "inside" adjusters who never leave the office, staff (carrier-employed) adjusters, public adjusters (policyholder-side, a different and adversarial role), and TPA/IA-firm management. Where those adjacent roles matter, they are named as backlog candidates, not covered here.

**A methodological caveat stated up front.** Reddit was unreachable from this research environment (proxy 403 on all `reddit.com` paths), so r/adjusters, r/Xactimate, r/CatAdjuster and r/InsuranceClaims produced **zero** directly quoted evidence in this cycle. That is the single largest hole in this report. Everything below is sourced from accessible forums, trade press, vendor documentation, regulatory primary sources, and product evidence. Confidence flags in Section 8 reflect this honestly, and Section 6 makes "recover the Reddit corpus" the first validation step.

---

## 1. Market examined

**Industry.** Property and casualty insurance claims handling, outsourced field segment.

**The professional.** A licensed independent adjuster ("IA") working as a **1099 independent contractor**, retained not by the carrier directly but by an independent adjusting firm (Crawford & Company, Sedgwick, Eberl, Pilot Catastrophe Services, ProNet Group, Alacrity, and dozens of smaller regional firms) that holds the carrier contract and subcontracts the field work. The IA is explicit about this status: a practitioner writing publicly states, "We file a 1099 each year and have never worked directly for any insurance carrier or been considered a 'staff adjuster'" ([Catastrophe Adjusting](https://catastropheadjusting.substack.com/p/we-lived-paycheck-to-paycheck)).

**Two operating modes inside the subspecialty:**

- **Daily-claim adjuster.** Works a defined territory, typically within a ~50-mile radius, carrying **20–30 active claims** at a time over weeks-to-months cycles. Year-round, lower intensity, steadier income.
- **CAT (catastrophe) adjuster.** Deploys within 24–48 hours of a named event, works roughly 12-hour days seven days a week, and may process **100–200 claims in a single deployment**, with days rather than weeks per file ([BSA Claims](https://www.bsaclaims.com/difference-between-cat-daily-claims-adjusters/)). One practitioner account describes receiving a "batch of claims" of **20–50 files at a time** with a 24-hour first-contact obligation on each ([Catastrophe Adjusting](https://catastropheadjusting.substack.com/p/we-lived-paycheck-to-paycheck)).

Most working IAs do both, and many hold rosters with **several IA firms simultaneously** so they can chase work across events — which is the origin of several problems below.

**Organization size.** This is the defining structural feature of the market: **the economic unit is one person.** The IA is a sole proprietor or single-member LLC with no IT department, no procurement process, and no software budget line. Their "organization" is a laptop, a phone, a ladder, a truck, a Xactimate license, and an E&O policy. The IA firms above them range from ~20 staff to several thousand, but the firm does not buy tools for the field adjuster — the adjuster buys their own.

**Licensing scale.** 33 states license independent adjusters (40 license public adjusters; 15 license staff adjusters) per the [NAIC State Licensing Handbook, Ch. 18](https://content.naic.org/sites/default/files/inline-files/Chapter%2018%20-%20Adjuster%20Licensing.pdf). Reciprocity is real but inconsistent — New York grants reciprocity to no non-residents; Texas reciprocates with most states except NY, CA and HI ([ResourcePro](https://www.resourcepro.com/blog/adjuster-licensing-reciprocity-and-the-designated-home-state/)). A CAT adjuster who wants to chase storms nationally therefore accumulates a substantial portfolio of non-resident licenses off a Designated Home State, each with its own renewal date and CE obligation.

**Type of user.** Practical, field-based, moderately technical. They already operate Xactimate (an unforgiving professional tool), a sketching workflow, a camera, sometimes a drone under FAA Part 107. IA Path's advice to new adjusters that "Windows proficiency is essential, not Apple" ([IA Path](https://iapath.com/the-good-bad-ugly-adjuster/)) is a useful signal for anyone building for them: **Windows desktop, offline-capable, and file-based is the native environment.** They are not going to install Docker.

---

## 2. How the work is performed

### 2.1 Assignment

Work arrives through **XactAnalysis** (Verisk), the dominant carrier↔IA-firm↔field routing hub, via the XactAnalysis SP service-provider interface ([Verisk](https://www.verisk.com/products/xactanalysis-sp/)). Dispatchers at the IA firm work an **Assignment Queue**, filtering by type of loss, assignment type, policy type and map location, then pushing files to individual XactNet addresses — a substantially **manual, dispatcher-driven** routing step ([XactAnalysis Help — Assignment Queue](https://xactanalysis.helpdocs.io/l/enUS/article/bu084m7ah3-updated-assignment-queue)).

The assignment packet the adjuster opens contains: insured and claim identifiers, a CLIENT/POLICY tab with coverages, a DETAILS tab tracking customer-contact date / site-inspection date / job-completion date and approval statuses, a MAP tab, DOCUMENTS, PHOTOS/VIDEOS/SKETCHES, NOTES, dated ACTION ITEMS, PREVIOUS LOSS history, and an EXTERNAL DATA tab carrying third-party reports and ClaimSearch results ([XactAnalysis Help — Assignment Detail](https://xactanalysis.helpdocs.io/l/enUS/article/kb5nfomssh-assignment-detail-en-us)).

Some carriers run **Symbility / Cotality Mobile Claims** instead — Crawford trains CAT adjusters on it in a dedicated two-day course covering claim setup, coverages, deductibles, and floor/roof/elevation plan creation ([Crawford](https://www.crawco.com/cat/training/symbility-training)). Others layer **ClaimXperience** for policyholder video collaboration and virtual inspection ([Verisk](https://www.verisk.com/products/claimxperience/)). On top of all of this, each IA firm runs its own roster/deployment portal. **A working IA is therefore logged into three to eight different systems, with different credentials and different rules, in any given week.**

### 2.2 The clock starts

Statutory floors vary by state — California requires acknowledgment within 15 calendar days and a coverage decision within 40 days of proof of claim; Texas requires an accept/reject decision within 15 business days and payment within 5 business days of written acceptance, with an 18%/year penalty plus attorney fees for lateness ([National Adjuster Authority](https://nationaladjusterauthority.com/claims-handling-standards-and-regulations/)).

Layered on top are **contractual** carrier/IA-firm SLAs, which are tighter and are not published. The consistent pattern across sources is 24–48 hour first contact, inspection within days, estimate uploaded within days of inspection. Compliance is measured continuously: the XactAnalysis Performance Scorecard tracks "cycle times, customer satisfaction, and estimate quality" so carriers can "determine if teams are meeting company standards" ([Verisk](https://www.verisk.com/products/xactanalysis/)). Falling off the scorecard means fewer assignments next event — an existential outcome for a 1099 contractor.

### 2.3 Field inspection

Increasingly, measurement happens *before* arrival. **EagleView** supplies a 3D roof model with five-angle photos, facet-length and pitch diagrams, facet labels and area calculations, feeding directly into Xactimate wireframes ([EagleView](https://www.eagleview.com/product/measurement-reports-for-claims-adjusting/)). **Hover** does comparable photogrammetry. Drone capture is now formalized inside IA firms: Eberl requires FAA Part 107 certification, uses a proprietary flight app, captures 4K imagery, runs "AI-assisted image analysis reviewed by licensed adjusters," and pushes results into XactAnalysis or Cotality so the adjuster can measure damage from the desktop ([Eberl](https://eberls.com/drone-roof-inspection-what-adjusters-need-to-know/)).

On site the adjuster scopes room by room, takes moisture readings on water losses, builds a sketch (carriers commonly expect accuracy within two inches — [Docusketch](https://www.docusketch.com/post/how-to-write-an-xactimate-estimate)), and photographs everything. Volume is high and rising: a contractor-side estimator advises that "a three room water loss should have at least 50 photos" ([Claims Delegates](https://www.claimsdelegates.com/how-not-to-take-pictures-for-xactimate-scopes/)), and photo-organizing vendors describe a normal file as "100+ pictures" ([myAdjustiMate](https://myadjustimate.com/)). A CAT roof-and-interior claim routinely runs several hundred.

### 2.4 Estimate writing

The estimate is built on a **regional price list** identified by state/region/version/month/year — e.g. `OHCO8X_APR24` for Columbus, Ohio, April 2024 pricing. Line items carry category (Cat) and selector (Sel) codes — WTR for water, RFG for roofing — which experienced adjusters key directly instead of searching, and **macros** batch common scopes. Valuation logic runs RCV → depreciation → ACV, with O&P typically applied when three or more trades must be coordinated ([Docusketch, read](https://www.docusketch.com/post/how-to-read-an-xactimate-estimate) / [write](https://www.docusketch.com/post/how-to-write-an-xactimate-estimate)).

Xactimate exposes roughly **50,000 line items** ([AdjusterPro](https://adjusterpro.com/adjusterproqa/)). The estimate is where professional judgment concentrates and where most rework originates.

### 2.5 The claim file package

Beyond the estimate, the adjuster produces a **captioned narrative report**. Claims-law authority Barry Zalma is blunt about its role: it must be written "immediately after the adjuster's first meeting with the insured on every file, no matter how small," and must "explain to the adjuster's supervisor all the adjuster knows about the loss so that decisions required of them by the insurer and the law can be made" ([Zalma](https://barryzalma.substack.com/p/a-video-explaining-why-insurers-require)). A **statement of loss** is a three-column reconciliation of insurance available, loss by category, and claim amount after deductible, depreciation, sublimits and coinsurance ([Zalma](https://barryzalma.substack.com/p/how-an-insurer-resolves-a-claim-part-94d)).

Also in the package, depending on the loss: coverage analysis with endorsement and exclusion flags, subrogation referral, **ITEL** material-match/repairability lab reports ([Nearmap itel NOW](https://www.nearmap.com/products/itel-now)), mortgagee/loss-payee identification, and — on contents losses — a **personal property inventory**. Florida's Citizens inventory form shows how granular that is: per item, the form demands item number, quantity, description, owner, make, purchase date with receipt Y/N, original price, place of purchase, model number, sales tax percentage, clean/repair/replace disposition, and cost to remediate, with receipts attached and a fraud-statute signature ([Citizens PPI form, PDF](https://www.citizensfla.com/documents/20702/54161/personal-property-inventory-form.pdf/3e8054dc-fc27-4990-930c-f8846c6e4b52)).

### 2.6 Upload, QA, and the kickback loop

The file transmits back through XactAnalysis, which auto-generates a Report Rough Draft, a **Variation Report** and an **Estimate Audit Report** for the reviewer. Carrier-side QA runs through **XactAnalysis QR** ([Verisk](https://www.verisk.com/products/xactanalysis-qr/)) plus human desk examiners applying carrier-specific guidelines.

Files that fail get returned. **"Kickback" is the practitioner's own word for it** — AdjusterPro sells a QA product explicitly to adjusters "tired of kickbacks," on the logic that "less claims kicked back... means... more money you make" because pay is per closed claim ([AdjusterPro](https://adjusterpro.com/adjusterproqa/)). Supplements — additional scope discovered during repair — reopen files later and start a second round of the same loop.

### 2.7 Getting paid

The IA firm bills the carrier off a **fee schedule** keyed to the *final settled claim amount*, then splits it with the field adjuster, typically **55–70%** to the adjuster ([AdjusterPro](https://adjusterpro.com/fee-schedules/), [IA Path](https://iapath.com/independent-adjuster-fee-schedule/)). A rare publicly posted example — the [TWIA/TFPA 2019 Claims RFQ Adjuster Fee Schedule (PDF)](https://www.twia.org/wp-content/uploads/2019-Claims-RFQ_Adjuster-Fee-Schedule.pdf) — shows the tiering:

| Final claim amount | Residential fee | Commercial fee |
|---|---|---|
| No inspection / erroneous assignment | $100 | $100 |
| $0 – $2,500 | $400 | $500 |
| $2,501 – $5,000 | $500 | $600 |
| $5,001 – $10,000 | $700 | $800 |
| $10,001 – $15,000 | $900 | $1,000 |
| $15,001 – $25,000 | $1,100 | $1,300 |
| $25,001 – $50,000 | $1,500 | $1,700 |
| $50,001 – $75,000 | $1,800 | $2,000 |
| Above $75,001 | Time & Expense | Time & Expense |

with T&E hourly rates of $75 residential adjuster / $90 commercial / $125 general adjuster / $155 executive general adjuster.

Two consequences fall directly out of this structure and drive most of Section 3:

- **The fee is a step function of a number that keeps moving.** A supplement of a few hundred dollars can cross a breakpoint and change the fee by $200. The adjuster's revenue per file is therefore not knowable at the time the work is done.
- **Payment is slow, partial, and reversible.** IA Path states plainly that "it takes 2 weeks to 3 months for an adjuster to get paid on a property claim," and that some firms will not pay until the carrier pays them ([IA Path](https://iapath.com/independent-adjuster-fee-schedule/)). AdjusterPro describes roughly 80% paid up front with **20% held back** pending carrier review, plus audits where "money [is] questioned or pulled back" ([AdjusterPro](https://adjusterpro.com/blog-how-fast-do-insurance-adjusters-get-paid/)). Income is violently seasonal — one practitioner account: "$80,000 hit your checking account... but that money needed to last till the following May," which the same author calls "the largest deterrent from adjusters staying in the industry" ([Catastrophe Adjusting](https://catastropheadjusting.substack.com/p/we-lived-paycheck-to-paycheck)).

---

## 3. Most important problems, ranked

### P1 — Estimate and file rejection ("kickbacks") caused by carrier-specific guideline variance

**Who.** Every field IA, worst for adjusters newly rostered with a carrier they have not worked before.

**When.** At submission and for days afterward, every claim.

**How handled now.** Memory, personal notes, a carrier "cheat sheet" in Word or OneNote, asking a peer, or paying for carrier-specific certification training. Crawford runs formal "Carrier-Specific Certification," "Carrier Auto Certification," and a "Multiple Carrier Track" academy ([Crawford](https://www.crawco.com/cat/training/carrier-specific-certification-2022-04-13)) — the existence of paid, repeatable, per-carrier certification tracks is itself proof the requirements diverge materially.

**Why inadequate.** R&R Magazine's estimating guidance says the quiet part out loud: guideline variation is so extensive that "it is impossible to remember all of them unless you... specialize," advises estimators to "pay attention to what you are getting rejected for," and warns that labor (LAB) line items are "guaranteed to be questioned" ([R&R Magazine](https://www.randrmagonline.com/articles/88186-the-10-commandments-of-xactimate-estimating-success)). The failure list is stable and knowable: overlooked or mis-typed depreciation (recoverable vs. non-recoverable), duplicate labor, omitted damaged items, weak narratives, building-vs-contents misclassification — and the trainer's own conclusion is "**always QC your own file before turning it in**" ([AdjustingExpectations](https://www.adjustingexpectations.com/adjuster-blog/the-most-common-estimating-mistakes)). That instruction exists precisely because no tool does it for them at the point of submission.

**Frequency and cost.** Rework on a meaningful share of files. Each kickback costs re-opening the estimate, re-reasoning the scope, sometimes a re-inspection, and — critically — it delays claim closure, which delays the fee. On a per-claim fee model, an hour of rework is an hour that generates zero revenue.

**Evidence strength.** **Strongest in this report.** An entire product category exists to address it (AdjusterProQA at $149/mo — [AdjusterPro](https://adjusterpro.com/adjusterproqa/)), plus trade press, plus trainer content, plus paid carrier-specific certification programs.

---

### P2 — Fee reconciliation: proving you were actually paid what you earned

**Who.** Every 1099 IA, acutely those rostered with three or more firms.

**When.** Every pay cycle (commonly biweekly), and again at year end.

**How handled now.** A hand-built spreadsheet, if anything. Searches for adjuster-specific fee-tracking templates return essentially nothing purpose-built — results are generic ClickUp/Smartsheet KPI templates and Etsy mileage logs aimed at realtors. Dragonfile, the newest entrant serving solo adjusters, explicitly pitches itself as the replacement for spreadsheet-based claim tracking ([Dragonfile](https://dragonfile.io/2026/03/how-to-transition-from-spreadsheets-to-automated-claims-tracking/)), which is a vendor admitting the incumbent is Excel.

**Why inadequate.** The adjuster must independently reproduce a calculation the payer controls, across a moving input:

1. Fee tier depends on **final** claim amount, which changes with supplements and reopenings.
2. Each firm has a different schedule and a different split.
3. ~20% is held back and released later, so a payment statement never matches the claims closed in that period.
4. Chargebacks and audit reversals claw money back after the fact.
5. Nothing reconciles across firms.

Adjusters demonstrably do not trust this. A CatAdjuster.org thread exists for the sole purpose of comparing fee schedules across carriers and vendor firms, with participants reporting a peer earning "at least twice" as much on the same carrier through a different vendor in fewer weeks, and treating timely payment as a material term of employment ([CatAdjuster.org](https://catadjuster.org/Forums/tabid/60/aft/11318/Default.aspx)). A separate thread on the history of the fee schedule tracks hourly-equivalent T&E rates rising only ~$65 → ~$105 over 34 years — real compensation erosion that raises the stakes on every disputed file ([CatAdjuster.org](https://catadjuster.org/Forums/tabid/60/aft/9067/Default.aspx)).

**Cost.** Direct dollars. A single mis-tiered claim is $200–$400. An entirely missed claim on a settlement statement is the full fee. Across a 150-claim deployment, a 2% error rate is real money, and today the adjuster has no practical way to detect it.

**Evidence strength.** Verified that the structure creates the exposure and that adjusters actively compare notes because they distrust the numbers. **Not** verified with a documented case of a specific underpayment — no adjuster-facing reconciliation product exists to point at, which is simultaneously the gap and the reason direct evidence is thin.

---

### P3 — Photo volume, labeling, and completeness

**Who.** Every field IA.

**When.** After every inspection, before every submission.

**How handled now.** Manually: transfer from phone to laptop, sort, rename, caption, order, insert into a photo report.

**Why inadequate.** myAdjustiMate quantifies the baseline it displaced — labeling and sorting a "100+ picture" report takes **40 to 50 minutes**, which it claims to cut under 10 ([myAdjustiMate](https://myadjustimate.com/)). The downstream cost of doing it badly is a rejection: "uploading large batches of unlabeled images forces the adjuster to sort and interpret each one manually," close-ups without location reference "create uncertainty," and missing context causes carriers to bounce claims back, stalling payment ([CompanyCam](https://companycam.com/blog/3-costly-mistakes-when-submitting-photos-to-insurance-carriers)).

**Frequency.** Daily, several times daily on CAT deployment.

**Cost.** ~45 minutes per claim of pure clerical work. On a 100-claim deployment that is roughly **75 hours** — nearly a full extra work-week per event.

**Evidence strength.** Verified, and heavily contested commercially. Verisk itself now ships "Automatic Photo Labeling" in XactAI ([Verisk](https://www.verisk.com/company/newsroom/verisk-introduces-new-ai-tools-to-streamline-the-property-claims-experience/)), and ClaimMate, PHOTO iD, CaptionBuilder, FieldScribe AI ($199/mo) and CompanyCam all fish this pond. **The pain is real; the labeling half of it is crowded.** The *completeness-check* half is not.

---

### P4 — Contact, cycle-time, and documentation compliance

**Who.** Every IA; the consequences land on the carrier but the scorecard lands on the adjuster.

**When.** Continuously, from assignment to close.

**How handled now.** Claim notes typed into whichever portal the carrier uses, plus memory, plus a personal aging list.

**Why inadequate.** A file can be "operationally adequate while remaining non-compliant if it omits required elements — such as... **the date of each contact attempt**," and denial files with incomplete rationale "are among the most commonly cited deficiencies" in state market-conduct exams ([Adjuster Authority](https://adjusterauthority.com/adjuster-report-writing-standards/)). This is not theoretical: a Wolters Kluwer analysis found **270 P&C claims-related enforcement actions in 2019 totaling $4.7 million in fines**, with the top categories being failure to acknowledge/investigate/pay within required timeframes and documentation deficiencies — summarized by a compliance expert as "a lot of it goes back to documentation that proves what they've done, when they've done it and how they've done it" ([Claims Journal](https://www.claimsjournal.com/news/national/2020/10/05/299731.htm)).

**Cost.** Scorecard damage → fewer assignments. Statutory interest penalties (Texas: 18%/yr plus attorney fees). E&O exposure, since "failure to conduct a thorough investigation" and "failure to deliver services" are named leading triggers of claims against adjusters ([Schneider Insurance](https://schneider-insurance.com/errors-omissions-adjusters-guide/)).

**Evidence strength.** Verified on obligation and consequence; the mechanics of how individual adjusters track attempts today is a strong inference, not a quoted practice.

---

### P5 — Deployment economics: expenses, mileage, per diem, and whether the storm was worth it

**Who.** CAT adjusters specifically.

**When.** Throughout deployment; painfully in April.

**How handled now.** Shoebox of receipts, a generic mileage app, a spreadsheet, or nothing until the CPA asks.

**Why inadequate.** The IRS wants a reasonably contemporaneous log with date, mileage, destination and business purpose, plus year-start and year-end odometer readings; the 2026 business standard mileage rate is **72.5 cents/mile** ([IRS](https://www.irs.gov/newsroom/irs-sets-2026-business-standard-mileage-rate-at-725-cents-per-mile-up-25-cents), [DriversNote](https://www.driversnote.com/irs-mileage-guide/self-employed-deductions)). There is a rule here that catches self-employed adjusters constantly: **a self-employed person may use the federal M&IE per diem for meals but may NOT use the federal per diem for lodging — lodging must be actual cost with receipts** ([TaxAudit](https://www.taxaudit.com/tax-audit-blog/2025/can-self-employed-claim-per-diem-deductions)). Searches turned up **no adjuster-specific tax guidance product at all** — only generic Schedule C content-farm articles.

**Cost.** Lost deductions, audit exposure, and — the strategic version — no ability to answer "did that deployment actually make money after 3 weeks of hotel, fuel and rental?" before deciding whether to accept the next one.

**Evidence strength.** Rules verified from primary IRS/NAIC-grade sources. The behavior (adjusters improvising) is a strong inference from the total absence of purpose-built tooling.

---

### P6 — Multi-state license and CE renewal exposure

**Who.** Any IA holding non-resident licenses; severe for national CAT chasers.

**When.** Rolling, per state, biennially.

**How handled now.** Manually. ResourcePro characterizes the current state as "fragmented spreadsheets and reactive renewals," warning that manual tracking creates "a dual threat: regulatory fines for non-compliance and severe deployment delays" ([ResourcePro](https://www.resourcepro.com/blogs/claims-adjuster-licensing-compliance-playbook)). (Vendor content selling a compliance product — weight accordingly, but the structural claim is independently supported.)

**Why inadequate and what it costs.** Texas: biennial expiry on birth month, $50 renewal, $100 with late fee inside a 90-day grace period during which **the license is invalid and you cannot legally adjust**; past 90 days you redo the 40-hour pre-licensing course, background check, and $250–500 in fees — **and reciprocal non-resident licenses built off that home state can be automatically invalidated** ([Texas License Path](https://texaslicensepath.com/texas-adjuster-license-renewal/)). That is a cascading single point of failure. Other penalties cited: Delaware $200 CE penalty, Florida up to $10,000 for unlicensed adjusting, Maryland $5,000 per violation ([ResourcePro](https://www.resourcepro.com/blogs/claims-adjuster-licensing-compliance-playbook)). CE baseline is the NAIC-recommended 24 hours per 2 years including 3 ethics hours — Texas's actual requirement.

The related deployment question — *may I legally work this storm?* — has four possible answers per state: full license, temporary/emergency license, simple registration, or no requirement, activated by a governor's or commissioner's declaration, usually free or under $75, NAIC-recommended 90-day maximum though many states run 120–180 days. Emergency provisions cover **non-residents only** ([ResourcePro](https://www.resourcepro.com/blog/help-in-a-crisis-emergency-adjuster-licensing/)).

**Evidence strength.** Verified from NAIC primary documents and state sources. Note that **AdjusterTrack already sells exactly this** at $19–$99/month ([AdjusterTrack](https://www.adjustertrack.com/)) — so the problem is real but the space is occupied.

---

### P7 — Contents / personal property inventories

**Who.** IAs on contents-inclusive losses (fire, water, theft).

**When.** Whenever contents are in play.

**How handled now.** Carrier-supplied Excel or PDF forms, hand-typed, often transcribed from the insured's handwritten list.

**Why inadequate.** The Citizens form's 13 fields per item, multiplied by a household's worth of contents, is pure transcription with per-item depreciation judgment layered on. Data arrives as photos of handwritten lists, receipts, and verbal descriptions.

**Evidence strength.** Form requirements verified ([Citizens PPI form](https://www.citizensfla.com/documents/20702/54161/personal-property-inventory-form.pdf/3e8054dc-fc27-4990-930c-f8846c6e4b52)); the labor burden is a strong inference from the form's structure.

---

### P8 — Drive time and daily sequencing on deployment

**Who.** CAT adjusters running many inspections per day.

**How handled now.** Generic route planners (Zeo, Circuit, Badger Maps), or the adjuster's own judgment and Google Maps.

**Why inadequate.** A route-optimization vendor claims field adjusters spend "nearly 40% of their workday driving," 3–4 hours daily, and describes the characteristic failure — ten scheduled inspections, one emergency insert, and "adding this emergency stop creates chaos," with adjusters "zigzag[ging] across territories" and late responses triggering penalties ([Zeo](https://zeorouteplanner.com/how-to-optimize-adjuster-routes-cut-drive-time-by-30/)). That is vendor marketing and the 40% figure should be treated skeptically, but the underlying scenario matches how CAT deployment works.

**Evidence strength.** Weakest of the eight. Vendor-sourced, no practitioner corroboration in this pass. Ranked last deliberately.

---

### What is *not* a problem worth solving

- **Estimating itself.** Xactimate is entrenched, carrier-mandated, and not displaceable. Anything that tries to replace it is dead on arrival.
- **Aerial measurement.** EagleView, Hover and Nearmap own this and it requires imagery capital.
- **Generic photo capture apps.** Six vendors including Verisk are already there.

---

## 4. Application opportunities

Ten concepts. Each is scoped to be buildable by one developer, learnable in under an hour, and useful on day one — with a free open-source base and an obvious paid-customization path (usually: "encode *your* firm's or *your* carrier's rules").

A design constraint applies to all ten: **claim data is PII.** Names, addresses, policy numbers, loss detail, sometimes SSNs on contents inventories. 28 states/jurisdictions had adopted the NAIC Insurance Data Security Model Law as of August 2025, obliging licensees to maintain written information security programs and to oversee third-party service providers ([NAIC brief, PDF](https://content.naic.org/sites/default/files/government-affairs-brief-data-security-model-law.pdf)). Carriers push that obligation onto IAs through contract addenda. **Every concept below should therefore default to local-only, offline, no-cloud-account operation** — which happens to be both the cheapest architecture and the strongest sales point.

---

### A. **Preflight** — carrier-specific estimate and file QA checklist runner

- **User.** Field IA, immediately before uploading a file.
- **Problem.** P1. Kickbacks caused by carrier guideline variance nobody can memorize.
- **Current workflow.** Write estimate → upload → wait days → get returned with a reviewer comment → re-open, fix, resubmit → fee delayed.
- **Proposed workflow.** Export the Xactimate estimate PDF → drop it on Preflight with the carrier selected → get a pass/warn/fail checklist in 30 seconds → fix before upload.
- **Inputs.** Estimate PDF (and/or a CSV line-item export), claim metadata (carrier, date of loss, peril, state), optional photo folder path, optional roof report.
- **Outputs.** A prioritized findings list; a printable pre-submission QA sheet for the file; a personal "what got me kicked back last time" history.
- **Essential features.** A **human-editable rule pack format** (YAML/JSON) per carrier; a shipped baseline pack of universal checks — price list version vs. date of loss, missing F9 notes on LAB and non-standard items, recoverable vs. non-recoverable depreciation consistency, O&P applied with fewer than three trades, sketch area vs. roof report area mismatch beyond tolerance, contents on the dwelling coverage, missing required narrative sections, photo count below the peril minimum; rule-pack import/export so adjusters can share packs.
- **Excluded from v1.** Writing or correcting the estimate. Direct Xactimate integration. Any cloud service.
- **AI.** Optional and narrow — useful for reading the narrative and flagging a missing causation statement. The line-item checks must be deterministic rules; an adjuster will not trust a probabilistic "your depreciation is wrong."
- **Why not a spreadsheet.** The input is a PDF of a 200-line estimate. A spreadsheet cannot parse it, and a static checklist doesn't know that *this* carrier wants photos of every elevation while *that* one wants moisture readings logged in the notes.
- **Complexity.** Medium. **Learning.** 20 minutes. **Value.** If it prevents two kickbacks a month, it pays for a day of work.
- **Risks.** Xactimate PDF layout changes break the parser (mitigate: layout-tolerant extraction, ship a "parse check" mode). Rule packs encoding a carrier's confidential guidelines could raise contract questions — ship packs empty and let adjusters author their own from their own experience.
- **Substitutes.** AdjusterProQA, $149/mo, closed rules, generic best practice. **Differentiation:** the rules are *yours*, per carrier, editable, free, offline, and shareable.
- **Paid customization.** Very high. "Encode our firm's 40-carrier guideline library into rule packs" is a real engagement for an IA firm.

---

### B. **FeeLedger** — per-claim fee reconciliation and settlement statement auditor

- **User.** 1099 IA rostered with one or more firms.
- **Problem.** P2. No independent way to verify payment.
- **Current workflow.** Receive a settlement statement → glance at the total → assume it's right.
- **Proposed workflow.** Maintain a lightweight claim log (claim #, firm, carrier, final amount, close date) → import the firm's statement (CSV or PDF) → the tool recomputes expected fee from the encoded schedule and split, matches line by line, and reports: paid correctly / underpaid / missing / holdback outstanding / charged back.
- **Inputs.** Fee schedule per firm (tier table + split, entered once), claim log, settlement statements.
- **Outputs.** Exception list with dollar deltas; aging report of unpaid closed claims; holdback release tracker; year-end 1099 cross-check; a per-firm effective-rate comparison ("Firm A actually nets me $X/claim vs Firm B's $Y").
- **Essential features.** Tiered schedule modeling with commercial/residential variants and T&E crossover; supplement-driven tier changes; chargeback ledger; multi-firm rollup.
- **Excluded from v1.** Invoicing, accounting-package integration, tax filing.
- **AI.** Inappropriate for the math. Optional only for extracting rows from an unstructured PDF statement.
- **Why not a spreadsheet.** A spreadsheet *is* the current workaround, and it fails on statement import, on supplement-driven retiering, and on holdback tracking across periods. But this is honestly the concept closest to "well-built spreadsheet," which is an argument for shipping it as a small app with a spreadsheet-familiar grid rather than something heavier.
- **Complexity.** Medium (small if statement import is CSV-only in v1). **Learning.** 30 minutes. **Value.** Direct dollars recovered plus the negotiating leverage of knowing your real per-claim yield by firm.
- **Risks.** Firms may dislike adjusters auditing them — which is precisely why it must run locally with no telemetry. Statement formats vary per firm (mitigate: a mapping wizard, not hardcoded parsers).
- **Substitutes.** None found. Dragonfile ($29.99/mo) tracks payments but does not audit them against a schedule.
- **Paid customization.** Moderate — building the import mapping for a specific firm's statement format.

---

### C. **ClearToWork** — multi-state license, CE, and deployment-eligibility tracker

- **User.** IA holding non-resident licenses.
- **Problem.** P6.
- **Proposed workflow.** Enter licenses once → see a renewal/CE calendar with escalating alerts → when a storm hits, enter the state and check "am I clear to work here, and if not, what's the fastest path?"
- **Inputs.** License list (state, number, DHS, expiry, CE completed), CE certificates.
- **Outputs.** Renewal calendar with lead-time alerts; CE hour gap per state including ethics; a **deployment-eligibility answer** per state (licensed / emergency registration available / temporary license required / no requirement) with the DHS cascade risk flagged.
- **Essential features.** The four-way emergency-licensing state matrix; DHS dependency warning (home state lapse invalidating non-residents); document vault for certificates.
- **Excluded.** Filing licenses (NIPR/Sircon own that), selling CE.
- **AI.** Inappropriate.
- **Why not a spreadsheet.** A spreadsheet can hold dates. It cannot hold the state-by-state emergency-licensing matrix or model the DHS cascade — but a well-made spreadsheet gets 70% of the way, which is a real objection.
- **Complexity.** Small. **Learning.** 15 minutes. **Value.** Avoids a lapse that costs $250–500 plus a 40-hour course plus lost deployments.
- **Risks.** The state matrix must be maintained or it becomes dangerously wrong. Ship it as a versioned, dated, community-editable data file with a visible "last verified" date, and never present it as legal advice.
- **Substitutes.** **AdjusterTrack, $19–$99/mo — occupied space.** Differentiation is the deployment-eligibility layer and being free/offline.

---

### D. **ClaimClock** — contact attempt, SLA, and diary compliance log

- **User.** Field IA managing 20–150 open files.
- **Problem.** P4.
- **Proposed workflow.** Log each contact attempt in three taps (date, time, method, outcome) → the tool computes statutory and carrier clocks per claim → a daily "what's about to breach" list → one click generates the compliant, timestamped contact-attempt block to paste into the carrier's notes field.
- **Inputs.** Claim list with assignment date, state, carrier; contact attempts; inspection and estimate-upload dates.
- **Outputs.** Aging/at-risk dashboard; per-claim compliance timeline; **pasteable documentation text** that includes every element a market-conduct examiner looks for.
- **Essential features.** Per-state statutory clock table; per-carrier SLA overrides; the paste-block generator (this is the feature that earns daily use — it saves typing *and* improves the file).
- **Excluded.** Portal integration, being a CRM, storing claim documents.
- **AI.** Inappropriate. Dates and rules.
- **Why not a spreadsheet.** A spreadsheet cannot generate the narrative documentation block, and manual date math across 100 files with different state rules is exactly where errors live.
- **Complexity.** Small. **Learning.** 10 minutes. **Value.** Scorecard protection, E&O defensibility, and 2–5 minutes saved per contact event.
- **Risks.** Statutory table accuracy and maintenance; must be framed as a tracking aid, not compliance certification.
- **Substitutes.** Portal task lists (carrier-specific, don't span carriers); Dragonfile has deadline reminders but not the documentation generator.
- **Paid customization.** High — encoding a specific carrier's SLA matrix and preferred note format.

---

### E. **ShotList** — pre-upload photo completeness auditor and bulk renamer

- **User.** Field IA, at the truck before leaving the site, or at the laptop before upload.
- **Problem.** P3, specifically the *completeness* half rather than the crowded *captioning* half.
- **Proposed workflow.** Point the tool at the claim's photo folder → it checks the set against a per-carrier/per-peril required-shot list, flags technical defects, and renames/sequences into carrier order.
- **Inputs.** Photo folder, carrier + peril selection, claim number.
- **Outputs.** A missing-shots checklist **while you can still walk back to the property**; a defect list (blurry, underexposed, near-duplicate, EXIF date or geotag inconsistent with the inspection); bulk-renamed and sequenced files; a printable photo index page.
- **Essential features.** Editable required-shot templates (front/rear/left/right elevation, address verification, roof slopes, per-room overview, moisture readings on water losses); conventional CV for blur/exposure/duplicate detection; safe non-destructive renaming.
- **Excluded from v1.** Captioning, damage classification, cloud sync.
- **AI.** Optional, second version. Blur and duplicate detection are conventional image processing, not AI. Auto-classifying "this is a roof shot" is where AI would earn its place — and where Verisk, ClaimMate and CaptionBuilder already are.
- **Why not a spreadsheet.** It has to read image files and EXIF.
- **Complexity.** Small to medium. **Learning.** 10 minutes. **Value.** A single avoided return trip to a property pays for the year. Also 10–20 minutes of sorting per claim.
- **Risks.** **Crowded category.** Honest positioning: this is a *checklist-and-QC* tool, not another captioning app, and it must not pretend otherwise.
- **Substitutes.** myAdjustiMate ($4.99/5 projects), ClaimMate, PHOTO iD, CaptionBuilder, CompanyCam ($19–79/mo), FieldScribe AI ($199/mo), Verisk XactAI.
- **Paid customization.** Moderate — building a carrier's exact required-shot list and naming convention.

---

### F. **InventoryDesk** — contents / personal property inventory builder

- **User.** IA on a contents-inclusive loss.
- **Problem.** P7.
- **Proposed workflow.** Enter items once in a fast keyboard-driven grid (or dictate them) → apply category-based depreciation → export in the carrier's exact required format.
- **Inputs.** Item entries, category/age table, carrier form template.
- **Outputs.** Carrier-format inventory (Citizens-style 13-field layout and equivalents), depreciation schedule with per-category useful-life basis, totals reconciling to the statement of loss, CSV for import elsewhere.
- **Essential features.** Category library with default useful lives; per-item override with reason; duplicate detection; per-room grouping; sales-tax handling; export templates.
- **Excluded.** Pricing lookups against retailers, photo attachment, valuation opinions.
- **AI.** Optional — transcribing an insured's handwritten list photo into rows is a legitimate AI use where OCR alone struggles. The depreciation math must be deterministic.
- **Why not a spreadsheet.** The carrier form *is* a spreadsheet, which is exactly the problem: no depreciation logic, no category defaults, no validation, and a new blank one every claim.
- **Complexity.** Medium. **Learning.** 30 minutes. **Value.** Hours on a large contents loss, plus fewer depreciation kickbacks.
- **Risks.** Depreciation tables vary by carrier and state; must be user-editable and never presented as authoritative.
- **Paid customization.** High — every carrier has a different form.

---

### G. **StormBook** — deployment expense ledger and profitability calculator

- **User.** CAT adjuster.
- **Problem.** P5.
- **Proposed workflow.** Open a deployment (event, state, dates) → log mileage, lodging, meals, rental, supplies against it → at close, see net profit per deployment day and get a Schedule C category summary.
- **Inputs.** Trip legs with odometer readings, receipts, fee income (ideally imported from FeeLedger).
- **Outputs.** IRS-compliant mileage log (date, miles, destination, purpose, year-start/end odometer); GSA M&IE per diem by locality and date; lodging at actual with receipt links; **net-per-deployment-day**; Schedule C category rollup.
- **Essential features.** The self-employed per diem rule enforced in the UI — M&IE per diem allowed, lodging per diem **not** allowed; 2026 rate at 72.5¢/mile with rate-by-year history; receipt attachment; deployment comparison.
- **Excluded.** Filing taxes, bank integration, invoicing.
- **AI.** Optional for receipt OCR. Inappropriate for anything tax-determinative.
- **Why not a spreadsheet.** Honestly, a spreadsheet gets close. The differentiators are the built-in GSA locality tables, the enforced lodging rule, and per-deployment profitability — none of which a blank sheet gives you.
- **Complexity.** Small. **Learning.** 20 minutes. **Value.** Recovered deductions plus the strategic answer to "should I take this deployment?"
- **Risks.** Tax rules change annually; must be dated, versioned, and clearly not tax advice.
- **Substitutes.** MileIQ, QuickBooks Self-Employed, generic mileage templates — none deployment-aware.

---

### H. **DayPlan** — SLA-aware inspection sequencer

- **User.** CAT adjuster planning tomorrow.
- **Problem.** P8.
- **Proposed workflow.** Paste tomorrow's claims with addresses, appointment windows and SLA due dates → get a sequenced route that respects windows and prioritizes files closest to breach → export to Google Maps and calendar.
- **Inputs.** Claim list with addresses, windows, due dates; start/end location.
- **Outputs.** Ordered day plan with drive-time estimates; a "won't fit — these slip" warning; map/calendar export; actual-arrival capture that feeds ClaimClock.
- **Essential features.** Due-date-weighted priority (the wedge — generic planners optimize distance, not compliance risk); mid-day re-sequencing when an emergency file lands.
- **Excluded.** Live traffic, multi-adjuster dispatch, its own map rendering.
- **AI.** Inappropriate — this is a constrained optimization problem.
- **Why not a spreadsheet.** Needs geocoding and a solver.
- **Complexity.** Small to medium. **Learning.** 15 minutes. **Value.** Real if the 3–4 hours/day driving figure is anywhere near right — but that figure is vendor-sourced and unverified.
- **Risks.** Geocoding API dependency and cost; commoditized category; **weakest evidence base in the set.**
- **Substitutes.** Zeo, Circuit, Badger Maps.

---

### I. **ReportSmith** — carrier-format captioned report assembler

- **User.** IA writing the narrative report and statement of loss.
- **Problem.** Repetitive narrative drafting; reports rejected for missing required elements.
- **Proposed workflow.** Fill a structured field form once (peril, cause, coverage applied, scope summary, ITEL status, subrogation, mortgagee, contact history) → generate the carrier's report format with all required sections present → edit the prose, not the structure.
- **Inputs.** Structured claim facts (much of it already captured by ClaimClock and Preflight), a carrier report template.
- **Outputs.** Captioned report draft; statement of loss three-column reconciliation; a required-elements checklist showing what is still missing.
- **Essential features.** Template library; required-section validation before export; reusable phrase snippets for recurring findings.
- **Excluded.** Coverage decisions, liability opinions — the adjuster's judgment is the product and must stay theirs.
- **AI.** Optional and bounded. Useful to smooth prose from bullet facts. **Inappropriate** for generating coverage conclusions, and a real liability hazard if it hallucinates a fact into a legal document. If AI is offered, every generated sentence should be traceable to a field the adjuster filled.
- **Why not a spreadsheet.** It's document assembly.
- **Complexity.** Medium. **Learning.** 45 minutes. **Value.** 20–40 minutes per claim.
- **Risks.** Homogenized boilerplate reports are a documentation risk of their own — market-conduct citations often stem from generic language ("note 'fraud suspected'" without indicators, per [Adjuster Authority](https://adjusterauthority.com/adjuster-report-writing-standards/)). Template design must force claim-specific input, not permit blanks.
- **Substitutes.** FieldScribe AI ($199/mo), ClaimMate, Verisk XactAI note summarization.
- **Paid customization.** Very high — one template per carrier is a repeatable paid deliverable.

---

### J. **TierPoint** — supplement fee-tier impact calculator

- **User.** IA deciding how to handle a supplement or a borderline scope item.
- **Problem.** The fee is a step function of final claim amount, and adjusters cannot see the steps.
- **Proposed workflow.** Enter firm, claim type and current net claim amount → see the current tier, the distance to the next breakpoint, and the marginal fee change → track expected fee movement as supplements post.
- **Inputs.** Fee schedule (shared with FeeLedger), current claim amount, pending supplement amounts.
- **Outputs.** Current tier and fee; dollars to the next breakpoint; expected fee delta; a pending-supplement watchlist showing fees not yet realized.
- **Essential features.** Multi-firm schedules; residential/commercial variants; T&E crossover threshold; "expected receivable" total across open files.
- **Excluded from v1.** Anything that recommends scoping decisions.
- **AI.** Inappropriate.
- **Why not a spreadsheet.** This one genuinely could be a spreadsheet — and that is a legitimate finding. It is included because it is *tiny*, it makes an invisible economic structure visible, and it is the natural free on-ramp to FeeLedger.
- **Complexity.** Small (a weekend). **Learning.** 5 minutes. **Value.** Better forecasting; avoids the surprise of a supplement that adds work without adding fee.
- **Ethical note worth stating plainly.** This tool must never be framed as helping an adjuster push a claim over a breakpoint. It exists to let the adjuster *forecast income*, not to shape a settlement. Scope must be determined by damage, full stop — and any product in this space that blurs that line invites a bad-faith problem for everyone.
- **Substitutes.** None found.

---

## 5. Opportunity ranking

Scored 1–5 on each dimension; 50 maximum.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of impl. | Narrow scope | Differentiation | Customization | Test data | Evidence conf. | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **A** | **Preflight** — carrier guideline QA | 5 | 5 | 5 | 4 | 3 | 4 | 4 | 5 | 3 | 5 | **43** |
| **B** | **FeeLedger** — fee reconciliation | 5 | 4 | 5 | 4 | 4 | 5 | 5 | 4 | 2 | 4 | **42** |
| **D** | **ClaimClock** — contact/SLA log | 4 | 5 | 4 | 5 | 5 | 5 | 3 | 3 | 4 | 4 | **42** |
| **E** | **ShotList** — photo completeness audit | 4 | 5 | 4 | 5 | 4 | 4 | 2 | 3 | 4 | 5 | **40** |
| **G** | **StormBook** — deployment ledger | 3 | 4 | 4 | 5 | 5 | 5 | 3 | 3 | 4 | 4 | **40** |
| **J** | **TierPoint** — fee-tier calculator | 3 | 3 | 5 | 5 | 5 | 5 | 5 | 3 | 3 | 3 | **40** |
| **F** | **InventoryDesk** — contents inventory | 4 | 3 | 4 | 4 | 4 | 4 | 4 | 4 | 3 | 4 | **38** |
| **I** | **ReportSmith** — report assembler | 4 | 5 | 4 | 4 | 3 | 3 | 2 | 5 | 3 | 4 | **37** |
| **C** | **ClearToWork** — license/CE tracker | 4 | 2 | 3 | 5 | 4 | 5 | 2 | 2 | 4 | 5 | **36** |
| **H** | **DayPlan** — SLA-aware routing | 3 | 4 | 3 | 4 | 4 | 4 | 2 | 3 | 4 | 3 | **34** |

### The top three

**1. Preflight (43).** It sits on the best-evidenced problem in the market and the one with the most direct link to money: kickbacks delay closure, closure gates the fee. The competitive read is favorable — AdjusterProQA proves willingness to pay $149/month for a *closed, generic* version of this, which means an *open, carrier-specific, editable* version has a genuine wedge rather than a me-too position. The rule-pack format is the real asset: it turns tacit knowledge that currently lives in an adjuster's memory into a shareable file, and it is exactly the kind of thing a client pays to have built for their carrier list. The honest weakness is implementation risk on estimate parsing, which is why the scoring gives it only a 3 there.

**2. FeeLedger (42).** The largest genuinely *unoccupied* gap found in this entire research pass. Every structural condition for systematic underpayment exists — tiers keyed to a moving final amount, per-firm splits, 20% holdbacks, chargebacks, multiple firms, no reconciliation tool — and adjusters demonstrably distrust the numbers enough to compare notes in public forums. It is also the only concept here that touches the adjuster's actual income rather than their time. Scored down on test data (real settlement statements are hard to obtain without practitioner relationships) and on evidence (the structure is verified; a documented underpayment case is not).

**3. ClaimClock (42).** The most buildable of the three and the one most likely to earn daily habitual use, because the paste-block generator saves typing on every single contact event — a tool used ten times a day beats a tool used once a claim. It also has the clearest regulatory backing: $4.7M in P&C claims enforcement actions in a single year, dominated by timeliness and documentation deficiencies. Scored down on differentiation because deadline reminders exist elsewhere; the documentation generator is the part nobody else ships.

### What to investigate next

**FeeLedger, ahead of Preflight** — despite Preflight scoring one point higher. Reasoning: Preflight's remaining risk is *technical* (can the estimate PDF be parsed reliably?), which can be answered privately in a day with sample files. FeeLedger's remaining risk is *evidentiary* (does underpayment actually happen at a rate adjusters care about?), which can only be answered by talking to practitioners and is the kind of question that gets more expensive to answer the later you ask it. Resolve the question you cannot resolve alone first.

A strong second move is to note that **A + B + D + J share one data model** — a claim log with dates, amounts, carrier, firm and status. Building that model once and shipping four small tools against it is a materially better plan than building four independent apps, and it lets TierPoint (a weekend of work) act as the free on-ramp that gets the claim log populated.

---

## 6. Validation plan

### Questions to ask practitioners

**On kickbacks (Preflight):**
- Out of your last 20 files, how many came back? What were the top three reasons?
- Do you keep a carrier cheat sheet? Where does it live, and how did you build it?
- How long between submission and a kickback landing? How long to fix and resubmit?
- Would you export an estimate PDF to a desktop tool before uploading, or is that a step too many?

**On fees (FeeLedger):**
- Have you ever found an error on a settlement statement? How did you find it? What happened?
- Do you know your effective per-claim yield by firm? Could you produce it today?
- How do you track the 20% holdback? Do you know what's outstanding right now?
- Has a supplement ever changed your fee tier, and did you notice at the time or later?

**On compliance (ClaimClock):**
- How do you track contact attempts across carriers with different portals?
- Have you ever been dinged on a scorecard? For what?
- What do you type into a note after an unsuccessful contact attempt — the same thing every time?

### Who to interview

- **Working IAs** at 2–5 years' experience — past the learning curve, still doing the work personally. Reachable via CatAdjuster.org, IA Path's community, and adjuster LinkedIn groups.
- **IA firm QA reviewers / desk examiners** — the people issuing the kickbacks. They know the rejection distribution precisely, and they are the paid-customization buyer for Preflight.
- **IA firm accounting staff** — for how settlement statements are actually produced, and whether errors are known internally.
- **Adjuster trainers** (IA Path, AdjusterPro, Actionable Insights) — highest-leverage single conversations; they hear every complaint in the market and have distribution.
- **An adjuster-focused CPA**, for StormBook.

### Search terms for the next pass

`"kicked back" adjuster estimate carrier` · `adjuster "fee bill" statement dispute` · `"carrier guidelines" adjuster cheat sheet` · `Xactimate "estimate audit report" reviewer` · `adjuster "holdback" 20% fee` · `CAT deployment "didn't get paid"` · `site:catadjuster.org fee schedule chargeback` · `site:reddit.com/r/adjusters kickback` · `site:reddit.com/r/Xactimate carrier rejected` · `IA firm settlement statement adjuster reconcile`

### Sample files and data needed

- 5–10 **redacted Xactimate estimate PDFs** across carriers and perils — the single highest-value artifact; Preflight cannot be built without them.
- 2–3 **redacted settlement statements** from different IA firms, plus the matching fee schedules.
- One **carrier guideline document** (likely confidential — may only be describable, not obtainable).
- A **real claim photo folder** (200+ images) for ShotList.
- One completed **contents inventory** in a carrier's format.
- Public: the [TWIA fee schedule](https://www.twia.org/wp-content/uploads/2019-Claims-RFQ_Adjuster-Fee-Schedule.pdf) is already a usable test fixture for FeeLedger and TierPoint.

### Prototypes that would validate

- **Preflight, 2 days.** A Python script that extracts line items from one carrier's estimate PDF and runs six hardcoded checks. Success = it parses reliably and finds at least one real issue in a file the adjuster already submitted.
- **FeeLedger, 1 day.** A script that takes the TWIA schedule plus a 30-row claim CSV and produces expected fees. Show it to an adjuster and ask, "does this match what you were paid?" The answer to that one question decides the concept.
- **ClaimClock, 1 day.** A single-page HTML app with local storage of the claim list and a paste-block generator. Ship it and see if anyone uses it twice.

### Assumptions most likely to be fatal

1. **That estimate PDFs parse reliably.** If Xactimate output resists structured extraction across versions and carriers, Preflight collapses to a manual checklist — still useful, far less valuable.
2. **That underpayment is material.** If IA firms are largely accurate and adjusters mostly trust them, FeeLedger is solving anxiety rather than loss. *This is the assumption to test first.*
3. **That adjusters will add a step before upload.** A tired adjuster at 9pm on file 11 of the day may simply not run the check. Anything that takes more than 30 seconds will be skipped.
4. **That the rule-pack format survives contact with reality.** If carrier guidelines are too situational to encode as rules, the whole Preflight thesis weakens.
5. **That local-only is a feature, not a limitation.** Adjusters may want phone-to-laptop sync badly enough to prefer a cloud product — which would put these tools back into a crowded field on someone else's terms.
6. **That anyone will pay for customization.** The free base may simply be enough, leaving no revenue path.

---

## 7. Cross-industry patterns

Six patterns from this market that transfer to specific markets already sitting in the backlog.

**Pattern 1 — Reviewer-rejection preflight.** *Run the reviewer's checklist against your own deliverable before you submit it.* Wherever a professional submits work to an outside gatekeeper who returns it with comments, the rejection criteria are knowable and encodable, and the submitter — not the reviewer — bears the cost of rework.
→ *Construction submittal, RFI, and closeout coordination*; *Building permit expediting and code consulting firms*; *Environmental laboratories producing regulator EDD deliverables*; *Durable medical equipment (DME) suppliers — documentation and billing compliance*; *Mortgage post-closing QC and trailing document vendors*; *Fire protection / fire sprinkler design — handoffs-and-qa*.

**Pattern 2 — Tiered-fee reconciliation against a schedule you don't control.** *Independently recompute what you should have been paid and diff it against what you were paid.* Applies anywhere a contractor or vendor is paid per unit off a schedule administered by the payer, with holdbacks and retroactive adjustments.
→ *Independent pharmacy third-party reconciliation and PBM claw-backs*; *Small third-party medical billing companies (RCM service bureaus)*; *Freight bill audit and payment for small shippers*; *Small motor carriers (5-50 trucks) back office and settlement*; *Third-party truck dispatch services*; *Workers' compensation medical billing and state fee schedule compliance*.

**Pattern 3 — Dual-clock deadline tracker with generated documentation text.** *Track a statutory clock and a contractual clock simultaneously, and emit the compliance narrative as text the professional pastes into someone else's system.* The generated-paste-block is the transferable insight: it makes the tool valuable even when it cannot integrate with the system of record.
→ *HOA and condominium management companies — estoppel and demand response desk*; *County recorder offices — document intake, indexing and rejection handling*; *Mortgage servicer payoff and lien release departments*; *Title abstracting and independent title search contractors*; *Immigration law practice — back-office*.

**Pattern 4 — Multi-jurisdiction credential and eligibility matrix.** *Answer "am I legally cleared to do this work, in this place, today?" when the answer depends on a patchwork of state rules and a portfolio of credentials with cascading dependencies.*
→ *Welding inspection (AWS CWI) and NDT service providers under ASTM E543 / SNT-TC-1A*; *Title 24 acceptance test technicians (ATT)*; *Special inspection agency accreditation consultants (IAS AC291, ANAB, WABO)*; *Radiation safety officer services and portable gauge licensee compliance*; *Mobile notary and loan signing service operators*; *Remote online notarization (RON) notaries*.

**Pattern 5 — Field-evidence completeness auditor keyed to a required-shot list.** *Check the evidence set against a required list while the professional is still on site and can fix it.* The value is concentrated entirely in catching the gap before leaving, not in organizing what was captured.
→ *Building envelope and roofing consultants performing field water testing (ASTM E1105, AAMA 501.2)*; *Ready-mix concrete producer quality control departments*; *Asphalt plant producer quality control technicians*; *UAS / drone mapping and reality-capture service providers*; *Geotechnical drilling subcontractors and rig operations*.

**Pattern 6 — Per-engagement profitability ledger for the 1099 field professional.** *Bind expenses and revenue to a discrete deployment or job so the contractor can answer "did that one make money?" before accepting the next.* Generic accounting tools track the year; these professionals need the unit.
→ *Intermodal drayage operators and port trucking*; *Third-party truck dispatch services (5-50 owner-operator trucks)*; *UAS / drone mapping and reality-capture service providers*; *Mobile notary and loan signing service operators*; *Geotechnical drilling subcontractors*.

---

## 8. Sources and confidence

### Verified findings — primary or authoritative sources, directly checked

| Finding | Source |
|---|---|
| 2026 IRS business standard mileage rate is 72.5¢/mile | [IRS](https://www.irs.gov/newsroom/irs-sets-2026-business-standard-mileage-rate-at-725-cents-per-mile-up-25-cents) |
| 33 states license independent adjusters; DHS and reciprocity framework | [NAIC State Licensing Handbook Ch. 18 (PDF)](https://content.naic.org/sites/default/files/inline-files/Chapter%2018%20-%20Adjuster%20Licensing.pdf) |
| Claim files retained calendar year of closing + 3 years (5 in some states) | [NAIC Model Law 910 (PDF)](https://content.naic.org/sites/default/files/model-law-910.pdf) |
| 28 states/jurisdictions adopted the Insurance Data Security Model Law as of Aug 2025 | [NAIC brief (PDF)](https://content.naic.org/sites/default/files/government-affairs-brief-data-security-model-law.pdf) |
| Actual tiered adjuster fee schedule with T&E crossover | [TWIA/TFPA 2019 Claims RFQ (PDF)](https://www.twia.org/wp-content/uploads/2019-Claims-RFQ_Adjuster-Fee-Schedule.pdf) |
| 270 P&C claims enforcement actions / $4.7M fines in 2019; documentation is the dominant root cause | [Claims Journal](https://www.claimsjournal.com/news/national/2020/10/05/299731.htm) |
| Assignment packet contents and workflow status tracking in XactAnalysis | [XactAnalysis Help](https://xactanalysis.helpdocs.io/l/enUS/article/kb5nfomssh-assignment-detail-en-us) |
| Performance scorecard measures cycle time, satisfaction, estimate quality | [Verisk XactAnalysis](https://www.verisk.com/products/xactanalysis/) |
| "Kickback" is practitioner terminology; ~50,000 Xactimate line items; QA product at $149/mo | [AdjusterPro / AdjusterProQA](https://adjusterpro.com/adjusterproqa/) |
| Carrier guideline variance "impossible to remember"; LAB items always questioned | [R&R Magazine](https://www.randrmagonline.com/articles/88186-the-10-commandments-of-xactimate-estimating-success) |
| Common estimating errors; "always QC your own file before turning it in" | [AdjustingExpectations](https://www.adjustingexpectations.com/adjuster-blog/the-most-common-estimating-mistakes) |
| Carrier-specific certification exists as a formal paid training track | [Crawford](https://www.crawco.com/cat/training/carrier-specific-certification-2022-04-13) |
| Photo labeling of a 100+ image report takes 40–50 minutes manually | [myAdjustiMate](https://myadjustimate.com/) |
| Unlabeled/context-free photos cause carrier resubmission requests | [CompanyCam](https://companycam.com/blog/3-costly-mistakes-when-submitting-photos-to-insurance-carriers) |
| Verisk shipping AI photo labeling and note summarization | [Verisk XactAI](https://www.verisk.com/company/newsroom/verisk-introduces-new-ai-tools-to-streamline-the-property-claims-experience/) |
| Contact-attempt dates are a required report element; denial-rationale gaps are top exam deficiencies | [Adjuster Authority](https://adjusterauthority.com/adjuster-report-writing-standards/) |
| Payment takes 2 weeks–3 months; predatory-firm risk | [IA Path](https://iapath.com/independent-adjuster-fee-schedule/) |
| ~80/20 payment with holdback; audit clawbacks | [AdjusterPro](https://adjusterpro.com/blog-how-fast-do-insurance-adjusters-get-paid/) |
| First-person: 1099 status, $80k compressed into a season, biggest retention deterrent | [Catastrophe Adjusting](https://catastropheadjusting.substack.com/p/we-lived-paycheck-to-paycheck) |
| Adjusters publicly comparing fee schedules across vendor firms; 34-year T&E rate history | [CatAdjuster.org 1](https://catadjuster.org/Forums/tabid/60/aft/11318/Default.aspx), [CatAdjuster.org 2](https://catadjuster.org/Forums/tabid/60/aft/9067/Default.aspx) |
| Texas renewal/lapse mechanics and DHS cascade risk; 24 CE hrs / 2 yrs incl. 3 ethics | [Texas License Path](https://texaslicensepath.com/texas-adjuster-license-renewal/) |
| Four-way emergency licensing state matrix; NAIC-recommended 90-day cap | [ResourcePro](https://www.resourcepro.com/blog/help-in-a-crisis-emergency-adjuster-licensing/) |
| Self-employed may use M&IE per diem but not lodging per diem | [TaxAudit](https://www.taxaudit.com/tax-audit-blog/2025/can-self-employed-claim-per-diem-deductions) |
| Contents inventory field requirements (13 fields/item) | [Citizens PPI form (PDF)](https://www.citizensfla.com/documents/20702/54161/personal-property-inventory-form.pdf/3e8054dc-fc27-4990-930c-f8846c6e4b52) |
| Xactimate mechanics: price list naming, Cat/Sel codes, macros, RCV/ACV/O&P, 2" sketch tolerance | [Docusketch — read](https://www.docusketch.com/post/how-to-read-an-xactimate-estimate), [write](https://www.docusketch.com/post/how-to-write-an-xactimate-estimate) |
| Captioned report obligation and statement-of-loss structure | [Zalma 1](https://barryzalma.substack.com/p/a-video-explaining-why-insurers-require), [Zalma 2](https://barryzalma.substack.com/p/how-an-insurer-resolves-a-claim-part-94d) |
| E&O commonly contractually required at $1M/$1M; leading claim triggers | [Schneider Insurance](https://schneider-insurance.com/errors-omissions-adjusters-guide/) |
| Competitive pricing: AdjusterTrack $19–99/mo, ClaimWizard $99–250/mo, Dragonfile $29.99/mo, DocuSketch 1099-adjuster plan from $500/mo, FieldScribe AI $199/mo, CompanyCam $19–79/mo | [AdjusterTrack](https://www.adjustertrack.com/), [ClaimWizard](https://claimwizard.com/pricing/), [Dragonfile](https://dragonfile.io/features-for-solo-adjusters/), [DocuSketch](https://www.docusketch.com/pricing), [FieldScribe](https://fieldnotesai.com/blog/best-mobile-apps-insurance-field-adjusters-claims-photos-2026), [CompanyCam](https://roofingsoftwareguide.com/guides/companycam-pricing/) |
| Drone workflow formalized inside an IA firm (Part 107, XactAnalysis/Cotality integration) | [Eberl](https://eberls.com/drone-roof-inspection-what-adjusters-need-to-know/) |
| Daily 20–30 claims / 50-mi radius vs. CAT 100–200 claims per deployment | [BSA Claims](https://www.bsaclaims.com/difference-between-cat-daily-claims-adjusters/) |

### Strong inferences — well-supported but not directly quoted by a practitioner

- **Adjusters manage claim pipelines and fees in self-built spreadsheets.** Supported by the total absence of adjuster-specific templates in search results and by Dragonfile explicitly marketing "transition from spreadsheets" ([Dragonfile](https://dragonfile.io/2026/03/how-to-transition-from-spreadsheets-to-automated-claims-tracking/)) and IA Path's tool list showing generic SaaS stitched together ([IA Path](https://iapath.com/insurance-adjuster-tools/)).
- **Multi-portal login burden is real.** Inferred from AdjusterPortal's existence, scale ("10,000+ adjusters") and positioning against "managing multiple logins and portals" ([AdjusterPortal](https://www.adjusterportal.com/)).
- **Adjusters routinely leave claim data on personal devices.** No NAIC or DOI text was found addressing this directly; it is governed by carrier vendor-security addenda ([legal analysis](https://cgl-llp.com/insights/cybersecurity-independent-contractors/)). The design conclusion (build local-first) holds either way.
- **Supplement-driven fee-tier changes are a live irritation.** The structure is verified from the TWIA schedule; the irritation is inferred.
- **Contents inventory transcription is a major time sink.** Inferred from the form's structure.
- **Fee-schedule splits run 55–70%.** Consistent across four independent secondary sources but no primary contract seen.

### Tentative hypotheses — need practitioner validation before any build

- **That adjusters are materially underpaid by reconciliation errors.** *The load-bearing assumption under the #2-ranked concept.* Validate first.
- **That field adjusters spend ~40% of the workday driving.** Single vendor source ([Zeo](https://zeorouteplanner.com/how-to-optimize-adjuster-routes-cut-drive-time-by-30/)), unverified.
- **That Xactimate estimate PDFs parse reliably enough to automate line-item QA.** Untested; AdjusterProQA's existence is suggestive but not proof.
- **That a typical CAT adjuster holds 20–40 non-resident licenses.** Structurally plausible from the reciprocity patchwork; no source gave a number.
- **That the photo *completeness* niche is genuinely open** while captioning is crowded. Plausible from the product landscape; not confirmed with an adjuster.
- **That adjusters will adopt an extra desktop step before upload.** The behavioral assumption under Preflight, ShotList and ReportSmith alike.

### Known gaps in this cycle

1. **Reddit was unreachable** (proxy 403 across all paths). r/adjusters, r/Xactimate, r/CatAdjuster and r/InsuranceClaims are the densest source of unfiltered practitioner language in this market and contributed nothing here. **First action next cycle.**
2. **No real carrier guideline document** was obtained — likely confidential.
3. **No settlement statement or fee bill** artifact was found publicly.
4. **No systematic CAT deployment cost data** (hotel/night, average deployment length, typical out-of-pocket).
5. **Current Xactimate pricing is unconfirmed** — user-reported ~$2,390–2,690/year, not vendor-published.

---

*Cycle complete. Report written 2026-08-06 under claim `1c0329d5`.*
