# Land Surveying Firms — Core Practitioner Workflow

**Market research cycle · 3 August 2026**

---

## 0. Cycle header

| | |
|---|---|
| **Market claimed** | Land surveying firms |
| **Angle claimed** | core-practitioner-workflow |
| **Claim ID** | `2095f105` |
| **Date** | 2026-08-03 |
| **Backlog remaining after this cycle** | 108 assignments (109 at time of claim, minus one concurrent claim) |

### Why this assignment over the others available

At the time of claiming, the ledger held one completed entry (Immigration law practice / core-practitioner-workflow) and 110 open assignments. One concurrent run had already claimed Fire protection / core-practitioner-workflow.

I selected **Land surveying firms / core-practitioner-workflow** on three grounds, applied in the order the brief specifies:

1. **Zero prior coverage.** Every market except immigration law had zero completed entries, so criterion (a) did not discriminate. It did, however, eliminate immigration law and the fire-protection slot already taken.
2. **Density of primary practitioner evidence.** This was the deciding factor. Land surveying has an unusually well-preserved, publicly readable practitioner record: RPLS.com / SurveyorConnect carries decades of threads authored by named licensed surveyors with four-figure post counts, state societies publish conference handouts as open PDFs, and county surveyor offices publish their actual review checklists. Compare this to, say, freight brokerage or staffing, where most practitioner discussion sits behind LinkedIn or private Slack communities. A market I can evidence is worth more to this catalog than a market I can only theorize about.
3. **Structural fit with the catalog thesis.** Small survey firms are document-heavy, deadline-regulated, and demonstrably priced out of their own incumbent software (Section 3, Problem 8). They are also the exact profile — 3 to 30 staff, one or two licensees, no IT department — that enterprise vendors do not serve. That is the catalog's target.

A secondary consideration: **the 2026 ALTA/NSPS standards took effect 23 February 2026**, less than six months ago, and renumbered Table A. Several opportunities below are timely in a way they would not have been last year or will not be in three years. Researching this market now captures that.

### Honest limitation on evidence gathering

**reddit.com was unreachable from this environment** (egress proxy returned 403 on every attempt; the search index returned no reddit URLs across ~10 targeted queries). r/Surveying was the single highest-value target in the research plan and it was **not** mined. The forum evidence below comes from RPLS.com, Land Surveyors United, state society publications, trade press, live job postings, and primary regulatory sources — which is a substantial body, but a re-run on an unblocked network would materially strengthen Section 3. This gap is flagged again in Section 8.

---

## 1. Market examined

**Industry.** Surveying and mapping services (NAICS 541370). IBISWorld counts **17,511 US businesses in the industry as of 2025**, up 0.9% year over year. ([IBISWorld](https://www.ibisworld.com/united-states/number-of-businesses/surveying-mapping-services/1407))

**Target organization size.** Firms of roughly **3 to 30 staff**. Below three, the owner is the entire firm and buys almost no software. Above roughly 30, firms begin to acquire Deltek Vantagepoint or Ajera and a person whose job is systems, at which point a focused free tool competes against an internal standard rather than against a spreadsheet. The 3–30 band is where firm-specific logic lives in one person's head, one person's LISP routines, and one person's Excel workbook.

**Roles inside that firm.**

| Role | What they do | Software they touch daily |
|---|---|---|
| **Owner / PLS (Professional Land Surveyor)** | Boundary resolution, sealing, scope negotiation, liability ownership. Frequently also the rainmaker and the QC reviewer. | CAD, PDF, email, Excel |
| **Survey project manager** | Proposals, schedules, client and title-company communication, plat review comment resolution. Often a PLS. | TBC, Civil 3D, ArcGIS, Excel, Access |
| **Survey / CAD technician** | Deed plotting, base map compilation, field data reduction, drafting to CAD standard, QC of deliverables. | Civil 3D or Carlson, Excel |
| **Party chief / crew chief** | Field data collection, field notes, cross-referencing plans and deeds on site, reducing raw data. | Data collector (Trimble Access, FieldGenius, Carlson SurvCE), spreadsheets |
| **Field crew / rodperson** | Instrument and GNSS operation, monument recovery | Data collector |

These role definitions are drawn from live August 2026 job postings, not from generic description. Bohler's Senior Survey Technician posting (Nashville, $55,970–$81,651) lists **"Perform deed plotting, base map compilation, and data verification"** as a named duty. Astra Surveying's Survey CAD Technician posting lists **"Import and export field and GIS data in various formats (.txt, .csv, .dgn, .shp, .xml, .gml, .kml, etc.)"**, **"Draft and review legal descriptions"**, and **"Organize digital files, manage project data, and support archiving and revision control."** Rauch's CAD Technician posting (Easton MD, $52k–$80k) requires **"Proficiency in AutoCAD, Civil 3D, Carlson, and Excel"** — Excel listed as a peer of CAD, not an afterthought.

**Demographic pressure.** Land Surveyors United reports the average age of a licensed US surveyor **"hovers around 58"** and that **"for every new surveyor entering the field, two or three are preparing to retire."** ([Vanishing Lines](https://landsurveyorsunited.com/articles/vanishing-lines-confronting-the-surveying-workforce-shortage)) This is context, not a pain point in itself, but it changes the economics of every opportunity below: a firm that cannot hire a third technician has a stronger reason to buy a tool that makes the second one 20% faster.

---

## 2. How the work is performed

The following is the general boundary/ALTA production sequence at a small firm. Durations are given only where a practitioner stated them.

### 2.1 Intake and proposal

Client (attorney, title company, developer, homeowner, lender) requests a survey. For an ALTA/NSPS Land Title Survey the client must specify desired **Table A** optional items **in writing**, and the standards state that **"the exact wording of and fee for any selected item may be negotiated between the surveyor and client."** ([2026 ALTA/NSPS standards, official PDF](https://cdn.ymaws.com/nsps.us.com/resource/resmgr/alta_standards/2026_OFFICIAL_FINAL_PDF_ALTA.pdf))

Proposals are typically produced in Excel and retyped into a Word or PDF proposal. Pricing is judgment-driven and highly variable; RPLS practitioners give ranges from **"The simplest boundary I can envision will cost you $800"** to a mid-Atlantic ALTA **"ball park the job at $10K."** ([RPLS pricing spectrum](https://rpls.com/forums/strictly-surveying/how-it-goes-the-surveying-business-spectrum/), [RPLS ALTA pricing](https://rpls.com/forums/strictly-surveying/alta-pricing/paged/2/))

### 2.2 Records research

The surveyor gathers the subject deed, adjoiner deeds, recorded plats, prior surveys, easements, and — for ALTA work — the title commitment with its Schedule B-II exceptions and supporting documents. Under the **2026** standards the surveyor must be furnished complete copies of the most recent title commitment, and the prior expectation that the title insurer supply adjoiner deeds **was removed** — the surveyor now obtains them. ([Benesch](https://www.beneschlaw.com/insight/alta-nsps-key-changes-and-updates-in-the-2026-standards/))

Documents come out of county recorder portals as scanned PDFs, frequently with machine-generated filenames. Practitioner detail on how bad this is: an ALTA title packet described as **"an effort to reach some minimum requirement and not a thoroughly researched set of documents"** with file names like **`1009737#$%773.pdf`**. ([RPLS deed history thread](https://rpls.com/forums/discussion/deed-history-jr-sr-rights/))

Research depth varies enormously. One Massachusetts PLS ran grantor/grantee searches **"from the 1790's to the present day"** and **"spent three days in the registry"** for a single church survey. A New Jersey PLS outsources to professional title searchers whenever a search will exceed **"more than an hour or two of billable time."** ([same thread](https://rpls.com/forums/discussion/deed-history-jr-sr-rights/))

### 2.3 Deed plotting and record mosaic

Every relevant deed and plat is keyed into COGO and assembled into a composite. Three separate practitioners describe independently invented versions of the same system:

- **GaryG**: *"I actually plot every deed, and put them together in a mosaic. That includes the record plats. All computed and put together like a puzzle."*
- **murphy**: renames each PDF by hand to a deed key such as `3 Smith to Jones 1.4ac 2016 DB-543_Pg-235`, then sketches each deed in CAD on its own colored layer so **"any reasonably intelligent PLS [can] pick up my work."**
- **BStrand**: builds a `0-Record` layer of all deeds, imports field data, then copies and rotates record groups onto found monuments to test fit before building `0-Measured` linework.
- **WA-ID Surveyor**: maintains a per-drawing database of **"each and every deed, survey, plat"** foldered by township/range/section to avoid re-researching the same parcels.

([RPLS boundary research procedure](https://rpls.com/forums/strictly-surveying/boundary-survey-research-procedure/))

The technicians who do this do not enjoy it. From the Deed Reader Pro vendor forum (discount for vendor context, but the speaker is a practicing surveyor): **"Our technicians do most of the deed plots, but it isn't anyone's favorite part of the job."** ([RPLS](https://rpls.com/forums/deed-reader-pro/deed-reader-pro-plot-deeds-in-seconds/))

### 2.4 Field work

Crew recovers monuments, ties improvements, runs control, collects topography. Data is coded in the field using a **field-to-finish (F2F) code table** so that linework draws automatically in the office. Party chiefs **"verify field calculations, maintain detailed and accurate field notes, and cross-reference plans and deeds on-site"** (Bartram Trail Surveying posting, small Florida firm, Trimble SX12/S5/TSC7).

For an ALTA survey a practitioner estimate is **"3-5 days in the field and at least an equal amount of time in the office."** ([RPLS ALTA pricing](https://rpls.com/forums/strictly-surveying/alta-pricing/paged/2/))

### 2.5 Data reduction and adjustment

Raw data (`.rw5`, `.dc`, `.job`, `.fbk`) is imported, checked, and — for control networks — least-squares adjusted, typically in **STAR\*NET** (~$2,855, [MicroSurvey store](https://store.microsurvey.com/products/microsurvey-star-net)) or **Trimble Business Center**. The dominant real-world pattern is **hybrid**: process and adjust in TBC or STAR\*NET, **export a PNEZD coordinate file, and re-import into Carlson or Civil 3D to draft**. A practitioner states it directly: *"After adjustment, I exported a coordinate file for import into Carlson to complete drafting."* ([RPLS TBC thread](https://rpls.com/forums/software-cad-mapping/trimble-business-center-tbc-questions/))

### 2.6 Boundary resolution

The licensee weighs found monuments against record calls and decides where the lines are. This is the irreducibly professional act — the thing the seal is for. Practitioner framing of where the difficulty actually sits: *"The math part of metes and bounds is easy. Where I struggle is when the math doesn't work, and you have to go further back in the chain of title."* ([RPLS](https://rpls.com/forums/strictly-surveying/boundary-survey-research-procedure/))

### 2.7 Drafting and deliverable production

CAD technician produces the plat, map, or Record of Survey to the firm's CAD standard and the jurisdiction's requirements. Legal descriptions are written — and surveyors insist on writing them themselves: *"I write legal descriptions that are sometimes used in deeds. I insist on writing the descriptions from my work... Have seen far too many descriptions screwed up by the attorneys to leave my clients at their mercy."* ([RPLS legal descriptions](https://rpls.com/forums/strictly-surveying/legal-descriptions/))

### 2.8 QC, review, and revision

Internal QC, then delivery of a draft to client / title company / lender for comment, then revision, then seal. For recorded documents there is a second, statutory review loop with the county (Section 3, Problem 5).

### 2.9 The economics of the whole thing

This is the most quantified finding in the research, from an RPLS thread explicitly about office-to-field ratios:

- **chris-bouffard** (1,491 posts): *"for every hour spent in the field, 2.5 hours will be spent in the office between my time to prepare a proposal, set up the research for the job, resolve the boundary and passing it on to drafting, then there the QA/QC process."*
- **Norman_Oklahoma** (8,384 posts): baseline of *"an hour of office time for every hour of field"*, which *"can easily vary by a factor of 2 in either direction."*
- **jimcox** (2,107 posts): *"One place I worked was one hour drafting for every four in the field"* — but only with a good basemap and heavy field-to-finish coding, where drafting reduced to *removing extraneous data, formatting text, adding linework.*

([RPLS: How long does it take?](https://rpls.com/forums/software-cad-mapping/how-long-does-it-take/))

And from a separate thread on the working day: **thebionicman**: *"90 plus percent of my time is office."* ([RPLS average work day](https://rpls.com/forums/strictly-surveying/average-work-day/))

**The single most important structural fact about this market: office hours dominate field hours by somewhere between 1:1 and 2.5:1, and the office hours are where the manual, repetitive, judgment-light work lives.** Every opportunity in Section 4 attacks office hours.

### 2.10 Software actually in use, and what it costs

| Tool | Role | Cost (2026) |
|---|---|---|
| Autodesk Civil 3D | Drafting, surfaces, survey database | **$2,730/yr**, subscription only; perpetual discontinued |
| AutoCAD / AutoCAD LT | Drafting | $2,310/yr / $500/yr |
| Carlson Survey | Survey-first CAD, COGO, F2F, description writer | ~**$3,450 perpetual** (OEM), maintenance 10% of list/yr, **+10% penalty per lapsed year** |
| MicroSurvey STAR\*NET | Least-squares network adjustment | **$2,855** perpetual |
| Trimble Business Center | GNSS/TS processing | No public pricing; practitioners quote **~$3,000**, subscription-only from 2026 |
| Trimble Access | Field data collection | **$1,540/user/yr** |
| Bentley OpenRoads | DOT work | **$7,226/yr** practitioner license |
| Metes and Bounds (Sandy Knoll) | Deed plotting | **$39.95 / $79.95** |
| Bluebeam Revu | PDF markup | $260–$590/user/yr |
| BricsCAD Pro | AutoCAD alternative, LISP-capable | ~$800/yr, **perpetual available** |

Sources: [Autodesk 2026 pricing](https://autodesksaudits.com/blog/autodesk-subscription-pricing-2026/), [That CAD Girl / Carlson licensing](https://thatcadgirl.com/faq/what-to-know-about-purchasing-carlson-software/), [Carlson maintenance](https://www.carlsonsurveysupply.com/carlson-software-maintenance/), [MicroSurvey](https://store.microsurvey.com/products/microsurvey-star-net), [Trimble subscription plans](https://geospatial.trimble.com/en/products/software/trimble-business-center/subscription-plans), [NEI Trimble Access](https://neigps.com/shop/trimble-access-general-survey-1-year-subscription/), [Virtuosity](https://en.virtuosity.com/openroads-designer), [Sandy Knoll](https://www.tabberer.com/sandyknoll/more/metesandbounds/metes.html), [Bluebeam](https://www.bluebeam.com/pricing/), [Drafting Bench CAD comparison](https://draftingbench.com/autocad-vs-bricscad-vs-draftsight/)

Business-side software is bimodal. Deltek Ajera runs ~$200/user/month and BQE Core ~$40/user/month ([ITQlick](https://www.itqlick.com/compare/deltek-ajera/bqe-core)); the survey-specific Cyanic Job Book is $40/employee/month ([pricing](https://getjobbook.com/pricing)). What small firms **actually** use, per an RPLS project-management thread: Excel (*"personalize everything to my preference"*), **a dry erase board**, Google Calendar, Trello, and MS Project (*"a very powerful program but not easy to learn or use"*), with the recurring objection *"I really don't want to pay the monthly fees that seem to be the wave of things."* ([RPLS PM software](https://rpls.com/forums/strictly-surveying/project-management-software/))

---

## 3. Most important problems — ranked

### Problem 1 — Deed plotting and record mosaic assembly is manual, high-volume, and universally disliked

**Who.** Survey/CAD technicians primarily; PLS on complex chains. **When.** Every boundary and ALTA survey, at the front of the job. **Frequency.** Every project; multiple deeds per project (subject plus all adjoiners).

**How handled now.** Hand-keying metes-and-bounds calls into COGO; hand-renaming recorder PDFs; per-deed CAD layers; personal folder databases keyed to township/range/section. Outsourced to title searchers when it exceeds an hour or two of billable time.

**Why inadequate.** It consumes technician hours at a $56k–$82k salary level (Bohler posting) on work that is transcription, not judgment. It is error-prone at the point of transcription, and the error does not surface until closure is computed. And the resulting "database" is a personal filing convention that does not survive the person leaving — acute in a market where the average licensee is 58.

**Cost.** Not publicly quantified. Bounded inference: if deed research and plotting is even 10–20% of the 1:1-to-2.5:1 office ratio, a firm running 100 boundary jobs a year is spending on the order of several hundred technician hours annually on transcription.

**Evidence strength: high.** Named as a duty on live salaried job postings; three independent practitioner descriptions of homegrown systems; direct quote that it "isn't anyone's favorite part of the job"; and a visible 2024–2026 commercial wave built exclusively to solve it — [Deed Reader Pro](https://www.deedreaderpro.com/), [CADastral](https://cadastral.pro/), [ALTA-Plot](https://www.alta-plot.com/), [DeedPlotter AI](https://deedplotter.ai/), [Deed Pro](https://deedprosoftware.com/), free [MeteMap](https://metemap.com/). Six vendors do not appear in two years for an imaginary problem.

**Important caveat for anyone building here:** even the best current tool leaves substantial manual work. A Deed Reader Pro user reports snippet-based import means **"40% of deeds get recognized with zero additional input"** — meaning **60% still require manual intervention.** And a surveyor explains why OCR alone is insufficient: *"I have to enter the whole deed, and see what closes, to be sure."* ([RPLS](https://rpls.com/forums/deed-reader-pro/deed-reader-pro-plot-deeds-in-seconds/paged/2/))

---

### Problem 2 — Closure and traverse analysis of record descriptions is done with hand-rolled spreadsheet band-aids

**Who.** PLS and technicians. **When.** Immediately after deed plotting, and again when writing a new description. **Frequency.** Every deed, every description written.

**How handled now.** A practitioner describes his own workaround in detail: *"I've come up with a fairly quick adjustment method that is essentially a compass rule, but utilizes drafting methods and a spreadsheet because it's easier and more reliable than the PITA Auto desk traverse adjustment routines that never seem to work right anyway."* He then concedes: *"Admittedly, it is a 'band aid' work around."* The process is distances into a spreadsheet, running totals, ratios, scaled misclosure segments drawn in CAD, and manually snapped vertices. ([RPLS closure thread](https://rpls.com/forums/strictly-surveying/analyzing-older-deeds-closure-autodesk-land-desktop-3/))

Fallbacks named in the same thread: **Copan** (*"It's totally free... We use it a lot for what we call 'map traverses'"*) and **Wolfpack** (text-file-in, text-file-out compass rule from the Wolf & Ghilani textbook). On Land Surveyors United, a surveyor asked for a routine that would *"print out a closure sheet with any error check where the property did not close"*; the reply was *"I know the frustration you are having. So I developed my own software to assist in the use of autocad."* ([LSU](https://landsurveyorsunited.com/forum/topics/deed-map-closure-lisp-routine))

**Why inadequate.** The professional need is a defensible closure record, and it is being produced by an ad-hoc spreadsheet plus manual CAD manipulation. It is not auditable, not repeatable, and not attached to the file. The commercial ROI argument is stated by a practitioner himself: *"The time saved just highlighting the calls, or the time checking our own descriptions for closure would pay for a seat."*

**Cost.** Minutes per deed, dozens of deeds per year per technician — but the real exposure is a bad description going out the door. "Incorrect platting" and negligent misrepresentation on maps are named surveyor liability categories. ([Land Surveyor Liability white paper](https://www.lsacts.com/documents/Land%20Surveyor%20Liability%20V1.3%20final%20w%20appendixes.pdf))

**Evidence strength: high** (multiple independent practitioners describing homemade solutions to the same problem).

---

### Problem 3 — ALTA Schedule B-II exception handling is now a codified, per-exception compliance matrix, and every firm's templates just became obsolete

**Who.** PLS and PM. **When.** Every ALTA/NSPS Land Title Survey. **Frequency.** For firms doing commercial work, weekly to monthly.

**What changed.** The **2026 ALTA/NSPS Minimum Standard Detail Requirements took effect 23 February 2026**, superseding the 2021 version, and govern surveys *"commenced on or after that date."* ([ALTA](https://www.alta.org/news-and-publications/news/20251125-Key-Updates-to-the-2026-ALTANSPS-Land-Title-Survey-Standards), [McGuireWoods](https://www.mcguirewoods.com/client-resources/alerts/2026/2/updated-alta-nsps-land-title-survey-standards-take-effect-feb-23/))

Section **6.C.ii** now requires, for each right of way, easement, or survey-related matter, *"a statement indicating whether it lies within or crosses the surveyed property, and a related note for each of the following conditions, if present"* — an **eight-condition checklist**: location shown; location cannot be determined; no observed evidence; blanket easement; does not affect the property; limits access; illegible document; may have been released or terminated. ([official PDF](https://cdn.ymaws.com/nsps.us.com/resource/resmgr/alta_standards/2026_OFFICIAL_FINAL_PDF_ALTA.pdf), [NJSPLS SurvCon deck](https://cdn.ymaws.com/njspls.org/resource/resmgr/2026_survcon/_17__2026_alta-nsps_land_tit.pdf))

Separately, **Table A was renumbered**: 2021 had Items 1–19 with Item 20 as the client-negotiated catch-all; 2026 inserts a **new Item 20 (encroachment summary table)** and moves the catch-all to **Item 21**, subdivided 21(a), 21(b), etc., each of which *"must be explained"* on the plat. ([official PDF](https://cdn.ymaws.com/nsps.us.com/resource/resmgr/alta_standards/2026_OFFICIAL_FINAL_PDF_ALTA.pdf), [NJSPLS deck](https://cdn.ymaws.com/njspls.org/resource/resmgr/2026_survcon/_17__2026_alta-nsps_land_tit.pdf))

**How handled now.** Boilerplate note libraries and copy-paste. Practitioners on RPLS trade standard disclaimers — *"Not a matter of survey"*, *"Outside the purview of a Professional Land Surveyor"* — and the consensus practice is to **address every Schedule B item**, explicitly noting the ones outside survey expertise, *"to prevent clients from later asking if items were overlooked."* The same thread documents the recurring scope fight: title companies, lenders and attorneys frequently expect surveyors to review legal documents beyond their licensure, and some respondents suggest quoting **$500+/hour** specifically to discourage the requests. ([RPLS Schedule B thread](https://rpls.com/forums/discussion/addressing-a-title-committment-schedule-b))

The NV5 practitioner handbook describes the deliverable as a *"Summary of Easements in notation form addressing each recorded easement"* including **the reason if an easement cannot be plotted** — because the title company then relies on the surveyor to verify survey-related exceptions so they can be deleted from the policy. ([NV5 handbook](https://www.nv5.com/wp-content/uploads/2022/08/bc-handbook-alta-land-title-surveys.pdf))

**Why inadequate.** Every firm's note library, plat template, and Table A checklist PDF was written against the 2021 numbering. A boilerplate library that silently references "Table A Item 20" now means something different than it did in January. The eight-condition per-exception requirement is exactly the kind of completeness check humans miss on the twentieth exception of a forty-exception commitment.

**Cost.** A missed or mis-worded exception note is a title-policy problem, which is a claim. "Failure to identify encroachments in an as-built survey" is a documented liability case with cascading exposure. ([Point of Beginning](https://www.pobonline.com/articles/100693-traversing-the-law-surveyor-negligence-lawsuits))

**Evidence strength: high** (primary standards document, three independent law-firm analyses, a state society conference deck, a practitioner handbook, and a live forum thread). Note the dissenting read: Holland & Knight assesses the 2026 revisions as *not* materially expanding scope, cost, or timing in most transactions, while conceding surveys will carry *"more detailed... additional explanatory notes."* ([Holland & Knight](https://www.hklaw.com/en/insights/publications/2026/03/2026-alta-survey-standards-updates))

---

### Problem 4 — Table A scope is negotiated verbally and then disputed, and the standards' own authors call this out

**Who.** Owner/PLS. **When.** At proposal. **Frequency.** Every ALTA job.

**How handled now.** Verbal or email agreement, PDF checklists of varying vintage, and firm-specific fee sheets. The strongest practitioner statement in the research is an all-caps one: **"GIVE NO ESTIMATE UNTIL YOU HAVE A COMPLETED AND SIGNED TABLE A CHECKLIST!!"** — from the same surveyor who observes that *"An ALTA tries to put a TON of liability on your shoulders."* ([RPLS ALTA pricing](https://rpls.com/forums/strictly-surveying/alta-pricing/paged/2/))

**Why inadequate.** Table A items are not equal in cost or dependency and clients cannot be expected to know which are which:

- **Item 1** (monuments) adds **$500+** and may trigger a Record of Survey filing obligation in western states.
- **Items 6a/6b** (zoning) require the *client* to supply a zoning report, or the surveyor must add a disclaiming note.
- **Item 11** (utilities) is called *"common confusion"* because Section 5 already requires observed utility evidence.
- **Item 5** (contours) is *"one of the single largest cost drivers in Table A selection."*
- **Item 18** (appurtenant easements) extends the survey onto adjoining parcels, *"substantially increasing cost and timeline."*
- **Item 19** professional-liability limits above the industry-standard $1M *"may limit available surveyors or increase fees."*

([NV5 handbook](https://www.nv5.com/wp-content/uploads/2022/08/bc-handbook-alta-land-title-surveys.pdf), [Builoff Table A guide](https://www.builoff.com/blog-posts/how-to-choose-alta-table-a-items-cost-schedule-guide), [Partner ESI](https://www.partneresi.com/resources/articles/demystifying-alta-surveys-pro-tips-and-table-a-items/))

The buyer-side diagnosis is precise: *"The biggest mistake first-time ALTA buyers make isn't choosing the wrong items — it's choosing items without understanding what each one requires."* Some items are **prerequisite-dependent** (6, 11, 17 — schedule risk driven by third parties) and others are **scope-expanding** (1, 5, 18 — direct cost). ([Builoff](https://www.builoff.com/blog-posts/how-to-choose-alta-table-a-items-cost-schedule-guide))

Scope creep is named as an ongoing challenge by the standards work group itself, with the stated remedy being *"written contracts specifying scope, Table A items with qualifications, and names of certified parties."* ([NJSPLS deck](https://cdn.ymaws.com/njspls.org/resource/resmgr/2026_survcon/_17__2026_alta-nsps_land_tit.pdf)) A related recurring fee dispute: there is *"no such thing as an 'update'"* — a re-issued survey is a new survey under current standards. ([The American Surveyor](https://amerisurv.com/2026/02/01/the-2026-minimum-standard-detail-requirements-for-alta-nsps-land-title-surveys/))

**Cost.** Directly monetary. On a $10K ALTA, an un-agreed Item 5 or Item 18 is days of unbilled field and office work.

**Evidence strength: high**, and reinforced from an unexpected direction: the Victor professional-liability application for surveyors asks whether the firm *"engage[s] with your client to produce a documented scope of services and accuracy standards, such as those established by ALTA/ACSM surveys, which are incorporated into the written agreement."* ([Victor application](https://www.victorinsurance.com/content/dam/victor/victor2/documents/victor-us/architects-engineers/applications/US-architects-engineers-application-surveyors.pdf)) Carriers price this artifact. That is as strong a market signal as a practitioner complaint.

---

### Problem 5 — Recorded-map submittals get rejected on checklist items, on statutory clocks, and the clocks are short

**Who.** PLS (who signs) and the CAD technician (who fixes). **When.** After the map is drafted, at county submittal. **Frequency.** Every recordable map — Records of Survey, corner records, subdivision plats.

**The statutory clocks are real and tight:**

- **California**: a Record of Survey must be filed **within 90 days after setting boundary monuments or 90 days after completing the field survey, whichever occurs first**. ([BPC § 8762](https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=8762))
- **California**: a non-conforming ROS is returned *"together with a written statement of the changes necessary to make it conform"* and the surveyor must **resubmit within 60 days**. ([BPC § 8767](https://codes.findlaw.com/ca/business-and-professions-code/bpc-sect-8767/))
- **California**: a Corner Record is examined and either filed or returned **within 20 working days**; the surveyor then has **60 days** to resubmit; the county files within 10 working days. ([BPC § 8773.2](https://california.public.law/codes/business_and_professions_code_section_8773.2))
- **Washington**: Record of Survey must be filed with the county auditor *"within ninety days after the establishment, reestablishment, or restoration of a corner."* ([RCW 58.09](https://wa-law.org/rcw/58_boundaries_and_plats/58.09_surveys%E2%80%94recording.html))

**The checklists are published, granular, and different in every jurisdiction.** Placer County's Record of Survey Map Review Checklist contains roughly **40–45 discrete check items** across eight categories (legibility, mathematical accuracy, legend & references, statements, monuments, CCS83 basis of bearings, final, public entity surveys), citing Government Code 27383 and PRC 8813.3 / 8815.1 / 8815.5 and multiple subsections of 8764. Sample items include **"Text height minimum 0.10""**, "All bearings and distances shown", "Monuments found/set w/ desc. of kind/size/location/accessory", "Surveyor's Statement & date", and "Mylar sprayed with fixative." ([Placer County checklist](https://www.placer.ca.gov/DocumentCenter/View/3890/Record-of-Survey-Map-Review-Checklist-PDF)) Comparable published instruments exist for [San Diego County](https://www.sandiegocounty.gov/content/dam/sdc/dpw/COUNTY_SURVEYOR/survred.pdf), [Santa Barbara](http://surveyor.countyofsb.org/downloads/RS_2022.pdf), [Kern](https://www.kernpublicworks.com/services/development/surveying/record-of-survey-guidelines), and [Sonoma](https://permitsonoma.org/instructionsandforms/sur-003recordofsurveysubmittalrequirementschecklist).

**Comment volume is substantial.** A real second-submittal plat review packet (Adams County, Colorado, PLT2024-00007) contains roughly **60+ substantive comments across seven internal reviewers plus three external state agencies**. Surveyor-facing corrections included: correct legal descriptions to match the title commitment **verbatim**, fix ownership/dedication certificates and notary acknowledgments, put the case number on all sheets, fix a vicinity-map range designation, and replace handwritten with typed information. ([Adams County](https://adamscountyco.gov/wp-content/uploads/2025/08/PLT2024-00007-submittal2.pdf))

Some jurisdictions design multiple rounds in: Portland states *"Revision and resubmittal may be required"*, requires simultaneous submittal to the County Surveyor *"[because] revisions from that office may be needed"*, and voids applications without demonstrated progress every **180 days**. ([Portland.gov](https://www.portland.gov/ppd/zoning-land-use/land-use-review-fees-and-types/final-plat-reviews))

**Why inadequate.** The checklist exists as a PDF the technician is supposed to remember. Nothing checks the drawing against it before submittal. Rejection costs a review cycle — weeks — plus rework hours, and it burns the statutory clock.

**Cost.** Weeks of schedule per rejection cycle, plus rework. And the liability tail is explicit: **"non-compliance with Record of Survey filing requirements"** is named as a surveyor liability exposure category. ([Land Surveyor Liability white paper](https://www.lsacts.com/documents/Land%20Surveyor%20Liability%20V1.3%20final%20w%20appendixes.pdf))

**Evidence strength: high on the requirements** (primary statute and published county checklists). **Medium on frequency of rejection** — the Adams County packet is one real data point, not a national rate. The statutory existence of return-and-resubmit provisions in CA §§ 8767 and 8773.2 does, however, indicate the legislature expected the loop to be common.

---

### Problem 6 — Field-to-finish coding fails silently, and the firm's coding logic lives in un-versioned files

**Who.** CAD technicians and party chiefs. **When.** At data import, after every field day. **Frequency.** Daily to weekly.

**How handled now.** Debugging by hand. A representative thread: F2F *"created the point groups, but never generated the line work"* — traced to a configuration difference between a desktop and a new laptop, involving "Max Length for Linework", BEG/END codes in the Code Table, and a checkbox: *"verify that the box for 'Line' is checked in the 'Draw Field to Finish' window. Sometimes mine becomes unchecked."* ([RPLS F2F thread](https://rpls.com/forums/software-cad-mapping/carlson-f2f-not-generating-line-work/))

Curve coding produces geometry errors that a human has to eyeball: *"I've been mapping an island like this and it seems very, very clear where the PC and PT are, but cad draws it like this anyway"*, with the workaround *"going a few tenths into the curve seems to solve this issue"*; starting a curve in the wrong direction produces *"a big bubble underneath the gravel."* ([RPLS F2F tricks](https://rpls.com/forums/strictly-surveying/field-to-finish-tricks-n-tips/))

Duplicate points are a recurring, separately-threaded problem: *"now I have (2) points numbered 32949 on the same location"* — from re-running F2F with "not erase previous F2F entities" checked. The workarounds offered are all per-user settings and manual discipline: check "Erase Duplicates"; download each day to a separate ASCII file; use the Coordinate File Utility to *"skip, renumber or over right"*; make a new point group per day. ([RPLS duplicate points](https://rpls.com/forums/software-cad-mapping/duplicate-points-in-carlson/))

The NYSAPLS 2025 Advanced Field-to-Finish conference handout independently documents the same failure modes — inconsistent coding, over-combined companion codes, and "Locate Pts on Real Z" surface errors. ([NYSAPLS handout](https://cdn.ymaws.com/www.nysapls.org/resource/resmgr/2025_conference/2025_conf_handouts/advanced-guide-f2f.pdf))

**Why inadequate.** The code table (.FLD, description key set, TBC feature library) *is* the firm's production logic, and it is a binary or semi-structured file with no version control, no diff, no test, and typically one maintainer. Configuration drift between machines produces wrong output with no error message. The failure surfaces as bad linework a human must notice.

**Cost.** Unquantified publicly, but this is a daily tax on the highest-throughput step in the office, and the errors it produces are geometric errors in a sealed deliverable.

**Evidence strength: high** — three separate RPLS threads plus an independent state-society conference handout describing the same failure classes.

---

### Problem 7 — Provenance dies at the adjustment-to-drafting handoff, and format conversions corrupt silently

**Who.** PM and technician. **When.** Between adjustment and drafting. **Frequency.** Every project with control.

**How handled now.** A PNEZD CSV. That is the interchange. ([RPLS TBC thread](https://rpls.com/forums/software-cad-mapping/trimble-business-center-tbc-questions/))

**Why inadequate.** Adjustment statistics, redundancy, error ellipses, observation lineage, and field codes do not survive a coordinate file. Everything downstream of the CSV is disconnected from its evidence. The plat gets sealed on coordinates whose derivation is now only in a separate report nobody opens.

**Worse, some conversions corrupt silently.** Trimble `.fbk` files carry azimuths from the gun to each sideshot, but *"Carlson thinks they're angles"* — producing wrong coordinates. All the workarounds are manual: reconfigure the collector to "BS zero and measure AR", install style sheets to export TDS `.rw5` or SDR33 instead, or run Trimble's ASCII File Generator. ([RPLS .fbk thread](https://rpls.com/forums/software-cad-mapping/trimble-fbk-files-and-carlson/))

The vendor-neutral alternative is stagnant: **LandXML's stable release is v1.2, published 29 July 2008**; v2.0 has been in working-draft/preview since 2014 and was still not finalized as of 2025. Documented failures include incomplete LandXML exports into Civil 3D. ([LandXML](https://en.wikipedia.org/wiki/LandXML), [LP360 KB](https://support.lp360.com/hc/en-us/articles/41261700646419-LP360-Exported-LandXML-is-Incomplete-in-Civil-3D))

**Cost.** Long-tail. The specific fear is stated by a practitioner: bad coordinates persisting in a collector and being *"[built] on... by just building on their mistake"* years later. ([RPLS erroneous surveys](https://rpls.com/forums/discussion/erroneous-surveys/))

**Evidence strength: medium-high.** The .fbk corruption and the CSV handoff are directly evidenced. The claim that provenance loss *causes* measurable harm is my inference, not a practitioner statement.

---

### Problem 8 — Incumbent software cost is a live budget crisis, and the market is being force-migrated to subscriptions

**Who.** Owners. **When.** At renewal. **Frequency.** Annual.

**Evidence.** A surveyor in January 2026: *"I requested a quote to update my version [of TBC] a couple weeks ago and I was told $2200. I think I paid $3800 for it 3 years ago"* — in a thread noting Trimble ended maintenance renewals and perpetual licenses as of 2026. Another: TBC is *"not the most affordable cost v. functionality (bang for the buck) for a smaller company."* ([RPLS TBC subscription thread](https://rpls.com/forums/software-cad-mapping/trimble-tbc-subscription-packages-and-what-is-included/)) On scanning software: *"We recently got notice of some software pricing increases; heavy enough to take us well into the negative budget for the fiscal year."* ([RPLS scan software](https://rpls.com/forums/software-cad-mapping/scan-and-other-processing-software/)) Autodesk has raised list prices **6–9% in January 2026** on top of a documented 5–8%/yr pattern. ([Autodesk pricing analysis](https://autodesksaudits.com/blog/autodesk-subscription-pricing-2026/))

And the fit is poor for survey-only shops. On "Does Civil 3D provide value to the typical surveyor?": *"It's a sluggish program with twitchy graphics"*; *"If I were a survey only shop with no engineer clients I wouldn't use it"*; *"As a survey only tool it has an extreme learning curve and associated cost"*; *"I think that I understand C3D better than their programmers understand Surveying"*; *"if you are just producing plats and boundaries, then save your money."* ([RPLS Civil 3D thread](https://rpls.com/forums/software-cad-mapping/does-civil-3d-provide-value-to-the-typical-surveyor/))

Subscription resistance is explicit and repeated: two separate surveyors in the Deed Reader Pro thread object to *"the subscription model of software"*, one noting *"Looking at my desktop, I don't have any"* subscription software.

**Why this matters to the catalog.** It is not a problem to solve directly — nobody should build a Civil 3D replacement. It is the **market condition** that makes a free, offline, perpetually-usable tool attractive here in a way it would not be in a market comfortable with SaaS. Every opportunity below should ship as a local-first tool that does not phone home.

**Evidence strength: high.**

---

### Problem 9 — Elevation Certificates carry a very high observed error rate

**Who.** PLS (only a licensed surveyor, engineer, or architect can certify Section D). **When.** Per certificate. **Frequency.** A steady small-firm revenue line — $400–$900 in Florida, 1–2 hours on site plus 1–3 days office processing.

**Evidence.** An automated analysis of **5,082 residential Elevation Certificates issued after 1 January 2019 found 68.4% contained at least one flagged error, and 44% had multiple errors, averaging two per certificate.** Top error types: map/panel number mismatches (*"typos are common in this field"*), lowest-adjacent-grade below BFE on non-LOMA/LOMR-F certificates, regulatory floor below the community's Design Flood Elevation, lowest machinery elevation below DFE, and garages under elevated buildings not documented as enclosures per recent FEMA guidance *"which many surveyors haven't adopted."* ([Forerunner](https://www.withforerunner.com/post/elevation-certificates-errors)) **Caveat: Forerunner sells EC review software, so this metric is vendor-published — but the sample size and methodology are disclosed, which is more than most vendor statistics offer.**

Corroborating context: the current form (FF-206-FY-22-152) became mandatory **7 July 2023 with a one-week transition** between FEMA's posting and its announcement, drawing public criticism from a licensed surveyor; it introduced a WGS 84 datum option, expanded flood-opening items A8–A9, a new Limit of Moderate Wave Action item B13, and an entirely new Section H. A surveyor's specific complaint: **B13 forces a binary yes/no about LiMWA with no "don't know" option** in areas lacking coastal data. ([The American Surveyor](https://amerisurv.com/2023/08/12/better-late-than-never-the-new-elevation-certificate/)) FEMA's own OMB burden estimate is **12,735 annual hours across 3,517 respondents — roughly 3.6 hours per response.** ([Federal Register, 1 June 2026](https://www.federalregister.gov/documents/2026/06/01/2026-10842/agency-information-collection-activities-proposed-collection-comment-request-elevation)) And FEMA **retired** its dedicated surveyor training course IS-1103.A. ([FEMA EMI](https://training.fema.gov/is/courseoverview.aspx?code=IS-1103.a&lang=en))

**Evidence strength: high on the form and its churn** (primary FEMA and Federal Register sources); **medium on the error rate** (single vendor-published study, though methodologically disclosed).

---

### Problem 10 — Boundary resolution reasoning is not recorded in any structured way

**Who.** PLS. **When.** Throughout. **Frequency.** Every boundary survey.

**How handled now.** CAD layers, field notes, and the licensee's memory. The best-practice example found is murphy's colored-layer convention, motivated explicitly by wanting *"any reasonably intelligent PLS to pick up my work."*

**Why inadequate.** Florida requires retention for a **minimum of six years** from creation of signed and sealed drawings, plats and reports **plus related calculations and field notes, and documented records research** — and on ceasing practice the licensee must ensure *"safe storage and reasonable accessibility to clients"* for the same six years. ([FL 5J-17.053](https://regulations.justia.com/states/florida/5/5j/chapter-5j-17/section-5j-17-053/)) Meanwhile, typical professional-negligence limitation periods cited for surveyors are a **2-year discovery period with a 10-year absolute limit** — a longer tail than the retention minimum. ([POB](https://www.pobonline.com/articles/100693-traversing-the-law-surveyor-negligence-lawsuits), [The American Surveyor on statutes of repose](https://amerisurv.com/2004/06/30/surveyors-law-statutes-of-limitations-and-repose/))

Named liability categories include *"omission of evidence in boundary establishment"* and failure to locate or measure all pertinent monuments. ([Liability white paper](https://www.lsacts.com/documents/Land%20Surveyor%20Liability%20V1.3%20final%20w%20appendixes.pdf)) Carrier data across design professionals attributes roughly **30% of non-technical risk-driver claim dollars to communication breakdowns**, root-caused as *"lack of procedures to identify conflicts, omissions and errors."* ([AXA XL](https://axaxl.com/fast-fast-forward/articles/data-driven-insights-behind-design-professionals-eo-claims)) — though that dataset does not break out surveyors.

**Evidence strength: medium.** The retention requirements and liability categories are verified. That a structured resolution log would reduce claims is a **strong inference**, supported by the Victor underwriting questionnaire pricing documented peer review and documented project definition — but no practitioner asked for this tool.

---

## 4. Application opportunities

### Opportunity A — Metes-and-Bounds Closure & Mosaic Workbench

**Working title:** `DeedBench`
**Intended user:** Survey/CAD technician; PLS for verification.
**Problem solved:** Problems 1 and 2 — deed call transcription, closure computation, and record mosaic assembly.

**Current workflow:** Type calls into COGO one deed at a time; compute closure inside CAD or in a hand-built spreadsheet; draw each deed on its own CAD layer; eyeball the fit against found monuments.

**Proposed workflow:** Paste (or OCR) the description text for the subject and every adjoiner into one project. The tool parses calls, computes closure and precision ratio per parcel, flags ambiguous or unparseable calls for human resolution, assembles all parcels into a single mosaic, and exports a layered DXF (one layer per deed, named by book/page) plus KML and a PDF closure report.

**Inputs:** Description text (typed or pasted); optionally scanned PDFs; optionally a point file of found monuments for fit-testing.
**Outputs:** Layered DXF; KML; per-parcel closure report PDF with precision ratio, misclosure bearing and distance, and a call-by-call table; a CSV of parsed calls for audit.

**Essential features:** robust call parser handling bearing formats, curve calls (chord/arc/delta/radius, multiple solution methods), "more or less" acreage, and passing calls; per-call confidence flag; compass and transit rule adjustment; batch mode across many deeds; deterministic, reviewable output.
**Deliberately excluded from v1:** CAD editing, boundary resolution logic, title interpretation, any attempt to decide where the line *is*.

**AI:** **Optional, and confined to OCR of scanned/handwritten deeds.** The parsing of typed call text is a grammar problem, not an AI problem, and rule-based parsing is auditable in a way an LLM is not. For scanned 1890s handwriting, AI is the only realistic option — but it must present its transcription for human confirmation, never plot silently. A practitioner already articulated the reason: *"I have to enter the whole deed, and see what closes, to be sure."*

**Would a spreadsheet suffice?** Partially — and practitioners have proven it by building exactly that (the "band aid" compass-rule spreadsheet, Copan, Wolfpack). A spreadsheet cannot parse free text, cannot batch, and cannot emit layered CAD geometry. That gap is the product.

**Complexity:** Small-to-medium. **Learning difficulty:** Under 30 minutes.
**Value:** Minutes to hours per project; the closure report is a retainable QC artifact satisfying documented-calculation retention.
**Risks:** A parser that silently mis-reads a call is worse than no tool. Mitigation: every parsed call must be displayed against its source text before any geometry is produced; no silent success.
**Existing products:** Metes and Bounds ($39.95/$79.95, mature and cheap), Deed Reader Pro, CADastral ($10/100 credits to $700/10,000), MeteMap (free), DeedPlotter AI, Deed Pro.
**Why still attractive despite them:** This is the most crowded space in the report and the honest answer is *it is only attractive on specific differentiators*: (1) **batch mosaic across subject plus all adjoiners**, which the single-parcel tools do not do and which is the actual workflow GaryG and BStrand described; (2) **offline, perpetual, no subscription** — a stated purchase criterion in this market; (3) **the closure report as a liability exhibit**, not just a number on screen; (4) open source, so a firm can script it into their own pipeline.
**Paid customization:** Firm-specific DXF layer naming and CAD standards mapping; county-specific deed format quirks; integration into an existing Carlson or Civil 3D routine.

---

### Opportunity B — Recorder-Download Organizer & Research Log

**Working title:** `RecordKeeper`
**Intended user:** Technician doing records research; PLS for retention compliance.
**Problem solved:** Problem 1's filing half — the `1009737#$%773.pdf` problem — and Problem 10's documentation half.

**Current workflow:** Download PDFs from a county portal; rename each by hand to a personal convention; file into folders; remember what you looked at.

**Proposed workflow:** Point the tool at the download folder. It extracts document type, book/page or instrument number, recording date, grantor, grantee, and legal-description text from each PDF (text layer where present, OCR fallback), renames per a configurable firm template, files into a project structure, and generates a **hyperlinked research index** — an HTML or PDF sheet listing every document examined, what it is, and where the file sits.

**Inputs:** A folder of recorder PDFs; a firm naming template.
**Outputs:** Renamed and filed PDFs; a research index sheet; a CSV manifest; a "documents examined but not relevant" section (which is the part that satisfies *documented records research* retention).

**Essential features:** template-driven renaming; per-document field extraction with a confirm-before-rename review screen; never overwrite or delete originals; a manifest that reconstructs the operation.
**Excluded from v1:** Any connection to county portals (fragile, per-county, and legally grey); any title interpretation.

**AI:** **Optional.** Regex over the text layer handles most modern recorded documents. AI earns its place only on scanned pre-1980 documents and on grantor/grantee extraction from inconsistent layouts.

**Would a spreadsheet suffice?** No — the work is file manipulation and text extraction, which a spreadsheet cannot do.

**Complexity:** Small. **Learning difficulty:** Under 15 minutes.
**Value:** Directly replaces hand-renaming that at least one PLS documented doing on every job. Produces the retention artifact Florida requires (6 years, including *documented records research*) as a byproduct.
**Risks:** Mis-extraction producing a wrong filename. Mitigation: confirm-before-rename, and originals are never modified. Privacy: recorded documents are public records, so exposure is low — but the tool must run locally, since a firm will not upload a client's title packet to a third-party service.
**Existing products:** None found aimed at surveyors. General document-renaming tools exist but know nothing about book/page or grantor/grantee.
**Why attractive:** No incumbent, tiny scope, immediately understandable, and it produces a compliance artifact as a side effect.
**Paid customization:** Firm naming conventions; county-specific document layouts; hooks into an existing project folder structure.

---

### Opportunity C — ALTA 2026 Schedule B-II Exception Matrix Builder

**Working title:** `ExceptionMatrix`
**Intended user:** PLS and survey PM producing ALTA/NSPS surveys.
**Problem solved:** Problem 3 — per-exception compliance with 2026 §6.C.ii and its eight-condition checklist, plus the note-block that goes on the plat.

**Current workflow:** Read Schedule B-II. For each exception, decide disposition. Copy an appropriate boilerplate note from a prior project's plat. Hope nothing was skipped on a forty-exception commitment.

**Proposed workflow:** Enter (or import) the Schedule B-II exception list. For each exception the tool presents the **eight §6.C.ii conditions** as an explicit disposition selector plus a within/crosses statement. It will not let an exception be left undispositioned. It emits (1) a plat-ready note block in the firm's wording, (2) a surveyor's-report easement summary, and (3) a reviewable matrix for the file and for the title company.

**Inputs:** Exception list (typed, pasted, or CSV); firm note-language library.
**Outputs:** Plat note block as text and DXF-importable MTEXT; easement summary for the surveyor's report; a completion matrix showing every exception and its disposition; an exceptions-not-yet-dispositioned warning list.

**Essential features:** the eight conditions hard-coded from the standard with citation; completeness enforcement; editable firm note library with 2021→2026 migration warnings; export to plain text, DXF text, and CSV.
**Excluded from v1:** Plotting easement geometry (that is ALTA-Plot's territory and a much harder problem); reading the title commitment PDF automatically; any legal interpretation.

**AI:** **Optional, and only for extracting the exception list from a commitment PDF.** The compliance logic itself must be deterministic — an LLM deciding whether an easement "limits access" is precisely the wrong use of AI in a liability context.

**Would a spreadsheet suffice?** A spreadsheet gets you the matrix but not the enforced completeness, not the versioned note library, and not the generated plat text. It is a plausible v0 and a real competitor — the product must be meaningfully better than a good Excel template on day one.

**Complexity:** Medium. **Learning difficulty:** ~1 hour.
**Value:** Prevents a missed exception note on a document the title company relies on to delete policy exceptions. One avoided claim pays for a decade of the tool.
**Risks:** The tool encodes a standard that will change again (the 2021→2026 cycle took over three years to develop). Version the rule set explicitly and stamp outputs with the standard version used.
**Existing products:** [ALTA-Plot](https://www.alta-plot.com/) does AI classification of exception documents and DXF/KML export — it attacks the *plotting* half. Nothing found attacks the *note and completeness* half.
**Why attractive:** Timely (the standard is five months old and every firm's templates are stale), narrow, and squarely in the liability-reduction zone that carriers demonstrably price.
**Paid customization:** Firm note-language libraries; state-specific supplements; integration with a firm's plat template.

---

### Opportunity D — ALTA Table A Scope Configurator

**Working title:** `TableA`
**Intended user:** Owner/PLS at proposal time; secondarily the client, who fills it in.
**Problem solved:** Problem 4 — scope negotiated verbally, then disputed.

**Current workflow:** A PDF checklist of uncertain vintage, or an email. Sometimes nothing.

**Proposed workflow:** A single-page web app (runs from a local file, no server). The surveyor sends or screen-shares it. Each of the **21 items** in the 2026 standard is shown with: the exact standard language, a plain-English explanation of what it obligates, a **prerequisite flag** (Item 6 needs a client-supplied zoning report; Items 11 and 17 depend on third-party utility and jurisdiction response; Item 18 extends onto adjoining parcels), a **cost-driver flag** (1, 5, 18), and an optional firm fee adder. Item 21 sub-items are free-text with a required explanation field, matching the standard's requirement that each *"must be explained"* on the plat. Output is a dated, itemized scope exhibit as PDF, ready to attach to the contract and sign.

**Inputs:** Item selections; optional firm fee schedule.
**Outputs:** A signed-ready scope exhibit PDF; a fee summary; a JSON file the firm can archive or feed into a proposal.

**Essential features:** all 21 items with verbatim standard text and citation; prerequisite and cost-driver flags; free-text qualifications per item (the standard explicitly permits negotiating exact wording); dated output; a visible banner naming the standard version.
**Excluded from v1:** Fee calculation beyond simple adders; contract generation; e-signature.

**AI:** **Inappropriate.** This is 21 items of static, authoritative text plus arithmetic. Adding AI would introduce hallucination risk into a contract exhibit.

**Would a spreadsheet suffice?** No — the value is the client-facing explanatory layer and the clean signed exhibit, which is a document-generation problem.

**Complexity:** Small. Genuinely a weekend to a week for a competent developer.
**Learning difficulty:** Minutes. It is a form.
**Value:** Directly monetary and directly liability-reducing. The practitioner instruction is unambiguous: *"GIVE NO ESTIMATE UNTIL YOU HAVE A COMPLETED AND SIGNED TABLE A CHECKLIST!!"* On a $10K ALTA, one avoided scope dispute is worth more than the tool costs to build.
**Risks:** Must be updated when the standard changes; must not be mistaken for legal advice. Both handled with a prominent version stamp and a disclaimer.
**Existing products:** Law-firm explainer articles, the NV5 handbook, buyer-side guides, and static PDF checklists. **No interactive configurator found.** Note that a static PDF checklist is the real incumbent and it is free — the tool wins on the explanatory layer, the prerequisite flags, and being current with 2026 numbering, not on being digital.
**Paid customization:** Firm branding and fee schedules; standard qualification language; regional supplements; a version that writes directly into the firm's proposal template.

---

### Opportunity E — Recorded-Map Pre-Submittal Checker

**Working title:** `PlatCheck`
**Intended user:** CAD technician preparing the submittal; PLS signing it.
**Problem solved:** Problem 5 — checklist rejections and the statutory resubmittal clock.

**Current workflow:** The county's checklist PDF is open in one window and the drawing in another, if anyone remembers to open it at all.

**Proposed workflow:** Select the jurisdiction. The tool loads a **rule pack** — a structured, human-readable YAML/JSON encoding of that county's published checklist, with statute citations. It runs three tiers: (1) **automated checks** against the submitted PDF or DXF where mechanically possible (required statement blocks present by keyword, basis-of-bearings note present, text height on a DXF, sheet numbering, presence of a surveyor's statement and date); (2) **guided manual checks** the technician confirms one by one; (3) **deadline calculation** from the monument-set or field-completion date. Output is a completed, dated, signed-off checklist to include in the submittal package.

**Inputs:** The map (PDF and/or DXF); jurisdiction selection; key dates.
**Outputs:** A completed checklist PDF; a list of failed and unverifiable items; a deadline summary.

**Essential features:** rule packs as plain text files that a firm can author and share; statute citation on every item; explicit distinction between "automatically verified", "manually confirmed", and "could not be checked"; deadline arithmetic from the statutory triggers.
**Excluded from v1:** Any attempt to check mathematical closure of the map, drafting correction, or automated CAD fixes.

**AI:** **Inappropriate for the checking.** These are deterministic rules with statutory citations; an AI that "thinks" a statement block is present is useless. AI is **optional** as an authoring aid — converting a newly published county checklist PDF into a draft rule pack for human review. That is a real and defensible use.

**Would a spreadsheet suffice?** A shared checklist spreadsheet would capture tier 2, and some firms surely have one. It cannot do tier 1 or tier 3, and it does not stay current across jurisdictions.

**Complexity:** Medium — mostly because of the rule-pack content, not the code. **Learning difficulty:** ~1 hour.
**Value:** Avoiding one rejection cycle saves weeks of schedule and preserves a statutory clock. In California a missed 90-day filing is not merely inconvenient — non-compliance with ROS filing requirements is a named liability exposure.
**Risks:** **The maintenance burden is the central risk.** There are thousands of US counties. Mitigation: ship rule packs for a handful of high-volume jurisdictions, make authoring trivial, and treat the community-contributed rule-pack library as the actual product. The tool must never claim a map is compliant — only that specific listed items were checked.
**Existing products:** **None found.** Counties publish the checklists; nobody automates them.
**Why attractive:** Highest differentiation in this report and the highest paid-customization ceiling — "encode our three counties and our firm's internal QC list" is a natural, repeatable, billable engagement.
**Paid customization:** Per-jurisdiction rule packs; firm internal QC standards; integration into a firm's CAD title-block workflow.

---

### Opportunity F — Field-to-Finish Code Library Manager and Raw-Data Linter

**Working title:** `CodeGuard`
**Intended user:** The technician who owns the code table; every technician importing data.
**Problem solved:** Problem 6 — silent F2F failures, configuration drift, duplicate points, and un-versioned firm logic.

**Current workflow:** The .FLD or description-key file lives on a server. One person edits it. Nobody diffs it. Problems surface as wrong linework.

**Proposed workflow:** Two parts. **(1) Library manager:** import the firm's code table from Carlson .FLD, Civil 3D description keys, or a TBC feature library into a plain-text canonical format; version it in git; diff two versions in human-readable form; report codes present in the field data but absent from the library, and library codes never used. **(2) Linter:** run a raw file (.rw5, .fbk, PNEZD CSV) against the library *before* import and report unknown codes, unclosed BEG/END pairs, curve codes with implausible geometry, duplicate point numbers, points with identical coordinates and different numbers, elevation outliers, and codes used inconsistently within a job.

**Inputs:** Code table export; raw data files.
**Outputs:** A lint report with line references; a canonical code library file; a version diff report.

**Essential features:** read at least Carlson and Civil 3D code formats; deterministic lint rules with severities; exit codes suitable for scripting; no modification of source data.
**Excluded from v1:** Fixing anything, drawing linework, or replacing F2F processing. **This tool reports; it does not act.** That constraint is what makes it trustworthy and small.

**AI:** **Inappropriate.** These are parsing and rule checks. AI would add nondeterminism to a QC tool, which defeats the purpose.

**Would a spreadsheet suffice?** No — parsing binary and semi-structured survey formats is beyond a spreadsheet.

**Complexity:** Medium. Format reverse-engineering is the bulk of the work; `.rw5` is publicly documented ([Total Open Station](https://totalopenstation.readthedocs.io/en/stable/input_formats/if_carlson_rw5.html)), others less so.
**Learning difficulty:** ~1 hour for the linter; more for the library manager if the user has never used version control — which most will not have. **This is the concept's biggest adoption risk**, and it argues for hiding git behind a simple "snapshot / compare" UI.
**Value:** Catches geometry errors before they reach a sealed drawing. Turns the firm's most important undocumented asset into a versioned, reviewable file.
**Risks:** Format coverage is the make-or-break. Start with one or two formats done properly rather than five done badly.
**Existing products:** None found. CAD vendors ship the F2F engine but no linting or versioning layer around it.
**Why attractive:** No incumbent; the pain is daily; the evidence is strong across three forum threads and an independent state-society handout.
**Paid customization:** Firm-specific lint rules and code conventions; additional format readers; CI-style integration into a firm's import routine.

---

### Opportunity G — FEMA Elevation Certificate QC Validator

**Working title:** `ECheck`
**Intended user:** PLS or technician completing an Elevation Certificate; the reviewing PLS.
**Problem solved:** Problem 9 — a 68.4% observed error rate on a form the licensee seals.

**Current workflow:** Fill the PDF, eyeball it, seal it, send it. Errors surface when the community floodplain manager or lender rejects it.

**Proposed workflow:** Load the completed FF-206-FY-22-152 PDF. The tool reads the form fields and runs internal-consistency rules: map panel number format and community-number agreement; lowest adjacent grade versus BFE consistency for the certificate type; C2 elevations versus the community Design Flood Elevation where supplied; lowest machinery elevation versus DFE; enclosure/garage documentation per current FEMA guidance; datum consistency across sections; required photographs attached; Section H completeness; building diagram number consistent with the elevations reported. Output: a pass/flag report with the specific item, the rule, and the source citation.

**Inputs:** The filled PDF; optionally the community's DFE and FIRM panel data.
**Outputs:** A flag report; a reviewer sign-off sheet.

**Essential features:** read AcroForm fields from the FEMA PDF; rules with citations; severity levels (error vs. verify); a version banner naming the form edition; graceful handling of a flattened or scanned PDF (degrade to a guided manual checklist).
**Excluded from v1:** Filling the form, computing elevations, fetching FIRM data automatically, or LOMA/LOMR-F submission.

**AI:** **Inappropriate.** Every one of these checks is an arithmetic or field-consistency rule. This is the clearest "do not add AI" case in the report.

**Would a spreadsheet suffice?** No — it must read the PDF's form fields. A checklist could capture some rules but nobody would run it, which is precisely why the error rate is 68%.

**Complexity:** Small-to-medium. **Learning difficulty:** Under 30 minutes.
**Value:** If the Forerunner sample generalizes even loosely, roughly two in three certificates carry an error today. At $400–$900 per certificate and 3.6 hours of FEMA-estimated burden, avoiding rework and rejection is immediate ROI, and the reviewer sign-off is a documented-peer-review artifact carriers ask about.
**Risks:** The form changes on a roughly 3-year cycle (OMB collection 1660-0008 shows actions in 2003, 2005, 2009, 2012, 2015, 2018, 2022) and **a Federal Register notice of 1 June 2026 seeks an extension of the current collection, with the printed form expiration of 30 June 2026 already passed.** ([Federal Register](https://www.federalregister.gov/documents/2026/06/01/2026-10842/agency-information-collection-activities-proposed-collection-comment-request-elevation), [OMB history](https://omb.report/omb/1660-0008)) Any tool here must version its rule set against the form edition and must not be built assuming form stability. **This regulatory status should be confirmed with NFIP directly before building.**
**Existing products:** [Forerunner](https://www.withforerunner.com/post/elevation-certificates-errors) sells EC review software — but aimed at **communities and floodplain managers reviewing** certificates. This is the mirror image: the **surveyor-side pre-flight check**. That asymmetry is the whole opportunity.
**Paid customization:** Community-specific DFE tables; firm review workflow; batch validation for firms doing volume EC work.

---

### Opportunity H — Coordinate Handoff Auditor

**Working title:** `HandoffCheck`
**Intended user:** Survey PM and technician.
**Problem solved:** Problem 7 — provenance death at the PNEZD boundary and silent format corruption.

**Current workflow:** Export a coordinate file from TBC or STAR\*NET, import into Carlson or Civil 3D, trust it.

**Proposed workflow:** Register the pre-handoff source (adjustment output plus its report) and the post-handoff CAD point export. The tool compares them point by point, flags any point whose coordinates differ beyond tolerance, any point present in one and absent from the other, any renumbering, and any unit or datum mismatch. It also emits a **provenance sidecar** — a CSV/JSON keyed to point number carrying the adjustment residual, error ellipse, redundancy number, and observation count — so the statistics that die in the CSV are at least retained alongside it and can be annotated into a point table.

**Inputs:** Adjustment report and coordinate export; CAD point export.
**Outputs:** A reconciliation report; a provenance sidecar file; a flagged-differences list.

**Essential features:** parse STAR\*NET and TBC report formats; tolerance configuration; explicit unit checking (International vs US Survey Feet — a documented silent-corruption vector in the Civil 3D survey database); no modification of either file.
**Excluded from v1:** Performing adjustments; drawing anything; being a data management system.

**AI:** **Inappropriate.** Numeric comparison.

**Would a spreadsheet suffice?** A determined technician could VLOOKUP two coordinate files. Nobody does, and the spreadsheet cannot parse adjustment reports or check units.

**Complexity:** Medium. **Learning difficulty:** ~1 hour (requires understanding what a residual is — the user does).
**Value:** Catches the class of error nobody catches, including the documented `.fbk` azimuth-versus-angle corruption between Trimble and Carlson and the International/US Survey Foot mismatch.
**Risks:** **The lowest-confidence concept in this report.** The corruption modes are verified, but no practitioner asked for this tool, and the ROI is preventive rather than time-saving — a harder sell. Validate before building.
**Existing products:** None found.
**Paid customization:** Additional adjustment-report parsers; firm tolerance standards.

---

### Opportunity I — Boundary Evidence & Resolution Log

**Working title:** `ResolutionLog`
**Intended user:** PLS.
**Problem solved:** Problem 10 — unrecorded reasoning, retention obligations, and the "pick up my work" problem in a retiring profession.

**Current workflow:** CAD layers, field notes, memory, and — at best — a personal colored-layer convention.

**Proposed workflow:** A structured log per boundary. For each corner: monuments found (type, size, condition, accessories, who set it, record reference), record calls in conflict, the weight the surveyor assigned to each, the conclusion, and the reason. Attach photos and record excerpts. Output a **boundary resolution memo** as PDF for the project file, plus a monument table ready for the plat.

**Inputs:** Field observations; record references; photos.
**Outputs:** Resolution memo PDF; monument table CSV/DXF text; a retention-ready project record.

**Essential features:** a corner-by-corner structure; free-text reasoning with structured metadata around it; photo attachment; export that reads well to a third party years later; local file storage in an open format.
**Excluded from v1:** Any suggestion of what the boundary should be. The tool records reasoning; it does not produce it.

**AI:** **Inappropriate for the reasoning.** Optionally useful for drafting prose from structured notes — but a surveyor's boundary reasoning is the professional act, and an LLM writing it would be both useless and dangerous. If included at all, restrict to formatting a monument table.

**Would a spreadsheet suffice?** Closer than for most concepts here. The advantages are the memo output, photo handling, and a structure that prompts for the fields a claim defense would need.

**Complexity:** Small-to-medium. **Learning difficulty:** ~30 minutes; the adoption difficulty is much higher than the learning difficulty.
**Value:** Liability-facing, not time-saving. Directly serves Florida's 6-year retention of *calculations, field notes and documented records research*, against a 10-year absolute limitation period.
**Risks:** **Highest adoption risk in the report.** It adds work to the surveyor's day in exchange for a benefit that only materializes in a dispute. Anything that feels like documentation-for-its-own-sake will not be used. It has to produce the monument table the surveyor needs anyway, so the memo is a byproduct rather than an extra chore.
**Existing products:** None found.
**Paid customization:** Firm memo templates; state-specific monument documentation requirements; integration with plat monument tables.

---

### Opportunity J — Statutory Filing Deadline Tracker

**Working title:** `FilingClock`
**Intended user:** PLS and PM.
**Problem solved:** Problem 5's deadline half.

**Current workflow:** Memory, a calendar entry if someone remembers, or a whiteboard.

**Proposed workflow:** When a job records a triggering event — monuments set, field survey complete, county returned the map for correction — the tool computes every applicable statutory deadline from a per-state rule pack and shows a single dashboard of what is due when. California ROS: 90 days from the earlier of monuments set or field completion (BPC 8762); 60 days to resubmit a returned map (BPC 8767); corner records 20 working days county review, 60 days to resubmit (BPC 8773.2). Washington: 90 days from corner establishment (RCW 58.09). It also tracks the written-notice-before-deadline mechanism California provides for extensions.

**Inputs:** Job, jurisdiction, and triggering event dates.
**Outputs:** A deadline dashboard; per-job deadline sheet; optional calendar (.ics) export.

**Essential features:** per-state rule packs with statute citations; working-day versus calendar-day arithmetic done correctly; the "earlier of two triggers" logic; nothing that requires a server.
**Excluded from v1:** Project management, task assignment, or anything resembling a CRM. This tool answers one question: what is due, and when.

**AI:** **Inappropriate.** Date arithmetic against cited statutes.

**Would a spreadsheet suffice?** A well-built spreadsheet could do the arithmetic. It would not encode the "earlier of" logic or working-day rules reliably, and it would not be maintained as statutes change (California has active 2025–26 legislation touching records-of-survey law — [AB 1933](https://legiscan.com/CA/text/AB1933/id/3362832), text unverified).

**Complexity:** Small. **Learning difficulty:** Minutes.
**Value:** Risk elimination. Non-compliance with ROS filing requirements is a named liability exposure — negligence per se, essentially.
**Risks:** Must never be presented as legal advice; must cite the statute for every computed date; must be obviously versioned.
**Existing products:** None found; generic task managers do not know the rules.
**Why attractive:** Trivially small, and it addresses an obligation with a statutory penalty attached.
**Paid customization:** Additional states; firm-specific internal milestones; integration with an existing job list.

---

## 5. Opportunity ranking

Scored 1–5 on ten criteria. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of implementation | Stays narrow | Differentiation | Customization potential | Test data available | Evidence confidence | **Total** |
|---|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| **D** | ALTA Table A Scope Configurator | 4 | 4 | 5 | 5 | 5 | 5 | 4 | 4 | 4 | 5 | **45** |
| **E** | Recorded-Map Pre-Submittal Checker | 5 | 4 | 5 | 4 | 3 | 3 | 5 | 5 | 5 | 4 | **43** |
| **G** | FEMA Elevation Certificate QC Validator | 5 | 3 | 5 | 5 | 4 | 5 | 4 | 3 | 4 | 5 | **43** |
| **B** | Recorder-Download Organizer & Research Log | 3 | 5 | 4 | 5 | 4 | 4 | 4 | 5 | 4 | 4 | **42** |
| **J** | Statutory Filing Deadline Tracker | 4 | 3 | 4 | 5 | 5 | 5 | 4 | 3 | 4 | 5 | **42** |
| **A** | Metes-and-Bounds Closure & Mosaic Workbench | 4 | 5 | 4 | 5 | 4 | 4 | 2 | 3 | 5 | 5 | **41** |
| **C** | ALTA Schedule B-II Exception Matrix Builder | 5 | 3 | 4 | 4 | 4 | 4 | 4 | 4 | 3 | 5 | **40** |
| **F** | F2F Code Library Manager & Raw-Data Linter | 4 | 5 | 4 | 3 | 3 | 4 | 5 | 5 | 3 | 4 | **40** |
| **I** | Boundary Evidence & Resolution Log | 4 | 5 | 3 | 4 | 4 | 3 | 4 | 4 | 3 | 3 | **37** |
| **H** | Coordinate Handoff Auditor | 4 | 4 | 3 | 3 | 3 | 4 | 5 | 4 | 3 | 3 | **36** |

### The top three explained

**1. D — ALTA Table A Scope Configurator (45).** It wins on the composite, not on ambition. It is the smallest thing in the report to build, the easiest to learn, the hardest to scope-creep, and it has the most direct monetary ROI — an ALTA survey runs to five figures and the entire dispute surface is a 21-item list nobody documents properly. It is also the most *timely*: the 2026 standard took effect five months ago and renumbered Table A, so every firm's existing checklist PDF is now wrong in a way that is invisible until it matters. The evidence is unusually convergent: a practitioner shouting the instruction in all caps, the standards work group naming scope creep as a chronic problem, a buyer-side guide diagnosing the exact failure mode, and a professional-liability carrier asking on its application whether the firm produces a documented scope incorporating ALTA standards. When practitioners, the standards body, and the insurer all point at the same missing artifact, that is the artifact to build.

Its weakness is honest: it is small, and value per use is modest compared to E or F. It is the right *first* build precisely because it is small — a week of work, a real deliverable, and a credible calling card into this market.

**2. E — Recorded-Map Pre-Submittal Checker (43).** The highest ceiling and the highest differentiation in the report. Counties publish 40-item checklists with statutory citations, a real second-submittal packet ran 60+ comments, and California statute contains explicit return-and-resubmit machinery with 60-day clocks — meaning the legislature assumed rejection would be routine. Nobody automates any of it. The paid-customization story writes itself: "encode our three counties plus our internal QC list."

The reason it is not first is implementation risk, and it is a serious one. The product is not the code, it is the rule-pack library, and there are thousands of counties. Build it as a rule-pack *engine* with a handful of exemplary packs and treat community contribution as the growth model, or it becomes an unbounded content-maintenance obligation.

**3. G — FEMA Elevation Certificate QC Validator (43).** Tied with E and stronger on scope discipline. It has the single most striking number in the research — **68.4% of 5,082 certificates carried at least one error** — attached to a document a licensee personally seals, on a form whose dedicated federal training course has been retired. It is pure deterministic rule-checking on a machine-readable PDF, which makes it small, testable, and immune to the "should this use AI" question.

Two caveats keep it from first place. The error-rate figure is vendor-published (by a company selling the reviewer-side tool), and the form is in regulatory flux right now — the printed expiration passed on 30 June 2026 while an OMB extension is pending. Confirm the form's status with NFIP before committing.

### What should be investigated next

**Opportunity D first, then E.** D is a one-week build that produces a shareable artifact and an excuse to talk to surveyors — which is exactly what the validation plan below needs. Use the conversations D generates to test the assumptions behind E, which is the bigger prize.

**Opportunity A should be investigated but probably not built.** Deed plotting is the most-felt pain in the market and it scored 41 — but it is also the only space in this report with six commercial entrants in two years, including a free one. The differentiators (batch adjoiner mosaic, offline/perpetual, closure report as liability exhibit) are real but narrow. Before building, confirm with practitioners that the mosaic workflow is underserved by the existing tools; if it is not, redirect that effort to E or F.

---

## 6. Validation plan

### Questions to ask practitioners

**On Table A (Opportunity D):**
1. Walk me through the last ALTA proposal you sent. How did the Table A selections get agreed and documented?
2. Have you updated your Table A checklist for the 2026 renumbering? *(Diagnostic: if most say "what renumbering," the tool sells itself. If most say "our template vendor handled it," the opportunity shrinks.)*
3. Tell me about the last time a Table A item turned out to cost more than you priced. What happened?
4. Who fills out the checklist — you, or the client?

**On plat submittals (Opportunity E):**
5. Of your last ten recorded maps, how many came back with comments? How many comment rounds on average?
6. What are the three comments you get most often, and why do they keep happening?
7. Do you use the county's published checklist before submitting? *(If the honest answer is "no, we should," that is the product.)*
8. Have you ever missed or nearly missed a filing deadline?

**On Elevation Certificates (Opportunity G):**
9. How many ECs do you do a year, and what do you charge?
10. How often does one come back from a floodplain manager or lender? For what?
11. Who reviews an EC before it is sealed?

**On the whole workflow:**
12. What is your actual office-to-field hour ratio, and where does the office time go?
13. What is the last spreadsheet or LISP routine you built for yourself, and why?  *(This is the highest-yield question in the list — every homemade tool is an unmet need with proven willingness to invest.)*
14. What would you never let software do for you?

### Who to interview

- **Sole-practitioner and 2–5 person PLS firms** in a Record-of-Survey state (California, Washington, Nevada) — the E and J audience.
- **10–30 person firms with a dedicated CAD technician** — the A, B, and F audience. Recruit the technician, not the owner; the owner does not do the work.
- **Florida and Gulf Coast firms doing EC volume** — the G audience.
- **Firms doing regular commercial ALTA work** — the C and D audience.
- **A county surveyor's office plan checker** — the single highest-leverage interview for E. They can state the actual rejection reasons and their frequency, which no practitioner-side source can.
- **A professional-liability underwriter or broker serving surveyors** (Victor, or an A&E-focused broker) — can confirm which documentation artifacts actually move premium, validating C, D, and I.
- Recruiting channels: state society conferences and chapter meetings (NSPS state affiliates), RPLS.com, LinkedIn, and — once reachable — r/Surveying.

### Search terms for further research

`site:reddit.com/r/Surveying "tedious"` · `r/Surveying "I wrote a script"` · `"record of survey" rejected comments` · `county surveyor "check print" comments` · `"Table A" checklist 2026 site:*.org` · `NSPS state society conference handout field to finish` · `"elevation certificate" rejected "floodplain manager"` · `surveyor LISP routine mapcheck closure` · `"description key" OR ".fld" code table standard survey firm` · `surveyor E&O claim boundary "record of survey" not filed` · `"survey technician" job description deed plotting` · state society newsletters (NYSAPLS, CLSA, LSAW, FSMS, TSPS) for conference handouts, which are consistently the most candid published material in this market.

### Sample files and data needed

- 5–10 completed Elevation Certificates (FF-206-FY-22-152) with known defects — obtainable from public floodplain-management records in some communities, which also solves the privacy problem.
- 3–5 published county ROS/plat checklists in machine-readable form, plus at least one real **check print with comments** (the Adams County packet is one; more are findable in public planning records).
- A real Schedule B-II exception list with 20+ exceptions, redacted.
- A firm's Carlson `.FLD` or Civil 3D description key set, plus a matching `.rw5` and PNEZD file from the same job.
- A set of 20 metes-and-bounds descriptions spanning eras and formats, with known closure results — the standard test corpus for A.

### Prototypes that would validate

- **D:** A one-page HTML file with all 21 items, prerequisite flags, and PDF export. Two days. Send it to five surveyors and see whether any of them use it on a live proposal. Usage, not praise, is the signal.
- **E:** One county's rule pack plus a script that checks the five most mechanically-checkable items on a real submitted PDF. Then ask a county plan checker whether those five are actually the ones that get flagged.
- **G:** A Python script that reads AcroForm fields from a filled EC PDF and runs the five error types Forerunner named. Run it against ten real certificates. If it finds errors in six or seven, the vendor statistic replicates and the concept is confirmed.
- **A:** A parser run against 20 real descriptions. Measure the unambiguous-parse rate. If it is not well above the 40% that Deed Reader Pro users report, do not build it.

### Assumptions most likely to make these fail

1. **D:** That firms will change their proposal process at all. Many will keep emailing a PDF. *This is the most likely failure mode for the top-ranked concept.*
2. **E:** That per-county rule packs can be maintained. If each requires a day of expert attention per year, the model collapses beyond a handful of counties.
3. **E:** That enough checklist items are mechanically checkable from a PDF. If only three of forty are, the tool degrades to a digital checklist — still useful, far less compelling.
4. **G:** That the Forerunner error rate generalizes beyond their customer base and their flagging rules. And that the form does not change during development.
5. **A:** That practitioners will trust a parser. The stated position — *"I have to enter the whole deed, and see what closes, to be sure"* — suggests some will not, at any accuracy level.
6. **F:** That technicians will adopt version control in any form. Historically, this profession has not.
7. **I:** That anyone will do documentation work whose payoff is contingent on a lawsuit. Probably the single weakest assumption in the report.
8. **Across all:** That a free open-source tool can reach these buyers at all. This market discovers software through state society conferences, RPLS.com, and equipment dealers — not through GitHub. Distribution may be a harder problem than any of the engineering.

---

## 7. Cross-industry patterns

Seven patterns from this market transfer to named backlog markets.

**Pattern 1 — Standards-version diff and template migration assistant.** A governing standard renumbers or revises; every firm's templates, note libraries, and checklists silently reference the old version. Evidenced here by the 2021→2026 ALTA Table A renumbering. *Transfers to:* **Fire protection / fire sprinkler design** (NFPA 13 edition cycles, where an adopted-edition mismatch between the AHJ and the designer's details is a recurring and expensive problem), **Mechanical HVAC design at small MEP firms** (ASHRAE 62.1/90.1 and state energy-code cycles), **Structural engineering firms** (IBC / ASCE 7 revisions), **Small architectural studios** (MasterFormat and spec-section updates).

**Pattern 2 — Jurisdiction rule packs: turning published AHJ checklists into an automated pre-submittal check.** Regulators publish granular checklists as PDFs; nobody runs them. Evidenced here by county Record-of-Survey checklists. *Transfers to:* **Civil / land development engineering and entitlement consulting** (the closest sibling — same counties, same reviewers), **Small architectural studios** (building-department plan-check checklists), **Fire protection subcontractors** (fire-marshal submittal requirements, which vary by AHJ as much as ROS requirements vary by county), **GC preconstruction** (permit package completeness), **Construction submittal/RFI coordination**.

**Pattern 3 — Exception/exhibit disposition matrix with enforced completeness.** An externally supplied list of items, each of which must receive an explicit, categorized disposition, with nothing left blank. Evidenced here by ALTA §6.C.ii. *Transfers to:* **Title, escrow, and real estate closing** (the other side of this exact document), **Independent insurance agencies — commercial lines** (endorsement and exclusion review), **Construction submittal and RFI coordination** (submittal-register completeness), **Nonprofit grant management and compliance** (grant-condition disposition).

**Pattern 4 — Scope configurator producing a signed scope exhibit.** A menu of optional services where the buyer cannot see which items carry prerequisites or cost multipliers; output is a dated, signed exhibit that attaches to the contract. Evidenced here by Table A. *Transfers to:* **Structural engineering firms** (special inspection and observation scope), **Geotechnical and environmental consulting** (Phase I/II ESA scope and ASTM optional items — an almost exact structural analogue), **Small CPA tax preparation practices** (engagement-letter scope), **Marketing and creative agency account management** (statement-of-work scope).

**Pattern 5 — Rules-based QC validator for a high-error regulated form.** A government form with a measurable error rate, filled by a professional who signs it, checkable by deterministic internal-consistency rules. Evidenced here by the FEMA Elevation Certificate at 68.4%. *Transfers to:* **Immigration law practice** (USCIS form internal consistency — the same shape of problem on a form family with well-known rejection patterns), **Medical billing and revenue cycle** (claim scrubbing pre-submission), **Estate planning and probate** (court-form completeness), **Nonprofit grant management** (federal report forms).

**Pattern 6 — Versioned firm-logic library with a linter.** A firm's production logic lives in un-versioned config files maintained by one person; drift causes silent wrong output. Evidenced here by F2F code tables. *Transfers to:* **Fire protection design** (CAD block, fitting and fabrication libraries), **Mechanical HVAC design** (Revit family and schedule-parameter libraries), **Machine shop / job shop quoting** (tooling and material libraries feeding quotes), **Small architectural studios** (office CAD/Revit standards).

**Pattern 7 — Statutory deadline clock triggered by a field or file event.** A domain event starts a legally binding clock with jurisdiction-specific arithmetic; missing it is negligence per se. Evidenced here by CA BPC 8762/8767/8773.2 and RCW 58.09. *Transfers to:* **Immigration law practice** (filing and response deadlines), **Estate planning and probate** (probate court deadlines), **Title, escrow, and real estate closing** (recording and rescission periods), **Electrical/plumbing subcontractor operations and GC preconstruction** (preliminary notice and mechanics' lien deadlines, which are state-specific and routinely missed).

### New backlog markets discovered

| Market | Why it looks promising |
|---|---|
| Flood zone / FEMA elevation certificate and LOMA-LOMR consulting | Narrow regulated deliverable with a documented 68.4% error rate, recurring per-property revenue, and a retired federal training course |
| Title abstracting and independent title search contractors | Surveyors already outsource to them above 1–2 billable hours; document-extraction-heavy work with no visible tooling |
| County surveyor / municipal plan-check offices (public sector) | The other side of Pattern 2; they author the checklists and could validate every rule pack |
| UAS / drone mapping and reality-capture service providers | GCP management, processing pipelines, and deliverable QC; practitioners report 3-day processing runs on large jobs |
| Right-of-way and easement acquisition consulting | Legal descriptions, parcel exhibits, and per-parcel document tracking — adjacent to surveying but a distinct buyer |
| Geodetic control and network adjustment specialists | Candidate narrow-subspecialty for the land surveying market; strong open-source math base (SALSA, DynAdjust, JAG3D) with no workflow layer |

---

## 8. Sources and confidence

### Verified findings (primary or multiply corroborated)

**Standards and regulation — highest confidence, primary sources:**
- 2026 ALTA/NSPS standards, effective 23 February 2026, 21 Table A items, §6.C.ii eight-condition exception requirement — [official NSPS PDF](https://cdn.ymaws.com/nsps.us.com/resource/resmgr/alta_standards/2026_OFFICIAL_FINAL_PDF_ALTA.pdf), corroborated by [ALTA](https://www.alta.org/news-and-publications/news/20251125-Key-Updates-to-the-2026-ALTANSPS-Land-Title-Survey-Standards), [McGuireWoods](https://www.mcguirewoods.com/client-resources/alerts/2026/2/updated-alta-nsps-land-title-survey-standards-take-effect-feb-23/), [Benesch](https://www.beneschlaw.com/insight/alta-nsps-key-changes-and-updates-in-the-2026-standards/), [Holland & Knight](https://www.hklaw.com/en/insights/publications/2026/03/2026-alta-survey-standards-updates), [The American Surveyor](https://amerisurv.com/2026/02/01/the-2026-minimum-standard-detail-requirements-for-alta-nsps-land-title-surveys/), [NJSPLS SurvCon deck](https://cdn.ymaws.com/njspls.org/resource/resmgr/2026_survcon/_17__2026_alta-nsps_land_tit.pdf)
- California filing and resubmittal deadlines — [BPC § 8762](https://leginfo.legislature.ca.gov/faces/codes_displaySection.xhtml?lawCode=BPC&sectionNum=8762), [BPC § 8767](https://codes.findlaw.com/ca/business-and-professions-code/bpc-sect-8767/), [BPC § 8773.2](https://california.public.law/codes/business_and_professions_code_section_8773.2); Washington — [RCW 58.09](https://wa-law.org/rcw/58_boundaries_and_plats/58.09_surveys%E2%80%94recording.html)
- Florida 6-year retention including calculations, field notes and documented records research — [5J-17.053](https://regulations.justia.com/states/florida/5/5j/chapter-5j-17/section-5j-17-053/)
- County ROS checklists — [Placer](https://www.placer.ca.gov/DocumentCenter/View/3890/Record-of-Survey-Map-Review-Checklist-PDF), [San Diego](https://www.sandiegocounty.gov/content/dam/sdc/dpw/COUNTY_SURVEYOR/survred.pdf), [Santa Barbara](http://surveyor.countyofsb.org/downloads/RS_2022.pdf), [Kern](https://www.kernpublicworks.com/services/development/surveying/record-of-survey-guidelines), [Sonoma](https://permitsonoma.org/instructionsandforms/sur-003recordofsurveysubmittalrequirementschecklist)
- A real 60+-comment second-submittal plat review — [Adams County PLT2024-00007](https://adamscountyco.gov/wp-content/uploads/2025/08/PLT2024-00007-submittal2.pdf); multi-round review by design — [Portland.gov](https://www.portland.gov/ppd/zoning-land-use/land-use-review-fees-and-types/final-plat-reviews)
- FEMA EC form status and burden — [FF-206-FY-22-152](https://www.fema.gov/sites/default/files/documents/fema_form-ff-206-fy-22-152.pdf), [Federal Register 1 June 2026](https://www.federalregister.gov/documents/2026/06/01/2026-10842/agency-information-collection-activities-proposed-collection-comment-request-elevation), [OMB 1660-0008 history](https://omb.report/omb/1660-0008), [IS-1103.A retired](https://training.fema.gov/is/courseoverview.aspx?code=IS-1103.a&lang=en)

**Practitioner workflow and complaints — high confidence, named practitioners on a long-running professional forum:**
- Office-to-field ratios — [RPLS "How long does it take?"](https://rpls.com/forums/software-cad-mapping/how-long-does-it-take/), [RPLS "Average work day"](https://rpls.com/forums/strictly-surveying/average-work-day/)
- Deed research and mosaic practice — [RPLS boundary research procedure](https://rpls.com/forums/strictly-surveying/boundary-survey-research-procedure/), [RPLS deed history](https://rpls.com/forums/discussion/deed-history-jr-sr-rights/)
- Closure workarounds — [RPLS closure thread](https://rpls.com/forums/strictly-surveying/analyzing-older-deeds-closure-autodesk-land-desktop-3/), [LSU closure LISP request](https://landsurveyorsunited.com/forum/topics/deed-map-closure-lisp-routine)
- Field-to-finish failures — [RPLS F2F linework](https://rpls.com/forums/software-cad-mapping/carlson-f2f-not-generating-line-work/), [RPLS F2F tricks](https://rpls.com/forums/strictly-surveying/field-to-finish-tricks-n-tips/), [RPLS duplicate points](https://rpls.com/forums/software-cad-mapping/duplicate-points-in-carlson/), [NYSAPLS 2025 handout](https://cdn.ymaws.com/www.nysapls.org/resource/resmgr/2025_conference/2025_conf_handouts/advanced-guide-f2f.pdf)
- Schedule B and ALTA scope — [RPLS Schedule B](https://rpls.com/forums/discussion/addressing-a-title-committment-schedule-b), [RPLS ALTA pricing](https://rpls.com/forums/strictly-surveying/alta-pricing/paged/2/), [RPLS exception notes](https://rpls.com/forums/discussion/notes-for-exceptions-on-alta-surveys/), [NV5 handbook](https://www.nv5.com/wp-content/uploads/2022/08/bc-handbook-alta-land-title-surveys.pdf), [Builoff](https://www.builoff.com/blog-posts/how-to-choose-alta-table-a-items-cost-schedule-guide), [Partner ESI](https://www.partneresi.com/resources/articles/demystifying-alta-surveys-pro-tips-and-table-a-items/)
- Software cost and fit — [RPLS Civil 3D value](https://rpls.com/forums/software-cad-mapping/does-civil-3d-provide-value-to-the-typical-surveyor/), [RPLS TBC subscription](https://rpls.com/forums/software-cad-mapping/trimble-tbc-subscription-packages-and-what-is-included/), [RPLS TBC questions](https://rpls.com/forums/software-cad-mapping/trimble-business-center-tbc-questions/), [RPLS PM software](https://rpls.com/forums/strictly-surveying/project-management-software/), [Autodesk 2026 pricing](https://autodesksaudits.com/blog/autodesk-subscription-pricing-2026/), [Carlson licensing](https://thatcadgirl.com/faq/what-to-know-about-purchasing-carlson-software/)
- Format corruption and interchange — [RPLS .fbk/Carlson](https://rpls.com/forums/software-cad-mapping/trimble-fbk-files-and-carlson/), [LandXML v1.2 (2008)](https://en.wikipedia.org/wiki/LandXML), [LP360 incomplete LandXML](https://support.lp360.com/hc/en-us/articles/41261700646419-LP360-Exported-LandXML-is-Incomplete-in-Civil-3D), [Civil 3D survey database single-editor and unit-mismatch](https://designandmotion.net/autodesk/civil-3d-sharing-point-data-survey-database/)
- Live role definitions — August 2026 Indeed postings: [Astra Surveying CAD Tech](https://to.indeed.com/aa969rkyfv6g), [Bohler Senior Survey Tech](https://to.indeed.com/aafq8rm247tw), [Rauch CAD Tech](https://to.indeed.com/aap6y22fdrrz), [Blew & Associates](https://to.indeed.com/aaxxdgwdznyq), [Bartram Trail Party Chief](https://to.indeed.com/aayjytscbpy2), [ESP Associates PM](https://to.indeed.com/aayy28jg6zp4)
- Market size — [IBISWorld: 17,511 US businesses, 2025](https://www.ibisworld.com/united-states/number-of-businesses/surveying-mapping-services/1407)
- Liability and underwriting — [Land Surveyor Liability white paper](https://www.lsacts.com/documents/Land%20Surveyor%20Liability%20V1.3%20final%20w%20appendixes.pdf), [POB surveyor negligence](https://www.pobonline.com/articles/100693-traversing-the-law-surveyor-negligence-lawsuits), [Victor PL application for surveyors](https://www.victorinsurance.com/content/dam/victor/victor2/documents/victor-us/architects-engineers/applications/US-architects-engineers-application-surveyors.pdf)
- Competitive landscape in deed plotting — [Deed Reader Pro](https://www.deedreaderpro.com/), [CADastral](https://cadastral.pro/), [ALTA-Plot](https://www.alta-plot.com/), [DeedPlotter AI](https://deedplotter.ai/), [Deed Pro](https://deedprosoftware.com/), [MeteMap](https://metemap.com/), [Metes and Bounds](https://www.tabberer.com/sandyknoll/more/metesandbounds/metes.html)

### Strong inferences (reasoned from verified evidence, not directly stated)

1. **Deed research and plotting consumes a material share of office hours.** The 1:1-to-2.5:1 ratio is verified and deed plotting is verified as a named salaried duty, but no source apportions hours between them.
2. **Loss of adjustment provenance at the PNEZD handoff causes real downstream harm.** The handoff and the `.fbk` corruption are verified; the harm is inferred from one practitioner's stated fear about propagated coordinates.
3. **A structured boundary-resolution log would reduce claim exposure.** Supported by retention rules, named claim categories, and the Victor questionnaire pricing documented peer review — but no practitioner asked for it.
4. **Plat rejection is common rather than exceptional.** The statutory return-and-resubmit machinery in CA §§ 8767 and 8773.2 implies the legislature expected the loop to be routine, and the Adams County packet shows what one looks like. There is no published rejection rate.
5. **Small firms will prefer local-first, no-subscription tools.** Inferred from repeated, explicit subscription objections across three separate forum threads — strong, but it is sentiment, not purchase data.
6. **Firms have not updated their Table A checklists for the 2026 renumbering.** Plausible given the five-month elapsed time and template inertia, but entirely unverified. **This is the load-bearing assumption under the top-ranked concept and should be the first thing tested.**

### Tentative hypotheses requiring practitioner validation

1. **That the 68.4% EC error rate generalizes.** Vendor-published, from a company selling the reviewer-side product, on their own flagging rules. Methodology and sample size are disclosed, which is better than typical, but it needs independent replication — the G prototype is designed to do exactly that.
2. **That mosaic-style multi-deed batch plotting is underserved.** Practitioners describe the mosaic workflow; whether existing tools handle it adequately was not determined.
3. **That county rule packs are maintainable at scale.** Untested and it is the make-or-break for E.
4. **That technicians would adopt version control for code tables.** No supporting evidence; the profession's history suggests resistance.
5. **That a free open-source tool can reach these buyers.** Distribution in this market runs through state societies, RPLS.com, and equipment dealers. This may be the binding constraint on the whole catalog thesis in this vertical, and it is worth testing early and cheaply.

### Known evidence gaps

- **reddit.com was unreachable from this environment.** r/Surveying — the largest and most candid practitioner community in this market — was not mined. Re-running that search alone would likely surface more, and more quantified, pain points than any other single action.
- **RPLS.com has moved recent topics behind member support.** At least one directly relevant thread (surveyors using AI to generate LISP routines) was truncated to its opening post. A paid membership would unlock the most automation-relevant current discussion.
- **No published surveyor-specific E&O claims frequency or severity dataset** is publicly available. The AXA XL design-professional data does not break out surveyors.
- **No published plat/ROS rejection rate.** One real comment packet is not a rate. A county surveyor interview would settle it in twenty minutes.
- **BLS occupational employment data for surveyors and survey technicians** could not be retrieved (fetch authorization unavailable in this unattended run). Workforce sizing rests on the IBISWorld business count alone.

---

*Prepared by the market research cycle, claim `2095f105`, 3 August 2026.*
