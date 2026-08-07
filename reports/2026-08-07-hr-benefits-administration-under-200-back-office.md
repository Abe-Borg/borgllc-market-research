# HR and Benefits Administration in Companies Under 200 Employees — Back Office

**Market research cycle — Borg LLC free/open-source application catalog**

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market** | HR and benefits administration in companies under 200 employees |
| **Angle** | back-office |
| **Claim ID** | `bdf2a32e` |
| **Date** | 2026-08-07 |
| **Report** | `reports/2026-08-07-hr-benefits-administration-under-200-back-office.md` |
| **Backlog remaining after this claim** | 288 assignments |

### Why this assignment over the others available

The ledger held 289 open assignments and zero outstanding claims. Selection followed the stated preference order.

**(a) Markets with zero completed entries.** Nineteen markets have been covered. Roughly 40% of the completed catalog sits in the AEC/construction cluster (fire protection, land surveying, HVAC/MEP, geotechnical labs, construction submittals) and most of the remainder in insurance, real-estate transactions, healthcare billing, trucking, and accounting. "HR and benefits administration in companies under 200 employees" had zero completed entries and, more importantly, is the first assignment in the backlog whose user is **not a professional services firm selling work to clients** — it is an internal corporate function. That is a genuinely different buyer, a different economic logic (cost center, not billable hour), and a different data environment (payroll and carrier systems rather than drawings, specs, and case files). Catalog breadth is currently the binding constraint, and this is the largest single unexplored *category* in the backlog, not merely the largest unexplored market.

**(b) Expected strength of practitioner evidence.** This market is unusually well-documented from primary sources: IRS, DOL, EEOC, OSHA, USCIS/ICE and eCFR publish the actual rules with the actual dollar penalties; vendors publish pricing pages; review sites carry attributed complaints from named reviewers at companies explicitly sized "51–200 employees." That combination — regulator-verified severity plus named-practitioner complaints at exactly the target size — is rarer than it sounds and was decisive.

**(c) Angle diversity.** Completed angles stood at core-practitioner-workflow 7, back-office 4, handoffs-and-qa 4, narrow-subspecialty 4. Back-office was tied for least-covered. It is also the *correct* angle for this market: the "core practitioner workflow" of an HR generalist is recruiting and employee relations, which is judgment-heavy, conversation-shaped, and poorly suited to focused software. The back office — benefits billing, statutory filings, records, leave clocks, offboarding — is where the repeatable, checkable, error-prone work lives.

**What was passed over and why.** *General contractor preconstruction and estimating* and *Structural engineering firms* were the strongest untouched markets by expected evidence quality, but both deepen an already over-represented AEC cluster. *Small CPA tax preparation* was passed over because the accounting sector already has a completed bookkeeping report and tax prep is dominated by mature, cheap, near-universal software (Drake, UltraTax, Lacerte) — a poor fit for the "don't duplicate a mature inexpensive tool" criterion. *Estate planning and probate* remains attractive and is recommended for a near-term cycle.

**One deliberate constraint on this report.** Reddit is blocked at this environment's proxy, which removed r/humanresources — normally the single richest practitioner-complaint source for this market. Compensating sources were used (attributed review-site complaints from 51–200 employee companies, a live HR Generalist job description, named vendor surveys, and regulator primary sources). Where a claim rests only on vendor marketing with no published methodology, it is labeled as such and generally not used to justify an opportunity.

---

## 1. Market examined

**Industry.** Not an industry — a horizontal function. The buyer is the internal HR/People Operations function of a US company with roughly 20 to 200 employees, in any sector: professional services, light manufacturing, healthcare groups, nonprofits, agencies, distribution, veterinary and dental roll-ups, tech companies past seed stage.

**Professional role.** The titles are HR Generalist, HR Manager, People Operations Manager, HR & Benefits Administrator, Director of People and Culture, or — at the small end — the Controller, Office Manager, or founder who inherited HR. A live August 2026 job posting for a remote HR Generalist at a veterinary practice group ($60,000–$80,000) lists as a single person's responsibilities: FMLA/ADA/STD/LTD leave coordination and the ADA interactive process; handbook and policy maintenance; end-to-end onboarding; benefits administration including open enrollment and escalated carrier issues; multi-state employment law application (FMLA, ADA, FLSA, EEO); workers' compensation reporting and return-to-work; unemployment claims including hearing participation; and HRIS data integrity audits and payroll partnership. That is eight distinct compliance domains held by one person at a mid-five-figure salary. It is a fair portrait of the segment.

**Organization size and staffing reality.** SHRM's benchmark HR-to-employee ratio is 1.7 HR staff per 100 employees, with ADP Research Institute putting the workable band at 1.5–4.5 per 100; a size-segmented analysis puts businesses under 250 employees at roughly 3.4 HR staff per 100. Against those benchmarks a 60-person company "should" carry two HR FTE. It carries one, or half of one. The gap between benchmark and reality *is* the market.

The published data on the technology this person has is consistent and unflattering. HR.com's *State of Today's HR Tech Stack and Integrations* (n=275 HR professionals, fielded Nov 2023–Feb 2024) found that **only 41% of small organizations describe their HR tech stack as "moderately developed" or "advanced," versus 80% of large organizations** — 27% of small organizations call theirs undeveloped and 32% "beginning." Forrester research cited in Paycom's 2026 HR priorities report puts the average at **6.17 providers** across the employee lifecycle, with **77% storing employee data across multiple HCM databases** and **80% saying disparate or duplicate employee data hurts their ability to produce accurate workforce reports.**

**Type of user for the tools proposed here.** A competent, non-technical, chronically time-poor generalist who is fluent in Excel, comfortable exporting a CSV from a payroll system, and unwilling to run anything that requires an IT project. Almost certainly on Windows. Frequently the only person in the company who understands what the tool is checking, which means the output must be legible to a skeptical CFO without the HR person present.

**The two structural facts that define the segment.**

1. **Every important obligation threshold falls inside the 20–200 band, and each counts a different population.** Federal COBRA at 20 employees. ADA and the Pregnant Workers Fairness Act at 15. FMLA at 50 (measured as 50+ on payroll for 20 calendar workweeks in the current *or preceding* year — sticky across two years). ACA Applicable Large Employer status at 50 full-time equivalents (a computed number, not a headcount). EEO-1 at 100 employees, or 50 for federal contractors. California pay data reporting at 100 payroll employees with at least one in California. Illinois EPRC at 100 Illinois employees. Form 5500 large-plan/audit status at 100 *participants with account balances* for a 401(k), or 100 *covered employees* for a welfare plan. OSHA electronic submission at 20–249 employees *per establishment* by peak headcount. A company crossing from 45 to 105 employees acquires eight new obligations counted eight different ways, and nothing in its software tells it so.

2. **Multi-state footprint, not headcount, is the burden multiplier.** A 60-person single-state company and a 60-person company distributed across twelve states have wildly different compliance loads: 12 withholding registrations, 12 SUTA accounts, 12 poster sets, up to 16 paid family and medical leave jurisdictions with separate rates and quarterly filings, 21+ paid-sick-leave states with five different accrual denominators, and 15+ state-mandated retirement programs with five new deadlines in 2026 alone. One vendor estimate puts DIY setup at 10–20 hours per state. Remote work made this the default rather than the exception for the segment.

---

## 2. How the work is performed

### 2.1 The monthly cycle

**People involved.** The HR person; the payroll processor (often the same person, sometimes the Controller); the benefits broker's account manager; carrier billing departments; a COBRA TPA if one exists; the 401(k) recordkeeper; and the CFO or owner who signs things.

**The benefits invoice.** Between the 1st and the 10th, invoices arrive from each carrier. For this segment the modal arrangement is a **list bill** — the carrier generates a per-subscriber invoice and the employer's job is to audit it, not to build it. Certifi's guidance is that the self-administered-billing candidate is "typically 100 or more lives," and that "for groups of 50 to 100 lives, list billing is typically simpler for both parties." This inverts a common assumption: the small employer's problem is not calculating premium, it is **catching the carrier's errors and chasing credits.**

The audit itself is a three-system, employee-level comparison. Selerix specifies the fields: from payroll, "payroll deduction reports, cost-per-pay amounts, deduction codes"; from the benefits administration system or HRIS, "active enrollments, coverage tiers, effective dates, eligibility status"; from the carrier, "carrier invoices, self-billed records, enrollment feeds." A broker's published five-step procedure directs the employer to use the enrollment census as source of truth, to "start with recent new hires, terminations, and qualifying life events, since they're the most common sources of discrepancies," to log each discrepancy with "what was found, who was contacted, and expected resolution timelines," and then to verify resolution **on the subsequent invoice**.

That last step is the load-bearing one and the first casualty of a one-person HR shop: a credit requested in month 1 appears in month 3, so verification requires holding an open item across two billing cycles in a spreadsheet that gets overwritten each month.

**Payroll.** Deductions are configured per employee per plan. If payroll is semi-monthly (24 periods), two deductions map cleanly to one monthly premium. If biweekly (26 periods), they do not, and the employer must configure a "deductions holiday" — flat-dollar benefit deductions taken only from the first two paychecks of each month, skipped on the third pay date in the two months per year that have one. UC Davis documents the rule precisely: flat-dollar deductions 24 times, percentage-based deductions 26 times, with health, life, FSA, parking/transit, loans and credit union skipped on the holiday check and taxes, retirement and garnishments never skipped. **2026 is a 27-biweekly-period year** — an event that "occurs roughly every 11 or 12 years." Worked example from a benefits consultancy: a $5,000 dependent care FSA election divided by 26 is $192.31; run 27 times without adjustment the employee contributes ~$5,192 and blows the $5,000 IRS limit.

### 2.2 The event-driven work

**New hire.** Three unforgiving clocks start on day one and none of them is visible in a standard HRIS dashboard: Form I-9 Section 2 within **3 business days** of hire (8 CFR 274a.2(b)(1)(ii)(B)); the E-Verify case within **3 business days** if the employer is enrolled; and the state new-hire report within **20 days** (42 U.S.C. §653a(b)(2)). Then benefits eligibility, enrollment windows, plan-entry dates, 401(k) eligibility and auto-enrollment, and a state retirement mandate if the company is in one of 15+ states running one.

**Enrollment change.** A new hire, termination, birth, marriage, divorce, or dependent age-out must be propagated to payroll and to every carrier. Whether this is automatic depends entirely on whether the group qualifies for an EDI 834 feed — see §3, Problem 1. For most of this segment it does not, and the change is keyed by hand into three to six carrier portals plus payroll.

**Termination.** Coverage termination requested at each carrier (against a retroactive window that is typically 60 days and as short as 30); final pay computed against a state-specific deadline that in California, Colorado, Montana and Massachusetts is effectively immediate; a state separation notice in the dozen-plus states that require a specific form; a COBRA election notice within **44 days** where the employer is also the plan administrator; 401(k) loan and distribution handling; and, days or weeks later, an unemployment claim notice with a response window that is typically 10 days.

**Leave.** The FMLA notice cascade under 29 CFR 825.300: eligibility and rights-and-responsibilities notice (WH-381) within **5 business days** of the employer *acquiring knowledge* that leave may be FMLA-qualifying, medical certification requested within 5 business days and due back in 15 calendar days with a 7-day cure period for deficiencies, and the designation notice (WH-382) within another **5 business days**. Critically, 29 CFR 825.302(c) provides that an employee "need not expressly assert rights under the FMLA or even mention the FMLA" — so the 5-day clock can start from a text message to a supervisor that never reaches HR.

Running concurrently: state PFML in up to 16 jurisdictions, each with its own clock, minimum increment, qualifying reasons and quarterly premium filings; employer short-term disability with benefit-offset provisions that can zero out; state paid sick leave with five different accrual denominators; and ADA/PWFA accommodation obligations that bind at 15 employees with no statutory cap and no FMLA scaffolding.

### 2.3 The annual cycle

Open enrollment in the fall: elections collected, then rekeyed into payroll and every carrier portal. ACA reporting: 1095-Cs furnished (or the alternative-manner notice posted) by **March 2, 2026** and e-filed via the IRS AIR system by **March 31, 2026**. OSHA Form 300A posted February 1 through April 30 and, if in scope, electronically submitted by **March 2**. EEO-1 in the spring, if it happens at all this year. California pay data by the **second Wednesday of May**. VETS-4212 between **August 1 and September 30** for federal contractors over $200,000. Form 5500 by **July 31** or October 15 on extension. 401(k) census to the recordkeeper for nondiscrimination testing. Workers' compensation premium audit. Handbook update for the new year's state law changes.

### 2.4 Software currently in use

Payroll and HRIS at this size means Gusto, Rippling, BambooHR, ADP RUN or Workforce Now, Paylocity, Paycor, isolved or Namely; or the whole employment relationship is handed to a PEO (TriNet, Justworks, Insperity). Benefits administration is usually **Employee Navigator or Ease, licensed by the benefits broker and provided to the employer at no direct charge** — a distribution model that matters enormously (see §3, Problem 7). Leave, accommodations, compensation planning, org charts, ACA measurement periods and benefits reconciliation are, per the survey data below, largely done in Excel.

Two facts about this stack constrain every tool proposed in this report:

- **Gusto — the largest platform in the segment, claiming "more than 500,000 growing businesses" — does not offer a customer-facing API.** Its own help center: "We currently do not support API access for Gusto customers who want to connect their own company systems directly to their Gusto account." **Paycom offers no API to customers or third-party developers at all.** Paylocity's API requires a Web Services Access Request Form and account-executive-quoted PEPM pricing. BambooHR is the outlier, offering self-serve API keys.
- Therefore **any tool built for this market must consume CSV/XLSX exports and PDFs, not live integrations.** This is not a limitation to apologize for; it is the correct architecture, and it is also why the incumbents' integration-dependent products cost what they cost.

---

## 3. Most important problems, ranked

Ranked by (severity × frequency × tractability by focused software), with evidence quality stated for each.

---

### Problem 1 — Small groups are structurally excluded from carrier EDI feeds, so every enrollment change is keyed by hand into 3–6 systems

**Who experiences it.** Every HR person at a company below roughly 100 subscribed employees who offers more than one benefit line.

**When it occurs.** Every new hire, termination, and qualifying life event — continuously.

**How it is currently handled.** Manual entry into each carrier's employer portal, plus payroll, plus the ben-admin system.

**Why that is inadequate.** Carriers set minimum group sizes before they will build an 834 EDI feed, and the minimums sit above most of this segment. A carrier-by-carrier minimum table (vendor-hosted, dated 2018 — see caveat below) shows Aetna, UnitedHealthcare, Humana, Highmark, Medical Mutual of Ohio, Empire BCBS NY and several Blues plans at **100 subscribed employees**; BCBS Massachusetts at 150; Horizon BCBS New Jersey at 150–200; **VSP at 300; The Standard at 250; Dearborn National at 350; Cigna at 500 for Life/AD&D/STD/LTD** (though no minimum for medical). Ancillary carriers are frequently *stricter* than medical.

Corroboration from a current, non-dated source: **Employee Navigator**, the dominant small-group benefits administration platform, advises that an 834 feed "should be considered if the group size is 100+ or if the group has significant turnover," and steers everyone else to XML integrations. **Namely** states that "some carriers will not build a feed for a small group" and that builds "can take up to 12 weeks." **Netchex** puts setup at "90–120 days" and states the decisive fact plainly: "Ultimately the carriers decide if they will accept electronic data feeds from their clients or not, and under what conditions." There is no true standard format — each carrier issues its own companion guide.

Even where a feed exists it is metered: Employee Navigator charges **$0.45 per enrolled employee per month for 834 EDI feeds** on its middle tiers, free only at its top tier. Ease's payroll integration module runs "$0 to $1.50 PEPM."

**Frequency.** Continuous. At 22% annual turnover — the figure used in a benefits vendor's own worked example — a 100-person company processes ~22 terminations and ~22 hires a year plus life events, each requiring the same data in 4–7 places.

**Likely cost.** Compounding transcription error. The accepted ceiling for acceptable manual data entry is around 1% per field, tracing to Panko's human-error research. An enrollment record carries roughly 8–12 discrete fields (plan, tier, dependent names, dependent dates of birth and SSNs, coverage volumes, beneficiary). Transcribed 4–7 times, the probability that a given employee's record is identical across all systems falls sharply. *This is a modeled figure, not a measured one, and should be presented that way.*

**Evidence quality.** Strong. The Employee Navigator, Namely and Netchex statements are current vendor primary sources. The 2018 carrier minimum table is directionally corroborated but should be spot-verified before being republished as a table.

---

### Problem 2 — The termination-to-carrier gap costs real money on a 60-day fuse, and the legal rule contradicts the billing practice

**Who experiences it.** Every employer that terminates an employee enrolled in coverage.

**When it occurs.** At every termination; discovered at the next monthly invoice audit, or not at all.

**How it is currently handled.** HR requests a retroactive termination from the carrier when it notices the person is still on the bill.

**Why that is inadequate.** Carriers cap retroactivity. **Harvard Pilgrim's published administrative guide** — the best primary evidence located on this point — allows retroactive termination "60 days retroactive beginning on the date the notice was received" in MA, RI and ME, and **30 days in New Hampshire**, with status changes to be notified within 60 days of the qualifying event. Cape Cod Municipal Health Group's published policy is likewise 60 days, and notes that credits are **net**: "fees and payments withheld by the health plan, healthcare provider, and/or reinsurance premiums will be subtracted from the amount owed." Practitioner guidance describes the window as "generally limited to two to three months." **A termination caught more than two billing cycles late is generally unrecoverable.**

There is a genuine tension worth naming. **45 CFR 147.128** prohibits rescission — retroactive cancellation of coverage — absent fraud or intentional misrepresentation, and requires 30 days' advance written notice; the carve-out is retroactive termination "attributable to a failure to timely pay required premiums." Benefits counsel accordingly advise that the correct remediation is to terminate **prospectively**, issue a COBRA election notice, and eat the premium. Employers overwhelmingly do the other thing and are rarely challenged — because the affected person is a former employee with no claims. **The exposure crystallizes only when the ex-employee incurred claims during the phantom-coverage window.**

**Frequency.** Every termination. At 22% turnover, ~22 events/year at 100 employees.

**Likely cost.** A vendor estimate puts it at "$400–$1,600 per terminated employee remaining on carrier invoices for 1–4 billing cycles," which is arithmetically credible: KFF's 2025 Employer Health Benefits Survey puts the average family premium at firms with 10–199 workers at **$26,054/year**, i.e. ~$2,170/month, of which the employer share is roughly two-thirds. The same vendor estimates **$5,000–$15,000 in annually recoverable overpayments for a 100-employee group with ~$500K of benefits spend** (1–3%). A widely repeated "5% of premium spend is inaccurate" figure appears in at least two independent vendor sources with **no published methodology anywhere** and should not be presented as measured.

**Evidence quality.** Very strong on mechanics (carrier administrative guide, eCFR). Weak on aggregate dollar impact — every dollar figure in this space is vendor-published without methodology.

---

### Problem 3 — Deductions are taken for coverage that was never actually put in force, and nobody finds out until a claim

**Who experiences it.** The employee or their surviving family; the employer, as an ERISA fiduciary.

**When it occurs.** Silently at enrollment; discovered at a death claim, sometimes years later.

**How it is currently handled.** It is not tracked. Pending evidence-of-insurability (EOI) status lives in a carrier portal or an email thread; eligibility-ending life events (divorce, dependent age-out) arrive verbally and must be propagated by memory.

**Why that is inadequate.** Two federal appellate decisions establish direct employer liability.

- ***Gimeno v. NCHMD, Inc.***, 11th Cir. 2022. The employer failed to submit the required EOI form for supplemental life coverage, "deducted premiums for the supplemental coverage for **three years** and provided a benefits summary stating that the supplemental coverage was in effect." The employee died; the insurer denied because it never received EOI. **$350,000** of coverage at stake. The Eleventh Circuit held ERISA permits **equitable surcharge** — money damages equal to the lost benefit — against the *employer*, and reinstated the widow's suit.
- ***McIver v. Metropolitan Life Insurance Co.***, 9th Cir., Sept. 11, 2024. The employer continued deducting dependent life premiums for **11 months after** being notified of a divorce that had automatically terminated the ex-spouse's eligibility. She died; the claim was denied. The Ninth Circuit reversed dismissal, holding fiduciaries breach their duties by "failing to investigate… ongoing eligibility" and by continuing to collect premiums for ineligible participants.

DOL has an active enforcement focus on exactly this pattern — "premiums are deducted but EOIs are not submitted to the insurer" — and has settled with insurers over collecting premiums "for months or years, and then deny[ing] payment of death benefits."

**Frequency.** Rare per event, universal in exposure. Any employer offering voluntary/supplemental life with EOI requirements has this risk open right now and cannot easily tell.

**Likely cost.** Full face value of the denied benefit plus attorney's fees. $350,000 in *Gimeno*.

**Evidence quality.** Excellent — decided appellate cases plus documented DOL enforcement posture. This is the best-evidenced high-severity finding in the report.

---

### Problem 4 — ACA 1094-C/1095-C coding is done by a vendor module the employer cannot audit, and the information-return penalty attaches to coding errors regardless of coverage

**Who experiences it.** Every Applicable Large Employer in the 50–199 FTE range — a population that includes companies that do not know they are ALEs.

**When it occurs.** January–March each year, with the underlying data errors accumulating all year.

**How it is currently handled.** A payroll or ben-admin module generates the forms; the HR person spot-checks a few and files.

**Why that is inadequate.** Three compounding problems.

*First, ALE status is invisible.* IRS's own rule: aggregate the hours of all non-full-time employees for the month, capped at 120 per employee, and divide by 120. A company with 35 full-timers and 30 part-timers averaging 60 hours/month is a 50-FTE ALE. Nothing in a standard small-business HRIS surfaces this, and the look-back measurement method **may not** be used for the ALE determination.

*Second, the code logic is genuinely hard.* A specialist ACA filing firm reviewing "Forms 1094-C and 1095-C submissions across hundreds of employers" catalogs four recurring vendor-module failure modes: full-time misclassification from incorrect look-back measurement periods, including "measurement periods that start on legally impermissible dates"; Form 1094-C Part III boxes checked "No" or left blank when the 95% threshold *was* met; blank Line 16 safe-harbor codes; and W-2 safe-harbor miscalculation where inaccurate Line 15 data "throws off the entire calculation for the IRS." An independent benefits-compliance source publishes the same error taxonomy. A separate list of the six most common employer mistakes adds 1A-vs-1E confusion, partial-month offers coded as if full-month, COBRA for terminated employees coded 2C instead of 2A, and **level-funded plans mistakenly treated as fully insured** (they are self-insured and require Part III covered-individual reporting) — the last of which matters because **37% of covered workers at 10–199-worker firms are in level-funded plans**, per KFF 2025.

*Third, the penalty attaches to the coding, not the coverage.* §6721 and §6722 information-return penalties for returns filed in 2026 are **$340 per return**, and they stack: furnish + file. A 120-employee ALE that gets every 1095-C wrong is exposed to roughly **120 × $340 × 2 ≈ $81,600** with no coverage failure at all. Meanwhile §4980H(a) for 2026 is **$3,340 per full-time employee minus 30** — for a 100-FTE ALE, **$233,800** for a single year's failure to offer to 95% of full-timers. The specialist filer's own estimate: "A 200-person employer who falls below the 95 percent threshold for a single month can easily reach $200,000 or more."

Two 2026-specific traps: the affordability percentage jumped from **9.02% (2025) to 9.96% (2026)**, a 94-basis-point loosening many employers will not have adjusted for; and the e-filing threshold aggregation rule (T.D. 9972) counts W-2s, 1099s and 1095-Cs together against a **10-return** threshold, which means paper ACA filing is effectively dead for this entire segment and every employer must go through a vendor or filing agent.

**Frequency.** Annual, but the data errors are continuous.

**Likely cost.** $81,600 in information-return penalties for a 120-person ALE; $233,800 in 4980H(a) for a 100-FTE ALE; the IRS's own PRA burden estimate is 4 hours per 1094-C plus 12 minutes per 1095-C — **28 hours/year for a 120-employee ALE by IRS's own reckoning**, which practitioners consider a substantial understatement of the data-assembly work.

**Evidence quality.** Excellent on rules and penalties (IRS primary sources, Revenue Procedures, eCFR). Good on error taxonomy (two independent specialist sources agreeing). One attributed reviewer at a 51–200 employee company described their HRIS's ACA reporting process as **"a nightmare"** requiring manual workarounds.

---

### Problem 5 — I-9 clerical omissions became immediately fineable in March 2026, retroactively, with no cure period

**Who experiences it.** Every US employer. Acutely: anyone in hospitality, construction, staffing, transportation, healthcare, retail, landscaping.

**When it occurs.** At every hire; discovered when ICE serves a Notice of Inspection with a **3-business-day** response window.

**How it is currently handled.** A folder of paper or PDF I-9s, completed by whoever onboarded the person, never audited.

**Why that is inadequate.** On **March 16, 2026**, ICE updated its Form I-9 Inspection fact sheet — per Morgan Lewis, with "no Federal Register notice, no proposed rulemaking, and no public announcement" — reclassifying more than ten categories of error from *technical* (curable within a 10-business-day window) to *substantive* (immediately fineable). The newly substantive list is almost a catalog of what a busy manager skips:

- omission of the employee's date of birth, immigration/USCIS numbers, or Section 1 signature date
- **the employer's failure to list the authorized representative's title in Section 2**
- **failure to list the employee's first date of employment in Section 2**
- failure to fully or correctly record List A/B/C documentation
- use of the Spanish-language I-9 outside Puerto Rico
- failure to examine and verify documents within three business days of hire
- failure to reverify by the authorization expiration date
- deficiencies in electronic I-9 systems or in the remote verification procedure
- retaining document copies no longer cures missing Section 2 data

Current civil penalties per 8 CFR 274a.10 (as adjusted January 2, 2025): **$288–$2,861 per individual** for verification-requirement failures; **$716–$5,724 per unauthorized alien** for a first knowing-hire offense. Morgan Lewis quantifies the shift directly: "An employer with 200 Forms I-9 containing errors previously flagged as technical … could now face paperwork penalties of approximately **$57,600 to $572,200**."

The enforcement environment matches. Greenspoon Marder reports that "ICE's rate of Notices of Inspection in the first half of 2025 was at least **ten times higher** than in 2024," across hospitality, construction, staffing, transportation, health care, retail, landscaping, car washes and bakeries, and notes a **$6.18 million** I-9/knowing-employment fine against a Denver company in 2025. Fines are computed from a violation percentage (substantive violations ÷ total I-9s) across six bands, then adjusted ±25% for business size, good faith, seriousness, presence of unauthorized workers and history.

A separate, quieter trap: the 08/01/23 Form I-9 edition bearing a **07/31/2026** expiration became unusable on August 1, 2026 — five days before this report. Employers who downloaded a PDF in 2023 and never re-downloaded are completing an invalid form today, and "failure to prepare or present the Form I-9" is substantive.

**Frequency.** Every hire. Every reverification. And the reclassification applies to the **entire existing file**, not just new forms.

**Likely cost.** Directly computable: (substantive errors) × ($288 to $2,861), adjusted. For a 150-employee company with historic turnover, a file of 400 I-9s at even a 30% substantive error rate is 120 violations — six figures.

**Evidence quality.** Excellent. eCFR for the penalties; three independent law-firm alerts (Morgan Lewis, Sheppard Mullin, National Law Review) documenting the March 2026 reclassification; ICE's own fact sheet for the inspection process. *Caveat: the widely circulated "76% of I-9s contain at least one error" statistic has no locatable primary source and is not used here.*

---

### Problem 6 — Leave clocks start where HR cannot see them, and the rolling-window math is not maintainable by hand

**Who experiences it.** Any employer at or above 50 employees (FMLA), and any employer at all in one of 16 PFML jurisdictions or 21+ paid-sick-leave states.

**When it occurs.** Whenever an employee tells *anyone* they need time off for a health reason.

**How it is currently handled.** Spreadsheets and email. The AbsenceSoft *2026 State of Leave and Accommodations Report* (n=1,200 HR/People Ops leaders, **500+ employee organizations**) found **41% manage state leave laws manually using spreadsheets, email and reminders** and **43% manage accommodations manually via spreadsheets and email**; 8% "report they are struggling without a solution." If 41–43% of *enterprise* teams are on spreadsheets, the rate below 200 employees is almost certainly far higher — though no published data measures it.

**Why that is inadequate.** Four separate reasons, each independently sufficient:

1. **Detection.** 29 CFR 825.300(b)(1) starts a 5-business-day eligibility-notice clock when the employer "acquires knowledge that an employee's leave may be for an FMLA-qualifying reason," and 825.302(c) says the employee "need not expressly assert rights under the FMLA or even mention the FMLA." The clock can start with a text to a shift lead.
2. **The rolling window.** 29 CFR 825.200(b) permits four leave-year methods; practitioner consensus is that only the **rolling 12-month period measured backward** prevents stacking (12 weeks at the end of one year plus 12 at the start of the next = 24 consecutive weeks). That method requires recomputing, on every leave day, the sum of all FMLA hours used in the trailing 365 days from that date. Trivial in a database; not maintainable by hand once intermittent leave is involved. And 825.200(e) punishes indecision: if the employer never selected a method, "the option that provides the most beneficial outcome for the employee will be used."
3. **Increment granularity.** 29 CFR 825.205(a)(1) requires accounting in an increment "no greater than the shortest period of time that the employer uses to account for use of other forms of leave" — for many payroll systems, minutes. And DOL Opinion Letter **FMLA2025-02-A (Sept. 30, 2025)** confirmed that entitlement is based on the employee's *actual* regularly scheduled workweek including mandatory overtime, not a default 40-hour conversion: an employee with 84 regularly scheduled hours per two weeks is entitled to **504 hours**, not 480.
4. **Concurrency.** State PFML runs alongside, with different clocks and different consequences for documentation failure. **Washington HB 1213**, effective January 1, 2026, is the sharpest example: an employer may count FMLA-only leave against PFML job-protection maximums **only if** it gives timely written notice on request of FMLA leave *and monthly thereafter*; if it fails, "PFML will protect the employee's job for the entire FMLA and PFML leave periods" — the leaves stack. That converts a documentation failure directly into a doubled job-protection obligation, a far harsher standard than FMLA's prejudice-based rule.

**Frequency.** DOL's 2018 FMLA surveys — the most recent federal data — put the incidence at **15% of US employees taking a qualifying leave in the prior 12 months**, with a mean length of 28 business days and **31% of leave-takers taking leave on multiple occasions for the same reason**. That is ~15 leave events per year at a 100-person company, of which some meaningful fraction are intermittent.

**Likely cost.** Be precise about this, because the vendor literature is not. **DOL administrative enforcement of FMLA is nearly negligible**: FY2025 saw 301 compliance actions with violations, 342 employees, and **$1,029,463** in total back wages nationally. The real exposure is private litigation — FMLA provides liquidated damages and attorney's fees — and the *Kemp v. Regeneron* (2d Cir., Sept. 9, 2024) discouragement theory, which holds that an employer can violate the FMLA by discouraging leave **even where leave is ultimately granted**. The correct pitch to a small employer is not "DOL will fine you." It is "your former employee's lawyer will subpoena your leave file, and you don't have one."

There is also a real safe harbor worth building toward: *Ragsdale v. Wolverine World Wide* (535 U.S. 81, 2002) and the post-*Ragsdale* 29 CFR 825.301(d) permit an employer to **retroactively designate** leave as FMLA where the failure caused no prejudice. A tool that surfaces "you have an undesignated qualifying absence from three weeks ago" retains defensive value long after the 5-day window has closed.

**Evidence quality.** Excellent on rules (eCFR, DOL opinion letters, Supreme Court and circuit decisions). Good on prevalence (DOL 2018 survey; AbsenceSoft 2026 for the tooling split, with the 500+ employee sample caveat stated). **No credible published benchmark exists for hours or dollars per leave case** — the entire "cost of manual leave administration" genre is vendor-produced with undisclosed methodology.

---

### Problem 7 — The benefits system belongs to the broker, the payroll system has no API, and custom reporting is an upsell — so everything ends up in Excel

**Who experiences it.** Everyone in the segment.

**When it occurs.** Every time a question requires joining data across two systems.

**How it is currently handled.** CSV export, VLOOKUP, pivot table.

**Why that is inadequate.** Three structural facts.

*Reporting is deliberately monetized.* Gusto gates custom reports behind its Premium tier at **$180/month + $22 PEPM** — roughly 3.7× the entry PEPM. BambooHR gates advanced analytics and compensation planning behind Elite at **$25 PEPM**, and prices Payroll, Benefits Administration and Time & Attendance as separate add-ons on top of any tier, with a **$250/month floor for organizations of 25 or fewer**. The complaint that follows is remarkably consistent and specific across every vendor and always names the same shape of failure — **cross-tabulation**:

> "The reporting engine can feel a bit rigid when you need hyper-specific, cross-tabular data." — BambooHR reviewer
> "advanced reporting is quite limited, making it difficult to generate deep, cross-tabulated insights." — BambooHR reviewer
> "System set up in 3 silos and does not communicate with the other modules well." — Paylocity, Chief Administrative Officer
> "The payroll system does NOT talk directly to accounting system." — Namely, Administrator, 201–500 employees
> "Paycom doesn't have an open API… it doesn't integrate directly with our other systems" — Paycom, Partner/HR, with the reviewer stating manual Excel workflows are the consequence

*The data is often not extractable at all.* Gusto and Paycom have no customer-facing API (§2.4). Paylocity's is gated and priced by an account executive with no published rate limits.

*The benefits system is not the employer's.* Ease states its model on its own pricing page: subscriptions are "for insurance brokers to use for their clients." Employee Navigator's pricing page is headed "Plans designed for brokers of all sizes." **Employee Navigator acquired Ease on April 4, 2023**, and now claims **195,000+ employers, 7,000+ brokers, 600+ partners** — effectively a monopoly in SMB broker-distributed benefits administration. The employer's enrollment history, dependent data and plan configuration live in a system the employer does not contract for, and switching brokers plausibly means re-implementing benefits administration. *(This last consequence follows from the licensing structure; no source states it explicitly, and it should be confirmed in practitioner interviews.)*

**Frequency.** Continuous.

**Likely cost.** Not directly quantifiable, but it explains everything else in this section. **HR still runs on spreadsheets not from backwardness but as a rational substitute for a deliberately upsold feature.** Corroborating datapoints: SHRM — the profession's own body — publishes downloadable **Excel FMLA absence-tracking spreadsheets** as standard tools; an OrgChart survey of 400+ US HR leaders (June 2025) found **43% manually create org charts in PowerPoint or Visio** and **50% spend 5+ hours a month** maintaining them; Aeqium's interview study of 60 organizations found **58% rely on spreadsheets for compensation planning**.

**Evidence quality.** Very strong. Vendor pricing pages are primary; reviewer complaints are attributed with company-size bands; the Employee Navigator/Ease consolidation is documented in the acquirer's own press release.

---

### Problem 8 — Records requests and unemployment claims arrive with short clocks and per-instance penalties

**Who experiences it.** Any employer; acutely in California.

**Why it is inadequate today.** California runs **two different clocks with two different triggers and the same $750 penalty**: Labor Code §1198.5 requires personnel records be made available "not later than **30 calendar days**" from a written request, and Labor Code §226 requires payroll records "no later than **21 calendar days**." An employee who emails asking for "my file and my pay stubs" starts both simultaneously. §1198.5 also requires retaining personnel records for **not less than three years after termination**.

Unemployment claims carry a harder edge than most HR people realize. The **Unemployment Insurance Integrity Act** (P.L. 112-40, §§251–252) required every state by October 21, 2013 to bar relief of charges where an employer "established a pattern of failing to respond timely or adequately" — meaning **the employer's account is charged even if the claimant is subsequently found ineligible.** "Pattern" is defined at the state level and varies enormously: Alabama at two or more offenses with no timeframe; Kansas at the greater of two offenses or 2% of claims; **Hawaii approaching almost strict liability with a single offense.** California's response window is **10 days** from the notice date, and failure to respond means the employer "cannot appeal the EDD's decision." Littler notes the structural squeeze: post-2011 state laws demand *more* information without extending the sub-10-day response window.

The free fix — **SIDES E-Response**, a NASWA/DOL system requiring no IT integration and providing date-stamped confirmation of receipt — is explicitly designed for low-volume employers (full SIDES targets those with "more than 30 UI information requests per week," a threshold no 200-person company reaches). *No published data measures adoption by employer size, but nothing pushes a small employer toward registering; the default is a mailed paper notice.*

**Evidence quality.** Excellent on rules (DIR, EDD, Littler, NASWA, statute). No data on prevalence of failure.

---

### Problems noted but not carried into opportunities

- **COBRA notice content.** *Marrow v. E.R. Carpenter Co.* (M.D. Fla.) alleges over $700,000 exposure for a single family based on four purely *drafting* defects — expressing the election deadline as a day-count rather than a specific date, misstating the deadline's start, inconsistent payment timing, and directing recipients to call for the premium amount rather than stating it. All four would be invisible to an employer using a generic template. **This is a strong argument for outsourcing COBRA notices rather than building a tool** — the risk is in notice content, which small employers cannot self-audit. Jackson Lewis notes no COBRA-notice case has yet succeeded on the merits; the exposure is settlement pressure.
- **Welfare-plan Form 5500 non-filing.** Likely the highest-frequency undetected failure in the segment: the wrap-plan aggregation rule means employer-paid basic life covering all 130 employees pulls the entire plan over 100 participants even when medical enrollment is below it, and there is no carrier or payroll vendor whose workflow surfaces this. DOL exposure is **$2,739/day with no cap**; DFVCP self-correction for a small plan caps at **$750 per filing / $1,500 per plan** — a ~3,600× difference. This is folded into Opportunity 9 as its most valuable single test rather than being a standalone product.

---

## 4. Application opportunities

Nine concepts. All assume **file-in, file-out** architecture (CSV/XLSX/PDF), local execution, no live integrations, no cloud storage of employee data by default — which is both the correct privacy posture for this data and a direct consequence of the API reality documented in §2.4.

---

### C1 — I9Audit: Form I-9 self-audit and substantive-error scanner

**Intended user.** HR generalist or office manager at any employer; also the fractional-HR consultant doing a client intake.

**Problem solved.** Problem 5. The March 2026 ICE reclassification converted the most common clerical omissions into immediately fineable substantive violations with no cure window, and the reclassification applies to the file the employer already has.

**Current workflow.** A binder or a folder of PDFs, never reviewed. Discovery happens when ICE serves a Notice of Inspection with a 3-business-day response window.

**Proposed workflow.** Point the tool at a folder of I-9 PDFs, or paste in a structured export from an electronic I-9 system, or type the fields for a single form. Get a per-form findings list, each finding labeled **substantive (fineable now)** / **technical (curable)** / **advisory**, with the specific defect, the correction procedure, and a rough exposure figure at the current $288–$2,861 range. Plus a file-level summary: total forms, substantive violation count, resulting violation percentage, and which of ICE's six penalty bands that lands in.

**Required inputs.** Completed I-9s (PDF, image, or structured export), plus a roster with hire dates and termination dates to evaluate the 3-business-day timing rule and the retention rule.

**Expected outputs.** (1) A findings register, per form, per defect. (2) A remediation worklist ordered by severity. (3) A retention report: which I-9s may now be purged (3 years after hire or 1 year after termination, whichever is later) and — importantly — which may **not**, because purging a form that should have been retained is itself a violation. (4) A one-page summary for the CFO.

**Essential features.** The current substantive/technical classification as of March 2026, encoded as a versioned, citable ruleset. Form-edition validity checking (the 08/01/23 edition with a 07/31/2026 expiration went dead August 1, 2026). Section 2 completeness including the two fields most often skipped — **authorized representative title** and **employee first date of employment**. Section 1 signature and date. Reverification date tracking against the Section 1 authorization expiration date, with the correct rules that reverification is *never* required for US citizens, expired permanent-resident cards, expired US passports, or expired List B identity documents. Spanish-form-outside-Puerto-Rico detection. Timing checks against hire date.

**Deliberately excluded from initial scope.** Actually completing or storing I-9s (that is a different product and a regulated one). E-Verify case creation. Document authenticity assessment — the tool checks whether the *form* is correctly completed, never whether the *documents* were genuine. Legal advice on how to handle a discovered unauthorized worker.

**AI: optional, and only for one job.** Extracting fields from scanned or handwritten paper I-9s. The rules engine itself must be deterministic and citable — an AI that "thinks" a form is fine is worthless against a fine schedule. A defensible design puts OCR/vision behind an explicit "extracted, please verify" state where every extracted field is shown next to the source image for human confirmation before the rules run.

**Why a spreadsheet would not suffice.** The classification ruleset is the product, it changed in March 2026 without notice, and it will change again. A spreadsheet cannot encode the conditional reverification logic (which depends on citizenship status *and* document type *and* the Section 1 attestation), and cannot version itself when ICE next edits a fact sheet.

**Complexity.** Small to medium. The ruleset is perhaps 40 rules over 25 fields. The OCR path is the only hard part and is optional.

**Learning difficulty.** Fifteen minutes. Drop in files, read a list.

**Measurable value.** Directly computable and unusually legible: Morgan Lewis's published example is **$57,600–$572,200** for a 200-form file of previously-technical errors. Even a partial cure before a Notice of Inspection arrives is worth multiples of any plausible price.

**Risks, privacy, regulatory.** I-9s contain SSNs, immigration status and document numbers — among the most sensitive data an employer holds. **Local-only execution is mandatory**; a cloud version would be a liability, not a feature. The tool must be explicit that it is not legal advice and that a self-audit should generally be conducted under counsel's direction, since discovered violations create their own decisions. Anti-discrimination law constrains remediation: the tool must never suggest re-verifying an employee whose status does not require it.

**Existing products and substitutes.** Full I-9 management platforms (Tracker I-9, WorkBright, Equifax I-9 Anywhere, HireRight) — subscription HR software that manages the I-9 lifecycle going forward. Immigration counsel and consultancies performing paid audits. **Neither substitute serves the employer who has 400 legacy paper I-9s, no budget, and a rule that changed five months ago.** A free, local, versioned checker keyed to the March 2026 list is not obviously available anywhere.

**Why still attractive.** Sharpest possible scope. A ruleset the incumbents encode privately and charge for. A live 2026 catalyst with a documented 10× enforcement increase. And the ideal open-source shape: the ruleset benefits from public scrutiny and community correction, which is exactly what an employer wants in something it will show to counsel.

**Paid customization potential.** High and immediate. Bulk digitization of a legacy paper file; a remediation memo per finding; an annual re-audit engagement; a version tuned to a specific electronic I-9 vendor's export format. This is the clearest services attach in the report.

---

### C2 — Form1095 Preflight: 1094-C/1095-C code, affordability and Part III validator

**Intended user.** HR manager or Controller at a 50–199 FTE Applicable Large Employer, running the check before authorizing the filing vendor to transmit.

**Problem solved.** Problem 4. The forms are produced by a module the employer cannot audit, penalties attach to coding rather than coverage, and the specialist literature documents a stable, checkable taxonomy of recurring errors.

**Current workflow.** The payroll or ben-admin module generates forms in January. HR spot-checks a handful and approves transmission. Errors surface 18–30 months later as Letter 226-J.

**Proposed workflow.** Export the draft 1095-C data (most vendors will produce a CSV or the AIR XML), plus a payroll census with monthly hours, plus the plan's lowest-cost self-only monthly contribution by plan year. The tool cross-validates and returns a ranked defect list with the citation and the dollar exposure for each.

**Required inputs.** Draft 1095-C data; monthly hours-of-service by employee; hire/termination dates; lowest-cost self-only employee contribution; whether the plan is self-insured or level-funded; the employer's chosen affordability safe harbor and measurement method.

**Expected outputs.** (1) Line 14/15/16 combination validity — flagging impossible pairs (1H with 2C; 1A with Line 15 populated; a 2-series safe-harbor code where no offer was made). (2) Missing Line 16 codes, the single most commonly omitted field. (3) Affordability recomputation under all three safe harbors at the correct year's percentage (**9.02% for 2025, 9.96% for 2026**) with the FPL threshold computed rather than looked up. (4) A per-month 95% offer-rate calculation with a red flag on any month below it, alongside what 4980H(a) would cost — **$3,340 per full-time employee minus 30 for 2026**. (5) A 1094-C Part III consistency check — the "checked No when the 95% threshold was actually met" error. (6) A self-insured/level-funded detector that flags a missing Part III when the plan is level-funded. (7) An FTE recomputation confirming ALE status independently of what the vendor assumed.

**Essential features.** The affordability percentages, FPL figures, and 4980H amounts as a dated, versioned data file with the Revenue Procedure cited for each — this is the part vendors get wrong, and this research found two separate vendor sources publishing mislabeled penalty years. Every finding must cite the rule.

**Deliberately excluded.** Filing. Furnishing. Correcting and re-transmitting. Letter 226-J response drafting. The tool checks and explains; it never becomes a filing agent, which is a regulated, support-heavy business.

**AI: inappropriate.** This is deterministic arithmetic and finite-state code validation over structured data. An AI here would add non-determinism to a calculation that must be reproducible in front of the IRS.

**Why a spreadsheet would not suffice.** It nearly would — and some sophisticated HR people do build one. What a spreadsheet cannot do is stay current with three annually-indexed values across a dozen Revenue Procedures, encode the full 1A–1U × 2A–2H validity matrix, or recompute FTE status under the 120-hour cap rule. And a spreadsheet built once in 2023 is now silently wrong in three places.

**Complexity.** Medium. The rules are numerous but each is simple, and the IRS AIR schema is published.

**Learning difficulty.** One hour, given a working knowledge of what a 1095-C is. Zero for someone who does not — but that person should not be filing.

**Measurable value.** Averted exposure of **~$81,600** in stacked §6721/§6722 penalties for a 120-employee ALE (120 × $340 × 2), and up to **$233,800** in §4980H(a) for a 100-FTE ALE. Against an IRS-estimated 28-hour annual burden that practitioners consider understated.

**Risks and constraints.** The tool must be emphatic that it validates *internal consistency and arithmetic*, not the truth of the underlying offer data — it cannot tell you the census is wrong. Employee-level compensation and coverage data is sensitive; local execution. Rules change annually and the tool is worthless if stale, which means a maintenance commitment and an obvious "rules as of [date]" banner.

**Existing products and substitutes.** ACA filing vendors (BoomTax, ACAwise, Trusaic, ACA-Track, Points North) that validate as part of filing; specialist firms (Accord, OneDigital) doing paid reviews; the HRIS module itself. The gap: **an independent second opinion that runs before you commit, that you can read, and that audits the vendor rather than being the vendor.**

**Why still attractive.** The specialist literature documents that the modules themselves are the error source. An independent checker is a different product from a filer, and reviewers at 51–200 employee companies are on record calling their module's ACA process "a nightmare."

**Paid customization potential.** High. Mapping to a specific vendor's export; adding the employer's own plan and measurement configuration; an annual pre-filing review engagement.

---

### C3 — PremiumMatch: three-way benefits invoice reconciliation with credit aging

**Intended user.** HR/benefits administrator or Controller at a 30–200 employee employer, monthly.

**Problem solved.** Problems 1 and 2 — the money leg.

**Current workflow.** Print the carrier invoice, pull the payroll deduction register, pull the enrollment census, compare by eye or in a one-off spreadsheet, email the discrepancies to the broker, overwrite the spreadsheet next month.

**Proposed workflow.** Drop in three files. Get a per-employee, per-plan variance report with an assigned reason code, plus a **persistent open-items register** that carries unresolved variances forward and ages them against the carrier's retroactivity window.

**Required inputs.** Carrier invoice (CSV or PDF); payroll deduction register; enrollment census; a small plan-rate table (tier rates, employer/employee split, effective dates).

**Expected outputs.** (1) Employee-level variance list: on invoice but not enrolled; enrolled but not on invoice; tier mismatch; rate mismatch; deducted but not billed; billed but not deducted. (2) The plan balance identity — deductions plus employer contributions minus carrier premium, which should net to zero — computed per plan per month. (3) Reason codes distinguishing genuine errors from expected timing artifacts: enrollment in transit, termination in transit, retroactive newborn addition, mid-month effective date with no proration, deduction-holiday month, rounding. (4) **The open-items register with a days-open counter and a hard alert when an item approaches the carrier's retroactive limit** (default 60 days, configurable to 30 for New Hampshire and other strict states). (5) A payroll-frequency reconciliation showing 24-vs-26-vs-27 period effects, with an explicit 2026 27th-pay-period warning.

**Essential features.** The open-items register is the differentiator and the reason this is not a spreadsheet. So is the reason-code taxonomy — the tool's job is to shrink a 40-line variance list to the four lines that are actually money.

**Deliberately excluded.** Paying carriers. Generating invoices. Self-bill construction. Any write-back to any system. Claims data. This is a read-only auditor.

**AI: optional, narrowly.** Parsing carrier invoice PDFs where no CSV is available, and only with a human-verified extraction step showing the parsed table against the source page. The reconciliation logic itself is arithmetic.

**Why a spreadsheet would not suffice.** A spreadsheet does the month. It does not carry state across months, and the entire recoverable value is in state that persists across two to three billing cycles — the credit requested in January that must be verified on the March invoice. Every published reconciliation procedure names that verification step, and it is exactly what a monthly spreadsheet loses.

**Complexity.** Medium. The matching logic is straightforward; input format variability is the real work.

**Learning difficulty.** One to two hours for the first run (mostly column mapping), then minutes per month.

**Measurable value.** A vendor's estimate of **$5,000–$15,000 annually recoverable for a 100-employee group** is plausible if unmethodologized; the **$400–$1,600 per terminated employee left on for 1–4 cycles** figure is arithmetically consistent with KFF's $26,054 average family premium. Time: a published per-task estimate puts reconciliation at **1 hour per plan per month**, so ~5 hours/month for a five-plan employer.

**Risks and constraints.** Carrier invoices contain names, coverage tiers and dependent information; a level-funded group's reporting may carry claims data, which is PHI. Local execution, no cloud default, and an explicit warning if a file appears to contain claims-level detail. The tool must not encourage retroactive terminations that would constitute a rescission under 45 CFR 147.128 — it should surface the 60-day window *and* note the prospective-termination-plus-COBRA alternative where claims were incurred.

**Existing products and substitutes.** Tabulera, Beneration, AdminaHealth, Insynctive, Certifi, CleartrackHR — a real and crowded category. All of it sells either to employers well above this size, to carriers and TPAs, or as an outsourced service. None of it is free, local, or usable by an HR person on a Tuesday afternoon.

**Why still attractive.** The category's existence validates the problem. The category's pricing and sales model excludes the segment. And the specific feature that matters most — cross-cycle credit aging — is the one a spreadsheet cannot do at all.

**Paid customization potential.** Very high; arguably the best in the report. Every employer's carrier invoice formats are different, and a parser per carrier is a clean, repeatable, per-client engagement.

---

### C4 — EligibilityLedger: pending-EOI and eligibility-event register

**Intended user.** The HR person responsible for voluntary life, supplemental life, dependent life, and voluntary disability.

**Problem solved.** Problem 3 — the *Gimeno* / *McIver* failure mode.

**Current workflow.** There is none. EOI status lives in a carrier portal or an email thread. Eligibility-ending events arrive in conversation.

**Proposed workflow.** A tiny, disciplined register with exactly two jobs. **Job one:** every coverage election that requires evidence of insurability enters as *pending* and cannot leave that state without a recorded carrier approval or denial — with an escalating alert if a payroll deduction has started while the record is still pending. **Job two:** every eligibility-ending event (divorce, dependent turning 26, employee dropping below hours, loss of student status) enters with the date it was *learned* and produces a propagation checklist across payroll and each carrier, closed only when each is confirmed.

**Required inputs.** Election records for EOI-required coverages; a payroll deduction extract to detect the deduct-without-coverage state; dependent dates of birth for age-out projection; manually entered life events.

**Expected outputs.** (1) An aging pending-EOI list. (2) **A "deducting without confirmed coverage" alert — the single most valuable output in the report relative to its complexity.** (3) A rolling 90-day dependent age-out forecast, with a configurable rule for the end-of-month-of-26th-birthday convention versus the anniversary-date convention some products use. (4) An open eligibility-event list with a per-system propagation checklist. (5) A dated, exportable audit trail of who was notified and when.

**Essential features.** The deduction-versus-coverage cross-check, and the immutability of the audit trail. Everything else is a to-do list.

**Deliberately excluded.** Submitting EOI. Any carrier integration. Enrollment. Claims. Beneficiary designation management.

**AI: inappropriate.** This is a state machine with alerts.

**Why a spreadsheet would not suffice.** It nearly would, and this concept is deliberately the closest thing in the report to "a smart spreadsheet." Two things a spreadsheet cannot do: cross-check against a payroll deduction file to detect the deduct-without-coverage state, and produce a tamper-evident dated record that is worth anything as evidence of prudent fiduciary process. The second is the whole point — the defense in *Gimeno* would have been a record showing the employer chased the EOI.

**Complexity.** Small. Genuinely small — this could be a single-page local web application over a SQLite file.

**Learning difficulty.** Under 30 minutes.

**Measurable value.** Low-frequency, catastrophic-severity. **$350,000** in *Gimeno*. Eleven months of wrongly-collected premiums in *McIver*. This is insurance, and it should be sold as insurance: the ROI case is not time saved, it is the one event that does not happen.

**Risks and constraints.** The tool creates a written record of what the employer knew and when — which cuts both ways and must be said out loud. An employer with a bad process may prefer not to have documented it. The honest answer is that the record is far more likely to help than hurt, since *Gimeno* and *McIver* both turned on the employer having done nothing rather than having documented something imperfect. Also: the tool should be careful to keep any medical information incidental to EOI out of the general personnel record, consistent with the confidential-separate-file requirement that governs FMLA certifications.

**Existing products and substitutes.** Enterprise benefits administration platforms track EOI status when a carrier integration supplies it — which, per Problem 1, is precisely what this segment does not have. Nothing free and standalone was located.

**Why still attractive.** Highest severity-to-complexity ratio in the report. The evidence is two decided appellate cases and a documented DOL enforcement focus. And it is a natural companion install alongside C3, since both consume a payroll deduction extract.

**Paid customization potential.** Moderate. Configuring carrier-specific EOI rules and age-out conventions; an annual eligibility audit engagement.

---

### C5 — ALEWatch: FTE threshold and look-back measurement period monitor

**Intended user.** HR or finance at a company between roughly 35 and 80 employees, or any employer with a substantial part-time or variable-hour population.

**Problem solved.** The first half of Problem 4 — the ALE cliff is invisible, and look-back measurement periods are the documented root cause of downstream 1095-C misclassification.

**Current workflow.** "We have 47 employees, so the ACA doesn't apply to us." Sometimes correct. Sometimes an unnoticed $200,000 problem.

**Proposed workflow.** Feed a monthly payroll hours export. The tool computes the ALE determination per IRS's rule — full-time count plus (total non-full-time hours, capped at 120 per employee, divided by 120) — month by month across the prior calendar year, and shows the trailing average against 50 with a projection. Separately, for a confirmed ALE, it maintains standard and initial measurement periods per employee and produces the stability-period full-time roster.

**Required inputs.** Monthly hours of service by employee; hire and termination dates; the employer's declared measurement/administrative/stability period configuration.

**Expected outputs.** (1) Month-by-month FTE calculation with the prior-year average and current-year running projection, with the arithmetic shown. (2) A "you are within X FTEs of ALE status" alert. (3) Per-employee measurement period status: which period they are in, hours accrued, projected full-time determination, and the date their stability period locks. (4) The stability-period full-time roster — the list that determines who must be offered coverage. (5) Flags for the documented configuration errors, notably measurement periods starting on impermissible dates and administrative periods exceeding 90 days.

**Essential features.** Correct implementation of the 120-hour cap and the rule that hours of service **include paid non-working time** — vacation, holiday, illness, disability, layoff, jury duty, military duty, leave of absence. This is where hand calculations go wrong.

**Deliberately excluded.** Form generation (that is C2). Offer tracking. Enrollment. Affordability (C2).

**AI: inappropriate.** Arithmetic.

**Why a spreadsheet would not suffice.** The FTE calculation alone is spreadsheet-tractable. The measurement-period state machine is not: it requires per-employee period tracking with different rules for ongoing versus newly-hired variable-hour employees, an initial measurement period that can run "up to 13 months plus a partial month," and the counter-intuitive rule that during a stability period an ongoing employee's *current* hours are irrelevant.

**Complexity.** Small to medium.

**Learning difficulty.** One hour, and the output is legible to a CFO — which matters, because the person who needs convincing that the company is now an ALE is usually the CFO.

**Measurable value.** Avoiding an unknowing ALE year: **$233,800** in 4980H(a) exposure at 100 FTEs, plus the information-return penalties, plus a Letter 5699 for non-filing. Also avoids the opposite error — a company that believes it is an ALE and isn't, buying compliance it does not owe.

**Risks and constraints.** Hours data is sensitive but less so than most in this report. The controlled-group aggregation rule under IRC §414 (commonly-owned companies combine for ALE determination) is a real trap the tool should surface as a question rather than attempt to answer.

**Existing products and substitutes.** ACA compliance vendors do this as part of a subscription; Ease charges **$6 per employee per form per year** for its ACA module. Payroll systems generally do not surface it at all below their ACA add-on tier.

**Why still attractive.** It answers a question the employer does not know it has, using data it already exports for payroll. Cheap to build, easy to verify against IRS's published examples.

**Paid customization potential.** Moderate. Controlled-group configuration; measurement-period design consulting, which is a genuinely expert task.

---

### C6 — LeaveClock: FMLA/PFML intake, rolling-balance and notice generator

**Intended user.** The one-person HR function at a 50–200 employee multi-state employer.

**Problem solved.** Problem 6.

**Current workflow.** Spreadsheets and email — per AbsenceSoft, 41% even at 500+ employees. Notices are generated ad hoc from DOL PDFs, or not at all.

**Proposed workflow.** Five jobs, in order of value: **(a)** an intake capture that any manager can use in thirty seconds, which timestamps the moment the employer acquired knowledge and starts the 5-business-day clock; **(b)** an applicability determination — which of FMLA, state PFML, state paid sick leave, ADA/PWFA and company policy apply to *this* person on *this* date, given tenure, hours, worksite, and work state; **(c)** generation of the correct dated notices (WH-381, WH-382, certification request) with the dates filled in and the record stamped; **(d)** a rolling-365-day FMLA balance maintained at the employer's payroll increment, with concurrent state balances tracked separately; **(e)** a defensible exportable case file.

**Required inputs.** Employee roster with hire dates, hours worked (or scheduled hours), work state and assigned worksite; company configuration (leave-year method, increment, worksite locations); absence records.

**Expected outputs.** Dated notices; a rolling balance per employee per statute; certification and recertification due-date tracking (15 calendar days for certification, 7-day cure, recertification no more often than every 30 days or 6 months for indefinite conditions); a per-case chronological file; and a "clocks at risk" dashboard of everything approaching a deadline.

**Essential features.** The intake capture is the highest-value component and the cheapest to build — most of the loss in this segment is not misapplying a rule, it is never learning the clock started. The rolling-backward window is second. Notice generation is third.

**Deliberately excluded.** Claims adjudication. Medical certification review or sufficiency determination. STD/LTD benefit calculation. Payroll integration. State PFML claim filing. ADA accommodation *decisions* (tracking the interactive process is in scope; deciding it is not). **Critically, in a v1: state PFML rules for more than two or three states.** The honest failure mode of this concept is trying to be a 16-jurisdiction rules engine on day one and shipping nothing.

**AI: optional and secondary.** Classifying free-text intake ("my mom's having surgery and I need Thursdays for a while") into a probable qualifying reason and leave type, as a *suggestion* requiring confirmation. Everything downstream must be deterministic.

**Why a spreadsheet would not suffice.** SHRM publishes FMLA tracking spreadsheets, which is the strongest possible admission that the profession expects people to do this by hand. What the spreadsheet cannot do: start a clock from an event it never sees, recompute a trailing-365-day sum on every leave day at minute granularity, hold concurrent balances against different statutes with different increments, or produce a dated notice record that proves what was sent when — which under Washington HB 1213 is now worth an entire second leave entitlement.

**Complexity.** Medium, and the largest scope risk in the report.

**Learning difficulty.** Two to three hours, plus a configuration decision (leave-year method) the user may need counsel for. This is the least learnable concept here.

**Measurable value.** Hard to state honestly, and this report will not invent it: **no credible published benchmark exists for hours or dollars per leave case.** DOL's own enforcement is small ($1.03M nationally in FY2025). The real value is litigation defense — the leave file that exists when the demand letter arrives — plus, in Washington specifically, avoiding a doubled job-protection period from a documentation failure. DOL's 2018 survey implies ~15 leave events/year at 100 employees.

**Risks and constraints.** Medical certifications must be stored separately from personnel files under 29 CFR 825.500(g); the tool's data model must enforce that separation rather than merely recommend it. Getting an applicability determination wrong is worse than not offering one — every determination must show its inputs and cite its rule, and the tool must refuse to answer rather than guess where it lacks the state rules.

**Existing products and substitutes.** A real market with a clear pricing floor. **Stiira publishes $9,950/year for up to 500 employees** — an effective $16.58 PEPM at 50 employees versus $1.66 at 500. Tilt publishes $4–6 PEPM. AbsenceSoft, Cocoon and Sparrow publish nothing and sell consultatively. G2's 2026 roundup notes mid-market is the sweet spot "with limited discussion of affordability or simplified features specifically designed for small teams under 50 employees." And **TriNet announced on April 9, 2026 that it will acquire Cocoon, expressly "Expanding Leave Management Solutions for SMBs"** — the incumbents' answer to this gap is *bundle it into a PEO*, which is a full employment-relationship commitment rather than a tool.

**Why still attractive despite them.** The gap is not absence of software; it is a **pricing floor plus category confusion**. The SMB market's "leave management software" — BambooHR, Gusto, Rippling, Timetastic, LeaveBoard — is PTO-balance tracking, not statutory-leave case management. Buyers cannot tell them apart from the category name and therefore believe they already have the tool. A free, honest, narrowly-scoped statutory tracker names the distinction.

**Paid customization potential.** Very high — per-state rule packs, handbook-policy alignment, and configuration are natural paid work.

---

### C7 — StateOnboard: new-state employment obligation pre-flight

**Intended user.** HR or finance about to hire the company's first employee in a new state.

**Problem solved.** The multi-state burden multiplier described in §1.

**Current workflow.** Google, the payroll rep, and hope. Per NSBA's 2025 survey, **only 1 in 10 small businesses have dedicated staff monitoring regulatory changes.**

**Proposed workflow.** Enter the state, the expected in-state headcount, total company headcount, industry, and federal-contractor status. Get a dated, cited obligation checklist.

**Required inputs.** Five fields.

**Expected outputs.** A checklist covering: state income tax withholding registration (skip in the nine no-income-tax states); **SUTA registration — required in every state including the nine**; workers' compensation, flagging the monopolistic state funds in ND, OH, WA and WY; new-hire reporting (20-day federal floor, with the multistate-employer election and its HHS designation requirement); the applicable PFML program with its 2026 rate, split, small-employer exemption and quarterly filing obligation; the paid sick leave accrual denominator (1 hour per 30 / 35 / 37 / 40 / 52 hours worked, or Nevada's 0.01923/hour) and the size-dependent annual cap; any state-mandated retirement program with its threshold, deadline and per-employee penalty; the separation notice form if the state requires one; the final-pay deadline and penalty; and the required poster set.

**Essential features.** **The dataset is the product.** The code is a thin shell around a versioned, cited, community-correctable data file. Every row carries a source URL and a "verified as of" date, because half the value is the user being able to check.

**Deliberately excluded.** Actually registering anything. Payroll tax calculation. Nexus determination for corporate income tax. Anything requiring an account with a state agency.

**AI: inappropriate.** Wrong answers here are expensive and the data must be human-curated and citable.

**Why a spreadsheet would not suffice.** It would — and that is the point. This *is* a spreadsheet, published, versioned, cited and kept current. The software is the conditional logic (which rows apply given headcount and industry) and the change log.

**Complexity.** Medium, entirely in data curation, which is ongoing rather than one-time.

**Learning difficulty.** Five minutes.

**Measurable value.** A vendor estimate puts manual DIY setup at **10–20 hours per state**; a 60-person company across 15 states implies 150–300 hours. Penalties avoided are concrete: CalSavers at $250/eligible employee; Oregon at $100/employee to a $5,000 cap; Virginia RetirePath at $200/eligible employee; New Jersey escalating $100 → $250 → $500.

**Risks and constraints.** Stale data is worse than no data, and this is the highest-maintenance concept in the report. The tool must display a prominent "verified as of" date per row and degrade honestly — showing "not verified since [date]" rather than a confident stale answer.

**Existing products and substitutes.** **This is the weakest differentiation in the report and should be said plainly.** Mosey, Middesk, Warp and Rippling all sell state compliance registration and monitoring; Rippling in particular bundles it. The open-source angle is real (a free, citable, forkable dataset versus a subscription) but it competes against well-funded incumbents doing exactly this.

**Why still attractive.** As a data asset rather than a product. The dataset underpins C6's applicability logic and C9's threshold logic, and a maintained public dataset is a credible reputation and lead-generation asset even if the tool itself never wins on features.

**Paid customization potential.** Moderate — a monitored footprint for a specific company, with change alerts.

---

### C8 — CensusDiff: carrier eligibility audit

**Intended user.** HR/benefits administrator, quarterly and immediately after open enrollment.

**Problem solved.** Problem 1's eligibility leg, distinct from C3's money leg. C3 asks "are we paying the right amount?" C8 asks **"is everyone who should be covered actually covered, and is anyone covered who shouldn't be?"** The *Gimeno* fact pattern lives on this side.

**Current workflow.** Not done, except by accident when an employee reports a denied claim.

**Proposed workflow.** Export a census from each carrier portal and one from the system of record. The tool produces a per-carrier, per-employee difference report.

**Required inputs.** A census export per carrier; the system-of-record enrollment export; the active employee roster.

**Expected outputs.** Per carrier: enrolled in system-of-record but absent from the carrier (**the highest-severity finding — this is the employee who thinks they have coverage and does not**); present at the carrier but not an active employee; tier mismatch; dependent present at one and not the other; coverage-volume mismatch on life/disability; and effective-date mismatch. Plus a cross-carrier view showing employees whose enrollment pattern differs between medical and ancillary lines, which is the fingerprint of a missed portal.

**Essential features.** Fuzzy name matching that is conservative and shows its work — carrier censuses use maiden names, middle initials and truncated fields, and an over-eager matcher hides exactly the record that matters.

**Deliberately excluded.** Correcting anything. Any write-back. Claims. Premium arithmetic (C3).

**AI: optional and marginal.** Name/entity matching. A well-tuned deterministic matcher with a manual review queue is probably better and certainly more auditable.

**Why a spreadsheet would not suffice.** VLOOKUP across five carrier exports with inconsistent name formatting and no common key is exactly the task people do badly and give up on. And the highest-severity finding — the person missing entirely from a carrier — is the one a VLOOKUP against the carrier file will silently skip.

**Complexity.** Small.

**Learning difficulty.** Under an hour.

**Measurable value.** Same litigation exposure as C4 — *Gimeno*'s $350,000 — plus the recurring smaller cost of employees discovering mid-year they were never enrolled, which a named survey puts in context: **50% of employees who experienced a payroll or benefits mistake say it took over a week to correct.**

**Risks and constraints.** Census files contain dependent names and dates of birth. Local only.

**Existing products and substitutes.** Enterprise ben-admin platforms reconcile when they hold an EDI feed. Which, per Problem 1, this segment does not.

**Why still attractive.** Small, sharp, high-severity, and it pairs naturally with C3 and C4 into a coherent three-tool "benefits back office" bundle sharing the same input files.

**Paid customization potential.** High — a carrier-export parser per client, and a quarterly audit engagement.

---

### C9 — ThresholdCheck: headcount cliff and filing-obligation determinator

**Intended user.** HR or finance at any growing company, run once a year and whenever headcount changes materially.

**Problem solved.** The first structural fact in §1 — eight obligations, eight counting populations, one person.

**Current workflow.** Discovery by accident, or by a broker or accountant happening to mention it.

**Proposed workflow.** Enter the company profile once: headcount by state and worksite, peak headcount per establishment, FTE calculation (from C5), participants with 401(k) account balances, employees covered by *any* ERISA welfare benefit, federal contract value, industry NAICS. Get a determination per obligation: **applies / does not apply / borderline**, with the counting rule shown, the deadline, and the penalty for missing it.

**Required inputs.** A short structured profile plus two payroll extracts.

**Expected outputs.** A per-obligation determination covering federal COBRA (20), ADA/PWFA (15), FMLA (50 on payroll for 20 calendar workweeks in the current *or preceding* year), ACA ALE (50 FTE), EEO-1 (100, or 50 for federal contractors — with the current rescission status noted), California pay data (100 payroll employees with ≥1 in CA, deadline the second Wednesday of May, penalties now **mandatory and non-waivable under SB 464 effective January 1, 2026** with "good faith" no longer a defense), Illinois EPRC (100 Illinois employees, $150 fee, biennial), OSHA electronic submission (per-establishment peak headcount, Appendix A/B industry test, March 2 deadline), VETS-4212 (**$200,000 contract value with no employee-count floor**, filing window August 1 – September 30), and Form 5500.

**The killer feature is the Form 5500 welfare-plan wrap test.** The counting population is employees plus COBRA beneficiaries covered by *any* ERISA benefit — medical, dental, vision, **life**, disability. The most common silent failure in this segment is a company whose medical plan has 85 enrolled (so HR believes it is exempt) but whose employer-paid basic life covers all 130 employees, pulling the entire wrap plan over 100 and creating an unfiled 5500. DOL exposure is **$2,739/day with no cap**; DFVCP self-correction caps at **$750 per filing / $1,500 per plan**. A tool that surfaces this once has paid for the entire catalog.

**Essential features.** Each determination must show the counting population it used and the source it counted from, because the entire failure mode is counting the wrong people.

**Deliberately excluded.** Filing anything. Preparing anything. Reminders and task management — this is a determinator, not a calendar; it outputs an ICS file and stops.

**AI: inappropriate.**

**Why a spreadsheet would not suffice.** The tests use different populations from different source files. A spreadsheet with one headcount cell answers all eight questions wrong.

**Complexity.** Small.

**Learning difficulty.** Thirty minutes.

**Measurable value.** The 5500 case alone: uncapped $2,739/day versus $750 to self-correct. California pay data at 150 CA employees is a mandatory **$15,000** minimum for an initial violation at $100/employee.

**Risks and constraints.** Aggregation rules (controlled groups under IRC §414 for ACA; common ownership generally) are genuinely hard and the tool should raise them as flagged questions rather than pretend to resolve them. Thresholds move — EEO-1 is under an active rescission NPRM published July 23, 2026, with obligations remaining in force unless and until a final rule issues.

**Existing products and substitutes.** Benefits brokers and CPAs advise on this informally. Compliance calendars exist as content marketing. A determinator that computes *from the employer's own data* was not located.

**Why still attractive.** Cheapest build in the report, and it is the natural top of the funnel: it tells the employer which of the other eight tools it actually needs.

**Paid customization potential.** Moderate — controlled-group analysis and an annual review.

---

## 5. Opportunity ranking

Scored 1–5 on ten criteria. **Sev** = severity of problem; **Freq** = frequency of use; **ROI** = clarity of return; **Learn** = ease of learning; **Impl** = ease of implementation; **Scope** = ability to stay narrowly scoped; **Diff** = market differentiation; **Cust** = customization potential; **Data** = availability of realistic test data; **Conf** = confidence in the underlying evidence.

| # | Concept | Sev | Freq | ROI | Learn | Impl | Scope | Diff | Cust | Data | Conf | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **C1** | **I9Audit** — I-9 substantive-error scanner | 5 | 4 | 5 | 5 | 4 | 5 | 4 | 4 | 4 | 5 | **45** |
| **C2** | **Form1095 Preflight** — 1094-C/1095-C validator | 5 | 3 | 5 | 4 | 4 | 4 | 4 | 5 | 5 | 5 | **44** |
| **C4** | **EligibilityLedger** — pending-EOI register | 5 | 3 | 3 | 5 | 5 | 5 | 4 | 3 | 4 | 4 | **41** |
| **C3** | **PremiumMatch** — invoice reconciliation | 4 | 5 | 5 | 4 | 3 | 4 | 3 | 5 | 3 | 4 | **40** |
| **C5** | **ALEWatch** — FTE / measurement monitor | 4 | 4 | 4 | 4 | 4 | 4 | 3 | 4 | 4 | 5 | **40** |
| **C8** | **CensusDiff** — carrier eligibility audit | 4 | 4 | 4 | 5 | 4 | 5 | 3 | 4 | 3 | 4 | **40** |
| **C9** | **ThresholdCheck** — headcount cliff determinator | 4 | 2 | 3 | 5 | 5 | 4 | 4 | 3 | 5 | 5 | **40** |
| **C7** | **StateOnboard** — new-state pre-flight | 4 | 3 | 4 | 5 | 4 | 3 | 2 | 4 | 5 | 4 | **38** |
| **C6** | **LeaveClock** — FMLA/PFML tracker | 5 | 3 | 4 | 3 | 3 | 2 | 4 | 5 | 3 | 5 | **37** |

### The top three

**1. C1 — I9Audit (45).** It wins on the combination the criteria are designed to reward: maximum severity, minimum scope, near-zero learning curve, and a directly computable dollar value. Uniquely among the nine, it has a **live catalyst with a date** — ICE's unannounced March 16, 2026 fact-sheet revision moved a dozen categories of ordinary clerical omission from curable to immediately fineable, retroactively across every I-9 already in the cabinet, against a documented tenfold increase in Notice of Inspection volume and a 3-business-day response window. The two most commonly skipped Section 2 fields — the representative's *title* and the employee's *first date of employment* — are now $288–$2,861 events apiece. It is also the best open-source fit in the report: the ruleset benefits from public scrutiny, which is exactly what an employer wants in something it will hand to counsel. The one honest weakness is data ingestion from scanned paper, which is why the OCR path must be optional and human-verified rather than load-bearing.

**2. C2 — Form1095 Preflight (44).** The most defensible ROI of the nine, and the only concept where the specialist literature independently documents that *the incumbent modules themselves* are the error source. It scores highest on test-data availability because the IRS publishes the AIR schema, the code matrix, and worked examples — meaning the tool can be validated against authority rather than opinion. The exposure is stacked and computable: ~$81,600 in §6721/§6722 for a 120-employee ALE from coding alone, before any coverage failure, against 2026 affordability and penalty figures (9.96%, $3,340/$5,010) that changed materially from 2025 and that this research found at least two vendors publishing incorrectly. An independent second opinion that runs *before* transmission — and audits the vendor rather than being the vendor — is a different product from everything currently sold.

**3. C4 — EligibilityLedger (41).** The best severity-to-complexity ratio here by a wide margin. It is a small local register that could ship in a weekend, and it addresses a failure mode with two decided federal appellate decisions behind it — *Gimeno* (11th Cir. 2022, $350,000, three years of deductions for coverage that was never in force) and *McIver* (9th Cir. 2024, eleven months of deductions after an eligibility-ending divorce) — plus a documented DOL enforcement focus. Its low ROI score is honest and reflects a real sales problem, not a real value problem: the return is a catastrophe that does not occur, which is always harder to sell than hours saved. That argues for shipping it as a companion to C3, with which it shares its payroll-deduction input file.

### What should be investigated next

**Build C1 first.** Smallest scope, highest score, live catalyst, and the ruleset is self-contained enough that a working version validates the entire market thesis in days rather than weeks.

**Investigate C3 next, not C2.** C2 scores higher, but C3 has the higher *information* value: it is the concept whose feasibility is least certain, because its viability turns on a question this research could not answer — what carrier invoices actually look like as files, and whether small employers can obtain them as CSV or only as PDF. That question is cheap to answer and determines whether C3 is a small tool or a parser-maintenance business. Answer it before committing.

**Defer C6 despite its severity.** It has the worst scope-control score in the report and its incumbent landscape just consolidated (TriNet/Cocoon, April 2026). If pursued, pursue only the intake-and-notice slice — clock detection and dated notice generation — and explicitly refuse the multi-state rules engine in v1.

---

## 6. Validation plan

### For C1 — I9Audit

**Questions to ask practitioners.**
- When did you last look at your I-9 file? Do you know how many you have?
- Are they paper, scanned PDF, or in a system? If a system, can you export the field data or only a PDF image per employee?
- Who completes Section 2 — HR, a manager, a location supervisor? Do they sign with their title?
- Were you aware anything changed about I-9 enforcement in March 2026?
- If a tool told you 90 of your 400 I-9s had immediately fineable errors, what would you do next — fix them yourself, call a lawyer, or nothing?

**Who to interview.** HR generalists at 50–200 employee companies in hospitality, construction, staffing and healthcare (the named enforcement-priority industries); immigration attorneys who perform I-9 audits, who will know both the real error distribution and where a self-audit tool creates problems; fractional-HR consultants, who see many companies' files and are the most likely early adopter.

**Search terms for further research.** `I-9 self audit checklist 2026`, `ICE substantive violation March 2026`, `Form I-9 error rate audit study`, `I-9 internal audit under attorney-client privilege`, `M-274 handbook for employers 2026`.

**Sample data needed.** A dozen completed I-9s spanning the 08/01/23 and 01/20/25 editions with realistic defects — best obtained synthetically, since real ones are among the most sensitive documents an employer holds. USCIS publishes the blank form and the M-274 handbook, which together are enough to build a defensible test corpus.

**Prototype that would validate it.** A single-page local tool with a manual entry form for one I-9 that returns the classified findings list. No OCR, no batch. If an HR person enters one form, sees three findings they did not know were findings, and immediately asks "can I do this for all of them?" — validated.

**Assumptions most likely to make it fail.** (1) That employers can get I-9 field data out of their systems in structured form; if everything is a scanned image, the product's cost is dominated by OCR quality, which changes the build. (2) That employers will act on findings rather than preferring not to know — a real risk, since a documented self-audit that is not remediated is arguably worse than none, and counsel may advise against running the tool outside privilege. (3) That the March 2026 classification holds; ICE changed it once without notice and could change it again.

### For C2 — Form1095 Preflight

**Questions.** Who produces your 1095-Cs? Have you ever received a Letter 226-J or 5699? Do you know which affordability safe harbor you use and why? Which measurement method — monthly or look-back? Has anyone other than the vendor ever checked the forms?

**Who to interview.** Benefits brokers serving 50–200 employee clients (they see the failure pattern across a book); ACA specialist filers; a Controller who has actually responded to a 226-J, who will describe the reconstruction burden better than any secondary source.

**Search terms.** `226-J response reconstruction`, `1095-C line 16 blank penalty`, `ACA measurement period configuration error`, `level funded plan Part III 1095-C`, `AIR schema validation errors TY2025`.

**Sample data.** IRS publishes the AIR XML schema and business rules; synthetic 1095-C datasets with deliberately seeded errors are straightforward to construct and are the correct test corpus.

**Prototype.** A CSV-in, findings-out validator covering only Line 14/15/16 combination validity and affordability recomputation — perhaps 25 rules. Run it against one real employer's prior-year file (with a broker's permission) and count the findings. If a clean vendor-produced file yields zero findings, the thesis is wrong and that is worth knowing immediately.

**Assumptions most likely to fail.** (1) That the module's output is exportable in a usable form. (2) That the error rate in vendor-produced files is materially above zero — the entire concept rests on the specialist firms' claim that it is, which is credible but comes from parties selling remediation. **This is the single assumption most worth testing first.** (3) That employers will run a check they cannot act on without going back to the vendor.

### For C3 / C8 / C4 — the benefits back-office trio

**Questions.** How do you receive carrier invoices — PDF, portal download, CSV, paper? Can you export a census from each carrier portal? How many portals do you log into? What do you do when you find a discrepancy, and how do you know it got fixed? Has an employee ever discovered they were not enrolled?

**Who to interview.** Benefits account managers at independent brokerages (they do this reconciliation for clients and know every carrier's file formats); HR administrators at 50–150 employee companies; a benefits reconciliation service provider, who will describe the actual error distribution better than their own marketing does.

**Search terms.** `carrier list bill CSV export`, `benefits invoice reconciliation template`, `retroactive termination credit carrier 60 days`, `evidence of insurability pending tracking`, `deduction holiday biweekly 27 pay periods 2026`.

**Sample data needed — this is the gating item.** Real carrier invoice files from three or four different carriers, de-identified. Without them, C3's difficulty is unknowable. A friendly broker is the fastest path.

**Prototype.** For C8, a two-file diff with conservative fuzzy name matching — buildable in a day and immediately convincing if it surfaces one missing person. For C3, a hand-run reconciliation of one employer's single month using their real files, done manually, purely to characterize the variance distribution and the reason-code taxonomy before writing any code.

**Assumptions most likely to fail.** (1) That carrier invoices are obtainable as structured data rather than PDF-only — the make-or-break question. (2) That the recoverable dollar amounts are real; every published figure is vendor-sourced without methodology, and it is entirely possible that a well-run broker already catches most of this. **Ask brokers directly what they catch and what they miss.** (3) That the employer, not the broker, is the buyer — if brokers do this work as a retention service, the product's customer is the brokerage, which is a different go-to-market and possibly a better one.

### Cross-cutting research gaps worth closing

Four gaps in the public record surfaced repeatedly and would each materially improve targeting:

1. **No published statistic exists for spreadsheet use in HR at 20–200 employee companies.** Every available figure is enterprise (AdviserPlus, 1,000+) or mid-market (Aeqium 500–10,000; AbsenceSoft 500+). This is the strongest argument for original primary research and would be cheap to run.
2. **No survey measures how many carrier portals a small employer touches.** The 3–6 estimate used in this report is derived from carrier-line structure, not measured.
3. **No data on SIDES E-Response adoption by employer size**, despite it being free and clearly correct for this segment.
4. **No credible benchmark for hours or dollars per leave case.** The entire genre is vendor-produced with undisclosed methodology.

---

## 7. Cross-industry patterns

Six patterns from this market that transfer to specific markets already in the backlog.

**P1 — Regulator-classification linter: a checker whose value is the classification ruleset, not the checking.** The I-9 case is pure: the same form, the same fields, but a March 2026 reclassification moved a dozen defects from curable to fineable. The software is trivial; the maintained, dated, cited ruleset is the entire asset, and it is exactly what incumbents encode privately and charge for. *Transfers to:* **Certified payroll and prevailing wage compliance service providers** (WH-347 field validity and fringe-benefit statement classification); **Environmental laboratories producing regulator EDD deliverables (EQuIS and state formats)**; **Truck permitting and registration service agencies (IRP, IFTA, OS-OW, state permits)**; **County recorder offices — document intake, indexing and rejection handling**.

**P2 — Cross-cycle open-item aging: the value is in the state that persists between runs, not in any single run.** The benefits credit requested in January and verifiable only on the March invoice is invisible to a monthly spreadsheet, and every published reconciliation procedure names that verification step as the one people skip. Any reconciliation whose corrections arrive one or more cycles after the request has this shape. *Transfers to:* **Freight bill audit and payment for small shippers**; **Independent pharmacy third-party reconciliation and PBM claw-backs**; **Submetering and utility expense recovery service providers**; **Cargo claims and OS&D handling at brokerages and small carriers**.

**P3 — Pending-state register: things submitted to a third party that must reach a terminal state, tracked to closure.** The EOI case is the sharpest version — a premium is being deducted for coverage that exists only if a form the employer sent reached approval, and nothing anywhere reports the pending state. Wherever a submission's approval is a precondition to something already being relied upon, the same silent failure exists. *Transfers to:* **Provider credentialing and payer enrollment services**; **Delegated-design submittal coordination (specialty engineers of record for delegated components)**; **Building permit expediting and code consulting firms**; **Special inspection agency accreditation consultants (IAS AC291, ANAB, WABO)**.

**P4 — Threshold determinator: which obligations apply to us, and by which counting rule.** Eight obligations at eight thresholds counting eight different populations, with a single headcount cell producing eight wrong answers. Wherever applicability is computed rather than declared — and especially where the counting population differs from the intuitive one — the determination is a harder and more valuable problem than the compliance work that follows it. *Transfers to:* **Sales tax compliance outsourcing for small multi-state sellers** (economic nexus thresholds); **ITAR and EAR export compliance administration at small manufacturers**; **Community floodplain administration at small municipalities (permit-side floodplain compliance)**; **Government contracts administration at small govcons (clause and mod review)**.

**P5 — Statutory clock detection at the point of first knowledge.** FMLA's 5-business-day clock starts when the employer "acquires knowledge," and the employee "need not expressly assert rights under the FMLA or even mention the FMLA" — so the most common failure is not misapplying a rule but never learning a clock started. Cheap intake capture at the moment of first knowledge is worth more than any amount of downstream rules engineering. *Transfers to:* **HOA and condominium management companies — estoppel and demand response desk**; **Mortgage servicer payoff and lien release departments**; **Estate planning and probate practice**; **Public adjusting firms (policyholder-side property claims)**.

**P6 — Jurisdiction rule dataset as the product, code as a thin shell.** Paid sick leave uses five different accrual denominators across 21+ states; PFML has 16 jurisdictions with different rates, exemptions and filing calendars; 15+ states run retirement mandates with five new deadlines in 2026. The differentiator is a versioned, cited, per-row-dated dataset that degrades honestly rather than a clever engine. *Transfers to:* **Multi-state charitable solicitation registration compliance**; **Workers' compensation medical billing and state fee schedule compliance**; **Title 24 acceptance test technicians (ATT) and acceptance testing providers**; **Fire protection inspection, testing and maintenance (ITM) contractors under NFPA 25** (state and AHJ amendments to the adopted standard).

**One negative pattern worth recording.** *Free-because-someone-else-pays software creates a switching trap and a data-ownership gap.* Employee Navigator and Ease are licensed **by the broker** and provided to the employer at no direct charge; the employer's enrollment history, dependent data and plan configuration therefore live in a system it does not contract for. The same structure appears wherever a service provider supplies the client's system of record as a retention device — and it reliably produces a market for tools that work on *exports* rather than integrations, because the export is the only thing the client actually owns. This is a structural reason the file-in/file-out architecture used across all nine concepts is correct rather than merely convenient.

---

## 8. Sources and confidence

### Verified findings — primary regulatory, statutory, judicial and vendor-primary sources

**Form I-9 and worksite enforcement**
- [8 CFR 274a.2 — completion and retention](https://www.ecfr.gov/current/title-8/chapter-I/subchapter-B/part-274a/subpart-A/section-274a.2) · [8 CFR 274a.10 — current civil penalty ranges](https://www.ecfr.gov/current/title-8/chapter-I/subchapter-B/part-274a/subpart-B/section-274a.10) · [DHS civil monetary penalty adjustment, Jan 2, 2025](https://www.federalregister.gov/documents/2025/01/02/2024-31204/civil-monetary-penalty-adjustments-for-inflation)
- [ICE Form I-9 Inspection fact sheet](https://www.ice.gov/factsheets/i9-inspection) · [Morgan Lewis — ICE Rewrites the Rules on Form I-9 Violations (April 2026)](https://www.morganlewis.com/pubs/2026/04/ice-rewrites-the-rules-on-form-i-9-violations) · [National Law Review — Fixable to Fineable](https://natlawreview.com/article/fixable-fineable-ices-quiet-overhaul-i-9-violation-classifications) · [Sheppard Mullin — ICE's expanded list of substantive errors](https://www.sheppard.com/insights/blogs/what-employers-need-to-know-ices-expanded-list-of-i-9-substantive-errors-and-penalties)
- [E-Verify — minor changes to Form I-9 (01/20/25 edition)](https://www.e-verify.gov/about-e-verify/whats-new/minor-changes-to-form-i-9-and-e-verify-updates) · [USCIS — completing Section 2](https://uscis.gov/i-9-central/complete-correct-form-i-9/completing-section-2-employer-review-and-verification) · [E-Verify — EAD revocation guidance](https://www.e-verify.gov/ead-revocation-guidance-for-e-verify-employers) · [Greenspoon Marder — 2025/2026 immigration compliance statistics](https://www.gmlaw.com/news/u-s-immigration-compliance-statistics-for-2025-2026/)

**ACA employer reporting**
- [IRS — determining if an employer is an ALE](https://www.irs.gov/affordable-care-act/employers/determining-if-an-employer-is-an-applicable-large-employer) · [IRS — identifying full-time employees](https://www.irs.gov/affordable-care-act/employers/identifying-full-time-employees) · [IRS — instructions for Forms 1094-C and 1095-C](https://www.irs.gov/instructions/i109495c) · [IRS Q&A on employer shared responsibility](https://www.irs.gov/affordable-care-act/employers/questions-and-answers-on-employer-shared-responsibility-provisions-under-the-affordable-care-act)
- [Rev. Proc. 2025-26 — 2026 4980H amounts ($3,340 / $5,010)](https://www.irs.gov/pub/irs-drop/rp-25-26.pdf) · [Rev. Proc. 2024-14 — 2025 amounts](https://www.irs.gov/pub/irs-drop/rp-24-14.pdf) · [Rev. Proc. 2024-40 — §6721/6722 penalties](https://www.irs.gov/pub/irs-drop/rp-24-40.pdf) · [Mercer — 2026 affordability percentage 9.96%](https://www.mercer.com/insights/law-and-policy/2026-affordability-percentage-for-employer-health-coverage-increases/) · [Newfront — ACA affordability determination in 2026](https://www.newfront.com/blog/the-aca-affordability-determination-in-2026) · [Newfront — the ACA look-back measurement method](https://www.newfront.com/blog/the-aca-look-back-measurement-method) · [Newfront — ACA reporting requirements in 2026](https://www.newfront.com/blog/aca-reporting-requirements-in-2026)
- [ADP on T.D. 9972 — the 10-return e-file aggregation rule](https://www.adp.com/spark/articles/2023/02/irs-dramatically-expands-electronic-filing-mandate-in-2024.aspx) · [Segal — Paperwork Burden Reduction Act & Employer Reporting Improvement Act](https://www.segalco.com/consulting-insights/new-laws-modify-aca-employer-shared-responsibility-reporting/) · [IRS PRA burden estimate, Fed. Reg. 2024-09021](https://regulations.justia.com/regulations/fedreg/2024/04/26/2024-09021.html)
- Error taxonomy: [Accord — hidden costs of inaccurate ACA reporting](https://accord-aca.com/articles/the-hidden-costs-of-inaccurate-aca-reporting) · [OneDigital — correcting ACA reporting mistakes](https://www.onedigital.com/blog/guide-to-correcting-aca-reporting-mistakes/) · [ERISAfire — six most common mistakes](https://help.erisafire.com/en/articles/3630274-the-six-most-common-mistakes-employers-make-in-aca-reporting)

**Benefits billing, enrollment and eligibility**
- [Harvard Pilgrim administrative guide — retroactivity windows](https://www.harvardpilgrim.org/documents/broker/administrative-guide) · [CCMHG retroactive transactions policy](https://ccmhg.com/retroactive-health-transactions-policy/) · [45 CFR 147.128 — prohibition on rescissions](https://www.ecfr.gov/current/title-45/subtitle-A/subchapter-B/part-147/section-147.128) · [Newfront — terminated employees not terminated from coverage](https://www.newfront.com/blog/terminated-employees-not-terminated-coverage-2)
- [Employee Navigator integrations guide — "group size 100+"](https://myatlaslogin.employeenavigator.com/the-definitive-guide-to-integrations-with-employee-navigator/) · [Namely — carrier feeds getting started](https://vensure.clientspace.net/Namely/Content/Namely%20Files/Benefit%20Admin/Carrier%20Feeds%20Getting%20Started.htm) · [Netchex carrier feeds FAQ (PDF)](https://netchex.com/wp-content/uploads/2020/05/Frequently-Asked-Questions-Carrier-Feeds-5-18.pdf) · [Carrier EDI minimum group size table (2018, vendor-hosted)](https://d3bql97l1ytoxn.cloudfront.net/app_resources/320467/documentation/934228_en.pdf)
- [Selerix — how to audit your benefits data](https://selerix.com/blog/how-to-audit-your-benefits-data-and-eliminate-costly-errors/) · [NIS Benefits — employer's guide to monthly reconciliation](https://blog.nisbenefits.com/employers-guide-to-monthly-reconciliation) · [Certifi — self-administered billing](https://www.certifi.com/blog/what-is-employer-self-administered-billing-and-when-should-insurers-support-it/) · [Tabulera — list bills vs self bills](https://tabulera.com/blog/list-bills-and-self-bills-difference-in-the-reconciliation-process)
- EOI liability: [Thomson Reuters on *Gimeno v. NCHMD* (11th Cir. 2022)](https://tax.thomsonreuters.com/blog/eleventh-circuit-allows-claim-for-equitable-relief-based-on-fiduciary-breach-in-erisa-plan-enrollment/) · [McKennon Law Group on *McIver v. MetLife* (9th Cir. 2024)](https://mslawllp.com/in-a-win-for-mckennon-law-group-pcs-client-the-ninth-circuit-rules-that-plan-fiduciaries-with-erisa-plan-eligibility-duties-are-liable-when-they-mistakenly-collect-insurance-premiums-for-ine/) · [BAS — DOL investigations: managing EOI](https://www.basusa.com/blog/u.s.-department-of-labor-investigations-managing-evidence-of-insurability-eoi-for-life-insurance-benefits)
- Payroll mechanics: [UC Davis — biweekly deductions holiday](https://financeandbusiness.ucdavis.edu/finance/payroll-services/ee-resources/benefits-hol) · [HRP — the extra biweekly payroll period in 2026](https://hrp.net/hrp-insights/how-an-extra-biweekly-payroll-period-in-2026-impacts-employee-benefits/) · [Newfront — final paycheck issues and Section 125 uniform intervals](https://www.newfront.com/blog/final-paycheck-issues-2)
- [KFF 2025 Employer Health Benefits Survey — summary of findings (PDF)](https://files.kff.org/attachment/Employer-Health-Benefits-Survey-2025-Annual-Survey-Summary-of-Findings.pdf)

**COBRA**
- [DOL — an employer's guide to COBRA (PDF)](https://www.dol.gov/sites/dolgov/files/ebsa/about-ebsa/our-activities/resource-center/publications/an-employers-guide-to-group-health-continuation-coverage-under-cobra.pdf) · [Chard Snyder — required COBRA notices and deadlines](https://www.chard-snyder.com/employers-and-advisors/compliance-watch/cobra-compliance-required-cobra-notices-and-deadlines/) · [29 CFR 2575.502c-1 — $110/day](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-XXV/subchapter-L/part-2575/section-2575.502c-1) · [Carlton Fields on *Marrow v. E.R. Carpenter*](https://www.carltonfields.com/insights/publications/2025/faulty-cobra-notices-can-cost-big-bucks) · [Jackson Lewis — COBRA notice litigation](https://www.jacksonlewis.com/insights/cobra-notice-litigation-cases-are-mushrooming-and-settlements-are-too)

**Leave**
- eCFR: [825.105 coverage](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-A/section-825.105) · [825.111 worksite/75 miles](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-A/section-825.111) · [825.200 leave-year methods](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-B/section-825.200) · [825.205 increments](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-B/section-825.205) · [825.300 notice cascade](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-D/section-825.300) · [825.302 employee notice](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-D/section-825.302) · [825.305 certification](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-D/section-825.305) · [825.500 recordkeeping](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-E/section-825.500) · [825.213 premium recovery](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-V/subchapter-C/part-825/subpart-B/section-825.213)
- [*Ragsdale v. Wolverine World Wide*, 535 U.S. 81 (2002)](https://supreme.justia.com/cases/federal/us/535/81) · [*Kemp v. Regeneron*, 2d Cir. Sept. 9, 2024](https://law.justia.com/cases/federal/appellate-courts/ca2/23-174/23-174-2024-09-09.html) · [DOL Opinion Letter release, Sept. 30, 2025](https://www.dol.gov/newsroom/releases/whd/whd20250930) · [DOL opinion letters, Jan. 5, 2026](https://www.dol.gov/newsroom/releases/whd/whd20260105) · [DOL FMLA enforcement data](https://www.dol.gov/agencies/whd/data/charts/fmla) · [DOL 2018 FMLA survey executive summary (PDF)](https://www.dol.gov/sites/dolgov/files/OASP/evaluation/pdf/WHD_FMLA2018SurveyResults_ExecutiveSummary_Aug2020.pdf)
- Washington HB 1213: [Ballard Spahr](https://www.ballardspahr.com/insights/alerts-and-articles/2026/01/significant-changes-to-washingtons-paid-family-medical-leave-act-impose-new-obligations-on-employers) · [Williams Kastner](https://www.williamskastner.com/news-insights/article/washington-paid-family-medical-leave-significant-changes-2026/) · State PFML 2026 rates: [WA ESD](https://esd.wa.gov/about-us/news-release/2025/paid-family-medical-leave-premium-rate-increases-113-2026) · [CO FAMLI](https://famli.colorado.gov/employers) · [MA](https://www.mass.gov/info-details/paid-family-and-medical-leave-employer-contribution-rates-and-calculator) · [OR small employers](https://paidleave.oregon.gov/employers/small-employers.html) · [MN small-employer premiums](https://mn.gov/uimn/employers/paid-leave/small-employer-premiums.jsp) · [Epstein Becker Green — 2026 leave law updates, seven states](https://www.ebglaw.com/insights/publications/2026-family-and-medical-leave-law-updates-what-employers-in-seven-states-need-to-know)
- [JAN — workplace accommodations: low cost, high impact (26,028 employers)](https://askjan.org/topics/costs.cfm) · [AbsenceSoft 2026 State of Leave and Accommodations Report](https://absencesoft.com/resources/absencesoft-2026-state-of-leave-and-accommodations-report-finds-leave-and-accommodation-requests-have-risen-for-a-third-year-in-a-row/) · [SHRM FMLA absence tracking spreadsheet](https://www.shrm.org/topics-tools/tools/forms/fmla-absence-tracking-calendar-spreadsheet) · [Stiira pricing ($9,950 entry)](https://www.stiira.com/pricing-for-stiira-leave-management-software/) · [TriNet to acquire Cocoon, April 9, 2026](https://www.prnewswire.com/news-releases/trinet-to-acquire-cocoon-expanding-leave-management-solutions-for-smbs-302738636.html)

**Filings, thresholds and records**
- [OSHA injury reporting / ITA FAQs](https://www.osha.gov/injuryreporting/faqs) · [29 CFR 1904.32 — posting and certification](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-XVII/part-1904/subpart-D/section-1904.32) · [29 CFR 1904.7 — recording criteria](https://www.ecfr.gov/current/title-29/subtitle-B/chapter-XVII/part-1904/subpart-C/section-1904.7)
- [EEOC — EEO data collections](https://www.eeoc.gov/data/eeo-data-collections) · [Federal Register — EEOC Removal of Reporting Requirements NPRM, July 23, 2026](https://www.federalregister.gov/documents/2026/07/23/2026-14937/removal-of-reporting-requirements) · [Littler on the rescission](https://www.littler.com/news-analysis/asap/eeoc-proposes-rescind-all-eeo-reporting-and-recordkeeping-requirements) · [Jackson Lewis — 2026 employee data reporting requirements](https://www.jacksonlewis.com/insights/2026-employee-data-reporting-requirements-are-employers-ready)
- [California CRD pay data reporting FAQs](https://calcivilrights.ca.gov/paydatareporting/faqs/) · [Amundsen Davis on SB 464 (mandatory penalties, 2026)](https://www.amundsendavislaw.com/labor-employment-law-update/sb-464-guide-californias-new-mandatory-pay-data-penalties-for-2026) · [Illinois EPRC FAQs](https://labor.illinois.gov/laws-rules/conmed/eprc-faqs.html) · [DOL VETS-4212](https://www.dol.gov/agencies/vets/programs/vets4212)
- [Newfront — Form 5500 small plan exemption and the wrap-plan trap](https://www.newfront.com/blog/form-5500-small-plan-exemption-2) · [Newfront — Form 5500 participant count change](https://www.newfront.com/blog/form-5500-updates-participant-count-win-and-large-plan-filer-warning) · [DOL EBSA DFVCP fact sheet (PDF)](https://www.dol.gov/sites/dolgov/files/EBSA/about-ebsa/our-activities/resource-center/fact-sheets/delinquent-filer-voluntary-compliance-program-fact-sheet.pdf)
- [California DLSE — right to inspect personnel files](https://www.dir.ca.gov/dlse/FAQ_RightToInspectPersonnelFiles.htm) · [California DLSE — paydays and final pay](https://www.dir.ca.gov/dlse/faq_paydays.htm) · [EEOC recordkeeping requirements](https://www.eeoc.gov/employers/recordkeeping-requirements) · [DOL WHD Fact Sheet 21 — FLSA recordkeeping](https://www.dol.gov/agencies/whd/fact-sheets/21-flsa-recordkeeping)
- [NASWA UI SIDES](https://www.naswa.org/uisides) · [California EDD — responding to UI claim notices](https://www.edd.ca.gov/en/unemployment/responding_to_ui_claim_notices/) · [Littler — the federal UI Integrity Act](https://littler.com/publication-press/publication/federal-unemployment-insurance-integrity-act-creates-tough-new) · [ACF — new hire reporting FAQs (20-day rule)](https://acf.gov/css/faq/new-hire-reporting-answers-employer-questions) · [Betterment at Work — 50-state guide to state-mandated retirement plans](https://www.betterment.com/work/resources/guide-to-state-mandated-retirement-plans)

**Software landscape**
- Vendor pricing (primary): [Gusto](https://gusto.com/product/pricing) · [BambooHR](https://www.bamboohr.com/pricing/) · [Rippling](https://www.rippling.com/pricing) · [Justworks](https://www.justworks.com/pricing) · [Employee Navigator](https://www.employeenavigator.com/pricing/) · [Ease](https://www.ease.com/pricing/) · [Gusto API help — no customer API](https://support.gusto.com/article/106622056100000/gusto-api-integrations) · [Finch on Paycom — no API](https://www.tryfinch.com/integrations/paycom) · [Paylocity developer FAQ](https://developer.paylocity.com/integrations/docs/integrations-faq)
- [Employee Navigator announces acquisition of Ease](https://www.employeenavigator.com/employee-navigator-announces-acquisition-of-ease/) · Reviewer complaints: [BambooHR/Capterra](https://www.capterra.com/p/110968/BambooHR/reviews/) · [Paylocity/TrustRadius](https://www.trustradius.com/products/paylocity/reviews?f=cons) · [Namely/TrustRadius](https://www.trustradius.com/products/namely/reviews?f=cons) · [Paycom/TrustRadius](https://www.trustradius.com/products/paycom/reviews?f=cons) · [TriNet/TrustRadius](https://www.trustradius.com/products/trinet/reviews?f=cons) · [Justworks/TrustRadius](https://www.trustradius.com/products/justworks/reviews?f=cons)
- [HR.com State of Today's HR Tech Stack and Integrations 2024 (PDF)](https://eightfold.ai/wp-content/uploads/State-of-Todays-HR-Tech-Stack-and-Integrations-2024-Research-Report.pdf) · [Sapient Insights HR Systems Survey via HR Executive](https://hrexecutive.com/what-are-the-top-findings-from-sapients-hr-systems-survey/) · [OrgChart State of Workforce Planning 2026](https://theorgchart.com/resources/workforce-planning-gaps-manual-org-charts/) · [Aeqium state of compensation review management](https://www.aeqium.com/resources/state-of-compensation-review-management) · [Lattice — transitioning off a PEO](https://lattice.com/articles/peo-transition)

**Market context**
- [SHRM — how many HR staff members is best](https://www.shrm.org/topics-tools/news/talent-acquisition/how-many-hr-staff-members-is-best-shrm) · [NSBA 2025 Small Business Regulations Survey](https://www.prnewswire.com/news-releases/new-survey-regulatory-complexity-stymies-job-creation-and-business-growth-302516686.html) · [U.S. Chamber Small Business Index Q4 2024](https://www.uschamber.com/small-business/small-businesses-are-spending-more-time-money-on-regulatory-compliance) · [Payroll Integrations / Dynata survey, Sept 2024](https://www.businesswire.com/news/home/20240919989299/en/73-of-Employees-Want-More-Education-on-Company-Benefits-Employers-HR-Administrative-Burdens-Are-Getting-in-the-Way) · [Panko — human error rates](https://panko.shidler.hawaii.edu/HumanErr/Basic.htm)
- Live role scope: [HR Generalist, VetEvolve (remote, posted Aug 6, 2026, $60,000–$80,000)](https://to.indeed.com/aaf9nssc4vtf)

### Strong inferences — reasoned from verified facts, not directly stated by any source

1. **The 20–200 band is structurally the worst-served zone, by vendor design.** ADP splits RUN (1–49) from Workforce Now (50+); Paycor publishes tiers only under 50; BambooHR sets a $250/month floor at 25 employees; PEOs re-tier at 25, 50 and 100; PEO exit typically occurs at 50–100. A company growing from 20 to 200 crosses at least one forced migration inside almost every vendor's product architecture.
2. **The default architecture for this market is file-in/file-out, and that is a feature.** It follows directly from Gusto and Paycom having no customer API, Paylocity's being gated and priced, and benefits data living in a broker-owned system. Tools that require integrations cannot serve this segment at a price it will pay.
3. **"Custom reports" is systematically monetized, which is why HR runs on Excel.** Gusto puts custom reports at ~3.7× its entry PEPM; BambooHR puts advanced analytics at its top tier. Combined with the near-universal "cannot cross-tabulate" complaint, exporting to Excel is the rational response to a deliberately upsold feature, not a failure of adoption.
4. **The termination-to-carrier gap is governed by two conflicting rules and small employers live in the space between them.** Carriers permit ~60-day retroactive terminations with net credits; 45 CFR 147.128 generally prohibits retroactive cancellation. The conflict is only expensive when claims were incurred in the phantom-coverage window.
5. **Welfare-plan Form 5500 non-filing is probably the most common undetected failure in the segment.** The wrap-plan aggregation trigger is usually employer-paid basic life covering all employees, not medical enrollment, and no third party's workflow surfaces it. DFVCP's very low caps ($750/$1,500) are indirect evidence that DOL expects widespread delinquency.
6. **The March 2026 I-9 reclassification is retroactive in practical effect.** ICE changed how it classifies errors on inspection, not what the law required at completion. Every I-9 already in a cabinet with a missing employer title, missing first-day-of-employment or missing date of birth was curable in February 2026 and is fineable now. This makes a self-audit conducted *before* an NOI arrives worth vastly more than one conducted after.
7. **Small-employer PFML exemptions exempt the premium, not the administration.** A 40-person company with employees in Washington, Colorado and Minnesota pays little or no employer premium in any of the three, yet must register with three agencies, file three quarterly returns, issue three sets of notices on different schedules, and reconcile three job-protection clocks against FMLA. **Compliance burden is essentially uncorrelated with dollar cost** — which is precisely the asymmetry that makes it a software problem rather than a budgeting problem.
8. **Broker-owned benefits technology creates a switching trap in a market that changes brokers regularly.** Follows from Ease and Employee Navigator licensing to brokers rather than employers. Not stated by any source; should be confirmed in interviews.
9. **Payroll-to-401(k)-recordkeeper drift is the most expensive form of data drift in the segment**, because six of ten documented 401(k) operational failures trace to payroll data disagreeing with plan records — and those convert into qualification failures requiring EPCRS correction, not mere annoyance.

### Tentative hypotheses requiring practitioner validation

1. **That small employers touch 3–6 carrier portals.** Derived from carrier-line structure, not measured. No survey found.
2. **That carrier invoices are obtainable as structured data.** The gating assumption for C3. Unknown.
3. **That vendor-produced 1095-C files contain material error rates.** The gating assumption for C2. Asserted by specialist firms that sell remediation; not independently measured.
4. **That the employer, not the broker, is the buyer for the reconciliation tools.** If brokers perform this work as a retention service, the customer is the brokerage — a different and possibly better go-to-market.
5. **That the majority of 20–200 employee companies use spreadsheets for FMLA and accommodation tracking.** Measured only at 500+ employees (41–43%). The sub-200 rate is unmeasured and probably higher.
6. **That employers will act on I-9 self-audit findings rather than preferring not to know.** A documented but unremediated self-audit may be worse than none, and counsel may advise running it only under privilege.
7. **The "5% of premium spend is inaccurate" figure.** Appears in at least two independent vendor sources with no published methodology anywhere; it may all trace to a single origin. Not used to justify any opportunity in this report.
8. **SIDES E-Response adoption rates by employer size.** No data. Its correctness for this segment is inferred from its own design threshold (>30 requests/week for full SIDES).
9. **The 2018 carrier EDI minimum group size table.** Directionally corroborated by three current vendor sources, but the specific per-carrier numbers are eight years old and vendor-hosted. Spot-verify before republishing.
10. **Any hours-per-leave-case or dollars-per-leave-case figure.** The entire genre is vendor-produced with undisclosed methodology. No peer-reviewed, government or independent source exists.

### A note on evidence hygiene in this market

This research encountered a pattern worth recording for future cycles: **vendor-published compliance guidance in the HR space is measurably unreliable, and that unreliability is itself part of the burden the target user carries.** Two separate vendors published mislabeled ACA penalty years (2024 amounts presented as 2025; a calendar-2026 figure presented as applying to tax year 2025); one published I-9 penalty figures matching neither the current eCFR text nor the 2025 adjustment rule; one page contradicted itself on hours spent per week within the same article; a widely cited "76% of I-9s contain errors" statistic has no locatable primary source; and a benefits-billing press release's own arithmetic ($200M across 110,000 employees) is irreconcilable with the same industry's "5% of spend" rule of thumb by a factor of three. A one-person HR team researching any of these questions will encounter contradictory numbers within the first page of results. That is a reason a free, cited, versioned ruleset has value beyond the software wrapped around it — and it is the strongest argument in this report for the open-source model specifically.
