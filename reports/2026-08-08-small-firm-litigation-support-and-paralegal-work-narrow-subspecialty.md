# Market Research Cycle — Small-Firm Litigation Support & Paralegal Work

## Narrow subspecialty: plaintiff-side personal injury medical records, chronology, and demand-package production at 2–20 attorney firms

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market claimed** | Small-firm litigation support and paralegal work |
| **Angle claimed** | narrow-subspecialty |
| **Named subspecialty** | Plaintiff-side personal injury (PI) pre-litigation records work: retrieval, organization, medical chronology, bill reconciliation, and demand-package assembly at firms of 2–20 attorneys |
| **Claim ID** | `e6d5d6aa` |
| **Date** | 2026-08-08 |
| **Report** | `reports/2026-08-08-small-firm-litigation-support-and-paralegal-work-narrow-subspecialty.md` |
| **Backlog remaining after this claim** | 328 assignments across 190 untouched markets |

### Why this assignment over the others available

The ledger held 329 open assignments spanning 190 markets with zero completed coverage, so market **breadth** was the governing criterion. Within the untouched set I applied the three tie-breakers in order:

1. **Untouched market.** "Small-firm litigation support and paralegal work" had no completed entries in any angle. Three legal-adjacent markets are already in the catalog (immigration practice, estate planning/probate, title & escrow), but none of them touch litigation support, and none of them touch the plaintiff PI economy, which is a structurally different business (contingency fee, volume caseload, non-billable back office).
2. **Expected strength of practitioner evidence.** This subspecialty is unusually well documented in public sources: state bar and trial-lawyer association magazines publish operational how-to articles, paralegal training organizations publish step-by-step method pieces, several plaintiff firms publish their own cost-reduction playbooks with actual invoice numbers, live job postings enumerate the exact task list, and a well-funded vendor category (EvenUp, Supio, Filevine, CASEpeer) publishes benchmark data while attacking each other's accuracy. There is also *peer-reviewed* literature on the two technical failure modes that matter — duplicate text in medical records and LLM hallucination/omission rates on clinical summarization.
3. **Angle diversity.** `narrow-subspecialty` was the least-covered angle in the ledger (5 of 25 completed reports versus 8 for core-practitioner-workflow). Claiming it here rebalances the catalog.

One caveat about the choice: this market is *crowded* with venture-funded AI vendors. That is normally a reason to avoid a market. It is a reason to enter this one carefully rather than avoid it, because the crowding is concentrated at a price point — $150–$400 per user per month, or $300–$800 per demand — that the target firm segment demonstrably cannot absorb. Clio's 2025 solo-and-small-firm data shows the average small firm spends **2% of total expenses on software** and only **4% of small firms have adopted AI widely**, against **67%** who have touched it. The gap between "tried it" and "adopted it" is the opportunity, and most of the unmet need in that gap is not AI at all — it is deterministic document plumbing that the AI vendors skipped past on their way to the demand letter.

---

## 1. Market examined

**Industry.** Plaintiff-side personal injury law — auto/trucking collision, premises liability, dog bite, and soft-tissue-to-catastrophic bodily injury claims. Excludes defense-side work (different regulatory posture — see §4 privacy notes) and excludes medical malpractice, which has a distinct expert-review workflow.

**Organization size.** The target is the 2–20 attorney contingency firm. NALA's 2024 National Utilization and Compensation Report puts roughly **one third of all paralegals** working with 2–5 attorneys, so this is not a fringe segment; it is the modal paralegal employment context. Below two attorneys, the solo does the work personally and buys nothing. Above roughly 25 attorneys, firms start hiring dedicated records departments and can amortize a Filevine or Litify implementation, plus an EvenUp or Supio subscription.

**Professional roles that would be the user.**

- **Pre-litigation case manager** (sometimes titled "PI case manager") — owns the case from signup to demand. Live 2026 postings in the Los Angeles and Houston markets show $21–$50/hour, with bilingual Spanish frequently required and CASEpeer proficiency named explicitly.
- **Personal injury paralegal** — $32–$55/hour in the LA market; adds discovery, subpoenas, deposition notices, calendar/deadline control, and trial exhibit assembly on top of the records work.
- **"Demand writer"** — a job title that now exists as a standalone role. Two Los Angeles-area postings advertise $28–$40/hour and $30–$60/hour for someone whose entire job is to "own the demand writing process end-to-end" and "analyze and synthesize medical records." The emergence of this as a separable, hireable role is the strongest single market signal in this report: the work has been decomposed far enough to be staffed independently, which means it is decomposed far enough to be tooled independently.
- **Legal nurse consultant (LNC)** — hired per-case at $150–$175/hour for review and analysis, $250–$400/hour as a testifying expert. The LNC is a *substitute* for tooling at the high end and a potential *user* of tooling at the low end.
- **Attorney/owner** — the buyer. Sees the workflow only as elapsed time between last treatment and demand sent, and as write-offs on records invoices.

**Economic shape of the buyer.** Contingency revenue, so every hour spent on records is pure overhead that does not bill. Staff salaries are about **30% of small-firm expenses**. Firm software spend is about **2% of expenses**. Startup and running overhead guidance from within the industry puts legal software at $500–$2,000/month for the whole firm. A tool priced per-seat at $150–$400/month is therefore not a small purchase for a five-person firm — it is a material fraction of the entire software line.

---

## 2. How the work is performed

The pre-litigation arc runs: **signup → treatment monitoring → records and bills retrieval → organization and Bates → chronology → bill reconciliation → demand package → adjuster negotiation → lien resolution → disbursement.** The records subspecialty owns the middle six steps.

### 2.1 Retrieval

After signup the case manager builds a provider list from the client interview, then generates a request per provider. The request path forks three ways:

- **HIPAA authorization** on the firm's form or, very often, on *the provider's own mandatory form*, which the firm must locate and use. Records then go to a release-of-information (ROI) intermediary — Datavant (formerly Ciox), Sharecare, MRO, Verisma/ScanSTAT, MediCopy, ChartSwap, HealthMark/RRS — each with its own portal and login.
- **Patient-directed request under 45 CFR §164.524**, signed by the client, in which the client exercises their own right of access and directs the copy to the firm. This is the fee-reduction path (§2.2).
- **Subpoena / records deposition** when the provider will not respond to authorization. In California this triggers the Code of Civil Procedure §1985.3 Notice-to-Consumer machinery — 5 days' notice before personal service, 10 if mailed, 15-day consumer objection window, production typically 15–20 days after service — and adds "up to a month or so" per a practitioner account.

Follow-up runs on a manual **10–14 day cycle** against HIPAA's 30-day response clock plus one permitted 30-day extension. A widely used internal rule is to flag a request as stalled at **30 days**. Every one of these follow-ups is a phone call, a portal login, or a re-faxed letter, tracked in whatever the firm has: a spreadsheet, a case-management module, or Outlook tasks.

### 2.2 The fee fight embedded in retrieval

Three plaintiff firms have published their own cost data on the difference between the authorization path and the patient-directed path:

- **Locke Law Firm (Atlanta)** publishes a side-by-side: the same records invoiced at **$143.12** under a HIPAA authorization and **$7.08** under a HITECH/right-of-access request. Their internal control is that charges under $20 are auto-approved and anything above needs prior approval.
- **Fell Law (San Diego)** reports moving from "**$1.50 per page**, hundreds or thousands more" to "**won't pay more than about $10**," and maintains a **template letter for disputing excessive invoices**.
- **Wetherington Law Firm (Atlanta)** instructs that the letter be signed by the client, kept short, and sent **without firm letterhead**, because providers "can deny requests if they suspect it came from an attorney's office."

The legal terrain underneath this is genuinely messy, which is precisely why it is a software problem. *Ciox Health v. Azar* (D.D.C. 2020) vacated HHS's 2016 patient-rate fee guidance and vacated the 2013 expansion of the third-party directive beyond electronic records held in an EHR. The **right** to direct a copy to a third party survives in the regulation text; the **fee cap** on that directive did not. HHS's post-ruling position is that cost-based fee limits apply to an individual's request for their own records but not to a request to transmit to a third party. The practical consequence is the "records go to the client's address, client forwards to firm" workaround, and a live dispute over what ROI vendors may charge. That dispute has teeth: OCR's Right of Access Initiative has produced **54 financial penalties**, most recently **Concentra at $112,500** (May 2025) for a 13-month delay on a request where the invoice started at $82.57 and was "later adjusted to $6.50"; *Justis v. CIOX Health* (W.D. Va.) challenged a $2.00 "electronic fee" against Virginia's statutory schedule; a Texas class action against Ciox settled for **$1.85M** over charges such as $77.50 where $25 was lawful.

State fee schedules that a firm must apply, per state, per request type, include (verify each before relying on it — several are indexed annually):

| State | Rate |
|---|---|
| California — patient request | $0.25/page (H&S §123110) |
| California — subpoena | $0.10/page; clerical max $24/hr computed at $6 per quarter hour; $15 max on-site delivery (Evid. Code §1563(b)) |
| New York | $0.75/page + postage; access cannot be denied for inability to pay (PHL §18) |
| Texas — physician office | $25 first 20 pages + $0.50/page; $25 electronic ≤500 pages, $50 >500 (22 TAC §165.2) |
| Virginia | Paper $0.50/$0.25; electronic $0.37/$0.18; $20 search cap; **$160 total cap** (§8.01-413) |
| Oregon | $30.00 flat pages 1–10, then $0.50/page (ORS §192.563) |
| Massachusetts | $0.96/page (1–100) + $28.69 search (243 CMR 2.07(13)) |
| Alaska, Arizona, Iowa, Kansas, Wyoming | No statutory cap — "reasonable fee" only |

No small firm's case manager holds this in their head. Most simply pay the invoice.

### 2.3 What actually arrives

Records arrive as PDFs — frequently **one undifferentiated 400–1,200 page file per provider**, sometimes per *system* rather than per encounter. Documented characteristics:

- Clinical notes, itemized bills, EOBs, insurance adjustments, intake forms, and duplicate pages interleaved in the same PDF.
- Fax cover sheets, blank pages, and unrelated documents mixed in.
- "The same ER report may appear several times."
- Imaging **reports** without the **images**; labs in a separate system; **operative reports omitted while pre-op and post-op notes are present**; anesthesia and pathology missing.
- Pages "without dates, encounter IDs, or legible pagination."
- Mixed typed, handwritten, and multiply-faxed content in a single file.

Two hard data points bracket the scale of the noise. The peer-reviewed figure: Steinkamp et al., *JAMA Network Open* 2022, analyzed **104.5 million notes across 1.96 million patients** and found **50.1% of all text in the record was duplicated from prior text**, rising to 54.2% for notes written in 2020. (Important precision: that is duplicated *text within EHR notes*, not duplicated *pages in a litigation production*. The two are related but not the same metric and should not be conflated.) The operational figure: OCR accuracy on handwriting runs roughly 50–70% with traditional engines and 82–95% with modern AI systems, against 98–99% on clean printed text — meaning the exact pages most likely to contain the treating physician's real impressions are the pages the software reads worst.

### 2.4 Organization, Bates, chronology

The paralegal splits the blob by provider and by encounter, puts it in date order, and Bates numbers it — overwhelmingly using Adobe Acrobat Pro's built-in Bates tool, with prefixes like `Plaintiff-001` or client-initials-plus-practice-initials. Adobe community threads show ongoing confusion about continuous versus per-exhibit numbering, which tells you this is being done by hand, per case, by someone without a repeatable macro.

The chronology itself is, per the dominant training sources, **a spreadsheet**. The canonical column set is *Date of service | Provider | Facility | Description of visit / findings | Charges | Bates or PDF page*. The demand-side variant collapses to four columns: date, provider, description, charge. The editorial rule practitioners are taught is a signal-to-noise rule: "The fact that the plaintiff has two legs does not belong on the medical summary, nor does the fact that he has full cervical range of motion if he is complaining of lower back pain." Reviewers are told to go to the **Findings** section of diagnostic reports and to mine **pharmacy records and health-insurance claims history** for prior conditions before the defense finds them.

Throughput figures found in public sources — all vendor-published, none independently surveyed, so treat as an order of magnitude rather than a benchmark:

| Task | Reported rate | Source type |
|---|---|---|
| Review of clear/typed records | ~50 pages/hour | vendor |
| Review of handwritten/complex records | ~20 pages/hour | vendor |
| Deposition transcript summarizing | 20–25 pages/hour | trainer + vendor, two independent |
| 600-page case → comprehensive chronology | 4–8 hours | vendor |
| Average chronology | 8–10 hours, 20+ for complex | vendor, **unattributed** |
| Full timeline + specials + demand prep, one named firm | 80+ hours per case | vendor case study, single firm |

The most useful practitioner quote in the entire corpus comes from a senior paralegal and pre-litigation manager at a Northern California plaintiff firm, describing why the chronology is worse than it looks: *"Before Supio, we entered all medical treatment on a timeline manually. It was all entered again once we submitted the demand. That's twice we're doing the same work. Probably two full-time jobs just to enter medical records."* The chronology is not one data-entry pass. It is two or three, into different documents, with no shared source of truth.

### 2.5 Bills and specials

Separately from the clinical review, someone reconciles **billing records against clinical records**: confirming that billed dates of service correspond to documented encounters, that CPT codes correspond to services described in the notes, and that ICD codes correspond to documented diagnoses. Failure modes named in practice literature: charges with no clinical support, documented treatment with no corresponding bill, providers who send a **one-page summary statement instead of an itemized bill**, and chronologies "prepared without CPT/ICD code support." The document types in play are itemized statements, summary statements, EOBs, letter-of-protection (LOP) billing, and Medicare/Medicaid payment documentation.

The output is the **facility billing table** that goes in the demand — total charges by facility — plus itemized out-of-pocket costs including mileage at the IRS rate for the year in question.

### 2.6 The demand package

The demand is the deliverable the whole subspecialty exists to produce. The best practitioner articulation, from a California trial-lawyer association magazine, lists seven required elements: liability, economic damages, non-economic damages, an appropriate monetary demand, reasonable conditions, a reasonable deadline, and treatment of additional exposures. Operational details that matter for tooling:

- Liability is usually proved by attaching the **traffic collision report** (or animal control report for dog bites).
- Wage loss needs employer documentation of duties, time missed, and rate of pay, **plus** the physician's off-work note.
- Non-economic damages are built from **subjective complaints recorded in the treatment notes** and from the **count and duration of appointments** — i.e., directly out of the chronology.
- Conditions typically demand the declarations page for every policy tendered and a sworn declaration identifying all insurance.
- A consortium claim that goes unaddressed "can render the demand defective and make the insurance company 'unable to accept or reject.'"

In time-limited/policy-limits demand states the statute controls form. Georgia's O.C.G.A. §9-11-67.1 requires five material terms — a period **not less than 30 days from receipt**, the amount, the parties to be released, the type of release, and the claims to be released — sent by certified mail or statutory overnight delivery, and it must **specifically reference the code section**. Getting any of that wrong forfeits the bad-faith setup. This is a checklist a piece of software can enforce and a human under deadline reliably cannot.

Elapsed time to produce a demand, per three attorneys answering publicly: "two to four weeks once all necessary documents and medical records are in hand," "days, weeks or months." An industry data point from EvenUp's own case corpus: **42% of demands are sent more than 100 days after last treatment.**

### 2.7 Liens and disbursement

After the demand comes lien resolution, which is a deadline-driven compliance exercise the same person usually owns. The lien universe includes Medicare (MSP conditional payments), Medicaid, ERISA plans, VA, workers' compensation, hospital liens under state hospital lien acts, and letters of protection. Perfection matters — California practice literature directs counsel to verify "whether the hospital has perfected its lien claim by giving the notice required by statute to the tortfeasor's insurance carrier (Civ. Code §3045.3)."

The Medicare conditional-payment track alone is a dense clock: conditional payment letter roughly 65 days after reporting; the Final Conditional Payment Process opens within 120 days before expected settlement; disputes resolved within 11 business days; final amount locked within exactly 3 business days of settlement; settlement reported within 30 days; **payment due within 60 days of the demand date with interest accruing on day 61**; first-level appeal within 120 days. Missing any of these costs real money out of the client's net and, at the far end, out of the firm's.

### 2.8 Software actually in use

| Layer | Products | Verified price |
|---|---|---|
| PI case management | CASEpeer | **$79 / $119 / $149** per user/month; medical treatment tracking in Basic, "Medical Requests Report" only in Pro+ |
| | Neos (Assembly/Needles) | **$109**/user/month annual, **3-user minimum** |
| | Filevine, Litify, SmartAdvocate | No public pricing; third-party estimate ~$87/user/month for Filevine, moving to per-case AI charges |
| Retrieval service | ChartRequest Active Retrieval | **$25/request** |
| | Record Retrieval Solutions | **$45 flat/request**, and **two departments at one hospital = two fees** |
| | ChartSquad, Ontellus, Keais | Quote-gated |
| Outsourced human review | LezDo TechMed | 0–100 pp **$100 flat**; 101–500 pp **$0.75/page**; 501–1,000 **$0.40**; >2,000 **$0.20**; deposition summary **$1.00–$1.50/page**; expedited +20% |
| | RRR Health Tech (offshore) | **$25/hour** for chronology, narrative summary, demand letter, deposition and billing summaries |
| | Legal nurse consultant | **$150–$175/hour** review; $250–$400 testifying |
| AI demand/chronology | CaseMark | **$100/user/month** including $80 AI credits — *published* |
| | Casefleet | $30–$140/user/month; OCR overage **$1 per 100 pages** past 3,000/user/month |
| | Precedent | **$275 per demand maximum**, unlimited revisions |
| | EvenUp | Case-based pricing, **no public figure**; a competitor alleges $300 base rising past $800 |
| | Supio, Eve | **No public pricing**; third-party estimates $150–$400/user/month |
| Bates / PDF | Adobe Acrobat Pro | Universal default |

Market structure is consolidating around the buyer's throat: **Datavant acquired Ontellus** (closed August 2025) to build a legal/claims retrieval vertical, then **agreed to acquire DigitalOwl** (October 2025) to add AI summarization on top of retrieval. Datavant's own press release concedes the state of the market: *"The record retrieval process remains highly fragmented, with inconsistent workflows, procedures, and data formats across thousands of organizations."* Meanwhile EvenUp raised **$150M at a $2B+ valuation** and in May 2026 launched a staffed "Pre-Litigation-as-a-Service" offering — which is to say the best-funded software vendor in the category concluded that the problem is currently solved by *labor*, not software.

---

## 3. Most important problems, ranked

### P1. Records arrive as an undifferentiated PDF blob and someone must split, order, deduplicate, and Bates it by hand

**Who.** Case manager or PI paralegal, on every case, for every provider.
**When.** Immediately on receipt, before any substantive review can begin.
**Currently handled by.** Manual page-by-page scrolling in Acrobat, manual page extraction into per-provider files, manual date sorting, Acrobat's Bates tool, and a hand-typed index. At firms that can afford it, the entire package is shipped to an offshore LPO at $0.20–$0.75 per page for "PDF sorting and indexing" — one published rate card charges **$0.07–$0.10/page for sorting and indexing alone**, on top of review.
**Why inadequate.** It is pure transcription with no professional judgment in it, it scales linearly with page count, and it is the step where the reviewable page count is set. Every duplicate page that survives this step is a page someone reads and, at outsourced firms, a page someone *bills for*. The failure is also silent: the practitioner literature's canonical horror story is that "the demand may be almost ready when someone realizes that the MRI report is missing."
**Frequency.** Every case, multiple times per case (records arrive in waves as treatment continues).
**Cost.** At 400–1,200 pages per provider set and vendor-reported review rates of 20–50 pages/hour, organizing and reading a mid-sized case is 10–40 hours of $25–$40/hour loaded staff time, before any chronology is written. If 30–50% of pages are redundant — plausible given the JAMA duplicate-text finding and the practitioner accounts, though not directly measured for productions — a meaningful fraction of that is spent twice.
**Evidence quality.** Strong. Multiple independent practitioner and vendor descriptions of the same failure modes; a published rate card that prices sorting/indexing as a discrete line item, which only happens when it is a discrete, painful task.

### P2. Firms overpay for records because nobody applies the right fee rule at the right moment

**Who.** The firm's owner (it hits the case expense ledger) via the case manager who approves invoices.
**When.** Once per provider per request — dozens of times per case.
**Currently handled by.** Paying the invoice. Sophisticated firms have built a manual playbook — client-signed patient-directed letter, no firm letterhead, template dispute letter for excessive invoices, dollar-threshold approval rules.
**Why inadequate.** The correct fee depends on the *request type* (patient-directed vs. authorization vs. subpoena), the *state*, the *provider type* (hospital vs. physician office in Texas), the *format* (paper vs. electronic vs. microfilm), and the post-*Ciox* federal overlay. Nobody carries that matrix. The three firms that publish their results found order-of-magnitude overcharges.
**Frequency.** Every request.
**Cost.** Directly measured by the firms themselves: **$143.12 → $7.08** on one invoice; "$1.50/page and hundreds or thousands more" → "about $10." At even 8 providers per case and a mid-sized firm's caseload, this is five figures a year in recoverable case expense, plus the reduction improves the client's net and the firm's reputation for lien/expense discipline.
**Evidence quality.** Strong and unusually concrete — three separate firms published their own before/after numbers, and the regulatory backdrop (OCR's 54 penalties, the Ciox class settlement, the *Justis* complaint) is primary-source verifiable.

### P3. The chronology is entered two or three times into different documents with no shared source of truth

**Who.** Case manager, then demand writer, then whoever assembles litigation exhibits.
**When.** Every case that reaches demand.
**Currently handled by.** An Excel or Word table, re-keyed into the demand letter, sometimes re-keyed again into the case-management system's treatment tracker.
**Why inadequate.** Named directly by a practitioner: *"That's twice we're doing the same work. Probably two full-time jobs just to enter medical records."* Beyond the duplication, the re-keying breaks the Bates linkage — the demand cites facts that can no longer be traced back to a page, which is exactly what gets attacked in litigation.
**Frequency.** Every case.
**Cost.** Vendor-reported 8–10 hours per chronology (20+ complex), and the double-entry is a defined fraction of it. One firm's case study claims 80+ hours per case across timeline, specials, and demand prep.
**Evidence quality.** Moderate-to-strong. The double-entry complaint is a named practitioner at a named firm, but the surrounding hour figures are vendor-published and unattributed.

### P4. Nobody can prove the record set is complete until it is too late

**Who.** Case manager; the cost lands on the attorney at demand or, worse, at deposition.
**When.** Continuously, but discovered at demand assembly.
**Currently handled by.** Memory, a request-tracking spreadsheet, and a recommended "completeness review within 48 hours of receipt" that most firms do not staff.
**Why inadequate.** The universe of what *should* exist is not knowable from what *did* arrive. Imaging reports come without images; operative reports go missing while pre-op and post-op notes arrive; a hospital's radiology department is a separate request from its HIM department (and, at $45/request vendors, a separate fee). Referrals mentioned inside received records name providers nobody has requested from yet. Requests get "routed to wrong departments or external vendors without notification," and authorizations expire mid-chase.
**Frequency.** Every case; catastrophic on the minority of cases where a missing operative report or a missing prior-treatment record surfaces after the demand.
**Cost.** Elapsed-time cost is the visible one — one vendor's 500-firm internal survey claims an **average of 4 months** to assemble a complete set in-house, and 42% of demands go out more than 100 days after last treatment. The tail risk is a demand built on an incomplete record that the adjuster or defense counsel then punctures.
**Evidence quality.** Strong on the failure modes, weak on the quantification (the 4-month figure is an unpublished vendor survey and should be cited as such).

### P5. Treatment gaps and prior-condition exposure are found by the defense before they are found by the firm

**Who.** Attorney; discovered at negotiation or deposition.
**When.** Any case with a gap in care — which is most of them.
**Currently handled by.** The paralegal noticing while reading, plus a deliberate "prior medical history" section in the demand meant to preempt the argument.
**Why inadequate.** Gap detection is date arithmetic across a merged multi-provider timeline. A human reading provider-by-provider PDFs is structurally bad at it, because the gap only exists in the *merged* timeline.
**Frequency.** Per one vendor's corpus analysis: **16.8%** of plaintiffs open a 30-day gap within three months, **32.4%** by six months, and **43%** of cases eventually have a gap exceeding 30 days.
**Cost.** Direct valuation impact — treatment gaps are the standard adjuster discount lever, and the discount is applied to the whole claim.
**Evidence quality.** Moderate. The percentages are vendor-proprietary and unaudited, but the mechanism is uncontroversial and the fix is arithmetic, so the idea does not depend on those numbers being exactly right.

### P6. Bills and clinical records are reconciled by eye, or not at all

**Who.** Case manager or demand writer.
**When.** Demand assembly.
**Currently handled by.** Reading the bill next to the chronology.
**Why inadequate.** Providers send summary statements instead of itemized bills; charges appear without clinical support; documented treatment goes unbilled; CPT and ICD codes are missing from chronologies entirely. Coded specials — where the ICD establishes the injury and the CPT establishes the treatment for that injury — measurably harden a demand against "interpretation" by the adjuster.
**Frequency.** Every case.
**Cost.** Understated specials are permanently lost money; overstated specials get attacked and cost credibility on the whole demand.
**Evidence quality.** Moderate. Well described in vendor and LPO literature, no independent quantification.

### P7. AI-generated chronologies are cheap, fast, and unverifiable

**Who.** Any firm that has adopted an AI summarizer, or bought a vendor chronology.
**When.** Every AI-produced work product.
**Currently handled by.** Human spot-checking, or nothing.
**Why inadequate.** This is the best-documented problem in the report and the one with actual peer-reviewed numbers. *PLOS Digital Health*, on 100 emergency-department encounter summaries: GPT-4 produced hallucinations in **42%** of summaries, omitted clinically relevant information in **47%**, and was entirely error-free in only **33%**; the most common fabrications were invented follow-up arrangements. *npj Digital Medicine* (2025), on 450 transcript-note pairs and 12,999 clinician-annotated sentences: a 1.47% hallucination rate of which **44% were major**, and a 3.45% omission rate of which **16.7% were major**. Separately, a pilot in which LLM judges were used to catch hallucinations found they caught **2 of 9** expert-identified errors — i.e., AI does not reliably check AI. And *Business Insider* reported in November 2024 that former EvenUp employees said supervisors instructed them not to use the AI due to unreliability, and that it "missed injuries, fabricated medical conditions, and incorrectly recorded doctor visits."
**Frequency.** Every AI-produced chronology.
**Cost.** A fabricated treatment date in a demand is a credibility loss with the adjuster; the same fabrication surviving into a verified discovery response is a sanctions and malpractice exposure. The explainability problem is stated plainly in the trade press: "If an AI-generated medical chronology contains errors or omissions, attorneys may struggle to defend its accuracy."
**Evidence quality.** Strong — two peer-reviewed studies plus mainstream reporting.

### P8. Lien and Medicare deadlines are tracked in a spreadsheet

**Who.** Case manager / settlement coordinator.
**When.** Post-settlement, under time pressure, with client funds held.
**Currently handled by.** A spreadsheet and calendar reminders.
**Why inadequate.** The MSP clock has at least seven distinct deadlines with different triggers and units (65 days, 120 days, 11 business days, 3 business days, 30 days, 60 days, 120 days), and interest starts on day 61. State hospital-lien perfection has its own notice requirements that determine whether the lien is even enforceable.
**Frequency.** Every settled case.
**Cost.** Interest, unreduced liens, delayed client disbursement, and — where a lien was never perfected but got paid anyway — money handed over that was not owed.
**Evidence quality.** Moderate-to-strong on the rules (CMS primary sources exist), weak on prevalence of failure.

---

## 4. Application opportunities

Ten concepts. They are deliberately layered: several are the deterministic plumbing the AI vendors skipped, one is an explicit trust layer *on top of* AI output, and none of them is a case-management system.

A design constraint applies to all of them and is the single most important strategic point in this report: **a plaintiff firm that receives records under its own client's authorization is generally not a HIPAA business associate** — the client may give their own records to anyone. Defense counsel receiving PHI *from* a covered entity is a business associate; plaintiff intake is different. (A widely-read vendor guide asserts flatly that law firms "are considered business associates"; for plaintiff-side intake this is over-broad and should not be treated as authority.) The consequence for product design is decisive: **a local-first, offline desktop tool that never transmits PHI to a vendor server sidesteps the entire business-associate-agreement conversation**, which is the single biggest procurement obstacle a small firm faces when evaluating cloud AI tools. Every concept below assumes local-first unless noted.

---

### A1. Right-of-Access Request Kit

- **Working title.** RecordsRate — patient-directed request generator and fee-dispute engine.
- **Intended user.** Case manager at a 2–20 attorney plaintiff PI firm.
- **Problem solved.** P2. Firms pay authorization-path prices for records they could obtain at right-of-access prices, and pay invoices that exceed the applicable state or federal fee limit.
- **Current workflow.** Firm's standard HIPAA authorization goes to every provider; whatever invoice comes back gets paid.
- **Proposed workflow.** Enter client and provider details once. The tool emits, per provider: (a) a client-signed §164.524 patient-directed request letter in plain first-person language on plain paper, no firm letterhead; (b) the accompanying personal-representative authorization where needed; (c) a fallback traditional HIPAA authorization. It then computes the **maximum lawful charge** for that provider under the applicable state schedule and request type, and when an invoice arrives above that figure, generates a citation-bearing dispute letter and, optionally, a drafted OCR Right-of-Access complaint.
- **Inputs.** Client name/DOB/address, provider name/type/state, request format (paper/electronic), date range.
- **Outputs.** Print-ready letters (PDF/DOCX), an invoice-check verdict with the governing citation, a dispute letter, a per-case expense log.
- **Essential features.** Maintained state fee-schedule table as a plain versioned data file; request-type fork; letter templates; invoice checker; expense export.
- **Excluded from v1.** Sending anything (no fax/mail integration), storing records, portal automation, e-signature.
- **AI.** Inappropriate. This is a rules table and a mail merge. Adding a model would introduce error into the one thing that must be exactly right — the citation.
- **Would a spreadsheet suffice?** No. The fee logic is a multi-dimensional decision table plus document generation, and the value is in the *maintained* fee schedule, which no individual firm will keep current.
- **Complexity.** Small. **Learning difficulty:** minutes.
- **Value.** The published firm data implies $50–$135 saved per request; at 6–10 providers per case this is $300–$1,300 per case in reduced case expense, on top of the disputes never filed today.
- **Risks.** The fee-schedule table is a maintenance liability and a soft liability exposure if wrong — ship it with prominent "verify before relying" framing and per-entry citations and last-verified dates. Post-*Ciox* uncertainty on third-party-directed fees must be surfaced as uncertainty, not resolved silently. No PHI leaves the machine.
- **Substitutes.** Individual firm playbooks published as blog posts; retrieval vendors who profit from the status quo. None of them is a tool.
- **Why still attractive.** Nobody sells this because the entire vendor ecosystem's revenue depends on firms *not* doing it. That is the definition of a gap an open-source tool should fill.
- **Paid customization.** State-specific and firm-specific letter branding; integration of the firm's approval thresholds; a maintained-schedule subscription.

---

### A2. Production Splitter and Bates Indexer

- **Working title.** ChartSplit.
- **Intended user.** Case manager / paralegal.
- **Problem solved.** P1. The 900-page blob.
- **Current workflow.** Scroll, extract pages by hand in Acrobat, save per-provider files, sort by date, run Acrobat's Bates tool, hand-type an index.
- **Proposed workflow.** Drop the PDF in. The tool detects document boundaries using deterministic signals first — fax headers, page-of-N footers, form-type headers, repeated letterhead, blank-page separators, date-of-service patterns — proposes a segmentation with provider/facility/date/document-type labels, lets the user correct any boundary in a side-by-side view, then emits per-encounter PDFs, a continuously Bates-numbered master, and a CSV/XLSX index keyed to Bates ranges.
- **Inputs.** One or more PDFs; optional provider list from A5.
- **Outputs.** Segmented PDFs, Bates-stamped master, index CSV, unrecognized-pages report.
- **Essential features.** Boundary detection with confidence display; human correction UI; configurable Bates prefix/start/width; index export; **an explicit list of pages the tool could not classify** (never silently guess).
- **Excluded from v1.** Clinical content extraction, redaction, cloud sync, multi-user.
- **AI.** Optional, and only for *classification* of document type and provider on pages where deterministic rules fail — with the label always shown as a suggestion tied to a page the human can see. Never for boundaries alone.
- **Would a spreadsheet suffice?** No — this is PDF manipulation.
- **Complexity.** Medium. **Learning difficulty:** under an hour.
- **Value.** Displaces the LPO "PDF sorting and indexing" line item priced at $0.07–$0.10/page — $70–$100 per thousand pages — and several hours of in-house work per provider set.
- **Risks.** A missed boundary buries a document. Mitigate by making the unclassified report loud and by never deleting pages. PHI stays local.
- **Substitutes.** Acrobat (manual), Wisedocs/DigitalOwl (cloud, priced for insurers), LPO vendors.
- **Why still attractive.** The cloud products require a BAA conversation and a per-page fee; the incumbent free option is a human with a mouse.
- **Paid customization.** Provider-specific boundary rule packs for the hospital systems a given firm sees repeatedly — this gets better the more a firm uses it, which is a natural services hook.

---

### A3. Duplicate and Junk Page Suppressor

- **Working title.** PageDiet.
- **Intended user.** Whoever is about to read, or pay someone per page to read, a production.
- **Problem solved.** P1, specifically the redundant-page fraction.
- **Current workflow.** Read the same ER report four times.
- **Proposed workflow.** Hash every page two ways — normalized extracted text and a perceptual image hash for scanned pages — cluster near-identical pages, and produce (a) a reduced review set with one canonical instance per cluster and (b) a **suppression log** listing every removed page by Bates number and the page it duplicates. Also flags fax cover sheets, blank pages, and pure-boilerplate pages by pattern.
- **Inputs.** Bates-stamped PDF (ideally A2's output).
- **Outputs.** Reduced PDF, suppression log CSV, page-count-before/after summary.
- **Essential features.** Two-channel hashing; adjustable similarity threshold; the suppression log as a first-class deliverable, not a debug artifact; **nothing is ever deleted from the original**.
- **Excluded from v1.** Semantic near-duplicate detection, OCR improvement, content summarization.
- **AI.** Inappropriate. Hashing is exact, explainable, and defensible in a way that a model's "these look similar" is not.
- **Would a spreadsheet suffice?** No.
- **Complexity.** Small. **Learning difficulty:** minutes.
- **Value.** Directly reduces the billing unit for outsourced review ($0.20–$0.75/page) and the reading unit for in-house review (20–50 pages/hour). A 20% reduction on a 1,000-page case is 4–10 staff hours or $40–$150 of vendor cost, per case, on a tool that runs in seconds.
- **Risks.** Suppressing a page that differs in a legally material way — mitigated by the never-delete rule, the log, and a conservative default threshold. Two identical-looking pages with different Bates numbers may both need producing in discovery; the tool is a *review* aid, not a production tool, and should say so.
- **Substitutes.** None widely used at small firms. Some e-discovery platforms dedupe at the document level, but small PI firms do not own e-discovery platforms.
- **Why still attractive.** Trivially explainable ROI: "your 1,000-page case is now 780 pages, here is exactly what I removed and why."
- **Paid customization.** Firm-specific junk-page pattern libraries.

---

### A4. Chronology Workbench

- **Working title.** ChronoDesk.
- **Intended user.** Case manager, demand writer, LNC.
- **Problem solved.** P3 (double entry) and the traceability half of P7.
- **Current workflow.** Excel table typed while scrolling a PDF, then re-typed into the demand.
- **Proposed workflow.** A single local application with the PDF on one side and the chronology grid on the other. Every row is **anchored to a Bates page** — clicking a row jumps to the page. Controlled vocabularies for provider and facility prevent the "Dr. Smith / Smith, John MD / J. Smith DO" spread that makes later grouping impossible. From the same data the tool exports: the litigation chronology (full detail), the demand-letter treatment narrative (condensed, per the four-column convention), and the facility billing table — **one source, three documents, zero re-keying**.
- **Inputs.** Bates-stamped PDF + index from A2; optional bill data from A6.
- **Outputs.** Chronology XLSX, demand-ready DOCX tables, JSON/CSV for downstream tools.
- **Essential features.** Bates anchoring with click-through; controlled provider/facility lists; templated row types (office visit, imaging, PT, surgery, ER); export set; keyboard-first entry.
- **Excluded from v1.** Automatic extraction of clinical content, multi-user collaboration, cloud storage, case management.
- **AI.** Optional and strictly assistive: a "propose rows from this page" action that pre-fills date/provider/type and must be confirmed by a human, with the source page visible. Never a bulk unattended pass.
- **Would a spreadsheet suffice?** Partly — and this is the honest answer. A spreadsheet does the grid. What it cannot do is the Bates anchoring and click-through, or the three-way export from one source. The concept must beat Excel on exactly those two axes or it should not be built.
- **Complexity.** Medium. **Learning difficulty:** an hour, because it looks like a spreadsheet.
- **Value.** Eliminates one full re-keying pass on an 8–10 hour artifact; keeps every demand assertion traceable to a page.
- **Risks.** Scope creep toward case management. Hold the line: no calendar, no tasks, no contacts.
- **Substitutes.** Excel; Casefleet's chronology feature ($30–$140/user/month, cloud); CMS treatment trackers; AI summarizers.
- **Why still attractive.** The paid options are either cloud-only or bundled inside a system the firm has not bought. A free local tool that is *better than Excel at exactly two things* is an easy yes.
- **Paid customization.** Firm-specific export templates matched to the firm's demand format — this is the highest-value customization in the whole catalog, because every firm's demand looks different and nobody wants to reformat.

---

### A5. Provider Index and Completeness Gap Report

- **Working title.** GapCheck.
- **Intended user.** Case manager; reviewed by the attorney before demand.
- **Problem solved.** P4. You cannot audit for missing records against a list you never built.
- **Current workflow.** A request-tracking spreadsheet listing providers the client remembered.
- **Proposed workflow.** Build the expected-provider index from three sources rather than one: (1) client intake, (2) health-insurance claims history or EOBs where available, and (3) **referral and prior-treatment mentions extracted from records already received** — "patient was referred to Dr. X," "MRI performed at Y Imaging," "follow-up with orthopedics." Then diff expected against received, and apply a rules-based completeness checklist per encounter type: a surgery date with no operative report; an imaging report with no images; an ER visit with no facility bill; a hospital stay with no anesthesia or pathology; a provider whose records stop before the last known treatment date. Output a **gap report** with the specific next request to send.
- **Inputs.** Intake list; received records index (A2); optional EOB/claims data.
- **Outputs.** Provider index, gap report with recommended requests, request-status log with the 30/60-day HIPAA clock and a 10–14 day follow-up prompt.
- **Essential features.** Three-source index construction; encounter-type completeness rules; statutory clock tracking; **authorization expiry warnings**; department-level tracking (radiology vs. HIM are separate requests and separate fees).
- **Excluded from v1.** Sending requests, portal automation, provider contact directory.
- **AI.** Optional and well-justified for exactly one job — extracting referral and prior-provider mentions from free text. This is genuine unstructured-text extraction that rules do poorly. Every extraction must cite its Bates page and be human-confirmed before entering the index.
- **Would a spreadsheet suffice?** For the tracking column, yes. For mining referrals out of 900 pages of prose, no — and that is where the missing providers actually hide.
- **Complexity.** Medium. **Learning difficulty:** an hour.
- **Value.** Attacks the elapsed-time problem directly — the difference between discovering a missing operative report at week 3 versus at demand assembly.
- **Risks.** False confidence: a clean gap report is not proof of completeness. The UI must frame output as "requests you have not made" rather than "your file is complete."
- **Substitutes.** CASEpeer's "Medical Requests Report" (Pro tier and up); retrieval vendors' portals; nothing that reasons about what *should* exist.
- **Why still attractive.** Every existing tool tracks requests you made. None tells you about the request you did not know to make.
- **Paid customization.** Health-system-specific department maps for the hospitals a firm sees repeatedly.

---

### A6. Bill-to-Treatment Reconciler and Specials Builder

- **Working title.** SpecialsCheck.
- **Intended user.** Case manager / demand writer.
- **Problem solved.** P6.
- **Current workflow.** Eyeballing bills against the chronology; a hand-summed facility table.
- **Proposed workflow.** Ingest itemized bills (CSV where available, PDF table extraction otherwise), join to the chronology on date of service and provider, and produce an exception report: **billed dates with no clinical encounter**, **encounters with no bill**, **summary-only statements needing an itemized follow-up request**, missing CPT/ICD codes, duplicate charges, and adjustment/payment columns that change the lien math. Then generate the facility billing table and the itemized out-of-pocket schedule including mileage at the correct IRS rate for the year.
- **Inputs.** Bills, chronology (A4), IRS mileage rate table.
- **Outputs.** Exception report, facility billing table (DOCX/XLSX), out-of-pocket schedule, specials total with provenance.
- **Essential features.** Fuzzy date/provider matching with a human review queue; exception typology; IRS mileage table by year; totals that trace to source rows.
- **Excluded from v1.** Lien negotiation, payment tracking, reasonableness-of-charges analysis, insurance adjudication logic.
- **AI.** Optional for extracting line items from unstructured PDF bills. The reconciliation logic itself must be deterministic — a model that "thinks" two charges match is not something to put in a damages number.
- **Would a spreadsheet suffice?** A skilled paralegal with VLOOKUP gets most of the way. The tool wins on bill *extraction* and on the standard exception typology, not on the arithmetic.
- **Complexity.** Medium. **Learning difficulty:** an hour.
- **Value.** Understated specials are permanently lost money; a demand with charges the adjuster can puncture costs credibility on everything else in it.
- **Risks.** Wrong specials are worse than slow specials. Every total must show its constituent rows.
- **Substitutes.** EvenUp's Medical Bill Summary (bundled, priced per case); LPO billing summaries at $25/hour offshore.
- **Why still attractive.** The exception report — "here are 6 charges with no documented encounter and 2 encounters with no bill" — is a distinct deliverable nobody ships standalone.
- **Paid customization.** Firm-specific demand table formats; payer-specific EOB parsers.

---

### A7. Treatment Gap and Timeline Risk Flagger

- **Working title.** GapWatch.
- **Intended user.** Case manager, weekly; attorney, at case review.
- **Problem solved.** P5.
- **Current workflow.** Noticing.
- **Proposed workflow.** Against the merged multi-provider timeline, compute: latency from date of incident to first treatment, every inter-visit gap exceeding a configurable threshold (30 days default), current days since last treatment, and days since last treatment against the demand-readiness flag. Output a per-case risk line and a firm-wide list sorted by exposure, plus a drafted client-outreach note for gaps still open.
- **Inputs.** Chronology dates (A4) or a bare date/provider CSV. Nothing else.
- **Outputs.** Per-case gap memo for the file; firm-wide watchlist; client outreach draft.
- **Essential features.** Merged-timeline gap math; configurable thresholds; DOI-to-first-treatment latency; watchlist sort.
- **Excluded from v1.** Case valuation, settlement prediction, client messaging delivery.
- **AI.** Inappropriate. It is subtraction between dates. Any AI here is decoration.
- **Would a spreadsheet suffice?** Genuinely, almost — and this concept must be honest about that. It earns its place as a **free companion utility** that seeds adoption of the rest of the suite, not as a standalone product. It is a weekend build.
- **Complexity.** Small. **Learning difficulty:** minutes.
- **Value.** Gaps are the standard adjuster discount. Catching a gap while it is 25 days old and fixable is worth more than documenting it at 90 days. Vendor corpus data suggests 43% of cases develop a 30+ day gap.
- **Risks.** Encouraging treatment for litigation rather than medical reasons is an ethical line the tool must not cross — frame output as *documentation risk*, addressed to the firm, never as treatment advice or client-facing instruction.
- **Substitutes.** EvenUp's Medical Management tool (December 2025), bundled.
- **Why still attractive.** Cheapest possible thing to build, immediately understandable, and a natural front door to the suite.
- **Paid customization.** Minimal — this is a loss leader by design.

---

### A8. Demand Package Assembler and Statutory Checklist

- **Working title.** DemandBuild.
- **Intended user.** Demand writer / paralegal.
- **Problem solved.** The assembly tax on every demand, plus jurisdiction-specific statutory defects.
- **Current workflow.** Merge exhibits in Acrobat, hand-build a TOC and exhibit index, hope the Bates numbering still lines up, remember the statute.
- **Proposed workflow.** Take the letter body, the chronology, the billing table, and the exhibit set; produce a single paginated PDF with a generated exhibit index and table of contents, Bates numbering consistent with the underlying production, and a per-exhibit cover sheet. Before export, run a **jurisdiction checklist** from a versioned rules file — for a Georgia time-limited demand, verify the five §9-11-67.1 material terms are present, the acceptance period is at least 30 days from receipt, the code section is specifically referenced, and the delivery method is certified mail or statutory overnight. Generic checks include: is a consortium claim addressed or affirmatively waived; is a declarations-page condition stated; is every specials figure sourced.
- **Inputs.** Letter body DOCX, chronology, billing table, exhibit PDFs, jurisdiction selection.
- **Outputs.** Assembled demand PDF, exhibit index, checklist result with citations, transmittal cover.
- **Essential features.** Deterministic assembly; exhibit index generation; Bates consistency check across the package; checklist rules as human-readable YAML so firms and contributors can add jurisdictions.
- **Excluded from v1.** Writing the letter, valuing the claim, sending, e-signature, negotiation tracking.
- **AI.** Inappropriate for assembly and checklist. Arguably useful for a first draft of the narrative — but the market is saturated there, the accuracy record is poor (P7), and the assembly problem is the unserved one.
- **Would a spreadsheet suffice?** No.
- **Complexity.** Medium. **Learning difficulty:** an hour.
- **Value.** Compresses a recurring half-day assembly task; the checklist catches a class of defect that voids the bad-faith setup and is currently caught only by an experienced attorney's memory.
- **Risks.** A checklist that is wrong or stale about a statute is worse than no checklist. Version and date every rule, cite the statute inline, and label output as a drafting aid, not legal advice. Unauthorized-practice-of-law framing matters: the tool checks form, it does not advise.
- **Substitutes.** CMS demand templates (CASEpeer's automated demand templates); AI demand vendors at $275–$800 per demand.
- **Why still attractive.** The paid vendors sell the *writing*. Nobody sells the *assembly and statutory conformance*, which is the part that is mechanical and the part that voids a demand when missed.
- **Paid customization.** Jurisdiction rule packs; firm-branded exhibit and cover formats.

---

### A9. Chronology Verification Pass (the trust layer)

- **Working title.** ChronoAudit.
- **Intended user.** The paralegal or attorney who received a chronology from an AI vendor, an offshore LPO, or a junior staffer.
- **Problem solved.** P7. Nobody can currently afford to check an AI or outsourced chronology, so nobody does.
- **Current workflow.** Spot-check a few rows, or trust it.
- **Proposed workflow.** Feed in the chronology (any table with a Bates or page citation column) and the source production. For each row, verify mechanically that the cited page **exists**, that the **date** on the row appears on that page, and that the **provider or facility** string appears on that page. Then check global properties: rows out of chronological order, dates outside the treatment window, dates before the date of incident, providers not present anywhere in the production, duplicate rows, and encounters present in the production but absent from the chronology (the omission failure, which is empirically more common than fabrication). Output a per-row verdict — verified / unverifiable / contradicted — and a coverage percentage.
- **Inputs.** Chronology table (CSV/XLSX/DOCX) + source PDF.
- **Outputs.** Annotated chronology with verdicts, exception list, coverage statistic, one-page QC summary suitable for the file.
- **Essential features.** Page-existence, date-presence, and entity-presence checks; date-order and window validation; omission detection against the production's own date index; a QC summary that documents the check was performed.
- **Excluded from v1.** Judging clinical accuracy or medical significance, rewriting rows, scoring vendors.
- **AI.** Inappropriate for the verification itself — the whole point is that the checker must be deterministic, because AI checking AI caught 2 of 9 known errors in the one pilot found. Fuzzy string matching, yes; a model, no.
- **Would a spreadsheet suffice?** No — it requires reading the source PDF.
- **Complexity.** Medium. **Learning difficulty:** under an hour.
- **Value.** Converts an unverifiable work product into a defensible one at near-zero marginal cost, and produces a QC artifact for the file. Against published error rates — 42% of GPT-4 clinical summaries containing a hallucination in one peer-reviewed study, 47% containing a material omission — even a check limited to dates, pages, and providers catches a large share of the failures that matter.
- **Risks.** Verifying that a date *appears on a page* is not verifying that the clinical characterization is correct. The tool must state its own scope plainly or it becomes false assurance — which would be worse than the problem.
- **Substitutes.** None found. This is the clearest white space in the report.
- **Why still attractive.** It is *complementary* to the funded vendors rather than competitive with them, which means it can be adopted by firms already paying for AI, and it turns their strongest objection into a workflow step.
- **Paid customization.** Vendor-specific chronology format adapters; firm QC report templates; a batch mode for firms auditing an outsourcing relationship.

---

### A10. Lien and Settlement Deadline Docket

- **Working title.** LienClock.
- **Intended user.** Case manager / settlement coordinator.
- **Problem solved.** P8.
- **Current workflow.** Spreadsheet plus calendar reminders.
- **Proposed workflow.** Register each lien by type (Medicare/MSP, Medicaid, ERISA, VA, workers' comp, hospital lien, LOP, private health plan). The tool applies the deadline rules for that type from a versioned rules file and generates the dated task list — for MSP: conditional payment letter expectation, the 120-day Final Conditional Payment window, the 11-business-day dispute resolution, the 3-business-day final lock, the 30-day settlement report, the **60-day payment deadline with day-61 interest**, and the 120-day appeal window. For hospital liens, a state-specific **perfection checklist** (was statutory notice given to the tortfeasor's carrier?). Ends in a disbursement worksheet that ties gross settlement, fees, costs, each lien at claimed and negotiated amounts, and client net.
- **Inputs.** Settlement date and amount, lien inventory, state.
- **Outputs.** Dated deadline docket (with ICS export), perfection checklist per lien, disbursement worksheet.
- **Essential features.** Lien-type rule packs; business-day vs. calendar-day arithmetic (these are mixed in the MSP rules and are a real source of error); perfection checklists; disbursement math.
- **Excluded from v1.** Trust accounting, payment execution, CMS portal integration, lien negotiation correspondence.
- **AI.** Inappropriate. Deadline arithmetic and statutory checklists.
- **Would a spreadsheet suffice?** The disbursement math, yes. The rule-driven deadline generation and the business-day arithmetic, no.
- **Complexity.** Medium. **Learning difficulty:** an hour.
- **Value.** Avoided interest, avoided unreduced liens, faster client disbursement, and — via the perfection checklist — occasionally the discovery that a lien being paid was never enforceable.
- **Risks.** Highest regulatory sensitivity in the set. Rules change; CMS process changes. Version and date everything, cite CMS primary sources inline, and label as a docketing aid. Do **not** touch trust accounting — that is a bar-compliance minefield and a different product.
- **Substitutes.** Lien resolution services (per-case fee); CMS portals; CMS-adjacent vendor tooling.
- **Why still attractive.** Lien services are priced for catastrophic cases. The soft-tissue case with a $4,200 hospital lien gets a spreadsheet.
- **Paid customization.** State hospital-lien rule packs; firm disbursement statement formats.

---

## 5. Opportunity ranking

Scored 1–5 on ten criteria; maximum 50.

**Criteria key:** SEV = severity of problem · FREQ = frequency of use · ROI = clarity of ROI · LEARN = ease of learning · IMPL = ease of implementation · SCOPE = ability to stay narrowly scoped · DIFF = market differentiation · CUST = customization potential · DATA = availability of realistic test data · CONF = confidence in evidence.

| # | Concept | SEV | FREQ | ROI | LEARN | IMPL | SCOPE | DIFF | CUST | DATA | CONF | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| A1 | RecordsRate — right-of-access request & fee dispute | 5 | 5 | 5 | 5 | 5 | 5 | 5 | 4 | 5 | 5 | **49** |
| A3 | PageDiet — duplicate & junk page suppressor | 4 | 5 | 5 | 5 | 5 | 5 | 5 | 3 | 4 | 4 | **45** |
| A9 | ChronoAudit — chronology verification pass | 5 | 4 | 4 | 4 | 4 | 5 | 5 | 4 | 4 | 5 | **44** |
| A2 | ChartSplit — production splitter & Bates indexer | 5 | 5 | 5 | 4 | 3 | 4 | 4 | 5 | 4 | 4 | **43** |
| A5 | GapCheck — provider index & completeness report | 5 | 5 | 4 | 4 | 3 | 4 | 5 | 4 | 3 | 4 | **41** |
| A4 | ChronoDesk — chronology workbench | 5 | 5 | 4 | 4 | 3 | 3 | 3 | 5 | 4 | 4 | **40** |
| A8 | DemandBuild — package assembler & statutory checklist | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 4 | 3 | 4 | **38** |
| A6 | SpecialsCheck — bill/treatment reconciler | 4 | 5 | 4 | 4 | 3 | 4 | 4 | 4 | 2 | 3 | **37** |
| A10 | LienClock — lien & settlement deadline docket | 4 | 4 | 4 | 4 | 4 | 4 | 3 | 4 | 2 | 3 | **36** |
| A7 | GapWatch — treatment gap flagger | 3 | 5 | 3 | 5 | 5 | 5 | 2 | 1 | 4 | 3 | **36** |

### The top three

**A1 — RecordsRate (49).** It scores at the ceiling because it is the rare concept where every axis aligns. The problem is measured in dollars by the practitioners themselves ($143.12 versus $7.08 on the same invoice). The tool never touches PHI — it generates letters and evaluates invoices — so it has no business-associate exposure and no security review to survive, which is the practical thing that kills small-firm software purchases. It is a decision table plus a mail merge, buildable in days. And the reason it does not exist commercially is structural: every vendor in the retrieval chain makes money from the fee status quo, so none of them will ever ship a tool that tells a firm the invoice is illegal. Open source is the only distribution model that fits. The maintenance burden — keeping fifty state fee schedules current — is real, and is precisely the thing a community can carry and a consultant can be paid to certify.

**A3 — PageDiet (45).** Highest ratio of value to build effort in the set. Page hashing is a solved technique; the innovation is entirely in framing — shipping the *suppression log* as the deliverable rather than hiding it, so the tool is auditable and a paralegal can defend it. ROI is arithmetic anyone can check in one minute: pages before, pages after, at $0.20–$0.75 per outsourced page or 20–50 pages per staff hour. It also feeds every other tool in the suite, which makes it an ideal adoption wedge.

**A9 — ChronoAudit (44).** Ranked third on total but first on strategic interest. It is the only concept in the set backed by *peer-reviewed* evidence of the underlying failure — 42% hallucination and 47% omission rates on clinical summarization in one PLOS study, a 1.47%/44%-major hallucination profile in another — and the only one with no identified substitute. It is also positioned uniquely: it does not compete with EvenUp or Supio, it makes their output defensible, which means the firms most likely to adopt it are the ones already spending money in this market. The risk is scope discipline. It must verify what can be verified mechanically — page exists, date present, provider present, nothing omitted — and refuse to imply it has checked clinical accuracy. A verifier that overstates its own coverage is worse than no verifier.

### What to investigate next

**A1 first**, because it is small, it is unblocked by privacy review, and its value can be validated with a single phone call to a firm that will read its last ten records invoices out loud. **A3 second**, as the wedge that gets the suite onto a machine. **A9 third**, but start the validation now, because it depends on an assumption not yet tested: that AI and LPO chronologies actually carry Bates or page citations that can be checked. If they routinely do not, A9 collapses into "verify against the whole production," which is a materially harder product.

A note on sequencing that matters more than the individual scores: A2 → A3 → A4 → A6 → A8 is a **pipeline**, and each stage is separately useful. Building it in that order means every release ships something a firm can use alone, and the integration value accrues to whoever installed the earlier pieces. A1, A5, A7, A9, and A10 are satellites that attach to the pipeline but do not require it.

---

## 6. Validation plan

### Questions to ask practitioners

**On retrieval and fees (A1):**

- Pull your last ten records invoices. What did you pay per provider, and what request path did you use?
- Have you ever disputed a records invoice? What happened?
- Do you use client-signed patient-directed requests? If not, what stopped you — is it the extra client contact, or not knowing it was available?
- What percentage of your requests get rejected, and for what reason?

**On production handling (A2, A3):**

- What is the largest single PDF you received last month, and what did you do with it first?
- Do you Bates number before or after you review? Who does it, and in what tool?
- Roughly what fraction of a typical production is pages you have already read?
- Have you ever paid an outsourcing vendor per page? Did you try to reduce the page count first?

**On the chronology (A4, A9):**

- Show me your chronology template. How many times does the same date of service get typed into something?
- When the demand cites a treatment date, can you find the page it came from in under thirty seconds?
- If you buy AI or outsourced chronologies: **does the output carry Bates or page citations on every row?** *(This is the load-bearing question for A9.)*
- Have you ever caught an error in a vendor or AI chronology? What kind?

**On completeness and gaps (A5, A7):**

- Tell me about the last time you discovered a missing record late. What was missing, and when did you find out?
- How do you know when you have all the records?
- Do you track treatment gaps? At what threshold, and who looks?

**On demand and liens (A8, A10):**

- How long does assembling the package take once the writing is done?
- Has a demand of yours ever been rejected or treated as defective on form grounds?
- How do you track Medicare conditional payment deadlines today?

### Who to interview

- **Pre-litigation case managers and demand writers at 3–15 attorney plaintiff firms** — the actual users. Los Angeles, Houston, Atlanta, and Phoenix are dense markets with heavy public hiring; the "demand writer" postings identify firms that have already separated this function and are therefore easiest to talk to about it.
- **Independent legal nurse consultants** — they see many firms' record sets and will be candid about quality, and they are a plausible *paying* customer segment for A9 and A4.
- **Paralegal trainers and continuing-education providers** — Paralegal Boot Camp-style organizations know the method taught versus the method practiced, and they are a distribution channel.
- **Small-firm consultants serving PI practices** — the caseload-benchmark consultancies have visibility into staffing ratios nobody publishes.
- **State trial-lawyer association listservs and section meetings** (CAALA, GTLA, TTLA and equivalents) — the operational articles in their magazines are written by members who will talk.
- **A firm that already pays for EvenUp or Supio** — the only way to test whether A9's premise holds.

### Search terms for further research

`"medical chronology" template paralegal` · `"demand writer" personal injury job description` · `HITECH request medical records law firm cost` · `"right of access" records fee dispute attorney` · `Bates numbering medical records production paralegal` · `"records request" tracking spreadsheet personal injury` · `medical bill "itemized statement" request personal injury demand` · `AI medical chronology accuracy attorney complaint` · `Medicare conditional payment deadline paralegal checklist` · `hospital lien perfection notice [state]` · plus targeted searches on **r/paralegal, r/LawFirm, r/Lawyertalk** — see the confidence note in §8; these were inaccessible from this environment and remain the single largest gap in the evidence base.

### Sample files and data needed

- **Three to five de-identified real productions** of 300–1,200 pages spanning at least one hospital ROI vendor, one physician office, and one imaging center. Without these, A2's boundary detection cannot be tuned and A3's duplicate rates cannot be measured. Synthetic PDFs will not do — the failure modes are artifacts of real fax and scan pipelines.
- **A real chronology with its source production**, to measure A9's verification coverage.
- **A vendor-produced or AI-produced chronology**, to confirm citation practice.
- **A set of records invoices** across at least five states, to build and test A1's fee table.
- **Itemized bills in both good and degraded form** (true itemized versus one-page summary) for A6.

De-identification is the practical obstacle. The most likely path is a partner firm willing to work under a written arrangement on closed files, or a public-record source: exhibits filed in litigation are sometimes available through PACER and county e-filing and contain real productions with real formatting pathologies.

### Prototype that would validate

Build **A1 in a weekend**, covering three states only (California, Texas, Georgia — chosen because their schedules differ structurally: per-page cap, tiered flat fee, and search-fee model respectively). Give it to two firms. The validating measurement is unambiguous: **the delta between what they paid on their last ten requests and what the tool says was owed.** If that number is small, the entire fee thesis is wrong and A1 should be abandoned. If it is large, A1 sells itself and pulls the rest of the suite in behind it.

Build **A3 in parallel** and run it over any real production to produce a single number — percentage of pages suppressed. That number either justifies the tool or kills it in an afternoon.

### Assumptions most likely to make this fail

1. **That small firms will install desktop software at all.** The industry has moved to cloud case management; a local Python or Electron tool may hit an IT-comfort wall even though it is *more* private. If this fails, everything here needs rehosting as a local web app with a one-click installer, or as an add-in to something they already run.
2. **That AI and LPO chronologies carry page citations.** A9 depends entirely on this. Untested.
3. **That the fee delta is real at scale.** Three firms published favorable numbers. Publication bias is obvious — firms that tried and got nowhere do not blog about it. The post-*Ciox* uncertainty on third-party-directed fees may mean the savings are smaller and more contested than the blog posts imply.
4. **That duplicate pages are a large fraction of productions.** The 50.1% JAMA figure is duplicate *text within EHR notes*, which is not the same as duplicate *pages in a produced PDF*. The page-level rate has never been measured publicly. If it turns out to be 5%, A3's ROI story evaporates.
5. **That the firm, not the vendor, is the buyer.** If small firms increasingly outsource the whole pre-litigation function — which is precisely what EvenUp's May 2026 "Pre-Litigation-as-a-Service" launch is betting on — then the user of these tools becomes the LPO and the offshore vendor, not the firm. That is not fatal (they buy tools too, and they are more price-sensitive per unit) but it changes distribution completely.
6. **That the case-management vendors do not simply absorb these features.** CASEpeer already gates a "Medical Requests Report" behind its Pro tier. The defense is that the highest-scoring concepts are ones a CMS vendor is structurally unlikely to build — A1 antagonizes the retrieval partners they integrate with, and A9 casts doubt on the AI features they are selling.

---

## 7. Cross-industry patterns

Patterns from this market and the specific backlog markets they transfer to.

**1. Statutory fee-schedule checker.** Compute the maximum lawful charge for a routine transaction from a versioned, jurisdiction-keyed rules table, and generate a citation-bearing dispute letter when an invoice exceeds it. Transfers to: **Workers' compensation medical billing and state fee schedule compliance** (backlog, narrow-subspecialty — nearly identical mechanics against state WC fee schedules); **Patient financial counseling / No Surprises Act Good Faith Estimate compliance**; **Independent pharmacy third-party reconciliation and PBM claw-backs**; **Freight bill audit and payment for small shippers**; **Property tax consulting and assessment appeal firms**.

**2. Document-blob decomposer with human-correctable boundaries.** Split a large multi-document PDF into labeled units using deterministic layout signals first, with a mandatory human correction pass and an explicit "could not classify" report. Transfers to: **Title abstracting and independent title search contractors**; **Mortgage post-closing QC and trailing document vendors**; **County recorder document intake and indexing**; **Environmental laboratories producing regulator EDD deliverables**; **Federal construction contractors handling UFGS submittal registers**.

**3. Duplicate suppression with an auditable suppression log.** Two-channel hashing (normalized text + perceptual image) to collapse redundant pages, where the log of what was removed is a first-class deliverable and nothing is deleted. Transfers to: **Third-party claims administration and self-insured program operations**; **IA firm claims operations and file QA desks**; **Supplier quality engineering at OEMs receiving supplier deliverables**; **Aerospace supplier quality clause library administration**.

**4. Expected-versus-received completeness diff.** Build the universe of what *should* exist from multiple independent sources — including references mined out of the documents already received — then diff against what arrived and emit the specific next request. Transfers to: **Construction submittal, RFI and closeout coordination** (submittal register versus received submittals); **Provider credentialing and payer enrollment services**; **Prime contractor supplier cyber-compliance desks collecting attestations**; **C3PAO assessment operations and evidence sampling**; **Certificate-of-insurance compliance from the holder side**.

**5. Deterministic verification layer over AI or outsourced work product.** Mechanically check every assertion in a generated document against its cited source — does the citation exist, does the cited value appear there, and what in the source is missing from the output — and refuse to use AI to check AI. Transfers to: **every market in the backlog where an AI summarizer has entered**, and specifically **Independent property and casualty claims adjusting**, **Medicare Advantage risk adjustment / HCC coding**, **Forensic engineering cause-and-origin reporting**, **Third-party estimate writing services (Xactimate desks)**, and **Fiduciary and forensic accountants producing court accountings**.

**6. Source-once, export-many.** One structured dataset with source-page anchoring that emits every downstream document format, eliminating re-keying between an internal working artifact and a client- or counterparty-facing one. Transfers to: **Geotechnical and environmental consulting field data → report tables**; **Fire protection ITM inspection findings → NFPA 25 report → deficiency proposal**; **Commissioning providers' issue logs → owner reports**; **Test, adjust and balance contractors' field readings → certified TAB report**; **Conservatorship and guardianship court accountings**.

**7. Statutory-form conformance checklist as versioned rules.** Encode a jurisdiction's mandatory elements for a document that has legal effect (content, delivery method, timing, required citation) as human-readable rules, and check the assembled document before it goes out. Transfers to: **Multi-state charitable solicitation registration compliance**; **Community floodplain administration permit issuance**; **Government contracts administration clause and mod review**; **Real estate closing law firms in attorney-opinion states**; **Certified payroll and prevailing wage compliance**.

**8. Mixed business-day/calendar-day regulatory deadline docket.** Generate a dated task list from lien- or claim-type rule packs where the arithmetic mixes business days and calendar days and interest begins on a specific day. Transfers to: **Third-party claims administration**; **Unclaimed property and escheat compliance**; **Retirement plan third-party administrators**; **DOT compliance consultancies serving small fleets**; **Court probate examiner and clerk offices**.

---

## 8. Sources and confidence

### Verified findings — primary sources or peer-reviewed literature

- **Duplicate text in medical records.** Steinkamp J, Kantrowitz JJ, Airan-Javia S. *JAMA Network Open.* 2022;5(9):e2233348 — 104,456,653 notes, 1,960,689 patients; 50.1% of total text duplicated from prior text, rising from 33.0% (2015) to 54.2% (2020). https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2796664
- **LLM hallucination and omission on clinical summarization.** *PLOS Digital Health* — 100 ED encounter summaries; GPT-4: 42% with hallucinations, 47% with clinically relevant omissions, 33% error-free. https://journals.plos.org/digitalhealth/article?id=10.1371%2Fjournal.pdig.0000899 · *npj Digital Medicine* (2025) — 450 transcript-note pairs, 12,999 clinician-annotated sentences; 1.47% hallucination rate (44% major), 3.45% omission rate (16.7% major). https://www.nature.com/articles/s41746-025-01670-7
- **HIPAA right of access.** 45 CFR §164.524 — 30-day response, one 30-day extension; permitted fee components limited to copying labor, supplies/media, postage, and agreed summary preparation; third-party directive text. https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-E/section-164.524
- **Designated record set includes billing records.** 45 CFR §164.501. https://hhhealthlawblog.com/hipaa-patient-access-and-designated-record-sets/
- **Subpoena route assurances.** 45 CFR §164.512(e). https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-C/part-164/subpart-E/section-164.512
- ***Ciox Health v. Azar*** (D.D.C. 2020) — vacatur of the 2016 patient-rate fee guidance and the 2013 third-party-directive expansion. Opinion: https://www.privacysecurityacademy.com/wp-content/uploads/2021/06/Ciox-v-Azar.pdf · Analysis: https://www.bairdholm.com/blog/late-breaking-on-heels-of-major-court-defeat-ocr-issues-notice-regarding-individuals-right-of-access-to-health-records/
- **OCR Right of Access enforcement.** Concentra settlement, $112,500, May 2025 — https://www.hhs.gov/press-room/ocr-settles-with-concentra.html · https://www.hipaajournal.com/concentra-hipaa-settlement-2025/ · Prior actions summary: https://www.nixonpeabody.com/insights/alerts/2024/04/08/cmp-and-financial-settlement-are-latest-results-of-ocrs-hipaa-right-of-access-initiative-enforcement
- **Information blocking disincentives.** Final rule published 7/1/2024; median hospital disincentive $394,353. https://www.federalregister.gov/documents/2024/07/01/2024-13793/21st-century-cures-act-establishment-of-disincentives-for-health-care-providers-that-have-committed
- **ROI fee litigation.** *Justis v. CIOX Health*, No. 3:22-cv-00023 (W.D. Va.) — https://www.classaction.org/news/class-action-claims-ciox-health-charges-unauthorized-fees-for-copies-of-medical-records · Ciox Texas class settlement, $1.85M — https://topclassactions.com/lawsuit-settlements/money/fees/ciox-health-records-fees-1-85m-class-action-lawsuit-settlement/ · NOSSCR OCR complaint (3/25/2024) — https://nosscr.org/article/nosscr-files-complaint-against-ciox-health-alleging-excessive-fees-and-more/
- **State fee schedules.** Cal. Evid. Code §1563(b) — https://law.justia.com/codes/california/code-evid/division-11/chapter-2/article-4/section-1563/ · N.Y. Pub. Health Law §18 — https://www.health.ny.gov/publications/1443/ · 22 TAC §165.2 (Texas physician offices) — https://william-beaumont.tricare.mil/Portals/149/TX%20Medical%20Records%20Fees%20Jan%202022.pdf · Texas SB 490 itemized-billing requirement — https://capitol.texas.gov/tlodocs/88R/analysis/html/SB00490F.htm
- **California subpoena procedure.** CCP §1985.3 notice-to-consumer timelines; Evid. Code §1561 custodian declaration. https://www.oncalllegal.com/how-to-subpoena-medical-records-in-california/
- **Georgia time-limited demand statute.** O.C.G.A. §9-11-67.1, five material terms and delivery requirements. https://www.christophersimon.com/ocga-9-11-67-1-georgia-policy-limits-demand-statute.html
- **Paralegal market structure and compensation.** NALA 2024 National Utilization and Compensation Report — $134/hour average billing rate; approximately one-third of paralegals work with 2–5 attorneys; 15% compensation increase 2022–2024. https://nala.org/wp-content/uploads/2025/01/2024-NALA-Compensation-Utilization-Report-ExecSumm-FINAL-1-15-25.pdf
- **Small-firm software and AI adoption economics.** Clio 2025 Legal Trends for Solo and Small Firms — 67% of small firms use AI in some capacity but only 4% widely; average small firm spends 2% of expenses on software; salaries are 30% of small-firm expenses. https://www.clio.com/blog/solo-small-law-firms-highlights-2025-legal-trends/
- **Live role definitions and pay bands (August 2026).** Demand writer postings at $28–$40/hr and $30–$60/hr — https://to.indeed.com/aaxf96hkdkgp · https://to.indeed.com/aaqgg8qdwwfw · PI paralegal $32–$55/hr with discovery, subpoena, calendar and exhibit duties — https://to.indeed.com/aabjjgbmb4bp · Houston pre-litigation case manager, $43k–$63k, explicitly owning records, chronologies, summaries, demand packages and lien tracking — https://www.careerbuilder.com/job-details/pre-litigation-personal-injury-paralegal-case-manager-houston-tx--7761e61f-a897-4b09-909f-3a2fdc9e86bc
- **Published vendor pricing (verifiable on the vendor's own page).** CASEpeer $79/$119/$149 — https://www.casepeer.com/pricing/ · Neos $109/user/month, 3-user minimum — https://www.assemblysoftware.com/pricing · ChartRequest $25/request — https://chartrequest.com/medical-records-retrieval-for-lawyers/ · Record Retrieval Solutions $45/request — https://www.recordrs.com/pricing/ · LezDo TechMed per-page rate card — https://www.lezdotechmed.com/medical-record-review-pricing/ · CaseMark $100/user/month — https://casemark.com/pricing · Casefleet $30–$140/user/month with per-page OCR overage — https://www.casefleet.com/blog/legal-ai-pricing-rate-limits-and-overages
- **Market consolidation.** Datavant–Ontellus acquisition, including Datavant's own admission that retrieval "remains highly fragmented" — https://www.datavant.com/press-release/datavant-to-acquire-ontellus-to-transform-medical-record-retrieval-with-tech-enabled-health-records-retrieval-and-claims-intelligence-solutions · Datavant–DigitalOwl — https://www.healthcareittoday.com/2025/10/30/datavant-to-acquire-digitalowl-powering-faster-smarter-medical-data-reviews/ · EvenUp Pre-Litigation-as-a-Service, May 2026 — https://www.lawnext.com/2026/05/evenup-extends-beyond-software-with-launch-of-pre-litigation-as-a-service-offering-for-pi-law-firms.html

### Strong inferences — practitioner-authored, credible, but single-source or self-interested

- **The fee-reduction playbook and its dollar results.** Locke Law Firm's $143.12 versus $7.08 comparison — https://thelockefirm.com/hitech · Fell Law's "$1.50/page" to "about $10" — https://www.fellfirm.com/saving-money-on-medical-records-requests-with-the-hitech-act/ · Wetherington Law Firm's no-letterhead technique and Georgia caps — https://wfirm.com/getting-medical-records-cheaply-using-the-hitech-act/ · Duffy & Duffy's CURES Act / information-blocking alternative — https://www.duffyduffylaw.com/blog/patient-access-to-low-cost-medical-records/ — **Confidence caveat:** all four are firms publicizing their own success. Publication bias is structural here.
- **Chronology method and column conventions.** Paralegal Boot Camp — https://paralegal-bootcamp.com/10-tips-for-summarizing-medical-records/ and https://paralegal-bootcamp.com/preparing-the-personal-injury-demand-package/ · The Paralegal Society — https://theparalegalsociety.wordpress.com/2013/01/21/personal-injury-summarizing-medical-records/ — Consistent across independent trainers over more than a decade, which is why I treat the spreadsheet-as-chronology finding as reliable despite no survey behind it.
- **Demand-package requirements.** "The reasonable demand," *Advocate* (CAALA), July 2021 — https://www.advocatemagazine.com/article/2021-july/the-reasonable-demand · Lien practice at mediation, *Advocate*, September 2023, including Civ. Code §3045.3 perfection and *Nager v. Allstate* (2000) 83 Cal.App.4th 284 — https://www.advocatemagazine.com/article/2023-september/mediating-cases-with-large-medical-liens · Small-firm CMS reality at a 7-person plaintiff firm, *Advocate*, August 2025 — https://www.advocatemagazine.com/article/2025-august/embracing-casepeer
- **The double-entry complaint.** Named senior paralegal at a named Northern California firm: "That's twice we're doing the same work." Published in a **vendor case study**, so the framing serves the vendor — but the specific complaint is too concrete and too unflattering to the pre-existing workflow to be invented. https://www.supio.com/customers/paralegals-at-j-chrisp-law-reclaimed-80-hours-per-case-through-supio-ai
- **AI accuracy reporting on a specific vendor.** *Business Insider*, November 2024 — former EvenUp employees on AI unreliability, missed injuries, and fabricated conditions. Original inaccessible from this environment; verified only via secondaries: https://slashdot.org/story/24/12/13/154228/legal-tech-unicorn-evenup-relied-heavily-on-humans-despite-ai-claims and https://opentools.ai/news/evenups-ai-overpromise-legal-tech-startup-faces-scrutiny — **cite as reported, not as verified at source.**
- **Production pathology descriptions.** Interleaved bills and records, fax covers, repeated ER reports, missing operative reports and imaging — described consistently across four independent commercial sources with different business models: https://gsblposervices.com/why-unorganized-medical-records-delay-personal-injury-settlements/ · https://www.chartrequest.com/articles/incomplete-medical-records-legal · https://www.tavrn.ai/blog/medical-records-paralegal · https://www.wisedocs.ai/blogs/how-do-paralegals-review-medical-records-for-claims-cases-and-files — The convergence across competitors is what makes this credible; the individual sources are marketing.
- **Bill-to-record reconciliation as a discrete task**, with named failure modes — https://gsblposervices.com/understanding-medical-bills-vs-medical-records-in-pi-claims/ · ICD/CPT hardening of demands — https://triventlegal.com/blogs/how-icd-and-cpt-codes-strengthen-settlement-demand-letters-for-personal-injury-cases/
- **Medicare MSP deadline set** — https://partnerwithsynergy.com/understanding-medicare-conditional-payments-timelines-final-demands-your-obligations/ — specialist vendor; **cross-check every date against CMS primary sources before encoding into A10**: https://www.cms.gov/medicare/coordination-benefits-recovery/attorney-services
- **The plaintiff-firm business-associate position.** A plaintiff firm holding records under its own client's authorization is generally not a HIPAA business associate — https://www.semelconsulting.com/2014/05/20/when-is-a-lawyer-or-accountant-a-hipaa-business-associate/ — **directly contradicted** by a major vendor guide asserting law firms "are considered business associates" (https://www.clio.com/resources/personal-injury-for-lawyers/medical-records/). The consultant's analysis is better reasoned and distinguishes plaintiff from defense posture, but **this should be confirmed with health-privacy counsel before it is used as a product marketing claim**, because A1's entire positioning rests on it.
- **First-party complaint evidence on ROI vendors.** Datavant/Ciox BBB profile — 31 reviews averaging 1 of 5 stars, including a 38-year legal professional on "the level of incompetence." https://www.bbb.org/us/ga/alpharetta/profile/health-and-wellness/datavant-formally-ciox-health-0443-27163823/customer-reviews — Small, self-selected, negative-skewed sample. Directionally useful, statistically meaningless.

### Tentative hypotheses requiring practitioner validation

- **Duplicate pages are a large fraction of litigation productions.** The 50.1% JAMA figure measures duplicate *text within EHR notes*, not duplicate *pages in a produced PDF*. No public source measures the page-level rate. **A3's ROI story depends on a number nobody has measured.** Measure it before building.
- **Hours per chronology (8–10, 20+ complex) and hours per case (80+).** All vendor-published; the 8–10 figure is explicitly unattributed, the 80+ is one named paralegal at one firm in a vendor case study.
- **Review throughput of 20–50 pages/hour.** Single vendor source.
- **Caseload of 25–40 active cases per PI records paralegal.** Single vendor source with no survey behind it; a separate consultancy publishes 20–100 depending on support structure and maturity, which is a range wide enough to be unusable for sizing.
- **"Average of 4 months" to assemble a complete record set in-house, and the $76-labor/$68-provider per-request figures.** From an unpublished self-run survey of "500+ firms" by a vendor selling the alternative. https://chartsquad.com/about-us/medical-records-news-and-information/records-request-operational-costs/
- **Treatment gap prevalence (16.8% / 32.4% / 43%).** Proprietary corpus analysis by a vendor launching a product to solve it. https://www.lawnext.com/2025/12/evenup-launches-medical-management-tool-to-address-treatment-gaps-in-personal-injury-cases.html
- **EvenUp, Supio, Eve, and Filevine actual prices.** None published. Every figure circulating is a third-party estimate or a competitor's claim. The "$300 base rising past $800" figure comes from a direct competitor and should not be repeated as fact.
- **Whether AI and LPO chronologies carry per-row page citations.** Untested and load-bearing for A9.
- **Word versus Excel versus CMS module split for chronologies.** No survey exists. Trainers recommend spreadsheets; vendors assume their own module.
- **Malpractice claim frequency from missed litigation deadlines.** Searched; only vendor blogs surfaced. No ABA professional-liability claims data located.

### Method limitations

**Practitioner forums were inaccessible.** Reddit — r/paralegal, r/LawFirm, r/Lawyertalk, r/personalinjury — returned HTTP 403 from this environment's egress proxy across HTML, JSON, and domain-restricted search, and per policy I did not route around it. Two independent research passes both hit this wall. *Business Insider* and portions of hhs.gov were likewise blocked. The unfiltered practitioner-complaint layer is therefore **absent from this report**, and I substituted first-party review platforms, live job postings, trial-lawyer association magazines, and practitioner-authored training material. Those substitutes are good — the job postings in particular are unusually informative because they enumerate the task list without a sales motive — but they systematically under-represent frustration, workarounds, and the things practitioners say only anonymously. **Any follow-up cycle on this market should begin by re-running the forum searches from an unrestricted network**, and the top three concepts should not be built without at least five practitioner conversations, because the strongest quantitative claims in this report all originate with parties who profit from them.
