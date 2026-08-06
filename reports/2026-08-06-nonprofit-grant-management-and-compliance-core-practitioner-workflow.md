# Nonprofit Grant Management and Compliance — Core Practitioner Workflow

**Market research cycle report**

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market claimed** | Nonprofit grant management and compliance |
| **Angle claimed** | core-practitioner-workflow |
| **Claim ID** | `3e860bb7` |
| **Date** | 2026-08-06 |
| **Backlog remaining after this claim** | 184 assignments across 64 distinct markets |
| **Reports completed before this one** | 7 |

### Why this assignment over the others available

The ledger showed seven completed reports concentrated in four sectors: architecture/engineering/construction (fire protection design, land surveying, MEP mechanical design — three of seven), legal services (immigration), insurance distribution (commercial lines agency back-office), discrete manufacturing (machine shop quoting), and logistics (freight brokerage). Sixty-four distinct markets sat in the backlog, of which fifty-seven had zero completed entries.

The claiming rule prefers markets with zero coverage, then markets where strong practitioner evidence exists online, then angles that expand catalog diversity. Nonprofit grant management wins on all three:

1. **Zero coverage, and orthogonal to everything already done.** The nonprofit sector is the only entry in the backlog that is not a for-profit professional services firm, a trade contractor, or a manufacturer. Every completed report so far describes a business that invoices a client. A grants office does not invoice anybody — its revenue arrives conditioned on documented compliance with a rule set it did not write. That is a structurally different economic engine and it produces a different class of software problem. Adding it widens the catalog's reach more than an eighth AEC report would.

2. **Unusually strong and unusually *specific* evidence.** Most markets require inferring rules from practice. Here the rules are published, numbered, and enumerable: 2 CFR Part 200 states exactly which fourteen data elements must appear in a subaward, exactly which ten actions require prior written approval, and exactly what documentation supports a payroll charge. Grants.gov publishes the exact filename character set that will cause a submission to be rejected. A specification that precise is the best possible input to a small, narrowly scoped, deterministic tool.

3. **A live, dated regulatory transition.** OMB published a proposed rewrite of the Uniform Guidance in the Federal Register on 29 May 2026; the comment period closed 13 July 2026; the target effective date is 1 October 2026, the start of FY2027. Roughly two months from the date of this report, tens of thousands of grantees will need to re-inventory their awards, stand up subaward reporting workflows, and re-audit spending against changed allowability rules. Regulatory transitions are the single most reliable generator of demand for narrow, cheap, immediately-useful tools.

The **core-practitioner-workflow** angle was chosen over back-office deliberately. A grants manager's *production* work — the thing the organization hires the role to do — is the award lifecycle itself: reading the agreement, building the budget, charging costs correctly, assembling the reports, closing out. Leaving the back-office angle unclaimed keeps a clean lane for a later run to cover organization-level finance, audit preparation, and charitable-registration administration without overlap.

---

## 1. Market examined

**Industry.** US charitable nonprofits that receive restricted grant funding from federal agencies, state and local pass-through entities, private foundations, and corporate funders.

**Scale of the sector.** The IRS recognized approximately **1.5 million** charitable, religious, and similar tax-exempt organizations in FY2024. Nonprofits employed **12.8 million** workers in 2022 — nearly 10% of the private-sector workforce. **Government grants and contracts account for roughly 32% of nonprofit revenue** sector-wide, making government the single largest institutional funding stream. ([National Council of Nonprofits, *About the Nonprofit Sector 2025*](https://www.councilofnonprofits.org/files/media/documents/2025/ncn-about-the-nonprofit-sector-2025.pdf))

**Which organizations actually matter for this catalog.** The size distribution is extremely bottom-heavy: 59% of organizations report annual budgets under $50,000, and **97% operate below $5 million**. The $50k-and-under tier is mostly volunteer-run and does not buy software. The realistic target band is:

- **Lower bound — roughly $500k annual budget.** Below this, an organization typically holds one or two small foundation grants and no federal award. Compliance obligation is thin.
- **Sweet spot — $1M to $15M annual budget.** These organizations hold somewhere between four and forty concurrent restricted awards, frequently including at least one federal or federal pass-through award. They have a finance person and a development person but usually not a dedicated grants compliance specialist. They are above the single-audit threshold or close enough to it to be nervous.
- **Upper bound — roughly $25M.** Above this, organizations begin buying Sage Intacct, Blackbaud, or a purpose-built grants platform and hiring a full-time compliance director. They are no longer the buyer for a small focused tool.

**The user.** Titles vary widely and the role is rarely pure. From active August 2026 job postings: *Grants & Compliance Manager* (Gulfcoast Legal Services, up to $65,000 — the same person writes proposals, manages reporting schedules, coordinates cross-departmental data collection, compiles programmatic *and* financial outcomes, and supports audit activity); *Grants Coordinator* (Diocese of Orlando, $45,704–$65,754); *Senior Grant Compliance Manager* (YWCA Seattle/King/Snohomish, $108,000–$118,000); *Grants Manager*, part-time at $25/hour (Devereux). The named technical skill requirements in these postings are Microsoft Excel, Word, and Adobe Pro — not a grants platform.

That last point is the market thesis in miniature. **61% of organizations depend on only one or two people for grant writing and submission**, and 74% of grant seekers are internal employees rather than contractors ([Instrumentl grant statistics](https://www.instrumentl.com/blog/grant-statistics-and-trends)). The typical user is a competent generalist, working alone, holding an entire regulated lifecycle in a spreadsheet, whose employer's continued ability to make payroll depends on her getting the paperwork right.

**A note on employment risk that shapes buying behavior.** The Gulfcoast posting states plainly: *"GLS is a non-profit agency and relies on grant funding. Continued employment is contingent upon grant funding."* The person operating this software is often funded by the awards she administers. Tools that visibly reduce compliance risk are not an efficiency purchase for her — they are a job-security purchase.

---

## 2. How the work is performed

The award lifecycle below is synthesized from practitioner guidance, agency instructions, and the regulation itself. Timings are typical for a $1M–$15M organization holding a mix of federal, state pass-through, and foundation awards.

### 2.1 Pre-award: opportunity to submission

**People involved.** Grants manager (owns the process), executive director (go/no-go and signature), program director (scope, staffing, outcomes), finance director or bookkeeper (budget, indirect rate, match).

**Sequence.**

1. **Opportunity identification.** Grants.gov saved searches, state agency listservs, Candid/Foundation Directory, Instrumentl, funder 990 review. Output: a "pipeline" tab in a spreadsheet.
2. **Go/no-go.** Judgment call weighing fit, match requirement, indirect cost recovery, staff capacity, and reporting burden against expected award. Rarely documented.
3. **Registration prerequisites.** For federal awards: active SAM.gov registration with a valid UEI, Grants.gov applicant account, agency-specific portal accounts (eRA Commons, GrantSolutions, agency-specific systems). SAM registration is **active for 365 days from the date of submission — not the calendar year — with no grace period**.
4. **Narrative production.** Organizational history, need statement, program design, logic model, evaluation plan, staff qualifications, sustainability plan, letters of support. Most of this text exists in prior applications and is retrieved by opening old documents and copying.
5. **Budget construction.** For federal awards, an SF-424A by object class category, plus a budget narrative justifying every line. Salary lines require a stated effort percentage per employee. Indirect is computed either at a negotiated rate (NICRA) or at the de minimis rate.
6. **Match/cost-share commitment.** If the program requires match, the applicant commits a specific non-federal dollar amount in the proposal budget. That commitment becomes legally binding on acceptance.
7. **Package assembly and submission.** Forms plus attachments uploaded to Grants.gov Workspace or an agency/foundation portal, each with its own field limits, file-type restrictions, and naming rules.

**Effort.** A foundation application runs **15–20 hours**. A federal application runs **100+ hours**. Overall success rate is approximately **10%**; one third of grant cycles run 1–3 months from submission to decision and another third run 4–6 months ([Instrumentl](https://www.instrumentl.com/blog/grant-statistics-and-trends)).

### 2.2 Award acceptance and setup (days 1–30)

Practitioner guidance is consistent that this window determines whether the rest of the award is manageable ([Instrumentl post-award guide](https://www.instrumentl.com/blog/post-award-grant-management)):

- Full read of the executed agreement to identify prior-approval triggers, cost restrictions, and special conditions
- Creation of a dedicated cost center / class / fund code in the accounting system
- Centralized grant file with standardized naming
- Internal kickoff between program and finance
- Population of the compliance calendar with every deadline

In practice at this organization size, "the compliance calendar" is a spreadsheet. The State of New Jersey's grants-management training deck (March 2026) prescribes exactly this and specifies the columns: grant name, funder, award amount, grant period, reporting frequency, due dates, reconciliation dates, special conditions, subrecipients, match requirements — with a **color-coding convention (red = due within 30 days, yellow = 60 days, green = on track, blue = new award)** and a 30/60/90-day planning rhythm. ([NJ Treasury, *Managing Multiple Grants Without Chaos*](https://www.nj.gov/treasury/grants-management/documents/State%20of%20NJ-Lunch%20and%20Learn-Griffin%20Managing%20Multiple%20Grants%20wo%20Chaos_OCPE_March%2010%202026-FINAL.pdf))

That a state treasury department's official recommendation to grantees is *a color-coded Excel file* is the clearest available evidence that no accessible purpose-built tool exists at this end of the market.

### 2.3 Active management (ongoing)

**Monthly, per award.**

- Code expenditures to the correct cost center; allocate shared costs (rent, utilities, insurance, admin salaries) across awards
- Allocate payroll across awards — e.g. a program director at 50% Grant A, 30% Grant B, 20% unrestricted
- Reconcile the accounting system's grant-level actuals against the parallel spreadsheet the grants manager maintains
- Review burn rate against the approved budget by line item
- Log match/in-kind contributions
- Draw down federal cash (HHS Payment Management System, Treasury ASAP, or state portal) against actual incurred expenditures

**Ongoing personnel documentation.** Under 2 CFR 200.430, payroll charges must be supported by records that reflect **work actually performed**, must account for **100% of each employee's compensated time** across all activities, must be contemporaneous, and must be retained three years from final financial report submission.

**Prior-approval watch.** Under 2 CFR 200.308, ten categories of change require prior written approval before the action is taken, including scope change, key personnel change, a project director disengaging for more than three months or reducing effort by 25%, reallocating participant support costs, adding a subaward not in the proposal, changing the cost-share commitment, and requesting a no-cost extension. Separately, agencies may restrict transfers between budget categories once the **cumulative transfer exceeds 10% of the total budget** on awards above the simplified acquisition threshold.

**Subaward administration.** If the organization passes funds through, 2 CFR 200.332(b)(1) requires **fourteen specific data elements** in every subaward instrument — subrecipient name matching the UEI, the UEI itself, FAIN, federal award date, period of performance dates, budget period dates, amount obligated in this action, total obligated to date, total committed, FFATA project description, agency and pass-through contact information, Assistance Listings title and number, R&D indicator, and the indirect cost rate. The pass-through entity must also perform a documented risk assessment covering prior experience, audit history, personnel/system changes, and federal monitoring, then monitor proportionally to assessed risk.

### 2.4 Reporting cycles

Three report families run in parallel on incompatible calendars:

- **Financial reports.** Federal awards generally use the SF-425 Federal Financial Report, submitted through the Payment Management System or an agency portal, reporting cumulative cash receipts, cash disbursements, federal share of expenditures, unliquidated obligations, recipient share, program income, and indirect cost detail.
- **Programmatic/performance reports.** Activities delivered, participants served, demographic breakdowns, outcome measures against targets, narrative on challenges and successes.
- **Foundation reports.** Whatever that particular foundation asks for, in that foundation's portal, in that foundation's word limits.

The critical structural fact: **no two funders ask for the same thing in the same shape, but they mostly ask about the same underlying reality.** The same client-served count, the same salary dollars, the same outcome measure gets pulled from the case management system, the accounting system, and last quarter's report, then reformatted three different ways.

The measured cost of that is substantial. One analysis of reporting workload reports **mid-sized organizations spending 100+ staff hours per quarter on funder reports**, and a development director's time study showing **~45 hours per quarter across multiple staff**, of which **70% was data extraction, reconciliation, and formatting** rather than analysis or writing ([FundEasy](https://fundeasy.com/blog/why-grant-reporting-is-eating-your-staff-alive)).

### 2.5 Amendments, closeout, and audit

Budget modifications and no-cost extensions require agency-specific request forms and justifications. Closeout (final 60 days) requires final narrative and financial reports, reconciliation, return of unexpended funds, disposition of equipment, and records retention for three years from final expenditure report submission.

If federal expenditures cross **$1,000,000** in a fiscal year — raised from $750,000 by the 2024 Uniform Guidance revisions, effective for fiscal years ending 30 September 2025 and after — the organization must undergo a **Single Audit**, which requires a Schedule of Expenditures of Federal Awards (SEFA) reconciled to the general ledger and tested against each major program's compliance requirements.

### 2.6 Software currently in use

| Layer | What is actually used | Where it falls short |
|---|---|---|
| Accounting | QuickBooks Online with classes/locations/projects; Aplos; occasionally Sage Intacct at the top of the range | No native grant lifecycle, no restriction logic tied to transactions, no real-time remaining-budget view, no funder-formatted reporting; requires "export data, reformat reports manually, and customize views for each funder" |
| Grant tracking | **Excel or Google Sheets**, per state-agency training decks and job postings | No validation, no cross-award checks, breaks silently, dies with the employee who built it |
| Prospect research / pipeline | Instrumentl, Candid Foundation Directory, GrantStation | Priced for larger orgs; pre-award focused |
| Proposal writing | Word + copy/paste from prior applications; increasingly Grantable, Granted AI, Grant Assistant | Content libraries are new and largely unvalidated; do not bind numbers to source data |
| Submission | Grants.gov Workspace, agency portals, foundation portals (Submittable, Foundant, Fluxx grantee side) | Validation is post-hoc and cryptic; errors surface at submission |
| Payments | HHS Payment Management System, Treasury ASAP, state portals | Separate credentials, separate reconciliation |
| Registration | SAM.gov, UEI, agency portals | Annual expiry, no organizational memory |

**Price points of the incumbent tooling.** Instrumentl's published 2026 tiers run **$3,588/year** (single user), **$5,988/year** (team), and **$11,988/year** (full lifecycle). One analysis notes that for an organization on a $150k–$200k budget the base tier represents 1–2% of total revenue and "could consume half of their annual tech budget," since nonprofits typically allocate 3–5% of budget to technology overall, and concludes negative ROI below roughly $2M in revenue. Cheaper adjacent tools sit near **$99/month** (GrantStation, Grantable). ([FundRobin pricing analysis](https://www.fundrobin.com/articles/how-to-guide/ai-tools-for-nonprofits/instrumentl-pricing-roi-small-nonprofits-2026/))

**Open-source coverage is effectively nil.** Searches of software directories for open-source grant management return general project-management tools and CRM re-labels, not grant-lifecycle software. There is no equivalent of an OpenProject or a Dolibarr for this domain. That is a real gap, not a marketing observation.

---

## 3. Most important problems, ranked

### P1. Payroll is charged to grants by budgeted percentage rather than documented actual effort

**Who.** Every organization charging salaries to federal or federal pass-through awards. Highest exposure at organizations without a formal time-tracking system.

**When.** Every payroll run; discovered at audit, up to three years later.

**Currently handled how.** A standing allocation table — "Maria is 50/30/20" — entered once in payroll setup and left alone. Effort certification, where it happens, is a semi-annual form signed after the fact to match what was already charged.

**Why inadequate.** 2 CFR 200.430 requires records reflecting work actually performed and explicitly rejects budget estimates as documentation. If the employee actually spent 30% on the grant, only 30% is allowable — the other 20% is a questioned cost. Certifications signed by supervisors without first-hand knowledge, and records completed weeks later to match already-charged amounts, are both named failure modes.

**Frequency and cost.** Personnel is **60–80% of most federal grant budgets**, which makes this the largest single dollar exposure in the award and the most common source of audit findings. Auditors may examine the full three-year retention period, so a systematic allocation error compounds across every payroll in that window. On a $500,000 award with $350,000 of personnel, a 10-percentage-point overcharge is $35,000 of questioned cost per year. ([GrantMetric](https://grantmetric.com/grant-management/federal-grant-time-effort-reporting))

**Evidence quality.** Verified — regulation text plus multiple independent compliance-practice sources naming it the leading finding category. Small nonprofits are explicitly identified as more exposed than large institutions because they assign staff to grants by position rather than documenting hours.

---

### P2. Every funder report requires the same facts in a different shape, and assembling them is manual

**Who.** Grants manager, plus program staff pulled in for data, plus finance for the numbers.

**When.** Monthly, quarterly, semi-annually, and annually — on as many different calendars as the organization has funders.

**Currently handled how.** Open the funder's template or portal. Pull outcome data from the case management system, financial data from QuickBooks, demographics from a third system. Reconcile them by hand. Retype into the funder's fields and word limits.

**Why inadequate.** The measured split is **70% extraction, reconciliation, and formatting vs. 30% analysis and writing**. Nearly three-quarters of the effort produces no new information; it moves existing information between formats. It is also the point where program and finance numbers diverge, because they are reconciled once per report rather than continuously.

**Frequency and cost.** **100+ staff hours per quarter** at mid-sized organizations, ~45 hours per quarter in one documented time study. At a fully loaded $45/hour, 100 hours per quarter is roughly **$18,000/year of staff time spent reformatting**.

**Evidence quality.** Verified for the qualitative pattern across many independent sources; the specific hour figures come from a single vendor-published analysis and should be treated as directional rather than precise.

---

### P3. Shared costs and indirect are allocated by informal, poorly documented methods

**Who.** Bookkeeper or finance director, at organizations holding more than two restricted awards.

**When.** Monthly close.

**Currently handled how.** A spreadsheet that splits rent, utilities, admin salaries, and insurance across awards on a percentage that was decided once — often by revenue share — and rarely revisited or documented. Indirect is applied at a flat rate without carefully computing the base.

**Why inadequate.** Two independent failures. First, the *allocation basis* must be documented, consistently applied, and defensible; "insufficient documentation of payroll allocations" and "inconsistent application of indirect costs" are named single-audit findings. Second, the *base* is arithmetically fiddly: the de minimis rate applies to **Modified Total Direct Costs**, which excludes equipment, capital expenditures, participant support costs, rent, tuition, scholarships, and — under the 2024 revisions — includes only the **first $50,000 of each subaward**. The 2024 revisions also raised the de minimis rate from 10% to **15%**, which means every organization that elected de minimis before October 2024 and has not re-elected is leaving 5 percentage points of recovery on the table.

**Frequency and cost.** Monthly, forever. On $2M of MTDC, the difference between 10% and 15% is **$100,000 per year of unrecovered indirect** — money the organization is entitled to and is not claiming.

**Evidence quality.** Verified. Regulation text plus multiple accounting-firm compliance summaries.

---

### P4. Federal applications are rejected or delayed for mechanical, entirely preventable packaging faults

**Who.** Whoever hits submit — usually one person, often at 4:45pm on the deadline date.

**When.** At submission, after 100+ hours of work.

**Currently handled how.** Careful manual checking against the NOFO, then hope.

**Why inadequate.** Grants.gov enforces rules that are strict, published, and invisible until violated. Attachment **filenames must be 50 characters or fewer** and may use only a specified UTF-8 character set; violations produce a `VIRUSDETECT` error or cause "the entire application to be rejected or cause issues during processing." Other named failure modes: mandatory forms not completed, blank spaces left in fields, schema validation errors from an incompatible Adobe Reader version, and transmission failures that leave no tracking number. None of these have anything to do with the quality of the proposal.

**Frequency and cost.** Low frequency per organization, catastrophic per occurrence. A federal deadline missed by a filename is the loss of 100+ hours of labor plus a full funding cycle — commonly 12 months. Against a ~10% success rate, the expected value destroyed by one rejected submission is the entire cost of roughly ten applications' worth of pipeline.

**Evidence quality.** Verified directly from Grants.gov's own published instructions and error-message documentation.

---

### P5. Match and cost-share commitments are under-documented and double-counted

**Who.** Organizations holding awards with a match requirement — common in federal formula programs, DOE, USDA, and most state pass-throughs.

**When.** Continuously during performance; discovered at audit.

**Currently handled how.** A tab in the grant spreadsheet listing in-kind contributions, often valued by estimate, sometimes supported by a pledge letter.

**Why inadequate.** 2 CFR 200.306(b) imposes a seven-part test on every contribution: verifiable from records, not counted toward any other federal award, necessary and reasonable, allowable, not federally paid, in the approved budget, and conforming to Part 200. "A pledge letter is not verification, and neither is a good-faith estimate. Auditors want the same trail they would demand for a direct cost." Valuation rules are specific and frequently mis-applied — loaned equipment must be valued at **fair rental value, not purchase price**; donated space at fair rental value of comparable local space; volunteer time at the rate the organization would pay for similar work. **The most frequent finding is double-counting the same staff hour or dollar against two awards**, a check that is structurally impossible to perform inside a single-award spreadsheet.

**Frequency and cost.** Once accepted in a proposal budget, match is a binding obligation. A 50% cost-share requirement on a $1,000,000 federal award obligates $1,000,000 of documented non-federal spending. Undocumented match is disallowed dollar-for-dollar against the federal share.

**Evidence quality.** Verified — regulation text plus practitioner analysis identifying double-counting as a recurring single-audit finding.

---

### P6. Prior-approval triggers are tripped without anyone noticing

**Who.** Program directors making ordinary operational decisions; the grants manager finds out later.

**When.** Whenever staffing changes, a purchase is made, or spending drifts between categories.

**Currently handled how.** Institutional memory. The award agreement was read once at kickoff.

**Why inadequate.** Ten enumerated actions require prior *written* approval — approval obtained after the fact does not cure the violation. A project director reducing effort by 25%, a subaward not in the original proposal, a change to the cost-share amount, moving participant support costs — these are all things a program director would reasonably do without thinking to check. The 10% cumulative-transfer restriction is worse, because no single transaction trips it; it accumulates silently across a year.

**Frequency and cost.** "Missed prior approval requirements triggering compliance violations" is a named recurring pain point. Costs incurred under an unapproved change are questioned costs.

**Evidence quality.** Verified from 2 CFR 200.308 plus practitioner guidance.

---

### P7. Registrations and prerequisites expire silently and freeze the money

**Who.** The whole organization, via whoever holds the SAM.gov Entity Administrator role — frequently someone who has left.

**When.** 365 days after the last submission, on a date nobody has written down.

**Currently handled how.** Automated reminder emails, sent to whatever address was on the account.

**Why inadequate.** Registration is active for **365 days from the date of submission, not the calendar or fiscal year**, and every organization has a unique expiration date. There is **no grace period**. On lapse: no new awards, no payment processing, and **existing grant drawdowns freeze**. Reactivation requires IRS and CAGE validation of "up to 10 business days," with practical recovery of **two to four weeks**. The named failure mode is passive expiration — "reminders sent to departed staff; organizations discover lapses only when payments fail." A March–July 2026 SAM.gov defect that corrupted NAICS codes, employee counts, and revenue data on renewal makes post-renewal verification necessary as well.

**Frequency and cost.** Once a year per registration, with several registrations in play. A lapse discovered when payroll cannot be made is an operational emergency at an organization with a two-month cash reserve.

**Evidence quality.** Verified from federal registration guidance.

---

### P8. Sub-recipient administration is assembled by hand from a regulation checklist

**Who.** Organizations that pass funds to partners — coalitions, backbone organizations, larger nonprofits with community partners.

**When.** At every subaward execution and every modification.

**Currently handled how.** Last year's subaward agreement, edited in Word.

**Why inadequate.** Fourteen mandatory data elements must be present and correct in every subaward instrument, several of which (FAIN, federal award date, Assistance Listings number, indirect cost rate, R&D indicator) are copied from the prime award and are easy to transcribe wrong. Risk assessment must be documented against four specified factors and must drive the monitoring plan. "Skipped risk assessments" and "failure to review subrecipient audit reports" are named findings. The 2024 threshold increase makes this materially harder: subrecipients whose federal expenditures now fall below $1,000,000 no longer produce a single audit, so **pass-through entities that relied on reading a subrecipient's audit report must now build an alternative monitoring method from scratch**.

**Frequency and cost.** Per subaward per year. The pass-through entity is liable for its subrecipients' noncompliance.

**Evidence quality.** Verified from 2 CFR 200.332 and accounting-firm analysis of the 2024 revisions.

---

### P9. Drawdowns and the SF-425 diverge from the general ledger

**Who.** Finance director or bookkeeper.

**When.** Each drawdown; each quarterly FFR.

**Currently handled how.** Draw against projected cash need, reconcile later.

**Why inadequate.** Federal cash management requires drawdowns to match expenditures actually incurred. Named errors: premature drawdown before costs are earned, co-mingling multiple awards rather than maintaining separate job cost reports with properly allocated indirect, drawing on cash need rather than revenue recognized, and — the most common — "reporting amounts drawn down to match the amounts earned without the underlying documentation to support that assertion." Excess cash on hand and unreconciled draws are standard cash-management findings.

**Frequency and cost.** Monthly to quarterly. Findings here can trigger reimbursement-basis payment, which is a severe cash-flow penalty for an organization with thin reserves.

**Evidence quality.** Verified.

---

### P10. Narrative content is rebuilt from scratch every application

**Who.** Grant writer / grants manager.

**When.** Every application, ~15–20 hours for a foundation ask.

**Currently handled how.** Open the last three applications, copy paragraphs, edit. Storage in SharePoint or Google Drive "organizes files but lacks intelligence to understand content meaning."

**Why inadequate.** The genuinely repeated material — organizational history, program descriptions, staff qualifications, evaluation frameworks, sustainability strategies — is not the hard part of a proposal, but it consumes the hours. Worse, embedded *numbers* go stale: last year's client count, last year's budget, last year's staff roster get copied forward into this year's application without anyone noticing.

**Frequency and cost.** Constant. At a ~10% success rate with 15–20 hours per foundation application, an organization submitting 25 applications a year invests 375–500 hours to win 2–3.

**Evidence quality.** Strong inference. The pattern is widely described and a commercial category has formed around it; the specific time-saving claims come from vendors and are unvalidated.

---

## 4. Application opportunities

### A1. Grants.gov Package Preflight

| | |
|---|---|
| **Intended user** | Grants manager assembling a federal application |
| **Complexity** | Small |
| **AI** | Inappropriate for the core check; optional for NOFO parsing |

**Problem solved.** A federal application representing 100+ hours of work is rejected for a filename, a blank field, or a missing form (P4).

**Current workflow.** Manual check against the NOFO, upload, submit, hope, check the tracking email.

**Proposed workflow.** Point the tool at the folder holding the application package. It walks every file and reports, in one screen: filenames over 50 characters, filenames containing characters outside the permitted UTF-8 set, disallowed file extensions, scanned-image PDFs where a text PDF is required, page counts against declared limits, embedded font and margin compliance where the NOFO specifies them, and a required-attachment checklist reconciled against a user-entered list. Each finding names the file and the exact fix. Optionally exports a corrected copy with sanitized filenames.

**Inputs.** A local folder of application files; optionally the NOFO PDF; optionally a required-attachment list.

**Outputs.** A pass/fail report with per-file findings; a sanitized copy of the package.

**Essential features.** Filename character and length validation against the published Grants.gov rule set; extension whitelist; scanned-vs-text PDF detection; page count per file; required-file checklist; one-click filename remediation with a rename log.

**Excluded from initial scope.** Submitting to Grants.gov. Reading the applicant's account. Any judgment about proposal quality. Any portal other than Grants.gov in v1.

**AI.** Inappropriate for the validation itself — these are deterministic string and file rules, and a language model would introduce nondeterminism into a check whose entire value is that it is exactly right. Optional and genuinely useful as a *separate* v2 feature: extracting the "required attachments" and page-limit table from a 90-page NOFO PDF into the checklist, which is a real extraction problem conventional code handles poorly.

**Why not a spreadsheet.** A spreadsheet cannot read a directory, inspect a PDF's page count, or detect whether a PDF contains a text layer.

**Learning difficulty.** Minutes. Drop a folder in, read the list.

**Value.** Prevents a low-frequency, total-loss event. One prevented rejection saves 100+ hours plus a funding cycle.

**Risks and constraints.** The rule set changes when Grants.gov changes it — the rules must live in an editable config file, not in code, and the tool must display which rule-set version it checked against and when that version was published. No application content leaves the machine, which sidesteps confidentiality concerns entirely.

**Existing substitutes.** Grants.gov's own validation, which runs *after* submission and returns cryptic errors like `VIRUSDETECT`. Agency-specific checkers exist for some programs. No general-purpose free preflight tool.

**Why still attractive.** The rule set is published, stable, and mechanically checkable. The failure it prevents is catastrophic and entirely avoidable. It is the cleanest small-tool opportunity in this market.

**Paid customization.** Agency-specific and state-portal rule packs; organization-specific required-attachment templates; integration into an organization's shared drive structure.

---

### A2. Effort Allocation and Certification Workbook

| | |
|---|---|
| **Intended user** | Finance director / bookkeeper / grants manager |
| **Complexity** | Medium |
| **AI** | Inappropriate |

**Problem solved.** Payroll charged by budgeted percentage rather than documented actual effort — the single largest dollar exposure and the leading audit finding category (P1).

**Current workflow.** A fixed allocation table in payroll setup; semi-annual certification forms signed to match what was already charged.

**Proposed workflow.** Each period, staff (or supervisors) record actual hours or effort percentage by activity — grant-funded, other-grant-funded, unrestricted, fundraising, admin. The tool enforces that every employee's entries total 100% of compensated time, imports the payroll register, computes the dollar allocation that *actually documented effort* supports, compares it against what was *charged*, and produces: (a) a per-employee, per-period effort certification ready for signature, (b) a variance report flagging any employee whose charged percentage differs from documented percentage by more than a settable tolerance, and (c) a proposed correcting journal entry.

**Inputs.** Payroll register export (CSV from QuickBooks, Gusto, Paychex, ADP); a roster of awards; effort entries.

**Outputs.** Signed-ready effort certifications (PDF); charged-vs-documented variance report; correcting journal entry file; an audit packet for a selected date range.

**Essential features.** 100%-of-time enforcement; period locking so records cannot be silently backdated; an immutable change log recording who changed what and when (this is the feature that converts the output from "a spreadsheet" to "contemporaneous documentation"); charged-vs-actual reconciliation; per-award personnel cost rollup.

**Excluded from initial scope.** Being a timesheet system for hourly payroll. Payroll processing. Integration with any HRIS beyond CSV import. Project-level time tracking below the award level.

**AI.** Inappropriate. Every operation is arithmetic and rule-checking against a regulation. Introducing a model here would create audit exposure rather than reduce it.

**Why not a spreadsheet.** The 100%-of-time constraint across many employees and awards, period locking, and a tamper-evident change log are precisely what a spreadsheet cannot provide — and the change log is the thing an auditor asks for. A spreadsheet that can be silently edited after the fact is the exact failure mode the regulation names.

**Learning difficulty.** Under an hour for the finance user; a few minutes for staff entering effort.

**Value.** Directly addresses the largest questioned-cost exposure in the award. On a $500k award with $350k of personnel, catching a 10-point misallocation is $35,000/year.

**Risks and constraints.** Contains employee compensation data — must run locally or self-hosted, never in a shared cloud instance without explicit design. Retention must span three years past final report. The tool must be clear that it *documents* effort; it cannot make an undocumented allocation compliant.

**Existing substitutes.** University-grade effort reporting systems (Huron, Cayuse) priced for research institutions. Some payroll systems allocate but do not certify or reconcile. Nothing free and nothing at this scale.

**Why still attractive.** The compliance requirement is universal for federal grantees, the exposure is the largest in the budget, and small nonprofits are explicitly identified as the most vulnerable population precisely because they lack a formal system.

**Paid customization.** Payroll-system-specific importers; agency-specific certification form layouts; multi-entity/fiscal-sponsor configurations.

---

### A3. Cost Allocation and Indirect Recovery Calculator

| | |
|---|---|
| **Intended user** | Bookkeeper / finance director |
| **Complexity** | Medium |
| **AI** | Inappropriate |

**Problem solved.** Shared costs allocated by undocumented methods, and indirect under-recovered because the MTDC base is computed wrong or the 15% de minimis election was never updated (P3).

**Current workflow.** A spreadsheet splitting rent and admin by a revenue-share percentage decided once, plus a flat indirect application.

**Proposed workflow.** Define cost pools (occupancy, IT, admin salaries, insurance) and an allocation basis for each (FTE count, square footage, direct salary dollars, modified total direct cost). Import the trial balance by class. The tool computes the allocation, produces the journal entry, and — critically — produces a **defensible allocation worksheet** showing the basis, the driver values, the math, and the period, in a form that answers an auditor's question directly. Separately, it computes MTDC per award with correct exclusions (equipment, capital expenditures, participant support, rent, tuition, scholarships) and the **$50,000-per-subaward cap**, applies either the negotiated rate or the 15% de minimis rate, and reports the difference between what was recovered and what was recoverable.

**Inputs.** Trial balance or GL export by class/award; cost pool definitions; driver values (FTE, square footage); award list with rate elections and any funder-imposed rate caps.

**Outputs.** Monthly allocation journal entry; per-period allocation worksheet with methodology narrative; indirect recovery report showing claimed vs. claimable; a written cost allocation plan document.

**Essential features.** Multiple pools with independent bases; MTDC computation with the full exclusion list and subaward cap; de minimis vs. negotiated rate handling; funder rate caps (many state and foundation funders cap below the federal rate); recovery-gap reporting.

**Excluded from initial scope.** Being a general ledger. Posting entries back to the accounting system (export a file; let the bookkeeper post it). Preparing a NICRA proposal package.

**AI.** Inappropriate. This is defined arithmetic with a published exclusion list.

**Why not a spreadsheet.** It *is* a spreadsheet today, and that is the problem: the exclusion list is long and easy to get wrong, the basis is undocumented, and the whole thing breaks when awards are added. The tool's value is that the methodology is explicit, versioned, and re-runnable rather than embedded in cell formulas nobody else understands.

**Learning difficulty.** An hour to configure pools; minutes per month thereafter.

**Value.** Two-sided — reduces a named audit finding *and* recovers real money. The 10%→15% de minimis change alone is worth $100,000/year on $2M of MTDC to an organization that has not re-elected.

**Risks and constraints.** Financial data; local-first. The tool must never present its output as a substitute for an accountant's professional judgment on allocability. Funder-specific rate caps must be respected or the tool will produce over-claims.

**Existing substitutes.** Sage Intacct and Blackbaud handle allocation at their price point. QuickBooks does not. Spreadsheets do it badly and undocumented.

**Why still attractive.** The MTDC exclusion list and subaward cap are exactly the kind of fiddly, published, deterministic rule that software gets right and humans get wrong; the recovery gap makes the ROI arithmetic obvious in one screen.

**Paid customization.** Organization-specific cost allocation plan drafting; NICRA proposal support; funder-cap rule libraries by state.

---

### A4. Match and Cost-Share Ledger

| | |
|---|---|
| **Intended user** | Grants manager; program staff logging in-kind |
| **Complexity** | Medium |
| **AI** | Inappropriate |

**Problem solved.** Match commitments under-documented, mis-valued, and double-counted across awards (P5).

**Current workflow.** A tab in the grant spreadsheet; valuation by estimate; pledge letters as "documentation."

**Proposed workflow.** Register each award's match commitment (amount, type allowed, period). Log contributions as they occur — volunteer hours, donated goods, donated space, third-party cash, unrecovered indirect where allowed — each with a required valuation basis and a required supporting-document reference. The tool applies the correct valuation rule per type, **checks every contribution against every other award's ledger to detect the same hour or dollar counted twice**, tracks cumulative match against commitment with a projection to period end, and generates a match documentation packet.

**Inputs.** Award match commitments; contribution entries; volunteer hour logs; comparable-rate references for valuation.

**Outputs.** Match status dashboard per award; double-count exception report; per-award match documentation packet for audit; a shortfall projection with time remaining.

**Essential features.** Valuation rules by contribution type (volunteer time at the rate paid for similar work; loaned equipment at **fair rental value, not purchase price**; space at comparable local fair rental value); the seven-part 200.306(b) test as an explicit per-contribution checklist; cross-award double-count detection; required-evidence enforcement that blocks a contribution from counting until a supporting document reference is attached.

**Excluded from initial scope.** Volunteer scheduling or recruitment. Donor management. Storing the documents themselves (store references and paths; the documents live in the organization's drive).

**AI.** Inappropriate. The valuation rules are published and the double-count check is set logic.

**Why not a spreadsheet.** The double-count check is inherently cross-award and cross-period. A per-award spreadsheet is structurally incapable of performing it, which is exactly why it is the most frequent finding.

**Learning difficulty.** Under an hour.

**Value.** Undocumented match is disallowed dollar-for-dollar against the federal share. On a $1M award with 50% match, the exposure is $1M.

**Risks and constraints.** The tool must not imply that its valuation is authoritative — it applies a rule and records the basis; the organization remains responsible. Volunteer names may be personal data.

**Existing substitutes.** None found at this price point. Enterprise grant systems handle match as a field, not as a documented ledger with cross-award checks.

**Why still attractive.** Sharp scope, a named recurring audit finding, a check no incumbent performs, and a regulation that supplies the entire specification.

---

### A5. Award Terms Obligation Register

| | |
|---|---|
| **Intended user** | Grants manager at award acceptance |
| **Complexity** | Medium |
| **AI** | Genuinely valuable |

**Problem solved.** Award agreements are read once at kickoff; obligations, prior-approval triggers, special conditions, and deadlines then live in someone's memory (P6, and the setup half of P2).

**Current workflow.** Read the agreement. Type deadlines into a color-coded spreadsheet. Never open the agreement again.

**Proposed workflow.** Upload the executed award agreement and any incorporated terms. The tool extracts a structured **obligation register**: every reporting deadline with type and period, every special condition, every prior-approval trigger the agreement imposes beyond the standard ten, the match commitment, the period of performance, the indirect rate and any cap, the retention period, and any programmatic deliverable with a date. Every extracted item carries a **page-and-quote citation back into the source document**. The grants manager reviews and confirms each item — nothing enters the register unconfirmed. Confirmed items export to ICS and to a portfolio view across all awards.

**Inputs.** Award agreement PDF; optionally the NOFO and general terms.

**Outputs.** A reviewed obligation register; an ICS calendar feed; a cross-award deadline view with lead-time warnings; a one-page award summary sheet for program staff.

**Essential features.** Extraction with mandatory human confirmation; citation back to source page and quote; obligation typing; lead-time rules (e.g. a 60-day pre-report trigger and a 30-day draft deadline, per the NJ Treasury model); cross-award rollup.

**Excluded from initial scope.** Task assignment and workflow. Document storage. Anything resembling a project management tool. Actually *doing* the reporting.

**AI.** Genuinely valuable and hard to replace. Award agreements are long, unstructured, inconsistently formatted across agencies and foundations, and state obligations in prose. Locating and typing them is a language task. **But the design must treat extraction as a draft.** Nothing enters the register without human confirmation, and every item shows its source quote. This is the correct shape for AI here: it drafts, the practitioner ratifies, and the citation makes ratification fast.

**Why not a spreadsheet.** The spreadsheet is the current solution and it works — for the deadlines someone remembered to type in. The value added is completeness (catching the special condition on page 34) and traceability (the quote that proves why the date is what it is).

**Learning difficulty.** Under an hour, though the review step takes real attention on the first award.

**Value.** Turns a 2–4 hour careful read into a 30–45 minute confirm-and-correct, and — more importantly — produces something a successor can inherit. At organizations with turnover in a one-person grants role, this is the difference between institutional memory and starting over.

**Risks and constraints.** Award agreements may contain confidential terms; a local or self-hosted model, or explicit consent for cloud processing, is required. **The biggest risk is over-trust** — a missed obligation the tool did not extract is worse than no tool, because the register creates false confidence. The UI must state coverage limits plainly and never present the register as complete.

**Existing substitutes.** Enterprise grant management platforms have calendar modules but do not extract from agreements. Generic contract-analysis tools are priced for legal departments and are not tuned to award terms.

**Why still attractive.** It is the highest-leverage 30 minutes in the entire lifecycle, and it is the natural hub that later tools can attach to.

**Paid customization.** Agency-specific extraction tuning (HHS, DOJ, DOE, ED, state agencies); foundation-specific templates; integration into an existing calendar or shared drive.

---

### A6. Subaward Builder and Monitoring Register

| | |
|---|---|
| **Intended user** | Pass-through entity grants manager |
| **Complexity** | Medium |
| **AI** | Inappropriate |

**Problem solved.** Subaward instruments are edited from last year's Word file and routinely omit or mis-transcribe required elements; risk assessments are skipped; monitoring is undocumented (P8).

**Current workflow.** Copy last year's agreement, change the names.

**Proposed workflow.** Enter the prime award once. For each subaward, the tool generates all **fourteen 200.332(b)(1) data elements** — most inherited automatically from the prime, which eliminates the transcription errors — and refuses to produce an agreement with any element blank. It then runs a scored risk assessment against the four required factors, and the score drives a generated monitoring plan (frequency, method, evidence required). It tracks SAM.gov exclusion checks, subrecipient audit report receipt, and — new under the proposed rule — **subaward reporting to SAM.gov above $30,000**.

**Inputs.** Prime award data; subrecipient information (name, UEI, audit history, prior experience); risk assessment responses.

**Outputs.** A complete subaward data-elements sheet ready to attach to the agreement; a documented risk assessment; a monitoring calendar and evidence log; an exception report for missing audit reports, expired exclusion checks, or overdue monitoring.

**Essential features.** All fourteen elements with inheritance from the prime; completeness enforcement; four-factor risk scoring with the score driving monitoring intensity; monitoring evidence log; the sub-$1M alternative-monitoring path (see below).

**Excluded from initial scope.** Drafting subaward legal terms. Payment processing to subrecipients. Being a contract management system.

**AI.** Inappropriate. The regulation enumerates the fields; this is a form with inheritance and validation.

**Why not a spreadsheet.** Inheritance from prime to sub, completeness enforcement, and monitoring scheduling driven by risk score are workflow logic, not a grid. And a spreadsheet does not refuse to be wrong.

**Learning difficulty.** Under an hour.

**Value.** Prevents a finding class the pass-through entity is directly liable for, and cuts subaward setup from hours of careful copying to minutes.

**Risks and constraints.** The regulation is being rewritten effective 1 October 2026; the element list must be versioned with an effective date so an organization can see which rule set a given subaward was built under.

**Existing substitutes.** University research administration systems. Harvard's publicly posted subrecipient monitoring toolkit is a set of Word and Excel templates — which tells you what the state of the art is even at a well-resourced institution.

**Why still attractive.** The **2024 threshold change created new, dated demand**: subrecipients now falling below $1,000,000 in federal expenditures no longer produce a single audit, so pass-through entities that relied on reading audit reports must build an alternative monitoring method. That is a specific, recent, universal problem with no established solution — and it is exactly the sort of gap an enterprise vendor will take years to notice.

**Paid customization.** Organization-specific risk scoring weights; state pass-through requirement packs; agency-specific subaward templates.

---

### A7. Burn Rate and Prior-Approval Tripwire

| | |
|---|---|
| **Intended user** | Grants manager and program directors |
| **Complexity** | Medium |
| **AI** | Inappropriate |

**Problem solved.** Budget variance discovered too late to fix, and prior-approval thresholds crossed silently (P6).

**Current workflow.** Monthly export from QuickBooks into the grant spreadsheet, eyeballed.

**Proposed workflow.** Import the GL by award and line item. The tool computes, per award: spend to date by budget category, percentage of period elapsed vs. percentage of budget spent, projected end-of-period position at current run rate, and — the distinguishing feature — **cumulative net transfer between budget categories as a percentage of total budget**, with a warning band approaching 10%. It also flags spending outside the period of performance, unspent balances large enough to warrant a no-cost extension request while there is still time to request one, and category lines projecting to overspend.

**Inputs.** Approved budget by category per award; GL export by class and account; period of performance dates.

**Outputs.** Per-award burn dashboard; prior-approval tripwire alerts with the specific 200.308 citation; projected end-of-award position; a suggested action list ranked by deadline.

**Essential features.** Cumulative category-transfer tracking (the thing nobody tracks); period-of-performance boundary checks; run-rate projection; no-cost-extension lead-time warning.

**Excluded from initial scope.** Being an accounting system. Forecasting future awards. Cash flow for the whole organization.

**AI.** Inappropriate. Arithmetic and thresholds.

**Why not a spreadsheet.** A spreadsheet can compute burn rate. It does not compute *cumulative* category transfer against the original approved budget across a full period of performance, and it does not raise its hand.

**Learning difficulty.** Under an hour.

**Value.** Converts a quarterly surprise into a monthly nudge. The specific catch — a no-cost extension request made in month 9 rather than month 12 — is worth the entire remaining balance of the award.

**Risks and constraints.** Depends on the GL being coded correctly by award, which is not always true; the tool should surface uncoded or mis-coded transactions rather than silently absorbing them.

**Existing substitutes.** QuickBooks budget-vs-actual by class, which does not know what a period of performance or a prior-approval threshold is.

**Why still attractive.** The 10% cumulative transfer rule is invisible in every tool a small nonprofit uses, and it accumulates silently by design.

---

### A8. Federal Financial Report Reconciler

| | |
|---|---|
| **Intended user** | Finance director / bookkeeper |
| **Complexity** | Small to medium |
| **AI** | Inappropriate |

**Problem solved.** SF-425 figures that do not tie to the general ledger or to drawdown history (P9).

**Current workflow.** Pull numbers from QuickBooks, pull drawdowns from the payment portal, type into the form, submit.

**Proposed workflow.** Import the GL by award and the drawdown history. The tool computes each SF-425 line from source data, reconciles cash received against cash disbursed, computes cash on hand and flags it against the allowable window, checks that cumulative expenditures never exceed cumulative drawdowns plus payables, verifies that the indirect section ties to the applied rate and base, and produces a reconciliation worksheet showing every figure's derivation. Findings are stated as questions the reviewer will ask.

**Inputs.** GL export by award; drawdown history export; award terms (rate, base, period).

**Outputs.** Populated SF-425 line values; a reconciliation worksheet with derivations; an exception list; a filed-report archive for audit.

**Essential features.** Line-by-line derivation with drill-down; cash-on-hand check; cumulative-vs-period handling (a classic error source); indirect section tie-out; period-over-period continuity check so this quarter's opening ties to last quarter's closing.

**Excluded from initial scope.** Submitting to PMS or ASAP. Being an accounting system. Agency-specific report variants beyond the standard SF-425 in v1.

**AI.** Inappropriate.

**Why not a spreadsheet.** Cumulative-vs-period continuity across many quarters and awards is exactly where spreadsheets drift, and the drift is invisible until an auditor traces it.

**Learning difficulty.** Under an hour for a bookkeeper.

**Value.** Prevents cash-management findings whose remedy — being placed on reimbursement basis — is severe for a thinly capitalized organization.

**Risks and constraints.** Depends on clean award-level GL coding. Financial data; local-first.

**Existing substitutes.** Agency "helpful hints" PDFs. Nothing computational.

---

### A9. Registration and Prerequisite Watchdog

| | |
|---|---|
| **Intended user** | Executive director, grants manager, or office manager |
| **Complexity** | Small |
| **AI** | Inappropriate |

**Problem solved.** SAM.gov and other registrations expiring silently and freezing drawdowns (P7).

**Current workflow.** Automated emails to an address that may belong to a former employee.

**Proposed workflow.** A single register of every organizational prerequisite — SAM.gov (365 days from submission), UEI, agency portal accounts, state charitable solicitation registrations, audited financial statement due dates, insurance certificates, board conflict-of-interest disclosures, indirect rate agreement expiry. Each carries a required lead time; the tool **back-solves the action date** (e.g. SAM renewal must *begin* 45–60 days before expiry to absorb up to 10 business days of IRS and CAGE validation) and shows a single ranked "start this now" list. It assigns each item to a named person *and* a backup, so departure does not create a silent gap.

**Inputs.** Manually entered registration records with dates and responsible parties.

**Outputs.** A ranked action list; a printable one-page status sheet for the board; ICS export; a post-renewal verification checklist (prompted by the March–July 2026 SAM defect that corrupted NAICS codes, employee counts, and revenue data on renewal).

**Essential features.** Lead-time back-solving; primary and backup owner per item; the 365-days-from-submission rule modeled correctly rather than as an annual calendar date; post-renewal data verification checklist.

**Excluded from initial scope.** Actually performing renewals. Scraping SAM.gov (fragile, and the terms of service are a real constraint). Any integration.

**AI.** Inappropriate.

**Why not a spreadsheet.** Barely — a disciplined spreadsheet could do most of this. The honest differentiators are back-solved action dates rather than expiry dates, mandatory backup owners, and the fact that it is a standing artifact rather than a file someone made once. This is the weakest "why not a spreadsheet" answer in the set and the concept is scored accordingly.

**Learning difficulty.** Fifteen minutes.

**Value.** A lapse freezes drawdowns for two to four weeks. For an organization with a two-month reserve, that is an emergency.

**Existing substitutes.** Federal registration services will renew SAM for a fee. Compliance platforms (Harbor Compliance) handle multi-state registration at enterprise pricing.

**Why still attractive.** Trivial to build, trivial to learn, prevents an operational emergency. Good candidate for the free tier that introduces an organization to the rest of the catalog.

---

### A10. Funder Report Assembler with Bound Metrics

| | |
|---|---|
| **Intended user** | Grants manager / grant writer |
| **Complexity** | Medium |
| **AI** | Optional and useful, but not the core |

**Problem solved.** The same facts reformatted for every funder, at 70% extraction-and-formatting overhead (P2, P10).

**Current workflow.** Copy from prior reports and applications; retype numbers; hope last year's figures got updated.

**Proposed workflow.** Two structures. First, a **metrics table**: canonical facts about the organization and its programs, each with a value, a period, a source, and a last-verified date — clients served, budget total, staff FTE, outcome rates, board size. Second, an **answer library**: reusable narrative blocks keyed to canonical question types, written with **placeholders bound to metrics** rather than hard-coded numbers. When assembling a report or application, the user selects the question type; the tool retrieves candidate blocks, resolves the placeholders against the *current* metrics table, enforces the funder's word or character limit, and flags any metric whose last-verified date is older than a threshold.

**Inputs.** Metrics table (maintained by the user); narrative blocks; the target funder's questions and limits.

**Outputs.** Assembled draft answers with current figures; a stale-metric warning list; a per-funder word/character compliance check.

**Essential features.** Metric binding with staleness dates; word and character limit enforcement per field; block versioning with a note on which application a block came from and whether it was funded; plain-text and portal-friendly output.

**Excluded from initial scope.** Writing the proposal. Program design. Pulling metrics automatically from a case management system (v2 — the integration surface is too fragile for v1). Being a CRM.

**AI.** Optional, and the distinction matters. The **metric binding and limit enforcement are conventional code** and deliver most of the value. AI adds real value for *matching* a new funder's oddly-worded question to the right library block — a semantic retrieval problem conventional keyword search handles poorly — and for compressing a 400-word block into a 250-word limit without losing the substance. It should never generate a number; numbers come only from the bound metrics table.

**Why not a spreadsheet.** A spreadsheet holds the metrics. It cannot resolve placeholders inside narrative prose, enforce per-field character limits, or tell you that the client-served figure in the paragraph you just pasted is fourteen months old.

**Learning difficulty.** Two to three hours to set up the initial library, then minutes per use. This is the highest setup cost in the set and the main adoption risk.

**Value.** Attacks the 70% of reporting effort that is extraction and formatting. Even a one-third reduction on 100 hours/quarter is ~130 hours/year.

**Risks and constraints.** If AI drafts text that goes to a funder under the organization's signature, provenance and review must be explicit. Some funders now ask about AI use in applications; the tool should track which blocks were model-generated. Program data may include client information — the metrics table should hold aggregates only, never records.

**Existing substitutes.** Grantable, Granted AI, Grant Assistant, and Instrumentl's full-lifecycle tier all offer content libraries. **This is the most competitive concept in the set.** The differentiator is narrow and real — bound metrics with staleness tracking, so a stale number is caught rather than propagated — but it is a feature, not a moat, and an incumbent could add it.

**Why still attractive despite that.** The incumbents start at $99/month and run to $999/month, and a free, local, single-purpose tool that does the boring correctness part well has a genuine niche. But it should be built after the higher-ranked concepts.

---

## 5. Opportunity ranking

Each concept scored 1–5 on ten dimensions. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of build | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| A1 | Grants.gov Package Preflight | 4 | 4 | 5 | 5 | 5 | 5 | 4 | 4 | 5 | 5 | **46** |
| A2 | Effort Allocation & Certification | 5 | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 5 | **45** |
| A3 | Cost Allocation & Indirect Recovery | 4 | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 4 | **43** |
| A6 | Subaward Builder & Monitoring | 4 | 3 | 4 | 4 | 5 | 5 | 5 | 4 | 4 | 5 | **43** |
| A4 | Match & Cost-Share Ledger | 5 | 4 | 4 | 4 | 4 | 5 | 5 | 4 | 3 | 4 | **42** |
| A8 | Federal Financial Report Reconciler | 4 | 4 | 4 | 4 | 4 | 5 | 4 | 4 | 3 | 4 | **40** |
| A9 | Registration & Prerequisite Watchdog | 4 | 2 | 4 | 5 | 5 | 5 | 3 | 3 | 4 | 5 | **40** |
| A7 | Burn Rate & Prior-Approval Tripwire | 4 | 5 | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 4 | **40** |
| A5 | Award Terms Obligation Register | 4 | 4 | 4 | 4 | 3 | 3 | 3 | 4 | 4 | 4 | **37** |
| A10 | Funder Report Assembler | 4 | 5 | 4 | 3 | 3 | 3 | 2 | 4 | 3 | 4 | **35** |

### The top three

**A1 — Grants.gov Package Preflight (46).** The highest score comes from an unusual property: the entire specification is published by the counterparty. Grants.gov states the exact filename character set, the exact 50-character limit, and the exact allowed extensions, and documents the errors that result from violating them. There is no interpretation, no judgment, and no ambiguity — which means the tool can be *provably correct*, learnable in one screen, and built in days rather than months. It also runs entirely locally on files the user already has, so there is no privacy story to manage and no integration to break. The failure it prevents is rare per organization but total when it happens: 100+ hours of work and a 12-month funding cycle lost to a filename. Build this one first.

**A2 — Effort Allocation and Certification Workbook (45).** The highest-severity problem in the market. Personnel is 60–80% of the typical federal grant budget, charging by budgeted percentage rather than documented actual effort is the leading source of audit findings, and small nonprofits are explicitly the most exposed population because they lack any formal system. The build is genuinely tractable — CSV import, an allocation grid, a 100%-of-time constraint, a variance report, a PDF certification — and the one architectural feature that matters, an append-only change log with period locking, is straightforward to implement and is precisely what converts the output from "a spreadsheet" into "contemporaneous documentation." Customization potential is the highest in the set, because every organization's payroll export format differs and every agency's certification layout differs. That is exactly the shape of a free base plus paid client-specific work.

**A3 — Cost Allocation and Indirect Recovery Calculator (43).** The only concept in the set that both reduces risk *and* recovers cash, which makes the ROI conversation trivially easy. The de minimis rate rose from 10% to 15% and the MTDC base now includes the first $50,000 of each subaward; any organization that elected de minimis before October 2024 and has not revisited it is under-recovering. That gives the tool a demonstration that pays for itself in the first screen — enter your numbers, see the gap. The exclusion list is long enough that humans get it wrong and short enough that software gets it right.

**Tied with A3 at 43, and worth calling out: A6 — Subaward Builder and Monitoring Register.** It scores lower on frequency because only a subset of organizations pass funds through. But it has the best *differentiation* score in the set, because the 2024 threshold change created a specific, dated, universal problem — pass-through entities that relied on reading subrecipient single audit reports can no longer do so for subrecipients below $1,000,000 — with no established solution and no incumbent moving to fill it.

### What to investigate next

**A1 first**, because it is small, provable, entirely offline, and produces a working artifact fast enough to use as the calling card that gets practitioner conversations started. **A2 second**, because it addresses the largest dollar exposure and the validation conversation with a finance director will be short and decisive. **A3 third**, on the strength of the recovery-gap demonstration.

A5 and A10 — the two AI-dependent concepts — should wait. Both are less differentiated, harder to scope, and carry over-trust risk. They also become substantially easier to build well *after* A1–A3 exist, because those tools produce the structured award data that A5's register and A10's metrics table would otherwise have to invent from nothing.

---

## 6. Validation plan

### Questions to ask practitioners

**On effort reporting (A2):**
- Walk me through how a program manager's salary gets split across grants. Who decided the percentages and when were they last changed?
- What does your effort certification look like — is there a form, who signs it, and how long after the period does it get signed?
- Has an auditor ever asked you to support a payroll charge? What did you hand them?
- If your charged percentage and your actual percentage differ by five points, what happens today?

**On packaging and submission (A1):**
- Have you ever had a federal submission rejected or bounced back? What was the cause?
- How long before the deadline do you finish assembling attachments, and what do you check?
- Who taught you the filename rules, and how?

**On allocation and indirect (A3):**
- What's your indirect rate, and did you re-elect after the de minimis rate went to 15%?
- Show me how you allocated rent last month. Where is the basis written down?
- Which of your funders cap indirect below your rate?

**On match (A4):**
- Which of your awards have a match requirement, and how do you know you're on track?
- How do you value donated space and volunteer time?
- If the same volunteer hour supported two programs, how would you know?

**Open-ended, for all:**
- What did you spend last Friday afternoon doing? (More reliable than asking what is painful.)
- What is the spreadsheet you'd be most afraid to lose?
- What did the last audit ask for that you had to reconstruct?

### Who to interview

- **Grants managers at $2M–$10M direct-service nonprofits** with at least one federal or pass-through award. Reachable through state nonprofit associations (every state has one), the Grant Professionals Association, and the National Grants Management Association.
- **Outsourced nonprofit CFO firms** — YPTC, JFW Accounting, Your Part-Time Controller and regional equivalents. Highest-information counterparty in the market: they see thirty organizations' books and know exactly which failures repeat. Interview two or three of these before interviewing thirty nonprofits.
- **Single audit practitioners at regional CPA firms.** They can rank findings by actual frequency in their practice, which no published source does well.
- **State pass-through agency grants staff** — the New Jersey Treasury Office of Grants Management authored the training deck cited here and is the kind of office that both sees grantee failures at scale and publishes about them.
- **Community action agencies and Head Start grantees**, which sit at the maximum-compliance end and will surface every edge case.

### Search terms for further research

`"questioned costs" nonprofit single audit finding payroll allocation` · `Federal Audit Clearinghouse findings by compliance requirement` · `"effort certification" template nonprofit semi-annual` · `"cost allocation plan" nonprofit sample 2 CFR 200` · `de minimis 15 percent re-election nonprofit indirect` · `subrecipient monitoring below single audit threshold alternative procedures` · `SF-425 unliquidated obligations error` · `NOFO "page limit" "attachment" required format checklist` · state nonprofit association conference agendas 2026 (session titles are a direct readout of what practitioners are worried about)

### Sample files and data needed

- Three or four real NOFOs with their attachment requirements and page limits (public, downloadable from Grants.gov — no access problem)
- A sanitized federal application package folder, to test A1 against real filenames
- A payroll register export from QuickBooks, Gusto, and Paychex — format differences are the main build risk for A2
- A trial balance exported by class from QuickBooks Online, for A3 and A7
- Two or three executed award agreements (federal and foundation), for A5
- A real NICRA and two or three funder agreements with indirect caps
- The Federal Audit Clearinghouse dataset, which is public and contains actual finding text at scale — the single best available source for ranking problems by real frequency rather than by what compliance blogs choose to write about

### Minimum prototypes

**A1:** A command-line script over a folder that reports filename length violations, disallowed characters, disallowed extensions, and PDF page counts. Half a day. Validate by running it against three or four real application packages and seeing whether it finds anything.

**A2:** A single-page web app: paste a payroll register, enter effort percentages, see the variance report and a printable certification. Two to three days. Validate by walking a finance director through her own numbers.

**A3:** A calculator that takes a budget and computes MTDC with correct exclusions, then shows recovery at 10% vs. 15%. One day. Validate by showing three organizations their own gap — the reaction to that number is the whole test.

### Assumptions most likely to make these fail

1. **That the buyer will adopt a separate tool at all.** The strongest competitor is not Instrumentl; it is the existing spreadsheet, which is free, familiar, and infinitely flexible. Anything requiring more than one screen of setup will lose to it.
2. **That accounting data is clean enough to import.** A3, A7, and A8 all assume the GL is coded correctly by award. If coding is unreliable, these tools produce confident wrong answers — which is worse than nothing. Each must surface uncoded and ambiguous transactions rather than absorbing them.
3. **That a free tool is trusted for compliance work.** Grants staff are risk-averse by selection and may not stake an audit position on unsupported software. Mitigations: show the regulation citation next to every rule, version the rule sets with effective dates, and make outputs explainable line by line. A tool that shows its work is trustable; a tool that just outputs a number is not.
4. **For A2 specifically: that staff will enter effort at all.** The tool cannot manufacture documentation that people refuse to create. If the organization will not record actual effort, no software helps. This is the assumption most likely to kill the highest-severity concept, and it should be tested before any code is written.
5. **That the October 2026 rewrite lands as proposed.** The final rule may differ from the May 2026 proposal. Rule sets must be data, not code, and must be versioned with effective dates — which is good architecture regardless.
6. **That reported time-burden figures are real.** The 100-hours-per-quarter and 70%-formatting figures come from vendor-published analyses. They are directionally consistent with everything else observed, but a time study with two or three real organizations should precede any ROI claim made to a customer.

---

## 7. Cross-industry patterns

Patterns from this market that transfer to specific markets already in the backlog:

**Published-rule preflight validator.** A gatekeeper publishes exact mechanical acceptance rules; submitters violate them and discover it only at rejection, after the expensive work is done. A local validator that checks the package before submission is cheap to build and provably correct. → **Building permit expediting and code consulting firms**; **County surveyor and municipal plan-check offices** (build the reviewer's side); **Title 24 acceptance test technicians**; **Small defense suppliers navigating CMMC Level 2**; **Contract manufacturers serving FDA-regulated medical devices**.

**Regulation-enumerated field set as generated instrument.** When a regulation literally lists the required data elements of a document (200.332's fourteen), the correct tool inherits what it can from the parent record, refuses to emit an incomplete instrument, and versions the field list by effective date. → **Small defense suppliers navigating CMMC Level 2** (flow-down clauses); **Supplier quality engineering at OEMs and primes**; **Right-of-way and easement acquisition consulting** (parcel document sets); **Managing general agents and program administrators** (binding authority documentation).

**Allocation with provenance.** A shared cost or shared resource must be split across several obligations, and the *basis* for the split is what gets audited — not the arithmetic. The tool's product is the defensible worksheet, not the number. → **Machine shop / job shop quoting and production control** (burden and overhead allocation); **Freight brokerage and dispatch operations** (settlement allocation); **Mechanical (HVAC) design engineering at small MEP firms** (fee allocation across disciplines); **Third-party claims administration**.

**Cross-obligation double-count sentinel.** The same unit of value — an hour, a dollar, a part, a claim — must not be counted against two obligations, and the check is structurally impossible inside any per-obligation record. The tool's whole reason to exist is that it sees all obligations at once. → **Cargo claims and OS&D handling** (same damage claimed twice); **Premium audit and payroll classification consulting**; **Freight bill audit and payment for small shippers**; **Small motor carriers back office and settlement**.

**Expiry watchdog with back-solved action dates.** Credentials and registrations expire on rolling, per-entity dates with mandatory processing lead times, and the useful output is not the expiry date but the *start-work-now* date, with a named backup owner so staff departure does not create a silent gap. → **Fire protection inspection, testing and maintenance (ITM) contractors under NFPA 25**; **Calibration and metrology service providers**; **Staffing and recruiting agency operations** (credentialing); **Electrical or plumbing trade subcontractor field operations** (licensing).

**Answer library with bound metrics.** Repeated narrative responses across submissions, where the prose is reusable but the embedded numbers go stale. Bind the numbers to a maintained metrics table with staleness dates; enforce per-field length limits. → **General contractor preconstruction and estimating** (prequalification questionnaires); **Staffing and recruiting agency operations** (RFP responses); **Independent insurance agencies — commercial lines** (submission narratives); **Nonprofit grant management** back-office angle.

**Regulatory-transition inventory tool.** When a rule set changes on a known date, every affected organization must re-inventory existing commitments against the new rules. A one-shot tool — inventory in, delta report out — has a sharp demand window and a natural expiry. → **Contract manufacturers serving FDA-regulated medical devices** (QMSR, 2 February 2026); **Building automation and controls contractors** (ASHRAE Guideline 36, 1 January 2026); **Owner-side facilities engineering** (heat-pump replacement mandate).

---

## 8. Sources and confidence

### Verified findings

Regulation text and official agency publications; directly checkable.

- [2 CFR 200.332 — Requirements for pass-through entities](https://www.ecfr.gov/current/title-2/subtitle-A/chapter-II/part-200/subpart-D/subject-group-ECFR031321e29ac5bbd/section-200.332) — the fourteen required subaward data elements; four risk assessment factors; monitoring requirements.
- [2 CFR 200.308 — Revision of budget and program plans](https://www.ecfr.gov/current/title-2/subtitle-A/chapter-II/part-200/subpart-D/subject-group-ECFRea9a4d0b7ba1e8a/section-200.308) — the ten prior-approval categories; the 10% cumulative transfer restriction.
- [Grants.gov — SF-424 attachment and field-level instructions](https://files.simpler.grants.gov/opportunities/1871987d-36c4-4b14-8d6a-2ce6e9570a45/attachments/404db49a-9f12-4180-92fc-b35d032b4e1e/Attachments_form_SF-424_and_SF-424c_Instructions_Updated.pdf) — 50-character filename limit; permitted UTF-8 character set; allowed file types; rejection consequences.
- [Grants.gov — Encountering error messages](https://www.grants.gov/applicants/encountering-error-messages.html) — `VIRUSDETECT`, mandatory forms, blank spaces, schema validation errors.
- [Plante Moran — 2024 Uniform Guidance audit changes are here](https://www.plantemoran.com/explore-our-thinking/insight/2026/02/2024-uniform-guidance-audit-changes-are-here) — $1,000,000 single audit threshold effective FYE 30 September 2025 onward; 15% de minimis; $50,000-per-subaward MTDC inclusion; the subrecipient monitoring gap created by the threshold change.
- [OpenGrants — Federal grant rules for nonprofits: the October 1 rewrite](https://opengrants.io/federal-grant-rules-nonprofits-october-1-rewrite/) — proposed rule published 29 May 2026; comments closed 13 July 2026; target effective date 1 October 2026; SAM.gov subaward reporting above $30,000; E-Verify; termination discretion.
- [National Council of Nonprofits — OMB Uniform Guidance](https://www.councilofnonprofits.org/trends-and-policy-issues/omb-uniform-guidance) — confirms the 15% de minimis and single audit requirements are unchanged in the proposal.
- [National Council of Nonprofits — About the Nonprofit Sector 2025](https://www.councilofnonprofits.org/files/media/documents/2025/ncn-about-the-nonprofit-sector-2025.pdf) — 1.5M organizations; 59% under $50k; 97% under $5M; 32% of revenue from government grants and contracts; 12.8M employees.
- [State of New Jersey Treasury — Managing Multiple Grants Without Chaos (March 2026)](https://www.nj.gov/treasury/grants-management/documents/State%20of%20NJ-Lunch%20and%20Learn-Griffin%20Managing%20Multiple%20Grants%20wo%20Chaos_OCPE_March%2010%202026-FINAL.pdf) — the prescribed spreadsheet tracker fields, color-coding convention, and 30/60/90 rhythm.
- [Indeed — Gulfcoast Legal Services, Grants & Compliance Manager, posted 5 August 2026](https://to.indeed.com/aa79js4wfr8y) — the combined writing/compliance/reporting role; Excel/Word/Adobe as the named tool stack; employment contingent on grant funding.

### Strong inferences

Consistent across multiple independent practitioner and professional-services sources, but not directly verifiable from primary regulation.

- [GrantMetric — Federal grant time and effort reporting](https://grantmetric.com/grant-management/federal-grant-time-effort-reporting) — personnel at 60–80% of federal grant budgets; the four named failure modes; small nonprofits more exposed than large institutions.
- [GRF CPAs — Common findings in single audits](https://www.grfcpa.com/resource/how-nonprofits-can-strengthen-compliance/) — the nine finding categories. Ranking within them is not published here and remains unvalidated.
- [OpenGrants — Grant matching requirements are an audit liability](https://opengrants.io/grant-matching-requirements-audit-liability/) — the seven-part 200.306(b) test in practice; valuation rules; double-counting as a recurring finding.
- [Cherry Bekaert — FFR SF-425 common mistakes](https://www.cbh.com/insights/articles/ffr-sf-425-what-it-is--common-mistakes/) — premature drawdown, co-mingling, indirect over-recovery, undocumented assertions.
- [OpenGrants — SAM.gov registration renewal](https://opengrants.io/sam-gov-registration-renewal-verify-what-it-saved/) — 365-day cycle from submission; no grace period; 10-business-day validation; 2–4 week recovery; the March–July 2026 data corruption defect.
- [Jetpack Workflow — How nonprofits manage grants using QuickBooks](https://jetpackworkflow.com/blog/how-nonprofits-manage-grants-using-quickbooks-and-where-it-falls-short/) and [Actually — Grant management for QuickBooks](https://actuallyfi.com/post/grant-management-for-quickbooks-complete-guide-for-nonprofits) — spreadsheet overlays alongside QuickBooks; shared-cost and payroll allocation as the named breaking points.
- [Instrumentl — Post-award grant management guide](https://www.instrumentl.com/blog/post-award-grant-management) — the five-phase lifecycle; first-30-days tasks; four named pain points.
- [FundRobin — Instrumentl pricing and ROI for small nonprofits (2026)](https://www.fundrobin.com/articles/how-to-guide/ai-tools-for-nonprofits/instrumentl-pricing-roi-small-nonprofits-2026/) — $3,588 / $5,988 / $11,988 annual tiers; the 3–5% technology budget observation; negative ROI below ~$2M revenue. Vendor-adjacent source; price points are checkable, the ROI conclusion is commercially motivated.

### Tentative hypotheses requiring practitioner validation

- **The reporting time-burden figures.** 100+ staff hours per quarter and the 70/30 extraction-to-analysis split come from a single vendor-published analysis ([FundEasy](https://fundeasy.com/blog/why-grant-reporting-is-eating-your-staff-alive)). Directionally consistent with everything else, but no independent time study was located. Do not put these numbers in front of a customer without a own time study.
- **Application effort figures.** 15–20 hours foundation, 100+ hours federal, ~10% success rate ([Instrumentl grant statistics](https://www.instrumentl.com/blog/grant-statistics-and-trends)) — widely repeated, original methodology not traced.
- **The size of the de minimis under-recovery.** That a meaningful number of organizations elected 10% before October 2024 and have not re-elected at 15% is a reasonable inference from the recency of the change and the thinness of small-nonprofit finance capacity — but it is an inference, not a measurement. It is also the single most testable claim in this report: ask five organizations their rate and when they last reviewed it.
- **Willingness to record actual effort.** A2's entire value depends on staff entering effort data. Nothing found addresses whether small nonprofits will sustain that practice. This is the highest-value unknown in the report.
- **The content library competitive picture.** Grantable, Granted AI, and Grant Assistant were identified by search but not trialed. A10's differentiation claim rests on none of them binding narrative placeholders to a maintained metrics table with staleness tracking — plausible, but unverified, and it should be checked before any work on A10 begins.

---

*Report produced 2026-08-06 under claim `3e860bb7`. All dollar thresholds and regulatory citations reflect the Uniform Guidance as amended by the 2024 revisions, with the OMB rule proposed 29 May 2026 noted as pending and targeted for 1 October 2026.*
