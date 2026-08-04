# Market Research Cycle — Mechanical (HVAC) Design Engineering at Small MEP Consulting Firms

## Narrow Subspecialty: HVAC Alterations and Equipment Replacement in Existing Nonresidential Buildings

---

## 0. Cycle Header

| Field | Value |
|---|---|
| **Market claimed** | Mechanical (HVAC) design engineering at small MEP consulting firms |
| **Angle claimed** | narrow-subspecialty |
| **Named subspecialty** | HVAC alterations, retrofits, and equipment replacement in **existing** nonresidential buildings — tenant improvements, rooftop-unit and air-handler replacements, boiler/chiller swaps, and controls retrofits — including the energy-code compliance documentation chain that gates the permit and the certificate of occupancy |
| **Claim ID** | `1c509b0e` |
| **Date** | 2026-08-04 |
| **Backlog remaining after this claim** | 164 assignments (before this cycle's discoveries were appended) |

### Why this assignment over the others available

Three filters were applied in the order the brief specifies.

**Breadth first.** Five assignments are complete, covering five markets. Mechanical/HVAC design at small MEP firms had **zero** completed entries, so it adds a new market to the catalog rather than deepening one already touched. Roughly 40 backlog markets are in the same position, so this alone did not decide it.

**Angle diversity.** Of the five completed reports, three are `core-practitioner-workflow`, one is `back-office`, and one is `handoffs-and-qa`. **`narrow-subspecialty` had never been run.** Choosing it forces the catalog's first genuinely narrow, named-niche investigation, which is the angle most likely to surface tools small enough to actually build.

**Evidence availability.** This subspecialty sits on top of an unusually well-documented regulatory surface: California's 2025 Title 24 Part 6 took effect 1 January 2026 and publishes its alteration triggers, its 23 mechanical acceptance-test forms, and its compliance-form catalog online in citable detail; the DOE/PNNL Commercial Energy Code Field Study publishes measured compliance failure data nationally; and jurisdictional COMcheck submittal guidelines publish exactly what gets a mechanical permit rejected. Very few markets in the backlog offer that density of *verifiable* practitioner-facing rules.

**Rejected alternatives worth naming.** *Structural engineering / narrow-subspecialty* was a close second on breadth but the equivalent regulatory surface (IEBC alteration levels) is less machine-readable. *Special hazard / clean agent suppression design* (backlog item 108) is attractive and adjacent to fire protection already covered, but it only has `core-practitioner-workflow` in the backlog, so taking it would have repeated the catalog's most-used angle. *Flood zone / FEMA elevation certificate consulting* has an excellent published error statistic but is a very small trade; it stays high on the list for a future cycle.

One limitation of this cycle should be stated up front: **the search proxy could not reach Reddit**, which removed the richest source of unfiltered practitioner complaint. Evidence below leans on engineering forums (Eng-Tips, The Building Code Forum), federal field studies, code-authority publications, and trade press instead. Section 8 marks which findings are consequently weaker.

---

## 1. Market Examined

**Industry.** Mechanical/HVAC consulting engineering — NAICS 541330 (Engineering Services). BLS counted roughly 964,620 workers across all of 541330; the mechanical/MEP building-systems slice is a small fraction of that, and it is structurally dominated by small firms. ACEC's own commentary to the SBA on size standards reflects an industry where the overwhelming majority of firms are well under the small-business threshold.

**Professional role.** The target user is the mechanical design engineer or senior designer — often the *only* mechanical person on the project — at a firm of roughly **2 to 30 staff**. Titles vary: Mechanical Designer, HVAC Design Engineer, Project Engineer, Principal. At the smallest firms one person does field survey, load calculation, equipment selection, drafting, energy-code forms, permit response, submittal review, and construction administration on the same project. There is no dedicated energy-code specialist, no dedicated BIM manager, and usually no QA/QC department — the principal reviews the set if there is time.

**Organization size most likely to benefit.** Firms of **3 to 25 people** doing project fees between roughly $5,000 and $80,000 per project, on construction values from a few hundred thousand to a few million dollars. These firms are large enough to have repeatable process pain but too small to justify a $50,000 enterprise system or a full-time compliance coordinator. Sole practitioners benefit even more per seat but pay less; firms above ~50 people begin building internal Revit/Dynamo tooling and standard spreadsheets that partly substitute for these products.

**Type of user.** Technically strong, code-literate, spreadsheet-fluent, Revit- or AutoCAD-native, deeply skeptical of software that requires modeling the building twice. Practitioners in the Eng-Tips thread on small-commercial load calculation explicitly rejected IES as "way too expensive and way too complex for my projects" and gravitated to a *free* Revit plugin (Ripple HVAC) specifically because "you don't have to model the building again." That sentence is the single best statement of this market's buying psychology: **low friction beats feature depth, and integration into what they already have beats a new environment.**

**Why the existing-building niche specifically.** Retrofit is now the majority of the work. One market analysis puts building HVAC retrofits at **$91.7 billion globally in 2024**, growing ~7.2% CAGR, and reports that retrofit projects captured **58% of HVAC services market revenue in 2024**, growing at 8.9% annually and outpacing new construction. Vendor market-research figures deserve skepticism as to precision, but the direction is corroborated by policy: California's 2025 code now requires that "end-of-life rooftop HVAC on stores, schools, and offices must be replaced with high-efficiency heat pumps above set thresholds," and the federal A2L refrigerant transition is forcing equipment turnover independent of building owner intent. The work is moving into existing buildings, and existing buildings are where the design workflow is least supported by software.

---

## 2. How the Work Is Performed

The following is the composite workflow for a mid-sized HVAC alteration — say, replacing six rooftop units and reconfiguring the ductwork for a 22,000 sq ft office tenant improvement — at a 12-person MEP firm.

### 2.1 Intake and fee proposal (0.5–3 hours)

A general contractor, architect, or building owner sends a scope description and, if the firm is lucky, a set of old drawings as scanned PDFs. The engineer estimates hours from memory. **Critically, the fee is committed before anyone knows what is actually on the roof.** Base Builders' analysis of mechanical-firm project management identifies this as a structural profitability problem: coordination, controls, and commissioning scope is "chronically underscoped," and equipment substitution reviews during construction are "almost never captured as additional services."

### 2.2 Existing-conditions field survey (4–16 hours including travel)

The engineer visits the building with a phone, a tape measure, a flashlight, and sometimes a printed floor plan. For each unit they attempt to record: manufacturer, model number, serial number, nominal tonnage, heating input, supply airflow, voltage/phase, MCA and MOCP, refrigerant type, curb dimensions and orientation, operating weight, economizer presence and condition, controls type and protocol, filter sizes, and physical condition. Nameplates are frequently faded, painted over, facing a parapet, or unreachable without a ladder. The output is **a phone camera roll and handwritten notes**, which are later transcribed by hand into Excel — often days later, when the engineer can no longer remember which photo belongs to which unit.

Ceiling access, pneumatic controls, undocumented past renovations, and missing as-builts compound this. The retrofit literature is explicit that older buildings present "obsolete control protocols, inadequate electrical capacity, and structural limitations not documented in original specifications."

### 2.3 Load calculation and system sizing (4–20 hours)

The engineer builds or updates a load model. For small commercial work the tools in real use are CHVAC, Trane TRACE 3D Plus, Carrier HAP, Revit-integrated plugins, or — very commonly — **an in-house spreadsheet**. Practitioners in the Eng-Tips thread describe HAP support as "non-existent," describe legacy tools as dated but valued for "simplicity," and describe the decisive advantage of a Revit-integrated tool as avoiding duplicate modeling.

In alteration work the load question is usually narrower than the tooling assumes: *is the existing unit still adequate for the new layout, or does it need to change size?* Answering that with a full 3D energy model is disproportionate, so engineers frequently answer it with a block-load spreadsheet and professional judgment.

### 2.4 Equipment selection (2–8 hours)

The engineer picks candidate replacement equipment from manufacturer selection software, then verifies it against a mental checklist: does it meet the code-minimum efficiency for its category and capacity; will it fit the existing curb or need an adapter; is the new operating weight within what the roof structure can take; does MCA/MOCP still fit the existing breaker and feeder; is the gas input within the existing pipe's capacity; is the refrigerant class acceptable to the owner and to the local code; will it fit through the access path. **Every one of those checks is done manually, and each is a plausible late-stage change order if it is missed.**

The A2L transition has added a live constraint: R-454B and R-32 equipment carries mildly flammable classification and, in some configurations, leak-detection and ventilation implications that did not apply to the R-410A unit being removed.

### 2.5 Energy-code compliance documentation (2–12 hours, and rising)

This is where the alteration niche diverges sharply from new construction, and where the burden is heaviest.

**In California**, alterations are governed by Title 24 Part 6 §141.0(b)2. The trigger rules are genuinely intricate:

- §141.0(b)2C governs new or replacement space-conditioning systems or components, excluding duct-only replacement.
- §141.0(b)2E governs alteration by installation or replacement of equipment "including replacement of the air handler, outdoor condensing unit of a split system air conditioner or heat pump, or cooling or heating coil."
- §141.0(b)2E1 requires that where equipment is replaced and the unit lacks demand-responsive controls, the existing thermostat be replaced with a demand-responsive one complying with §110.12.
- Duct rules bifurcate: entirely new or ≥75%-new-material duct systems require leakage testing per §120.4(g); duct *extensions* must be sealed to 15% of nominal airflow only if four criteria are all met (including serving ≤5,000 sq ft on a constant-volume system with ≥25% of duct surface area outdoors or in unconditioned space); if the criteria are not met, all accessible leaks must be sealed by visual inspection and smoke testing; and ducts exempt from leakage testing must still meet CMC §603.9.2 per §141.0(b)2Diii.
- Economizer requirements under §140.4(e) reach replacement systems below 54,000 Btu/h through Exception 4 to §141.0(b)2C.
- Table 141.0-D grants additional fan power allowances banded by airflow (≤5,000 cfm; >5,000–10,000 cfm; >10,000 cfm).

The 2025 code, effective for **every California permit submitted on or after 1 January 2026**, added mandatory ASHRAE Guideline 36 control sequences for VAV systems and economizers, new DOAS/VRF/heat-pump efficiency thresholds, and a heat-pump replacement mandate for end-of-life rooftop equipment on stores, schools, and offices above set thresholds.

Compliance is documented on registered forms. Paper and dynamic PDF forms were eliminated for the 2022 code and later; most NRCC and NRCI forms must now be completed through the Virtual Compliance Assistant. For the 2025 code there are **23 mechanical acceptance-test forms (2025-NRCA-MCH-02-A through -24-A)**, every one of which must be completed by a **Certified Acceptance Test Technician**, alongside the NRCC-MCH-E certificate of compliance and the NRCI mechanical installation certificates.

**Outside California**, the equivalent burden is COMcheck plus jurisdictional overlays. Houston's published guideline, for example, requires the mechanical compliance certificate to reference ASHRAE Standard 183 load calculations with the completed Appendix B and software summary attached, requires refrigeration equipment specifications to appear both on the drawings and as separate sheets in a designated ProjectDox subfolder, requires commissioning form CE-1190 unless exempt, and states flatly that "digital modifications to the rejected printed version are not acceptable" — a rejected report must be regenerated from inside COMcheck. Notably, that guideline applies the **same five-part submission to alterations as to new construction**, softened only by the vague note that "some alteration projects may not require submittal of all four compliance certificates depending on the exact scope of work." Deciding which ones you actually owe is left entirely to the engineer.

### 2.6 Drawing production and QA (8–40 hours)

Plans, sections, details, equipment schedules, control diagrams, sequences of operation, and code-compliance notes. The equipment schedule is the hub document: it carries the tag, capacity, airflow, external static pressure, efficiency, electrical characteristics, and physical data that the compliance report, the specification, the structural note, and the electrical panel schedule all depend on. **It is maintained by hand and it drifts.** Permit rejections commonly cite "inconsistent drawing sets — mismatched dimensions, missing schedules, or conflicting revisions across sheets."

### 2.7 Permit submission and plan-check response (2–16 hours per cycle)

Submit; wait; receive comments; respond in a comment-response matrix; resubmit. Each cycle costs calendar weeks. Mechanical/energy comments in this niche cluster on: the compliance report not matching the schedule, the wrong alteration exception cited, missing acceptance-test callouts, missing duct-sealing or economizer documentation, and load calculations not attached in the required format.

### 2.8 Construction administration (10–60 hours, largely unbudgeted)

Submittal review; substitution review; RFI response; site observation. Substitution review is the acute case — the engineer must "review the substitution, evaluate whether the replacement meets the design intent, and often redesign portions of the distribution system," and this is "almost never captured as additional services."

### 2.9 Testing, balancing, acceptance, and closeout (4–20 hours)

The TAB contractor produces a report; the engineer compares measured airflows against the design schedule terminal by terminal. Separately, in California, the ATT performs the applicable NRCA-MCH acceptance tests. The consequence of a gap here is absolute: "Enforcement agencies may not release a final certificate of occupancy unless the submitted certificate of acceptance demonstrates that the specified systems and equipment have been shown to perform in accordance with the applicable acceptance requirements."

An enforcement wrinkle worth noting for anyone building in this space: full CMATT/ATT enforcement for mechanical tests has been phased against a threshold of certified technicians statewide, and jurisdictional enforcement has historically varied — kW Engineering's guidance notes that "it is ultimately up to your local Authority Having Jurisdiction (AHJ) to ask for acceptance forms." **Any tool here must be configurable per jurisdiction rather than assuming uniform enforcement.**

### 2.10 Software actually in use

| Category | Typical tools |
|---|---|
| Drafting/modeling | AutoCAD, Revit MEP |
| Load calc / energy model | CHVAC, TRACE 3D Plus, Carrier HAP, IES VE, Revit plugins (e.g. Ripple HVAC), in-house spreadsheets |
| Energy compliance | CBECC-Com / NORESCO BEES, EnergyPro, IES Title 24 module, COMcheck, Energy Code Ace VCA |
| Equipment selection | Manufacturer selection software (Trane, Carrier, Daikin, AAON, Greenheck), AHRI Directory |
| Specs | MasterSpec / SpecLink / Word templates |
| Project delivery | Procore, Bluebeam Revu, SharePoint/Dropbox, Outlook |
| Everything else | **Excel** |

Excel is not a gap in this list. It is the operating system of the niche.

---

## 3. Most Important Problems (Ranked)

### Problem 1 — Determining which code requirements an alteration actually triggers

**Who.** The mechanical engineer of record, and secondarily the plan reviewer who must adjudicate the answer.

**When.** At the start of design, and again every time scope changes — which on retrofit work is constantly.

**Currently handled by.** Reading the code, asking a colleague, calling the AHJ, or reusing the note block from the last project of vaguely similar type.

**Why inadequate.** The trigger logic is a genuine decision tree with numeric thresholds and interacting exceptions: ≥75% new duct material versus duct extension; four simultaneous criteria including a 5,000 sq ft ceiling and a 25% outdoor-surface-area test; a 54,000 Btu/h economizer threshold reached through an exception to an exception; fan-power allowances banded at 5,000 and 10,000 cfm; thermostat replacement contingent on the absence of existing demand-response capability. Reusing last project's note block silently mis-answers all of it. The disagreement is not hypothetical — on The Building Code Forum, code officials openly split on whether replacing mechanical equipment invokes new-construction provisions at all, with one citing IMC 102.4 ("Minor additions, alterations, renovations and repairs to existing mechanical systems shall meet the provisions for new construction") and another countering that repair provisions only require not making the building "less conforming than it was before."

**Frequency.** Every alteration project. For a small firm, 20–80 times a year.

**Cost.** One missed trigger produces a plan-check correction cycle (2–6 weeks calendar), or worse, an addendum or change order in construction. A missed acceptance-test requirement discovered at final inspection blocks the certificate of occupancy outright.

**Evidence strength.** **Verified.** Requirements and thresholds are directly citable to code text; the interpretive disagreement is directly quoted from practicing code officials.

---

### Problem 2 — The equipment schedule, the compliance report, and the specification drift apart

**Who.** The engineer producing the set; the plan reviewer; the contractor buying equipment from a schedule that no longer matches the compliance report.

**When.** Every time a unit is resized, an efficiency changes, a tag is renumbered, or a manufacturer basis-of-design is swapped — which is many times per project.

**Currently handled by.** Manual re-checking, usually late and usually partial. Some firms run a Revit schedule; almost none reconcile it against the COMcheck/NRCC output field by field.

**Why inadequate.** The compliance report is generated once from a snapshot and then goes stale. Jurisdictions explicitly require the two to agree — Houston requires refrigeration equipment specs to appear both on the drawings *and* as separate submitted sheets, and requires load calculations in a mandated format attached to the COMcheck. And rejections cannot be patched: a rejected COMcheck must be regenerated inside the software rather than marked up.

**Frequency.** Every project; the drift accumulates continuously.

**Cost.** A rejection cycle is typically weeks of calendar time and 2–16 hours of engineer time, on a fee already fixed. On alteration projects with a live tenant, calendar delay is the expensive part.

**Evidence strength.** **Verified** for the requirement and the rejection mechanic; **strong inference** for the frequency of drift (the mechanism is documented; the rate is not measured).

---

### Problem 3 — Existing-conditions capture is a camera roll that becomes a hand-typed spreadsheet

**Who.** Whoever does the site visit — often the most junior person, sometimes the principal.

**When.** Once per project, occasionally twice when the first survey missed data.

**Currently handled by.** Phone photos, notebooks, and manual transcription. Purpose-built alternatives exist on the *contractor* side (field service and equipment-capture apps) and in facility-asset tooling, but they are built for service management and asset registers, not for producing a design deliverable.

**Why inadequate.** The transcription step is where errors enter and where hours vanish. Photos are unlabeled and unlinked to units. Missing data items are not discovered until the engineer is back at the desk and the ladder is 40 miles away. There is no structured capture of the specific fields a *replacement design* needs (curb dimensions and orientation, operating weight, MCA/MOCP, gas input, refrigerant, clearances), as opposed to the fields a *service call* needs.

**Frequency.** Every alteration project.

**Cost.** 2–8 hours of transcription per project plus the cost of return trips. A single missed nameplate field that forces a second site visit can cost a half day and delay the schedule a week.

**Evidence strength.** **Strong inference.** The workflow is well described in retrofit literature and in the equipment-survey tooling that exists on the contractor side; the specific time cost is estimated, not measured, and needs practitioner validation.

---

### Problem 4 — Replacement equipment feasibility is checked from memory

**Who.** The engineer selecting the replacement unit.

**When.** During equipment selection, and again when a substitution arrives in construction.

**Currently handled by.** A mental checklist, sometimes a firm-standard Word checklist.

**Why inadequate.** The checks are numerous, deterministic, and consequential: curb footprint delta, operating weight versus structural capacity, MCA/MOCP versus existing breaker and feeder, gas input versus existing pipe capacity, refrigerant class, service clearances, rigging path. Industry guidance on rooftop replacement puts "equipment configurations, electric/voltage, rigging, structural load" at the top of the list and recommends like-for-like curb matching specifically to avoid adapters — but no tool enforces the check. Everything about this problem says *deterministic rules engine*, and everything about current practice says *human memory under fee pressure*.

**Frequency.** Every unit on every replacement project.

**Cost.** A missed weight or electrical check surfaces as a change order or a field stop. Curb-adapter surprises are common enough to be a standing topic in industry guidance and, in some jurisdictions, a regulated safety issue in their own right.

**Evidence strength.** **Strong inference**, supported by industry replacement guidance; the failure *rate* is anecdotal and needs validation.

---

### Problem 5 — Acceptance-test scope is decided at design time but discovered at final inspection

**Who.** The design engineer (who specifies the tests), the contractor (who budgets and schedules them), the ATT (who performs them), and the AHJ (who withholds occupancy).

**When.** The requirement is created in design; the pain is realized at closeout.

**Currently handled by.** The Virtual Compliance Assistant "will indicate what acceptance tests are to be completed for each efficiency feature at permit application phase" — but only for what the engineer told it about, and the resulting list then lives in a PDF that nobody tracks to completion. Energy Code Ace's own guidance notes that "the technician or ATT must verify with the help of the responsible person what acceptances are to be performed and on what efficiency features" — i.e., the authoritative determination is a *conversation*, months after the design decision.

**Why inadequate.** Twenty-three distinct 2025 NRCA-MCH forms, all ATT-required, each tied to a specific efficiency feature, each mapping to specific equipment tags, with no artifact that carries the mapping from design through construction to sign-off. The consequence of a gap is binary and severe: no certificate of occupancy.

**Frequency.** Every California project with mechanical scope; analogous commissioning/functional-test gates exist elsewhere.

**Cost.** Occupancy delay. For a tenant with a lease commencement date, this is the most expensive failure mode in the entire workflow.

**Evidence strength.** **Verified** for the rules, forms, roles, and occupancy consequence. **Tentative** on how often it actually fails — no published failure-rate data was located.

---

### Problem 6 — Controls sequences are copy-pasted, and the code just raised the bar

**Who.** The design engineer; the controls contractor who has to implement whatever was written.

**When.** Construction documents phase, and again during controls submittal review.

**Currently handled by.** Copying a prior project's sequence and editing it. LBNL's `ctrl-flow` exists as a free G36 sequence generator but is self-described as **Beta**, supports only three system types (multi-zone VAV AHU, cooling-only VAV terminal, VAV terminal with reheat), outputs a single Word document, and states that its output "will require further review and editing prior to use on a project."

**Why inadequate.** California's 2025 code made Guideline 36 **mandatory** for VAV systems and economizers. Meanwhile, the DOE Commercial Energy Code Field Study found that **none of the study sites fully met energy code requirements** for HVAC and lighting controls, that VAV controls and nighttime shutdown were among the most-missed measures, and that BAS programming frequently "deviated from intended sequences after occupancy." Lost savings ran **$195 per 1,000 sq ft/year for offices and $221 for education buildings**. The copy-paste sequence is a direct contributor: the document that is supposed to define correct behavior is the least-verified deliverable in the set.

**Frequency.** Every project with a VAV system or an economizer — which after the 2025 code is most nonresidential mechanical work in California.

**Cost.** Measured in lost energy savings and in rework when the controls contractor implements a sequence that contradicts the acceptance test.

**Evidence strength.** **Verified** for the code change, the tool landscape, and the field-study findings.

---

### Problem 7 — Substitution and submittal review is unbilled, unbounded, and unstructured

**Who.** The engineer during construction administration.

**When.** Continuously through construction.

**Currently handled by.** Reading the submittal, comparing to the spec and schedule by eye, and writing a review stamp. The record "lives in BIM coordination logs, submittal registers, and email threads — not in a system that connects it to the project fee."

**Why inadequate.** The comparison is a structured, repeatable, field-by-field task being done as unstructured reading; and the effort is invisible to billing.

**Frequency.** Dozens of submittals per project.

**Cost.** Direct margin erosion. This is the single best-documented *financial* problem in the market.

**Evidence strength.** **Verified** as a described industry problem; the dollar magnitude is not published.

---

### Problem 8 — TAB report review is a manual number-by-number comparison

**Who.** The engineer at closeout.

**When.** Once per project, under schedule pressure, when everyone wants to occupy.

**Currently handled by.** Printing the TAB report and the design schedule side by side and checking deviations by hand.

**Why inadequate.** It is arithmetic against a tolerance band, performed by an expensive human at the moment of least available attention. NEBB and UFGS master specifications define the tolerance framework precisely enough to automate.

**Frequency.** Once per project, but on every terminal — often hundreds of rows.

**Cost.** 2–8 hours, plus the risk of accepting an out-of-tolerance system.

**Evidence strength.** **Strong inference.** Specifications and tolerance frameworks are verified; the review burden is inferred from the structure of the deliverable.

---

## 4. Application Opportunities

### 4.1 AlterationTrigger — HVAC alteration code-trigger and requirement determinator

**Intended user.** Mechanical engineer of record at a 3–25 person MEP firm, at the start of an alteration project.

**Problem solved.** Problem 1. Turns "which code requirements does this scope of work trigger?" from a memory-and-phone-call exercise into a deterministic, cited answer.

**Current workflow.** Read §141.0(b) or the IECC alterations chapter; guess; reuse last project's note block; discover the error at plan check.

**Proposed workflow.** Answer 10–20 structured questions about scope (replacing complete unit / coil only / condensing unit only; duct new vs. extended and what percentage; square footage served; system type; capacity; airflow; existing thermostat capability; economizer present). Receive: a requirement list with clause-level citations; the applicable exceptions and why they do or do not apply; the acceptance-test list; a drawing note block ready to paste; and a one-page plan-check narrative explaining the compliance path.

**Inputs.** Structured scope answers; jurisdiction and code-year selection.

**Outputs.** Requirement report (PDF/Markdown) with citations; drawing note block (plain text/RTF); acceptance-test matrix (CSV/Excel); plan-check narrative.

**Essential features.** Versioned rule packs as human-readable YAML, one per code and cycle (Title 24 2025, Title 24 2022 for projects permitted earlier, IECC 2021, ASHRAE 90.1-2022). Every output line carries its citation. A visible "why" trace showing which answers drove each conclusion. Jurisdictional override notes.

**Deliberately excluded from v1.** Envelope, lighting, plumbing, and process systems. Automatic form filing. Any attempt to replace the official compliance software. Multi-project management.

**AI.** **Inappropriate for the determination itself** — this is exactly the case the brief warns about, where rules and conditionals beat a model, and where a hallucinated citation is a liability event. AI is *optional* in one narrow place: drafting the prose of the plan-check narrative from the deterministic result, with the citations injected rather than generated.

**Why not a spreadsheet.** The logic is a nested decision tree with interacting exceptions and a citation trail. A spreadsheet can encode it once, but it cannot be versioned per code cycle, cannot show a why-trace, and cannot be safely maintained by the one person who understands it. This is the classic case where the spreadsheet exists, is 400 rows, and nobody trusts it.

**Complexity.** Medium. The engine is small; the rule authoring is the real work.

**Learning difficulty.** Very low — it is a questionnaire.

**Value.** Avoiding one plan-check correction cycle per year pays for it. Realistically it saves 2–6 hours of code research per project and materially reduces rejection risk.

**Risks and constraints.** **Professional liability is the dominant risk.** The tool must present itself as a research aid producing citations for the engineer to verify, never as a compliance determination. Rule packs must be dated and version-pinned so a project permitted under a prior code is evaluated under that code. Code text is copyrighted — the tool must cite and paraphrase, not reproduce.

**Existing products and substitutes.** Energy Code Ace's reference materials and Virtual Compliance Assistant (excellent, official, but organized as reference text and forms — you must already know what to look up); UpCodes (searchable code text, no scope-driven determination); the AHJ phone call. **None of them answer "given this scope, what do I owe?"**

**Why still attractive.** It sits precisely in the gap between "here is the code" and "here is your filled-out form." The determination step in the middle is currently unassisted and is where the errors originate.

**Customization potential.** High. Firm-specific note-block language, jurisdiction-specific overlays, and client-standard compliance paths are all natural paid customizations. A firm doing repeat work for one retailer across 40 jurisdictions would pay well for a jurisdiction-overlay pack.

---

### 4.2 SpecMatch — equipment schedule ↔ compliance report ↔ specification cross-checker

**Intended user.** The engineer or a QA reviewer, immediately before every submission.

**Problem solved.** Problem 2.

**Current workflow.** Eyeball the schedule against the compliance report; miss things; get rejected.

**Proposed workflow.** Drop in the equipment schedule (Excel export, Revit schedule export, or CSV), the compliance report (COMcheck `.cck` project file or PDF; NRCC PDF), and optionally the spec section. Get back a reconciliation table: every tag present in one source and missing in another, and every field mismatch (capacity, airflow, ESP, efficiency, electrical) with the two values shown side by side and a severity flag for anything that is a code-minimum violation rather than a mere inconsistency.

**Inputs.** Schedule file; compliance report file; optional spec.

**Outputs.** Reconciliation report (HTML/Excel) with a clean/dirty verdict; a punch list ordered by severity.

**Essential features.** Configurable field-mapping profiles per firm (because everyone's schedule columns are named differently). Tolerance settings (a 0.1% capacity difference is rounding, not an error). Code-minimum efficiency tables per equipment category and capacity band so the tool can flag a *substantive* failure, not just a mismatch.

**Deliberately excluded.** Editing either source. Generating the compliance report. Revit live-link (v1 reads exports).

**AI.** **Optional and confined to extraction.** Reading a table out of a PDF compliance report is a legitimate AI use where a rules-based parser is brittle. The comparison itself must be deterministic. Extracted values should be shown to the user with the source page for confirmation.

**Why not a spreadsheet.** A VLOOKUP does the tag matching; it does not parse a PDF, hold code-minimum tables, or produce a reviewable audit artifact. Firms that have built this in Excel maintain it badly.

**Complexity.** Medium — driven by parser variety and the efficiency-table data.

**Learning difficulty.** Low: three file pickers and a report.

**Value.** Avoids the most common mechanical rejection category. Saves 1–3 hours of manual checking per submission, and 2–6 weeks of calendar time when it prevents a rejection.

**Risks.** Efficiency tables must be maintained per code cycle and cited. Parsing failures must fail loudly rather than silently reporting "no mismatches." Note the AHRI licensing constraint below.

**Existing products.** Generic AI submittal-review products (BuildSync, Pelles.ai and similar) target the *contractor's* submittal register, not the designer's pre-submission self-check, and are subscription platforms. Revit schedules enforce internal consistency within the model but know nothing about the compliance report.

**Why still attractive.** The specific reconciliation that gets projects rejected — drawings versus energy compliance report — is not the reconciliation any existing product performs.

**Customization potential.** High: per-firm schedule profiles and per-jurisdiction required-field sets are natural billable configuration.

---

### 4.3 SwapCheck — replacement equipment fit and feasibility checker

**Intended user.** The engineer selecting a replacement unit; also useful to the contractor's project manager.

**Problem solved.** Problem 4.

**Current workflow.** Mental checklist under fee pressure.

**Proposed workflow.** Enter existing unit data (or import it from the survey tool in 4.4) and candidate replacement data. The tool computes and flags: curb footprint delta and whether an adapter is implied; operating weight delta against a user-entered allowable structural capacity; MCA/MOCP against the existing breaker and feeder ampacity; gas input against existing pipe capacity at the stated length and pressure; refrigerant class change and its implications; service clearance conflicts; and a rigging/access note. Output is a one-page feasibility memo listing green checks, flags, and the specific questions that must be answered by others (structural engineer, electrical engineer).

**Inputs.** Existing and proposed unit data; existing electrical and gas service parameters; structural allowable (user-supplied).

**Outputs.** One-page feasibility memo (PDF); a coordination-request list addressed to the structural and electrical disciplines.

**Essential features.** Deterministic checks with the arithmetic shown. Explicit "unknown — must verify" states rather than silent assumptions. A concise defensible memo suitable for the project record.

**Deliberately excluded.** Structural analysis (it reports a delta against a user-supplied allowable; it does not analyze the roof). Load calculations. Equipment selection or pricing. Manufacturer catalogs.

**AI.** **Inappropriate.** Every check is arithmetic and table lookup. Adding a model here would add risk and remove auditability. *Possible* narrow exception: extracting specs from a manufacturer submittal PDF as an input convenience — which is really feature 4.4's job.

**Why not a spreadsheet.** Honestly, a very good spreadsheet would get most of the way. The advantages of an app are the enforced "unknown" states, the memo output that becomes a project record, and shareability with a contractor who does not have your spreadsheet. This is a case where the *deliverable*, not the calculation, justifies the software.

**Complexity.** Small.

**Learning difficulty.** Very low.

**Value.** Prevents change orders. One avoided curb-adapter or electrical-upgrade surprise on one project exceeds any plausible cost.

**Risks.** Must not read as engineering certification of structural adequacy. Refrigerant-safety logic (A2L) must be conservative and jurisdiction-aware, and should point to the governing standard rather than asserting compliance.

**Existing products.** Manufacturer selection software checks the manufacturer's own constraints, not the building's. Nothing found performs the cross-discipline existing-building fit check.

**Customization potential.** Moderate — firm checklists, client equipment standards, and portfolio-owner constraints.

---

### 4.4 NameplateCapture — existing-conditions equipment survey to schedule generator

**Intended user.** Whoever performs the field survey.

**Problem solved.** Problem 3.

**Current workflow.** Photos plus notes plus later hand transcription.

**Proposed workflow.** A browser-based, **offline-capable** form (roofs have poor signal) driven by a field template that lists exactly the data a replacement design needs. Photograph the nameplate; the tool extracts manufacturer, model, serial, capacity, voltage/phase, MCA/MOCP, refrigerant, and weight into editable fields; the surveyor confirms or corrects. Dimensional and condition fields are entered directly. Photos bind automatically to the unit record. The tool refuses to mark a unit complete while a required field is blank, so gaps are caught *on site*. Output: an equipment inventory workbook, a photo log indexed by tag, and a draft existing-equipment schedule in the firm's column format.

**Inputs.** Nameplate photos; typed field data; a firm-configurable field template.

**Outputs.** Excel inventory; indexed PDF photo log; CAD/Revit-ready schedule CSV; per-unit data sheet feeding SwapCheck.

**Essential features.** Offline-first with sync. Required-field enforcement. Photo-to-unit binding. Firm-configurable templates. Round-trip export.

**Deliberately excluded.** Asset management, maintenance history, work orders, QR-code tagging, multi-year condition tracking — all of which turn this into a CMMS and violate the narrow-scope rule.

**AI.** **Optional but genuinely valuable.** Nameplate OCR and field extraction is a task conventional software does poorly (weathered plates, inconsistent layouts, varied terminology) and a vision model does well. The design must keep AI in an assist role: every extracted value is presented for human confirmation, and the tool works fully without it.

**Why not a spreadsheet.** A spreadsheet cannot enforce completeness before you leave the roof, cannot bind photos to records, and cannot be filled in one-handed on a ladder.

**Complexity.** Medium.

**Learning difficulty.** Low.

**Value.** 2–8 hours of transcription per project, plus avoided return trips.

**Risks.** Photos of a client's building may be sensitive, especially for secure facilities — local-first storage should be the default with cloud sync opt-in. OCR errors must be visibly flagged, never silently accepted.

**Existing products.** Contractor-side field capture apps and generic mobile form builders exist. They are built to feed service management and asset registers; none output a *design deliverable* (an equipment schedule in the engineer's format) and none enforce the replacement-design field set.

**Customization potential.** High — firm templates, client asset-tagging conventions, portfolio survey standards.

---

### 4.5 ATClose — acceptance-test scope carrier and closeout package assembler

**Intended user.** The design engineer at CD phase; the contractor's PM and the ATT during construction; the AHJ at final.

**Problem solved.** Problem 5.

**Current workflow.** A test list in a PDF at permit time, then a conversation months later, then a scramble at final inspection.

**Proposed workflow.** At design, the tool takes the AlterationTrigger output (or a manual selection) and produces the acceptance-test matrix mapped to equipment tags, with a responsible-party column, formatted for a drawing sheet. At closeout, it accepts the completed forms and verifies the package: is a form present for every required test on every tagged unit; is it the correct 2025-NRCA-MCH number for that feature; are the equipment tags on the form consistent with the schedule; is the technician's certification recorded. Output is a bound, indexed submission PDF plus a deficiency list naming exactly which unit is missing which form.

**Inputs.** Test matrix (from 4.1 or manual); completed form PDFs; equipment schedule.

**Outputs.** Drawing-ready test matrix; bound closeout PDF with index; deficiency list.

**Essential features.** Per-tag, per-test completeness checking. Jurisdiction profile controlling which tests that AHJ actually enforces. Explicit tracking of the design → construction → sign-off handoff.

**Deliberately excluded.** Performing or scoring the tests. Scheduling technicians. Serving as a commissioning platform or an issue-tracking system. Any live integration with a certification registry (verify manually; registries change).

**AI.** **Inappropriate for the logic; optional for reading form PDFs** to pull tag and test numbers. The completeness rule is a set difference.

**Why not a spreadsheet.** The spreadsheet handles the matrix fine and is what firms use today. It does not assemble and verify the package, and it does not survive the handoff between three organizations. This concept's value is concentrated in the closeout assembly half.

**Complexity.** Medium.

**Learning difficulty.** Low to moderate.

**Value.** The failure it prevents — occupancy delay — is the most expensive in the workflow.

**Risks.** Enforcement genuinely varies by AHJ; the tool must be configurable and must not assert that a package *will* be accepted. Certification-status checking must remain a prompt to verify, not an authoritative claim.

**Existing products.** Commissioning platforms (large, expensive, aimed at Cx providers) and the official form tools (which generate forms but do not verify a package). Nothing small sits in the middle.

**Customization potential.** High — per-jurisdiction profiles are the obvious paid product.

**Caution.** This concept has the highest overlap with the fire-protection cycle's `SubmittalBinder` and with the general "required-artifact completeness gate" pattern. That is a signal about pattern reusability (section 7), but it means the *incremental* catalog value is lower than the raw problem severity suggests.

---

### 4.6 SeqForge — retrofit sequence-of-operation and points-list generator

**Intended user.** The engineer writing controls documentation for a retrofit.

**Problem solved.** Problem 6.

**Current workflow.** Copy the last project's sequence; edit; hope the controls contractor reads it.

**Proposed workflow.** Select the system archetype from a retrofit-focused set (single-zone packaged RTU with economizer and DCV; packaged VAV with reheat; split system with DOAS; heat-pump replacement retaining existing distribution), answer configuration questions, and receive a Guideline-36-derived sequence in Word with live numbering, a matching BACnet points list in Excel, and a cross-reference showing which acceptance test verifies which paragraph.

**Inputs.** System archetype and configuration answers.

**Outputs.** Word sequence; Excel points list; sequence-to-acceptance-test cross-reference.

**Essential features.** Retrofit archetypes, not just new-construction ones. The points list — currently the most tedious deliverable. The acceptance-test cross-reference, which is the differentiator and directly addresses the field-study finding that BAS programming drifts from intent.

**Deliberately excluded.** Simulation. Controller programming or code generation. Graphics. Anything resembling a BAS.

**AI.** **Optional and secondary.** Template assembly is deterministic. AI could help tailor prose to a firm's house style — a convenience, not the value.

**Why not a spreadsheet.** The deliverable is a numbered narrative document with cross-references; that is Word's job, not Excel's, and generating it consistently is a program's job.

**Complexity.** Medium, trending toward the upper end. Guideline 36 is long, and getting sequences wrong is worse than not offering them.

**Learning difficulty.** Moderate.

**Value.** Real but harder to price. Saves 4–12 hours per project and improves a deliverable that is measurably deficient industry-wide.

**Risks.** Highest liability exposure of any concept here — a wrong sequence causes real operational failures. Guideline 36 is copyrighted, which constrains how much text can be reproduced. Output must be positioned as a starting draft requiring engineering review, exactly as LBNL positions `ctrl-flow`.

**Existing products.** LBNL `ctrl-flow` — free, Beta, three system types, Word output only, no points list, no acceptance-test cross-reference, no retrofit archetypes. It is the closest thing to a competitor and it is also a partial validation that the need is real.

**Why still attractive despite ctrl-flow.** The retrofit archetypes and the points list are the two things a small firm needs most, and neither is offered. A points list alone might be the better first build.

**Customization potential.** Very high — firm-standard sequence libraries are a natural paid engagement, and arguably the strongest consulting hook in this entire report.

---

### 4.7 SubSwap — equipment substitution comparison and additional-services log

**Intended user.** The engineer during construction administration; the principal reviewing project profitability.

**Problem solved.** Problem 7.

**Current workflow.** Read the submittal; compare by eye; stamp; absorb the cost.

**Proposed workflow.** Log the substitution request against the specified basis-of-design unit. The tool produces a side-by-side comparison on the parameters that matter (capacity, efficiency versus code minimum, airflow and ESP, electrical, physical dimensions and weight, sound, refrigerant, warranty), flags every deviation, and drafts a review response. Separately and simultaneously, it logs the review time against the project as a candidate additional service, producing a monthly summary the principal can actually invoice from.

**Inputs.** Specified unit data; proposed substitution data (manual or extracted from the submittal PDF); review time.

**Outputs.** Comparison sheet (PDF); draft response letter; additional-services log (Excel).

**Essential features.** The comparison sheet. The code-minimum efficiency check. The billing log — which is what converts a QA tool into a revenue tool, and is the reason a principal buys it.

**Deliberately excluded.** Submittal workflow management, routing, approvals, or a document repository. Procore integration. This is a *review aid plus a log*, not a submittal system.

**AI.** **Optional, confined to extraction** from the submittal PDF. Comparison and flagging are deterministic.

**Why not a spreadsheet.** The comparison could be. The linkage between technical review and the fee record is the part firms have not built, and it is the part with documented financial pain behind it.

**Complexity.** Medium.

**Learning difficulty.** Low.

**Value.** Directly recoverable revenue. This is the only concept in the report with a *revenue* case rather than a cost-avoidance case, which makes it unusually easy to sell to a principal.

**Risks.** Extraction errors on submittal PDFs. The response letter must remain engineer-authored in substance.

**Existing products.** AI submittal-review platforms exist for contractors and larger firms; they are subscription platforms aimed at volume review, and none connect review effort to the engineering fee.

**Customization potential.** Moderate to high — firm response templates, client equipment standards, integration with the firm's time system.

---

### 4.8 TABCheck — test-and-balance report deviation checker

**Intended user.** The engineer at closeout.

**Problem solved.** Problem 8.

**Current workflow.** Manual row-by-row comparison of the TAB report against the design schedule.

**Proposed workflow.** Load the TAB report (Excel or PDF) and the design schedule. The tool matches terminals by tag, computes percentage deviation per terminal and per system, applies the tolerance band from the specification, and produces a punch list of out-of-tolerance items sorted by severity, plus system-level totals showing whether supply, return, and outside air actually balance.

**Inputs.** TAB report; design schedule; tolerance settings.

**Outputs.** Deviation report with pass/fail per terminal; punch list; system-level summary; draft acceptance or rejection letter.

**Essential features.** Tag matching with fuzzy handling of the inevitable naming inconsistencies. Configurable tolerance bands matching NEBB/AABC/UFGS-style specifications. System-level airflow reconciliation, which catches problems terminal-level review misses.

**Deliberately excluded.** Performing balancing. Interpreting *why* a terminal is off. Generating TAB reports.

**AI.** **Optional, extraction only.** TAB reports arrive as PDFs with inconsistent table layouts — a legitimate extraction case. The arithmetic is arithmetic.

**Why not a spreadsheet.** If the TAB report arrives as Excel with matching tags, a spreadsheet is genuinely adequate and should be said so honestly. The app earns its place when the report is a PDF, when tags do not match, and when a defensible reviewed artifact is wanted for the record.

**Complexity.** Small to medium.

**Learning difficulty.** Very low.

**Value.** 2–8 hours per project plus reduced risk of accepting a non-compliant system.

**Risks.** Extraction reliability. Must not be positioned as replacing the engineer's judgment about *why* a reading is off.

**Existing products.** TAB firms have their own reporting software; the *reviewer's* side is unserved.

**Customization potential.** Moderate — per-firm tolerance standards and letter templates.

---

## 5. Opportunity Ranking

Scored 1–5 on each dimension; maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of implementation | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **AlterationTrigger** | 5 | 5 | 4 | 5 | 3 | 4 | 5 | 5 | 4 | 5 | **45** |
| 2 | **SpecMatch** | 5 | 4 | 5 | 4 | 3 | 4 | 4 | 4 | 4 | 4 | **41** |
| 3 | **SwapCheck** | 4 | 4 | 4 | 5 | 4 | 5 | 4 | 4 | 3 | 3 | **40** |
| 4 | **NameplateCapture** | 4 | 5 | 4 | 5 | 3 | 4 | 3 | 4 | 4 | 4 | **40** |
| 5 | **TABCheck** | 3 | 3 | 4 | 5 | 4 | 5 | 4 | 4 | 3 | 3 | **38** |
| 6 | **ATClose** | 5 | 4 | 4 | 4 | 3 | 3 | 3 | 5 | 3 | 4 | **38** |
| 7 | **SubSwap** | 4 | 4 | 4 | 4 | 3 | 4 | 3 | 4 | 3 | 4 | **37** |
| 8 | **SeqForge** | 4 | 3 | 4 | 3 | 2 | 3 | 4 | 5 | 3 | 4 | **35** |

*Rows are ordered by total: AlterationTrigger 45, SpecMatch 41, SwapCheck 40, NameplateCapture 40, TABCheck 38, ATClose 38, SubSwap 37, SeqForge 35. Where totals tie, the tiebreak favors ease of implementation and scope discipline.*

### Top three explained

**1. AlterationTrigger (45).** It scores highest because it is upstream of everything else. The determination it makes drives the compliance forms, the acceptance tests, the drawing notes, and the plan-check narrative — so its output is an input to concepts 2 and 5. It is also the concept with the strongest verified evidence: the thresholds, exceptions, and interpretive disagreement are all directly citable. It scores 3 rather than 5 on implementation because the rule authoring is careful, unglamorous work that must be redone each code cycle — which is simultaneously its moat. Its liability exposure is real but manageable by positioning it as a cited research aid.

**2. SpecMatch (41).** Highest ROI clarity in the set, because the failure it prevents has a named, published mechanism: jurisdictions require the compliance report and the drawings to agree, and a rejected report cannot be patched. It requires no behavior change — the engineer already has all three files — and the before/after demo is immediate and visceral. Its ceiling is set by parser reliability and by the maintenance burden of code-minimum efficiency tables.

**3. SwapCheck (40, chosen over NameplateCapture on tiebreak).** Both scored 40. SwapCheck wins the tiebreak on implementation ease and scope discipline: it is the smallest buildable thing in the report, has no mobile/offline requirement, needs no AI, and its logic is pure arithmetic. It is the best candidate for a first shipped artifact — a weekend-to-fortnight build that produces a real deliverable. Its weakness is evidence: the failure rate is anecdotal and needs practitioner validation before investing further.

**NameplateCapture** is noted as the strongest *complement*: it and SwapCheck form a natural pair (survey feeds feasibility check), and together they cover the front half of the retrofit workflow.

### What should be investigated next

**Build SwapCheck first as a validation vehicle, and research AlterationTrigger in parallel.** SwapCheck is small enough to ship quickly and concrete enough that showing it to five practitioners produces real feedback on the underlying assumption (that these checks are actually missed). AlterationTrigger is the more valuable product but needs a rule-authoring investment that should not be made before someone confirms the determination problem is felt as acutely as the code text suggests.

**Do not start with SeqForge**, despite its high customization potential — it has the highest liability exposure, the largest content burden, and an existing free federal tool in the space.

---

## 6. Validation Plan

### Questions to ask practitioners

On alteration triggers: *Walk me through the last equipment-replacement project — how did you decide which code requirements applied? Have you ever gotten a plan-check comment saying you cited the wrong exception? Do you reuse a note block from a prior project, and how do you know it is still right for this code cycle?*

On schedule/compliance drift: *When you resize a unit late in CD, what makes you re-run the compliance report? Has a permit ever been rejected for a mismatch between the schedule and the energy report? How long did that cost you?*

On field survey: *How do you record nameplate data? How many hours does transcription take? When did you last have to go back for data you missed?*

On replacement feasibility: *Have you ever had a curb, weight, electrical, or gas surprise in construction? What did it cost? Do you have a written checklist, and does anyone actually use it?*

On acceptance testing: *Who tracks which NRCA forms are owed? Have you ever had occupancy held up over a missing acceptance form?*

On substitutions: *How many substitution requests per project? How long does each review take? Do you bill for it?*

### Who to interview

- Principals and lead mechanical engineers at 5–20 person MEP firms, ideally 6–10 of them, split between California (maximum regulatory intensity) and non-California IECC/90.1 jurisdictions (to test generality).
- Two or three mechanical plan reviewers or building officials — they see the aggregate failure pattern that individual engineers only see once each. Backlog item 125 (public-sector plan-check offices) is the systematic version of this.
- One or two Certified Acceptance Test Technicians and one commissioning provider, for the closeout half.
- One TAB contractor, to learn what report formats actually circulate.
- One controls contractor, on how sequences arrive and what is wrong with them.

### Search terms for further research

`Title 24 141.0(b)2 alteration mechanical plan check comment`; `NRCA-MCH acceptance test missed certificate of occupancy`; `COMcheck mechanical rejected schedule mismatch`; `rooftop unit replacement curb adapter change order`; `existing conditions survey MEP checklist template`; `Guideline 36 sequence retrofit single zone`; `TAB report review tolerance percent design airflow`; `MEP substitution review additional services billing`. Reddit (`r/MEPEngineering`, `r/HVAC`, `r/BuildingCodes`) should be re-attempted from an environment that can reach it — it was blocked this cycle and is likely the highest-yield remaining source.

### Sample files and data needed

Three to five complete alteration project sets, each containing: existing-conditions survey notes; the equipment schedule (Excel and PDF); a COMcheck `.cck` or NRCC PDF; the plan-check comment letter and response; two or three equipment submittals including one substitution; a TAB report; and the acceptance-test forms. **The plan-check comment letters are the single most valuable artifact** — they are the ground truth on what actually fails, and they would let AlterationTrigger and SpecMatch be validated against real rejections rather than against theory.

### Simplest validating prototype

For AlterationTrigger: a single-page HTML questionnaire hard-coded to Title 24 2025 §141.0(b)2 mechanical triggers only, with citations, and no persistence. If ten engineers use it and two say "that is not what I would have concluded," the concept is validated *and* the disagreement is the most valuable finding.

For SwapCheck: a one-page form with eight inputs and a printable memo. Buildable in a day.

For SpecMatch: a script that takes two CSVs and prints mismatches — deliberately skipping PDF parsing — to test whether the *comparison* is valued before investing in extraction.

### Assumptions most likely to make these fail

1. **That engineers will trust a tool's code determination enough to act on it.** They may treat any output as needing full independent verification, which erases the time saving and leaves only the citation convenience. This is the single most dangerous assumption in the report.
2. **That the schedule/compliance mismatch is actually common.** The mechanism is documented; the rate is not. If firms already catch it reliably, SpecMatch's value collapses.
3. **That files are extractable.** If compliance reports and TAB reports arrive as scanned images or in wildly inconsistent formats, extraction cost swamps the benefit.
4. **That free open-source distribution reaches this audience.** Small MEP firms discover tools through colleagues, ASHRAE chapters, and manufacturer reps — not GitHub. Distribution may be a harder problem than construction.
5. **That per-code-cycle rule maintenance is sustainable.** California revises Title 24 every three years; the 2025 code took effect 1 January 2026 and the next cycle is already in motion. A rule-based product that falls a cycle behind is worse than useless.
6. **That liability concerns do not block adoption outright.** Some principals will refuse to let staff use any tool that appears to make code determinations, regardless of disclaimers.

---

## 7. Cross-Industry Patterns

**Pattern A — Scope-of-work → applicable-requirement determinator with citation trail.** A questionnaire about what is being changed, evaluated against versioned rule packs, producing a cited requirement list and a paste-ready note block. Transfers to: **Building permit expediting and code consulting firms** (backlog 110) where it is arguably the entire business; **Structural engineering firms, 5–30 staff** (7–10) for IEBC alteration-level determination; **Small architectural studios** (15–18) for accessibility-upgrade and path-of-travel triggers; **Electrical or plumbing trade subcontractor field operations** (23–26); **Fire alarm system design and programming subcontractors** (107).

**Pattern B — Cross-document field reconciliation before a regulatory gate.** Two or three documents that must agree, reconciled field by field with severity ranking. Transfers to: **Construction submittal, RFI, and closeout coordination** (27–30); **Supplier quality engineering at OEMs and primes** (157–160); **Contract manufacturers serving FDA-regulated medical devices** (145–148) for DHR-versus-DMR reconciliation; **Certificate-of-insurance compliance from the holder side** (113) — and it is the same shape as the completed insurance cycle's `ContractCheck`, which strengthens the pattern.

**Pattern C — Structured field capture with completeness enforcement, producing a design deliverable rather than an asset register.** The distinguishing move is that the output is the professional's own deliverable format, and the tool refuses to let you leave the site with a gap. Transfers to: **Fire protection inspection, testing and maintenance (ITM) contractors under NFPA 25** (109); **Geotechnical and environmental consulting / materials testing labs** (34–37); **Calibration and metrology service providers** (153–156); **Commercial property management** (68–71) for condition assessment; **UAS / drone mapping and reality-capture providers** (129–132) for GCP and flight-log capture.

**Pattern D — Required-artifact completeness gate before an irreversible sign-off.** Given a determined requirement set, verify that every required artifact exists, is the correct version, references the correct item, and is signed by a qualified party; output a bound package plus a deficiency list. Already observed in the fire-protection cycle (`SubmittalBinder`) and now again here (`ATClose`), which makes it the most-confirmed pattern in the catalog. Transfers to: **Flood zone / FEMA elevation certificate and LOMA-LOMR consulting** (117–120); **County surveyor and municipal plan-check offices** (125–128, the receiving side); **Small defense suppliers navigating CMMC Level 2** (149–152); **Title, escrow, and real estate closing** (49–52); **Nonprofit grant management and compliance** (99–102).

**Pattern E — Measured-versus-specified deviation report with configurable tolerance bands.** Import measured results, match to specified values by identifier, compute deviation against a tolerance, output a ranked punch list and a system-level reconciliation. Transfers to: **Machine shop / job shop** inspection reporting (88–90, market already touched from another angle); **Calibration and metrology providers** (153–156); **Geotechnical and materials testing labs** (34–37); **Independent property and casualty claims adjusting** (64–67) for estimate-versus-actual reconciliation.

**Pattern F — Technical-review effort logged as a billable additional service.** Attach a lightweight effort log to a review task so unbilled professional work becomes visible and invoiceable. This is a *business-model* pattern rather than a technical one and it is unusually portable: it applies anywhere professionals perform reviews outside a fixed scope. Transfers to: **Small-firm litigation support and paralegal work** (38–41); **Independent insurance agencies** (61–63); **Marketing and creative agency account and production management** (95–98); **Bookkeeping and outsourced accounting firms** (53–56).

---

## 8. Sources and Confidence

### Verified findings (directly supported by primary or authoritative sources)

| Finding | Source |
|---|---|
| Title 24 §141.0(b)2 alteration triggers, duct thresholds (≥75% new material; 15% sealing with four criteria; 5,000 sq ft and 25% surface-area tests), 54,000 Btu/h economizer exception, Table 141.0-D fan-power bands, demand-responsive thermostat replacement | [Energy Code Ace — Section 141.0](https://energycodeace.com/content/section-1410-additions-alterations-and-repairs-to-existin); [2025 California Energy Code, ICC](https://codes.iccsafe.org/content/CAEC2025P2/subchapter-1-all-occupancies-general-provisions) |
| 2025 California Energy Code effective 1 January 2026; Guideline 36 mandatory for VAV and economizers; new DOAS/VRF/heat-pump thresholds; end-of-life rooftop replacement mandate for stores, schools, offices | [2025 Title 24 Energy Code Changes](https://title24calcs.com/californias-2025-title-24-energy-code-whats-changed/) |
| 23 mechanical acceptance-test forms (2025-NRCA-MCH-02-A … -24-A), all requiring a Certified Acceptance Test Technician; NRCC-MCH-E; paper and dynamic PDF forms discontinued | [Energy Code Ace — 2025 Nonresidential Forms](https://energycodeace.com/NonresidentialForms/2025); [2022 forms](https://energycodeace.com/NonresidentialForms/2022) |
| Certificate of occupancy may not be released without compliant certificates of acceptance; VCA indicates required tests at permit application; ATT/responsible-person coordination is a conversation | [Energy Code Ace — Acceptance Test Requirements](https://energycodeace.com/content/14-acceptance-test-requirements); [CALBO / PIER acceptance testing infographic](https://www.calbo.org/sites/main/files/file-attachments/pier_t24_infographic.pdf) |
| AHJ enforcement of acceptance forms varies; CMATT enforcement gated on a certified-technician threshold | [kW Engineering — When is T24 Mechanical Acceptance Testing Required](https://kw-engineering.com/title-24-t24-mechanical-acceptance-testing-required-occupancy-permit/) |
| COMcheck submittal requirements: ASHRAE 183 load calcs with Appendix B attached; equipment specs on drawings and as separate sheets; commissioning form CE-1190; rejected reports must be regenerated, not edited; alterations receive the same five-part submission | [City of Houston COMcheck Guideline](https://www.houstonpermittingcenter.org/media/6166/download) |
| No study site fully met HVAC and lighting controls code requirements; VAV controls, nighttime shutdown, BAS programming drift and commissioning were the leading deficiencies; lost savings $195/1,000 sq ft/yr office, $221 education, $72 multifamily | [IMT — Takeaways from DOE's Commercial Energy Code Field Study](https://imt.org/news/making-sense-of-lost-savings-takeaways-from-the-does-commercial-energy-code-field-study/); [DOE Commercial Energy Code Field Study](https://www.energycodes.gov/commercial-energy-code-field-study) |
| LBNL `ctrl-flow` is Beta, supports three system types, outputs a Word sequence only, requires further review before project use, free | [lbl-srg/ctrl-flow](https://github.com/lbl-srg/ctrl-flow) |
| Code officials disagree on whether mechanical equipment replacement invokes new-construction provisions (IMC 102.4 versus repair provisions) | [The Building Code Forum — Replacing Mechanical Equipment](https://www.thebuildingcodeforum.com/forum/threads/replacing-mechanical-equipt.23507/) |
| Practitioner tool preferences: IES "way too expensive and way too complex"; HAP support "non-existent"; decisive advantage of not re-modeling the building | [Eng-Tips — HVAC Load calculation for small commercial projects](https://www.eng-tips.com/threads/hvac-load-calculation-for-small-commercial-projects-usa.515978/) |
| Equipment substitution reviews "almost never captured as additional services"; controls and commissioning "chronically underscoped"; coordination records live in email and logs, disconnected from the fee | [Base Builders — Project Management for Mechanical Engineers](https://www.basebuilders.com/articles/project-management-for-mechanical-engineers) |
| AHRI certified-directory data is licensable under a paid subscription agreement; scraping the public directory is prohibited; third-party certificate generation is not permitted | [AHRI — License Directory Data](https://www.ahrinet.org/certification/license-ahri-directory-data) |
| Rooftop replacement requires assessing "equipment configurations, electric/voltage, rigging, structural load"; like-for-like curb matching avoids adapters | [Enervise — 9 Tips for Replacing Commercial Rooftop Units](https://www.enervise.com/expert-tips/9-tips-for-replacing-commercial-rooftop-units/) |
| Permit rejection causes include "inconsistent drawing sets — mismatched dimensions, missing schedules, or conflicting revisions across sheets" | [CADTRI — Why Building Permits Get Rejected](https://www.cadtri.com/blog/why-building-permits-get-rejected-and-how-to-pass-plan-check-the-first-time) |
| TAB tolerance frameworks are specified in master specifications | [NEBB TAB specification](https://www.nebb.org/wp-content/uploads/2022/04/230593-Testing_-Adjusting_-Balancing-for-HVAC-DWP-edits-2020-04-16_approved.pdf); [UFGS 23 05 93](https://www.wbdg.org/FFC/DOD/UFGS/UFGS%2023%2005%2093.pdf) |
| NAICS 541330 employment ≈ 964,620 (BLS, May 2018 basis) | [BLS OES NAICS 541330](https://www.bls.gov/oes/2023/may/naics5_541330.htm); [NAICS 541330 description](https://www.naics.com/what-is-naics-541330-full-description-and-statistics/) |

### Strong inferences (mechanism documented, magnitude estimated)

- **Retrofit now exceeds new construction in HVAC services revenue.** The 58%-of-revenue and $91.7B figures come from a trade-press summary of vendor market research and should be treated as directional, not precise. The direction is independently corroborated by the 2025 code's equipment-replacement mandate and by the A2L transition forcing turnover. Source: [World Construction Today — The Growing Shift Toward HVAC Retrofits](https://www.worldconstructiontoday.com/industries/the-growing-shift-toward-hvac-retrofits-in-modern-construction/).
- **Retrofit-specific technical constraints** — compact mechanical rooms, low ceilings, limited duct pathways, 1970s–80s pneumatic controls lacking communication capability, inadequate electrical capacity, and "structural limitations not documented in original specifications" — same source; consistent with practitioner experience but not independently measured.
- **A2L refrigerant transition is materially affecting equipment replacement decisions in 2025–2026.** Well documented as an industry transition; its specific effect on *design* workflow at small firms is inferred. Sources: [Johnson Controls — Navigating the Refrigerant Transition](https://www.johnsoncontrols.com/navigating-the-refrigerant-transition); [XOi — A2L Refrigerant Transition 2026](https://xoi.io/article/a2l-refrigerant-transition-2026/).
- **Excel is the de facto integration layer** for these firms. Consistent with every practitioner source encountered; not separately measured.
- **Small-firm dominance of the mechanical consulting market.** Directionally supported by ACEC's SBA size-standard commentary and general industry structure; a precise firm-size distribution for the mechanical/MEP subset was not located. Source: [ACEC comments on SBA size standards](https://mo.acec.org/default/assets/File/ACEC%20Comments%20on%20SBA%20Size%20Standards%20(FINAL).pdf).
- **Contractor-side field-capture apps do not produce design deliverables.** Inferred from product positioning; not confirmed by hands-on evaluation. Source: [BuildOps — HVAC field capture tools](https://buildops.com/resources/hvac-field-capture-tools/); [Layer — Equipment Inventory Surveys](https://layer.team/blog/an-introduction-to-equipment-inventory-surveys).

### Tentative hypotheses requiring practitioner validation

- **All time estimates in section 2 and all "hours saved" figures in section 4 are estimates**, constructed from workflow structure rather than measured. They must be treated as hypotheses until practitioners confirm them.
- **The frequency of schedule-versus-compliance-report drift is unmeasured.** The requirement and the rejection mechanic are verified; the rate is not. This is the load-bearing assumption under SpecMatch.
- **The frequency of curb, weight, electrical, and gas surprises in replacement projects is anecdotal.** This is the load-bearing assumption under SwapCheck.
- **No published data was found on acceptance-test-related occupancy delays.** The consequence is verified as a rule; its realized frequency is unknown.
- **Willingness to trust and act on a tool's code determination is unknown**, and is the assumption most likely to invalidate the top-ranked concept.
- **Distribution to small MEP firms via open-source channels is unproven** for this audience.
- **Reddit and other practitioner forums were unreachable this cycle**, so the unfiltered complaint literature that would ordinarily anchor problem severity is missing. Every severity ranking in section 3 should be re-tested against that source before significant build investment.
