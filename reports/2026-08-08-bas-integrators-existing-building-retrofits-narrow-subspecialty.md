# Building Automation & Controls Contractors (BAS Integrators) for Existing-Building Retrofits — Narrow Subspecialty

**Narrow subspecialty examined: legacy-to-open controls *modernization engineering* — the as-found survey → points list → station database → point-to-point checkout → verified turnover chain inside a retrofit project.**

---

## 0. Cycle header

| Field | Value |
|---|---|
| Market | Building automation and controls contractors (BAS integrators) for existing-building retrofits |
| Angle | `narrow-subspecialty` |
| Named subspecialty | Legacy-to-open controls modernization engineering (as-found survey, point inventory, point mapping, checkout, verified turnover) |
| Claim ID | `d306b04c` |
| Date | 2026-08-08 |
| Backlog remaining after this claim | 370 assignments |

### Why this assignment over the others available

The ledger held 371 backlog assignments across 254 distinct markets, 226 of which had zero completed reports. Selection followed the stated preference order:

1. **Zero prior coverage of the market.** No completed report touches building automation at all. The closest neighbours — *Mechanical (HVAC) design engineering at small MEP consulting firms* (2026-08-04) and *Commissioning providers* (still in backlog) — sit on either side of this work but do not overlap it: the MEP engineer writes the sequence and never implements it; the Cx agent audits the result and never builds it. The integrator in the middle is unexamined.
2. **Expected strength of practitioner evidence.** This market has an unusually good public record for a trade of its size: a dedicated trade press with fresh 2025–2026 material (AutomatedBuildings.com), a practitioner newsletter written by a working Niagara engineer (BAS Briefing), a training podcast with episodes specifically about point-to-point checkout and estimating (Smart Buildings Academy), published owner Division 25 standards from universities that state the deliverables verbatim, vendor migration guides, and DOE/LBNL/CalNEXT field studies. That mix lets verified findings be separated from inference, which several thinner markets in the backlog would not allow.
3. **Angle diversity.** `narrow-subspecialty` was the least-covered angle in the completed set (6 of 31 reports, versus 10 core-practitioner-workflow and 8 back-office).
4. **A dated regulatory forcing function.** ASHRAE Guideline 36 sequences entered the 2025 California Energy Code §140.4 with an implementation date of **1 January 2026** — seven months before this cycle. That puts a new, much more complex control sequence in front of the same contractor workforce that is already short-staffed, which is exactly the condition under which narrow tools get bought.

One deliberate scoping decision: the market entry says "for existing-building retrofits," and I stayed there. New-construction BAS is a different job — the drawings are correct, every device is new, and the points list arrives with the bid documents. Retrofit work is defined by the opposite condition: **the documentation is wrong and the field is the only source of truth.** Every concept below is anchored on that asymmetry.

---

## 1. Market examined

**Industry.** HVAC/building controls contracting — NAICS 238220 (plumbing, heating, air-conditioning contractors) with a slice under 238210 (electrical/low-voltage) and 541330 for the engineering-heavy independents. The US commercial building automation market was sized at **USD 21.23 billion in 2025**, growing to a projected USD 22.53 billion in 2026 at a 6.12% CAGR ([Mordor Intelligence](https://www.mordorintelligence.com/industry-reports/united-states-commercial-building-automation-market)).

**Why the retrofit half is the growing half.** Nearly **70% of US office space predates 2000** ([AutomatedBuildings, June 2026](https://www.automatedbuildings.com/2026/06/five-global-trends-reshaping-building-automation-retrofitting/)). Mordor characterises the typical commercial property as housing **three to five discrete control systems installed over decades**, and reports that **integration alone consumes 20–80% of retrofit budgets**, that working in an occupied building adds **25–40% to project cost** because of phasing, and that the sector carries a **25% technician shortfall** with commissioning labour at **USD 80–120/hour**. Building performance standards (NYC Local Law 87's ten-year audit-and-retro-commissioning cycle, plus the widening BPS map across US cities) push owners toward controls upgrades on a legal clock rather than a capital-planning whim.

**Types of organization doing the work.**

| Organization type | Typical size | Role in this subspecialty |
|---|---|---|
| Independent systems integrator (Niagara/Tridium-based, often a Cochrane/Stromquist-type distributor's dealer) | 5–60 employees | The core buyer. Wins retrofits precisely because it is vendor-neutral and can integrate legacy trunks |
| Manufacturer branch office (JCI, Siemens, Honeywell, Schneider, ALC) | 20–200 per branch | Does modernization of its own installed base; has internal tooling but not for competitors' legacy gear |
| Mechanical contractor with a controls division | 3–15 in the controls group | Retrofit work rides along with equipment replacement; least tooled, most spreadsheet-bound |
| Owner-side controls group (university, health system, large campus) | 2–10 | Writes the Division 25 standard, receives the deliverables, and re-does the work when they are wrong |
| Independent commissioning agent / TAB firm | 2–20 | The reviewer at the far end of the handoff |

**The professional.** The person this subspecialty describes carries titles like *controls engineer*, *systems specialist*, *project engineer*, *lead technician*, or *applications engineer*. Typical profile: HVAC or electrical background plus vendor certification (Niagara N4, Metasys, Desigo); comfortable with BACnet MS/TP addressing and PID tuning; **not** a software developer, but entirely comfortable in Excel and in vendor tools that consume CSV. A firm doing $8–15M/year in controls revenue may have only three to six people who can do this specific work, and they are the same people who are billable on site.

**Target size for the tools below.** Firms of **5–60 people** running **10–40 retrofit projects a year**, where a single person carries the survey, the points list, the station build and the checkout on two to four concurrent jobs. Below five people the tooling budget is zero but the free open-source base version still lands; above ~200 people the firm has internal developers and a corporate standard.

---

## 2. How the work is performed, start to finish

### Stage 1 — The site walk (as-found survey)

The trade press describes this as a formal, tooled activity, not a casual look. The recommended kit is "**tablet or printed data collection sheets**, flashlight, small hand tools for panel access, temperature and humidity meter, CO2 meter," plus camera and network tester, and the findings are organised by a standing form covering "**BAS architecture, central plant, air handlers and RTUs, terminal units, critical spaces, PSA opportunities, retrofit candidates**" ([AutomatedBuildings, Dec 2025](https://www.automatedbuildings.com/2025/12/how-to-perform-a-site-walk-that-actually-sells-bas-retrofits-and-planned-service-agreements/)).

What gets recorded per controller: "**controller family and model numbers, firmware versions if easily visible, mix of legacy and modern controllers on the same trunks**," and per network segment: "**each trunk and its protocol (BACnet MS/TP, BACnet IP, LON, proprietary, etc.), count devices per segment and compare to best practice limits**," plus notes on end-of-life and unsupported controllers.

The output today is a phone camera roll, a marked-up floor plan, and handwritten sheets that someone re-types into Excel back at the office — usually the same person, usually at night, usually two to five days later when half the panel photos have become ambiguous.

The independent-integrator literature formalises the same first step as "**system inventory — document all controllers, software versions, network configuration, and known failures**" ([Controls.nyc](https://controls.nyc/blog/johnson-controls-metasys-upgrade-integrate/)), and puts phased migration of a legacy Metasys estate at **5–7 years** with per-controller replacement at **$3,000–$8,000** (Metasys-native) or **$2,000–$5,000** (open BACnet), and integration-layer-only work at **$50,000–$140,000**.

### Stage 2 — Estimating and takeoff

Estimators run a "**device takeoff**" — listing "each controller, sensor, actuator, and interface required for the job" — from specifications, mechanical and electrical drawings and client requirements, then add network equipment, panels and cabling ([Smart Buildings Academy ep. 490](https://podcast.smartbuildingsacademy.com/490)). The named failure mode is that "misinterpreting or overlooking" the documents "can cause serious gaps in the estimate," with scope gaps between trades (power wiring, device mounting, connectivity) called out as the expensive ones.

In a retrofit the documents are the problem. There are no reliable contract drawings for the existing controls; the takeoff *is* the survey. Where labour is **50–75% of total project cost** ([FractionalBAS](https://fractionalbas.com/guides/bas-cost-breakdown/), citing NREL) and installed cost runs **$2.50–$7.00/sq ft**, a missed trunk or an undercounted terminal-unit population is a direct margin event.

A second, purely arithmetic risk lands here: **licensing.** Niagara JACE licences are sold in device tiers (5, 10, 25, 100, 200+), and "**in Niagara 50 points equals one device**" for licensing purposes — so a 30-point VAV controller consumes well under a device while a 100-point plant integration consumes two ([Stromquist](https://www.stromquist.com/blog/11117/blog-niagara-jace-licensing-explained-device-limits-points-and-sma-made-simple)). Getting this wrong is discovered at commissioning, when the licence must be upgraded under schedule pressure.

### Stage 3 — Points list production and approval

The points list is the spine of the entire job. It originates "in the temperature controls section of the consulting engineer's specification," working alongside the Sequence of Operation, and carries per-point: description, type (AI/BI/AO/BO), alarm flag, non-DDC flag, and spare capacity ([AutomatedBuildings points list primer](https://www.automatedbuildings.com/news/may09/columns/090415012333calabrese.htm)). The same primer warns that a comprehensive points list gives "**upwards of 90 percent of what is required**" — the remaining safety and limit devices hide in the sequence text — and recommends deliberately over-counting points to avoid being boxed in later.

Owner specifications treat the list as a controlled, signed artifact. Oregon State's Section 230900 requires that "**the final points list shall be verified by the Control Contractor, the Owner's Representative, and signed by both parties**" ([OSU 230900](https://bid.oregonstate.edu/opportunity/viewFile/48222/230900%20Building%20Automation%20System%20(BAS)%20Controls.pdf)). UConn's Division 25 appendix requires the software submittal to contain "**descriptive point lists, application program listings with comments, alarm lists, and point-to-point checkout records**," graphics released at 50/75/90% completion, and a final database backup plus source graphic files at turnover ([UConn Appendix V](https://updc.uconn.edu/wp-content/uploads/sites/1525/2016/04/Appendix_V_Building_Automation_Standards_May2015.pdf)).

In practice this document exists in **at least three divergent versions** on any retrofit: what the engineer specified, what the contractor submitted, and what actually got installed and discovered on the wire. Nothing in the standard toolchain reconciles them.

### Stage 4 — Station build, naming and graphics

The integrator builds the supervisory station, discovers devices, creates proxy points and binds them to logic and graphics. This is where naming discipline either pays or costs. A working Niagara engineer states the problem plainly: manufacturers name the same point differently — "**Siemens uses CTL_TEMP, JCI uses ZN-T**" — and "**inconsistent naming will prevent us from using auto-tags, using the batch editor, re-using graphics, using BQL to collect data**" ([BAS Briefing, Niagara Best Practices](https://basbriefing.substack.com/p/niagara-best-practices)). A retrofit is by definition a multi-vendor naming collision.

The same author quantifies the payoff of bulk operations in Niagara's Batch Editor: it turned "**a tedious, 16-hour task**" into "**just 10-15 minutes**" — the tasks being mass setpoint changes, standardising names where "some points named ZN-T, others ZoneTemp or RM_T," adding history extensions across many points, and editing alarm/history slots in bulk ([BAS Briefing, Niagara Batch Editor](https://basbriefing.substack.com/p/niagara-batch-editor)). That 64× ratio is the honest measure of how much of this job is bulk data manipulation performed by hand.

Graphics is a parallel drain. A growing integrator described technicians being "**drawn into graphics tasks that pull them away from programming, startup, service, and customer care**," with "every individual applying their own style, workflow, and interpretation," and turnaround that independent contractors "struggled to maintain pace with" — the firm ended up outsourcing **100% of floor-plan services** to a specialist vendor ([AutomatedBuildings, June 2026](https://www.automatedbuildings.com/2026/06/a-growing-integrators-path-to-scaling-bas-floor-plans-and-graphics/)). A dedicated outsourced-graphics industry ([QA Graphics](https://www.qagraphics.com/system-graphics/), [BASGFX](https://www.basgfx.com/)) exists because of this.

### Stage 5 — Point-to-point checkout

The trade's own training material lays out the process: prepare control drawings, IO schedules and testing logs; use a tablet on site; follow a consistent test sequence; **label each point immediately after testing**; test every sensor individually; document each step ([Smart Buildings Academy ep. 519](https://podcast.smartbuildingsacademy.com/519)). The named mistakes are skipping documentation, failing to label tested points, and "assuming similar points behave identically."

A vendor checkout workbook shows the actual paperwork: a **P2P Checkout Template**, Trunk Checklist, Controller Checklist, Input and Output Cheat Sheets, plus functional test templates capturing pass/fail — with inputs recorded by type (dry contact, resistive, DC voltage, milliamp) including wiring configuration, polarity and calibration values, and controllers recorded with addressing, mounting, firmware version ([Stromquist BAS Startup and Checkout](https://www.stromquist.com/customer/docs/bam/BAS%20Startup%20and%20Checkout%20v1.pdf)). Its framing: "point-to-point checkout is your opportunity to validate system performance prior to the warranty period."

Specifications require it explicitly — OSU demands "a point-to-point check out of **all** newly installed points to verify point existence, proper end to end connection and correct SI units with the Owner's Representative."

How well does it work? A commissioning consultant's field observation is damning and specific: "**in a building with a controls system verified '100% Point-to-Point', I have had projects on which I reported more than 50 controls items operating incorrectly**," and a colleague sampling ten rooms found "**three rooms were not operating as commanded**" ([CFMS Consulting](https://www.cfms.ca/blog/commissioning-controls-systems-sampling-vs-100-point-to-point-verification/)). The paperwork says complete; the building says otherwise.

### Stage 6 — Sequence verification and functional testing

Retrofits increasingly carry Guideline 36 sequences. LBNL's OpenBuildingControl programme states the core difficulty directly: "**control programmers still need to convert this text into computer language specific to the building's HVAC and BAS and adapt it to the BAS point naming conventions**," and "**the higher complexity of ASHRAE G36 exposes the system to more errors during the programming and implementation stages**" ([CalNEXT final report, Nov 2025](https://calnext.com/wp-content/uploads/2025/11/ET22SWE0039_ASHRAE-Guideline-36-Open-Source-Supervisory-Control-Technology-Development-and-Demonstration_Final-Report.pdf)). Its own field deployment surfaced trim-and-respond timing inconsistencies, sign-convention discrepancies between the guideline text and the implementation, chilled-water plant reverse-engineering "due to outdated/incorrect drawings," and PID retuning.

LBNL's verification method compares trended controller outputs against a simulated reference and requires "**point mappings — JSON files correlating CDL variable names with actual BAS point names, including unit conversions**," with trends at 5–60 second intervals ([OpenBuildingControl §12](https://obc.lbl.gov/specification/verification.html)). It also concedes the practical barrier: "automated verification requires development of tools for matching building automation system objects to CDL specifications, presenting **significant implementation overhead**." This is a research-grade Modelica toolchain. No 20-person integrator will run it.

### Stage 7 — Turnover

Deliverables: as-built shop drawings in CAD, signed points list, checkout records, trend logs ("completed versions of reports, checklists, and trend logs used to meet requirements"), graphics source files, station/database backup, O&M manuals with part numbers and software versions, and operator training. UConn additionally requires 48-hour trend reports for each occupancy sensor input.

And then the value leaks. Practitioner observation: communication faults "can often take **a minimum of four hours to uncover**"; operators change setpoints without understanding cascading effects; and "**building HVAC systems typically start to consume more energy within five years even with proper maintenance**" because nobody re-adapts the controls to how the building actually changed ([AutomatedBuildings, When Building Automation Fails to Deliver](https://www.automatedbuildings.com/news/may14/articles/denning/140423012707denning.html)).

---

## 3. Most important problems, ranked

### P1 — The as-found survey is captured on paper/photos and re-keyed into Excel, and it is the sole basis for the price

**Who:** the lead controls engineer or estimator doing the walk. **When:** once per pursuit, on every retrofit. **Currently handled by:** a printed or PDF survey form, phone photos, a marked-up plan, then hours of transcription into an estimating spreadsheet. **Why inadequate:** the transcription is lossy and delayed; the person who walked the site is the only one who can decode the notes; nothing enforces completeness, so a trunk with no device count or a panel with no photo is invisible until it becomes a change order. **Frequency:** 10–40 times per year per firm. **Cost:** with labour at 50–75% of project cost and integration at 20–80% of a retrofit budget, an undercounted terminal-unit population on a $400k job is a five-figure margin event; the re-key itself costs 4–12 hours per building. **Evidence:** the site-walk methodology article (verified); Mordor's integration-share and occupied-building cost premiums (verified, vendor-analyst); margin consequence (strong inference).

### P2 — Three versions of the points list exist and nobody reconciles them

**Who:** the project engineer, and later the commissioning agent and the owner. **When:** at submittal, at station build, and at turnover. **Currently handled by:** manual visual comparison of an Excel submittal against the spec, and against whatever the discovery tool found. **Why inadequate:** the comparison is done by eye across hundreds to thousands of rows with inconsistent descriptions; specifications explicitly require a *signed*, verified final list (OSU), which means someone is attesting to a reconciliation they performed by scrolling. The points list primer's own warning — that ~10% of required points live only in the sequence text, not the list — guarantees systematic omissions. **Frequency:** every project, 2–4 times per project as revisions land. **Cost:** each missed point is a controller I/O shortfall, a licence overage, or a field change order; each phantom point is a licence and labour cost carried for nothing. **Evidence:** OSU signed-list requirement (verified); UConn submittal contents (verified); the 90% completeness warning (verified).

### P3 — Point naming is inconsistent across legacy vendors, which blocks every downstream automation

**Who:** the station engineer. **When:** during station build, and again every time analytics, graphics reuse or bulk edits are attempted. **Currently handled by:** hand-renaming in Workbench, or bulk queries written per-project by the one engineer who knows BQL. **Why inadequate:** a retrofit integrates two to five vendors' naming schemes into one station; the practitioner statement is that inconsistent naming "will prevent us from using auto-tags, using the batch editor, re-using graphics, using BQL to collect data" — i.e. it disables the very tools that make the job economic. **Frequency:** every retrofit; recurring for the life of the site. **Cost:** the Batch Editor case gives the shape of it — 16 hours of manual work versus 10–15 minutes when the data is uniform enough to query. **Evidence:** BAS Briefing naming and batch-editor posts (verified, first-person practitioner); LBNL's requirement for an explicit point-name mapping file (verified); Haystack/Brick literature on tagging effort (verified, academic).

### P4 — Point-to-point checkout is paper-based and its completion signature does not correspond to a working building

**Who:** field technicians; consequences land on the Cx agent, GC and owner. **When:** at startup, under schedule pressure, usually the compressed final weeks. **Currently handled by:** printed P2P templates, IO schedules, sometimes a tablet PDF; results re-typed into a closeout package. **Why inadequate:** no enforcement of coverage, no live percent-complete by panel, no forced capture of the measured value, and no linkage between the point tested and the point in the database — so a signed 100% package coexists with "more than 50 controls items operating incorrectly." **Frequency:** every project; thousands of individual point tests per building. **Cost:** at commissioning labour of $80–120/hour, re-verification and return trips are direct; the reputational cost with the Cx agent and owner is larger. **Evidence:** CFMS field observation (verified, first-person); OSU 100%-of-new-points requirement (verified); the existence of dedicated P2P products and patents (verified — problem is real enough to patent).

### P5 — Sequences are re-implemented from prose and never verified against what was written

**Who:** the controls programmer; increasingly under a code mandate. **When:** every retrofit that touches AHU/VAV control; now every California project under §140.4 from 1 Jan 2026. **Currently handled by:** the programmer reads the sequence, writes logic, and a Cx agent later performs a handful of functional tests by manually overriding points and watching. **Why inadequate:** LBNL states the translation problem outright and observes that G36's complexity increases programming error exposure; its own field team found timing and sign-convention errors in a *reference* implementation. The rigorous verification method requires Modelica and a research toolchain. **Frequency:** every AHU/plant on every retrofit. **Cost:** un-verified sequences are the mechanism by which retrofit energy savings quietly fail to materialise; PNNL/DOE and the practitioner literature both describe savings decaying within a few years. **Evidence:** CalNEXT/LBNL (verified); Title 24 §140.4 G36 adoption with 1 Jan 2026 implementation date (verified via secondary code summary); savings decay (strong inference).

### P6 — Niagara device/point licence sizing is done by hand and discovered late

**Who:** estimator and station engineer. **When:** at bid, again at station build. **Currently handled by:** a manual count in the takeoff spreadsheet. **Why inadequate:** the 50-points-equals-one-device rule interacts with trunk-loading best practice and with the phased nature of retrofits (points added in later phases push over a tier boundary). **Frequency:** every project. **Cost:** an unplanned licence tier upgrade plus the schedule disruption of procuring it during commissioning. **Evidence:** Stromquist licensing explainer (verified); site-walk guidance to count devices per segment against best-practice limits (verified).

### P7 — Legacy controller replacement selection is a multi-table lookup exercise per device type

**Who:** the applications engineer. **When:** during scoping of a controller-swap retrofit. **Currently handled by:** flipping through vendor modernization guides. JCI's N2 guide requires, per legacy device family (VMA14xx, DX-9100, UNT, VAV1xx, AHU, DCM, XTM-105, XBN/XRE/XRL/XRM), consulting **footprint comparisons, wiring-connection comparisons, and point comparisons**, plus control-logic reconfiguration and supervisor changes, with special handling where "Zone Bus not supported" and "XT Bus not supported" ([JCI Modernization Guide for N2 Controllers](https://docs.johnsoncontrols.com/bas/r/Metasys/en-US/Modernization-Guide-for-N2-Controllers-Metasys/12.0)). **Why inadequate:** it is deterministic table lookup performed by a senior person, repeatedly, and the "points lost in translation" cases are exactly what generates change orders. **Frequency:** per retrofit, per device family. **Cost:** engineering hours plus the risk of a mid-install discovery. **Evidence:** the guide's own structure (verified).

### P8 — Graphics production pulls billable technicians off billable work

**Who:** technicians and station engineers. **When:** late in every project. **Currently handled by:** in-house ad-hoc creation or outsourcing to a graphics vendor. **Why inadequate:** it is inconsistent, unschedulable, and displaces higher-value labour — the integrator case study is explicit about technicians being "drawn into graphics tasks." **Frequency:** every project. **Cost:** displaced technician hours during the highest-pressure phase. **Evidence:** AutomatedBuildings integrator case study (verified); existence of a specialist outsourcing industry (verified).

### P9 — Turnover packages are assembled by hand against a specification checklist

**Who:** project manager. **When:** at closeout, under retainage pressure. **Currently handled by:** a folder and a memory of what Division 25 asked for. **Why inadequate:** owner standards enumerate a long, specific list (as-built CAD, signed points list, checkout records, trend logs, graphics source files, database backup, O&M with part numbers and software versions, spare parts list with lead times, training records); missing one delays final payment. **Frequency:** every project. **Cost:** retainage delay measured in weeks. **Evidence:** UConn and OSU specifications (verified).

---

## 4. Application opportunities

### A. **AsFound** — retrofit site-survey capture that outputs a points list and a takeoff

- **Intended user:** lead controls engineer / estimator doing the walk.
- **Problem solved:** P1.
- **Current workflow:** paper form + phone photos + marked-up plan → 4–12 hours of transcription → estimating spreadsheet.
- **Proposed workflow:** offline-capable browser app on a tablet or phone. Hierarchy is enforced: Site → Building → Trunk (protocol, media) → Panel → Controller (family, model, firmware, address) → Device/Point (type, service, condition). Each level has a small fixed form plus photos attached to the node, not to a camera roll. On return to the office it exports (1) a normalized controller/point inventory CSV, (2) an estimating summary by controller family and point type, (3) a Niagara device/licence consumption estimate, (4) a **gap report** listing every node missing a required field or photo, and (5) a photo index keyed to node IDs.
- **Inputs:** field observation; optionally an imported prior points list or equipment schedule to pre-seed the tree.
- **Outputs:** inventory CSV/XLSX, gap report, photo bundle, takeoff summary, licence estimate.
- **Essential features:** offline-first with local storage sync; enforced hierarchy; per-node photos; required-field validation; duplicate-address detection; a per-firm survey template (JSON) so the form matches the firm's own scope sheet.
- **Excluded from v1:** pricing/labour rates, CRM, proposal generation, BIM/floor-plan pinning, multi-user real-time sync.
- **AI:** *optional and confined* — OCR of nameplate photos to pre-fill model/serial, proposed for human confirmation. Core value requires none.
- **Why not a spreadsheet:** the data is a tree, not a table; spreadsheets cannot enforce per-node required fields, cannot attach photos to rows meaningfully, and are miserable on a tablet in a mechanical room. The transcription step that spreadsheets force *is* the problem.
- **Complexity:** medium. **Learning:** 20 minutes. **Value:** eliminates 4–12 hours of re-keying per building and materially reduces undercounted-scope change orders.
- **Risks:** photos of a client's facility are mildly sensitive (local-first storage answers this); no regulatory constraint.
- **Substitutes:** GoCanvas HVAC survey forms, SiteCapture, ArcSite, generic form builders — all generic, none produce a points list or a licence count.
- **Why still attractive:** the differentiator is the *output shape*, not the capture. A generic form app gives you a PDF; this gives you the artifact the next four stages consume.
- **Customization potential:** high — per-firm survey templates and per-firm export layouts are a natural paid service.

### B. **PointList Reconciler** — three-way diff of specified vs submitted vs discovered points

- **Intended user:** project engineer at the integrator; equally the owner's rep and the Cx agent.
- **Problem solved:** P2.
- **Current workflow:** visual comparison of spreadsheets, then a signature on a "verified" final list.
- **Proposed workflow:** load up to three sources — the engineer's specified list (XLSX/CSV, or pasted from a spec table), the contractor's submittal list, and the live discovered list exported from the station/discovery tool. Map columns once per source (saved as a profile). The tool matches rows using a configurable key (equipment tag + point role, with fuzzy fallback on description), then produces a **four-bucket exception report**: specified-but-not-submitted, submitted-but-not-discovered, discovered-but-not-specified (the "where did this come from" bucket), and matched-but-attribute-mismatched (type, units, alarm flag). Output includes a signable reconciliation sheet listing every exception with a disposition column.
- **Inputs:** two or three point lists in any tabular form.
- **Outputs:** exception report (XLSX + PDF), signable reconciliation sheet, a clean merged master list.
- **Essential features:** column-mapping profiles; configurable match key; fuzzy description matching with a confidence column and a human-confirm step; per-project saved state so re-runs after a revision show *what changed since last reconciliation*.
- **Excluded from v1:** parsing points lists out of PDF specification documents; live BACnet discovery; workflow/approval routing.
- **AI:** *optional, narrow*. Fuzzy matching of differently-worded descriptions ("Zone Temp" ↔ "ZN-T" ↔ "Space Temperature") is better served by a dictionary of vendor abbreviations plus string distance than by a model. An LLM is defensible only for the unmatched remainder, presented as suggestions.
- **Why not a spreadsheet:** VLOOKUP handles a clean single key; it does not handle three sources with different keys, unit mismatches, and a re-runnable change history. Practitioners already *try* to do this in Excel — that is the evidence it is needed, and the evidence that Excel loses.
- **Complexity:** medium (small if launched as two-way). **Learning:** 30 minutes. **Value:** turns a signature-on-faith into a signature-on-evidence; each caught missing point avoids a field change order.
- **Risks:** none regulatory; point lists are not sensitive. Main risk is column-mapping friction on first use.
- **Substitutes:** none specific. Cx platforms (CxAlloy, Facility Grid, Bluerithm) manage issues and checklists, not list reconciliation.
- **Why still attractive:** it addresses a *contractually named* deliverable ("signed by both parties") with no incumbent, and it sells to three parties in the same transaction.
- **Customization:** high — per-owner naming standards and per-vendor export profiles.

### C. **CheckoutKit** — offline point-to-point checkout generated from the points list

- **Intended user:** field technicians; PM monitors progress.
- **Problem solved:** P4.
- **Current workflow:** printed P2P templates and IO schedules; results re-typed into a closeout package.
- **Proposed workflow:** import the reconciled points list → the app generates one test record per point, grouped by trunk/panel/controller. Technician works offline: per point, records commanded value, measured value, pass/fail, calibration offset applied, optional photo, and initials with timestamp. Live **percent-complete by panel and by point type**, an "untested points" list that cannot be hidden, and one-click generation of the signed checkout package PDF plus a punch list of failures grouped by responsible party (controls / mechanical / electrical).
- **Inputs:** points list CSV; optionally a template of expected value ranges per point type.
- **Outputs:** checkout package PDF, failures/punch CSV, coverage report, raw results CSV.
- **Essential features:** offline-first; generated-from-list (never hand-typed point names); mandatory measured-value entry for analog points; coverage that is computed, not asserted; export that matches the spec's documentation requirement.
- **Excluded from v1:** live BACnet reads, functional-test scripting, multi-trade Cx issue management, scheduling.
- **AI:** **inappropriate.** This is structured data capture with arithmetic.
- **Why not a spreadsheet:** a spreadsheet on a tablet in a ceiling is unusable, offers no coverage enforcement, and produces no signed package. The failure being addressed — a 100% signature over a building with 50 broken items — is precisely a coverage-accounting failure.
- **Complexity:** small. **Learning:** 10 minutes. **Value:** removes the re-typing step entirely; makes coverage auditable; reduces return trips at $80–120/hour.
- **Risks:** low. Records could later be evidence in a dispute — which argues for immutable, timestamped entries and an export that cannot be silently edited.
- **Substitutes:** KORE PointCheck (purpose-built commercial product), CxAlloy/Facility Grid/Bluerithm (Cx platforms, priced and scoped for the Cx agent, not the installing contractor), paper.
- **Why still attractive despite them:** the incumbents sell to the commissioning agent or to the enterprise; the 5–40 person integrator uses paper because the Cx platforms are the wrong size and the wrong buyer. A free, offline, single-purpose tool that ingests the points list the firm already has is a different product at a different price point (zero). It is also the natural wedge: it is the easiest to build and the easiest to adopt, and it pulls the firm into the points-list discipline that concepts A and B monetise.
- **Customization:** medium-high — per-owner checkout form layouts, per-firm branding, spec-specific documentation formats.

### D. **NameForge** — point-name normalizer and rename plan generator

- **Intended user:** station engineer.
- **Problem solved:** P3.
- **Current workflow:** hand-renaming in Workbench, or one-off BQL/batch queries written per project by the one person who knows how.
- **Proposed workflow:** import a discovered point export (CSV). The tool applies a **rule pack** — a per-owner or per-firm naming standard expressed as ordered rules plus a vendor-abbreviation dictionary (Siemens `CTL_TEMP`, JCI `ZN-T`, generic `ZoneTemp` → standard `ZN_T`) — and produces a proposed rename table: current name, proposed name, matched rule, confidence, conflicts. Flags collisions, illegal characters, leading digits, over-length names, and orphans that matched nothing. Exports a **batch-edit-ready CSV** for the target tool and a human-readable rename audit trail.
- **Inputs:** point export CSV; a naming-standard rule pack (YAML/JSON).
- **Outputs:** rename plan CSV, conflict report, audit trail, optional equipment/role tag columns for later analytics onboarding.
- **Essential features:** rule packs as data, not code; dry-run always; conflict detection; reversible plan (old↔new mapping preserved as the artifact).
- **Excluded from v1:** writing to the BAS directly; full Haystack/Brick model generation; graphics rebinding.
- **AI:** *optional, for the remainder only*. Rules and a dictionary will resolve the large majority; an LLM classifying leftover oddities into (equipment type, point role) is a reasonable assist with human confirmation. Building the whole thing on a model would be slower, less auditable and less trusted.
- **Why not a spreadsheet:** find-and-replace has no conflict detection, no rule provenance, and no audit trail — and the renaming is the thing you must be able to justify to an owner later.
- **Complexity:** medium. **Learning:** 45 minutes (the rule pack is the learning curve). **Value:** the batch-editor anecdote (16 h → 15 min) is the ceiling; realistically several hours per project, plus it unlocks graphics reuse and analytics onboarding.
- **Risks:** renaming a live station is genuinely dangerous — hence dry-run-first, plan-as-artifact, and never writing directly in v1.
- **Substitutes:** Niagara Batch Editor (free, powerful, requires BQL fluency and operates *inside* the station), Bulk Slots from CSV, Haystack tagging tools, analytics vendors' onboarding services.
- **Why still attractive:** the incumbents execute changes; none *plan and justify* them, and none work vendor-agnostically on an export before you commit. The rule pack — an owner's naming standard as machine-readable data — is the durable asset.
- **Customization:** very high. A campus owner's naming standard encoded as a rule pack is a repeatable paid engagement.

### E. **TrendAssert** — trend-data assertion checker for as-installed sequences

- **Intended user:** integrator's commissioning lead; also Cx agents and owner engineers.
- **Problem solved:** P5.
- **Current workflow:** manual overrides and eyeball observation on a sample of units; trend CSVs opened in Excel and charted one AHU at a time.
- **Proposed workflow:** drop in trend exports (CSV) plus a small **assertion file** describing expected behaviour in plain declarative terms — economizer disabled above the high-limit, SAT reset stays within its bounds and moves in the right direction, no simultaneous heating and cooling, commanded vs actual damper/valve agreement within tolerance, minimum-OA maintained during occupancy, no flatlined or railed sensors, trim-and-respond changes bounded per interval, occupied/unoccupied transitions follow the schedule. Output: a findings report per equipment, ranked by hours-in-violation, each with the offending time window and a chart.
- **Inputs:** trend CSVs (timestamp + point columns), a point-name mapping (reusing NameForge output), an assertion pack.
- **Outputs:** findings report (HTML/PDF), per-finding time-series excerpts, CSV of violations.
- **Essential features:** a library of prewritten assertion packs for common G36 AHU/VAV sequences; tolerant CSV ingestion (irregular timestamps, gaps, mixed units); unit handling (°F/°C, %, in. w.c.); ranking by duration and severity rather than count.
- **Excluded from v1:** live BAS connection, Modelica/simulation-based reference comparison, FDD-style diagnosis or root-cause inference, energy savings estimation.
- **AI:** **inappropriate for detection** — these are deterministic rules over time series and must be defensible line by line. Optional for drafting the narrative summary of already-computed findings.
- **Why not a spreadsheet:** possible for one AHU and one rule; not for twenty pieces of equipment × a dozen assertions × two weeks of one-minute data, repeated after every fix.
- **Complexity:** medium. **Learning:** 1–2 hours for the assertion syntax; near-zero if using the shipped packs.
- **Value:** converts "we functionally tested a sample" into "we checked every unit against every rule for two weeks." Directly relevant to Title 24 §140.4's G36 adoption from 1 Jan 2026 and to Local Law 87-style retro-commissioning obligations.
- **Risks:** false positives erode trust — mitigated by tolerance bands and duration thresholds. A finding report can be discoverable in a dispute; it should be framed as an internal QC aid, not a certification.
- **Substitutes:** full FDD/analytics platforms (Clockworks, CIM, Buildings IOT, SkySpark) — powerful, subscription-priced, and aimed at ongoing operation, not project QC; LBNL OpenBuildingControl — rigorous but Modelica-based with acknowledged "significant implementation overhead."
- **Why still attractive:** there is a wide, empty middle between "open the CSV in Excel" and "deploy an analytics platform." Project-duration QC on exported trends is that middle.
- **Customization:** very high — per-owner or per-sequence assertion packs; this is the most obviously billable customization in the set.

### F. **LicenseSizer** — device/point licence and trunk-loading calculator

- **Intended user:** estimator and station engineer.
- **Problem solved:** P6.
- **Current workflow:** hand counting in the takeoff spreadsheet.
- **Proposed workflow:** feed it the controller/point inventory (from AsFound or any CSV). It computes per-supervisory-controller device and point consumption under the platform's rule (e.g. Niagara's 50 points = 1 device), maps that to purchasable licence tiers, flags headroom below a configurable reserve (default 20% for later phases), and checks devices-per-MS/TP-segment against best-practice limits. Output: a licence and architecture bill of materials plus a riser summary table.
- **Inputs:** inventory CSV; a platform rule profile.
- **Outputs:** licence BOM, per-JACE loading table, trunk-loading warnings.
- **Essential features:** rule profiles as data (platforms change their licensing); phase-aware headroom; clear "you are 3 points from the next tier" warnings.
- **Excluded from v1:** pricing lookups, procurement, vendor part numbers beyond a user-maintained table.
- **AI:** **inappropriate.** Arithmetic.
- **Why not a spreadsheet:** it genuinely *could* be a spreadsheet — and should ship as one alongside the tool. Its value is in being pre-loaded with correct, current rules and in consuming the inventory format the other tools emit.
- **Complexity:** small. **Learning:** 10 minutes. **Value:** avoids one late licence-tier surprise per year, which is worth more than the tool costs to build.
- **Risks:** stating another company's licensing rules creates an accuracy obligation; ship rules as user-editable data with a "verify against your distributor" notice.
- **Substitutes:** distributor sales engineers, vendor sizing tools behind partner logins.
- **Why still attractive:** free, vendor-neutral, and works from the inventory the firm already produced. Modest but frictionless.
- **Customization:** low-medium.

### G. **SwapRef** — legacy controller replacement cross-reference and scope generator

- **Intended user:** applications engineer.
- **Problem solved:** P7.
- **Current workflow:** page through vendor modernization guides per device family, three comparison tables each.
- **Proposed workflow:** a maintained, community-editable cross-reference dataset (legacy family → candidate replacements, with I/O count and type comparison, footprint note, wiring-reuse note, bus-support caveats such as "Zone Bus not supported," and a **points-lost** flag). Feed it the as-found controller inventory; it returns a replacement schedule with quantities, per-device caveats, and an exceptions list of legacy devices with no clean equivalent — which is exactly the list that must be priced as engineering rather than as a swap.
- **Inputs:** controller inventory CSV.
- **Outputs:** replacement schedule, exceptions list, per-device caveat sheet.
- **Essential features:** dataset as an open, versioned, citation-carrying file; "no equivalent" as a first-class outcome; nothing asserted without a source reference.
- **Excluded from v1:** pricing, availability, automatic wiring diagrams.
- **AI:** **inappropriate.** This is curated reference data; a hallucinated I/O count is a five-figure field error.
- **Why not a spreadsheet:** it *is* a spreadsheet at heart — the product is the curated, sourced, maintained content plus the join against an inventory.
- **Complexity:** medium (small code, heavy content). **Learning:** 15 minutes.
- **Value:** hours of senior engineering per project, and earlier discovery of the expensive exceptions.
- **Risks:** the real one. Vendor documentation is copyrighted; the dataset must be independently compiled facts with citations to public documents, never reproduced tables. Getting a fact wrong has direct commercial consequence — so every row needs a source link and a "verify against current manufacturer documentation" disclaimer.
- **Substitutes:** the vendors' own guides (authoritative, single-vendor, PDF).
- **Why still attractive:** no cross-vendor version exists, and retrofits are cross-vendor by definition. But the legal/accuracy risk is real and it is why this ranks below the others.
- **Customization:** medium.

### H. **GraphicsBind** — point-binding manifest and graphics QA report

- **Intended user:** station engineer or the outsourced graphics vendor.
- **Problem solved:** P8.
- **Current workflow:** hand-binding points to graphic objects; inconsistent per-person style; errors found by clicking around.
- **Proposed workflow:** given the normalized point list and an equipment-template mapping (this AHU is template "AHU-VAV-Econ"), emit a per-equipment binding manifest listing every graphic placeholder and the exact point path it should bind to — plus, on re-import of the built station's export, a **QA report** of unbound placeholders, dead bindings, and points that appear on no graphic.
- **Inputs:** point list; template definitions; optionally a station point export for the QA pass.
- **Outputs:** binding manifest per equipment, QA/coverage report.
- **Essential features:** template definitions as data; the QA pass (which is the durable half of the value); vendor-agnostic manifest format.
- **Excluded from v1:** rendering graphics, generating SVG/PX files, floor-plan drafting.
- **AI:** inappropriate.
- **Why not a spreadsheet:** the manifest could be; the QA reconciliation could not.
- **Complexity:** medium. **Learning:** 1 hour. **Value:** removes hand-binding drudgery and catches the "point exists but nobody can see it" class of defect.
- **Risks:** highly dependent on target-platform file formats, which are vendor-specific and change — the reason this ranks low.
- **Substitutes:** QA Graphics / BASGFX outsourcing; vendor template tooling.
- **Why still attractive:** the QA half is vendor-neutral and unserved. But it is the most fragile concept here.
- **Customization:** medium.

### I. **TurnoverPack** — Division 25 closeout completeness checker and package builder

- **Intended user:** project manager at the integrator; mirror-image value for the owner's rep receiving it.
- **Problem solved:** P9.
- **Current workflow:** a folder, a memory, and a rejection letter.
- **Proposed workflow:** select or author a **deliverable profile** encoding what a given owner's Division 25 requires (as-built CAD, signed points list, P2P records, trend logs, graphics source files, station backup, O&M with part numbers and software versions, spare-parts list with lead times, training sign-in). Point it at the closeout folder; it reports present/missing/stale per item, checks basic properties (file type, non-zero size, dates after substantial completion), and assembles an indexed, bookmarked PDF/ZIP package with a cover checklist.
- **Inputs:** a folder; a deliverable profile.
- **Outputs:** completeness report, indexed package, cover checklist for signature.
- **Essential features:** profiles as data (a small library seeded from published university standards); missing-vs-stale distinction; no cloud dependency.
- **Excluded from v1:** document generation, e-signature, owner portal upload, content-level review of the documents.
- **AI:** *optional* — extracting a deliverables list from a pasted spec section into a draft profile is a reasonable one-time assist with human review. Detection is file-system logic.
- **Why not a spreadsheet:** a checklist in Excel does not look at the folder. The value is that the check is executed, not remembered.
- **Complexity:** small-medium. **Learning:** 20 minutes. **Value:** weeks of retainage; also protects against the "we shipped it" / "we never got it" dispute.
- **Risks:** none material.
- **Substitutes:** GC closeout modules in Procore/Kahua (owned by the GC, not the sub; generic to all trades).
- **Why still attractive:** the sub's own pre-flight check before the GC's gate is a different tool with a different owner. Modest but very easy.
- **Customization:** high — an owner-specific profile is a one-hour paid deliverable that saves the same owner's contractors repeatedly.

---

## 5. Opportunity ranking

Scored 1–5 on each criterion; maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of build | Stays narrow | Differentiation | Customization | Test data available | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| C | **CheckoutKit** | 4 | 5 | 5 | 5 | 5 | 5 | 3 | 4 | 5 | 5 | **46** |
| B | **PointList Reconciler** | 5 | 4 | 5 | 4 | 4 | 5 | 5 | 4 | 4 | 4 | **44** |
| A | **AsFound** | 5 | 4 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 4 | **43** |
| D | **NameForge** | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 5 | 5 | 5 | **43** |
| F | **LicenseSizer** | 3 | 4 | 4 | 5 | 5 | 5 | 4 | 3 | 4 | 4 | **41** |
| E | **TrendAssert** | 5 | 4 | 5 | 3 | 3 | 3 | 4 | 5 | 4 | 4 | **40** |
| I | **TurnoverPack** | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | **40** |
| G | **SwapRef** | 4 | 3 | 3 | 5 | 3 | 4 | 4 | 3 | 3 | 3 | **35** |
| H | **GraphicsBind** | 3 | 3 | 3 | 4 | 3 | 4 | 3 | 4 | 3 | 3 | **33** |

### The top three

**1. CheckoutKit (46).** It wins not because it is the deepest problem but because it is the cleanest trade in the set: the smallest build, the shortest learning curve, the most abundant test data (every firm has old checkout sheets), and evidence that is first-person and unambiguous. Point-to-point checkout happens on every job, thousands of times per building, currently on paper, and the specification-mandated signature is demonstrably not correlated with a working system — a consultant reporting "more than 50 controls items operating incorrectly" in a building certified 100% point-to-point is the single most damning fact found this cycle. Its weakest score is differentiation: KORE PointCheck exists, and the Cx platforms overlap. The answer is buyer and price — those products are sold to commissioning agents and enterprises, while the 15-person integrator uses paper. A free, offline, generated-from-the-points-list tool is a different product for a party the incumbents do not court. It is also the strategic wedge: it forces the firm to have a clean points list, which is what makes A, B and D valuable.

**2. PointList Reconciler (44).** The highest-severity, best-differentiated concept. Three divergent versions of the same document exist on every retrofit; the specification requires a signed reconciliation; and nobody sells a reconciler. It scores 5 on differentiation because the search turned up estimating tools, checkout tools, Cx platforms and analytics platforms — and nothing that diffs a specified list against a submitted list against a discovered list. It also sells to three parties in one transaction (integrator, owner's rep, Cx agent), which is unusual. It loses points only on build effort (column mapping and fuzzy matching are fiddly) and on evidence confidence, since the pain is documented indirectly — through the *requirement* for a signed verified list and the *warning* that ~10% of points hide in the sequence text — rather than through a practitioner saying "this reconciliation takes me six hours."

**3. AsFound (43).** The largest dollar consequence — it sits on the estimate, and Mordor's numbers (integration = 20–80% of retrofit budget, occupied-building phasing = +25–40%, labour = 50–75% of cost) mean survey error converts straight to margin loss. It also generates the input every other tool in the set consumes, which makes it the natural centre of a suite. It ranks third only because it is a bigger build than CheckoutKit and competes with a crowded generic form-app market; its defence is the output shape (points list + licence count + gap report), not the capture.

NameForge ties AsFound at 43 on strictly stronger evidence — the 16-hours-to-15-minutes datum and the "inconsistent naming prevents everything" statement are both first-person from a working engineer — but scores lower on ROI clarity because the beneficiary is downstream and diffuse.

### What to investigate next

**Investigate the PointList Reconciler next**, ahead of building anything. It is the highest-severity, best-differentiated concept, but it rests on the thinnest direct practitioner testimony — everything supporting it is a specification requirement or an expert warning rather than someone describing their afternoon. Two or three practitioner conversations would either confirm a several-hour recurring manual task (in which case it becomes the flagship) or reveal that firms simply skip the reconciliation and absorb the change orders (in which case it becomes a much harder sell and CheckoutKit should absorb the effort).

Build order, if the validation holds: **CheckoutKit first** (fastest to useful, easiest adoption, generates the relationship), **Reconciler second** (highest differentiation, upstream of CheckoutKit's input), **AsFound third** (largest build, completes the chain and becomes the suite's front door). Treat A→B→C→D as one data model with four entry points rather than four products — the shared artifact is a normalized point record with identity, location, type and provenance.

---

## 6. Validation plan

### Questions to ask practitioners

*On the survey (A):* Walk me through the last retrofit you priced. How long between the site walk and a number? How many hours of transcription? How many times in the last two years did something you did not see on the walk turn into a change order — and what was it? Do you use a standard survey form, and who wrote it?

*On the points list (B):* Who produces the points list for a retrofit, and from what? When the owner's rep signs the final list, what did you actually do to verify it? Have you ever discovered at commissioning that a specified point was never installed — how did you find out? How many revisions does the list go through, and how do you know what changed between revisions?

*On checkout (C):* Paper, PDF or tablet? Who re-types the results, and how long does that take? Has a Cx agent ever found points you had signed off? What percentage of points do you actually test on a typical job, honestly?

*On naming (D):* On your last multi-vendor retrofit, how did you decide the naming convention, and how long did renaming take? Do you have a written standard? Has an owner ever rejected your naming?

*On sequences (E):* For a G36 job, how do you satisfy yourself that what you programmed matches what was specified? Do you trend and review, or override and observe? What do you do with the trend CSVs today? (California specifically: what changed for you after 1 Jan 2026?)

*Cross-cutting:* What is the single most tedious hour of a retrofit project for you? What have you built in Excel that you would be embarrassed to show me?

### Who to interview

- Owner/lead engineer at 3–5 independent Niagara integrators in the 10–50 employee range (reachable via Tridium/Niagara distributor networks — Cochrane Supply, Stromquist — and the Niagara Community forum).
- Two campus/health-system controls managers who publish a Division 25 standard (universities are unusually accessible and their standards are public — UConn, Oregon State, Texas A&M, U Toronto all publish).
- Two independent commissioning agents (BCxA or ACG member directories) — they see the failure modes and are a second buyer for B, C and E.
- One outsourced BAS graphics vendor (QA Graphics, BASGFX) — they see many integrators' data hygiene and would validate or kill H.
- One controls estimator specifically, separate from the engineers.

### Search terms for further research

`"points list" site:*.edu "division 25"` · `BAS "point to point" checkout template xlsx` · `Niagara BQL rename points batch` · `"as-found" controls survey form site:*.gov` · `Guideline 36 "functional test" procedure VAV` · `BACnet discovery export csv "object name"` · `controls retrofit change order "existing conditions"` · Niagara Community forum, HVAC-Talk BAS subforum, r/BuildingAutomation, ControlTrends, AutomatedBuildings archives, Smart Buildings Academy podcast back catalogue.

### Sample files and data needed

1. Three real points lists from the same project at different stages (spec / submittal / as-built) — the single most valuable artifact; without it the Reconciler cannot be designed.
2. A discovered-point CSV export from Niagara (or Metasys/Desigo) for a mixed-vendor building — for NameForge and LicenseSizer.
3. Two completed paper P2P checkout packages — for CheckoutKit's output format.
4. Two weeks of one-minute AHU trend data with a written sequence of operations — for TrendAssert.
5. Two or three published Division 25 specifications — already obtainable free; seed the TurnoverPack profiles from them.

### Simple prototypes that would validate

- **CheckoutKit:** a single-file offline HTML page that imports a points list CSV and produces test records, coverage percentage and a printable package. One weekend. Hand it to one technician on one job; the validation signal is whether they use it for the second panel without being asked.
- **Reconciler:** a Python script that takes two CSVs and emits the four-bucket exception report. Run it on one real project's spec-vs-submittal lists in front of a project engineer. The signal is whether the exceptions are news to them.
- **TrendAssert:** three hard-coded assertions (economizer high-limit, simultaneous heat/cool, commanded-vs-actual disagreement) run against one real trend export. The signal is whether any finding is something they did not already know.

### Assumptions most likely to make these fail

1. **That integrators will change field behaviour at all.** The binding constraint is that the people who would use these tools are billable and busy. A tool that requires setup during a project will not be adopted, no matter how good.
2. **That points lists exist in tabular electronic form.** If the specified list arrives only as a PDF table inside a spec, the Reconciler's ingestion problem is bigger than its logic problem.
3. **That the firm's problem is time rather than pricing power.** If retrofit margin is set by competitive bidding rather than by internal efficiency, saving eight hours may simply lower the next bid rather than raise profit — which changes the sales argument from ROI to risk reduction.
4. **That "signed 100% P2P with 50 broken items" is common rather than one consultant's bad luck.** This single observation carries a lot of weight in the ranking and needs at least two more independent confirmations.
5. **That the free-and-open-source base version reaches these buyers.** This trade does not shop on GitHub. Distribution runs through distributors, the Niagara Community, trade press and podcasts — an unusual go-to-market that must be planned, not assumed.
6. **That Title 24's G36 adoption actually increases verification demand** rather than being absorbed by manufacturers shipping pre-certified G36 application libraries, which would shrink TrendAssert's market to the buildings where those libraries are misapplied.

---

## 7. Cross-industry patterns

**Pattern 1 — "Generate the field checklist from the equipment list, complete it offline, and let coverage be computed rather than asserted."** The defect this kills is a signature that outruns the work. Transfers to: **Test, adjust and balance (TAB) contractors**; **Commissioning (Cx) providers for small and midsize buildings**; **Backflow prevention assembly testers and cross-connection control programs**; **Fire door inspection providers under NFPA 80**; **Fire pump service, testing and repair specialists**; **Special inspection agency** work; **Calibration and metrology service providers**.

**Pattern 2 — "Three-way reconciliation: what was specified vs what was submitted vs what was actually installed."** Wherever a document is signed as verified but the verification is done by scrolling. Transfers to: **Delegated-design submittal coordination**; **Federal construction contractors on NAVFAC/USACE projects (UFGS submittal register)**; **Equipment manufacturer and manufacturer-rep submittal desks**; **Aerospace supplier quality clause library administration**; **Industrial distributors and metal service centers issuing material test reports**.

**Pattern 3 — "Name normalization against an owner standard, delivered as a reversible plan with an audit trail rather than an executed change."** The insight is that the *plan* is safer and more sellable than the *execution*. Transfers to: **Environmental laboratories producing regulator EDD deliverables (EQuIS and state formats)**; **Freight bill audit and payment for small shippers**; **E-commerce accounting specialists (Amazon/Shopify/Stripe settlement reconciliation)**; **Provider credentialing and payer enrollment services**.

**Pattern 4 — "Capacity/licence sizing computed from a component inventory, with headroom warnings before the tier boundary."** Transfers to: **Fire alarm system design and programming subcontractors** (battery/standby and voltage-drop calculations); **Special hazard / clean agent suppression design** (agent quantity and enclosure integrity); **Electrical or plumbing trade subcontractor field operations**; **Pipe and duct fabrication shops** (nesting/capacity).

**Pattern 5 — "Assertion checking of exported telemetry against a written specification, ranked by hours-in-violation."** The general form is: the spec is prose, the evidence is a CSV, and nobody joins them. Transfers to: **Test, adjust and balance (TAB) contractors** (measured vs design airflow against NEBB/AABC tolerance); **Title 24 acceptance test technicians (ATT)**; **Utility energy-efficiency program implementers and trade-ally rebate documentation**; **Commissioning (Cx) providers**; **Owner-side facilities engineering: end-of-life equipment replacement planning**.

**Pattern 6 — "As-found field survey structured as a tree, producing a priced scope rather than a PDF."** Transfers to: **Building envelope and roofing consultants performing field water testing**; **Electrical or plumbing trade subcontractor field operations**; **Owner-side facilities engineering**; **Geotechnical drilling subcontractors**; **Independent heavy-truck repair shops serving outside fleet customers**.

**Pattern 7 — "Closeout completeness checked against a machine-readable profile of the owner's own published standard."** Public owner standards (universities, states, federal agencies) are free, stable and enumerable — which makes the profile library a compounding asset. Transfers to: **Construction subcontractor project management at 15–150 employee specialty trades**; **Federal construction contractors on NAVFAC/USACE projects**; **Architectural construction administration (CA) desks at small A/E firms**; **Nonprofit grant management** (closeout reporting).

---

## 8. Sources and confidence

### Verified findings — stated directly by a primary or first-person source

| Finding | Source |
|---|---|
| Site-walk methodology: tablet/data collection sheets, structured categories, record controller family/model/firmware, protocol per trunk, devices per segment vs best-practice limits | [AutomatedBuildings — How to Perform a Site Walk That Actually Sells BAS Retrofits (Dec 2025)](https://www.automatedbuildings.com/2025/12/how-to-perform-a-site-walk-that-actually-sells-bas-retrofits-and-planned-service-agreements/) |
| Batch operations turned "a tedious, 16-hour task" into "just 10-15 minutes"; tasks include mass renaming, history extensions, alarm slots | [BAS Briefing — Niagara Batch Editor](https://basbriefing.substack.com/p/niagara-batch-editor) |
| "Siemens uses CTL_TEMP, JCI uses ZN-T"; "inconsistent naming will prevent us from using auto-tags, using the batch editor, re-using graphics, using BQL to collect data" | [BAS Briefing — Niagara Best Practices](https://basbriefing.substack.com/p/niagara-best-practices) |
| "More than 50 controls items operating incorrectly" in a building verified 100% point-to-point; 3 of 10 sampled rooms not operating as commanded | [CFMS Consulting — Sampling vs 100% Point-to-Point Verification](https://www.cfms.ca/blog/commissioning-controls-systems-sampling-vs-100-point-to-point-verification/) |
| P2P checkout paperwork: P2P Checkout Template, Trunk/Controller Checklists, Input/Output cheat sheets; per-point wiring, polarity, calibration; controller addressing and firmware | [Stromquist — BAS Startup and Checkout](https://www.stromquist.com/customer/docs/bam/BAS%20Startup%20and%20Checkout%20v1.pdf) |
| Checkout practice: label each point immediately, test every sensor individually, never assume similar points behave identically | [Smart Buildings Academy ep. 519](https://podcast.smartbuildingsacademy.com/519) |
| Estimating is a device takeoff from specs and drawings; scope gaps between trades are the costly oversight | [Smart Buildings Academy ep. 490](https://podcast.smartbuildingsacademy.com/490) |
| "The final points list shall be verified by the Control Contractor, the Owner's Representative, and signed by both parties"; P2P checkout of **all** newly installed points | [Oregon State Section 230900 BAS Controls](https://bid.oregonstate.edu/opportunity/viewFile/48222/230900%20Building%20Automation%20System%20(BAS)%20Controls.pdf) |
| Submittal must contain descriptive point lists, program listings, alarm lists, P2P checkout records; graphics at 50/75/90%; database + graphics source files at turnover; 48-hour occupancy-sensor trends | [UConn Appendix V — Building Automation Standards](https://updc.uconn.edu/wp-content/uploads/sites/1525/2016/04/Appendix_V_Building_Automation_Standards_May2015.pdf) |
| Points list contents and the warning that a comprehensive list still gives only "upwards of 90 percent of what is required" | [AutomatedBuildings — Points List Primer](https://www.automatedbuildings.com/news/may09/columns/090415012333calabrese.htm) |
| "Control programmers still need to convert this text into computer language… and adapt it to the BAS point naming conventions"; "the higher complexity of ASHRAE G36 exposes the system to more errors" | [CalNEXT — ASHRAE Guideline 36 Open-Source Supervisory Control, Final Report (Nov 2025)](https://calnext.com/wp-content/uploads/2025/11/ET22SWE0039_ASHRAE-Guideline-36-Open-Source-Supervisory-Control-Technology-Development-and-Demonstration_Final-Report.pdf) |
| Sequence verification requires trended I/O at 5–60 s and JSON point mappings with unit conversion; "automated verification requires development of tools for matching BAS objects to CDL specifications, presenting significant implementation overhead" | [LBNL OpenBuildingControl §12 Verification](https://obc.lbl.gov/specification/verification.html) |
| Niagara licensing: device tiers; 50 points = 1 device; point counts affect scalability and design | [Stromquist — Niagara JACE Licensing Explained](https://www.stromquist.com/blog/11117/blog-niagara-jace-licensing-explained-device-limits-points-and-sma-made-simple) |
| N2 modernization requires per-family footprint, wiring and point comparison tables plus logic and supervisor reconfiguration; Zone Bus / XT Bus not supported on replacements | [JCI — Modernization Guide for N2 Controllers](https://docs.johnsoncontrols.com/bas/r/Metasys/en-US/Modernization-Guide-for-N2-Controllers-Metasys/12.0) |
| Technicians "drawn into graphics tasks that pull them away from programming, startup, service"; style inconsistency; outsourcing 100% of floor-plan services | [AutomatedBuildings — A Growing Integrator's Path to Scaling BAS Floor Plans and Graphics (June 2026)](https://www.automatedbuildings.com/2026/06/a-growing-integrators-path-to-scaling-bas-floor-plans-and-graphics/) |
| Network faults "can often take a minimum of four hours to uncover"; systems consume more energy within five years absent re-adaptation | [AutomatedBuildings — When Building Automation Fails to Deliver](https://www.automatedbuildings.com/news/may14/articles/denning/140423012707denning.html) |
| Legacy Metasys phased migration 5–7 years; $3,000–$8,000/controller Metasys, $2,000–$5,000 open BACnet, $50k–$140k integration layer; inventory is step 1 | [Controls.nyc — Metasys: Upgrade or Integrate?](https://controls.nyc/blog/johnson-controls-metasys-upgrade-integrate/) |
| Labour is 50–75% of BAS project cost (NREL); installed $2.50–$7.00/sq ft; commissioning 10–20% of installed cost | [FractionalBAS — BAS Cost Breakdown](https://fractionalbas.com/guides/bas-cost-breakdown/) |
| ~70% of US office space predates 2000 | [AutomatedBuildings — Five Global Trends Reshaping Building Automation: Retrofitting (June 2026)](https://www.automatedbuildings.com/2026/06/five-global-trends-reshaping-building-automation-retrofitting/) |
| EMIS/FDD deployment costs ($0.03/sq ft median setup; $0.05/sq ft FDD); "significantly more work is required to integrate BAS data into FDD software… a variety of points must be mapped" | [LBNL — Building Analytics and Monitoring-Based Commissioning (Kramer)](https://eta-publications.lbl.gov/sites/default/files/building_analytics_-_kramer.pdf) |

### Strong inferences — well supported but assembled across sources or from analyst material

- **US commercial building automation at $21.23B (2025) → $22.53B (2026), 6.12% CAGR; 3–5 discrete control systems per typical property; integration = 20–80% of retrofit budgets; occupied-building phasing +25–40%; 25% technician shortfall; commissioning labour $80–120/hr.** ([Mordor Intelligence](https://www.mordorintelligence.com/industry-reports/united-states-commercial-building-automation-market)) — vendor-analyst data, directionally credible and internally consistent with the practitioner sources, but not independently verifiable.
- **2025 California Energy Code §140.4 adopts ASHRAE Guideline 36 for VAV systems, economizers, SAT reset and DDC controller logic, implementation date 1 January 2026, applying to new or replacement systems rather than repairs.** ([Schnackel Engineers overview of 2025 Title 24 Part 6 changes](https://schnackel.com/wp-content/uploads/2025/06/Overview-of-2025-Title-24-Part-6-Changes_Update.pdf); see also [CEC Blueprint 151, Fall 2025](https://www.energy.ca.gov/sites/default/files/2025-11/CEC-400-2025-015.pdf)) — confirmed through a competent secondary summary; **the code text itself should be read before this is relied on commercially**, and note that the "replacement not repair" applicability limit meaningfully narrows which retrofits are captured.
- **Point-to-point checkout automation is a recognised, patent-attracting problem** — multiple filings exist on point-to-point checkout automation and points-list tooling, and a commercial product ([KORE PointCheck](https://koretrax.com/pointcheck.html)) targets exactly this. That validates demand and simultaneously caps the differentiation score for CheckoutKit.
- **Retrofit demand is being pulled forward by building performance standards** (NYC Local Law 87's 10-year audit + retro-commissioning cycle and the widening US BPS map — [Facilities Dive 2026 BPS map](https://www.facilitiesdive.com/news/map-tracking-building-performance-standards-across-the-us/743214/)). The link from BPS to *controls retrofit specifically* is inference, not a measured share.
- **A generic-form-app market exists and does not serve this need** (GoCanvas HVAC survey forms, SiteCapture, ArcSite). Their existence is verified; the claim that integrators find them insufficient is inference from the output-shape argument.
- **BAS estimating tooling exists but is takeoff-centric, not retrofit-survey-centric** ([PataBid](https://www.patabid.com/building-automation-estimating-software), [McCormick ABS](https://www.mccormicksys.com/industries/automated-building-systems/)) — both work from drawings, which is precisely what a retrofit lacks.

### Tentative hypotheses requiring practitioner validation

1. **That transcription of a site survey costs 4–12 hours per building.** Derived from the described method, not measured. This is the load-bearing number for AsFound's ROI and must be measured before anything is built.
2. **That the three-version points-list divergence is experienced as a painful recurring task rather than silently absorbed.** The requirement to reconcile is documented; the *felt cost* is not. This is the single most important thing to test, and it is why the Reconciler is nominated for investigation rather than construction.
3. **That "signed 100% P2P over a broken building" generalises.** One consultant, two anecdotes. Needs at least two independent confirmations before it carries the weight the ranking gives it.
4. **That firms will adopt free open-source tooling distributed outside their normal channels.** No evidence either way was found. This is a go-to-market hypothesis, not a product one, and it applies to every concept equally.
5. **That the outsourced-graphics vendors would tolerate rather than resist GraphicsBind.** They may be the natural distribution partner, or the incumbent it threatens — unknown.
6. **That per-vendor export formats are stable enough to build against.** NameForge, LicenseSizer and GraphicsBind all assume a parseable CSV export exists and does not change every release. Verified for Niagara; assumed elsewhere.
7. **That the sequence-verification market is not about to be absorbed by manufacturers shipping certified G36 libraries.** If it is, TrendAssert's addressable problem shrinks to misapplication cases.

---

*Report produced 2026-08-08 · claim `d306b04c` · market: building automation and controls contractors (BAS integrators) for existing-building retrofits · angle: narrow-subspecialty (legacy-to-open controls modernization engineering).*
