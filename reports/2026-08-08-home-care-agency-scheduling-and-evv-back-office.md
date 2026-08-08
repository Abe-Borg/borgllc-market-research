# Home care and home health agency scheduling and EVV back office — back-office

**Cycle date:** 2026-08-08
**Market:** Home care and home health agency scheduling and EVV back office
**Angle:** back-office
**Claim ID:** `814fb26b`

## 0. Cycle header

**Why this assignment.** The ledger held 343 open assignments across 228 markets, 203 of which had zero completed entries. I filtered to zero-coverage markets first (catalog breadth beats depth per the standing instruction), then applied two further tests: is there hard, citable, non-vendor evidence of the problem online, and does the assignment expand the catalog into a domain it has not touched?

Home care back office won on all three:

- **Zero coverage, new domain.** The catalog currently has 27 reports across legal, insurance, construction/AEC, manufacturing, trucking, accounting, dental, staffing and grants. It has nothing in home- and community-based services (HCBS). The nearest neighbours — staffing agency operations (2026-08-07) and medical billing/RCM (2026-08-06) — share the credential-and-visit-verification loop but not the regulatory machinery, and the ledger's own backlog note flagged that similarity as a reason to look here.
- **Unusually hard evidence.** Most markets force you to infer pain from vendor marketing. This one has *numeric regulatory thresholds published by state Medicaid agencies and managed-care plans* — Michigan's 85%-per-payer clean-capture rule, MassHealth's 30/40/50% phased checkpoints, Highmark Wholecare's 85%/15% manual-edit ceiling with corrective action plans and network termination. That converts "agencies find EVV annoying" into a measurable, dated, financially enforced obligation. Verified obligations are the strongest possible foundation for a narrow tool.
- **Angle balance.** Completed angles stood at core-practitioner-workflow 9, back-office 6, narrow-subspecialty 6, handoffs-and-qa 6. Taking a back-office assignment keeps the non-core angles from falling further behind.

Assignments I considered and passed over: *Retirement plan TPAs for small 401(k) plans* (strong, but core-practitioner-workflow, the already-over-represented angle); *Provider credentialing and payer enrollment* (good, but heavily adjacent to the medical-billing report already in the catalog); *Court reporting and deposition services* (smaller market, thinner published-obligation evidence); *Calibration and metrology providers* (strong candidate, kept in backlog — recommend it next).

**Backlog after this claim:** 342 assignments remaining (before this report's discovered additions).

---

## 1. Market examined

### The two adjacent industries

The phrase "home care" covers two regulated businesses that share a back office but almost nothing else:

| | **Non-medical home care / personal care** | **Medicare-certified home health** |
|---|---|---|
| Service | ADL assistance, homemaking, companionship, respite | Skilled nursing, PT/OT/ST, home health aide under a plan of care |
| Staff | Personal care aides, HHAs, caregivers | RN, LPN, therapists, HHAs |
| Payers | Medicaid HCBS waivers, Medicaid managed care (MCOs), private pay, long-term care insurance, VA, area agencies on aging | Medicare (PDGM), Medicare Advantage, Medicaid |
| Licensure | State home care licensure (varies widely; some states none) | State licensure + CMS certification + accreditation |
| Typical unit | 15-minute or hourly units against an authorization | 30/60-day periods, OASIS, NOA |

Both are subject to **Electronic Visit Verification (EVV)** for Medicaid personal care services (since 1 January 2020) and Medicaid home health services (since 1 January 2023) under §12006 of the 21st Century Cures Act. EVV is the spine this report is built around, because it is the single obligation that touches scheduling, payroll, billing, compliance and licensure simultaneously — which is exactly what makes its back-office cost so high and so poorly served.

### Organization profile

- **Population.** Roughly 35,000 companies in the broader US home care industry, of which about 17,000 are personal care / home care aide agencies ([Ankota industry statistics](https://www.ankota.com/home-care-industry-overview-and-statistics)). Highly fragmented: independents, small multi-site operators, and franchise units (Home Instead, Right at Home, Comfort Keepers, Visiting Angels, BrightStar) that run their own P&L and their own back office.
- **Size.** The 2026 Activated Insights (formerly Home Care Pulse) Home Care Benchmarking Report puts **median agency revenue at $1.40M for agencies that do not track every client inquiry and $3.15M for those that do** — a gap that has widened five consecutive years ([Home Care Post summary](https://www.homecarepost.com/activated-insights-releases-2026-home-care-benchmarking-report/)). That $1M–$5M band is the sweet spot for this catalog.
- **Workforce shape.** A $2M personal-care agency typically runs 60–150 active caregivers serving 60–120 clients, against an office of **3 to 8 people**: an administrator/owner, one or two schedulers (often called care coordinators), one billing/payroll person, one recruiter/HR person, and a DON or care manager if clinical services are provided. Caregiver turnover has run in the **77%–80%** range in association reporting ([HCAOA](https://www.hcaoa.org/newsletters/home-care-turnover-rate-jumps-to-80hcaoa-is-here-to-help-members)), so the office is permanently rebuilding its own workforce while operating it.
- **The user of these tools.** Not the caregiver and not the owner. The intended user is the **scheduler/care coordinator and the billing/payroll administrator** — a non-technical, Excel-literate, chronically interrupted person, usually paid $19–$28/hr, who is measured on shifts filled, claims paid, and audits survived.

---

## 2. How the work is performed

The back office of a home care agency is a loop that runs weekly, with a quarterly compliance overlay. Traced end to end:

### 2.1 Referral and authorization intake

A referral arrives from a hospital discharge planner, an MCO care manager, an area agency on aging, or a family. For Medicaid clients the agency receives (or must chase) a **service authorization**: member ID, procedure code (e.g. T1019 for personal care), an allotment of units, and a date range. NJ's Office of the State Comptroller warns providers explicitly that **MCOs may retroactively modify authorizations** based on reassessment, and that eligibility must be re-verified monthly ([NJ Comptroller PCA Q&A](https://www.nj.gov/comptroller/library/Resources/PCA%20Q%20and%20A%20(Final)_10242023.pdf)).

Authorizations arrive as PDFs, portal screens, faxes, or MCO letters. They are re-keyed by hand into the agency system. In small agencies a parallel spreadsheet of "auths and end dates" is near-universal.

### 2.2 Recruiting and onboarding the workforce

Because turnover is ~80%, hiring is a continuous back-office process, not an episodic one. Published 2026 funnel data from agencies using automated recruiting workflows shows **application → interview in 3.19 days, 46.1% application-to-interview conversion, and a 42.6% interview no-show rate** ([HelloHire, May 2026](https://www.tryhellohire.com/the-state-of-home-care-hiring-may-2026-hiring-trends/)) — applicants typically apply to 10–20 agencies at once. Every hire then generates a personnel file that a state surveyor will later inspect: application, license/certification verification, competency evaluation, references, criminal background check, TB screening, orientation record, in-service training records, annual evaluation ([Virginia home care licensure survey checklist](https://townhall.virginia.gov/l/GetFile.cfm?File=C:%5CTownHall%5Cdocroot%5CGuidanceDocs%5C601%5CGDoc_VDH_4271_v3.pdf)).

Several EVV programs additionally require the **servicing caregiver's license or certification number inside the EVV record itself**, distinct from the agency NPI — so a lapsed credential is not merely a survey finding, it is a data-quality defect in every visit that caregiver performs.

### 2.3 Scheduling

The scheduler builds a recurring "master week" per client and fills exceptions daily. The real job is the exception traffic: call-offs, client hospitalizations, new starts of care, caregiver availability changes, and geography. Job descriptions describe the role as ensuring "100 percent of shifts are fully and reliably staffed," managing client-caregiver matching, and carrying an on-call rotation ([TN Advance Care scheduling coordinator posting](https://www.tnadvancecare.com/homecare-scheduling-coordinator-2)). In practice this is done by phone and text against a scheduling grid, with the authorization constraint held in the scheduler's head or in a side spreadsheet.

### 2.4 Visit capture (EVV)

The caregiver clocks in and out at the point of care by mobile app with GPS, by client landline telephony (IVR), or by a fixed device/FOB in the home. Six data elements are federally required for every visit: **who received service, who provided it, type of service, location, date, and start/end time** ([CalEVV Alternate EVV User Guide](https://www.dhcs.ca.gov/wp-content/uploads/2025/10/Alternate-EVV-User-Guide.pdf)).

The visit record flows to a **state aggregator** — Sandata, HHAeXchange, Netsmart, CareBridge, or a state-branded instance such as CalEVV — either from the state's free EVV system or from the agency's own "alternate EVV" (alt-EVV) system via a published interface spec (Ohio, North Carolina, Pennsylvania, Rhode Island, Arizona and California all publish their own).

### 2.5 Visit maintenance — the daily exception queue

Visits that do not arrive clean become **exceptions**. Causes are mundane and constant: caregiver forgot to clock out, clocked in from an unregistered phone number, GPS outside the geofence, service code mismatch against the authorization, client Medicaid ID changed, duplicate client record, wrong jurisdictional entity. CalEVV's guidance is representative: identify red-dot records in the aggregator, correct the data in the alt-EVV system, resubmit, and for a changed Medicaid ID inactivate the client with status `04` and resend as `02` with a new SequenceID.

Every one of these corrections is a **manual edit**, and manual edits are the metric the payers now police.

### 2.6 Payroll

Hours flow from EVV (or from a parallel timesheet — NJ's guidance is blunt that "EVV was not implemented as a timesheet solution; time keeping is a separate process") into payroll. Complications that are normal here and rare elsewhere: multiple visit types with distinct pay rates, weekend and holiday differentials, live-in and 24-hour shift rules, mileage, and **compensable travel time between consecutive client visits**. Agencies routinely run 50+ visit types and a corresponding sprawl of pay codes, and reconcile across systems by hand ([Whirks, "The 6 Biggest Home Care Payroll Problems"](https://www.whirks.com/blog/home-care-payroll-problems)).

### 2.7 Billing

Verified visits become claims to Medicaid FFS, MCOs, VA, or invoices to private-pay clients and long-term care insurers. **Approximately 82% of Medicaid claim denials in home care stem from administrative, eligibility and documentation failures rather than billing errors**, with the named triggers being caregiver codes not matching the authorization, expired or exceeded authorizations, and missing EVV data points ([HHAeXchange](https://www.hhaexchange.com/blog/billing-problems)).

### 2.8 The quarterly compliance overlay

Payers now grade agencies on EVV data quality:

- **Michigan (MMP 26-10, effective 1 April 2026):** at least **85% of verified visits captured with no manual edits**, measured **separately for each payer** each quarter — not blended. A worked example: Medicaid FFS 94%, MCO A 91%, MCO B 79%, agency average 92% — and the agency is still non-compliant because of the smallest payer ([Caretap analysis](https://caretap.net/blog/how-michigan-scores-evv-compliance-per-payer/)).
- **Highmark Wholecare (PA), 2026 enforcement:** 85% verified-visit compliance, manual entries not to exceed 15%; exceeding for **two consecutive quarters** triggers a formal non-compliance letter and a Corrective Action Plan due in 30 days, with continued violation exposing the agency to "overpayment notifications or termination from the network" ([Highmark provider newsfeed](https://providers.highmark.com/wholecare/wholecare-newsfeed/2026-evv-compliance-enforcement-for-home-health-providers.html)).
- **MassHealth:** phased checkpoints of 30% (Apr–Jun 2025), 40% (Jul 2025–Mar 2026) and 50% (from Apr 2026, alongside claims edits) auto-approved verified visits, measured on visits submitted, assessed from the Sandata BI reporting tool mid-month after each period, with "sanction enforcement" for failure ([MassHealth EVV compliance checkpoints](https://www.mass.gov/doc/evv-compliance-checkpoints-0/download)).
- **Texas HHS** runs formal EVV Compliance Reviews with published Usage and Reason Code policy in its EVV Policy Handbook ([TX HHS EVV Policy Handbook](https://www.hhs.texas.gov/handbooks/electronic-visit-verification-policy-handbook)).

The critical structural fact: **these are period-end scores computed after the period closes.** By the time the agency learns it failed, the quarter is unrecoverable.

### 2.9 Software actually in use

| Layer | Products | What they do well | Where they fall short for a $1–5M agency |
|---|---|---|---|
| Agency platform | HHAeXchange, WellSky Personal Care (ClearCare), AxisCare, AlayaCare, Axxess, Alora, KanTime, CareVoyant, Smartcare, MatrixCare | Scheduling, EVV capture, claims, credential expiry alerts | Reviewers cite slow/timing-out systems, EVV freezes, 10-minute delays viewing clock-ins, reports that take minutes to load, claim batches that miscount, poor support ([Capterra HHAeXchange reviews](https://www.capterra.com/p/140366/eXchange-Suite/reviews/?page=3)) |
| State aggregator | Sandata, HHAeXchange, Netsmart, CareBridge, CalEVV | Authoritative compliance data | Reporting is transactional, not managerial; scores surface after period close; per-payer view requires manual assembly |
| Payroll | ADP, Paychex, Paycor, QuickBooks | Pay runs, taxes | Not built for visit types, differentials, travel time; drives 50+ pay-code sprawl |
| Everything else | Excel, shared drives, email, text | Whatever the platform doesn't do | Undocumented, unversioned, dies with the employee who built it |

The gap is consistent and specific: **the platforms are systems of record, not systems of early warning.** They will tell you what happened. They will not tell you, on a Tuesday in month two of the quarter, that MCO B is tracking to 79% and you have eleven clean visits of headroom left.

---

## 3. Most important problems, ranked

### P1 — Per-payer EVV clean-capture rate drifts to failure invisibly, and is only scored after the quarter closes

**Who:** Owner/administrator and billing manager. **When:** continuously; discovered quarterly.
**Currently handled by:** pulling an aggregator report at or after quarter end, or not at all.
**Why inadequate:** the threshold is per payer, the agency's instinct is to watch the blended average, and the blended average is systematically optimistic — Michigan's own arithmetic shows a 92% agency at 79% on one plan. Remediation after quarter close is impossible; the score is final.
**Frequency:** every quarter, every payer, forever.
**Cost:** a Corrective Action Plan is 20–60 hours of administrative work; two consecutive failing quarters at a Highmark-style plan puts network participation — often 15–40% of revenue — at risk. There is no upper bound on the cost of losing an MCO contract.
**Evidence:** Michigan MMP 26-10 85% per-payer rule; Highmark Wholecare 85%/15% two-quarter CAP-to-termination ladder; MassHealth 30/40/50% checkpoints with sanction language. **Verified.**

### P2 — The visit-exception (visit maintenance) queue is unstructured daily manual labour

**Who:** scheduler and billing clerk. **When:** every business day.
**Currently handled by:** working a list in the aggregator or platform, correcting records one at a time, selecting a reason code and typing free text.
**Why inadequate:** the queue is presented transactionally, so the same root cause (a client whose landline is not registered; a caregiver whose phone changed; a geofence set too tight) is re-fixed dozens of times instead of once. Corrections must also happen inside a state-specific time window, and each correction is counted against P1.
**Frequency:** daily; a 100-client agency plausibly generates dozens of exceptions per day.
**Cost:** conservatively 5–10 admin hours/week at a mid-size agency, plus its direct contribution to the compliance score.
**Evidence:** CalEVV correction workflow; Capterra reviewer complaints about EVV freezes and delayed clock-in visibility; state alt-EVV specs. **Verified process, inferred hour count.**

### P3 — Authorization units are consumed, exceeded, or left unused without anyone seeing it in time

**Who:** scheduler (over-schedule risk) and owner (revenue leakage risk). **When:** throughout each authorization period.
**Currently handled by:** a spreadsheet of authorizations with end dates, checked when someone remembers; platform reports that show consumption but not *projected* consumption against the recurring schedule.
**Why inadequate:** over-authorization produces an unbillable visit that was still worked and must still be paid — pure margin loss plus an audit exposure. Under-utilization is silent lost revenue the client was entitled to. MCOs retroactively modify authorizations, so yesterday's arithmetic can be wrong today.
**Frequency:** continuous; every client, every auth period.
**Cost:** expired/exceeded authorizations are named as a top denial trigger inside the 82% administrative-denial figure. At a $25.16 PCA rate, one client running 4 unauthorized hours/week for a month is ~$400 of unpaid worked time — trivially reaching five figures annually across a book.
**Evidence:** HHAeXchange denial-cause analysis; NJ Comptroller guidance on retroactive MCO authorization changes and monthly eligibility verification. **Verified.**

### P4 — Schedule, EVV, payroll and claim never get reconciled against each other

**Who:** billing/payroll administrator. **When:** each pay period and each billing cycle.
**Currently handled by:** manual comparison of exported reports; "agencies spend hours manually reconciling reports and entering data multiple times across systems, despite having software integrations in place."
**Why inadequate:** four systems, four record sets, and no artifact that proves they agree. The failure modes are asymmetric and expensive: paid-but-never-billed (silent margin loss), billed-but-not-EVV-verified (audit and recoupment exposure), verified-but-never-scheduled (fraud flag), and duplicates.
**Frequency:** biweekly at minimum.
**Cost:** revenue leakage from claims never resubmitted before timely-filing windows close is called out explicitly by HHAeXchange; OIG home health provider compliance audits routinely find overpayments traced to internal safeguards that "failed to detect the errors" because of "staffing shortages and human error" ([OIG audit, Alternate Solutions Homecare of Dayton, 2026](https://oig.hhs.gov/reports/all/2026/medicare-home-health-agency-provider-compliance-audit-alternate-solutions-homecare-of-dayton/)).
**Evidence:** Whirks payroll analysis; HHAeXchange; OIG audit series. **Verified.**

### P5 — Overtime and travel-time exposure is discovered after the pay run, not before it

**Who:** payroll administrator and owner. **When:** every pay period.
**Currently handled by:** running payroll and reacting; off-cycle runs to fix errors.
**Why inadequate:** overtime in home care is created by the *schedule*, days before payroll — but nothing in the scheduling workflow prices it. Travel time between consecutive same-day client visits is compensable and routinely missed. Massachusetts fined one home health agency **$85,000+, including $77,000 in restitution to 79 workers**, precisely for paying a reduced overtime rate and failing to pay travel time between job sites ([Mass AG](https://www.mass.gov/news/home-health-agency-to-pay-more-than-85000-for-failing-to-pay-workers-overtime-and-travel-time)).
**Frequency:** every pay period.
**Cost:** unbudgeted OT is the largest controllable margin line in a labour business; wage-and-hour exposure is uncapped and personally attaches to owners in some states.
**Regulatory note:** DOL published an NPRM on **2 July 2025** proposing to return to the 1975 regulations and restore the companionship and live-in exemptions for third-party employers; comments closed 2 September 2025 and **no final rule or effective date has been announced — the 2013 rule remains operative** ([DOL Direct Care page](https://www.dol.gov/agencies/whd/direct-care), [Federal Register](https://www.federalregister.gov/documents/2025/07/02/2025-12316/application-of-the-fair-labor-standards-act-to-domestic-service)). Any tool here must treat the classification rule as a configurable input, not a hard-coded assumption.
**Evidence:** Mass AG enforcement action; Whirks; DOL rulemaking record. **Verified.**

### P6 — Caregiver credential and training expirations are tracked in spreadsheets and discovered at survey

**Who:** HR/recruiter and administrator. **When:** at rehire, at survey, at claim denial.
**Currently handled by:** platform expiry alerts where they exist (HHAeXchange reviewers do praise this), otherwise Excel plus a folder of scanned PDFs.
**Why inadequate:** with ~80% turnover the file set churns completely inside 18 months; expiry alerting without *scheduling enforcement* means an expired-credential caregiver still gets assigned. Where the payer requires the caregiver certification number in the EVV record, the defect propagates into the visit data.
**Frequency:** continuous; acute at annual survey.
**Cost:** survey deficiencies, plan-of-correction cycles, and unbillable visits.
**Evidence:** Virginia licensure survey checklist; NJ EVV caregiver-credential requirement; Capterra. **Verified.**

### P7 — Missed and late visits are neither reliably detected nor defensibly documented

**Who:** scheduler; escalates to owner and MCO. **When:** daily.
**Currently handled by:** noticing the absence, phoning around, and completing an MCO missed-visit form (Texas MCOs use a universal home health missed-visit form).
**Why inadequate:** detection depends on someone noticing a *non-event*. Alora's worked example: 10 missed visits per week at $140 each is **~$67,000 in annual lost revenue**, before rescheduling overtime, satisfaction and audit-flag costs ([Alora](https://www.alorahealth.com/blog-the-financial-impact-of-missed-homecare-visits/)).
**Evidence:** Alora; TAHC MCO universal missed-visit form. **Verified problem, vendor-sourced dollar figure — treat as illustrative.**

### P8 — Accounts receivable ages by payer with no early warning against timely-filing deadlines

**Who:** billing administrator, owner. **When:** monthly, felt at payroll.
**Currently handled by:** monthly AR aging review; weekly in better shops.
**Why inadequate:** payment lags differ structurally by payer — **Medicaid waiver 45–65 days, private LTC insurers 70–90+ days** — so a blended DSO hides the problem payer. Aging past 90 days traces back to coding errors or missing authorizations, i.e. to P3 and P4 ([PRN Funding](https://prnfunding.com/why-accounts-receivable-management-is-the-key-to-scaling-your-homecare-agency/)).
**Evidence:** PRN Funding; HHAeXchange on timely-filing revenue leakage. **Verified (finance-vendor sourced).**

### P9 — Long-term care insurance claim packets are assembled by hand, per carrier

**Who:** billing administrator, private-pay side. **When:** monthly per LTCi client.
**Currently handled by:** manually assembling invoices, service logs, care plans and caregiver notes to each carrier's format; families often mismanage elimination periods and physician documentation, and the agency absorbs the rework.
**Why inadequate:** carriers reimburse on documentation, each has its own requirements, and the agency carries 70–90+ day AR while the packet is in dispute.
**Evidence:** [Assisting Hands on common LTCi claim mistakes](https://assistinghands.com/130/tennessee/franklin/blog/common-long-term-care-insurance-claim-mistakes/); PRN Funding on LTCi payment lags. **Verified problem, agency-blog sourced — validate with practitioners.**

### P10 — Alt-EVV submissions are rejected by the aggregator for spec violations found downstream

**Who:** agencies running their own EVV system that transmits to a state aggregator.
**Currently handled by:** submit, wait, read the rejection, call the vendor.
**Why inadequate:** states publish detailed interface specs (Ohio v4.3, NC OpenEVV-altEVV v7.10, Arizona, Rhode Island 3.2, CalEVV). The rules — required elements, ID immutability, status codes, SequenceID discipline — are knowable *before* transmission.
**Evidence:** the published state specs themselves. **Verified obligation; the frequency of rejection at small agencies is an inference.**

---

## 4. Application opportunities

Design constraint applied throughout: **every one of these works from files the agency can already export** (visit detail CSV, payroll register, claim/remit file, authorization list). No API integration, no vendor partnership, no cloud data custody. That is the wedge — these agencies cannot get their vendors to build anything, but every one of them can click "Export to Excel."

---

### C1 — CleanRate: per-payer EVV clean-capture scorecard and quarter-end projector

- **User:** owner/administrator and billing manager at a 40–300 caregiver agency.
- **Problem solved:** P1. The agency cannot see, mid-quarter, which individual payer is tracking to fail its clean-capture threshold.
- **Current workflow:** pull an aggregator report at or after quarter end; look at the agency-wide number; discover the failure in the payer's letter.
- **Proposed workflow:** weekly, drop the visit-detail export into the tool. It computes clean-capture % **per payer** for the quarter to date, projects the quarter-end score at current run-rate, and answers the only question that matters: *"How many more clean visits — or how few more manual edits — before payer X falls below threshold?"* It ranks the caregivers, clients and exception reasons driving the edits.
- **Inputs:** visit detail export (visit ID, client, payer/plan, caregiver, date, verified flag, manual-edit/reason-code flag). A per-payer threshold profile (Michigan 85%, Highmark 85%, MassHealth 50%, custom).
- **Outputs:** a one-page per-payer scorecard with headroom in *visits*, a trend line, a top-10 root-cause table, and a printable quarter-end evidence sheet.
- **Essential features:** payer grouping and aliasing; threshold profiles as editable data; run-rate projection; headroom in whole visits; drill-down to the offending visits.
- **Deliberately excluded:** submitting or correcting visits, any write-back to the platform, live integration, caregiver-facing anything, multi-agency benchmarking.
- **AI:** **inappropriate.** This is arithmetic against a published threshold. Adding a model would reduce trust in a compliance number.
- **Why not a spreadsheet:** a one-off pivot gets you the current percentage. It does not get you threshold profiles per payer maintained as rules, run-rate projection, headroom expressed in whole visits, or a repeatable weekly artifact a non-analyst can produce. In practice the spreadsheet is built once by the one capable person and abandoned when they leave — and the failure mode of this task is precisely *not doing it every week*.
- **Complexity:** small (a focused single-page web app or Python + HTML report; no server needed).
- **Learning difficulty:** ~10 minutes. Upload, read.
- **Value:** avoids a CAP (20–60 admin hours) and, at the tail, protects an MCO contract worth 15–40% of revenue.
- **Risks / privacy:** contains PHI. Must be local-first — browser-side processing or a local script, no upload. Say so loudly; it is a selling point in this market.
- **Substitutes:** aggregator BI reports (transactional, post-hoc, not per-payer projected); platform compliance dashboards (blended); consultants.
- **Why still attractive:** the incumbents own the data and still do not answer the forward-looking question. The threshold profiles are the product, and they change by state and by plan every year — which is exactly the shape of thing an open-source rule pack maintains well.
- **Paid customization:** per-state and per-MCO threshold packs; agency-specific payer alias maps; branded quarterly board report; multi-site roll-up for franchise operators.

---

### C2 — ExceptionSort: visit-maintenance root-cause triage queue

- **User:** scheduler / billing clerk.
- **Problem solved:** P2. The exception queue is fixed one record at a time instead of one *cause* at a time.
- **Current workflow:** work the aggregator's list top to bottom, daily, forever.
- **Proposed workflow:** import the exception export; the tool clusters exceptions by inferred root cause (unregistered client phone, caregiver device change, geofence too tight for this address, service code mismatch, chronic late clock-out by one caregiver, client Medicaid ID change) and produces a **fix-the-cause worklist** ranked by how many future exceptions each fix prevents. It also produces a per-exception reason-code suggestion consistent with the state's code list, and tracks whether the cause actually stopped recurring.
- **Inputs:** exception/visit-maintenance export; optional client address and phone list.
- **Outputs:** ranked cause list with projected exception reduction; a per-cause action card; a recurrence tracker.
- **Essential features:** clustering rules per state code list; recurrence measurement; export of the still-manual corrections.
- **Deliberately excluded:** performing the corrections, connecting to the aggregator, caregiver messaging.
- **AI:** **optional and secondary.** Clustering should be rule-based on structured columns. AI is defensible only for grouping free-text reason narratives where agencies have typed prose — a nice-to-have, not the core.
- **Why not a spreadsheet:** the clustering rules are the asset and they encode state-specific code semantics; recurrence tracking requires state across weeks, which spreadsheets handle badly and non-analysts maintain worse.
- **Complexity:** small–medium.
- **Learning difficulty:** ~30 minutes.
- **Value:** removes a meaningful share of a 5–10 hr/week task and directly improves C1's number.
- **Risks:** PHI; state code lists drift.
- **Substitutes:** the aggregator's own queue.
- **Paid customization:** state-specific rule packs; agency-specific geofence and phone-registry hygiene reports.

---

### C3 — AuthRadar: authorization burn-down and expiry projector

- **User:** scheduler and owner.
- **Problem solved:** P3.
- **Current workflow:** an "auths" spreadsheet with end dates; consumption checked reactively.
- **Proposed workflow:** load the authorization list, the delivered-visit export, and the recurring schedule. The tool projects, per client per service code, the date on which authorized units will be exhausted at the current recurring schedule; flags every authorization expiring within a configurable window; and flags **underutilization** (clients tracking to leave >15% of authorized units unused) as recoverable revenue. It produces a weekly "authorizations at risk" sheet the scheduler works before building next week's schedule.
- **Inputs:** authorization export (client, payer, procedure code, units, start/end), delivered visits, recurring schedule.
- **Outputs:** projected-exhaustion date per authorization; expiring-soon list; over-schedule warnings for next week; underutilization list with dollars.
- **Essential features:** unit-basis handling (15-minute vs hourly vs visit); multi-authorization clients; retroactive-change re-baselining.
- **Deliberately excluded:** requesting reauthorization, portal integration, care planning.
- **AI:** **inappropriate.** Arithmetic and calendars.
- **Why not a spreadsheet:** it is a three-way join plus a forward projection over a recurring calendar, re-run weekly across 100+ clients. Spreadsheets do the join badly and the recurrence projection worse; and this is the exact spreadsheet that already exists and already fails.
- **Complexity:** medium.
- **Learning difficulty:** ~1 hour.
- **Value:** eliminates worked-but-unbillable hours and recovers silent under-utilization; attacks a named top-3 denial cause.
- **Risks:** PHI; authorizations retroactively modified by MCOs — the tool must timestamp its inputs and never present a projection as authoritative.
- **Substitutes:** platform authorization reports (consumption to date, not projection).
- **Paid customization:** payer-specific unit rules; MCO authorization-letter parsing for a specific agency's carriers.

---

### C4 — FourWay: schedule ↔ EVV ↔ payroll ↔ claim reconciliation

- **User:** billing/payroll administrator; also the owner preparing for an audit or a sale.
- **Problem solved:** P4.
- **Current workflow:** hours of manual export comparison, or nothing.
- **Proposed workflow:** drop in four exports for a date range. The tool matches on client + caregiver + date + time window and emits a categorized exception report: **paid but never billed**, **billed but not EVV-verified**, **EVV-verified but never scheduled**, **scheduled and paid but no EVV record**, **duplicates**, and **quantity mismatches**. Each category carries a dollar figure and a suggested owner. It also emits a signed-off reconciliation certificate per period — the artifact that does not currently exist anywhere in this industry.
- **Inputs:** schedule export, EVV visit export, payroll register, claim/billing register (or 835 remittance).
- **Outputs:** categorized exception workbook with dollars; period reconciliation certificate; trend of exception counts by category.
- **Essential features:** fuzzy time-window matching with configurable tolerance; category rules; dollar attribution; period archive.
- **Deliberately excluded:** correcting anything, posting adjustments, general ledger.
- **AI:** **inappropriate** for matching (deterministic rules must be auditable). Arguably optional for parsing heterogeneous export headers on first setup — but a saved column-mapping profile does that better.
- **Why not a spreadsheet:** four-way matching with time tolerance across thousands of rows, re-run every period, producing an archived artifact. This is the canonical case where a spreadsheet technically can and practically does not.
- **Complexity:** medium.
- **Learning difficulty:** ~1 hour for first column mapping, minutes thereafter.
- **Value:** direct cash recovery from paid-not-billed; audit defense against the exact finding pattern the OIG reports describe; and it makes the agency materially more sellable.
- **Risks:** PHI plus payroll data — the most sensitive combination in this report. Local-only is mandatory.
- **Substitutes:** none focused; platform "unbilled visits" reports cover one of six categories.
- **Paid customization:** column-mapping profiles per platform; agency-specific category rules; quality-of-earnings pack for agencies preparing to sell.

---

### C5 — ShiftCost: pre-payroll overtime and travel-time exposure simulator

- **User:** scheduler (before publishing the week) and payroll administrator (before the run).
- **Problem solved:** P5.
- **Current workflow:** find out on the payroll register.
- **Proposed workflow:** load next week's schedule. The tool projects each caregiver's weekly hours across all clients and sites, flags those crossing 40, prices the marginal OT, identifies consecutive same-day visits with a travel gap that is likely compensable, and flags classification-sensitive arrangements (live-in, 24-hour, companionship-only) against a configurable rule profile. Run it again against actuals before the pay run.
- **Inputs:** schedule export; caregiver pay rates; client addresses; a jurisdiction rule profile.
- **Outputs:** per-caregiver projected hours and OT dollars; travel-time exposure list; classification-risk flags; a "cheapest reassignment" hint list.
- **Essential features:** multi-client hour aggregation per caregiver; configurable OT and travel rules by state; before/after comparison.
- **Deliberately excluded:** running payroll, auto-reassigning shifts, giving legal advice.
- **AI:** **inappropriate.** Wage-and-hour arithmetic must be explainable line by line.
- **Why not a spreadsheet:** caregivers work across multiple clients, so per-client schedules must be aggregated per person before the 40-hour test — the exact aggregation the scheduler's per-client view hides. And the rule profile must be maintainable as the FLSA rulemaking resolves.
- **Complexity:** small–medium.
- **Learning difficulty:** ~30 minutes.
- **Value:** OT is often the largest controllable variance in a labour business; the Massachusetts action shows the wage-and-hour tail ($85k on 79 workers at a single small agency).
- **Risks:** must not be presented as legal compliance certification. Rule profiles must be dated and cite their source. The pending DOL companionship/live-in rule means the rule pack will change — build for that.
- **Substitutes:** payroll system OT reports (after the fact); platform overtime alerts (per-client, not per-person, in some products).
- **Paid customization:** state rule packs (CA, NY, MA, WA are materially different); agency-specific differential structures.

---

### C6 — CredGate: credential expiry board with scheduling enforcement and survey binder export

- **User:** HR/recruiter and administrator.
- **Problem solved:** P6.
- **Current workflow:** Excel plus a scan folder; platform alerts where present.
- **Proposed workflow:** maintain a credential matrix per caregiver against a **state licensure rule pack** (the survey checklist items: background check, TB screening, competency evaluation, references, orientation, annual in-service hours, annual evaluation) plus **payer-specific** requirements (e.g. certification number required in the EVV record). Cross-check the next two weeks of schedule against expirations to produce a "do not assign" list, and export a survey-ready personnel-file index showing, per employee, which required document is present, its date, and where it lives.
- **Inputs:** caregiver roster, credential dates, document folder, schedule export, state rule pack.
- **Outputs:** expiry calendar; do-not-assign list; per-employee survey binder index; missing-document report.
- **Essential features:** state rule packs as data; schedule cross-check; document presence verification (does the file actually exist?); printable binder index.
- **Deliberately excluded:** document storage/DMS, e-signature, training delivery, HRIS.
- **AI:** **optional, narrow.** Reading an expiry date off a scanned certificate is a real OCR/extraction win. Everything else is rules. Ship v1 without it.
- **Why not a spreadsheet:** the spreadsheet exists and is the status quo; what it cannot do is verify the document is actually in the folder, cross-check the forward schedule, and print a survey index. Also, with ~80% turnover the roster churns faster than a hand-maintained sheet survives.
- **Complexity:** small–medium.
- **Learning difficulty:** ~45 minutes; ongoing use is trivial.
- **Value:** survey deficiency avoidance; prevents unbillable visits by uncredentialed staff.
- **Risks:** PII-heavy. Local-only. Rule packs vary enormously by state — under-promise coverage.
- **Substitutes:** **this is the most contested concept in the list.** HHAeXchange reviewers explicitly praise its credential tracking with expiration alerts, and most platforms ship something. Differentiation rests entirely on (a) state survey rule packs, (b) schedule enforcement rather than alerting, (c) the printable binder index, (d) working for agencies whose platform does it badly or who run two platforms.
- **Paid customization:** state rule packs; franchise-brand requirement overlays.

---

### C7 — MissedVisit Ledger: gap detection and MCO notification packet

- **User:** scheduler; reviewed by administrator.
- **Problem solved:** P7.
- **Current workflow:** notice, phone around, fill a form.
- **Proposed workflow:** diff scheduled visits against verified visits daily. Every unmatched scheduled visit becomes a ledger entry requiring disposition (client refused, client hospitalized, caregiver call-off covered, caregiver call-off uncovered, documentation error). The tool pre-fills the payer's missed-visit notification form, tracks whether notification was sent within the payer's window, and produces a monthly pattern report by caregiver, client, day-of-week and geography.
- **Inputs:** schedule export, verified visit export, payer form templates.
- **Outputs:** daily disposition worklist; pre-filled notification forms; monthly pattern analysis with revenue impact.
- **Essential features:** matching with tolerance; disposition taxonomy; notification-window timer; pattern report.
- **Deliberately excluded:** filling the shift, caregiver messaging, client communication.
- **AI:** **inappropriate.**
- **Why not a spreadsheet:** it is a daily diff of two changing datasets plus a deadline timer.
- **Complexity:** small.
- **Learning difficulty:** ~20 minutes.
- **Value:** the $67k/yr illustrative figure aside, the defensible artifact matters more — missed-visit documentation is what an MCO audit asks for.
- **Risks:** PHI; forms vary by payer.
- **Substitutes:** platform missed-visit reports; the manual form.
- **Paid customization:** payer form templates; state reporting-window rules.

---

### C8 — PacketBuilder LTCi: long-term care insurance claim packet assembler

- **User:** billing administrator on the private-pay side.
- **Problem solved:** P9.
- **Current workflow:** hand-assemble invoice + service log + care plan + notes per carrier, monthly, per client.
- **Proposed workflow:** maintain a **carrier requirement profile** (which documents, which fields, what format, submission channel, elimination-period handling). Generate the month's packet per client from the visit export and note export, validate it against the profile before sending, log the submission, and age the receivable against a carrier-specific expected-payment window.
- **Inputs:** visit export, care notes, client policy details, carrier profile.
- **Outputs:** assembled PDF packet; pre-submission completeness check; submission log and aging.
- **Essential features:** carrier profiles as data; completeness validation; aging by carrier.
- **Deliberately excluded:** carrier portal automation, benefit-eligibility determination, policy interpretation.
- **AI:** **optional.** Reading a carrier's requirement letter into a draft profile is a legitimate extraction task; the profile is then human-reviewed and reused. Core assembly is templating.
- **Why not a spreadsheet:** the output is a document packet, not a table.
- **Complexity:** medium.
- **Learning difficulty:** ~1 hour to build the first carrier profile.
- **Value:** compresses a 70–90+ day receivable and reduces resubmission cycles.
- **Risks:** PHI; carrier requirements are not publicly documented in a usable way — profiles must be built from real correspondence, which makes this **evidence-thin without practitioner input**.
- **Substitutes:** platform private-pay invoicing (invoice only, not packet).
- **Paid customization:** this concept is almost entirely customization revenue — each agency's carrier mix is different.

---

### C9 — AgingSplit: payer-segmented AR aging with timely-filing countdown

- **User:** billing administrator and owner.
- **Problem solved:** P8.
- **Current workflow:** monthly aging review on a blended report.
- **Proposed workflow:** ingest the AR export and/or 835 remittances. Segment aging **by payer against that payer's normal payment window** (Medicaid waiver 45–65 days, LTCi 70–90+) so "late" means late *for that payer*, not late in the abstract. Overlay a timely-filing countdown per claim and rank by dollars about to become permanently unbillable. Cluster denials by reason code × payer × service code.
- **Inputs:** AR aging export or 835 files; payer profile (payment window, timely-filing limit).
- **Outputs:** payer-segmented aging; "dollars expiring in 30 days" list; denial-cluster report.
- **Essential features:** payer profiles; timely-filing arithmetic; CARC/RARC grouping.
- **Deliberately excluded:** claim submission, appeals, collections workflow.
- **AI:** **inappropriate** for the arithmetic; optional for parsing denial letters received as PDFs.
- **Why not a spreadsheet:** the timely-filing countdown and per-payer normalization must be maintained as rules and re-run.
- **Complexity:** medium.
- **Learning difficulty:** ~45 minutes.
- **Value:** directly recovers revenue that would otherwise be lost to filing deadlines.
- **Risks:** PHI. **Note the overlap:** the catalog already contains "Remit Lens" (2026-08-06, medical billing) doing 835 denial analytics for small practices. The home care differentiator is payer-window normalization and the timely-filing countdown, not the 835 parsing — consider whether this should be a home-care rule pack *for* Remit Lens rather than a separate product.
- **Paid customization:** payer profile libraries by state.

---

### C10 — AltEVV Preflight: aggregator submission validator

- **User:** agencies transmitting from their own EVV system to a state aggregator; also the small alt-EVV vendors themselves.
- **Problem solved:** P10.
- **Current workflow:** submit, wait, read rejections, call the vendor.
- **Proposed workflow:** validate the outbound payload against the **published state spec** before transmission — required elements present, ID formats, client status codes, SequenceID monotonicity, service codes valid for the payer, timestamps well-formed, no duplicate visit IDs. Produce a pass/fail report with per-record errors keyed to the spec section.
- **Inputs:** the outbound file/payload; a state spec profile (Ohio v4.3, NC OpenEVV-altEVV v7.10, AZ, RI 3.2, CalEVV).
- **Outputs:** validation report; corrected-file checklist.
- **Essential features:** spec profiles as versioned data; per-record error messages citing the spec.
- **Deliberately excluded:** transmitting, correcting, or storing the data.
- **AI:** **inappropriate.** Schema validation.
- **Why not a spreadsheet:** it is schema validation of a structured payload.
- **Complexity:** small–medium per spec, and it scales by adding specs.
- **Learning difficulty:** ~20 minutes.
- **Value:** removes a rejection-and-rework cycle; highest value to the smallest alt-EVV vendors, who may be a better customer than the agencies.
- **Risks:** specs version frequently; a stale profile is worse than none, so version-stamping is mandatory.
- **Substitutes:** the aggregator's own rejection messages (after the fact); the alt-EVV vendor's validation (variable quality).
- **Paid customization:** per-state spec profiles; white-label for alt-EVV vendors — the clearest B2B upsell in this list.

---

## 5. Opportunity ranking

Scored 1–5 on each of ten criteria; 50 maximum.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of build | Stays narrow | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|:--:|
| C1 | **CleanRate** — per-payer EVV clean-capture scorecard | 5 | 5 | 5 | 5 | 5 | 5 | 4 | 5 | 4 | 5 | **48** |
| C3 | **AuthRadar** — authorization burn-down and expiry | 5 | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 3 | 5 | **44** |
| C4 | **FourWay** — schedule/EVV/payroll/claim reconciliation | 5 | 4 | 5 | 4 | 3 | 4 | 5 | 5 | 3 | 5 | **43** |
| C5 | **ShiftCost** — pre-payroll OT and travel-time exposure | 5 | 5 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | 4 | **42** |
| C7 | **MissedVisit Ledger** — gap detection + MCO packet | 4 | 5 | 4 | 5 | 5 | 5 | 3 | 4 | 3 | 4 | **42** |
| C2 | **ExceptionSort** — visit-maintenance root-cause triage | 4 | 5 | 4 | 4 | 4 | 4 | 3 | 4 | 3 | 4 | **39** |
| C6 | **CredGate** — credential expiry + schedule enforcement | 4 | 4 | 3 | 5 | 4 | 4 | 2 | 4 | 4 | 4 | **38** |
| C10 | **AltEVV Preflight** — aggregator submission validator | 3 | 3 | 3 | 5 | 4 | 5 | 4 | 5 | 4 | 4 | **40** |
| C9 | **AgingSplit** — payer-segmented AR + filing countdown | 4 | 4 | 4 | 4 | 3 | 3 | 2 | 4 | 3 | 4 | **35** |
| C8 | **PacketBuilder LTCi** — LTC insurance claim packets | 4 | 3 | 4 | 4 | 3 | 4 | 4 | 5 | 2 | 3 | **36** |

### The top three

**1. CleanRate (48/50).** The strongest concept in this cycle and, on the evidence, one of the strongest in the catalog. Three things make it unusual. First, the obligation is *published, numeric and dated* — Michigan's 85% per-payer rule effective 1 April 2026, Highmark's 85%/15% two-quarter ladder, MassHealth's 50% checkpoint from April 2026. There is no need to persuade anyone the problem exists; the payer already sent them a letter. Second, the incumbents structurally cannot serve it: aggregators report transactionally after period close, and platforms show a blended average that is *systematically optimistic* against a per-payer threshold. Third, it is genuinely small — a few hundred lines over a CSV, no server, no PHI leaving the building. The threshold profiles are the durable asset, and they are exactly the kind of thing an open-source rule pack maintains better than a vendor roadmap.

**2. AuthRadar (44/50).** Attacks a named component of the 82% administrative-denial figure and has a symmetric payoff — it stops unbillable worked hours on one side and recovers unused authorized units on the other. The reason it scores below CleanRate is build risk: authorization data is messier than visit data, unit bases differ by payer, and MCOs retroactively modify authorizations, so the tool must be honest about the age of its inputs. Still, the "spreadsheet that already exists and already fails" test points straight at it.

**3. FourWay (43/50).** The highest ceiling and the highest effort. It produces something that does not exist anywhere in this industry — a per-period artifact proving the four systems agree — which is valuable at three separate moments: cash recovery now, audit defense later, and diligence when the owner sells. Its scoring is dragged down by build complexity and by needing four clean exports rather than one. Best treated as the second build, reusing CleanRate's export-parsing layer.

**Investigate next:** **CleanRate**, without qualification. Build the Michigan and Highmark threshold profiles first because those are the two with hard 2026 dates and explicit escalation ladders, then add MassHealth and Texas. C3 and C4 should share its file-ingest and column-mapping foundation, which argues for treating C1/C3/C4 as one codebase with three reports rather than three products.

**Reconsider before building:** C6 (CredGate) — platform vendors genuinely ship this and reviewers praise it; only the state survey rule packs and schedule enforcement differentiate. C9 (AgingSplit) — likely better as a home-care rule pack for the catalog's existing Remit Lens than as a new product.

---

## 6. Validation plan

### Questions to ask practitioners

**On C1 (highest priority):**

1. Which payers do you bill, and do you currently know your clean-capture percentage for each one *separately*?
2. When in the quarter do you find out your EVV score? What do you do if it's bad?
3. Have you ever received a corrective action plan or non-compliance letter over EVV? What did it cost you in hours?
4. Can you export a visit detail report that includes payer and a manual-edit or reason-code flag? *(This is the make-or-break feasibility question — ask for the actual file.)*
5. Who in the office would run this weekly, and would they actually do it?

**On C3:** How do you track authorization units today — show me the spreadsheet. How often do you work hours you can't bill because the auth ran out? How often do you find out an auth expired *after* the visit?

**On C4:** Do you ever find visits you paid for but never billed? How do you find them today? What would you pay to have that list every pay period?

**On C5:** How much overtime do you budget vs actual? Do you pay travel time between same-day clients? Has a wage claim ever been filed against you?

### Who to interview

- Owners and administrators of independent agencies with 40–300 caregivers in **Michigan, Pennsylvania and Massachusetts** — the three states with dated 2026 thresholds and therefore the sharpest pain right now.
- Franchise unit owners (Home Instead, Right at Home, Comfort Keepers) — they run their own back office but share brand-level requirements, which is a natural rule-pack customer.
- Billing/payroll administrators specifically, not just owners: they know which exports actually exist.
- Home care association staff: HCAOA, state associations (PHA, Michigan HomeCare & Hospice Association, Home Care Alliance of Massachusetts, TAHC in Texas).
- Small alt-EVV vendors — the natural design partner for C10 and a channel to agencies for C1.
- Home care–specialist bookkeeping and payroll firms (e.g. the kind that publish the payroll-problem analyses cited here) — they see many agencies' data and are a distribution channel.

### Search terms for further research

`"EVV" "manual edit" percentage provider compliance <state>` · `visit maintenance reason code <state> EVV handbook` · `alt-EVV interface specification <state> version` · `home care "corrective action plan" EVV managed care` · `"missed visit" form MCO home health <state>` · `personal care services audit findings state auditor <state>` · `home care agency "unbilled visits" report` · `HCBS provider EVV compliance webinar 2026` · `home care agency quality of earnings diligence EVV`

### Sample files needed for prototyping

1. A **visit detail export** with payer, verified status and manual-edit/reason-code columns from HHAeXchange, Sandata and AxisCare — de-identified. Without this, C1 cannot be built; with it, C1 is a weekend.
2. An **exception / visit maintenance export**.
3. An **authorization export** showing units, procedure code and date range.
4. A **payroll register** and a **claim register** for the same period (for C4).
5. One **state EVV compliance report** as the payer actually issues it, to confirm the tool's arithmetic reproduces the official score.

### Minimum prototype that validates C1

A single self-contained HTML file. The agency drops in a visit detail CSV; everything is computed in the browser, nothing is uploaded. It outputs one table: payer, visits this quarter, clean %, projected quarter-end %, headroom in visits before threshold. Two hours of work if the export format is known. If a practitioner looks at that table and immediately says "wait, that plan is at 79%?" — the concept is validated and everything else is elaboration.

### Assumptions most likely to be fatal

- **That the manual-edit flag is exportable.** If platforms do not expose a per-visit manual-edit indicator in any user-accessible export, C1 collapses to an estimate and its whole value proposition — reproducing the official score — evaporates. **Verify this first, before anything else.**
- **That payer identity is a usable field.** If MCO plans appear as inconsistent free text, the per-payer grouping needs an alias map the user must maintain, which raises learning cost.
- **That agencies will run something weekly.** The entire premise is that mid-quarter visibility changes behaviour. An agency that will not open the tool until quarter end gets no value from it. Mitigation: make it a 30-second task and make the output a single printable page the owner asks for.
- **That state thresholds stay stable enough to package.** They will not; that is why they are rule packs, and why an open-source project with practitioner contributors beats a vendor's annual release cycle.
- **That the platform vendors won't just build it.** They could. They have not, across a decade of EVV, because their incentive is to report their own data favourably, not to tell an agency it is failing. That is a durable but not permanent moat.

---

## 7. Cross-industry patterns

Five patterns from this market that transfer, with the specific backlog markets they transfer to.

**Pattern A — Threshold-compliance early-warning meter.**
A regulator or counterparty grades the small business on a *rate* against a published threshold, computed after the period closes, and reported as a blended figure that hides per-counterparty failure. The tool recomputes the rate the way the grader does, per counterparty, mid-period, and expresses remaining headroom in whole units of work. Transfers to: **Fire protection ITM contractors under NFPA 25** (inspection-completion rates per AHJ/customer); **DOT compliance consultancies and third-party safety managers serving small fleets** (CSA BASIC percentile trajectory between refresh dates); **MSP program offices and VMS supplier-management desks** (supplier scorecard trajectory per client program); **Personnel certification bodies under ISO/IEC 17024**; **Utility energy-efficiency program implementers and trade-ally rebate documentation** (per-program QC pass rates); **State licensing board education/CE audit units**.

**Pattern B — Export-only reconciliation bridge.**
The business runs three to five systems that all hold the same transaction and none of which agree; the vendors will not integrate and the business cannot make them. A tool that consumes each system's ordinary CSV export, matches on a natural key with tolerance, and emits a categorized discrepancy report plus a per-period reconciliation artifact. Requires no vendor cooperation, which is why it is buildable at all. Transfers to: **Payroll service bureaus and small independent payroll providers**; **Staffing back-office service bureaus and payroll funders**; **Small third-party medical billing companies (RCM service bureaus, 1-25 staff)**; **Freight bill audit and payment for small shippers**; **Retirement plan third-party administrators (TPAs) for small 401(k) plans**; **Independent pharmacy third-party reconciliation and PBM claw-backs**.

**Pattern C — Entitlement burn-down radar.**
A finite, dated allotment (units, dollars, hours, credits) is consumed against a recurring commitment, and both overrun and underrun are expensive in opposite ways. The tool projects the exhaustion date against the forward schedule, flags expiries, and prices the underrun as recoverable. Transfers to: **Insurance defense litigation support and claims file review at small defense firms** (litigation budget burn against case plan); **Third-party claims administration (TPA) and self-insured program operations**; **Durable medical equipment (DME) suppliers**; **Tenant-side lease audit and occupancy cost consulting**; **Retirement plan TPAs** (contribution/testing limits); **Community action agencies and Head Start grantees** (grant line burn).

**Pattern D — Pre-flight validator against a published interface specification.**
A public authority publishes a versioned data-interchange spec; the small business submits against it blind and learns of defects only through rejection. A local validator with versioned spec profiles catches defects before transmission. Transfers to: **Environmental laboratories producing regulator EDD deliverables (EQuIS and state formats)**; **County recorder offices — document intake, indexing and rejection handling** (and the submitter side); **Information return (1099/W-2) filing service providers**; **Mortgage post-closing QC and trailing document vendors**; **Apprenticeship program sponsors and DOL RAPIDS reporting**.

**Pattern E — Exposure simulator run before an irreversible commit.**
A cost or legal exposure is created by a decision made days before the moment it is discovered (the schedule creates the overtime; the pay run reveals it). A simulator run at the decision point, pricing the consequence with configurable jurisdiction rules, converts a post-hoc report into a choice. Transfers to: **Certified payroll and prevailing wage compliance service providers**; **Small motor carriers (5-50 trucks) back office and settlement** (HOS and settlement exposure before dispatch); **Staffing back-office service bureaus**; **Construction subcontractor project management at 15-150 employee specialty trades** (crew cost before the week is committed); **Home care's own neighbours in adult day and PACE**.

---

## 8. Sources and confidence

### Verified findings — cited to regulators, payers, enforcement actions, or published specifications

- Michigan MMP 26-10: 85% of verified visits with no manual edits, **measured separately per payer**, effective 1 April 2026, with the worked example showing a 92% agency failing on a 79% plan — [Caretap analysis of Michigan per-payer scoring](https://caretap.net/blog/how-michigan-scores-evv-compliance-per-payer/), [Michigan EVV compliance calendar](https://caretap.net/blog/michigans-evv-rule-grades-quarter-ends-stay-ahead/)
- Highmark Wholecare 2026 enforcement: 85% verified-visit compliance, manual entries ≤15%, two consecutive failing quarters → non-compliance letter → CAP in 30 days → overpayment notification or network termination — [Highmark provider newsfeed](https://providers.highmark.com/wholecare/wholecare-newsfeed/2026-evv-compliance-enforcement-for-home-health-providers.html)
- MassHealth phased EVV checkpoints 30% / 40% / 50% auto-approved verified visits, measured on visits submitted, assessed from Sandata BI mid-month after each period, sanction enforcement for failure — [MassHealth EVV compliance checkpoints](https://www.mass.gov/doc/evv-compliance-checkpoints-0/download)
- Texas HHS EVV Policy Handbook (compliance reviews, usage, reason codes, reports) — [TX HHS](https://www.hhs.texas.gov/handbooks/electronic-visit-verification-policy-handbook)
- Six federally required EVV data elements; CalEVV visit-exception and correction workflow; Medicaid ID immutability, status codes `02`/`04`, SequenceID discipline — [CalEVV Alternate EVV User Guide (Oct 2025)](https://www.dhcs.ca.gov/wp-content/uploads/2025/10/Alternate-EVV-User-Guide.pdf)
- Published alt-EVV interface specifications: [NC OpenEVV-altEVV v7.10](https://medicaid.ncdhhs.gov/documents/providers/programs-services/evv/openevv-altevv-v7-10-final/download), [Ohio ODM Alt-EVV v4.3](https://dam.assets.ohio.gov/image/upload/medicaid.ohio.gov/Providers/EVV/AltSystem/ODM_AltDataCollectionInterface_v4.3_8-28-2025.pdf), [Arizona AHCCCS](https://www.azahcccs.gov/AHCCCS/Downloads/EVV/OpenEVV_AltEVV.pdf), [Rhode Island 3.2](https://eohhs.ri.gov/sites/g/files/xkgbur226/files/2022-07/RI%20Alt%20EVV%20Specification%203.2.pdf), [Pennsylvania DHS](https://www.pa.gov/agencies/dhs/resources/for-providers/evv/alternate-evv)
- NJ Office of the State Comptroller PCA guidance: monthly eligibility verification, retroactive MCO authorization modification, caregiver license/certification number required in the EVV record, "EVV was not implemented as a timesheet solution" — [NJ Comptroller PCA Q&A](https://www.nj.gov/comptroller/library/Resources/PCA%20Q%20and%20A%20(Final)_10242023.pdf)
- Wage-and-hour enforcement: $85,000+ settlement including $77,000 restitution to 79 workers for reduced-rate overtime and unpaid travel time between job sites — [Massachusetts Attorney General](https://www.mass.gov/news/home-health-agency-to-pay-more-than-85000-for-failing-to-pay-workers-overtime-and-travel-time)
- FLSA companionship/live-in rulemaking: NPRM published 2 July 2025, comments closed 2 September 2025, **no final rule or effective date announced; 2013 rule remains operative** — [DOL Direct Care](https://www.dol.gov/agencies/whd/direct-care), [Federal Register 2025-12316](https://www.federalregister.gov/documents/2025/07/02/2025-12316/application-of-the-fair-labor-standards-act-to-domestic-service), [Littler analysis](https://www.littler.com/news-analysis/asap/dol-proposes-rule-reinstate-companionship-live-exemptions-minimum-wage-and)
- State licensure survey personnel-file items: application, license/certification verification, competency evaluation, references, criminal background check, TB/substance screening, annual evaluation, in-service training records — [Virginia home care licensure survey checklist](https://townhall.virginia.gov/l/GetFile.cfm?File=C:%5CTownHall%5Cdocroot%5CGuidanceDocs%5C601%5CGDoc_VDH_4271_v3.pdf); see also [NC initial survey checklist](https://info.ncdhhs.gov/dhsr/ahc/pdf/checklist.pdf), [Washington DOH in-home services survey program](https://doh.wa.gov/licenses-permits-and-certificates/facilities-z/home-care-agencies/survey-program)
- OIG home health provider compliance audit series, including the 2026 finding that internal safeguards "failed to detect the errors" due to "staffing shortages and human error" — [Alternate Solutions Homecare of Dayton (2026)](https://oig.hhs.gov/reports/all/2026/medicare-home-health-agency-provider-compliance-audit-alternate-solutions-homecare-of-dayton/), [VNS Health (2026)](https://oig.hhs.gov/reports/all/2026/medicare-home-health-agency-provider-compliance-audit-vns-health/)
- Practitioner product complaints (system slowness, EVV freezes, 10-minute clock-in visibility delay, claim batch miscounts, poor support) alongside praise for credential expiry alerts — [Capterra HHAeXchange reviews](https://www.capterra.com/p/140366/eXchange-Suite/reviews/?page=3)

### Strong inferences — well-supported but industry- or vendor-sourced

- **82% of Medicaid claim denials** in home care stem from administrative, eligibility and documentation failures rather than billing errors; named triggers include caregiver codes not matching the authorization, expired/exceeded authorizations, and missing EVV data points — [HHAeXchange](https://www.hhaexchange.com/blog/billing-problems). Vendor-published; the causal breakdown is consistent with the OIG and state audit record, so treated as strong.
- Median agency revenue **$1.40M vs $3.15M** split on inquiry tracking, gap widening five consecutive years — [Activated Insights 2026 Home Care Benchmarking Report, via Home Care Post](https://www.homecarepost.com/activated-insights-releases-2026-home-care-benchmarking-report/) (full report paywalled)
- Caregiver turnover in the **77–80%** range — [HCAOA](https://www.hcaoa.org/newsletters/home-care-turnover-rate-jumps-to-80hcaoa-is-here-to-help-members)
- Hiring funnel: **3.19 days application→interview, 46.1% application-to-interview conversion, 42.6% interview no-show, 12.8% cancellation**; applicants apply to 10–20 agencies — [HelloHire, May 2026](https://www.tryhellohire.com/the-state-of-home-care-hiring-may-2026-hiring-trends/) (vendor's own customer base, so optimistic on speed metrics)
- Payer payment lags: **Medicaid waiver 45–65 days, private LTC insurers 70–90+ days**; DSO above 60–65 days signals systemic issues — [PRN Funding](https://prnfunding.com/why-accounts-receivable-management-is-the-key-to-scaling-your-homecare-agency/) (a factoring company — directionally credible, motivated on the conclusion)
- Payroll structural problems: disconnected systems requiring hours of manual reconciliation despite "integrations," 50+ visit types driving pay-code sprawl, chronic off-cycle runs as a systemic-failure signal — [Whirks](https://www.whirks.com/blog/home-care-payroll-problems)
- Industry scale: ~35,000 home care companies, ~17,000 in personal care specifically — [Ankota](https://www.ankota.com/home-care-industry-overview-and-statistics)

### Tentative hypotheses requiring practitioner validation

- **That a per-visit manual-edit flag is present in ordinary user-accessible exports** from HHAeXchange, Sandata, AxisCare and WellSky Personal Care. This is the single load-bearing assumption for the top-ranked concept and it has not been verified. Everything else in C1 is arithmetic.
- **That the exception queue costs 5–10 admin hours per week** at a 100-client agency. Reasonable from the described workflow; no published measurement found.
- **The $67,000/year missed-visit figure** ($140 × 10 visits/week) — [Alora](https://www.alorahealth.com/blog-the-financial-impact-of-missed-homecare-visits/). Vendor-constructed illustration, not measured; the per-visit rate is plausible for skilled home health and far too high for personal care. Use the *mechanism*, not the number.
- **That LTC insurance packet assembly is a significant recurring back-office cost.** Sourced only to agency marketing content ([Assisting Hands](https://assistinghands.com/130/tennessee/franklin/blog/common-long-term-care-insurance-claim-mistakes/)) and inferred from the 70–90+ day AR lag. C8 should not be built before a practitioner confirms both volume and pain.
- **That alt-EVV file rejection is frequent enough at small agencies to justify C10 on its own.** The specs are verified; the rejection frequency is not. C10 may be a better product for alt-EVV *vendors* than for agencies.
- **That platform vendors will continue not to build the per-payer mid-quarter view.** Reasoned from incentives, not from evidence.
