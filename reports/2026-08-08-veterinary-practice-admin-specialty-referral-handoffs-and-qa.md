# Veterinary Practice Administration & Specialty Referral Coordination — Handoffs and QA

**Market research cycle report**

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market claimed** | Veterinary practice administration and specialty referral coordination |
| **Angle claimed** | handoffs-and-qa |
| **Claim ID** | `0f90c511` |
| **Date** | 2026-08-08 |
| **Report path** | `reports/2026-08-08-veterinary-practice-admin-specialty-referral-handoffs-and-qa.md` |

### Why this assignment over the others available

At claim time the ledger held 33 completed reports and 385 open backlog assignments across 269 markets, of which 239 markets had zero completed entries. Selection followed the stated preference order:

**(a) Breadth first.** Companion-animal veterinary medicine is a sector the catalog has never touched. The nearest completed neighbour is *Dental and specialty clinic practice administration* (2026-08-08, handoffs-and-qa) — human dentistry. Everything else in the healthcare cluster (medical billing, home care/EVV, independent pharmacy) is human-side and payer-driven. Veterinary medicine is structurally different in the one way that matters most for this catalog: **HIPAA does not apply**, there is no CMS, no ICD-10 mandate, no HITECH incentive, and no TEFCA. The regulatory scaffolding that forced human healthcare into interoperability is simply absent, which means the manual workarounds are still in place and still visible.

**(b) Evidence availability.** This market has an unusually good primary-source base for a research cycle: a peer-reviewed referral-satisfaction survey with hard turnaround numbers ([JVIM, n=187 rDVMs + 92 specialists](https://academic.oup.com/jvim/article/32/2/822/8449637)); a brand-new professional guideline published specifically about this handoff ([2025 AAHA Referral Guidelines](https://www.aaha.org/resources/2025-aaha-referral-guidelines/)); a vendor-independent quantified productivity study ([IDEXX, n=786](https://www.prnewswire.com/news-releases/groundbreaking-idexx-study-reveals-opportunities-to-increase-veterinary-practice-productivity-301750165.html)); a sector census of the receiving side ([Instinct, ~1,600 ER/specialty hospitals](https://info.instinct.vet/state-of-er-specialty-veterinary-care-2024)); and an unusually candid independent technical analysis of why the software doesn't connect ([Prior Knowledge & Practice](https://priorknowledgeandpractice.substack.com/p/the-pims-integration-problem-is-real)).

**(c) Angle diversity.** `handoffs-and-qa` was the least-covered angle in the ledger (7 completed, versus 10 for core-practitioner-workflow and 8 each for the other two). This market's defining problem *is* the handoff, so the angle is not a stretch fit.

**Assignments remaining in backlog after this claim:** 384 (before this report's discovered additions).

---

## 1. Market examined

### The two sides of the handoff

This report examines a single transaction — the transfer of a patient, and the record that describes it, between two independent veterinary businesses — from both ends.

**Side A — the referring practice (rDVM).** A general/primary-care companion animal clinic. The US has roughly 30,000–35,000 companion animal practices ([Prior Knowledge & Practice](https://priorknowledgeandpractice.substack.com/p/the-pims-integration-problem-is-real) cites ~30,000; [Insurnest](https://insurnest.com/blog/veterinary-invoice-standardization-pet-insurance-claims/) cites 35,000). Typical staffing is 1–6 veterinarians plus 4–20 support staff (technicians/nurses, veterinary assistants, and client service representatives — "CSRs" — who are the front desk). The person who actually executes a referral is usually a CSR or a veterinary technician, not the veterinarian.

**Side B — the receiving hospital (specialty / emergency).** As of 2024 there were approximately **1,600 emergency, specialty and urgent-care veterinary centers** in the US, employing an estimated **131,200 people, averaging 82 employees per facility**; 42% corporate-owned, 32.5% privately owned, 18.6% partnership/group ([Instinct, *State of ER & Specialty Veterinary Care 2024*](https://info.instinct.vet/state-of-er-specialty-veterinary-care-2024)). 51.3% run 6–20 full-time veterinarians. These hospitals employ a dedicated job title — **referral coordinator** or **referral specialist** — whose entire function is managing this handoff.

There are **20,636 active board-certified veterinary diplomates** in the US as of 31 December 2025, of whom the referral-relevant clinical colleges dominate: ACVIM 4,537 (small animal internal medicine 1,957; oncology 656; neurology 557; cardiology 497) and ACVS 2,588 (small animal 1,167) ([AVMA](https://www.avma.org/resources-tools/reports-statistics/veterinary-specialists)).

**Side C — the third parties who also demand records.** Pet insurers, reference and histopathology laboratories, teleradiology reading groups, and (increasingly) online pharmacies. North American pet insurance covered **7.6 million pets at end-2025 on $6.2B gross written premium, up 8.5% in pets and 19.4% in premium year over year**, though still only ~4.3% of pets ([NAPHIA](https://naphia.org/industry-data/); [Insurance Business](https://www.insurancebusinessmag.com/us/news/breaking-news/naphia-only-4-27-of-us-pets-insured-despite-decade-of-doubledigit-growth-580314.aspx)). Every one of those policies is a potential records request landing on a practice's front desk.

### Organization size most likely to benefit

The sweet spot for the tools proposed here is:

- **rDVM side:** 1–4 doctor independent practices and small 2–8 location groups, where nobody has a full-time records person and the referral packet is assembled between appointments.
- **Specialty side:** single-site and 2–5 site specialty/ER hospitals with 1–3 referral coordinators — large enough to feel the volume, too small to fund a custom integration project or to be a priority customer for IDEXX.
- **Explicitly outside scope:** the large consolidators (Ethos/NVA, BluePearl/Mars, VEG, Thrive) who will build or buy platform solutions, and academic teaching hospitals who mostly already run rVetLink.

### Type of user

Non-technical. The primary user is a CSR, referral coordinator, or veterinary technician earning around $45–60k (technician average ~$57,000 per the Instinct report), working on a Windows desktop, comfortable with a PIMS and Outlook and a scanner, and with essentially zero tolerance for setup friction. The secondary user is the practice owner or hospital administrator who signs off. Any tool that requires an IT project is dead on arrival.

---

## 2. How the work is performed

### 2.1 The outbound referral (rDVM → specialist)

1. **The decision.** A general practitioner determines a case exceeds their scope — a mass needing oncology, a cruciate needing surgery, a seizure needing neurology, a refractory GI case needing internal medicine. The 2025 AAHA Referral Guidelines formalize three modes: general collaborative conversation, professional-to-professional consultation (no transfer of care), and hands-on referral (formal transfer) ([dvm360 summary](https://www.dvm360.com/view/aaha-releases-2025-guidelines-for-effective-veterinary-specialist-referrals)).

2. **The client conversation.** The GP explains why, sets cost expectations, and warns that the specialist may repeat diagnostics. AAHA specifically calls out that primary teams often *cannot* give accurate estimates before specialist assessment, and recommends normalizing that conversation.

3. **Choosing the destination and learning its rules.** Every receiving hospital has different requirements, and they are not uniform even *within* a hospital. UF's Small Animal Hospital, for example, **requires** a referral letter plus supporting documentation for Dentistry, Infectious Disease, Internal Medicine, Medical Oncology, Radiation Oncology and Surgical Oncology, but treats it as optional for Cardiology, Dermatology, Neurology and Ophthalmology, and requires a separate appointment-request form for non-emergent Orthopedic Surgery ([UF](https://smallanimal.vethospital.ufl.edu/contact-us/referring-veterinarians/)). Submission channels are equally scattered: Integrity Veterinary Center runs *two* separate email addresses — `referrals@` for the case and `records@` for the documents — plus a phone line and a web form with a 40 MB per-file cap ([Integrity](https://integrityvetcenter.com/for-veterinarians/how-referrals-work/)).

4. **Assembling the packet.** A CSR or technician exports the patient history from the PIMS — AVImark (25.4% share), IDEXX Cornerstone (19.5%), ezyVet (16.5%), and a long tail of 12+ others making up 38.6% ([Prior Knowledge & Practice](https://priorknowledgeandpractice.substack.com/p/the-pims-integration-problem-is-real)) — usually as a PDF or a print-to-PDF of the chart. They then hunt down the attachments: reference lab PDFs (IDEXX, Antech), in-house analyzer printouts, radiographs, prior specialist reports that were themselves received as faxes and scanned back in. Radiographs go separately, in DICOM, if the receiving hospital can take them — UF states "Digital radiographs are accepted DICOM format" and offers a fax line for paper items.

5. **Transmission.** Fax, email attachment, portal upload, or a burned CD/USB handed to the client. Fax remains widespread: it is described as "the most notorious offender" in a workflow analysis of inter-clinic record transfer ([PupPilot](https://www.puppilot.co/blog/from-chaos-to-continuity-automating-health-record-transfers-between-clinics)), and VitusVet's practitioner-facing critique lists fax's failure modes as: doesn't work after hours, staff forget to send, illegible copies, and excessive time cost on both ends ([VitusVet](https://vitusvet.com/blog/five-reasons-the-veterinary-referral-process-is-broken/)).

6. **What actually arrives.** Often nothing, or not in time. VitusVet's canonical example: a client calls an oncologist Monday, gets a Thursday appointment, and the records "STILL have not arrived" on Thursday. PetVet Magazine, summarizing specialists and ER doctors, reports that "the most common frustration expressed by specialists and emergency doctors was the lack of complete, legible records" ([PetVet Magazine](https://digital.petvetmagazine.com/issue/february-march-2023/5-ways-to-streamline-referrals-for-successful-collaborative-care/)).

### 2.2 Intake at the specialty hospital

The referral coordinator's posted duties are the workflow: answering incoming calls and triaging routine vs. emergency; scheduling consults, procedures and rechecks; **"gathering and maintaining accurate client and patient information"**; coordinating communication between clients, specialists, technicians and leadership; providing estimates; and acting as liaison to the referring veterinarian ([Thrive Pet Healthcare posting](https://careers.thrivepetcare.com/jobs/17592341-veterinary-referral-coordinator)). Notably, the posting names **no software at all** for the records-handling portion of the job.

In practice, intake means: open the `records@` inbox and the fax queue; identify which of 40 pages belongs to which patient; read a narrative chart written in another practice's shorthand; extract signalment, presenting complaint, current medications and doses, relevant lab values with dates, and what imaging has already been done; retype the essentials into the receiving hospital's own EMR (Instinct, ezyVet, Cornerstone); attach the PDF; and call the rDVM back for whatever is missing.

Two independently reported figures frame the cost of that retyping. Duplicate data entry across a single patient visit is estimated at **15–30 minutes per visit** across four or five separate entry points ([Digitail](https://digitail.com/blog/5-hidden-time-drains-stealing-hours-from-your-vet-team/)). And manual transcription of clinical data carries a **5–15% error rate**, with one cited study finding a **73% discrepancy rate in manually entered lab results** ([PupPilot](https://www.puppilot.co/blog/veterinary-data-interoperability-the-complete-guide-to-connecting-pims-labs-insurers)) — a figure I flag as tentative because the underlying study is not identified, but the direction is consistent with everything else.

### 2.3 The return leg (specialist → rDVM)

This is where the measurable failure lives. In the JVIM referral satisfaction study, the **average wait for the referring veterinarian to receive a discharge statement was 9 days — median 2, range 0 to 365** ([JVIM](https://academic.oup.com/jvim/article/32/2/822/8449637)). Satisfaction with discharge turnaround scored 68.33/100, well below satisfaction with quality of care (88.40), and the delay was negatively associated with overall satisfaction. Poor communication ranked as the third-largest barrier to referral named by referring veterinarians (15.5%), behind cost (26.4%) and lack of rDVM involvement (16.9%).

Practitioner-facing writing describes the same gap from the GP's chair: *"When a patient is referred to a specialist, your clinic sends the records. But do you get the specialist's SOAP notes and diagnostic test results back? Often not, or only after repeated calls"* ([PupPilot](https://www.puppilot.co/blog/from-chaos-to-continuity-automating-health-record-transfers-between-clinics)). VitusVet notes that most referring vets receive only a discharge fax, with no visibility into patient status during the stay.

This matters commercially, not just clinically. AAHA cites Collaborative Care Coalition research that client perceptions were **six times more likely to improve after a referral** when the primary care team stayed engaged. For a specialty hospital, the return leg *is* the marketing channel — and it is currently averaging nine days.

### 2.4 The parallel handoffs

The same practice, the same front desk, and often the same person handles three more outbound document flows:

- **Diagnostic lab and histopathology submissions.** Every reference lab and university diagnostic lab has its own requisition form (see e.g. [Iowa State](https://vetmed.iastate.edu/vpath/wp-content/uploads/Histopath-submission-Master-080520.pdf), [Cornell AHDC](https://www.vet.cornell.edu/sites/default/files/2024-11/AHDC-WEB-1001%20Histopathology%20Submission%20Form_V1.pdf)). A histopath submission with no clinical history produces a report the clinician can't act on.
- **Teleradiology.** The 2024 ACVR/ECVDI consensus statement specifies the minimum report header: client name, patient name/indicator, study type, study date and time, study location, report requester, report status, and *"relevant historical and clinical details, including specific clinical queries."* It states plainly that when pertinent information is absent and cannot easily be obtained, the radiologist should "seek it, provide the best possible interpretation, or **decline service**" ([ACVR/ECVDI, PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC11649853/)). Teleradiology SLAs typically run 2–4h routine / 1–2h urgent for radiographs and 4–8h for CT ([Asteris](https://www.asteris.com/blog/blog-veterinary-teleradiology-turnaround-time-sla/)) — turnaround the practice pays for and then squanders by submitting an incomplete history.
- **Pet insurance records requests.** Insurers want the *full* record: clear owner and pet identification, complete SOAP notes rather than after-visit summaries, and **actual numerical lab values with reference ranges** rather than "CBC normal," because they are looking for pre-existing conditions ([Lemonade](https://www.lemonade.com/pet/explained/pet-insurance-optimized-medical-records/)). Submission is by email or fax with a policy number, and "a single digit error can delay processing."

### 2.5 The software situation

There is a real product in this space: **rVetLink** (IDEXX). It gives a specialty hospital a branded referral portal, lets rDVMs submit cases from phone or desktop, auto-uploads reports/results/imaging from integrated PIMS, and pushes status notifications. Referring practices pay nothing; the specialty hospital pays a setup fee plus monthly subscription. It integrates directly with ezyVet, Cornerstone, DVMAX and ImproMed Infinity ([IDEXX](https://software.idexx.com/products/rvetlink)).

Its limits define the opportunity. It solves the transaction between *one* specialty hospital and the rDVMs who use *that hospital's* portal. It does nothing for a GP practice that refers to six different hospitals, four labs and two teleradiology groups — each with a different portal, form and requirement set. And on the receiving side it does not read an inbound 40-page fax from a non-integrated practice, which is the actual daily work.

The structural reason nothing better exists is well documented. Around 15 PIMS platforms with meaningful share sit beneath 140+ point solutions, a theoretical integration surface of 2,100+ pairs. APIs are "closed, undocumented, or fee-gated"; schemas don't align (`patient_name_first`/`patient_name_last` vs. `patient_full_name`); and above both, the semantic layer is unsolved — "Vomiting" vs "Emesis" vs "V+", "IMHA" vs "Immune-mediated hemolytic anemia", "DM" vs "Diabetes" ([Prior Knowledge & Practice, layers](https://priorknowledgeandpractice.substack.com/p/the-three-layers-of-veterinary-software)). Human medicine bought its way out with $30B of HITECH incentives against a $10–13B EHR market; the entire veterinary PIMS market is **$200–400M/year**. Nobody is coming to fix this with a platform. **85% of practices say their software does not integrate well with their PIMS** ([IDEXX study, n=786](https://www.prnewswire.com/news-releases/groundbreaking-idexx-study-reveals-opportunities-to-increase-veterinary-practice-productivity-301750165.html)).

Standards exist but are thin: VetXML/VetEnvoy is real but UK-centric ([VetXML Consortium](http://www.vetxml.co.uk/en/about-the-consortium/)); VeNom coding and a SNOMED-CT veterinary extension exist but adoption is inconsistent ([VeNom](http://venomcoding.org/)); DICOM is the one genuinely working standard because it came from human radiology. An open-source PIMS, [OpenVPM](https://openvpm.com/) (AGPLv3, REST API, $79/location/month managed tier), has appeared explicitly because "your data is locked in."

---

## 3. Most important problems, ranked

### P1 — The inbound referral packet must be read by a human before it is usable

**Who:** Referral coordinators, intake technicians and specialists at ER/specialty hospitals.
**When:** Every referred case. At ~1,600 hospitals averaging 82 staff, this is a continuous, all-day activity.
**Currently handled by:** A person opening a PDF or fax, reading someone else's narrative, and retyping signalment, history, medications, and lab values into the receiving EMR.
**Why inadequate:** It is the single largest retyping task in the transaction, it is where transcription error enters the clinical record, and it is unskilled work being done by clinically-trained staff. Duplicate data entry is estimated at 15–30 min per patient visit across all entry points; manual clinical transcription runs 5–15% error.
**Frequency:** Continuous.
**Cost:** For a hospital taking 30 referrals/day, even 10 minutes of extraction per case is 5 staff-hours/day — roughly a full-time position, in a sector where 78% report staffing shortages and 79.3% report technician turnover.
**Evidence:** Instinct sector census; Digitail time-drain analysis; PupPilot; Thrive job posting (records-gathering is an explicit duty with no named software).
**Confidence:** High on existence and mechanism; medium on the per-case minute count.

### P2 — The return report reaches the referring vet late, or not at all

**Who:** Referring general practitioners; secondarily the specialty hospital, which loses referral volume.
**When:** After every referral episode and every ER visit.
**Currently handled by:** A specialist dictating or typing a discharge/consult letter when they get to it, then someone faxing or emailing it. Whether it arrived is generally not tracked.
**Why inadequate:** The measured average is **9 days** (median 2, range 0–365). The GP is fielding client questions about a case they have no report on. AAHA's headline finding is that continued rDVM engagement makes positive client perception six times more likely — impossible when the GP is uninformed.
**Frequency:** Every case.
**Cost:** Directly measurable in referral-source retention. Satisfaction with discharge timeliness scored 68.33 vs. 88.40 for quality of care — the gap is entirely administrative, and 15.5% of rDVMs name poor communication as a top barrier to referring at all.
**Evidence:** JVIM (n=279 total respondents); AAHA 2025 guidelines; VitusVet; PupPilot.
**Confidence:** High. The JVIM population is equine, which is a genuine limitation — but the small-animal practitioner literature describes the identical failure qualitatively, and the AAHA guidelines were written in 2025 specifically because the problem persists.

### P3 — Records requests from insurers, new clinics and clients are unbounded manual assembly

**Who:** CSRs and practice managers at general practices, plus specialty hospitals.
**When:** Growing with insurance penetration — 7.6M insured pets, +8.5% YoY.
**Currently handled by:** Export from PIMS, hunt for attachments, print/scan, fax or email with a policy number on a cover sheet.
**Why inadequate:** What insurers actually need (complete SOAP notes; numerical lab values with reference ranges; unambiguous pet and owner identification) is systematically different from what a PIMS export produces (after-visit summaries, "CBC normal"). The consequence lands on the insurer and bounces back as another request: **35–45% of pet insurance claims require manual review**, manual claim processing costs **$40–60 vs $25–36**, resolution takes **15–30 days vs 3–7**, and error rates run **12–18% vs 2–5%**. Scanned/faxed documents drop OCR accuracy to **60–70%** against 92–97% for structured formats.
**Frequency:** Daily at any practice with insured clients.
**Cost/risk:** Beyond staff time, this is a compliance surface. HIPAA does not apply to veterinary records; state practice acts do, governing content, retention (CA 3 years, TX 5, NY 3, FL 3; AVMA recommends ≥5 where silent), release authorization and confidentiality. Releasing the wrong client's pages — a real risk when working from scanned fax piles — is a state-board matter.
**Evidence:** Insurnest; Lemonade; NAPHIA; co.vet records-law survey; AccountableHQ.
**Confidence:** High on the requirement mismatch and the regulatory frame. **Medium-low on the Insurnest percentages** — that is a vendor blog with no cited methodology, and the figures should be treated as directional, not as a basis for pricing.

### P4 — Outbound submissions to labs, radiologists and hospitals fail their recipient's requirements before they are sent

**Who:** GP practices sending to any external reader.
**When:** Every histopath submission, teleradiology study, and referral.
**Currently handled by:** Paper or PDF forms per recipient, filled from memory, with the clinical history section frequently left thin or blank.
**Why inadequate:** The recipient's own standards say what is required, and the recipient is entitled to refuse. ACVR/ECVDI: when pertinent clinical information is missing and cannot be obtained, the radiologist may "decline service." A histopath report without history is often non-diagnostic, which means a repeat biopsy — a second anesthesia on the patient and a second bill to a client already unhappy.
**Frequency:** Multiple per week at a typical GP practice.
**Cost:** A wasted teleradiology fee plus a lost 2–4h turnaround window; for histopath, the cost of a repeat procedure.
**Evidence:** ACVR/ECVDI consensus (PMC, open access); lab submission form specimens; UF/Integrity per-service requirement variation.
**Confidence:** High on the requirements; medium on failure frequency, which I could not quantify from public sources.

### P5 — Prior diagnostics arrive as an unstructured pile, so trends are invisible at the moment of decision

**Who:** Specialists receiving a chronic case.
**When:** Any referral with a history — most internal medicine, oncology and nephrology cases.
**Currently handled by:** The specialist flips through PDFs from IDEXX, Antech, in-house Abaxis/Heska and a prior specialist, each with a different layout, and mentally reconstructs the trend.
**Why inadequate:** It is precisely the task computers do well and humans do badly, and getting it wrong means repeating diagnostics — which AAHA specifically flags as a referral failure mode and instructs teams to document against.
**Frequency:** Most non-trivial referrals.
**Cost:** Duplicate diagnostics billed to the client, plus specialist time (the scarcest resource in the transaction) spent on clerical reconstruction.
**Evidence:** AAHA 2025 (documenting completed/pending tests to avoid duplication); interoperability analyses on format fragmentation.
**Confidence:** Medium-high.

### P6 — Medication lists cross the boundary as free text and must be reconciled by hand

**Who:** Receiving clinicians.
**When:** Every transfer of care.
**Currently handled by:** Reading the med list out of a narrative and re-deriving mg/kg from a weight that may be stale.
**Why inadequate:** Veterinary free-text notes are documented as hostile to automated extraction — local shorthand ("bilat. ear," "PU/PD query Cushing's," "?IBD"), hedging ("I suspect we may be looking at early-stage otitis"), and procedures buried in narrative. Reported search sensitivity for diagnoses in free text ranges from **33% to 98%**, and accuracy can fall to **60%** on hard free-text coding tasks ([Tandem Health](https://tandemhealth.ai/resources/knowledge/why-veterinary-free-text-notes-break-automated-coding)).
**Frequency:** Every case.
**Cost/risk:** Direct patient-safety and professional-liability exposure. This is also the problem where AI is *most* justified and *least* trustworthy — see the design notes in §4.
**Confidence:** High on the difficulty; the same evidence that motivates the tool constrains how it may be built.

### P7 — Imaging transfer is a separate, badly-labelled channel

**Who:** Both sides.
**When:** Any referral involving radiographs, CT or MRI.
**Currently handled by:** DICOM on CD/USB, a vendor cloud link, or — worst case — JPEGs pasted into an email.
**Why inadequate:** DICOM is the one working standard in the stack, but veterinary DICOM tag hygiene is poor: patient name populated with the owner's surname, species/breed absent or in the wrong tag, study description blank. Recipients then can't match the study to the case. Portals impose file-size caps (Integrity: 40 MB) that a CT study blows through instantly.
**Frequency:** Common.
**Cost:** Repeat imaging, or a specialist reading a study they cannot confirm belongs to the patient in front of them.
**Confidence:** Medium. The mechanism is well established from human radiology and from the existence of a whole category of veterinary PACS products; I did not find a veterinary-specific quantification of tag-error rates. Flagged for validation.

---

## 4. Application opportunities

Nine concepts. All are deliberately *file-in / file-out* rather than integrations, because the integration surface is provably hostile and any tool depending on PIMS APIs inherits a five-year problem.

---

### A1 — Records Release Packet Assembler ("RelayVet")

- **Working title:** Records Release Packet Assembler
- **Intended user:** CSR or practice manager at a 1–4 doctor GP practice; records clerk at a specialty hospital.
- **Problem solved:** Assembling a records release that satisfies the specific recipient's requirements on the first attempt, and logging the disclosure.
- **Current workflow:** Export chart from PIMS → hunt down lab PDFs and imaging reports in a shared folder → print/scan/merge in whatever order they land → attach to email or fax with a handwritten cover sheet → no record kept of what was sent to whom.
- **Proposed workflow:** Drop the PIMS export and attachments into the tool → pick a **recipient profile** (Trupanion, Lemonade, Nationwide, "referral hospital — surgery", "new clinic — client transfer") → the tool filters to the requested date range, merges into one paginated, bookmarked PDF with a generated index, stamps patient/owner/policy identifiers on **every page**, runs a completeness check against the profile, and writes a disclosure log entry.
- **Inputs:** PDF exports, lab PDFs, image files; a recipient profile (YAML/JSON); date range; identifiers.
- **Outputs:** One indexed PDF; a completeness report listing what the profile requires and what wasn't found; a CSV disclosure log line (date, requester, authorization basis, date range, page count).
- **Essential features:** Profile library; page stamping; bookmark/index generation; date filtering; completeness checklist; disclosure log; "pages that mention a different patient name" warning (a cheap regex guard against the classic fax-pile leak).
- **Excluded from v1:** PIMS integration; e-fax sending; OCR of handwritten notes; e-signature; cloud storage.
- **AI:** *Optional.* Everything above is conventional PDF work. AI adds value only in one place — checking whether an included visit note actually contains all four SOAP elements rather than just an after-visit summary. Ship v1 without it.
- **Why not a spreadsheet:** The artifact is a PDF, not a table. A spreadsheet cannot merge, stamp, bookmark or verify.
- **Complexity:** Medium. **Learning:** ~20 minutes.
- **Value:** Eliminates the bounce-back cycle. If the directional Insurnest figures hold, each avoided bounce saves the practice a second assembly and the client 1–3 weeks of claim delay.
- **Risks/regulatory:** State practice acts govern release authorization, confidentiality and retention (CA 3y, TX 5y, NY 3y, FL 3y; AVMA ≥5y where silent). HIPAA does not apply, which lowers the compliance bar but does *not* remove state-board exposure. The tool must never auto-transmit; it assembles, a human sends. Must run fully local — records must not leave the practice.
- **Substitutes:** Adobe Acrobat plus discipline; PIMS "print record" functions; ScanSTAT-style ROI outsourcing (priced for human medicine).
- **Why still attractive:** No substitute encodes *per-recipient requirements*, and none produces a disclosure log. The profile library is the moat and it is community-maintainable.
- **Paid customization:** High — a practice group's own profiles, letterhead, insurer list, and PIMS export quirks.

---

### A2 — Inbound Referral Brief Generator

- **Intended user:** Referral coordinator / intake technician at a specialty or ER hospital.
- **Problem solved:** Turning a 40-page inbound fax or PDF into a one-page structured case brief plus an explicit list of what's missing.
- **Current workflow:** Read the whole thing; retype the essentials; call the rDVM for gaps; hope nothing was missed.
- **Proposed workflow:** Drop the inbound PDF in → OCR if needed → extract into a fixed schema (signalment, weight + date of weight, presenting complaint, problem list, current medications with dose/route/frequency, most recent lab panel with dates, imaging performed, known allergies/adverse reactions, rDVM name and callback) → render a one-page brief with **every extracted field hyperlinked to its source page** → render a second page listing required-but-absent fields.
- **Inputs:** PDF/TIFF (native or scanned).
- **Outputs:** One-page HTML/PDF brief with page-level provenance; a gap list; a structured JSON/CSV for optional paste into the EMR.
- **Essential features:** OCR fallback; schema extraction; **click-through to source page for every field**; gap list; confidence flags on low-certainty extractions.
- **Excluded from v1:** Writing into the EMR; diagnosis coding; any clinical interpretation or recommendation.
- **AI:** *Needed.* This is the one concept where conventional parsing genuinely fails — narrative charts, local shorthand, hedged language. But the free-text literature (33–98% sensitivity; ~60% accuracy on hard tasks) is the design constraint, not a footnote. **The tool must be built as an assistive index into the source document, never as a replacement for it.** Every field shows its provenance; nothing is presented as authoritative.
- **Why not a spreadsheet:** The input is unstructured prose.
- **Complexity:** Medium. **Learning:** ~30 minutes, most of it spent learning to distrust it appropriately.
- **Value:** If it saves 8 of 12 minutes per case at 30 cases/day, that is ~4 staff-hours/day.
- **Risks:** Extraction error entering a clinical record is the central hazard, hence provenance-first design and a hard rule against auto-writing to the EMR. Local or private-endpoint inference only; a fax pile contains other people's client data.
- **Substitutes:** rVetLink (only for integrated, portal-using rDVMs); human labour.
- **Paid customization:** High — house schema, EMR-specific export format, specialty-specific field sets (oncology vs. cardiology need different summaries).

---

### A3 — rDVM Report Aging & Send Ledger

- **Intended user:** Specialty/ER hospital administrator or referral coordinator.
- **Problem solved:** Nobody currently owns the fact that a discharge report hasn't gone out. The measured average is 9 days.
- **Current workflow:** Reports go out when the clinician gets to them; delivery is unverified; the GP calls to chase.
- **Proposed workflow:** Daily case-list export from the EMR + a send log (manual tick, or parsed e-fax/email confirmations) → an aging queue grouped by clinician and by referral source → a per-rDVM ledger showing every case sent, when, and by what channel → a weekly "your referral sources are waiting on these" email to service heads.
- **Inputs:** CSV case export; send confirmations.
- **Outputs:** Aging queue (overdue / due today / sent); per-rDVM communication ledger; weekly summary.
- **Essential features:** Configurable SLA per case type (ER discharge: 24h; specialty consult: 72h); clinician and referral-source rollups; sent-log with channel and timestamp.
- **Excluded from v1:** Writing the report; sending it; anything resembling a general task manager. **This is a single queue with a single clock.** If it grows tabs, it has failed.
- **AI:** *Inappropriate.* Dates and joins.
- **Why not a spreadsheet:** Honestly, a well-built spreadsheet gets you most of the way. The tool earns its keep by ingesting the EMR export automatically and by holding the per-rDVM ledger over time.
- **Complexity:** Small. **Learning:** ~15 minutes.
- **Value:** Directly attacks a measured 9-day mean against a 68/100 satisfaction score on a metric that drives referral volume.
- **Risks:** Low. Could be perceived as clinician surveillance — frame and default it as service-level, not individual, reporting.
- **Substitutes:** rVetLink status notifications; EMR task lists; spreadsheets.
- **Why still attractive:** Cheap, obvious, and the thing that makes it real is the *sent-and-confirmed* log, which no substitute keeps.
- **Paid customization:** Medium.

---

### A4 — Submission Pre-Flight Checker (lab / teleradiology / referral)

- **Intended user:** GP technician or CSR preparing an outbound submission.
- **Problem solved:** Catching a missing clinical history, absent clinical question, or unmatched patient ID *before* the submission leaves.
- **Current workflow:** Fill the recipient's PDF form from memory; send; discover the problem when a non-diagnostic report comes back.
- **Proposed workflow:** Choose recipient profile → the tool presents that recipient's required fields as a short form (pre-filled from the case where available) → validates completeness, checks that the DICOM study's patient identifier matches the requisition, warns when the clinical-question field is empty → emits the completed requisition plus a packaging manifest.
- **Inputs:** Recipient profile; case data; optional DICOM folder.
- **Outputs:** Completed requisition PDF; validation report; manifest.
- **Essential features:** Profile library (built directly from published lab forms and the ACVR/ECVDI header requirements); required-field validation; DICOM ID cross-check; clinical-question prompt.
- **Excluded from v1:** Submitting to lab portals; specimen tracking; billing.
- **AI:** *Inappropriate* for validation. Rules and required-field logic. (A "your history says 'mass' — the lab asks for location, duration and growth rate" prompt is a template, not a model.)
- **Why not a spreadsheet:** Needs to read DICOM headers and emit a filled PDF.
- **Complexity:** Small. **Learning:** ~10 minutes.
- **Value:** Each avoided non-diagnostic histopath report avoids a repeat biopsy; each avoided teleradiology re-query preserves a paid 2–4h turnaround.
- **Risks:** Profile drift — labs revise forms. Version the profiles and show the profile's date in the output.
- **Substitutes:** The labs' own web portals (where they exist, one per lab).
- **Why still attractive:** The practice deals with 4–8 recipients; no single recipient's portal solves the practice's problem. A neutral, local, multi-recipient checker is precisely the gap enterprise vendors have no reason to fill.
- **Paid customization:** High, and naturally recurring — profile maintenance is a service.

---

### A5 — Longitudinal Diagnostics Timeline Builder

- **Intended user:** Specialist receiving a chronic case; also GPs managing CKD, diabetes and thyroid patients.
- **Problem solved:** Reconstructing an analyte trend from lab PDFs issued by several different labs in several different layouts.
- **Current workflow:** Flip through PDFs; mentally interpolate; sometimes re-run the panel.
- **Proposed workflow:** Drop the folder of lab PDFs in → layout-aware extraction of analyte / value / units / reference range / date → one tidy longitudinal table plus small-multiple sparklines with reference bands → flag unit mismatches between labs (the classic mg/dL vs µmol/L trap) → export CSV and a one-page PDF for the chart.
- **Inputs:** Lab report PDFs (IDEXX, Antech, in-house analyzers).
- **Outputs:** Tidy CSV; sparkline sheet; unit-conflict warnings.
- **Essential features:** Per-lab layout templates; unit normalization with explicit conflict flagging; reference-range banding; provenance column (which file/page each value came from).
- **Excluded from v1:** Clinical interpretation, staging, or alerts. It charts; it does not opine.
- **AI:** *Optional.* Template extraction handles the big labs. Reserve a model for unrecognized layouts only, and mark those values as low-confidence.
- **Why not a spreadsheet:** The spreadsheet is the *output*. The work is getting values out of heterogeneous PDFs.
- **Complexity:** Medium. **Learning:** ~15 minutes.
- **Value:** Avoids duplicate diagnostics — the exact failure AAHA tells teams to document against — and returns specialist minutes, the most expensive minutes in the building.
- **Risks:** A misextracted creatinine is a clinical hazard. Provenance column and confidence marking are non-negotiable; never suppress the source document.
- **Substitutes:** IDEXX VetConnect PLUS trends *within* IDEXX only — which is exactly the neutrality problem.
- **Paid customization:** High — a hospital's own in-house analyzer layouts.

---

### A6 — Medication Reconciliation Sheet Generator

- **Intended user:** Receiving clinician or technician at referral intake.
- **Problem solved:** Turning a free-text medication narrative into a checkable table with computed mg/kg.
- **Current workflow:** Read the narrative; re-derive dosing by hand; hope the weight is current.
- **Proposed workflow:** Paste or drop the inbound record → extract candidate medication mentions → build a table (drug, strength, dose, route, frequency, computed mg/kg against the recorded weight, weight date, prescriber, last dispensed) → flag out-of-range doses, duplicate therapy within a class, and **stale weights** → present for human confirmation before anything is saved.
- **Inputs:** Record text/PDF; patient weight and its date.
- **Outputs:** Reconciliation table (PDF/CSV) with a confirm-and-initial column.
- **Essential features:** Extraction with per-row provenance; mg/kg computation; species-specific dose-range reference (a maintained data file, not a model); duplicate-class detection; stale-weight warning; mandatory human confirmation step.
- **Excluded from v1:** Prescribing, dispensing, interaction checking beyond duplicate-class, controlled-substance logging.
- **AI:** *Needed for extraction, inappropriate for the check.* The dose-range comparison must be deterministic table lookup — a model must never be the thing that says a dose is safe.
- **Why not a spreadsheet:** The input is prose; the arithmetic and range check are the easy part.
- **Complexity:** Medium. **Learning:** ~20 minutes.
- **Value:** Removes a genuine patient-safety hole at the handoff.
- **Risks:** The highest-liability concept here. Ship it as a worksheet a clinician signs, never as a decision. Given 33–98% extraction sensitivity in free text, the UI must make omission visible — show the source paragraph alongside every row, and show paragraphs it *didn't* extract from.
- **Substitutes:** None specific to the handoff.
- **Paid customization:** Medium-high — house formulary ranges.

---

### A7 — DICOM Study Packager & Identity Fixer

- **Intended user:** Imaging technician at either end.
- **Problem solved:** Studies that arrive unlabelled, mislabelled, or too large for the recipient's portal.
- **Current workflow:** Burn a CD, or upload and hope; recipient can't confirm the study matches the patient.
- **Proposed workflow:** Point at a study folder → audit tags against a house convention (PatientName, PatientID, species/breed, StudyDescription, ReferringPhysicianName) → propose corrections with a full before/after diff → write a corrected copy (**never in place**) → split into portal-sized parts if needed → emit a transfer manifest listing series, image counts, and a checksum per file.
- **Inputs:** DICOM folder.
- **Outputs:** Corrected copy; manifest; size-split archives.
- **Essential features:** Tag audit; safe non-destructive rewrite with audit trail; manifest with checksums; size splitting; optional pseudonymization for teaching/consult use.
- **Excluded from v1:** Viewing, PACS functions, cloud hosting, any image processing.
- **AI:** *Inappropriate.*
- **Why not a spreadsheet:** Binary format.
- **Complexity:** Small-medium (pydicom does the heavy lifting). **Learning:** ~20 minutes; the user is already technical about imaging.
- **Value:** Prevents repeat imaging and the "is this the right dog?" call.
- **Risks:** Editing DICOM tags alters a medical record — hence copy-only, with a diff log retained. Note that pseudonymization here is a courtesy feature, not a legal requirement, since HIPAA doesn't apply.
- **Substitutes:** Full veterinary PACS products (dicomPACS Vet, PostDICOM, MedDream) — which solve storage and viewing, at storage-and-viewing prices.
- **Why still attractive:** A practice that already has a PACS still has no clean tool for *outbound* packaging and identity QA.
- **Confidence caveat:** This concept rests on the weakest evidence in the set (P7). Validate before building.
- **Paid customization:** Medium.

---

### A8 — Referral Loop-Closure Audit (GP side)

- **Intended user:** Practice manager at a GP practice.
- **Problem solved:** The GP does not know which of their referred patients never generated a return report.
- **Current workflow:** Nobody tracks it. The gap surfaces when a client asks a question the GP can't answer.
- **Proposed workflow:** Maintain a lightweight referral register (case, date, destination, service) → periodically reconcile against inbound documents (by scanning the records inbox/folder for matching patient names and destination senders) → produce an open-loop list: referred ≥N days ago, no report received.
- **Inputs:** Referral register (CSV, or entries made in the tool); inbound document folder.
- **Outputs:** Open-loop list; per-destination response-time report (which becomes real leverage when choosing where to refer).
- **Essential features:** Register; fuzzy matching of inbound docs to referrals; aging; per-destination scorecard.
- **Excluded from v1:** Email integration, client messaging, anything CRM-shaped.
- **AI:** *Optional* — only for matching inbound documents to register entries; fuzzy string matching handles most of it.
- **Why not a spreadsheet:** The register is a spreadsheet. The tool adds the reconciliation against inbound documents.
- **Complexity:** Small. **Learning:** ~15 minutes.
- **Value:** Moderate time savings; substantial risk reduction; the per-destination scorecard is a genuinely novel artifact — it gives the GP data for the conversation AAHA says they should be having.
- **Risks:** Low.
- **Substitutes:** None found.
- **Paid customization:** Low-medium.

---

### A9 — Referral Destination Requirements Profile Kit

- **Intended user:** Practice manager; also the maintainer of profiles for A1 and A4.
- **Problem solved:** The requirement knowledge for each destination lives in someone's head or a binder, and each hospital differs *by service*.
- **Current workflow:** Institutional memory; a laminated sheet at the front desk.
- **Proposed workflow:** A small structured schema for a destination profile (per service: required documents, required form, submission channel, file-size cap, contact, promised turnaround) plus an editor and a one-page printable per destination — and a shared, versioned open profile repository seeded from public hospital referral pages.
- **Inputs:** Manual entry; seeded profiles.
- **Outputs:** Machine-readable profiles consumed by A1/A4; printable front-desk sheets.
- **Essential features:** Schema; editor; export; version stamps; diff when a profile updates.
- **Excluded from v1:** Scraping hospital websites automatically (fragile and impolite); any directory-of-hospitals ambition. **This is a schema and an editor, not a marketplace.**
- **AI:** *Inappropriate.*
- **Complexity:** Small. **Learning:** ~10 minutes.
- **Value:** Low standalone — this is infrastructure. It is listed because A1 and A4 both depend on it, and because a community-maintained open profile set is the durable asset in this whole space.
- **Risks:** Staleness. Version stamps and a visible "last verified" date.
- **Paid customization:** This *is* the customization product.

---

## 5. Opportunity ranking

Scored 1–5 on ten criteria (max 50).

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of implementation | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| A1 | Records Release Packet Assembler | 4 | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 5 | **44** |
| A2 | Inbound Referral Brief Generator | 5 | 5 | 5 | 4 | 3 | 4 | 4 | 5 | 3 | 5 | **43** |
| A4 | Submission Pre-Flight Checker | 3 | 4 | 4 | 5 | 5 | 5 | 4 | 5 | 4 | 4 | **43** |
| A3 | rDVM Report Aging & Send Ledger | 4 | 5 | 4 | 5 | 5 | 5 | 2 | 3 | 4 | 5 | **42** |
| A5 | Longitudinal Diagnostics Timeline | 4 | 5 | 5 | 4 | 3 | 4 | 5 | 4 | 4 | 4 | **42** |
| A6 | Medication Reconciliation Sheet | 5 | 5 | 4 | 4 | 3 | 4 | 4 | 4 | 3 | 4 | **40** |
| A8 | Referral Loop-Closure Audit | 3 | 4 | 3 | 5 | 5 | 5 | 4 | 3 | 3 | 4 | **39** |
| A7 | DICOM Packager & Identity Fixer | 4 | 4 | 4 | 4 | 4 | 5 | 3 | 4 | 4 | 3 | **39** |
| A9 | Destination Requirements Profile Kit | 2 | 5 | 2 | 5 | 5 | 5 | 3 | 5 | 4 | 4 | **40** |

### The top three

**A1 — Records Release Packet Assembler (44).** The strongest concept, and not because it is the most clever. It wins on the boring criteria: the problem occurs daily at essentially every practice, the volume is growing with insurance penetration (+8.5% pets YoY), the ROI is legible to a practice owner in one sentence, and — critically — **it needs no clinical judgment and no AI to deliver its core value.** It is PDF assembly, page stamping, and a checklist. That means it can be built correctly by one developer, it can be verified deterministically, and it carries no patient-safety liability. The per-recipient profile library is the piece that makes it hard to copy and easy to sell as a customization service, and it doubles as the shared asset behind A4 and A9. The disclosure log is a small feature that quietly addresses a real state-board exposure nobody currently tracks.

**A2 — Inbound Referral Brief Generator (43).** The highest-severity problem in the market and the concept a specialty hospital would pay most for — 1,600 hospitals averaging 82 staff, 78% reporting staffing shortages, doing this work by hand all day. It scores lower than A1 only on implementation and test data, and both discounts are real: the extraction problem is genuinely hard (33–98% sensitivity in the literature), and getting realistic sample records requires a partner practice willing to share de-identified charts. The provenance-first design is what makes it defensible: a tool that indexes the source document is honest about its own error rate in a way a tool that summarizes is not.

**A4 — Submission Pre-Flight Checker (43).** The best risk-adjusted first build. Smallest scope, no AI, requirements published in citable form by the recipients themselves (ACVR/ECVDI consensus, lab requisition forms), immediately demonstrable before-and-after, and it forces you to build the profile schema that A1 and A9 both need. If the goal is to enter this market with something shippable in weeks rather than months, this is the entry point.

### What to investigate next

**A4 first, A1 second.** Build A4 as the beachhead: it is small, it validates the profile schema, and it puts you in conversation with practice managers about their recipient list — which is exactly the discovery you need to build A1's profile library. Then A1 as the commercial product.

**A2 deferred until a partner exists.** Do not start it without a specialty hospital willing to supply de-identified inbound packets. Building a clinical extractor against synthetic data would produce a tool that fails in exactly the ways the free-text literature predicts.

**A3 is a candidate for a weekend build** to open doors on the specialty side, but its differentiation score of 2 is honest — do not build a business on it.

---

## 6. Validation plan

### Questions to ask practitioners

**GP practice managers and CSRs:**
- How many records requests did you fulfil last week? From whom — insurers, other clinics, clients, specialists?
- How long does one take, start to finish? How often does one come back asking for more?
- How many different referral destinations do you send to? Do you keep their requirements written down anywhere?
- Do you know which of the patients you referred last month generated a report back to you?
- What do you actually send — a PIMS export, a printed chart, a scan? Show me one.

**Specialty referral coordinators:**
- Walk me through the last referral that arrived this morning. What did you have to retype?
- How often do you call the rDVM back for something missing? What is it usually?
- What percentage of your inbound arrives by fax vs. email vs. portal?
- What is your internal target for getting a report back to the rDVM, and do you know whether you hit it?

**Specialists:**
- When a chronic case is referred, how do you reconstruct the lab trend?
- How often do you repeat a diagnostic because you couldn't confirm what was already done?

### Who to interview

- Practice managers at 1–4 doctor independent GP practices (VHMA membership is the natural channel).
- Referral coordinators at single-site specialty hospitals — deliberately *not* the corporate groups, whose workflows are being centralized.
- A veterinary technician specialist (VTS) in ECC.
- A boarded radiologist doing teleradiology reads, on submission quality specifically.
- A pet insurance claims adjudicator on what actually causes a claim to bounce.
- The [OpenVPM](https://openvpm.com/) maintainer — an aligned open-source project already fighting the same data-lock-in problem.

### Search terms for further research

`veterinary referral coordinator workflow`; `rDVM portal requirements <specialty>`; `histopathology submission form <lab name>`; `teleradiology submission clinical history requirements`; `pet insurance medical records request veterinary practice`; `VeNom coding adoption`; `veterinary DICOM tag conventions`; `VHMA records request survey`; `veterinary practice act medical records release <state>`; plus targeted forum reads on VIN (paywalled — needs a member contact), VetPartners, and the r/Veterinary and r/VetTech communities (both blocked to automated fetch in this environment; validate manually).

### Sample files and data needed

1. Three to five real PIMS record exports (de-identified) from **different** PIMS — AVImark, Cornerstone and ezyVet cover 61.4% of the market between them.
2. Ten inbound referral packets as actually received (fax scans included — the OCR-quality question is decisive for A2).
3. Lab report PDFs from IDEXX, Antech and at least two in-house analyzers, for the same patient across ≥3 dates.
4. A DICOM study as it left a GP practice, unedited, tag warts and all.
5. Referral requirement pages from 20 specialty hospitals — these are public and can be collected immediately.
6. Two or three insurer records-request letters.

### Simplest validating prototype

**One week, for A4:** a single-page local HTML tool with three hardcoded recipient profiles (one histopath lab, one teleradiology group, one specialty hospital surgery service). User picks a profile, fills the short form, drops a DICOM folder, and the tool reports "requisition complete / PatientID matches / clinical question present." Take it to five practice managers. If three of them say *"which lab profiles do you have?"*, the profile library is the product and A1 follows. If they shrug, the pre-flight framing is wrong and you should test A1's assembly value directly instead.

### Assumptions most likely to be wrong

1. **That practices perceive records assembly as a problem worth paying for.** It may be so normalized as invisible. This is the assumption that kills A1 — test it first, and test it by asking what they *did* last week, not what they think.
2. **That PIMS exports are consistent enough to parse.** If AVImark's export is unstable across versions, A1 and A5 both get much harder. Test with real files early.
3. **That the buyer exists.** A CSR feels the pain; a practice owner writes the cheque. If owners see this as front-desk overhead rather than revenue or risk, nothing sells. The disclosure log and the per-destination scorecard exist partly to give the owner a reason to care.
4. **That AI extraction clears the accuracy bar for clinical use.** The published range (33–98%) says it may not. Provenance-first design is the mitigation, but if coordinators don't trust it, they will re-read the source anyway and A2's value collapses.
5. **That the 9-day discharge finding generalizes from equine to small animal.** The qualitative small-animal literature agrees, but the hard number does not transfer. Verify before quoting it to a customer.
6. **That IDEXX doesn't simply extend rVetLink downward.** They own the PIMS, the labs and the portal. The defensible ground is precisely where IDEXX cannot go — neutral, multi-vendor, local-first tooling for practices that use *someone else's* lab.

---

## 7. Cross-industry patterns

Six patterns from this market that transfer to named backlog markets.

**Pattern 1 — Per-recipient submission profile driving a pre-flight validation (A1, A4, A9).**
The general shape: N senders, M recipients, each recipient publishing its own requirements, and no sender able to hold all M rule sets in their head. Transfers directly to: *Environmental laboratories producing regulator EDD deliverables (EQuIS and state formats)* — the same problem with more formal schemas; *First Article Inspection (AS9102) report production at small aerospace machine shops*; *Federal construction contractors on NAVFAC/USACE projects — UFGS submittal register*; *Aerospace supplier quality clause library administration*; *Certified payroll and prevailing wage compliance service providers*; *Title abstracting and independent title search contractors*.

**Pattern 2 — Inbound document pile → structured brief + explicit gap list, with per-field provenance (A2).**
Any desk where work arrives as someone else's unstructured documents. Transfers to: *Small third-party medical billing companies (RCM service bureaus)*; *Healthcare credentialing service bureaus and CVOs*; *Hospital and clinic release-of-information (ROI) departments*; *Legal process outsourcing vendors producing medical chronologies*; *Public adjusting firms*; *Mortgage post-closing QC and trailing document vendors*; *Freight factoring client onboarding/verification desks*. The provenance-first design rule — index the source, never replace it — is the transferable part, not the extraction itself.

**Pattern 3 — Outbound deliverable aging queue against a promised turnaround, with a send-and-confirm ledger (A3).**
Wherever a professional owes an external party a document by an implied deadline and nobody owns the clock. Transfers to: *Court reporting and deposition services firms (transcript production)*; *Accredited calibration laboratories (certificate delivery)*; *Fire protection ITM contractors (NFPA 25 reports to AHJs and owners)*; *Independent specification writers*; *Third-party estimate writing services (Xactimate desks)*; *Environmental laboratories (holding-time and report-due tracking)*.

**Pattern 4 — Cross-vendor result extraction into one longitudinal, unit-normalized table (A5).**
Where the same measurand is reported over time by several vendors in several layouts. Transfers to: *Environmental laboratories and their EDD consumers*; *Calibration and metrology service providers* (as-found/as-left history across vendors); *Ready-mix concrete producer quality control departments*; *Asphalt plant producer QC technicians*; *Property tax consulting and assessment appeal firms* (assessment history across jurisdictions); *Premium audit and payroll classification consulting*.

**Pattern 5 — Identity normalization and manifest generation for binary artifact transfer (A7).**
Where the deliverable is a folder of binaries whose internal metadata is the only thing tying it to the job. Transfers to: *UAS/drone mapping and reality-capture service providers*; *BAS graphics and floor-plan production vendors*; *Print brokers, trade printers and prepress service bureaus*; *CMM programming and inspection-data management at small machine shops*.

**Pattern 6 — Loop-closure audit: reconcile what I sent out against what came back, and score the counterparty (A8).**
Transfers to: *Prime contractor supplier cyber-compliance desks (supplier attestation collection)*; *Construction submittal, RFI and closeout coordination*; *Approved supplier list and supplier qualification administration*; *Special process source approval administration at primes*; *Mortgage post-closing QC and trailing document vendors*; *Multi-state charitable solicitation registration compliance*. The counterparty scorecard — turning your own tracking data into leverage in the next negotiation — is the part that usually goes unbuilt.

---

## 8. Sources and confidence

### Verified findings (primary, peer-reviewed, or first-party with stated methodology)

| Finding | Source |
|---|---|
| Discharge statement to rDVM: mean 9 days, median 2, range 0–365. Discharge-timeliness satisfaction 68.33 vs 88.40 for care quality. Poor communication is the #3 rDVM barrier (15.5%). n=187 rDVMs + 92 specialists. **Equine population.** | [JVIM — Survey of Equine Referring Veterinarians' Satisfaction](https://academic.oup.com/jvim/article/32/2/822/8449637) |
| 85% of practices say their software does not integrate well with their PIMS; 82% struggling to hire; up to 2,000 hours/year of recoverable time. n=786. | [IDEXX productivity study press release](https://www.prnewswire.com/news-releases/groundbreaking-idexx-study-reveals-opportunities-to-increase-veterinary-practice-productivity-301750165.html) |
| 2025 AAHA Referral Guidelines: three collaboration models; document completed/pending tests to prevent duplication; designate a single referral coordinator; web-based portals recommended; client perceptions 6× more likely to improve when rDVM stays engaged. | [AAHA](https://www.aaha.org/resources/2025-aaha-referral-guidelines/) · [dvm360](https://www.dvm360.com/view/aaha-releases-2025-guidelines-for-effective-veterinary-specialist-referrals) |
| Imaging report minimum header requirements incl. clinical history and specific clinical queries; radiologist may decline service when pertinent info is missing. | [ACVR/ECVDI consensus statement, PMC11649853](https://pmc.ncbi.nlm.nih.gov/articles/PMC11649853/) |
| 20,636 active US board-certified veterinary diplomates as of 2025-12-31; ACVIM 4,537; ACVS 2,588. | [AVMA](https://www.avma.org/resources-tools/reports-statistics/veterinary-specialists) |
| ~1,600 US ER/specialty/urgent care hospitals; 131,200 professionals; avg 82 employees; 78% report staffing shortages; 79.3% technician turnover; 71% on cloud PIMS/EMR. | [Instinct, State of ER & Specialty Veterinary Care 2024](https://info.instinct.vet/state-of-er-specialty-veterinary-care-2024) |
| 7.6M North American pets insured end-2025; $6.2B GWP; +8.5% pets, +19.4% premium; ~4.3% penetration. | [NAPHIA](https://naphia.org/industry-data/) · [Insurance Business](https://www.insurancebusinessmag.com/us/news/breaking-news/naphia-only-4-27-of-us-pets-insured-despite-decade-of-doubledigit-growth-580314.aspx) |
| PIMS share: AVImark 25.4%, Cornerstone 19.5%, ezyVet 16.5%, others 38.6%; ~15 platforms + 140 point solutions; vet PIMS market $200–400M/yr vs $10–13B human EHR. | [Prior Knowledge & Practice](https://priorknowledgeandpractice.substack.com/p/the-pims-integration-problem-is-real) |
| Free-text extraction: diagnosis search sensitivity 33–98%; accuracy as low as 60% on hard tasks; specific shorthand/hedging failure modes. | [Tandem Health](https://tandemhealth.ai/resources/knowledge/why-veterinary-free-text-notes-break-automated-coding) |
| HIPAA generally does not apply to veterinary records; state practice acts govern content, retention, release and confidentiality. Retention: CA 3y, TX 5y, NY 3y, FL 3y; AVMA recommends ≥5y. | [AccountableHQ](https://www.accountablehq.com/post/veterinary-clinic-hipaa-requirements-what-applies-and-what-doesn-t) · [co.vet records laws](https://co.vet/post/veterinary-medical-records-laws/) |
| rVetLink: specialty hospital pays setup + monthly, rDVMs free; integrates ezyVet, Cornerstone, DVMAX, ImproMed Infinity. | [IDEXX](https://software.idexx.com/products/rvetlink) |
| Per-service referral requirement variation; DICOM accepted; rVetLink used for discharge/report return. | [UF Small Animal Hospital](https://smallanimal.vethospital.ufl.edu/contact-us/referring-veterinarians/) |
| Separate `referrals@` and `records@` intake addresses; 40 MB per-file portal cap. | [Integrity Veterinary Center](https://integrityvetcenter.com/for-veterinarians/how-referrals-work/) |
| What insurers require: full SOAP notes not after-visit summaries; numerical lab values with reference ranges; unambiguous pet/owner ID; email or fax with policy number. | [Lemonade](https://www.lemonade.com/pet/explained/pet-insurance-optimized-medical-records/) |
| Teleradiology SLA norms: 2–4h routine / 1–2h urgent radiographs; 4–8h routine CT. | [Asteris](https://www.asteris.com/blog/blog-veterinary-teleradiology-turnaround-time-sla/) |
| VetXML/VetEnvoy exists as a UK-centric standard; VeNom coding exists with inconsistent adoption; OpenVPM is an AGPLv3 open PIMS motivated by data lock-in. | [VetXML](http://www.vetxml.co.uk/en/about-the-consortium/) · [VeNom](http://venomcoding.org/) · [OpenVPM](https://openvpm.com/) |

### Strong inferences (consistent across independent practitioner-facing sources, not formally measured)

- **Records routinely do not arrive before the specialist appointment**, and fax remains a primary channel with well-described failure modes (after-hours, forgotten sends, illegibility). Asserted independently by [VitusVet](https://vitusvet.com/blog/five-reasons-the-veterinary-referral-process-is-broken/), [PetVet Magazine](https://digital.petvetmagazine.com/issue/february-march-2023/5-ways-to-streamline-referrals-for-successful-collaborative-care/) and [PupPilot](https://www.puppilot.co/blog/from-chaos-to-continuity-automating-health-record-transfers-between-clinics). All three are vendor-adjacent, which is why this sits here and not above — but the AAHA guidelines exist because the problem is real.
- **"Lack of complete, legible records" is specialists' most common frustration** (PetVet Magazine, summarizing specialists and ER doctors — no n given).
- **The return leg frequently fails entirely** — "do you get the specialist's SOAP notes back? Often not, or only after repeated calls" (PupPilot). Consistent with the JVIM 0–365 day range.
- **Records handling is an unnamed-software job.** The Thrive referral coordinator posting lists gathering and maintaining patient information as a core duty and names no system for it.
- **Prescription administration is a large, quantified adjacent burden** — 400–600 staff hours/year per practice, per an FDB white paper cited by [AAHA Trends](https://www.aaha.org/trends-magazine/publications/reclaiming-lost-hours-how-digital-prescription-management-is-reshaping-veterinary-workflows/). Vendor-sponsored, and adjacent rather than central to this angle, but it establishes that the sector quantifies and publishes this kind of burden.

### Tentative hypotheses requiring practitioner validation

- **Insurance claim economics** — 35–45% of claims needing manual review, $40–60 vs $25–36 per claim, 15–30 vs 3–7 days, 12–18% vs 2–5% error, 60–70% OCR on scans. All from [Insurnest](https://insurnest.com/blog/veterinary-invoice-standardization-pet-insurance-claims/), a vendor blog with no stated methodology. **Directionally useful, not quotable.** Verify with a claims adjudicator before using in any pitch.
- **Transcription error rates** — 5–15% general, "73% discrepancy in manually entered lab results" ([PupPilot](https://www.puppilot.co/blog/veterinary-data-interoperability-the-complete-guide-to-connecting-pims-labs-insurers)). The 73% figure cites an unnamed study and should be treated as unverified.
- **Duplicate data entry at 15–30 min/visit and 1.8 h/employee/day lost to scattered communication** ([Digitail](https://digitail.com/blog/5-hidden-time-drains-stealing-hours-from-your-vet-team/)) — vendor content marketing. Plausible, unverified.
- **Veterinary DICOM tag hygiene is poor.** Inferred from the existence of the veterinary PACS product category and from human-radiology experience. **No veterinary-specific evidence found.** This is the sole basis for A7 and must be validated by inspecting real studies before any build.
- **The 9-day discharge delay generalizes to small animal practice.** The measured population is equine.
- **Practices will pay for records assembly tooling.** Untested. The single most important commercial assumption in this report.

### Sources that could not be retrieved

Reddit (r/Veterinary, r/VetTech) was blocked to automated fetch, and VIN News returned a request-blocked page. Both are the richest sources of unfiltered practitioner complaint in this market, and their absence is the main gap in this cycle's evidence base. A follow-up cycle with manual access to VIN message boards would materially strengthen — or usefully undermine — the severity rankings in §3.

---

*Report generated 2026-08-08 · claim `0f90c511` · Borg LLC market research catalog*
