# Flood Zone / FEMA Elevation Certificate and LOMA–LOMR Consulting
## Angle: narrow-subspecialty

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market claimed** | Flood zone / FEMA elevation certificate and LOMA-LOMR consulting |
| **Angle** | narrow-subspecialty |
| **Claim ID** | `08d5b219` |
| **Date** | 2026-08-07 |
| **Report** | `reports/2026-08-07-flood-zone-elevation-certificate-loma-lomr-consulting-narrow-subspecialty.md` |
| **Backlog remaining after this claim** | 282 assignments |

### Why this assignment over the others available

The ledger held 283 open assignments across 163 markets, of which 18 markets had at least one completed report. Selection followed the stated preference order.

**(a) Breadth first.** This market had zero completed entries. It is adjacent to `Land surveying firms` (completed, core-practitioner-workflow, score 45) but is a genuinely distinct buyer: the flood specialist is credentialed differently (CFM rather than, or in addition to, PLS), sells a different deliverable, is paid per-certificate rather than per-project, and has a regulatory counterparty (FEMA and the local floodplain administrator) that ordinary boundary and topographic surveying does not.

**(b) Evidence strength.** This was the deciding factor. Very few markets in the backlog offer a *published, quantified* error rate for the exact artifact a proposed tool would validate. Here one exists: an analysis of 5,082 residential Elevation Certificates found **68.4% contained at least one error and 44% contained two or more**, averaging two errors per certificate. On top of that, the governing rule set is public and already written as a checklist (the CRS Elevation Certificate review checklist), the reference data is a free public API (FEMA's National Flood Hazard Layer REST services), and the source document is a *fillable PDF with named form fields*. That combination — quantified defect rate, published rule set, free authoritative reference data, machine-readable input — is rare and makes the feasibility claims in Section 4 checkable rather than hopeful.

**(c) Angle diversity.** Completed reports skew to `core-practitioner-workflow` (7 of 18). `narrow-subspecialty` was the least represented at 3 of 18. This assignment corrects that skew.

**(d) Timing.** Two dated events make this cycle unusually informative. The current Elevation Certificate form **expired 30 June 2026**, five weeks before this report, and FEMA's renewal notice for it published in the Federal Register on **1 June 2026** with a comment period that closed 31 July 2026. Separately, the NFIP's authorization **expires 30 September 2026**, seven weeks out, after having already lapsed once during the autumn 2025 shutdown. A market in the middle of a form transition and an authorization cliff is a market where document-version and compliance-evidence tooling has unusually visible value — and also one where a researcher must be careful not to mistake temporary noise for durable demand. Both effects are treated explicitly below.

**A note on what I did not choose and why.** `Certified payroll and prevailing wage compliance` and `Fire protection ITM under NFPA 25` were the two strongest alternatives, both with excellent evidence. Both are `core-practitioner-workflow`, the already-overweighted angle, and both remain in the backlog with their notes intact for a future cycle.

---

## 1. Market examined

### Industry

The niche sits at the intersection of land surveying, civil/water-resources engineering, floodplain administration, and property insurance. It exists because of one federal program — the National Flood Insurance Program (NFIP) — and one federal map product, the Flood Insurance Rate Map (FIRM). Everything transacted here is either (i) evidence about where a specific structure sits relative to a mapped Base Flood Elevation, or (ii) a request to change the map.

### The practitioner roles

Four distinct roles produce or consume the same small set of documents. They are separate buyers with separate budgets, which matters for any product decision.

**1. The elevation-certificate producer.** A licensed land surveyor (PLS), or in some states a professional engineer or architect, who visits a structure, shoots elevations against a benchmark, photographs the building, classifies its foundation against FEMA's building diagrams, and certifies FEMA Form FF-206-FY-22-152. Typically a sole practitioner or a 2–15 person survey firm. In coastal and riverine counties, ECs can be a meaningful and highly repeatable revenue line rather than an occasional favor.

**2. The flood-zone consultant / LOMA shop.** A CFM-credentialed specialist, sometimes housed inside a survey firm, sometimes a standalone practice serving title agencies, lenders, investors, and homeowners. They read Flood Insurance Study profiles to interpolate a Base Flood Elevation at a specific station, compare a structure's Lowest Adjacent Grade against it, and prosecute a Letter of Map Amendment to remove the property from the Special Flood Hazard Area. One observed firm advertises a traditional LOMA at roughly **$150 and 6–8 weeks**, or an expedited eLOMA at roughly **$400 and 5–10 business days**, and explicitly positions itself against the "industry-standard 1-page flood report" sold by determination vendors. Firm size: 1–10.

**3. The map-revision engineer.** A water-resources PE at a small-to-midsize civil firm who prepares CLOMR and LOMR (MT-2) packages for developers, DOTs, and municipalities: hydrologic and hydraulic modelling, certified topographic work maps, annotated FIRMs, project narratives. Firm size: 5–100, with the flood group often being 2–8 people.

**4. The community floodplain administrator (FPA).** The reviewer. Usually a building official, planner, or public works engineer at a city or county, very often part-time on floodplain duties, who receives ECs at permit closeout, reviews them, files them, and answers to FEMA and to the Community Rating System. This is the *counterparty* to roles 1–3, and — importantly for this report — a plausible second customer for the same validation logic, with a different willingness to pay and a procurement process measured in months.

### Organization size most likely to benefit

Practitioner side: **1–15 employees**. Below that threshold there is no budget for anything; above roughly 100 the firm has an in-house GIS/IT group and buys or builds. Community side: municipalities under roughly 50,000 population, where floodplain administration is a fraction of one person's job.

### Type of user

Technically literate but not software-literate. Comfortable with CAD, survey data collectors, HEC-RAS, ArcGIS, and Excel. Hostile to subscriptions, cloud data custody, and anything requiring an IT department. Almost universally Windows. Deliverables are PDFs, and the professional seal on them carries personal license liability — a fact that shapes every product decision in Section 4.

### Scale sanity check, and a caution

FEMA's own Federal Register renewal notice for the Elevation Certificate (1 June 2026) estimates **3,517 respondents, 3,517 annual responses, 12,735 total annual burden hours (~3.6 hours per response), $680,316 total annual respondent cost**. Those numbers should not be taken at face value as market size. The per-response burden (3.6 hours) is plausible and useful. The response count is not: a single mid-size coastal county can receive hundreds of ECs a year, Florida has required statewide EC submission since 2017, and the analysed sample above alone was 5,082 certificates. The honest read is that FEMA's Paperwork Reduction Act accounting materially undercounts real EC volume, and that **the defensible number to build a business case on is the 3.6-hour-per-certificate burden, not the national count.** I flag this rather than resolve it; Section 6 lists it as a validation question.

---

## 2. How the work is performed

### 2A. Producing an Elevation Certificate

1. **Intake.** A homeowner, insurance agent, lender, closing agent, or builder requests an EC. The surveyor confirms the property is in or near a Special Flood Hazard Area and quotes. Market price runs **$170 to $2,000+, averaging around $600**, with $400–$1,000 typical; turnaround is commonly around **five business days**.
2. **Research (office).** Pull the FIRM panel, panel suffix, FIRM index date, panel effective/revised date, flood zone, and Base Flood Elevation for the site. Identify the community name and NFIP community ID. Determine whether the site is in a CBRS/OPA area, and for coastal sites whether it is landward or seaward of the Limit of Moderate Wave Action (LiMWA). Locate a vertical benchmark and establish the datum.
3. **Field.** Shoot top of bottom floor, next higher floor, bottom of lowest horizontal structural member (V zones), attached garage slab, lowest elevation of machinery and equipment servicing the building, and Lowest and Highest Adjacent Grade. Photograph the building — the 2022 form requires **four clear photographs**, up from the earlier "two, preferably four." Measure and count flood openings, now split into non-engineered and engineered categories with separate net/rated areas.
4. **Classification.** Choose the Building Diagram Number from FEMA's set (1A, 1B, 2A, 2B, 3, 4, 5, 6, 7, 8, 9). This single judgment call propagates through the rest of the form and is a leading source of downstream error.
5. **Form completion.** Fill Sections A, B, C, and D. If the datum of the BFE differs from the datum of the survey, apply and *document* a conversion factor — a requirement reinstated on the 2022 form after being absent since 2012. Seal and sign.
6. **Delivery.** PDF to the requester. Often the community never receives a copy unless the permit process forces it — a documented, structural gap in municipal records.

### 2B. Reviewing an Elevation Certificate (community side)

The FPA opens the PDF and checks it against a checklist. The authoritative one is the CRS Elevation Certificate review checklist published at CRSresources.org. It is not a completeness checklist; it is a **cross-field consistency** checklist. The rules that matter:

| Check | Fields compared | Rule |
|---|---|---|
| Datum alignment | B11 (BFE datum) vs C2 (survey datum) | Must match, or conversion factor documented with source in Comments |
| Diagram consistency | A7 vs the C2 items populated | Diagram must logically correspond to the elevations provided |
| Compliance | C2.a (top of bottom floor) vs B9 (BFE) | Determines compliance and insurance implications |
| Grade sanity | C2.f (LAG) vs C2.g (HAG) | HAG must not be lower than LAG |
| Required items | C2.a, C2.f, C2.g | Must always carry a value; others N/A if inapplicable |
| Section applicability | B8 (zone) | AO / AR-AO / A-without-BFE drive Section E instead of Section C |
| As-built compliance | G9.a vs G10.a | Local official's determination of permit compliance |
| Construction status | C1 | Only "Finished Construction" is acceptable for submitted certificates |
| Form edition | Footer | CRS reviewers enforce the form's official date strictly |

The reviewer then triages: **errors in Sections A, B, or C1 (community name, NFIP number, partial map/panel number) can be fixed by a Correction Memo signed by the floodplain administrator.** Errors elsewhere in Section C — a blank machinery/equipment field, a garage-versus-enclosure misclassification, a missing engineered opening certification, a missing or incomplete V Zone certificate — **require the surveyor to resubmit a corrected, resealed certificate.** An expired form edition requires reprinting the current form, copying Sections A/B/C across, completing Section G, and submitting both versions.

That triage rule — *which defects I can fix at my desk versus which force a round trip to a licensed professional* — is the single most operationally important thing in the entire review workflow, and it is currently held in the reviewer's head.

### 2C. Removing a property from the SFHA (MT-1: LOMA / LOMR-F)

Assemble the MT-1 package (Forms 1, 2, 3 as applicable), attach the Elevation Certificate or equivalent elevation data, the FIRM panel, deed or plat, and for fill-based requests the community acknowledgment. Submit through FEMA's Online LOMC portal, or, if the applicant is a Licensed Professional and the case is straightforward, through the **eLOMA** tool, which returns a determination immediately. FEMA states **60 days** from receipt of complete documentation for MT-1 determinations; LOMAs themselves carry no FEMA fee. Practitioners quote clients longer and charge a service fee for the assembly and the risk of a bounce.

A recent wrinkle worth noting: FEMA now permits **Base Level Engineering** data, accessible through the Estimated Base Flood Elevation viewer, to be used as the BFE source in LOMA submittals in unmapped or approximate-zone areas — which materially expands the population of properties a consultant can screen without commissioning new hydraulics.

### 2D. Revising the map (MT-2: CLOMR / LOMR)

The heavyweight process. Required package: MT-2 Forms 1, 2, 3 and payment; a project narrative explaining objectives and engineering judgments; hydrologic and hydraulic computations *plus the executable digital model files*; a certified topographic work map with floodplain delineations; an annotated FIRM; PE and/or PLS certification; community acknowledgment; property owner notification; and, for CLOMRs, Endangered Species Act compliance documentation.

The modelling must be built as a progression — **Duplicate Effective → Corrected Effective → Existing Conditions → Revised Conditions** — with water-surface elevations tying back to the effective study **within 0.5 foot** at the study limits, and all five recurrence intervals (10%, 4%, 2%, 1%, 0.2%) carried through.

Timelines, per a 2025 state-coordinator presentation: FEMA quotes **90 days** for MT-2 determinations; practitioners are told to **assume a minimum nine-month CLOMR timeline and two or more review rounds**, with the community unable to issue permits until the CLOMR is issued, and the eventual LOMR becoming effective 120 days after the second newspaper publication. FEMA's stated performance goal is **no more than two requests for additional information per case** — an implicit admission that rounds are the currency of this process.

Who reviews varies by state and by year. Kentucky became a FEMA LOMR Review Partner on 1 January 2024. Illinois's State Water Survey **paused** its LOMR review role for want of FY2025 Cooperating Technical Partner funding, pushing all new applications to FEMA's national contractor. A consultant working multi-state therefore faces a moving target of reviewers, checklists, and informal expectations.

### 2E. Software currently in use

| Layer | What they use | Assessment |
|---|---|---|
| Field data | Trimble / Leica / Carlson collectors, TBC, Carlson Survey | Mature, expensive, does not touch the EC form |
| Form completion | The FEMA fillable PDF in Adobe Acrobat or Bluebeam; office Word/Excel templates for the cover letter | Universal; zero validation |
| Flood data lookup | FEMA Map Service Center, NFHL Viewer, FIS profile PDFs | Free, authoritative, entirely manual |
| Submittals | FEMA Online LOMC portal, eLOMA | Government portal; validates its own fields, not your document |
| Hydraulics | HEC-RAS (free), HEC-HMS, occasionally proprietary 2D | Excellent engines, no submittal-packaging layer |
| Community-side records | Spreadsheets, network folders, permit systems; **Forerunner** as the one real vertical SaaS | Forerunner is genuinely good and genuinely aimed at *communities*, not practitioners |
| Tracking | Excel, Outlook, whiteboards | The default everywhere |

**On Forerunner specifically.** It is the incumbent worth taking seriously and worth being honest about. It ingests EC PDFs, auto-detects the form version across the 2009–2026 editions, extracts dozens of fields, geocodes to a property, and runs automated checks: required-field verification, format validation on dates/elevations/coordinates, flood-zone consistency against configured FIRM layers, address-format checking, and certification completeness. It reports processing in **1–5 minutes** against "hours of manual data entry," with human verification against the source PDF still required.

Three things follow from that, and they define the whitespace for everything in Section 4:

1. Forerunner is sold to **communities**, as a platform, on a municipal procurement cycle. The surveyor who *produces* the certificate — the party who eats the cost of a rejection — is not its customer and gets no pre-flight check.
2. Its published check list is largely **completeness and format**. The checks that catch the expensive errors are the **cross-field engineering-consistency** rules in the table above, plus authoritative-registry joins. Whether it runs those internally is not publicly documented; the published description does not claim them.
3. It does not touch MT-1 or MT-2 at all.

---

## 3. Most important problems, ranked

### Problem 1 — Elevation Certificates are wrong most of the time, and the producer finds out last

**Who:** The surveyor who sealed it, then the FPA who reviews it, then the property owner who paid for it.
**When:** At community review, days to weeks after delivery and payment.
**Evidence (verified):** Of 5,082 residential ECs analysed, **68.4% contained at least one error; 44% contained two or more; the average was two errors per certificate.** The five most frequent were: map/panel number mismatches ("Map/Panel numbers are long, typos are common in this field"); Lowest Adjacent Grade below BFE (frequently exposing a wrong Building Diagram Number underneath); regulatory lowest floor below Design Flood Elevation; lowest machinery elevation below DFE; and garages beneath the principal structure not documented as enclosures. County-level training materials independently name the same defects and add blank C2.e machinery fields, missing engineered-opening and V-Zone certificates, expired form editions, and wrong building diagrams.
**Currently handled by:** Manual checklist review at the community, with wide variation in reviewer skill — the same source notes some communities staff this with "staff members who are not trained to evaluate floodplain compliance," and that the organisations that do it well use "redundancy using multiple EC reviewers, checklists, and tools."
**Why inadequate:** The check happens after the money is spent, at the wrong end of the chain, by the party least able to fix it. The producer gets a rework request; the owner gets a delay; the reviewer absorbs the correspondence.
**Frequency:** Every certificate. Two-thirds of them generate at least one finding.
**Cost:** A resubmittal consumes surveyor office time on a fixed-price ~$600 deliverable — a plausible 10–25% margin hit per affected job — plus re-mobilisation if a field measurement is missing, plus permit-closeout or closing delay. At a 68% defect rate, a firm doing 200 ECs a year is fielding well over a hundred correction cycles annually.
**Confidence:** High. Quantified, and corroborated across independent community and association sources.

### Problem 2 — The most consequential errors are cross-field, not missing-field

**Who:** Reviewers and producers.
**When:** Throughout.
**Evidence (verified):** The CRS checklist's operative content is comparisons, not blanks: B11 datum against C2 datum; A7 building diagram against the C2 items actually populated; C2.a against B9; C2.f against C2.g; G9.a against G10.a; and zone-driven applicability of Section C versus Section E. The published error analysis reinforces it — a LAG-below-BFE flag was valuable primarily because it *surfaced a wrong Building Diagram Number*, i.e. the useful finding was two fields deep.
**Currently handled by:** Human inspection, or by automated tooling whose published checks are completeness- and format-oriented.
**Why inadequate:** A form can be 100% complete and internally contradictory. Datum mismatches in particular are silent: NGVD 1929 and NAVD 1988 differ by roughly a foot in much of the country — enough to flip a compliance determination — and nothing about a filled form announces the error.
**Frequency:** Every certificate carries the risk; the datum-conversion field returned to the form in 2022 specifically because it was being lost.
**Cost:** This is the error class that produces *wrong compliance determinations* rather than paperwork churn — a structure certified as compliant that is not, with the surveyor's seal on it. Professional liability, not just rework.
**Confidence:** High for the rule set (published). Medium for the frequency split between completeness and consistency errors — the published analysis does not break its 68.4% down that way. Section 6 treats this as the most important open question.

### Problem 3 — Multi-round regulatory submittals with 90-day rounds

**Who:** Map-revision engineers; developers waiting on permits; FPAs who cannot issue permits until a CLOMR lands.
**When:** Every CLOMR/LOMR.
**Evidence (verified):** FEMA quotes 90 days for MT-2 and 60 days for MT-1 *from receipt of complete documentation*. A 2025 state presentation instructs practitioners to assume a nine-month minimum CLOMR timeline and two-plus rounds, and identifies FEMA's performance goal as no more than two additional-information requests per case. The same source enumerates the failure modes: incomplete submittals, poor documentation of model inputs and engineering judgments, inadequate project narratives, topographic data inferior to or inconsistent with the effective analysis, model-to-map disagreement, missing or unsigned community acknowledgments, and improper property-owner notification.
**Currently handled by:** Senior-engineer memory, agency checklists in PDF, and pre-submittal phone calls to the state coordinator.
**Why inadequate:** Every failure mode listed is a *completeness or consistency* defect, not a hydraulics defect. The engineering is usually right; the package is wrong. And the review landscape shifts under the consultant — a state that reviewed LOMRs last year may have handed them back to FEMA's national contractor this year for grant-funding reasons.
**Frequency:** Lower volume than ECs, far higher stakes per event.
**Cost:** One avoidable round is a 90-day slip in a project's critical path, against carrying costs on a development site. This is the largest per-event dollar figure in the market.
**Confidence:** High.

### Problem 4 — Datum handling and an approaching national datum change

**Who:** Every producer and reviewer of an elevation on a FEMA form.
**When:** Whenever the BFE datum and the survey datum differ, and prospectively across the whole market.
**Evidence (verified):** The 2022 EC reinstated conversion-factor documentation, with the source required in Comments. The CRS checklist makes datum alignment a named cross-field rule. Separately, NOAA is replacing NAD 83 and NAVD 88 with NATRF2022 (and regional equivalents) plus the NAPGD2022 geopotential datum; the October 2024 Federal Register notice put the change at **2025 or 2026**, with supporting tools and services following **within five years**.
**Currently handled by:** VERTCON lookups pasted into Comments, or institutional habit.
**Why inadequate:** Unautomated, undocumented, and about to be disrupted. Every archived elevation on every EC in every community's files is expressed in a datum that is being retired, while the FIRMs those elevations are compared against will migrate on a different schedule.
**Frequency:** Continuous, rising.
**Cost:** Today: silent compliance errors. Over the transition: a systematic reconciliation burden across entire municipal EC archives.
**Confidence:** High on the datum rules and the NSRS timeline. **Low on the transition's practical shape** — the Federal Register notice explicitly does not address impacts on surveyors, floodplain mapping, or FEMA, and FEMA has not published a coordinated migration plan. This is a real hazard for anyone building on it; treated as a hypothesis in Section 8.

### Problem 5 — LOMA eligibility is screened by hand, and the unqualified cases are the expensive ones

**Who:** Flood-zone consultants and the survey firms feeding them.
**When:** At intake.
**Evidence (verified):** The consultant workflow is documented explicitly — read the county Flood Insurance Study profiles, interpolate a BFE, compare to the structure elevation, decide LOMA eligibility. Fee points observed: ~$150 / 6–8 weeks traditional, ~$400 / 5–10 business days eLOMA. FEMA's Online LOMC and eLOMA both require complete documentation before the clock starts. Base Level Engineering data is now an accepted BFE source in approximate zones.
**Currently handled by:** Manual FIS profile reading, NFHL Viewer, and experience.
**Why inadequate:** On a $150–$400 engagement, a single bounced application or a case that was never eligible destroys the margin. The screen is the profitable part of the job and the least systematised.
**Frequency:** Every inquiry, most of which never become paid work.
**Cost:** Modest per case, high in aggregate; the real loss is unbillable screening labour.
**Confidence:** Medium-high. Fee and cycle-time figures come from a single firm's public marketing and should be treated as one data point, not a market rate.

### Problem 6 — CRS Activity 310 credit rests on a 90% accuracy threshold nobody measures until the audit

**Who:** FPAs in the ~1,500 CRS communities.
**When:** At the cyclical verification visit.
**Evidence (verified):** Activity 310 offers up to **38 points (312.a), 48 points (312.b), and 30 points (312.c)**. Communities must maintain written Construction Certificate Management Procedures covering collection, review, correction, storage, and public availability, produce them at every verification visit, and hold to the **90% document accuracy threshold** in Section 301. The published characterisation of the ongoing effort is "high." Communities lose credit when procedures lack required detail or the accuracy threshold is missed.
**Currently handled by:** Spreadsheets and folders; the accuracy rate is discovered, not monitored.
**Why inadequate:** A CRS class step is a **5% flood-insurance premium discount for every policyholder in the community**. That is a large, community-wide, recurring dollar amount hinging on a document-quality metric that is measured once every few years, retrospectively, by an outside verifier.
**Frequency:** Continuous exposure, episodic discovery.
**Cost:** A dropped class costs the community's policyholders in aggregate far more than any software; the FPA's personal exposure is reputational and budgetary.
**Confidence:** High on the mechanics. Medium on FPA willingness to buy — municipal procurement is slow and Forerunner already sells here.

### Problem 7 — Correction-loop bookkeeping

**Who:** FPAs, and the surveyors on the receiving end.
**When:** After every failed review.
**Evidence (verified):** The memo-versus-resubmit triage is explicit in county training material: A/B/C1 errors take a Correction Memo signed by the FPA; other Section C errors require surveyor resubmittal; expired forms require a specific reprint-and-transcribe procedure with both versions submitted. Communities are further instructed to match permit lists against submitted ECs, name files by street address, and not combine certificates into single PDFs — housekeeping rules that exist precisely because the loop is leaky.
**Currently handled by:** Email and memory.
**Why inadequate:** Open corrections fall between the permit system and the EC file. A certificate-of-occupancy can issue against an uncorrected certificate.
**Frequency:** Follows directly from the 68.4% defect rate.
**Cost:** Small per event, relentless, and it is the mechanism by which the 90% CRS accuracy threshold is quietly missed.
**Confidence:** High.

### Problem 8 — Substantial Improvement / Substantial Damage determinations

**Who:** FPAs; adjacent to the consultants who advise owners.
**When:** Every permit on a pre-FIRM structure in the SFHA, and en masse after a flood.
**Evidence (verified):** The 50% rule is FEMA's most-litigated floodplain concept — there is a dedicated FEMA appeals docket for it and a widely-read industry explainer titled around its being "commonly misinterpreted." FEMA publishes a Substantial Damage Estimator tool for the damage side.
**Currently handled by:** Spreadsheets, appraisal or assessor values, and locally-defined cumulative lookback periods.
**Why inadequate:** The determination is a defensible-record problem: cost of improvement over market value of the structure (not the land), tracked cumulatively over a local lookback window, with a documented basis for both numbers. Existing tooling covers post-disaster damage, not routine improvement permitting.
**Frequency:** Ongoing, spiking after events.
**Cost:** A wrong determination means a non-compliant structure, an NFIP compliance finding against the community, and litigation.
**Confidence:** Medium-high on the problem; **lower on whether small communities will pay** for a tool rather than continue with a spreadsheet.

### Problem 9 — Documented, non-actionable: the EC coverage gap and the RR 2.0 demand question

Two findings are real but do not, on the evidence available, support a product.

*Coverage.* Even communities holding every EC ever filed represent "only a fraction of the city's built structures," because homeowners commission ECs only at purchase, refinance, or substantial renovation and **do not pass them to local government**. Florida legislated a fix in 2017 (mandatory submission to the state Division of Emergency Management); New Jersey municipalities run mail campaigns and negotiate group-purchase discounts with surveyors. This is an outreach and statutory problem, not a software problem, and I decline to invent an app for it.

*Demand.* Risk Rating 2.0 removed the EC from insurance rating on 1 April 2022. ECs remain required for floodplain-management compliance, CRS, and LOMAs, and remain useful for rating because the insurer must use the First Floor Height **more favourable to the policyholder** — so a certified FFH that beats FEMA's modelled estimate still buys the owner money. But the *net* effect on EC volume since 2022 is not established by any source I found. Anyone sizing this market must resolve it. Section 6 makes it the first validation question.

---

## 4. Application opportunities

> Every concept below assumes: local-first, Windows-friendly, no mandatory cloud custody of client survey data, and no claim to substitute for professional judgment. The seal is the practitioner's; the tool advises.

---

### 4.1 — **ECheck** — Elevation Certificate pre-submittal validator

**User:** Surveyor/EC producer (primary). Community floodplain administrator (secondary).
**Problem:** Problems 1 and 2. Two-thirds of certificates carry an error, and the producer learns about it after delivery.
**Current workflow:** Fill the PDF → seal → deliver → wait → receive a correction request → rework.
**Proposed workflow:** Drop the completed PDF on the tool before sealing → 15-second report listing each finding with form-section citation, severity, and the specific rule → fix → seal → deliver clean.
**Inputs:** The completed EC PDF. Optionally an internet connection for NFHL lookups.
**Outputs:** A findings report (HTML/PDF) grouped as *blocking* / *review* / *informational*, each finding citing the field and the rule; plus a CSV of extracted field values.
**Essential features:**
- **AcroForm field extraction.** The 2022 EC is a fillable PDF with named fields. For any certificate produced digitally, extraction is deterministic — no OCR, no AI, no confidence scores.
- **Completeness rules:** C2.a / C2.f / C2.g always populated; N/A explicitly marked elsewhere; four photographs present; A7 diagram number valid; A5 lat/long present with horizontal datum.
- **Cross-field consistency rules** (the differentiator): B11 vs C2 datum with conversion factor and documented source; A7 diagram against the C2 items populated; C2.f ≤ C2.g; C2.a vs B9; zone-driven Section C vs Section E applicability; C1 = Finished Construction; C2.e machinery populated or justified.
- **Authoritative registry join:** lat/long from A5 → FEMA NFHL REST service → verify B1.b community ID, B4/B5 map panel and suffix, B6/B7 dates, B8 zone, and B9 BFE against what was typed. This kills the single most common error — panel-number typos — outright.
- **Form-edition and validity check:** identify the edition from the footer and compare against the signature date in Section D.
**Deliberately excluded from v1:** OCR of scanned/flattened certificates; batch processing; any database; any hosted storage; automatic form correction; Sections E/F/G/H/I beyond applicability checks.
**AI:** **Not needed, and adding it would be a defect.** Every rule is deterministic. AI becomes *optional* only in a later scanned-legacy-document module (see 4.9), where it is genuinely the right tool.
**Why not a spreadsheet:** The input is a PDF form, and the highest-value check is a live query against a federal GIS service. Neither is spreadsheet work.
**Complexity:** Small-to-medium. Python + pypdf/pdfplumber + `requests` against the NFHL REST endpoint; a rules file in YAML; a single-page HTML report. Realistically a few focused weeks to a credible v1.
**Learning difficulty:** Minutes. Drag, drop, read.
**Value:** If it removes even a third of correction cycles at a 68% defect rate, a 200-EC/year firm avoids ~45 rework loops. Against a 3.6-hour-per-certificate federal burden estimate and a ~$600 price point, that is real margin — and the liability reduction on wrong compliance determinations is worth more than the time.
**Risks / constraints:** Certificates contain property addresses and owner names — hence local-first, no upload. The tool must be unambiguous that it does not certify anything. NFHL service availability and schema drift require a cached-fallback path. Rules must be versioned per form edition, which is ongoing maintenance, not a one-time build.
**Existing products / substitutes:** Forerunner (community-side platform, published checks are completeness/format, 1–5 minute processing); the CRS checklist as a manual PDF; nothing at all aimed at the producer.
**Why still attractive:** The party who pays for an error has no pre-flight tool. The rule set is public. The reference data is a free federal API. The input format is machine-readable. And the incumbent's business model — municipal platform sales — makes a free, local, single-purpose producer-side checker an awkward thing for it to ship.
**Customisation potential:** High and immediate. Communities layer higher standards on the NFIP minimum — freeboard requirements above BFE, local Design Flood Elevation definitions, extra certifications. A paid "your community's rules" profile is the obvious first commercial engagement, and a firm working one county will pay for one.

---

### 4.2 — **Datum Bridge** — vertical datum reconciliation and conversion memo generator

**User:** Surveyors; community EC archives.
**Problem:** Problem 4. Silent datum mismatches; undocumented conversions; an approaching national datum change.
**Current workflow:** VERTCON in a browser, a number typed into Comments, sometimes without its source.
**Proposed workflow:** Enter or import site coordinates and elevations with their stated datums → tool computes the conversion, flags disagreement between B11 and C2, and emits a signed-ready conversion memo with method, model version, and source.
**Inputs:** Coordinates, elevation values, source and target datum identifiers. Batch CSV for archive work.
**Outputs:** Converted elevations, a per-record conversion memo, an exception list of records whose datums cannot be reconciled.
**Essential features:** NGVD29↔NAVD88 via NOAA VERTCON; geoid model selection and explicit versioning; batch mode for a community's archive; an NSRS-2022 **readiness report** flagging which records will need re-expression.
**Excluded:** Performing the NAPGD2022 transformation itself until NOAA ships the tooling; horizontal datum work; any survey adjustment.
**AI:** Inappropriate. This is geodesy.
**Why not a spreadsheet:** VERTCON is a grid-model lookup, not arithmetic, and the deliverable is a *documented* memo.
**Complexity:** Small for the EC use case; medium with batch archive mode.
**Learning difficulty:** ~30 minutes for a surveyor. Zero conceptual novelty.
**Value:** Prevents the highest-consequence silent error class and produces the documentation the 2022 form now demands.
**Risks:** **The NSRS timing risk is the whole risk.** The October 2024 Federal Register notice says "2025 or 2026" with tools following within five years and says nothing about FEMA. Building the readiness module ahead of NOAA's tooling and FEMA's guidance is speculative. Ship the VERTCON/documentation core, which is valuable today regardless; treat readiness as a later increment.
**Existing products:** NOAA VERTCON (free, web, single-point, no memo); CAD/GIS built-ins (present but not documentation-producing).
**Why still attractive:** Nothing produces the *documented conversion record* the form requires, and no one is positioned for the transition.
**Customisation:** Medium. State-plane and local vertical-control profiles.

---

### 4.3 — **LOMA Pre-Flight** — eligibility screener and MT-1 package assembler

**User:** Flood-zone consultants, LOMA shops, survey firms with a flood line.
**Problem:** Problem 5. Manual eligibility screening on a $150–$400 engagement.
**Current workflow:** Pull the FIRM, find the FIS profile, interpolate a BFE at the station, compare by hand, decide, assemble the package, submit, hope.
**Proposed workflow:** Address or coordinates → NFHL query returns zone, panel, effective date, and mapped BFE (with Estimated BFE / Base Level Engineering as the fallback in approximate zones) → enter LAG and lowest floor from the EC → tool returns a structure-versus-lot eligibility determination with the comparison shown → generates the MT-1 document checklist and pre-fills the fixed fields.
**Inputs:** Address/coordinates; LAG and LFE; property description; determination type sought.
**Outputs:** A go/no-go screening memo suitable for sending to the client; a package checklist; pre-filled form fields.
**Essential features:** NFHL and Estimated BFE queries; explicit structure-vs-lot logic; a plain-language client memo; a case checklist reflecting eLOMA versus Online LOMC paths.
**Excluded:** Auto-submission to FEMA (portal terms and licensure make this a bad idea); hydraulic modelling; LOMR-F fill certification logic in v1.
**AI:** Not needed for the determination. **Optional** for reading elevation values out of a legacy scanned EC.
**Why not a spreadsheet:** The BFE lookup is a spatial query against a federal service, and the deliverable is a client-facing memo.
**Complexity:** Medium.
**Learning difficulty:** ~1 hour. The user already knows the domain; they are learning a UI.
**Value:** Converts unbillable screening into minutes and prevents ineligible cases from consuming a fee-bearing slot.
**Risks:** **Liability is the constraint.** A LOMA determination is FEMA's to make; the tool must present a screen, never a determination. NFHL currency versus recently issued LOMCs is a genuine correctness trap — mitigated by joining FEMA's weekly LOMC batch files (published within about two weeks of each issue window, back to December 2021). Base Level Engineering data has documented accuracy limits and must be labelled as such.
**Existing products:** FEMA's own portal (submission, not screening); commercial flood-determination vendors (lender-oriented one-page reports, explicitly criticised by consultants as insufficiently rigorous); consultants' own spreadsheets.
**Why still attractive:** The screen is the profitable, judgment-bearing, unsystematised step, and the free federal data to automate it now exists.
**Customisation:** High. Per-firm memo templates and CRM/intake wiring.

---

### 4.4 — **MT-2 Submittal Auditor** — CLOMR/LOMR package completeness gate

**User:** Water-resources engineers at small and midsize civil firms.
**Problem:** Problem 3. Ninety-day rounds lost to package defects rather than engineering defects.
**Current workflow:** A senior engineer's mental checklist, an agency PDF checklist, and a pre-submittal call.
**Proposed workflow:** Point the tool at the submittal folder → it inventories against the MT-2 requirement matrix → produces a signed-off submittal register and an exception list before anything goes to FEMA.
**Inputs:** The submittal directory; case metadata (request type, community, state, watercourse).
**Outputs:** A submittal register PDF; an exception list; a reviewer-facing transmittal index.
**Essential features:** Requirement matrix covering MT-2 Forms 1/2/3 and payment, project narrative, H&H computations, **executable** model files (the guidance explicitly warns against truncated ones), certified topographic work map, annotated FIRM, PE/PLS certification, community acknowledgment signature presence, property-owner notification evidence, and ESA documentation for CLOMRs; a **recurrence-interval coverage check** (10%, 4%, 2%, 1%, 0.2%); a **tie-in check** confirming ≤0.5 ft agreement at study limits; and a state-reviewer profile, because who reviews changes (Kentucky took MT-2 in-house in January 2024; Illinois handed it back to FEMA's national contractor over FY2025 funding).
**Excluded:** Model review, hydraulics validation, or any opinion on the engineering.
**AI:** Not needed. Inventory and comparison. AI would introduce uncertainty into a task whose entire value is determinism.
**Why not a spreadsheet:** It reads a filesystem, parses model outputs for the tie-in and interval checks, and produces a dated register. A checklist that does not look at the actual files is the status quo that is failing.
**Complexity:** Medium.
**Learning difficulty:** ~1 hour.
**Value:** The highest per-event value in this report. One avoided round is 90 days off a project critical path against site carrying costs, and FEMA's own goal of ≤2 information requests per case tells you rounds are the binding constraint.
**Risks:** Requirements vary by FEMA region, state partner, and year — the tool must make its rule set visibly editable and dated rather than pretend to authority. Model-file parsing is version-sensitive (HEC-RAS in particular).
**Existing products:** Agency PDF checklists; state pre-submittal assistance (free, but a queue, and Illinois's example shows it can vanish with a grant cycle); nothing that reads the actual package.
**Why still attractive:** The documented failure modes are all clerical. Nobody sells the gate.
**Customisation:** Very high — a per-firm or per-state rule profile is a natural paid engagement, and this buyer bills hourly and understands paying for schedule certainty.

---

### 4.5 — **Effective-Model Diff** — H&H model progression comparator and tie-in reporter

**User:** The same water-resources engineers; the strongest "empower the expert" concept here.
**Problem:** The Duplicate Effective → Corrected Effective → Existing → Revised progression must be demonstrated, and reviewers reject model-to-map disagreement and undocumented judgments. The comparison tables are built by hand.
**Current workflow:** Export runs, paste into Excel, build the WSEL comparison table manually, write the narrative from memory.
**Proposed workflow:** Select the model runs → tool emits a cross-section-by-cross-section water-surface comparison across all five recurrence intervals, applies the 0.5 ft tie-in test at the study limits, and drafts the changed-parameter section of the narrative from the actual model deltas.
**Inputs:** HEC-RAS project files for each stage.
**Outputs:** Comparison tables (XLSX + PDF), a tie-in pass/fail exhibit, and a parameter-change log.
**Essential features:** Multi-run parsing; per-station deltas; the tie-in test; a parameter diff (n-values, geometry, flows) so the narrative documents what actually changed.
**Excluded:** Running or editing models; 2D in v1; anything other than HEC-RAS in v1.
**AI:** Inappropriate for the numbers. Defensible only as an optional draft-narrative assist over a table the tool computed deterministically — and even then, the engineer edits and seals.
**Why not a spreadsheet:** It is exactly what people do in a spreadsheet today, badly and slowly. The tool's value is parsing the native model files so the table cannot drift from the model.
**Complexity:** Medium — the highest technical risk in this report, all of it in HEC-RAS file-format handling across versions.
**Learning difficulty:** ~1–2 hours.
**Value:** Hours per submittal, and it directly attacks two named rejection reasons (poor documentation of model inputs and judgments; model-to-map disagreement).
**Risks:** File-format churn across HEC-RAS versions. A wrong comparison table is worse than no tool — this one needs a validation suite against known-good projects before it is fit to release.
**Existing products:** HEC-RAS itself (has comparison views, not submittal exhibits); firms' internal spreadsheets and macros.
**Why still attractive:** Genuinely differentiated, and the open-source HEC ecosystem plus existing Python RAS libraries means the parsing problem is tractable rather than novel.
**Customisation:** High — firm exhibit templates.

---

### 4.6 — **Correction Loop** — EC defect triage, memo generator, and resubmittal tracker

**User:** Community floodplain administrators.
**Problem:** Problem 7, feeding Problem 6.
**Current workflow:** Reviewer identifies errors, decides from memory whether a memo suffices, writes an email, and hopes to remember.
**Proposed workflow:** Findings in (from 4.1 or manual entry) → tool applies the published triage rule and splits them into *FPA Correction Memo* versus *surveyor resubmittal required* → drafts both documents → opens a tracked item against the permit → shows an aging list of open corrections that blocks closeout.
**Inputs:** The certificate, the findings, permit number, surveyor contact.
**Outputs:** A signed-ready Correction Memo; a surveyor request letter naming the exact fields; an open-corrections register with aging.
**Essential features:** The triage rule encoded (A/B/C1 → memo; other Section C, D → resubmittal; expired edition → the reprint-and-transcribe procedure with both versions retained); document generation; permit-list-to-EC reconciliation, which community guidance explicitly instructs administrators to perform; file-naming enforcement by street address, likewise explicitly instructed.
**Excluded:** Being a permit system. It reconciles against an exported permit list; it does not replace one.
**AI:** Not needed.
**Why not a spreadsheet:** A spreadsheet can hold the register but cannot apply the triage rule or generate the memo — and the triage rule is the expertise being packaged.
**Complexity:** Small.
**Learning difficulty:** Under an hour.
**Value:** Directly protects the CRS 90% accuracy threshold, which is the mechanism behind a community-wide 5% insurance discount step.
**Risks:** Municipal record-retention rules apply; the tool must export cleanly and never become the system of record. Procurement is slow — which is exactly why it should be free and open-source at the base tier.
**Existing products:** Forerunner (for communities already on it); email and memory for everyone else.
**Why still attractive:** Smallest build in this report, encodes a rule that is published but not implemented anywhere, and pairs naturally with 4.1 to form a producer-side/reviewer-side pair that share a rules engine.
**Customisation:** Medium — local memo templates and letterhead.

---

### 4.7 — **CRS 310 Evidence Builder** — accuracy sampling and verification-visit package

**User:** Floodplain administrators and CRS coordinators in CRS communities.
**Problem:** Problem 6. The 90% accuracy threshold is discovered at the audit rather than monitored.
**Current workflow:** Assemble binders before the verification visit; hope the sample holds.
**Proposed workflow:** Point at the EC archive → tool draws a defensible random sample, runs the 4.1 rule set over it, computes the accuracy rate against the 90% threshold with a documented methodology, and assembles the verification package alongside a Construction Certificate Management Procedures template covering every element the manual requires.
**Inputs:** The EC archive; community CRS class and activity elections.
**Outputs:** An accuracy report with sampling methodology; a findings list ranked by frequency (i.e. what to fix first); a written-procedures document; a verification-visit index.
**Essential features:** Defensible sampling; the accuracy computation; a written-procedures generator covering certificate types required, timing, responsible department, review process, correction procedure, storage, and public availability — the exact elements the manual demands be described.
**Excluded:** Other CRS activities; points forecasting; anything that implies it can predict a verifier's judgment.
**AI:** Not needed for the metric. **Warranted** for reading scanned legacy certificates in an archive that predates digital forms — and this is one of only two places in this report where AI earns its place, because OCR plus field-level extraction from heterogeneous scanned forms is not tractable with rules alone.
**Why not a spreadsheet:** The work is reading hundreds of PDFs and computing a metric over them.
**Complexity:** Medium.
**Learning difficulty:** ~1 hour for the report; the CRS knowledge is already the user's.
**Value:** Very high leverage, hard to attribute. A class step is a 5% premium discount for every policyholder in the community, recurring. Losing 310 credit costs points that must be replaced from somewhere.
**Risks:** Must not claim to predict ISO/CRS verifier outcomes. Depends on 4.1's rules being right, so the two are coupled. Municipal sales cycle.
**Existing products:** CRS resources and checklists (documents, not tools); Forerunner's CRS-oriented guidance content; consultants who do this manually as a service.
**Why still attractive:** The 90% threshold is a *number*, published, that no one currently computes continuously. Making an audit metric visible before the audit is a durable software pattern.
**Customisation:** High — and it converts naturally into a paid annual service engagement, which is the strongest recurring-revenue path in this report.

---

### 4.8 — **SI/SD Workbench** — Substantial Improvement / Substantial Damage determination record

**User:** Floodplain administrators; secondarily consultants advising owners.
**Problem:** Problem 8. The 50% rule decided on spreadsheets without an audit trail.
**Current workflow:** Spreadsheet comparing improvement cost to structure market value, with a locally-defined cumulative lookback.
**Proposed workflow:** Enter the structure, its value basis and source, and each improvement/repair with cost basis → tool computes the ratio, applies the community's cumulative lookback, and issues a determination letter with the full basis attached.
**Inputs:** Structure identification, market value with documented source, improvement costs, permit history.
**Outputs:** A determination letter, a cumulative-tracking record, and an appeal-ready basis file.
**Essential features:** Configurable lookback period and cumulative rules (these are local, not federal); value-basis documentation (assessor, appraisal, or cost approach — and which was used, and why); cumulative history per structure; a defensible letter.
**Excluded:** Damage estimation itself — FEMA publishes the Substantial Damage Estimator for that; this is the improvement-side and record-keeping complement.
**AI:** Not needed.
**Why not a spreadsheet:** The determination is a *defensible record over time*, not a calculation. Spreadsheets lose the cumulative history across staff turnover, which is precisely when the appeal arrives.
**Complexity:** Medium.
**Learning difficulty:** ~1 hour.
**Value:** High per event — a wrong determination is an NFIP compliance finding and a litigation exposure.
**Risks:** Local ordinance variation is wide; the tool must be configuration-driven and must not imply a federal answer. FEMA's own appeals docket on this topic is a reminder of how contested these get.
**Existing products:** FEMA SDE (damage side, post-disaster); local spreadsheets.
**Why still attractive:** Routine improvement permitting is the high-frequency case and is unserved.
**Customisation:** Very high — every ordinance differs, which is both the opportunity and the reason the free base version must be configurable rather than opinionated.

---

### 4.9 — **FFH Advantage** — legacy EC archive extraction and first-floor-height comparison

**User:** Insurance agents, portfolio owners, and consultants advising owners; secondarily communities digitising archives.
**Problem:** Under Risk Rating 2.0 the insurer must use the First Floor Height more favourable to the policyholder, but nobody can compare across a portfolio of scanned certificates sitting in folders.
**Current workflow:** Open PDFs one at a time, or do nothing.
**Proposed workflow:** Batch-ingest an archive of ECs across form editions → extract address, FFH-relevant elevations, diagram, and datum → produce a table flagging properties where a certified FFH is likely more favourable than a modelled estimate.
**Inputs:** A folder of EC PDFs, digital and scanned.
**Outputs:** A structured table plus a per-property flag with the source page cited.
**Essential features:** Multi-edition handling (the form has changed repeatedly; commercial tooling already spans 2009–2026 editions, which sets the bar); OCR for scanned certificates; confidence scores with page-level provenance so every value can be checked against its source.
**Excluded:** Quoting insurance; anything resembling a rate calculation.
**AI:** **Warranted.** Heterogeneous scanned forms across a decade and a half of editions are the canonical case where extraction models beat rules. Note the honest caveat from the incumbent's own documentation: even with automated extraction, reviewers must still "compare extracted values against the original PDF." Any design that hides that step is wrong.
**Why not a spreadsheet:** The input is a pile of scanned PDFs.
**Complexity:** Medium.
**Learning difficulty:** ~1 hour.
**Value:** Real for whoever owns a large archive; **weakest ROI story in this report** for a small practitioner, because the benefit accrues to the property owner rather than the tool's operator.
**Risks:** Extraction errors on a document that drives an insurance decision. Owner PII across a whole archive. And the underlying premise depends on the unresolved RR 2.0 demand question in Problem 9.
**Existing products:** Forerunner's ingestion (community-side, platform-priced); manual entry.
**Why still attractive:** Marginal as a standalone product. Its real value is as the **scanned-document module that unlocks 4.1 and 4.7 for legacy archives** — which is how I would sequence it.
**Customisation:** Medium.

---

## 5. Opportunity ranking

Each criterion scored 1–5. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of impl. | Narrow scope | Differentiation | Customisation | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 4.1 | **ECheck** — EC validator | 5 | 5 | 5 | 5 | 4 | 4 | 4 | 5 | 5 | 5 | **47** |
| 4.6 | **Correction Loop** — triage & tracker | 4 | 5 | 4 | 5 | 5 | 5 | 4 | 4 | 5 | 5 | **46** |
| 4.4 | **MT-2 Submittal Auditor** | 5 | 3 | 5 | 5 | 4 | 4 | 4 | 5 | 4 | 5 | **44** |
| 4.3 | **LOMA Pre-Flight** | 4 | 4 | 5 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | **41** |
| 4.2 | **Datum Bridge** | 4 | 4 | 4 | 5 | 4 | 5 | 4 | 3 | 4 | 4 | **41** |
| 4.7 | **CRS 310 Evidence Builder** | 4 | 2 | 5 | 4 | 3 | 4 | 5 | 5 | 3 | 4 | **39** |
| 4.8 | **SI/SD Workbench** | 5 | 4 | 5 | 4 | 3 | 3 | 3 | 4 | 3 | 4 | **38** |
| 4.5 | **Effective-Model Diff** | 4 | 3 | 4 | 3 | 2 | 3 | 5 | 4 | 3 | 4 | **35** |
| 4.9 | **FFH Advantage** | 3 | 3 | 3 | 4 | 3 | 4 | 3 | 3 | 3 | 3 | **32** |

### The top three

**1. ECheck (47).** It wins because the case for it is quantified rather than argued. A published analysis of 5,082 certificates puts the defect rate at 68.4%. The rules are already written down as a public checklist. The reference data is a free federal REST service. The input is a fillable PDF with named fields, so extraction is deterministic and needs no AI. And the party who bears the cost of the errors — the surveyor who sealed the document — has no tool at all, because the one real vertical product in this space is sold to the other side of the transaction. It is a small build with an unusually short path to a demonstrable before/after. Its one genuine weakness is maintenance: rules must be versioned per form edition, and the form just turned over.

**2. Correction Loop (46).** Scores nearly as high on a different basis — it is the *smallest* build here and encodes a rule that is published, operationally decisive, and implemented nowhere: which defects an administrator may fix by memo versus which force a resealed resubmittal. It also shares a rules engine with ECheck, so the pair together is barely more work than either alone and covers both sides of the same document exchange. Marked down slightly on ROI clarity because the benefit is diffuse (avoided drift against the CRS 90% threshold) rather than a line item.

**3. MT-2 Submittal Auditor (44).** Highest value per event by a wide margin — a 90-day round on a project critical path — and every documented rejection reason is clerical rather than technical, which is exactly what a checklist engine that reads the actual files can catch. Marked down on frequency (LOMRs are not daily work) and on the fact that requirements shift by region, state and year, which makes the rule set a maintained artifact rather than a fixed one. But this buyer bills hourly, understands schedule risk in dollars, and is the most likely of any user in this report to pay for customisation.

### What to investigate next

**ECheck, built against the CRS checklist rule set, with the NFHL join as the headline feature.** Two reasons beyond its score. First, its rules engine is the shared substrate for 4.6, 4.7, and the sampling in 4.9 — building it first makes three other concepts cheap. Second, it is the only concept here that can be validated in an afternoon: run it over a public archive of real certificates (several counties publish them) and see whether the measured defect rate lands anywhere near 68.4%. If it does, the premise is confirmed against independent data. If it does not, the whole thesis needs revisiting before a line of production code is written — which is exactly what a first investigation should be able to tell you.

---

## 6. Validation plan

### Questions for practitioners

**Surveyors / EC producers**
1. Of the ECs you sealed last year, roughly what fraction came back for correction? What were the top three reasons? *(Directly tests the 68.4% figure against lived experience.)*
2. When one comes back, what does it actually cost you — office time only, or do you re-mobilise to the field?
3. Would you run a checker before sealing, or does the seal mean you have already satisfied yourself?  *(The honest failure mode: professionals may read a pre-flight tool as an insult to their judgment. This question is designed to find that out early.)*
4. Has EC volume gone up, down, or sideways since Risk Rating 2.0 took effect in April 2022? *(The single most important unresolved question in this report.)*
5. What did the 30 June 2026 form expiry actually change for you day to day?
6. Would you send a client's EC to a cloud service? If not, is a local desktop tool acceptable, or does it need to be offline entirely?

**Floodplain administrators**
7. How many ECs do you review a year, and how long does each take?
8. Do you use the CRS checklist, a local one, or your own judgment?
9. How do you currently track open corrections, and has a CO ever issued against an uncorrected certificate?
10. What was your last CRS verification visit like, and did document accuracy come up?

**Map-revision engineers**
11. On your last five LOMRs, how many additional-information rounds did each take, and what triggered them?
12. What fraction of those triggers were package/clerical versus engineering?  *(Tests the central premise of 4.4.)*
13. Do you build the effective-model comparison tables by hand?

### Who to talk to
- ASFPM and state chapter members (FFMA in Florida, KAMM in Kentucky, and the Texas and New Jersey associations) — the chapter conference circuit is where these complaints are aired publicly.
- State NFIP coordinating offices, especially Kentucky DOW (a LOMR Review Partner since January 2024) and the Illinois State Water Survey (which paused its review role over FY2025 funding) — two ends of the same spectrum.
- CRS coordinators in Class 5–7 communities, who have the most points at risk.
- Small survey firms in coastal Florida, coastal New Jersey, and the Texas Gulf Coast, where EC work is high-volume.
- State surveying societies (NYSAPLS and equivalents) that publish EC guidance to members.

### Search terms for further research
`elevation certificate common errors [state] floodplain`; `EC review checklist community rating system 310`; `LOMR additional data request reasons`; `MT-2 submittal checklist [state]`; `no-rise certification requirements`; `CRS verification visit 310 documentation`; `substantial improvement cumulative lookback ordinance`; `HEC-RAS duplicate effective model FEMA submittal`; `eLOMA licensed professional audit`; `NAPGD2022 FEMA flood map datum transition`.

### Sample files and data needed
- **20–50 real completed ECs across editions.** These are public records; multiple counties publish EC archives online (Pima County's flood control district is one observed example). This is the test corpus, and it is obtainable today without asking anyone's permission.
- The current EC form and instructions, plus prior editions, for field-name mapping across versions.
- The CRS EC checklist from CRSresources.org as the authoritative rule source.
- An NFHL REST endpoint exercise, plus a batch of LOMC files from the Map Service Center for the currency join.
- Two or three complete, redacted MT-2 packages (state coordinators sometimes publish examples) for 4.4.
- A pair of HEC-RAS effective/revised model sets for 4.5.

### Prototype that would validate the idea
A command-line script that takes a folder of EC PDFs, extracts AcroForm fields, applies roughly fifteen rules — the six required-field checks and the nine cross-field consistency checks in Section 2B — queries the NFHL for each A5 coordinate, and emits a CSV of findings. **The measured defect rate on a real public archive is the validation.** If it approaches 68.4%, the premise holds and the rules are catching real things; if it comes out near zero, either the rules are wrong or the published statistic does not generalise, and either answer is worth knowing before building a product. This is a few days of work and it de-risks four of the nine concepts at once.

### Assumptions most likely to make this fail

1. **That surveyors will accept a checker.** They may not. The seal is a professional attestation, and a tool that second-guesses it can read as an accusation. Mitigation: position it as a delivery-QC step for the *firm*, not a judgment on the *surveyor*, and let it run silently as part of the package-out process.
2. **That EC volume survived Risk Rating 2.0.** Not established by anything I found. If volume has fallen sharply since April 2022, the frequency scores for 4.1, 4.2, 4.6, and 4.7 are all too high and the ranking changes.
3. **That the 68.4% figure generalises.** It is one analysis, of residential certificates, published by a company that sells EC software. The statistic is specific and internally consistent — 44% with two or more, averaging two per certificate — which argues for real underlying data. But it has an interested author and should be independently reproduced before anyone builds a business case on it. The prototype above does exactly that.
4. **That a free tool can reach these buyers.** Small survey firms are not browsing GitHub. Distribution likely runs through state surveying societies and ASFPM chapters, which is a slower and more relationship-driven channel than open-source distribution usually assumes.
5. **That the rules stay put.** The form expired 30 June 2026 and its renewal notice closed comments on 31 July 2026. A materially revised form would invalidate field mappings. Mitigation: externalise rules and field maps into versioned data files from day one — a design constraint, not an afterthought.
6. **That NFHL currency is adequate.** If practitioners find the tool contradicting recently issued LOMCs, trust evaporates immediately. The LOMC batch-file join is not a nice-to-have; it is a correctness requirement.

---

## 7. Cross-industry patterns

Seven patterns from this market transfer to named backlog markets.

**P1 — Regulator-form cross-field consistency validator.** The insight is that completeness checking is the easy, low-value half; the expensive errors are contradictions *between* fields that are each individually populated. Transfers to: **Fire protection inspection, testing and maintenance (ITM) contractors under NFPA 25** (inspection reports where device counts, deficiency classifications, and system descriptions must agree); **Certified payroll and prevailing wage compliance service providers** (WH-347, where the fringe-per-hour calculation must reconcile against hours and classification); **Provider credentialing and payer enrollment services**; **Environmental laboratories producing regulator EDD deliverables**; **Flood zone consulting** itself.

**P2 — Authoritative-registry join to validate self-reported identifiers.** Typed identifiers are validated against the issuing authority's live API rather than against a format regex — here, NFHL lookups confirming map panel, suffix, effective date, zone, and BFE. Transfers to: **DOT compliance consultancies and third-party safety managers** (FMCSA SAFER/SMS); **Commercial trucking insurance agencies and fleet underwriting submissions**; **Title abstracting and independent title search contractors** (recorder indices); **Special inspection agency accreditation consultants** (IAS/ANAB registries); **Calibration and metrology service providers** (accreditation scope lookups).

**P3 — Defect triage: reviewer-fixable versus originator-must-resubmit.** The rule that separates what the reviewer may correct at their desk from what forces a round trip to a sealing professional is the most operationally valuable knowledge in a review workflow, and is almost never encoded. Transfers to: **Construction submittal, RFI, and closeout coordination**; **Architectural construction administration desks at small A/E firms**; **Supplier quality engineering at OEMs and primes**; **Machine shop / job shop quoting and production control**; **County recorder offices — document intake, indexing and rejection handling**.

**P4 — Submittal-round economics: gate the package before the clock starts.** Where a review cycle is long and fixed (90 days here), the entire economics of the workflow reduce to round count, and a pre-submission completeness gate is worth more than any improvement to the work itself. Transfers to: **Federal construction contractors on NAVFAC/USACE projects** (UFGS submittal registers); **Registered Practitioner Organizations and CMMC consultancies**; **C3PAO assessment operations**; **FedRAMP 3PAO body-of-evidence production**; **Building permit expediting and code consulting firms**; **Delegated-design submittal coordination**.

**P5 — Baseline-versus-proposed diff with a documented tolerance test.** The Duplicate Effective → Revised progression with a 0.5 ft tie-in tolerance is structurally identical to any discipline that must demonstrate its change against an established baseline within a stated tolerance. Transfers to: **Test, adjust and balance (TAB) contractors** (design versus measured against NEBB/AABC tolerances — an almost exact analogue); **Commissioning providers for small and midsize buildings**; **Building automation and controls contractors** (implemented sequence versus designed sequence); **Geodetic control and least-squares network adjustment specialists**.

**P6 — Continuous audit-metric monitoring against a published threshold.** Where a program publishes a numeric compliance threshold audited episodically (CRS's 90% document accuracy), computing it continuously converts a periodic surprise into a managed number. Transfers to: **Small defense suppliers navigating CMMC Level 2 compliance**; **Contract manufacturers serving FDA-regulated medical devices**; **Special inspection agency accreditation consultants**; **Calibration and metrology providers** (ISO 17025); **Nonprofit grant management and compliance**.

**P7 — Form-edition and validity-window sentry.** Where a regulator issues dated form editions with hard transition dates, using the wrong edition voids otherwise correct work — and the check is trivially automatable and almost never automated. Transfers to: **Certified payroll and prevailing wage compliance**; **Remote online notarization platform operators and RON-commissioned notaries**; **Provider credentialing and payer enrollment services**; **County recorder offices**; **Truck permitting and registration service agencies**.

---

## 8. Sources and confidence

### Verified findings (directly supported by cited sources)

- **68.4% of 5,082 residential ECs contained at least one error; 44% had two or more; average two per certificate**, with the five most common errors named — [Elevation Certificates: Common Errors and Challenges, Forerunner](https://www.withforerunner.com/post/elevation-certificates-errors)
- **Error-by-section breakdown and the Correction Memo vs. resubmittal triage rule**; expired-form procedure; finished-construction-only; file-naming and permit-list reconciliation instructions — [Common EC Errors & Recertification Tips, Monmouth County NJ](https://www.co.monmouth.nj.us/documents/24/Common_EC_Errors_slidesR.pdf)
- **The full CRS EC review checklist including all cross-field consistency rules** — [2022 EC Checklist, CRSresources.org](https://crsresources.org/files/300/2022_ec_checklist.pdf)
- **2022 EC form: effective 7 July 2023, mandatory after 1 Nov 2023, valid through 30 June 2026; new Sections H and I; LiMWA line B13; WGS 84 option; four required photographs; reinstated conversion factor; ~15 additional mandatory fields** — [FEMA releases new Elevation Certificate, ASFPM](https://www.floods.org/news-views/fema-news/fema-releases-new-elevation-certificate-and-dry-floodproofing-certificate/); [Getting started with the new Elevation Certificate, Forerunner](https://www.withforerunner.com/post/getting-started-with-the-new-elevation-certificate); [Better Late Than Never: The New Elevation Certificate, The American Surveyor](https://amerisurv.com/2023/08/12/better-late-than-never-the-new-elevation-certificate/)
- **OMB renewal, 1 June 2026: 3,517 respondents, 3,517 annual responses, 12,735 burden hours (~3.6 hr/response), $680,316 respondent cost, $37,414 federal cost; comments closed 31 July 2026** — [Federal Register 2026-10842](https://www.federalregister.gov/documents/2026/06/01/2026-10842/agency-information-collection-activities-proposed-collection-comment-request-elevation)
- **MT-1 60-day / MT-2 90-day processing; Online LOMC vs eLOMA; licensed-professional requirements** — [Online LOMC FAQ, FEMA](https://hazards.fema.gov/onlinelomc/ext/Help/loadFaq)
- **MT-2 package contents, model progression, 0.5 ft tie-in, five recurrence intervals, 9-month CLOMR assumption, 2+ rounds, FEMA's ≤2 information-request goal, and the enumerated failure modes; Kentucky as LOMR Review Partner from 1 Jan 2024** — [CLOMRs, No Rises, LOMRs and Floodplain Development, KAMM 2025](https://eec.ky.gov/Environmental-Protection/Water/FloodDrought/Documents/KY-CLOMR-LOMR-KAMM2025-Presentation.pdf)
- **Illinois State Water Survey paused LOMR review for lack of FY2025 CTP funding** — [ISWS LOMR Review](https://www.illinoisfloodmaps.org/lomr-review.aspx)
- **CRS Activity 310 point values (38/48/30), required written procedures, 90% accuracy threshold, "high" effort level, credit-loss reasons** — [CRS Guide, Activity 310](https://crsguide.withforerunner.com/310-elevation-certificates/)
- **Forerunner's automated EC checks, 2009–2026 edition detection, 1–5 minute processing, and the retained manual verification step** — [Reviewing Elevation Certificates, Forerunner Help Center](https://withforerunner.com/docs/files/reviewing-elevation-certificates)
- **EC cost $400–$1,000+, homeowners do not forward ECs to communities, coverage represents only a fraction of structures, Florida's 2017 statute** — [Elevation Certificate Data: Challenges and Opportunities, Forerunner](https://www.withforerunner.com/post/elevation-certificates-flood-data)
- **EC cost $170–$2,000+, average ~$600, ~5 business days typical turnaround** — [Elevation Certificate Cost, HomeAdvisor](https://www.homeadvisor.com/cost/inspectors-and-appraisers/elevation-certificate/)
- **Risk Rating 2.0 removed the EC rating requirement 1 April 2022; insurer must use the more favourable First Floor Height; remaining EC uses** — [Vantage Point: Elevation Certificates and Risk Rating 2.0, The American Surveyor](https://amerisurv.com/2022/05/15/vantage-point-elevation-certificates-and-risk-rating-2-0/); [RR2 and Elevation Certificates fact sheet, ASFPM](https://asfpm-library.s3.us-west-2.amazonaws.com/General/RR2-ElevationCertificate-FactSheet-FINAL.pdf)
- **Consultant workflow and fee points: FIS profile interpolation, LOMA ~$150 / 6–8 weeks, eLOMA ~$400 / 5–10 business days, client mix** — [Western Technologies Group](https://www.westerntechnologiesgroup.com/blog/certified-floodplain-managers-flood-determination)
- **NFHL public REST services available for programmatic query** — [FEMA NFHL MapServer](https://hazards.fema.gov/arcgis/rest/services/public/NFHL/MapServer); [Flood Data Viewers and Geospatial Data, FEMA](https://www.fema.gov/flood-maps/national-flood-hazard-layer)
- **LOMC batch files: all newly issued LOMAs/LOMRs/revalidations/SOMAs, weekly, posted within ~2 weeks of the issue window, back to December 2021** — [LOMC Batch Files, FEMA MSC](https://msc.fema.gov/portal/resources/lomc)
- **NSRS modernization: NAD 83 and NAVD 88 replaced by NATRF2022 et al. plus NAPGD2022; "2025 or 2026"; tools within five years; notice does not address surveyor/FEMA impacts** — [Federal Register 2024-23347](https://www.federalregister.gov/documents/2024/10/09/2024-23347/updated-implementation-timeline-for-the-modernized-national-spatial-reference-system-nsrs)
- **NFIP lapsed in the autumn 2025 shutdown, was reauthorized in November 2025, and expires 30 September 2026** — [NFIP Reauthorized With Passage of Funding Bill, Insurance Journal](https://www.insurancejournal.com/news/national/2025/11/13/847559.htm); [FAQ: NFIP Expires September 30, 2026, NAR](https://www.nar.realtor/flood-insurance/faq-national-flood-insurance-program-expires-september-30-2026)
- **MT-1 forms and instructions; LOMA/LOMR-F process** — [MT-1 Application Forms, FEMA](https://www.fema.gov/flood-maps/change-your-flood-zone/paper-application-forms/mt-1); [LOMA & LOMR-F Process, FEMA](https://www.fema.gov/flood-maps/change-your-flood-zone/loma-lomr-f)
- **Substantial Damage Estimator tool; the 50% rule as a recognised misinterpretation problem with a FEMA appeals docket** — [Substantial Damage Estimator, FEMA](https://www.fema.gov/emergency-managers/risk-management/building-science/substantial-damage-estimator-tool); [FEMA's 50% Rule Explained, J.S. Held](https://www.jsheld.com/insights/articles/femas-commonly-misinterpreted-50-rule)
- **Base Level Engineering usable as a BFE source for LOMA submittals** — [Using Base Level Engineering for LOMA submittals, FEMA](https://www.fema.gov/sites/default/files/documents/fema_BLE-for-LOMA-submittals_fact-sheet_08-16-21.pdf)

### Strong inferences (reasoned from verified findings, not directly stated)

- **The producer side is unserved while the reviewer side has a real incumbent.** Forerunner's own materials position it as a community platform; no producer-facing EC checker surfaced in any search. Inference, not a stated fact — absence of evidence in web search is weaker than evidence of absence.
- **Cross-field consistency checks are the underserved half.** Forerunner's published check list is completeness- and format-oriented while the CRS checklist is comparison-oriented. Whether Forerunner also runs engineering-consistency rules internally is not publicly documented, and I could not determine it. The gap is inferred from published descriptions only.
- **FEMA's 3,517 annual EC responses materially undercounts reality.** A single analysis examined 5,082 certificates; Florida has collected them statewide since 2017. The 3.6-hour per-response burden is credible; the count is not usable for sizing.
- **Package defects rather than engineering defects drive MT-2 rounds.** Every failure mode in the Kentucky presentation is clerical or documentary. Strong, but drawn from one state's practitioner material.
- **A CRS class step is worth roughly 5% in premium discount community-wide**, making the 90% accuracy threshold disproportionately valuable. The CRS discount structure is well established; the specific dollar leverage per community was not verified here.
- **Fillable-PDF field extraction is deterministic for digitally-produced ECs.** Follows from the form being an AcroForm, but should be confirmed against a real corpus — some firms flatten PDFs on export, which would break it.

### Tentative hypotheses requiring practitioner validation

- **EC demand post-Risk Rating 2.0 is stable.** Unestablished. The most important open question in this report; if it is wrong, several rankings shift materially.
- **Surveyors would adopt a pre-seal validator.** Untested, and plausibly wrong for professional-identity reasons. Validation question 3 exists specifically to probe this.
- **The 30 June 2026 form expiry is creating live confusion in the field.** Timing-plausible, and the renewal notice is real, but I found no practitioner reports of actual disruption. Do not build on it.
- **The NSRS transition will create a reconciliation market for EC archives.** The datum change is real and dated; the practical impact on FEMA products is explicitly not addressed by the notice, and FEMA has published no migration plan. Highly speculative.
- **The observed $150 / $400 LOMA fee points are representative.** One firm's public pricing. Needs three to five more data points before it means anything.
- **Small communities would pay for an SI/SD tool** rather than continue with a spreadsheet. Untested; municipal willingness to pay for a narrow tool is the weakest link in concepts 4.6, 4.7, and 4.8.

---

*Report prepared 2026-08-07 · claim `08d5b219` · market: Flood zone / FEMA elevation certificate and LOMA-LOMR consulting · angle: narrow-subspecialty*
