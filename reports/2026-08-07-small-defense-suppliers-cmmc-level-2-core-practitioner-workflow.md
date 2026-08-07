# Small Defense Suppliers Navigating CMMC Level 2 Compliance — Core Practitioner Workflow

**Market research cycle report**

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market** | Small defense suppliers navigating CMMC Level 2 compliance |
| **Angle** | core-practitioner-workflow |
| **Claim ID** | `031af032` |
| **Date** | 2026-08-07 |
| **Report** | `reports/2026-08-07-small-defense-suppliers-cmmc-level-2-core-practitioner-workflow.md` |
| **Backlog remaining after this claim** | 255 assignments across 133 markets |

### Why this assignment over the others available

The ledger held 256 open assignments when this cycle started, and 15 completed reports. Three considerations decided it.

**Catalog breadth.** The 15 completed reports cluster hard into four families: AEC/design services (fire protection, land surveying, MEP/HVAC, geotechnical labs, construction submittal coordination), insurance (commercial lines back office, claims adjusting), transportation (freight brokerage, motor carriers), and real-estate/health-care back office (property management, title/escrow, medical billing, nonprofit grants). **Zero completed reports touch manufacturing quality-and-compliance systems, and zero touch cybersecurity/regulatory-attestation work of any kind.** This assignment opens both at once: the practitioner is usually a quality manager or an owner-operator at a 15–200 person machine shop, electronics assembler, or specialty fabricator, and the work product is a regulated attestation package. Priority (a) in the brief — markets with zero completed entries over markets already partially covered — points here strongly.

**Evidence availability, with an unusual bonus.** This market is documented to a degree most are not, because three separate government bodies audited it inside the last twelve months: GAO-26-107955 on CMMC program risk, DODIG-2026-047 on the DoD's own failure to mark CUI, and the Department of War's own July 2026 reform memoranda. Better still, there is a **live government request for exactly the evidence this report needs**: the CMMC Reform Task Force RFI, with responses due **August 14, 2026 — seven days from today**. Its Question 1 asks industry to "identify the top five most prohibitive cost drivers, administrative burdens, or operational challenges," and its Question 5 asks what challenges exist in "maintaining, verifying, and reporting compliance" for self-assessments. When the regulator itself publishes a hypothesis that the paperwork is the burden, that is a strong signal for a catalog of small focused tools.

**Angle diversity and timing.** Completed angles run core-practitioner-workflow ×6, back-office ×3, narrow-subspecialty ×3, handoffs-and-qa ×3. Core-practitioner-workflow is the most-covered angle, which argues against it — but for this market the core practitioner workflow *is* the compliance workflow, and the other three angles would be derivative of it. Taking core first makes the later three angles (subcontractor flowdown as handoffs-and-qa; ITAR/export administration as narrow-subspecialty; contract and clause administration as back-office) more tractable rather than less.

**One caveat I want on the record.** On **July 13, 2026** the Department of War suspended CMMC Phase 2 — the third-party C3PAO certification requirement — pending a 60-day reform review whose recommendations are due around **September 13, 2026**. A reasonable person might read that as "this market just evaporated." It did not, and the reason matters for everything downstream: the suspension removed the *auditor*, not the *obligation*. DFARS 252.204-7012, NIST SP 800-171 Rev 2 implementation, the System Security Plan, the POA&M, the SPRS score, and the annual affirmation by a named senior executive all remain contractually binding. Several law firms reached the same conclusion independently — that removing prospective third-party verification while retaining self-attestation *raises* False Claims Act exposure, because verification now happens retrospectively through DIBCAC audits and qui tam relators. The Department of Justice priced a false self-assessment at **$507,144** six weeks before the suspension. This report is written to that reality, and Section 4 deliberately favours concepts whose value survives whatever the task force recommends in September.

---

## 1. Market examined

**Industry.** The United States Defense Industrial Base (DIB) — roughly **200,000 companies**, of which small businesses are "roughly three-quarters" (GAO-26-107955). This report addresses the small-supplier tier, not primes.

**Typical organizations.** Precision machine shops and job shops; sheet metal and weldment fabricators; wire harness and electronics assemblers; injection moulders and metal finishers; small engineering and test-services firms; specialty component suppliers two to four tiers below a Lockheed, RTX, Boeing, or Northrop. Many do defense work as 20–60% of revenue, with commercial and medical work filling the rest — a fact that shapes the economics badly, because compliance cost lands on the whole company while the revenue it protects is a minority slice.

**Organization size most likely to benefit from focused tools.** **10 to 200 employees**, with the sweet spot at **15–75**. Two published datapoints bracket it usefully:

- **Micro-Precision Technologies** (Salem, NH), **15 employees**, 8,500 sq ft, invested **$20,000 in workforce and $60,000 in information systems** to protect **$500,000 in sales** (NIST MEP success story).
- **Kform**, a machine shop whose CEO Callye Keen framed the annual decision as: *"Year after year, we have to make the decision: Do I buy another piece of equipment? Do I invest in a robot? Do I hire another engineer? Or do I meet CMMC compliance?"*

**Type of user.** Almost never a dedicated security person. In practice the compliance work lands on one of four people:

1. The **owner/president**, who is also the named **Affirming Official** signing the SPRS attestation under threat of 18 U.S.C. § 1001 and the False Claims Act.
2. The **quality manager**, who already owns ISO 9001 or AS9100 and gets CMMC bolted on because it looks like another standard with clauses and evidence.
3. The **one-person IT department**, or nobody, with a **Managed Service Provider** filling the gap.
4. An outside **Registered Practitioner Organization** or consultant, engaged in bursts the company cannot afford to make continuous.

The Alluvionic 2025 survey of small DIB contractors (<$100M revenue) found **50% lack documented cybersecurity policies**, **56% have no gap analysis**, **70% lack compliant technical solutions**, and **32% do not know which CMMC level applies to them**. That last figure is the one to sit with: a third of this market cannot yet name its own obligation.

---

## 2. How the work is performed

### 2.1 The trigger

Work begins with a contract document, not a decision. A purchase order, a solicitation, or a prime's supplier portal notice arrives carrying cybersecurity clauses. The supplier must read them and determine what is owed. **As of 2026 this first step is genuinely hard, because the clause numbering is in flux.**

The "Revolutionary FAR Overhaul," effective **February 1, 2026** and implemented by **class deviation rather than rulemaking**, eliminated **DFARS 252.204-7019**, moved **252.204-7020** to **252.240-7997** (stripping out the Basic self-assessment requirement), renumbered **FAR 52.204-21** to **FAR 52.240-93**, left **252.204-7012** and **252.204-7021** unchanged, and added a new **DFARS 252.204-7025 (NOV 2025)**, "Notice of CMMC Level Requirements." Because class deviations do not alter published DFARS text, **acquisition.gov still publishes 252.204-7019 (NOV 2023) as current**. Both numbering systems are live in the wild. A 30-person shop's contracts administrator must read the actual solicitation and cannot rely on the public regulation text.

### 2.2 Scoping — deciding what is in the boundary

The supplier must determine which of its systems process, store, or transmit **Federal Contract Information** and **Controlled Unclassified Information**, and assign every asset to one of five categories from the official Level 2 Scoping Guide: **CUI Assets**, **Security Protection Assets**, **Contractor Risk Managed Assets**, **Specialized Assets** (IoT/IIoT/OT, government-furnished equipment, test equipment, restricted systems), and **Out-of-Scope Assets**.

This is where a machine shop's reality collides with the framework. CUI does not stay in a server. ProShop ERP's practitioner guidance describes it plainly: CUI "is printed on paper in dozens of filing cabinets, flowing around the shop floor in job travelers, sitting in machinist tool boxes in the form of setup books, or drawings, on the laptops of their sales people as they travel around visiting clients." Drawings, CAD models, BOMs, customer POs, and job travelers may all be CUI. A CNC programmer or inspector needs to see the print; a delivery driver does not.

The consequence of getting the boundary wrong is total, not proportional. DoD's CMMC FAQ v6: *"any company information systems not represented by the CMMC UID(s) provided … are considered non-compliant."*

**And the supplier frequently cannot scope correctly, because the government does not mark its own data.** DODIG-2026-047 (January 29, 2026) sampled 300 DoD documents and found **48% lacked a CUI designation indicator block**; of 40 document types reviewed, **28 (70%)** had no designation block or were still carrying the retired "For Official Use Only" marking. The Inspector General attributed the root cause to OUSD(I&S) having "provided conflicting and insufficient guidance and training." NDIA formally asked for "clear and consistent CUI identification and marking guidance," citing "inconsistencies, ambiguities, and inaccuracies," and did not get it.

### 2.3 Standing up the environment

CUI must live somewhere defensible. Three paths, all expensive:

- **Microsoft GCC High** — after the July 1, 2026 price increase, G3 is **$65.20/user/month**, G5 **$97.50**. A new **Business Premium GCC High** SKU at **$35.80** launched November 3, 2025 with a **300-seat cap** but is not sold through Microsoft's online portal; under 300 seats you must buy through an AOS-G partner. Twenty-five users on G3 is roughly **$19,560/year in licences alone**, before Defender/Purview add-ons (~$24.40/user/month, available February 20, 2026). Migration commonly runs **$25,000–$200,000** over three to six months.
- **A small enclave** — PreVeil at **$30/user/month**, which achieved DoD FedRAMP Moderate *equivalency*; Totem's single-PC enclave at **$6,495–$19,995/year**; ZCaaS at **$1,300/month for up to ten users**. Generic managed enclave-as-a-service runs **$300–$400/user/month**.
- **Roll your own**, which almost never survives assessment.

Any cloud service touching CUI must meet **FedRAMP Moderate** per DFARS 252.204-7012(b)(2)(ii)(D). "Equivalency" under the December 21, 2023 DoD CIO memo is stricter than most buyers assume: **100% of the 323 FedRAMP Moderate controls** implemented, assessed by a **FedRAMP-recognized 3PAO** (self-attestation explicitly not permitted), a full Body of Evidence including penetration test results, and **zero control-related POA&Ms** — "no such risk acceptance exists." DoD FAQ v6 closes the popular workaround: encryption does not cure a non-compliant cloud. A non-FedRAMP-Moderate service cannot hold even encrypted CUI.

### 2.4 The documentation build — where the hours actually go

This is the heart of the workflow and the heart of the opportunity.

**The System Security Plan.** NIST SP 800-171 requirement 3.12.4 obliges the supplier to "develop, document, and periodically update system security plans that describe system boundaries, system environments of operation, how security requirements are implemented, and the relationships with or connections to other systems." In practice that means: organizational overview and CUI types handled; user roles; the system boundary with hardware, software, and network inventory; physical and logical operating environment; system interconnections; **all 110 requirements with the specific implementation of each**, plus justification for any deemed not applicable; supporting policies, procedures, and training material; and an update cadence. Kieri's reference SSP for a small company runs **roughly 177 pages**.

**The 110-versus-320 problem — the single most-cited documentation defect in this market.** The 110 requirements decompose, under NIST SP 800-171A, into **320 determination statements** ("assessment objectives"). The Level 2 Assessment Guide is explicit about the arithmetic that follows: *"Each assessment objective in NIST SP 800-171A must yield a finding of MET or NOT APPLICABLE in order for the overall security requirement to be scored as MET."* One unmet objective fails the whole requirement. The Guide adds the line that sinks a large share of first attempts: *"all evidence must be in final form and not draft."*

Five named C3PAO assessors — Koren Wise (Wise Technical Innovations), Adam Glover (Insight Assurance), Travis Goldbach (Coalfire Federal), Mike Gallagher (A-LIGN), and Sammy Chowdhury (Prescient Security) — independently describe the same failure: SSPs written to the 110 rather than to the 320, boilerplate or AI-generated plans, and divergence between the SSP, the written procedure, and what the company actually does. Gallagher: *"When the organization talks through their CUI flow, and that doesn't match how it's represented in the system security plan — that is the biggest signal."* Prescient Security reports roughly **one third of organizations fail to advance past Phase 1**.

Commercial documentation kits acknowledge the gap by measuring themselves against it. Kieri markets its documentation as addressing "**more than 240 of the 320 assessment objectives**" — an implicit admission that even a purpose-built $10k+ kit leaves the buyer to close 80 objectives by hand.

**Hours.** The only credible authored-documentation figure I could verify anywhere comes from V. Amira Armond, owner of Kieri Solutions and chief editor of cmmcaudit.org: *"Just writing policies and gathering proof of compliance will take 300–600 hours for existing networks."* She adds that bringing existing systems up to the required security level "can easily take 1,000–2,000 consultant hours," and that "it could take 100 hours for your Linux administrator to fully secure a single Red Hat database server." (Written in CMMC 1.0 vocabulary, where "Level 3" maps to today's Level 2 / 800-171 baseline.)

### 2.5 Scoring and submission

The supplier self-scores under the **DoD Assessment Methodology, Version 1.2.1 (June 24, 2020)**. Start at 110 and subtract:

- **5 points** for each of 44 requirements "that, if not implemented, could lead to significant exploitation of the network, or exfiltration of DoD CUI."
- **3 points** for each of 14 requirements with "a specific and confined effect on the security of the network and its data."
- **1 point** for each of the remaining 51 derived requirements, with "limited or indirect effect."

Two requirements carry partial credit, and they are the two that trip people up: **3.5.3 (MFA)** costs 3 points if multifactor is implemented only for remote and privileged users, 5 if not implemented at all; **3.13.11 (FIPS)** costs 3 points if encryption is employed but not FIPS-validated, 5 if not employed. The range is **110 down to −203**, and a **"Not Met" on 3.12.4 (SSP) yields "No Score"** entirely rather than a deduction.

Submission to the **Supplier Performance Risk System** is a ten-field form: HLO CAGE code, assessment standard, assessment date, score (the form accepts −205 to 110), assessing scope (Enterprise / Contracts / Enclave), plan-of-action completion date (mandatory whenever the score is under 110), SSP name, SSP version, SSP date, and included CAGE codes. CMMC entries add a **Unique Identifier** per in-scope system.

**Self-scores are systematically and enormously wrong.** Jacob Hill of Summit 7, describing what third-party review found: contractors *"were probably 100, 150 points less than what you thought you were."* CyberSheath's fourth annual survey (Merrill Research, October 2025) found **1% of contractors report being fully prepared**, 42% have submitted SPRS scores, **17% report negative scores**, and the median score moved from 20 in 2022 to 60 in 2025.

### 2.6 POA&M and conditional status

Anything not implemented is a deduction; the POA&M controls *status*, not score. Under **32 CFR 170.21**, Conditional status requires a score of at least **0.8 × 110 = 88**, and the POA&M must be closed out by assessment **within 180 days of the Conditional CMMC Status Date** or the status expires. **Six requirements are ineligible for a POA&M at all**: AC.L2-3.1.20 (external connections), AC.L2-3.1.22 (control public information), **CA.L2-3.12.4 (System Security Plan)**, PE.L2-3.10.3 (escort visitors), PE.L2-3.10.4 (physical access logs), PE.L2-3.10.5 (manage physical access). Counterintuitively, none of the 5-point requirements are on that list — the ineligible set is mostly 1-point items, which is exactly why practitioners misplan around it. NDIA's formal comment on the rule notes that "close to two-thirds of the 320 assessment objectives in Level 2 are related to requirements that are not eligible for POA&Ms."

### 2.7 Affirmation

Under **32 CFR 170.22**, a "senior level representative from within each Organization Seeking Assessment" affirms in SPRS that the organization "has implemented and will maintain implementation of all applicable CMMC security requirements." Affirmation is required at conditional status, at final status, **annually thereafter**, and after POA&M closeout. The screen the Affirming Official clicks reads, verbatim: *"Misrepresentation of this CMMC compliance status to the Government may result in criminal prosecution, including actions under section 1001, Title 18 of the United States code, civil liability under the False Claims Act, and contract remedies as determined appropriate by the contracting officer."*

### 2.8 Ongoing operation

- **Evidence maintenance** against 320 objectives, in final form, refreshed on some cadence the supplier must invent — the standard does not specify one.
- **72-hour incident reporting** under DFARS 252.204-7012(c). Note a process change most references still get wrong: the **DIBNet portal was decommissioned June 6, 2025**; reporting now goes through the **Incident Collection Format portal at icf.dcise.cert.org**, with the completed ICF transmitted to DC3 by encrypted email or DoD SAFE. Authentication requires a **DoD-approved medium assurance credential** available from only **two** authorized ECA issuers, IdenTrust and WidePoint, at several hundred dollars, installed per machine per user account, with identity proofing. The predictable failure mode: nobody obtains the credential until an incident occurs, and by then the 72 hours are gone. Affected system images and monitoring data must be preserved **90 days**.
- **Subcontractor flowdown** under 32 CFR 170.23: a sub handling FCI only needs Level 1 self; a sub handling CUI needs Level 2 self at minimum; and "prime contractors shall comply and shall require subcontractors to comply with and to flow down CMMC requirements, such that compliance will be required throughout the supply chain at all tiers."
- **CUI marking**, continuously, on every outgoing and internal document.
- **Annual re-affirmation**, and SSP review and update as required by 3.12.4's own objectives.

### 2.9 CUI marking mechanics — the part small manufacturers get wrong

Governed by **32 CFR Part 2002** (NARA), **DoDI 5200.48**, and **DoDI 5230.24** for technical documents and drawings.

- **Banner and footer:** the bare acronym **"CUI"**, bold, capitalized, centered, **top and bottom of every page** (DoDI 5200.48 ¶3.4.a). Do not prefix "UNCLASSIFIED."
- **A DoD-specific rule that contradicts the general federal CUI Marking Handbook:** in DoD you do **not** put the category or limited dissemination control in the banner. DoD's own training aid: *"Do not add the CUI category to the top and bottom of the page. The category is listed in the CUI designation indicator block."* So correct DoD practice is a bare `CUI` banner — **not** `CUI//SP-CTI//FEDCON`. This is among the most common marking errors in the DIB, and it is an error in the direction of looking *more* rigorous.
- **Designation indicator block** (¶3.4.f), first page or cover: Controlled by (component), Controlled by (office), CUI Category, Limited Dissemination Control or Distribution Statement, and a point of contact.
- **Limited Dissemination Controls:** NOFORN, FED ONLY, **FEDCON**, **NOCON**, DL ONLY, REL TO, DISPLAY ONLY. FEDCON versus NOCON is the pair that bites contractors — NOCON means the contractor is not an authorized recipient at all.
- **Drawings and engineering documents.** Two CUI categories mandate a distribution statement: export-controlled information and controlled technical information. Per DoDI 5200.48 ¶3.7.c(2), engineering drawings and associated specifications require **Distribution Statements B through F** per DoDI 5230.24, placed directly beneath the designation indicator — on a drawing, in or adjacent to the title block. So a CUI drawing physically carries a `CUI` banner top and bottom of **every sheet**, the designation indicator block, **the full distribution statement**, and an export-control warning where ITAR or EAR applies. **A bare `CUI` stamp on a drawing is non-compliant.**
- **Physical media:** SF 902 labels (2.125" × 1.25") for hard drives, SF 903 (2.125" × 0.625") for USB drives, SF 901 cover sheets as best practice. Transmittal documents must state that CUI is enclosed and that "when enclosure is removed, the document is Uncontrolled Unclassified Information."

### 2.10 External service providers

Under **32 CFR 170.19(c)(2)**, a cloud provider handling CUI must meet the FedRAMP requirements in DFARS 252.204-7012; a non-cloud ESP such as an MSP does **not** need its own CMMC certification, but "the services provided by the ESP are in the OSA's assessment scope and shall be assessed as part of the OSA's assessment." And the mandate that generates real work: *"The use of an ESP, its relationship to the OSA, and the services provided need to be documented in the OSA's SSP and described in the ESP's service description and customer responsibility matrix (CRM)."*

Assessors expect CRMs **incorporated into the SSP**, not merely attached; the full CRM in the Body of Evidence; and CRM references in the POA&M where remediation is shared. Documented failure modes: no CRM collected at all; MSP contracts silent on who validates patches, reviews logs, and escalates alerts; CRMs collected too late. FutureFeed's guidance states it bluntly: *"Vague language like 'our MSP handles security' will not satisfy an assessor."*

For Microsoft GCC High specifically, **53 of 110** requirements are inherited at the platform level, **56 of 110** are shared (the capability exists; the customer must configure it), and only **1 of 110** is customer-only at the requirement level. But the same analysis notes that "when examining all 320 assessment objectives across the 110 requirements, customer responsibility expands substantially beyond the single high-level requirement." Microsoft's CRM is not publicly downloadable — it requires an active GCC High deployment or a direct email request, which is itself a barrier for a 25-person shop trying to evaluate the platform *before* buying it.

---

## 3. Most important problems, ranked

### Problem 1 — The SSP is authored against 110 requirements while it is graded against 320 objectives

**Who.** The person writing the SSP: owner, quality manager, or outside consultant.
**When.** During initial documentation build, and again at every review cycle and every environment change.
**Currently handled by.** A purchased Word template (ComplianceForge CMMC Bundle 2 at **$10,530**; Kieri KCD, quote-only, ~177 pages, "more than 240 of the 320" objectives), a consultant's template, or a from-scratch document. Sometimes an LLM.
**Why inadequate.** The document's structure mirrors the 110, so the author has no place to record — and no way to notice the absence of — a narrative and an evidence pointer for each of the 320 determination statements. Because a single unmet objective fails the entire requirement and costs the full 5, 3, or 1 point, the arithmetic is unforgiving. Templates that stop at 240 objectives leave 80 gaps invisible.
**Frequency.** Continuous. The SSP is a living document; 3.12.4's own objectives require that it be "reviewed and updated" and "approved by an authoritative source."
**Cost.** 300–600 hours of authoring and evidence-gathering (Armond). One third of organizations fail to advance past Phase 1 (Prescient Security). At the low end of DoD's own estimate, a Level 2 self-assessment path costs a small entity **$34,277 initial plus $2,919 in affirmations over three years**.
**Evidence.** VERIFIED — five named C3PAO assessors describe this specific defect; the Level 2 Assessment Guide states the MET/NOT-MET arithmetic verbatim; Kieri's own marketing quantifies the gap. *(One caveat: the count of 320 is industry consensus across at least five independent sources, but I could not find it stated in a NIST or DoD primary document, including CMMC Assessment Guide L2 v2.13.)*

### Problem 2 — The SPRS score is wrong, and it is now the only thing standing between the owner and the False Claims Act

**Who.** The Affirming Official, personally.
**When.** At initial submission, annually, and on every material change.
**Currently handled by.** Manual arithmetic in a spreadsheet, a free web calculator, or a consultant's one-time computation. Usually no retained record of *why* each requirement was scored the way it was, or on what evidence, as of what date.
**Why inadequate.** Three reasons compound. The weighting is non-obvious (44/14/51 split, two partial-credit rules, an SSP gate that produces "No Score" rather than a deduction). The score is a point-in-time assertion that immediately begins to decay as the environment changes. And nothing in the ordinary workflow preserves the provenance a defence would require.
**Frequency.** Formally annual; practically, every time the environment changes.
**Cost.** Directly measurable in DOJ settlements:

| Contractor | Amount | Date | What happened |
|---|---|---|---|
| **MORSECORP Inc.** | **$4,600,000** | Mar 2025 | Submitted a score of **104** in January 2021; a third-party assessment in July 2022 found the actual score was **−142**; not corrected until June 2023, after a subpoena. No consolidated written SSP from Jan 2018 to Jan 2021. Relator received $851,000. |
| **Raytheon / RTX / Nightwing** | **$8,400,000** | Apr 2025 | Failed to implement an 800-171-compliant SSP, Aug 2015 – Jun 2021. |
| **Georgia Tech Research Corp.** | **$875,000** | Sep 2025 | No anti-virus deployed, delayed SSP, **submitted inflated assessment scores**. |
| **LOGZONE Inc.** (Alabama) | **$507,144** | **Jun 18, 2026** | Two Navy contracts, May 2021 – Mar 2025. DCMA assessed the actual score at **−170**. |

LOGZONE is the case this market should read: a **half-million-dollar settlement is within reach of a 30-person company's balance sheet**, and DIBCAC scores are now feeding DOJ referrals directly.
**Evidence.** VERIFIED — DOJ press releases; the DoD Assessment Methodology; the verbatim SPRS affirmation text; multiple law-firm analyses concluding FCA exposure rose after the suspension.

### Problem 3 — CUI marking on drawings and shop-floor documents is done by hand, per sheet, or not at all

**Who.** Engineering, document control, the print room, the quality manager.
**When.** Every incoming customer drawing package; every internal derivative (setup sheet, traveler, inspection report, FAI package); every outgoing deliverable.
**Currently handled by.** A stamp, a CAD title-block template if someone remembered to build one, a PDF annotation done sheet by sheet, or nothing.
**Why inadequate.** Compliant marking of a drawing requires four coordinated elements — `CUI` banner top and bottom of **every sheet**, the designation indicator block, the correct DoDI 5230.24 distribution statement (B through F), and an export-control warning where applicable — placed per DoD-specific rules that **contradict the general federal marking handbook** on whether the category belongs in the banner. Manual marking across a 40-sheet package is slow enough that it gets skipped, and the most common error (adding the category to the banner) looks *more* diligent, so nobody catches it.
**Frequency.** Daily. Highest-frequency task in this entire report.
**Cost.** Hard to price directly, and I will not invent a figure. Two indirect anchors: marking failures are a recurring assessor finding, and DODIG-2026-047 documents that the government's own marking compliance sits at roughly 52% on designation blocks — a strong signal that the task is genuinely difficult rather than merely neglected.
**Evidence.** VERIFIED for the rules (DoDI 5200.48, DoDI 5230.24, DoD training aids, CDSE job aids) and VERIFIED for the shop-floor circulation pattern (ProShop ERP practitioner guidance). STRONG INFERENCE on the time cost — no practitioner has published hours per package.

### Problem 4 — The supplier cannot determine what it received, because the government did not mark it

**Who.** Whoever opens the customer's file transfer: sales, estimating, engineering.
**When.** Every incoming RFQ, drawing package, and specification.
**Currently handled by.** Judgement. Sometimes an email to the buyer. Often an assumption in whichever direction is cheaper.
**Why inadequate.** DODIG-2026-047 found **48% of a 300-document DoD sample lacked a designation indicator block**, and **70% of 40 reviewed document types** had no block or carried legacy FOUO markings. DoD-wide figures: 9% of 48,000 documents (2023) and 11% of 26,000 (2024) missing required blocks. The supplier is asked to scope its assessment boundary against markings the originator does not reliably apply — and the penalty for scoping wrong is that everything outside the declared UIDs is "considered non-compliant."
**Frequency.** Every incoming package.
**Cost.** Two-sided: over-scope and you pay to protect commercial work at CUI rates; under-scope and you have a false attestation and a spillage exposure.
**Getting worse, then better, then unclear.** The **FAR CUI proposed rule (June 23, 2026, 91 FR 37550, FAR Case 2017-016)** would require the contracting officer to complete a standardized CUI identification form for every solicitation, and require contractors to notify the agency **within 72 hours** of discovering "unmarked or mismarked CUI, or any inconsistency between the SF XXX and the contract clauses." That fixes the root cause and simultaneously creates a new, clocked, per-document notification obligation. It also specifies **NIST SP 800-171 Rev 3**. It remains **proposed, not final** — comments closed July 23, 2026.
**Evidence.** VERIFIED — DoD Inspector General report, NDIA public comment, DoD CIO FAQ v6, the proposed rule text as reported by multiple law firms.

### Problem 5 — Evidence is collected once, goes stale, and nobody knows which objectives are uncovered

**Who.** Whoever prepares for an assessment or a customer audit.
**When.** In a panic, in the weeks before a DIBCAC assessment, a prime's supplier review, or an annual re-affirmation.
**Currently handled by.** A folder tree, a SharePoint site, screenshots in a Word document, and — per a practitioner MSP's own description of the market — "dozens of Excel spreadsheets."
**Why inadequate.** Three structural problems. Evidence maps many-to-many onto 320 objectives, which a spreadsheet models badly. The Level 2 Assessment Guide requires that "all evidence must be in final form and not draft," and nothing tracks draft status. And **there is no standard for how much evidence an objective needs**: a peer-reviewed survey of Certified CMMC Assessors (Therrien & Hastings, Dakota State University, arXiv 2602.09905 — 556 assessors invited, **17 usable responses**, 59% having done more than ten assessments) found that **71% said their C3PAO provided no evidence sampling methodology**, **71% had observed sampling inconsistency between assessors**, only **12%** referenced any quantitative model, and for one identical scenario proposals ranged from **1–3% spot checks to 95–100% census review**.
**Frequency.** Continuous obligation, episodic practice — which is the defect.
**Cost.** Assessors report the specific downstream failures: audit logs collected but never reviewed; logs in raw format ("if it's raw code you won't get information out of — that's not meeting the control"); vulnerability scans substituted for risk assessments; missing tabletop evidence for incident response testing.
**Evidence.** VERIFIED for assessor variance (peer-reviewed) and for the specific failure modes (named assessors). *Not verified:* the widely-assumed complaints about screenshot burden and artifact staleness cadence. I searched for a practitioner statement on either and found none. Treat those as HYPOTHESIS.

### Problem 6 — "Our MSP handles security" is the answer, and it is not an answer

**Who.** The supplier, who has outsourced IT and assumes it has outsourced the obligation.
**When.** At assessment, when the assessor asks who reviews the logs.
**Currently handled by.** An MSP contract written for commercial customers, with no CRM.
**Why inadequate.** 32 CFR 170.19(c)(2) puts the ESP's services inside the supplier's assessment scope and requires the CRM to be documented in the supplier's SSP. Assessors expect CRMs *incorporated*, not attached. Kform reported that its prior MSPs "lacked expertise in government compliance." And the CRM for the single most common platform — Microsoft GCC High — is not publicly downloadable.
**Frequency.** Once per ESP, revisited at each assessment and each ESP change.
**Cost.** A failed requirement or a whole failed family, plus renegotiation of an MSP contract mid-engagement.
**Evidence.** VERIFIED — 32 CFR 170.19 text, FutureFeed practitioner guidance, Kform customer account (vendor-hosted but attributed).

### Problem 7 — Flowdown verification is a paper exercise with no way to verify anything

**Who.** The small prime or higher-tier supplier that buys from others.
**When.** At every subcontract award, and whenever a prime demands supply-chain attestation.
**Currently handled by.** A questionnaire, a flowdown clause, and a portal.
**Why inadequate.** **SPRS scores are visible to the Government, not to peer companies.** There is no self-service lookup. Verification is contractual and portal-mediated, with no independent means of validating the number a supplier reports. Meanwhile the primes are demanding it regardless of the Phase 2 suspension:

| Prime | Date | Requirement | Mechanism |
|---|---|---|---|
| Raytheon (RTX) | Feb 2025 | Active CMMC certification at the appropriate level; disclose current or intended status | Annual Supplier Registration form |
| Lockheed Martin | Jun 2025 | Level 2 readiness; began contacting suppliers whose assessments showed unimplemented controls | **Exostar CCRA module** |
| Boeing | Sep 2025 | Specified CMMC level as a condition of award for suppliers handling FCI/CUI | Gap assessments across the supply base |
| Elbit America | Nov 5, 2025 | Immediate Level 1 self-assessment and affirmation in SPRS | SPRS submission + affirmation |
| Northrop Grumman | Dec 2025 | "Neither contracting officers nor prime contractors may waive or deviate from the CMMC cybersecurity control and assessment requirements" | Purchase order restrictions, no waivers |

Summit 7's observation is the operative one: primes including L3Harris, Lockheed, and Boeing continue demanding Level 2 **independently of** the DoD suspension, so the suspension provides little commercial relief in practice.
**Evidence.** VERIFIED — 32 CFR 170.23 text; documented prime mandates with dates.

### Problem 8 — The 72-hour incident clock cannot be met, because the credential takes longer than 72 hours to get

**Who.** Whoever discovers an incident.
**When.** Once, catastrophically.
**Currently handled by.** Not handled. The plan is to figure it out at the time.
**Why inadequate.** The DIBNet portal was decommissioned June 6, 2025; reporting moved to the ICF portal. Authentication requires an ECA medium-assurance credential from one of only two issuers, at several hundred dollars, per machine per user account, with identity proofing. The ICF itself is roughly a **20-question form** requiring DUNS and CAGE codes, contract numbers, multiple role contacts, discovery date, compromise type, techniques used, impact on defense operations, and an outcome determination. A documented practitioner complaint: contractors frequently cannot determine attack methodology within 72 hours and get no clarification on ambiguous fields.
**Frequency.** Rare — which is exactly why it is unprepared for.
**Cost.** A missed 72-hour report is a DFARS 7012 violation on the record.
**Evidence.** VERIFIED — DFARS 252.204-7012(c), DC3 ECA instructions, the portal transition.

### Problem 9 — Nobody can tell what their contract currently requires

**Who.** Contracts administration, which at this company size is the owner or the office manager.
**When.** Every solicitation and every contract modification.
**Currently handled by.** Reading the clause list and hoping.
**Why inadequate.** As of August 2026 a supplier faces simultaneously: the RFO renumbering by class deviation (7019 eliminated, 7020 → 252.240-7997, FAR 52.204-21 → 52.240-93) while **acquisition.gov still publishes 7019 as current text**; a new DFARS 252.204-7025 (NOV 2025); Class Deviation 2024-O0013 Rev 1 freezing DFARS 7012 to **Rev 2** while the FAR CUI proposed rule specifies **Rev 3**; the Phase 2 suspension requiring contracting officers to strip Level 2 (C3PAO) and Level 3 requirements from active solicitations "as soon as practicable" and from existing contracts at the next option exercise; and a reform task force whose recommendations land around September 13, 2026. **32% of small DIB contractors do not know which CMMC level applies to them** (Alluvionic) — and that is a rational response to this environment, not negligence.
**Evidence.** VERIFIED for each regulatory fact. The acquisition.gov-versus-class-deviation conflict is real and I confirmed the published 7019 text is still live; the reconciliation (class deviations do not alter published DFARS text) is STRONG INFERENCE.

### Problem 10 — The Rev 2 to Rev 3 transition is coming with an unpriced cliff in it

**Who.** Everyone who just finished a Rev 2 program.
**When.** Unknown. DoD FAQ v6 says Revision 3 will be incorporated "through future rulemaking," that companies **may** voluntarily implement it using DoD's published Organization-Defined Parameters, but that "assessments continue against Revision 2 until the class deviation is withdrawn." Commentary in April 2026 estimated 12–18 months; **no official date has been announced**.
**Why it matters.** Rev 3 has 13 fewer requirements than 110 but heavy consolidation, **88 ODPs**, and three new families. The hidden cost: the **61 Rev 2 "NFO" controls that were treated as assumed-satisfied become mandatory core requirements**.
**Evidence.** VERIFIED for the mechanics; the transition date is genuinely unknown. This ranks tenth because it is real but unscheduled, and building for it now would be building on sand.

---

## 4. Application opportunities

Ten concepts. I have deliberately weighted them toward tasks whose value **survives the September 2026 task force recommendations** — that means favouring obligations rooted in DFARS 252.204-7012, DoDI 5200.48, and 32 CFR 2002 (which the CMMC review does not touch) over obligations rooted in the CMMC assessment apparatus itself.

---

### 4.1 — CUI Stamper: batch marking for drawings and document packages

**Intended user.** Document control, engineering, or the print room at a 15–150 person defense manufacturer.

**Problem solved.** Compliant CUI marking of drawing packages and documents requires four coordinated elements per DoDI 5200.48 and DoDI 5230.24, applied to every sheet, following DoD-specific rules that contradict the general federal marking handbook. Doing it by hand is slow enough to get skipped, and the most common error looks like diligence.

**Current workflow.** Open the PDF. Add a header and footer manually, or stamp physically. Type or paste the designation indicator block on page one. Look up which distribution statement applies, hope it is the right one, paste it. Repeat per sheet or accept an incomplete job. On a 40-sheet package, either it takes an hour or it does not get done.

**Proposed workflow.** Select a folder or a set of files. Choose a **marking profile** (a saved per-customer or per-contract configuration: controlling office, CUI category, LDC, distribution statement letter and its controlling-office/date fill-ins, export-control warning on or off). Run. The tool applies the `CUI` banner and footer to every page, places the designation indicator block on the first page or cover, places the distribution statement directly beneath it, and — for drawings — places both in a configurable title-block-relative position. It writes a marking log recording which files were marked with which profile, when, and by whom.

**Required inputs.** PDF files (native or scanned). A marking profile. Optionally a title-block coordinate template per drawing size (A through E, ANSI/ISO).

**Expected outputs.** Marked PDFs with originals preserved. A CSV marking log. An exception report listing files that were skipped, already marked, or **mismarked** — including the category-in-the-banner error and legacy FOUO markings.

**Essential features.** Per-customer marking profiles. Every-page banner/footer. Designation indicator block templating. The full DoDI 5230.24 Distribution Statement A–F text with fill-in fields. DoD-specific validation (reject a category in the banner). Detection of existing markings so re-running is idempotent. Marking log. Runs entirely locally.

**Deliberately excluded from initial scope.** OCR of scanned drawings. DWG/DXF native marking (PDF only at first). Any attempt to *decide* whether a document is CUI. Email marking. Physical media label printing. Access control or a document repository.

**AI.** **Inappropriate for the stamping itself** — this is a deterministic rules-and-geometry problem and an LLM would only add nondeterminism to a compliance artifact. **Optional, clearly separated, for a second feature:** classifying whether an *incoming* document is likely CUI based on markings, distribution statements, and content cues. That belongs in concept 4.2, not here.

**Why a spreadsheet would not suffice.** The output is a modified PDF. A spreadsheet cannot render a banner onto page 37 of a drawing package.

**Complexity.** **Small to medium.** `pypdf`/`pikepdf` plus `reportlab` overlays, a profile store, a Tkinter or small local web UI. A competent developer builds a working version in two to three weeks.

**Learning difficulty.** Very low. Pick a profile, pick files, press go. Under fifteen minutes.

**Value.** Direct and measurable in a before-and-after demo: a 40-sheet package marked correctly in seconds versus an hour manual, with the DoD-specific banner rule enforced rather than remembered.

**Risks and constraints.** The tool must never phone home — it will be handling CUI, so local-only operation is a hard requirement, not a preference. Getting the marking rules wrong would produce confidently non-compliant documents at scale, so the rule pack needs to cite its source per rule and be reviewed by someone who has read DoDI 5200.48. Distribution statement selection is a legal determination the user must make; the tool should present the criteria and refuse to guess.

**Existing products and substitutes.** Adobe Acrobat and Bluebeam Revu both do batch stamping and Bluebeam is already on many engineering desktops — but they are generic, they encode none of the DoD rules, they do not validate, and configuring them correctly is precisely the expertise the user lacks. Titus/Fortra and Microsoft Purview do sensitivity labelling at enterprise scale and price. **I found no purpose-built, affordable, DoD-rule-aware drawing marker.** The nearest open-source thing in the whole ecosystem is a 38-star SSP generator.

**Why still attractive.** The obligation comes from DoDI 5200.48 and 32 CFR 2002, not from CMMC — it is entirely unaffected by the Phase 2 suspension and by whatever the task force recommends. It is the highest-frequency task in this market. And it is small enough to actually finish.

**Paid customization potential.** Excellent. Per-customer marking profiles, title-block coordinate mapping for the client's CAD standards, integration with the client's PDM or ERP output folder, ITAR/EAR warning variants, batch-processing hooks into an existing print workflow.

---

### 4.2 — CUI Intake Register: log what arrived, and notify when it is unmarked

**Intended user.** Estimating, sales, or engineering — whoever receives customer files.

**Problem solved.** DODIG-2026-047 found 48% of sampled DoD documents lacked a designation indicator block. Suppliers must scope against markings that frequently are not there, and the FAR CUI proposed rule would require notifying the agency **within 72 hours** of discovering unmarked or mismarked CUI.

**Current workflow.** Files arrive by email, portal, or mail. Someone eyeballs them. Nothing is recorded. Nobody can later demonstrate what was received, how it was marked, or why the boundary was drawn where it was.

**Proposed workflow.** Drop the incoming package into a watched folder or register it manually. The tool records source, date, contract or RFQ number, customer, and file inventory; extracts any markings present (banner text, designation block fields, distribution statement, legacy FOUO); classifies the package as marked-CUI, unmarked-but-probably-CUI, mismarked, or apparently-uncontrolled; and where markings are absent or inconsistent, drafts the notification to the contracting officer with the specifics filled in. Everything becomes a searchable register that doubles as scoping evidence.

**Required inputs.** Incoming files. A minimal contract register (contract number, customer, CO contact, clause list).

**Expected outputs.** An intake register (CSV/SQLite). Per-package marking assessment. Draft notification letters or emails. A scoping evidence pack listing every document determined to be CUI and why.

**Essential features.** Watched-folder or drag-drop intake. Marking extraction from PDF text. Legacy FOUO detection. Mismarking detection. Notification drafting with a 72-hour countdown. Full-text search of the register. Local-only.

**Deliberately excluded.** Email server integration. Automatic sending of notifications (a human signs those). File storage or version control. Portal scraping.

**AI.** **Optional and genuinely useful, in one narrow place:** reading marking blocks off inconsistently formatted PDFs and flagging content cues suggesting controlled technical information where markings are absent. A regex pass handles well-formed markings; the value of a model is in the malformed 48%. **The classification must always be advisory** and presented as "review this" rather than "this is CUI" — the determination has legal consequences and belongs to a human.

**Why a spreadsheet would not suffice.** A spreadsheet cannot read markings out of PDFs, and a manually maintained one will not be maintained. The register only has value if creating an entry is cheaper than not creating one.

**Complexity.** **Medium.**

**Learning difficulty.** Low — under an hour.

**Value.** Two forms. It produces the scoping evidence that an assessor asks for and that most small suppliers cannot produce. And if the FAR CUI rule finalizes as proposed, it converts a new 72-hour obligation from a liability into a logged routine.

**Risks and constraints.** The register itself contains CUI metadata and must be treated as in-scope. Over-reliance on an advisory classifier is the main failure mode; the UI must make the human decision unavoidable.

**Existing products and substitutes.** Enterprise DLP and data-classification suites (Purview, Titus/Fortra, Netwrix) at enterprise price and complexity. Nothing at this scale.

**Why still attractive.** It sits on the one problem in this market that is unambiguously the *government's* fault and therefore unlikely to be regulated away. It also pairs naturally with 4.1 as a two-tool bundle.

**Paid customization potential.** Good — customer-specific portal intake, ERP hooks, notification templates matched to specific contracting offices.

---

### 4.3 — Defensible SPRS: score calculator with a signed, versioned record

**Intended user.** The Affirming Official, and whoever prepares the number for them.

**Problem solved.** SPRS scores are commonly wrong by 100–150 points, the self-attestation is now the only gate, and the DOJ has settled false-score cases at $507,144 (LOGZONE, −170 actual) and $4.6M (MORSECORP, 104 claimed versus −142 actual). Free calculators produce a number; **nothing cheap produces a defensible record of how the number was reached.**

**Current workflow.** Walk the 110 requirements. Mark met or not met. Subtract in a spreadsheet or a web form. Type ten fields into SPRS. Sign the affirmation. Retain, at best, the spreadsheet.

**Proposed workflow.** Walk the 110 requirements in a guided interface that implements DoD Assessment Methodology 1.2.1 exactly: the 44 five-point requirements, the 14 three-point, the 51 one-point, the partial-credit branches for 3.5.3 (MFA) and 3.13.11 (FIPS), and the 3.12.4 gate that yields "No Score" rather than a deduction. For each determination, capture who decided, on what date, and a pointer to the evidence. Produce the score, the ten-field SPRS submission packet, a **cryptographically hashed snapshot** of the whole determination set, and a **diff against the previously submitted snapshot** showing exactly what changed and why.

**Required inputs.** Requirement-by-requirement determinations. Evidence pointers (paths or hashes, not the artifacts). Assessor and date. Scope selection (Enterprise, Contracts, or Enclave) and CAGE codes.

**Expected outputs.** The score with a full per-requirement audit trail. The SPRS submission field packet, ready to type. A signed snapshot. A change report versus the prior submission. A Conditional-status eligibility check against the 88-point threshold.

**Essential features.** Exact Methodology 1.2.1 weights with source citations per requirement. Both partial-credit rules. The SSP gate. Snapshot hashing and immutable history. Submission diff. Threshold checks. Local-only, single-file storage.

**Deliberately excluded.** Any SPRS API submission (there is no public one, and automating a legal attestation would be reckless). Automated technical scanning. Remediation guidance. Multi-tenant hosting.

**AI.** **Inappropriate.** This is arithmetic with legal consequences. A model in this path adds risk and subtracts defensibility.

**Why a spreadsheet would not suffice.** A spreadsheet does the arithmetic fine — that is not the product. The product is the immutable, dated, evidence-linked, diffable record. A spreadsheet is silently editable, which is the precise opposite of what a defence needs.

**Complexity.** **Small.** The domain data is a fixed table of 110 rows. Two to three weeks.

**Learning difficulty.** Very low.

**Value.** Asymmetric. The tool costs nothing and the downside it addresses is a six-figure settlement plus personal § 1001 exposure for a named individual. That is the cleanest ROI story in this report, even though the *probability* is low for any one company.

**Risks and constraints.** The tool must not imply that using it makes a score correct — it makes a score *documented*. Marketing must be careful here; overclaiming would be both wrong and a liability. The scoring table needs a version stamp so a snapshot taken under Methodology 1.2.1 stays interpretable if DoD publishes a successor.

**Existing products and substitutes.** Free calculators from Totem, greypike, and others produce a number and no record. FutureFeed at **$99/month for ≤25 FTE plus $1,008/year for the Level 2 add-on** (~$2,196/year) does this as part of a platform and is honestly good value. Excel templates circulate widely.

**Why still attractive despite FutureFeed.** Three reasons. Roughly half this market has not bought any platform — the CyberSheath survey found 42% have submitted scores at all, and Keysight found only 3% of contractors use automated security validation tools. A free, local, single-purpose tool meets people where they are. Second, the *provenance and diff* angle is not what platform scoring modules emphasize; they emphasize progress tracking. Third, it is a natural on-ramp: a company that adopts this tool has just built the input dataset for concept 4.4.

**Paid customization potential.** Moderate — multi-CAGE and multi-enclave configurations, consultant-branded reporting for RPOs managing several clients.

---

### 4.4 — SSP-320: objective-level System Security Plan compiler

**Intended user.** The person authoring or maintaining the SSP.

**Problem solved.** Problem 1 — the SSP is written to 110 requirements and graded against 320 determination statements, so gaps are structurally invisible until an assessor finds them.

**Current workflow.** Open a purchased or inherited Word template organized by the 110. Write an implementation narrative per requirement. Attach or reference evidence. Hope the narratives happen to satisfy every underlying objective. Discover during assessment that several do not.

**Proposed workflow.** Work through a structure organized by **objective**, not requirement. For each determination statement: a status (met / not met / not applicable), a narrative, and at least one evidence pointer with a date and a draft/final flag. The tool rolls objectives up to requirement status using the Assessment Guide's own rule — every applicable objective must be MET or NOT APPLICABLE for the requirement to be MET — and generates two artifacts: a conventional SSP document in the shape assessors expect, and a **coverage report** listing every objective with no narrative, no evidence, stale evidence, or draft evidence.

**Required inputs.** The 800-171A objective structure. Per-objective narratives and evidence pointers. Boundary, inventory, and environment descriptions. ESP/CRM responsibility splits (imported from 4.7 if present).

**Expected outputs.** A generated SSP (DOCX and PDF). An objective coverage report. A requirement roll-up that feeds directly into 4.3. A machine-readable export (JSON, and ideally OSCAL-shaped) so the data outlives the tool.

**Essential features.** The full 110 → 320 mapping with per-objective narrative and evidence fields. Roll-up logic matching the Assessment Guide. Draft-versus-final tracking. Coverage gap report. Document generation from templates. Reuse of narratives across similar objectives. Local-only.

**Deliberately excluded.** Automated evidence collection from live systems. Policy and procedure authoring. Technical remediation. Anything resembling continuous monitoring. Hosting.

**AI.** **Optional, and only as a drafting aid with a hard guardrail.** Assessors named AI-generated boilerplate SSPs as a *failure mode*, so an AI feature here must work against that: suggest a narrative skeleton from the user's own stated implementation, never from the objective text alone, and flag anything the user did not edit as unreviewed. The honest framing is that AI can speed up the typing and cannot supply the facts.

**Why a spreadsheet would not suffice.** Three reasons. The one-to-many requirement→objective structure with many-to-many evidence links is a relational model, not a grid. The deliverable is a formatted ~177-page document. And the roll-up rule is conditional logic that spreadsheet users implement wrong.

**Complexity.** **Medium** — the largest build in this report, and the one whose scope most needs defending. The 320-objective dataset must be curated by hand from NIST SP 800-171A, and that is real work before a line of application code.

**Learning difficulty.** Moderate. Not an hour — realistically a half day to understand the objective-level model, though individual sessions are simple once the mental model lands. This is the one concept that violates the catalog's "learnable in about an hour" criterion, and that is a genuine mark against it.

**Value.** Directly attacks the defect five independent C3PAO assessors named as the most common cause of failure, in a market where roughly a third of organizations fail to advance past Phase 1.

**Risks and constraints.** The objective dataset is the moat and the liability — an error in the mapping propagates into every user's SSP. It needs source citations per objective and a published errata process. Rev 3 will eventually invalidate the dataset (13 fewer requirements, 88 ODPs, three new families), so the schema must anticipate a revision axis from day one. And note the licensing subtlety: NIST publications are US Government works and freely usable, but the CMMC Assessment Guides carry DoD document numbers and should be checked before redistribution.

**Existing products and substitutes.** ComplianceForge CMMC Bundle 2 at **$10,530** (static Word/Excel, no objective tracking). Kieri KCD, quote-only, ~177-page SSP, "more than 240 of the 320" objectives, explicitly built for organizations under 1,000 users. FutureFeed, Totem, Paramify ($8k–$25k/year, OSCAL-based). RegScale, enterprise, unpriced. **Open source: essentially nothing.** The most active project, `JAKTOOL/cmmc`, has 38 stars and generates an SSP as markdown and a POA&M as CSV — locally, offline, IndexedDB, which is architecturally exactly right — but does not work at objective granularity. `usnistgov/oscal-content` contains 800-53 rev4/rev5 and SP 800-172 rev3 but **not SP 800-171**, which is the single biggest structural gap in the open-source ecosystem: there is no official machine-readable 800-171 catalog to build on. One 18-star repo (`FATHOM5CORP/oscal`) exists specifically because of this, stating its reason for being as "NIST has not yet published similar OSCAL content for SP 800-171."

**Why still attractive.** A curated, openly licensed, objective-level 800-171 catalog with a generator on top would be the most valuable artifact in the open-source compliance ecosystem for this market, and it does not exist. It would also become the foundation the other concepts import.

**Paid customization potential.** Very high — client-specific SSP templates and house style, ESP language, multi-enclave boundaries, consultant multi-client deployments.

---

### 4.5 — Evidence Locker: an artifact register with a freshness clock

**Intended user.** The quality manager or compliance owner maintaining readiness between assessments.

**Problem solved.** Problem 5 — evidence is gathered in a panic, goes stale, and nobody can say which objectives are uncovered. The Assessment Guide requires all evidence "in final form and not draft," and assessor sampling expectations vary from 1% to 100% with no published methodology.

**Current workflow.** A folder tree, SharePoint, screenshots pasted into Word, and "dozens of Excel spreadsheets."

**Proposed workflow.** Register each artifact once: title, type (mapped to the Assessment Guide's examine / interview / test methods), owner, capture date, review cadence, draft-or-final status, file hash, and the objectives it supports. A dashboard answers the question a small supplier currently cannot: **which objectives have no evidence, stale evidence, or draft evidence, as of today.** A pre-assessment pack exports the current artifact set with its mapping.

**Required inputs.** Artifact metadata and file paths. The objective list (shared with 4.4). Per-artifact cadence.

**Expected outputs.** A coverage dashboard. A staleness queue by owner. A pre-assessment evidence pack with an index. A gap list.

**Essential features.** Many-to-many artifact↔objective mapping. Cadence and staleness computation. Draft/final flag. Hashing so silent file replacement is detectable. Owner assignment. Export. Local-only.

**Deliberately excluded.** Automated evidence capture. Screenshot tooling. Document storage (register paths and hashes, never copies). Ticketing or workflow approvals. Hosting.

**AI.** **Inappropriate.** This is a register with date arithmetic.

**Why a spreadsheet would not suffice.** The many-to-many mapping is the whole product and is exactly what spreadsheets model worst. Practitioners have already tried the spreadsheet; "dozens of Excel spreadsheets" is the documented result.

**Complexity.** **Small to medium.**

**Learning difficulty.** Low, once artifacts are registered. The registration itself is the adoption cost and should be made as cheap as possible — bulk import from a folder scan.

**Value.** Converts assessment prep from a scramble into a queue. Given documented assessor sampling variance from 1% to 100%, the defensive posture is to have *everything* current, which is only tractable with a clock.

**Risks and constraints.** Adoption is the risk: a register nobody populates is worthless, and the initial population is the expensive part. Mitigate with folder-scan import and by shipping a starter mapping for the most commonly required artifacts.

**Existing products and substitutes.** Every GRC platform does this as a module — Vanta, Drata (**$15,000–$100,000/year**), Hyperproof (median ACV **$41,400/year**), Apptega (~**$9,950/year** starting, criticized for "limited customization and reporting flexibility" and only ~15 integrations against 300–400 for peers). FutureFeed at ~$2,196/year is the realistic small-shop competitor.

**Why still attractive.** The differentiation is thinnest of the ten concepts, and I want that on the record. Its real case is as a companion to 4.4 rather than a standalone: once the objective dataset exists, the evidence register is a small increment on top of it, and the pair is worth more than either alone. As a standalone it would score lower.

**Paid customization potential.** Moderate.

---

### 4.6 — POA&M Clock: eligibility guard and 180-day countdown

**Intended user.** The compliance owner and the Affirming Official.

**Problem solved.** Problem 5's sibling. Six requirements are POA&M-ineligible and they are *not* the ones people expect — mostly 1-point items, including the SSP itself. Conditional status requires ≥88 of 110. Closeout is due within 180 days of the Conditional Status Date or the status expires.

**Current workflow.** A spreadsheet of open items with target dates, and someone remembering the rules.

**Proposed workflow.** Import the not-met determinations from 4.3. The tool refuses to place any of the six ineligible requirements on a POA&M and explains why with a citation. It computes the score and tests it against the 0.8 threshold. It sets the 180-day clock from the Conditional Status Date, shows time remaining per item and overall, and generates the POA&M in the format assessors expect, with milestones, owners, and resources.

**Required inputs.** Not-met determinations (from 4.3). Conditional Status Date. Milestones, owners, target dates.

**Expected outputs.** A POA&M document. An eligibility violation report. A countdown view. A closeout readiness check.

**Essential features.** The six-requirement ineligibility guard with citations to 32 CFR 170.21. The 88-point threshold test. The 180-day clock. POA&M generation. Milestone tracking.

**Deliberately excluded.** Project management. Resource planning. Remediation how-to guidance. Anything that becomes a task manager.

**AI.** **Inappropriate.** Rules and dates.

**Why a spreadsheet would not suffice.** Marginal on its own — a disciplined person could do this in Excel. The tool's value is that it encodes rules the user does not know, in particular the counterintuitive ineligibility list. That is a knowledge-transfer product wearing a calculator's clothes.

**Complexity.** **Small.**

**Learning difficulty.** Very low.

**Value.** Prevents a specific, documented planning error with a hard 180-day consequence.

**Risks and constraints.** The most CMMC-apparatus-dependent concept in the set. If the September task force overhauls conditional status or POA&M rules, the rule pack needs rework. Build it as a data-driven rule table, not hardcoded logic.

**Existing products and substitutes.** Platform POA&M modules; the `JAKTOOL/cmmc` open-source project emits a POA&M as CSV; RegScale tracks a 180-day SLA at enterprise price.

**Why still attractive.** It is a two-week build that pairs with 4.3, and the ineligibility guard is a genuinely non-obvious piece of knowledge worth encoding.

**Paid customization potential.** Low to moderate.

---

### 4.7 — ESP Register and CRM-to-SSP Insert Generator

**Intended user.** The compliance owner at a supplier that outsources IT, and the MSP itself.

**Problem solved.** Problem 6. 32 CFR 170.19(c)(2) requires the ESP relationship and its CRM to be documented in the supplier's SSP; assessors expect the CRM *incorporated*, not attached; "our MSP handles security" fails.

**Current workflow.** An MSP contract in a drawer. Maybe a CRM PDF, attached as an appendix. Often nothing.

**Proposed workflow.** Register each external service provider: name, services, whether it processes/stores/transmits CUI, its category under 32 CFR 170.19 (CSP handling CUI, non-CSP ESP, Security Protection Asset), and its FedRAMP posture (Moderate authorized / equivalency with a Body of Evidence / neither). Import or transcribe the CRM into a per-requirement responsibility split — provider, customer, or shared. The tool then **generates SSP-ready narrative language** per requirement describing the split, and flags every requirement where responsibility is unassigned or where an ESP touching CUI lacks FedRAMP standing.

**Required inputs.** ESP inventory. CRMs (PDF or spreadsheet). FedRAMP status.

**Expected outputs.** An ESP register. A per-requirement responsibility matrix. Generated SSP insert language. A red-flag report (ESP handling CUI without FedRAMP Moderate or documented equivalency; requirements with no owner).

**Essential features.** The 32 CFR 170.19 category decision aid. Per-requirement responsibility capture. SSP language generation. FedRAMP posture flagging, including the six equivalency criteria from the December 2023 DoD CIO memo. Gap report.

**Deliberately excluded.** Live FedRAMP Marketplace lookups (fragile; ship a periodically refreshed snapshot instead). Contract management. Vendor risk scoring. MSP tooling integration.

**AI.** **Optional, narrow:** parsing a heterogeneous CRM PDF into a per-requirement table. CRM formats vary wildly between providers, which is exactly where extraction earns its place. Output must be presented for confirmation, never accepted silently.

**Why a spreadsheet would not suffice.** The generation of SSP-ready language and the FedRAMP flagging logic are the value; the matrix itself is spreadsheet-shaped.

**Complexity.** **Small to medium.**

**Learning difficulty.** Low.

**Value.** Closes a whole class of assessment findings, and forces the FedRAMP question early — before a supplier discovers mid-assessment that its email host disqualifies it. This is precisely the failure MORSECORP settled $4.6M over: third-party email hosting "without requiring and ensuring that the third party met security requirements equivalent to the FedRAMP Moderate baseline."

**Risks and constraints.** FedRAMP status changes; a stale snapshot could mislead, so date-stamp it prominently and refuse to assert current status. Microsoft's CRM is not publicly downloadable, so the tool cannot ship it and must guide the user through obtaining it.

**Existing products and substitutes.** Buried inside platform features. FutureFeed publishes good written guidance on CRM-versus-SRM but the register itself is a platform feature. Nothing standalone or free.

**Why still attractive.** High differentiation, small build, and it addresses a failure mode with a $4.6M settlement attached. Also sellable to MSPs, who need to *author* CRMs for every DIB client and currently do it ad hoc — that is a second customer segment from one build.

**Paid customization potential.** Very high, especially the MSP-side variant: an MSP with forty DIB clients needs consistent, per-client CRMs and SSP inserts, which is a recurring service, not a one-off.

---

### 4.8 — Flowdown Tracker: subcontractor level determination and attestation collection

**Intended user.** Purchasing or contracts at a small prime or higher-tier supplier.

**Problem solved.** Problem 7. Flowdown is mandatory at all tiers, level determination follows 32 CFR 170.23, and there is no way to independently verify a supplier's claim — so the only defence is a complete, dated paper record.

**Current workflow.** A questionnaire emailed when someone remembers, a clause in the PO, and a spreadsheet that falls behind.

**Proposed workflow.** Register each supplier and each PO or subcontract, flagging whether it conveys FCI, CUI, or neither. The tool applies the 170.23 decision table to determine the required level, generates the appropriate questionnaire and flowdown clause packet, tracks issuance and receipt, records the supplier's reported SPRS score, assessment date, and affirmation with expiry dates, and produces a pre-award gap list of suppliers who are unverified or expired.

**Required inputs.** Supplier list. PO/subcontract register with an FCI/CUI flag. Returned attestations.

**Expected outputs.** A required-level determination per supplier. Questionnaire and clause packets. An attestation register with expiries. A pre-award gap list. An audit trail proving flowdown was executed.

**Essential features.** The 170.23 decision table. Questionnaire generation. Attestation register with expiry tracking. Pre-award blocking list. Export for prime portal submission (Exostar CCRA, supplier registration forms).

**Deliberately excluded.** Any attempt to verify a supplier's score independently — it is not possible, and pretending otherwise would be the tool's worst feature. No supplier portal. No procurement workflow. No integration with the prime portals themselves.

**AI.** **Inappropriate.** A decision table and a register.

**Why a spreadsheet would not suffice.** Genuinely marginal. The value is the encoded 170.23 logic, the generated packets, and expiry alerting. A well-built Excel workbook with formulas would get most of the way — and this concept should be honest about that in its own README.

**Complexity.** **Small.**

**Learning difficulty.** Very low.

**Value.** Real but modest, and mostly defensive: the record is what protects the buyer if a supplier's attestation turns out false. Note that the required-level rows referencing C3PAO assessment are **currently inoperative** for new solicitations because of the suspension, which the rule table must reflect with an effective-date dimension.

**Risks and constraints.** The 170.23 table is directly in the path of whatever the task force recommends in September. Build it as versioned data.

**Existing products and substitutes.** Exostar (effectively mandatory for many, because primes route supplier attestation through it — Lockheed uses the CCRA module; current pricing unverified and the tier descriptions I found still reference CMMC 1.0-era Levels 3 and 5). Supplier-risk platforms at enterprise price. Spreadsheets.

**Why still attractive.** Low build cost, and it lands on a live commercial pressure: five named primes issued supplier cyber mandates between February 2025 and December 2025, and they are continuing regardless of the DoD suspension. A supplier that cannot answer a Lockheed questionnaire quickly loses the PO whatever the regulation says.

**Paid customization potential.** Moderate — prime-specific questionnaire and export formats.

---

### 4.9 — Clause Decoder: what does this contract actually obligate me to do

**Intended user.** The owner or contracts administrator reading a solicitation.

**Problem solved.** Problem 9. Two clause numbering systems are live simultaneously, 7019 is eliminated by class deviation but still published as current on acquisition.gov, 7025 is new, Rev 2 is frozen by class deviation while the FAR CUI proposed rule specifies Rev 3, and Phase 2 requirements must be stripped from active solicitations. 32% of small DIB contractors do not know which level applies to them.

**Current workflow.** Read the clause list. Search the internet. Ask the buyer. Guess.

**Proposed workflow.** Upload or paste a solicitation or contract. The tool identifies cybersecurity-relevant clauses across **both** numbering systems (252.204-7012, 7021, 7025, 252.240-7997, FAR 52.204-21 / 52.240-93, FAR 52.240-6 / -7) and produces a one-page plain-language obligation sheet: which standard and revision applies, whether self-assessment or certification is required and whether that requirement is currently suspended, what must be in SPRS and by when, incident reporting obligations and the current portal, flowdown obligations, and a scoping question set to work through. Every statement cites its source.

**Required inputs.** A solicitation or contract PDF, or a pasted clause list.

**Expected outputs.** A one-page obligation summary with citations. A scoping questionnaire. A watch-list of unresolved items (for example: does this contract convey CUI, and has the CO said so).

**Essential features.** A clause knowledge base spanning old and new numbering with effective dates and deviation status. Clause extraction from PDF. Plain-language obligation mapping. Citations throughout. **A prominent as-of date and a stated review cadence** — a decoder with stale rules is worse than no decoder.

**Deliberately excluded.** Legal advice, and the tool must say so plainly. Bid/no-bid analysis. Any non-cyber clause. Contract management.

**AI.** **Needed, for extraction only.** Clause lists appear in wildly variable formats — incorporated by reference, in tables, in scanned attachments — and this is where a model genuinely outperforms regex. But the **obligation mapping must be a hand-maintained rules table**, never generated: an LLM asked what DFARS 252.240-7997 requires in August 2026 will confabulate, because the renumbering post-dates most training data. Extraction by model, interpretation by table.

**Why a spreadsheet would not suffice.** Clause extraction from PDFs and a citation-backed narrative output are not spreadsheet work.

**Complexity.** **Medium**, and it carries the highest maintenance burden of the ten — the rules table must be reviewed whenever the regulation moves, which in 2026 is often.

**Learning difficulty.** Very low to use.

**Value.** Addresses the very first step of the workflow, where a wrong answer propagates into everything downstream. Also the single best lead-generator for the rest of the catalog: a supplier who runs this and learns it needs Level 2 self-assessment immediately needs 4.3, 4.4, and 4.1.

**Risks and constraints.** Maintenance is the whole risk. If the rules table goes stale it becomes actively harmful, so it needs a visible as-of date, a changelog, and an honest statement that it is not legal advice. This is the concept most dependent on sustained attention, which is a real argument for ranking it below the others despite its usefulness.

**Existing products and substitutes.** Law firm client alerts (excellent, free, not tool-shaped, and not company-specific). GovCon clause databases at subscription price. Consultants at **$360/hour** (Totem's published rate).

**Why still attractive.** Nothing free and tool-shaped exists, and the regulatory churn of 2026 makes it more valuable than it would have been in any other year.

**Paid customization potential.** Good — client-specific obligation playbooks, quarterly rule-pack maintenance as a subscription service. Note that the maintenance service is arguably the *real* product here.

---

### 4.10 — 72-Hour Kit: incident reporting readiness

**Intended user.** The owner, and whoever would discover an incident.

**Problem solved.** Problem 8. The ICF requires roughly twenty fields including DUNS, CAGE, and contract numbers; authentication requires an ECA credential from one of two issuers with identity proofing and per-machine installation; the clock is 72 hours from discovery; and nobody obtains the credential until it is too late.

**Current workflow.** None. The plan is to figure it out during the incident.

**Proposed workflow.** Pre-stage every ICF field that can be known in advance — DUNS, CAGE, contract numbers, role contacts — in a printable, offline-readable readiness sheet. Track whether an ECA credential exists, from which issuer, on which machines and user accounts, and when it expires, with lead-time warnings. When an incident is declared, start a countdown checklist: preserve images and monitoring data for 90 days, complete the remaining ICF fields, submit via the ICF portal, transmit to DC3 by encrypted email or DoD SAFE, notify the prime with the incident report number per DFARS 252.204-7012(m)(2), and record the report number.

**Required inputs.** Company identifiers. Contract register. Contact roster. ECA credential inventory.

**Expected outputs.** A pre-filled ICF worksheet. A one-page printed readiness card (it must work when systems are down — that is the point). A countdown checklist with timestamps. An incident record.

**Essential features.** Pre-staged field storage. ECA inventory with expiry and lead-time alerts. The 72-hour countdown. The 90-day preservation reminder. Prime notification tracking. **Offline/printable operation as a first-class requirement.**

**Deliberately excluded.** Incident detection or response tooling. Forensics. Automated submission. SIEM integration.

**AI.** **Inappropriate.**

**Why a spreadsheet would not suffice.** Barely — a spreadsheet plus a printed page would cover most of it. The genuine increments are the ECA lead-time alerting and the countdown with timestamps.

**Complexity.** **Small.** A weekend build.

**Learning difficulty.** Trivial.

**Value.** Low expected frequency, high consequence, near-zero cost. The honest framing: this is a checklist product, and its value is that it causes the ECA credential to be obtained *before* it is needed.

**Risks and constraints.** The reporting process changed once already (DIBNet decommissioned June 6, 2025), so the process rules must be versioned and dated. Ranked last because frequency is genuinely low.

**Existing products and substitutes.** Incident response plan templates inside the documentation bundles. Nothing that tracks ECA readiness.

**Why still attractive.** Trivial to build, and it fixes a specific documented failure mode that no other tool addresses.

**Paid customization potential.** Low.

---

## 5. Opportunity ranking

Each concept scored 1–5 on ten criteria; maximum 50.

**Criteria:** SEV = severity of the problem · FRQ = frequency of use · ROI = clarity of return · LRN = ease of learning · IMP = ease of implementation · SCP = ability to stay narrowly scoped · DIF = market differentiation · CUS = customization potential · DAT = availability of realistic test data · CNF = confidence in evidence

| # | Concept | SEV | FRQ | ROI | LRN | IMP | SCP | DIF | CUS | DAT | CNF | **Total** |
|---|---|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| 4.1 | **CUI Stamper** (batch drawing/document marking) | 4 | 5 | 5 | 5 | 4 | 5 | 5 | 5 | 4 | 4 | **46** |
| 4.3 | **Defensible SPRS** (score + signed record) | 5 | 3 | 5 | 5 | 5 | 5 | 4 | 3 | 5 | 5 | **45** |
| 4.2 | **CUI Intake Register** (+ mismarking notice) | 4 | 5 | 4 | 5 | 4 | 4 | 5 | 4 | 3 | 5 | **43** |
| 4.4 | **SSP-320** (objective-level SSP compiler) | 5 | 4 | 5 | 3 | 3 | 4 | 5 | 5 | 4 | 5 | **43** |
| 4.7 | **ESP Register + CRM→SSP generator** | 4 | 3 | 4 | 4 | 4 | 5 | 5 | 5 | 3 | 5 | **42** |
| 4.6 | **POA&M Clock** | 4 | 3 | 4 | 5 | 5 | 5 | 3 | 3 | 4 | 5 | **41** |
| 4.8 | **Flowdown Tracker** | 4 | 4 | 4 | 5 | 5 | 4 | 3 | 4 | 3 | 5 | **41** |
| 4.9 | **Clause Decoder** | 5 | 4 | 4 | 5 | 3 | 3 | 5 | 4 | 4 | 4 | **41** |
| 4.5 | **Evidence Locker** (freshness clock) | 4 | 5 | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 4 | **40** |
| 4.10 | **72-Hour Kit** | 5 | 1 | 3 | 5 | 5 | 5 | 4 | 3 | 3 | 5 | **39** |

### The top three explained

**1. CUI Stamper — 46.** This wins on the least glamorous grounds: it is the only concept that is simultaneously daily-frequency, small enough to finish, unambiguously undersupplied, and **immune to the regulatory uncertainty hanging over this entire market**. The obligation flows from DoDI 5200.48, DoDI 5230.24, and 32 CFR Part 2002 — none of which the CMMC Reform Task Force is reviewing. Whatever lands in September, engineering drawings containing controlled technical information will still need a `CUI` banner on every sheet, a designation indicator block, and a Distribution Statement B-through-F. The before-and-after demo is the most persuasive in this report: forty sheets, correctly marked, in the time it takes to describe the problem. And the specific DoD rule that the category does *not* go in the banner — which contradicts the general federal marking handbook and which practitioners get wrong in the direction of looking more rigorous — is exactly the kind of encoded knowledge that makes a small tool worth more than the hour it saves. Its 4 on evidence confidence rather than 5 reflects one honest gap: the marking *rules* are primary-source verified, but no practitioner has published hours-per-package, so the time-savings claim is inference.

**2. Defensible SPRS — 45.** The cleanest risk-reduction story available. Free calculators already produce the number, so the product is not the arithmetic — it is the dated, hashed, evidence-linked, diffable record of how the number was reached and by whom. That record is precisely what MORSECORP and LOGZONE did not have. DOJ has now settled false-score cases at $4.6M and $507,144, and the July suspension made self-attestation the *only* gate, which multiple law firms read as raising rather than lowering FCA exposure for the named Affirming Official. It scores a 3 on frequency because formally this happens annually, and a 3 on customization because there is not much to customize. Everything else is a 5. It is also two to three weeks of work over a fixed 110-row table, which makes it the best effort-to-value ratio in the set.

**3. Tie at 43 — CUI Intake Register and SSP-320,** and they should be read as opposite bets.

*CUI Intake Register* is the tactical bet: small, daily, and sitting on the one problem in this market that is unambiguously the government's own fault. The DoD Inspector General found 48% of sampled DoD documents lacking a designation block; suppliers are asked to scope against markings that are not there. That will not be regulated away quickly, and if the FAR CUI proposed rule finalizes as written, its 72-hour mismarking notification requirement turns this tool from useful into necessary. It pairs so naturally with the Stamper that they are arguably one product with two verbs.

*SSP-320* is the strategic bet: the largest build, the only concept that breaks the catalog's one-hour learning guideline, and the one carrying real dataset-maintenance liability. But it attacks the defect five independent C3PAO assessors named as the most common cause of failure, in a market where roughly a third of organizations fail Phase 1. And it would produce something that does not currently exist anywhere: a curated, openly licensed, machine-readable 800-171 catalog at objective granularity. `usnistgov/oscal-content` has 800-53 rev4 and rev5 and SP 800-172 rev3 but **not SP 800-171**; one repo exists solely to note that absence. Whoever builds that catalog owns the foundation every other tool in this space imports.

### What to investigate next

**Investigate 4.1 (CUI Stamper) first**, for three reasons. Its regulatory basis is the most stable thing in this market. It is buildable and demonstrable inside a month. And it is validatable without an interview: the rules are published in DoDI 5200.48, DoDI 5230.24, and the CDSE job aids, so correctness can be established against primary sources before any practitioner is asked anything — which is the right sequencing when practitioner access is the scarce resource.

**Then 4.3 (Defensible SPRS)**, which is nearly as small and completes a coherent two-tool opening: one for the daily document work, one for the annual attestation.

**Hold 4.4 (SSP-320) until after the task force reports around September 13, 2026.** Its dataset is the most expensive artifact in this report and the most exposed to a change in the assessment framework. Investigating it means, concretely, hand-curating the 320-objective mapping — that is not work to start eight days before a possible framework overhaul.

**One thing worth doing in the next seven days regardless:** the CMMC Reform Task Force RFI closes **August 14, 2026**, and its published responses will eventually be the single best corpus of first-person small-supplier pain statements in existence. Whether or not anyone responds to it, the responses are worth reading when they surface, and their existence should shape the timing of everything above.

---

## 6. Validation plan

### For 4.1 — CUI Stamper

**Questions for practitioners** (document control, quality managers, engineering managers at 15–150 person defense manufacturers):

- Walk me through what physically happens to a customer drawing package from the moment it arrives to the moment a machinist has it at the spindle. Where does it get printed, copied, marked?
- Who applies CUI markings today, with what tool, and how long does a typical package take?
- Have you ever had a customer, a prime, or an assessor comment on your markings? What did they say?
- Do you put the CUI category in the banner? *(This is the diagnostic question — a "yes" confirms the specific error the tool prevents, and a "no, why would I" tells me the market is more sophisticated than the evidence suggests.)*
- Which distribution statement do your drawings carry, and who decided that?
- What happens to derivative documents — setup sheets, travelers, inspection reports, FAI packages? Do those get marked?
- If a tool marked a 40-sheet package in one pass, what would you need to trust it enough to use it on real CUI?

**Who to interview.** Quality and document-control managers at small AS9100-certified machine shops; NIST MEP center cybersecurity advisors (they see dozens of these shops and are publicly funded to help); Registered Practitioner Organizations serving 20–50 person manufacturers; the ProShop ERP community, which has published practitioner guidance on CUI in machine shops and therefore has customers who have thought about it.

**Search terms for further research.** `CUI marking drawing title block distribution statement`; `DoDI 5230.24 distribution statement B drawings contractor`; `"designation indicator" drawing sheet CUI machine shop`; `batch stamp PDF CUI banner footer`; `Bluebeam batch stamp CUI compliance`; `CUI marking error assessor finding`; and per-CAD-system searches for title-block CUI templates.

**Sample files needed.** Public-domain DoD drawings carrying real distribution statements (DTIC and NAVSEA publish some). Synthetic multi-sheet drawing packages at A through E sizes. Examples of correctly and incorrectly marked documents from the CDSE and dodcui.mil training aids — those double as a test oracle.

**Prototype that would validate it.** A command-line script that takes a folder of PDFs and one JSON marking profile and emits marked PDFs plus a log. No UI. Run it against the DoD training-aid examples and check that the output matches the published correct markings, and that the known-bad examples are flagged. That is a weekend of work and it settles the core technical and correctness questions before any UI exists.

**Assumptions most likely to make it fail.**

1. **That marking is done manually.** If most shops have already built CAD title-block templates that emit correct markings at plot time, the incremental value collapses. *This is the assumption I would test first, and it is the one I am least sure of.*
2. That a stamped overlay is acceptable to customers and assessors, rather than markings needing to originate in the CAD file.
3. That PDF is the operative format — if packages arrive as native CAD or as scanned raster, the technical approach changes.
4. That title-block geometry is regular enough to place markings reliably without per-drawing intervention.
5. That shops will run an unfamiliar executable against CUI at all. Local-only operation and readable source help; a security-conscious document controller may still refuse.

### For 4.3 — Defensible SPRS

**Questions.** How was your current SPRS score produced, by whom, and what record of that exists today? Could you reconstruct, per requirement, why you scored what you scored and on what evidence? Who is your Affirming Official, and what did they see before signing? Have you re-scored since the July suspension? Did you know the SSP being "Not Met" produces No Score rather than a deduction? Do you know which two requirements carry partial credit?

**Who to interview.** Affirming Officials — owners and presidents, not IT staff, because the exposure is theirs. RPOs who compute scores for multiple clients. Former DIBCAC assessors. Government-contracts attorneys who have advised on SPRS accuracy (the law firms publishing on LOGZONE are a warm list).

**Search terms.** `SPRS score wrong DIBCAC assessment difference`; `False Claims Act SPRS score misrepresentation settlement`; `DoD Assessment Methodology 1.2.1 partial credit 3.5.3 3.13.11`; `SPRS "no score" system security plan not met`; `affirming official personal liability CMMC`.

**Sample data needed.** The DoD Assessment Methodology 1.2.1 PDF (the authoritative weight list). The SPRS entry tutorial transcript (the ten fields). A synthetic set of determinations exercising both partial-credit branches and the SSP gate. The DOJ press releases as narrative test cases — MORSECORP's 104-versus-−142 is a perfect regression fixture.

**Prototype.** A single-file local web page implementing the 110-row scoring table with the two partial-credit branches and the SSP gate, producing a score, a JSON snapshot, and a hash. Validate against the published examples and against −203 as the floor. One weekend.

**Assumptions most likely to make it fail.**

1. **That anyone wants a durable record.** A defensible record is only attractive to someone who believes they might be audited. If small suppliers regard FCA exposure as abstract, the value proposition evaporates and the tool becomes just another calculator. *This is the load-bearing assumption.*
2. That FutureFeed at ~$2,196/year has not already saturated the segment that cares.
3. That an owner will personally engage with a 110-row questionnaire rather than delegating it — and if they delegate, the provenance value weakens.
4. That the scoring methodology remains stable through the September review.

### Cross-cutting validation note

The one thing I could not do in this cycle, and the single most valuable next step: **read the actual small-supplier voices.** Reddit, LinkedIn, and Elsmar Cove were all unreachable from this environment, so not one raw practitioner forum post is cited anywhere in this report. Everything in Section 3 rests on government documents, peer-reviewed work, named practitioners quoted in trade press, published vendor prices, and DOJ filings. That is a respectable evidence base — arguably a more reliable one than forum sentiment — but it systematically over-weights what institutions say and under-weights what a frustrated quality manager says at 6pm.

Two concrete fixes, in priority order:

1. **regulations.gov comment bodies** on docket **DOD-2023-OS-0063** and the FAR CUI docket (**FAR Case 2017-016**). These contain hundreds of named small-supplier comments written in their own words. My subagent hit the DEMO_KEY rate limit; a real regulations.gov API key unlocks them, and this is the highest-value single unblock available.
2. **The CMMC Reform Task Force RFI responses**, closing August 14, 2026. If any portion is published, it will be the best corpus of first-person burden statements this market has ever produced — generated by the government asking exactly the right question.

Also unretrieved and worth a manual read: the two National Defense Magazine pieces, "VIEWPOINT: AI, Crippling CMMC Regulations Converge on Small Businesses" (April 17, 2026) and "Pentagon's CMMC Pause Draws Praise, Criticism from Industry" (July 14, 2026). Both are JavaScript-rendered and returned empty.

---

## 7. Cross-industry patterns

Seven transferable patterns, each named with the specific backlog markets it adapts to.

### Pattern A — Objective-decomposition compiler

A standard's headline requirements decompose into finer determination statements, and practitioners author to the headline while being graded on the leaves. The tool inverts the structure: one narrative plus one dated evidence pointer per leaf, roll up to the headline using the standard's own conjunction rule, generate the conventional document, and emit a coverage report on uncovered leaves.

**Transfers to:** *Contract manufacturers serving FDA-regulated medical devices (ISO 13485 / QMSR)* — clauses decompose into auditable sub-requirements with the same authoring gap, and the February 2026 QMSR transition creates the same "which revision applies" problem. *Special inspection agency accreditation consultants (IAS AC291, ANAB, WABO)*. *Calibration and metrology service providers* under ISO/IEC 17025. *Workforce development boards and WIOA subrecipients*. *Federally qualified health centers — HRSA Section 330 grant compliance*.

### Pattern B — Weighted-score recorder with provenance and diff

A regulator publishes a scoring formula; the practitioner self-computes and submits; the submission carries legal weight; and nothing in the ordinary workflow preserves *why* each input was what it was. The tool computes exactly per the published method, captures per-input provenance and date, hashes an immutable snapshot, and diffs against the prior submission.

**Transfers to:** *Premium audit and payroll classification consulting* — classification decisions drive premium and are disputed retrospectively. *Property tax consulting and assessment appeal firms*. *Medicare Advantage risk adjustment / HCC coding at small groups* — RADV audits are precisely retrospective provenance challenges. *Ready-mix concrete producer quality control departments* (mix design compliance records). *Asphalt plant producer quality control technicians*.

### Pattern C — Batch document marking with jurisdiction rule packs

A document must carry a specific set of marks whose composition depends on jurisdiction, document type, and customer, applied per page across large packages, following rules that are published but contradictory between sources. The tool holds versioned rule packs, applies marks deterministically, validates against the rules, and logs what it did.

**Transfers to:** *Independent specification writers and master-spec maintenance consultants*. *Delegated-design submittal coordination (specialty engineers of record)* — seal, signature, and jurisdiction-specific statements per sheet. *Structural engineering firms, 5–30 staff* (multi-state sealing rules). *Environmental laboratories producing regulator EDD deliverables* (per-state header and format rules). *Title abstracting and independent title search contractors*.

### Pattern D — Incoming-deliverable defect register with auto-drafted notice to originator

A practitioner receives deliverables from an upstream party who is *obligated* to prepare them correctly and frequently does not. The receiver bears downstream consequences and has a clocked duty to notify. The tool logs every receipt, assesses it against the expected form, and drafts the notice back upstream.

**Transfers to:** *Architectural construction administration desks at small A/E firms* — incoming submittals with missing or wrong data. *County recorder offices — document intake, indexing and rejection handling* (the same pattern from the rejecting side). *Mortgage post-closing QC and trailing document vendors*. *Supplier quality engineering at OEMs and primes (receiving side of supplier deliverables)*. *Industrial distributors and metal service centers issuing material test reports* (mirror image: the sender's obligation).

### Pattern E — Evidence-freshness clock keyed to a control or task set

A recurring obligation set requires artifacts refreshed on a cadence the standard does not specify. Practitioners gather in a panic before inspection. The tool registers artifacts against the control set with owner, capture date, cadence, and final-versus-draft status, and surfaces staleness continuously.

**Transfers to:** *Fire protection inspection, testing and maintenance (ITM) contractors under NFPA 25* — frequency-driven records where the cadence *is* the standard. *Calibration and metrology service providers / in-house gage management* (calibration due dates are the canonical case). *Radiation safety officer services and portable gauge licensee compliance*. *Consortium / third-party administrators (C-TPAs) for DOT drug and alcohol programs*. *Title 24 acceptance test technicians and acceptance testing providers*.

### Pattern F — Third-party responsibility-matrix register with document-insert generation

Work is split with an outside party; a regulator or reviewer requires the split to be documented *inside* the practitioner's own deliverable, not merely attached; and "the vendor handles that" is an insufficient answer. The tool registers each third party, captures a per-requirement responsibility split, flags unassigned requirements, and generates insert language for the primary document.

**Transfers to:** *Delegated-design submittal coordination* — the responsibility split between EOR and delegated engineer is exactly this artifact. *Integrated facilities management providers serving corporate real estate*. *Fiscal sponsorship organizations administering awards for sponsored projects*. *Third-party claims administration (TPA) and self-insured program operations*. *Building automation and controls contractors (BAS integrators)* — the split with the mechanical contractor and the owner's IT.

### Pattern G — Obligation decoder across a renumbered or forked regulatory regime

A regulation is renumbered, deviated from, or forked across jurisdictions such that the published text no longer describes the live obligation. The tool extracts the citations actually present in the practitioner's document and maps them through a hand-maintained, date-stamped rules table to plain-language obligations. **Extraction by model, interpretation by table** — never the reverse.

**Transfers to:** *Certificate-of-insurance compliance from the holder side (GCs, property managers, municipalities)* — requirement sets forked per contract with no canonical text. *Energy code compliance consultants and Title 24 documentation shops* (code cycle versus permit date). *Multi-state charitable solicitation registration compliance* (fifty forked regimes). *Building permit expediting and code consulting firms*. *Truck permitting and registration service agencies (IRP, IFTA, OS-OW, state permits)*.

---

## 8. Sources and confidence

### Verified findings

Primary government and judicial sources, and peer-reviewed work.

**Regulation and program**
- 32 CFR 170.21, POA&M and conditional status — https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-D/part-170/section-170.21
- 32 CFR 170.22, affirmation — https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-D/section-170.22
- 32 CFR 170.19, external service providers and the CRM mandate — https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-G/part-170/subpart-B/section-170.19
- 32 CFR 170.23, subcontractor flowdown — https://www.law.cornell.edu/cfr/text/32/170.23
- DFARS 252.204-7012 — https://www.acquisition.gov/dfars/252.204-7012-safeguarding-covered-defense-information-and-cyber-incident-reporting.
- DFARS 252.204-7025 (NOV 2025) — https://acquisition.gov/dfars/252.204-7025-notice-cybersecurity-maturity-model-certification-level-requirements.
- DFARS 252.204-7019 (NOV 2023), still published as current despite reported elimination — https://www.acquisition.gov/dfars/252.204-7019-notice-nistsp-800-171-dod-assessment-requirements.
- DoD Assessment Methodology v1.2.1 (June 24, 2020) — https://www.acq.osd.mil/asda/dpc/cp/cyber/docs/safeguarding/NIST-SP-800-171-Assessment-Methodology-Version-1.2.1-6.24.2020.pdf
- CMMC Assessment Guide Level 2, v2.13 (Sept 2024) — https://dodcio.defense.gov/Portals/0/Documents/CMMC/AssessmentGuideL2.pdf
- CMMC Level 2 Scoping Guide — https://dodcio.defense.gov/Portals/0/Documents/CMMC/ScopingGuideL2.pdf
- DoD CIO CMMC FAQs v6 — https://dowcio.war.gov/Portals/0/Documents/CMMC/FAQsv6.pdf
- SPRS NIST SP 800-171 entry tutorial transcript (the ten fields) — https://www.sprs.csd.disa.mil/pdf/training/NIST_SP_800-171_Entry-Transcript.pdf
- NIST SP 800-171A Rev 3 — https://csrc.nist.gov/pubs/sp/800/171/a/r3/final
- NIST SP 800-171 3.12.4 requirement text — https://csf.tools/reference/nist-sp-800-171/r2/3-12/3-12-4/

**CUI marking**
- DoDI 5200.48 — https://www.dodcui.mil/Portals/109/Documents/Policy%20Docs/DoDI%205200.48%20CUI.pdf
- DoD CUI Markings training aid (the "no category in the banner" rule) — https://www.dodcui.mil/Portals/109/Documents/Desktop%20Aid%20Docs/Cleared%20CUI%20Training%20Aid%20-%20%20Markings%202024.pdf
- DoDI 5230.24, distribution statements — https://www.esd.whs.mil/portals/54/documents/dd/issuances/dodi/523024p.pdf
- DTIC Guide to Marking Documents (verbatim Distribution Statement A–F text) — https://discover.dtic.mil/wp-content/uploads/2023/08/GuideToMarkingDocuments_Jan2023.pdf
- CDSE CUI Quick Marking Tips (SF 901/902/903) — https://www.cdse.edu/Portals/124/Documents/jobaids/CUI-Quick-Marking-Tips.pdf

**Audits and oversight**
- DODIG-2026-047, CUI dissemination controls — 48% of a 300-document sample lacked a designation indicator block — https://media.defense.gov/2026/Feb/04/2003870671/-1/-1/1/DODIG-2026-047_REDACTED%20SECURE.PDF · coverage: https://federalnewsnetwork.com/defense-news/2026/04/dod-still-failing-to-properly-mark-cui-data-years-after-initial-audit/
- GAO-26-107955, CMMC program — 92 C3PAOs, 633 assessors against ~200,000 DIB companies; assessment costs $4,042–$117,768 — https://files.gao.gov/reports/GAO-26-107955/index.html
- NDIA public comment, docket DOD-2023-OS-0063 — "close to two-thirds of the 320 assessment objectives … are not eligible for POA&Ms" — https://downloads.regulations.gov/DOD-2023-OS-0063-0252/attachment_1.pdf
- SBA Office of Advocacy, CMMC Reform Task Force RFI (responses due Aug 14, 2026) — https://advocacy.sba.gov/2026/07/20/dow-requests-information-for-cmmc-reform-task-force/
- SBA on the Phase II suspension — https://legacy.sba.gov/article/2026/07/13/sba-commends-us-department-wars-suspension-cmmc-phase-ii-small-defense-contractors

**DOJ enforcement**
- LOGZONE Inc., $507,144, June 18, 2026, DCMA score −170 — https://www.justice.gov/opa/pr/alabama-defense-contractor-agrees-pay-507144-resolve-false-claims-act-liability-relating
- MORSECORP Inc., $4.6M — claimed 104, actual −142 — https://www.justice.gov/opa/pr/defense-contractor-morsecorp-inc-agrees-pay-46-million-settle-cybersecurity-fraud
- DOJ FY2025 FCA statistics — https://www.justice.gov/opa/media/1424126/dl
- Ice Miller DOJ Cyber-Fraud tracker — https://icemiller.gjassets.com/content/uploads/2025/10/DOJ-Cyber-Fraud-Tracker_2025-10-01.pdf

**Peer-reviewed**
- Therrien & Hastings, Dakota State University, arXiv 2602.09905 — assessor evidence-sampling survey; 71% report no C3PAO sampling methodology; 71% observed inconsistency; sampling proposals ranged 1–3% to 95–100% — https://arxiv.org/html/2602.09905v1

**Named practitioners on the record**
- V. Amira Armond (Kieri Solutions; cmmcaudit.org) — "300–600 hours" to write policies and gather proof — https://www.cmmcaudit.org/cmmc-allowable-cost-discussion/
- Jacob Hill (Summit 7) — contractors "probably 100, 150 points less than what you thought"; Under Secretary Duffey's ~$150,000 average; DoW CIO Kirsten Davies on "burdensome red tape-driven check-the-box" — https://govciomedia.com/where-the-pentagons-cmmc-overhaul-could-go-next/
- Callye Keen (CEO, Kform) — the equipment-versus-compliance capital decision — https://defensescoop.com/2026/07/17/pentagon-task-force-to-review-cmmc-hits-the-ground-running/
- Five named C3PAO assessors on the 110-versus-320 SSP defect (vendor-hosted, attributed quotes) — https://secureframe.com/blog/cmmc-implementation-challenges-lessons-learned
- Scott Jack (E-N Computers, RPO) — GRC tool criticisms; "dozens of Excel spreadsheets" — https://www.encomputers.com/2024/02/best-grc-cmmc/
- NIST MEP, Micro-Precision Technologies — 15 employees, $20k workforce + $60k systems, $500k sales retained — https://www.nist.gov/mep/successstories/2023/cmmc-compliance-was-key-micro-precision-technologies-inc
- ProShop ERP — CUI circulation on a shop floor — https://proshoperp.com/blog/3-common-sense-tips-for-managing-cui-in-a-machine-shop/

**Suspension mechanics and legal analysis**
- Federal News Network — https://federalnewsnetwork.com/cybersecurity/2026/07/pentagon-suspends-cmmc-phase-two-requirements-launches-review-of-program/
- WilmerHale — https://www.wilmerhale.com/en/insights/client-alerts/20260720-pentagon-suspends-cmmc-phase-2-requirements-and-launches-review-of-cybersecurity-certification-program
- Hunton, on rising FCA exposure — https://www.hunton.com/government-contracts-intelligence-briefing/dow-suspends-cmmc-phase-ii-nist-sp-800-171-self-assessment-becomes-the-interim-standard-with-rising-false-claims-act-exposure
- ArentFox Schiff, the seven RFI questions — https://www.afslaw.com/perspectives/alerts/cmmc-reform-task-force-rfi-defense-contractors-have-chance-shape-federal
- Mayer Brown, FAR CUI proposed rule (Rev 3, 72-hour mismarking notice) — https://www.mayerbrown.com/en/insights/publications/2026/07/far-council-proposes-revised-cui-safeguarding-and-incident-reporting-framework-while-dow-pauses-cmmc-implementation
- Crowell, on the Rev 2 class deviation — https://www.crowell.com/en/insights/client-alerts/miss-me-with-rev-3-says-dod-dod-issues-class-deviation-linking-dfars-7012-to-nist-sp-800-171-rev-2
- CMMC.com, what still applies — https://www.cmmc.com/newsroom/cmmc-phase-2-suspension

**Market and pricing**
- Alluvionic small-contractor survey — 50% lack documented policies; 32% don't know their level; 15% have lost business; $120k+ annual sustainment — https://alluvionic.com/small-contractors-share-where-they-stand-on-cmmc/
- CyberSheath / Merrill Research 4th annual — 1% fully prepared; 17% negative SPRS scores — https://markets.financialcontent.com/clarkebroadcasting.mymotherlode/article/bizwire-2025-10-1-new-study-reveals-only-1-of-defense-contractors-fully-ready-for-imminent-cmmc-deadline
- FutureFeed published pricing — https://futurefeed.co/pricing/
- Totem published service and enclave pricing — https://www.totem.tech/cybersecurity-compliance-pricing/
- ComplianceForge CMMC Bundle 2, $10,530 — https://complianceforge.com/bundle/nist-800-171-cmmc-bundle-2-L3
- Kieri KCD, "more than 240 of the 320 assessment objectives" — https://www.kieri.com/kieri-compliance-documentation-kcd-cmmc/
- GCC High pricing after July 1, 2026 — https://secureframe.com/blog/gcc-high-pricing
- FedRAMP Moderate equivalency, six criteria — https://secureframe.com/blog/fedramp-equivalency-cmmc
- GCC High shared responsibility, 53/56/1 split — https://secureframe.com/blog/cmmc-shared-responsibility-model
- CRM versus SRM; "our MSP handles security" will not satisfy — https://futurefeed.co/mastering-responsibility-matrices/cybersecurity/
- Prime supplier mandates (RTX, Lockheed, Boeing, Elbit, Northrop) with dates — https://secureframe.com/blog/prime-contractor-cmmc-compliance
- DIBNet decommissioned June 6, 2025; ICF portal — https://www.getpeerless.com/blog/dod-retires-dibnet-new-icf-portal
- DC3 ECA credential instructions — https://www.dc3.mil/Portals/100/Documents/DC3/Missions/DCISE/DCISE%20Slick%20Sheets/DCISE-DIBNet-ECA-Instructions%203.0.pdf
- Reuters/Yahoo analysis on supplier non-compliance and exit — https://finance.yahoo.com/news/analysis-cybersecurity-rules-us-defense-110251610.html

**Open source landscape**
- `JAKTOOL/cmmc` — 38 stars, MIT, local-only SSP/POA&M generator — https://github.com/JAKTOOL/cmmc
- `usnistgov/oscal-content` — contains 800-53 and SP 800-172 rev3, **not** SP 800-171 — https://github.com/usnistgov/oscal-content
- `FATHOM5CORP/oscal` — exists because "NIST has not yet published similar OSCAL content for SP 800-171" — https://github.com/FATHOM5CORP/oscal
- `mattj23/cmmc-gen-model` — 800-171A crosswalk generator — https://github.com/mattj23/cmmc-gen-model
- `oscal-compass/compliance-trestle` — 265 stars, generic OSCAL — https://github.com/oscal-compass/compliance-trestle
- Awesome OSCAL index — https://github.com/oscal-club/awesome-oscal

### Strong inferences

Well-supported but resting on secondary sources, arithmetic reconciliation, or convergent evidence rather than a single primary citation.

1. **The count of 320 determination statements.** Asserted consistently by at least five independent sources, and Kieri's "more than 240 of the 320" is a commercial party quantifying against it. But **not found stated in any NIST or DoD primary document**, including CMMC Assessment Guide L2 v2.13. Every downstream design in Section 4 assumes it; a builder should derive the count directly from NIST SP 800-171A rather than trust it.
2. **The −203 floor.** Reconciles arithmetically only if 3.12.4 is treated as a gate rather than a 1-point deduction: 44×5 + 14×3 + 51×1 = 313, and 110 − 313 = −203. Consistent with DoD FAQ v6 ("Receive 'No Score' if system security plan is marked 'Not Met'") and DOJ's own recitation of the range in the LOGZONE release. Note the SPRS entry form accepts −205 as an input bound, which is wider than the methodology's floor.
3. **The RFO clause renumbering, and its conflict with published DFARS text.** The renumbering is reported consistently by multiple practitioner and law-firm sources; acquisition.gov still publishing 7019 as current is directly confirmed. The reconciliation — that class deviations do not alter published DFARS text — is inference, not a quotation from the deviation memo, which was inaccessible.
4. **That documentation, not the audit fee, is the cost centre.** Converging from three directions: DoD's own self-assessment-only estimate is still $34,277 initial for a small entity; Summit 7 states roughly two-thirds of total cost is untouched by suspending C3PAO audits; and the C3PAO fee itself is ~$31,234 of a ~$102,000 certification estimate. Each source alone is arguable; together they are persuasive.
5. **That horizontal GRC platforms are not where this market lands.** Every search for practitioner tool comparisons returned vendor listicles. Combined with the Keysight finding that only 3% of contractors use automated security validation tools, the "dozens of Excel spreadsheets" quote, and Kiteworks/Coalfire finding 23% of small orgs had approved CMMC budgets against 62% of large orgs, the working picture is Word plus Excel plus possibly one CMMC-native tool plus an MSP. Not directly verified.
6. **That the Phase 2 suspension provides little commercial relief.** Five named primes issued supplier mandates between Feb and Dec 2025, and Summit 7 states L3Harris, Lockheed and Boeing continue demanding Level 2 independently of the suspension. Convergent, but no survey measures post-suspension prime behaviour.
7. **Time savings for the CUI Stamper.** The marking rules are primary-source verified; the hours-per-package figure is not published anywhere. The value claim is inference from task structure.

### Tentative hypotheses requiring practitioner validation

Stated explicitly because acting on them without validation is how a catalog builds the wrong thing.

1. **That CUI marking is done manually rather than via CAD title-block templates.** The single highest-stakes unvalidated assumption in this report, since concept 4.1 ranks first on the strength of it. If shops already emit correct markings at plot time, 4.1's value collapses to validation and exception reporting. **Test this first.**
2. **That screenshot gathering and evidence staleness are top irritants.** Universally assumed in vendor marketing. I searched specifically and found **no verifiable practitioner statement on either**. The peer-reviewed assessor survey explicitly does not cover them. Concept 4.5's premise rests partly on this, which is part of why it ranks ninth.
3. **That small suppliers perceive FCA exposure as personally real.** Concept 4.3's entire value proposition depends on the Affirming Official believing an audit could happen to them. Two settlements in fourteen months is a thin base rate, and the tool is worthless to someone who has not internalized it.
4. **That a small supplier will run an unfamiliar local executable against CUI.** Every concept here is designed local-only for exactly this reason, but a security-conscious document controller may still refuse — and being security-conscious is the whole point of the market.
5. **That the September 2026 task force recommendations will not invalidate the CMMC-apparatus-dependent concepts.** Concepts 4.6 and 4.8 encode rules the task force is explicitly reviewing. The mitigation is architectural: versioned, date-stamped rule tables rather than hardcoded logic.
6. **That an aggregate DIB exit count exists.** It does not. GAO frames supplier exit as an unmitigated *risk*, not a measured fact; DoW's own memo asserts CMMC is "actively forcing innovative new entrants and small businesses to opt out"; NDIA's Vital Signs 2026 (1,177 respondents, 615 small businesses) mentions CMMC exactly once, in a government-shutdown staffing context. The only hard figure is Alluvionic's 15% who have "already lost business," and lost business is not exit.
7. **That the market for these tools survives a favourable September outcome.** If the task force materially reduces small-supplier obligations, demand for concepts 4.3 through 4.8 softens. Concepts 4.1 and 4.2 do not depend on CMMC at all, which is the strongest single argument for their ranking.

### A note on what this report is not

No raw practitioner forum post is cited anywhere in it. Reddit returned HTTP 403 on every endpoint tried, Elsmar Cove threads rendered without post bodies, and LinkedIn is not fetchable. Rather than paraphrase forum sentiment from memory and dress it as evidence, I substituted source classes that carry comparable practitioner weight and are verifiable: DOJ filings, GAO and DoD Inspector General reports, a peer-reviewed assessor survey, named practitioners quoted on the record, and published vendor prices. That is arguably a more reliable base than forum sentiment — but it systematically over-weights institutions and under-weights the frustrated quality manager, and every opportunity in Section 4 should be read with that bias in mind.
