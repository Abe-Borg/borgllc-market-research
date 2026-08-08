# Dental and Specialty Clinic Practice Administration — Handoffs and QA

**Market research cycle report — Borg LLC open-source business application catalog**

---

## 0. Cycle header

| | |
|---|---|
| **Market claimed** | Dental and specialty clinic practice administration |
| **Angle claimed** | handoffs-and-qa |
| **Claim ID** | `340ca135` |
| **Date** | 2026-08-08 |
| **Reports completed before this one** | 23 |
| **Backlog remaining after this claim** | 318 assignments (plus 6 newly discovered, see §7) |

### Why this assignment was chosen over the others available

The ledger showed 23 completed reports and 319 available backlog assignments, with zero active claims. Applying the stated preference order:

**(a) Markets with zero completed entries.** 256 of the 319 backlog items sat in markets with no completed report. But most of those clustered into sectors the catalog already covers deeply. Counting completed reports by sector: architecture/engineering/construction 7, insurance 3, manufacturing and quality 3, legal 2, real estate 2, transportation 2, plus a scattering of finance and back-office markets. The sectors with **literally zero coverage** were healthcare delivery (as opposed to healthcare *billing*, which is covered by "Medical billing and revenue cycle for small practices"), education and training, marketing/creative services, and hospitality.

Healthcare delivery was the largest of those and the one where I expected the strongest practitioner evidence. Dental was the best entry point into it: ~180,000–195,000 discrete practice locations, an unusually well-documented set of external counterparties, and a large body of peer-reviewed and regulatory material to work from.

**(b) Markets where strong practitioner evidence exists online.** This turned out to be the decisive filter. Dentistry has three properties that make the handoff angle unusually researchable: state dental boards publish statutory requirements for the practice→laboratory work authorization; dental payers publish per-CDT-code documentation requirements as PDFs; and OCR has brought an unusual number of enforcement actions against dental practices specifically. There is also a small peer-reviewed literature quantifying referral-packet completeness and medical-consult response rates that has no analogue in most of the other backlog markets.

**(c) Angles that expand catalog diversity.** Completed angle counts were core-practitioner-workflow 8, back-office 5, narrow-subspecialty 5, handoffs-and-qa 5. Any angle other than core-practitioner-workflow was defensible. I chose handoffs-and-qa deliberately because a dental practice's *core* clinical workflow is the part of the market least addressable by small software — the chair-side work is clinical judgment plus imaging hardware — while the practice's boundaries with outside organizations are almost entirely paper, fax, and untracked email. The angle and the market fit each other better than the alternatives did.

**A note on what I deliberately did not claim.** "Dental billing and insurance coordination / back-office" is a separate backlog item. This report touches claim attachments because attachments are an outbound deliverable to an external reviewer, which is squarely a handoff. It does not attempt to cover posting, collections, AR aging, or fee schedules, which belong to that other assignment.

---

## 1. Market examined

### 1.1 Who is in it

| Segment | Count / figure | Source |
|---|---|---|
| Professionally active US dentists | **202,485** (2024) | [ADA HPI, US Dentist Workforce 2025](https://www.ada.org/-/media/project/ada-organization/ada/ada-org/files/resources/research/hpi/US_dentist_workforce_2025.pdf) |
| Share who are specialists | **21.2%** (≈159,562 GPs) | [ADA HPI Dentist Workforce](https://www.ada.org/resources/research/health-policy-institute/dentist-workforce) |
| Orthodontists | ~10,000 | ADA HPI |
| Pediatric dentists | 9,312 | ADA HPI |
| Endodontists | 5,685 | ADA HPI |
| Periodontists | 5,471 | ADA HPI |
| Oral & maxillofacial surgeons | 4,977 | ADA HPI |
| Prosthodontists | 3,540 | ADA HPI |
| Solo practitioners (1 location, 1 dentist) | **34%** | ADA HPI |
| Practice ownership, all dentists | 85% (2005) → **73% (2023)** | [ADA HPI, Practice Ownership Trends](https://www.ada.org/-/media/project/ada-organization/ada/ada-org/files/resources/research/hpi/practice_ownership_trends_dentistry_new_look_old_data.pdf) |
| DSO-affiliated dentists | **16.1%** overall; **27%** of those ≤10 yrs out | ADA HPI; [Becker's Dental](https://www.beckersdental.com/benchmarking/16-of-us-dentists-affiliated-with-a-dso-state-by-state-breakdown/) |
| National dental expenditures | **$189B** (2024) | [ADA HPI, The Dental Care Market](https://www.ada.org/resources/research/health-policy-institute/dental-care-market) |
| Average GP net income | **$215,320** (2025) | [ADA HPI, Trends in Dentists' Income](https://www.ada.org/resources/research/health-policy-institute/dental-practice-research/trends-in-dentist-income) |
| Commercial dental laboratories with employees | 7,800 (2004) → **~6,100** (2019) | [Group Dentistry Now](https://www.groupdentistrynow.com/dso-group-blog/current-dental-laboratory-market-trends-their-impact-on-dsos-part-1-technology/) |
| Lab cases processed annually in the US | **~35 million** | [Henry Schein DDX](https://henryscheinequipmentcatalog.com/content-library/launch-labwork-into-the-cloud-with-henry-schein-ddx) |

**Practice-count caution.** ADA HPI counts *dentists* (202,485); IBISWorld counts *businesses* (179,584 in 2026). Neither is a count of physical office locations. A defensible working estimate is **~180,000–195,000 discrete US dental office locations**, of which roughly 55,000–65,000 are specialty offices. Any market sizing in this report uses that band and says so.

### 1.2 The organization that would actually buy

The target buyer for everything in §4 is a **1–4 dentist independent practice or a small specialty practice, with 1 to 4 administrative staff**. The staffing benchmark that anchors this: McGill Advisory's ratio of **one front-desk FTE per $60,000/month of production** (average practice), rising to $75,000 at the 75th percentile and $100,000 at the 95th ([McGill via Advanced Practice Management](https://advancedpracticemanagement.com/wp-content/uploads/2018/11/MCGILL-ARTICLE-NOVEMBER-2018.pdf)). A solo GP producing $70–90k/month therefore runs on **1 to 1.5 administrative FTEs**. Total staff cost runs ~26% of collections, of which administrative staff is 6–8 percentage points.

The economic pressure that makes admin tooling interesting right now is visible in ADA HPI's own numbers: over five years, **practice revenues rose 1.4% while expenses rose 4.9%**. The only lever available to most owners is administrative labor productivity.

The user is almost never the dentist. It is the office manager, the treatment coordinator, the insurance/billing coordinator, or in a specialty office the referral coordinator. These are people who already maintain elaborate manual systems — the evidence in §2 and §3 includes several of those systems captured in the wild — and who will adopt a tool that removes a phone call, but will abandon anything that adds a login.

### 1.3 The external counterparties — the actual subject of this report

A dental practice's day is structured around five recurring handoffs to organizations it does not control:

1. **The dental laboratory** — outbound prescription + impression or scan; inbound finished restoration, materials disclosure, and point-of-origin statement.
2. **The specialist (or the referring GP, in the other direction)** — outbound referral packet with imaging and history; inbound consultation report.
3. **The dental payer** — outbound claim with radiographs, perio charting, narrative; outbound predetermination; inbound denial, request for information, and periodically an audit.
4. **The patient's physician** — outbound medical clearance/consult request; inbound (or not) labs, medication detail, and an opinion.
5. **Whoever requests the record** — the patient, the next dentist, an attorney, a payer auditor; outbound a compiled record including radiographs, under a statutory clock.

Every one of these is a package of documents assembled by hand from two or three different software systems, transmitted over a channel with no receipt, and reviewed by a stranger against rules the sender does not have in front of them.

---

## 2. How the work is performed

### 2.1 The laboratory handoff

**People:** dentist (design intent), dental assistant (usually fills out the prescription and packs the case), front desk (schedules the seat appointment and tracks the due date), lab case coordinator or technician on the receiving side.

**The artifact.** A work authorization, which is a legal document in the states that regulate it. Its content requirements vary enormously. California ([16 CCR § 1063](https://www.law.cornell.edu/regulations/california/16-CCR-1063)) requires four things: date, description of work, dentist's signature, license number. Ohio ([OAC 4715-5-02](https://codes.ohio.gov/ohio-administrative-code/rule-4715-5-02)) requires contractor name and address, patient identification, work description with diagrams, material types, date, and the dentist's **original ink signature**, license number and office address — plus a *return section* the laboratory must complete disclosing materials used, fabrication location **with FDA registration number**, subcontractors, and disinfection method. Retention is 2 years on both sides in Ohio and Mississippi, **4 years on both sides in Florida**, where lab noncompliance is a second-degree misdemeanor and the lab is civilly liable for inaccurate material or origin disclosures ([Fla. Stat. § 466.021](https://law.justia.com/codes/florida/title-xxxii/chapter-466/section-466-021/)). Washington requires labs to register with DOH, employ a CDT from Jan 2025, disclose complete material content and point of origin, and requires **the dentist to put the lab's registration number on the work order** ([RCW 70.352.030](https://lawfilesext.leg.wa.gov/Law/RCWArchive/2023/htm/RCW%20%2070%20%20TITLE/RCW%20%2070%20.352%20%20CHAPTER/RCW%20%2070%20.352%20.030.htm)).

Twelve states regulate dental laboratories at all; nine require material and/or point-of-origin disclosure (FL, IL, KY, MN, MO, NC, SC, TX, VA) ([NADL](https://dentallabs.org/state-regulation/)). A 2009 ADA survey found **nearly 65% of dentists believed technicians were regulated in their state** when they were not.

A real production Rx form ([D&S Dental, Wisconsin](https://dnsdental.com/wp-content/uploads/2021/10/rx_form.pdf)) carries roughly **60 discrete fields**: doctor identity and license, patient identity, shade, finish, try-in, a Mon–Fri grid for date *and time* to be returned, impression material and disinfectant used, a lab-use received-items checklist, an 11-option substructure material menu, minimal occlusal clearance, ridge relief, contacts, glaze level, partial framework material, denture tooth mold and acrylic color.

**Transmission.** Physical case in a box by courier or carrier, or digital. On the digital side the fragmentation is countable: [Oral Arts Dental Laboratories publishes connection instructions for **12 distinct scanner ecosystems**](https://www.oralartsdental.com/intraoral-scanners/) — 3Shape, AS Connect, Carestream Connect, CEREC/Sirona Connect, DEXIS IS Connect, DS Core, iTero Element, Medit Link, Ori, Planmeca, Shining 3D, Straumann AXS — each with a different onboarding path. One of them requires phoning the scanner manufacturer to have the lab added by ID.

A lab owner's own description of the state of play, on a public technician forum: *"We use every matching portal, 3Shape, iTero, Sirona, Medit, Dexis, Care Stream, EasyRX, and about **50% of our daily cases just get sent via email**."* Verdict on the landscape: *"A mess, if you ask me."* ([Dental Lab Network](https://dentallabnetwork.com/forums/threads/what-portal-do-you-use-for-sending-or-receiving-scans.35376/))

**Tracking on the practice side.** Open Dental and CareStack both ship lab-case modules at no additional charge, which attach cases to appointments and carry a tracking status ([Open Dental](https://www.opendental.com/site/0_labcases.html); [CareStack](https://carestack.com/dental-software/features/lab-case-management)). Open Dental's own marketing names the two canonical failures the module exists to prevent: staff need to "quickly see how many appointments for the day have labs outstanding," and cases get "forgot[ten] to attach to appointments." The defensive practice consultants teach is to put the **earliest possible** due date on the Rx and then build **a week of buffer** between arrival and the insertion appointment ([The Ultimate Patient Experience](https://theultimatepatientexperience.com/dental-business-processes-101-ordering-and-receiving-dental-laboratory-cases/)).

That a market exists for a [printable dental lab case log sheet](https://www.carepatron.com/templates/printable-dental-lab-case-log-sheet/) and a [dental lab case tracking spreadsheet template](https://www.dentallabguru.com/templates/case-tracking-spreadsheet/) is decent circumstantial evidence that a meaningful share of practices track cases outside the PMS entirely.

### 2.2 The specialist referral handoff

**The artifact is still a paper slip.** The ADA's own [sample Referral to Dental Specialist form](https://www.ada.org/-/media/project/ada-organization/ada/ada-org/files/publications/guidelines-for-practice-success/mngpatients_referral_to_specialist.pdf) is a carbon-style slip whose radiograph field is a set of checkboxes: *"Radiographs: sent with patient | mailed/transmitted | attached | **none available**."* The profession's canonical form anticipates a referral arriving with no imaging.

A periodontist quoted in *Dental Products Report*: *"For the most part, it's been the good old carbon copy, paper referral that…gets sent out."* A practice-management consultant's description of the actual eight-step process — doctor fills the slip, front office phones the specialist, follow-up reminders, chart documentation, *"scanning and emailing referral slips, x-rays, perio charts,"* chase the specialist's report, rebuild the treatment plan from insurance info, call the patient back — ends with: *"I recall spending hours alone just going back and forth on the phone with the specialist's office for all of the necessary follow ups."* ([Candice Martin Consulting](https://www.candicemartinconsulting.com/finally-a-way-to-streamline-specialty-referrals/))

**Imaging is the hard part.** The ADA formally told HHS and ONC in March 2026 that *"Dental diagnostic images are often stored in systems that operate independently of electronic dental records, restricting efficient exchange between dentists,"* naming *"reliance on proprietary formats, inconsistent implementation of the Digital Imaging and Communications in Medicine standard"* and *"fragmented exchange pathways"* as causes, and **"repeat imaging and unnecessary radiation exposure"** plus *"image quality degradation and metadata loss during transfers"* as consequences. The ADA's explanation for how dentistry got here: dentistry was excluded from the federal Meaningful Use health-IT incentive programs ([ADA News, Mar 2026](https://adanews.ada.org/ada-news/2026/march/ada-calls-for-improved-interoperability-standards-for-dental-imaging/)).

The mechanics are concrete. *Dentistry Today* names `.dex` (DEXIS) and `.jif` (Gendex) as native formats not universally readable, and its practical advice reveals the workaround culture: *"If you are unsure of the system or technical experience of the receiving doctor… send in JPEG format"* — i.e., degrade the diagnostic image to guarantee it opens. CBCT is worse: **100–500 MB per scan**, one `.dcm` file per slice. A dental laboratory that receives CBCT for surgical guides publishes a spec — *"uncompressed, multi-file, DICOM, 0.3mm or 0.4mm slices"*, files must *"remain as individual DICOM files (.dcm), not converted to viewer applications or executable files"* — and maintains video tutorials for **18+ CBCT manufacturers** because each export path is different ([ROE Dental Lab](https://www.roedentallab.com/collaboration/managing-dicoms)).

**Specialist-side intake.** Receive the packet by whatever channel; check for a legible tooth number and reason; open the imaging and verify it is openable, recent, and adequate; verify medical history and medications; verify insurance; call the referring office for anything missing; key the patient in; call the patient to schedule. Academic centers publish the turnaround this implies: the University of Minnesota's OMS clinic tells referrers to *"allow two weeks after referral submission"* before the patient may call to schedule; Iowa asks for 48 hours.

**Existing software.** Standalone referral platforms exist and are cheap — Sindi ($59/mo Pro, 500 MB attachments), Refera ($29 GP / $99 specialist, 2 GB, accepts DICOM, and critically **specialists do not need an account to receive**), RecordLinc ($47/mo), Brightsquid Secure-Mail (500 MB per message), PepCare, eDossea (free, and mandates a radiograph-date field before submission). The incumbent PMS offerings are thinner than they look: **Dentrix Ascend's "Outbound Referrals" feature marks procedures as referred and colors them purple on the odontogram** — its documentation describes no image attachment, no transmission method, and no status report coming back ([Dentrix Ascend docs](https://learn.dentrixascend.com/outbound-referrals/)). It is a tagging feature, not a handoff feature.

### 2.3 The payer handoff

**Two outbound artifacts: the claim-with-attachments and the predetermination.**

Every major payer publishes per-procedure documentation requirements, and they do not agree with each other. Delta Dental nationally requires bitewings **within 12 months** showing bone levels on both arches for scaling and root planing; Delta Dental of NJ/CT's 2025 required-documentation chart says radiographs **within 36 months** for the same codes; Aetna's global rule is **less than 36 months old**; Medi-Cal Dental uses **8 months for primary teeth, 14 months for permanent, 36 months for arch integrity**. Cigna publishes numeric clinical criteria (SRP requires pockets **≥4 mm**; osseous surgery **≥5 mm** plus a re-evaluation of non-surgical therapy generally within 3–6 months); UnitedHealthcare's guideline specifies *documents* but no numeric thresholds at all.

Delta states flatly: *"Claims submitted without the required documentation will be denied automatically."*

**How practices cope: a hand-built rules table outside the software.** The single most revealing artifact found in this cycle is a dental group's internal claim-requirements cheat sheet, publicly hosted on its own website ([Verber Dental Group, 2025](https://verberdentalgroup.com/wp-content/uploads/2025/01/Claim_Requirements_-_Supporting_Information-1.pdf)). It is a per-CDT-code grid with columns for **Narrative / Radiographs / Perio Chart / Intraoral Photo / Seat Date / Submission Notes**, containing entries like "D2950 — narrative explains why treatment is necessary. Add endo completion date," payer exceptions in capitals — **"BLUE CROSS DENTAL DOES NOT ALLOW ELECTRONIC ATTACHMENTS — CLAIMS MUST BE MAILED"** — and an internal QA rule: ***"ALL PREPPED CLAIMS NEED A CORRESPONDING CLAIM STATUS NOTE."***

That PDF is the product any attachment-completeness tool would be replacing. It is maintained by hand, specific to one practice's payer mix, and goes stale when Delta or Cigna revises a guideline, which they do roughly annually.

**Transmission.** The attachment and the claim are usually two separate objects joined by a reference number. NEA FastAttach / Vyne is the incumbent: upload images, get an NEA number, type it into the claim. Open Dental's manual notes the NEA number *"is inserted into the claim **after** the claim has been sent."* Open Dental's own attachments tab warns that attachments added there *"are for reference only and **are not sent by Open Dental**"* — they must be exported to a temp folder and sent by a third-party service ([Open Dental manual](https://www.opendental.com/manual/claimtabattach.html)). DentalXChange's ClaimConnect help documents that it *"doesn't permit attachments with initial claims unless you have a FastAttach account,"* and for MetLife describes a **print-and-mail cover-sheet loop** as the sanctioned workflow, in 2026 ([ClaimConnect help](https://claimconnect.dentalxchange.com/dci/claims/help/singleclaim/attachments.jsp)).

Dentrix (G7.3+) does automatically include required attachments and warns when one can't be found — but the rules are hand-maintained: *"as you work with different insurance payors and learn their requirements, you can customize Dentrix by adding or updating which procedures require attachments"* ([Dentrix blog](https://blog.dentrix.com/blog/2020/01/29/add-required-attachments-to-claims-automatically/)). There is no shipped, maintained payer library.

**Adoption reality.** The 2024 CAQH Index puts dental attachments at **37% fully electronic / 63% fully manual** (26 million electronic vs 45 million manual transactions), against 90% electronic adoption for dental *claim submission*. Provider cost per attachment transaction: **$5.54 manual vs $4.51 electronic**. Total dental savings opportunity: **$2.1 billion** ([2024 CAQH Index](https://www.caqh.org/hubfs/Index/2024%20Index%20Report/CAQH_IndexReport_2024_FINAL.pdf)).

**A regulatory clock is now running.** CMS finalized the HIPAA claims-attachment standard — X12N 275 v6020 plus HL7 C-CDA implementation guides — **effective May 26, 2026, with full compliance required May 26, 2028**. Prior-authorization attachments were explicitly **not** included ([CMS fact sheet](https://www.cms.gov/files/document/nsg-attachments-final-rule-fact-sheet.pdf-0)). That means the claim-attachment path is being standardized while the predetermination path is not.

**Predeterminations** are the other outbound artifact and are worse behaved. Turnaround estimates range from Delta Dental of Virginia's *"seven to ten days"* to CDA's and Dentaltown's *"four to six weeks."* Validity ranges from 60 days (preauthorization) to **90 days** (Delta VA's predetermination). None guarantee payment — the ADA is explicit that *"the benefit outlined in the preauthorization is tempered by the allowable benefits at the time of service, not the time of preauthorization submission"* — and the ADA specifically flags the **calendar-year rollover** failure, where a predetermination received in one year is stale by the time treatment begins in the next because maximums and deductibles have reset.

### 2.4 The physician handoff (medical clearance)

**When it happens.** Before oral surgery, sedation, or invasive treatment on a patient with anticoagulants or DOACs, antiresorptive therapy (MRONJ risk), recent MI/stent, uncontrolled hypertension or diabetes, high-risk cardiac conditions, or pulmonary compromise.

**The current mechanism is a fax.** Every clearance form found in the wild is a one-page PDF designed to be faxed to a physician's office — none reference a portal, a health information exchange, or Direct secure messaging. Dental PMS systems are essentially never connected to an HIE, and dentists rarely hold credentials at the physician's practice. This is close to the last fully analog interface in US ambulatory care.

**The best quantitative evidence in this entire cycle** comes from a retrospective study of **240 consult requests for 179 patients** at a dental institution over three years ([Frontiers in Digital Health 2022;4:838538](https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2022.838538/full)):

| | Requested | Actually returned |
|---|---|---|
| Laboratory / diagnostic reports | 56.3% | **34.2%** |
| Recommendations / clearance | 39.6% | **19.2%** |
| Medication information | 38.3% | 41.3% |
| Current medical conditions | 19.2% | 13.3% |

Turnaround: **57% returned within 10 days, 86% within 30 days, 14% took more than 30 days**, mean **19.6 ± 36.6 days** — a standard deviation nearly twice the mean. **About 20% of responses contained none of the requested information.** Dental providers **needed multiple contact attempts in 45% of cases.**

**What a good request contains,** per MedPro Group's risk guidance: the specific planned procedure; whether local anesthetic with epinephrine will be used; whether anxiolytics, nitrous oxide, or sedation are planned; and for anticoagulated patients, an explicit ask for **the most recent INR or PT** and an assessment of stability. *"A dentist should not rely on a patient stating that blood tests are stable."* If the physician doesn't respond, call and **document the name of the staff member and the message left** ([MedPro](https://resource.medpro.com/what-dentists-should-know-about-medical-clearance)).

**A meaningful share of this volume should not exist.** The two most commonly requested clearances are exactly the two current guidelines say are usually unnecessary. ADA/AAOS: *"In general, for patients with prosthetic joint implants, prophylactic antibiotics are not recommended prior to dental procedures."* ADA on anticoagulants: *"treatment regimens with older anticoagulants (e.g., warfarin) and antiplatelet agents… should not be altered before dental procedures,"* and for DOACs *"no change to the anticoagulant regimen is required"* in most patients. AAFP's physician-facing summary states plainly that *"stable chronic diseases rarely require physician consultation before dental treatment."*

### 2.5 The records-release handoff

**The rules.** A covered entity must act on an access request **no later than 30 calendar days** after receipt, with **one 30-day extension** available only if a written explanation is provided *within* the initial 30 days. Fees must be reasonable and cost-based: labor for copying, supplies, and postage are chargeable; **search and retrieval, administrative overhead, and vendor fees are not**. There is no fee at all for inspection without copies. The **$6.50 flat-fee option is a safe harbor, not a cap** ([HHS OCR Right to Access FAQs](https://www.hhs.gov/hipaa/for-professionals/faq/right-to-access-and-research/index.html)).

The ADA adds an ethical obligation with sharp operational teeth: a dentist must furnish records on request of the patient or the new dentist ***"whether or not the patient's account is paid in full."***

**Dental practices are conspicuously over-represented in OCR's enforcement docket:**

| Entity | Amount | Date | Facts |
|---|---|---|---|
| Great Expressions Dental Center of Georgia | **$80,000** | Sept 2022 | Records withheld pending a **$170 copying fee**; delivered ~15 months after request; fee found not reasonable and cost-based |
| Gums Dental Care, LLC (solo, MD) | **$70,000 CMP** | Oct 2024 | Requests April and June 2019; records not attempted until May 2022. Withheld over a **$25 certified-mail fee** when the patient had asked for **email** delivery. OCR found **willful neglect** |
| Family Dental Care, P.C. (IL) | **$30,000** | Sept 2022 | Partial records only; full set 5+ months late |
| B. Steven L. Hardy DDS / Paradise Family Dental (NV) | **$25,000** | Sept 2022 | Records requested April 2020, provided Dec 2020 (~8 months) |
| Elite Dental Associates (TX) | **$10,000** | Oct 2019 | Not access — a **Yelp reply** disclosing a patient's condition, treatment plan, insurance and cost |

Sources: [HIPAA Journal](https://www.hipaajournal.com/dental-practices-fined-for-hipaa-right-of-access-violations/), [Saul Ewing on Gums Dental](https://www.saul.com/insights/alert/scary-ocr-cmp-imposed-upon-solo-dental-practice), [HIPAA Journal on Elite Dental](https://www.hipaajournal.com/dental-practice-fined-10000-for-phi-disclosures-on-yelp/).

**The pattern is the important part: in four of five cases the proximate trigger was a copying-fee dispute or a partial/slow response, not a refusal in principle.** Two turned specifically on charging for a delivery method the patient never asked for.

**Why it breaks.** The request arrives by fax, voicemail, walk-in, or a general inbox — there is no queue, no clock, and no owner, and the practice often cannot prove when receipt occurred. Assembling the record is a multi-system job: chart notes from the PMS, radiographs from a separate imaging application (frequently a *different* application for intraoral vs pano vs CBCT), scanned consents from a document module. In Dentrix and Eaglesoft, **imaging is stored outside the SQL database in a separate folder structure requiring independent backup** — the chart and the images are two systems with two export paths. Dentrix users on Capterra describe imaging/X-ray transfer as *"hard and time-consuming."*

### 2.6 What software is actually installed

There is **no credible public vendor-level market-share dataset** for US dental PMS. What can be verified: Dentrix claims *"over 35,000 teams"*; Planet DDS claims 13,000+ practices; analyst reports publish no vendor splits. Directional consensus from integration-partner lists is Dentrix first, Eaglesoft second, Open Dental third and fastest-growing, then a long tail.

**The API economics are the most decision-relevant fact for anyone building here** ([Dentrix Developer Program FAQ](https://ddp.dentrix.com/pages/faq)):

- **Dentrix on-premise: $5,000 one-time for the READ API, $5,000 for the WRITE API, plus a monthly royalty** by API category.
- **Dentrix Ascend: $5,000 one-time registration, then $47/month per location**, including 30,000 calls and 3 GB; overages $0.0018/call and $1.00/GB.
- **Prohibited categories for third-party developers: patient financing, credit card processing, and insurance claim processing.** Henry Schein One explicitly fences off the revenue-cycle categories it competes in.
- Henry Schein One's public vendor page prominently lists **~60+ *unauthorized* vendors** — a naming-and-shaming posture toward companies reading the database directly, and indirect evidence of a large gray market of direct-SQL readers.

**Open Dental is the opposite.** A REST API with **80+ resource endpoints** (Patients, Appointments, Procedures, TreatPlans, Claims, InsPlans, Benefits, Carriers, Documents, PerioExams, Diseases, MedicationPats, SecurityLogs…), two-key auth, onboarding by plain email to vendor relations, a **free test database**, a MySQL back end with direct database access, and fully public office pricing ($199/mo/location for 12 months, then $149) ([API setup](https://www.opendental.com/site/apisetup.html), [spec](https://www.opendental.com/site/apispecification.html), [fees](https://www.opendental.com/site/fees.html)). Planet DDS launched an open API program in July 2024 with writebacks and webhooks but no public pricing.

**Implication for every concept in §4: build Open Dental first, Denticon second, Dentrix on request.** And note that anything touching claim submission is structurally harder on Dentrix by contract, not by technology.

---

## 3. Most important problems, ranked

### Problem 1 — The medical clearance request is a fax into a void, and the reply usually doesn't answer the question

**Who:** any practice doing oral surgery, extractions, implants, periodontal surgery, or sedation. Disproportionately OMS, periodontics, and GPs who place implants.
**When:** before scheduling an invasive procedure on a medically complex patient. For an OMS office, several times a week.
**Currently handled:** a one-page fax PDF, followed by phone calls.
**Why inadequate:** clearance was specifically requested in 39.6% of consults and specifically returned in **19.2%**. Roughly **20% of replies contained none of the requested information**. **45% required multiple contact attempts.** Mean turnaround 19.6 days with a standard deviation of 36.6.
**Cost:** the direct cost is staff time chasing — plausibly 20–40 minutes per consult across attempts. The larger cost is a deferred or cancelled surgical appointment, which for an OMS is an hour of surgical block. The tail risk is a malpractice claim: MedPro cites cases where a missing clearance preceded anticoagulant bleeding complications, undisclosed pulmonary disease after sedation, cardiac arrest, and seizure activity.
**Evidence quality:** **strong.** One peer-reviewed retrospective study with per-item request/return rates, plus a malpractice carrier's published guidance on what a proper request must contain.

### Problem 2 — Payer documentation requirements are heterogeneous, unversioned, and re-learned practice by practice

**Who:** the insurance/billing coordinator in every insurance-participating practice.
**When:** at every claim for a major or basic service, and again at every denial.
**Currently handled:** a hand-maintained PDF or spreadsheet of per-code, per-payer requirements, owned by one person; supplemented by Dentrix's office-maintained attachment rules; or outsourced entirely.
**Why inadequate:** the rules genuinely conflict across payers and even within a payer brand (Delta national's 12-month bitewing window vs Delta NJ/CT's 36-month window for the same codes). They change roughly annually. No PMS ships a maintained payer-specific rules library; clearinghouse validation checks *file format and carrier eligibility*, not *clinical completeness for this code under this plan*. And the linkage failure is separately documented: *"A surprising number of 'missing X-ray' denials happen because the attachment was uploaded but not correctly associated"* with the claim.
**Frequency:** continuous. Roughly 71 million dental attachment transactions per year, 63% still fully manual.
**Cost:** MGMA's figure of **~$25 rework per denied claim** and **50–65% of denied claims never reworked** is the defensible pair. Zentist's Feb 2026 survey of 160+ dental RCM professionals found **78% report denials and payer scrutiny increased in the past 12 months** and **71% name insurance verification as their top operational challenge**. The retroactive tail is real: a Texas HHS OIG dental settlement of **$66,804** (roughly half penalties) plus a **2-year Medicaid exclusion**, driven by *"poor quality and non-diagnostic X-rays, missing or incomplete documentation"* and failure to produce **86 of 120 requested records**. Commercial payers offset unrecovered overpayments directly against future claims after 90 days.
**Evidence quality:** **strong on requirements and mechanism; weak on the specific share of denials attributable to documentation.** A cluster of very specific-sounding statistics (19.3% first-submission denial rate, 18% of denials from missing documentation, $117 rework cost) circulates across dental-AI vendor blogs; traced to origin, the source page cites no studies and the $117 figure conflicts with MGMA's $25 by nearly 5×. **Those numbers should not be used.** That a defensible documentation-share-of-denials figure does not exist is itself a finding.

### Problem 3 — Referral packets arrive incomplete, and the imaging that does arrive is often not diagnostically adequate

**Who:** specialist front desks (receiving); GP front desks (assembling).
**When:** every outbound referral. US per-GP referral volume is unmeasured, but 53% of GPs now refer root canals to endodontists, and the average endodontist sees ~1,930 referred patients/year.
**Currently handled:** paper slip plus a separate scan-and-email of radiographs, or the patient carries it.
**Why inadequate:** the best dataset is a Swedish audit of **1,891 oral surgery referrals** ([CCIDE 2017](https://www.dovepress.com/article/download/35616)):

| Element | Missing or inadequate |
|---|---|
| Tobacco use | 90.1% absent |
| Allergies | 71.8% absent |
| Previous treatment | 63.6% absent |
| Current medication | 60% absent |
| **Adequate radiographs** | **53.4% inadequate** |
| Presenting complaint | 40% absent |
| Radiographs missing entirely | 9.8% |

**Note the shape:** radiographs usually arrive (only 9.8% missing) but are **inadequate more than half the time**. This is a QA problem, not a transport problem — and every referral platform in the market competes on file-size caps (50 MB → 500 MB → 2 GB), not on adequacy. The audit's own recommendation is exactly the product spec: *"electronic referral systems should only allow for submission once all of the essential information has been considered."*

Corroborating from the receiving side: a 2025 BDJ service evaluation of **673 periodontal referrals** found **160 (23.8%) rejected at triage, 93% of them for "insufficient clinical information"** ([BDJ 2025](https://www.nature.com/articles/s41415-025-9047-y)). And a 2002 BDJ study found a structured proforma produced a **29.3% increase in information provided** over free-text letters.

**Cost:** up to **20 minutes of staff time** per referral when the receiving office must contact the referring dentist or the patient for missing information, vs ~3 minutes for a complete electronic referral. A retaken radiograph is unnecessary radiation, which the ADA has now named to HHS. The tail risk is documented and severe: MedPro's published case of a phone-only referral for *"upper right #8"* — the central incisor in the Universal system, the third molar in Palmer — with no written referral and no radiographs, resulting in **extraction of the wrong tooth**.
**Evidence quality:** **strong** (peer-reviewed audits on both sides, a carrier case study), with the caveat that the largest audits are non-US.

### Problem 4 — Lab prescriptions omit the design-intent fields, and nobody measures it

**Who:** dental laboratories (receiving), assistants and dentists (sending).
**When:** every case. ~35 million lab cases/year in the US.
**Currently handled:** paper Rx or a scanner-portal order form; clarification by telephone.
**Why inadequate:** the omissions are systematic and specific. A technician survey (85 labs) found **69% of work authorizations lacked preferred margin design**, **56% did not specify pontic design**, **51.2% did not say whether a try-in was required**, and **60.7% said fewer than 25% of forms arrived with photographs** ([PMC7335025](https://pmc.ncbi.nlm.nih.gov/articles/PMC7335025/)). A dentist-side survey (n=453) found shade not selected on **44.6%**, alloy type unspecified on **46.7%**, and *"nearly 43% of dentists did not draw the design of the restoration"* ([Appl. Sci. 12(12):6263](https://www.mdpi.com/2076-3417/12/12/6263)). A UK survey of 248 labs found the two most commonly omitted items were **shade and date required**, that 13% of labs had to contact dentists for clarification — but **22% among the labs that answered from records rather than memory** ([BDJ 2014](https://www.nature.com/articles/sj.bdj.2014.643)).

The consistent cross-study signal: **the fields that get skipped are the design-intent fields, not the identity fields.** Patient name and signature are nearly always present because they are on the legal checklist. This is exactly the pattern you get when a form is filled under time pressure with a compliance-shaped mental model of "complete."

Digital has added a new failure mode rather than removing one. Implant scan-body library version mismatches produce documented **0.1–0.2 mm platform offsets**, and mixing scan body / Ti-base / implant brands produced a documented **0.5 mm screw channel displacement** — and essentially none of the required fields (scan body brand, SKU, height, lot, library name and version) exist on a conventional Rx form ([Associated Dental Lab](https://associateddl.com/scan-body-libraries-version-control-brand-mixing-accuracy-traps/)).

**Cost:** the prospectively measured single-unit crown remake rate is **3.8%** across 3,750 crowns ([PMC7005880](https://pmc.ncbi.nlm.nih.gov/articles/PMC7005880/)); labs consider **10% remake-or-significant-adjustment** normal ([Glidewell](https://glidewelldental.com/company/blog/how-to-reduce-crown-remake-rates-and-recover-lost-chair-time)). LMT's 2024 survey found *"over 80% of external remakes are attributed to dentist error,"* stable across the 2011, 2018 and 2024 surveys, with inadequate impressions and incorrect shade specification the primary causes. On the practice side the cost is chair time: a 20-minute adjustment ≈ **$125** of lost revenue, a 30-minute recall ≈ **$187.50**, against practice overhead of roughly **$375/hour**; Glidewell computes that a 15-crown-per-week practice at a 10% rate loses ~75 cases and **~40 hours per year — a full clinical week**.

**The asymmetry is why this never gets fixed:** the lab's remake cost is bounded (materials + tech hours, self-insured at 3–5% of revenue) while the practice's cost is chair time plus a patient in the chair twice — and that cost appears in no lab KPI. Each side measures the other, which is why "80% dentist error" (lab survey) and "laboratory error most common" (clinician survey) coexist.

**Evidence quality:** **strong on omission rates and remake rates; weak on US-specific Rx completeness.** The two best field-by-field datasets are from India and Pakistan; the UK BDJ survey is the strongest Western dataset. The widely repeated claim that *"80% of dentists do not complete the information legally required on the prescription form"* is a US claim with **no traceable source** and should not be cited.

### Problem 5 — Lab cases and the appointment schedule drift apart, in one direction only

**Who:** front desk and the seating dentist; the lab.
**When:** whenever a patient reschedules, or a case runs late.
**Currently handled:** PMS lab-case modules where they exist; whiteboards, printed log sheets and spreadsheets where they don't; a week of deliberate schedule buffer as defense.
**Why inadequate:** every system found pushes lab status **to** the practice. **Nothing found pushes "the patient moved to the 22nd" back to the lab.** A practice consultant's symptom list reads like a bug report: *"Doctor always has to ask if the case is here"*; *"Patient scheduled and product has not been delivered from lab"*; *"Vital information about the prescription is missing from the patient's chart"* ([Desergo](https://desergo.com/blog/9-smart-ways-to-improve-your-dental-lab-case-management-system)). The consultant's opening anecdote is a patient arriving for a sedated extraction and immediate denture whose prosthetic had not arrived.
**Cost:** a wasted seat appointment is 45–60 minutes of chair time (~$280–$375 at typical overhead) plus a patient inconvenienced. Henry Schein's 2011 DDX survey found **35% of DDX-enabled practices attributed reduced patient rebookings to it**, and DDX-enabled labs reported an **~30% reduction in staff phone time** — the only sourced figure available on lab phone burden.
**Evidence quality:** **moderate.** Vendor marketing frames the problem consistently; consultant content treats a week of buffer as necessary; commercial log-sheet templates sell. No published study quantifies the rate of seat appointments without a case.

### Problem 6 — Records requests have a statutory clock and no queue

**Who:** office manager or front desk.
**When:** a few times a month in a small practice; more in a practice with turnover or active litigation.
**Currently handled:** ad hoc. A fax lands, someone remembers.
**Why inadequate:** the 30-day clock starts on receipt and the practice frequently cannot prove when receipt occurred. Fee logic is the number one enforcement trap — staff apply a habitual per-page or flat records fee without distinguishing paper copying from electronic delivery and without knowing that search/retrieval and unrequested-delivery charges are prohibited. Balance holds persist despite being contrary to both the right of access and ADA ethics. And **no dental PMS ships a records-request queue with an SLA timer.**
**Cost:** the enforcement record is unambiguous — **$80,000, $70,000, $30,000, $25,000** in four dental right-of-access actions, with the $70,000 case turning on a **$25 mailing fee applied to an email request**. Ordinary-course cost is smaller but real: assembling a record across PMS, imaging, and document systems is 30–90 minutes.
**Evidence quality:** **strong** (federal enforcement actions with amounts, dates, and published facts; OCR fee guidance is explicit).

### Problem 7 — Predeterminations expire, reset, and are matched to claims by hand

**Who:** treatment coordinator and billing coordinator.
**When:** on any treatment plan above roughly $250 — Delta Dental of Virginia's own stated trigger.
**Currently handled:** a manual log or a tickler, plus carrying a reference number forward from a document generated weeks earlier.
**Why inadequate:** predeterminations take 7–10 days to 6 weeks, are valid 60–90 days, are non-binding, and **reset at the plan year**. MetLife requires the predetermination reference number as an attachment on the eventual claim, and Delta Oregon's submission process leaves procedure dates blank on the predetermination form — meaning the predetermination and the eventual claim are literally different documents with no shared key beyond what staff carry forward. **No PMS or clearinghouse feature was found that reconciles an approved predetermination against the eventual claim or flags one approaching expiry or crossing a plan year.** Note also that the 2026 CMS attachments rule explicitly excluded prior authorization — regulation is not coming to fix this.
**Cost:** patient attrition during the wait (Dentaltown: during 4–6 weeks *"patients often lose interest or reconsider treatment plans"*), plus the harder failure of treatment delivered against a stale approval. Dentaltown documents a case where an insurer stated 50% coverage of a $5,000 plan when the actual annual maximum was $1,000, and the patient refused treatment.
**Evidence quality:** **moderate to strong on mechanism; the absence of an existing feature is "no evidence found," not proven absence.**

### Problem 8 — Radiographs and CBCT volumes cannot reliably be opened by the recipient

**Who:** whoever sends imaging out — to a specialist, a lab, an insurer, or a patient.
**When:** every referral, every surgical-guide case, every records release involving imaging.
**Currently handled:** burn to CD/USB with a bundled viewer executable; zip the DICOM folder to Dropbox or WeTransfer; or export to JPEG and email.
**Why inadequate:** each path has a distinct failure mode. Optical media assume a drive the receiving office no longer has and an `.exe` its IT may block. Cloud links raise HIPAA exposure and expire. JPEG is the only one that reliably opens — and it irreversibly degrades the diagnostic image, which is why it persists. Practitioner voice on the underlying lock-in: *"some devices are privet [sic] tagged and can not be viewed by any other software but it's own"*; on crippled bundled viewers: *"The Simplant viewer only allows you to look at the scan but cannot add IAN or place implants."* Endodontists now publish "how to open the scan I'm sending you" instruction pages.

The standards pipeline exists but is early: ANSI/ADA Std. No. 1114 (DICOM conformance for dentistry) was out for public comment through December 2025, and dentistry's **first full record exchange via HL7 FHIR happened at a Connectathon in September 2024**.
**Cost:** a re-request cycle, a retaken radiograph, or a rescheduled appointment.
**Evidence quality:** **strong** (ADA's own submission to HHS/ONC; a receiving lab's published spec with named failure modes; practitioner forum voice).

### Problem 9 — The referral loop does not close, and the money says it matters

**Who:** the referring GP (production and liability) and the specialist (revenue).
**Currently handled:** hope, plus a phone call if someone remembers.
**Why inadequate:** in general healthcare, **up to 50% of referrals are not completed**, and *"while 70 percent of referring physicians said they sent patient histories, less than 35 percent of specialists reported receiving them"* — a 35-point perception gap. **20–30% of diagnostic errors** are attributed to breakdowns in the referral process ([The Doctors Company](https://www.thedoctors.com/articles/patient-safety-in-dentistry-communication), citing Weiner et al., O'Malley & Reschovsky, and Singh et al.). Dental-specific: paper referrals show a **30–40% failure rate for patient follow-through**. The frequently cited "46% of dental specialist referrals go unfulfilled, at $953–$5,150 per unfulfilled referral" figure is **from 2008 Kelton Research with no disclosed sample size** and must be dated when used.

Meanwhile the AAE's 2009 GP survey (n=983) found **96% of GPs rate "timely follow-up of reports and film" as an effective relationship-builder — the highest-rated item in the survey.**

**A non-obvious asymmetry worth stating:** the loop most likely to close is the one where the *specialist* has commercial incentive. Specialist→GP reports probably arrive more reliably than GP→specialist packets do, because the report is the specialist's primary marketing instrument. The failure runs *with* the direction of the referral, not against it.
**Cost:** lost production on both sides; documented malpractice exposure for failure to document and follow up a referral.
**Evidence quality:** **moderate.** The strongest statistics are general-healthcare, not dental. The dental-specific numbers are old or vendor-sourced.

---

## 4. Application opportunities

Nine concepts. Complexity is rated relative to a solo developer or a two-person team: **small** ≈ 2–6 weeks to a usable v1; **medium** ≈ 2–4 months.

A structural note that applies to all of them: **the integration path is Open Dental first.** Its REST API has 80+ endpoints, onboarding is an email, and a free test database is provided. Dentrix costs $5,000–$10,000 up front plus royalties and **contractually prohibits third-party insurance claim processing**. Any concept below that touches claims is therefore effectively Open-Dental-and-Denticon-first regardless of technical merit.

---

### C1 — Clearance Request Builder & Reply Tracker

**Working title:** *ClearanceDesk*
**Intended user:** OMS, periodontal and implant-placing GP practices; the surgical scheduler or office manager.
**Problem solved:** the dentist asks a physician a vague question by fax and gets, 19.2% of the time, the answer they asked for.

**Current workflow:** staff pull a generic one-page clearance PDF, hand-write the patient name and a sentence about the procedure, fax it, and put a sticky note on the monitor. If nothing comes back in a week or two, someone calls. Mean turnaround 19.6 days; 45% need multiple attempts; 20% of replies are empty.

**Proposed workflow:** the user picks the planned procedure and the patient's flagged conditions from a short list. The tool (a) runs a **guideline pre-check** — if the only trigger is a prosthetic joint or stable warfarin, it says so and cites the ADA/AHA position rather than generating a request; (b) if a request is warranted, generates a **structured one-page form with named answer slots** the physician fills in — INR value *and* draw date, A1C value *and* date, antiresorptive drug/dose/route/duration, "is the patient stable for a 60-minute procedure under local with epinephrine: yes/no," "sedation planned: nitrous / oral anxiolytic / IV" — rather than a blank "please advise"; (c) opens a tracked item with a due date, escalation reminders at 7 and 14 days, and a contact log that records who was called and what was said; (d) on reply, checks whether each requested slot was actually filled and flags the ones that weren't.

**Required inputs:** patient name/DOB, planned procedure, anesthesia plan, flagged medical conditions and medications, physician name and fax/email.
**Expected outputs:** a printable/faxable structured request; a tracked request record; a reply-completeness check; a chart-ready documentation note including all contact attempts.

**Essential features:** procedure→question templates for the ~12 common triggers; the guideline pre-check table; the tickler with escalation; the contact log; a one-page audit summary that satisfies MedPro's documentation guidance.
**Deliberately excluded from v1:** actually sending faxes (print or export a PDF and let the office's existing fax or eFax handle it); any HIE or Direct messaging integration; physician-side portal; e-signature.

**AI:** *optional, and not in v1.* The guideline pre-check is a lookup table over ~12 conditions, not a reasoning problem, and a table is auditable in a way a model is not. AI has one credible later use: parsing a returned free-text reply to detect which requested items it actually contains. That is a nice-to-have on top of a manual checkbox.

**Would a spreadsheet suffice?** Partially — a spreadsheet can hold the tickler. It cannot generate the structured form, cannot hold the guideline table in a usable way at the point of decision, and produces no chart-ready documentation artifact. The value is concentrated in the *form generation* and the *documentation output*, not the list.

**Complexity:** small-to-medium. **Learning difficulty:** ~15 minutes; the interface is "pick procedure, pick conditions, print."
**Value:** eliminates a meaningful fraction of the 45% of consults requiring repeat contact by making the reply fillable; removes guideline-obsolete requests entirely; produces the documentation a malpractice carrier explicitly asks for.
**Risks and constraints:** the guideline table is clinical content and must cite its sources and carry a "not clinical advice; verify against current ADA/AHA guidance" disclaimer. Guidelines change — the table needs a visible version and date. PHI is present, so a local-first or self-hosted deployment is strongly preferable; a cloud version needs a BAA.
**Existing products/substitutes:** free clearance form PDFs from a hundred practice websites; general practice-management ticklers. **No product was found that addresses medical clearance as a workflow.** Every AI dental product maps to radiographs, phones, verification, notes, or marketing.
**Why still attractive:** the failure is quantified in peer-reviewed literature, the fix is a form and a timer, and nobody is in the category.
**Paid customization:** per-specialty question libraries; a practice's own physician directory with preferred fax numbers; hospital-specific clearance forms for OMS practices with privileges; integration to pull the medication list and conditions from Open Dental's `MedicationPats` and `Diseases` endpoints.

---

### C2 — Claim Attachment Completeness Gate

**Working title:** *ClaimGate*
**Intended user:** insurance/billing coordinator in an insurance-participating practice; also outsourced dental billing companies as a per-seat tool.
**Problem solved:** the hand-maintained per-payer, per-code documentation cheat sheet.

**Current workflow:** the coordinator consults a PDF or spreadsheet built by a predecessor, checks whether the radiograph exists and is recent enough, writes or pastes a narrative, uploads images to NEA or DentalXChange, and types the reference number into the claim. Delta says the claim is auto-denied if documentation is missing.

**Proposed workflow:** before submission, the tool takes the claim's CDT codes, tooth numbers, dates of service, and the patient's plan, and produces a **per-claim requirements checklist** from a maintained rules corpus: radiograph type required (PA vs BW vs pano, and whether pano is an acceptable substitute for this payer), currency window (12 / 24 / 36 months / 8 or 14 months for Medi-Cal), perio charting site count and threshold values, narrative required elements (does this payer want percent of tooth structure lost? the endo completion date? the seat date? prior SRP dates?), and dependent dates. It checks what the chart actually contains, and flags what's missing **before** submission rather than after denial.

**Required inputs:** claim lines (CDT, tooth, surface, DOS), payer and plan identifier, and read access to imaging dates and perio exam data.
**Expected outputs:** a pass/fail checklist per claim; a list of specific missing items in the words the payer uses; an exportable pre-submission audit log.

**Essential features:** the rules corpus (YAML or JSON, versioned in git, one file per payer, with a source URL and effective date on every rule — this is the actual product); the claim evaluator; a radiograph-currency check against imaging dates; a narrative element checker (regex/keyword against required elements, not generation).
**Deliberately excluded from v1:** narrative *writing*; transmitting anything; posting or AR; eligibility verification; any payer whose rules aren't published.

**AI:** *optional and secondary.* The gate itself must be rules — an auditable rule with a source URL is worth more than a probabilistic judgment when the downstream consequence is a denial or an audit. AI is defensible for one narrow job: drafting the narrative *scaffold* from the chart's measurements. Note the live tension — eAssist warns that *"a cookie-cutter narrative template may be a red flag to a claim examiner,"* while the entire industry distributes template libraries. The real requirement is a template populated with patient-specific measurements, which is exactly the AI shape and exactly the audit-flag risk.

**Would a spreadsheet suffice?** No, and the proof is that practices already use one and it fails — it goes stale, it lives with one person, and it cannot look at whether *this* patient's bitewing is 14 months old.

**Complexity:** medium. **Learning difficulty:** ~30 minutes for the checklist; ongoing effort is in trusting it.
**Value:** at MGMA's ~$25 rework per denied claim, with 50–65% of denials never reworked, a practice that prevents a handful of documentation denials a month pays for the tool many times over. The larger value is audit posture — the Texas OIG settlement was $66,804 plus a two-year exclusion, driven by documentation.
**Risks and constraints:** the corpus is a maintenance commitment; a stale rule is worse than no rule, so every rule needs a visible effective date and source link. **Henry Schein One prohibits third-party insurance claim processing integrations on Dentrix** — this is a contractual, not technical, barrier and must shape go-to-market. The 2026–2028 CMS attachments transition (X12 275 v6020) will replatform the transport layer underneath this, which is an opportunity, not a threat, since the gate operates above transport.
**Existing products/substitutes:** Dentrix's office-maintained attachment rules; DentalXChange/Denticon format validation; VideaHealth ClaimsAI and Overjet (image selection and narrative generation); eAssist and Dental Claim Support (human expertise at $1,400/month or 2.5–3.5% of collections). Each solves an adjacent slice. **None was documented to ship a maintained, payer-specific, code-level completeness gate.**
**Why still attractive:** the outsourcers' actual moat is a maintained payer-rules corpus plus labor. An open corpus attacks the corpus half directly, and it is the kind of asset that gets better from community contribution — a practice that learns Blue Cross won't take electronic attachments can submit that as a pull request.
**Paid customization:** building a practice's specific payer mix into the corpus; importing an existing cheat-sheet PDF; DSO-wide deployment with per-region payer sets.

---

### C3 — Lab Case / Schedule Reconciler

**Working title:** *SeatCheck*
**Intended user:** front desk and office manager; a solo practice's single administrative person.
**Problem solved:** the patient arrives and the case isn't here — or the case arrives and nobody scheduled the patient.

**Current workflow:** a lab-case module if the PMS has one, a whiteboard or printed log if not, plus a deliberate week of schedule buffer as insurance.

**Proposed workflow:** a small daily job that reads lab cases and appointments from the PMS and emails or prints a four-part exception report:
1. **Seat appointments in the next N days with no case received** — the one that costs chair time.
2. **Cases received with no scheduled appointment** — the one that costs production.
3. **Cases past their due date with no receipt logged** — the one that requires a call to the lab.
4. **Appointments rescheduled or cancelled since the case was sent** — with a one-click "notify the lab" email, because *nothing in the market pushes this direction.*

**Required inputs:** read access to the PMS lab-case table and appointment table (Open Dental exposes both), plus lab contact emails.
**Expected outputs:** a daily exception list; a pre-drafted reschedule notice to the lab; a weekly on-time-delivery summary per lab.

**Essential features:** the four exception queries; configurable lead-time window; the lab-notification email; per-lab on-time statistics accumulated over time — a metric labs themselves are not measuring (8&9 Consulting's argument is precisely that labs do not track customer-facing compliance).
**Deliberately excluded from v1:** case status polling from lab portals; anything that requires the lab to adopt software; shipping/tracking integration; a case-tracking UI to replace the PMS module.

**AI:** *inappropriate.* This is four SQL queries and a mail merge. Adding a model would add cost, latency, and failure modes to something whose entire value is that it is boring and correct.

**Would a spreadsheet suffice?** Only if someone retypes both lists daily, which is the current state and is why it fails. The value is that it runs unattended and compares two systems of record.

**Complexity:** small. **Learning difficulty:** near zero — the output is an email.
**Value:** the clearest ROI in this report. One prevented wasted seat appointment is 45–60 minutes of chair time at roughly $375/hour of overhead. Henry Schein's DDX survey found 35% of practices attributed reduced rebookings to better lab-case visibility.
**Risks and constraints:** minimal. PHI in the exception report means it should be delivered internally, not to a personal email. The reschedule notice to the lab should carry the case number and date only, not clinical detail.
**Existing products/substitutes:** Open Dental and CareStack lab-case modules (which cover exceptions 1–3 partially, if staff actually attach cases to appointments — Open Dental's own blog says they forget); Henry Schein DDX (free to dentists, Dentrix-anchored, 15 years old); printable log sheets and spreadsheet templates.
**Why still attractive:** it works *because* staff forget to attach cases — the exception report catches the omission the module depends on. And exception 4, the practice→lab direction, appears genuinely unserved.
**Paid customization:** per-lab SLA thresholds; multi-location rollups; adding the lab's own tracking numbers; a lab-side version sold to laboratories that want to give their accounts the report.

---

### C4 — Right-of-Access Request Register

**Working title:** *AccessLog*
**Intended user:** office manager or HIPAA privacy officer in a 1–10 person practice.
**Problem solved:** a statutory 30-day clock with no queue, and a fee policy that has produced four federal enforcement actions against dental practices.

**Current workflow:** a fax lands, or a patient calls, or an attorney's letter arrives. Someone starts assembling. Nobody records the receipt date. Someone applies a habitual copying fee.

**Proposed workflow:** log the request the moment it arrives — requester, relationship, records requested, **delivery format requested**, receipt timestamp. The tool computes the 30-day due date, warns at day 20, and generates the **extension letter** (which is only valid if sent within the initial 30 days). A **fee calculator with guardrails** computes a permissible charge: labor for copying and supplies and postage yes; search and retrieval, administrative overhead, and vendor fees no; **no delivery charge for a method the requester didn't ask for**; offers the $6.50 flat-rate safe harbor; and blocks a fee entirely when the request is for inspection only. It refuses to let the user mark a request "held for balance" without displaying the ADA ethical obligation and the access rule. On fulfillment it logs what was sent, how, and when.

**Required inputs:** typed request details; optionally a scan of the request form.
**Expected outputs:** a live queue with due dates; a compliant extension letter; a fee worksheet showing the basis for every charge; a delivery log; an exportable register for a privacy audit.

**Essential features:** the clock; the fee guardrails; the extension letter; the delivery log; a records-assembly checklist (chart notes / radiographs / consents / referral letters, per the ADA's definition of the dental record).
**Deliberately excluded from v1:** actually assembling or transmitting records; identity verification; state-by-state retention rules beyond a configurable value; anything resembling a document management system.

**AI:** *inappropriate.* Statutory deadlines and fee rules are exactly the domain where a deterministic rule with a citation beats a model. A wrong answer here costs $70,000.

**Would a spreadsheet suffice?** A spreadsheet can hold the dates. It cannot generate the extension letter, cannot enforce fee logic at the moment staff are about to quote a number to a patient, and produces no register. Note that in the Gums Dental case the practice had three years and still didn't act — the binding constraint is not calculation, it is that nothing is watching.

**Complexity:** small. **Learning difficulty:** ~10 minutes.
**Value:** insurance-shaped rather than time-saving, and that should be stated honestly. The expected value is dominated by tail risk: $25,000 to $80,000 per enforcement action, four of them against dental practices, with the largest turning on a $25 fee. Secondary value is real but modest — 30–90 minutes saved per request in assembly coordination, plus not having a fee argument at the front desk.
**Risks and constraints:** it must not be presented as legal advice. Fee rules have state overlays. The register itself contains PHI-adjacent metadata and should be local or self-hosted.
**Existing products/substitutes:** generic release-of-information vendors serving hospitals (priced and scoped for institutions); nothing dental-sized. **No dental PMS ships a records-request queue with an SLA timer.**
**Why still attractive:** it maps one-to-one onto every published OCR dental case, it is genuinely small, and it is the kind of thing a practice adopts after reading about a $70,000 penalty — a marketing hook that writes itself.
**Paid customization:** state retention rules; practice letterhead and fee schedule; multi-location registers for a group; an attorney-request variant with subpoena handling.

---

### C5 — Predetermination Register

**Working title:** *PredetWatch*
**Intended user:** treatment coordinator; billing coordinator.
**Problem solved:** approvals that expire, reset at the plan year, or never get matched to the eventual claim.

**Current workflow:** a manual log, a tickler, or nothing. The reference number is carried forward by memory or by a note in the chart.

**Proposed workflow:** log each submitted predetermination with payer, patient, planned codes, submission date, and the payer's stated validity window. On approval, record the reference number and the approved amounts. The register then does three things nothing else does: **counts down to expiry** with a warning at 30 and 7 days; **flags any predetermination whose validity window crosses a plan-year boundary**, because maximums and deductibles reset; and **flags divergence** when the treatment actually scheduled no longer matches the approved code set. At claim time, it surfaces the reference number to be attached.

**Required inputs:** predetermination submissions and responses (typed, or parsed from the payer's letter); the patient's plan-year boundary.
**Expected outputs:** an aging register; expiry and plan-year alerts; a divergence flag; a claim-time reference-number prompt.

**Essential features:** the register; the three alerts; per-payer default validity windows (60 days preauth, 90 days for Delta VA's predetermination, configurable); a stale-predetermination report for the treatment coordinator's follow-up calls.
**Deliberately excluded from v1:** submitting predeterminations; eligibility verification; benefit breakdowns; any attempt to predict approval.

**AI:** *inappropriate for the register.* Optionally useful later for extracting reference numbers and approved amounts from scanned payer letters — that is OCR plus extraction, and is a v2 convenience, not the product.

**Would a spreadsheet suffice?** Closer here than anywhere else in this report, and that should be conceded. A disciplined coordinator with a good spreadsheet gets most of the value. What the spreadsheet doesn't do is know the plan-year boundary, know each payer's default validity window, or notice that the scheduled treatment drifted from the approved codes. The honest positioning is "a spreadsheet with the three rules that matter built in," which is a modest but real claim.

**Complexity:** small. **Learning difficulty:** ~15 minutes.
**Value:** prevents treatment delivered against a stale approval and gives the treatment coordinator a call list that is currently improvised. Note that **CMS explicitly excluded prior-authorization attachments from the 2026 standard**, so no regulatory relief is coming.
**Risks and constraints:** validity windows vary by payer and are sometimes unpublished; the register must present them as *the practice's configured value*, not as authoritative.
**Existing products/substitutes:** none found. Every source describes tracking as a manual log or tickler. This is stated as "no evidence found," not proven absence.
**Paid customization:** payer-specific windows for a practice's mix; integration to pull the treatment plan from the PMS and diff it against the approved codes.

---

### C6 — Lab Rx Design-Intent Gate

**Working title:** *RxComplete*
**Intended user:** dental assistant filling out the prescription; the dentist signing it; secondarily the laboratory receiving it.
**Problem solved:** the legal core of the work authorization gets filled in; the design-intent fields — margin design, pontic design, occlusal clearance, shade, try-in, due date — do not.

**Current workflow:** a paper form or a scanner-portal order screen. The assistant fills the identity fields; the design fields get skipped under time pressure; the lab calls.

**Proposed workflow:** a structured Rx builder organized around the *restoration type*, not around the form. Choosing "zirconia crown, tooth #19" surfaces exactly the fields that matter for that restoration and marks them required: margin design, occlusal clearance, contacts, glaze level, shade **with a prompt to attach a photo including the shade tab in frame**, try-in required yes/no, and a due date *and time*. For implant cases it surfaces the fields that don't exist on any conventional form: implant system and platform, **scan body brand / SKU / height / lot with a photo of the packaging**, scan body library name and version, planned Ti-base, torque and driver. It will not produce a signed authorization until required fields are answered — which is precisely the recommendation the largest published referral audit made about referral systems, applied here. It then renders a work authorization that satisfies the sending state's statutory content requirements, retains a copy per that state's retention period, and files the returned materials disclosure against the case.

**Required inputs:** restoration type, tooth numbers, patient and doctor identity, laboratory identity (including the lab's registration number where the state requires it on the work order, as Washington does).
**Expected outputs:** a printable/PDF work authorization; a structured record retained per state rules; a case file that later holds the returned materials and point-of-origin disclosure.

**Essential features:** restoration-type field templates; the completeness gate; state content and retention profiles for the ~12 regulating states plus a generic profile; photo attachment; the returned-disclosure filing slot.
**Deliberately excluded from v1:** transmitting scan files (the scanner ecosystems own that and will not be dislodged); lab production management; billing; any attempt to be a lab management system.

**AI:** *optional and marginal.* Shade selection from a photograph is a real research area but is a clinical claim with a device-regulation shadow, and belongs nowhere near a v1. Everything the gate does is a required-field rule.

**Would a spreadsheet suffice?** No — the output is a legal document with state-specific content requirements and a retention obligation, and the value is in conditional field logic that a spreadsheet cannot express cleanly.

**Complexity:** medium. **Learning difficulty:** ~30 minutes for an assistant; the field vocabulary is already familiar.
**Value:** attacks the documented omissions directly — 69% missing margin design, 56% missing pontic design, 51.2% missing try-in instruction, 44.6% missing shade. If it moves the crown remake-and-adjustment rate even modestly, the practice-side value is chair time at ~$375/hour, and Glidewell's arithmetic puts a 15-crown/week practice's exposure at ~40 hours/year.
**Risks and constraints:** the state content profiles are legal content and need citations and dates. Several states require an **original ink signature** (Ohio explicitly), and a Virginia lab reports board inspectors demanding ink signatures — so "print and sign" must remain a first-class output, not a fallback. Retention obligations differ (2 years typical, **4 years in Florida on both sides**).
**Existing products/substitutes:** EasyRx (from $68/month, plus a no-cost per-script lab plan); Henry Schein DDX (free to dentists, Dentrix-anchored); scanner-portal order forms; lab management systems (LabStar ~$250/mo, Seazona ~$80/mo) which are lab-internal. **The structural gap is that the scanner Rx and the legal work authorization are two different documents that no system reconciles** — a lab owner's own words: *"Digital order systems from scanning devices bypass traditional prescription workflows entirely, creating ambiguity about documentation requirements."*
**Why still attractive:** existing tools digitize the compliance layer; the omissions are in the design-intent layer. And the state-legal layer is real, unglamorous work that nobody has open-sourced.
**Paid customization:** a specific laboratory's field set and material menu, distributed by that lab to its accounts (the lab is arguably the better customer here than the practice); DSO-wide standardization.

---

### C7 — Referral Packet Completeness Gate

**Working title:** *ReferReady*
**Intended user:** GP front desk assembling an outbound referral; secondarily the specialist's referral coordinator.
**Problem solved:** referrals arrive with radiographs 90% of the time and with *adequate* radiographs 47% of the time, and 23.8% get rejected at triage — 93% of those for insufficient clinical information.

**Current workflow:** fill a paper slip, scan it, separately export radiographs from the imaging application, attach both to an email, and hope. A Dentrix user's feature request describes the workflow verbatim: scan the referral slip to the Document Center, export it to the desktop, separately go to the Image Center to export x-rays, and manually attach everything to an email.

**Proposed workflow:** choose the receiving specialty and the tool presents that specialty's required-element set (endo, OMS, perio, ortho, pedo each differ). It enforces the elements the audits say go missing: **tooth number rendered simultaneously in Universal, Palmer and FDI notation** — the single cheapest fix for the documented wrong-site extraction failure mode — reason for referral, presenting complaint, current medications, allergies, relevant medical history, imaging with **acquisition date**, and an explicit "written report requested" flag with an expected-return date. It assembles a single PDF cover packet plus an imaging folder, produces a manifest, and logs what was sent and when. It refuses to finalize with required elements blank.

**Required inputs:** patient demographics, medical history and medications (pullable from the PMS), tooth number, reason, imaging files and their dates.
**Expected outputs:** a single referral PDF; an imaging bundle with a manifest; a chart-ready transmission log entry.

**Essential features:** per-specialty required-element sets; tri-notation tooth rendering; imaging date capture; the completeness gate; the transmission log.
**Deliberately excluded from v1:** being a referral network — no accounts for the receiving specialist, no directory, no two-sided marketplace. **The account-creation wall is why fifteen years of dental referral platforms have failed to reach general penetration**, and the successful ones (Refera) explicitly let specialists receive without an account. The output here is a file the practice sends by its existing channel.

**AI:** *inappropriate for the gate.* One later possibility with real merit: checking whether an attached radiograph actually shows the referenced tooth. That is a clinical image claim and probably a regulated one — out of scope.

**Would a spreadsheet suffice?** No. This is document assembly plus conditional required fields.

**Complexity:** medium — image handling is the hard part and the reason implementation scores lower than the problem severity would suggest.
**Learning difficulty:** ~20 minutes.
**Value:** the receiving side spends up to 20 minutes chasing missing information per incomplete referral vs ~3 minutes for a complete one; a structured proforma produced a measured **29.3% increase in information provided**. The tail risk avoided is wrong-site surgery.
**Risks and constraints:** PHI in transit — the tool should produce a package, not a transmission channel, unless the practice already has secure email. Image export remains dependent on whatever the imaging application permits.
**Existing products/substitutes:** Sindi, Refera, RecordLinc, PepCare, Brightsquid, eDossea, CareStack's built-in referrals, Dentrix Ascend's tagging-only feature. The category is crowded on *transport* — the competition is on file-size caps, 50 MB → 500 MB → 2 GB — and **empty on completeness enforcement**. Given the Swedish audit found radiographs present 90% of the time but inadequate 53% of the time, the industry is optimizing the wrong axis.
**Why still attractive despite the crowding:** it is not competing with them. It produces a better package for whatever channel the practice already uses, which means it can be adopted unilaterally by one office without asking anyone else to sign up.
**Paid customization:** a specific specialist's required-element set, distributed by that specialist to their referrers (the specialist is the natural buyer — this is their marketing budget); imaging-system-specific export helpers.

---

### C8 — Imaging Export Validator

**Working title:** *WillItOpen*
**Intended user:** anyone in the practice who sends imaging out — front desk, assistant, or the person handling a records request.
**Problem solved:** the recipient can't open the file, so it gets re-sent, degraded to JPEG, or the radiograph gets retaken.

**Current workflow:** export from the imaging application by whatever path is quickest, zip it, and send. Discover the problem days later.

**Proposed workflow:** point the tool at an export folder. It reports, in plain language: whether the DICOM series is complete and multi-file (a receiving lab's published spec demands *"uncompressed, multi-file DICOM, 0.3mm or 0.4mm slices"* and explicitly rejects single-file and viewer-executable conversions); slice thickness and file count, warning when 0.1–0.2 mm slicing has produced a file count too large to upload; whether any `.exe` viewer is bundled (and offers to strip it, since many IT departments block executables); whether the files are proprietary rather than standard (`.dex`, `.jif` and similar); total size against common transfer limits; and whether acquisition dates are present. It then writes a **manifest** — patient, tooth or region, acquisition date, modality, file count, format — and a one-page **plain-language "how to open this" sheet** for the recipient.

**Required inputs:** a folder of exported imaging.
**Expected outputs:** a validation report; a cleaned, correctly structured package; a manifest; a recipient instruction sheet.

**Essential features:** DICOM series integrity check; slice-thickness and count reporting; executable detection and removal; proprietary-format detection; the manifest; the instruction sheet.
**Deliberately excluded from v1:** exporting *from* imaging applications (each vendor is different and this is where projects die); viewing or rendering images; anonymization; transmission.

**AI:** *inappropriate.* This is file inspection against a spec.

**Would a spreadsheet suffice?** Not applicable.

**Complexity:** small-to-medium. **Learning difficulty:** ~5 minutes — drag a folder, read a report.
**Value:** prevents a re-request cycle and, per the ADA's own submission to HHS, prevents repeat imaging and unnecessary radiation. Applies across referrals, lab surgical-guide cases, records releases, and insurer submissions — one tool, four workflows.
**Risks and constraints:** it touches PHI-bearing files and should run entirely locally with no upload. It must not claim to assess *diagnostic* adequacy, only technical openability — that distinction is the line between a utility and a regulated device.
**Existing products/substitutes:** generic DICOM validators aimed at radiology; nothing dental-shaped or front-desk-shaped. Vendors are building *around* the gap (Carestream's Imaging Case Collaboration, CBCTHub, browser DICOM viewers) rather than validating exports.
**Why attractive:** it is the smallest genuinely useful thing in this report, it has no competitor at this scope, and the ADA has publicly named the underlying problem to a federal regulator — which is unusually good validation for a market-research finding.
**Paid customization:** per-recipient profiles (this lab wants 0.4 mm multi-file DICOM; this endodontist wants PAs as PNG); a batch mode for a DSO's records department.

---

### C9 — Referral Loop Closer

**Working title:** *LoopClose*
**Intended user:** GP treatment coordinator; specialist marketing/relationship coordinator.
**Problem solved:** up to half of referrals never complete, and the report often never comes back.

**Current workflow:** nothing systematic.

**Proposed workflow:** each outbound referral gets an expected-contact date and an expected-report date. The tool produces two weekly lists: **patients who were referred and show no evidence of having gone**, and **referrals with no report received by the expected date**. It drafts the patient follow-up call script and the specialist report request, and — importantly for liability — logs every attempt, including a structured "patient declined referral" outcome with an informed-refusal note, which is exactly what malpractice carriers instruct practices to document.

**Required inputs:** referral records (from C7 or entered directly); report receipt logging.
**Expected outputs:** two exception lists; drafted follow-ups; a documentation trail.

**Essential features:** the two lists; the outcome vocabulary including informed refusal; the log.
**Deliberately excluded from v1:** anything requiring the specialist to participate; patient messaging automation; analytics dashboards.

**AI:** *inappropriate.*

**Would a spreadsheet suffice?** Largely yes, which is why this ranks last. The differentiator is the informed-refusal documentation artifact and the fact that it runs unattended.

**Complexity:** small. **Learning difficulty:** ~10 minutes.
**Value:** GPs rate timely report-back the single most important specialist relationship factor (96%); referral breakdowns are implicated in 20–30% of diagnostic errors. But the dental-specific completion statistics are 2008-vintage or vendor-sourced, so the ROI case is softer than the others here.
**Risks and constraints:** requires disciplined data entry, which is the failure mode of every tracking tool.
**Existing products/substitutes:** every referral platform claims tracking; CareStack and Dentrix Ascend include status flags.
**Why still attractive:** modest. It is included because it is cheap to build alongside C7 and because the documentation artifact has independent liability value — but it should not be built first.
**Paid customization:** specialist-side deployment measuring referrer-by-referrer completion.

---

## 5. Opportunity ranking

Scored 1–5 on ten criteria. **SEV** severity of problem · **FRQ** frequency of use · **ROI** clarity of return · **LRN** ease of learning · **IMP** ease of implementation · **SCP** ability to stay narrowly scoped · **DIF** market differentiation · **CST** customization potential · **DAT** availability of realistic test data · **CNF** confidence in evidence.

| # | Concept | SEV | FRQ | ROI | LRN | IMP | SCP | DIF | CST | DAT | CNF | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| C1 | Clearance Request Builder & Reply Tracker | 4 | 4 | 4 | 5 | 5 | 5 | 5 | 4 | 4 | 5 | **45** |
| C2 | Claim Attachment Completeness Gate | 5 | 5 | 5 | 4 | 3 | 3 | 4 | 5 | 5 | 5 | **44** |
| C3 | Lab Case / Schedule Reconciler | 4 | 5 | 5 | 5 | 4 | 5 | 3 | 4 | 5 | 4 | **44** |
| C4 | Right-of-Access Request Register | 4 | 3 | 4 | 5 | 5 | 5 | 5 | 3 | 4 | 5 | **43** |
| C5 | Predetermination Register | 4 | 4 | 4 | 5 | 4 | 5 | 5 | 4 | 4 | 4 | **43** |
| C6 | Lab Rx Design-Intent Gate | 4 | 5 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 5 | **42** |
| C7 | Referral Packet Completeness Gate | 4 | 5 | 4 | 4 | 3 | 4 | 3 | 4 | 5 | 5 | **41** |
| C8 | Imaging Export Validator | 4 | 4 | 4 | 5 | 4 | 5 | 5 | 3 | 3 | 4 | **41** |
| C9 | Referral Loop Closer | 4 | 4 | 4 | 5 | 4 | 5 | 3 | 3 | 3 | 4 | **39** |

### The top three

**C1 — Clearance Request Builder & Reply Tracker (45).** It wins on the combination that matters most for this catalog: a failure quantified in peer-reviewed literature, a fix that is a form and a timer, and **no competitor in the category at all**. Every AI dental product found maps to radiographs, phones, verification, notes, or marketing; clearance is unoccupied despite having a documented 19.2% success rate, a 45% repeat-contact rate, and a malpractice carrier publishing exactly what the artifact should contain. It also has a feature no other concept here has — the guideline pre-check that *eliminates* work rather than speeding it up, by telling the practice that a prosthetic-joint or stable-warfarin clearance isn't indicated. That is the kind of thing a professional notices and remembers.

**C2 — Claim Attachment Completeness Gate (44).** The largest dollar value and the strongest evidence, held back by scope discipline and by one contractual fact. Scope: the rules corpus is a permanent maintenance commitment, and a stale rule is worse than no rule. Contract: **Henry Schein One prohibits third-party insurance claim processing integrations on Dentrix**, which by itself removes the largest installed base from the addressable market unless the tool operates purely as an advisor outside the claim path. Its real strategic appeal is that the open corpus is a community asset — a practice that discovers Blue Cross won't accept electronic attachments contributes a rule, and the corpus compounds. That is a genuinely good fit for a free open-source base with paid per-practice customization, because the customization ("build my payer mix in") is exactly what practices currently do by hand.

**C3 — Lab Case / Schedule Reconciler (44).** The cleanest, smallest, most immediately demonstrable of the nine. Four queries, one email, near-zero learning curve, and a before-and-after a dentist understands in one sentence: *"you will stop finding out at 8:40 that the crown isn't here."* It scores lower on differentiation because PMS lab modules exist — but it works precisely *because* those modules depend on staff remembering to attach cases, and Open Dental's own marketing admits they forget. Exception 4, notifying the lab when the patient reschedules, appears genuinely unserved by anything in the market.

### What should be investigated next

**Build C3 first, even though it ranks third.** It is the fastest path to a working artifact with a real practice, it requires only read access to Open Dental, it contains no clinical or legal content, and a working exception report is the credibility that gets a conversation about C1 or C2. Use it as the wedge, then interview the same practices for C1.

**Investigate C2's corpus feasibility before committing.** Spend a week building the rules corpus for exactly three payers — Delta Dental (one state entity), Cigna DPPO, and one state Medicaid — from their published PDFs. If three payers take a week, the corpus is viable; if they take a month, the concept needs to shrink to a single-payer or single-procedure-family tool.

---

## 6. Validation plan

### Questions to ask practitioners

**For C1 (clearance) — ask an OMS or perio office manager:**
- How many clearance requests do you send in a typical month, and what fraction come back with what you actually asked for?
- When a reply comes back as a signature with no data, what do you do next?
- Have you ever postponed or cancelled a surgical appointment because clearance hadn't arrived? How often?
- Do you ever send a clearance request for a joint replacement or a patient on warfarin? (Listen for whether they know current guidance says it's usually unnecessary — this tests whether the pre-check has value or is insulting.)
- Who decides the request is needed — the surgeon, or the scheduler working from a rule?

**For C2 (attachments) — ask a billing coordinator:**
- Show me the document you use to know what each payer requires. *(Ask to see it. If it's a PDF or spreadsheet, the thesis is confirmed; photograph the structure.)*
- Who maintains it, and when was it last updated?
- What happens when a payer changes a rule — how do you find out?
- Of your denials last month, how many were documentation problems? *(Ask for the actual denial report, not a recollection.)*
- Have you ever had a claim denied for "missing X-ray" when you know you uploaded it?

**For C3 (lab cases) — ask a front desk:**
- Walk me through this morning. How did you know which of today's patients have lab work outstanding?
- When was the last time a patient came in and the case wasn't here? What happened?
- When a patient reschedules a seat appointment, does the lab find out? How?
- Do you keep anything outside the software — a whiteboard, a binder, a spreadsheet? *(Ask to see it.)*

### Who to interview

- **2–3 independent GP practices on Open Dental** — the beachhead, and the only ones who can give you a test database easily.
- **1–2 oral surgery practices and 1 periodontal practice** — the clearance and referral-intake volume lives here.
- **1–2 commercial dental laboratories under 25 employees** — they see hundreds of practices' Rx habits and are the most quantitatively honest party in the whole chain, because remakes cost them money. Dental Lab Network is a publicly readable forum where lab owners speak candidly; it is the best recruiting ground.
- **1 outsourced dental billing company** (eAssist-style) — they will tell you exactly what the payer-rules corpus is worth, because it is their moat.
- **1 dental practice-management consultant or AADOM member** — for cross-practice pattern, not for single-practice truth.

### Search terms for further research

`dental "work authorization" statute [state]` · `"required documentation" dental claim [payer] PDF` · `dental lab "remake" rate KPI` · `"medical clearance" dental fax form template` · `OCR right of access settlement dental` · `Open Dental API labcase appointment` · `CBCT export DICOM lab surgical guide requirements` · `dental referral rejected triage insufficient information` · `predetermination expiration dental plan year`

### Sample files and data needed

- A real (de-identified) **claim-requirements cheat sheet** from a practice — the Verber Dental Group PDF is a public specimen to start from.
- **Three payer documentation PDFs** to seed the corpus: Delta Dental of NJ/CT's 2025 Required Documentation Chart, Cigna's 2026 DPPO Coverage Determination Guidelines, and one state Medicaid manual.
- An **Open Dental test database** (provided free by Open Dental to developers) with lab case and appointment tables populated.
- A **de-identified CBCT export** from at least three different scanner ecosystems — this is the hardest artifact to obtain and the one that determines whether C8 is real.
- Three or four **blank lab Rx forms** from labs in different states, to derive the field templates.
- A set of **clearance forms** from practice websites (dozens are public) to derive the question templates.

### Cheapest prototypes that would validate

- **C3:** a Python script against the Open Dental test database that prints the four exception lists. One day of work. If a real practice looks at the output and says "wait, that one's wrong" and then goes and fixes it, the concept is validated.
- **C1:** a single well-designed PDF — one procedure family, structured answer slots — faxed by one OMS office for two weeks. Measure the reply completeness rate against their historical baseline. No code at all.
- **C2:** the three-payer corpus plus a script that takes a CSV of claim lines and prints the requirements checklist. If a billing coordinator finds one thing their cheat sheet had wrong, that's the validation.
- **C8:** a script that walks a folder and prints the validation report. Half a day. The binding question is whether you can get three real CBCT exports.

### The assumptions most likely to make each fail

- **C1:** that practices *want* fewer clearance requests. Some send them defensively regardless of guidelines, precisely because the request is a liability transfer. If the pre-check is perceived as talking them out of documentation, the feature is a liability, not an asset. Test this early and be prepared to make the pre-check advisory only.
- **C2:** that published payer rules match what payers actually enforce. The Verber cheat sheet says D7210 needs no PA x-ray while Delta and Aetna both require one — either the practice learned an unpublished exception, or the practice is wrong. If the answer is "the published rules aren't the real rules," the corpus is much less valuable and the outsourcers' moat is knowledge that cannot be documented.
- **C3:** that the PMS lab-case table is actually populated. If staff don't create lab case records at all, there is nothing to reconcile and the tool needs a data-entry front end, which changes its complexity class entirely. **Check this first — it is a single query and it determines whether the concept exists.**
- **C4:** that practices perceive the risk. Four enforcement actions in a profession with 180,000+ offices is a low base rate; the tool may be a hard sell absent a news hook.
- **C6:** that assistants will tolerate a gate. A required-field wall on a form someone fills 20 times a day is the classic adoption failure. It may need a "save incomplete, flag for doctor" path, which weakens the gate.
- **C7:** that a completeness gate on the *sending* side helps when the *receiving* side has no obligation to use the format. It may be that the specialist is the real customer and the GP tool is the giveaway.
- **All of them:** that the buyer is the practice. For C6 and C7 the natural buyer may be the *counterparty* — the laboratory and the specialist respectively — who would distribute the tool to their accounts as a relationship investment. That is a materially different go-to-market and worth testing directly.

---

## 7. Cross-industry patterns

Seven patterns from this market that transfer to named backlog markets.

**P1 — Completeness gate at the moment of transmission.** Block or flag an outbound package against a recipient-specific required-field schema, rather than validating after rejection. Grounded here in a 1,891-referral audit whose own recommendation was that systems *"only allow for submission once all of the essential information has been considered."*
*Transfers to:* Architectural construction administration (CA) desks at small A/E firms · Delegated-design submittal coordination · Federal construction contractors on NAVFAC/USACE projects (UFGS submittal register) · Equipment manufacturer and manufacturer-rep submittal desks · Title abstracting and independent title search contractors · Provider credentialing and payer enrollment services.

**P2 — Structured ask with named answer slots.** When you must get information from an external party you do not control, the leverage is not in faster transmission but in converting a free-text request into a form whose reply has slots to fill — and then checking whether they were filled. Grounded here in a 19.2% clearance return rate against a 39.6% request rate.
*Transfers to:* Right-of-way and easement acquisition consulting · Employer immigration compliance and I-9 audit consultancies · Prime contractor supplier cyber-compliance desks (supplier attestation collection) · Consortium/third-party administrators (C-TPAs) for DOT drug and alcohol programs · Commercial real estate acquisition due diligence and rent roll verification.

**P3 — Statutory-clock register for inbound external requests.** Log receipt with a timestamp, compute the statutory deadline, generate the extension instrument, guard the fee calculation, and log delivery. Grounded here in four OCR dental right-of-access actions totaling $205,000, four of five triggered by a fee dispute or a slow partial response.
*Transfers to:* HOA and condominium management companies (estoppel and demand response desk) · County recorder offices (document intake and rejection handling) · Mortgage servicer payoff and lien release departments · Unclaimed property and escheat compliance service providers · County surveyor and municipal plan-check offices.

**P4 — Versioned counterparty rule corpus with change diffing.** A maintained, machine-readable, source-cited table of what each external authority requires, replacing a hand-built spreadsheet owned by one person. The corpus, not the UI, is the product. Grounded here in per-CDT-code payer documentation charts that conflict across and within payer brands and change roughly annually.
*Transfers to:* Workers' compensation medical billing and state fee schedule compliance · Certified payroll and prevailing wage compliance service providers · Multi-state charitable solicitation registration compliance · Sales tax compliance outsourcing for small multi-state sellers · Aerospace supplier quality clause library administration at machine shops and Tier 2 suppliers.

**P5 — Approval-document ↔ eventual-invoice reconciliation.** An approval is granted weeks before the work, expires, and is matched to the eventual billing document by a reference number carried forward by hand. Grounded here in predeterminations valid 60–90 days, resetting at plan year, matched to claims manually.
*Transfers to:* Oversize/overweight permitting and heavy-haul route survey coordination · Government contracts administration at small govcons (clause and mod review) · Insurance restoration contractors and supplement writers · Truck permitting and registration service agencies.

**P6 — Receiver-openability validation for technical file deliverables.** Before sending a technical file package, verify the recipient can actually consume it: format, structure, completeness, embedded executables, size, required metadata — and ship a manifest and instruction sheet with it. Grounded here in the ADA formally telling HHS that dental imaging transfer causes repeat imaging and radiation exposure, and in a receiving lab publishing a spec with named failure modes across 18+ scanner manufacturers.
*Transfers to:* Environmental laboratories producing regulator EDD deliverables (EQuIS and state formats) · UAS/drone mapping and reality-capture service providers · Pipe and duct fabrication shops serving mechanical and fire protection trades · Investment casting and forging suppliers under Nadcap · Geodetic control and least-squares network adjustment specialists.

**P7 — Bidirectional schedule ↔ external-production-order reconciliation.** Every system pushes production status *to* the scheduler; almost none pushes schedule changes *back* to the producer. The unserved direction is usually the cheaper one to build and the more valuable one to the counterparty. Grounded here in the finding that nothing in the dental market notifies a laboratory when the patient reschedules.
*Transfers to:* Pipe and duct fabrication shops serving mechanical and fire protection trades · Ready-mix concrete producer quality control departments · Construction subcontractor project management at 15–150 employee specialty trades · Warehouse and 3PL fulfillment receiving/shipping document control · Machine shop / job shop quoting and production control (already completed — this pattern would be a second-pass finding there).

---

## 8. Sources and confidence

### Verified findings — high confidence, primary or peer-reviewed sources

**Market structure**
- [ADA HPI, US Dentist Workforce 2025 (PDF)](https://www.ada.org/-/media/project/ada-organization/ada/ada-org/files/resources/research/hpi/US_dentist_workforce_2025.pdf) — 202,485 dentists, specialty counts, solo/group/DSO splits.
- [ADA HPI, Practice Ownership Trends (PDF)](https://www.ada.org/-/media/project/ada-organization/ada/ada-org/files/resources/research/hpi/practice_ownership_trends_dentistry_new_look_old_data.pdf) — ownership 85%→73%; DSO 27% early-career.
- [ADA HPI, The Dental Care Market](https://www.ada.org/resources/research/health-policy-institute/dental-care-market) — $189B, 2024.
- [ADA HPI, Trends in Dentists' Income](https://www.ada.org/resources/research/health-policy-institute/dental-practice-research/trends-in-dentist-income) — revenue +1.4% vs expenses +4.9%.
- [McGill Advisory admin staffing ratios (PDF)](https://advancedpracticemanagement.com/wp-content/uploads/2018/11/MCGILL-ARTICLE-NOVEMBER-2018.pdf) — 1 admin FTE per $60k/month production.

**Medical clearance**
- [Frontiers in Digital Health 2022;4:838538](https://www.frontiersin.org/journals/digital-health/articles/10.3389/fdgth.2022.838538/full) — **the single most important source in this report.** 240 consults; clearance requested 39.6% / returned 19.2%; 20% empty replies; 45% needed repeat contact; mean 19.6 ± 36.6 days.
- [MedPro Group, What Dentists Should Know About Medical Clearance](https://resource.medpro.com/what-dentists-should-know-about-medical-clearance) — required contents of a proper request; documentation duties.
- [ADA, Antibiotic Prophylaxis Prior to Dental Procedures](https://www.ada.org/resources/ada-library/oral-health-topics/antibiotic-prophylaxis) — AHA 2021 high-risk list; prosthetic joints generally not indicated.
- [ADA, Oral Anticoagulant and Antiplatelet Medications](https://www.ada.org/resources/ada-library/oral-health-topics/oral-anticoagulant-and-antiplatelet-medications-and-dental-procedures) — do not alter regimens; INR ≤3.0.
- [AFP 2021;104(5):476, Medical Clearance for Common Dental Procedures](https://www.aafp.org/pubs/afp/issues/2021/1100/p476.html) — physician-side view; 6 wks post-MI, 6 mo post-DES; A1C in the reply.

**Referrals and imaging**
- [Alwaeli et al., CCIDE 2017 (PDF)](https://www.dovepress.com/article/download/35616) — n=1,891 oral surgery referrals; 53.4% inadequate radiographs; 60% missing medications; recommends blocking submission until complete.
- [BDJ 2025, GDP referral letters: reasons for rejection](https://www.nature.com/articles/s41415-025-9047-y) — 673 perio referrals, 23.8% rejected, 93% for insufficient information.
- [BDJ 2002, restorative referral proforma study](https://www.nature.com/articles/4811477) — structured proforma → +29.3% information.
- [ADA News, Mar 2026 — ADA calls for improved interoperability standards for dental imaging](https://adanews.ada.org/ada-news/2026/march/ada-calls-for-improved-interoperability-standards-for-dental-imaging/) — proprietary formats, inconsistent DICOM, repeat imaging and radiation, exclusion from Meaningful Use.
- [ROE Dental Lab, Managing DICOMs](https://www.roedentallab.com/collaboration/managing-dicoms) — the receiving spec; 18+ CBCT manufacturer tutorials; explicit rejection of viewer executables.
- [MedPro OMS, wrong-site extraction from a phone-only referral](https://oms.medprodental.com/risk-tips/communication-mishap-between-providers-leads-to-wrong-site-extraction) — Universal vs Palmer "#8."
- [The Doctors Company, Patient Safety in Dentistry: Communication](https://www.thedoctors.com/articles/patient-safety-in-dentistry-communication) — up to 50% of referrals not completed; 70%/35% histories gap; 20–30% of diagnostic errors.
- [AAE 2009 GP Referrals Study (PDF)](https://www.aae.org/specialty/wp-content/uploads/sites/2/2017/08/2009_gp_referrals_study.pdf) — n=983; 96% rate timely report-back as top relationship driver.
- [ADA sample Referral to Dental Specialist form (PDF)](https://www.ada.org/-/media/project/ada-organization/ada/ada-org/files/publications/guidelines-for-practice-success/mngpatients_referral_to_specialist.pdf) — the "Radiographs: …none available" checkbox.

**Payer documentation and claims**
- [Delta Dental NJ/CT Required Documentation Chart 2025 (PDF)](https://www.deltadentalct.com/-/media/DDCT/pdf/DDNJCT_Required-Documentation-Chart-2025.ashx) — the most granular per-code payer artifact found.
- [Delta Dental, 2026 complete documentation for claims](https://www1.deltadentalins.com/dentists/fyi-online/2026/complete-documentation-for-claims.html) — named documentation gaps by code.
- [Cigna DPPO Coverage Determination Guidelines 2026 (PDF)](https://campaigns.cigna.com/static/campaigns-cigna-com/docs/dental-hcpemails/Clinical%20Documents/Cigna%20Dental%20Coverage%20Determination%20Guidelines%20-%20DPPO%20-%202026%20-%20Final.pdf) — numeric criteria (4 mm SRP, 5 mm osseous).
- [Aetna Dental Claim Documentation Guidelines (PDF)](https://www.aetnadental.com/professionals/pdf/claim-documentation-guidelines.pdf) — radiographs <36 months, six probing depths per tooth.
- [UnitedHealthcare National Standardized Dental Claim Review Guidelines (PDF)](https://www.uhcprovider.com/content/dam/provider/docs/public/policies/dental/dental-utilization-review-guideline.pdf) — documents specified, no numeric thresholds.
- [Medi-Cal Dental TAR denials FAQ (PDF)](https://www.dental.dhcs.ca.gov/DC_documents/providers/FAQ_TAR_denials.pdf) — 8/14/36-month radiograph currency; 45-day RTD clock; wet signatures.
- [Verber Dental Group internal claim requirements cheat sheet (PDF)](https://verberdentalgroup.com/wp-content/uploads/2025/01/Claim_Requirements_-_Supporting_Information-1.pdf) — **a real practice's per-code rules table, in the wild.** The single best evidence for the C2 thesis.
- [2024 CAQH Index Report (PDF)](https://www.caqh.org/hubfs/Index/2024%20Index%20Report/CAQH_IndexReport_2024_FINAL.pdf) — dental attachments 37% electronic / 63% manual; $2.1B savings opportunity.
- [CMS attachments final rule fact sheet (PDF)](https://www.cms.gov/files/document/nsg-attachments-final-rule-fact-sheet.pdf-0) — X12 275 v6020 effective 5/26/2026, compliance 5/26/2028; **prior authorization excluded.**
- [ClaimConnect attachments help](https://claimconnect.dentalxchange.com/dci/claims/help/singleclaim/attachments.jsp) — no attachment on initial claim without NEA; MetLife print-and-mail loop.
- [Open Dental manual, claim attachments](https://www.opendental.com/manual/claimtabattach.html) — "for reference only and are not sent by Open Dental."
- [Texas HHS OIG dental cases review](https://oig.hhs.texas.gov/about-us/news/dental-cases-review-offers-insight-avoiding-billing-and-compliance-issues) — $66,804 settlement; 86 of 120 records unproduced; 2-year exclusion.
- [ADA, Pre-authorizations vs predeterminations](https://www.ada.org/resources/practice/dental-insurance/pre-authorizations) and [CDA](https://www.cda.org/newsroom/billing/dental-benefits-101-preauthorization-versus-predetermination/) — validity, calendar-year rollover, why payers prefer the non-binding instrument.

**Laboratory**
- [Ohio Admin. Code 4715-5-02](https://codes.ohio.gov/ohio-administrative-code/rule-4715-5-02) — the most complete statutory work-authorization spec found, including the lab return-disclosure section.
- [Fla. Stat. § 466.021](https://law.justia.com/codes/florida/title-xxxii/chapter-466/section-466-021/) — 4-year retention both sides; criminal penalty for lab noncompliance.
- [RCW 70.352.030 (Washington)](https://lawfilesext.leg.wa.gov/Law/RCWArchive/2023/htm/RCW%20%2070%20%20TITLE/RCW%20%2070%20.352%20%20CHAPTER/RCW%20%2070%20.352%20.030.htm) — registration, CDT staffing, material content and point-of-origin disclosure.
- [NADL, State Regulation](https://dentallabs.org/state-regulation/) — 12 regulating states; 65% of dentists wrongly assume regulation.
- [PMC7005880 — Remake rates for single-unit crowns](https://pmc.ncbi.nlm.nih.gov/articles/PMC7005880/) — **3.8% measured** across 3,750 crowns; causes ranked.
- [PMC7335025 — technician survey on work authorizations](https://pmc.ncbi.nlm.nih.gov/articles/PMC7335025/) — margin design missing 69%, pontic 56%, try-in 51.2%.
- [Appl. Sci. 2022, 12(12):6263](https://www.mdpi.com/2076-3417/12/12/6263) — dentist-side omission rates (shade 44.6%, alloy 46.7%).
- [BDJ 2014, UK communication methods survey](https://www.nature.com/articles/sj.bdj.2014.643) — 24% say >half of prescriptions inadequate; 22% clarification rate among record-keeping labs.
- [LMT 2024 Remakes Survey](https://lmtmag.com/articles/survey-report-productivity-disrupter-remakes) — >80% of external remakes attributed to dentist error, stable since 2011.
- [Dental Lab Network, portal fragmentation thread](https://dentallabnetwork.com/forums/threads/what-portal-do-you-use-for-sending-or-receiving-scans.35376/) — "about 50% of our daily cases just get sent via email"; "A mess, if you ask me."
- [Oral Arts, 12 scanner ecosystems](https://www.oralartsdental.com/intraoral-scanners/) · [Associated Dental Lab, scan body library version control](https://associateddl.com/scan-body-libraries-version-control-brand-mixing-accuracy-traps/) — 0.1–0.5 mm error magnitudes.

**Records and privacy**
- [HHS OCR, Right to Access FAQs](https://www.hhs.gov/hipaa/for-professionals/faq/right-to-access-and-research/index.html) — 30 days, one extension, permitted vs prohibited fees.
- [Saul Ewing on Gums Dental Care, $70,000 CMP](https://www.saul.com/insights/alert/scary-ocr-cmp-imposed-upon-solo-dental-practice) — $25 mailing fee on an email request; willful neglect.
- [HIPAA Journal, three dental right-of-access fines](https://www.hipaajournal.com/dental-practices-fined-for-hipaa-right-of-access-violations/) — $80,000 / $30,000 / $25,000.
- [ADA, Dental Records (PDF)](https://www.aapd.org/globalassets/media/safety-toolkit/dental-records-ada.pdf) — record contents; retention; the "whether or not the patient's account is paid in full" obligation.

**Software and integration**
- [Dentrix Developer Program FAQ](https://ddp.dentrix.com/pages/faq) — **$5,000 READ + $5,000 WRITE plus royalty; Ascend $47/location/month; insurance claim processing prohibited.** The most decision-relevant single URL for anyone building here.
- [Open Dental API setup](https://www.opendental.com/site/apisetup.html) · [API specification](https://www.opendental.com/site/apispecification.html) · [Fees](https://www.opendental.com/site/fees.html) · [Program Bridges](https://www.opendental.com/site/programbridges.html).
- [Henry Schein One API Exchange vendors list](https://www.henryscheinone.com/dental-solutions/api-exchange/vendors-list/) — publishes ~60+ *unauthorized* vendors.
- [Planet DDS Open API Program](https://www.planetdds.com/newsroom/planet-dds-unveils-open-api-program/) — launched July 2024; writebacks and webhooks.
- [Dentrix Ascend Outbound Referrals](https://learn.dentrixascend.com/outbound-referrals/) — tagging only; no transmission, no images, no report-back.
- [ADA HPI, Dentists' AI Usage and Attitudes (July 2026)](https://www.ada.org/resources/research/health-policy-institute/dental-practice-research/dentists-ai-usage-and-attitudes) — 43.3% use AI for some task; **planned growth is 34.8% charting/notes and 32.6% insurance verification vs 25.4% imaging**; 82.6% will not use AI for treatment recommendations.

### Strong inferences — reasoning from verified facts, not directly sourced

1. **No PMS ships a maintained, payer-specific, code-level attachment-completeness rules engine.** Dentrix comes closest and explicitly hands maintenance to the practice; clearinghouse validation checks format and carrier eligibility, not clinical completeness. Stated as documented absence across the systems whose documentation is accessible, not as proven absence across all systems.
2. **No product addresses medical clearance or records-release as a workflow.** Every AI dental product found maps to radiographs, phones, verification, notes, or marketing.
3. **No system pushes practice-side schedule changes back to the laboratory.** Every case-tracking product found moves status in the other direction.
4. **The referral market competes on transport, not adequacy.** Every platform's differentiation is a file-size cap; the audit evidence says the binding constraint is imaging adequacy and clinical completeness.
5. **Open Dental is the correct first integration** for any new dental admin product — not because of installed base but because it is the only major system where a two-person team can prototype without a five-figure contract.
6. **Administrative AI has roughly 2.4× the forward demand of diagnostic AI in dentistry and none of the FDA burden** — ADA HPI's planned-adoption numbers against 44 dental AI 510(k) clearances issued 2021–2025.
7. **The outsourced dental billing companies' actual moat is a maintained payer-rules corpus plus labor**, not proprietary technology — which is what makes an open corpus a credible attack.
8. **A practice's hand-built per-payer cheat sheet is near-universal above a few operatories**, and is a key-person and staleness liability. One public specimen plus consistent descriptions across billing-industry sources; not surveyed.

### Tentative hypotheses requiring practitioner validation

1. That practices *want* fewer clearance requests rather than sending them defensively as liability transfer. **This is the assumption most likely to sink C1 and should be tested first.**
2. That published payer documentation rules match enforced rules. The Verber sheet's "D7210 — PA x-ray not required" contradicts both Delta and Aetna.
3. That PMS lab-case tables are actually populated in practices that would buy C3.
4. That pulp-testing results are re-performed on arrival at endodontic offices because they are never transmitted. Plausible from the absence of such fields on every referral form reviewed, but **not documented as a complaint anywhere** — treat as an interview question, not a finding.
5. That the natural buyer for C6 and C7 is the counterparty (laboratory, specialist) rather than the practice.
6. That the ~10–25% band for "share of lab cases requiring a clarification touch" holds in the US. Derived from a UK survey (13% recalled, 22% among labs answering from records); **no US figure exists.**

### Statistics encountered and deliberately rejected

Stated here so a future cycle does not re-import them:

- **"19.3% first-submission denial rate," "18% of denials from missing documentation," "$117 average rework cost per denied claim."** Circulated widely across dental-AI vendor blogs; traced to a single uncited page claiming "analysis of over 500,000 dental claims" with no footnotes. The $117 conflicts with MGMA's ~$25 by nearly 5×. **A defensible documentation-share-of-denials figure does not currently exist. That absence is itself a finding.**
- **"80% of dentists do not complete the information legally required on the prescription form."** A US claim with no traceable source, repeated across lab-industry content.
- **"46% of dental specialist referrals go unfulfilled; $953–$5,150 lost per unfulfilled referral."** Kelton Research, **2008**, no disclosed sample size or sponsor. The most-cited dental referral statistic in the industry and eighteen years old. Date it explicitly if used at all.
- **TrazaLab's cluster** (34% of paper prescriptions missing a critical field; 65% of remakes from communication failures; 45 min/technician/day chasing information). Vendor blog, attributions vague, untraceable to any primary source.
- **Vendor referral-completion claims** (Refera "80% vs 50%," CareStack "35%+ no-show," PepCare "47% leakage reduction"). Marketing.

### Known gaps in this cycle's research

- **Reddit and Dentaltown message boards were inaccessible** from this environment (403 / not indexed). Dental Lab Network *was* readable and supplied the best practitioner voice in the lab thread; the equivalent GP and specialist voice is missing. Open Dental Forum threads on sharing CBCTs and on sending reports to referring GPs were identified but not retrievable.
- **No US study quantifies lab Rx completeness**, referral packet assembly time, referrals per GP per month, or share of production referred out.
- **No published on-time-delivery benchmark exists for the dental laboratory industry**, and the strongest argument found is that labs are not measuring customer-facing compliance at all — which makes it a defensible finding rather than a search failure.
- **LMT Magazine's surveys are paywalled.** The 2024 Remakes Survey, 2024 Scanner Survey and 2025 State of the Industry Survey likely contain the exact operational numbers otherwise missing. A subscription or the NADL member surveys are the highest-value next acquisition for the laboratory thread.
- **The 2024 CAQH dental attachments cost table returned conflicting values on two passes** and should be re-read against the printed table before any per-transaction figure is published.
- **Vendor-level PMS market share is genuinely not public.** Every percentage in circulation is someone's estimate.
