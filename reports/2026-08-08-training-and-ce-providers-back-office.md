# Training Organizations and Continuing-Education Providers — Back Office

**Market:** Training organizations and continuing-education providers
**Angle:** back-office
**Claim ID:** 9460e720
**Date:** 2026-08-08

---

## 0. Cycle header

### Why this assignment

The ledger held 323 open assignments across 179 markets with zero completed entries. The
selection rule prioritizes breadth over depth, then evidence availability, then angle
diversity. Three considerations decided it:

1. **Breadth.** The catalog to date is heavily weighted toward architecture/engineering/
   construction (7 of 24 reports), insurance and claims (4), transportation (2), and
   healthcare revenue cycle (2). Professional education is an entirely untouched vertical
   that sits *adjacent* to almost every market already covered — nearly every licensed
   profession in the completed reports (CPAs, engineers, insurance adjusters, nurses,
   attorneys, contractors) is a *consumer* of CE. Covering the supply side opens a market
   whose customers overlap the catalog's existing research base.
2. **Angle diversity.** Completed angles skew to `core-practitioner-workflow` (9 of 24).
   `back-office` had 5. More importantly, for CE providers the back office *is* the
   regulated function — the teaching is unregulated craft, the recordkeeping and filing is
   where the license risk lives. This is one of the rare markets where "back-office" is the
   high-stakes angle rather than the residual one.
3. **Evidence quality.** Every obligation in this market is written down in public
   regulatory text, and the *file formats* providers must produce are published. That means
   findings are verifiable rather than inferred — the strongest possible base for
   recommending software. This turned out to be correct: the research below cites exact
   deadlines, retention periods, field-level file specifications, and a published list of
   the top five audit deficiencies.

Assignments considered and passed over: *Small CPA tax preparation practices* (crowded
incumbent software: Drake, Lacerte, UltraTax — most pain is inside tools we cannot displace);
*Marketing and creative agency account and production management* (the honest answer there is
"generic project management," which the brief explicitly tells us to avoid); *Structural
engineering firms* (more AEC, and the catalog is already saturated there).

**Backlog remaining after this claim: 323 assignments.**

---

## 1. Market examined

### Who is in this market

"Continuing-education provider" is a regulatory status, not an industry. The entities holding
it are diverse, and that diversity is itself the market structure:

| Provider type | Typical size | Examples |
|---|---|---|
| Independent CE publishers / course shops | 1–15 staff | ce-classes.com, NetCE, small self-study catalogs |
| Trade and professional associations (state and specialty) | 3–40 staff, 1–3 on education | State CPA societies, state bar sections, specialty nursing associations |
| Training companies serving a trade | 5–50 staff | Insurance CE schools, contractor CE schools, safety training firms |
| Vendors/manufacturers running CE as marketing | 1–3 people, part-time | AIA CES providers, product manufacturers, law-firm-hosted CLE |
| Hospital/health-system education departments | 2–10 staff | ACCME-accredited providers, ANCC provider units |
| University and community-college continuing-ed units | 5–30 staff | CE divisions issuing IACET CEUs |
| Consultancies and firms offering CE to clients | education is a side function | Accounting firms with NASBA sponsor IDs, law firms with MCLE approval |

### The professional this report is about

The **CE administrator** — variously titled Continuing Education Coordinator, Education
Manager, Program Specialist, CME Coordinator, Accreditation Manager, or (at the small end)
"the office manager who also does the CE." Characteristics observed consistently:

- Frequently **one person**, sometimes 0.5 FTE, rarely more than three.
- Not a developer; lives in Excel, Outlook, a registration platform, and a stack of
  regulator web portals.
- Holds the organization's **regulatory approvals** — meaning a clerical mistake is a
  license-level risk, not just an annoyance.
- Turnover in the role is high, and the institutional knowledge (which board wants which
  file, by when) leaves with them.

### Organization size most likely to benefit

**2–40 total staff, delivering 10–300 credit-bearing sessions per year, holding between 3 and
40 separate regulatory approvals.** Below that, the volume does not justify tooling. Above
it, the organization has bought a $30k–$150k/yr accreditation LMS. The gap in the middle is
wide and poorly served — which is exactly the catalog's target.

---

## 2. How the work is performed

The back office of a CE provider is a **repeating cycle per activity**, wrapped in an
**annual approval-maintenance cycle**, both underlaid by a **retention obligation**. All three
run on spreadsheets at the target organization size.

### 2.1 Before the activity — approval and setup

1. **Confirm the provider approval is current** for every jurisdiction where credit will be
   claimed. Approvals are per-board, per-profession, per-state, and they expire on
   independent schedules. Texas TDLR provider registration is "valid for one year from the
   date of issuance." IRS CE provider status carries a **$650 annual fee** payable each
   calendar year. New York charges **$50 per instructor** application and **$50 per renewal**.
2. **Confirm the course approval is current.** Some boards approve courses permanently
   (North Carolina insurance: course approvals "are not subject to renewal," though a
   provider that runs no course for a full calendar year is deactivated). Others expire:
   IRS program numbers expire "12/31 of the third year after issuance," and Annual Federal
   Tax Refresher program numbers expire **every December 31**.
3. **File pre-presentation notices.** Washington State requires a "10-day notice of course
   presentation" filed minimum 10 and maximum 60 days before each classroom or webinar
   session held in the state — per session, not per course.
4. **Assemble the instructor file.** Resumes/CVs and qualification evidence, plus — for
   NASBA sponsors — documented credentials for authors, developers, instructors, *and*
   program reviewers.
5. **Compute the credit award.** Under the NASBA Statement on Standards, one credit is 50
   minutes; credits after the first may be awarded in one-fifth or one-half increments; and
   self-study totals must be **rounded down**, never up. Breaks, introductions, and
   administrative time are not creditable — miscounting them is an audit finding.

### 2.2 During the activity — evidence capture

This is where the compliance burden actually bites, and it differs by delivery method:

- **Group live:** sign-in *and* sign-out, arrival and departure times, handling of late
  arrivals and early departures, monitor attestations. Washington requires attendance
  registers with signatures and arrival/departure times.
- **Group internet based (webinar):** a real-time attendance-monitoring mechanism, plus
  "at least three instances of interactivity completed by the participant per CPE credit,"
  distributed at irregular intervals so participants cannot anticipate them. Participants
  must be told in advance how many polls are required and how many must be answered
  correctly for full credit. Washington goes further and requires the webinar record to
  contain "names, phone numbers, WAOIC numbers, log-in/log-out times, chat history, and
  polling responses."
- **New York insurance:** photo-ID inspection before admission, arrival times, sign-out
  times, return-from-meal-break times, and **100% attendance with no partial credit
  permitted**.
- **Self-study:** a final exam with a passing grade (70% in New York), plus pilot-test
  results or word-count formula calculations retained as evidence for NASBA.

### 2.3 After the activity — the filing scramble

Within a window measured in **days**, the administrator must:

1. Reconcile registration data against actual attendance data.
2. Compute per-attendee credit, including partial credit where allowed and zero credit where
   not.
3. Generate certificates containing board-specific required elements.
4. File the roster with each board, in each board's format, through each board's portal.
5. Pay per-roster fees where they exist.
6. Answer the inevitable "my credit isn't showing" emails.

**The deadlines are short and they are not aligned:**

| Regime | Filing deadline after course completion |
|---|---|
| Texas TDLR | **7 days**, electronically via TDLR portal |
| Washington OIC (insurance) | **10 days** — "repeated violations of the 10-day roster rule can result in an enforcement action" |
| Ohio CSWMFT (social work/counseling/MFT) | **14 business days**, via CE Broker |
| North Carolina DOI (insurance) | **15 business days**, via Sircon |
| New York DFS (insurance) | roster within **2 weeks**; completion record filed electronically within **30 days** |
| Florida (CE Broker) | **30 days** |
| ACPE / CPE Monitor (pharmacy) | provider has **60 days** from course date to submit to ACPE |
| California MCLE (attorneys) | electronic attendance records within **60 days** |
| District of Columbia (CE Broker) | **90 days** |
| IRS CE providers | quarterly by Mar 31 / Jun 30 / Sep 30, then **within 10 business days of each program** from Oct 1–Dec 31 |

A provider holding approvals in ten jurisdictions is running ten different clocks against a
single roster.

### 2.4 The file formats are not interchangeable

This is the single most under-appreciated fact about this market. The published CE Broker
Excel upload specification is not a spreadsheet in any normal sense — it is a **positional
fixed-format record layout that happens to live in .xls**:

- Six record types in order: Provider (1 per file), Course (≥1), Attendee (≥1 per course),
  Partial Credit (optional), Course Control (≥1), End-of-File (1).
- "Each row, or record, is allowed a maximum length of **100 characters**."
- Attendee records carry a 4-character **profession code** plus a 9-digit license number,
  because "the License # assigned by PRAES is a 4+9 digit alphanumeric number."
- State is encoded as a literal string: `State=FL`.
- Dates are `mm/dd/ccyy`. Course Control carries a 4-digit attendee count; EOF carries a
  6-digit course count and a 6-digit total record count.
- Files are rejected pre-import for "Incorrect Record Length," "Invalid Record Type,"
  "The File must contain only one Provider record," "License Number not found on the DOH/MQA
  Licensing Database," "Completed hours cannot be greater than offered hours."
- Rows are rejected post-import for duplicate attendees within a course publication, license
  numbers absent from the licensing database, completion dates mismatched with the
  publication end date, subject-area codes outside the course's approved areas, and partial
  credit not permitted by that licensee's board.
- A Roster Summary returns "within one minute" with rejected fields highlighted in red for
  correction and resubmission.

Meanwhile the IRS requires a **different** structure — attendee first and last name (matching
the PTIN record exactly), attendee PTIN, program number, hours, and completion date — via an
XLSX template with a **2MB file size cap**, recommended for batches of 25+, with erroneous
records requiring deletion and a **24-hour wait** before resubmission. California MCLE
requires the State Bar's own Attendance Record Upload Template with its own General
Instructions tab, submitted through the MCLE Attendance Record Upload Form. North Carolina
routes through Sircon and charges **$2.00 per credit hour per student** in roster fees.

**One roster. Six or ten incompatible destination formats. Zero shared tooling.**

### 2.5 The retention obligation

Records must be kept — but for wildly different periods, and nobody has one clock:

| Regime | Retention |
|---|---|
| Texas TDLR | 2 years after course completion |
| Washington OIC | 3 years |
| New York DFS | 3 years |
| North Carolina DOI | 3 years |
| Minnesota Board of Social Work | 3 years |
| California MCLE | **4 years** for attendance records; 1 year for evaluations |
| IRS CE providers | **4 years** after last completion date (syllabi, materials, evaluations, certificates, attendance) |
| NASBA / CPA-facing | CPAs retain 5 years; sponsors retain Standard No. 24 documentation |

IACET has separately flagged the collision between GDPR "right to be forgotten" requests and
the obligation to retain learner records — an unresolved tension for any provider with
international learners.

### 2.6 Software currently in use

- **Registration/e-commerce:** Eventbrite, Cvent, Wild Apricot, association AMS modules.
- **Delivery:** Zoom Webinars, Teams, GoToWebinar; Moodle, Thinkific, LearnDash for self-study.
- **Accreditation LMS (the "real" tools):** EthosCE, CloudCME, Highmarks CE, CE21, Blue Sky,
  Cadmium, Arlo, CEU Events. EthosCE lists an entry point around **$1,750 per installation**
  with tiers "not readily available, requiring a custom quote" — the standard pattern in this
  segment is opaque pricing, annual contracts, and implementation projects.
- **Everything else:** Excel. Arlo's own marketing describes providers where "learner details,
  payments, and course records are scattered across spreadsheets, email threads," and cites a
  customer spending **up to 30 hours a week** on administrative process.

---

## 3. Most important problems (ranked)

### P1 — One roster must become N incompatible regulator filings, each on its own short clock

**Who:** The CE administrator at any provider holding approvals in more than two jurisdictions.
**When:** After every single credit-bearing activity, 10–300 times per year.
**Currently handled by:** Manually re-keying or hand-transforming an attendee list into each
board's portal or template — CE Broker's positional .xls, the IRS XLSX template, the CalBar
template, Sircon's web forms, TDLR's PIN-protected page.
**Why inadequate:** The transformations are mechanical but unforgiving. CE Broker rejects on
row length, record type, record counts, license-database lookup failure, and subject-code
mismatch. The IRS returns records with invalid PTINs and imposes a 24-hour wait before
resubmission. Every rejection is a manual correction cycle against a 7–15 day statutory clock.
**Frequency:** Every activity × every jurisdiction. For a mid-sized provider this is the single
highest-volume recurring back-office task.
**Cost:** Estimated 30–90 minutes per activity per jurisdiction at the manual end. At 60
activities/year across 6 jurisdictions, that is 180–540 hours annually. Late or failed filings
carry enforcement exposure (Washington explicitly), and per-roster fees mean errors can also
cost cash (NC's $2/credit-hour/student is charged on what you file).
**Evidence:** Published deadlines and file specifications from CE Broker, IRS, CalBar, NCDOI,
NY DFS, TDLR, WA OIC — all cited in §8. This is verified, not inferred.

### P2 — Approvals, program numbers, and instructor authorizations expire silently

**Who:** The person who holds the provider's regulatory approvals.
**When:** Continuously; discovered at the worst possible moment.
**Currently handled by:** A spreadsheet, a calendar reminder, or nothing.
**Why inadequate:** The expirations are numerous, independent, and invisible until a learner's
credit is denied. **The clearest evidence in this entire report:** ce-classes.com, a real CE
provider, publicly lists its approvals — and multiple approval numbers on that page carry
**expired dates**: ASWB #1142 (expired 1/5/2020), NBCC ACEP #6320 (expired 4/30/2019), Texas
Board of Social Work Examiners #5674 (expired 4/30/2020), CCAPP (expired 02/2021), Ohio
#RCST031201 (expired 5/31/2021), California BRN CEP 15647 (expired 11/30/2022). That is a
provider carrying **12 distinct approvals** across national bodies and 8 state boards, with the
public-facing register visibly out of date. If the public page is stale, the internal tracking
almost certainly is too.
**Frequency:** Each approval renews annually to triennially; a 12-approval provider faces
roughly one renewal event per month, plus IRS program numbers expiring on 12/31 of their third
year and AFTR numbers expiring every year.
**Cost:** Renewal fees are small ($50 NY instructor, $650 IRS annual). The real cost is a
**lapse**: credit awarded under a dead approval is credit the learner may not be able to use,
which means refunds, reissued certificates, reputational damage with the board, and potentially
a re-application rather than a renewal.
**Evidence:** Verified — expired numbers visible on a live provider site; TDLR one-year
registration; IRS three-year program-number expiry; NY per-instructor renewal fees.

### P3 — Webinar telemetry does not equal audit-grade attendance evidence, and the gap is manual

**Who:** Any provider delivering live online credit.
**When:** After every webinar.
**Currently handled by:** Exporting the Zoom/Teams participant report and eyeballing it.
**Why inadequate:** The raw export is the wrong shape. Attendees appear multiple times when
they drop and rejoin; registration and participant reports must be reconciled; custom
registration answers (license number, state, profession) must be read per row. One vendor
describes the manual job as needing to "manually de-duplicate attendance data, reconcile
registration and participant report and scroll through each custom answer response," then
determine eligibility from cumulative duration plus responses. Separately, the credit rule is
not "did they attend" — under NASBA it is minutes-based with round-down and fractional
increments, gated on completing at least three interactivity instances per credit; under New
York insurance it is all-or-nothing at 100% attendance; under CE Broker it may be a partial-
credit record with subject-area codes.
**Frequency:** Every live online session — for many providers, weekly.
**Cost:** 1–3 hours per webinar of clerical reconciliation, plus a persistent error rate.
Under-awarding generates complaint traffic; over-awarding is a compliance finding.
**Evidence:** Verified — vendor description of the manual workflow, NASBA interactivity and
increment rules, WA OIC's explicit requirement that webinar records include log-in/log-out
times, chat history, and polling responses.

### P4 — Attendance documentation fails audits in a small, known, repeating set of ways

**Who:** Every registered sponsor subject to periodic compliance audit.
**When:** On audit selection — random and unannounced (NY DFS may conduct "announced or
unannounced audits").
**Currently handled by:** Retrieving sign-in sheets and hoping.
**Why inadequate:** NASBA publishes the **top five group-live attendance deficiencies**, and
they are all documentation-shape problems rather than conduct problems:
1. Supporting documentation does not match the monitoring procedure the sponsor described on
   the audit form.
2. Records lack duration, time-out stamps, or an explanation of how late arrivals and early
   departures are handled — "a scanning system capturing only check-in times is insufficient."
3. Participant self-certification alone is not sufficient.
4. Written policies are too vague — "sign-in sheets" without sign-out, facilitator
   verification, or break management.
5. Where delivery is outsourced to a client, accountability stays with the registered sponsor.
A related published list adds promotional-material omissions, missing instructor/reviewer
credentials, and CPE calculation errors (wrong rounding, crediting breaks or introductions).
**Frequency:** Low per provider, catastrophic per occurrence.
**Cost:** Remediation cycles, possible suspension or revocation of sponsor status. New York's
Superintendent may impose "fine or suspension or revocation of approvals"; California's State
Bar may suspend or revoke provider approval for failure to maintain records.
**Evidence:** Verified and unusually specific — the regulator publishes the failure modes.

### P5 — Certificates carry different mandatory contents per board, and must be reproducible for years

**Who:** Administrator; and the learner who lost theirs.
**When:** After each activity, then unpredictably for years.
**Currently handled by:** Word mail-merge, or the registration platform's generic certificate.
**Why inadequate:** Required elements differ materially. NASBA: sponsor name, participant name,
course title, date, location, instructional delivery method, credits by field of study, sponsor
ID number, state registration number. California MCLE: provider name, activity title and date,
total hours **broken out by credit category** (ethics, elimination of bias, implicit bias,
wellness, technology, civility, specialization), activity type (participatory vs. self-study),
and the licensee's name and bar number — with different labels for participatory
("Certificate of Attendance") versus self-study ("Certificate of Completion"). Minnesota social
work: sponsor name, title and date, clock hours, **names of presenters**. The IRS adds a
negative requirement — PTINs must appear on the submitted record but **must not** appear on the
certificate. BACB ACE Providers must "provide replacement certificates to participants when
requested, **up to 3 years after the event**."
**Frequency:** Every activity; reissues indefinitely.
**Cost:** Modest per instance, high in aggregate; a template that silently omits a required
element produces a defect across every certificate issued under it.
**Evidence:** Verified from primary sources for four independent regimes.

### P6 — Retention clocks conflict and nobody knows what can be destroyed

**Who:** Administrator, and whoever inherits the shared drive.
**When:** Never, which is the problem.
**Currently handled by:** Keeping everything forever in nested folders.
**Why inadequate:** Retention ranges from 2 years (TX) to 4 years (CA MCLE, IRS) with 3 years
common, and different artifact classes within one regime have different clocks (CA MCLE:
attendance 4 years, evaluations 1 year). IACET has flagged that indefinite retention now
collides with erasure rights.
**Frequency:** Continuous, low-salience.
**Cost:** Low direct cost; real risk is over-retention of licensee PII and inability to produce
the *right* record on audit because it is buried among ten years of the wrong ones.
**Evidence:** Verified retention periods; the GDPR tension is documented by IACET.

### P7 — Roster fees and reporting costs are unbudgeted and unreconciled

**Who:** Whoever signs the checks.
**When:** Per filing and annually.
**Currently handled by:** Paying invoices as they arrive.
**Why inadequate:** Fees are per-transaction and volume-driven — NC insurance at $2.00 per
credit hour per student (a 4-credit course with 40 students = $320 in filing fees alone), TDLR
at $5 per licensee for barber/cosmetology and tow providers, IRS at $650/year. These are
rarely modeled into course pricing.
**Frequency:** Per filing.
**Cost:** Direct cash, small but systematically ignored in pricing decisions.
**Evidence:** Verified fee schedules.

---

## 4. Application opportunities

### A1 — Board Filing Formatter ("one roster in, every regulator format out")

- **User:** CE administrator at a provider holding 3–15 approvals.
- **Problem solved:** P1.
- **Current workflow:** Export attendees → hand-build a CE Broker positional .xls → separately
  hand-build the IRS XLSX → separately fill the CalBar template → key the rest into portals →
  fix rejections against a 7–15 day clock.
- **Proposed workflow:** Maintain one canonical roster CSV (name, license/PTIN/bar number,
  profession, state, minutes attended, credit awarded, completion date). Select target
  regimes. The tool emits a validated, ready-to-upload file per regime plus a pre-flight
  exception list.
- **Inputs:** Canonical roster CSV; a provider profile (provider numbers per board, course
  tracking numbers, publication end dates, profession/subject codes).
- **Outputs:** CE Broker-compliant .xls with all six record types in order, ≤100-char rows,
  correct control and EOF counts; IRS XLSX under 2MB with batch splitting; CalBar template;
  generic CSVs for portal-paste regimes; a rejection-risk report.
- **Essential features:** Record-length enforcement; profession/subject-code lookup tables;
  date normalization to `mm/dd/ccyy`; duplicate-attendee detection within a course
  publication; completion-date vs. publication-end-date consistency check;
  hours-awarded ≤ hours-offered check; automatic 2MB batch splitting for IRS.
- **Excluded from v1:** Direct API/FTP submission (CE Broker offers web services and FTP, but
  credentialed integration is a v2 paid-customization concern, not a free-base-version
  concern); registration; payments; content delivery.
- **AI:** **Inappropriate.** These are deterministic format transformations. AI here would
  add nondeterminism to a task whose entire value is being exactly right.
- **Why not a spreadsheet:** A spreadsheet can hold the data but cannot enforce a six-record-
  type positional layout with per-row character caps, cross-record count reconciliation, and
  conditional partial-credit records. People do attempt this in Excel — that is precisely why
  rejections happen.
- **Complexity:** Medium. **Learning difficulty:** Low — it is an import/export screen.
- **Value:** Removes the 30–90 min/filing transformation and most rejection cycles. At 6
  jurisdictions × 60 activities, plausibly 150–400 hours/year.
- **Risks:** Format drift — regulators change templates. Mitigate by making format definitions
  external, versioned, data-driven files rather than code, so a community can maintain them.
  Handles licensee PII (names, license numbers) — must be local-first, no cloud upload by
  default.
- **Substitutes:** Accreditation LMSs (EthosCE, CloudCME, CE21) do this *if* you run your whole
  program inside them. Nothing serves the provider who registers in Eventbrite and delivers on
  Zoom.
- **Customization potential:** High — a paid engagement per additional board format, or a
  connector to a specific AMS export.

### A2 — Approval & Credential Expiration Register

- **User:** The holder of the provider's regulatory approvals.
- **Problem solved:** P2.
- **Current workflow:** A spreadsheet nobody opens, or memory.
- **Proposed workflow:** Register every approval — provider approvals, course approvals, program
  numbers, instructor authorizations — with issuing body, number, effective and expiry dates,
  renewal fee, renewal lead time, renewal URL, and the evidence file. The tool produces a
  rolling renewal calendar, a 90/60/30-day alert digest, and a **public-facing approval block**
  the provider can paste onto its website that is generated from live data rather than
  hand-maintained.
- **Inputs:** Approval records (initially typed or CSV-imported); optional renewal receipts.
- **Outputs:** Renewal calendar (ICS export); alert digest; annual renewal fee forecast;
  generated approvals list; "at-risk activities" report flagging any scheduled future activity
  whose governing approval expires before the activity date.
- **Essential features:** That last one is the differentiator — cross-referencing the *activity
  calendar* against the *approval calendar* catches exactly the ce-classes.com failure mode.
- **Excluded from v1:** Automated renewal filing; document management beyond file links.
- **AI:** **Optional and marginal.** Could parse an approval letter PDF to pre-fill dates.
  Nice-to-have, not the value.
- **Why not a spreadsheet:** A spreadsheet *can* do this and many providers nominally have one.
  The evidence says it fails anyway — because a spreadsheet does not notify, does not
  cross-check against the teaching calendar, and does not regenerate the public page. The
  differentiator is the alerting and cross-check, not the storage.
- **Complexity:** Small. **Learning difficulty:** Very low.
- **Value:** Prevents lapse events. Low time savings, high risk reduction.
- **Risks:** Minimal. No sensitive learner data at all — this is provider metadata.
- **Substitutes:** Generic compliance calendars; nothing purpose-built at this price point.
- **Customization potential:** Moderate — seeding the register with a specific provider's real
  approval set is a natural paid onboarding.

### A3 — Webinar Attendance-to-Credit Reconciler

- **User:** Administrator running live online credit.
- **Problem solved:** P3.
- **Current workflow:** Download Zoom participant CSV, poll report, and registration report;
  manually dedupe rejoins, sum minutes, read custom-question answers, decide eligibility,
  build the award list.
- **Proposed workflow:** Drop in the three exports. The tool joins them on email, collapses
  multiple join/leave rows into cumulative attended minutes, pulls license number / state /
  profession from registration custom fields, applies a selected board's credit rule, and emits
  an award list plus an exception list.
- **Inputs:** Zoom/Teams/GoToWebinar participant export, poll report, registration export;
  a session definition (scheduled credit minutes, break windows, required poll count).
- **Outputs:** Canonical roster (feeding A1 directly); exception report (attended but no license
  number; below threshold; missed poll threshold; duplicate registrations; name mismatches);
  an **audit-evidence sheet** listing per-participant log-in/log-out times, cumulative minutes,
  poll responses, and the credit calculation applied.
- **Essential features:** Rejoin collapsing; break-window exclusion; per-board rule profiles —
  NASBA 50-minute with round-down and 1/5 or 1/2 increments plus ≥3 interactivity instances per
  credit; all-or-nothing 100%-attendance profiles (NY insurance); partial-credit profiles with
  subject-area allocation (CE Broker).
- **Excluded from v1:** Live in-session monitoring; running the webinar; certificate design
  (that's A5).
- **AI:** **Inappropriate.** Arithmetic and joins.
- **Why not a spreadsheet:** The dedupe-and-sum across variable-length join/leave rows joined
  to a second export and then run through fractional rounding rules is exactly the kind of
  thing that gets done wrong in Excel every week. It's a 200-line script that pays for itself
  the first Tuesday.
- **Complexity:** Small-to-medium. **Learning difficulty:** Low.
- **Value:** 1–3 hours per webinar, plus a defensible audit artifact that directly answers
  NASBA deficiency #2 ("records lack duration, time-out stamps") and WA's webinar record
  requirements.
- **Risks:** Platform export schema changes; PII in exports (keep local).
- **Substitutes:** Salepager, CertFusion, Certopus, CEU Events address slices of this, mostly
  as SaaS tied to certificate delivery. None outputs a regulator-ready roster *and* an
  audit-evidence sheet.
- **Customization potential:** High — per-platform ingest adapters and per-board rule profiles
  are natural paid work.

### A4 — Audit Evidence Package Builder

- **User:** Administrator facing a compliance audit or self-certification renewal.
- **Problem solved:** P4.
- **Current workflow:** Search the shared drive for weeks.
- **Proposed workflow:** Select an activity. The tool assembles the standard evidence binder
  and — more usefully — produces a **manifest of what is missing**, mapped to the published
  deficiency list.
- **Inputs:** Activity record; links to attendance evidence, agenda, instructor CVs,
  promotional material, evaluations, certificates issued, credit-calculation worksheet.
- **Outputs:** Indexed PDF binder; gap manifest keyed to the five NASBA deficiency categories;
  a written attendance-monitoring policy statement generated from the actual procedure recorded
  for that activity (addressing deficiency #1, "documentation does not match the described
  procedure," and #4, "vague policies").
- **Essential features:** The gap manifest. Deficiency-mapped checklists per regime.
- **Excluded from v1:** Document storage — link to existing files rather than becoming a DMS.
- **AI:** **Optional, genuinely useful in one narrow place** — checking promotional material
  against the required-disclosure list (learning objectives, prerequisites, delivery method,
  credit hours, refund/cancellation policy, complaint resolution). That is interpretation of
  free text against a checklist, which conventional code does poorly. Everything else should be
  rules.
- **Why not a spreadsheet:** A checklist could be a spreadsheet. Binder assembly and free-text
  disclosure checking could not.
- **Complexity:** Medium. **Learning difficulty:** Moderate.
- **Value:** Converts a multi-week scramble into a day; more importantly, surfaces gaps *before*
  the audit rather than during it.
- **Risks:** Must not imply a compliance guarantee. Frame output as preparation aid, not
  assurance. Liability language matters here.
- **Substitutes:** The LMS vendors pitch this as a reason to buy the whole platform.
- **Customization potential:** High — per-accreditor checklist packs.

### A5 — Board-Compliant Certificate Batch Issuer

- **User:** Administrator; secondarily the learner requesting a reissue.
- **Problem solved:** P5.
- **Current workflow:** Word mail-merge from a template of uncertain provenance.
- **Proposed workflow:** Certificate templates are defined per regime with **required-element
  validation** — the tool refuses to generate a CalBar certificate that lacks a credit-category
  breakdown or the participatory/self-study designation, refuses a NASBA certificate missing
  the sponsor ID or delivery method, and refuses to print a PTIN on an IRS certificate.
  Generates a batch of PDFs, logs every issuance with a verification code, and keeps a reissue
  log.
- **Inputs:** Canonical roster; provider identity block; regime selection.
- **Outputs:** Per-attendee PDFs; a manifest; an issuance/reissue log; optionally a static
  verification lookup file.
- **Essential features:** Required-element validation per regime; credit-category breakdown;
  participatory/self-study labeling; reissue tracking against BACB's 3-year replacement
  obligation.
- **Excluded from v1:** Email delivery infrastructure; digital badging; learner portals.
- **AI:** **Inappropriate.**
- **Why not a spreadsheet:** Mail-merge is the current answer and it produces the defect —
  a spreadsheet has no concept of "this board requires these nine fields."
- **Complexity:** Small. **Learning difficulty:** Very low.
- **Value:** Moderate time savings, meaningful defect elimination — a bad template propagates
  to every certificate issued under it.
- **Risks:** PII on generated documents; local-first generation.
- **Substitutes:** Certifier, Certopus, LMS certificate modules — all generic, none
  board-rule-aware.
- **Customization potential:** Moderate — branded templates, additional regimes.

### A6 — CPE/CE Credit Calculation Worksheet

- **User:** Program planner setting the credit award before marketing the course.
- **Problem solved:** The credit-calculation subset of P4 (published as a top-five audit
  failure: "incorrect rounding methods, failing to round down, or crediting breaks/
  introductions").
- **Current workflow:** Mental arithmetic on an agenda.
- **Proposed workflow:** Enter the agenda as timed segments, each flagged creditable or not
  (welcome, breaks, lunch, sponsor remarks, Q&A). Select regime. The tool computes creditable
  minutes, applies 50-minute conversion, applies round-down and permitted increments, and
  prints a **dated calculation worksheet** — which is exactly the artifact auditors ask for.
- **Inputs:** Agenda segments; regime.
- **Outputs:** Credit figure; signed/dated calculation worksheet; a warning list (e.g. "breaks
  included in creditable time," "total rounds down to 2.5 not 2.6").
- **Essential features:** Multi-regime rules; the printable worksheet; a "what to advertise"
  output so promo material and certificate agree.
- **Excluded:** Scheduling, room booking, speaker management.
- **AI:** **Inappropriate.**
- **Why not a spreadsheet:** Honestly, this one *could* be a spreadsheet — and that is a fine
  v0. The advantage of a small app is the multi-regime rule library and the fact that the
  worksheet output is a compliance artifact rather than a working file. This is the strongest
  candidate in the set for a "smart spreadsheet" deliverable rather than an application.
- **Complexity:** Small. **Learning difficulty:** Very low.
- **Value:** Small per use, but it eliminates a *published* audit failure category and takes
  about a day to build.
- **Risks:** Rule accuracy; cite the source rule inline on the worksheet.
- **Substitutes:** None specific.
- **Customization potential:** Low-moderate.

### A7 — Roster Pre-Flight Validator (registration data hygiene)

- **User:** Administrator, at registration time rather than filing time.
- **Problem solved:** The upstream cause of P1's rejections — bad license numbers collected at
  registration.
- **Current workflow:** Discover the bad license number when the board rejects the row, weeks
  later, against a deadline.
- **Proposed workflow:** Validate the attendee list *as soon as registration closes*, against
  per-board license-number format rules (length, alphanumeric structure, profession-code
  prefix, PTIN pattern, bar-number pattern), flag missing/implausible entries, and produce a
  chase list of attendees to email before the session.
- **Inputs:** Registration export.
- **Outputs:** Clean list; chase list with per-attendee reason; a paste-ready reminder email.
- **Essential features:** Format rule library; profession-code mapping; duplicate detection;
  name-format normalization (the IRS requires the name exactly as it appears on the PTIN
  record).
- **Excluded:** Live lookups against board licensee databases — those are inconsistently
  available and would create a fragile-integration dependency the brief warns against. Format
  validation catches most of it.
- **AI:** **Inappropriate.** Regex and lookup tables.
- **Why not a spreadsheet:** Conditional formatting can approximate it; a rule library across
  a dozen boards cannot live in conditional formatting maintainably.
- **Complexity:** Small. **Learning difficulty:** Very low.
- **Value:** Converts post-deadline rejection cycles into pre-session email chases.
- **Risks:** False confidence — format-valid does not mean database-valid. Say so in the UI.
- **Substitutes:** None at this granularity.
- **Customization potential:** Moderate.

### A8 — Retention Clock & Disposition Scheduler

- **User:** Administrator; records owner.
- **Problem solved:** P6.
- **Current workflow:** Keep everything.
- **Proposed workflow:** Register each activity with its governing regimes; the tool computes
  the controlling retention date per artifact class (attendance vs. evaluations vs. materials)
  as the **maximum across applicable regimes**, and produces an annual disposition list of what
  is now eligible for destruction — plus a hold list for anything under audit or dispute.
- **Inputs:** Activity register; regime mapping.
- **Outputs:** Retention schedule; annual disposition list; legal-hold register; an erasure-
  request response worksheet reconciling a learner's deletion request against live retention
  obligations.
- **AI:** **Inappropriate.**
- **Why not a spreadsheet:** It could be, with effort. The max-across-regimes computation and
  the erasure-conflict worksheet are what justify code.
- **Complexity:** Small. **Learning difficulty:** Low.
- **Value:** Risk reduction and PII minimization rather than time savings.
- **Risks:** Advising destruction is consequential — output must be a *recommendation with the
  governing rule cited*, requiring human sign-off.
- **Substitutes:** Enterprise records-management, wildly oversized for this market.
- **Customization potential:** Moderate.

### A9 — Regulator Rule-Card Extractor

- **User:** The provider expanding into a new state or profession; also the maintainer of the
  A1 format library.
- **Problem solved:** The research burden behind everything above — nobody has a consolidated,
  current, machine-readable table of "board → filing deadline → format → retention → credit
  increment rules."
- **Current workflow:** Read the board's provider packet PDF and take notes.
- **Proposed workflow:** Point the tool at a board's provider-requirements document. It extracts
  a structured rule card — filing deadline, submission channel, required fields, retention
  period, credit increment rules, partial-credit allowance, certificate elements, fees — each
  field carrying a **quoted source snippet and page reference**. A human verifies and accepts.
- **Inputs:** Regulator PDF or page.
- **Outputs:** Draft rule card (JSON/YAML) with citations; a diff against the previously
  accepted card when re-run, so format and deadline changes get caught.
- **AI:** **Necessary and appropriate.** This is exactly the case the brief carves out —
  extraction and classification from unstructured regulatory prose, where conventional parsing
  fails. Crucially, AI produces a *draft with citations for human acceptance*, never a
  self-applying rule.
- **Why not a spreadsheet:** Reading PDFs is not a spreadsheet task.
- **Complexity:** Medium. **Learning difficulty:** Moderate.
- **Value:** Indirect but compounding — it is the maintenance engine for A1/A5/A6/A8.
- **Risks:** **Highest-risk concept in the set.** A hallucinated deadline is worse than no
  deadline. Mandatory mitigations: every field must carry a verbatim quote; unverified cards
  must be visibly marked; the tool must never be the sole authority.
- **Substitutes:** Compliance-content vendors sell curated regulatory databases at enterprise
  prices.
- **Customization potential:** High, but sell it as *research assistance*, never as a
  compliance guarantee.

---

## 5. Opportunity ranking

Scored 1–5 on ten criteria (max 50).

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of build | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| A3 | Webinar Attendance-to-Credit Reconciler | 5 | 5 | 5 | 4 | 4 | 4 | 4 | 4 | 5 | 5 | **45** |
| A2 | Approval & Credential Expiration Register | 5 | 3 | 5 | 5 | 5 | 5 | 3 | 3 | 5 | 5 | **44** |
| A1 | Board Filing Formatter | 5 | 5 | 5 | 4 | 3 | 3 | 4 | 5 | 4 | 5 | **43** |
| A6 | CPE/CE Credit Calculation Worksheet | 4 | 4 | 4 | 5 | 5 | 5 | 3 | 3 | 5 | 5 | **43** |
| A5 | Board-Compliant Certificate Batch Issuer | 3 | 5 | 4 | 5 | 5 | 4 | 2 | 4 | 5 | 5 | **42** |
| A7 | Roster Pre-Flight Validator | 4 | 5 | 4 | 5 | 4 | 4 | 3 | 4 | 4 | 4 | **41** |
| A4 | Audit Evidence Package Builder | 5 | 2 | 4 | 3 | 3 | 3 | 4 | 5 | 3 | 5 | **37** |
| A8 | Retention Clock & Disposition Scheduler | 3 | 2 | 3 | 5 | 5 | 5 | 3 | 3 | 4 | 4 | **37** |
| A9 | Regulator Rule-Card Extractor | 4 | 2 | 3 | 3 | 2 | 3 | 5 | 4 | 4 | 3 | **33** |

### The top three

**A3 — Webinar Attendance-to-Credit Reconciler (45).** This wins on the combination the
catalog cares most about: it fires *every week*, its inputs are files anyone can produce in
thirty seconds (a Zoom participant export), its logic is deterministic, and its output is
immediately useful in two directions — an award list for today and an audit artifact for three
years from now. It is also the only concept whose test data requires no customer at all; a
developer can generate realistic Zoom exports and build the whole thing before speaking to a
single provider. It scores 4 rather than 5 on scope discipline only because "apply the board's
credit rule" invites scope creep toward becoming a rules engine — that must be resisted in v1
by shipping two or three hard-coded rule profiles.

**A2 — Approval & Credential Expiration Register (44).** The lowest build cost in the set
paired with the most concrete evidence of failure in the entire report. A live provider is
publicly advertising six expired approval numbers. That is not a hypothesized pain point; it is
a screenshot. It scores lower on frequency (renewals are monthly, not weekly) and
differentiation (a spreadsheet is the obvious substitute), but the activity-calendar
cross-check — "you have a class scheduled in March under an approval that dies in February" —
is a genuinely novel and genuinely valuable feature no spreadsheet performs.

**A1 — Board Filing Formatter (43).** The highest ceiling and the flagship of the eventual
product line, held back only by build complexity and scope-discipline risk. Its
differentiation is real: producing a compliant CE Broker positional .xls — six ordered record
types, 100-character row cap, 4+9 profession-code-plus-license structure, reconciled control
and EOF counts — is a task nobody outside the enterprise LMS vendors has solved for the small
provider. The format library should be external versioned data files, not code, so that
regulator changes are a data update rather than a release.

### What to investigate next

**Build A3 first.** It is the wedge: it produces the canonical roster that A1 consumes and the
evidence sheet that A4 assembles. A3 → A1 → A5 is a coherent product line where each tool's
output is the next tool's input, and the free open-source base can be A3 alone.

**Deprioritize A9** until at least two of the others have real users. Its value is entirely
derivative of a rule library that does not yet need maintaining, and its risk profile — an AI
asserting a regulatory deadline — is the wrong risk to take before there is a customer
relationship to absorb it.

---

## 6. Validation plan

### Questions to ask practitioners

1. How many separate regulatory approvals do you currently hold, and can you name them from
   memory or do you have to look them up? *(Tests P2 severity; the answer "I'd have to look"
   is itself the finding.)*
2. Walk me through the last webinar you ran, from the moment it ended to the moment credit
   was posted. How long did that take in wall-clock time? *(Quantifies P3.)*
3. Which board's filing do you dread most, and why? *(Identifies which format to build first.)*
4. When was the last time a roster was rejected? What was the reason and how long did the fix
   take?
5. Have you ever discovered an approval had lapsed after you'd already awarded credit under it?
   What happened?
6. Who else in your organization can do this job if you're out for two weeks? *(Tests the
   single-point-of-failure hypothesis.)*
7. What did you evaluate before settling on your current setup, and what made you not buy it?
   *(Tests the "enterprise LMS is oversized" hypothesis directly.)*
8. Do you know what your per-roster filing fees cost you last year?

### Who to interview

- **State CPA society education directors** — NASBA sponsors, multi-format delivery, small
  teams, and a professional network that talks to each other.
- **Independent behavioral-health CE publishers** — the ce-classes.com archetype: many boards,
  tiny staff, publicly verifiable approval sprawl.
- **Insurance CE school operators in NC, NY, TX, WA** — four genuinely different filing regimes,
  short deadlines, per-student fees.
- **Hospital CME/CNE coordinators at community hospitals** (not academic medical centers) —
  ACCME/ANCC obligations without an academic medical center's staffing.
- **Manufacturer AIA CES providers** — education-as-marketing, so the administrator is a
  marketing person with no compliance background. Likely the highest pain-per-competence ratio.
- **Association management companies (AMCs)** — they run education for many small associations
  at once and would feel every one of these problems multiplied.

### Search terms for further research

`"course completion roster" provider upload rejected` · `CE provider audit findings [state]` ·
`"attendance monitoring" policy CPE sponsor template` · `"provider number" expired credit
denied` · `association education "one person" CE reporting` · `[board name] "provider
information packet" filetype:pdf` · `"CE Broker" roster rejected license number` ·
`NASBA compliance audit findings report sponsor` · site-restricted searches on
`nasbaregistry.org/what-sponsors-need-to-know`

### Sample files needed for testing

- A real Zoom Webinar **participant** export, **poll** report, and **registration** export from
  the same session (the three-way join is the whole problem).
- A CE Broker roster that was **rejected**, plus its Roster Summary — the error text is the
  specification.
- A CalBar Attendance Record Upload Template, an IRS CE bulk-upload XLSX template, and one
  state insurance roster form.
- Two or three real certificates from different boards, to validate the required-element rules
  in A5.
- One provider's actual approval register, however scruffy.

### Prototype that would validate

A **single-file HTML page, no server, no upload** that accepts three Zoom CSVs by drag-and-drop
and produces (a) an award list, (b) an exception list, (c) an audit-evidence table. Everything
runs in the browser, which also answers the PII objection before it is raised. A CE
administrator can try it during a lunch break with real data and no procurement conversation.
If they use it twice, the hypothesis is confirmed.

### Assumptions most likely to be wrong

1. **That providers file to many boards.** Many file to exactly one. If the median provider has
   1–2 approvals, A1's value collapses and A3 carries the product alone. **This is the single
   assumption most worth testing first**, and it is cheap to test — approval counts are usually
   published on provider websites, so a sample of 50 provider sites answers it without a single
   interview.
2. **That the administrator can adopt a tool unilaterally.** If IT procurement is involved,
   local-first desktop tools win and anything server-based dies.
3. **That the registration platform export contains license numbers.** If providers collect
   license numbers by email instead, A7 becomes more important than A1.
4. **That "free open-source base" is attractive here.** Compliance buyers sometimes distrust
   free tools precisely because there is no vendor to blame. The paid-customization tier may
   need to lead, not follow.
5. **That Zoom exports are stable.** If schemas shift often, the ingest adapter becomes ongoing
   maintenance rather than a one-time build.

---

## 7. Cross-industry patterns

**Pattern 1 — Canonical record → many regulator-specific file formats.** One internal dataset
must be emitted in N mutually incompatible, positionally-specified, deadline-bound regulator
formats. Transfers directly to: *Environmental laboratories producing regulator EDD deliverables
(EQuIS and state formats)* — same problem, same shape, arguably worse; *Truck permitting and
registration service agencies (IRP, IFTA, OS-OW)*; *Multi-state charitable solicitation
registration compliance*; *Provider credentialing and payer enrollment services*; *Unclaimed
property and escheat compliance service providers*.

**Pattern 2 — Credential expiration register with forward calendar cross-check.** The value is
not storing expiry dates but cross-referencing them against *scheduled future work* to catch
"you have work booked under a credential that dies first." Transfers to: *Calibration and
metrology service providers / in-house gage management* (calibration due vs. scheduled
inspections); *Special inspection agency accreditation consultants (IAS AC291, ANAB, WABO)*;
*Welding inspection (AWS CWI) and NDT service providers* (technician certification vs. job
assignments); *DOT compliance consultancies and third-party safety managers serving small
fleets* (driver qualification file currency vs. dispatch); *Radiation safety officer services
and portable gauge licensee compliance*.

**Pattern 3 — Session telemetry → audit-grade compliance evidence.** Platform exports
(join/leave, polls, chat) are operationally shaped, not evidentiarily shaped; the transformation
between them is manual and repeated. Transfers to: *Remote online notarization (RON) platform
operators and RON-commissioned notaries* (session recordings and identity-proofing evidence);
*Consortium / third-party administrators (C-TPAs) for DOT drug and alcohol programs* (random
selection and testing evidence); *Test, adjust and balance (TAB) contractors* (instrument
readings → certified report).

**Pattern 4 — Multi-regime retention clock with max-across-regimes disposition.** Transfers to:
*Government contracts administration at small govcons*; *ITAR and EAR export compliance
administration at small manufacturers*; *County recorder offices*; *Title abstracting and
independent title search contractors*.

**Pattern 5 — Published-deficiency-list-driven evidence package builder.** Where a regulator
publishes its own top failure modes, a tool that assembles evidence *and produces a gap
manifest keyed to that published list* is high-value and low-ambiguity. Transfers to: *C3PAO
assessment operations and evidence sampling*; *Special inspection agency accreditation
consultants*; *Federally qualified health centers — HRSA Section 330 grant compliance*;
*Premium audit and payroll classification consulting*.

---

## 8. Sources and confidence

### Verified findings (primary regulatory and vendor documentation)

- [CE Broker — Electronic File Upload, Excel File specification (PDF)](https://secure.cebroker.com/help/provider/Electronic%20File%20Upload%20-%20Excel%20File.pdf) — six record types, 100-character row limit, 4+9 license structure, `State=FL` encoding, pre-import and post-import rejection reasons, Roster Summary within one minute.
- [CE Broker — Technical Details for Reporting](https://help.cebroker.com/hc/en-us/articles/15226531886868-Technical-Details-for-Reporting) — reporting channels; jurisdiction deadline examples (30 days FL, 90 days DC); text-file uploads not recommended.
- [CE Broker — Reporting Course Completions Using Excel](https://help.cebroker.com/hc/en-us/articles/15226533297428-Reporting-Course-Completions-Using-Excel)
- [IRS — Mandatory information reporting for continuing education providers](https://www.irs.gov/tax-professionals/mandatory-information-reporting-for-continuing-education-providers) — five required fields, quarterly deadlines, 10-business-day Q4 rule, 2MB cap, 24-hour resubmission wait.
- [IRS — CE FAQs for continuing education providers](https://www.irs.gov/tax-professionals/ce-faqs-continuing-education-providers) — $650 annual fee, program numbers expire 12/31 of third year, AFTR annual expiry, PTIN validation, PTIN must not appear on certificates, 4-year retention.
- [Washington Office of the Insurance Commissioner — Procedures, reporting, and recordkeeping](https://www.insurance.wa.gov/producers-adjusters/education/continuing-education-ce-providers/procedures-reporting-and-recordkeeping) — 10-day roster rule and enforcement language, webinar record contents, 3-year retention, 10-day notice of presentation.
- [New York DFS — Continuing Education Provider Program Criteria (PDF)](https://www.dfs.ny.gov/system/files/documents/2026/02/Continuing-Education-Provider-Program-Criteria.pdf) — 2-week roster / 30-day completion record, 3-year retention, 100% attendance no partial credit, photo ID, $50 instructor fees, announced and unannounced audits.
- [North Carolina DOI / Prometric — Insurance CE Provider Packet (PDF)](https://www.prometric.com/files/nc-insurance/NC-Provider-Packet.pdf) — 15 business days via Sircon, $2.00 per credit hour per student, 3-year retention, deactivation for a dormant calendar year.
- [Texas TDLR — Continuing Education Providers FAQ](https://www.tdlr.texas.gov/continuing-education-providers/faq.htm) — 7-day electronic completion report, 2-year retention, one-year provider registration, $5-per-licensee fees for certain programs.
- [California State Bar — MCLE Provider Responsibilities](https://www.calbar.ca.gov/legal-professionals/entities/mcle-providers/mcle-provider-responsibilities) — 4-year attendance retention, 1-year evaluation retention, 60-day electronic submission, certificate element list, participatory vs. self-study distinction.
- [Ohio CSWMFT — CE Provider Approval Process](https://cswmft.ohio.gov/license-renewal/CE-provider-approval-process) — 14-business-day CE Broker reporting, required documentation.
- [Minnesota Board of Social Work — CE Provider Responsibility](https://mn.gov/boards/social-work/ceprovider/ce-provider-responsibility.jsp) — 3-year retention, certificate contents including presenter names.
- [NASBA Registry — Top five attendance monitoring deficiencies, group live](https://www.nasbaregistry.org/what-sponsors-need-to-know/top-five-attendance-monitoring-deficiencies-found-during-compliance-audit-group-live-delivery-method) — the published failure-mode list underlying A4.
- [NASBA/AICPA — 2024 Statement on Standards for CPE Programs (PDF)](https://cdn.asp.events/CLIENT_NASBA_287596D2_5056_B733_49DFF69B632BDF66/sites/nasba-registry-composer-2/media/Documents/2024-standards-fos/2024-Statement-on-Standards-for-CPE-Programs.pdf) — Standard No. 24 documentation, three interactivity instances per credit for group internet based, certificate contents, one-fifth/one-half increments, round-down rule.
- [NASBA Registry — Group Internet Based: Measurement](https://www.nasbaregistry.org/resources/best-practices/group-internet-based-measurement) — irregular polling intervals, increment rules, small-group facilitator verification.
- [LCvista — How to avoid failing a NASBA audit](https://lcvista.com/how-to-avoid-failing-a-nasba-audit/) — five common deficiency categories including CPE calculation errors and missing engagement evidence.
- [ce-classes.com — National and state approvals page](http://ce-classes.com/approvals/) — 12 approvals across 4 national bodies and 8 state boards, with multiple expired approval numbers publicly displayed. Direct evidence for P2.
- [NABP — CPE claim submission deadlines](https://nabp.pharmacy/help/when-do-i-submit-cpe-claims-and-what-if-i-miss-the-submission-deadline/) — 60-day provider window to ACPE; no retroactive transcript modification.
- [BACB — ACE Provider FAQs (PDF)](https://www.bacb.com/wp-content/uploads/2026/05/ACE-Provider-FAQs_260504-a.pdf) — replacement certificates required up to 3 years after the event.
- [IACET — Navigating the GDPR right to be forgotten while retaining learner records](https://iacet.org/events/iacet-blog/blog-articles/navigating-the-gdpr-right-to-be-forgotten-while-retaining-learner-records-a-guide-for-iacet-accredited-providers/) — retention vs. erasure conflict.

### Strong inferences (well-supported, not directly stated)

- **The CE administrator is usually a single person at the target organization size.** Supported
  by role descriptions, the AMC business model, and the ce-classes.com evidence pattern, but not
  established by a headcount survey.
- **Enterprise accreditation LMSs are priced out of reach for the 2–40 staff provider.** Supported
  by EthosCE's ~$1,750 entry point with custom-quote tiers and the segment-wide absence of
  published pricing ([ITQlick EthosCE pricing](https://www.itqlick.com/ethosce-lms/pricing)),
  but actual small-provider quotes were not obtained.
- **Manual Zoom reconciliation is a 1–3 hour per-session task.** The workflow is documented
  ([Salepager](https://medium.com/@salepager/assigning-continuing-education-credits-and-sharing-certificates-with-zoom-webinar-attendees-ae76ecedd6ea)) and the vendor
  positioning implies the pain, but no independent time study was found. Arlo's cited "up to 30
  hours a week" on administration ([Arlo](https://www.arlo.co/blog/continuing-education-registration-software-for-ce-training-providers))
  is vendor marketing and should be treated as directional only.
- **Filing rejections are common enough to matter.** Inferred from the length and specificity of
  CE Broker's published rejection-reason list — regulators do not document failure modes that
  never occur — but no rejection-rate statistic was located.

### Tentative hypotheses requiring practitioner validation

- **That the median provider holds enough approvals for A1 to pay off.** ce-classes.com holds 12;
  a manufacturer AIA CES provider may hold 1. The distribution is unknown and it is the pivotal
  variable for the whole product line. Testable cheaply against published provider pages.
- **That providers would trust a local-first open-source tool for regulatory filing.** Plausible
  given the PII advantage, but compliance buyers sometimes prefer a vendor to hold accountability.
- **That certificate-element defects are actually occurring in the field.** The divergent
  requirements are verified; that real providers are getting them wrong is assumed.
- **That approval lapses cause material downstream cost.** The lapses are verified; the
  consequences (refunds, denied credit, board friction) are reasoned, not observed.
- **That AI extraction of regulator rule cards can reach acceptable accuracy.** Untested, and
  the failure mode is severe. Do not build on this assumption without a measured accuracy trial
  against hand-coded ground truth across at least 20 boards.
