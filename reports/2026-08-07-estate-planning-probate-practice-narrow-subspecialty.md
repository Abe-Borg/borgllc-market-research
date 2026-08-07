# Estate Planning and Probate Practice — Narrow Subspecialty

## Decedent's Estate Administration and Court-Required Fiduciary Accounting

**Cycle date:** 2026-08-07
**Market:** Estate planning and probate practice
**Angle:** narrow-subspecialty
**Named niche:** the *post-death administration desk* — decedent's estate administration and the statutory fiduciary accounting filed with the probate court — at law firms of 1–15 attorneys, plus the professional fiduciaries and private trustees who serve the same estates
**Claim ID:** `a001b2b9`

---

## 0. Cycle header

### Why this assignment was chosen over the alternatives

At claim time the ledger held 20 completed reports across 20 markets, 296 backlog assignments, and zero live claims. The selection rules are (a) prefer markets with zero completed entries, (b) prefer assignments where strong practitioner evidence exists online, (c) prefer angles that increase catalog diversity.

157 backlog markets had zero completed entries, so criterion (a) alone did not narrow the field. Two secondary considerations decided it:

**Sector concentration.** The completed catalog is heavily weighted toward architecture/engineering/construction (fire protection, land surveying, HVAC/MEP, geotechnical labs, construction submittals, flood-zone consulting — six of twenty) and toward insurance/logistics/accounting. The entire legal sector had exactly one completed report (immigration law, core-practitioner-workflow). Adding a second legal market widens the catalog more than a seventh AEC market would.

**Angle balance.** Completed angles run: core-practitioner-workflow 7, back-office 5, handoffs-and-qa 4, narrow-subspecialty 4. `narrow-subspecialty` is tied for least-covered, and it is the angle that most rewards a market where a genuinely distinct sub-practice exists inside a broader one.

Within "Estate planning and probate practice," the post-death administration desk is a real and separable subspecialty. Estate *planning* (drafting wills and trusts) is a document-assembly business already well served by WealthCounsel, ElderCounsel, Wealth.com and Vanilla. Estate *administration* is a fundamentally different job: it is a multi-year, deadline-governed, court-supervised bookkeeping and reporting engagement with a statutorily prescribed output format. Those two halves are usually staffed by the same small firm and are frequently conflated in vendor marketing — which is precisely why the administration half is under-tooled.

I rejected three strong runners-up. *Small CPA tax preparation practices* has an unusually mature and inexpensive incumbent stack (Drake, UltraTax, Lacerte, SafeSend) that makes differentiation hard. *Dental and specialty clinic practice administration* is dominated by all-in-one PMS vendors whose gravity pulls every idea toward a platform. *Calibration and metrology services* is attractive but sits in the same manufacturing-quality cluster as three already-completed reports.

**Backlog after this claim:** 295 assignments remaining at claim time. See §9 for the post-run count after newly discovered markets are appended.

---

## 1. Market examined

### Industry and role

Post-death estate administration in the United States. The work is performed by:

| Actor | Typical org size | Role in this workflow |
|---|---|---|
| Small trusts & estates law firm | 1–15 attorneys, 1–6 support staff | Represents the personal representative (PR) / executor / administrator; prepares and files all court documents including the accounting |
| Trusts & estates paralegal | 1–3 per firm | Does the majority of the actual administration labor — asset schedules, transaction records, notice letters, deadline tracking, draft petitions |
| Licensed professional fiduciary / private trustee | 1–10 person shops | Serves *as* the fiduciary for unrelated or conflicted families; must produce the same accountings, often for many estates at once |
| Personal representative / executor | Individual, usually a family member | Signs the account under penalty of perjury; supplies the raw bank and brokerage statements |
| Outside CPA | 1–20 person firms | Form 1041 fiduciary income tax return; Form 706 when required; coordinates date-of-death valuation |
| Probate referee (California) | State-appointed individual | Appraises non-cash, non-quoted assets; paid 0.1% of appraised value, $75 minimum |
| Probate examiner (court staff) | Public sector | Reviews every petition before hearing and publishes written defect notes |

### Why the target user is the small firm, not the large one

Large trusts & estates departments at AmLaw firms and bank trust departments already run TEdec, Lackner Group's 6-in-1, or Gillett's GEMS, and have dedicated fiduciary accountants. The economics below explain why the small firm cannot.

California Probate Code §§10800 and 10810 set an identical statutory fee schedule for the personal representative and for the attorney, computed on the **gross** estate value with no deduction for mortgages or debts: 4% of the first $100,000, 3% of the next $100,000, 2% of the next $800,000, 1% of the next $9,000,000, 0.5% of the next $15,000,000. A $1,000,000 gross estate yields $23,000 to the attorney and $23,000 to the PR. That fee is **capped, but the work required to earn it is not**. A professional-fiduciary firm writing about the same problem puts it bluntly: on an $850,000 estate generating roughly a $20,000 statutory gross fee, at ~50% overhead the theoretical $10,000 of profit "evaporates" once the attorney also performs the administrator's duties — "the attorney often ends up doing two jobs but can only charge one fee."

Two consequences follow, and both define the buying behavior of this market:

1. **Every hour of administrative drudgery is unbillable margin destruction**, not billable revenue. This is the opposite of litigation practice and it makes small probate firms unusually receptive to narrow time-saving tools — and unusually hostile to per-seat SaaS with a long onboarding.
2. **The labor is scarce and expensive.** Legal recruiters report that trust & estate administration paralegal roles carry a **30.9% pay premium** over general-practice paralegal roles because the skillset is niche and experienced candidates are mostly passive. A tool that lets a general paralegal do administration-desk work has direct, quantifiable value.

### Market size signal

Probate is a volume business at the low end. California raised its small-estate affidavit ceiling to **$208,850** effective April 1, 2025 (Prob. Code §13100, inflation-adjusted every three years), which means every estate above that line — a very large population, since a single modest home clears it — is pushed into full administration. Florida's summary-administration ceiling is $75,000. Texas allows independent administration with an affidavit in lieu of inventory. The result is thousands of small firms nationwide each carrying a rolling caseload of open estates.

---

## 2. How the work is performed

### 2.1 The administration lifecycle

The sequence below is California-centric because California is the most form-rich jurisdiction and the one whose statutory accounting format is most explicitly codified. Equivalents in Michigan, Florida, Texas, New York and Ohio follow.

**Open the estate.** Petition for Probate (DE-111) → Notice of Petition to Administer Estate (DE-121), mailed to all heirs and beneficiaries and published in a newspaper of general circulation → Order for Probate (DE-140) → Letters (DE-150) issue, together with Duties and Liabilities of Personal Representative (DE-147). The PR is now empowered to act.

**Notice creditors.** Publication plus actual notice to *known or reasonably ascertainable* creditors — a constitutional requirement since *Tulsa Professional Collection Services v. Pope*, 485 U.S. 478 (1988). California bars most claims **four months after Letters issue** (Prob. Code §9100). Michigan runs a **four-month** window from publication (MCL 700.3801/3803). Florida runs **three months from first publication**, with known creditors getting **30 days after service** (Fla. Stat. §§733.702, 733.2121).

**Inventory and appraise.** In California, Inventory and Appraisal (DE-160) plus Attachment (DE-161) is due **within four months of Letters** (Prob. Code §8800). Attachment 1 lists assets the PR may value itself — cash, bank deposits, and publicly traded securities with quoted market prices. Attachment 2 lists everything else and goes to a **probate referee**, who is assigned by rotation from a county roster maintained by the State Controller (the executor does not choose one), and who charges 0.1% of appraised non-cash value with a $75 minimum. Deadlines elsewhere: Michigan **91 days** from appointment (MCL 700.3706); Texas **90 days** from qualification (Estates Code §309.051), or an Affidavit in Lieu of Inventory under §309.056 for independent administrations with debts satisfied; Florida **60 days** after Letters (Fla. Prob. R. 5.340).

**Administer.** Open the estate bank account and obtain an EIN (IRS Form SS-4). Collect income. Pay debts, funeral expenses, taxes. Sell real property or securities (California: Report of Sale and Petition for Order Confirming Sale, DE-260; Order Confirming Sale, DE-265; Notice of Proposed Action, DE-165, for certain acts). Handle creditor claims (DE-172). File Form 1041 for each fiduciary tax year the estate has income; file Form 706 if required.

**Account.** This is the subspecialty's defining artifact and is treated separately in §2.2.

**Close.** Petition for Final Distribution (no statewide Judicial Council number in California; local pleading paper, e.g. San Diego local form PR-165) → order → distribute → collect a signed **distributive receipt** from every distributee → Ex Parte Petition for Final Discharge and Order (DE-295/GC-395), which discharges the PR and exonerates the bond. California requires the petition for final distribution or a status report **within one year of Letters**, extended to **18 months if a Form 706 is required** (Prob. Code §12200). Ohio requires a first and final account **within six months** of appointment with a 13-month outer limit absent statutory exceptions (R.C. §2109.301).

### 2.2 Mechanics of the accounting itself

This is the heart of the subspecialty and the place where the software gap is widest.

**The balancing rule is statutory, not conventional.** California Probate Code §1061(b) prescribes a summary format organized into CHARGES (property on hand at start, additional property received, receipts, gains on sale, net income from trade or business) and CREDITS (disbursements, losses on sale, net loss from business, distributions, property on hand at end), and §1061(c) states flatly: *"Total charges shall equal total credits."* Every jurisdiction examined implements the same identity in different clothing:

- **Michigan** PC584 (Account of Fiduciary, Long Form): *Beginning Balance + Schedule A (Income & Gain) − Schedule B (Expenses, Losses, Disbursements) = Schedule D (Itemized Remaining Assets)*, with Schedule C carrying asset-disposition detail — acquisition date, sale date, original value, proceeds, gain/loss.
- **Florida** Fla. Prob. R. 5.346 (built on the ABA/AICPA National Fiduciary Accounting Standards): Schedule A Receipts, B Disbursements, C Distributions, D Capital Transactions and Adjustments, E Assets on Hand at close.
- **New York** Surrogate's Court judicial accountings: Schedules A through K, with principal and income tracked in parallel series (A/A-1/A-2, E/E-1, G/G-1) and separate schedules for creditor claims (D), new investments (F), commissions (I), cash reconciliation (J), and estate tax allocation (K).

**Two value bases must be carried simultaneously.** California §1062 requires the property-on-hand schedule to state each item at its **carry value**, while §1063 separately requires a schedule of **estimated market values** at the period end. Florida Rule 5.346(b)(4) requires the closing asset schedule to show **both** "asset acquisition value or carrying value, *and* estimated current value." A stock position bought by the decedent in 1994, stepped up at death, partially sold during administration, and still partly held at period end therefore appears in at least three places with two different numbers.

**Principal and income must be allocated.** The Uniform Principal and Income Act (and its successor, the Uniform Fiduciary Income and Principal Act) is adopted with state variations in California, Michigan (Act 159 of 2004), New York, Washington (RCW 11.104B) and most other states. Dividends, interest, rent and business income are income; sale proceeds, the corpus, and most capital items are principal. Depreciation reserves, ordinary vs. extraordinary distributions, and the treatment of unitrust conversions all turn on statute. This allocation is genuine professional judgment; it is not something a tool should decide for the practitioner.

**Florida adds a readability mandate.** Rule 5.346 requires the account to be "understandable to persons not familiar with practices and terminology peculiar to the administration of estates." In practice this means the practitioner produces the technical schedules *and* a plain-language explanation.

### 2.3 Where the data actually comes from

The inputs to the accounting are the estate's bank and brokerage statements for the full accounting period, plus the firm's own record of disbursements. Every deposit, withdrawal, trade, fee and transfer must be classified into a schedule and itemized with payee name (California §1062 requires "itemized receipts, disbursements with payee names"). The beginning and ending balances then have to tie to the summary.

**This conversion is manual or semi-manual at the small-firm level.** The evidence is triangulated rather than directly surveyed:

- Estateably, a modern cloud estate-administration platform, ships a documented "Import CSV or Excel transactions" feature — meaning that even in a purpose-built 2020s SaaS product, the normal path is exporting from the bank and importing a file, not an integrated feed.
- EstateExec markets direct bank-transaction import that "automatically identifies distributions, debt payments, etc." as a *differentiator*, which only makes sense if the alternative is hand entry.
- EstateLedger, a newer entrant, positions itself explicitly against manual methods, claiming to "audit what the bank says actually happened" and reconcile "to the penny."
- The ACTEC Foundation — the leading professional organization of trust and estate counsel — distributes **Quicken templates** to produce accountings conforming to national fiduciary accounting standards. That the top professional body's answer is consumer-grade personal-finance software with custom templates is the single most telling artifact in this market.
- Free "Probate Accounting Spreadsheet" Excel templates circulate widely and are indexed on general template sites.

### 2.4 Software currently in use

| Product | What it is | Position in the workflow |
|---|---|---|
| Lackner Group **6-in-1** (since 1986) | Desktop estate & trust administration; Forms 1041, 706, 709, state death tax, state inventory and accounting documents | The deep incumbent for tax-heavy estates; sold heavily to CPAs |
| Gillett Publishing **GEMS** | Dedicated estate/trust accounting built to National Fiduciary Accounting Standards, with state modules including California | Fiduciary accounting specialist tool |
| **TEdec** | Long-tenured desktop estate administration system; recently added embedded EVP valuations | Same tier as above |
| **Estateably** | Cloud estate administration; CSV/Excel transaction import, document generation | Modern entrant |
| **EstateExec** | Executor-facing with a "for Lawyers" tier; bank transaction import, inventory and accounting reports | Straddles consumer and professional |
| **EVP Systems / EstateVal** | Date-of-death and alternate-date securities valuation for Form 706; mean pricing, accrued dividends and interest; billed **per security**, no setup or minimum; calculations run locally so portfolio data never leaves the firm | Narrow, mature, cheap, well-loved — a model for what this catalog should build |
| **Clio, MyCase, Smokeball, Actionstep, PracticePanther, CARET, LEAP** | General practice management | Matter, time and document management; their "trust accounting" is IOLTA compliance, **not** estate court accounting |
| **Quicken + ACTEC templates**, Excel, Word | Improvised | The realistic default at firms below the GEMS/6-in-1 threshold |

**Notably absent from any of these:** none of the general practice-management products produce a statutory fiduciary account. Reviewers say so directly. On G2, a Clio Manage user at a small firm writes: *"My prior practice management had a very robust accounting software built in, and Clio doesn't have that"* — requiring a separate accounting product "which kind of duplicates the work"; other reviewers flag that reporting "features are not detailed enough" and that reconciling old accounts is hard. Actionstep reviewers on Capterra describe setup as *"perfect and functionality outstanding, IF YOU HAVE AN IT DEGREE AND 1000hrs to set it up"* and note that *"the accounting reports cannot be changed and at times the accounting functions don't work the way we would want them to."*

**The dedicated fiduciary-accounting vendors have essentially no third-party review footprint.** Targeted searches across G2, Capterra and Trustpilot returned no independent user reviews for TEdec, Lackner 6-in-1, or GEMS — only vendor pages, LinkedIn and press releases. For practice-area software this absence is itself diagnostic: these are entrenched, aging, low-competition desktop products serving a small insular base.

---

## 3. Most important problems, ranked

### P1 — Converting raw bank and brokerage activity into statutory schedules is hand labor, and it is the largest single time sink in the engagement

**Who:** the trusts & estates paralegal, and the professional fiduciary managing many estates at once.
**When:** at every accounting period — often annually for supervised estates and conservatorships, and always at final accounting.
**Currently handled by:** exporting or retyping statement lines into Excel or Quicken, classifying each into a schedule, then hand-reconciling to make charges equal credits.
**Why inadequate:** the classification is repetitive and mechanical, but the arithmetic is unforgiving — a single misclassified $412 transfer breaks the statutory identity and the whole account must be re-footed. The dual carry-value/market-value requirement means the same asset must be tracked in two bases across the period. Errors surface only at the end, when the summary refuses to balance.
**Frequency:** every estate, every period, for the life of the engagement.
**Cost:** unbillable against a capped statutory fee, absorbed as margin. Against an attorney fee capped at $23,000 on a $1M estate, and a paralegal commanding a 30.9% market premium, hours here are the most expensive hours in the practice.
**Evidence:** California Prob. Code §§1061–1063 (itemization, dual valuation, balancing identity); Florida Prob. R. 5.346; Michigan PC584 schedule structure; the existence and marketing positioning of Estateably's CSV import, EstateExec's bank import and EstateLedger's "reconciled to the penny" pitch; ACTEC's Quicken templates. **Verified as a structural requirement; the per-estate transaction count is not published anywhere I could find and would need practitioner interviews to size.**

### P2 — Probate examiner notes create a rejection-and-supplement loop with real calendar cost, and the defect corpus is public but unmined

**Who:** the attorney and paralegal who filed the petition.
**When:** days before every noticed hearing.
**Currently handled by:** checking the county's probate-notes web page, reading free-text defect notes, drafting a supplement, and filing before a hard cutoff.
**Why inadequate:** timing is brutal and county-specific. Los Angeles Superior Court posts notes roughly two weeks ahead with a "Matters To Clear" section and requires corrections to be **filed by the third court day preceding the hearing**, or the court will continue, take the matter off calendar, or deny without prejudice — and the examiner email address is explicitly *not* for arguing the merits. Orange County posts notes as little as **24–72 hours** ahead. Missing the window costs a continuance measured in weeks, which cascades into the §12200 one-year closing deadline.
**Frequency:** notes are generated for effectively every petition; the question is whether they contain clearable defects.
**Cost:** each continuance is a re-noticed hearing, a re-drafted supplement, a delayed distribution, and an unhappy client who is already in a billing-sensitive posture. In one practitioner's words, probate clients suffer "billable hour shock."
**Evidence:** LA Superior Court's own Probate Notes system documentation; Merced County's published probate notes PDFs, which contain verbatim defect language — e.g., *"Distributive Receipts and an Ex Parte Petition For Final Discharge And Order (DE-295) have not been submitted"* and *"No Notice to all heirs, beneficiaries & executors"* / *"Proposed Order for Probate has not been lodged."* **Verified.** Note that a widely-circulated blog statistic breaking LA deficiencies into "Missing Documents 60% / Procedural Errors 25% / Incorrect Information 15%" carries no methodology and should be treated as marketing content, not data.

### P3 — Trusts and estates is now the highest-risk practice area for legal malpractice, and the dominant error types are the ones software can address

**Who:** the firm and its malpractice carrier.
**When:** discovered years later, often by a beneficiary.
**Currently handled by:** attorney diligence, tickler files, and hope.
**Why inadequate:** the ABA's *Profile of Legal Malpractice Claims, 2020–2023* moved estate/trust/probate to the **highest-risk practice area**, up from fourth in the prior study period, attributed to the aging population and the largest intergenerational wealth transfer in US history. The historical trend is consistent: T&E claims rose from under 7% of national malpractice claims in 1985 to 10.7% by 2011. The error-type breakdown for T&E claims is: **attorney-client communication errors 33%, inadequate investigation 25%, errors of law 16%, time-related errors 8%, clerical errors 8%, conflicts 6%**. ALPS reported estate/trust/probate claims rising a further 1.6% in 2024, citing improper titling of assets, unrecorded deeds, and **missed tax filing deadlines**.
**Frequency:** rising.
**Cost:** the Ohio Bar Liability Insurance Company reports that roughly **70% of estate-planning malpractice claims close with zero loss payment — but average defense cost still runs about $30,000**, because these claims are fact-specific and not amenable to motion practice. A small firm can therefore "win" and still lose a paralegal-year of revenue.
**Evidence:** ABA Profile of Legal Malpractice Claims 2020–2023 (via trade press); Lawyers Mutual NC historical series; ALPS 2024 claims trends; OBLIC risk bulletin. **Verified.** No source isolates "missed 706/portability deadline" or "missed creditor-claim deadline" as a standalone claim category; those fold into the calendar and substantive-law buckets.

### P4 — Deadline calendaring is jurisdiction-specific, date-derived, and re-derives on every change

**Who:** paralegal, attorney.
**When:** at appointment, and again every time a controlling date moves.
**Currently handled by:** Outlook reminders, a paper checklist, or the practice-management system's generic task list.
**Why inadequate:** the deadlines are *computed*, not fixed — four months from Letters, 91 days from appointment, 60 days from Letters, three months from first publication, one year from Letters unless a 706 is required in which case eighteen. Each state's arithmetic is different, several counties add local rules on top, and if the date of Letters changes because the hearing was continued (see P2) every downstream date moves. General legal calendaring products are built around litigation rules engines and do not ship probate rule sets for most counties.
**Frequency:** continuous, per matter.
**Cost:** "time-related errors" are 8% of T&E malpractice claims, and missed tax filing deadlines are called out explicitly by ALPS.
**Evidence:** Prob. Code §§8800, 9100, 12200; MCL 700.3706, 700.3801; Fla. Prob. R. 5.340, Fla. Stat. §733.702; Tex. Est. Code §309.051; Ohio R.C. §2109.301. **Verified as to the rules; the failure rate is inferred from the malpractice error-type data.**

### P5 — The Form 706 / portability decision is a cheap-now, catastrophic-later election with a long but finite cure window

**Who:** attorney, with the CPA.
**When:** within nine months of death, or under the simplified relief procedure within five years.
**Currently handled by:** professional judgment plus a calendar entry, and a client letter if the firm is careful.
**Why inadequate:** for a surviving-spouse estate below the filing threshold, no 706 is *required* — so nothing forces the question — but failing to file loses the deceased spouse's unused exclusion permanently. **Rev. Proc. 2022-32** extended automatic simplified relief from two years to **the fifth anniversary of the date of death**, for estates of decedents dying after December 31, 2010 who were survived by a spouse and were not otherwise required to file; the return must carry a statement that it is filed pursuant to the revenue procedure. The IRS extended the window precisely because it was drowning in private letter ruling requests from estates that missed it. If the estate turns out to have been required to file, the relief is void.
**Frequency:** every surviving-spouse estate, which is a large fraction of the caseload.
**Cost:** at 2026 exclusion levels a lost DSUE is a seven-figure exposure for the surviving spouse's eventual estate. This is a textbook malpractice fact pattern and it does not surface until the second death, often a decade later.
**Evidence:** Rev. Proc. 2022-32; Journal of Accountancy coverage. **Verified.**

### P6 — Distribution mechanics and receipt collection: one holdout stalls the entire close

**Who:** paralegal, attorney, and the PR who wants to be discharged.
**When:** at the very end, when the client believes the matter is over.
**Currently handled by:** a spreadsheet of distributees, hand-computed fractional shares, mailed receipt-and-release forms, and follow-up phone calls.
**Why inadequate:** the arithmetic itself is error-prone once specific bequests, abatement, per stirpes representation, and residuary fractions interact — and California discharge (DE-295) is not available until distributive receipts are on file. Washington practitioners describe receipt-and-waiver collection as *"an 'all or nothing' situation"*: if one beneficiary declines to sign, closing "necessitat[es] substantially more paperwork, mailing, and filing" and adds "a delay of approximately a month."
**Frequency:** every estate.
**Cost:** a month of carry per stalled estate, plus the reputational cost of a matter that will not die.
**Evidence:** wa-probate.com practitioner guidance; Merced County probate notes citing missing distributive receipts as a live defect. **Verified.**

### P7 — Asset discovery is a diligence obligation whose defensibility depends on documenting the search, not just its result

**Who:** paralegal, PR.
**When:** early administration, and again whenever a stray statement arrives.
**Currently handled by:** asking the executor for statements, opening mail, and reacting.
**Why inadequate:** "inadequate investigation" is the **second-largest** category of T&E malpractice claims at 25%. OBLIC's bulletin lists inadequate investigation of assets, prior wills and family relationships among the common triggers, along with failing to confirm the estate has adequate money to pay claims and taxes. Meanwhile *Tulsa Professional Collection Services v. Pope* makes actual notice to *reasonably ascertainable* creditors a due-process requirement — which is itself a search obligation. There is no artifact in the ordinary file that proves the search was performed.
**Frequency:** every estate.
**Cost:** the exposure is the malpractice claim, and defense costs average ~$30,000 even when the claim pays nothing.
**Evidence:** ABA error-type breakdown; OBLIC; *Pope*, 485 U.S. 478. **Verified as to the obligation and the claim statistics; the absence of a diligence artifact in the typical file is inferred.**

### P8 — Beneficiaries objecting to accountings hit the same recurring defects

**Who:** the fiduciary and the drafting firm.
**When:** in contested administrations.
**Currently handled by:** litigation.
**Why inadequate:** a California trust-litigation firm reports recurring objection patterns that "appear repeatedly across contested trust administrations": accountings that "omit beginning or ending balances, combine multiple categories into single line items, fail to reconcile income and expenses, or exclude supporting documentation," undocumented fiduciary reimbursements, and "accounts that disappear between accounting periods." Every one of those is a *format and completeness* defect detectable before filing.
**Frequency:** unknown; the source describes patterns, not rates.
**Cost:** surcharge exposure to the fiduciary and fee exposure to the firm.
**Evidence:** practitioner-authored litigation guidance. **Verified as pattern description, not as frequency.**

---

## 4. Application opportunities

### A1 — **ScheduleForge**: bank and brokerage activity → statutory fiduciary accounting schedules

**Intended user:** trusts & estates paralegal; professional fiduciary.
**Problem solved:** P1.
**Current workflow:** download or retype statement lines into Excel; classify each by hand; build the summary; discover it does not balance; re-foot.
**Proposed workflow:** drop in CSV/OFX/QFX exports (and PDF statements where no export exists) for the accounting period → the tool normalizes and de-duplicates transactions → proposes a schedule classification per line (receipt of principal, receipt of income, disbursement, distribution, gain on sale, loss on sale, non-cash transfer) using rules plus a learned payee memory → the user confirms or corrects in a single scrolling review pane → the tool emits the jurisdiction's schedule set and a summary that provably balances, plus a carry-value register for the property-on-hand schedules.
**Inputs:** period start/end dates; opening carry-value register; transaction files; a small chart of estate-specific payees.
**Outputs:** Schedules in the target format (California GC-400/405 series; Florida Rule 5.346 A–E; Michigan PC584 A–D; New York A–K); a charges-equals-credits proof page; an exportable working ledger; a CSV the CPA can use for the 1041.
**Essential features:** rules-based classification with per-matter payee memory; explicit principal/income flag the user sets, never the software; dual carry-value and market-value tracking on every held asset; lot-level gain/loss on partial sales; hard balancing check that refuses to export an unbalanced account; full audit trail of every reclassification.
**Deliberately excluded from v1:** direct bank API connections (fragile, expensive, and a security liability); tax return preparation; trust accounting for ongoing trusts; document assembly of the petition itself; multi-user workflow.
**AI:** *optional and bounded.* Useful for (a) extracting transaction tables from PDF statements that offer no export, and (b) first-pass payee classification. **Every arithmetic operation must be conventional deterministic code**, and the balancing proof must be computed, not generated. A tool that hallucinates a number in a document signed under penalty of perjury is worse than no tool.
**Why a spreadsheet is insufficient:** a spreadsheet can hold the ledger but cannot enforce the carry-value/market-value duality across periods, cannot do lot-level basis tracking on partial sales, and cannot carry a prior period's ending register forward as the next period's opening register without manual re-keying — which is exactly where the errors enter.
**Complexity:** medium. **Learning difficulty:** low — the mental model is "bank register with a schedule column."
**Value:** the single largest labor block in the engagement, recurring annually per open matter.
**Risks:** decedent financial data is highly sensitive; the tool should default to local-only processing, following the EVP Systems model where "calculations are performed locally and no portfolio or decedent information is transmitted." State-by-state schedule format variation is the real implementation cost and must be data-driven, not hard-coded.
**Substitutes:** GEMS, 6-in-1, TEdec (heavy, desktop, no public review footprint, priced for higher-volume shops); Estateably and EstateExec (import exists but the products are platforms, not focused tools); Excel and ACTEC's Quicken templates (free but unenforcing).
**Why still attractive:** the incumbents are either full platforms or 1980s-era desktop suites. Nothing in the market is a narrow, free, open-source, locally-run converter that a firm can adopt in an afternoon without changing practice-management systems. The open-source base plus per-jurisdiction paid schedule packs is a natural business model.
**Customization potential:** very high — every state, and some counties, is a paid schedule module; professional fiduciaries with 40 open matters are a natural paid-support tier.

### A2 — **CrossFoot**: fiduciary account validator and reconciliation proof

**Intended user:** the attorney doing final review before filing; the fiduciary who signs under penalty of perjury.
**Problem solved:** P1 and P8, from the review side rather than the production side.
**Current workflow:** the attorney re-adds the schedules by hand or trusts the paralegal.
**Proposed workflow:** paste or import a completed accounting (from any source, including Excel or GEMS) → the validator cross-foots every schedule against the summary, checks that the prior period's ending property-on-hand equals this period's opening, confirms charges equal credits, flags any asset appearing in a market-value schedule but not the carry-value schedule (and vice versa), flags line items with no payee named, flags categories that have been combined, and flags assets that "disappear between accounting periods" → outputs a one-page reconciliation proof suitable for the file.
**Inputs:** a schedule set in CSV, XLSX, or a simple structured paste.
**Outputs:** pass/fail report with every exception located by schedule and line; a signed-off proof page.
**Essential features:** the exception rules above; zero dependence on how the account was produced.
**Excluded:** producing the account; legal advice about principal/income allocation.
**AI:** **inappropriate.** This is pure arithmetic and set logic. Introducing a model here would destroy the tool's only value proposition, which is that its output is trustworthy.
**Why a spreadsheet is insufficient:** the spreadsheet *is* the thing being checked; an independent checker is the point.
**Complexity:** small. **Learning difficulty:** minimal.
**Value:** converts a nervous manual re-add into a thirty-second check, and directly targets the objection patterns litigators say recur.
**Risks:** minimal. Local processing, no data retention.
**Substitutes:** none identified. This is a genuine white space.
**Customization:** exception rule sets per jurisdiction and per court examiner's known preferences.

### A3 — **NoteClear**: probate examiner note triage and supplement scaffold

**Intended user:** small-firm paralegal and attorney.
**Problem solved:** P2.
**Current workflow:** refresh the county's probate-notes page, read prose, manually enumerate defects, draft a supplement under a 72-hour-to-3-court-day clock.
**Proposed workflow:** paste the county's posted notes for the matter → the tool splits the free-text block into discrete numbered items, classifies each (notice defect, missing form, inconsistency across forms, proposed-order defect, missing receipt, accounting defect), maps each to the standard cure (which form, which declaration, whether re-notice is required and therefore whether the hearing must be continued regardless), computes the filing cutoff from the hearing date and the county's rule, and emits a supplement skeleton with one numbered response per note.
**Also — the more interesting half:** many counties publish their probate notes openly. A one-time scrape and classification of a county's published notes yields a **defect corpus** that becomes a *pre-filing* checklist: "in this county, these fifteen defects account for most notes; here is your packet checked against them."
**Inputs:** county, hearing date, the pasted notes text, optionally the filed packet's document list.
**Outputs:** an itemized cure list with deadlines; a supplement draft skeleton; a pre-filing checklist per county.
**Essential features:** county rule table for note-posting lead time and cure cutoff; note-to-cure mapping; the pre-filing checklist mode.
**Excluded:** e-filing; arguing the merits; anything that pretends to be legal advice.
**AI:** *optional and genuinely useful* for splitting and classifying unstructured examiner prose into discrete items — this is exactly the language-shaped task conventional code handles badly. Deadline arithmetic and the cure mapping stay deterministic.
**Why a spreadsheet is insufficient:** the input is unstructured prose on a clock.
**Complexity:** medium. **Learning difficulty:** low.
**Value:** each avoided continuance is weeks of calendar and a re-noticed hearing.
**Risks:** county practices change; the rule table needs maintenance and must show its "last verified" date. Do not scrape any court site that prohibits it — check each county's terms.
**Substitutes:** none. Firms do this by hand or pay document-prep services.
**Customization:** per-county corpora are the paid product; a firm's own historical notes are a paid private corpus.

### A4 — **ProbateClock**: jurisdictional deadline engine for estate administration

**Intended user:** paralegal, attorney, professional fiduciary.
**Problem solved:** P4.
**Current workflow:** manual Outlook reminders from a paper checklist.
**Proposed workflow:** enter state, county, date of death, date Letters issued, administration type (supervised/independent/summary), whether a 706 is required, and publication date → the tool computes every statutory date with its citation, exports an .ics calendar and a printable schedule, and **recomputes the whole chain when any controlling date changes**.
**Inputs:** the six or seven controlling dates and flags above.
**Outputs:** .ics file; PDF deadline schedule with statutory citations next to each date; a change log when dates move.
**Essential features:** citation next to every computed date; a visible "rules last verified" stamp per jurisdiction; recompute-on-change; court-holiday-aware date math.
**Excluded:** task assignment, matter management, time tracking — this is not a practice-management system.
**AI:** **inappropriate.** Statutory date arithmetic must be a rules table, verifiable by reading it.
**Why a spreadsheet is insufficient:** a spreadsheet can compute one state's dates; it cannot hold a maintained multi-jurisdiction rule set with citations, and it will not be updated when a statute changes.
**Complexity:** small core, medium if many jurisdictions ship. **Learning difficulty:** minimal.
**Value:** directly targets the 8% of T&E malpractice claims that are time-related, plus ALPS's "missed tax filing deadlines."
**Risks:** publishing legal deadlines invites reliance. Ship with an explicit non-advice disclaimer, per-rule citations so the user can verify, and dated rule provenance. This is a professional-liability-sensitive product and should be designed to be *auditable*, not authoritative.
**Substitutes:** litigation calendaring engines (CompuLaw, Deadlines.com) do not generally cover probate rules at the county level; practice-management task templates are static, not computed.
**Customization:** each additional state or county is a paid rule pack; firm-specific internal milestones layered on top.

### A5 — **PortabilityGuard**: 706-requirement determination and election documentation memo

**Intended user:** attorney; the CPA is a secondary user.
**Problem solved:** P5.
**Current workflow:** professional judgment, a calendar entry, and sometimes a client letter.
**Proposed workflow:** enter gross estate components, adjusted taxable gifts, surviving-spouse status, and date of death → the tool determines whether a 706 is *required* versus *portability-only*, computes the nine-month deadline, the six-month extension date, and the **Rev. Proc. 2022-32 fifth-anniversary** simplified-relief date, and produces a dated client memo recording the recommendation, the deadline, and the consequence of declining — which the firm keeps as its malpractice-defense artifact.
**Inputs:** a short structured questionnaire.
**Outputs:** determination sheet with citations; three computed dates; a client memo and a signed acknowledgment form.
**Essential features:** annually-updated exclusion amounts with effective dates; the required Rev. Proc. 2022-32 filing statement language; the client acknowledgment.
**Excluded:** preparing the 706 itself.
**AI:** **inappropriate.** Threshold arithmetic and a decision tree.
**Why a spreadsheet is insufficient:** the deliverable is the *documented advice*, not the number. The memo is the product.
**Complexity:** small. **Learning difficulty:** minimal.
**Value:** the failure mode it prevents is a seven-figure client loss discovered a decade later, and a malpractice claim whose defense alone averages ~$30,000.
**Risks:** exclusion amounts and revenue procedures change; hard-code nothing without an effective-date table. Must not read as tax advice to a consumer.
**Substitutes:** 6-in-1 and OneSource prepare the return but do not produce the *decision-and-documentation* artifact; nothing narrow exists.
**Customization:** firm-branded memo templates; state estate/inheritance tax overlays for the seventeen or so states that levy one.

### A6 — **ReceiptRunner**: distribution schedule builder and distributive-receipt tracker

**Intended user:** paralegal.
**Problem solved:** P6.
**Current workflow:** hand-built spreadsheet of distributees and fractions; mailed receipt forms; phone follow-up; a mental note about who has not signed.
**Proposed workflow:** enter specific bequests, the residuary structure (fractions or percentages, per stirpes or per capita), and the distributable balance → the tool computes each distributee's entitlement with abatement applied in statutory order, generates the distribution schedule for the petition, generates a receipt-and-release per distributee, and tracks signature status with automatic reminder letters → refuses to mark the matter closeable until every receipt is logged, because discharge (DE-295) depends on it.
**Inputs:** distributee list, bequest structure, distributable balance, in-kind assets with values.
**Outputs:** distribution schedule; per-beneficiary receipt forms; a signature status board; a "ready for discharge" gate.
**Essential features:** representation math (per stirpes/per capita); abatement ordering; in-kind distribution at carry and market value; the status gate.
**Excluded:** e-signature (integrate with whatever the firm already uses); beneficiary portal.
**AI:** **inappropriate.** Fractional arithmetic and document merge.
**Why a spreadsheet is insufficient:** the fraction math under representation and abatement is where errors hide, and a spreadsheet does not chase signatures.
**Complexity:** small. **Learning difficulty:** low.
**Value:** the Washington practitioner estimate of roughly a month of delay per non-signing beneficiary is the benchmark; earlier visibility into who has not signed pulls that forward.
**Risks:** distribution math has real consequences; every computation should show its work so the attorney can verify.
**Substitutes:** Word merge plus Excel. No focused tool found.
**Customization:** per-state receipt and release forms.

### A7 — **DiligenceLog**: defensible asset-search and creditor-notice record

**Intended user:** paralegal, attorney, professional fiduciary.
**Problem solved:** P7.
**Current workflow:** ad hoc; the file contains the results of the search but no record of the search.
**Proposed workflow:** work a structured checklist of asset and creditor search steps — state unclaimed property databases for every state of residence, prior-year tax return review, decedent credit report, safe deposit box inquiry, life insurance policy locator, employer/pension inquiry, mail hold review, known-creditor identification from statements and mail → each step is timestamped with who did it, what was searched, and what was found (including "nothing found," which is the entry that matters) → outputs a signed diligence memo for the file that demonstrates a reasonable search under *Pope* and against the "inadequate investigation" malpractice pattern.
**Inputs:** the checklist responses; states of residence and employment.
**Outputs:** dated diligence memo; a to-do list of unfinished steps; a known-creditor list feeding the notice-to-creditors mailing.
**Essential features:** timestamped step log; "nothing found" as a first-class recorded result; direct links to each state's unclaimed property portal; export of the known-creditor list.
**Excluded:** automated searching of third-party databases; anything requiring a credentialed data broker relationship.
**AI:** **optional and marginal** — could extract candidate creditor names from uploaded statement PDFs. Not required for v1.
**Why a spreadsheet is insufficient:** a spreadsheet can hold a checklist but produces no tamper-evident dated record, which is the whole point.
**Complexity:** small. **Learning difficulty:** minimal.
**Value:** aimed squarely at the 25% of T&E malpractice claims arising from inadequate investigation, where the average defense cost is ~$30,000 even on claims that pay nothing.
**Risks:** must not imply the search is exhaustive; the artifact documents diligence, it does not guarantee completeness.
**Substitutes:** firm-internal Word checklists.
**Customization:** firm-specific checklists; carrier-approved versions co-branded with a malpractice insurer would be a compelling distribution channel.

### A8 — **PlainAccount**: beneficiary-facing narrative summary of a filed accounting

**Intended user:** paralegal, professional fiduciary.
**Problem solved:** P8 and the 33% of T&E malpractice claims attributed to attorney-client communication errors.
**Current workflow:** send the beneficiary the technical schedules and field the phone calls.
**Proposed workflow:** feed the same structured ledger used by A1 → generate a plain-language narrative: what the estate started with, what came in, what went out and to whom in categories, what was sold and at what gain or loss, what remains, and what each beneficiary is projected to receive — with every figure traceable back to a schedule line.
**Inputs:** the structured account.
**Outputs:** a two-to-four page beneficiary letter and a one-page visual summary.
**Essential features:** every narrative figure hyperlinked or footnoted to its schedule line; a "no new numbers" guarantee — the generator may only restate figures present in the account.
**Excluded:** anything that computes a new number.
**AI:** *optional and well-suited* for the prose, **provided it is structurally forbidden from introducing figures**. Generate the narrative from a template filled by computed values, and use the model only for phrasing.
**Why a spreadsheet is insufficient:** the deliverable is readable prose for a non-accountant.
**Complexity:** small (given A1's data model). **Learning difficulty:** minimal.
**Value:** Florida Rule 5.346 requires accounts be "understandable to persons not familiar with... terminology peculiar to... estates," so in Florida this is close to a compliance artifact; everywhere else it is a beneficiary-relations tool aimed at the largest single malpractice error category.
**Risks:** any hallucinated figure in a beneficiary communication is a litigation exhibit. The architectural guarantee above is non-negotiable.
**Substitutes:** hand-written cover letters.
**Customization:** firm voice and branding; per-state compliance language.

### A9 — **FeeExhibit**: statutory and extraordinary fee calculator with declaration output

**Intended user:** attorney, paralegal.
**Problem solved:** a smaller but universal chore — computing and documenting statutory compensation.
**Current workflow:** a calculator, a legal pad, and a hand-typed declaration.
**Proposed workflow:** enter the accounting's gross value inputs → compute PR and attorney statutory compensation under the applicable schedule (California §§10800/10810; Florida §733.6171 and §733.617; others as added), compute the probate referee fee, itemize extraordinary services from a time export, and emit the fee schedule exhibit plus a declaration skeleton.
**Inputs:** gross estate value per the accounting; time entries for extraordinary services.
**Outputs:** tiered fee computation showing every band; referee fee; declaration draft.
**Essential features:** show the arithmetic band by band so the examiner can verify it; correct treatment of the fact that California computes on gross value without deducting encumbrances.
**Excluded:** billing, time tracking, invoicing.
**AI:** **inappropriate.**
**Why a spreadsheet is insufficient:** it barely is — this is the weakest of the nine on that test. Its justification is that it ships as a five-minute add-on to A1 and A6, using the same data, and produces the declaration text.
**Complexity:** small. **Learning difficulty:** trivial.
**Value:** modest per use, but universal, and fee-computation errors are a named examiner-note category.
**Risks:** low, but the fee schedules change and must be dated.
**Substitutes:** free online probate fee calculators are abundant. The differentiation is the *declaration output* and the integration with the accounting.
**Customization:** per-state fee statutes.

---

## 5. Opportunity ranking

Scores are 1–5 on each of ten criteria. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of implementation | Stays narrow | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| A1 | **ScheduleForge** | 5 | 5 | 5 | 4 | 3 | 4 | 4 | 5 | 4 | 5 | **44** |
| A3 | **NoteClear** | 5 | 4 | 5 | 4 | 3 | 3 | 5 | 4 | 5 | 5 | **43** |
| A2 | **CrossFoot** | 4 | 4 | 4 | 5 | 5 | 5 | 4 | 3 | 5 | 4 | **43** |
| A4 | **ProbateClock** | 5 | 5 | 4 | 5 | 3 | 3 | 3 | 5 | 4 | 5 | **42** |
| A5 | **PortabilityGuard** | 5 | 3 | 4 | 5 | 5 | 5 | 4 | 3 | 3 | 5 | **42** |
| A6 | **ReceiptRunner** | 4 | 4 | 4 | 5 | 4 | 5 | 3 | 4 | 4 | 4 | **41** |
| A7 | **DiligenceLog** | 4 | 4 | 3 | 5 | 4 | 4 | 4 | 4 | 3 | 4 | **39** |
| A9 | **FeeExhibit** | 3 | 4 | 3 | 5 | 5 | 5 | 2 | 3 | 5 | 5 | **40** |
| A8 | **PlainAccount** | 3 | 4 | 3 | 5 | 4 | 4 | 3 | 4 | 4 | 4 | **38** |

### The top three

**A1 — ScheduleForge (44).** It attacks the largest recurring labor block in the subspecialty, in a market whose fee structure makes that labor pure margin loss. The requirement it serves is statutory and therefore stable: California §1061's "total charges shall equal total credits" is not going to be repealed. The evidence that the work is manual is strong and comes from three independent directions — the statutes that mandate itemization, the marketing positioning of every modern vendor in the space, and ACTEC's own Quicken templates. The incumbents are either 1980s desktop suites with no public review footprint or full platforms requiring a practice-management migration; nothing occupies the narrow, local-first, free-base-plus-paid-jurisdiction-pack position. It is the only concept here with a natural recurring-revenue customization story (a state module per state, forever).

**A3 — NoteClear (43).** The most differentiated idea in the set, because it exploits a public data asset nobody has mined: counties publish their probate examiner notes, and those notes are a labeled corpus of exactly what the gatekeeper rejects. Turning that corpus into a *pre-filing* checklist inverts the workflow from reactive to preventive. It also has the clearest single-event ROI — one avoided continuance in Los Angeles, where corrections must be filed by the third court day before the hearing, pays for the tool. It scores lower on "stays narrow" because the temptation to grow it into a filing-management system is strong and must be resisted.

**A2 — CrossFoot (43).** The cheapest thing to build here and the easiest to validate, because it needs no integration with anything — it consumes whatever the firm already produces. It also has the rare property of being useful to *both* the firm producing the account and the litigator or beneficiary reviewing one, which doubles the addressable user base. Its ceiling is lower than A1's, but as a wedge product that establishes credibility and produces a data model, it is close to ideal.

### What to investigate next

**A2 first, A1 second, A3 third.** A2 is buildable in a weekend, requires no proprietary data, and its output — a reconciliation exception report against real filed accountings — is the fastest way to *test* whether the problems in §3 are as common as the evidence suggests. If CrossFoot run against a sample of publicly filed accountings surfaces frequent defects, that finding validates A1 and A8 simultaneously and is itself a publishable piece of market evidence. A1 should not be started until the transaction-volume question in §6 is answered by actual practitioners.

---

## 6. Validation plan

### Questions to ask practitioners

For a trusts & estates paralegal or professional fiduciary:

1. For a typical estate you closed last year, roughly how many transaction lines were in the final accounting? Twenty? Two hundred? Two thousand? *(This is the single most important unknown in this report; no public source answers it.)*
2. How do the statements get into your working document today — retyped, CSV export, or something else? What percentage of institutions give you a usable export?
3. How many hours does one annual accounting take from statements to filed schedules? How much of that is classification versus reconciliation versus formatting?
4. When an account does not balance, how do you find the error?
5. How many of your filed petitions drew examiner notes last year, and how many required a supplement? How many were continued?
6. Do you keep a checklist of your county examiner's habitual objections? Is it written down or in someone's head?
7. Do you carry a written record of the asset search you performed, separate from what you found?
8. What do you use today — Excel, Quicken with ACTEC templates, GEMS, 6-in-1, TEdec, Estateably, something else? What made you choose it and what do you hate about it?
9. Is your fee on this work statutory, flat, or hourly? How much administration time do you write off?

For an attorney: what is your firm's malpractice-carrier guidance on documenting the portability recommendation? Do you send a written memo when you advise *not* to file a 706?

### Who to interview

- Solo and 2–5 attorney probate firms in California, Florida and Michigan — three states with maximally different accounting formats, which stress-tests the jurisdiction-module architecture.
- Licensed professional fiduciaries (California has a Professional Fiduciaries Bureau licensee roster; the Professional Fiduciary Association of California is a route in). These are the highest-volume users of accountings and the best early adopters.
- Trusts & estates paralegals via NALA and NFPA chapters, and via the ABA Real Property, Trust and Estate Section.
- One probate examiner or probate clerk supervisor, to understand the defect corpus from the reviewing side.
- A malpractice carrier's risk-management counsel (ALPS, OBLIC, Lawyers Mutual) — they publish on exactly these error types and are a plausible distribution partner for A7 and A5.

### Search terms for further research

`"probate notes" [county] site:courts.ca.gov` · `"account of fiduciary" long form schedule` · `fiduciary accounting standards NFAS schedule A receipts` · `"petition for final distribution" sample accounting exhibit` · `professional fiduciary annual accounting conservatorship GC-400` · `probate paralegal accounting workflow CLE` · `"charges" "credits" probate account does not balance` · `estate administration checklist [state] statutory deadlines` · `Rev. Proc. 2022-32 portability late relief` · `trust accounting objection surcharge petition`

### Sample files and data needed

- Ten to twenty **publicly filed** accountings from different counties and states, pulled from court dockets (these are public records) — enough to build and test the exception rules in A2 and to learn the real distribution of schedule structures.
- Anonymized or synthetic bank and brokerage CSV/OFX exports covering a full accounting period, including at least one partial-lot securities sale and one real-property sale.
- A county's published probate notes archive covering several months, to build the A3 defect corpus. Los Angeles and Merced both publish; verify each site's terms before any automated collection.
- The blank official forms: California GC-400 series and DE-160/161, Michigan PC583/PC584, Florida local accounting forms built to Rule 5.346.

### Simplest validating prototype

**A single-file, browser-based, entirely local CrossFoot.** Accepts a pasted or uploaded schedule set, cross-foots it, and prints an exception report. No server, no accounts, no data leaving the machine. Hand it to five probate paralegals and three professional fiduciaries with real (redacted) accountings. The validation question is not "do you like it" but **"did it find anything you had missed?"** If it finds nothing in eight real accountings, the accounting-quality thesis behind A1, A2 and A8 is weaker than the evidence suggests and the portfolio should tilt toward A3 and A4.

### Assumptions most likely to be wrong

1. **That transaction volume is high enough to matter.** If the median estate accounting has thirty lines, ScheduleForge's ROI collapses and A2/A3/A4 become the whole portfolio. This is the load-bearing unknown.
2. **That bank and brokerage exports are obtainable.** Estate accounts are often opened after death at a single bank; if the institution provides only PDF statements and the executor is the one downloading them, the input pipeline is worse than assumed and the PDF-extraction path becomes mandatory rather than optional.
3. **That small firms will adopt a standalone tool.** They may insist it live inside Clio or Smokeball. Countervailing evidence: EVP Systems has thrived for forty years as a narrow standalone with per-security billing, which suggests this market does buy focused point tools.
4. **That "manual" really means manual.** GEMS and 6-in-1 penetration among 1–15 attorney firms is genuinely unknown; no adoption survey exists. If penetration is higher than assumed, A1's addressable market shrinks toward the sub-five-attorney and professional-fiduciary segment.
5. **That published examiner notes are consistently structured enough to mine.** The Merced samples are clean; other counties may be terse, inconsistent, or not published at all.
6. **That the liability of publishing computed deadlines is manageable.** A4 in particular needs a lawyer's review of its disclaimer posture before release.

---

## 7. Cross-industry patterns

**Pattern 1 — Ledger-to-statutory-schedule classifier with a mandatory balancing identity.** Take raw financial transactions, classify each into a prescribed statutory reporting category, and prove the totals tie by a rule the statute itself states. The classification is mechanical; the arithmetic must be deterministic; the output format varies by jurisdiction.
*Transfers to:* **Trust accounting and IOLTA three-way reconciliation for law firms** (backlog: back-office) — same shape, different rule; **Community association (HOA and condominium) management back office** (backlog: back-office) — reserve-study and assessment accounting; **Church, school and small-nonprofit bookkeeping (fund and restricted-fund accounting)** (backlog: narrow-subspecialty) — restricted-fund release is structurally identical to principal/income allocation; **Real estate brokerage trust and escrow account compliance administration** (backlog: back-office).

**Pattern 2 — Mine the gatekeeper's own published rejection notices to build a pre-filing defect checklist.** The reviewing authority publishes, in prose, exactly what it rejected and why. That corpus is a free labeled dataset for a preventive checker, inverting a reactive workflow.
*Transfers to:* **County recorder offices — document intake, indexing and rejection handling** (backlog: back-office) and its filer-side counterpart; **Building permit expediting and code consulting firms** (backlog: core-practitioner-workflow); **County surveyor and municipal plan-check offices** (backlog: all four angles); **Mortgage post-closing QC and trailing document vendors** (backlog: handoffs-and-qa). This extends the existing ledger pattern "Checklist-as-data pre-flight validation before an external gatekeeper publishes its rubric" to the case where the gatekeeper *does* publish, in unstructured form.

**Pattern 3 — All-or-nothing signature ledger, where one holdout blocks the close.** A closing step requires signed acknowledgments from every counterparty; the process is gated on the last signature, and visibility into who has not signed is the entire value.
*Transfers to:* **Prime contractor supplier cyber-compliance desks (supplier attestation collection)** (backlog: handoffs-and-qa); **Certified payroll and prevailing wage compliance service providers** (backlog: core-practitioner-workflow); **Mortgage post-closing QC and trailing document vendors** (backlog: handoffs-and-qa); construction closeout lien-waiver collection, adjacent to the completed construction-submittal report.

**Pattern 4 — Election-window guard: a decision that is cheap to make now, catastrophic to miss, with a long but finite statutory cure period, and no forcing event.** Nothing in the ordinary workflow prompts the decision, because the default is inaction. The deliverable is a dated memo documenting the recommendation, not the filing itself.
*Transfers to:* **SBIR/STTR small business award administration and data rights marking** (backlog: back-office) — unmarked technical data becomes government-rights data permanently; **Unclaimed property and escheat compliance service providers** (backlog: back-office); **Property tax consulting and assessment appeal firms** (backlog: core-practitioner-workflow) — appeal windows are short, annual, and unforgiving; **Premium audit and payroll classification consulting** (backlog: narrow-subspecialty).

**Pattern 5 — The diligence log as the deliverable: the artifact is the documented record of the search, not its result.** Where a professional obligation is to search reasonably, the defensible output is a timestamped record of what was searched — including the searches that found nothing.
*Transfers to:* **Employer immigration compliance and I-9 audit consultancies** (backlog: core-practitioner-workflow); **C3PAO assessment operations and evidence sampling** (backlog: handoffs-and-qa); **Special inspection agency accreditation consultants** (backlog: core-practitioner-workflow); **Forensic engineering firms performing cause-and-origin investigations** (backlog: core-practitioner-workflow).

**Pattern 6 — Restate a compliance artifact in plain language with a structural no-new-numbers guarantee.** A regulator or court requires a technical document; a second audience needs it comprehensible. AI drafts the prose; the figures are injected from computed values and the generator is architecturally forbidden from producing a number.
*Transfers to:* **Patient financial counseling and No Surprises Act Good Faith Estimate compliance** (backlog: handoffs-and-qa); **Retirement plan third-party administrators for small 401(k) plans** (backlog: core-practitioner-workflow) — participant fee disclosures; **Nonprofit grant management** (completed) — funder narrative reports from financial reports.

---

## 8. Sources and confidence

### Verified findings — primary sources

**Statutes, rules and forms**

- California Probate Code §1061 (summary format; "total charges shall equal total credits") — https://california.public.law/codes/probate_code_section_1061
- California Probate Code §§1060–1064 (accounts, carry value, market-value schedule) — https://law.justia.com/codes/california/2009/prob/1060-1064.html
- California Probate Code §8800 (inventory due within four months of Letters) — https://law.justia.com/codes/california/code-prob/division-7/part-3/chapter-1/section-8800/
- California Probate Code §12200 (final distribution within one year, 18 months if 706 required) — https://law.justia.com/codes/california/code-prob/division-7/part-11/chapter-1/section-12200/
- California Judicial Council forms: DE-160 Inventory and Appraisal — https://courts.ca.gov/sites/default/files/courts/default/2024-11/de160.pdf ; GC-400(SUM) Summary of Account — https://courts.ca.gov/sites/default/files/courts/default/2024-11/gc400sum.pdf ; DE-295 Ex Parte Petition for Final Discharge — https://courts.ca.gov/sites/default/files/courts/default/2024-11/de295.pdf
- Michigan SCAO form PC584, Account of Fiduciary (Long Form), Schedules A–D — https://www.courts.michigan.gov/siteassets/forms/scao-approved/pc584.pdf ; short form PC583 — https://www.courts.michigan.gov/siteassets/forms/scao-approved/pc583.pdf
- Florida Probate Rule 5.346, Fiduciary Accounting (Schedules A–E; dual carrying/current value; understandability requirement) — https://floridarules.net/probate/rule-5-346-fiduciary-accounting/
- Ohio Revised Code §2109.301 (account due within six months; 13-month outer limit) — https://codes.ohio.gov/ohio-revised-code/section-2109.301
- National Fiduciary Accounting Standards, original report hosted by the Pennsylvania courts — https://www.pacourts.us/Storage/media/pdfs/20210224/230114-natlfiduciaryacctgstdsrpt-000819.pdf
- Michigan Uniform Principal and Income Act, Act 159 of 2004 — https://www.legislature.mi.gov/documents/mcl/pdf/mcl-Act-159-of-2004.pdf
- Uniform Principal and Income Act (2008), Uniform Law Commission — https://www.uniformlaws.org/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3d79cfdc-0b53-f752-8e59-a6dc04ddb5fd
- *Tulsa Professional Collection Services, Inc. v. Pope*, 485 U.S. 478 (1988) (actual notice to reasonably ascertainable creditors) — https://supreme.justia.com/cases/federal/us/485/478/
- Rev. Proc. 2022-32 (portability late-election relief extended to five years) — https://www.journalofaccountancy.com/news/2022/jul/estates-now-request-late-portability-election-relief-5-years/
- New York Surrogate's Court sample estate account showing Schedules A–K reconciled — https://www.oteasoftware.com/md/mdocs/samples/nysampleestateaccount.pdf ; practitioner explanation — https://tcnylaw.com/trust-and-estate-accounting-basics-for-surrogates-court-practice/

**Court practice and examiner notes**

- Los Angeles Superior Court Probate Notes system (posting lead time; "Matters To Clear"; third-court-day cure cutoff) — https://www.lacourt.ca.gov/ProbateNotes/v2pubweb3/
- Merced County Superior Court published probate notes with verbatim deficiency language — https://www.merced.courts.ca.gov/system/files/probate-notes-cr10-monday-march-24-2025-815-am.pdf
- Orange County probate notes timing, practitioner guidance — https://rmolawyers.com/blog/orange-county-superior-court-probate-notes-and-supplements/
- Probate note deficiency categories — https://justdocprep.com/what-is-a-probate-note-deficiency/
- Washington closing practice; receipt-and-waiver as all-or-nothing, ~1 month delay — https://www.wa-probate.com/closing/

**Malpractice and liability data**

- ABA *Profile of Legal Malpractice Claims 2020–2023*: estate/trust/probate now the highest-risk practice area (trade press summary) — https://minnlawyer.com/2025/10/21/legal-malpractice-trends-aba-epic-lockton-2020-2023/
- Historical T&E claim share trend, 1985–2011 — https://lawyersmutualnc.com/article/rise-in-malpractice-claims-against-estate-lawyers
- T&E error-type breakdown (communication 33%, inadequate investigation 25%, errors of law 16%, time-related 8%, clerical 8%, conflicts 6%) — https://lbcclaw.com/news/trusts-and-estates-lawyers-face-increasing-risks-of-malpractice-claims
- ALPS 2024 claims trends (estate/trust/probate up 1.6%; titling, deeds, missed tax deadlines) — https://www.alpsinsurance.com/blog/6-most-common-legal-malpractice-claims-in-2024
- OBLIC risk bulletin (~70% of estate-planning claims close with zero payment; ~$30,000 average defense cost) — https://www.oamic.com/resources/common-estate-trust-probate-errors
- Recurring beneficiary objections to accountings — https://www.aldavlaw.com/trust-accounting-objections-trustee-surcharge-california/

**Software landscape and practice economics**

- EVP Systems / EstateVal: per-security billing, no minimum, local computation — https://evpsys.com/static/legal/Brief%20Description.pdf and https://evpsys.com/group/estateval
- Lackner Group 6-in-1, 2024 release — https://www.businesswire.com/news/home/20240212612467/en/2024-Version-of-6-in-1-Estate-and-Trust-Administration-Software-Released-by-The-Lackner-Group
- Gillett Publishing GEMS, NFAS-format accounting with a California module — https://www.gillettpublishing.com/estate-accounting.php
- Estateably CSV/Excel transaction import documentation — https://support.estateably.com/en/articles/10736280-import-csv-or-excel-transactions ; user reviews (prepopulation errors, dropped form data, no bulk download) — https://www.capterra.com/p/212966/Estateably/reviews/
- EstateExec for lawyers: bank transaction import — https://www.estateexec.com/for_lawyers.html
- EstateLedger positioning against manual methods — https://getestateledger.com/
- ACTEC Foundation Quicken templates for NFAS-conforming accountings — https://actecfoundation.org/quicken-templates/
- Clio Manage reviewer complaints about accounting and reporting — https://www.g2.com/products/clio-clio-manage/reviews?qs=pros-and-cons
- Actionstep reviewer complaints about setup and accounting reports — https://www.capterra.com/p/139923/Actionstep/reviews/
- QuickBooks limitations for legal trust accounting (competitor-authored but specific and checkable) — https://trustbooks.com/resources/the-risks-of-putting-your-trust-in-quickbooks/
- Statutory fee arithmetic, California §10810 with worked example — https://legalclarity.org/executor-fees-in-california-probate-code-10810-explained/
- Probate referee role and fee — https://www.estateandtrustlawyer.com/what-is-a-probate-referee-in-california-how-estate-assets-get-appraised/
- Probate profitability and the capped-fee/uncapped-work problem, $850K worked example — https://privatetrustees.com/news/making-probate-profitable/
- Trusts & estates paralegal 30.9% pay premium; "quasi-accounting" scope — https://primelegalstaff.com/how-to-hire-probate-trust-estate-paralegals/
- Paralegal role in estate administration, ABA RPTE — https://www.americanbar.org/groups/real_property_trust_estate/resources/probate-property/2023-september-october/maximizing-efficiency-estate-administration-role-paralegals/
- Practitioner on "billable hour shock" and flat fees in probate — https://californiaprobate.info/2016/02/billable-hours-be-careful/
- California small-estate affidavit threshold $208,850 effective April 1, 2025 — https://www.orangecountyestateplanningfirm.com/new-ca-small-estate-affidavit-maximum-after-april-1-2025-is-208-850

### Strong inferences

- **The statement-to-schedule conversion is manual or semi-manual at most firms of this size.** Triangulated from the statutory itemization requirement, from three vendors independently marketing import/automation as a differentiator, from ACTEC distributing Quicken templates, and from the circulation of free probate-accounting Excel templates. Not directly surveyed.
- **The dedicated fiduciary-accounting vendors are entrenched, aging and low-competition.** Inferred from a complete absence of third-party reviews for TEdec, 6-in-1 and GEMS across G2, Capterra and Trustpilot, which is unusual for practice-area software.
- **The economics make small probate firms unusually receptive to narrow point tools and hostile to platforms.** Inferred from the capped-statutory-fee structure, the professional-fiduciary worked example, and the flat-fee practitioner commentary — reinforced by EVP Systems' forty-year survival as a narrow standalone.
- **County-published examiner notes constitute a mineable defect corpus.** Verified that at least Los Angeles and Merced publish them and that Merced's are cleanly structured; the consistency across all counties is inferred.

### Tentative hypotheses requiring practitioner validation

- **Typical transaction volume per estate accounting.** No public source anywhere gives a figure. This is the load-bearing unknown for A1 and must be answered before building.
- **Frequency and duration of continuances caused by examiner notes.** Courts publish the mechanism but not aggregate analytics; a widely-cited 60/25/15 deficiency breakdown for Los Angeles has no stated methodology and should not be relied on.
- **GEMS / 6-in-1 / TEdec penetration among 1–15 attorney firms.** No adoption survey exists.
- **Whether firms would adopt a standalone tool or demand practice-management integration.**
- **Whether the "asset search diligence memo" is genuinely absent from typical files**, or whether firms already keep an equivalent under another name.
- **No Reddit or practitioner-forum content was retrievable during this research cycle** — search did not surface thread bodies and direct fetches were blocked. Nothing in this report is attributed to practitioner forums, and a future cycle covering this market should attempt that channel by another route.

---

*Report produced 2026-08-07 under claim `a001b2b9`.*
