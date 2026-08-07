# Staffing and Recruiting Agency Operations — Back Office

**Market:** Staffing and recruiting agency operations
**Angle:** back-office
**Claim ID:** `1c4aa110`
**Date:** 2026-08-07

---

## 0. Cycle header

### Why this assignment

At claim time the ledger held **17 completed reports, 277 backlog assignments, and 140 markets with zero completed coverage**. There were no live claims, so the whole backlog was available.

Selection reasoning, against the stated preference order:

**(a) Breadth over depth.** The completed set is heavily concentrated in three clusters: AEC/design-and-construction (fire protection design, MEP/HVAC design, land surveying, geotechnical labs, construction submittal coordination), insurance/claims/title (agency back office, IA adjusting, title & escrow), and money-movement (medical billing, bookkeeping, freight brokerage, motor carrier settlement). **Staffing and recruiting is an entirely untouched vertical** — no adjacent market in the completed set shares its workflows, its counterparties, or its software vendors. It is also very large: ASA counts roughly **27,000 US staffing and recruiting companies operating close to 54,000 offices**, with **~2.2 million temporary and contract employees working in an average week in 2024** and **12.7 million hired during 2023** ([ASA staffing industry statistics](https://americanstaffing.net/research/fact-sheets-analysis-staffing-industry-trends/staffing-industry-statistics/)).

**(b) Expected strength of evidence.** Staffing back office generates unusually good public artifacts: SEC-filed factoring agreements, published buyer invoice-rejection code sets, VMS supplier job aids from SAP and Beeline, Joint Commission certification measure definitions, and a dense body of named-reviewer software criticism on Capterra/G2/SoftwareAdvice. That expectation held (see §8), with one significant miss noted there.

**(c) Angle diversity.** Completed angles skew to `core-practitioner-workflow` (7 of 17). `back-office` had only 3. For staffing specifically, the back office is also the more differentiated target: the front office (sourcing, screening, submitting) is crowded with ATS vendors and AI resume tooling, while pay/bill, compliance and cash are where small agencies still run on Excel.

**Assignments remaining in the backlog after this cycle:** see §9 (276 at claim, adjusted by discoveries appended in §7).

### Scope boundary

This report covers agencies that place **W-2 temporary and contract workers** — the population where a back office exists at all. Pure perm/contingent-search firms (fee on placement, no payroll) are treated only where their commission and fall-off mechanics overlap. The target organization is **5–150 internal staff**, carrying anywhere from 50 to 3,000 field employees.

---

## 1. Market examined

### Industry and segment

**NAICS 5613 — Employment Services**, principally 561320 (Temporary Help Services) and 561311/561312 (Employment Placement Agencies / Executive Search). The economically meaningful sub-segments by occupational mix ([ASA](https://americanstaffing.net/research/fact-sheets-analysis-staffing-industry-trends/staffing-industry-statistics/)):

| Segment | Share of staffing employment | Back-office character |
|---|---|---|
| Industrial / light industrial | 36% | Highest volume, highest turnover, worst SUTA and workers' comp exposure, OSHA joint responsibility |
| Office-clerical and administrative | 24% | Moderate volume, simplest compliance |
| Professional-managerial | 21% | Lower volume, higher rates, heavy VMS/MSP exposure |
| Engineering, IT, scientific | 11% | Longest assignments, most VMS-mediated, highest bill rates |
| Health care | 8% | Smallest headcount share, **by far the heaviest compliance load** — credentialing, per diem, Joint Commission |

### The professionals doing this work

The back office at a firm of this size is one to five people wearing overlapping hats. Titles observed in real postings and org descriptions:

- **Payroll & Billing Specialist / Revenue Specialist** — the core role. At Insight Global the VMS-facing version is titled **Revenue Specialist, VMS** and is explicitly responsible for "collecting and confirming consultant customer approved timesheets **against what has been reported**," registering workers in the VMS, generating invoices, running monthly audits of hours and bill rates, and "recognizing timesheet dispute deadlines and escalating" ([posting](https://www.themuse.com/jobs/insightglobal/revenue-specialist-vms)). Required skill listed: **Excel**.
- **A/R Billing Specialist** — invoicing, billing-profile setup for new contractors, rate documentation collection, collections against a monthly cash goal, **"unapplied cash reconciliation if the customer payment does not provide invoice details,"** customized aging and unbilled reports, credit memo documentation ([posting](https://www.themuse.com/jobs/insightglobal/ar-billing-specialist-a39d1f)). Escalates to Sales **and to a separate "Timesheet Verification team."**
- **Credentialing & Onboarding Coordinator** — in healthcare staffing this is a dedicated FTE. A Texas Nursing Services posting (Plano/Frisco TX, **$22–28/hr, $45,000–$58,000/yr**, posted 2026-01-14) defines it as "a compliance and operations role, not a recruiting or sales position," with duties: verify license status and **track expiration dates**, proactively manage renewals and missing documentation, maintain **audit-ready** credential files, ensure onboarding requirements are met **prior to submission or scheduling**, and **"generate compliance reports and credential rosters as needed"** ([posting](https://to.indeed.com/aayhk7c9kvjk)). Systems familiarity is listed as *preferred, not required*.
- **Controller / Office Manager / owner** — at under ~30 internal staff, one person owns pricing, burden, factoring relationship, commissions, and the tax calendar.

### Organization size most likely to benefit

The sweet spot is **$2M–$60M in annual billings, 5–50 internal staff**. Below ~$2M the firm is still running on a general ledger and a spreadsheet and may not yet feel the pain; above ~$60M it is more likely to have bought an integrated middle/back-office suite and staffed a finance team. A back-office provider aimed at firms **under $2M** describes the inflection point precisely: hours tracking is fine at 3 contractors, but *"when you have thirty, it becomes a full-time job that is prone to human error"* ([USA Staffing Services](https://www.usastaffingservices.com/how-to-avoid-the-biggest-back-office-pitfalls-when-scaling-under-2m/)) — *vendor source, but the threshold matches the job-posting evidence above*.

### The user of a tool

Not a developer, not an accountant by training in most cases. Comfortable in Excel to the level of VLOOKUP and pivot tables. Works under a hard weekly clock. Will not adopt anything requiring an implementation project.

---

## 2. How the work is performed

The staffing back office is one weekly loop with four monthly/quarterly/annual loops hanging off it.

### 2.1 The weekly loop (the spine)

**Sunday — period ends.** Most agencies run a Sun–Sat pay week.

**Monday/Tuesday — time capture and chase.** Hours arrive through four incompatible channels, often simultaneously for the same agency:

1. **Agency's own time system** (Bullhorn Time & Expense / Peoplenet, TempWorks, Avionté). The operational reality is documented in TalentLaunch's internal FAQ for its operating companies: worker submission reminders fire **Friday 5:00 p.m. and Monday 8:00 a.m. ET**; **approver** reminders fire **Monday, Tuesday, and Wednesday mornings**; pay files run on a staggered Mon–Fri schedule at 8am/11am/1pm/3pm, and time approved after that day's file waits for the next business day. Account managers are told to monitor an "unsubmitted time" tab and an "unapproved time" tab **daily** and trigger reminders manually ([TalentLaunch BH T&E FAQ](https://support.mytalentlaunch.com/support/solutions/articles/8000004425-bullhorn-time-expense-operating-companies-faq)). *Three separate nag cycles is the designed-for normal — approvals routinely slip three days past period end.*
2. **Paper and photographs of paper.** Agencies still publish signable PDF timesheets returned by email or fax (e.g. [MSG Staffing](https://msgstaffing.com/wp-content/uploads/2020/03/MSG-Staffing-Time-Sheet-9-17.pdf), [Superior Staffing](http://www.superiorstaffing.com/timesheets.html)). Marketplace platforms formally support **photographed paper timesheets** as a fallback ([Clipboard Health worker instructions](https://workers.clipboardhealth.com/hc/en-us/articles/29559872022935-How-do-I-submit-a-paper-timesheet)).
3. **Client punch systems** — the worker clocks into the client's Kronos/UKG or badge system and the agency receives an export.
4. **VMS portals** — the client's Fieldglass/Beeline/Coupa instance is the system of record.

**Tuesday — payroll.** Gross-to-net for the field population across every state where work was performed, with per-jurisdiction OT rules, sick-leave accrual, garnishments, per diem splits, and multi-state withholding.

**Tuesday/Wednesday — reconciliation and billing.** The two datasets must agree before an invoice exists. Where a VMS is involved, **the agency does not control its own invoice**: SAP's supplier documentation states plainly that *"Supplier invoices are automatically created in SAP Fieldglass when items are approved"* and that a **self-billing document** is generated automatically for approved timesheets, expenses and milestones, with **"no paper invoices and no invoices need to be created on ARIBA for orders created on SAP Fieldglass"** ([SAP Fieldglass supplier FAQ](https://assets.cdn.sap.com/agreements/supplier-portal/fieldglass-supplier-enablement/sap-suppliers-faqs-englishglobal.pdf)). The agency's own computed rates and hours become a *reconciliation target*, not a source of truth.

**Wednesday/Thursday — invoice delivery.** Into the client's AP channel: emailed PDF, Ariba Network, Tungsten, Coupa, Taulia, or a client-specific portal, each with its own format rules.

**Ongoing — cash application and collections.** Remittance advice frequently references the **VMS's** invoice number rather than the agency's — Beeline's own supplier job aid exists specifically to bridge "IQN invoice number" to "supplier internal reference number," and notes that **you must export to Excel to see the supplier reference fields at all** ([Beeline Supplier Organization Invoice Reconciliation Report job aid](https://webapps.beeline.com/beelinetms/!_IQN_ShellJobAids/SupplierOrganizationInvoiceReconciliationReport-SupplierJobAid.pdf)).

**Continuously — funding.** Payroll clears weekly; cash arrives on ~60-day terms. Kelly Services reported **global DSO of 59 days** at both Q2 2025 and year-end 2024 on $1.2B of trade AR ([Kelly Services Form 10-Q, 2025-08-07](https://ir.kellyservices.com/static-files/8f1ca1d3-9a9a-490d-ac52-134fc8582a83)). A large, sophisticated firm with an MSP-heavy book runs 59 days; an SMB agency with worse tooling should be assumed no better. The gap is bridged by invoice factoring, which most agencies of this size use.

### 2.2 The per-assignment loop

Every new placement re-triggers a set of obligations that general-purpose HR and payroll platforms treat as one-time employee-master events:

- **Workers' comp class code.** Under NCCI-style Rule 1, leased workers "must be classified the same as direct employees of the client performing the same or similar duties"; temp labor services qualify for **multiple basic classifications** but must keep **separate payroll records per code** ([NCRB Basic Manual Rule 1](https://www.ncrb.org/digitallibrary/basicmanual/Rule_1_-_Assignment_of_Classifications.htm)).
- **State/local new-hire notices.** California Labor Code **§2810.5(a)(3)** requires temporary services employers to additionally disclose *the name, physical address of main office, mailing address and telephone number of the legal entity for whom the employee will perform work* — a client-specific notice regenerated per assignment — and §2810.5(b) requires written notice of any change **within seven calendar days** ([statute text](https://codes.findlaw.com/ca/labor-code/lab-sect-2810-5/), [DLSE form](https://www.dir.ca.gov/dlse/lc_2810.5_notice.pdf)). New York publishes a **dedicated temp-help form, LS 51**, and requires it in English **and** the employee's primary language where DOL offers a translation ([NY DOL](https://dol.ny.gov/notice-pay-rate)).
- **Credential and eligibility check** against both statutory and *customer* requirements (§2.3).
- **Rate card application** — bill rate, markup, OT/DT multipliers, shift differentials, per diem split, MSP fee deduction.

### 2.3 The credential loop (healthcare and light industrial)

This is where the strongest regulatory hook in the whole market sits. Joint Commission-certified healthcare staffing firms must report **standardized performance measures**, two of which are literally document-completeness measures:

- **HCSS-6, "Completeness of Personnel File – Per Diem"** ([measure definition](https://manual.jointcommission.org/releases/HCSS2026A/MIF0125.html))
- **HCSS-7, "Completeness of Personnel File – Travel"** ([measure definition](https://manual.jointcommission.org/releases/HCSS2026B/MIF1358.html))

Numerator: placements whose personnel file contains **all three** of (1) job-appropriate credentials, (2) current competency evidence, (3) background check. Denominator: all clinical placements of that type completed in the month. **Quarterly reporting no later than 45 days after quarter end is a condition of maintaining certification, with monthly numerator and denominator values submitted** ([HCSS introduction](https://manual.jointcommission.org/releases/HCSS2026B/IntroductionHCSS.html)). The "Competency" data element is abstracted **"N" if documentation is missing, expired, or competency cannot be verified** ([data element definition](https://manual.jointcommission.org/releases/HCSS2026A/DataElem0179.html)) — **expired scores identically to absent**. Firms are stratified into Groups 1–4 by annual clinical placements starting at **<40**, so very small firms are in scope.

On-site, reviewers work a standardized **Personnel File Review Checklist** covering primary-source-verified licensure required by state, the firm, **or the customer**; initial and ongoing competency evaluation; CPR; TB test; MMR; flu immunization **or declination**; Hep B status; drug screen; criminal background per law **and customer requirements** — sampling a **minimum of 20 clinical personnel files per review day**, with recertification carrying only **7 days' advance notice** plus a mandatory one-year intra-cycle evaluation ([HCSS Certification Review Process Guide 2026](https://digitalassets.jointcommission.org/api/public/content/98126fe27d044380ac507cbc816413d1?v=0b97856f)).

Light industrial has a parallel, less formalized load. OSHA's **Temporary Worker Initiative** holds the staffing agency and host **jointly responsible**, states that **"staffing agencies have a duty to inquire into the conditions of their workers' assigned workplaces,"** and has issued **15 bulletins** spanning PPE, hazard communication, powered industrial truck (forklift) training, respiratory protection, lockout/tagout, heat, and warehousing ([OSHA TWI](https://www.osha.gov/temporaryworkers), [TWI Bulletin No. 1](https://www.osha.gov/sites/default/files/OSHA_TWI_Bulletin.pdf)).

### 2.4 The periodic loops

- **Monthly/quarterly:** ACA measurement-period tracking and offer deadlines; multi-state tax deposits and returns; commission calculation.
- **Annual:** 1094-C/1095-C filing; W-2s; workers' comp premium audit; SUTA rate notices; policy renewal.
- **Event-driven:** unemployment claim responses (most states require reply in **10–14 days**), I-9 audits, client AP audits, factor field exams.

### 2.5 Software actually in use

| Layer | Typical SMB choice | Notes |
|---|---|---|
| ATS/CRM | Bullhorn, Crelate, Avionté, TempWorks, Tracker, JobDiva, COATS | Bullhorn publishes SMB pricing at **$99–$165/user/mo**, but states on the same page that **back office, Time & Expense and payroll are optional add-ons "priced separately"** ([Bullhorn small-agency pricing](https://www.bullhorn.com/small-agency-software/pricing/)) |
| Time | Bullhorn T&E (Peoplenet), TempWorks, client punch, paper | See §2.1 |
| Payroll | The ATS vendor's module, or ADP/Paychex/Gusto alongside | |
| Billing/AR | The ATS vendor's module, or QuickBooks, **plus Excel** | |
| Funding | Advance Partners, Madison Resources, Signature, PRN Funding | Factoring fees commonly quoted at **1–5% of invoice value** ([Signature Back Office](https://signaturebackoffice.com/factoring-for-staffing-firms/), [Madison Resources FAQ](https://madisonresources.com/payroll-funding-and-back-office-support-faqs/)) |
| Everything the above cannot do | **Excel** | |

The "everything Excel" row is not an assumption. Named practitioner reviewers describe the specific holes that push work out:

- **Linda F., Director of Administration, Staffing & Recruiting, 2+ years on Avionté:** *"A/R Module does not allow users to create an invoice with multiple line items or adding free text comments"*; *"Payroll does not allow use of a negative deduction to refund something withheld"* ([Capterra](https://www.capterra.com/p/76635/Avionte-for-Staffing-Firms/reviews/)).
- **Misty R., HR Administrator:** *"Unemployment Module—completely barebones, only 2 reports exist when this type of reporting is crucial"*; *"Employee documents can be a mess when the employee is longstanding or has had multiple jobs"*; and on ACA, her firm was left *"scrambling to manually code our 1095's"* ([Capterra](https://www.capterra.com/p/76635/Avionte-for-Staffing-Firms/reviews/), [G2](https://www.g2.com/products/avionte-avionte/reviews)).
- **Janell O., Director of Corporate Services (<6 months in):** *"We are 2+ months post conversion and still don't have ACA reporting capabilities"*; *"Our data is so out of whack."*
- **Nick H., Senior Operations Analyst (TempWorks):** wants the system to *"automatically identify and flag pay rates that are below certain local minimum wage thresholds"* — i.e. nothing catches a rate that has become illegal under a new local ordinance.
- **Jerod S. (TempWorks):** *"The billing process feels somewhat counterintuitive, making it difficult to reconcile invoices from different sources."*
- **Jaime D., CFO (TempWorks):** *"We must custom-build some of the more complex reports we require."*
- **Melinda M. (Avionté, Enterprise):** *"details that are required for tax setup and reporting are not required fields when setting up the employee"* — the system will happily create a billable record missing a determinant field.

Two structural notes. First, Avionté's own back-office investment went **up-market** — its June 2024 standalone back-office launch was aimed at *enterprise* staffing agencies ([Businesswire](https://www.businesswire.com/news/home/20240611850151/en/Aviont-Introduces-Standalone-Back-Office-Solution-for-Enterprise-Staffing-Agencies)). Second, historical back-office data is an explicit migration upsell: Tracker's implementation tiers put **timesheets, invoices and shifts only in the Enterprise onboarding tier**, with direct imports at **$250/file** ([Tracker implementation](https://www.tracker-rms.com/implementation/)). Both facts push the 5–150 segment toward keeping a parallel spreadsheet layer permanently.

---

## 3. Most important problems, ranked

### P1 — Mispricing at quote time: the burden stack is not in the calculator

**Who:** Owner, branch manager, salesperson quoting a new req or a renewal.
**When:** Every new client, every rate negotiation, every OT-heavy assignment, every VMS program bid.
**How handled now:** A markup percentage applied to pay rate, often a house-standard markup applied uniformly.
**Why inadequate:** The markup-versus-margin confusion is arithmetic, not opinion. A worked example: bill $40.00, pay $28.00, burden $5.50 → **gross margin 16.25% while markup is 42.86%** ([USA Staffing Services](https://www.usastaffingservices.com/staffing-agency-gross-margin/)). An owner who "prices at 40% markup" believing that is a 40% margin is off by roughly 24 points. Beyond that headline error, at least six real cost components are routinely omitted:

1. **FUTA front-loading.** FUTA is ~0.6% net on the **first $7,000 per worker** ([USA Staffing Services](https://www.usastaffingservices.com/staffing-agency-payroll-tax-burden/)). On a high-turnover light-industrial book, that is a large, seasonally front-loaded cost per *worker*, not per hour — the effective burden on Q1 hours is materially higher than the annual average the pricing sheet uses.
2. **SUTA, which hits staffing differently than anyone else.** Because temp workers churn before reaching the taxable wage ceiling, agencies "pay unemployment taxes on virtually every dollar earned," making the *rate* dominant rather than the wage base ([Madison Resources](https://madisonresources.com/why-suta-rates-hurt-low-skilled-staffing-agencies/) — vendor, but the mechanic is arithmetically sound and is the single largest cost driver in this category). Rates are experience-rated and change annually **after** contracts are priced.
3. **Workers' comp by class code** — which varies enormously by code (see P2).
4. **MSP/VMS program fee**, typically deducted from the bill rate rather than added to it — a documented 5% fee turns a $90/hr bill into **$85.50 received** ([Vars Health](https://www.varshealth.com/post/understanding-msp-fees-in-healthcare-staffing-and-their-market-impact)).
5. **Overtime margin dilution.** Pay OT at 1.5× pay rate, bill OT at 1.5× bill rate, and the *dollar* margin scales but the *percentage* margin on the OT hour is unchanged while the burden components that are percentage-of-wage (FICA, WC) scale with the higher wage — the effect on blended margin depends on OT mix, which nobody models at quote time.
6. **Cost of capital at actual DSO, not contractual terms.** A "Net 60" VMS program routinely runs Net 70+ because approval cutoffs extend the clock before the invoice even exists ([Madison Resources](https://madisonresources.com/vms-software-for-staffing-firms-what-actually-matters-when-youre-the-supplier/)). At a 3% factoring fee, thirty extra days is real money.

**Frequency:** Every quote. For an active agency, weekly to daily.
**Cost:** Staffing gross margins average about **25% for temp staffing**, ranging roughly **14–41%**, with markups **20–75%** ([Advance Partners, citing SIA](https://www.advancepartners.com/calculate-how-to-price-your-staffing-services/)). Industrial averages ~18%, and "below 18% = competing on price with no buffer." A two-point pricing error on a $40 bill rate across a 2,000-hour assignment is **$1,600 of margin per placement, permanently**, because the rate is locked for the contract term. Madison Resources' conclusion is the sharpest statement of the problem: *"Firms that price work inside VMS programs at their standard markup are usually funding the difference themselves without realizing it."*
**Evidence quality:** Strong on mechanism, medium on magnitude (the segment margin figures come via vendors citing SIA).

### P2 — Workers' comp class code assignment and payroll-by-code recordkeeping

**Who:** Owner/controller at placement time; the carrier's auditor at renewal.
**When:** At every placement (code assignment) and annually (premium audit).
**How handled now:** The code the client suggests, or the code that was used last time for "something similar," recorded in a field the payroll system does not segregate cleanly.
**Why inadequate:** The classification obligation belongs to the **staffing agency**, not the host, and the per-$100-of-payroll spread between codes is enormous. From a broker paper distributed by the **Midwest Staffing Association** ([PDF](https://msastaffing.org/wp-content/uploads/2024/09/Staffing-Company-Class-Codes-A-Shot-in-the-Dark-RS.pdf)):

| Case | Error | Outcome |
|---|---|---|
| CA warehouse | Coded 3681 electronics (~$2.00/$100) instead of 8292 general warehousing (~$11.50/$100) | **$80,000** back-premium demand; business closed |
| TX welding | Coded 8810 office clerical instead of welding | Mid-term reclassification; business closed |
| Medical staffing, $50M payroll | Assisted-living staff coded 8833 instead of 8824 | **$620,000** premium adjustment ≈ **35% of net profit** |

The damage compounds: a code that cannot absorb the actual losses per $100 of payroll drives the **experience mod up**, and the mod applies company-wide. Underwriter pre-approval of host-employer details is expected **within 24 hours before placement** — a real-time operational task, not an annual one. Pay-as-you-go does not remove the audit; it still verifies reported payroll and catches "unreported changes in employee classifications" ([Insurepay](https://insurepay.com/blog/the-role-of-estimates-and-audits-in-pay-as-you-go-workers-comp/) — vendor).

**Frequency:** Every placement; audited annually.
**Cost:** The three documented cases run $80k, business-ending, and $620k. Even in the ordinary case, a single miscoded crew of ten at a $9/\$100 spread on $400k of annual payroll is **$36,000/yr**.
**Evidence quality:** Strong. Rating-bureau rule is primary; the case studies are broker-authored but association-distributed and internally consistent.

### P3 — VMS/self-billing reconciliation

**Who:** Payroll & billing specialist, revenue specialist.
**When:** Every billing cycle for every VMS-mediated client.
**How handled now:** Export the VMS report to Excel, export the agency's own hours to Excel, sort both, eyeball or VLOOKUP, chase the differences.
**Why inadequate:** Five recurring discrepancy classes are well characterized — rate discrepancies (VMS bill rate ≠ contracted rate), hours mismatches (split shifts, rounding), missing entries (hours never appear because approval was skipped), duplicate entries (same hours under different cost codes), and **period boundary issues** (weekly payroll against semi-monthly or calendar-month VMS billing) ([invoicedataextraction.com](https://invoicedataextraction.com/blog/staffing-agency-invoice-processing) — vendor, but the taxonomy matches the primary VMS documentation). The format varies **"not only between VMS providers but between client configurations within the same platform"** — corroborated by Beeline's own job aid, which notes some fields are "not a required entry for IQNavigator, but required for the Shell process."

Two structural facts make this permanent rather than fixable by better data entry. First, self-billing means the agency's numbers are the *challenger*, not the record ([SAP Fieldglass FAQ](https://assets.cdn.sap.com/agreements/supplier-portal/fieldglass-supplier-enablement/sap-suppliers-faqs-englishglobal.pdf)). Second, the period boundary mismatch is a calendar fact — a Sun–Sat payroll week against a calendar-month billing period guarantees a partial-period allocation every single month.

**Frequency:** Weekly to monthly per client, forever.
**Cost:** The best-known published figures are vendor-authored and should be treated as directional, not measured: **>5% of total billable revenue** lost annually to preventable billing errors, **20–40 basis points** of margin erosion per account, and **+7 to +14 days DSO** from invoice disputes ([SIA *Staffing Stream*, authored by the CFO of Hercules](https://www.staffingindustry.com/editorial/staffing-stream/revenue-leakage-the-silent-threat-to-staffing-firm-margins)). The most defensible evidence that this is real and expensive is not a statistic at all — it is that a venture-backed product category exists solely to reconcile VMS billing for healthcare staffing, and was acquired: **LaborEdge acquired Reconciled** in 2025, with the target's own site quoting an unnamed **CFO of a $75M-AR locums firm**: *"After 20 years, it's exciting that someone has a solution for this issue!"* ([EIN Presswire](https://www.einpresswire.com/article/908787891/laboredge-acquires-reconciled-eliminating-revenue-leakage-and-manual-vms-billing-burden-for-staffing-agencies), [SIA](https://www.staffingindustry.com/news/global-daily-news/laboredge-acquires-reconciled)).
**Evidence quality:** Mechanism — strong (SAP and Beeline primary docs). Magnitude — weak; every quantified error rate traces to a vendor. **That absence of independent benchmarking is itself a finding.**

### P4 — Credential expiry and per-facility eligibility

**Who:** Credentialing coordinator, recruiter, account manager, and ultimately the client's compliance officer.
**When:** Continuously; acutely at submission and at shift start.
**How handled now:** Spreadsheets and calendar reminders, plus document folders in the ATS. The strongest available evidence for the current state is indirect but consistent: a dedicated **$45–58k FTE** whose job description asks them to *"track expiration dates"* and *"generate compliance reports and credential rosters as needed"* — you generate a roster when the system does not hold one — and lists systems familiarity as *preferred, not required* ([posting](https://to.indeed.com/aayhk7c9kvjk)). Add the Avionté reviewer's *"employee documents can be a mess when the employee is longstanding or has had multiple jobs."*
**Why inadequate:** Requirements are the union of statutory, firm, and **customer-specific** rules, each with its own expiry clock, and the customer's set changes per facility. Joint Commission scores expired identically to missing (§2.3). Timelines are long and serial: healthcare onboarding runs **one to four weeks**, with employment work-history verification alone taking *"three days or two full weeks, depending on how quickly employers respond"* ([Intuitive Health Services](https://intuitivehealthservices.com/blog/healthcare-staffing-agency-onboarding-process/)).
**Frequency:** Every worker, every credential, every assignment.
**Cost:** A worker pulled mid-shift for an expired license is an immediate revenue loss plus a client-relationship event — *"a nurse removed mid-shift due to an expired license leaves gaps that jeopardize patient care and team morale"* ([Gotham Companies](https://www.gothamcompanies.com/2025/07/02/navigating-compliance-credentialing-in-healthcare-staffing/)). Placing someone on the **HHS OIG exclusion list** exposes the facility to substantial fines, and exclusion monitoring is an ongoing obligation, not a one-time check — nurses are *"the largest category of licensed caregivers"* and *"the most commonly excluded discipline"* ([ProviderTrust](https://www.providertrust.com/blog/travel-nurses-credentialing-and-monitoring/)). Failing HCSS-6/7 threatens certification, which threatens contracts.
**Evidence quality:** Regulatory hook — very strong (primary Joint Commission measure definitions). Current-state tooling mix — **weak; see §8 gaps.**

### P5 — Invoice rejection and resubmission at client AP portals

**Who:** Billing specialist.
**When:** Every submission to a portal-mediated client.
**How handled now:** Submit, wait, receive a rejection code, fix, resubmit under a new invoice number, re-age.
**Why inadequate:** The rejection rules are published, deterministic, and machine-checkable — but nobody checks them before submitting. Georgia-Pacific publishes its full code set ([GP supplier portal](https://www.gp.com/georgia-pacific-supplier-portal/invoice-rejections)). The staffing-relevant ones:

| Code | Rule | Why it bites staffing |
|---|---|---|
| R3 | Quantity × price must agree with displayed amount | Rounding an hours×rate extension by one cent kills the invoice |
| R5 | Invoice referencing multiple POs must be split | Fatal to a consolidated multi-department weekly staffing invoice |
| R9 | Invoice number >16 characters or with special characters other than hyphens | Agency numbering schemes routinely violate this |
| R11 | Invoice must be dated within 7 days of submission | Late-arriving approvals push the invoice date out of range |
| R16 / R12 | Handwritten invoices not accepted; poor image quality | Kills scan-of-signed-timesheet-as-invoice |
| R23 | Debit and credit lines cannot share a document | Every correction becomes two documents and another aging cycle |
| R7/R20/R28 | Invalid or blank facility/ship-to/location | Multi-site clients |

Tungsten adds hard constraints of its own: **duplicate invoice numbers are absolutely rejected**, so every correction burns a new number and breaks the agency's sequence; one PO per header, with multiple POs distributed line by line; and **a maximum of 3 attachments, TIFF format only, within a 24-hour window** before the invoice auto-submits without them ([Tungsten/Apple supplier FAQ](https://www.tungsten-network.com/customer-campaigns/apple/faqs-and-documentation/)). For a 40-worker weekly invoice, a 3-attachment TIFF cap means per-worker signed-timesheet backup simply cannot ride along.

**Frequency:** Weekly per portal client.
**Cost:** Each rejection is a full cycle — typically a week of additional DSO on that invoice plus 15–45 minutes of specialist time, and in monthly-billing programs, *"one unclicked button means the invoice cannot be generated for another full cycle."*
**Evidence quality:** Very strong. The rules are published by the buyers themselves.

### P6 — Multi-jurisdiction employment paperwork per assignment

**Who:** Onboarding/HR coordinator.
**When:** Every placement, and again whenever a rate or client changes.
**How handled now:** Word templates in folders, assembled by hand, with the client details typed in.
**Why inadequate:** The requirements are per-assignment and per-jurisdiction and they interlock. California's §2810.5 requires the **client legal entity's** name and addresses on the notice, and a fresh notice within **7 calendar days** of any change. New York requires **LS 51** specifically, in the worker's primary language where a DOL translation exists (Spanish, Chinese, Haitian Creole, Korean, Polish, Russian). Illinois is the heaviest: the amended **Day and Temporary Labor Services Act** requires the *agency* — not the client — to compute equal pay and benefits after **720 hours** with a client in 12 months, using comparator data the client must supply, and to state the comparator's seniority and hourly wage (or the SOC code used) in the assignment notice; after **4,160 hours over 48 months** wages rise to the **75th percentile** of BLS data. The agency must also notify laborers of strikes or lockouts at the worksite and issue **application receipts to applicants who are never placed** ([Jackson Lewis](https://www.jacksonlewis.com/insights/illinois-amends-temp-worker-law-boosting-employer-obligations)). Illinois registration alone costs **$3,000/year per agency plus $750 per branch**, and operating unregistered is **$500 per day, each day a separate violation** ([Illinois DOL](https://labor.illinois.gov/laws-rules/fls/day-temporary-labor.html)).

I-9 also got materially worse: on **March 16, 2026**, ICE reclassified over ten previously correctable errors as **substantive violations and eliminated the 10-day cure period** — including missing date of birth, incomplete Section 2 document data, and missing employment dates — and removed the rule allowing retained document copies to cure missing Section 2 data. Range **$288–$2,861 per form**; Morgan Lewis models 200 deficient forms at **$57,600–$572,200** ([Morgan Lewis](https://www.morganlewis.com/pubs/2026/04/ice-rewrites-the-rules-on-form-i-9-violations)). A firm hiring 3,000 temps a year at a 10% substantive error rate carries 300 forms of exposure annually.

**Frequency:** Every placement.
**Cost:** 10–30 minutes per assignment of pure clerical assembly, plus tail risk in the hundreds of thousands.
**Evidence quality:** Very strong — statutes, regulator forms, and law-firm alerts.

### P7 — ACA measurement and break-in-service for a churning population

**Who:** Controller/HR.
**When:** Monthly measurement, annual filing, continuous rehire testing.
**How handled now:** Spreadsheets, or a bolt-on module. Avionté ships a separate **"ACA Companion" admin tool** ([Avionté support](https://support.avionte.com/hc/en-us/articles/235826607-ACA-Companion-Admin-Tools-Setup)); TempWorks documents a separate monthly-measurement setup ([TempWorks KB](https://kb.tempworks.com/help/setting-up-aca-monthly-measurement-option)). The existence of a *companion* tool is itself evidence this is not native to payroll — and reviewers report it going stale (§2.5).
**Why inadequate:** The rehire rules are volume killers for staffing. General rule: rehire within **less than 13 weeks** = continuing employee, not a new hire. **Rule of parity**: a break of at least 4 weeks *and* longer than the prior employment period may be treated as a new hire. Under look-back, *"the measurement and stability periods continue as if the employee had never left,"* with no hours credited during the break ([AssuredPartners summary](https://www.assuredpartners.com/-/media/Files/Corporate/EB-Compliance-Documents/50-99-Employees/Column-1/ACA---Lookback-and-Variable-Hour/Break-in-Service-Rules-Summarized.pdf); primary regulation [26 CFR 54.4980H-3](https://www.ecfr.gov/current/title-26/chapter-I/subchapter-D/part-54/section-54.4980H-3)). For a firm placing workers on 4–13 week assignments, **essentially every worker record hits this test repeatedly**. Practitioners at an ASA Staffing World session named the failure modes directly: manual spreadsheet tracking, **inconsistent rehire calculation**, failure to distinguish break-in-service periods, missed pre-submission checkpoints ([Selerix write-up](https://selerix.com/blog/staffing-world-takeaways-aca-compliance-faqs/) — vendor writing up a real session).

There is also a billing-system consequence nobody expects: the staffing-firm safe harbor at **Treas. Reg. §54.4980H-4(b)(2)** gives the client credit for the agency's offer of coverage *only if* **"the fee the client employer would pay to the staffing firm for an employee enrolled in health coverage under the plan is higher than the fee… if that employee did not enroll"** ([Newfront](https://www.newfront.com/blog/aca-employer-mandate-and-outside-staffing-firms-2)). That forces a **two-tier bill rate** into the rate card and into every client contract.

**Frequency:** Monthly; annual filing.
**Cost:** 2026 penalties are **§4980H(a) $3,340** per FTE (less the 30-employee reduction) and **§4980H(b) $5,010** per subsidized employee ([Thomson Reuters on Rev. Proc. 2025-26](https://tax.thomsonreuters.com/news/irs-announces-increases-for-2026-aca-employer-shared-responsibility-penalties/)). Reporting penalties for TY2025 1095-Cs run **$60/form** if fixed within 30 days, **$130/form** through Aug 1, **$340/form** thereafter, with e-filing mandatory at **10 or more information returns in aggregate** ([BDO](https://www.bdo.com/insights/tax/employer-filing-obligations-and-penalty-exposure-for-late-or-missing-affordable-care-act-forms)). A mid-size agency generates several thousand 1095-Cs against a handful of internal staff.

### P8 — Recruiter commission calculation, fall-offs and clawbacks

**Who:** Controller/owner; every recruiter checking their statement.
**When:** Monthly or semi-monthly.
**How handled now:** Excel. Named-firm evidence from a commission vendor's case studies (the firms and their numbers are their own): **Klein Hersh** — commissions were *"a 12-hour (at least) ordeal every pay period"*; **Spencer Thomas Group** — *"2–3 days to process monthly commissions, and 3–4 days for quarterly commissions"*; **Acuity** — *"sporadically missed commissions and weren't paying recruiters the amount that was due to them"*; **Direct Staff** — *"errors resulting in miscalculated commissions"* ([QCommission staffing overview](https://www.qcommission.com/industries/industries-four/staffing-overview.html)).
**Why inadequate:** The join is four-dimensional — GP by placement by period, split across multiple recruiters at **different rates per payment received**, against tier thresholds, net of draw balances, adjusted by fall-off and bad-debt clawbacks. Guarantee periods cluster at **90 days (44.9%)**, with 30 days (20.3%) and 60 days (20.0%) close behind; refund policy is **replacement/no money back for 61.4%**, prorated for 17.6%, full refund for 8.4% ([Top Echelon recruiter poll](https://topechelon.com/blog/recruiter-guarantees-once-i-am-paid-i-do-not-refund-any-money/)). Structures observed include prorated **1/3 of fee per 30-day interval** and guarantees **contingent on the client paying the invoice within 10 days of start** ([NPAworldwide](https://npaworldwide.com/blog/2017/05/25/8-guarantee-refund-policies/)). Add temp-side reality: *"if a temp leaves early or a client refuses payment, commission clawbacks and adjustments become frequent"* ([Everstage](https://www.everstage.com/best-sales-commission-software-for-staffing-firms) — vendor).
**Frequency:** Monthly.
**Cost:** 12 hours to 4 days per cycle at the named firms, plus recruiter trust damage and shadow-accounting time.

### P9 — Unapplied cash, short-pays and remittance matching

**Who:** AR specialist.
**When:** Every deposit.
**How handled now:** Manual matching, often in Excel, against an aging report.
**Why inadequate:** Three structural mismatches. (1) The remittance references the **VMS's** invoice number, not the agency's (§2.1). (2) When the MSP fee is a **deduction from cash received** rather than a line on the invoice, AR ages at gross while cash arrives net — a permanent short-pay that looks identical to a dispute; VectorVMS states roughly **75% of VMS contracts** use the supplier-funded model where suppliers deduct a percentage from each invoiced hour ([VectorVMS](https://vectorvms.com/blog/vendor-management/how-much-vms-cost-vendor-funded-model-explained/) — VMS vendor, low trust on the percentage). (3) Corrections must flow through credit memo + rebill because portals forbid mixed debit/credit documents and number reuse (§P5). That "unapplied cash reconciliation if the customer payment does not provide invoice details" appears as a **named duty in a real job description** is the cleanest proof this is a standing job, not an exception.

### P10 — Timesheet cutoff and cash timing

Ranked last not because it is small but because the incumbent vendors genuinely address the *chasing* part (exception queues, automated reminders). What they do not address is the **economic** consequence: a worked example of 40 field employees × $32/hr × 40 hrs = **~$51,200 in weekly billings**, where one missed approval before cutoff pushes payment 7+ days further out while payroll clears on schedule — a gap funded 100% by the agency ([Madison Resources](https://madisonresources.com/vms-software-for-staffing-firms-what-actually-matters-when-youre-the-supplier/)). Compliance exposure also concentrates here: FLSA's "suffered or permitted" standard means the agency owes for hours the client supervisor never recorded, rounding becomes a violation when it shows **directional bias**, and **"the staffing agency remains responsible for payroll accuracy even when a client supervisor reviews the worker's hours"** — supervisor approval is evidence, not a liability transfer ([USA Staffing Services](https://www.usastaffingservices.com/temp-staffing-time-tracking-compliance/) — vendor, but legally grounded).

---

## 4. Application opportunities

### A1 — True Burden Bill Rate & Margin Calculator

- **Working title:** RateGuard
- **Intended user:** Agency owner, branch manager, salesperson quoting a req.
- **Problem solved:** P1. Quotes are priced on a markup heuristic that omits FUTA front-loading, experience-rated SUTA, class-code-specific workers' comp, MSP fee deduction, ACA and sick-leave accrual, and the cost of capital at *actual* DSO.
- **Current workflow:** Pay rate × house markup, mentally cross-checked against "what we usually get."
- **Proposed workflow:** Enter pay rate, state, WC class code, expected hours and OT mix, client payment terms and MSP fee. Get true GP% and GP$ at straight time, at the blended OT mix, and net of financing cost — plus the reverse solve: "what bill rate hits 22% true margin?"
- **Inputs:** Pay rate; work state (and locality for sick leave and minimum wage); WC class code and the agency's rate for it; agency SUTA rate; YTD wages for the worker (for FUTA/SS ceiling logic); expected weekly hours and OT hours; assignment length; client terms; MSP/VMS fee %; factoring rate; per-hour ACA and benefit loads.
- **Outputs:** A one-page quote sheet — burden waterfall, GP$ and GP% at ST/OT/blended, break-even bill rate, margin sensitivity to a ±2-point SUTA move and to +30 days DSO. Exportable to PDF and CSV.
- **Essential features:** Per-state SUTA and wage-base table; FICA/FUTA ceilings; user-maintained WC rate table by class code; markup↔margin conversion shown side by side; scenario compare (2–3 candidate rates).
- **Excluded from v1:** Quote storage/CRM, approval workflow, e-signature, integration with any ATS.
- **AI:** **Inappropriate.** This is arithmetic and rate tables. Adding AI would reduce trust in the number.
- **Why not just a spreadsheet:** A spreadsheet *can* do this and some agencies have one. What they do not have is the **maintained rate tables** (51 SUTA rates and wage bases changing annually, ~90 local minimum wages, class code rates), the ceiling logic that makes FUTA/SS burden depend on YTD wages, or a defensible version history. The tool's value is the curated data plus correct ceiling math, not the formula.
- **Complexity:** Small.
- **Learning difficulty:** Under 10 minutes.
- **Value:** Prevents 2–5 points of margin error on assignments where the rate is locked for the contract term — $1,600+ per 2,000-hour placement per two points on a $40 bill rate.
- **Risks/constraints:** Rate-table currency is the whole product; stale tables are worse than no tool. Must carry a clear "not tax or insurance advice" boundary. No PII involved, which makes it easy to distribute.
- **Existing substitutes:** [Advance Partners' bill rate calculator](https://www.advancepartners.com/calculate-how-to-price-your-staffing-services/) and similar lead-magnet calculators; the pricing screen inside Bullhorn/Avionté.
- **Why still attractive:** Every substitute is a simple markup calculator. None model FUTA front-loading, per-state SUTA, class-code WC, MSP deduction, or DSO carry. It is also the cheapest possible entry point into this market and a natural free base with obvious paid customization.
- **Paid customization:** Load the client's actual SUTA rates, WC schedule, benefit loads and factoring terms; build their house margin floors and approval thresholds in; add their branded quote sheet. Straightforward $2–5k engagements.

### A2 — Per-Assignment Employment Notice Packet Generator

- **Working title:** AssignmentPack
- **Intended user:** Onboarding/HR coordinator.
- **Problem solved:** P6. Per-assignment, per-jurisdiction wage and assignment notices are hand-assembled from Word templates, with client entity details retyped and change-notices routinely missed.
- **Current workflow:** Find last month's version of the right template, retype client name/address, print, chase signature, file.
- **Proposed workflow:** Enter or import the assignment record (worker, work state/locality, pay rate, OT rate, pay frequency, client legal entity name + physical and mailing address + phone, start date, primary language). The tool emits the complete correct packet for that jurisdiction, in the correct language, with a signature block and a versioned record. A change to rate or client triggers a change-notice with the statutory deadline shown (CA: 7 calendar days).
- **Inputs:** Assignment record; client legal entity record; a maintained jurisdiction rules table; language selection.
- **Outputs:** A PDF packet (e.g. CA §2810.5 temp-services notice; NY **LS 51** in English plus required translation; IL DTLSA assignment notice); a change-notice; a compliance log line per issuance.
- **Essential features:** Rules table keyed to work state + locality; client-entity records reused across assignments; language variants; change detection against the prior issued notice; searchable issuance log for audit.
- **Excluded from v1:** E-signature (export PDF and let them use whatever they already have), I-9 itself, benefits enrollment, general HRIS functions, states beyond an initial CA/NY/IL/NJ/MA set.
- **AI:** **Inappropriate for generation** (it must be deterministic and exact). Arguably *optional* later for triaging new statutes into the rules table, with human review — but never in the output path.
- **Why not just a spreadsheet:** The output is a formatted, multilingual, signable legal document set, with per-assignment variation and a change-detection rule. A spreadsheet cannot produce it and cannot prove what was issued when.
- **Complexity:** Small to medium.
- **Learning difficulty:** Under 30 minutes.
- **Value:** 10–30 minutes per assignment saved; at 500 placements/year that is 80–250 hours. Tail risk avoided is much larger.
- **Risks/constraints:** This is compliance output — the rules table must be maintained and the tool must never claim to be legal advice. Contains worker PII and pay rates; should run locally or self-hosted by default.
- **Existing substitutes:** HRIS onboarding modules (built around a stable employee record, not a per-assignment one); law-firm template packs; the agency's own Word folder.
- **Why still attractive:** The temp-specific requirements (CA's client-entity disclosure, NY's LS 51, IL's comparator statement) are exactly the ones general HRIS onboarding does not model, because they depend on the *assignment*, not the *hire*.
- **Paid customization:** Add the client's specific states; wire it to their ATS export; add their branded packet cover and internal acknowledgement forms. **The Illinois 720-hour equal-pay watchdog is the standout paid module** — track cumulative hours per worker per client, project the 720-hour crossing date, and auto-generate the comparator-data request to the client.

### A3 — Invoice Pre-Flight Validator

- **Working title:** PreFlight
- **Intended user:** Billing specialist.
- **Problem solved:** P5. Invoices are submitted into client AP portals and rejected on published, deterministic rules that nobody checks first.
- **Current workflow:** Submit → wait days → rejection code → fix → new invoice number → resubmit → re-age.
- **Proposed workflow:** Drop the invoice file (CSV/XLSX export from the billing system, or PDF) and pick the client profile. Get a pass/fail list before submitting: invoice number length and character set, extension arithmetic to the cent, one-PO-per-invoice, invoice date within the allowed window, required fields present, no mixed debit/credit lines, attachment count and format, ship-to/facility validity.
- **Inputs:** Invoice file; per-client rule profile (a small YAML/JSON the user edits); optionally the attachment set.
- **Outputs:** A pass/fail report with the specific offending line and the rule it violates; a corrected-file suggestion where the fix is mechanical (rounding, number truncation, PO split); a per-client rejection history.
- **Essential features:** Ship with starter profiles for the published rule sets (Georgia-Pacific codes, Tungsten/Apple constraints, generic Ariba/Coupa); let users add profiles; rejection-reason logging so the agency can see its own top two causes.
- **Excluded from v1:** Actually submitting to the portals (no fragile integrations — this is a checker, not a connector); invoice generation; AR aging.
- **AI:** **Optional and peripheral.** Rules checking is deterministic. AI is genuinely useful only for one thing: reading a free-text rejection email from a client's AP and proposing a new rule for the profile. Ship v1 without it.
- **Why not just a spreadsheet:** Conditional formatting can catch a rounding error. It cannot enforce "no more than 3 TIFF attachments," "no mixed debit/credit lines," or "one PO per invoice with line-level distribution," and it cannot keep 25 client profiles versioned.
- **Complexity:** Small to medium.
- **Learning difficulty:** Under 30 minutes.
- **Value:** Each avoided rejection saves roughly a week of DSO on that invoice plus 15–45 minutes. For an agency submitting 40 portal invoices a week at even a 5% rejection rate, that is ~100 rejections a year.
- **Risks/constraints:** Invoice files contain client and worker data; run locally. The starter profiles must be labeled as user-maintained, not guaranteed current.
- **Existing substitutes:** None focused. AP-side validation tools exist, but they serve the buyer. Billing modules do not validate against the receiver's rules.
- **Why still attractive:** The rules are **published by the buyers themselves** — this is a rare case of a compliance target that is fully documented and fully deterministic, with nobody serving the supplier side.
- **Paid customization:** Build profiles for the client's specific top-20 customers from their actual rejection history. Recurring value as customers change portals.

### A4 — Credential Expiry & Assignment Eligibility Guard

- **Working title:** ShiftClear
- **Intended user:** Credentialing/onboarding coordinator; scheduler.
- **Problem solved:** P4. Expiration tracking lives in spreadsheets; eligibility is the union of statutory, firm and *customer* requirements; expired scores the same as missing under Joint Commission HCSS-6/7.
- **Current workflow:** A spreadsheet of workers × credentials with dates, plus calendar reminders, plus a folder of PDFs, plus a per-facility checklist in Word.
- **Proposed workflow:** Maintain three tables — workers, credentials (with issue/expiry and document link), and **client requirement profiles**. The tool answers three questions on demand: (1) who is non-compliant *for a shift scheduled on a given future date*, (2) what exactly is missing for worker X to be submittable to facility Y, (3) what are this month's HCSS-6/HCSS-7 numerator and denominator.
- **Inputs:** Worker roster; credential records; per-client requirement profile; assignment/shift schedule (CSV import from ATS or manual).
- **Outputs:** Forward-looking expiry report keyed to *scheduled shifts, not calendar dates*; per-worker per-facility gap list; renewal chase list with owner and due date; monthly personnel-file-completeness numerator/denominator; an audit-ready packet export per worker.
- **Essential features:** Requirement profiles composable from statutory + firm + customer layers; "as of date" evaluation; document storage with expiry metadata; simple email/CSV chase output.
- **Excluded from v1:** Primary-source verification integrations (state boards, NPDB, OIG LEIE) — these are the fragile-integration trap; instead, record *that* verification was done, by whom, on what date, with an attached screenshot/PDF. Also excluded: scheduling itself, credential *application* workflows, payer credentialing (a different problem entirely).
- **AI:** **Optional, narrow.** Extracting issue and expiry dates from an uploaded license or certification PDF/photo is a real AI win — it is exactly the interpretation task conventional code handles badly, and it is the highest-friction data-entry step. Everything else is deterministic. Ship v1 with manual date entry and add extraction in v2.
- **Why not just a spreadsheet:** A spreadsheet evaluates expiry against *today*. The question that matters is "is this worker clear for a shift on the 14th of next month, at *this* facility, under *its* requirement set" — a three-way join a spreadsheet cannot express without becoming unmaintainable. It also cannot produce the HCSS numerator/denominator, which requires evaluating each *placement* against the file state.
- **Complexity:** Medium.
- **Learning difficulty:** 1–2 hours.
- **Value:** Avoids mid-shift pulls (immediate lost revenue plus client damage), reduces submission rejections, and turns a quarterly certification-reporting scramble into a query. Displaces a meaningful slice of a $45–58k FTE's time.
- **Risks/constraints:** Holds PHI-adjacent and HR data — licenses, immunization records, background checks, drug screens. **Must be self-hostable and encrypted at rest**; a hosted free version is a poor idea for this one. Retention rules apply.
- **Existing substitutes:** Credentialing modules inside healthcare staffing suites; standalone credentialing SaaS (Med Staff Tracker, TalentPathway); generic expiry-reminder tools. Also the incumbent: Excel.
- **Why still attractive:** The substitutes either sit inside a suite the 5–50-person agency has not bought, or are generic reminder tools with no concept of a *client requirement profile* or a *scheduled shift*. The HCSS-6/7 numerator is a bright, specific, unserved output.
- **Paid customization:** Build the agency's actual facility requirement profiles (this is the labor-intensive part and is worth real money); map their ATS export; add their competency checklists.

### A5 — VMS Reconciliation Workbench

- **Working title:** ThreeWay
- **Intended user:** Payroll & billing / revenue specialist.
- **Problem solved:** P3. Two datasets that "almost never agree on the first pass," reconciled by hand in Excel every cycle.
- **Current workflow:** Export VMS report → export internal hours → sort → VLOOKUP → eyeball → chase.
- **Proposed workflow:** Configure a **column mapping profile per client** once. Each cycle, drop in the VMS export and the internal pay/bill register. The tool matches on worker + assignment + date and classifies every difference into the five known classes — rate, hours, missing, duplicate, period boundary — producing an exception worklist and a clean "safe to bill" set.
- **Inputs:** VMS export (CSV/XLSX; PDF via extraction); internal hours/rate register; contracted rate card; client profile (billing period definition, rounding rule, OT rule, MSP fee %).
- **Outputs:** Exception list grouped by class and owner, with dollar impact per exception; a clean billable file; a "hold" list; an MSP-fee accrual line so AR is booked net; a trend report of exception counts by class and by client (so the agency can kill its top two causes).
- **Essential features:** Per-client column mapping profiles; period-boundary allocation (weekly payroll → semi-monthly/monthly billing); rate-card comparison; tolerance thresholds so one-cent rounding does not flood the list; run history.
- **Excluded from v1:** Direct VMS API/SFTP integration (fragile, per-client, and gated by the client's program office); invoice submission; payroll.
- **AI:** **Optional, narrow.** Deterministic matching does the work. AI earns its place in exactly two spots: parsing a heterogeneous VMS **PDF** export into a table, and *suggesting* a column mapping for a new client's file. Both are assistive with human confirmation, neither is in the arithmetic path.
- **Why not just a spreadsheet:** This is where the spreadsheet genuinely fails. Period-boundary allocation, five-way exception classification with dollar impact, per-client mapping profiles, and run-over-run trending are not maintainable in Excel — and the current spreadsheet approach is precisely what practitioners describe as the constraint on how fast they can invoice.
- **Complexity:** Medium.
- **Learning difficulty:** 1–2 hours for the first client profile, minutes thereafter.
- **Value:** The published leakage figures are vendor-authored and should not be quoted as fact, but the direction is not in dispute: this is the process that gates invoicing speed, and invoicing speed is DSO, and DSO at a 1–5% factoring fee is cash.
- **Risks/constraints:** Contains rate and worker data — run locally. **Getting realistic test data is the hardest part of this build** (see §6). Client contracts may restrict what VMS data can leave the portal environment; the tool reading a file the user already downloaded is the safe posture.
- **Existing substitutes:** **Reconciled** (acquired by LaborEdge in 2025) is the direct competitor, aimed at healthcare staffing at $50–75M AR scale; Bullhorn markets "VMS Time" on the same premise.
- **Why still attractive:** Every existing product is priced and scoped for firms an order of magnitude larger, and is sold as a platform commitment. A file-in/file-out desktop workbench for a 15-person agency with three VMS clients is a different product at a different price. The acquisition is validation, not foreclosure.
- **Paid customization:** Per-client mapping profiles are the natural recurring service — each new VMS client is a small paid engagement.

### A6 — Workers' Comp Class Code Assigner & Payroll-by-Code Reconciler

- **Working title:** ClassCheck
- **Intended user:** Owner/controller; account manager at placement.
- **Problem solved:** P2. Codes are assigned casually and payroll is not segregated by code, so the annual audit is a surprise.
- **Current workflow:** Accept the client's suggested code or copy the last similar one; discover the consequences at audit.
- **Proposed workflow:** At placement, enter the job duties, industry and host-employer operations; the tool proposes a shortlist of candidate class codes with the agency's own rate for each and the dollar delta between them, requiring the user to confirm and record the rationale. Throughout the year it maintains a **payroll-by-class-code register** and flags drift — payroll accumulating under codes not on the policy, or a mix diverging from what was quoted.
- **Inputs:** Job title and duty description; host operations; state; the agency's class-code rate schedule; periodic payroll register with code tags.
- **Outputs:** Code recommendation with rationale and dollar impact, stored as an audit trail; payroll-by-code register reconcilable to the carrier's audit worksheet; a drift alert; a pre-audit self-check pack.
- **Essential features:** Rate schedule import; code-assignment audit trail (who chose what, when, why — this is the artifact that survives an audit dispute); payroll segregation by code; comparison of actual vs. quoted mix.
- **Excluded from v1:** Being an authority on classification (it proposes and documents; the broker and carrier decide); claims management; certificate issuance.
- **AI:** **Genuinely useful, and this is the clearest AI case in the report.** Mapping a free-text job duty description to a candidate set of NCCI/state class codes is a semantic classification task with a large, irregular taxonomy — exactly what conventional rules handle badly. But it must be **suggest-and-confirm with recorded rationale, never auto-assign**, because the liability is real.
- **Why not just a spreadsheet:** The register part could be a spreadsheet. The duty→code suggestion and the drift detection could not, and neither could the audit trail that makes the recommendation defensible.
- **Complexity:** Medium.
- **Learning difficulty:** 1 hour.
- **Value:** The documented failure cases are $80,000, $620,000, and two businesses closed. Even ordinary miscoding of one crew is tens of thousands a year.
- **Risks/constraints:** **Liability framing is essential** — this is a documentation and decision-support tool, not a classification authority. Class code tables and rates vary by state and bureau (NCCI vs. independent states like CA, NY, PA, NJ); v1 should cover NCCI states and be explicit about the gaps.
- **Existing substitutes:** The broker's judgment; carrier portals; the payroll system's class-code field.
- **Why still attractive:** Brokers are involved at renewal, not at 4pm on a Tuesday when a placement needs a code. The *audit trail* is the differentiator — the broker paper's whole point is that agencies cannot defend the codes they chose.
- **Paid customization:** Load the agency's actual rate schedule and policy code list; build their state mix; map their payroll export.

### A7 — Remittance & Short-Pay Classifier

- **Working title:** ShortPay
- **Intended user:** AR specialist.
- **Problem solved:** P9. Remittances reference the wrong invoice numbers, MSP fees arrive as deductions, and unapplied cash is a standing job.
- **Current workflow:** Manual matching against an aging report; unapplied cash sits.
- **Proposed workflow:** Import the remittance advice (CSV or PDF), the AR aging, and the VMS cross-reference report. The tool auto-matches on the agency invoice number *or* the VMS invoice number, then classifies every residual into: MSP/program fee deduction (expected, book as contra-revenue), rounding, known credit memo, rate dispute, hours dispute, or unknown.
- **Inputs:** Remittance advice; AR aging export; VMS cross-reference (e.g. the Beeline supplier reconciliation report); client profile with the expected MSP fee %.
- **Outputs:** Application file for the accounting system; classified short-pay worklist with owner and dollar amount; a dispute pack per unresolved item; an aging view *net of expected fee deductions* so real disputes stand out.
- **Essential features:** Dual-key matching (agency number and VMS number); expected-deduction modeling; residual classification; export to QuickBooks/CSV.
- **Excluded from v1:** Bank feed integration; dunning automation; collections CRM.
- **AI:** **Optional.** Parsing an unstructured remittance PDF into a table is a fair AI use. Classification is rules-driven.
- **Why not just a spreadsheet:** Dual-key matching plus expected-deduction netting plus residual classification across many clients is beyond practical spreadsheet maintenance — and the "expected deduction vs. real dispute" distinction is the whole value.
- **Complexity:** Medium.
- **Learning difficulty:** 1 hour.
- **Value:** Directly attacks a duty that appears in real job descriptions. Shrinks unapplied cash and separates structural short-pays from genuine disputes, which is what makes collections calls productive.
- **Risks/constraints:** Financial data; local execution.
- **Existing substitutes:** Enterprise cash-application tools (Billtrust and similar) — priced and scoped far above this segment; the ERP's auto-match.
- **Why still attractive:** The staffing-specific twist — VMS invoice numbering and fee-deduction short-pays — is exactly what generic cash-application tools do not model.

### A8 — ACA Look-Back & Break-in-Service Tracker

- **Working title:** LookBack
- **Intended user:** Controller/HR.
- **Problem solved:** P7. Break-in-service and rule-of-parity testing on a churning population, done in spreadsheets or in a bolt-on module practitioners describe as neglected.
- **Current workflow:** Spreadsheet, or an "ACA Companion" module that lags the payroll system.
- **Proposed workflow:** Import a payroll hours history plus hire/term events. The tool applies the 13-week rule and the rule of parity, computes measurement/administrative/stability periods per worker, flags who averages ≥130 hours/month, and produces an offer-deadline worklist plus a pre-check of proposed 1095-C line 14/16 codes against the computed status.
- **Inputs:** Payroll hours by worker by month; hire/rehire/term dates; plan offer records; the agency's chosen measurement method and period dates.
- **Outputs:** Per-worker status timeline; offer-deadline worklist; ALE calculation; 1095-C code pre-check with exceptions; a filing-readiness summary.
- **Essential features:** Look-back and monthly-measurement methods; break-in-service and parity logic; multiple EINs; configurable measurement/admin/stability periods; exception report rather than a filing engine.
- **Excluded from v1:** Actually e-filing to the IRS (that is a regulated transmission path with its own certification burden — stay out of it); benefits enrollment; carrier feeds.
- **AI:** **Inappropriate.** This is regulation-as-code. Any nondeterminism is a liability.
- **Why not just a spreadsheet:** Rule of parity requires comparing each break against the *preceding employment period length*, per worker, across an unbounded number of stints. That is a loop, not a formula, and it is where practitioners report inconsistent results.
- **Complexity:** Medium.
- **Learning difficulty:** 2 hours — this one requires the user to already understand their own ACA method.
- **Value:** §4980H(a) at $3,340/FTE and 1095-C penalties at up to $340/form make this high-consequence, though low-frequency. Real value even for firms that *have* a module, as an independent verification pass before filing.
- **Risks/constraints:** Compliance output; must be positioned as a check, not as tax advice. Contains PII.
- **Existing substitutes:** ACA modules in Avionté/TempWorks; ACA filing services; benefit-broker spreadsheets.
- **Why still attractive:** The named-practitioner evidence that these modules go stale and that firms end up "scrambling to manually code our 1095's" is unusually direct. A verification tool has value precisely because it is independent of the system that might be wrong.

### A9 — Commission & Clawback Ledger

- **Working title:** SplitLedger
- **Intended user:** Controller/owner; recruiters as read-only recipients.
- **Problem solved:** P8. Commission runs taking 12 hours to 4 days, with errors and recruiter shadow accounting.
- **Current workflow:** Excel, rebuilt each period.
- **Proposed workflow:** Define plans once (basis, tiers, splits, draw, guarantee/clawback rules). Import GP by placement by period and events (fall-off, client nonpayment, extension). Produce per-recruiter statements with a full line-level audit trail, plus a clawback ledger tracking guarantee windows and prorated refunds.
- **Inputs:** GP by placement by period; recruiter split assignments; plan definitions; draw balances; fall-off and bad-debt events; guarantee terms per placement.
- **Outputs:** Per-recruiter statement (PDF/CSV) showing every placement, split, tier, draw application and clawback; a payroll-ready summary; a clawback ledger with open guarantee windows and their expiry dates.
- **Essential features:** Line-level payee assignment; tiered rates on quota attainment; draw against commission with carry-forward; guarantee windows including **prorated 1/3-per-30-days** and payment-contingent variants; commission-on-cash-received vs. on-billing toggle.
- **Excluded from v1:** Quota planning, forecasting, gamification dashboards, payroll disbursement.
- **AI:** **Inappropriate.** Recruiters will audit every line; the calculation must be explainable and reproducible.
- **Why not just a spreadsheet:** It *is* a spreadsheet today, and the named-firm evidence is that it takes 12 hours to 4 days and produces missed payments. The specific killer is commission recognized on **cash received**, split across multiple recruiters at **different rates**, against tiers, net of draw, adjusted by clawbacks — a four-way join with a temporal dimension.
- **Complexity:** Medium.
- **Learning difficulty:** 2–3 hours to set up plans; minutes per run thereafter.
- **Value:** Reclaims 1–4 days per period at the documented firms, and the statement audit trail is what ends shadow accounting.
- **Risks/constraints:** Compensation data — highly sensitive; self-hosted only. Plan definitions vary enormously, which is a modeling risk: v1 must cover the common shapes and refuse gracefully rather than approximate.
- **Existing substitutes:** QCommission, Everstage, CaptivateIQ — all priced for larger sales orgs; Excel.
- **Why still attractive:** The staffing-specific mechanics (GP basis, split desks, temp fall-offs, bad-debt clawback, payment-contingent guarantees) are the reason generic commission SaaS fits badly. Ranked lower here only because plan heterogeneity makes the scope harder to hold narrow.

---

## 5. Opportunity ranking

Scored 1–5 on each dimension; maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of impl. | Stays narrow | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| A1 | True Burden Bill Rate & Margin Calculator | 4 | 5 | 5 | 5 | 5 | 5 | 3 | 4 | 5 | 4 | **45** |
| A2 | Per-Assignment Notice Packet Generator | 4 | 5 | 4 | 5 | 4 | 5 | 4 | 5 | 4 | 4 | **44** |
| A3 | Invoice Pre-Flight Validator | 4 | 5 | 4 | 5 | 4 | 5 | 4 | 4 | 4 | 4 | **43** |
| A4 | Credential Expiry & Eligibility Guard | 5 | 5 | 5 | 4 | 3 | 4 | 3 | 5 | 4 | 5 | **43** |
| A5 | VMS Reconciliation Workbench | 5 | 5 | 5 | 4 | 3 | 4 | 3 | 5 | 3 | 5 | **42** |
| A6 | WC Class Code Assigner & Reconciler | 5 | 3 | 5 | 4 | 3 | 4 | 4 | 4 | 3 | 4 | **39** |
| A7 | Remittance & Short-Pay Classifier | 4 | 5 | 4 | 4 | 3 | 4 | 3 | 4 | 3 | 4 | **38** |
| A8 | ACA Look-Back & Break-in-Service Tracker | 5 | 3 | 4 | 3 | 3 | 4 | 4 | 4 | 3 | 5 | **38** |
| A9 | Commission & Clawback Ledger | 4 | 4 | 4 | 3 | 3 | 3 | 3 | 5 | 4 | 4 | **37** |

### The top three

**A1 — True Burden Bill Rate & Margin Calculator (45).** It wins on the unglamorous dimensions: it is the easiest to build, the easiest to learn, the easiest to test (no client data required at all), the easiest to distribute, and the problem it addresses is the one that compounds silently. Every other concept on this list recovers money that was already earned; this one prevents money from never being earned. It also has the best cold-start properties in a market where the buyer is a skeptical owner — a free, no-signup, no-data-upload calculator that shows them their real margin is a credible first contact, and the paid version (their SUTA rates, their WC schedule, their factoring terms, their margin floors) sells itself. Its weakness is differentiation: markup calculators exist. The answer is that none of them model ceiling-dependent burden, per-state SUTA, class-code WC, MSP deduction, or DSO carry — and the gap between "markup calculator" and "true burden calculator" is exactly the 24-point error in the worked example.

**A2 — Per-Assignment Notice Packet Generator (44).** Narrow, deterministic, per-assignment, and backed by primary statutory sources rather than vendor claims. It sits precisely in the gap that defines this market: general HRIS onboarding is built around a stable employee master record, while California, New York and Illinois impose obligations keyed to the *assignment* and the *client entity*. The Illinois 720-hour comparator obligation is a genuinely hard requirement with no obvious incumbent solution and would make an excellent paid module. Risk is scope creep toward "an HRIS," which must be resisted hard.

**A3 — Invoice Pre-Flight Validator (43).** The rarest thing in this report: a compliance target that the counterparty **publishes in full**. Georgia-Pacific's rejection codes and Tungsten's constraints are machine-checkable rules that nobody is checking on the supplier side. Small build, immediate before/after demo (submit-and-pray versus 20 seconds of validation), no integration required, and the value scales with how many portal-mediated clients an agency has — which is exactly the direction the market is moving.

### What should be investigated next

**Build A1 first** as the wedge — it is a weekend-to-two-week build with no data-access dependency and it opens the conversation.

**Investigate A4 (Credential Expiry & Eligibility Guard) next**, and investigate it *before* building. It has the highest severity, the strongest regulatory hook (HCSS-6/7 are primary-source certification requirements where expired scores the same as missing), and the clearest paid-customization story — but §8 flags a real gap: **there is no defensible evidence of how agencies actually track expirations today**, only vendors asserting that spreadsheets are the incumbent. That single question determines whether A4 is a large, obvious opportunity or a crowded one. Five practitioner conversations would settle it.

**A5 (VMS Reconciliation) is the highest-ceiling opportunity in the report** and deliberately ranked fifth only on implementation risk and test-data access. If sanitized VMS exports can be obtained from two or three agencies, it moves to the top of the build queue.

---

## 6. Validation plan

### Questions to ask practitioners

**For A1 (pricing):**
1. Walk me through how you set the bill rate on your last new client. What did you start from?
2. Do you know your true blended burden percentage? How was it computed and when was it last updated?
3. When your SUTA rate notice arrives in December, what happens to contracts already priced?
4. On a VMS account, is the program fee added to the bill rate or deducted from it — and where does it show up in your margin reporting?
5. What is your actual average days-to-cash by client, versus the contractual terms?

**For A4 (credentialing):**
6. Show me — literally — where a worker's license expiry date lives right now.
7. When did you last have someone pulled from or refused at a shift for a credential problem? What did it cost?
8. How many distinct facility requirement profiles do you maintain, and where do they live?
9. If I asked you for last month's HCSS-6 numerator and denominator, how long would it take to produce?
10. Who does the chasing for renewals, and how do they know what to chase?

**For A5 (VMS reconciliation):**
11. How many hours between "period closes" and "invoice submitted," and where does that time go?
12. What are your two most common exception types, and could you name their dollar impact last quarter?
13. How do you handle a weekly payroll week that straddles a monthly billing period?
14. When the VMS rate differs from your contracted rate, who wins and how long does it take to fix?

**For A3 (invoice rejections):**
15. How many invoices bounced back from a client portal last month, and for what reasons?
16. Do you have a written list anywhere of each client's invoice formatting rules?

### Who to interview

- Owners and controllers at agencies of **$3M–$40M** in billings across three verticals: light industrial, IT/professional (heaviest VMS exposure), and healthcare (heaviest credentialing). Aim for 4–6 per vertical.
- **Payroll & billing specialists** — the daily users, and the ones who know where the spreadsheets are. More valuable than owners for workflow detail.
- **Credentialing coordinators** at Joint Commission-certified firms.
- **Back-office service bureaus and payroll funders** (Advance Partners, Madison Resources, Signature) — they see hundreds of agencies' processes and know which failures are universal.
- **Staffing-specific accountants and fractional CFOs.**
- **ASA chapter meetings and state staffing associations** (the Midwest Staffing Association publishes the kind of operator-facing material that indicates an engaged membership).

### Further search terms

`staffing "pay bill" specialist workflow` · `"revenue specialist" VMS staffing duties` · `Fieldglass supplier reconciliation staffing` · `"self-bill" staffing invoice discrepancy` · `staffing agency "burden rate" calculation spreadsheet` · `NCCI class code temporary staffing audit dispute` · `HCSS-6 personnel file completeness` · `"720 hours" Illinois equal pay staffing comparator` · `LS 51 temporary help notice` · `"break in service" ACA staffing rule of parity` · `staffing commission "fall off" clawback spreadsheet` · `r/staffing` and `r/recruiting` (**requires Reddit access — unavailable in this environment**)

### Sample files and data needed

| For | Needed |
|---|---|
| A1 | Current-year SUTA rate and wage base tables (all states); a real agency's WC rate schedule by class code; two or three real quote sheets |
| A2 | Blank CA §2810.5, NY LS 51 and IL DTLSA assignment notices (all publicly available); an anonymized assignment record export from an ATS |
| A3 | 10–20 real rejected invoices with their rejection codes; two or three clients' published AP supplier requirements |
| A4 | An anonymized credential spreadsheet; two or three real facility requirement checklists (**the hardest and most valuable artifact to obtain**); an anonymized shift schedule export |
| A5 | Sanitized Fieldglass and Beeline exports from two different client programs; the matching internal pay/bill register; the contracted rate card |
| A7 | Sanitized remittance advices, one with MSP fee deductions; a matching AR aging |
| A9 | Two or three real commission plan documents; a GP-by-placement export |

### Prototypes that would validate

- **A1:** A single-page HTML calculator with hardcoded tables for three states. Put it in front of five owners and ask them to price a req they already priced. If the tool's number differs from theirs by more than two points, the thesis is confirmed on the spot. **This is a one-day prototype and the single highest-information experiment in the plan.**
- **A3:** A Python script that reads one invoice CSV and checks it against the Georgia-Pacific code set. Demonstrate by finding a real violation in a real invoice.
- **A4:** A spreadsheet-to-query prototype: take one agency's credential sheet plus one facility checklist plus one week of schedule, and answer "who is not clear for Tuesday." If that answer is not already easy for them, the opportunity is real.
- **A5:** A notebook that takes one VMS export and one pay register and produces the five-class exception list. The demo *is* the pitch: run it on their actual last cycle and show them what they missed.

### Assumptions most likely to make these fail

1. **A1:** That owners do not already know their true margin. Some — especially those using a back-office partner — do. The tool may be redundant for exactly the segment most willing to buy software. *Test with question 2 above.*
2. **A4:** That expiry tracking is spreadsheet-based. If most healthcare agencies of this size have already bought a credentialing module, the opportunity shrinks to light industrial, which has weaker regulatory pressure. **This is the largest single unvalidated assumption in the report.**
3. **A5:** That agencies can and will export VMS data to a local tool. Client contracts or program-office rules may restrict it, and the willingness to hand a vendor rate data is uncertain. Also: LaborEdge/Reconciled may push down-market faster than expected.
4. **A3:** That rejection rates are high enough to matter. If the typical agency bounces two invoices a quarter, the ROI evaporates. *Test with question 15.*
5. **A2:** That agencies are actually issuing these notices. Some are simply non-compliant and do not feel the pain until an audit — meaning the tool sells a risk they have not priced. That is a harder sale than a time saving.
6. **All:** That a 5–50-person agency will adopt any new tool at all mid-week. The weekly cutoff is brutal and the switching window is narrow. Anything requiring setup during a billing week will not get adopted. **File-in / file-out with zero configuration is not a design preference here; it is a survival requirement.**
7. **Cross-cutting:** That "free and open source" is an asset rather than a trust liability for financial and compliance tooling. It may need to be paired with self-hosting (a genuine plus for PII/PHI) rather than sold on price.

---

## 7. Cross-industry patterns

These are the transferable shapes, with the specific backlog markets they map to.

**Pattern 1 — Pre-flight validation against a receiver's published rejection rules.** When a deliverable must satisfy a gatekeeper who publishes deterministic acceptance rules, a supplier-side checker run *before* submission converts a multi-day rejection loop into seconds. Transfers to: *medical billing and RCM* (claim scrubbing against payer edits), *county recorder offices — document intake, indexing and rejection handling*, *environmental laboratories producing regulator EDD deliverables*, *building permit expediting and code consulting firms*, *federal construction contractors on NAVFAC/USACE projects* (UFGS submittal register), and *title abstracting*.

**Pattern 2 — Per-assignment (not per-employee) compliance re-trigger.** Where obligations attach to each engagement rather than to the person or the year, general-purpose master-record systems systematically under-serve. Transfers to: *construction subcontractor project management at 15-150 employee specialty trades*, *electrical or plumbing trade subcontractor field operations*, *DOT compliance consultancies and third-party safety managers serving small fleets*, and *contract manufacturers serving FDA-regulated medical devices* (per-lot rather than per-product records).

**Pattern 3 — True-cost quoting calculator that models the burden the incumbent calculator omits.** Every service business with a markup convention has a gap between markup and true margin, driven by costs that are ceiling-dependent, experience-rated, or deferred. Transfers to: *machine shop / job shop quoting*, *general contractor preconstruction and estimating*, *third-party truck dispatch services*, *small motor carriers*, and *marketing and creative agency account and production management*.

**Pattern 4 — Two-source reconciliation where the counterparty owns the invoice (self-billing).** Whenever the payer generates the billing document, the supplier's system becomes a challenger and reconciliation is permanent. Transfers to: *freight brokerage and dispatch operations* (carrier settlement), *medical billing* (835/ERA to charge matching), *warehouse and 3PL fulfillment document control*, *industrial distributors and metal service centers*, and *submetering and utility expense recovery service providers*.

**Pattern 5 — Expiry-and-eligibility guard: credential × requirement-profile × scheduled date.** The three-way join that spreadsheets cannot express, wherever people or equipment must be qualified for a specific job at a specific future time under a customer-specific rule set. Transfers to: *welding inspection (AWS CWI) and NDT service providers*, *calibration and metrology service providers / in-house gage management*, *special inspection agency accreditation consultants*, *DOT compliance consultancies* (driver qualification files), *radiation safety officer services and portable gauge licensee compliance*, and *Title 24 acceptance test technicians*.

**Pattern 6 — Jurisdictional document generator driven by a maintained rules table.** Deterministic assembly of the correct forms, in the correct language, for the correct jurisdiction, with change detection and an issuance log. Transfers to: *HR and benefits administration in companies under 200 employees*, *payroll service bureaus and small independent payroll providers*, *community association (HOA and condominium) management back office* (statutory notices), *multi-state charitable solicitation registration compliance*, and *estate planning and probate practice*.

**Pattern 7 — Expected-deduction netting: distinguishing structural short-pays from genuine disputes.** Where a counterparty routinely remits net of contractual deductions, aging at gross makes every payment look like a dispute. Transfers to: *independent pharmacy third-party reconciliation and PBM claw-backs*, *freight bill audit and payment for small shippers*, *retail shopping center management — percentage rent*, and *e-commerce accounting specialists* (settlement reconciliation).

---

## 8. Sources and confidence

### Verified findings — primary or regulatory sources

| Finding | Source |
|---|---|
| Joint Commission HCSS-6/HCSS-7 make personnel-file completeness a monthly-collected, quarterly-reported certification metric; **expired = missing** | [HCSS-6](https://manual.jointcommission.org/releases/HCSS2026A/MIF0125.html) · [HCSS-7](https://manual.jointcommission.org/releases/HCSS2026B/MIF1358.html) · [Introduction](https://manual.jointcommission.org/releases/HCSS2026B/IntroductionHCSS.html) · [Competency data element](https://manual.jointcommission.org/releases/HCSS2026A/DataElem0179.html) · [Review Process Guide 2026](https://digitalassets.jointcommission.org/api/public/content/98126fe27d044380ac507cbc816413d1?v=0b97856f) |
| Fieldglass self-billing: supplier invoices auto-created on approval; no Ariba invoices for Fieldglass orders | [SAP Fieldglass supplier FAQ](https://assets.cdn.sap.com/agreements/supplier-portal/fieldglass-supplier-enablement/sap-suppliers-faqs-englishglobal.pdf) |
| Beeline reconciliation requires Excel export to see supplier reference fields; remittance references IQN invoice number | [Beeline supplier job aid](https://webapps.beeline.com/beelinetms/!_IQN_ShellJobAids/SupplierOrganizationInvoiceReconciliationReport-SupplierJobAid.pdf) |
| Published, machine-checkable invoice rejection codes (R1–R36) | [Georgia-Pacific supplier portal](https://www.gp.com/georgia-pacific-supplier-portal/invoice-rejections) |
| Duplicate invoice numbers absolutely rejected; 3 attachments, TIFF only, 24-hour window | [Tungsten/Apple supplier FAQ](https://www.tungsten-network.com/customer-campaigns/apple/faqs-and-documentation/) |
| Kelly Services global DSO **59 days** (Q2 2025 and YE 2024) on $1.2B trade AR | [Kelly Services Form 10-Q](https://ir.kellyservices.com/static-files/8f1ca1d3-9a9a-490d-ac52-134fc8582a83) |
| Factoring terms actually signed: 80% advance, 1.80%/30 days then 0.65%/10 days, 10% missing-notation fee, $1,000/day field exams, repurchase on any disputed receivable | [SEC-filed factoring agreement](https://www.sec.gov/Archives/edgar/data/1665300/000121390018004257/fs42018ex10-17_stellaracq3.htm) |
| Leased workers classified as the client's direct employees would be; separate payroll records per code required | [NCRB Basic Manual Rule 1](https://www.ncrb.org/digitallibrary/basicmanual/Rule_1_-_Assignment_of_Classifications.htm) |
| CA §2810.5 requires client legal-entity disclosure and 7-day change notice | [Statute](https://codes.findlaw.com/ca/labor-code/lab-sect-2810-5/) · [DLSE form](https://www.dir.ca.gov/dlse/lc_2810.5_notice.pdf) |
| NY LS 51 is a dedicated temp-help notice; primary-language requirement | [NY DOL](https://dol.ny.gov/notice-pay-rate) |
| Illinois DTLSA: 720-hour equal pay, comparator disclosure, $3,000+$750 registration, $500/day unregistered penalty | [Jackson Lewis](https://www.jacksonlewis.com/insights/illinois-amends-temp-worker-law-boosting-employer-obligations) · [Illinois DOL](https://labor.illinois.gov/laws-rules/fls/day-temporary-labor.html) |
| ICE eliminated the I-9 10-day cure period on 2026-03-16; $288–$2,861 per form | [Morgan Lewis](https://www.morganlewis.com/pubs/2026/04/ice-rewrites-the-rules-on-form-i-9-violations) |
| 2026 ACA penalties: §4980H(a) $3,340, §4980H(b) $5,010; 1095-C penalties to $340/form; e-file at 10 returns | [Thomson Reuters / Rev. Proc. 2025-26](https://tax.thomsonreuters.com/news/irs-announces-increases-for-2026-aca-employer-shared-responsibility-penalties/) · [BDO](https://www.bdo.com/insights/tax/employer-filing-obligations-and-penalty-exposure-for-late-or-missing-affordable-care-act-forms) |
| Staffing-firm safe harbor requires a **higher fee** for enrolled employees — forces a two-tier bill rate | [Newfront, quoting §54.4980H-4(b)(2)](https://www.newfront.com/blog/aca-employer-mandate-and-outside-staffing-firms-2) |
| Break-in-service: 13-week rule, rule of parity, periods continue as if never left | [26 CFR 54.4980H-3](https://www.ecfr.gov/current/title-26/chapter-I/subchapter-D/part-54/section-54.4980H-3) · [AssuredPartners summary](https://www.assuredpartners.com/-/media/Files/Corporate/EB-Compliance-Documents/50-99-Employees/Column-1/ACA---Lookback-and-Variable-Hour/Break-in-Service-Rules-Summarized.pdf) |
| OSHA joint responsibility; duty to inquire into worksite conditions; 15 TWI bulletins | [OSHA Temporary Worker Initiative](https://www.osha.gov/temporaryworkers) · [TWI Bulletin No. 1](https://www.osha.gov/sites/default/files/OSHA_TWI_Bulletin.pdf) |
| WH-347 filed weekly; DOL's own burden estimate **55 minutes per form**; §1001 criminal exposure | [DOL WH-347](https://www.dol.gov/agencies/whd/forms/wh347) |
| Per diem must be **separately stated on each invoice**, never blended into the billed pay rate | [SIA *Staffing Stream*](https://www.staffingindustry.com/editorial/staffing-stream/are-you-accounting-your-diems-correctly) |
| Industry scale: ~27,000 firms, ~54,000 offices, 2.2M weekly workers (2024), 12.7M hired (2023), sector mix | [ASA statistics](https://americanstaffing.net/research/fact-sheets-analysis-staffing-industry-trends/staffing-industry-statistics/) |
| Bullhorn SMB pricing $99–$165/user/mo with **back office priced separately as an add-on** | [Bullhorn small-agency pricing](https://www.bullhorn.com/small-agency-software/pricing/) |
| Tracker: back-office historical data (timesheets, invoices, shifts) only in the Enterprise onboarding tier; $250/file direct imports | [Tracker implementation](https://www.tracker-rms.com/implementation/) |
| Recruiter guarantee periods: 90 days 44.9%, 30 days 20.3%, 60 days 20.0%; replacement-only 61.4% | [Top Echelon poll](https://topechelon.com/blog/recruiter-guarantees-once-i-am-paid-i-do-not-refund-any-money/) |

### Strong inferences — practitioner testimony and consistent multi-source triangulation

- **Excel is the universal gap-filler.** Not directly surveyed, but converged on from four independent directions: named Capterra/G2 reviewers describing specific module holes (Avionté A/R cannot produce a multi-line-item invoice; TempWorks reports must be custom-built); "Excel" as a listed requirement in a Revenue Specialist job posting; Beeline's own documentation directing users to Excel export; and the existence of a dedicated "Timesheet Verification team" as an escalation target. [Capterra Avionté](https://www.capterra.com/p/76635/Avionte-for-Staffing-Firms/reviews/) · [G2 TempWorks](https://www.g2.com/products/tempworks-software/reviews?qs=pros-and-cons) · [Insight Global Revenue Specialist](https://www.themuse.com/jobs/insightglobal/revenue-specialist-vms) · [Insight Global A/R Billing Specialist](https://www.themuse.com/jobs/insightglobal/ar-billing-specialist-a39d1f)
- **Timesheet approval routinely slips 2–4 days past period end** — inferred from a tooling configuration that ships three consecutive weekday approver-reminder cycles as the default. [TalentLaunch FAQ](https://support.mytalentlaunch.com/support/solutions/articles/8000004425-bullhorn-time-expense-operating-companies-faq)
- **WC misclassification is the highest single-event dollar exposure** — three documented cases ($80k, business-ending, $620k) from a broker paper distributed by a state staffing association. Broker-authored, but association-distributed and consistent with the rating-bureau rule. [MSA class code paper](https://msastaffing.org/wp-content/uploads/2024/09/Staffing-Company-Class-Codes-A-Shot-in-the-Dark-RS.pdf)
- **VMS billing reconciliation is a real, expensive, unsolved problem for firms below enterprise scale** — inferred from the existence and 2025 acquisition of a product built solely to solve it, plus a named-role customer quote. [EIN Presswire](https://www.einpresswire.com/article/908787891/laboredge-acquires-reconciled-eliminating-revenue-leakage-and-manual-vms-billing-burden-for-staffing-agencies) · [SIA](https://www.staffingindustry.com/news/global-daily-news/laboredge-acquires-reconciled)
- **Commission runs consume 12 hours to 4 days per cycle at real named firms.** Extracted from a commission vendor's case studies — the vendor is selling, but the firms and their reported figures are their own. [QCommission](https://www.qcommission.com/industries/industries-four/staffing-overview.html)
- **Outsourced back-office / factoring costs 1–5% of invoice value.** Two independent providers publish the same range; nobody publishes actual rate cards. [Signature](https://signaturebackoffice.com/factoring-for-staffing-firms/) · [Madison Resources](https://madisonresources.com/payroll-funding-and-back-office-support-faqs/)
- **SUTA hits staffing structurally harder than other employers** because churn prevents workers from reaching the wage ceiling. Vendor-stated, but arithmetically self-evident. [Madison Resources](https://madisonresources.com/why-suta-rates-hurt-low-skilled-staffing-agencies/)

### Tentative hypotheses requiring practitioner validation

1. **How agencies actually track credential expirations today.** Every search returned vendors selling the replacement. The density of that vendor market is circumstantial evidence that spreadsheets are the incumbent, but **there is no defensible statistic.** This is the highest-priority gap and it directly gates opportunity A4.
2. **Timesheet capture channel mix** (paper vs. email vs. photo vs. VMS vs. client punch). No credible survey found.
3. **Whether overtime is conventionally billed at 1.5× bill rate or at bill rate plus a 1.5× pay premium.** No authoritative source found; the answer changes the margin math in A1.
4. **Per-facility compliance packet variability** — how many distinct facility profiles a mid-size healthcare staffing agency maintains, and how often they change. Searches collided with *payer* credentialing (a different problem).
5. **Invoice rejection rates.** The rules are published; the frequency is not. A3's ROI depends entirely on this number.
6. **All quantified error and leakage rates** (the 5% revenue leakage, the 20–40 bps margin erosion, the 7–14 day DSO impact) trace to vendors with something to sell. **There appears to be no independent benchmark of staffing billing error rates, and that absence is itself a finding worth stating.** [SIA *Staffing Stream* / Hercules CFO](https://www.staffingindustry.com/editorial/staffing-stream/revenue-leakage-the-silent-threat-to-staffing-firm-margins)
7. **Who files WH-347 when a staffing firm supplies labor under a contractor's supervision.** Genuinely under-documented; a good primary-interview question.
8. **TWIC, badge/site-access and client safety-orientation expiry tracking** in light industrial — nothing found.

### Methodological limitations of this cycle

- **Reddit was completely inaccessible.** `reddit.com`, `old.reddit.com` and the JSON API all returned HTTP 403 from this environment; eleven Redlib/Libreddit mirrors were attempted, most dead or blocked, two behind proof-of-work challenges. LinkedIn post text was likewise unreachable. This removed the single richest source of unfiltered practitioner complaint. Substitutes used: SEC filings, buyer-published supplier rules, VMS vendor primary documentation, regulator forms, law-firm alerts, named-reviewer software criticism, and job postings. **Any future cycle touching a practitioner-heavy market should account for this constraint up front.**
- **Staffing Industry Analysts is largely paywalled.** In particular, the *Global Staffing Middle and Back Office Software Landscape 2026 Update* — built on survey responses from **39 middle/back-office products** — would answer the segmentation and adoption questions directly. [SIA report page](https://www.staffingindustry.com/research/research-reports/americas/global-staffing-middle-and-back-office-software-landscape-2026-update-ai-agents-and-the-digital-workforce) · The **VMS and MSP Fees survey** would replace the anecdotal 5% fee figure with a real distribution. [SIA fees survey](https://www.staffingindustry.com/research/research-reports/americas/vms-and-msp-fees-and-recommended-msps-survey-insights)
- **ASA's substantive ACA and HCSS material is member-only**, and the Joint Commission's HCSS certification fee page returned 403.
- **Back-office software pricing is almost entirely quote-gated.** Bullhorn is the only vendor publishing SMB pricing, and it explicitly excludes the back office from the published number.
