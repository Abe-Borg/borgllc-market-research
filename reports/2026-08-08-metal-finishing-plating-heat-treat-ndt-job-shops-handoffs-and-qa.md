# Metal Finishing, Plating, Heat Treat and NDT Job Shops — Handoffs and QA

**Market research cycle report**

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market** | Metal finishing, plating, heat treat and NDT job shops (special-process suppliers) |
| **Angle** | handoffs-and-qa |
| **Claim ID** | `924337f2` |
| **Claimed** | 2026-08-07 (UTC) |
| **Report date** | 2026-08-08 |
| **Backlog remaining after this claim** | 313 assignments |

### Why this assignment over the others available

The ledger held 314 open assignments across 195 markets, 175 of them with zero completed reports. Three filters narrowed it:

**Breadth over depth.** The brief says catalog breadth currently matters more than depth. The 22 completed reports are heavily weighted toward AEC/construction (fire sprinkler design, MEP HVAC, geotechnical, land surveying, construction submittals, flood-zone consulting, NFPA 25 ITM), insurance/claims, trucking, and accounting. Discrete manufacturing has exactly one completed report — machine shop / job shop quoting. Special-process suppliers are a structurally different business from a machine shop: they sell a *transformation of someone else's part*, and their entire commercial output is a piece of paper.

**Angle diversity.** Of the 22 completed reports, `handoffs-and-qa` is the least covered angle (4 reports vs. 8 for `core-practitioner-workflow`). This market's handoff surface is unusually well documented because it is contractually specified in public prime-supplier quality clause documents.

**Evidence availability.** This was the deciding factor. Unlike most small-business markets, the paperwork obligations here are *published*: Nadcap audit checklists (AC7108, AC7102), prime quality-clause PDFs from Northrop Grumman, Ducommun, Leonardo DRS, Collins Aerospace and Lockheed Martin, Boeing's D1-4426 approved-processor list, AMS2750 pyrometry tables, and PRI's own most-common-NCR rankings. This report is built on primary documents, not on inference about what practitioners probably do.

The backlog entry itself pointed here: *"The counterparty receiving flow-down chaos from non-expert customers; Nadcap-accredited and defined by the documents they must produce."* That framing held up.

---

## 1. Market examined

### Who they are

Independent service businesses that perform an irreversible transformation on a customer-owned part and return it:

- **Electroplating, anodizing, chemical conversion coating, passivation, painting** — NAICS 332813 / 332812
- **Commercial heat treating** — hardening, annealing, carburizing, nitriding, vacuum, brazing — NAICS 332811
- **Non-destructive testing service providers** — fluorescent penetrant, magnetic particle, ultrasonic, radiographic/digital radiography, eddy current — inside NAICS 541380
- Adjacent: industrial coating applicators, shot peen, thermal spray

They are almost never the designer, the buyer of the raw material, or the final assembler. They sit between a machine shop and a prime, or between two machine shops.

### How many, and how small

BLS QCEW 2024 annual data (private, US total), computed from the source files:

| NAICS | Industry | Establishments | Employment | Avg emp/estab |
|---|---|---|---|---|
| 332811 | Metal heat treating | 685 | 18,101 | 26.4 |
| 332812 | Metal coating, engraving & allied services | 3,090 | 58,933 | 19.1 |
| 332813 | Electroplating, plating, polishing, anodizing | 2,384 | 52,440 | 22.0 |
| 541380 | Testing laboratories (broader than NDT) | 11,529 | 175,805 | 15.2 |

Size distribution is the load-bearing fact (QCEW 2024 Q1 size-class files):

- **332813 plating: 70.2% of establishments have fewer than 20 employees; 88.8% fewer than 50; only 3.8% have 100 or more.**
- **332811 heat treat: 60.0% under 20; 86.4% under 50.**
- But employment concentrates upward — in 332813, the 11.2% of establishments with 50+ employees hold **52.5%** of the industry's workers.

The [NASF 2022 Economic Impact Report](https://finishingandcoating.com/index.php/plating/1125-nasf-report-says-u-s-industry-is-over-2-600-shops-11-billion-in-output) independently reports **2,600+ US metal finishing shops, ~$10.7B in direct sales, 71,000+ employees**, with 68% under 20 people — closely matching QCEW's 70.2%. It describes the sector as predominantly *"family-owned businesses, many second- or third-generation."* Implied average revenue per shop: **~$4.1M**.

Commercial heat treating is smaller and similar in shape: [The Monty's 2025 survey](https://themonty.com/52-largest-north-american-commercial-heat-treaters-2025/) counts **~530 North American commercial heat treat plants and ~$3B in sales** (~$5.7M/plant), with eight plant closures in the prior ten months.

Consolidation exists but has barely dented the base. Valence Surface Technologies — backed by ATL Partners and BCI, and the largest independent aerospace finishing platform in the world — operates [12 locations after 12 add-on acquisitions](https://www.valencesurfacetech.com/press-release-for-foresight-finishing-press-release/). That is **under 0.5% of US finishing establishments.** In heat treat, Bodycote (62 NA plants) and Aalberts (which [acquired Paulo Products — 6 plants, 522 employees, ~$105M revenue — in May 2025](https://www.heattreattoday.com/aalberts-acquires-paulo-expands-heat-treat-reach-in-n-a/)) are the two multinationals; roughly 85%+ of plants remain independent and family-owned.

### The target user

The **quality manager** — frequently the only one. Two live job postings define the seat precisely:

- **[Electroplating Quality Manager, Heartland Precision Fasteners / DeTray Plating Works, Independence MO](https://to.indeed.com/aaqvgttcwxsg)** (posted 2026-07-29, $80–90k). A one-person quality function. Verbatim: *"Poor quality costs this business $15,000–$25,000 per month in rework, waste, and rejected lots."* Duties include: *"Serve as the final quality authority before parts are released — certifications do not go out without your review and approval"*; maintain *"all quality documentation including certifications, process records, chemical logs, inspection records, and non-conformance reports"*; review **every customer PO and drawing before processing to catch spec conflicts**; own NCRs and 8D corrective actions; run the calibration program; track spec revisions; and personally perform bath titrations.
- **[Metal Finishing Technical Services Manager, Durable Industrial Finishing, Tucker GA](https://to.indeed.com/aanplhlfxk8w)** (posted 2026-07-13, $95–125k). Manages *"3 Technical Services Personnel and 1 Waste Treatment Operator"* and fuses quality, EHS permitting, and plating chemistry into a single seat. It is a **succession posting** — an 18-month paid mentorship to replace a retiring veteran whose "proprietary processes and localized compliance networks" exist only in his head.

**The practical target: a 15–120 employee shop where one person is the certification-signing authority, the document custodian, the contract reviewer, the corrective-action owner, and the audit host.** That single human is the bottleneck any software here has to serve.

---

## 2. How the work is performed

### 2.1 Inbound — the order arrives underspecified

A customer PO arrives naming a process specification. Before accepting the order the shop must resolve a **compound key**, not a single number. Boeing's D1-4426 Appendix D requires the statement of work to define *"specification, specification revision, specification departures, Type, Class, Grade, program number, design authority, pre/post processing steps"* and states the shop must define and document this **["prior to accepting an order"](https://www.stackmet.com/wp-content/uploads/2018/12/d14426-appendix-d-complete.pdf)**.

That key is frequently incomplete on arrival. Documented failure modes:

- **No thickness callout.** Products Finishing, ["What is the Correct Anodizing Specification?"](https://www.pfonline.com/articles/what-is-the-correct-anodizing-specification): *"I come across poor or incorrect finishing specifications on a regular basis."* A reader writes in: *"There was no anodic coating thickness called out. We are not anodizers and we are at a loss as to how to write up a meaningful anodizing specification."*
- **Obsolete or trade-name process callouts.** Advanced Heat Treat publishes a ["Heat Treat Purchase Orders: DOs & DON'Ts"](https://www.ahtcorp.com/articles/blog/heat-treat-purchase-orders-dos-donts/) guide because customers order by discontinued process names ("melonite," "salt bath"), forcing a call-back for approval of an alternative. It also names **over-specification** — aerospace specs applied to non-aerospace parts — causing "unnecessary inspections, preparations, and delayed processing."
- **"Zinc & bake" with no standard reference.** [finishing.com thread 145/37](https://www.finishing.com/145/37.shtml) documents that without an explicit ASTM B633 (or equivalent) reference, platers and subcontractors lack guidance for hydrogen embrittlement relief, and failures often trace to the specification rather than the plating.

### 2.2 The revision problem, and who owns it

The most important structural fact in this market, stated plainly by a practitioner on Elsmar Cove: **["The customer has no PUSH system … to alert you that a revised specification is available."](https://elsmar.com/elsmarqualityforum/threads/whos-responsible-for-verification-of-customer-specifications.85345/)** Customers rarely reissue a PO for an existing part, yet the customer-specific requirements behind it may be revised repeatedly. Another participant in the same thread describes the incumbent control: *"I am responsible to verify all 6 of our customers every 6 months. I look on the portal for each customer and ensure I have the latest on file."*

Manual polling, twice a year, per customer, across portals the shop does not control.

Nadcap knows about the repeat order. AC7108 clause **3.4.3** asks directly: *"Is there a procedure that defines the review of repeat orders for changes in requirements?"* ([AC7108 Rev E](https://www.galvanizeit.com/uploads/resources/AC7108-Rev-E.pdf)).

### 2.3 Planning — building the traveler

The reviewed requirements become a shop traveler / job planning document. Nadcap AC7108 3.3.1 requires it to carry:

- *"Relevant purchase order number, purchase order requirements OR identification which is traceable to engineering requirements"* (3.3.1c)
- *"A step for each process performed, defining the required operator controlled process parameters/ranges"* (3.3.1f)
- *"Each step, or buy-off step in the process flow, is bought off and dated"* (3.3.1h)
- *"specified process parameters which are controlled by the operator are recorded and bought off for each lot"* (3.3.1i)
- All applicable specifications, **including revision level** (4.1.2.1)

A Seattle processor on the finishing.com hotline reports the compliance effect: [*"what used to be a 2 page shop traveler is now 12 pages"*](https://www.finishing.com/276/98.shtml) — with turnaround moving from 3–4 days to 11 days.

### 2.4 Processing — parallel record streams that must intersect

While the job runs, three independent record streams must remain valid *for the date and time that job ran*:

**Solution control (chemical processing).** AC7108 4.5.4 requires records containing tank ID and contents, working volume and level, analysis frequency, constituents analyzed, operating tolerances, date sampled/analyzed, *"Analysis result and calculated constituent values,"* additions and corrections, tank dumps, reanalysis after out-of-spec addition, and the identity of the analyst. Clause **4.5.3** requires *"a system for adjusting frequency of analysis based on rate of change"* — a trending obligation, not a fixed calendar. And **4.5.6** is the clause that turns a records gap into a product problem: it asks whether documents show *"the cessation of processing when any chemical constituent and/or operating parameter … does not comply."*

**Pyrometry (heat treat).** AMS2750G creates a matrix of per-furnace, per-class due dates: reference/primary standards 3 years, secondary annually, field test instruments quarterly, control instruments monthly to semi-annually by class (Table 7); SAT intervals from weekly (Class 1 Type D) to semi-annually (Class 6) (Tables 11–12); TUS intervals monthly to annually (Tables 15–16). Thermocouples carry a **dual trigger**: *"Types M, C, T, K, and E shall be limited to 3 months or five uses, whichever occurs first, between 500.0 °F and 1200.0 °F … and limited to a single use above 1200.0 °F"* (clause 3.1.7.3). Extrapolating correction factors beyond the calibrated range is prohibited (3.1.4.7); linear interpolation between points is permitted (3.1.4.8). And there is a rounding rule most spreadsheets get wrong — clause 2.2.25: *"If the next calibration, test, or sensor replacement is due on a calendar date not contained in that month, then the last day of that calendar month shall be used."*

**Personnel currency (NDT).** [NAS 410](https://ndttrainingonline.com/nas-410-ndt-certification-requirements/) requires annual vision examination (Jaeger 1 or equivalent), recertification at least every 5 years for Levels I and II, annual renewal for Level I Limited, *and* a separate mandatory **annual hands-on proficiency test**. Technique sheets require annual Level III review. A pre-audit checklist guide notes the auditor will want a *"clear and current list of all NDT personnel"* showing *"certification expiration dates and vision examination due dates"* — [the fact that this is offered as advice is itself evidence shops often cannot produce it](https://ogrehr.com/how-to-audit-your-written-practice-before-a-nadcap-visit).

**Time-window processes.** Hydrogen embrittlement relief bake is the sharpest: ASTM B633 requires parts at ≥1200 MPa be *"baked at 190 °C for 3 hours or more within 4 hours after electroplating"*; for aerospace hardened steels above ~HRC 36 the window drops to **30 minutes** ([Milt Stevenson Jr., finishing.com 145/37](https://www.finishing.com/145/37.shtml)). And the clock on the bake itself is disputed — James Watts: *"It is absolutely, positively when the parts reach temperature; since the amount of heater input, velocity of air movement and the mass of the load all contribute"* ([finishing.com 438/22](https://www.finishing.com/438/22.shtml)).

### 2.5 Outbound — the cert package

The commercial deliverable. There is **no industry-standard form**; every customer publishes its own field list.

| Customer | Required cert content (abridged) |
|---|---|
| [Northrop Grumman QAP01Q](https://cdn.northropgrumman.com/-/media/Supplier-Documents/Quality-Documents/Supplier_QAP01Q_101322/Revisions/Supplier_QAP01Q_63021.pdf?rev=9584f70e7f4f4d789c35f49e628ccafd) 01Q015 | PO number, part number, revision, serial/lot; applicable specification including *"revision, notice, amendment, type, grade, class, method"*; QM signature and title. 01Q016A heat treat: heat treat lot number + physical property test results. 01Q005A NDT: statement that certified personnel were used + NGC Level III technique approval |
| [Ducommun 38-4000 Rev U](https://www.ducommun.com/pdf/38-4000%20Quality%20Clauses%20-%20Carson%20(Rev.%20U).pdf) B7 | Processor name, PO number, **drawing number and revision**, **process spec number and latest revision**, quantity + serial/lot, authentication by supplier QA |
| [Collins Aerospace / Simmonds](https://www.rtx.com/collinsaerospace/-/media/CA/suppliers/hutc/simmonds-quality-clause-document.pdf?rev=b7f0c023d5034921ba0089e7fc7229d0&hash=6AEB25FFB355B4E5BB1DA90EF916013E) | Cl. 415: spec number **and revision**. Cl. 205: *"C of C must list all additional sub-tier C of C's and material certs with applicable identification numbers."* Cl. 469: hardness test actual results with each shipment |
| [Leonardo DRS SCM-004 Rev M](https://www.leonardodrs.com/wp-content/uploads/2023/06/scm-004-frm-common-quality-clauses_rev-m.pdf) QC210 | *"Process certifications are required for all special processes to be submitted to DRS with the delivered item … with the additional requirement of stating the process being certified"* |
| [Chandler Industries Rev N](https://www.chandlerindustries.com/wp-content/uploads/2026/02/Chandler_Supplier_Quality_Requirements_Rev_N.pdf) | Spec number + revision of all special processing; PO, P/N, rev letter, qty, **and Chandler's own work order number**; *"the order shall be processed and certified to latest revision of the specifications"* |
| [Ace Thermal Rev T](https://acethermalsystems.com/wp-content/uploads/2024/07/Quality-Clauses-Rev-T.pdf) Cl. 9 | *"a legible and reproducible copy of the detailed heat treatment cycle used"* with date, time, temperature and quench method; inspection reports must accompany |
| [Barnes Aerospace SQR-001](https://barnesaero.com/wp-content/uploads/2023/10/Supplier-Quality-Requirements_Lansing.pdf) | Adds a **"Document unique serial number"** to the cert |

Layered on top: DFARS specialty metals and country-of-origin declarations ([Stars & Stripes Q3](https://starsandstripesaerospace.com/documents/SSATermsConditionsQCodesRev2.pdf): *"The country of origin of the raw material must be declared on the certification"*), false-statement clauses ([Leonardo DRS QC362](https://www.leonardodrs.com/wp-content/uploads/2023/06/scm-004-frm-common-quality-clauses_rev-m.pdf)), and retention periods ranging **7 to 16 years** across the seven documents surveyed.

There is not even a stable name for the artifact. [Elsmar, "Documentation accompanying an aerospace part"](https://elsmar.com/elsmarqualityforum/threads/documentation-accompanying-an-aerospace-part.84250/): practitioners call it "the cert package," "the stack of paper," "the doc package," "shipping docs" — Mike S. notes *"there is no standardized term I know of,"* with packages running from one page to dozens.

### 2.6 How it is actually produced

Thin on hard published evidence, and the best number available is a vendor testimonial — flagged as such. Deborah James of Metalex Thermal Specialties, [quoted by Steelhead Technologies](https://gosteelhead.com/specifications-and-certifications): *"I used to fill those out in Word, which would take 20 to 30 minutes—now it's just one click."*

Structural corroboration is stronger. [IoT Analytics' 2025 MES study](https://iot-analytics.com/mes-vendors-replace-pen-paper-spreadsheets/) finds **54% of small and midsize plants use some combination of pen & paper or spreadsheets as their manufacturing execution system**, and only 8% use a commercial MES. A named plating case: Franke Plating Works (Fort Wayne, IN), 30 plating operators, ran on paper travelers with hand-calculated invoices — *"Before, we would print off a piece of paper and it would get lost"* ([case study](https://gosteelhead.com/plating-company-goes-paperless-shop-floor-software)). And QuickBooks is the de facto system of record for finishing shops, with [JobBOSS² explicitly marketed as the QuickBooks exit ramp for 10–100 employee shops](https://softwareconnect.com/reviews/jobboss-erp/).

Vendor capital confirms the diagnosis: Steelhead raised an [$84M growth investment from Mainsail Partners in December 2025](https://mainsailpartners.com/steelhead-technologies-announces-84m-growth-capital-investment/), with the announcement characterizing the target market as shops running on *"spreadsheets and paper travelers."*

### 2.7 The audit — where the handoff is graded

Nadcap audits do not primarily test procedures. They test **jobs**. AC7102 requires *["a total of one job audit, eight short jobs and two long jobs"](https://www.kacsik.com/blog/ac7102-checklist-review-part-1)*, and the shop must have **self-audited those same 10 jobs at least 30 days before the auditor arrives**. NDT requires three live witnessed job audits, tracing documentation *"from the purchase order, drawing, work instruction, travelers, specifications, procedures to the actual acceptance report"* ([Quality Magazine](https://www.qualitymag.com/articles/96140-nadcap-nondestructive-testing-special-process-audits-a-perspective)).

PRI's ranked most-common-NCR data for heat treat (May 2016–May 2017, [reproduced by Conrad Kacsik](https://www.kacsik.com/blog/the-most-common-ncrs)) shows what fails. For audits *with* job audits, the top ten include 14.3.4.2 (time parameter compliance), 1.1.1.1 (self-audit including all job audits), 14.6.2 (hardware treated in conformance), 14.2.1 (cycle parameters in job planning), 12.4.3 (time parameter compliance), 3.4.1 (previous corrective actions), 14.1.17 (cleaning requirement flow-down to job planning). **Half of the top ten are job-audit clauses — the shop's own paper on real parts, not its procedure manual.**

The 2021 top finding overall was para 1.1.4: failure to provide a completed self-audit *"including all 10 (ten) applicable job audits"* at least 30 days out ([Kacsik](https://www.kacsik.com/blog/blog/top-findings-nadcap-heat-treat-commodity-explained)).

---

## 3. Most important problems, ranked

### P1 — The cert is hand-assembled from data that already exists, in a format that differs per customer

**Who:** The quality manager (often the only signatory). **When:** Every shipment. **Frequency:** Daily to hourly.

**Currently handled** with per-customer Word or Excel templates, retyped from the traveler and the PO. The one specific number available — 20–30 minutes per cert in Word, from a named heat-treat practitioner — is a vendor testimonial and should be treated as directional.

**Why inadequate:** The cert is, structurally, a *projection of data the traveler already contains*. AC7108 3.3.1 forces the traveler to carry the PO number, the spec and revision, per-lot recorded parameters and dated buy-offs. The customer field lists (Northrop 01Q015, Ducommun B7) are a strict subset. Yet the projection is performed by a human retyping. Every retype is an opportunity to drop a revision letter, a class, or an amendment.

**Cost:** At 20 minutes per cert and 10 shipments/day, roughly **3.3 hours/day of the quality manager's time** — over 40% of the seat. Even at 5 minutes it is ~50 minutes/day. Plus the downstream cost of the errors it produces (P2).

**Evidence:** Verified — the customer field lists are published and mutually inconsistent (seven primary documents surveyed). Verified — AC7108 3.3.1 requires the source data on the traveler. Directional only — the 20–30 minute figure.

### P2 — Rejections and FAI failures caused by paperwork, not by product

**Who:** The shop, via its customer's receiving inspection or FAI reviewer. **When:** After the parts have already shipped and the job is closed.

**Evidence:** [GroundControl, "Top Five Reasons for an FAI Rejection"](https://gndctl.com/resources/top-five-reasons-for-an-fai-rejection/) states that **"most rejections stem from documentation errors rather than actual part nonconformance."** Its five causes are led by *"Incorrect or missing special process documentation"* — heat treat, plating, welding and NDT certs that *"lack proper supplier approvals or contain expired documentation and incorrect specification versions"* — and by **wrong revision level**, described as *"a primary failure point."*

**Why inadequate:** The hardware was conforming. The rework is entirely clerical, but it arrives days or weeks later, requires reopening a closed job, and lands on the same one person.

**Cost:** Beyond rework labor, primes rate suppliers on it. [Lockheed Martin's SCAR process](https://www.lockheedmartin.com/content/dam/lockheed-martin/aero/documents/scm/Quality-Requirements/Corrective-Action/supplier_CAP.pdf) states *"SCARs past the due date will negatively impact the supplier's quality rating."*

**Caveat, stated plainly:** No public source quantifies the paperwork-vs-product split in rejection rates. Four separate searches found none. GroundControl's qualitative "most rejections" is the strongest defensible claim available, and it is a consultant's assertion, not survey data. **This is the single most important thing to verify with practitioners before building.**

### P3 — Documentation defects get a *faster* corrective-action clock than product defects, and "human error" is a banned root cause

**Who:** The quality manager. **When:** Whenever a cert defect is caught downstream.

**Currently handled** by writing an 8D. Practitioner-reported windows from [Elsmar](https://elsmar.com/elsmarqualityforum/threads/number-of-days-to-respond-to-corrective-action-standard-response-time-frame.10086/) range 10 to 30 days generally — but one participant (Missileman) reports his organization uses *"7 calendar days for documentation problems and 10 calendar days for non-failure analysis and 20 calendar days for failure analysis."* **Documentation defects run on a separate, faster track.** [Barnes Aerospace](https://barnesaero.com/wp-content/uploads/2023/10/Supplier-Quality-Requirements_Lansing.pdf) issues SCARs for nonconformance in *"dimensions, appearance, or documentation"* — documentation listed co-equal with dimensions — with containment in 24 hours and an AS13000 8D in 30 days. Lockheed requires escape notification *"within 24 hours of suspect nonconforming product shipped regardless of destination"* and a **3-day** response for MRB dispositions.

**Why inadequate:** A [documented Elsmar case](https://elsmar.com/elsmarqualityforum/threads/how-can-i-respond-to-this-scar-supplier-corrective-action-request.67257/) shows the customer pre-banning the easy answers — forbidden root causes included *"Human error," "Procedures not followed," "Improper performance"*; forbidden corrective actions included *"Train a non-trained operator."* A shop that mistypes a spec revision cannot close the SCAR by saying "typo, retrained the clerk." It must produce a *systemic* answer in roughly one week.

**Inference worth stating:** automated cert generation is arguably the *only* corrective action that closes a transcription-defect SCAR under those constraints. No source says this; it follows from the cited constraints.

### P4 — The job audit demands instant reassembly of the full traceability chain for ten arbitrary historical jobs

**Who:** The quality manager, twice — once at self-audit (30 days out) and once live. **When:** Every 12–24 months per commodity.

**Currently handled** by pulling folders and binders and cross-referencing dates by hand.

**Why inadequate:** The chain spans systems that do not talk: PO (email/ERP) → contract review record (form) → traveler (paper) → in-process buy-offs (paper) → tank analysis logs or pyrometry records *covering that date* (separate binders) → outside-lab test report → the cert as issued (Word file, possibly overwritten). AC7108 4.2.1 requires records *"traceable to both shop travelers and certification/test report"* and sufficient to *"reconstruct the test samples or testing conditions."*

**Cost, and it is calculable.** Merit status governs audit frequency. Per [PRI OP 1111](https://www.kacsik.com/blog/benefits-challenges-nadcap-merit-process), 18-month merit requires **≤14 days cumulative delinquency** and no more than 50% of major / 60% of total NCRs allowed; 24-month merit requires **zero Major NCRs and ≤7 days cumulative delinquency.** Losing merit means an extra audit cycle. Published PRI onsite fees are **$4,420 (2-day) to $6,760 (5-day)** ([rate card](https://mpofcinci.com/blog/complete-nadcap-guide/)), plus 2–4 weeks of internal preparation labor. Small platers on the [finishing.com hotline](https://www.finishing.com/276/98.shtml) report initial audits at **$5,000–$8,000** and annual maintenance at **$4,150–$4,950**, with one shop stating it *"had to increase staffing just to support Nadcap."* One respondent's verdict: *"There has been absolutely no value added to our product. It has impacted our bottom line in a negative way."*

**Frequency of failure:** Suppliers averaged **four NCRs per initial audit 2018–2021, one of them Major**; Coatings and Materials Testing Laboratories averaged **~10 NCRs per initial audit in 2021** ([Products Finishing / PRI](https://www.pfonline.com/articles/how-to-avoid-the-common-pitfalls-of-a-nadcap-audit)). PRI's Ethan Akins on the leading cause: *"The most common reason for NCRs is not being fully prepared for the audit."*

### P5 — Spec revisions change without notification, and no one is watching

**Who:** The quality manager. **When:** Continuously and invisibly.

**Currently handled** by manual periodic portal polling — *"I am responsible to verify all 6 of our customers every 6 months."*

**Why inadequate:** [*"The customer has no PUSH system."*](https://elsmar.com/elsmarqualityforum/threads/whos-responsible-for-verification-of-customer-specifications.85345/) Meanwhile Chandler's clause CQR-3h says *"the order shall be processed and certified to latest revision of the specifications"* unless told otherwise — so a stale revision on a repeat order is a nonconformance the shop owns. AC7108 3.4.3 audits the repeat-order review procedure specifically.

**Cost:** Latent. Discovered at FAI review, receiving inspection, or a job audit — potentially covering months of shipped product.

### P6 — Recurring compliance clocks are state machines, not lists, and spreadsheets model them badly

**Who:** Quality manager / lab technician. **When:** Weekly through triennially, per instrument, per furnace, per tank, per technician.

**Why inadequate:** AMS2750G's thermocouple rule has a **dual trigger** (3 months OR five uses, whichever first, in a temperature band; single use above 1200 °F). SAT and TUS intervals vary by furnace class *and* instrumentation type *and* whether the shop has earned frequency reduction — and PRI's 2021 findings note shops misapplying the reduction rules (para 5.3.2), and applying correction factors *"in the test system but not the production system"* (para 5.4.1). AC7108 4.5.3 requires solution analysis frequency to **adjust based on rate of change** — a trending obligation a fixed weekly spreadsheet column does not satisfy on its face. NDT carries three independent clocks per technician plus per-technique annual Level III review.

**Cost:** [*"A disproportionate number of findings in audits surround pyrometry."*](https://www.kacsik.com/your-guide-for-how-to-pass-a-nadcap-audit) With a 7-day delinquency budget for 24-month merit, a single missed due date can cost an audit cycle.

**Honest caveat:** I could not find a published source stating that shops track these in spreadsheets. Valence comes closest, noting *"Manual process tracking (versus automated systems)"* increases *"the risk of drift going unnoticed"* ([source](https://www.valencesurfacetech.com/the-news/nadcap-plating-accreditation/)). The spreadsheet claim is a structural inference and needs practitioner validation.

### P7 — Customer approvals form a matrix the shop must reconcile itself, across systems it does not own

**Who:** Quality manager / sales. **When:** At order acceptance, and whenever anything expires.

The approval unit is not "we're Nadcap accredited." Boeing D1-4426 approves a numeric **Process Code** bound to a specific Boeing spec, optionally with **equipment limitation codes** — a real published listing shows *"Process Code 131 HT"* under spec *"BAC 5619,"* limited to *"Oven #1, 2, 4, 5, 6, 7, 11, 12, 13"* ([D1-4426 listing](https://dciaerotechcom.b-cdn.net/wp-content/uploads/2026/05/Boeing-D1-4426.pdf)). The same document warns: *"An acronym in the 'Nadcap Commodity' column only indicates that Nadcap accreditation may be required for this Process Code. It does not provide any indication of this company's actual Nadcap accreditation status."*

**Why inadequate:** The shop owns a five-dimensional reconciliation — customer × process code/spec × spec revision × equipment limitation × expiry — spread across the Boeing portal, eAuditNet's QML, Airbus/Rolls-Royce/GE portals, and its own quality manual. The prime explicitly does not do it for you. And the pre-audit package Nadcap demands 30 days out **includes "customer approvals"** — failure to submit it is AC7102 para 1.1.3, a perennial top-3 finding.

**Inference:** equipment limitation codes mean a furnace falling out of TUS compliance can silently invalidate a *specific customer's approval*. Not documented as having occurred; worth testing in interviews.

### P8 — Time-window processes are recorded as a single line when they need three timestamps

**Who:** Plating line lead + quality. **When:** Every hardened-steel plating lot.

**Currently handled** with an oven chart in a binder and a "bake: 375 °F / 3 hr" line — if anything — on the cert.

**Why inadequate:** The window can be **30 minutes** for aerospace hardened steels above HRC 36. Practitioners insist the bake clock starts when the *load center* reaches temperature, not the furnace: *"Baking times should start when the center of the furnace load reaches temperature"* (Matthew Horton); *"You need to embed some thermocouples within the loads in order to certify the baking process"* (Ken Vlach). A defensible record needs three timestamps: plating complete, oven in, load at temperature.

**Notable negative finding:** I searched seven published customer quality-clause documents for a clause requiring HE bake time/temperature on the outbound certificate. **None contained one.** The most safety-critical, most time-sensitive datum a plating shop generates is the one datum published customer paperwork requirements most consistently fail to demand on the face of the cert.

### P9 — "Where are my parts?" — no customer-facing status, so the phone is the interface

**Who:** Everyone in the office. **When:** Constantly.

Turnaround is short — a small plater publishes *"Typically, we can have your part ready within 5 to 7 business days"* ([Finishing Professionals](https://finishingpros.com/faqs/)) — and expedites are a marketed tier (Erie Plating offers [24–48 hour expedite](https://www.erieplatingcompany.com/fast-delivery), same-day on request), but neither publishes a status-lookup capability.

Steelhead's customer-portal page literally opens with *"Where are my parts? Are they done yet?"* and claims one customer saw an **80% reduction in phone calls**; a COO is quoted calling it *"the biggest game changer in Steelhead's platform"* ([source](https://gosteelhead.com/customer-portal-0)). That an 80%-call-reduction claim can headline a category ERP implies the baseline is **zero customer visibility.**

### P10 — Count and damage disputes are pre-managed by contract rather than by data

Shop terms of sale contractually cap exposure. [Metal Finishing Company's T&Cs](https://metalfinishingco.com/terms-and-conditions/): parts *"shall be presumed satisfactory unless we are notified of damages, shortages, or other discrepancies within 10 working days of receipt"*; *"The company assumes no liability for scrappage up to 3 percent"*; and liability is limited to direct labor and material damaged **"or three times our processing charges … whichever is lesser."** A plater who ruins a $4,000 machined part on a $60 plating operation is contractually liable for $180. Equivalent clauses appear at General Metal Finishing, Barry Avenue Plating, Plating Technology and others.

**Note:** I found no public, citable account of a specific split-lot or count-discrepancy dispute. The 3% scrappage allowance and the 10-day window are structural evidence that such disputes are routine enough to pre-manage, not direct testimony. Ranked last for that reason.

---

## 4. Application opportunities

### A1 — CertForge: per-customer certificate of conformance generator

**Intended user:** Quality manager at a 15–120 person plating, anodizing, coatings or heat treat shop.

**Problem solved (P1, P2, P3):** The cert is retyped by hand into a different template for every customer, and the most common downstream rejection is a wrong or missing spec coordinate.

**Current workflow:** Open the customer's Word template → read the traveler → retype PO number, part number, part revision, spec number, revision, type/class/grade/method, lot/serial, quantity, test results → print → sign → scan → file → email.

**Proposed workflow:** Select the job → the tool pulls the already-captured job record → selects the customer's field profile → validates that every required field for *that customer* is populated and that the spec coordinate is well-formed → assigns a unique sequential certificate number → renders a PDF → writes an immutable copy of the cert *as issued* to the retention archive.

**Inputs:** A job record (CSV/Excel export from the traveler system, or manual entry); a per-customer field profile (YAML/JSON, editable); a spec catalog (spec number → valid types/classes/grades, current revision, effective date).

**Outputs:** Signed-ready PDF cert; an immutable archive copy keyed by cert number; a per-shipment manifest listing sub-tier certs referenced (Collins clause 205).

**Essential features:** Per-customer field profiles shipped pre-built for the published clause sets surveyed here (Northrop, Ducommun, Collins, DRS, Chandler, Barnes). Spec coordinate validation with a hard block on missing revision. Unique cert serial numbering. DFARS/country-of-origin and false-statement blocks as toggles. Sub-tier cert manifest. Retention-clock metadata (7/10/12/15/16 years by customer).

**Excluded from v1:** Quoting, scheduling, invoicing, inventory, shop-floor data collection, EDI. This is not an ERP.

**AI:** Not needed for generation — this is templating and validation. **Optional** for one thing only: reading a *newly encountered* customer quality-clause PDF and proposing a draft field profile for human approval. That is genuine extraction work conventional code does badly. The generated cert itself must never be AI-authored.

**Why a spreadsheet won't do:** A spreadsheet can hold the data but cannot enforce per-customer required-field sets, cannot assign non-repeating serial numbers safely across users, cannot produce an immutable as-issued archive copy, and cannot validate that "MIL-A-8625 Type II Class 2" is a legal combination.

**Complexity:** Medium. **Learning:** Under an hour for the operator; a half-day to author the first customer profile. **Value:** If the 20-minute figure is even half right, 1–2 hours/day of the quality manager's time, plus the elimination of a rejection class.

**Risks:** The cert is a legal instrument carrying false-statement exposure ([18 U.S.C. § 1001](https://uscode.house.gov/view.xhtml?req=49&f=treesort&num=1262); DRS clause QC362). A tool that generates certs must be conservative: never infer a missing field, never auto-populate a revision, always require explicit human release. ITAR technical data may appear on drawings referenced by the job — see the deployment note below.

**Existing products:** Steelhead Technologies (cloud ERP, pricing unpublished, purpose-built for finishing, well capitalized), JobBOSS²/E2 ($200/user/mo), ProShop ERP ($500–$715/mo entry, on-premise option), Global Shop, Plex (~$500/user/mo, targets $11–50M revenue firms).

**Why still attractive:** Every incumbent requires the shop to *replace its system of record first*. ProShop implementation is quoted at **$20,000–$150,000+**; Plex at $100,000+ minimum. A 20-person plating shop at ~$3M revenue is being asked for 0.7–1.5% of revenue plus a 6–12 month implementation to solve a paperwork problem. A free tool that reads an Excel export and emits a correct cert is a **wedge, not a replacement** — and it can be adopted on a Tuesday.

**Paid customization:** High. Every shop has a different traveler format and a different customer list. "Build me profiles for my 14 customers and an importer for my traveler export" is a well-bounded engagement.

---

### A2 — Order Intake Reviewer: structured contract review record

**Intended user:** Quality manager or order-entry clerk.

**Problem solved (P5, P7, and AC7108 3.4.3 / AC7102 3.2.1.1):** PO review is done by reading, and misses are a named recurring Nadcap finding theme.

**Current workflow:** Read the PO and drawing, remember what this customer requires, start the job.

**Proposed workflow:** Enter or import the PO → the tool renders a mandatory checklist derived from the customer's clause set and the named spec → each item gets an explicit answer and initials → unresolved items block release to planning → the completed review is saved as a dated, signed record with a diff against the last order for the same part number.

**Inputs:** PO (PDF or manual entry), part number, named specs, customer profile.

**Outputs:** A signed contract review record (PDF); a "requirements delta vs. last order" report; a list of open questions to send back to the customer; the seed data for the traveler.

**Essential features:** The repeat-order diff (this is the whole point — AC7108 3.4.3). Customer approval status check with expiry. Spec revision currency check against the local spec catalog. Quality clause code expansion (turn "Q3, Q7, B28" into readable obligations). FAI trigger evaluation. Hard block on incomplete review.

**Excluded:** Quoting, pricing, scheduling.

**AI:** **Optional and valuable** — extracting part number, quantity, spec callouts and clause codes from a PDF PO is exactly the interpretation problem AI handles well and regex handles poorly. But every extracted field must be presented for human confirmation, never accepted silently.

**Why a spreadsheet won't do:** The diff-against-last-order is the core function and requires versioned history keyed on part number.

**Complexity:** Medium. **Learning:** ~1 hour. **Value:** Directly targets a top-10 Nadcap NCR clause and the highest-consequence latent error class.

**Risks:** If the tool's clause library drifts out of date it becomes a liability. Mitigate by making the clause library explicitly shop-owned and dated, never claiming currency the shop hasn't verified.

**Existing products:** None narrow. ERPs have "contract review" checkboxes; none produce the repeat-order diff.

**Paid customization:** Very high — clause library authoring per customer is the natural engagement.

---

### A3 — Job Audit Packet Assembler

**Intended user:** Quality manager preparing a self-audit or hosting an auditor.

**Problem solved (P4):** Ten arbitrary historical jobs must be fully reconstructable, twice, on demand.

**Current workflow:** Pull folders, cross-reference process dates against tank logs and pyrometry binders by hand, photocopy, staple, hope nothing is missing.

**Proposed workflow:** Enter a job/lot number → the tool assembles PO, contract review record, traveler with buy-offs, in-process records, **the tank analysis or pyrometry records whose validity window covers the process date/time**, outside-lab reports, and the cert as issued → outputs a single bookmarked PDF plus a **gap report** naming every missing or expired element.

**Inputs:** Job record, plus pointers to the record stores (folders, scans, CSV logs).

**Outputs:** Bookmarked traceability PDF per job; a gap report; a 10-job self-audit bundle.

**Essential features:** Date-window intersection (was this furnace in SAT compliance on the day this job ran?). The gap report is the product — the packet is the byproduct. Ability to run against *any* historical job, not just jobs created in the tool.

**Excluded:** Being the system of record. This tool *reads*; it does not own the data.

**AI:** Inappropriate for the assembly and intersection logic — that is date arithmetic and joins. Possibly useful to OCR scanned legacy records into an index, as a separate one-time utility.

**Why a spreadsheet won't do:** Temporal interval joins across five record types, plus PDF assembly.

**Complexity:** Medium. **Learning:** ~1 hour. **Value:** Highest per-event value in the catalog. Protects merit status (worth an audit cycle: $5–7k in fees plus 2–4 weeks of labor per cycle lost) and directly addresses the #1 published finding.

**Risks:** Depends on the shop having *some* machine-readable index of its records. Shops that are 100% paper get less value — which is also the honest scoping boundary.

**Existing products:** None found. ERPs store the records; none assemble an audit-trail packet with a gap report.

**Paid customization:** Very high — every shop's record layout differs.

---

### A4 — Pyrometry Clock (AMS2750 due-date engine)

**Intended user:** Heat treat quality manager or pyrometry technician.

**Problem solved (P6):** SAT/TUS/instrument/thermocouple due dates form a state machine with dual triggers and a non-obvious month-end rounding rule.

**Current workflow:** A spreadsheet with a due-date column, maintained by hand.

**Proposed workflow:** Register furnaces (class, instrumentation type, qualified operating ranges) and instruments → record each SAT, TUS, calibration and thermocouple use → the engine computes next-due dates per AMS2750 Tables 7, 11/12, 15/16, applies clause 2.2.25 month-end rounding, tracks thermocouple dual triggers, and flags any furnace whose next-due date has passed as **not releasable to production**.

**Inputs:** Furnace/instrument register; test events; thermocouple usage log.

**Outputs:** A due-date board; per-furnace release status; an exportable pyrometry compliance record for the pre-audit package; a "frequency reduction eligibility" indicator with the explicit note that the initial TUS does not count toward consecutive tests.

**Essential features:** The rounding rule. The dual trigger. Per-range SAT (multiple qualified operating ranges require SAT in each at least annually). Correction-factor storage with an explicit extrapolation block (clause 3.1.4.7). Lockout-furnace re-SAT-before-return-to-service flag.

**Excluded:** Actually performing the TUS, instrument drivers, chart digitization.

**AI:** Inappropriate. This is deterministic table lookup and date arithmetic, and getting it wrong is a compliance failure. Ordinary code, with the tables as reviewable data files.

**Why a spreadsheet won't do:** Spreadsheets can hold dates but reliably get the month-end rounding rule and the OR-triggers wrong, and cannot express per-class/per-instrumentation-type table selection without becoming unmaintainable.

**Complexity:** Medium (the tables are the work). **Learning:** ~1 hour. **Value:** Merit protection; addresses a named "disproportionate" share of findings.

**Risks:** **Serious and specific — AMS2750 is copyrighted SAE material.** The tool must ship with *empty* interval tables and require the shop to enter its own values from its licensed copy, or ship only user-authored table files. Do not redistribute the tables. This constraint should be designed in from day one, not bolted on.

**Existing products:** Commercial furnace-validation software exists (e.g. Fluke Calibration TQAERO), typically bundled with instrumentation. Nothing free and standalone found.

**Paid customization:** Moderate — per-shop furnace registers and integration with chart recorder exports.

---

### A5 — Approval Matrix Tracker

**Intended user:** Quality manager, sales.

**Problem solved (P7):** Customer × spec × revision × equipment limitation × expiry, reconciled by hand across portals the shop doesn't control.

**Current workflow:** A folder of approval letters and a memory.

**Proposed workflow:** Register each approval as a structured record (customer, process code, specification, revision scope, equipment limitations, granting document, effective date, expiry) → at order intake, query it → get a green/amber/red with the specific reason → run a scheduled review that lists approvals expiring in 90/60/30 days and every customer portal due for a polling check.

**Inputs:** Approval letters/certificates (PDF attachments), Nadcap scope certificates, manual entry.

**Outputs:** Order-time approval verdict; expiry calendar; **the "customer approvals" section of the Nadcap 30-day pre-audit package** (AC7102 1.1.3, a perennial top-3 finding) as a formatted export.

**Essential features:** Equipment limitation modeling (Oven #1, 2, 4…) so a furnace out of compliance can be cross-referenced against affected customer approvals. Portal polling checklist with last-checked dates. Evidence attachment.

**Excluded:** Scraping customer portals. Automated scraping of Boeing/Exostar/eAuditNet is fragile, likely against terms of use, and would poison the product. Poll manually; the tool tracks that you did.

**AI:** Inappropriate for the tracking. Marginal for reading an approval letter into structured fields.

**Why a spreadsheet won't do:** It could, badly — this is the weakest "spreadsheet insufficient" argument in the set. The real differentiators are the equipment-limitation cross-reference, the attached evidence, and the pre-audit export.

**Complexity:** Small. **Learning:** ~30 minutes. **Value:** Moderate but recurring; prevents the specific "processed on an unapproved source" escape.

**Risks:** Stale data is worse than no data. The tool must surface last-verified dates prominently.

---

### A6 — Solution Control Log with rate-of-change frequency

**Intended user:** Plating lab technician / quality manager at a chemical processing shop.

**Problem solved (P6, and AC7108 4.5.3 / 4.5.4 / 4.5.6 / 4.5.7d):** Tank analysis records must carry a specific field set, the analysis frequency must *adjust based on rate of change*, and processing must demonstrably stop when a constituent is out of tolerance.

**Current workflow:** A paper log book or a spreadsheet per tank, with a fixed frequency.

**Proposed workflow:** Define tanks (ID, contents, working volume, constituents, tolerance sets per applicable specification) → log each analysis with all AC7108 4.5.4 fields → the tool trends each constituent, recommends a frequency increase or decrease with the supporting data, flags out-of-tolerance immediately, and **lists every job that ran through that tank between the last in-tolerance result and the failure** as the impact-assessment scope.

**Inputs:** Analysis results (manual entry or CSV from titration equipment), tank definitions, job/tank associations.

**Outputs:** AC7108-compliant tank record; trend charts; frequency recommendation with justification; out-of-tolerance impact list.

**Essential features:** The 4.5.4 field set enforced. Multiple tolerance sets per tank (a tank serving three specs has three overlapping windows — "operating tolerances based on, multiple where applicable, specification requirements"). The impact list. Additions/corrections/dumps as first-class events.

**Excluded:** Automated dosing control, chemical inventory, wastewater reporting.

**AI:** Inappropriate. Trending and threshold logic.

**Why a spreadsheet won't do:** The rate-of-change frequency adjustment and the retroactive impact list both require relational structure. A fixed weekly column arguably does not satisfy 4.5.3 on its face.

**Complexity:** Medium. **Learning:** ~1 hour. **Value:** Addresses the clause that converts a lab miss into a shipped-product recall.

**Risks:** Wrong tolerance data is a safety issue. Ship empty; require the shop to enter its own values from its own specs and supplier datasheets.

---

### A7 — Bake Clock (hydrogen embrittlement relief timer and record)

**Intended user:** Plating line lead; quality manager.

**Problem solved (P8):** A 30-minute-to-4-hour window with three meaningful timestamps, currently recorded as one line.

**Current workflow:** Oven chart in a binder; a "375 °F / 3 hr" line on the cert, or nothing.

**Proposed workflow:** At plating completion, scan or enter the lot → the tool starts the window and shows a live countdown against the applicable limit (30 min / 4 hr, per the spec on the job) → record oven-in → record load-at-temperature (thermocouple-confirmed) → the tool computes soak duration from at-temperature, not oven-in, and emits a **bake record block** that A1 can print on the face of the cert.

**Inputs:** Lot ID, applicable spec/window, three timestamps, setpoint, chart reference.

**Outputs:** A bake record; a printable cert block with all three timestamps; an exception log of windows missed.

**Essential features:** The countdown (this is the operational value — it prevents the miss rather than documenting it). Per-spec window selection. The three-timestamp record.

**Excluded:** Furnace control, chart digitization.

**AI:** Inappropriate. A timer and a form.

**Why a spreadsheet won't do:** A spreadsheet cannot count down on a shop floor.

**Complexity:** Small. **Learning:** 15 minutes. **Value:** Prevents the highest-consequence, lowest-visibility failure a plating shop can commit, and creates a differentiating cert.

**Risks:** Must not be presented as certifying embrittlement relief adequacy — it records timing, nothing more. Fastener and aerospace embrittlement failures carry real liability; the tool's framing must be scrupulously narrow.

**Existing products:** None found. This gap is real: **no surveyed customer quality clause requires bake timestamps on the cert**, so no ERP prioritizes it.

---

### A8 — NDT Currency Board

**Intended user:** NDT Level III or quality manager at an NDT service provider or an in-house NDT function.

**Problem solved (P6):** Three independent clocks per technician (5-year cert, annual vision, annual practical) plus per-technique annual Level III review, and an auditor who will ask for the list.

**Current workflow:** A spreadsheet and a folder of vision exam forms.

**Proposed workflow:** Register technicians (method, level, cert date, vision date, practical date) and techniques (approval date, last Level III review) → the board shows currency at a glance → assigning an expired technician to a job raises a block → export the auditor's list on demand.

**Inputs:** Personnel records, exam records, technique sheet register.

**Outputs:** Currency board; expiry calendar; the auditor-ready personnel list with cert expiration and vision due dates; a written-practice-to-NAS-410 cross-reference worksheet.

**Essential features:** Three clocks, not one. Method-level granularity. The cross-reference worksheet matters because NAS 410 minimums *exceed* SNT-TC-1A (e.g. PT Level II: 32 hours formal training and 400 OJT hours vs. ASNT's 12 and 210) — a written practice derived from SNT-TC-1A will not pass.

**Excluded:** Training content, exam delivery, scheduling.

**AI:** Inappropriate.

**Why a spreadsheet won't do:** It nearly could. The differentiators are the assignment block and the pre-built NAS 410 cross-reference.

**Complexity:** Small. **Learning:** 30 minutes. **Value:** Moderate. Prevents the "test results invalid because the technician's cert had lapsed" scenario, which forces retest or recall.

---

### A9 — Escape and Corrective Action Clock

**Intended user:** Quality manager.

**Problem solved (P3):** Every customer has different notification and response deadlines, documentation defects often run a faster track, and delinquency days are counted against merit.

**Current workflow:** Email and memory.

**Proposed workflow:** Log an escape or SCAR → the tool applies that customer's clocks (24-hour escape notification, 3-day MRB, 7-day documentation, 30-day 8D) → produces a countdown and a pre-populated 8D skeleton seeded with the traceability chain from A3 → tracks cumulative delinquency days against the merit budget (14 days for 18-month, 7 for 24-month).

**Inputs:** Customer clause profile (shared with A1/A2), escape details, job reference.

**Outputs:** Notification deadline board; 8D document skeleton; a cumulative delinquency-days meter.

**Essential features:** Per-customer clock profiles. The delinquency meter — this converts an abstract compliance obligation into a visible budget. An 8D template that refuses to accept "human error" as a root cause, mirroring what customers actually reject.

**Excluded:** Being a full CAPA system.

**AI:** **Optional.** Drafting a first-pass 8D narrative from structured facts is real drafting assistance. The root cause must be human-authored; a generated root cause is exactly what customers ban.

**Complexity:** Small-to-medium. **Learning:** ~1 hour. **Value:** Moderate. Lower frequency than A1/A2 but high consequence.

---

### A10 — Customer Lot Status Page

**Intended user:** The shop's customer (a machine shop buyer or expediter); operated by the shop.

**Problem solved (P9):** "Where are my parts?" phone calls, and re-sending documents.

**Current workflow:** Phone and email.

**Proposed workflow:** The shop publishes a generated, read-only status page per customer showing open lots, current operation, promise date, and download links for the packing slip and cert once released. Regenerated on each traveler update.

**Inputs:** Job records; released cert PDFs from A1.

**Outputs:** A static per-customer HTML page or a single-token link.

**Essential features:** Read-only. Per-customer scoping with an unguessable token. Document self-service — this is where most of the value is, not the status.

**Excluded:** Chat, ordering, accounts, notifications, any two-way interaction.

**AI:** Inappropriate.

**Why a spreadsheet won't do:** Distribution, not computation, is the problem.

**Complexity:** Small. **Learning:** trivial. **Value:** The 80%-call-reduction claim is vendor marketing and should be discounted, but the underlying baseline (zero visibility) is well supported.

**Risks — the largest in the catalog.** Part numbers and program names are frequently **export-controlled technical data or customer-confidential**. A publicly reachable status page is a disclosure hazard. This must be designed as authenticated-by-default, and the honest recommendation is to ship it *last*, after the shop trusts the rest of the toolkit. Ranked accordingly.

---

### A deployment note that applies to all ten

These shops are defense-supply-chain participants. ITAR's [March 2020 encryption carve-out](https://sanctionsnews.bakermckenzie.com/ddtc-issues-itar-rule-affecting-technology-transfers-encryption-and-cloud-computing/) permits cloud storage of technical data only if it remains end-to-end encrypted with FIPS 140-2 (or ≥AES-128-equivalent) modules and never rests in §126.1 embargoed countries or Russia — tokenization does not qualify. CMMC Phase II was **suspended by DoD on 2026-07-13** ([SBA statement](https://legacy.sba.gov/article/2026/07/13/sba-commends-us-department-wars-suspension-cmmc-phase-ii-small-defense-contractors)), which relieves near-term certification pressure but does not change customer flow-downs already in contracts.

**Practical consequence: every tool in this catalog should run local-first — a single-file SQLite database, or plain files in a folder the shop already backs up — with no mandatory cloud component.** This is not a limitation; it is the primary differentiator against Steelhead (cloud-only SaaS) and a match for why ProShop sells an on-premise option "for full control over data and regulatory compliance." Local-first is also what makes a free open-source base version credible to a quality manager who cannot get IT approval for a SaaS account.

---

## 5. Opportunity ranking

Scored 1–5 on each dimension; 50 maximum.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of impl. | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| A1 | CertForge — cert generator | 5 | 5 | 5 | 4 | 4 | 4 | 3 | 5 | 5 | 5 | **45** |
| A2 | Order Intake Reviewer | 5 | 5 | 4 | 4 | 4 | 4 | 4 | 5 | 4 | 5 | **44** |
| A3 | Job Audit Packet Assembler | 5 | 3 | 5 | 4 | 3 | 4 | 5 | 5 | 4 | 5 | **43** |
| A4 | Pyrometry Clock (AMS2750) | 5 | 4 | 4 | 4 | 3 | 5 | 4 | 4 | 4 | 5 | **42** |
| A7 | Bake Clock (HE relief) | 5 | 4 | 3 | 5 | 5 | 5 | 4 | 3 | 4 | 4 | **42** |
| A5 | Approval Matrix Tracker | 4 | 3 | 4 | 5 | 4 | 5 | 4 | 4 | 3 | 4 | **40** |
| A6 | Solution Control Log | 4 | 5 | 4 | 4 | 3 | 4 | 3 | 4 | 4 | 5 | **40** |
| A8 | NDT Currency Board | 4 | 3 | 3 | 5 | 5 | 5 | 3 | 3 | 4 | 5 | **40** |
| A9 | Escape / CA Clock | 4 | 3 | 3 | 4 | 4 | 4 | 3 | 4 | 3 | 4 | **36** |
| A10 | Customer Lot Status Page | 3 | 5 | 3 | 5 | 4 | 3 | 2 | 4 | 3 | 4 | **36** |

### The top three

**A1 — CertForge (45).** The cert is the product. It is produced daily, by hand, from data that already exists in a structured form the audit standard *requires* the shop to have captured, into a format that differs per customer. That gap — structured source, structured target, human retyping in between — is the cleanest software opportunity in the market. It scores lowest on differentiation (3) because Steelhead does this well and is now capitalized to do it aggressively. But Steelhead requires the shop to replace its system of record; CertForge requires an Excel export. Those are different products sold to different moments in a shop's life.

**A2 — Order Intake Reviewer (44).** Highest leverage on *latent* error. A bad cert is caught in weeks; a stale spec revision accepted at order intake ships for months. It targets a specifically named Nadcap clause (AC7108 3.4.3, AC7102 3.2.1.1) and PRI's own multi-year finding theme. The repeat-order diff is the feature nothing else has. It shares the customer profile data model with A1, so building A1 first makes A2 substantially cheaper.

**A3 — Job Audit Packet Assembler (43).** Highest differentiation (5) and highest per-event value in the catalog, but frequency is low (3) — twice per audit cycle. It is the concept most likely to be *loved* and least likely to be used weekly. The gap report is what makes it more than a PDF stapler, and its temporal-interval logic is genuinely hard to replicate in a spreadsheet.

### What to investigate next

**Build A1 first.** It has the highest score, the shortest path to a demo, the best available test data (published cert field lists from seven primes plus real Nadcap traveler requirements), and it establishes the customer-profile data model that A2, A9 and A10 all reuse. A working prototype is a per-customer YAML profile, a job record CSV, and a PDF renderer — a weekend, not a quarter.

**But validate P2 before building anything.** The economic case for A1 rests on "most rejections stem from documentation errors," which is a single consultant's unquantified assertion. If practitioners say paperwork rejections are rare, A1's ROI story collapses to time savings alone — still real, but much weaker, and it would promote A2 and A3 above it.

**A7 (Bake Clock) is the sleeper.** Tied for fourth at 42, it is the easiest to build (5), the fastest to learn (5), the most narrowly scoped (5), and it addresses a gap I could verify *no customer quality clause currently demands* — which means no ERP has bothered. It is a strong candidate for a first shipped artifact precisely because it is small enough to finish, and it would open the door to A1 at the same shops.

---

## 6. Validation plan

### Questions to ask practitioners

**On the cert (A1):**
1. Walk me through producing one cert, start to finish. What do you open, in what order, and what do you type by hand?
2. How many different cert templates do you maintain? Have any customers rejected a cert for a formatting or content reason in the last year?
3. When a customer rejects paperwork, what actually happens — email, formal SCAR, or a rating hit? How long did the last one take to close?
4. Roughly what fraction of your returns and rejections are paperwork versus product? **(This is the critical question. Ask it neutrally, and ask it of receiving-side supplier quality engineers too.)**
5. Do you keep a copy of the cert exactly as issued, or do you regenerate it from the template?

**On intake (A2):**
6. When a repeat PO arrives for a part you ran last year, what do you check?
7. How do you find out a customer's spec revision changed? Who told you last time, and how late was it?
8. Have you ever processed to a superseded revision? What did it cost?

**On the audit (A3, A4, A5):**
9. How long did preparing your last self-audit's ten job packets take, in hours?
10. What was your last audit's NCR count, and were any of them records-completeness rather than process findings?
11. Are you on 12, 18 or 24-month merit? Have you ever lost merit, and why?
12. Show me how you track SAT/TUS/thermocouple due dates today. (Ask to *see* it — this is where the spreadsheet inference gets confirmed or killed.)

**On the bake (A7):**
13. What do you record for a relief bake, and where does it live? Does anything print on the cert?
14. Has a customer ever asked you to prove the bake window was met? Could you have?

### Who to interview

- Quality managers at 20–80 employee independent plating and heat treat shops. NASF chapter meetings and MTI chapter rosters ([MTI trustee-eligible list](http://docs.heattreat.net/MTITrusteeEligible.pdf), ~200 companies with chapter geography) are the most efficient sampling frames.
- **The receiving side** — supplier quality engineers at 50–500 person machine shops and Tier 2 suppliers. They see the rejection rate from the other end and will answer question 4 without defensiveness.
- Nadcap consultants (Conrad Kacsik, AQM Auditing and similar) — they have seen dozens of shops' record systems and can characterize the incumbent tooling in one conversation.
- A former PRI staff engineer or Nadcap auditor, for the NCR-classification question (Major vs. Minor for contract-review misses) that public sources do not answer.
- The hiring manager for the Heartland Precision Fasteners posting — the job description reads like a requirements document, and the $15–25k/month cost-of-poor-quality figure came from somewhere.

### Search terms for further research

`AC7108 revision I clause`; `AC7102 job audit self audit ten jobs`; `"most common NCRs" Nadcap coatings AC7109`; `AC7114 NDT checklist`; `supplier quality requirements filetype:pdf "certificate of conformance" "special process"`; `"process per print" plating specification missing`; `AS9102 Rev C section 1.3 special process supplier`; `NASF chapter meeting minutes`; `Products Finishing Top Shops benchmarking ERP`; `heat treat "job planning" traveler template`. Also: pull the AC7108/AC7102/AC7109/AC7114 checklists directly from **eAuditNet → Resources → Documents → Audit Criteria**, which is free without accreditation.

### Sample files and data needed

- Three to five real (redacted) certificates of conformance from different shops for different customers — the core artifact.
- Two real shop travelers, one plating and one heat treat, ideally the "12-page" modern kind.
- One real customer PO with quality clause codes, plus that customer's clause document.
- One tank analysis log book page and one pyrometry SAT/TUS record set.
- A self-audit job packet, if any shop will part with one.
- Redaction will be a live issue: part numbers and program names are frequently export-controlled. Expect to work from synthetic data modeled on real structure.

### The prototype that would validate the idea

**Two days of work, one screen.** A folder containing: a `job.csv` with one row; three `customer-*.yaml` field profiles authored from the Northrop, Ducommun and Collins clause documents cited above; and a Python script that emits three visibly different, correctly populated PDF certs from the same job row — plus a fourth run that *fails loudly* because the spec revision is blank.

Put that in front of five quality managers. The question is not "would you use this" but "is this cert acceptable to your customer as-is, and what's missing." If three of five can name the missing field, the data model is close and the field-profile approach works. If they can't agree on what's missing, the per-customer-profile hypothesis is wrong and the tool needs to be a form builder instead.

### Assumptions most likely to make it fail

1. **That paperwork rejections are frequent and expensive.** Single unquantified source. If wrong, A1 is a time-saver, not a risk-reducer, and the pitch weakens substantially.
2. **That the source data is machine-readable.** If most shops' travelers are genuinely paper, A1 requires data entry the shop is already doing elsewhere, and the net saving shrinks. The addressable segment may be the 30–120 employee shops that already have *something* — QuickBooks plus Excel — rather than the sub-20 shops.
3. **That the quality manager can adopt software without IT approval.** Local-first design assumes a Windows desktop and a folder. If shops are locked down, distribution is harder than the build.
4. **That Steelhead doesn't commoditize the wedge.** With $84M and 17% annual customer growth, a free cert generator is a feature they could bundle. The durable defense is local-first, no-account, no-migration — a posture a funded SaaS company structurally will not adopt.
5. **That shops will accept a free tool for a legally consequential document.** Certs carry false-statement exposure. Some quality managers will refuse anything they cannot audit. Open source is the answer to that objection, but it has to be argued explicitly, and the tool must never infer a field.
6. **That the market is big enough.** ~6,000 US finishing and heat treat establishments, ~90% under 50 employees, and the plating base **shrank 2.5% in 2024**. This is a small, contracting, and price-sensitive market. It is well suited to a free open-source base with paid customization; it is not suited to a venture-scale SaaS.

---

## 7. Cross-industry patterns

Seven patterns from this market, each with named backlog markets they transfer to.

**1. Compound-key validation (spec + revision + type/class/grade/method).** The recurring failure here is not a wrong number but an *incomplete coordinate*. A validator that knows which sub-fields a given standard requires, and refuses to emit a document with any of them blank, is portable wherever practitioners cite standards in deliverables.
→ *Independent specification writers and master-spec maintenance consultants; Energy code compliance consultants and Title 24 documentation shops; Welding inspection (AWS CWI) and NDT service providers under ASTM E543 / SNT-TC-1A; Fire alarm ITM under NFPA 72; Environmental laboratories producing regulator EDD deliverables.*

**2. One source record, N recipient-specific output formats.** The shop produces one job; every customer wants a different document from it. The general tool is a per-recipient field-profile renderer with required-field enforcement.
→ *Environmental laboratories producing regulator EDD deliverables (EQuIS and state formats); Payroll service bureaus; Information-return filing services and B-notice remediation providers; Mortgage post-closing QC and trailing document vendors; Freight bill audit and payment for small shippers.*

**3. Recurring-obligation state machines with dual triggers and non-obvious rounding.** AMS2750's "3 months OR five uses, whichever first" plus month-end rounding is a general shape: obligations that fire on elapsed time OR usage count, per asset, per class.
→ *Calibration and metrology service providers / in-house gage management; Third-party equipment calibration providers serving construction test labs; Backflow prevention assembly testers and cross-connection control programs; Fire door inspection providers under NFPA 80; Portable fire extinguisher and kitchen hood suppression service routes; Radiation safety officer services and portable gauge licensee compliance.*

**4. Evidence-packet assembly for an audit that samples random historical work.** The auditor picks ten jobs; you reassemble the chain. Any regime that audits by sampling historical files has this shape, and the gap report is the valuable half.
→ *C3PAO assessment operations and evidence sampling; FedRAMP 3PAO assessment and body-of-evidence production; Special inspection agency accreditation consultants (IAS AC291, ANAB, WABO); DCAA-audit-ready incurred cost and indirect rate submissions; Workforce development boards and WIOA subrecipients.*

**5. Time-window compliance with multiple meaningful timestamps.** The HE bake window needs three timestamps, not one, and the operationally valuable artifact is the live countdown, not the after-the-fact record.
→ *Ready-mix concrete producer quality control departments (discharge time limits); Environmental laboratories (sample hold times); Asphalt plant producer quality control technicians; Home care and home health agency scheduling and EVV back office.*

**6. Out-of-tolerance blast-radius calculation.** When a controlled parameter is found out of spec, the question is always "what shipped between the last good reading and this one." Trivial with a relational log, near-impossible with a paper binder.
→ *Third-party equipment calibration providers serving construction test labs; Environmental laboratories producing regulator EDD deliverables; Ready-mix concrete producer quality control departments; Asphalt plant producer quality control technicians; Calibration and metrology service providers.*

**7. Counterparty obligation register — N customers, N different clocks and field lists.** No standard exists; each counterparty publishes its own requirements, and the small party owns reconciliation across systems it does not control.
→ *Prime contractor supplier cyber-compliance desks (supplier attestation collection); Certificate-of-insurance compliance from the holder side; Supplier quality engineering at OEMs and primes; Delegated-design submittal coordination; Equipment manufacturer and manufacturer-rep submittal desks.*

**A cross-cutting deployment pattern worth recording separately:** in defense-adjacent markets, **local-first architecture is a feature, not a compromise.** ITAR and CUI handling constraints make cloud SaaS a hard sell to a shop that cannot verify data residency, and this is precisely what a free, self-hosted, single-file-database tool does better than a funded SaaS competitor. This applies to every defense-supply-chain market in the backlog.

---

## 8. Sources and confidence

### Verified findings (directly stated in the cited source)

**Market structure**
- Establishment, employment and size-class counts computed from BLS QCEW 2024 open-data files: [332811](https://data.bls.gov/cew/data/api/2024/a/industry/332811.csv), [332812](https://data.bls.gov/cew/data/api/2024/a/industry/332812.csv), [332813](https://data.bls.gov/cew/data/api/2024/a/industry/332813.csv), [541380](https://data.bls.gov/cew/data/api/2024/a/industry/541380.csv); [QCEW program](https://www.bls.gov/cew/)
- [NASF 2022 Economic Impact Report summary](https://finishingandcoating.com/index.php/plating/1125-nasf-report-says-u-s-industry-is-over-2-600-shops-11-billion-in-output) — 2,600+ shops, $10.7B, 71,000 employees, 68% under 20 people
- [The Monty, 52 Largest North American Commercial Heat Treaters 2025](https://themonty.com/52-largest-north-american-commercial-heat-treaters-2025/) — ~530 plants, ~$3B
- [Valence / Foresight Finishing acquisition](https://www.valencesurfacetech.com/press-release-for-foresight-finishing-press-release/); [Aalberts acquires Paulo](https://www.heattreattoday.com/aalberts-acquires-paulo-expands-heat-treat-reach-in-n-a/)
- [Heartland Precision Fasteners quality manager posting](https://to.indeed.com/aaqvgttcwxsg); [Durable Industrial Finishing posting](https://to.indeed.com/aanplhlfxk8w)

**Audit and standards requirements**
- [Nadcap AC7108 Rev E, Chemical Processing audit criteria](https://www.galvanizeit.com/uploads/resources/AC7108-Rev-E.pdf) — clauses 1.2, 3.3.1, 3.4.3, 3.5.2, 3.8.1, 4.1.2.1, 4.2.1, 4.4.3, 4.5.3, 4.5.4, 4.5.6, 4.5.7
- [Conrad Kacsik, "The Most Common NCRs"](https://www.kacsik.com/blog/the-most-common-ncrs) — PRI's ranked heat treat NCR clause lists
- [Kacsik, Top Findings Nadcap Heat Treat Commodity](https://www.kacsik.com/blog/blog/top-findings-nadcap-heat-treat-commodity-explained); [AC7102 checklist review](https://www.kacsik.com/blog/ac7102-checklist-review-part-1); [How to pass a Nadcap audit](https://www.kacsik.com/your-guide-for-how-to-pass-a-nadcap-audit); [Merit process](https://www.kacsik.com/blog/benefits-challenges-nadcap-merit-process)
- [Products Finishing, "How to Avoid the Common Pitfalls of a Nadcap Audit"](https://www.pfonline.com/articles/how-to-avoid-the-common-pitfalls-of-a-nadcap-audit) — 4 NCRs/initial audit; Coatings and MTL ~10 in 2021; PRI's Ethan Akins on preparation and PO review
- [Quality Magazine, Nadcap NDT audits](https://www.qualitymag.com/articles/96140-nadcap-nondestructive-testing-special-process-audits-a-perspective) — three witnessed job audits; top-5 NCRs on self-audit, calibration flow-down, procedures
- [PRI Nadcap getting started](https://www.p-r-i.org/nadcap/getting-started); [PRI FAQ](https://www.p-r-i.org/resources/frequently-asked-questions) — 50-day average accreditation lag
- AMS2750G clause and table text (calibration intervals Table 7; SAT Tables 11–12; TUS Tables 15–16; thermocouple limits 3.1.7.3; extrapolation 3.1.4.7; interpolation 3.1.4.8; month-end rounding 2.2.25) — [full-text PDF](https://pic01.sq.seqill.cn/uploads/1012/16655654646.pdf); [AMS2750F changes, Heat Treat Today](https://www.heattreattoday.com/equipment/heat-treating-accessories/thermocouples/thermocouples-technical-content/ams2750f-changes-and-implementation/); [AMS2750G vs H, Kacsik](https://www.kacsik.com/blog/key-changes-ams2750g-vs-ams2750h-pyrometry-requirements)
- [NAS 410 requirements summary](https://ndttrainingonline.com/nas-410-ndt-certification-requirements/); [written practice pre-audit checklist](https://ogrehr.com/how-to-audit-your-written-practice-before-a-nadcap-visit)

**Customer flow-down documents (primary)**
- [Northrop Grumman QAP01Q](https://cdn.northropgrumman.com/-/media/Supplier-Documents/Quality-Documents/Supplier_QAP01Q_101322/Revisions/Supplier_QAP01Q_63021.pdf?rev=9584f70e7f4f4d789c35f49e628ccafd) · [NGC EQI-011](https://cdn.northropgrumman.com/-/media/Supplier-Documents/Quality-Documents/EQI-011.pdf) · [Net-Inspect mandate](https://cdn.northropgrumman.com/-/media/Supplier-Documents/Announcements/2024_NetInspectRequiredFAIRSubmissionsApprovals.pdf)
- [Ducommun 38-4000 Rev U](https://www.ducommun.com/pdf/38-4000%20Quality%20Clauses%20-%20Carson%20(Rev.%20U).pdf) · [Leonardo DRS SCM-004 Rev M](https://www.leonardodrs.com/wp-content/uploads/2023/06/scm-004-frm-common-quality-clauses_rev-m.pdf) · [Collins/Simmonds clauses](https://www.rtx.com/collinsaerospace/-/media/CA/suppliers/hutc/simmonds-quality-clause-document.pdf?rev=b7f0c023d5034921ba0089e7fc7229d0&hash=6AEB25FFB355B4E5BB1DA90EF916013E) · [Chandler Rev N](https://www.chandlerindustries.com/wp-content/uploads/2026/02/Chandler_Supplier_Quality_Requirements_Rev_N.pdf) · [Barnes SQR-001](https://barnesaero.com/wp-content/uploads/2023/10/Supplier-Quality-Requirements_Lansing.pdf) · [Ace Thermal Rev T](https://acethermalsystems.com/wp-content/uploads/2024/07/Quality-Clauses-Rev-T.pdf) · [Bowman Plating Attachment Q](https://bowmanplating.com/QualityClauses.pdf) · [Stars & Stripes Q-codes](https://starsandstripesaerospace.com/documents/SSATermsConditionsQCodesRev2.pdf) · [SEPAC](https://sepac.com/information/quality-clauses) · [Advance Mfg SOF-005](https://www.advancemfg.com/downloads/SOF-005-N-Supplier-Purchase-Order-Requirements-20250523.pdf)
- [Boeing D1-4426 Appendix D](https://www.stackmet.com/wp-content/uploads/2018/12/d14426-appendix-d-complete.pdf) · [Boeing D1-4426 portal](https://active.boeing.com/doingbiz/d14426/index.cfm) · [published D1-4426 listing with process codes and oven limitations](https://dciaerotechcom.b-cdn.net/wp-content/uploads/2026/05/Boeing-D1-4426.pdf) · [Boeing Nadcap FAQ](https://www.boeingsuppliers.com/become/terms/nadcap-faq)
- [Lockheed Martin RMS/Sikorsky QCS](https://www.lockheedmartin.com/content/dam/lockheed-martin/eo/documents/suppliers/rms/rms-quality-procure-2-011-052023.pdf) — 24-hour escape notification, 3-day MRB, 40-year retention · [LM SCAR process](https://www.lockheedmartin.com/content/dam/lockheed-martin/aero/documents/scm/Quality-Requirements/Corrective-Action/supplier_CAP.pdf)

**Practitioner testimony**
- [Elsmar: who verifies customer specifications](https://elsmar.com/elsmarqualityforum/threads/whos-responsible-for-verification-of-customer-specifications.85345/) — "The customer has no PUSH system"
- [Elsmar: corrective action response timeframes](https://elsmar.com/elsmarqualityforum/threads/number-of-days-to-respond-to-corrective-action-standard-response-time-frame.10086/) — 7 days for documentation problems
- [Elsmar: how can I respond to this SCAR](https://elsmar.com/elsmarqualityforum/threads/how-can-i-respond-to-this-scar-supplier-corrective-action-request.67257/) — banned root causes
- [Elsmar: documentation accompanying an aerospace part](https://elsmar.com/elsmarqualityforum/threads/documentation-accompanying-an-aerospace-part.84250/) — no standard name for the package
- [Elsmar: extent of information required in a C of C](https://elsmar.com/elsmarqualityforum/threads/extent-of-information-required-in-coc-aka-c-of-c-and-certificate-of-conformance.45129/) · [Elsmar: Nadcap parts cert more than just the spec](https://elsmar.com/elsmarqualityforum/threads/nadcap-parts-cert-of-conformance-more-than-just-the-spec.49099/) · [Elsmar: AC7108 subcontract testing](https://elsmar.com/elsmarqualityforum/threads/nadcap-chemical-processing-question-about-testing-sub-contractor-requirements.71054/)
- [finishing.com 276/98](https://www.finishing.com/276/98.shtml) — Nadcap cost and "2 page shop traveler is now 12 pages"
- [finishing.com 145/37](https://www.finishing.com/145/37.shtml) and [438/22](https://www.finishing.com/438/22.shtml) — HE bake windows and the at-temperature dispute
- [Products Finishing: What is the correct anodizing specification](https://www.pfonline.com/articles/what-is-the-correct-anodizing-specification) · [AHT: Heat treat PO DOs & DON'Ts](https://www.ahtcorp.com/articles/blog/heat-treat-purchase-orders-dos-donts/) · [Finishing & Coating: how to "fire" customers](https://finishingandcoating.com/index.php/plating/476-shops-tell-us-how-to-fire-customers)
- [Metal Finishing Company T&Cs](https://metalfinishingco.com/terms-and-conditions/) and [minimum lot charges](https://metalfinishingco.com/minimum-lot-charges/) · [Finishing Professionals FAQ](https://finishingpros.com/faqs/) · [Erie Plating expedite](https://www.erieplatingcompany.com/fast-delivery)

**Software and cost**
- [IoT Analytics MES study](https://iot-analytics.com/mes-vendors-replace-pen-paper-spreadsheets/) — 54% pen & paper/spreadsheets
- [Mainsail / Steelhead $84M](https://mainsailpartners.com/steelhead-technologies-announces-84m-growth-capital-investment/) · [Steelhead customer portal](https://gosteelhead.com/customer-portal-0) · [Steelhead specs & certs](https://gosteelhead.com/specifications-and-certifications) · [Franke Plating case](https://gosteelhead.com/plating-company-goes-paperless-shop-floor-software) · [Capterra Steelhead reviews](https://www.capterra.com/p/276850/Steelhead/reviews/)
- [JobBOSS² pricing](https://www.top10erp.org/products/jobboss%C2%B2/pricing) · [ProShop pricing](https://softwarefinder.com/enterprise-resource-planning-software/proshop-erp/pricing) · [Global Shop pricing](https://www.erpresearch.com/pricing/global-shop-solutions) · [Plex pricing](https://www.top10erp.org/products/plex-manufacturing-cloud/pricing)
- [PRI audit fee rate card](https://mpofcinci.com/blog/complete-nadcap-guide/) · [AQM Nadcap cost and timeframe](https://aqmauditing.com/cost-timeframe-for-gaining-nadcap-certification/)
- [SBA on CMMC Phase II suspension, 2026-07-13](https://legacy.sba.gov/article/2026/07/13/sba-commends-us-department-wars-suspension-cmmc-phase-ii-small-defense-contractors) · [ITAR encryption carve-out](https://sanctionsnews.bakermckenzie.com/ddtc-issues-itar-rule-affecting-technology-transfers-encryption-and-cloud-computing/)

### Strong inferences (reasoned from verified inputs)

- **The cert is a pure projection of traveler data.** AC7108 3.3.1 forces the traveler to contain the PO number, spec + revision, per-lot recorded parameters and dated buy-offs; the customer field lists are a strict subset. No source states this; it follows directly from comparing the two documents. It is the core of the market thesis.
- **Automated cert generation may be the only acceptable 8D corrective action for a transcription defect**, given the ~7-day documentation SCAR track and customers' explicit prohibition on "human error" as a root cause.
- **The quality function at a 30–100 person shop is 1 manager plus 2–4 technicians, ~3–5% of headcount**, often merged with EHS and process chemistry, and frequently absent below ~30 employees. Supported by two job postings; not survey-validated.
- **A furnace falling out of TUS compliance can silently invalidate a specific customer approval**, because Boeing D1-4426 approvals carry equipment limitation codes. Structurally necessary; no documented instance found.
- **ERP TCO of 0.7–1.5% of revenue for a 25-person shop**, computed from published per-user pricing against QCEW-implied revenue — which makes "evaluate ERP, decide it's overkill, go back to the spreadsheet" a rational decision rather than a lazy one.
- **A defensible HE bake record requires three timestamps**, per the practitioner dispute over when the clock starts.
- **>85% of heat treat plants and >90% of finishing shops remain outside PE/strategic platforms.**

### Tentative hypotheses requiring practitioner validation

- **That paperwork-caused rejections outnumber product-caused rejections.** Rests entirely on [one consultant's unquantified assertion](https://gndctl.com/resources/top-five-reasons-for-an-fai-rejection/). Four separate searches found no quantification anywhere. **This is the load-bearing assumption of the top-ranked concept and must be tested first.**
- **That shops track AMS2750 and solution-analysis due dates in spreadsheets.** No public source says so. Structurally near-certain given the tables' complexity and the existence of commercial validation software, but unverified. Ask to *see* the tracker.
- **That cert production takes 20–30 minutes.** One named practitioner, in a vendor testimonial. An Elsmar practitioner separately estimates *"A simple template with handwriten info shouldn't take more than 5 minutes"* — a 6× spread that materially changes the ROI case.
- **That most shops give customers zero WIP visibility.** Indicated by an 80%-call-reduction marketing claim and by shops publishing expedite services without status tools. Not measured.
- **That multi-portal burden is a felt pain.** Compositionally obvious (Boeing/Exostar + Northrop/Net-Inspect + Lockheed + eAuditNet + per-customer EDI), but no first-person complaint from a special-process shop could be found in open sources.
- **Whether a contract-review miss is classified Major or Minor** by PRI. PRI reports it as a recurring theme producing Major NCRs, but the classification rules are not public.

### Known gaps

PRI's own "Most Common NCRs" documents are not openly published — the only public rendering is Kacsik's reproduction of 2016–2017 heat-treat data. No public per-commodity NCR percentages beyond the 2018–2021 average of four and the 2021 Coatings/MTL figure of ten. No public Nadcap failure rate. No survey measures ERP/MES adoption specifically among plating, anodizing or heat treat shops — Products Finishing's Top Shops survey measures process automation, not business software. Practical Machinist returns HTTP 403 to automated fetches, so four directly on-topic threads (plating shops ruining parts, vendor screw-ups, false certs) are verified to exist but unread. AS9102 Rev C §1.3 language extending applicability to special-process suppliers is reported secondhand by [Net-Inspect](https://www.net-inspect.com/blog/as9102-rev-b-vs-rev-c/) and should be verified against the standard before being relied on. SBA's CMMC cost figures (~$593,800/certification) are an order of magnitude above DoD's own estimates and the two are not reconciled in public sources.
