# Construction Materials Testing & IBC Chapter 17 Special Inspection — the branch CMT department

**Market:** Geotechnical and environmental consulting / materials testing labs
**Angle:** narrow-subspecialty
**Named subspecialty:** *IBC Chapter 17 special inspection and construction materials testing (CMT) for vertical building construction, as operated out of a single branch office — field technicians, one accredited branch laboratory, and one CMT department manager.*
**Claim ID:** 88358944
**Date:** 2026-08-06

---

## 0. Cycle header

### Why this assignment

The ledger held 202 open assignments across 81 markets and zero live claims. Selection criteria, applied in the order the brief specifies:

**(a) Markets with zero completed entries.** Geotechnical / environmental consulting / materials testing labs had **no** completed reports — all four angles were open. This eliminated roughly a third of the backlog (the partially-covered markets: fire protection, MEP/HVAC, land surveying, machine shops, freight, immigration law, insurance, nonprofit grants, property management).

**(b) Expected strength of practitioner evidence.** This market is unusually well-documented in *primary* sources, which matters because the brief penalizes reports written from general knowledge. Accreditation bodies (AASHTO re:source, CCRL, IAS, A2LA, CMEC) publish their own procedures manuals, fee schedules, and — critically — **lists of the actual nonconformities their assessors write up**. State DOTs publish calibration-interval tables. Municipalities publish special-inspection agreements that state required report contents verbatim. Public agencies publish CMT firms' fee schedules as contract exhibits, which exposes the billing structure in detail. That is a much better evidence base than a market where the only sources are vendor blogs.

**(c) Angle diversity.** Across the nine completed reports, the angle distribution was skewed: four `core-practitioner-workflow`, two `back-office`, two `handoffs-and-qa`, and only **one** `narrow-subspecialty`. Taking narrow-subspecialty corrects the catalog's least-covered angle while still opening a fresh market.

I also considered *Small defense suppliers navigating CMMC Level 2* (timely, entirely uncovered, well-documented) and *Title, escrow, and real estate closing*. CMMC lost on fit — it is an IT-security compliance market rather than a professional-workflow market, and its tooling landscape is already crowded with well-funded GRC vendors. Title/escrow lost on differentiation — the incumbent software (Qualia, ResWare, SoftPro) is mature and the workflow is heavily integrated, which the brief tells us to avoid.

**One caveat on my own choice:** taking `narrow-subspecialty` before `core-practitioner-workflow` on a fresh market means this report maps one branch of the market in depth rather than the whole market in outline. I have flagged the adjacent scopes I deliberately did **not** cover in §1.3 so the next run knows exactly what is left.

**Backlog after this run:** 201 assignments remaining at claim time; **207 after the additions in §6 of the ledger update** (see INDEX.md for the live count).

---

## 1. Market examined

### 1.1 The industry

Construction materials testing and special inspection is the third-party verification arm of building construction. It exists because **IBC Chapter 17 requires it**: certain categories of work — reinforced concrete placement, structural steel welding and high-strength bolting, structural masonry, soils and deep foundations, spray-applied fire-resistive materials — may not be accepted by the building official on the contractor's word alone. An "approved agency" independent of the contractor must observe and test the work, report it, and certify at the end that it complied.

The governing text ([2021 IBC / CBC §1704.2.4](https://gocodebook.com/us/california/california-building-code/special-inspections/process-and-responsibilities/special-inspector-qualifications-access-and-reporting)) is worth quoting because nearly every opportunity in this report descends from it:

> "Approved agencies shall keep records of special inspections and tests. The approved agency shall submit reports of special inspections and tests to the building official and to the registered design professional in responsible charge **at frequencies required by the approved construction documents or building official**."
>
> "All reports shall describe the nature and extent of inspections and tests, the location where the inspections and tests were performed, and indicate that work inspected or tested was or was not completed in conformance to approved construction documents."
>
> "**Discrepancies shall be brought to the immediate attention of the contractor for correction.** If they are not corrected, the discrepancies shall be brought to the attention of the building official and to the registered design professional in responsible charge prior to the completion of that phase of the work."
>
> "A final report documenting required special inspections and tests, and correction of any discrepancies… shall be submitted at a point in time agreed upon prior to the start of work."

IBC §1703 adds three agency-level obligations: the agency must be "objective, competent and independent from the contractor"; it must have adequate equipment and "**the equipment shall be periodically calibrated**"; and it must "employ experienced personnel" ([IBC §1703](https://www.drjcertification.org/ibc-section-1703)).

### 1.2 Who operates in it

The work is performed by three overlapping organizational types:

| Type | Description | Typical size |
|---|---|---|
| **Geotechnical/CMT firms** | The dominant model. A geotechnical engineering practice with a CMT department attached — the same firm that did the soils report during design does the compaction testing during construction. | 15–150 total staff; CMT department of 6–40 |
| **Pure CMT/SI agencies** | Testing and inspection only, no design practice. Often regional, often family-owned. | 5–60 |
| **Branch offices of national firms** | Terracon, UES, NV5, Intertek-PSI, ECS and similar operate branch CMT departments that behave, operationally, like independent 20-person firms with a corporate QMS overlay. | branch of 15–60 |

The **addressable universe of accredited laboratory locations is roughly 2,000–3,000**. AASHTO re:source's LAP program cites "[2,100+ accredited labs](https://aashtoresource.org/lap/overview)" and its assessors visit "over 2,000 laboratories" across all 50 states ([AASHTO Journal](https://aashtojournal.transportation.org/aashto-resource-podcast-looks-at-laboratory-assessments/)); CCRL separately "inspects over 1100 laboratories in the United States, Canada, and Mexico" ([Gilson](https://www.globalgilson.com/blog/lab-accreditation-for-materials-testing)), with substantial overlap. AASHTO re:source's Corporate QMS Review program requires "at least three accredited locations" to qualify, which tells you multi-branch is common enough to warrant its own product line.

### 1.3 The user, and the scope boundary

The buyer and primary user is the **CMT Department Manager** (titles vary: CMT Manager, Construction Services Manager, Branch Materials Manager). A real posting for this role — [Terradyne Engineering, Carrollton TX, posted 2026-07-31, **$46,900–$73,900**](https://to.indeed.com/aaxphz966tmv) — is effectively a job description of every problem in this report. Verbatim duties:

> "Daily monitor of the team members' attendance, and timesheets, including weekly approval."
> "Review reports and send them to clients once work is completed."
> "Prepare, review, and submit invoices daily to the branch manager."
> "Ensure technicians are certified within 90 days of employment… **Maintain field technicians' certifications current**, including but not limited to the ACI, and Nuclear Density Gauge."
> "**As the RSO (Radiation Safety Officer), you will maintain and oversee the Nuclear Density Gauges.**"
> "Oversee the daily activity of the CMT lab and ensure the clients receive the data **before the stipulated due date**."
> "Inspect and ensure equipment is maintained and calibrated."
> "Complete proposals, change orders." / "Market to obtain new clients."

Required software skills, stated in full: **"Basic computer skills such as Word and Excel."**

One person, at approximately $60k, simultaneously owns dispatch, timesheet approval, report QC, client delivery SLA, daily invoicing, certification compliance, radiation safety, equipment calibration, fleet, proposals, and sales — tooled with Word and Excel. That is the ideal customer profile for everything below.

Secondary users: the **field technician** (ACI Grade I / ICC certified, high turnover, $22–$35/hr), the **laboratory technician**, and the **QA manager** (often the same person as the department manager at a single-branch firm), plus the **PE or SE of record** who stamps final reports.

**Scope boundary — what this report deliberately excludes**, so the next run can pick it up cleanly:

- Geotechnical **exploration and design** (drilling, boring logs, gINT/LogPlot drafting, foundation recommendations) — that is the `core-practitioner-workflow` angle for this market and remains open.
- **Environmental** consulting (Phase I/II ESA, EQuIS/EDD deliverables, chain-of-custody for analytical chemistry) — a genuinely different regulatory stack; open.
- **DOT / highway materials testing** — same lab, different client, different spec regime (AASHTO methods, DOT prequalification, IA programs); adjacent but distinct.
- The **back-office** angle (proposals, AR, project setup, subcontractor management) and the **handoffs-and-qa** angle (client portals, EOR coordination) for this market; both open.

---

## 2. How the work is performed

### 2.1 The chain, start to finish

**Design phase.** The structural engineer of record produces a **Statement of Special Inspections** — a schedule listing every inspection and test required for the project, keyed to IBC Tables 1705.x, identifying each as *continuous* or *periodic*, and naming the responsible agency. The owner engages the agency. Many jurisdictions require the agency to countersign a **Special Inspection & Testing Agreement** before permit issuance ([Santa Clara GA31](https://www.santaclaraca.gov/home/showpublisheddocument/67169/639138254471370000), [San Ramon](https://www.sanramon.ca.gov/our_city/departments_and_divisions/community_development/building_and_safety_services/special_inspections/special_inspection_testing_agreement)).

That schedule is a PDF. It arrives as a PDF. It stays a PDF. **Nothing downstream in the firm ever turns it into a data structure** — which is the root cause of problem #1 in §3.

**Dispatch.** The contractor calls or texts the department manager, typically the afternoon before, sometimes the same morning. The manager must assign a technician who (a) is available, (b) holds the *specific* certification the jurisdiction requires for that inspection category, and (c) is not already committed. Per [ATSER](https://www.atser.com/from-field-sample-to-final-report-mapping-the-modern-materials-testing-workflow/), this is "often managed through **phone calls, texts, and shared calendars**."

The certification constraint is not soft. Spokane's published [minimum-qualifications matrix](https://static.spokanecity.org/documents/business/resources/permitting/commercial/guidesheets/special-inspection-qualifications.pdf) requires, for example:

| Category | Required certification (verbatim) |
|---|---|
| 2A Reinforced Concrete | "**ACI Field Technician – Grade I AND ICC Reinforced Concrete Special Inspector** and/or WABO Reinforced Concrete (RC)" |
| 4A Structural Steel Welding | "AWS Certified Welding Inspector (CWI); ICC Structural Steel & Welding and/or WABO Structural Welding (SW)" |
| 5A High-Strength Bolting | "ICC Structural Steel & Bolting and/or WABO Structural Steel & Bolting (SSB)" |
| 6A Sprayed Fire Resistant Materials | "ICC Spray-Applied Fireproofing and/or WABO Spray-Applied Fire-Resistive Materials (FP)" |
| 1B Site Soils | "WAQTC Aggregate, WAQTC Embankment & Base, ICC Soils, and/or NICET Soils Level 1" |

Phoenix maintains a parallel table with **different acceptable equivalents** ([Phoenix SI & Observation Manual](https://www.phoenix.gov/content/dam/phoenix/pddsite/documents/trt/external/dsd_trt_pdf_00595.pdf)). So does San Diego, which additionally requires each inspector to carry a **City-issued Registration Card number** that must appear on every report ([BLDG-17-2](https://www.sandiego.gov/development-services/forms-publications/technical-bulletins/BLDG-17-2)).

**Field.** The technician drives to site. For a concrete placement the sequence is hard-timed and unforgiving. From a published [ready-mix delivery and point-of-discharge method statement](https://quollnet.com/methods/method-statement-ready-mix-concrete-delivery-ticket-inspection-and-point-of-disc), all verbatim: batch ticket must be within "≤ 90 min from batching or ≤ 300 revolutions"; composite sample per ASTM C172 "from the middle portion of discharge, from at least two portions"; slump "within 5 min of obtaining final portion"; air content within 15 min; cylinders molded "within 15 min of sampling"; initial cure "in insulated curing box with water at 16–27 °C."

The technician therefore has roughly a **twenty-minute window per truck** to run four tests, mold six cylinders, transcribe a batch ticket, and write it all down — while, in the words of [MetaField's own field-tech piece](https://www.metafield.com/cmt-field-tech-life/), "People standing around watching you… not very patiently."

For soils, a nuclear density gauge is used. Per [TDOT SOP 7-1](https://www.tn.gov/content/dam/tn/tdot/hq-materials-tests/standard-operating-procedures/SOP_7-1.pdf): "A standard count must be taken daily on the reference standard block"; soil tests at 60-second counts; asphalt by the "Four Nineties" method — four tests rotated 90° and averaged. Results go onto named paper forms *or* into software; the same DOT offers both, and the paper form is still first-class.

For fireproofing, the arithmetic dominates. [Catawba County's SI chapter](https://www.catawbacountync.gov/building/_pdfs/SICCChapter13.pdf) requires thickness testing "at least once for each 1,000 square feet… and 25 per cent of the structural members on each floor," with "not less than four measurements for each 1,000 square feet" per ASTM E605, bond strength "at least once for each 10,000 square feet" at a minimum 150 psf per ASTM E736, and a tolerance of design thickness minus ¼ in. (or minus 25% for designs under 1 in.).

**The daily report.** The technician writes a Daily Field Report or Daily Inspection Report. Required contents, composited from published jurisdiction requirements: project address and permit number; work inspected with specific locations; conformance statement; **"The date of inspection, time of arrival, and departure from the job site"**; inspector name, registration card number, and signature; a list of all non-conforming items; how each was resolved or that it remains open; and — per Phoenix — the "**time and method of notification**" for each party notified of a discrepancy.

Santa Clara requires "a **daily handwritten report** in a format acceptable to the Building Division," left on site, with weekly transmittal to the agencies. San Ramon requires "weekly reports… directly to the building division, project engineer or architect." San Diego requires the daily report be left on site for the contractor. Missouri State University's Division 01 spec says simply "**promptly**" ([014500](https://design.missouristate.edu/_Files/Standards/Division1/014500Quality_Control.pdf)).

**There is no 24-hour rule in the model code.** The IBC deliberately delegates report frequency to "the approved construction documents or building official." What exists instead is a per-project, per-jurisdiction patchwork of undocumented delivery promises. The only "24 hours" I found anywhere in this domain is a **price**: [Los Gatos, CA](https://weblink.losgatosca.gov/WebLink/ElectronicFile.aspx?dbid=0&docid=1262293) prices "samples needing results within 24 hours" at a **50% mark-up**.

**Office.** The report goes back to the office — physically, in many firms. MetaField's own description of the current state: Friday fieldwork → paperwork dropped at the office → **office transcribes it Monday**. Someone types it into a template. A project manager or engineer reviews it. It goes to the client, the EOR, and the building official.

**Lab.** Cylinders arrive (transport "not to exceed 4 hours" per [NRMCA CI 40-08](https://www.nrmca.org/wp-content/uploads/2020/06/CI4008cylindercuring.pdf)), get logged in, go into the moist room, and get broken on a schedule with tight tolerances — per ASTM C39, "24 h ±0.5 h, 3 days ±2 h, 7 days ±6 h, **28 days ±20 h**, 90 days ±2 days." Break data goes onto a report that must contain "the date they were received at the lab, the test date, specimen identification, cylinder diameter, test age, maximum load applied, compressive strength, type of fracture, and any defects" ([NRMCA CIP 35](https://www.concreteanswers.org/CIPs/CIP35.htm)).

**Closeout.** At the end, the agency must produce the **Final Report of Special Inspections**, certifying that all required inspections were performed and all discrepancies corrected. In California this "**MUST BE STAMPED AND SIGNED BY A LICENSED CIVIL OR STRUCTURAL ENGINEER**" and must be accepted "**PRIOR TO SCHEDULE BUILDING FINAL & THE ISSUANCE OF A CERTIFICATE OF OCCUPANCY**" (Santa Clara GA31, capitals in original). No final report, no CO.

### 2.2 The compliance overlay running underneath all of it

The branch lab is simultaneously operating a formal quality management system. The dominant regime is **AASHTO Accreditation (AAP)**, built on **AASHTO R 18**, with **CCRL** performing concrete-side inspections and **ASTM C1077 / D3740 / E329 / E543** bolted on as prerequisite agency standards. Alternatives: A2LA, IAS AC89, ANAB, CMEC — all ISO/IEC 17025-based.

The hard numbers, all from the [AAP Procedures Manual](https://aashtoresource.org/docs/default-source/publicdocuments/aap-procedures-manual.pdf):

- Assessment tour frequency **~27 months** (§7.3.1); accreditation status re-evaluated **every 12 months** (§11.2).
- Nonconformities must be resolved **within 60 calendar days** of the final report (§8.2.1); +30 days only with a written plan (§8.2.5); beyond 120 days, "an additional on-site assessment may be required" (§8.2.9).
- The QMS "may be maintained **digitally or in hard copy** and is not required to be contained within a single binder or manual" (§7.2.2) — the explicit hook for software.
- Records retained **≥5 years**; a technical director may serve **no more than five facilities** and must be physically present "at least once per month for an entire day" (§4.9.2).

And on certifications, verbatim from the [AASHTO policy on certifications](https://aashtoresource.org/docs/default-source/publicdocuments/aap-pandg-certification-review.pdf):

> "**The AAP does not accept expired certifications of any kind.** Even if no requirement for recertification is stated in the ASTM standard, expired certifications are not considered to be valid."
> "**Certifications held by managers or supervisors do not fulfill the certification requirements for the staff they oversee.**"

Assessors verify this against, among other things, "the laboratory's organizational chart; test records; test reports; **technician matrices**."

### 2.3 Software actually in use

| Tier | What it is | Notes |
|---|---|---|
| **The real incumbent** | Excel, Word, paper carbonless forms, shared network folders, Outlook, a whiteboard or Google Calendar for dispatch | Confirmed by job postings: UES asks for "Microsoft Office Suite… and Field Data Collection (FDC) software or similar"; Terradyne asks for "Basic computer skills such as Word and Excel"; [HVEA's technician JD](https://hveapc.com/careers/job-description-material-testing-technician/) names **no software at all** |
| **Integrated CMT platforms** | MetaField (Agile Frameworks), Aldoa, eFieldData, ATSER, Omnant, SpectraQEST/QESTLab, ForneyVault + ForneyField | Full-suite: dispatch + field + LIMS + reporting + invoicing. Priced and sold as a platform commitment |
| **Point solutions** | R18LabQMS (Asphalt Institute), LOGitEASY / TabLogs (boring logs), Giatec/Concrete Sensors (maturity) | Narrow, and evidence that narrow sells here |
| **Accounting/PM** | Deltek Ajera or Vantagepoint, BQE Core, QuickBooks | Rarely connected to the field data |

The integrated platforms are the incumbents to beat. Their own marketing tells you what the market's baseline is: firms "currently using **spreadsheets, paper forms, or legacy systems**" moving away from "disconnected spreadsheets, paper test sheets, and manual report assembly" ([Aldoa](https://www.aldoa.com/blog/top-5-construction-materials-testing-software-in-2025)); records living in "paper binders," "file cabinets," "shared folders," "manual spreadsheets," "email chains" ([MetaField](https://www.metafield.com/laboratory-accreditation-for-cmt-firms-how-to-simplify-aashto-r18-compliance)); quality manuals as "**a three-ring binder gathering dust in a corner**" ([Omnant](https://omnant.com/blog/aashto-r18-dont-suffer-and-scramble)).

---

## 3. Most important problems, ranked

### P1 — Coverage of the Statement of Special Inspections is never reconciled until closeout, when it is too late to fix

**Who:** the department manager and the PE who must stamp the final report. **When:** at project closeout, months after the work. **Frequency:** on essentially every project of consequence.

The Statement of Special Inspections is a schedule of required items. The daily reports are the evidence those items were covered. **Nobody reconciles the two until someone tries to write the final report.** At that point, gaps in coverage are physically unfixable — the concrete is poured, the steel is clad, the fireproofing is behind drywall.

The consequence is documented. On [Eng-Tips, "Missed Special Inspection"](https://www.eng-tips.com/threads/missed-special-inspection.199057/), a practitioner reports that for masonry laid without an inspector present, "**Core sampling and testing were prescribed by DSA as remediation.**" Another describes the defensive fallback: reports worded "We were unable to inspect the following areas…"

That coverage is genuinely incomplete in practice is asserted by a contract inspector on [Eng-Tips](https://www.eng-tips.com/threads/structural-special-inspections-compliance-or-complacence.417314/): "**very few projects have the coverage performed as stated on the schedule of special inspections**"; on steel bolting and welding specifically, "the whole group of operations seems to be somewhat of a farce"; and "I have been warned on more than one occasion about 'opening a can of worms.'"

**Current handling:** a paper checklist, or the PM's memory, or an Excel sheet built once and abandoned. **Why inadequate:** the reconciliation is a set-difference between a PDF and a folder of PDFs; nobody does it weekly because doing it by hand weekly is unaffordable. **Cost:** remediation coring and testing on a mid-size building runs five figures; CO delay on a commercial building runs into rent-loss territory measured in weeks; and in the worst case the agency's E&O carrier gets involved.

### P2 — The daily field report is simultaneously the code record, the timesheet, and the invoice backup — and it is often handwritten

**Who:** technician, manager, billing. **When:** every single field visit. **Frequency:** dozens to hundreds per week per branch.

Note the structural coincidence: San Diego requires the daily report to state "the date of inspection, **time of arrival, and departure** from the job site." Those are exactly the fields the invoice is computed from. The code-compliance document *is* the time record. One illegible, incomplete, or lost form therefore produces a compliance gap, a billing dispute, and a rework cost simultaneously.

And it is often required in handwriting: Santa Clara mandates "a daily **handwritten** report."

The transcription cost is real. MetaField's own description of the failure modes — worth citing precisely because a vendor would not invent this level of specificity: "Your poor handwriting makes it difficult for them to decipher what you wrote"; "**What about the information you forgot to record?**"; "You forgot to record the external temperature at the site"; "go back and retrieve the information—**if you can**." ATSER: "The data that needs to be in the system tonight might not get there until tomorrow morning, or later, transcribed by hand"; the gap between collection and availability "can stretch to **hours or even days**"; and the failure mode is "**A report filled out from memory three hours later.**"

**Cost:** the closest quantified benchmark is from general construction daily reporting, not CMT, and must be labeled as such: [45–75 minutes per report to create, $12–$15 per manual transaction, ~4.8 hours of wasted labor per week](https://dancumberlandlabs.com/blog/the-field-report-written-twice/). Treat as directional only.

### P3 — Technician certification and R18 competency records are a combinatorial problem being managed in a spreadsheet

**Who:** department manager / QA manager. **When:** continuously, and catastrophically at assessment time. **Frequency:** perpetual.

Three separate matrices must be kept simultaneously true:

1. **Certification validity.** ACI = **5 years, no CEU path — full written *and* performance re-exam** ([ACI](https://www.concrete.org/certification/certificationprograms.aspx?m=details&pgm=Field+Concrete+Testing&cert=Concrete+Field+Testing+Technician%E2%80%94Grade+I)); ICC = **3 years, CEU-based**, 1.5 CEUs for one credential, 3.0 for 2–5, "50% of CEUs are required to be Part 1" ([ICC](https://www.iccsafe.org/wp-content/uploads/Renewal_EIB.pdf)); NICET = **3 years / 90 CPD points**, $120 late fee ([NICET](https://www.nicet.org/recertify/)); WACEL = **5 years**, re-exam, with prerequisite chains — Foundation SI requires "a valid **Concrete I and Soil I**" — and "proficiency and written exams must be completed **within 90 days of one another**," and WACEL "**does not accept internal company programs**" ([WACEL](https://www.wacel.org/technician-certification-program/technician-certification-program-prerequisites/)).

2. **Jurisdictional eligibility.** Which certificate satisfies which inspection category differs by AHJ (Spokane vs. Phoenix vs. San Diego, above).

3. **R18 competency evaluation**, which is a *separate* obligation from certification. From the [AASHTO training & competency policy](https://aashtoresource.org/docs/default-source/publicdocuments/aashto-accreditation-policy-and-guidance-on-training-and-competency-evaluation.pdf?sfvrsn=4): records must include "test method designation, date of training or evaluation, name of the individual who trained or evaluated… and a field for recording comments"; retained "**for a minimum of 5 years**"; "**competency must be evaluated for each test an individual performs at a set interval established by the laboratory**"; "**written testing alone does not meet the competency evaluation requirement**"; and "**the date of the evaluation must match when the test was actually demonstrated**."

A 12-technician lab covering 30 test methods carries on the order of **360 individual competency records**, each with a date, method, evaluator and comment, each on a lab-defined recurring interval, each retained five years, cross-referenced to an expiry matrix and an org chart that must itself be current.

AASHTO re:source names its own top-three R18 nonconformity families: **calibration record-keeping, training/competency evaluation, and internal audits** ([Mastering AASHTO R 18: Common Pitfalls](https://aashtoresource.org/university/newsletters/newsletters/2024/08/27/mastering-aashto-r18-common-pitfalls)). Two of the three are this problem. Named failure modes include "**Recording evaluation dates as the completion date rather than when evaluations actually occurred**" and "**Records that contradict stated QMS policies**" ([Evaluating Competency](https://aashtoresource.org/docs/default-source/newsletter/evaluating-competency---printer-friendly.pdf?sfvrsn=2)).

**Cost:** a nonconformity carries a 60-day clock; an unresolved one suspends accreditation for the affected methods; suspension means the firm cannot sell that test until it is cured.

### P4 — Cure-room monitoring produces a continuous data stream that nobody reviews until it matters, and a gap is unrecoverable

**Who:** lab technician / QA manager. **When:** continuously. **Frequency:** every day of every year.

ASTM C511, as summarized by [AASHTO re:source](https://aashtoresource.org/docs/default-source/newsletter/the-cure-for-the-cure--a-guide-to-astm-c511-and-your-curing-facilities---printer-friendly.pdf?sfvrsn=6), requires the moist room to "maintain a temperature from **21.0 – 25.0 °C (69.8 – 77 °F)**," monitored by a recorder "accurate and readable to 1 °C" and "capable of **recording the temperature at least once every 15 minutes**," with the data evaluated **weekly**, the recorder standardized **every 6 months**, tanks stirred **at least monthly**, and cleaned/refilled with calcium hydroxide **every 24 months**. Humidity must be ≥95% ([ODOT SOP-106](https://www.odot.org/materials/C97001_WEB_REP/SOP/SOP-106.pdf)).

The named nonconformities are, verbatim: "Failing to evaluate records of **weekly** temperature data"; "Failing to record **semi-annual** temperature recorder standardizations"; "The inability to control the temperature"; "Incomplete or nonexistent maintenance program."

Here is why this ranks above its apparent size. A recorder producing a reading every 15 minutes generates **~35,000 rows a year**. Nobody reads 35,000 rows. The weekly evaluation is, in practice, a signature on a form. When an excursion or a logger gap is later discovered — during an assessment, or during a dispute over a low break — the firm faces two questions it cannot answer: *how long was it out?* and *which specimens were in the room at the time?* The second question is the commercially dangerous one, because it determines how many test reports the client can now challenge. And the temptation to backfill the log is the falsification trap: R18 treats unauthorized data changes as "**falsification**" ([AASHTO re:source, Reports and Records](https://podcast.aashtoresource.org/1246739/episodes/10545526-reports-and-records)).

This matters because **almost any error in concrete testing produces an artificially low result**, and low results trigger expensive investigations. [Beton Consulting](https://www.betonconsultingeng.com/astm-c31-and-c39-what-could-go-wrong/) quantifies the initial-curing side: one day at 100 °F / 25% RH "reduced the strength by 12%; 3 days reduced it 18%" — and reports that "**in a study of jobsite practices, initial curing conformed to ASTM C31 about half the time.**" [NRMCA CI 40-08](https://www.nrmca.org/wp-content/uploads/2020/06/CI4008cylindercuring.pdf) puts the ceiling at "up to a **20% reduction** in the 28-day compressive strength," and notes the loss is permanent "**even if standard curing is provided subsequently**." A ready-mix QC engineer "estimates that he gets at least **100 calls and meetings a year** resulting from poor lab QC" ([Concrete Sensors](https://concretesensors.com/cylinders-are-crushing-productivity-and-quality/)).

### P5 — Billing under a minimums-and-multipliers rate schedule is reconstructed by hand from field tickets, and leaks

**Who:** department manager and billing. **When:** weekly/monthly. **Frequency:** every invoice cycle.

CMT rate schedules are not hourly. They are minimum-hour blocks plus portal-to-portal travel plus multi-tier overtime plus cancellation tiers plus equipment and per-diem multipliers. From published contract exhibits:

**[NV5 West](https://resources.finalsite.net/images/v1698078886/simivalleyusdorg/uplyxudmdpr7vqnixs5i/101723MeasureXAuthorizations.pdf)**, verbatim:
> "A minimum charge of **4 hours** applies to inspection/testing call-out between 0 and 4 hours. **Eight (8) hours** will be charged for work performed over 4 hours up to 8 hours."
> "A minimum of **24-hour notice** is required to schedule personnel (**48-hour for DSA/OSHPD** projects). For same-day scheduling, a **50% premium** applies. **Same-day cancellations will incur a 2-hour charge.**"
> "**Cancelation after field personnel have been dispatched will be charged a 4-hour minimum charge.**"
> "Hourly travel is charged **portal-to-portal**… may be waived for special inspectors within 25 miles of our laboratory."
> "**Per diem will be charged at 1.1 times the Federal (GSA) rate.**" OT 1.5× beyond 8/day or 40/week; **2.0× over 12 hours** or Sundays/holidays.

**[Terracon](https://eagenda.collincountytx.gov/docs/2024/CC/20240916_3004/56633_Amendment%20No.%202%20Modification%20to%20Exhibit%20C.pdf)**: "A **four (4) hour minimum charge**… is applicable to all trips"; "**The minimum charge is not applicable for trips to the project site for sample pick up only**"; "billed on a **portal to portal** basis from our office."

**[Los Gatos](https://weblink.losgatosca.gov/WebLink/ElectronicFile.aspx?dbid=0&docid=1262293)**: "Show-up time (less than 2 hours notice = 4 hour charge)"; OT tiers of 1.5× / 2× / **3×**; "shift differential +12.5%/hr for work 2:00 pm–4:00 am"; and the 50% lab expedite markup.

Each of those clauses is a function of *when the technician was notified, left, arrived, and departed* — data that lives on the handwritten daily report. Recovering it correctly requires someone to read every ticket against the right client's fee schedule. In practice the safe default is billing actual hours, which silently forfeits the minimum, the show-up charge, the cancellation charge, and the multiplier. Note the asymmetry: the firms *charge* for same-day cancellation, while technicians report "**schedule is day by day, so you don't know if you work Saturday until Friday around 5 pm**" ([UES reviews](https://www.indeed.com/cmp/Universal-Engineering-Sciences/reviews?fcountry=ALL&fjobtitle=Field+Technician)) and "**Lots of last minute jobs, inconsistent hours**" ([CMT Technical Services reviews](https://www.indeed.com/cmp/Cmt-Technical-Services-1/reviews)). The volatility is real and priced — but only if the paperwork captures it.

### P6 — Specimen break scheduling has tight tolerances and no alarm

**Who:** lab technician. **When:** daily. **Frequency:** every specimen set.

ASTM C39 age tolerances are narrow: **28 days ±20 hours**. A 28-day break that falls on a Sunday, a holiday, or the day the only Strength Testing Technician is out is a specimen that cannot be validly tested. There is no recovery — you cannot re-age a cylinder. The remedy is coring the structure.

Compounding: 56-day breaks are common in SCM-heavy mixes but **have no C39 age tolerance at all** — labs extrapolate, and that is an ambiguity, not a rule. And clients frequently need the 7-day early-warning break to decide whether to keep pouring.

**Current handling:** a wall calendar, a whiteboard, or an Excel sheet with a manually entered break date per set.

### P7 — Equipment calibration is a multi-cadence scheduling problem with content requirements, not just dates

**Who:** QA manager. **When:** perpetually. **Frequency:** dozens of items × several intervals.

R18 sets maximum intervals via Tables A1.1–A1.9. Reconstructed from state DOT derivatives, the cadences in a single CMT lab include: compression machine verification "**within 13 months**" *and* "immediately after relocation" *and* "immediately after repairs" ([ASTM C39](https://pdfcoffee.com/astm-c39-3-pdf-free.html)); moist room verification **6 months**; temperature recorder standardization **6 months**; cure tanks stirred **monthly**, refilled **24 months**; capping plates **12 months**; Type B air meter **3 months**; volumetric air meter **annually**; unit weight measures **annually**; C78 blocks lubricated **6 months**; single-use molds verified per C470 **per shipment**; sieves **12 months** *with recorded measurements of openings*; working thermometers **12 months**, reference thermometers **36 months**; gyratory mold "**12 months or 80 hours operation**"; kinematic viscometer tubes **36 months**; nuclear gauge leak and shutter tests **every 6 months** with records kept 3 years ([NRC](https://www.nrc.gov/materials/miau/miau-reg-initiatives/gltfaq)).

Two traps make this worse than a due-date list:

- **The record must contain specific content**, not just a date. Sieve records "did not include **measurements of critical dimensions**" is a written finding; go/no-go gauges are explicitly **insufficient** because "they provide no recorded measurements" ([AASHTO policy](https://aashtoresource.org/docs/default-source/publicdocuments/policy-and-guidance-on-go-no-go-gauges.pdf)). Digital thermometer records must carry "**separate unique identification numbers for both the readout and the probe**" ([thermometer policy](https://aashtoresource.org/docs/default-source/publicdocuments/aashto-accreditation-policy-and-guidance-on-thermometer-selection-and-records.pdf?sfvrsn=10)).
- **Calibration ≠ standardization ≠ check.** AASHTO re:source formally distinguishes them: calibration includes "**estimation of measurement uncertainty**"; standardization is the same minus the uncertainty ([Metrology Musings](https://aashtoresource.org/docs/default-source/newsletter/metrology-musings---calibration-vs-standardization---printer-friendly.pdf?sfvrsn=5)). A system that records a generic "calibration date" will generate findings.

### P8 — Field density reports carry silent methodology errors

**Who:** technician and reviewing engineer. **When:** on earthwork projects. **Frequency:** high on sitework-heavy jobs.

A percent-compaction result is meaningless unless the correct maximum dry density (Proctor) is referenced for that material and that location, and unless oversize corrections are applied and disclosed. Practitioners on [Eng-Tips](https://www.eng-tips.com/threads/compaction-testing-report.355658/) discussing a report on crushed rock with 38% oversize — above ASTM D1557's 30% threshold:

- **Ron:** "the only deficiency in the report… is that the report does not lay out all the assumptions and corrections that have been made"; the report "should include **both the corrected and uncorrected values**."
- **JuniorM:** "the deficiency of the report is that **it doesn't show the actual field density** and this is against ASTM."
- **JuniorM:** "there are lots of professionals who **don't understand the methodology and very often don't care**."

**Current handling:** the technician picks a Proctor from a folder of PDFs by memory or by asking. The reviewer may or may not catch a mismatch.

### P9 — Proficiency-sample failures start a clock that can end in a year out of accreditation

**Who:** QA manager. **When:** on PSP report issuance. **Frequency:** 1–2 rounds per program per year.

The math is published ([AASHTO re:source](https://aashtoresource.org/university/newsletters/newsletters/2016/08/02/proficiency-sample-ratings)): rating 5 at z ≤ 1, descending to rating 0 at z > 3; "**Any rating less than a 3 (z-score > 2) is considered a low rating.**" Within **60 calendar days** the lab must investigate, act, and document (AAP §8.3.1). Repeat ratings of ±1 or 0 on the same property across **two consecutive rounds** = suspension; a further failed round = **revocation**; reinstatement after revocation requires satisfactory ratings "for the **two last consecutive rounds**" ([suspension policy](https://aashtoresource.org/docs/default-source/publicdocuments/aashto-accreditation-policy-and-guidance-on-suspension-revocation-and-Reinstatement-Resulting-from-Proficiency-Samples-Issues.pdf?sfvrsn=18)).

Because many PSP programs ship only **one pair per year** ([PSP fees](https://aashtoresource.org/psp/fees)), the calendar arithmetic is brutal: a suspension can mean a year or more without accreditation for that method, and post-revocation reinstatement two more annual rounds. For a firm whose prequalification depends on that method, that is existential rather than administrative.

---

## 4. Application opportunities

Ten concepts. All are scoped as free open-source base tools with a paid customization path. Where a concept overlaps an incumbent platform, the differentiation is stated explicitly.

---

### 4.1 CureWatch — cure-room log auditor with specimen exposure mapping

**User:** lab technician and QA manager.
**Problem:** P4. The moist-room recorder produces ~35,000 readings a year that nobody reviews; the weekly C511 evaluation is a signature; when an excursion or gap is found later, nobody can say which specimens were affected.
**Current workflow:** export or ignore the logger; sign a weekly form; hope.
**Proposed workflow:** point the tool at the logger's CSV/XLSX export (or a folder of them). It parses the timestamp/temp/RH series, checks against 21.0–25.0 °C and ≥95% RH, and produces three outputs: (1) a one-page **weekly evaluation record** with the excursion summary, ready to sign and file — satisfying "evaluate weekly"; (2) an **excursion and gap register** listing every out-of-range period and, separately, every period with *missing data* (the failure mode most likely to be invisible); (3) given a specimen log (set ID, in-date, out-date), an **exposure report** naming every specimen present during each excursion.
**Inputs:** logger export; optional specimen in/out log (CSV export from whatever the lab uses); configured limits; recorder standardization dates.
**Outputs:** signed weekly PDF; excursion/gap register; specimen exposure list; an annual summary for the assessor.
**Essential features:** tolerant CSV parsing across common logger brands; explicit gap detection with configurable minimum gap; append-only evidence log so nothing can be silently edited; recorder-standardization due tracking (6 months); PDF output with the source file's hash recorded.
**Excluded from v1:** live logger integration/telemetry; alarms/notifications; multi-room dashboards; control of HVAC.
**AI:** inappropriate. This is arithmetic and interval logic. Adding a model would introduce non-determinism into a compliance record.
**Why not a spreadsheet:** a spreadsheet can chart 35,000 rows but cannot detect *missing* rows without deliberate work, cannot join to a specimen log, and produces no tamper-evident record. The exposure join is the part no spreadsheet gets built for.
**Complexity:** small-to-medium. **Learning:** minutes.
**Value:** eliminates a named recurring nonconformity; converts an unanswerable dispute question ("which cylinders?") into a one-click list. On the defense side, one avoided round of coring on a mid-rise pays for years of tooling.
**Risks:** the exposure report is a double-edged document — it creates discoverable evidence of a problem the firm might otherwise not have quantified. This must be framed honestly to buyers: it is a defensibility tool, and firms that would rather not know are not the customer. The falsification line must be enforced by design (append-only, no back-dating).
**Existing products:** MetaField/Omnant/QESTLab store calibration and QMS records; Giatec and Concrete Sensors sell maturity/wireless sensors (hardware plays). I found **no product that maps an environmental excursion window to the affected specimen population.**
**Customization potential:** high — per-lab logger formats, per-lab specimen ID schemes, multi-room and cure-tank variants.

---

### 4.2 SI Coverage Ledger — Statement of Special Inspections vs. reports actually filed

**User:** CMT department manager; the PE who stamps the final report.
**Problem:** P1. Coverage is never reconciled until closeout.
**Current workflow:** a PDF schedule, a folder of PDFs, and a memory.
**Proposed workflow:** the manager transcribes the Statement of Special Inspections once, at project setup, into a structured line-item list (item, code reference, continuous/periodic, required frequency, responsible party). Thereafter each filed daily report is tagged to one or more line items — either manually in 10 seconds or by parsing a filename/report header. The tool produces, on demand: a **coverage matrix** (required vs. covered vs. open), an **open-discrepancy register** with the date raised and the date closed, and a **closeout package** — the bookmarked PDF assembly plus a cover certification listing every item and its supporting reports.
**Inputs:** the SSI line items; the daily reports (PDFs) with a tag; discrepancy entries.
**Outputs:** weekly coverage-gap email/report; discrepancy register; assembled, bookmarked final-report PDF with an index.
**Essential features:** structured SSI entry with an import assist; per-report tagging; gap highlighting by phase so gaps surface *while the work is still accessible*; discrepancy lifecycle with the "time and method of notification" field Phoenix requires; PDF assembly with bookmarks.
**Excluded:** field data capture, scheduling, invoicing, client portal, e-signature.
**AI:** *optional, and only at one point* — extracting the SSI line items from the engineer's PDF table. That is genuine unstructured-document interpretation where conventional parsing fails on layout variation. Everything downstream must be deterministic. Ship v1 with manual entry; add extraction as an assist that a human confirms.
**Why not a spreadsheet:** the coverage matrix itself could be a spreadsheet. The PDF assembly, the bookmarked index, and the per-item evidence linkage cannot. And in practice the spreadsheet gets built on project #1 and abandoned by project #4.
**Complexity:** medium. **Learning:** ~1 hour, mostly for the SSI transcription convention.
**Value:** moves gap discovery from month 14 to week 3. Avoids remediation coring and CO delay.
**Risks:** the coverage matrix is an admission document if gaps exist — same honest framing as CureWatch. Also, tagging discipline is the failure mode: if technicians and PMs do not tag, the ledger is empty and lying.
**Existing products:** the integrated platforms produce reports and some produce closeout packages, but the reconciliation is against *their own* project setup, not against the EOR's schedule as a first-class object. Standalone: nothing found.
**Customization potential:** high — per-AHJ final-report formats, per-client cover-sheet language, firm templates.

---

### 4.3 CredMatrix — certification expiry, competency records, and "who can I send tomorrow"

**User:** department manager (dispatch) and QA manager (assessment).
**Problem:** P3.
**Current workflow:** one spreadsheet of certificate expiry dates, a folder of certificate scans, a separate binder of competency-evaluation forms, and a mental model of who is allowed to do what.
**Proposed workflow:** one data model with three tables — **people**, **credentials** (body, category, issue, expiry, renewal mechanism, certificate scan), and **competency evaluations** (person × test method × date × evaluator × comment) — plus a configurable **jurisdiction rulepack** mapping AHJ inspection categories to acceptable credentials. Queries the manager actually needs: *who is currently eligible for AHJ X category 2A?*; *what expires in the next 90 days, and what is the renewal mechanism for each?* (ACI = full re-exam, plan 6 months out; ICC = CEUs, plan differently); *which person × method competency evaluations are overdue against our own stated interval?*; *print the technician matrix the assessor will ask for.*
**Inputs:** roster; certificate data and scans; test-method list; the lab's own stated evaluation interval; AHJ rulepacks.
**Outputs:** eligibility answer; 30/60/90-day expiry report segmented by renewal mechanism; overdue-competency list; printable technician matrix and org chart.
**Essential features:** the AHJ rulepack as editable data, not code; explicit modeling that a supervisor's certificate does not cover subordinates; enforcement of the four required competency fields including full date; 5-year retention with no hard delete.
**Excluded:** training content, exam prep, scheduling/dispatch itself, HR records, payroll.
**AI:** inappropriate for the logic. Arguably useful *once*, to bootstrap the credential table from a pile of scanned certificates — a contained, human-verified extraction task.
**Why not a spreadsheet:** the expiry list is fine in a spreadsheet. The person × method × interval competency grid is not — it is three-dimensional, retention-bound, and must be queried two ways (by person for dispatch, by method for the assessor). Firms *do* keep it in a spreadsheet, and AASHTO re:source's own top-three nonconformity list tells you how well that works.
**Complexity:** medium. **Learning:** ~1 hour setup, then seconds per query.
**Value:** prevents the single most-cited category of assessment findings; prevents dispatching an ineligible inspector, which invalidates the inspection.
**Risks:** low regulatory risk; moderate privacy (personnel records — keep it local/self-hosted, no cloud requirement). The rulepack must be maintainable by the user, because AHJ requirements change and no vendor can track 20,000 jurisdictions.
**Existing products:** MetaField and Omnant both market certification tracking as a feature inside a platform. Nothing standalone, nothing that models the *jurisdictional eligibility* layer, nothing that separates certification from R18 competency evaluation — which is the distinction that actually generates findings.
**Customization potential:** very high — every firm's AHJ mix is different; rulepack authoring is a natural paid service.

---

### 4.4 TicketTrue — field ticket to invoice reconciliation against the client's rate schedule

**User:** department manager and billing.
**Problem:** P5.
**Current workflow:** technician hours → timesheet → someone applies the fee schedule from memory or from a PDF → invoice. Minimums, show-up charges, cancellation charges, portal-to-portal travel and multipliers are applied inconsistently or not at all.
**Proposed workflow:** encode each client's fee schedule once as structured rules — minimum blocks (4/8), show-up and cancellation tiers, notice-window premiums, portal-to-portal and mileage, OT tiers by hour-of-day and day-of-week, shift differentials, per-diem multipliers, equipment day rates, lab expedite markups, and exclusions (Terracon's "minimum charge is not applicable for trips for sample pick up only"). Feed in the week's field tickets (arrival/departure/notice times). The tool computes what *should* be billed, compares it to what *was* billed, and produces an exception list.
**Inputs:** rate-schedule rule set per client; field tickets with times; optional actual invoice lines for comparison.
**Outputs:** computed billable lines per ticket with the governing clause cited; under-billing exception list; a per-client summary of recovered value.
**Essential features:** rules as editable data with clause text attached to each rule so a disputed line can be defended by quotation; the "which rule governed this line" explanation; a look-back mode over prior periods.
**Excluded:** being an accounting system, AR, collections, timesheet capture, payroll.
**AI:** optional at the setup boundary only — assisting the initial translation of a PDF fee schedule into structured rules, with human confirmation. The computation must be deterministic; an AI-computed invoice is indefensible.
**Why not a spreadsheet:** a spreadsheet can hold one client's rules. A branch with 40 active clients has 40 different rate schedules with different minimum structures and OT definitions, and the reconciliation is per-ticket across all of them.
**Complexity:** medium. **Learning:** ~1 hour per rate schedule to encode, then automatic.
**Value:** direct revenue recovery, which is the easiest ROI conversation in this entire report. One missed 4-hour minimum at a $110/hr inspector rate is $440. A branch running 60 trips a week does not need many misses to fund this.
**Risks:** over-billing is the mirror risk and is worse than under-billing — the tool must present exceptions for human approval, never auto-invoice. Clause text attribution mitigates disputes.
**Existing products:** Deltek Ajera/Vantagepoint and BQE Core handle T&M billing but do not model minimum-block/show-up/cancellation logic natively; the CMT platforms do invoicing but as an integrated module, not as a reconciliation/audit tool. This is the pattern the ledger already recorded from commercial property management (escalation look-back audit) applied to a new domain.
**Customization potential:** very high — encoding a firm's client rate schedules is a natural paid onboarding service.

---

### 4.5 BreakBoard — specimen break scheduler with C39 age tolerances

**User:** lab technician; department manager.
**Problem:** P6.
**Current workflow:** whiteboard or spreadsheet with manually typed break dates.
**Proposed workflow:** log a specimen set once (project, set ID, cast date/time, count, specified strength, break schedule 7/14/28/56, mix ID). The tool computes each break's target datetime **and its valid window** from the C39 tolerance table, then produces the daily break list, a 14-day look-ahead, and — the differentiating output — a **risk list**: breaks whose valid window falls entirely on a weekend or holiday, or whose window opens and closes while the certified Strength Testing Technician is unavailable. It also flags sets where a 7-day result was below the trigger the client cares about, so the 28-day gets attention.
**Inputs:** specimen set log; holiday calendar; technician availability (optional).
**Outputs:** today's break list; 14-day look-ahead; window-risk list; overdue/missed register; per-set status.
**Essential features:** the tolerance table as data (24 h ±0.5 h, 3 d ±2 h, 7 d ±6 h, 28 d ±20 h, 90 d ±2 d); explicit handling of 56-day as *no published tolerance — firm policy required*, surfaced rather than silently assumed; missed-break register that never deletes.
**Excluded:** machine integration, result capture, report generation, LIMS.
**AI:** inappropriate.
**Why not a spreadsheet:** it nearly could be, and this is the concept where a spreadsheet template is the honest competitor. The wins are the window arithmetic (±20 hours is not a date), the holiday/availability collision detection, and the fact that the risk list is a *scheduling* output, not a log.
**Complexity:** small. **Learning:** minutes.
**Value:** each prevented missed 28-day break avoids either a coring campaign or an argument. Frequency is high; severity per event is high.
**Risks:** none material. Data is non-sensitive.
**Existing products:** every CMT platform schedules breaks. **ForneyVault** is purpose-built around concrete strength testing. The open-source niche is the firm that will not buy a platform — and the window-risk output, which I did not find advertised anywhere.
**Customization potential:** moderate — firm-specific break schedules, client early-warning rules.

---

### 4.6 CalCadence — calibration/standardization/check scheduler with record-content validation

**User:** QA manager.
**Problem:** P7.
**Current workflow:** a spreadsheet of due dates plus a binder of certificates.
**Proposed workflow:** an equipment register (name, in-service date, manufacturer, model, serial — the R18-required fields) where each item is bound to one or more **actions** typed as *calibrate*, *standardize*, or *check*, each with its own interval and its own **required record fields**. The tool schedules by interval, but it also **validates the record**: a sieve check with no recorded opening measurements is flagged incomplete; a digital thermometer record missing the probe's separate ID is flagged; a reference thermometer whose stated uncertainty exceeds half the working thermometer's accuracy is flagged. It handles event triggers (relocation, repair, "reason to suspect accuracy") as first-class re-verification events, and it prints an assessment binder in the order the assessor asks for it.
**Inputs:** equipment register; interval library (shipped with the published state-DOT-derived table, editable); calibration certificates as attachments; event log.
**Outputs:** due/overdue schedule; incomplete-record exception list; assessment binder PDF; per-item history.
**Essential features:** the calibrate/standardize/check distinction enforced in the data model; per-action required-field templates; event-triggered re-verification; usage-based intervals ("12 months **or 80 hours operation**").
**Excluded:** performing calibrations, uncertainty budget computation, asset depreciation, purchasing.
**AI:** inappropriate for the logic. Possibly useful to read a calibration certificate PDF into fields — a contained extraction task, human-verified.
**Why not a spreadsheet:** due dates fit a spreadsheet; *record content validation* does not, and content is what generates the findings. "Calibration records were not presented" and records that "did not include measurements of critical dimensions" are two different nonconformities and a date-only tracker prevents neither.
**Complexity:** medium — the interval library is the real work. **Learning:** ~1 hour.
**Value:** attacks AASHTO re:source's #1 named nonconformity family.
**Risks:** the shipped interval library must be clearly labeled as a starting point derived from published state DOT tables, **not** a substitute for R18 Tables A1.1–A1.9, which are copyrighted and must be purchased. Shipping wrong intervals would be actively harmful.
**Existing products:** MetaField, Omnant, QESTLab, R18LabQMS. R18LabQMS is the closest and is organized by R18 clause. The differentiation is content validation rather than storage, plus being free and self-hostable.
**Customization potential:** high — firm-specific interval policies (labs may set intervals shorter than the maximum), multi-branch rollups.

---

### 4.7 ReportGate — pre-transmittal daily report validator with per-AHJ rulepacks

**User:** the person who reviews reports before they leave (PM, manager, or the technician).
**Problem:** P2, specifically the "missing required field" half of it.
**Current workflow:** a reviewer reads each report and hopes to notice the missing arrival time or registration card number. Or nobody reads it.
**Proposed workflow:** define, per AHJ, the required elements of a daily report as a checklist-as-data rulepack — San Diego: permit number, work + specific location, conformance statement, arrival time, departure time, inspector name, **City registration card number**, signature; Phoenix: plus non-conforming items with "time and method of notification"; Santa Clara: plus resolution status and itemized authorized changes. The tool checks a structured report (or a form the technician fills) against the rulepack **before transmittal** and returns a pass/fail with the specific missing items.
**Inputs:** the report as structured data (or a simple form); the project's AHJ; the rulepack.
**Outputs:** pass/fail with itemized deficiencies; a clean PDF in the AHJ's expected layout; a transmittal log.
**Essential features:** rulepacks as editable YAML/JSON so firms can add their own AHJs; offline operation; a report template that is *also* the capture form so there is one keying, not two.
**Excluded:** photos and markup, GPS, e-signature workflows, client portal, dispatch.
**AI:** inappropriate for validation. Optionally useful to check narrative clarity — but this is exactly the "AI for novelty" the brief warns against, and a wrong AI edit to a legal record is a liability. Skip.
**Why not a spreadsheet:** a spreadsheet is a poor form and a worse validator; the value is the per-AHJ rule variation, which is a lookup problem.
**Complexity:** small-to-medium. **Learning:** minutes for the technician; ~1 hour to author a rulepack.
**Value:** removes the rework loop where a building official rejects a report for a missing element weeks later, and removes the "filled from memory" gap by putting the required fields in front of the technician on site.
**Risks:** Santa Clara's handwritten mandate means the tool sometimes produces a *supplement* to a handwritten form rather than a replacement. That must be designed for, not designed around.
**Existing products:** every CMT platform has field forms. None publish a per-AHJ rulepack library; each firm rebuilds its templates. An open, community-maintained AHJ rulepack repository is the durable asset here — and it is exactly the sort of thing a platform vendor will not build because it helps their competitors too.
**Customization potential:** high — authoring rulepacks for a firm's specific jurisdictions is a clean paid service.

---

### 4.8 ProctorCheck — field density report validator

**User:** technician (self-check) and reviewing engineer.
**Problem:** P8.
**Current workflow:** technician picks a Proctor from a folder; reviewer may or may not catch a mismatch; oversize corrections applied inconsistently and usually undisclosed.
**Proposed workflow:** maintain a small **Proctor library** per project (sample ID, material description, location/source, method D698 or D1557, max dry density, optimum moisture, oversize fraction, date). When a field density test is entered, the tool requires an explicit Proctor selection, recomputes percent compaction from the raw wet density and moisture, applies the ASTM D4718 oversize correction when the coarse fraction warrants it, and **requires both corrected and uncorrected values on the output** — the specific deficiency Ron identifies on Eng-Tips. It flags oversize above 30% as outside D1557's scope, prompting a documented alternative approach rather than a silent correction.
**Inputs:** Proctor library; field test raw values (wet density, moisture, gauge counts); location.
**Outputs:** validated field density report showing raw field density, referenced Proctor with its ID and material description, corrected and uncorrected percent compaction, and any scope flags.
**Essential features:** mandatory Proctor linkage (no free-text max density); recomputation from raw values rather than trusting the gauge display; the >30% oversize gate; D4718 correction shown transparently.
**Excluded:** gauge integration, GIS/plan location plotting, statistical acceptance analysis.
**AI:** inappropriate.
**Why not a spreadsheet:** many firms already have a spreadsheet doing the arithmetic. The addition is the enforced linkage to a Proctor record and the refusal to emit a report that hides its corrections.
**Complexity:** small. **Learning:** minutes.
**Value:** prevents a defect class that is invisible until litigation or a settlement problem. Moderate frequency, high severity when it bites.
**Risks:** none material.
**Existing products:** platform LIMS modules compute this. Standalone open tools are thin. Differentiation is the disclosure discipline, not the math.
**Customization potential:** moderate.

---

### 4.9 CARClock — nonconformity and proficiency-sample corrective action tracker

**User:** QA manager.
**Problem:** P9, plus the 60-day AAP nonconformity clock generally.
**Current workflow:** an email thread and a Word file per finding.
**Proposed workflow:** each finding (assessment nonconformity or low PSP rating) becomes a tracked item with its **statutory clock** attached — 60 days from final report issuance, +30 with a filed written plan, escalation at 120. PSP results are entered per round with z-score and rating; the tool computes the **suspension-risk state** (has this test property received ±1/0 on both samples in consecutive rounds?) and warns *before* the second round, not after. Each item carries a structured root-cause and corrective-action record in the form the assessor expects, with evidence attachments.
**Inputs:** findings; PSP round results; assessment dates; program ship calendars.
**Outputs:** clock dashboard with days remaining; suspension-risk warnings; printable CAR packet; historical performance chart per test property.
**Essential features:** the clock math including the 30-day extension gate; the two-consecutive-rounds suspension rule modeled explicitly; PSP calendar awareness (CCRL concrete ships August–November; most soil/aggregate programs ship one pair per year).
**Excluded:** internal audit management, full QMS document control, management review.
**AI:** inappropriate for the logic; possibly a drafting assist for the corrective-action narrative, which is genuinely a writing task — but keep it optional and clearly labeled.
**Why not a spreadsheet:** the clock is spreadsheet-able. The suspension-risk state machine across rounds is where spreadsheets fail quietly, and it is the part with existential consequences.
**Complexity:** small-to-medium. **Learning:** minutes.
**Value:** high severity, low frequency — which is why it scores below the daily-pain concepts despite mattering enormously when it fires.
**Risks:** must not be presented as accreditation advice.
**Existing products:** R18LabQMS covers CAR tracking as part of a QMS product. Nothing models the suspension-risk state machine as an early warning.
**Customization potential:** moderate.

---

### 4.10 SprayCount — SFRM thickness sampling planner and calculator

**User:** the fireproofing special inspector.
**Problem:** a bounded but genuinely error-prone slice of P2 — E605 sampling frequency and averaging done on paper with a calculator.
**Current workflow:** paper sheet, hand-tallied measurements, mental arithmetic against a tolerance, hand-counted member percentage.
**Proposed workflow:** enter floor area and the member schedule. The tool computes the **required sampling plan** — one thickness test per 1,000 sf, not fewer than four measurements per 1,000 sf, 25% of structural members per floor, one bond test per 10,000 sf — then accepts measurements, computes averages, and compares against design thickness less the applicable tolerance (¼ in. for designs ≥1 in.; 25% for designs <1 in.). Output is a completed, arithmetic-checked report showing the plan, the coverage achieved, and every pass/fail.
**Inputs:** floor areas; member schedule; design thicknesses; measurements; bond test results.
**Outputs:** sampling plan; completed inspection report; a coverage statement (did we actually hit 25% of members?).
**Essential features:** the frequency rules as data; the two-tier tolerance logic; running coverage tracking across floors.
**Excluded:** everything else.
**AI:** inappropriate.
**Why not a spreadsheet:** it is a spreadsheet, honestly — but one that most inspectors do not have, that gets the member-percentage denominator wrong, and that does not carry the plan/coverage reconciliation. Low ceiling, low cost.
**Complexity:** small. **Learning:** minutes.
**Value:** modest per project; useful as an easy first build and a credibility artifact.
**Risks:** none.
**Existing products:** none found standalone.
**Customization potential:** low-moderate.

---

## 5. Opportunity ranking

Scored 1–5 on each of ten criteria; maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of build | Stays narrow | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 4.1 | **CureWatch** | 5 | 5 | 5 | 5 | 4 | 5 | 5 | 4 | 5 | 5 | **48** |
| 4.2 | **SI Coverage Ledger** | 5 | 4 | 5 | 4 | 3 | 4 | 5 | 5 | 4 | 5 | **44** |
| 4.3 | **CredMatrix** | 5 | 5 | 4 | 4 | 4 | 4 | 4 | 5 | 4 | 5 | **44** |
| 4.4 | **TicketTrue** | 5 | 5 | 5 | 4 | 3 | 4 | 5 | 5 | 3 | 5 | **44** |
| 4.5 | **BreakBoard** | 4 | 5 | 4 | 5 | 5 | 5 | 3 | 3 | 5 | 5 | **44** |
| 4.6 | **CalCadence** | 5 | 4 | 4 | 4 | 3 | 3 | 4 | 5 | 4 | 5 | **41** |
| 4.7 | **ReportGate** | 3 | 5 | 3 | 5 | 4 | 4 | 4 | 5 | 4 | 4 | **41** |
| 4.8 | **ProctorCheck** | 4 | 4 | 3 | 5 | 4 | 5 | 3 | 3 | 4 | 3 | **38** |
| 4.9 | **CARClock** | 4 | 2 | 3 | 5 | 5 | 5 | 3 | 3 | 3 | 5 | **38** |
| 4.10 | **SprayCount** | 3 | 3 | 3 | 5 | 5 | 5 | 4 | 3 | 3 | 4 | **38** |

### The top three

**1. CureWatch (48).** It wins because it is the only concept where every criterion is simultaneously strong. The requirement is published and precise (21.0–25.0 °C, ≥95% RH, every 15 minutes, evaluated weekly, recorder standardized every 6 months). The failure is a *named* nonconformity in the assessing body's own published findings list. The input is a file the lab already has and never opens. The core computation is trivial. And the differentiating output — mapping an excursion window to the specimen population that was in the room — is something I could not find in any product, free or paid, and is the output that converts a vague worry into a bounded answer. It is also the smallest build with the largest asymmetry: a few hundred lines of parsing and interval logic standing between a firm and an unbounded challenge to its strength data.

**2. SI Coverage Ledger (44, and the one I would build second).** Highest ceiling, and the most strategically interesting because it changes *when* a firm learns something rather than just how fast it types. Coverage gaps discovered in week 3 are free; discovered at closeout they cost coring, CO delay, and possibly a claim. The reason it does not rank first is build risk: the SSI transcription step is a real adoption tax, tagging discipline is a real failure mode, and the closeout PDF assembly is more engineering than it looks. But it is the concept with the clearest path to a paid customization business, because every AHJ wants the final report in its own shape.

**3. Three-way tie at 44 — CredMatrix, TicketTrue, BreakBoard.** These separate by *what kind of buyer conversation you want to have.* **TicketTrue** is the easiest sale (it finds money) and the hardest build (40 rate schedules, and over-billing risk if you get it wrong). **CredMatrix** attacks two of the assessing body's three named nonconformity families and is the one the QA manager will ask for by name. **BreakBoard** is the fastest to ship — probably a weekend — and the best trust-builder, but it has the weakest differentiation because every platform already does break scheduling.

### What to investigate next

**CureWatch first**, for the reasons above and because it is buildable and demonstrable without any customer data — a synthetic logger CSV with a deliberate three-hour gap and a two-day excursion is enough for a compelling demo.

**Then validate SI Coverage Ledger before building it.** The whole concept rests on one assumption I could not verify from public sources: that firms will accept the cost of transcribing the Statement of Special Inspections once per project. If they will not, the concept collapses to a manual checklist and should be dropped in favor of TicketTrue. That is the single most important interview question in §6.

---

## 6. Validation plan

### Questions to ask practitioners

**On CureWatch (ask a lab manager or QA manager):**
1. Walk me through what happened the last time your moist room went out of range or the logger stopped. How did you find out? What did you do about the specimens that were in there?
2. Who signs the weekly C511 data evaluation, and what do they actually look at before signing?
3. Has an assessor ever written you up for cure-room records? What did the finding say verbatim?
4. If you could push a button and get a list of every specimen present during an excursion — would you want that list to exist? *(This is the honest question. A "no" is a real answer and reshapes the product.)*

**On SI Coverage Ledger (ask a CMT department manager and a PE who stamps final reports):**
5. When you write the final report of special inspections, how do you confirm every required item was actually covered? Show me.
6. Have you ever discovered a coverage gap at closeout? What did it cost to resolve?
7. **Would you spend 30–45 minutes at project start transcribing the Statement of Special Inspections into a structured list if it gave you a weekly gap report?** *(The make-or-break question.)*
8. Who tags reports to inspection items today, if anyone?

**On TicketTrue (ask a department manager and whoever produces invoices):**
9. How many distinct client rate schedules are active in your branch right now?
10. When a contractor cancels after your tech has left the yard, does that 4-hour charge reliably reach the invoice? How do you know?
11. Has a client ever disputed a minimum-hour charge? How did you defend it?

**On CredMatrix:**
12. Show me how you answer "who can I send to a City of ___ reinforced-concrete inspection tomorrow."
13. How do you track R18 competency evaluations as distinct from certifications? What did the last assessor ask to see?

### Who to interview

- CMT department managers at 1–3 branch firms (the Terradyne-style role) — the actual buyer.
- QA managers at AASHTO-accredited CMT labs; find them through **AASHTO re:source's public directory of accredited laboratories** and through state ACI chapters.
- Building officials / plan-check supervisors in two or three jurisdictions with published SI programs (San Diego, Santa Clara, Phoenix, Spokane) — they will tell you what makes them reject a report.
- Structural engineers of record who sign final reports of special inspections (reachable via SEAOC/NCSEA chapters).
- An AASHTO re:source assessor, if one will talk informally — they see 40+ labs a year and know exactly which records are always missing.

### Further search terms

`"final report of special inspections" template site:.gov` · `"special inspection agreement" agency responsibilities weekly report` · `ASTM C511 moist room nonconformity corrective action` · `AASHTO R18 internal audit checklist` · `"technician matrix" accreditation assessment` · `CMT laboratory "quality manual" filetype:pdf` · `"schedule of special inspections" excel` · `construction materials testing rate schedule filetype:pdf minimum charge` · `r/civilengineering CMT technician daily reports` *(note: Reddit was inaccessible from this research environment and remains an unexplored evidence source)*

### Sample files needed for testing

- A real moist-room data logger export (Onset HOBO, Dickson, Extech, Lascar are common) with at least a year of data, ideally containing a genuine gap.
- Two or three complete Statements of Special Inspections from real projects, in different AHJs, to test extraction and the line-item model.
- A set of daily field reports from one project, spanning several inspection categories.
- Three CMT fee schedules from different firms (public agency contract exhibits are a legitimate free source — the NV5, Terracon and Los Gatos schedules cited above are already public).
- A lab's equipment register and a handful of calibration certificates.
- A specimen log with cast dates, break schedule, and actual break dates.

### Minimum prototype that would validate

For **CureWatch**: a single-file Python script (or a browser-only HTML page — no upload, no server, which also solves the privacy objection) that takes a logger CSV and a specimen CSV and emits the three outputs. Demo it to three QA managers with their own file. The validating signal is whether they immediately ask "can you run this on last year's data?"

For **SI Coverage Ledger**: skip the software. Do it by hand on one real project, produce the coverage matrix, and see whether the manager's reaction is relief or indifference. If the by-hand version does not produce a visible reaction, the software will not either.

### Assumptions most likely to be wrong

1. **That firms want the exposure report.** CureWatch creates discoverable evidence. Some firms will actively prefer not to have it. If interviews show this, the product survives but the positioning must shift entirely to *prevention and weekly compliance*, with the exposure map as an optional module.
2. **That the SSI transcription cost is acceptable.** If not, concept 4.2 dies.
3. **That the buyer will adopt a free tool at all.** This market's decision-makers are $60k department managers with "basic computer skills such as Word and Excel," working inside firms with IT policies. A tool requiring a server install may be dead on arrival; a single HTML file or a single .exe may be the only viable delivery form. **This assumption cuts across every concept in this report and should be tested first.**
4. **That the integrated platforms have not already shipped these features.** My evidence on what MetaField/Aldoa/Omnant/QESTLab actually do is from their marketing sites, not from using them. A trial account for each would sharpen the differentiation claims considerably.
5. **That practitioner pain matches vendor-described pain.** A meaningful share of the "current state" evidence in §3 comes from vendor content. It is specific enough to suggest customer-interview provenance, but it is not independent, and Reddit — the obvious independent source — was unreachable from this environment.

---

## 7. Cross-industry patterns

Six patterns from this market that transfer to named markets already in the backlog.

**1. Exposure-window linkage — when a monitored environment goes out of spec, enumerate every unit of work that was inside it.** The core of CureWatch. The general form is: continuous environmental/process monitoring + a log of items and their residency intervals + a join. Transfers to **Metal finishing, plating, heat treat and NDT job shops** (furnace excursions → which lots were in the load), **Contract manufacturers serving FDA-regulated medical devices** (environmental monitoring excursions → affected lots), **Federally qualified health centers** (vaccine cold-chain excursions → affected doses), **Calibration and metrology service providers** (out-of-tolerance-on-receipt → every measurement made with that instrument since its last good calibration), and **Warehouse and 3PL fulfillment**.

**2. Interval-and-evidence compliance calendar — schedule by interval, but also validate that each record contains the fields the auditor will demand.** The insight is that due-date tracking is the easy half and record-content validation is where the findings actually come from. Transfers to **Calibration and metrology service providers / in-house gage management**, **Fire protection inspection, testing and maintenance (ITM) contractors under NFPA 25**, **Contract manufacturers serving FDA-regulated medical devices (ISO 13485/QMSR)**, **Small defense suppliers navigating CMMC Level 2**, and **Dental and specialty clinic practice administration**.

**3. Coverage reconciliation — a required-scope schedule versus the deliverables actually filed, producing a gap list before an external gate closes.** Transfers to **Nonprofit grant management and compliance** (required reports vs. submitted), **Construction submittal, RFI, and closeout coordination**, **Immigration law practice** (required exhibits vs. assembled), **Title, escrow, and real estate closing**, **Small defense suppliers navigating CMMC Level 2** (control set vs. evidence), and **Commissioning (Cx) providers for small and midsize buildings**.

**4. Contract rate-schedule reconciliation — recompute what should have been billed from primary field time records against a per-client fee schedule containing minimums, tiers, multipliers and exclusions, then present exceptions for approval.** This extends the escalation-audit pattern already recorded from commercial property management into time-and-materials service work. Transfers to **Freight brokerage and dispatch operations** (accessorials, detention), **Staffing and recruiting agency operations**, **Machine shop / job shop quoting**, **Electrical or plumbing trade subcontractor field operations**, **Third-party truck dispatch services**, and **Small-firm litigation support**.

**5. Person × task-authorization matrix with expiry and jurisdiction variance — who is legally permitted to do this specific task, in this specific place, today.** Distinct from generic credential tracking because the *rule mapping the credential to the task varies by jurisdiction or customer*, and because the authorization must be queryable in both directions (by person for dispatch, by task for audit). Transfers to **HR and benefits administration in companies under 200 employees**, **Staffing and recruiting agency operations**, **Electrical or plumbing trade subcontractor field operations**, **Fire alarm system design and programming subcontractors**, **Title 24 acceptance test technicians (ATT)**, and **Independent property and casualty claims adjusting** (state adjuster licensing).

**6. Tolerance-window scheduling for perishable or aging work items — the deadline is a window, not a date, and missing it destroys the item.** Transfers to **Medical billing and revenue cycle** (timely-filing windows), **Geotechnical and environmental consulting** on the environmental side (analytical hold times), **Title abstracting** (search currency windows), **Estate planning and probate practice** (statutory filing windows), and **Multi-state charitable solicitation registration compliance**.

---

## 8. Sources and confidence

### Verified findings — primary sources

**Code and jurisdiction requirements**
- [CBC/IBC §1704.2.4, reporting and final report](https://gocodebook.com/us/california/california-building-code/special-inspections/process-and-responsibilities/special-inspector-qualifications-access-and-reporting)
- [IBC §1703, approved agency independence, equipment calibration, personnel](https://www.drjcertification.org/ibc-section-1703)
- [San Diego Technical Bulletin BLDG-17-2 — daily report contents, registration card, calibration certificates affixed](https://www.sandiego.gov/development-services/forms-publications/technical-bulletins/BLDG-17-2)
- [Santa Clara GA31 — daily *handwritten* report, weekly transmittal, stamped final report before CO](https://www.santaclaraca.gov/home/showpublisheddocument/67169/639138254471370000)
- [San Ramon Special Inspection & Testing Agreement — weekly reports](https://www.sanramon.ca.gov/our_city/departments_and_divisions/community_development/building_and_safety_services/special_inspections/special_inspection_testing_agreement)
- [Phoenix Special Inspection & Observation Manual — nonconforming items, time and method of notification](https://www.phoenix.gov/content/dam/phoenix/pddsite/documents/trt/external/dsd_trt_pdf_00595.pdf)
- [Spokane minimum qualifications matrix for special inspectors](https://static.spokanecity.org/documents/business/resources/permitting/commercial/guidesheets/special-inspection-qualifications.pdf)
- [Catawba County SI Chapter 13 — SFRM thickness and bond test frequencies](https://www.catawbacountync.gov/building/_pdfs/SICCChapter13.pdf)

**Accreditation and quality system**
- [AASHTO AAP Procedures Manual](https://aashtoresource.org/docs/default-source/publicdocuments/aap-procedures-manual.pdf) — 27-month tours, 60-day nonconformity clock, digital QMS permitted, technical director limits
- [AASHTO policy on certifications](https://aashtoresource.org/docs/default-source/publicdocuments/aap-pandg-certification-review.pdf) — expired certifications not accepted; supervisor certs do not cover staff
- [AASHTO policy on training and competency evaluation](https://aashtoresource.org/docs/default-source/publicdocuments/aashto-accreditation-policy-and-guidance-on-training-and-competency-evaluation.pdf?sfvrsn=4)
- [Mastering AASHTO R 18: Common Pitfalls](https://aashtoresource.org/university/newsletters/newsletters/2024/08/27/mastering-aashto-r18-common-pitfalls) — top three nonconformity families
- [The Cure for the Cure: ASTM C511 guide](https://aashtoresource.org/docs/default-source/newsletter/the-cure-for-the-cure--a-guide-to-astm-c511-and-your-curing-facilities---printer-friendly.pdf?sfvrsn=6)
- [Common findings — ASTM C31/C39/C78/C511](https://aashtoresource.org/docs/default-source/newsletter/common-findings-in-concrete-assessments-astm-c31-c39-c78-c511.pdf)
- [Common findings — ASTM C138/C172/C173/C231/C617/C1231](https://aashtoresource.org/docs/default-source/newsletter/common-findings-in-concrete-assessments---astm-c138-c172-c173-c231-c617-c1231.pdf?sfvrsn=2)
- [Metrology Musings: calibration vs. standardization](https://aashtoresource.org/docs/default-source/newsletter/metrology-musings---calibration-vs-standardization---printer-friendly.pdf?sfvrsn=5)
- [Thermometer selection and records policy](https://aashtoresource.org/docs/default-source/publicdocuments/aashto-accreditation-policy-and-guidance-on-thermometer-selection-and-records.pdf?sfvrsn=10)
- [Go/no-go gauge policy](https://aashtoresource.org/docs/default-source/publicdocuments/policy-and-guidance-on-go-no-go-gauges.pdf)
- [Proficiency sample ratings and z-scores](https://aashtoresource.org/university/newsletters/newsletters/2016/08/02/proficiency-sample-ratings)
- [Suspension, revocation and reinstatement policy](https://aashtoresource.org/docs/default-source/publicdocuments/aashto-accreditation-policy-and-guidance-on-suspension-revocation-and-Reinstatement-Resulting-from-Proficiency-Samples-Issues.pdf?sfvrsn=18)
- [AAP fees](https://aashtoresource.org/aap/fees) · [LAP fees](https://aashtoresource.org/lap/tests-and-fees) · [PSP fees](https://aashtoresource.org/psp/fees) · [LAP overview](https://aashtoresource.org/lap/overview)
- [CCRL Laboratory Inspection Program](https://www.ccrl.us/Lip/LipProgramDescriptions.html) · [CCRL PSP](https://www.ccrl.us/Psp/PspProgramDescriptions.html)
- [IAS AC89 (June 2025)](https://www.iasonline.org/wp-content/uploads/2025/07/AC89-Final-new.pdf) · [A2LA CMT program](https://a2la.org/accreditation/construction-materials/) · [CMEC](https://cmec.org/testing-laboratories)

**Certification bodies**
- [ACI Concrete Field Testing Technician Grade I](https://www.concrete.org/certification/certificationprograms.aspx?m=details&pgm=Field+Concrete+Testing&cert=Concrete+Field+Testing+Technician%E2%80%94Grade+I) — 5-year cycle, full re-exam
- [WACEL prerequisites](https://www.wacel.org/technician-certification-program/technician-certification-program-prerequisites/) · [ICC renewal bulletin](https://www.iccsafe.org/wp-content/uploads/Renewal_EIB.pdf) · [NICET recertification](https://www.nicet.org/recertify/)

**Test methods, intervals, and field practice**
- [ASTM C39 text — age tolerances, machine verification, dimensional limits](https://pdfcoffee.com/astm-c39-3-pdf-free.html)
- [NRMCA CIP 35 — required break record contents; 2% diameter invalidation rule](https://www.concreteanswers.org/CIPs/CIP35.htm)
- [NRMCA CI 40-08 — initial curing temperatures, 4-hour transport, strength penalties](https://www.nrmca.org/wp-content/uploads/2020/06/CI4008cylindercuring.pdf)
- [AZDOT Appendix A3 calibration intervals](https://apps.azdot.gov/files/materials-manuals/materials-testing/appendix-a3-181102.pdf) · [WSDOT standardize and check procedures](https://wsdot.wa.gov/sites/default/files/2021-10/Standardize-And-Check-Procedures-For-Region-Equipment.pdf) · [ODOT SOP-106](https://www.odot.org/materials/C97001_WEB_REP/SOP/SOP-106.pdf)
- [TDOT SOP 7-1 nuclear gauge procedures](https://www.tn.gov/content/dam/tn/tdot/hq-materials-tests/standard-operating-procedures/SOP_7-1.pdf) · [NRC general license FAQ — 6-month leak/shutter tests](https://www.nrc.gov/materials/miau/miau-reg-initiatives/gltfaq)
- [Ready-mix delivery and point-of-discharge method statement](https://quollnet.com/methods/method-statement-ready-mix-concrete-delivery-ticket-inspection-and-point-of-disc)
- [The Masonry Society, Special Inspection & Testing](https://learn.masonrysociety.org/wp-content/uploads/2020/09/Special-Inspection-Testing_2019-10-31.pdf)

**Commercial terms (public contract exhibits)**
- [NV5 West fee schedule](https://resources.finalsite.net/images/v1698078886/simivalleyusdorg/uplyxudmdpr7vqnixs5i/101723MeasureXAuthorizations.pdf) · [Terracon schedule](https://eagenda.collincountytx.gov/docs/2024/CC/20240916_3004/56633_Amendment%20No.%202%20Modification%20to%20Exhibit%20C.pdf) · [Los Gatos schedule](https://weblink.losgatosca.gov/WebLink/ElectronicFile.aspx?dbid=0&docid=1262293) · [Pacific Crest Engineering](https://mcwd.org/docs/agenda_minutes/2019_board/2019-09-16_board/Item%2010-B%20-%20Attachment%203a4%20-%20Pacific_Crest_Engineering_Rate_Schedule.pdf) · [Butano Geotechnical](http://www.butanogeotech.com/schedule-of-fees)

**Practitioner voices**
- [Eng-Tips — Structural Special Inspections, Compliance or Complacence](https://www.eng-tips.com/threads/structural-special-inspections-compliance-or-complacence.417314/)
- [Eng-Tips — Missed Special Inspection](https://www.eng-tips.com/threads/missed-special-inspection.199057/)
- [Eng-Tips — Compaction testing report](https://www.eng-tips.com/threads/compaction-testing-report.355658/)
- [TheBuildingCodeForum — Sketchy Special Inspections?](https://www.thebuildingcodeforum.com/forum/threads/sketchy-special-inspections.35237/)
- [Terracon technician reviews](https://www.indeed.com/cmp/Terracon-Consultants-Inc/reviews?fjobtitle=Engineering+Technician) · [UES field technician reviews](https://www.indeed.com/cmp/Universal-Engineering-Sciences/reviews?fcountry=ALL&fjobtitle=Field+Technician) · [CMT Technical Services reviews](https://www.indeed.com/cmp/Cmt-Technical-Services-1/reviews)
- [Terradyne CMT Department Manager posting](https://to.indeed.com/aaxphz966tmv) · [UES CMT Field Technician posting](https://to.indeed.com/aagpplgpgwmn) · [HVEA technician job description](https://hveapc.com/careers/job-description-material-testing-technician/)

**Trade press**
- [Beton Consulting — ASTM C31 and C39: what could go wrong](https://www.betonconsultingeng.com/astm-c31-and-c39-what-could-go-wrong/) · [Concrete Facts — Bad concrete or bad testing?](https://concretefactsmagazine.com/2026/06/18/bad-concrete-or-bad-testing-handling-low-cylinder-breaks-in-concrete-testing/) · [STRUCTURE — Discrepancies in concrete strength testing](https://www.structuremag.org/article/a-look-at-discrepancies-in-concrete-strength-testing/) · [Asphalt Magazine — To assess or not to assess?](https://www.asphaltmagazine.com/to-assess-or-not-to-assess/) · [Concrete Sensors — 100 calls a year from poor lab QC](https://concretesensors.com/cylinders-are-crushing-productivity-and-quality/) · [AASHTO Journal — laboratory assessments](https://aashtojournal.transportation.org/aashto-resource-podcast-looks-at-laboratory-assessments/)

### Strong inferences — reasoned from verified facts, not directly stated by a source

- **The 360-record competency grid.** Derived from R18's per-person-per-method evaluation requirement plus typical lab staffing and method counts. The requirement is verified; the arithmetic is mine.
- **Nuclear gauge compliance is a separate records silo** from the R18 equipment records (NRC license, RSO, dosimetry, leak tests, standard counts, DOT shipping papers). Verified separately as a requirement; the "separate silo" claim is inference.
- **The multi-cadence scheduling problem.** CCRL's fixed annual PSP ship months + a ~27-month assessment tour + 12-month status review + 12-month management review + rolling 3/6/12/24/36-month calibration intervals do not fit any single calendar view. Each component verified; the synthesis is inference.
- **A PSP suspension can mean a year or more out of accreditation for a method**, because many programs ship one pair per year. Both facts verified; the consequence is arithmetic.
- **CMT chain of custody has no prescriptive form** analogous to the environmental-lab COC — the requirement is functional (identify, handle, store, trace, name personnel), so every lab invents its own and every assessor evaluates it against the lab's own written procedure. This explains why "records that contradict stated QMS policies" is a named finding.
- **Billing under-recovery.** The rate-schedule complexity is verified verbatim; that firms systematically under-collect minimums and cancellation charges is a strong inference from the structure plus the manual reconstruction workflow. **Not verified. This is the assumption behind TicketTrue and it needs a practitioner to confirm or kill it.**

### Tentative hypotheses requiring practitioner validation

- That firms **want** a specimen-exposure report. Could go either way.
- That the SSI transcription cost is acceptable to managers.
- That a free, self-hosted or single-file tool is deliverable inside these firms' IT constraints at all.
- That the integrated platforms have not already shipped these exact features — my knowledge of them is from marketing pages only.
- That cure-room log gaps are common. I found the *requirement* and the *named nonconformity for failing the weekly evaluation*, but no published statement of how often gaps occur or what specifically happens when one is found. This is the single most important gap in the evidence behind the top-ranked concept.

### Research limitations to disclose

1. **Reddit was inaccessible** from this environment (403 on both search-domain filters and direct fetch) across both research passes. r/civilengineering, r/geotech, and r/construction are the obvious independent practitioner sources for this market and remain entirely unexamined. Any claim in this report that reads like forum sentiment comes from Eng-Tips, TheBuildingCodeForum, or Indeed reviews instead.
2. **Vendor content is load-bearing in places.** MetaField, Omnant, Aldoa, ATSER and Certified MTP supplied several of the most vivid "current state" descriptions. They are specific enough to suggest customer-interview provenance, but they are marketing and are labeled as such throughout. Vendor-claimed magnitudes (MetaField's "91% reduction in report turnaround," "14 to 21 days preparing for an audit"; Aldoa's "95% fewer data entry errors") are **not** used as evidence anywhere in §3 or §5.
3. **AASHTO R 18 Tables A1.1–A1.9 are paywalled.** The interval table in §3/P7 is reconstructed from state DOT derivatives (AZDOT, WSDOT, ODOT, MnDOT) and AASHTO re:source newsletters. Before shipping CalCadence, the actual standard must be purchased.
4. **UpCodes blocks automated fetching**, so IBC Tables 1705.2 and 1705.3 (the continuous-vs-periodic grids) could not be reproduced verbatim.
5. **The double-entry cost figures** (45–75 min/report, $12–15/transaction) come from general construction daily reporting, not CMT, and are labeled directional only.
6. **No "24-hour reporting rule" exists in the model code.** If a future report or product claims one, it is wrong. Report frequency is contractual and jurisdictional.

---

*Report produced under claim 88358944 · 2026-08-06*
