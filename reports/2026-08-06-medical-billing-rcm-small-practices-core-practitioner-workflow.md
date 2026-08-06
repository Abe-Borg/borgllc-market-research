# Medical Billing and Revenue Cycle for Small Practices — Core Practitioner Workflow

**Market:** Medical billing and revenue cycle for small practices
**Angle:** core-practitioner-workflow
**Claim ID:** `790d3912`
**Date:** 2026-08-06

---

## 0. Cycle header

### Why this assignment

The ledger held 211 backlog items across 91 markets, of which **81 markets had zero completed reports**. The first-priority rule is catalog breadth, and the ten completed reports were heavily concentrated in the built environment and adjacent professional services: fire protection design, land surveying, MEP engineering, geotechnical/materials testing, commercial property management, machine shops, freight brokerage, insurance agency back office, nonprofit grants, immigration law. **Healthcare — the single largest administrative-labor market in the United States — was completely untouched.**

Within healthcare I chose small-practice medical billing over the adjacent candidates (dental practice administration, staffing agencies, title/escrow, small CPA practices) for three reasons:

1. **The core data is a public, standardized, machine-readable file format.** The X12 835 remittance advice and 837 claim are HIPAA-mandated standards. Practices can obtain their own raw files from clearinghouses. This is the single best precondition for small, local, open-source tooling — it is the healthcare analogue of the "standardized transaction file the incumbent hides" pattern already recorded in the ledger from the freight brokerage cycle.
2. **There is a documented, hard price floor in the commercial tooling.** Denial analytics and underpayment detection are sold almost exclusively to hospitals and multi-site groups at quote-only prices; the only vendor with published pricing starts at $6,000/year. Practices below roughly $1–2M in collections have Excel or nothing.
3. **The evidence base is unusually quantified.** CMS, KFF, MGMA, AMA, and CAQH all publish hard numbers on denial rates, appeal rates, per-transaction costs, and rework costs. Few markets in this backlog allow claims to be grounded that precisely.

I chose `core-practitioner-workflow` over `back-office` because for a small billing company — the most motivated buyer in this market — claim submission through cash collection *is* the billable production work, not overhead. Angle balance across the catalog was the third-priority criterion and market breadth won.

### Backlog status

**210 assignments remain** in the backlog after this claim was taken (211 → 210), across 91 markets. This report appends 11 newly discovered markets, so the standing backlog will grow rather than shrink.

---

## 1. Market examined

**Industry.** United States outpatient/ambulatory healthcare revenue cycle management (RCM) — the process of turning a delivered clinical service into collected cash.

**The two buyer types.**

- **Small physician practices, 1–10 clinicians.** Per the AMA's 2024 Physician Practice Benchmark Survey, **47.4% of US physicians still practice in groups of 10 or fewer**, and **11.9% are solo** — though both figures are in long decline (61.4% and 18.4% respectively in 2012, the first time the ≤10 figure has fallen below half). **42.2% of physicians remain in physician-owned private practice.** ([AMA PRP, 2024](https://www.ama-assn.org/system/files/2024-prp-pp-characteristics.pdf)) This is a shrinking but still very large installed base, and it is the segment with no in-house RCM analytics department.
- **Independent third-party billing companies, roughly 1–25 employees.** These are the highest-information, highest-motivation buyers. Their margin is directly hours-per-claim, they see five to thirty practices' books at once, and they are already accustomed to buying their own tools. Practitioner forum evidence for this report comes disproportionately from this population.

**The professional role.** Titles vary — medical biller, AR follow-up specialist, revenue cycle specialist, billing manager, practice administrator. In a 3-provider practice this is frequently **one person**, sometimes part-time, sometimes the office manager wearing a second hat. A representative job posting from an RCM firm that explicitly refuses hospital-only candidates asks for **10+ years of experience at $22–25/hour** and lists as duties: *"Aggressively manage insurance accounts receivable to maximize collections"*, *"Investigate, resolve, and appeal denied, rejected, and underpaid claims"*, *"Analyze payer trends and identify recurring reimbursement issues"*, *"Monitor timely filing deadlines"* ([AAPC forum](https://www.aapc.com/discuss/threads/we-are-hiring-experienced-medical-billers-remote-f-t.236242/)). Another posting reduces the entire job to four nouns: *"Appeals," "AR," "Denials," "Payment posting"* ([AAPC forum](https://www.aapc.com/discuss/threads/part-time-medical-biller.235659/)).

**Type of user for any tool built here.** Windows-first, Excel-fluent, not a programmer, working inside a browser-based PM/EHR all day, with local folder access and — critically — a legal obligation to keep protected health information (PHI) under control. The user will not stand up a server, will not sign an enterprise contract, and will not send patient data to an unknown cloud service without a Business Associate Agreement.

---

## 2. How the work is performed

The workflow below is the composite reconstructed from practitioner forum accounts, job postings, and vendor documentation. Software named is what small practices actually run: Tebra (formerly Kareo), AdvancedMD, eClinicalWorks, athenahealth, DrChrono, CareCloud, Practice Fusion, SimplePractice, TherapyNotes, ChiroTouch, Office Ally Practice Mate, Medisoft, OpenEMR.

### 2.1 Front end — eligibility and authorization

Before the visit, staff verify insurance eligibility and obtain prior authorization where required.

- **MGMA Stat (March 10, 2026; 294 respondents): 45% of practice staff phone time goes to eligibility and prior authorization** — the largest single category, ahead of scheduling at 31%. Practice leaders describe *"submitting requests, tracking status, handling denials and appeals, and responding to constant status-check calls"* and name the friction point as translating vague payer responses like *"we need more information."* ([MGMA](https://www.mgma.com/mgma-stat/phones-are-still-a-backlog-costing-medical-practices-time))
- **CAQH 2024 Index:** prior authorization is only **35% fully electronic**; provider cost per transaction is **$12.88 manual / $8.93 portal / $5.38 electronic**, and it takes **24 minutes by phone, 16 minutes by portal**. Eligibility verification is nominally 96% electronic but still costs providers **$8.57 manual / $4.46 portal / $2.00 electronic**. A practice quoted in the Index: *"When it comes to eligibility and benefits, I don't have an automated tool that I can trust, so I don't use it."* ([CAQH Index 2024, PDF](https://www.caqh.org/hubfs/Index/2024%20Index%20Report/CAQH_IndexReport_2024_FINAL.pdf))
- **AMA physician survey:** physicians and staff spend an average of **12–13 hours per week** on prior authorization; roughly **35–40% of practices have staff dedicated exclusively to it**. ([AMA](https://www.ama-assn.org/practice-management/prior-authorization/over-80-prior-auth-appeals-succeed-why-aren-t-there-more))

Practitioner accounts describe multi-touch verification with no dedicated tool: *"It starts at the time of appointment scheduling and again before the patient comes in"*; the tracking artifact is Excel — *"create an update Excel sheet with listing providers names, NPI with each assigned insurance payer ID"* ([AAPC](https://www.aapc.com/discuss/threads/insurance-verifications.189422/)).

### 2.2 Charge capture and coding

The clinician documents in the EHR; a superbill or charge ticket is produced; a biller or coder reviews CPT/HCPCS codes, ICD-10 diagnoses, modifiers, and units, then enters charges. In small practices this review is often a *"superbill accuracy check"* performed by an in-office specialist described as *"a bridge between our clinical team and our RCM partner"* ([AAPC](https://www.aapc.com/discuss/threads/medical-billing-charge-entry-specialists-in-office.235924/)).

Coders consistently report EHRs are not built for them. Comparing NextGen, Cerner, and Athena, one coder concludes flatly: *"EMR's are not designed with coders in mind"* — Cerner corrections *"very time consuming"* and taking ten times longer, Athena's RVU ordering unreliable ([AAPC](https://www.aapc.com/discuss/threads/what-is-the-best-emr-system-you-have-ever-used.172685/)).

### 2.3 Scrubbing and submission

The PM system or clearinghouse "scrubs" the claim against edit rules, then transmits an **X12 837P** file. Clearinghouses used by this segment: Office Ally, Claim.MD, Availity, Waystar, Optum/Change Healthcare, TriZetto.

Scrubbing is a genuine differentiator and a genuine complaint. One billing-service owner: *"out of ALL the billing systems I've worked on their e-scrubber is by far the most powerful."* Another, on the same product: *"takes almost 48 hours (2 days!!!) for the claim to exit their internal scrubber and go to the payor"* — attributed to double-scrubbing at the PM and then again at the clearinghouse ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,7276.0.html)).

### 2.4 Acknowledgment and rejection

The clearinghouse and payer return **999** (functional acknowledgment) and **277CA** (claim acknowledgment) files. Rejections at this stage never became claims and never appear in AR — they are invisible unless someone opens the report. Practitioner accounts of this stage are dominated by opacity: *"All my claims are rejected for Insurance Type"* with no path to diagnose, and support gated behind training signups ([AAPC](https://www.aapc.com/discuss/threads/office-ally-training-issues-and-what-it-can-do.233414/)).

### 2.5 Adjudication and remittance

The payer adjudicates and returns an **X12 835** electronic remittance advice (ERA), plus an EFT. The 835 carries, per service line: billed charge, allowed amount, paid amount, and one or more **CARC** (Claim Adjustment Reason Codes) with **CARC group codes** (CO = contractual obligation, PR = patient responsibility, OA = other adjustment, PI = payer initiated) and optional **RARC** (Remittance Advice Remark Codes). Provider-level adjustments — recoupments, offsets, interest, capitation — arrive in the **PLB** segment.

CAQH puts remittance advice at **$5.67 manual / $5.31 portal / $2.95 electronic** per transaction for providers, and notes providers routinely pull **both** the ERA and the plan portal for supplemental information, **creating a duplicate posting workflow**.

### 2.6 Payment posting

Payments are posted to the ledger, contractual adjustments written off, patient responsibility moved to the patient balance, and secondary claims generated. This is where the small-practice tooling gap first becomes financially dangerous:

> *"Kareo's can be weird at times when it throws something into the denial area that isn't actually a denial, but the two that drive me crazy are NueMd and Health Fusion. **They will automatically 'write off' any denied charges**, and to go back and 'undeny' those charges for resubmittal is tedious."* — kristin, biller working across multiple client systems ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,8305.0.html))

Auto-posting is frequently a **paid add-on**. A practice on Medisoft: *"We have never had the auto-post capability... They quoted me $499 to install a module to receive ERA's for auto-post"* — after 25 years of manual posting ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,8571.0.html)).

### 2.7 Denial management, AR follow-up, and appeals

Unpaid and underpaid claims are worked from an aging report. The tracking artifact is, verifiably, a spreadsheet. An AAPC Knowledge Center article by a CPC describes the recommended method as a **"Denial Tracking Log"** — denial reasons down the rows, the practice's top 10 payers across the columns, tick marks added as denials are worked, maintained *"over a two- to three-month period"* to see patterns ([AAPC](https://www.aapc.com/blog/10034-streamline-your-denials-with-one-simple-spreadsheet/)).

For AR recovery specifically, a billing-service owner's advice is to skip tooling entirely: *"If you're only going to do A/R Recovery I would just work off of reports"* — the client's PM aging report, accessed remotely. A second owner: *"I would highly recommend using the software of the client... Just try to figure out a way to log into their system"* ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,7422.0.html)).

Prioritization is by dollar size, not root cause: *"I would work the biggest balances first,"* noting *"it costs about $10 to send out a patient statement"* ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,8552.0.html)).

Appeal letters are hand-built each time: *"I constantly modify our appeal letters based on the patient's policy vs. provider/hospital contracts, state vs. federal laws, CMS policy manuals, LCD, and NCDs"* ([AAPC](https://www.aapc.com/discuss/threads/ins-appeal-letters.201352/)).

### 2.8 Patient balance and close

Statements go out; balances age; some go to collections; some are written off. Statement cost is real money at small volume (~$10 per statement cycle per the practitioner quote above; DrChrono publishes $0.90 per mailed statement, TherapyNotes $1.00 per paper claim).

### 2.9 What the workflow produces

Documents and files in play: superbill/charge ticket, CMS-1500 (paper) and 837P (electronic), 999/277CA acknowledgments, 835 ERA, paper EOB (still common from smaller payers and for secondaries), AR aging report, payer fee schedules and contracts, credentialing/enrollment files (CAQH ProView attestations, PTAN/group IDs, revalidation notices), appeal letters and supporting clinical documentation, patient statements.

---

## 3. Most important problems, ranked

### P1 — Denials are not measured, only individually worked

**Who:** Every biller and practice administrator in a 1–10 provider practice.
**When:** Continuously; visible at posting and at AR follow-up.
**Currently handled by:** Working the aging report claim-by-claim, largest dollar first. Pattern detection, if it happens at all, is a hand-tallied Excel log.
**Why inadequate:** Working claims individually treats symptoms. The recurring root cause — one payer's new modifier requirement, one provider's expired enrollment, one CPT that a specific plan never covers — is invisible until someone aggregates. The single most-cited *recommended practice* in the literature is manual tallying, which tells you the tooling doesn't exist.
**Frequency:** Continuous.
**Cost:** MGMA's figure, cited repeatedly in the family-medicine literature, is **~$25 to rework a denied claim**, with **more than 50% of denied claims never reworked at all**. A worked example for a single physician with 44 denials/month is **$1,100/month, $13,200/year** in pure rework labor, before counting the never-reworked claims as lost revenue ([AAFP FPM](https://www.aafp.org/fpm/2015/0300/p7)). Physicians Practice reports the same $25 figure and *"as many as 60% of returned claims are never resubmitted"* ([Physicians Practice](https://www.physicianspractice.com/view/why-getting-claims-right-first-time-cheaper-reworking-them)).
**Evidence strength:** High. Multiple independent sources; direct practitioner evidence of the spreadsheet workaround.

### P2 — Underpayment is essentially undetected at small practices

**Who:** Practice owners and billing companies.
**When:** At posting; almost never caught.
**Currently handled by:** Not handled. Every fee-schedule discussion I found among small-practice billers is about setting *charges* (*"our fees are determined by our Blue Cross allowed multiplied by 130%"*; *"I use the RVU/Medicare Allowable rate to see what Medicare's allowed amount is, but I know that I need to set our prices significantly higher"*), not about verifying *payments* ([AAPC](https://www.aapc.com/discuss/threads/determining-how-much-to-set-your-fee-schedule.193884/)). One thread's stated method is *"a hybrid process"* of CMS lookup, local rumor, and *"good old fashioned Googling"* ([AAPC](https://www.aapc.com/discuss/threads/setting-clinic-fee-schedule.195781/)).
**Why inadequate:** A payer paying 3% below the contracted rate on a high-volume code is invisible to claim-by-claim review and material in aggregate. When practitioners do catch it, the process is a one-off manual comparison — one biller compared payments to quoted benefits, called the payer, had the patient call, supplied a correctly-paid comparison claim, **and the payer still refused to adjust** ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,12613.0.html)). A neurologist could not even obtain her own annual reimbursement data from her payers; the forum administrator's answer: *"I do not believe there is any way to look that information up yourself"* ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,12503.0.html)).
**Frequency:** Every remittance.
**Cost:** Unquantified at small-practice scale — that is precisely the problem. The entire commercial "payment variance" category exists because the dollars are large at hospital scale; nobody has measured it at 3-provider scale because nobody has the tool.
**Evidence strength:** High for the *absence of tooling and practice*; low for the dollar magnitude. Flagged as the single most important thing to validate before building.

### P3 — Timely filing and appeal deadlines are tracked by nothing

**Who:** Billers; the practice eats the loss.
**When:** Silently, until the denial arrives.
**Currently handled by:** Memory and diligence. I found **no practitioner describing any deadline-tracking mechanism** — no tickler, no report, no calendar. The concept appears only as a job-posting duty ("Monitor timely filing deadlines").
**Why inadequate:** The deadline is unrecoverable and the money is unbillable to the patient. On a Medicare late-filing penalty: *"If you have been charged with a late filing fee you cannot charge the patient for that amount. You need to adjust it off as a contractual adjustment... By being a participating provider you agree to follow the rules of the insurance carrier"* ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,422.0.html)).

Three documented failure mechanisms, all deterministic and all preventable by arithmetic:
1. **Secondary-after-primary lag.** A claim where the primary paid in April, the secondary was billed in May, and the secondary denied for timely filing — because that plan's 95-day limit ran from *date of service*, not primary adjudication ([AAPC](https://www.aapc.com/discuss/threads/timely-filing-denial.193083/)).
2. **Patient withheld coverage.** Insurance disclosed ten months after service; denied untimely; and having already billed insurance, billing the patient becomes legally questionable ([AAPC](https://www.aapc.com/discuss/threads/timely-filing-when-patient-did-not-update-insurance.160670/)).
3. **Loss of access to denials.** *"Working from home... I have limited access to certain items making it difficult to get denials and respond timely"* ([AAPC](https://www.aapc.com/discuss/threads/timely-filing.172505/)).

Compounding this: **appealed claims fall out of AR visibility.** On writing off at 90 days while an appeal is pending, one biller notes that once written off *"it's much harder to track it and pursue the payment"*; another adds *"Some payers won't even decide on a 1st appeal/reconsideration until 60 days from date it is received"* ([AAPC](https://www.aapc.com/discuss/threads/a-r-question-about-writting-off-claims-that-are-being-appealed.131380/)).
**Frequency:** MGMA's denial-source poll put timely filing at **7% of denials** ([MGMA](https://www.mgma.com/mgma-stat/mgma-stats/finding-hidden-treasure-by-uncovering-and-fixing-the-sources-of-claim-denials)).
**Cost:** 100% loss of the claim value, not recoverable from anyone.
**Evidence strength:** High for the failure mechanisms; the absence of tooling is a strong negative finding across two forums.

### P4 — CARC/RARC codes do not map to actions

**Who:** Billers, especially the less experienced ones staffing small practices.
**When:** Every remittance.
**Currently handled by:** Individual lookup, forum questions, guessing.
**Why inadequate:** The codes are ambiguous and frequently point away from the real problem. A biller reports *"getting CO 45 denial codes that I am not getting paid anything for"* — CO-45 is a contractual adjustment, not a denial at all, and the real cause turned out to be a non-covered in-office surgical code ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,7438.0.html)). Even the liability split confuses experienced staff: PR-45 is billable to the patient, CO-45 is not, and a thread exists solely to establish that ([AAPC](https://www.aapc.com/discuss/threads/pr-45.233693/)). Generic codes are useless alone: *"The 16 tells you that there's a submission error on the claim. The remark code M51 is giving you more specific information"* ([AAPC](https://www.aapc.com/discuss/threads/835-healthcare-policy-identification.129991/)).

Systemically, denial reasons are opaque even in aggregate: KFF found that of ~79 million denial reasons reported for ACA marketplace in-network claims in 2024, **36% were coded "Other" and 25% "administrative"** — over half of denial reasons carry effectively no information ([KFF](https://www.kff.org/patient-consumer-protections/claims-denials-and-appeals-in-aca-marketplace-plans-in-2024/)).
**Frequency:** Continuous.
**Cost:** Folds into P1 rework cost; also causes misclassification and improper write-offs.
**Evidence strength:** High.

### P5 — Recoupments, offsets, and takebacks break the ledger

**Who:** Payment posters.
**When:** Whenever a payer claws back a prior payment.
**Currently handled by:** Workarounds. On eClinicalWorks, a question about posting a reversal went 18 months without resolution before someone suggested *"leaving recoupments in unallocated accounts rather than on original reversed claim... and explaining that to billing/accounting is my best suggestion"* ([AAPC](https://www.aapc.com/discuss/threads/ecw-posting-reversal-of-payments.179010/)). On a specific payer's takeback terminology: *"Does anyone understand the terminology that Oscar used in the EOB when doing takebacks. I am seeing the terms refund request, offset, overpayment"* — with claims appearing taken back multiple times ([AAPC](https://www.aapc.com/discuss/threads/eob-with-takebacks-oscar.202817/)).
**Why inadequate:** The offset arrives in a PLB segment on a *later, unrelated* remittance. If it is not linked back to the original claim, the practice cannot tell whether a recoupment was valid, whether it was taken twice, or whether the recoupment window had already expired. Nobody can even state the window: *"I cannot find a consistent answer to this: what is the window in which commercial payors can recoup an overpayment?"* — answers ranged from 180 days to 5 years, state-dependent ([AAPC](https://www.aapc.com/discuss/threads/insurance-recoupment.203359/)).
**Frequency:** Episodic but persistent.
**Cost:** Direct cash loss on invalid or duplicate recoupments; plus reconciliation labor.
**Evidence strength:** Medium-high. Clear practitioner pain; magnitude unquantified.

### P6 — Prior authorization burden, with a structural change now in flight

**Who:** Clinical and front-office staff.
**Currently handled by:** Phone and portal. 45% of practice phone time (MGMA 2026); 24 minutes per phone PA (CAQH).
**Why the appeal side is the leverage point:** In Medicare Advantage, insurers made **52.8 million PA determinations in 2024**, denying **7.7% fully or partially** (up from 6.4% in 2023). Only **11.5% of denials were appealed** — but **80.7% of appeals were partially or fully overturned** ([KFF](https://www.kff.org/medicare/medicare-advantage-insurers-made-nearly-53-million-prior-authorization-determinations-in-2024/)). The AMA reports the same asymmetry and why it persists: **62% of physicians don't appeal because they don't believe it will succeed**, 48% because care can't wait, 48% for lack of staff time ([AMA](https://www.ama-assn.org/practice-management/prior-authorization/over-80-prior-auth-appeals-succeed-why-aren-t-there-more)). **Roughly four in five appealable denials are simply abandoned, and four in five of the ones pursued win.**
**Structural change:** CMS-0057-F is now partially in effect. Since **January 1, 2026**, impacted payers (MA organizations, Medicaid/CHIP FFS and managed care, FFE QHP issuers) must decide expedited PAs in 72 hours and standard in 7 calendar days, **must give a specific reason for denials**, and must publicly report PA metrics annually. On **January 1, 2027**, the Patient Access, Provider Access, Payer-to-Payer, and Prior Authorization FHIR APIs become required ([CMS fact sheet](https://www.cms.gov/newsroom/fact-sheets/cms-interoperability-prior-authorization-final-rule-cms-0057-f)). Commercial/ERISA plans are **not** covered.
**Evidence strength:** Very high on the numbers; medium on whether a small tool can move the needle before 2027.

### P7 — Enrollment and credentialing lapses generate invisible denials

**Who:** Practice owners adding or moving providers.
**Currently handled by:** Nothing systematic at small scale. I found credentialing-tracking tools described only at 150–300 provider organizations; **no 1–10 provider practice described any tracking system**.
**Cost:** **MGMA Stat (Aug 2021, 425 responses): 54% of practices said credentialing-related denials increased that year**, with reported approval timelines up to **100 days**, closed panels, and providers loaded under **incorrect taxonomies** ([MGMA](https://www.mgma.com/mgma-stat/more-than-half-of-practices-report-credentialing-related-denials-on-the-rise-in-2021)). A practitioner account: after a group restructuring, *"it took almost 6 months for the insurances to have our updated TID/group and was a huge financial mess"* with claims denied out-of-network ([AAPC](https://www.aapc.com/discuss/threads/credentialing-company-vs-in-house-credentialing-specialist.193006/)).
**Evidence strength:** High for existence; the specific detection mechanism I propose in §4 is inferential.

### P8 — Single-person key risk

**Who:** Practice owners.
**When:** When the biller leaves.
**Evidence:** An AAPC thread titled *"Biller quit suddenly and has all insurance carrier logins"* — the departed employee exclusively held **all payer portal credentials plus PM system administration**, and the owner's stated concern is the time to re-establish Medicare credentials ([AAPC](https://www.aapc.com/discuss/threads/biller-quit-suddenly-and-has-all-insurance-carrier-logins.194380/)). Related: a new biller arriving at a practice with *"6 figure in old aging balances"* whose first job is auditing whether prior write-offs and patient-responsibility assignments were even legitimate ([Medical Billing Live](https://www.medicalbillinglive.com/members/index.php/topic,8552.0.html)).
**Why it stays unsolved:** It reads as a policy problem, not a software problem, and generic password managers don't model payer-specific enrollment identifiers. **I flag this as a real problem that I do not think justifies a dedicated application** — see §4 exclusions.

### P9 — Single-vendor concentration risk in the transaction path

**Evidence:** After the February 2024 Change Healthcare attack, the AMA surveyed 1,400 practices (1,297 with fewer than 100 physicians, 432 solo): **77% had service disruptions, 80% lost revenue from unpaid claims, 39% could not obtain ERAs, 32% could not submit claims, 55% used personal funds, 31% struggled to make payroll, 48% engaged alternative clearinghouses at higher cost** ([AMA survey, PDF](https://www.ama-assn.org/system/files/change-healthcare-survey-results.pdf)).
**Relevance here:** It establishes that a practice keeping its **own local copy** of its 835/837 history has genuine continuity value independent of analytics — a secondary argument for the ingestion tools proposed below.

---

## 4. Application opportunities

All nine concepts below assume the same deployment model: **a local desktop application or script that runs on the practice's own Windows machine, reads files from a local folder, writes results to a local SQLite database, and never transmits PHI anywhere.** This is not incidental — it is what makes free open-source distribution legally viable in this market. A locally-run tool with no data egress is arguably not a Business Associate arrangement at all, whereas any hosted equivalent requires a signed BAA and a HIPAA Security Rule posture that a solo developer giving software away cannot economically maintain.

---

### O1 — Remit Lens (835 denial analytics)

**Working title:** Remit Lens
**Intended user:** Biller, billing-company owner, or practice administrator at a 1–10 provider practice.
**Problem solved:** P1, P4. Denials are worked one at a time and never aggregated; recurring root causes stay invisible.
**Current workflow:** Post payments in the PM system → notice a lot of denials → optionally hand-tally a spreadsheet over two to three months → guess at the pattern.
**Proposed workflow:** Drop a folder of 835 files (downloaded from the clearinghouse via SFTP or portal) onto the app → it parses every service line, joins CARC/RARC to human-readable text, and produces: denial rate by payer, by CPT, by provider, by CARC; dollars denied and dollars at risk; month-over-month trend; a payer scorecard including average days-to-pay computed from claim dates; and a drill-down list of affected claims exportable to CSV for the work queue.
**Required inputs:** A folder of X12 835 files. Optionally 837 files to compute a true denial *rate* (denials ÷ submitted) rather than a denial share of remitted lines.
**Expected outputs:** An interactive local dashboard, a one-page monthly PDF/HTML summary suitable for showing a physician-owner, and CSV work lists.
**Essential features:** Robust 835 parsing including multiple CAS segments per line, group codes (CO/PR/OA/PI), RARC, and correct handling of reversals/corrections (CLP02 claim status codes). Human-readable CARC/RARC dictionary bundled and updateable. Payer normalization (the same payer arrives under many names and IDs). Zero-configuration first run.
**Deliberately excluded from v1:** Claim submission. Any write-back to the PM system. Patient-level clinical data. Multi-user access control. Cloud sync.
**AI:** **Inappropriate.** This is deterministic parsing and aggregation. Adding a model would introduce nondeterminism into numbers a practice will act on financially, plus an unnecessary PHI egress path.
**Why a spreadsheet won't do:** The input is a nested EDI hierarchy (interchange → functional group → transaction → claim → service line → multiple adjustments per line), not a table. No practitioner is going to reshape that in Excel — which is exactly why the recommended practice is a hand-tallied log rather than a pivot table.
**Complexity:** Medium. The parser is the hard part; the analytics are straightforward once normalized.
**Learning difficulty:** Very low. Drop a folder, read a chart.
**Value:** At MGMA's $25/rework and 44 denials/physician/month, a 3-provider practice is spending roughly **$40,000/year** on rework. Eliminating even one recurring root cause per quarter is measurable. The larger prize is the >50% of denials never reworked at all.
**Risks and constraints:** 835 files contain PHI (patient name, member ID, dates of service) — hence local-only. Payer-specific 835 quirks are the main technical risk; the existing free `edi-835-parser` states plainly that *"not all EDI 835 elements and segments are currently parsable and not all EDI codes are mapped"* ([PyPI](https://pypi.org/project/edi-835-parser)). CARC/RARC lists are free to *read* at [x12.org/codes](https://x12.org/codes) but X12 sells subscription feeds; the HL7 FHIR value sets republish the combined set in JSON as a practical free machine-readable route.
**Existing products:** Waystar, Adonis, Janus, AKASA, Rivet, FinThrive. **Every one is quote-only and enterprise-scoped except Rivet, which starts at $6,000/year** ([Capterra](https://www.capterra.com/p/205843/Rivet/)). MD Clarity's own competitive roundup states of ten underpayment vendors: *"None of the vendors have published pricing"*, with targets listed as hospitals, health systems, and IDNs ([MD Clarity](https://www.mdclarity.com/comparison/best-healthcare-underpayment-detection-software)). OpenEMR ships 835 import and a report builder but has **no built-in denial report** — denial rate and clean-claim rate require manual tallying or export ([CapMinds OpenEMR guide](https://www.capminds.com/blog/the-complete-openemr-billing-rcm-reporting-guide/)).
**Why still attractive:** The price floor is the whole opportunity. Nothing in the commercial market serves a practice below ~$1–2M collections, and the input data is free, standardized, and already in the practice's possession.
**Paid customization potential:** High. Specialty-specific denial taxonomies, payer-specific parsers, branded monthly client reports for billing companies that want to hand a physician-owner a scorecard.

---

### O2 — Allowable Check (payment variance vs. Medicare and contract)

**Working title:** Allowable Check
**Intended user:** Practice owner, billing-company owner, anyone in a contract negotiation.
**Problem solved:** P2. Underpayment is undetected.
**Current workflow:** None. Charges are set as a multiple of Medicare; payments are never systematically compared to what was contracted.
**Proposed workflow:** Load 835s (shares O1's parser) → the tool computes the **Medicare allowable** for each CPT/modifier/place-of-service using the free CMS PFS Relative Value Files (PPRRVU + GPCI + conversion factor) for the practice's locality → user enters each payer's contracted terms as a simple percent-of-Medicare or uploads a fee schedule CSV → tool reports **paid vs. expected** by payer and CPT, flags variances above a threshold, ranks by recoverable dollars, and produces an appeal-ready worklist.
**Required inputs:** 835 files; practice ZIP/locality; per-payer contract terms (a percentage or a CSV fee schedule). CMS files ship with the tool and update annually.
**Expected outputs:** Variance report (by payer, by code, by dollars), a "top 20 recoverable claims" list, and a negotiation-support view — "here is what this payer actually pays you as a percent of Medicare, by code, over the last 12 months."
**Essential features:** Correct PFS math (work/PE/MP RVUs × GPCI × conversion factor, with facility vs. non-facility differentiation and status indicators). Modifier handling for the common payment modifiers (26/TC, 50, 51, 59, 22). A clear "we could not price this code" bucket rather than silent zeros.
**Deliberately excluded:** Full contract-language modeling (carve-outs, stop-loss, per-diems). Facility/institutional claims. Automated appeal submission.
**AI:** **Inappropriate for the calculation.** Optionally useful for a stretch feature — extracting a fee schedule out of a PDF contract exhibit — but the arithmetic must be deterministic.
**Why a spreadsheet won't do:** It partly *could*, for one payer and twenty codes — and that is the honest answer. What a spreadsheet cannot do is join thousands of remitted lines to a 10,000-row RVU file with locality adjustment and modifier logic, repeated monthly.
**Complexity:** Medium. The PFS pricing logic has real edge cases.
**Learning difficulty:** Low to moderate — the user must supply contract terms, which is the adoption friction.
**Value:** Potentially the highest-dollar item in the catalog, and the least measured. Also the strongest negotiating artifact a small practice could own.
**Risks and constraints:** **CPT codes are AMA copyright.** The CMS RVU files carry AMA CPT license terms and any distributed tool must be read carefully against them — ship the CMS files as a user-fetched download rather than bundling descriptors, and display codes without long descriptors. Confirm whether the PFS Look-Up Tool requires a CPT license click-through (I could not verify this from the CMS overview page). CY2026 has, for the first time, **two statutory conversion factors — $33.57 for qualifying APM participants and $33.40 for others**, up from $32.35 in 2025 — so the tool must ask which applies.
**Existing products:** MD Clarity, Waystar Revenue Capture, Experian Contract Manager, FinThrive, Aroris. All quote-only, all hospital/large-group scoped, several gated behind being a customer of the same vendor's clearinghouse. Turquoise Health offers a genuinely free Medicare Pricer (CSV upload) but not payment-variance detection ([Turquoise](https://turquoise.health/plans/providers)).
**Why still attractive:** All inputs are free and public. The commercial category exists precisely because the money is real; nobody has built the version priced for three doctors.
**Paid customization:** Very high — loading and maintaining a specific practice's real contracts is exactly the kind of billable, recurring service work the catalog's business model contemplates.

---

### O3 — Filing Clock (timely filing and appeal deadline tickler)

**Working title:** Filing Clock
**Intended user:** Biller at a small practice or billing company.
**Problem solved:** P3. Deadlines tracked by nothing.
**Current workflow:** Memory. The claim ages; the denial arrives; the money is gone and cannot be billed to the patient.
**Proposed workflow:** Import the PM system's AR aging export (CSV — every system in §2 can produce one) → the tool joins each open claim to a **user-maintained payer rule library** (filing limit in days, what date it runs from — DOS vs. primary EOB date vs. discharge, appeal window, reconsideration window) → produces a work list sorted by *days remaining × dollars at risk*, with a red/amber view and a weekly digest. A parallel register tracks claims under appeal so they don't vanish from view when written off.
**Required inputs:** AR aging CSV; the rule library (ships with a starter set of well-documented public limits, user edits it).
**Expected outputs:** Ranked worklist CSV, a printable "expiring this week" sheet, and an appeal-pending register.
**Essential features:** The date-basis distinction is the whole point — the documented failure was a 95-day limit running from **date of service** rather than primary adjudication. Explicit modeling of secondary-claim clocks. Rule library as a plain editable file (YAML or CSV) so the practice owns and can share it.
**Deliberately excluded:** Any attempt to ship an authoritative national payer-limits database. Filing limits are contract-specific and change; shipping them as fact is a liability. Ship a *starter* file, clearly labeled "verify against your contract."
**AI:** **Inappropriate.** Date arithmetic.
**Why a spreadsheet won't do:** It nearly could — and a well-built spreadsheet is the honest competitor here. The tool wins on re-import (the aging report changes weekly), on the multi-basis date logic, and on not silently breaking when someone drags a formula.
**Complexity:** Small. This is the fastest thing in the catalog to build.
**Learning difficulty:** Very low.
**Value:** Timely filing is ~7% of denials (MGMA) and is a **100% loss** — not recoverable from the payer, not billable to the patient, and not even cleanly classifiable as bad debt (a forum thread on whether it can be written off to bad debt ends with "ask your accountant"). For a practice denying 44 claims/physician/month at an average allowed of $120, 7% is roughly **$4,400/year per physician** of pure preventable loss.
**Risks:** The rule library is only as good as the practice maintains it. Mis-stated limits could create false confidence — the UI must make provenance and last-verified date visible per rule.
**Existing products:** None found at this price point. Vendor content on timely filing limits is abundant; tooling is absent.
**Paid customization:** Moderate — loading a specific practice's actual contract limits.

---

### O4 — Ack Triage (999 / 277CA rejection reader)

**Working title:** Ack Triage
**Intended user:** Biller.
**Problem solved:** Claims rejected at the clearinghouse or payer front door never become claims, never enter AR, and are invisible unless someone opens a cryptic report.
**Current workflow:** Log into the clearinghouse portal, read a rejection list written in EDI error language, guess at the fix. Practitioner evidence: *"All my claims are rejected for Insurance Type"* with no diagnostic path.
**Proposed workflow:** Drop 999 and 277CA files in → tool renders each rejection as plain English with the offending loop/segment/element identified, groups rejections by cause, and produces a fix-list ranked by count and dollars.
**Required inputs:** 999 and 277CA files (and the corresponding 837 for context).
**Expected outputs:** Human-readable rejection worklist; a recurring-cause summary (the "you have submitted 41 claims this month with the same missing referring-provider NPI" view).
**Essential features:** Mapping of X12 syntax error codes and Claim Status Category/Status codes to plain language; segment/element pointer resolution back into the original 837 so the user sees the actual bad value.
**Deliberately excluded:** Fixing and resubmitting. Read-only diagnosis in v1.
**AI:** **Inappropriate.** Deterministic code-list translation.
**Why a spreadsheet won't do:** The input is EDI, not tabular.
**Complexity:** Small to medium. Shares infrastructure with O1.
**Learning difficulty:** Very low.
**Value:** Front-door rejections are the cheapest denials to fix and the easiest to miss, because they never age into an AR report.
**Risks:** Requires the practice to be able to download raw acknowledgment files — Office Ally offers SFTP and Claim.MD returns X12, so this is achievable but not universal.
**Existing products:** Stedi's free browser-based EDI Inspector renders X12 generically ([Stedi](https://www.stedi.com/edi/inspector)) but is a developer tool, not a biller worklist, and requires pasting data into a website — a non-starter for PHI.
**Paid customization:** Low to moderate.

---

### O5 — Offset Ledger (PLB recoupment and takeback register)

**Working title:** Offset Ledger
**Intended user:** Payment poster; billing-company owner reconciling a client's deposits.
**Problem solved:** P5. Recoupments arrive in a PLB segment on an unrelated later remittance and get lost.
**Current workflow:** Park it in an unallocated account and explain it to accounting — the literal advice given on a forum thread that went 18 months unanswered.
**Proposed workflow:** Parse PLB segments across all 835s → build a register of every provider-level adjustment with its reason code, amount, and the referenced original claim → reconcile each 835's total payment against the sum of its claim payments plus PLB adjustments → flag: recoupments with no matching original claim, the same claim recouped twice, and recoupments taken beyond a user-configured lookback window.
**Required inputs:** 835 files (shares O1's parser).
**Expected outputs:** Offset register CSV; an exception list of suspicious recoupments; an EFT-to-835 reconciliation summary.
**Essential features:** Full PLB reason-code handling (WO, FB, L6, CS, 72, and the rest); linkage from the PLB reference identifier back to the original claim across files.
**Deliberately excluded:** Determining whether a recoupment is *legally* valid — that is state-law dependent and the practitioner evidence shows even experts disagree (180 days to 5 years). The tool surfaces facts and a configurable threshold; it does not opine.
**AI:** **Inappropriate.**
**Why a spreadsheet won't do:** Cross-file claim linkage.
**Complexity:** Small, given O1's parser exists.
**Learning difficulty:** Very low.
**Value:** Direct cash. Duplicate and time-barred recoupments are pure recovery.
**Risks:** Low. Read-only.
**Existing products:** None found for small practices. This is the most differentiated concept in the list — I found no product, free or paid, that markets PLB-level offset reconciliation to a small practice.
**Paid customization:** Moderate.

---

### O6 — Appeal Kit (CARC-keyed appeal packet builder)

**Working title:** Appeal Kit
**Intended user:** Biller writing appeals.
**Problem solved:** P4 and P6. Appeal letters are rebuilt from scratch each time; four in five appealable denials are abandoned, and four in five pursued are won.
**Current workflow:** *"I constantly modify our appeal letters based on the patient's policy vs. provider/hospital contracts, state vs. federal laws, CMS policy manuals, LCD, and NCDs."*
**Proposed workflow:** Select a denied claim (from O1's output or a CSV) → the tool matches the CARC/RARC and payer to a **template library** → merges claim facts (dates, codes, amounts, provider, member ID) → produces a formatted letter plus an evidence checklist ("attach: op note, prior auth number, LCD L#####, proof of timely filing") → logs the appeal in a register with the deadline (feeding O3).
**Required inputs:** Denied-claim detail; a template library; practice letterhead details.
**Expected outputs:** DOCX or PDF appeal letter; evidence checklist; register entry.
**Essential features:** Template library as plain editable files under version control, so a practice's institutional appeal knowledge stops living in one person's head (addresses P8 obliquely without pretending to be a knowledge-management platform). Merge-field validation so no letter goes out with an unfilled placeholder.
**AI:** **Optional and genuinely useful — the one place in this catalog where it earns its keep.** Drafting the medical-necessity narrative paragraph from a pasted clinical note is exactly the interpretation-and-drafting task conventional code cannot do. It must be strictly opt-in, must default to off, must run against a local model or a BAA-covered endpoint, and must never be the source of any code, date, or dollar amount — those come from the deterministic merge. Without AI the tool is still fully useful; with AI it is faster.
**Why a spreadsheet won't do:** Document generation.
**Complexity:** Small to medium.
**Learning difficulty:** Low.
**Value:** The AMA/KFF asymmetry is the entire business case: **80.7% of appealed MA prior-auth denials were overturned in 2024, and only 11.5% were appealed.** Reducing the per-appeal cost changes the calculus for the 48% of physicians who cite staff time as the reason they don't appeal.
**Risks:** Templates that assert law or policy incorrectly are a liability. Ship templates as user-owned content with clear disclaimers, not as legal advice. Any AI drafting path must be off by default and PHI-aware.
**Existing products:** Appeal-letter generators exist inside enterprise RCM suites and as ad-hoc web tools; nothing free, local, and CARC-keyed that I could verify.
**Paid customization:** **Highest in the catalog.** A practice's appeal template library, tuned to its specialty and its top five payers, is a recurring, defensible service engagement.

---

### O7 — PreFlight (NCCI/MUE and claim-data validator)

**Working title:** PreFlight
**Intended user:** Biller/coder before submission.
**Problem solved:** Preventable front-end denials — MGMA's poll attributes 29% of denials to demographic issues and 23% of the "other" bucket to coding issues such as wrong modifier and improper CPT bundling.
**Current workflow:** Rely on whatever the PM system's scrubber catches, which varies enormously by vendor and tier.
**Proposed workflow:** Load a charge batch (837P file or CSV export) → run CMS **NCCI Procedure-to-Procedure edits** and **Medically Unlikely Edits**, plus structural checks (missing referring NPI when required, invalid POS/CPT combinations, units exceeding MUE, diagnosis pointer sanity, subscriber vs. patient mismatch) → return a pass/flag list before the batch goes out.
**Required inputs:** 837P or charge CSV; CMS NCCI files (free, quarterly ZIPs — the hospital PTP file alone contains 475,091 records).
**Expected outputs:** Flagged-claim list with the specific edit violated and the modifier that would (or would not) override it.
**Essential features:** Correct PTP modifier-indicator logic (0 = no override permitted, 1 = override allowed with an appropriate modifier, 9 = not applicable). Quarterly edit-file update workflow with a visible "your edits are from Q3 2026" banner.
**Deliberately excluded:** Payer-proprietary edits (which are the majority of commercial denials and are not published). Do not claim to replace a clearinghouse scrubber.
**AI:** **Inappropriate.** Rule tables.
**Why a spreadsheet won't do:** Half a million edit pairs.
**Complexity:** Medium.
**Learning difficulty:** Low.
**Value:** Prevention is worth roughly $25 per avoided rework plus the >50% never-reworked loss.
**Risks:** **Some MUE values are confidential and not published by CMS** — the tool must say so rather than implying full coverage. NCCI applies to Medicare and most Medicaid programs; commercial payers vary.
**Existing products:** This is the most crowded concept in the list — every clearinghouse and PM scrubber does some version. **The differentiator is narrow: it runs on a practice's own data, offline, before submission, at zero cost, and it explains *why*.** I score it lower for differentiation accordingly and would build it only after O1/O2.
**Paid customization:** Moderate — practice-specific and payer-specific rule additions.

---

### O8 — Enrollment Gap Detector

**Working title:** Enrollment Gap Detector
**Intended user:** Practice administrator, billing-company owner onboarding a new provider.
**Problem solved:** P7. Enrollment lapses generate months of denials before anyone connects the pattern to credentialing.
**Current workflow:** Denials accumulate; someone eventually notices they all involve one provider or one payer; six months of AR is already at risk.
**Proposed workflow:** Runs on top of O1's parsed 835 data. Maintains a small register of provider × payer enrollment records (effective date, PTAN/group ID, revalidation due, CAQH attestation date). Cross-references denials carrying enrollment-related CARC/RARC codes against that register and raises an alert the *first week* a pattern appears rather than the sixth month. Also flags upcoming revalidation and CAQH re-attestation dates.
**Required inputs:** 835 data; a manually maintained enrollment register.
**Expected outputs:** Alert list; a provider × payer enrollment matrix; upcoming-deadline view.
**Essential features:** The CARC/RARC-to-enrollment-cause mapping is the intellectual content — knowing which codes actually indicate a provider-not-on-file, wrong-taxonomy, or terminated-contract problem.
**Deliberately excluded:** Credentialing application workflow, CAQH integration, document collection. Those are a different (and crowded) product category.
**AI:** **Inappropriate.**
**Why a spreadsheet won't do:** The register alone is a spreadsheet; the value is the automatic join to denial data.
**Complexity:** Small, given O1.
**Learning difficulty:** Low, but requires the register be populated — real adoption friction.
**Value:** MGMA cites (via Merritt Hawkins, which I did not independently verify) **$10,122 per day** of delayed provider onboarding. Even at a fraction of that, catching a six-month enrollment gap in week two is large.
**Risks:** The CARC-to-cause mapping is inferential and needs practitioner validation before it can be trusted.
**Existing products:** Credentialing platforms (CredyApp, Modio, Medallion, Verifiable) manage applications; none that I found detect enrollment problems from remittance data.
**Paid customization:** Moderate.

---

### O9 — Scrub & Share (X12 de-identifier and synthetic file generator)

**Working title:** Scrub & Share
**Intended user:** Billing-company owners, consultants, and any developer building the other eight tools.
**Problem solved:** A practice cannot send a real 835 to a consultant, a vendor, a forum, or a developer for troubleshooting without transmitting PHI — so troubleshooting happens by description rather than by file. This is a direct, verifiable blocker: the forum evidence in §3 is full of people describing file problems in prose because they cannot show the file.
**Current workflow:** Screenshots with redaction boxes, or nothing.
**Proposed workflow:** Point at an 835/837 → the tool replaces the 18 HIPAA identifiers (names, member IDs, account numbers, dates shifted by a consistent per-patient offset, addresses, NPIs optionally) with realistic surrogates while preserving EDI structure, code values, and dollar amounts → outputs a shareable file plus a mapping key that stays local. A second mode generates synthetic 835s from scratch for testing.
**Required inputs:** A real 835/837, or a specification for synthetic generation.
**Expected outputs:** De-identified X12 file; local-only re-identification key; validation report confirming no residual identifiers.
**Essential features:** Structure-preserving substitution (so the file still parses). Consistent date-shifting so day-count arithmetic survives. An explicit residual-identifier scan — the tool's credibility depends on being able to prove it worked.
**Deliberately excluded:** Any claim of Safe Harbor or Expert Determination certification. The tool assists de-identification; it does not certify it, and the documentation must say so unambiguously.
**AI:** **Inappropriate** for substitution (deterministic), though free-text remark fields are the one place where detection is genuinely hard and where a local NER model could add value in a later version.
**Why a spreadsheet won't do:** EDI structure.
**Complexity:** Small.
**Learning difficulty:** Very low.
**Value:** Indirect but structural — it unlocks the entire rest of the catalog's testing, support, and community-contribution loop. It is also the tool most likely to earn goodwill and inbound users among developers, which matters for an open-source distribution strategy.
**Risks:** **The most important risk in this list.** A de-identification tool that misses an identifier creates the exact harm it claims to prevent. Conservative defaults, a loud residual scan, and honest documentation are mandatory.
**Existing products:** Commercial EDI de-identification services exist; open-source PHI de-identification tools target clinical free text, not X12.
**Paid customization:** Low. This is a credibility and ecosystem play, not a revenue play.

---

### Deliberately not recommended

- **A biller-continuity / credential-vault application (P8).** Real problem, wrong solution shape — this is a password manager plus a policy, and building a healthcare-specific one duplicates mature, inexpensive tools without meaningful advantage.
- **A prior-authorization submission portal.** CMS-0057-F's Prior Authorization API arrives January 1, 2027 for government-sponsored plans; building a pre-standard workflow now means building something with an expiry date. Revisit after the APIs are live.
- **A general practice-management or EHR system.** Explicitly excluded by the brief and by common sense; OpenEMR already occupies the free end.
- **An AI denial-prediction engine.** The adoption data reads as hype: the 2025 Smarter Technologies / Modern Healthcare survey found 57% "implemented some AI in RCM" but **49% dedicate under 10% of tech budget to it** and **34% cite insufficient ROI demonstration** as a barrier ([BusinessWire](https://www.businesswire.com/news/home/20251007979563/en/Smarter-Technologies-and-Modern-Healthcare-Release-Inaugural-2025-AI-in-RCM-National-Survey-Results)). Small practices need to *count* their denials before they need to predict them.

---

## 5. Opportunity ranking

Each concept scored 1–5 on ten criteria. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of impl. | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **O1** | **Remit Lens** (835 denial analytics) | 5 | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 5 | **45** |
| **O2** | **Allowable Check** (payment variance) | 5 | 4 | 5 | 4 | 3 | 4 | 5 | 5 | 4 | 4 | **43** |
| **O3** | **Filing Clock** (deadline tickler) | 4 | 5 | 4 | 5 | 5 | 5 | 4 | 4 | 3 | 4 | **43** |
| **O5** | **Offset Ledger** (PLB recoupments) | 4 | 3 | 4 | 5 | 4 | 5 | 5 | 3 | 3 | 4 | **40** |
| **O4** | **Ack Triage** (999/277CA reader) | 4 | 5 | 4 | 5 | 4 | 5 | 3 | 3 | 3 | 4 | **40** |
| **O6** | **Appeal Kit** (CARC-keyed packets) | 4 | 4 | 4 | 4 | 4 | 3 | 3 | 5 | 3 | 4 | **38** |
| **O8** | **Enrollment Gap Detector** | 4 | 3 | 4 | 5 | 4 | 4 | 4 | 4 | 3 | 3 | **38** |
| **O9** | **Scrub & Share** (X12 de-identifier) | 3 | 2 | 3 | 5 | 4 | 5 | 4 | 2 | 5 | 4 | **37** |
| **O7** | **PreFlight** (NCCI/MUE validator) | 4 | 5 | 4 | 4 | 3 | 3 | 2 | 3 | 4 | 4 | **36** |

### The top three

**O1 — Remit Lens (45).** It scores highest because it is the only concept where every criterion is at least a 4. The problem is universal and continuous, the evidence is the strongest in the report (the *recommended best practice* in the professional literature is a hand-tallied spreadsheet, which is a direct admission that no tool exists at this price), the input is a standardized file the practice already owns, and the output is immediately legible to a physician-owner who has never thought about denial rates. Critically, **it is the platform**: O2, O5, O8 and half of O6 are features layered on its parser. Build order should follow that dependency.

**O2 — Allowable Check (43).** The highest-value concept and the highest-uncertainty one. It scores 5 on differentiation because the entire commercial category is explicitly hospital-scoped and quote-only, and 5 on customization because loading a practice's real contracts is exactly the recurring paid service the catalog's model wants. It loses points on implementation (PFS pricing has real edge cases, and the AMA CPT licensing question is unresolved) and on evidence confidence — I have strong evidence that small practices *don't check* for underpayment, and no evidence of how much money is actually there. That gap is the first thing validation must close.

**O3 — Filing Clock (43).** Ties O2 on total with an opposite risk profile: lower ceiling, near-certain floor. It is the smallest build in the catalog, the easiest to learn, the most narrowly scoped, and it addresses a loss that is 100% unrecoverable — you cannot appeal it, cannot bill the patient, and cannot cleanly write it off. Its only weakness is that a determined Excel user could approximate it, which is why it scores 4 rather than 5 on differentiation.

### What to investigate next

**Build O1 first and O3 alongside it.** O3 requires none of O1's infrastructure and can ship in a fraction of the time, which gives something to put in practitioners' hands while the 835 parser hardens. Then O5 and O4, which are cheap once the parser exists. **O2 is the prize but should not be built until the validation in §6 confirms the dollars are real and the CPT licensing path is clear.** O9 should be built early and quietly, because without it there is no safe way to collect the real-world test files the other eight tools need.

---

## 6. Validation plan

### Questions to ask practitioners

**For O1 (Remit Lens):**
1. Can you download your raw 835 files today — from your clearinghouse, your PM system, or neither? How? (This is the single largest adoption gate. If the answer is "neither," the concept dies.)
2. Do you know your denial rate this month? Where would you look? How long would it take?
3. When you last found a recurring denial pattern, how did you find it, and how long had it been running?
4. What would you do differently if a report told you Payer X denies CPT Y 40% of the time?

**For O2 (Allowable Check):**
5. Do you have a written fee schedule from each of your top five payers? In what format — PDF, spreadsheet, portal-only, or "we never got one"?
6. Have you ever found a payer paying below your contracted rate? How did you find it? What happened when you challenged it?
7. If a tool told you a payer underpaid you $8,000 last year, what would you actually do with that?

**For O3 (Filing Clock):**
8. How many timely-filing write-offs did you take last year? Do you know? Where is that number?
9. When a secondary claim is involved, what date does the clock run from for your top payers — do you know per payer, or do you assume?
10. How do you keep track of a claim once it's under appeal?

**General:**
11. If a free tool ran entirely on your own computer and sent nothing anywhere, would that satisfy your privacy officer / your own comfort? What would you need to see to believe it?
12. Who decides to install new software on your machines?

### Who to interview

- **Owners of 1–15 person independent billing companies.** The highest-information counterparty: they see many practices, they buy their own tools, and the Medical Billing Live forum shows they discuss tooling openly and in detail. Recruit there and through AAPC local chapters.
- **AAPC local chapter officers and CPC-credentialed billers** at small practices — reachable through chapter meetings, which are explicitly designed for this.
- **Practice administrators at 3–8 provider single-specialty groups** in high-denial specialties (behavioral health, physical therapy, DME-adjacent, allergy/immunology).
- **Clearinghouse support staff at Office Ally and Claim.MD** — they know exactly which customers can and cannot retrieve raw files, and both companies serve the low end.
- **One healthcare privacy attorney or compliance consultant**, on the single question of whether a locally-run, no-egress tool distributed free creates a Business Associate relationship. This is a gating legal question, not a nice-to-have.

### Search terms for further research

`835 ERA download SFTP [clearinghouse name]` · `"denial rate" small practice benchmark specialty` · `"underpayment" appeal commercial payer small practice` · `CPT license "distribute" software CMS RVU file terms` · `X12 CARC list machine readable free bulk` · `"timely filing" appeal overturned "date of service" secondary` · `PLB segment recoupment posting [PM system]` · `NCCI MUE confidential values` · `CMS-0057-F Provider Access API provider implementation 2027` · `HIPAA business associate "locally installed" software no transmission`

### Sample files and data needed for testing

- **Real (de-identified) 835 files from at least six distinct payers** — Medicare, a Medicare Advantage plan, a Blues plan, a national commercial, a state Medicaid, and a small regional plan. Payer-specific 835 variance is the primary technical risk and cannot be assessed from the specification.
- **Matching 837P files** for the same claims, to test claim-to-remit linkage and compute true denial rates.
- **999 and 277CA acknowledgment files** including real rejections.
- **At least two real (de-identified) payer fee schedules** in whatever format practices actually receive them.
- **A real AR aging export** from each of Tebra, AdvancedMD, eClinicalWorks, and Office Ally, to establish how much CSV normalization O3 requires.
- **CMS PPRRVU, GPCI, and NCCI quarterly files** — free, but must be tested for parsing stability across releases.

Building **O9 first** is the practical way to obtain the first four items legally.

### A prototype that would validate the idea

A single Python script, run once against one practice's folder of 835s, that outputs one page: denial rate, top ten CARC codes by dollars, top five payer × CPT denial combinations, and total dollars denied. No UI, no installer, no configuration. Sit with three billers while it runs and watch what they point at. If they do not immediately name a claim they want to go work, the concept is wrong. This is a two-day build against the existing free `edi-835-parser` and it de-risks the entire catalog.

For O2, the parallel prototype is narrower: take one payer, one practice, twelve months of 835s, and one contracted percent-of-Medicare, and answer a single question — **is there any money there at all?** If the variance is under a few hundred dollars a year, O2 is dead regardless of how good the software would be.

### Assumptions most likely to make this fail

1. **That small practices can obtain their own raw 835 files.** If most are locked inside a PM system's auto-posting with no export path, the entire remittance-based half of the catalog collapses. Office Ally's SFTP and Claim.MD's X12 return prove it is *possible*; nothing proves it is *typical*.
2. **That underpayment at 3-provider scale is materially large.** Assumed, not demonstrated. Entirely untested.
3. **That "free and local" overcomes healthcare's software-procurement caution.** Practices are trained to ask for a BAA and a SOC 2 report reflexively. A gift with no vendor behind it may read as a risk rather than a bargain.
4. **That the AMA's CPT copyright does not block distribution.** Unresolved. If shipping code descriptors or the RVU files is restricted, O2 and O7 need redesign around user-supplied files.
5. **That payer-specific 835 variation is manageable.** The one mature free parser explicitly warns it does not handle everything. If each payer needs bespoke handling, the maintenance burden may exceed a solo developer's capacity.
6. **That the person with the pain has the authority to install software.** In a practice with outsourced IT and a locked-down workstation image, they may not.

---

## 7. Cross-industry patterns

**Pattern A — "The mandated transaction file is free, standardized, and nobody reads it."**
Where a regulator or industry body mandates a machine-readable exchange format, every party holds a rich structured dataset about its own business and almost nobody analyzes it, because the incumbent software presents only a rendered view. Here it is X12 835/837. *Transfers to:* **Third-party truck dispatch services** and **Small motor carriers (5-50 trucks)** (EDI 210/214/990 and factoring submission files), **Independent pharmacy third-party reconciliation** (NCPDP), **Dental billing and insurance coordination** (837D/835 with far lower electronic adoption — CAQH shows dental claim payment at only 33% electronic vs. 78% medical), **Workers' compensation medical billing** (state-mandated e-billing formats), and **Environmental laboratories producing regulator EDD deliverables**.

**Pattern B — "A free public rate table turns 'did I get paid right?' into arithmetic."**
When an authoritative public schedule exists (CMS Physician Fee Schedule RVU/GPCI/conversion factor files), variance detection against actual payments becomes a deterministic join rather than a judgment call — and the commercial products that do this sell only to large organizations. *Transfers to:* **Freight bill audit for small shippers** (published tariffs and contracted rate tables), **Premium audit and payroll classification consulting** (NCCI class-code rate tables), **Property tax consulting and assessment appeal firms** (assessor rolls and comparable sales), **Asphalt plant producer QC** (DOT pay-factor schedules), and **Ready-mix concrete producer QC** (bid item unit prices).

**Pattern C — "Deadline arithmetic from a user-owned rule library."**
Where the deadline varies by counterparty and by which event starts the clock, and where missing it is a total loss, a small tool that joins a work list to an editable rules file beats both memory and a spreadsheet. Ship a starter library, never claim it is authoritative. *Transfers to:* **Property tax consulting and assessment appeal firms** (county-by-county appeal windows), **Multi-state charitable solicitation registration compliance** (~40 state renewal calendars), **Cargo claims and OS&D handling** (49 CFR 370 windows), **Building permit expediting and code consulting** (AHJ resubmittal clocks), and **Small-firm litigation support** (jurisdictional filing deadlines).

**Pattern D — "Acknowledgment-file triage: the rejection that never became a record."**
Submissions rejected at the gate never enter the system of record, never age into a report, and are therefore invisible unless someone actively opens a cryptic acknowledgment. *Transfers to:* **Environmental laboratories producing regulator EDD deliverables** (EQuIS and state format validators), **Building permit expediting** (portal intake rejections), **Fire alarm and sprinkler AHJ submittals** (already in the catalog as the "checklist-as-data" pattern from the gatekeeper cycle — this is its acknowledgment-file sibling), and **Freight factoring client onboarding desks**.

**Pattern E — "De-identify so you can ask for help."**
In any regulated market, the practitioner with a broken file cannot show the file to the person who could fix it. A structure-preserving redaction tool is low-glamour infrastructure that unlocks community troubleshooting, vendor support, and developer testing for every other tool in the market. *Transfers to:* **Federally qualified health centers**, **Third-party claims administration (TPA)**, **Small defense suppliers navigating CMMC Level 2** (CUI rather than PHI, same shape), **Title abstracting**, and **Small CPA tax preparation practices**.

**Pattern F — "The appeal asymmetry."**
Where an automated adversary denies at scale and a manual practitioner appeals one at a time, the appeal win rate is high and the appeal rate is low — because per-appeal cost, not merit, determines whether anyone bothers. Any tool that drops the marginal cost of a well-formed challenge attacks a documented 5:1 gap. Here: 80.7% of appealed MA prior-auth denials overturned, 11.5% appealed. *Transfers to:* **Independent property and casualty claims adjusting**, **Tenant-side lease audit**, **Property tax appeal firms**, **Cargo claims and OS&D**, and **Premium audit disputes**.

---

## 8. Sources and confidence

### Verified findings — primary or authoritative sources, directly retrieved

| Finding | Source |
|---|---|
| 47.4% of physicians in practices ≤10; 11.9% solo; 42.2% physician-owned (2024) | [AMA Physician Practice Benchmark Survey / PRP 2024 (PDF)](https://www.ama-assn.org/system/files/2024-prp-pp-characteristics.pdf) |
| ACA marketplace: 19% in-network denial rate (range 3%–36%); 36% of denial reasons coded "Other," 25% "administrative"; fewer than 1% of denials appealed; 66% of appeals upheld | [KFF, Claims Denials and Appeals in ACA Marketplace Plans in 2024](https://www.kff.org/patient-consumer-protections/claims-denials-and-appeals-in-aca-marketplace-plans-in-2024/) |
| Medicare Advantage: 52.8M PA determinations in 2024; 7.7% denied; 11.5% of denials appealed; 80.7% of appeals overturned; insurer denial range 4.2%–12.8% | [KFF, MA Prior Authorization 2024](https://www.kff.org/medicare/medicare-advantage-insurers-made-nearly-53-million-prior-authorization-determinations-in-2024/) |
| 62% of physicians don't appeal due to expected futility; 48% staff time; 12–13 hrs/week on PA; 35–40% have PA-dedicated staff | [AMA, "Over 80% of prior auth appeals succeed"](https://www.ama-assn.org/practice-management/prior-authorization/over-80-prior-auth-appeals-succeed-why-aren-t-there-more) |
| ~$25 to rework a denied claim; >50% of denied claims never reworked; $13,200/physician/year example | [AAFP Family Practice Management, "The Cure for Claims Denials"](https://www.aafp.org/fpm/2015/0300/p7) |
| ~$25 rework; "as many as 60% of returned claims are never resubmitted" | [Physicians Practice](https://www.physicianspractice.com/view/why-getting-claims-right-first-time-cheaper-reworking-them) |
| Denial sources: 42% prior auth, 29% demographic, 7% timely filing (Dec 2020, 619 responses) | [MGMA Stat](https://www.mgma.com/mgma-stat/mgma-stats/finding-hidden-treasure-by-uncovering-and-fixing-the-sources-of-claim-denials) |
| 45% of practice phone time on eligibility/prior auth (Mar 2026, 294 responses) | [MGMA Stat](https://www.mgma.com/mgma-stat/phones-are-still-a-backlog-costing-medical-practices-time) |
| 54% of practices report credentialing-related denials rising; approvals up to 100 days (Aug 2021, 425 responses) | [MGMA Stat](https://www.mgma.com/mgma-stat/more-than-half-of-practices-report-credentialing-related-denials-on-the-rise-in-2021) |
| Per-transaction provider costs: PA $12.88/$8.93/$5.38 (24 min phone); eligibility $8.57/$4.46/$2.00; claim status $13.80/$5.24/$3.64 (25 min phone); remittance $5.67/$5.31/$2.95 | [CAQH Index 2024 (PDF)](https://www.caqh.org/hubfs/Index/2024%20Index%20Report/CAQH_IndexReport_2024_FINAL.pdf) |
| CAQH 2025: $20B remaining savings opportunity; ePA adoption 40%; claim status 81%; medical claim payment 78%; dental claim payment 33% | [AJMC on CAQH Index](https://www.ajmc.com/view/caqh-index-finds-20-billion-in-cost-savings-opportunities) |
| Experian State of Claims 2025: 41% report ≥1 in 10 claims denied; 54% say denials increasing; only 14% use AI; 56% say current tech adequate (down from 77% in 2022) | [Experian Health](https://www.experian.com/blogs/healthcare/healthcare-claim-denials-statistics-state-of-claims-report/) |
| Change Healthcare outage: 77% disrupted, 80% lost revenue, 39% could not obtain ERAs, 31% struggled with payroll (1,400 practices) | [AMA survey (PDF)](https://www.ama-assn.org/system/files/change-healthcare-survey-results.pdf) |
| CMS-0057-F: 72hr/7-day PA decisions and specific denial reasons effective Jan 1 2026; four FHIR APIs effective Jan 1 2027; commercial/ERISA excluded | [CMS fact sheet](https://www.cms.gov/newsroom/fact-sheets/cms-interoperability-prior-authorization-final-rule-cms-0057-f) |
| CMS PFS Relative Value Files free and machine-readable; CY2026 conversion factors $33.57 (QP) / $33.40 (non-QP) vs $32.35 in 2025 | [CMS PFS RVU files](https://www.cms.gov/medicare/payment/fee-schedules/physician/pfs-relative-value-files) |
| NCCI PTP and MUE files free, quarterly; one hospital PTP file = 475,091 records; some MUE values confidential | [CMS NCCI PTP](https://www.cms.gov/medicare/coding-billing/national-correct-coding-initiative-ncci-edits/medicare-ncci-procedure-procedure-ptp-edits) · [CMS NCCI MUE](https://www.cms.gov/medicare/coding-billing/national-correct-coding-initiative-ncci-edits/medicare-ncci-medically-unlikely-edits-mues) |
| CARC list free to view (139 codes, reviewed 8/1/2026); no free bulk download; FHIR value sets republish in JSON | [X12 codes](https://x12.org/codes/claim-adjustment-reason-codes) · [HL7 CARIN BB value set](https://build.fhir.org/ig/HL7/carin-bb/ValueSet-X12ClaimAdjustmentReasonCodesCMSRemittanceAdviceRemarkCodes.json.html) |
| Rivet published at $6,000/year; all other underpayment vendors quote-only and hospital-scoped | [Capterra](https://www.capterra.com/p/205843/Rivet/) · [MD Clarity comparison](https://www.mdclarity.com/comparison/best-healthcare-underpayment-detection-software) |
| Claim.MD published pricing $30/$60/$120 per month; Office Ally Practice Mate free with SFTP batch access | [Claim.MD pricing](https://www.claim.md/pricing.html) · [Office Ally pricing](https://cms.officeally.com/pricing) |
| eClinicalWorks $449–599/provider/month, RCM 2.9% of collections; AdvancedMD $429–1,070/provider/month, RCM 4–8% | [eCW pricing](https://www.eclinicalworks.com/products-services/pricing/) · [AdvancedMD pricing](https://www.advancedmd.com/software-pricing/) |
| OpenEMR imports/auto-posts 835 but has **no built-in denial report** | [CapMinds OpenEMR billing/RCM guide](https://www.capminds.com/blog/the-complete-openemr-billing-rcm-reporting-guide/) |
| `edi-835-parser` (MIT, PyPI) states not all 835 segments parsable, not all codes mapped | [PyPI](https://pypi.org/project/edi-835-parser) |
| pyx12 — maintained HIPAA X12 parser/validator, 4010 and 5010 | [GitHub](https://github.com/azoner/pyx12) |
| AI-in-RCM survey: 57% implemented, 49% under 10% of tech budget, 34% cite insufficient ROI | [BusinessWire](https://www.businesswire.com/news/home/20251007979563/en/Smarter-Technologies-and-Modern-Healthcare-Release-Inaugural-2025-AI-in-RCM-National-Survey-Results) |

### Verified practitioner evidence — direct quotes from named professional forums

All quotations in §2 and §3 are from two sources, both populated by credentialed coders/billers and independent billing-service owners rather than vendor marketing:

- **AAPC discussion forums** — [aapc.com/discuss](https://www.aapc.com/discuss/) (auto-write-off of denials, CO-45/PR-45 confusion, eCW recoupment posting, Oscar takeback terminology, timely filing failure modes, Office Ally limitations, credentialing gaps, "Biller quit suddenly and has all insurance carrier logins," appeal-letter construction, EMRs not designed for coders)
- **Medical Billing Live member forum** — [medicalbillinglive.com](https://www.medicalbillinglive.com/members/) (Kareo/NueMD/HealthFusion auto-posting behavior, $499 ERA module, ERA reader question with no answers, AR recovery worked "off of reports," fee schedules set as multiples of Medicare, Horizon BCBS underpayment case, "no way to look that information up yourself," COB calculation methods, LogMeIn access costs, billing-company software cost structures)
- **AAPC Knowledge Center** — [the "one simple spreadsheet" denial tracking log](https://www.aapc.com/blog/10034-streamline-your-denials-with-one-simple-spreadsheet/), the single most important artifact in this report: the profession's own published best practice for denial analysis is a hand-tallied grid.

### Strong inferences — well-supported but not directly stated by a practitioner

- **That a local, no-egress tool is the correct architecture for this market.** Follows from HIPAA structure and from the observed procurement caution, but I did not find a practitioner or attorney stating it.
- **That small billing companies are the best initial buyers.** Follows from their tool-purchasing behavior and margin structure, visible in forum discussions of software cost per claim, but not directly asserted.
- **That O1's parser is the platform for O2, O5, and O8.** An engineering judgment.
- **That CARC/RARC patterns can reliably detect enrollment gaps (O8).** Plausible from the code semantics; unvalidated against real data.
- **That small practices can generally retrieve raw 835s.** Proven possible (Office Ally SFTP, Claim.MD X12) but not proven typical. **This is the highest-leverage unknown in the report.**

### Tentative hypotheses requiring practitioner validation

- **The magnitude of underpayment at 1–10 provider scale is unknown.** O2's entire business case rests on it. No source I found measures it below hospital scale.
- **That a free tool will be adopted at all** in a market conditioned to demand BAAs and vendor accountability.
- **That AMA CPT licensing permits distributing a tool that consumes CMS RVU files.** Unresolved; could force redesign of O2 and O7.
- **The MGMA-cited $10,122/day onboarding-delay figure** traces to a 2019 Merritt Hawkins survey that was not independently retrieved.
- **Whether payer-specific 835 variance is manageable by one developer.** The single largest technical risk.

### Sources I could not reach

Reddit (r/medicalbilling, r/CodingandBilling, r/therapists, r/physicaltherapy, r/privatepractice) returned 403 to all retrieval attempts, as did Indeed, G2, Capterra, TrustRadius, Physicians Practice's archive, and Becker's. **The clinician-owner voice is therefore largely absent from this report** — the practitioner evidence skews toward certified coders and independent billing-service owners. Forum threads from Medical Billing Live cluster 2008–2020, so software-specific complaints (NueMD, HealthFusion, Medisoft) may be dated; the MGMA, CAQH, KFF, AMA, and CMS data are 2021–2026. Several AAPC threads rendered only their opening post, so where I noted "no replies" it may mean replies were not retrieved.

---

*Report produced 2026-08-06 · claim `790d3912` · market: Medical billing and revenue cycle for small practices · angle: core-practitioner-workflow*
