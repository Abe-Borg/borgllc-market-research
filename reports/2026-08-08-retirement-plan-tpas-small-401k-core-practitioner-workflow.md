# Retirement Plan Third-Party Administrators (TPAs) for Small 401(k) Plans
## Angle: Core Practitioner Workflow

---

## 0. Cycle Header

| Field | Value |
|---|---|
| **Market** | Retirement plan third-party administrators (TPAs) for small 401(k) plans |
| **Angle** | core-practitioner-workflow |
| **Claim ID** | `11240bde` |
| **Date** | 2026-08-08 |
| **Assignments remaining in backlog after this cycle** | 358 (before newly discovered items appended) |

### Why this assignment was chosen over the alternatives

At claim time the backlog held 359 open assignments spanning 243 markets, of which **216 markets had zero completed reports**. The selection rule prioritizes catalog breadth first, then evidence availability, then angle diversity.

1. **Breadth.** The 29 completed reports cluster into seven recognizable clusters: accounting/tax, legal, insurance, healthcare administration, AEC/construction, transportation, and manufacturing quality. Employee-benefits *plan administration* — the ERISA world of qualified retirement plans — is completely absent. The one adjacent report ("HR and benefits administration in companies under 200 employees") looks at the employer side, not the specialist service bureau that actually performs the compliance work. Adding retirement plan TPAs opens a genuinely new vertical rather than deepening an existing one.

2. **Evidence density.** This market has an unusually good public evidence base for a niche profession: the BenefitsLink message boards are a decades-old, publicly indexed practitioner forum with dedicated subforums for "Operating a TPA or Consulting Firm" and "401(k) Plans"; the IRS publishes a *401(k) Plan Fix-It Guide* that is effectively a ranked list of the failure modes this profession exists to prevent; the DOL publishes hard plan counts by size; and TPA job postings describe caseloads and duties in unusual detail. Very little of this report rests on inference.

3. **Structural fit with the catalog's thesis.** The work is document- and spreadsheet-mediated, deadline-driven, performed by 1–40 person firms that cannot buy enterprise software, and governed by rules that are complicated but *written down and deterministic*. That is close to the ideal profile for narrow, focused, free-and-open-source tooling.

4. **Angle.** `core-practitioner-workflow` is the most-covered angle (9 of 29), which argues against it. It was chosen anyway because for this market the annual compliance cycle *is* the business — the back-office and handoff angles are meaningfully downstream of understanding the core cycle first, and leaving them in the backlog gives later cycles a well-primed target.

Rejected alternatives worth noting: *Building automation and controls contractors* (strong, but adjacent to the already-covered MEP/HVAC design report); *Calibration and metrology service providers* (strong, all four angles open — recommended for a near-term cycle); *Test, adjust and balance (TAB) contractors* (strong, but again AEC).

---

## 1. Market Examined

### The industry

A retirement plan third-party administrator is a non-fiduciary (usually) service provider that performs the *compliance and administration* work for employer-sponsored qualified retirement plans — principally 401(k) plans, plus profit sharing, money purchase, cash balance, and defined benefit plans. The TPA sits between three other parties:

- the **plan sponsor** (the employer), who owns the fiduciary responsibility;
- the **recordkeeper** (Empower, Fidelity, John Hancock, Voya, Principal, Ascensus, American Funds, etc.), who holds the participant accounts and processes trades;
- the **financial advisor / broker** (often 3(21) or 3(38)), who advises on investments and usually controls the client relationship.

In the "bundled" model the recordkeeper performs the TPA function internally. In the "unbundled" model — which dominates the small-plan market where plan design is complex — an independent TPA is retained separately. Independent TPAs are the subject of this report.

### Scale of the market

Form 5500 filings for plan years ending in 2023 (DOL EBSA *Private Pension Plan Bulletin*, published September 2025 — the most recent complete abstract) report:

| Segment | Count |
|---|---|
| Total private pension plans | 836,843 |
| Defined contribution plans | 790,610 |
| 401(k)-type plans | 724,720 |
| **401(k)-type plans with fewer than 100 participants** | **641,689** |
| All plans with fewer than 100 participants | 734,856 |

So roughly **89% of all 401(k) plans in the United States are small plans** — under 100 participants, therefore exempt from the annual independent audit requirement, therefore filing Form 5500-SF rather than the full 5500 with Schedule H. This is precisely the population that cannot support enterprise software and that independent TPAs serve. The population is also growing rapidly, driven by state auto-IRA mandates, the SECURE 2.0 startup tax credits, and pooled plan formation.

### The firms

Independent TPA firms are overwhelmingly small businesses:

- **Solo / micro (1–5 staff):** often a single credentialed administrator plus admin support, 40–150 plans. BenefitsLink threads about "Selling a small one-person TPA firm" and "Starting a TPA in Florida" confirm this segment is populous and active.
- **Small (6–25 staff):** the modal independent TPA. 300–1,200 plans, an owner/consultant, a document specialist, several plan administrators, and possibly an in-house actuary if they do cash balance work.
- **Midsize (25–100 staff):** regional firms, often with a dedicated compliance-testing team separate from client-facing consultants.
- **Roll-ups:** Strongpoint Partners and similar private-equity-backed platforms are actively consolidating this space; BenefitsLink carries "Seeking Acquisition Opportunities for Small to Mid-Size 401(k) TPA Firm" threads. Consolidation matters for tooling because acquired firms arrive on different administration platforms and must be integrated.

### The practitioner

The core role is variously titled **Retirement Plan Administrator**, **Pension Administrator**, **Compliance Analyst**, or **Plan Consultant**. A representative posting (Compensation Planning Inc., via EmployeeBenefitsJobs.com) describes the job as:

> "Manage an assigned caseload of 80+ small-employer 401(k) plans, serving as a trusted point of contact"

with responsibilities covering Top Heavy, ADP/ACP, 401(a)(4) and 410(b) testing; safe harbor, matching, and cross-tested profit sharing allocations; trust accounting and deposit reconciliation across multiple recordkeeping platforms; and Form 5500-SF preparation. Required tooling: **"Proficiency with Excel, Word, Outlook, Adobe PDF, and comfort learning industry-specific systems."** Credentials are ASPPA (QKA, QPA, CPC) or NIPA (APA, APR) designations, and are preferred rather than required.

**A caseload of 80+ plans per administrator is the single most important economic fact in this report.** It means each plan gets, at best, a few dozen hours of professional attention per year across the whole annual cycle. Any tool that removes even one hour per plan per year removes roughly two working weeks from an administrator's calendar.

---

## 2. How the Work Is Performed

The TPA's year is dominated by one large recurring cycle plus several event-driven side workflows.

### 2.1 The annual administration cycle (calendar-year plan)

**January – February: data request and chase.**
The TPA issues an annual data request to each client, typically consisting of (a) a **census spreadsheet template**, (b) an **annual employer questionnaire**, and (c) a request for trust statements and payroll registers. The census must cover *every employee who received compensation during the plan year*, not just plan participants. Required fields, per a representative TPA's published requirements:

- SSN and legal name
- Officer title, ownership percentage, and family relationship to any >1% owner
- Date of birth, original hire date, termination date, rehire date
- **Hours of service** — "all paid hours (worked, vacation, sick leave)"
- Gross compensation, plus plan compensation, plus W-2 wages, plus deferrals and HSA/125 amounts
- Owner income from Schedule K-1 / Schedule C / Schedule SE
- Employee pre-tax and Roth deferrals; employer match; safe harbor; catch-up
- A remarks field

The questionnaire covers the things the census cannot show: **controlled group and affiliated service group membership**, **the operational definition of compensation**, and **leased employees**. One TPA's published FAQ is blunt about why: *"The incorrect application of the Plan's definition of compensation is one of the most common errors found upon IRS audits."*

The chase phase is the notorious bottleneck. Clients send whatever their payroll system exports, in whatever layout, frequently omitting terminated employees, frequently omitting employees who never enrolled, frequently reporting the wrong compensation buckets, and frequently with no hours data at all.

**February – March: data scrubbing and reconciliation.**
The administrator normalizes the client's file into the layout their administration software expects, then reconciles it against independent sources:

- census deferral totals vs. the recordkeeper's contribution detail, participant by participant and payroll by payroll;
- census compensation vs. W-2 / payroll register totals;
- trust asset activity vs. the recordkeeper's trust statement;
- prior-year ending balances vs. current-year opening balances.

Where balance-forward or trustee-directed plans are involved (still common in small professional-practice plans), the TPA performs the actual trust accounting and participant allocation itself rather than reading it off a recordkeeper report.

**March 15 (or 2½ months after plan year end): ADP/ACP correction deadline.**
Nondiscrimination testing has to be done early enough that any corrective distribution to HCEs can be processed by 2½ months after year end to avoid the employer-level 10% excise tax. This creates a hard, early, immovable crunch — for a firm with 800 plans, the entire testing population must be triaged in about six weeks.

**Testing itself** comprises, at minimum:
- **410(b) coverage** — does the plan cover enough NHCEs?
- **ADP / ACP** — deferral and match rate comparison between HCEs and NHCEs (skipped if safe harbor)
- **402(g)** — individual deferral limit, including catch-up eligibility
- **415(c)** — annual additions limit per participant
- **401(a)(17)** — compensation cap
- **Top-heavy** — key employee account balances >60% of total, triggering a 3% minimum to non-keys
- **401(a)(4) general test / rate group testing** — for cross-tested and new comparability profit sharing allocations
- **Gateway minimum** — the 5% (or 1/3) floor that must be met before cross-testing is allowed

**March – July: allocations, employer contribution calculation, and client reporting.**
The administrator computes the employer contribution — often iteratively, because in a cross-tested plan the owner's target allocation and the required NHCE gateway feed back into each other and into 415 and deduction limits. The output is a set of client deliverables: an allocation report, testing results, a summary annual report, participant statements (for balance-forward plans), and a contribution funding instruction.

**July 31 (extendable to October 15): Form 5500 / 5500-SF and Form 8955-SSA.**
The 5500-SF is prepared from the reconciled trust accounting; Form 8955-SSA identifies separated participants with deferred vested benefits. Extensions run on Form 5558. The employer signs electronically through EFAST2, which means the TPA spends weeks chasing signatures and credentials.

### 2.2 Event-driven workflows running in parallel

- **Distributions, rollovers, and hardships.** Forms arrive incomplete — missing spousal consent, missing notarization, wrong dates, wrong vesting. The TPA calculates vesting and certifies eligibility to the recordkeeper.
- **Participant loans.** Origination, amortization, and — the perennial failure mode — missed payment tracking and deemed distributions under §72(p). The IRS explicitly states it is the plan sponsor's responsibility to track loans and hardships; in practice sponsors delegate this to the TPA informally.
- **Late deferral deposits.** Detection, lost-earnings calculation, excise tax, VFCP filing, and Form 5500 reporting.
- **Corrections (EPCRS).** Missed deferral opportunity, wrong compensation, excluded eligible employees, missed match, top-heavy shortfalls — self-corrected under SCP where possible, submitted under VCP where not.
- **Plan documents.** Cycle 4 pre-approved defined contribution restatements: the IRS submission window ran February 1, 2024 to January 31, 2025, and adopting employers are being restated through 2025–2026 with an amendment deadline of December 31, 2026. Every plan in the book must be restated inside the window — a once-every-six-years mass production event happening right now.
- **New legislation absorption.** SECURE 2.0 long-term part-time employee eligibility (500 hours in 2 consecutive years for 401(k) deferrals), the mandatory Roth treatment of catch-up contributions for prior-year FICA-wage earners above the indexed $145,000 threshold effective 2026, and the forfeiture 12-month use rule for plan years beginning on or after January 1, 2024.

### 2.3 Software actually in use

**Administration / valuation / testing engines** (the "big four," all decades old):

| Product | Practitioner assessment (BenefitsLink, 2024–2026) |
|---|---|
| **Relius** (FIS) | Long-dominant. "The support is so, so, so bad now... it's just a shame." "It's simply not what it used to be." Firms are actively researching exits. |
| **ASC** | "Clunky," appears "last updated in the 90s." Released a web-based valuation system January 2026, but described as remote-server rather than true cloud. |
| **DATAIR** | "If ASC seemed like the 90s, Datair is the 80s." Still a *preferred* skill in current job postings. |
| **ftwilliam** (Wolters Kluwer) | Web-based, handles balance-forward and trustee-directed plans well, support described as "fantastic," migration from Relius described as straightforward. The current momentum choice. |

**Workflow / practice management:**
- **PensionPro** — the category leader; "initial cost ($3,000–$4,000) and annual cost ($16,000–$17,000) is a bit steep" for small firms.
- **NexusTPA**, **Pension Portal (EBG)** — smaller competitors.
- Documented alternatives from practitioners: a generic document management system with workflow; a **custom in-house system** built by the firm; and — quoted verbatim — **"colored folders and a handheld label maker."**

**Everything in between is Excel, Outlook, and Adobe.** The census template is an Excel workbook. The reconciliation is an Excel workbook. The lost-earnings calculation is an Excel workbook. The forfeiture tracker is an Excel workbook. The client's file arrives as an emailed spreadsheet or a secure-portal upload (BenefitsLink has a thread specifically about "receiving secure emails w/census info").

---

## 3. Most Important Problems, Ranked

### Problem 1 — Client census data arrives dirty, late, and in an arbitrary layout; normalizing it consumes the front half of the cycle

**Who experiences it:** Every plan administrator, on every plan, every year.
**When:** January–March, concentrated before the March 15 ADP/ACP correction deadline.
**How handled now:** Manual eyeballing of the client's spreadsheet, ad-hoc Excel formulas, and an email round-trip for each question. Some firms build per-client mapping macros; most re-key.
**Why inadequate:** The validation rules are *plan-specific* — what counts as compensation, what counts as an hour of service, which entry dates apply, who is excluded by class — and live in the plan document, not in any spreadsheet. Generic recordkeeper upload validators check file format, not plan rules. Every question costs an email round-trip with a client whose payroll clerk is not a benefits professional.
**Frequency:** 80+ times per administrator per year.
**Cost:** If normalizing and querying a census consumes 2–5 hours per plan (a conservative reading of an 80-plan caseload against a compressed Q1), that is 160–400 hours per administrator per year — a quarter to a half of a full-time equivalent, spent on data janitorial work by someone credentialed to interpret ERISA.
**Evidence:** Direct — published census requirement lists enumerating ~15 required fields including hours of service and family/ownership relationships; job postings that make "interpret plan documents and census data" a core duty; BenefitsLink threads on census transmission and entry-date disputes. **Verified.**

### Problem 2 — Incorrect application of the plan's compensation definition is the most common operational failure, and it is invisible until an audit

**Who:** The plan sponsor causes it; the TPA discovers it, owns the correction, and absorbs the reputational damage.
**When:** Continuously, every payroll, undetected — surfacing at first plan audit, IRS exam, or plan takeover.
**How handled now:** An annual questionnaire question asking the client to confirm what they include. In practice, nobody reconciles the client's actual payroll earnings codes to the document's definition.
**Why inadequate:** The failure is at the *earnings-code* level. A real BenefitsLink case: the document defined compensation as W-2 with only sign-on bonuses excluded, but payroll was also excluding group-term-life imputed income ("all employees have this"), domestic partner benefits, moving reimbursements, equity income, and vehicle allowances. It surfaced only when the company grew past 100 participants and required its first audit in 2025. New earnings codes get added by payroll departments with no notice to anyone.
**Frequency:** IRS names it #3 in the Fix-It Guide; a TPA's own client FAQ calls it "one of the most common errors found upon IRS audits."
**Cost:** Correction is a QNEC of 25–50% of the missed deferral, plus 100% of the missed match, plus lost earnings, **per affected employee per pay period, retroactively**. The BenefitsLink poster's own words: a "long painful process" of "calculating missed earnings for every employee across each paycheck historically." The alternative — retroactive amendment — requires a VCP submission with IRS user fee plus evidence (SPDs, enrollment materials) that participants understood the exclusion, evidence that usually does not exist.
**Evidence:** Direct — IRS Fix-It Guide item 3; the BenefitsLink correction thread; TPA questionnaire FAQ. **Verified.**

### Problem 3 — Late deferral deposits are detected late, and the correction math is disproportionately expensive relative to the amounts involved

**Who:** The plan sponsor breaches; the TPA detects and computes.
**When:** Discovered during the annual cycle, months after the fact.
**How handled now:** Compare payroll dates to trust deposit dates by hand; compute lost earnings in Excel.
**Why inadequate:** The correction hierarchy under EPCRS is *actual earnings first*, then best-performing-fund rate, then the plan's weighted average rate, and only then the DOL Online Calculator — and the DOL has been explicit that its calculator is available only in connection with a VFCP application. Practitioners routinely use the DOL calculator anyway without filing, a divergence one senior practitioner describes while explicitly saying "We do NOT recommend using this alternative." The math is two-stage (lost earnings during the delay, then earnings on those earnings) and must be done per participant per payroll.
**Cost:** Quoted directly from a practitioner: *"That can get hectic if there are more than a few participants involved, or multiple payrolls. Hectic and pricey — we charge by the hour, and the cost can easily overtake any benefit to the participants."* Plus a 15% excise tax on the lost earnings and Form 5500 reporting of the delinquency.
**Root cause:** Manual file movement between payroll and recordkeeper — manual uploads, file rejections requiring resubmission, off-cycle payrolls, multiple recordkeepers, staff turnover, holiday timing.
**Frequency:** Described by multiple independent sources as among the most common ERISA compliance findings and a perennial DOL audit target.
**Evidence:** Direct — BenefitsLink thread on lost earnings calculation; DOL VFCP mechanics; multiple accounting-firm advisories. **Verified.**

### Problem 4 — Missed deferral opportunity: eligible employees who were never enrolled, discovered a year or more later

**Who:** Administrator and sponsor.
**When:** Discovered during annual eligibility recomputation — i.e. up to 15 months after the employee should have entered.
**How handled now:** The administrator recomputes eligibility from the census hire/term/rehire and hours columns, compares to who actually deferred, and investigates gaps.
**Why inadequate:** It is a *retrospective* check on a *prospective* obligation. SECURE 2.0's long-term part-time rule (two consecutive years with 500+ hours) makes it dramatically worse, because it makes part-timers — the population whose hours are least reliably tracked and whose data clients most often omit from the census — newly eligible, and requires multi-year hours history that most small payroll exports do not carry forward.
**Cost:** QNEC of 25–50% of the missed deferral plus 100% of missed match plus earnings, per employee. Also failed 410(b) coverage risk if enough people were excluded.
**Evidence:** Direct — IRS Fix-It Guide item 6; extensive SECURE 2.0 LTPT commentary. **Verified.**

### Problem 5 — Payroll-to-recordkeeper contribution reconciliation is manual, participant-level, and period-level

**Who:** Administrator (and, for large plans, the independent auditor).
**When:** Every annual cycle; more often at firms that do quarterly reconciliation.
**How handled now:** Excel VLOOKUPs across a payroll register export and a recordkeeper contribution detail export with different participant identifiers, different date conventions, and different money-type labels.
**Why inadequate:** Variances occur "by period and participant," so a totals-only tie-out hides offsetting errors. Purpose-built tooling exists (AuditMiner) but is sold to *CPA firms performing plan audits*, not to TPAs, and small plans do not get audited at all — meaning the 641,689 small 401(k) plans have nobody systematically performing this reconciliation.
**Cost:** This is the reconciliation that *would have caught* Problems 2, 3, and 4 earlier. Its absence is upstream of the expensive corrections.
**Evidence:** Strong inference from direct evidence — job postings requiring "trust accounting and deposit reconciliation across various recordkeeping platforms"; AuditMiner's product description of the same reconciliation on the audit side. **Verified as a task; the time cost is inferred.**

### Problem 6 — Controlled group / affiliated service group status is asked once a year in prose and is frequently wrong

**Who:** Administrator; catastrophic for the sponsor.
**When:** Annual questionnaire; often wrong for years.
**How handled now:** A free-text question on a PDF questionnaire.
**Why inadequate:** §414(b)/(c)/(m) and §1563 attribution — parent-subsidiary, brother-sister, spousal attribution, minor children, community property, and the affiliated-service-group tests — are genuinely intricate rules being answered by a business owner reading a paragraph. Clients acquire entities, spouses start businesses, and nobody tells the TPA.
**Cost:** If related employers are not aggregated, coverage and nondiscrimination testing are wrong for every affected year. Correction is retroactive corrective contributions across all affected entities; the worst-case framing in the literature is plan disqualification.
**Evidence:** Direct — TPA questionnaire FAQ ("Employees of related employers must be considered together as though they are a single employer"); multiple advisory firms treating it as a top small-plan pitfall. **Verified.**

### Problem 7 — Forfeitures accumulate in suspense accounts past their use-by date

**Who:** Administrator and sponsor.
**When:** Discovered during annual reconciliation.
**How handled now:** A column in a spreadsheet, or nothing.
**Why inadequate:** Proposed regulations require forfeitures arising in a plan year to be used within 12 months after the close of that plan year (forfeitures in 2024 → used by December 31, 2025 for a calendar-year plan), with a transition rule sweeping pre-2024 balances into the first plan year beginning on or after January 1, 2024. Permitted uses (expenses, contribution offset, reallocation) must be authorized by the document. Meanwhile a substantial wave of class-action litigation over forfeiture *use* — whether offsetting employer contributions rather than paying expenses breaches fiduciary duty — ran through 2024–2025, with DOL weighing in during 2025.
**Cost:** Operational failure requiring correction; plus elevated litigation salience.
**Evidence:** Direct — proposed regulation summaries, litigation trackers. **Verified.**

### Problem 8 — The practice-management layer is either $17k/year or colored folders

**Who:** Firm owners at 1–25 person TPAs.
**When:** Continuously.
**How handled now:** PensionPro if affordable; a home-built system, a DMS with workflow, or physical file management if not.
**Why inadequate:** The gap between "$16,000–$17,000 per year" and "colored folders and a handheld label maker" is the entire small-firm segment. Note carefully: **this problem is deliberately excluded from the recommendations below.** Building another practice-management platform is exactly the generic, unscoped, enterprise-shaped product this catalog is supposed to avoid. It is listed here because it explains why the *narrow* tools below have no incumbent — small TPAs have no platform into which a vendor could embed these features.
**Evidence:** Direct — BenefitsLink workflow software threads. **Verified.**

### Problem 9 — Cycle 4 restatement is a mass-production event with a hard December 31, 2026 wall

**Who:** Document specialists at every TPA.
**When:** Now, through end of 2026.
**How handled now:** Document software (ftwilliam, Relius Documents, ASC) generates the restatements; tracking adoption, signature, and delivery is manual.
**Cost:** Every plan in the book, once, inside a window; a missed restatement is a qualification defect requiring VCP.
**Evidence:** Direct — IRS Cycle 4 announcement and law firm summaries. **Verified.**

### Problem 10 — Form 8955-SSA populations drift from reality

**Who:** Administrator.
**When:** With the 5500 filing.
**How handled now:** Administration software generates a candidate list; the administrator adjusts it by hand.
**Why inadequate:** Participants get reported as deferred-vested (Code A), then paid out, and must be removed (Code D). Miss the removal and the Social Security Administration keeps telling retirees they have a benefit in a plan that paid them out years ago — the sponsor receives the resulting inquiries. Prior-year filings are PDFs; nobody diffs them.
**Cost:** Low per event, high nuisance and reputational cost; late-filing penalties apply.
**Evidence:** Direct — ASPPA article specifically on 8955-SSA participant statement confusion; IRS instructions. **Verified as a real recurring irritation; magnitude is modest.**

---

## 4. Application Opportunities

### A. **CensusGuard** — plan-rule-aware census intake validator and normalizer

- **User:** Plan administrator at a 1–40 person TPA.
- **Problem solved:** Problem 1 (and early detection of 4 and 6).
- **Current workflow:** Client emails an arbitrary payroll export. Administrator opens it, hand-maps columns, eyeballs for missing terminations, sends 3–8 clarifying emails, re-keys into the administration software's import layout.
- **Proposed workflow:** Administrator selects the plan's saved **rule profile** (eligibility service requirement, entry dates, hours-counting method, excluded classes, compensation definition, plan year, prior-year census). Drops the client file in. Gets back (1) an **exception report** organized by severity and by *who must answer it* — client vs. administrator; (2) a **normalized census** in the target software's import layout; (3) a **year-over-year delta report** — who appeared, who vanished without a termination date, whose DOB or hire date changed, whose compensation moved implausibly.
- **Inputs:** Client file (xlsx/csv), plan rule profile (JSON), prior-year normalized census.
- **Outputs:** Exception report (xlsx + PDF), normalized census (xlsx/csv), client-ready query letter listing only the questions the client can actually answer.
- **Essential features:** Column auto-mapping with a per-client saved mapping; ~60 deterministic checks (duplicate/invalid SSN, DOB after DOH, term before hire, rehire without term, negative or zero compensation with nonzero deferrals, deferrals exceeding 402(g), compensation exceeding 401(a)(17), missing hours where hours matter, owner rows without ownership %, missing family-relationship flags, participants present last year and absent this year with no termination); severity ranking; prior-year diff.
- **Excluded from v1:** Actually running compliance tests. Direct API connections to payroll providers. Multi-user workflow. Storage of anything server-side.
- **AI:** *Optional, and only for one job* — proposing a column mapping for an unseen payroll layout, which the human confirms once and which is then saved as a deterministic mapping. Every validation rule must be conventional code. AI must never adjudicate a compliance question.
- **Why not a spreadsheet:** Firms already do this in spreadsheets. The spreadsheet fails because the rules are per-plan (so the workbook must be re-edited for each of 80 plans), because the prior-year diff requires joining two files, and because the exception list needs to be *split by audience* — a formula cannot decide which questions to put in a client letter.
- **Complexity:** Small-to-medium. **Learning:** 20 minutes. **Value:** 1–3 hours per plan per year; at 80 plans, 80–240 hours per administrator.
- **Risks:** Census files contain full SSNs, DOBs, and compensation for every employee. This *must* be an offline, local-only, single-file tool. Any cloud version needs real security posture. A false "clean" result creates reliance risk — the tool must be framed as a checklist assistant, not an opinion.
- **Substitutes:** Recordkeeper upload validators (format only, not plan rules); administration software import validators (schema only); Excel. None validate against the *plan document*.
- **Why still attractive:** The rule profile is the moat — nobody else has the plan's terms in machine-readable form at the moment the file arrives.
- **Customization:** Very high. Per-firm rule libraries, per-client mappings, and output in the firm's specific administration-software import layout are all obvious paid work.

### B. **CompMap** — payroll earnings-code to plan-compensation crosswalk with unmapped-code alarm

- **User:** Plan consultant / administrator; secondarily the client's payroll manager.
- **Problem solved:** Problem 2.
- **Current workflow:** A yes/no question on an annual questionnaire.
- **Proposed workflow:** Once per client, import the payroll system's **earnings code list**. For each code, record its treatment under each compensation definition the plan uses — 415 compensation, plan compensation for allocations, compensation for deferral withholding, testing compensation, and post-severance/severance treatment. Produce a **signed crosswalk** the sponsor attests to. On each subsequent census or payroll register import, the tool re-reads the code list and **flags codes that did not exist last time** — the exact mechanism by which this failure begins.
- **Inputs:** Payroll earnings/deduction code list, plan document compensation elections, payroll register with code-level detail.
- **Outputs:** Crosswalk matrix (xlsx + signable PDF), new/changed-code alert, a reconciliation showing whether deferrals were actually withheld on the code set the crosswalk says they should be.
- **Essential features:** Multi-definition columns; effective dating; attestation block; new-code detection; a plain-English rationale field per code.
- **Excluded from v1:** Computing corrections. Payroll API integrations. Auto-classifying codes without human sign-off.
- **AI:** *Optional* — suggesting a likely treatment for a code named `GTL-IMP` or `MOVEXP`, always as a suggestion requiring confirmation. The classification is a legal determination; AI proposes, the practitioner disposes.
- **Why not a spreadsheet:** A spreadsheet cannot detect that the client added an earnings code in June. The alarm is the product.
- **Complexity:** Medium. **Learning:** 45 minutes for the first client, 10 minutes thereafter. **Value:** Prevents a single correction that costs tens of thousands of dollars in QNECs plus VCP fees; also converts a vague annual question into a documented, dated, signed artifact — which is professional-liability value independent of the compliance value.
- **Risks:** The crosswalk becomes a liability document. It must clearly record who decided what and when. Getting a code list out of some payroll systems is itself work.
- **Substitutes:** None found. This is a genuine gap.
- **Customization:** High — pre-loaded code libraries for ADP, Paychex, Paylocity, Gusto, QuickBooks, and the regional payroll bureaus a given TPA sees repeatedly.

### C. **DepositWatch** — deferral remittance timeliness monitor and lost-earnings workpaper

- **User:** Administrator; also directly useful to the plan sponsor.
- **Problem solved:** Problem 3.
- **Current workflow:** Compare two date columns by hand once a year; compute earnings in an ad-hoc workbook.
- **Proposed workflow:** Import payroll register dates and withheld amounts; import trust/recordkeeper deposit dates and amounts. The tool matches payroll periods to deposits, computes the remittance lag, applies the plan's stated standard and the small-plan 7-business-day safe harbor, and flags exceptions. For each exception it produces a **lost-earnings workpaper** computing the amount under each permitted method side by side — actual participant earnings (if a rate file is supplied), best-performing fund rate, plan weighted-average rate, and the DOL Online Calculator method — with the two-stage earnings-on-earnings computation, the 15% excise tax on the resulting amount, and the totals formatted for Form 5500 delinquent-participant-contribution reporting.
- **Inputs:** Payroll register (date, participant, deferral amount, Roth/pre-tax, loan repayments), deposit detail, optional fund return series.
- **Outputs:** Timeliness exception report; per-participant lost earnings workpaper (xlsx); VFCP-application-ready summary; 5500 line amounts.
- **Essential features:** Period matching with partial-deposit handling; configurable timeliness standard; all four earnings methods; method-comparison summary; audit trail of inputs.
- **Excluded from v1:** Filing anything with anyone. Bank connections. Advising which method to use.
- **AI:** **Inappropriate.** This is arithmetic against published rates. Introducing a language model here would be indefensible.
- **Why not a spreadsheet:** It is a spreadsheet today, and the practitioner quote — "hectic and pricey... the cost can easily overtake any benefit to the participants" — is the direct measurement of why the spreadsheet fails. The methods hierarchy and the earnings-on-earnings second stage are where the manual version breaks.
- **Complexity:** Medium. **Learning:** 30 minutes. **Value:** Converts a multi-hour hourly-billed exercise into minutes; the side-by-side method comparison also lets the firm *choose the defensible cheapest method*, which is a real dollar outcome for the client.
- **Risks:** Getting the DOL calculator's underlying rate methodology right matters and the rates must be maintained. The tool must state clearly that the DOL calculator method is tied to VFCP eligibility — building a tool that makes the shortcut *easier* would be professionally irresponsible without that warning surfaced prominently.
- **Substitutes:** The DOL's own online calculator (single-participant, single-period, no workpaper); Excel.
- **Customization:** Moderate-to-high — firm-branded workpaper templates, fund return series loading for a specific recordkeeper.

### D. **EntryCheck** — eligibility, entry date, and LTPT engine with missed-deferral early warning

- **User:** Administrator; strong candidate for a sponsor-facing version.
- **Problem solved:** Problem 4.
- **Current workflow:** Recompute eligibility annually from the census; notice gaps after the fact.
- **Proposed workflow:** Given a multi-year employment and hours history plus the plan's eligibility elections, compute for every employee: statutory eligibility date, plan entry date, LTPT status under the 500-hours/2-consecutive-years rule, and vesting service. Then **cross-reference against who actually has a deferral election or deferrals on file** and produce a ranked list of probable missed-deferral-opportunity cases with the estimated correction cost for each. Also produce a **forward-looking roster**: who becomes eligible in the next 12 months and on what date — the deliverable that prevents the failure instead of finding it.
- **Inputs:** Multi-year census/employment history with hours, plan eligibility elections, deferral election status.
- **Outputs:** Per-employee eligibility determination with the computation shown; upcoming-eligibility roster with dates; suspected-MDO list with estimated QNEC exposure.
- **Essential features:** Elapsed-time and hours-counting methods; computation period elections; rehire and break-in-service rules; LTPT tracking with the multi-year hours carryforward; the "should have deferred but didn't" cross-check.
- **Excluded from v1:** Actually calculating and documenting the correction. Notice generation. Enrollment.
- **AI:** **Inappropriate.** Deterministic date and service arithmetic.
- **Why not a spreadsheet:** Break-in-service rules, rehire handling, and multi-year LTPT hours accumulation across changing census files defeat a flat workbook. Firms do build these workbooks; they break every time an edge case appears.
- **Complexity:** Medium. **Learning:** 45 minutes. **Value:** One avoided MDO correction on a 40-person plan justifies the tool permanently. The forward roster is what a client will actually pay for.
- **Risks:** Multi-year hours history frequently does not exist — the tool must degrade gracefully and say so rather than silently assuming zero. Getting a rule wrong produces a confidently incorrect determination.
- **Substitutes:** Administration software computes eligibility, but as a black box inside the annual valuation, not as a forward-looking roster or an MDO detector.
- **Customization:** High — LTPT tracking as a standalone paid service is a plausible product for a TPA to resell.

### E. **TieOut** — payroll-to-recordkeeper contribution reconciler

- **User:** Administrator; also the sponsor's controller.
- **Problem solved:** Problem 5.
- **Current workflow:** VLOOKUPs between two exports with mismatched keys.
- **Proposed workflow:** Load a payroll register export and a recordkeeper contribution-detail export. Fuzzy-match participants (SSN where available, else name+DOB), normalize money types across the two vocabularies via a saved per-recordkeeper mapping, and produce a **variance report by participant and by period** with the variances classified: timing difference, money-type misclassification, missing participant, amount difference, off-cycle payroll not remitted.
- **Inputs:** Payroll register, recordkeeper contribution detail, per-recordkeeper money-type mapping.
- **Outputs:** Variance report (xlsx), reconciliation summary, feed of candidate late deposits into DepositWatch.
- **Essential features:** Participant matching with a manual override list; money-type mapping library; variance classification; roll-forward of unresolved variances to next period.
- **Excluded from v1:** Trust asset reconciliation. Investment activity. Correcting anything.
- **AI:** **Inappropriate** for the matching logic; a narrow, arguable *optional* use is proposing a money-type mapping for an unfamiliar recordkeeper export, confirmed once.
- **Why not a spreadsheet:** It is a spreadsheet today; the failure mode is that a totals-level tie-out passes while offsetting participant-level errors hide inside it.
- **Complexity:** Medium (participant matching across systems is the hard part). **Learning:** 45 minutes. **Value:** Moves detection of Problems 2, 3, and 4 from annual to per-payroll for firms that want to sell quarterly reconciliation as a service.
- **Risks:** Export formats vary by recordkeeper and change without notice; the mapping library is ongoing maintenance. Highest implementation risk of the set.
- **Substitutes:** AuditMiner — but aimed at CPA audit firms and at the 100+ participant plans that get audited, leaving the 641,689 small plans entirely uncovered.
- **Customization:** High, but the maintenance burden is real; price accordingly.

### F. **RelatedCo** — controlled group and affiliated service group interview with determination memo

- **User:** Consultant or administrator, during annual questionnaire season or at new-plan takeover.
- **Problem solved:** Problem 6.
- **Current workflow:** A paragraph on a PDF asking the owner to self-assess.
- **Proposed workflow:** A branching interview capturing entities, ownership percentages, individual owners, family relationships, and service relationships. The tool applies §1563 attribution (spouse, minor children, parents/grandparents of adult children, and the noninvolvement exceptions) and the parent-subsidiary / brother-sister / combined tests, plus the affiliated-service-group A-org / B-org / management-function screens. Output: an **ownership diagram**, a **determination memo** showing the arithmetic, and a **year-over-year change log** highlighting what the client changed since last year.
- **Inputs:** Interview responses; prior year's saved answers.
- **Outputs:** Determination memo (PDF), ownership diagram (SVG), change log, aggregated employee-group definition for testing.
- **Essential features:** Attribution engine; the arithmetic shown, not just the conclusion; explicit "insufficient information — escalate to ERISA counsel" outcomes; change log.
- **Excluded from v1:** Rendering an opinion on genuinely ambiguous ASG facts — the tool should *flag and stop*, not conclude. No coverage testing.
- **AI:** **Inappropriate** for the determination. Arguably useful to summarize a client's narrative description into structured entity/ownership facts for confirmation.
- **Why not a spreadsheet:** Attribution is graph traversal with exceptions, not tabular arithmetic. And the change log — "last year you said you owned no other business; this year you listed two" — is the actual value.
- **Complexity:** Small-to-medium. **Learning:** 30 minutes. **Value:** Catches a failure whose worst case is described in the literature as plan disqualification. Also produces a dated professional work product, which is E&O value.
- **Risks:** **The most legally sensitive concept in this list.** Affiliated-service-group determinations are legal conclusions. The product must be positioned as a structured interview and worksheet that *prepares* a determination for a qualified professional, never as one. An overconfident output here is worse than no tool.
- **Substitutes:** ERISA counsel; the questionnaire paragraph. Nothing in between.
- **Customization:** High — firm-branded memo templates; integration into the firm's annual questionnaire.

### G. **ForfeitureClock** — forfeiture ledger with 12-month use tracking

- **User:** Administrator.
- **Problem solved:** Problem 7.
- **Current workflow:** A spreadsheet column, or nothing.
- **Proposed workflow:** Record forfeiture events by participant, source, and plan year of forfeiture. Apply the plan document's permitted uses and ordering. Compute the use-by date under the 12-month rule (with the pre-2024 transition sweep). Show a running balance with an aging bucket and a hard flag on anything approaching or past its deadline. Reconcile the ledger to the recordkeeper's forfeiture account balance.
- **Inputs:** Forfeiture events (from the vesting/distribution process), plan document forfeiture provisions, recordkeeper forfeiture account statements.
- **Outputs:** Aging report with use-by dates, reconciliation to recordkeeper balance, a suggested application worksheet.
- **Essential features:** Aging; use-by computation with transition rule; document-driven permitted uses; reconciliation.
- **Excluded from v1:** Executing the application. Fee-payment analysis. Any opinion on the fiduciary litigation question.
- **AI:** **Inappropriate.**
- **Why not a spreadsheet:** Marginal — it genuinely could be a well-built spreadsheet. The advantages are the transition rule, cross-plan rollup for a firm's whole book, and the reconciliation. This is honestly the weakest "not a spreadsheet" argument in the set, which is why it scores as it does.
- **Complexity:** Small. **Learning:** 15 minutes. **Value:** Prevents an operational failure; produces a defensible record during a period of active forfeiture litigation.
- **Risks:** The proposed regulations are proposed. The tool must be versioned against the rule as adopted.
- **Substitutes:** Excel; recordkeeper reports.
- **Customization:** Moderate.

### H. **SSA8955Builder** — separated-vested population builder with prior-year reconciliation

- **User:** Administrator preparing the 5500 package.
- **Problem solved:** Problem 10.
- **Current workflow:** Accept the administration software's candidate list, adjust by hand, hope prior filings were right.
- **Proposed workflow:** From the current census plus vesting and distribution history, derive the separated-participants-with-deferred-vested-benefits population, assign entry codes, and **diff against parsed prior-year filings** to find people who were reported as Code A and have since been paid out (needing Code D), people reported twice, and people who should have been reported and never were.
- **Inputs:** Census, vesting/balance data, distribution history, prior-year 8955-SSA filings (PDF or data).
- **Outputs:** Current-year population with codes, prior-year exception list, filing-ready data file.
- **Essential features:** Code assignment logic; prior-year parsing and diff; exception list.
- **Excluded from v1:** Actually filing. Signature workflow.
- **AI:** **Inappropriate** for the logic; a narrow *optional* use is extracting participant rows from prior-year PDF filings where no data file survives — a legitimate document-extraction task.
- **Why not a spreadsheet:** The prior-year diff against PDFs is the whole point.
- **Complexity:** Small. **Learning:** 20 minutes. **Value:** Modest per plan; eliminates a recurring irritation and a small penalty exposure.
- **Risks:** Contains SSNs. Low.
- **Substitutes:** Administration software output.
- **Customization:** Low-to-moderate.

### I. **AnnualAsk** — branching annual plan questionnaire with year-over-year change detection

- **User:** Administrator issuing the annual data request; the client fills it in.
- **Problem solved:** Problems 1, 2, and 6 at the point of intake.
- **Current workflow:** A static PDF or Word questionnaire, emailed, returned incomplete.
- **Proposed workflow:** A single-file local web form, pre-populated with last year's answers, that branches (answering "yes" to other business ownership opens the RelatedCo sub-interview; a compensation question opens the CompMap code review). It refuses to submit while required items are blank, and produces both a filled response document and a **change log** — "these four answers differ from last year" — which is the report the administrator actually reads.
- **Inputs:** Prior-year responses, plan profile.
- **Outputs:** Completed questionnaire (PDF), change log, structured data feeding the other tools.
- **Essential features:** Prefill; branching; required-field enforcement; change log; export.
- **Excluded from v1:** Client portal accounts, e-signature, email sending, hosted anything. It should be a file you send and a file they send back.
- **AI:** **Inappropriate.**
- **Why not a spreadsheet:** Branching and required-field enforcement; and a spreadsheet cannot produce a diff against last year's PDF.
- **Complexity:** Small-to-medium. **Learning:** 10 minutes for the client — which is the metric that matters, since the client is the reluctant user.
- **Risks:** Clients dislike new formats; must work with zero installation and no account. A single self-contained HTML file that saves to a downloadable JSON is the right shape.
- **Substitutes:** PDF forms; recordkeeper year-end questionnaires (Vestwell and others publish these, but they serve the recordkeeper's needs, not the independent TPA's).
- **Customization:** Very high — every firm's questionnaire differs, and adapting it is exactly the kind of small paid engagement this catalog is designed to generate.

---

## 5. Opportunity Ranking

Scores are 1–5 on each of ten criteria; maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of impl. | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| A | **CensusGuard** — census intake validator | 5 | 5 | 5 | 5 | 4 | 4 | 3 | 5 | 4 | 5 | **45** |
| B | **CompMap** — earnings-code crosswalk | 5 | 4 | 4 | 4 | 4 | 5 | 5 | 5 | 3 | 5 | **44** |
| C | **DepositWatch** — late deposits + lost earnings | 5 | 4 | 5 | 5 | 3 | 5 | 4 | 4 | 4 | 5 | **44** |
| D | **EntryCheck** — eligibility / LTPT / MDO warning | 5 | 5 | 5 | 4 | 3 | 4 | 4 | 5 | 4 | 5 | **44** |
| I | **AnnualAsk** — branching annual questionnaire | 4 | 4 | 4 | 5 | 4 | 4 | 4 | 5 | 3 | 5 | **42** |
| F | **RelatedCo** — controlled group / ASG interview | 4 | 4 | 4 | 5 | 4 | 4 | 4 | 4 | 3 | 5 | **41** |
| G | **ForfeitureClock** — forfeiture 12-month ledger | 4 | 3 | 4 | 5 | 5 | 5 | 4 | 3 | 4 | 4 | **41** |
| H | **SSA8955Builder** — separated-vested population | 3 | 3 | 3 | 5 | 5 | 5 | 4 | 3 | 4 | 4 | **39** |
| E | **TieOut** — payroll ↔ recordkeeper reconciler | 4 | 5 | 4 | 4 | 3 | 4 | 3 | 4 | 3 | 4 | **38** |

### The top three

**1. CensusGuard (45).** It sits at the exact point where the profession's cost is incurred. Every downstream problem in this report — wrong compensation, missed eligibility, unreported terminations, bad testing — enters through the census file. It is the only concept that every administrator uses on every plan every year, which makes its return purely multiplicative: an hour saved is eighty hours saved. Its weakness is differentiation (3): recordkeepers and administration software both offer *some* file validation, so the pitch has to be specifically that this validates against the **plan document's rules**, not the file's schema. That distinction is real but requires explaining, and the rule-profile concept is the thing that must be gotten right in a prototype.

**2. CompMap (44).** The highest-severity single failure in the report. The IRS ranks compensation-definition error third in its Fix-It Guide and a working TPA's own client materials call it "one of the most common errors found upon IRS audits." It scores a rare 5 on differentiation because nothing on the market does it — the entire industry currently handles it with a yes/no question. The insight that makes it a product rather than a form is the **new-code alarm**: the failure does not begin when someone answers the questionnaire wrong, it begins when a payroll department adds an earnings code in June and tells nobody. Its lower frequency score (4) reflects that it is a per-client setup plus a periodic check rather than a per-plan-per-year grind.

**3. DepositWatch (44) and EntryCheck (44), tied.** DepositWatch has the cleanest measurable ROI in the whole set because a practitioner has stated the cost in their own words — hourly billing that "can easily overtake any benefit to the participants." It is also the concept where AI is most clearly inappropriate and conventional code most clearly sufficient, which is a virtue. EntryCheck is the one concept with a genuinely *preventive* deliverable — the forward-looking eligibility roster — rather than a detective one, and SECURE 2.0's LTPT rule is actively increasing its severity. Both are dragged down only by implementation difficulty (3): DepositWatch needs maintained rate data, EntryCheck needs multi-year history that often does not exist.

### What should be investigated next

**CensusGuard first**, because it is the wedge: it is the tool an administrator opens on day one of the cycle, and the rule profile it requires is the same data structure that EntryCheck, CompMap, and AnnualAsk all need. Build the rule-profile schema once and three other products become substantially cheaper.

**Then CompMap**, because it is the highest-differentiation, highest-severity concept and the one most likely to be *sold* rather than merely used — it produces a signed artifact a plan sponsor can hand an IRS examiner.

TieOut (38) is the one to deprioritize despite its high frequency score: export-format volatility across a dozen recordkeepers makes it a maintenance treadmill, and a well-capitalized incumbent already serves the adjacent audit market.

---

## 6. Validation Plan

### Questions to ask practitioners

*On CensusGuard:*
1. Walk me through the last census you received. How many round-trips with the client before it was usable? How long between "file arrives" and "file is loaded"?
2. What fraction of your Q1 hours are data cleanup versus professional judgment?
3. Do you maintain per-client column mappings today? In what — macros, saved import templates, memory?
4. When a client's file is missing hours, what do you actually do?
5. Which errors do you find every single year, on every client?

*On CompMap:*
6. Have you ever discovered a compensation-definition failure? How was it found — audit, takeover, or accident? What did the correction cost?
7. Do you ever ask a client for their payroll earnings-code list? If not, why not?
8. Would a sponsor sign an attestation on a code-level crosswalk? What would make them refuse?

*On DepositWatch:*
9. How many late-deposit corrections did you handle last year? How many hours each?
10. Which lost-earnings method do you actually use, and how do you document the choice?
11. Do your clients file VFCP, or self-correct without filing? (Ask carefully — this is a sensitive question.)

*On EntryCheck:*
12. How are you handling LTPT tracking right now? Do your clients' payroll exports carry prior-year hours?
13. Have you ever found a missed-deferral-opportunity case? How long after it started?
14. Would you sell a forward-looking eligibility roster as a deliverable?

*Cross-cutting:*
15. What would stop you from using a tool that runs entirely on your own machine with no cloud component?
16. Who at your firm decides on new software, and what does an approval require?

### Who to interview

- Owners of 3–15 person independent TPAs — reachable via the BenefitsLink "Operating a TPA or Consulting Firm" forum, ASPPA and NIPA local chapter events, and the NIPA Annual Forum.
- Credentialed plan administrators (QKA/QPA/APA) carrying 70–100 plan caseloads.
- Document specialists currently working Cycle 4 restatements — they will have the sharpest view of which plans have unreliable data.
- ERISA employee benefit plan auditors at small CPA firms — they see the failures from outside and know which ones recur.
- Payroll managers at 30–150 employee companies — the *reluctant user* whose cooperation determines whether AnnualAsk and CompMap work at all. This interview matters more than it looks.

### Search terms for further research

`"missed deferral opportunity" correction QNEC 25%` · `EPCRS "earnings on earnings" lost earnings method` · `benefitslink "census" cleanup hours` · `"long-term part time" hours tracking payroll export 401k` · `"earnings code" 401k "plan compensation" mapping` · `ftwilliam import layout census specification` · `Relius census import file format` · `ASPPA annual conference agenda data quality` · `NIPA annual forum session automation` · `TPA "value add services" pricing per plan` · `"3(16)" fiduciary services scope TPA` · `plan takeover checklist prior TPA data`

### Sample files / data needed

- Three or four **anonymized census files** in different payroll-system export layouts (ADP, Paychex, Paylocity, QuickBooks) — the single most valuable artifact for building CensusGuard.
- A **payroll earnings-code list** with descriptions from at least two payroll systems.
- One **recordkeeper contribution-detail export** and the matching payroll register for the same period.
- A **plan document / adoption agreement** for a typical small safe-harbor 401(k) with a cross-tested profit sharing allocation, so the rule profile can be derived from a real document rather than a hypothetical one.
- Two consecutive years of **Form 8955-SSA** filings for one plan.
- Published import specifications for ftwilliam and ASC census loads.

### Prototype that would validate the idea

A single-file, offline HTML application. Left pane: a JSON rule profile with about fifteen fields (plan year, eligibility service and hours method, entry dates, excluded classes, compensation definition flags, safe harbor status). Right pane: drop zone for a census xlsx. Output: a two-column exception report split into "client must answer" and "administrator must resolve," plus a normalized CSV.

Take that to five TPAs with **their own real anonymized files**. The test is not whether they like it — everyone likes a demo. The test is: **does it find something they missed?** If it surfaces even one exception per file that the administrator had not caught, the concept is validated. If it only finds things they already catch reliably, the value is time saved rather than risk reduced, which is a materially weaker pitch and should change the pricing and positioning.

### Assumptions most likely to make it fail

1. **That plan rules can be captured in a profile a non-programmer will maintain.** If encoding the plan's terms takes 45 minutes per plan, an 80-plan administrator will never do it. Setup cost is the make-or-break variable, and it must be tested before anything else. Mitigation: derive most of the profile from the administration software's existing plan specification export rather than asking the human.
2. **That administrators have authority to introduce tools.** In a 4-person firm, yes. In a 60-person firm or a PE-backed roll-up, IT and compliance approval may make a free desktop tool harder to adopt than a $17k platform.
3. **That the census file is the actual bottleneck.** It may be that the true bottleneck is *client responsiveness* — the calendar time waiting for a reply — in which case a faster validator saves hours but not weeks, and the value proposition shifts from throughput to error reduction.
4. **That firms will accept a tool with no liability backing.** These practitioners carry E&O insurance and are acutely aware of reliance risk. A free open-source tool that produces a compliance determination is something a cautious firm may refuse on principle. Positioning everything as a *worksheet* rather than a *conclusion* is not merely good marketing — it is a requirement.
5. **That SSN-bearing data can be handled acceptably.** Any hint of a cloud upload kills adoption. Offline-only is a hard constraint, not a preference.
6. **That the 2026 regulatory churn is a tailwind, not a distraction.** Cycle 4 restatements, mandatory Roth catch-up, and LTPT are consuming exactly the attention a new tool would need. The same churn is what makes the tools valuable — but timing an introduction into the middle of it is risky.

---

## 7. Cross-Industry Patterns

Five reusable patterns emerge from this market. Each names specific backlog markets it transfers to.

**Pattern 1 — Rule-profile-driven intake validator.** A per-client configuration file encodes the governing document's rules; a recurring inbound data file is validated against it; exceptions are split by who must answer them. The configuration, not the validation code, is the product.
*Transfers to:* Payroll service bureaus and small independent payroll providers · Third-party COBRA administrators serving small groups · Certified payroll and prevailing wage compliance service providers · Medicaid HCBS self-direction Financial Management Services (FMS) agencies · Retirement plan TPAs (origin).

**Pattern 2 — Source-system code crosswalk with unmapped-code alarm.** Map an external system's arbitrary codes to a governed internal taxonomy, require attestation, and alarm when a code appears that has never been classified. The alarm on *new* codes is the product; the mapping is the setup.
*Transfers to:* Workers' compensation class code and premium audit defense for high-payroll-churn employers · Premium audit and payroll classification consulting · Restaurant and hospitality bookkeeping (POS-to-GL daily sales journal) · Independent pharmacy third-party reconciliation and PBM claw-backs · Industrial distributors and metal service centers issuing material test reports.

**Pattern 3 — Two-source reconciliation at entity-and-period granularity with variance classification.** Totals-level tie-outs hide offsetting errors; the value is in matching at the finest grain and *classifying* each variance by probable cause so it can be routed.
*Transfers to:* E-commerce accounting specialists (Amazon/Shopify/Stripe settlement reconciliation) · Freight bill audit and payment for small shippers · Submetering and utility expense recovery service providers · Independent pharmacy third-party reconciliation and PBM claw-backs · Mortgage servicer payoff and lien release departments.

**Pattern 4 — Regulatory clock ledger.** An event creates an obligation with a computed deadline derived from rules rather than entered by hand; the ledger ages the obligations, applies transition rules, and escalates as deadlines approach.
*Transfers to:* Unclaimed property and escheat compliance service providers · Multi-state charitable solicitation registration compliance · Radiation safety officer services and portable gauge licensee compliance · Calibration and metrology service providers (gage recall intervals) · Fire protection ITM contractors under NFPA 25 (already covered — the pattern is confirmed to recur there).

**Pattern 5 — Branching annual attestation with year-over-year change log.** A recurring client questionnaire that prefills last year's answers, branches into sub-interviews, and whose primary output is the **diff** rather than the responses. The reviewer reads only what changed.
*Transfers to:* Third-party COBRA administrators serving small groups · Multi-state income and franchise tax nexus monitoring for small businesses · Government contracts administration at small govcons (clause and mod review) · Certificate-of-insurance compliance from the holder side · Employer immigration compliance and I-9 audit consultancies.

**Pattern 6 — Structured legal-determination worksheet that refuses to conclude.** For determinations that are genuinely legal conclusions (controlled group, worker classification, nexus), the tool gathers facts, shows the arithmetic, and explicitly declines to opine on ambiguous cases — escalating instead. This makes the tool usable by liability-conscious professionals who would reject an oracle.
*Transfers to:* Multi-state income and franchise tax nexus monitoring for small businesses · Employer immigration compliance and I-9 audit consultancies · Property tax consulting and assessment appeal firms · Elder law and Medicaid planning practices.

---

## 8. Sources and Confidence

### Verified findings — supported by primary or direct practitioner sources

| Finding | Source |
|---|---|
| 641,689 of 724,720 401(k)-type plans have fewer than 100 participants (2023 plan years) | [DOL EBSA Private Pension Plan Bulletin Abstract 2023](https://www.dol.gov/sites/dolgov/files/ebsa/researchers/statistics/retirement-bulletins/private-pension-plan-bulletins-abstract-2023.pdf) |
| The twelve most common 401(k) operational failures, including compensation definition (#3), excluded eligible employees (#6), untimely deposits (#8), and top-heavy minimums (#11) | [IRS 401(k) Plan Fix-It Guide](https://www.irs.gov/retirement-plans/401k-plan-fix-it-guide) |
| A real compensation-definition failure: GTL imputed income and other codes excluded contrary to the document; discovered at first audit; correction = 25–50% QNEC + 100% missed match + earnings, or retroactive amendment via VCP | [BenefitsLink — "Error with Compensation definition - how to fix?"](https://benefitslink.com/boards/topic/80259-error-with-compensation-definition-how-to-fix/) |
| Lost-earnings method hierarchy; DOL calculator restricted to VFCP filings; two-stage earnings-on-earnings; practitioner quote on cost exceeding participant benefit | [BenefitsLink — "Late deferrals: calculating lost earnings"](https://benefitslink.com/boards/topic/80658-late-deferrals-calculating-lost-earnings/) |
| Administrator caseload of 80+ small-employer plans; duties spanning Top Heavy, ADP/ACP, 401(a)(4), 410(b), cross-tested allocations, trust accounting, 5500-SF; tooling is Excel/Word/Outlook/PDF | [EmployeeBenefitsJobs — Retirement Plan Administrator/Consultant posting](https://employeebenefitsjobs.com/job/H177581) |
| Practitioner assessments of Relius, ASC, DATAIR, ftwilliam; support decline; migration experience | [BenefitsLink — "Researching Relius alternatives"](https://benefitslink.com/boards/topic/80151-researching-relius-alternatives/) |
| PensionPro pricing ($3–4k setup, $16–17k/year) described as steep; alternatives including custom in-house builds and "colored folders and a handheld label maker" | [BenefitsLink — "What workflow/client management system do you use?"](https://benefitslink.com/boards/topic/54053-what-workflowclient-management-system-do-you-use/) |
| Census required fields including hours of service, ownership %, family relationships to 1% owners, K-1/Schedule C income | [Benefits² Administrators — Retirement Plan Census Data Requirements](https://www.benefits2llc.com/giving_post/retirement-plan-census-data-requirements/) |
| Annual questionnaire covers related employers, compensation definition, and leased employees; "the incorrect application of the Plan's definition of compensation is one of the most common errors found upon IRS audits" | [The Retirement Advantage — Employer Questionnaire FAQs (PDF)](https://tra401k.com/wp-content/uploads/2018/11/Employer-Questionnaire-FAQs.pdf) |
| Cycle 4 pre-approved DC restatement submission window Feb 1 2024 – Jan 31 2025; amendment deadline Dec 31 2026 | [Spencer Fane — IRS Announces New Plan Amendment and Cycle 4 Restatement Deadlines](https://www.spencerfane.com/insight/irs-announces-new-plan-amendment-and-cycle-4-restatement-deadlines/) |
| Forfeiture 12-month use rule for plan years beginning on/after Jan 1 2024, with pre-2024 transition sweep; permitted uses must be in the document | [Barnes Dennig — Retirement Plan Forfeitures: New IRS Deadline Requirements](https://www.barnesdennig.com/retirement-plan-forfeitures-new-irs-deadline-requirements/) |
| Active 401(k) forfeiture class-action litigation through 2024–2025; DOL statement of position in 2025 | [Gibson Dunn — Update on ERISA 401(k) Plan Forfeiture Litigation](https://www.gibsondunn.com/update-on-erisa-401k-plan-forfeiture-litigation/) · [Holland & Knight — DOL Weighs in on 401(k) Forfeiture Class Actions](https://www.hklaw.com/en/insights/publications/2025/07/department-of-labor-weighs-in-on-401k-forfeiture-class-actions) |
| Root causes of late deferral deposits: manual uploads, file rejections, off-cycle payrolls, multiple recordkeepers, staff turnover; consequences include 15% excise tax and 5500 reporting | [Payroll Integrations — Late 401(k) Deferral Deposits](https://www.payrollintegrations.com/insights/blog/late-deferral-deposits-why-it-keeps-happening) |
| Payroll-to-recordkeeper reconciliation performed at participant and period level; commercial tooling exists but is aimed at CPA audit firms | [AuditMiner — Payroll and TPA Reconciliation](https://www.auditminer.com/payroll-and-tpa-reconciliation) |
| Controlled group / affiliated service group aggregation requirements and disqualification risk | [Employee Fiduciary — Is Your Company Part of a Controlled Group?](https://www.employeefiduciary.com/blog/is-your-company-part-of-a-controlled-group-you-need-to-know-or-risk-401k-plan-disqualification) · [Employee Benefits Law Group](https://www.employeebenefitslawgroup.com/controlled-group-401k-plan/) |
| ADP/ACP correction deadline mechanics and the 10% excise tax on late corrective distributions | [DWC — What Is the Deadline to Correct a Failed ADP/ACP Test?](https://www.dwc401k.com/blog/deadlines-for-adp-acp-tests) · [Employee Fiduciary — Options to Correct a Failed ADP/ACP Test](https://www.employeefiduciary.com/blog/when-adp-acp-testing-fails-401k-fiduciaries-should-understand-their-options) |
| Form 8955-SSA entry codes and the recurring confusion over previously-reported participants who were later paid out | [ASPPA — Form 8955-SSA Participant Statement: Clearing Up the Confusion](https://www.asppa-net.org/news/2017/11/form-8955-ssa-participant-statement-clearing-confusion/) · [IRS Instructions for Form 8955-SSA](https://www.irs.gov/instructions/i8955ssa) |
| SECURE 2.0 long-term part-time eligibility (500 hours / 2 consecutive years) | [RSM — Retirement plan changes for long-term, part-time employees](https://rsmus.com/insights/services/business-tax/retirement-plan-changes-for-long-term-part-time-employees.html) |
| Mandatory Roth catch-up for high earners effective 2026 (prior-year FICA wages above the indexed $145,000 threshold) | [Employee Fiduciary — 401(k) Catch-Up Contributions: Final SECURE 2.0 Rules](https://www.employeefiduciary.com/blog/401k-catch-up-contributions) · [Quarles — Roth Catch-Up Contributions in 2026](https://www.quarles.com/newsroom/publications/secure-2-0-act-retirement-plan-update-roth-catch-up-contributions-in-2026) |
| Expanded EPCRS self-correction under SECURE 2.0 | [Proskauer — SECURE 2.0 Delivers New Rules for Correcting Retirement Plan Errors](https://www.proskauer.com/blog/secure-20-delivers-new-rules-for-correcting-retirement-plan-errors) · [IRS Self-Correction Program FAQs](https://www.irs.gov/retirement-plans/self-correction-program-scp-faqs) |
| Cross-tested / new comparability allocation mechanics and the gateway minimum | [Employee Fiduciary — New Comparability 401(k) Plans](https://www.employeefiduciary.com/blog/new-comparability-401k-plans-are-they-right-for-your-small-business) · [Belfint — Minimum Allocation Gateway Test](https://employeebenefitplanaudit.belfint.com/basics-of-comparability-plans/) |
| Plan sponsor responsibility to track loans and hardship distributions | [IRS — It's up to plan sponsors to track loans, hardship distributions](https://www.irs.gov/retirement-plans/its-up-to-plan-sponsors-to-track-loans-hardship-distributions) |
| Active TPA firm-operator discussion topics: E&O insurance, SOC reports, firm sale, acquisitions, staffing structures, paperless workflow | [BenefitsLink — Operating a TPA or Consulting Firm forum](https://benefitslink.com/boards/forum/24-operating-a-tpa-or-consulting-firm/) |

### Strong inferences — well-grounded but not directly stated by a practitioner

- **2–5 hours per plan spent on census normalization and client query round-trips.** Derived from the 80+ plan caseload, the compressed Q1 window before the March 15 deadline, and the breadth of the required field list. No source states this figure. It is the number most worth measuring first.
- **The absence of systematic payroll-to-recordkeeper reconciliation for small plans.** Follows from small plans being audit-exempt under 100 participants and from AuditMiner's positioning toward audit firms. Not directly asserted anywhere.
- **New earnings codes are the dominant mechanism by which compensation-definition failures begin.** Consistent with the BenefitsLink case (GTL imputed income affecting "all employees") and with the annual-questionnaire model of control, but not documented as a mechanism by any source.
- **Firm size distribution (solo through 100 staff) and plans-per-firm.** Assembled from job postings, BenefitsLink thread content, and roll-up activity. No census of TPA firms was located; NIPA and ASPPA do not publish member firm counts publicly.
- **Offline-only operation is a hard adoption requirement.** Inferred from SSN-bearing data plus the existence of a BenefitsLink thread specifically about secure transmission of census information. Plausible but untested.

### Tentative hypotheses requiring practitioner validation

- **That a rule profile can be maintained by an administrator in under 10 minutes per plan.** Entirely unvalidated, and the single assumption most likely to sink CensusGuard.
- **That a plan sponsor will sign an earnings-code crosswalk attestation.** Attractive in theory; sponsors may balk at attesting to something they do not understand, and their payroll vendor may not readily produce a code list.
- **That TPAs would resell a forward-looking eligibility roster as a client deliverable.** Plausible given the industry's interest in "value-add services," but no evidence was found of anyone doing so today.
- **That multi-year hours history is obtainable for LTPT tracking at small clients.** Commentary universally treats LTPT as burdensome, but nothing found quantifies how often the underlying data simply does not exist.
- **That the calendar bottleneck is data quality rather than client responsiveness.** If it is responsiveness, every tool here saves hours without shortening the cycle — a materially different value proposition.
- **That free open-source positioning is an advantage rather than a liability signal** in a profession that carries E&O insurance and is unusually conscious of reliance risk.

---

*Report generated 2026-08-08 · Claim `11240bde` · Market research cycle for the free open-source business application catalog.*
