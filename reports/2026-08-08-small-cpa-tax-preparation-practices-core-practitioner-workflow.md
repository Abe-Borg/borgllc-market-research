# Small CPA / EA Tax Preparation Practices — Core Practitioner Workflow

**Market research cycle · 2026-08-08**

---

## 0. Cycle header

| | |
|---|---|
| **Market** | Small CPA tax preparation practices |
| **Angle** | core-practitioner-workflow |
| **Claim ID** | `8295946c` |
| **Date** | 2026-08-08 |
| **Report** | `reports/2026-08-08-small-cpa-tax-preparation-practices-core-practitioner-workflow.md` |
| **Backlog remaining after this claim** | 333 assignments |

### Why this assignment over the others available

The ledger held 26 completed reports across 26 distinct markets and 334 open backlog assignments spanning 219 markets. Essentially every backlog market has zero completed entries, so criterion (a) — breadth over depth — did not discriminate. The choice came down to criteria (b) strength of available practitioner evidence and (c) diversity of the catalog.

Three considerations decided it:

1. **The catalog is structurally lopsided toward AEC and construction-adjacent work.** Six of 26 completed reports sit in architecture/engineering/construction (fire protection design, fire protection ITM, land surveying, MEP/HVAC, geotech labs, construction submittals), plus flood consulting. Taking another AEC seed (structural engineering, civil/land development, GC preconstruction, architectural studios, electrical/plumbing subs) would have deepened an already-deep vein.

2. **Tax preparation is the largest under-examined professional-services market in the backlog by practitioner headcount.** The IRS counted **879,698 individuals holding a current PTIN as of 1 August 2026** — 208,519 CPAs and 68,548 Enrolled Agents among them ([IRS Tax Professional Management Office statistics](https://www.irs.gov/tax-professionals/tax-professional-management-office-federal-tax-return-preparer-statistics)). The overwhelming majority work in firms of 1–30 people. That is the exact organization size this catalog targets, and no completed report covers it. The one adjacent entry — *Bookkeeping and outsourced accounting firms / core-practitioner-workflow* — covers a different deliverable (monthly close and client accounting), different software (QBO/Xero), and a different regulatory regime.

3. **The evidence base is unusually good and unusually dated.** Tax practice generates a public, timestamped defect corpus that most markets do not: IRS-published e-file reject code catalogs, IRS-published penalty amounts that change annually, professional liability carrier claim statistics, vendor feature-request boards with vote counts, and open practitioner forums. Several forcing dates fall inside the next 18 months (FIRE system retirement 19 November 2026, the 2026 Form 8867 penalty schedule, the expanded 2024 FTC Safeguards MFA rule).

**Method note and an honest limit.** `reddit.com` (r/taxpros, r/accounting) and `taxprotalk.com` were both blocked by this session's egress proxy on every access method. Those are the two richest veins of unfiltered practitioner voice in this market. I substituted **atxcommunity.com** (an open practitioner forum with the same character), the **Intuit Accountants Community and Idea Exchange** (where vote counts function as revealed demand), **G2 reviews with job titles attached**, and primary IRS/AICPA/carrier documents. Where a number would normally come from Reddit and I could not source it elsewhere, I say so rather than inventing it. Sections 3 and 4 would be stronger with Reddit access.

---

## 1. Market examined

**Industry.** US paid tax return preparation — NAICS 541213 (tax preparation services) and the tax practice inside NAICS 541211 (offices of CPAs).

**Professional role.** The tax preparer and the tax reviewer. In a firm of 1–5 these are the same person; from roughly 6 staff upward they separate, and the reviewer becomes the constraint. A current remote Senior Tax Advisor posting ($100–115k) lists as its *first* responsibility "Perform final technical review of individual, business, fiduciary, nonprofit, and multi-state tax returns prior to filing," with preferred software listed as "UltraTax CS, QBO, Xero, **Microsoft Excel**, Outlook, Teams" ([Indeed](https://to.indeed.com/aalwg26484rl)). Excel appearing in the software stack of a six-figure technical review role is the whole thesis of this report in one line.

**Organization size.** Sole practitioners through ~30 staff. The Rosenberg MAP survey — the industry benchmark — only covers firms above **$2M** in revenue, reporting income per partner of **$615k**, revenue growth of **7.9%** (down from 10.7%), and staff turnover of **11%**, down from 19% in 2022 ([Rosenberg Associates](https://rosenbergassoc.com/2025-rosenberg-survey-what-the-numbers-are-telling-us/)). Notably, the **$2M–$5M band saw income per partner jump ~25%, $371k → $464k**, while $10M–$20M firms *declined* 7.2% — small firms are currently the healthy end of the market. Below $2M, which is where most of the 879,698 PTIN holders sit, there is **no credible published firm-size distribution**; the Census SUSB tables would answer it but require a registered API key this session could not obtain. Treat the sole-practitioner / 2–10 / 11–30 split as unquantified.

**Type of user.** Owner-operators and small-firm partners who are technically expert, cost-sensitive, Windows-based, running desktop software (**71.5% still run their tax software locally** — [2025 Tax Software Survey, *The Tax Adviser*](https://www.thetaxadviser.com/issues/2025/aug/2025-tax-software-survey/)), and structurally under-supported: **75.6% needed technical support** in the last year and **60% never received any training from their software provider**.

**Market trajectory.** Unit volume through the professional channel is flat to shrinking. For the week ending 13 March 2026, of 68,697,000 e-filed returns, **34,059,000 were e-filed by tax professionals (down 1.2% YoY)** while 34,637,000 were self-prepared (**up 1.9%**) ([IRS filing season statistics](https://www.irs.gov/newsroom/filing-season-statistics-for-week-ending-march-13-2026)). Firms are defending revenue on price, not volume: CPA Trendlines reports the average 1040-with-schedules fee moved from **$162 (2024) to $236 (2026), a 45.7% nominal increase in two years** ([CPA Trendlines](https://cpatrendlines.com/2026/01/06/outlook-2026-tax-prep-prices-surge-and-diverge)). Meanwhile the labor supply is contracting: accounting degrees conferred fell to **55,152 in 2023–24, down 6.6%**, and new CPA Exam candidates fell **42,626 (2023) → 28,082 (2024) → 16,448 in the first half of 2025** ([*Journal of Accountancy*](https://www.journalofaccountancy.com/news/2025/oct/the-accounting-graduate-pipeline-where-do-things-stand/)).

**The economic shape that matters for tooling.** Fees are per-return and modest. NATP's 2025 biennial fee study puts a base 1040 with Schedules 1–3 at **$185 (non-credentialed), $228 (EA), $280 (CPA)**; Schedule C adds $123–135; the average business return minimum fee is **$634**; the average hourly rate is **$182**, with half of preparers between $129 and $250 ([Accounting Today](https://www.accountingtoday.com/news/what-do-tax-preparers-charge), [NATP](https://www.natptax.com/news-insights/blog/how-much-do-tax-professionals-charge-in-2025-insights-from-natp-s-fee-study/)). A firm that saves 20 minutes on a return recovers roughly $60 of capacity — against a $236 fee. **That ratio is why small, cheap, single-purpose tools can pay for themselves here and why a $10,000 platform cannot.**

---

## 2. How the work is performed

### The stage model

There is no single authoritative published description of the small-firm 1040 workflow. The canonical process lives in each firm's undocumented SOP. What follows is assembled from the vendor stage model, the AICPA quality-control requirements, and practitioner descriptions of what actually happens.

SurePrep's remote 1040 workflow guide names four macro-stages — **Document Collection → Data Extraction & Verification → Preparation & Review → Return Delivery & Payment** ([SurePrep guide, PDF](https://corp.sureprep.com/wp-content/uploads/Guide-to-a-Remote-1040-Tax-Automation-Workflow.pdf)). The AICPA Tax Practice Quality Control Guide wraps compliance obligations around those stages: prospective clients must be evaluated using "prior year tax returns of the prospective client"; "An engagement letter or memorandum of understanding is used for all tax returns"; "**Before delivery to the client all returns are reviewed by a qualified tax reviewer other than the preparer**"; and — the single most tool-shaped sentence in the document — "**The tax firm will maintain due date control logs for the various types of returns filed**" ([AICPA Tax Practice Quality Control Guide, PDF](https://assets.ctfassets.net/rb9cdnjh59cm/4p8klxa4ktw1fQei7xDx77/eb9ab6403944b508b887586c5709f5cc/tax-practice-quality-control-guide.pdf)).

Expanded to the ten stages a small firm actually runs:

**1 — Engagement and rollforward (Dec–Jan).** Prior-year clients are rolled forward in the tax software (proforma), engagement letters go out, and fees are set. Engagement letters are supposed to be reissued annually and scoped to specific forms; *The Tax Adviser* advises listing specific forms rather than "all income tax returns" and explicitly excluding tax planning if the engagement is compliance-only ([*The Tax Adviser*](https://www.thetaxadviser.com/issues/2022/feb/best-practices-engagement-letter-poas-tax-return-extensions/)).

**2 — Organizer / document request (Jan).** The classic 30-page organizer is largely dead at small firms. From the ATX Community, in a single thread ([Tax Organizers](https://www.atxcommunity.com/topic/34389-tax-organizers/)):

> *"I only give them to clients who request them. That equals about 3 to 4 clients."* — mcb39
> *"I stopped using organizers."* — BulldogTom
> *"Almost anyone who ever got one fills out a couple of tiny items, then writes 'see attached' everywhere else."* — Catherine
> *"I give a $15 credit if they bring them back filled out!"* — WITAXLADY

The substitute is a short checklist: *"I mail 4 pages in January... Fourth is checklist of items in 4 parts"* (kathyc2); *"We now use a 2-page questionnaire that addresses most of the issues we need to ask about"* (Sara EA) ([second thread](https://www.atxcommunity.com/topic/17780-time-to-send-out-tax-organizers/)).

**3 — Document intake (Jan–Apr, and Apr–Oct for extended returns).** Portal upload, email, drop-off, mail, and physical folders, in unpredictable mixture. Documents arrive in waves, not batches.

**4 — Scan / OCR / populate (optional).** SurePrep 1040SCAN "eliminates the need to verify OCR data for 65% of standard documents" — meaning the other 35% goes to human verification ([SurePrep](https://corp.sureprep.com/learning-center/1040scan/features/verification/)). GruntWorx publishes per-unit pricing: **Organize & Populate 50¢/page, Populate $1.25/form, Trade Details 30¢/trade, Trade Summary $6.00/brokerage** ([GruntWorx](https://www.gruntworx.com/pricing/variable-pricing.php)).

**5 — Workpaper assembly.** PDF binder, bookmarked and indexed, tied to the return. The *Journal of Accountancy* quantified the trade: indexed workpapers "may take about 20 minutes per return but can reduce the time it takes the preparer to actually work on the return by approximately 50 minutes" — at 400 returns, "can save the equivalent of one fulltime person during tax season" ([JofA](https://journalofaccountancy.com/issues/2011/jan/20103384.html)).

**6 — Preparation.** Data entry into Drake / UltraTax CS / Lacerte / ProSeries / ProConnect / CCH Axcess. Market share, per the 2025 survey: **UltraTax CS 22.9%, Drake 16.3%, Lacerte 15.8%, CCH Axcess 12.5%, ProSeries 10.5%, ProSystem fx 8.3%, ATX 4.6%**.

**7 — Review.** The bottleneck. "Inevitably, firms have more preparers than reviewers. The latter are highly skilled professionals who are more difficult to train or find... if a bottleneck is going to develop it will be at the reviewer level" ([CPA Trendlines, *How to Review Tax Returns*](https://cpatrendlines.com/shop/htrtr/)).

**8 — E-file authorization (Form 8879).** Legally constrained: "The IRS requires the ERO to transmit the return for e-filing within **three days** of receiving the signed Form 8879," signed forms must be retained **three years**, and §6695(a) carries a **$50 per violation, $25,500 annual maximum** penalty ([*The Tax Adviser*](https://www.thetaxadviser.com/issues/2018/jan/form-8879/)). Remote signature adds a knowledge-based authentication gate that clients resist.

**9 — Transmission, acknowledgement, and reject handling.** Covered in detail in §3.

**10 — Delivery, billing, extension, and estimate management.** Extensions are their own workflow. Mark Gallegos, CPA (Porte Brown): "**Extensions require more time and can be inefficient because you have to revisit what you did earlier**" ([JofA](https://www.journalofaccountancy.com/issues/2024/jan/tips-for-a-better-tax-season/)).

### The software actually in use

- **Tax engine:** Drake, UltraTax CS, Lacerte, ProSeries, ProConnect, CCH Axcess, ATX.
- **Portal / practice management:** TaxDome (**$800–$1,200 per seat per year**, billed upfront — [TaxDome pricing](https://www.taxdome.com/pricing/)), Canopy (**$74–$149 per user per month** annual, plus **$1.25 per KBA credit** — [Canopy pricing](https://www.getcanopy.com/pricing)), Karbon, Liscio, SafeSend, TaxCaddy.
- **Everything else:** Excel, Outlook, Adobe Acrobat, Word, Windows folders, and paper.

Published tax-software list prices for reference: **Drake Tax Pro Unlimited $3,145**, Drake Pay-Per-Return $379.99 for ten individual returns then $49.99/$74.99 each; **ProSeries Basic from $729/yr**, ProSeries Professional from **$2,605/yr**; Lacerte publishes no package price at all ([Drake pricing](https://www.drakesoftware.com/pricing/), [ProSeries pricing](https://accountants.intuit.com/tax-software/proseries/pricing/), [Lacerte pricing](https://accountants.intuit.com/tax-software/lacerte/pricing/)).

**The residual budget.** A three-person firm already spends roughly **$3,100 (Drake) + $2,400–3,600 (TaxDome or Canopy) ≈ $6,000–7,000/year** on the core stack. Any single-purpose add-on competes for what's left. The credible commercial band for one focused utility is **$200–800 per firm per year, or $1–3 per return** — about 1% of a single 1040 fee. Above roughly $1,500/year for one function, a firm will instead buy more of a suite it already owns.

### What sits outside the software entirely

Practitioners describe, verbatim, the improvised systems that carry the workflow's state:

> *"write down each name as it came in/dropped off. And I would occasionally look at the book and say 'crap...I forgot about that guy'"*
> *"A log which list every job in chronological order... has columns for date in, client name, extension if applicable, date out, amount billed"*
> *"I only use a few [statuses], such as **can do, waiting, need 8879, extended and done**... The column has filters, so I can quickly see which clients"*
> *"routing sheet for every return that comes in. There are lines for client name, ID, date in, date completed, preparer... date client contacted on completion"*
> *"Drop offs that haven't been touched go in 2 different locked drawers... Items in current process go in 2 other locked drawers"*
> — [ATX Community, "how do you track tax returns thru the in and out cycle"](https://www.atxcommunity.com/topic/28486-how-do-you-track-tax-returns-thru-the-in-and-out-cycle-of-the-office/)

And in review:

> *"I have an excel spreadsheet called 'control totals'"* — matching source documents against the Lacerte Tax Summary
> *"It is critical to know what the return is supposed to show before considering it correct."*
> — [Intuit Accountants Community, "Tax Return Review"](https://accountants.intuit.com/community/lacerte-tax-discussions/discussion/tax-return-review/00/101752)

This is the finding that structures everything below: **the return's state — what is missing, what is waiting, what was checked, what was transmitted — lives outside the tax software, in spreadsheets, logs, drawers and heads.** The tax engine computes; nothing owns the workflow.

---

## 3. Most important problems, ranked

### P1 — Missing client information stalls returns, and nothing derives the missing-items list

**Who.** Every preparer and every admin, at every firm size.

**When.** Continuously from mid-January through 15 October.

**How it is handled today.** Free-text email or a portal message, composed from memory at the moment the preparer sets the return down.

**Why that is inadequate.** The *Journal of Accountancy* named the failure mode fifteen years ago and it has not changed: "**Often, returns are put aside at the review or assembly stage, with one or two open items that can easily be answered with a follow-up call to the client**," alongside the advice to "reduce the number of staff 'touches' on returns" and "Don't start a return until all of a client's information is in the office" ([JofA](https://journalofaccountancy.com/issues/2011/jan/20103384.html)). The open-items list is not derived from the return, not versioned, and not re-evaluated when a partial response arrives — so a client who answers three of five items resets the loop instead of advancing it.

**Frequency and cost.** This is the **number one reported busy-season problem**. CPA Trendlines' 2024 Busy Season Barometer put late/unprepared clients at **50% of respondents**, with the verbatim "**Clients are not prepared and K-1s are late**"; staffing was second at 37% ([CPA Trendlines](https://cpatrendlines.com/tax-and-accounting-professionals-survey-results-busy-season-barometer-2024/)). The 2026 barometer headline: "**The returns aren't harder—they're just later**" ([CPA Trendlines](https://cpatrendlines.com/2026/04/09/busy-season-2026-too-much-work-not-enough-time/)). Wolters Kluwer's survey of 1,983 firms (1,445 completed US responses) independently found "half of this year's survey respondents reported late or unprepared clients to be a top challenge" ([Businesswire](https://www.businesswire.com/news/home/20221202005484/en/New-Wolters-Kluwer-annual-accounting-survey-reveals-how-technology-is-helping-firms-tackle-top-5-challenges-and-achieve-2023-goals)). Thomson Reuters concedes the point on its own product blog: "**For most firms, requesting and gathering the necessary client documents and data is the most challenging stage of the 1040 workflow process. It is also a primary source of workload compression**" ([Thomson Reuters](https://tax.thomsonreuters.com/blog/how-to-efficiently-file-individual-income-tax-returns-a-workflow-guide-for-accounting-firms/)).

**Evidence quality:** Verified, multiple independent sources. **Evidence gap:** no published "touches per return" metric exists.

### P2 — The organizer is a dead artifact and its replacement was never built

**Who.** Every firm sending intake requests.

**Evidence.** The **single most-voted open request in Intuit's Idea Exchange is a fillable PDF organizer: 610 votes, 213 replies** — "*My clients are requesting FILLABLE organizers. Can you make this happen so we can stop with the paper organizers?*" Two duplicate ideas hold **167** and **163** votes, one noting "**The format hasn't changed in 20 years**" ([ProSeries Idea Exchange](https://accountants.intuit.com/community/proseries-tax-idea-exchange/idb-p/603)). Roughly **940 aggregate votes for one feature, unshipped for two decades**, is the strongest quantified unmet-need signal found anywhere in this research.

**Why inadequate.** The organizer's actual job — telling the client what to send *this* year based on what they sent *last* year — is implemented as a software diagnostic, not a client-facing artifact. UltraTax CS produces "an instant checklist detailing all the fields where you had entries last year but haven't entered data for this year" ([Thomson Reuters](https://tax.thomsonreuters.com/blog/how-to-efficiently-file-individual-income-tax-returns-a-workflow-guide-for-accounting-firms/)); Lacerte ships a Missing Client Data Utility ([Intuit video](https://vimeopro.com/customersuccessteam/lacerte-tax-software/video/231394190)). These face inward. TaxCaddy's Custom DRL is the closest client-facing implementation — it "lets you automate the task of requesting tax documents from your clients based on the proforma information in the tax software" ([Thomson Reuters help](https://www.thomsonreuters.com/en-us/help/sureprep/taxcaddy/document-requests/create-custom-drl-import-proforma-data)) — but it is locked inside a per-return-priced SurePrep/Thomson Reuters stack. Practitioners have asked their own vendors for it directly: Lacerte Idea Exchange item "*One page organizer list of documents needed*" ([idea page](https://accountants.intuit.com/community/lacerte-tax-idea-exchange/one-page-organizer-list-of-documents-needed/idi-p/131248)).

**Evidence quality:** Verified.

### P3 — E-file transmission and acknowledgement have no reliable control log

**Who.** Whoever transmits — often the owner, in the last week of a deadline.

**When.** Every transmission; catastrophically around 15 April, 15 September and 15 October.

**How it is handled.** Manually, by looking at a status column. The practitioner remedy offered in the Intuit forum is literally "*Change your display to show efile status, Fed & State, as well as Ext file status (F & S)*."

**Why inadequate.** Verbatim from the same thread: "**I want to be sure that I didn't miss an efile reject… I don't want to check each return as that is time consuming**" ([Intuit Community](https://accountants.intuit.com/community/lacerte-product-discussions-2/e-file-success-reject-need-redundant-process-53413)). And from a ProSeries reviewer on G2: "**If a electronically filed tax return does not successfully get transmitted, I do not receive any special alerts**" ([G2 ProSeries](https://www.g2.com/products/intuit-proseries-tax/reviews)). This is a silent-failure mode with a deadline attached.

**Cost.** Direct liability. The AICPA/CNA program reports that "**The leading cause of loss for tax claims asserted in 2021 was a filing error**," displacing incorrect advice ([JofA](https://www.journalofaccountancy.com/issues/2022/aug/malpractice-claims-2021-future-predictions/)); Aon separately reports "**The number of professional liability claims involving missed due dates has been rising**" ([Accounting Today](https://www.accountingtoday.com/news/a-tax-season-liability-risk-alert)). CAMICO reports "**more than 60% of CAMICO's claims originating from tax-related matters**" ([CAMICO](https://www.camico.com/blog/risk-management-tips-for-the-tax-practitioner/)). And the AICPA quality-control guide already *requires* the artifact — "The tax firm will maintain due date control logs" — without specifying any system.

**Evidence quality:** Verified, and unusually well-triangulated (practitioner complaint + vendor limitation + carrier claim data + professional standard).

### P4 — E-file rejects are dominated by identity data the software never tracks year over year

**Evidence.** Drake's published Top Federal Rejects are almost entirely identity and duplicate-filing failures, not computation: **R0000-500-01** (SSN/name mismatch against the IRS database), **IND-452** (SSN already used on an accepted return), **F1040-164-01** (Form 8862 required with EIC), **F1040-087-02** (taxpayer not allowed to claim EIC), **R0000-905-01** (EFIN not in accepted status) ([Drake KB 13833](https://kb.drakesoftware.com/kb/Drake-Tax/13833.htm)). TaxSlayer Pro's catalog groups them identically and adds the **IP PIN family — IND-180-01, IND-181-01, IND-182-1, IND-183-01, F2441-995/996** — plus EIN mismatches (**FW2-502**, **F1099R-502-02**) and **IND-689-01**, where the 8879 signature date year doesn't match the processing year ([TaxSlayer Pro](https://support.taxslayerpro.com/hc/en-us/articles/360009294953-Common-Form-1040-e-File-Reject-Codes)).

**Why it persists.** None of that data is computable from the return. IP PINs arrive on IRS letters the client forgets to bring; dependent claims are contested by ex-spouses; EFIN status is an administrative fact. Practitioners have asked for exactly this: an open Idea Exchange request, "**Identity Protection PIN (IPPIN) Exporting and Diagnostic**" (27 votes), asks for automatic alerts and exportable reports for clients who had a prior-year IP PIN, because there is no built-in carryforward flag ([Intuit Idea Exchange](https://accountants.intuit.com/community/ideas)).

**Cost.** Each reject is a re-touch, a client call, a re-signature in some cases, and a transmission-window risk near a deadline.

**Evidence quality:** Verified (IRS/vendor-published code catalogs plus a vote-counted feature request).

### P5 — Carryovers, basis, and depreciation silently break, especially across software changes

**Evidence.** Intuit's own Drake→ProConnect conversion document enumerates what does **not** convert and must be re-keyed by hand: suspended losses from Schedules C/E/F and K-1, capital loss carryovers, §1231 loss carryovers, NOLs, foreign tax credit carryovers, business-use-of-home carryovers, charitable contribution carryovers, **all IRA basis carryover amounts**, state tax refund carryovers, overpayment applied to the next year, general business credit carryovers, Form 8801 items, investment interest carryovers, installment sale information, estimated tax payments made, and prior-year tax liability and AGI for penalty calculation. It also warns "**The conversion program converts a maximum of 2,500 assets**" and "Be sure to pay close attention to the Depreciation area of the conversion" ([Intuit conversion guide, PDF](https://digitalasset.intuit.com/render/content/dam/intuit/pcgcs/en_us/cross-product/ty25dataconversion/Drake_to_PTO.pdf)). Drake's side confirms the mirror image: "UltraTax depreciation items entered into the UltraTax fixed asset manager will not convert" ([Drake KB 10869](https://kb.drakesoftware.com/kb/Drake-Tax/10869.htm)).

Basis specifically is already a spreadsheet artifact — Drake, TaxAct and TaxSlayer Pro all publish shareholder/partner adjusted basis *worksheets* as standalone documents ([Drake 1120-S Basis Wks](https://kb.drakesoftware.com/kb/Drake-Tax/10919.htm), [Drake 1065 Basis Wks](https://kb.drakesoftware.com/kb/Drake-Tax/10920.htm)), and third parties sell Excel "S-Corp Shareholder Basis Tracker" templates. The IRS's own burden estimate for **Form 7203 alone** is recordkeeping 2 hr 10 min + learning 15 min + preparing 1 hr 21 min — **3 hours 46 minutes for one form** ([IRS Instructions for Form 7203](https://www.irs.gov/instructions/i7203)).

**Frequency.** Every software conversion (which every firm eventually does — "Changed tax software last year. So there was a learning curve," CPA Trendlines verbatim), plus every year in which a carryforward is not exercised and therefore not noticed.

**Cost.** Silent, deferred, and expensive: an unnoticed lost NOL or capital loss carryover is a client-money error discovered years later, squarely inside the "filing error" claim category.

**Evidence quality:** Verified from vendor primary documents.

### P6 — Review has no data structure

**Evidence.** Mainstream tax software ships no review-note object. Two standing requests on Intuit's Idea Exchange say so plainly: "*Add a place for reviewers to mark each line item on the return as reviewed and add comments to the preparer where applicable*" ([idea](https://proconnect.intuit.com/community/proconnect-tax-idea-exchange/review-comments-on-returns/idi-p/172209)) and "*tickmarks - reviewing tax returns*" ([idea](https://accountants.intuit.com/community/proconnect-tax-idea-exchange/tickmarks-reviewing-tax-returns/idi-p/305453)). Firms fall back to Acrobat stamps — GruntWorx publishes a how-to on **building tick-mark stamps in Acrobat** ([PDF](https://www.gruntworx.com/wp-content/uploads/2015/02/GWX140_CREATE-TICK-MARKS1.pdf)) — Excel control-total sheets, printed returns with pen marks, or email. The paid alternative (SPbinder / SurePrep) is priced and scoped for larger firms ([SPbinder](https://tax.thomsonreuters.com/en/products/spbinder)).

*The Tax Adviser* even supplies the working defect taxonomy small firms use informally: "content-related errors, such as incorrectly including municipal bond interest in gross income, and input errors, such as transposing numbers," plus data in the wrong location, duplicated information, and omissions ([*The Tax Adviser*](https://www.thetaxadviser.com/issues/2021/nov/assuming-reviewer-role-professor-prepared-tax-return/)).

**Evidence gap — worth naming.** No one publishes review-points-per-return, rework rates, or hours-per-return. Vendors assert review-time savings with zero numbers. **The metric itself is unowned**, which is both a research problem and a product opportunity.

### P7 — Passthrough dependencies are untracked, so extension decisions are made blind

**Scale.** Partnerships filed "over 4.5 million returns for TY 2023" representing "more than 30.2 million partners, a 5.0% increase" ([IRS SOI, PDF](https://www.irs.gov/pub/irs-soi/soi-a-copa-id2505.pdf)) — ~30 million partnership K-1s before S-corp K-1s.

**The blocking mechanism.** Tiering. "Many VC funds with separate providers file extensions, which can push final K-1 delivery to **September or even later**... you might not receive your K-1 until nine months after year-end," and early delivery is only possible for "funds that aren't waiting on lower-tier or look-through K-1s" ([Carta](https://carta.com/blog/k-1-delivery-for-lps/)).

**How it is handled.** As a status word — "waiting," "extended" — in the spreadsheet described in §2. **There is no link between the blocked 1040 and the blocking entity return.** No tool found in this research models that relationship.

**Evidence quality:** Verified on scale and mechanism; the absence of tooling is a null result across targeted searching.

### P8 — Compliance evidence is required, penalized, and tracked in four different places

Four separate obligations, four separate clocks, no shared home:

- **Form 8867 due diligence.** For a return filed in 2026 the penalty is "**$650 per failure**" and "the penalty can be up to **$2,600 per return** or claim" across EITC, CTC/ACTC/ODC, AOTC and HOH. It forces a five-item, three-year record per return: the 8867 itself, the credit worksheets, "copies of any documents provided by the taxpayer on which you relied," a record of how/when/from whom information was obtained, and "a record of any additional information you relied upon, **including questions you asked**" ([IRS](https://www.irs.gov/tax-professionals/eitc-central/consequences-of-filing-eitc-returns-incorrectly), [Instructions for Form 8867](https://www.irs.gov/instructions/i8867)). The IRS instructs preparers to document questions and answers **contemporaneously**. Non-monetary consequences include suspension from IRS e-file and an injunction barring return preparation.
- **§7216 consents.** Criminal statute. "A taxpayer's consent to each separate disclosure or use must be contained in a **separate consent document**"; minimum 12-point type; "If you do not specify the duration of your consent, your consent is valid for **one year**"; extra mandatory language if an SSN goes outside the United States; penalties up to $1,000 and one year, or $100,000 in identity-theft cases ([Rev. Proc. 2013-14, PDF](https://www.irs.gov/pub/irs-drop/rp-13-14.pdf), [*The Tax Adviser*](https://www.thetaxadviser.com/issues/2024/jan/the-many-implications-of-sec-7216/)). This bites hardest on the firms that outsource or offshore preparation.
- **Circular 230 §10.29 conflict consents.** "Copies of written consents must be retained by the practitioner for **at least 36 months** from the date of conclusion of the representation" ([eCFR 31 CFR Part 10](https://www.ecfr.gov/current/title-31/subtitle-A/part-10)). Divorcing couples, shareholder-and-S-corp, and partner-and-partnership are the recurring triggers.
- **Form 8879.** Transmit within three days of receipt; retain three years ([*The Tax Adviser*](https://www.thetaxadviser.com/issues/2018/jan/form-8879/)).

And the engagement letter, which is not a retention clock but is the single best-quantified liability item in the market: **56% of tax claims asserted in the AICPA Professional Liability Insurance Program in 2024 "lacked an engagement letter related to the underlying service"** ([JofA, Nov 2025](https://www.journalofaccountancy.com/issues/2025/nov/blocking-and-tackling-engagement-letters-for-tax-compliance-services/)). The AICPA's recommended fix is explicitly a workflow gate: **empower assembly teams to halt return finalization until a signed letter is obtained.**

### P9 — The January information-return crunch is about to change systems

**The forcing date.** "Due to the planned retirement of the Filing Information Returns Electronically (FIRE) System, the IRS is no longer accepting new Information Returns (IR) Applications for Transmitter Control Codes." Final FIRE filing deadline: "**Nov. 19, 2026, at 3 p.m. ET**." Current users "must complete an Information Returns Intake System (IRIS) Application for TCC and transition to IRIS to file tax year 2026 information returns during the 2027 filing season" ([IRS](https://www.irs.gov/e-file-providers/filing-information-returns-electronically-fire)).

**The volume driver.** "If you have **10 or more** information returns to file in a calendar year, those information returns must be filed electronically" — an **aggregate** count across form types (T.D. 9972, effective for returns filed in 2024) ([IRS Pub 5718, PDF](https://www.irs.gov/pub/irs-pdf/p5718.pdf), [Intuit Tax Pro Center](https://accountants.intuit.com/taxprocenter/tax-law-and-news/e-filing-mandate-for-10-info-returns-explained/)).

**The friction.** The free IRIS Taxpayer Portal accepts CSV upload but "**Each CSV file holds up to 100 records**," and files must be **single tax year and single form type** — different forms require separate files ([IRS IRIS FAQs, PDF](https://www.irs.gov/pub/irs-efile/info-returns-intake-system-faqs.pdf)). Commercial pricing is cheap in absolute terms (Avalara: **$3.10/form for 1–15, $2.30 for 16–165, $1.30 for 166–500, $0.63 for 501+**; TIN matching $0.45/form — [Avalara](https://www.avalara.com/us/en/products/1099/pricing.html)). **The cost is not money; it is January labor** spent reshaping messy client vendor lists into conformant files.

### P10 — Software cost and integration are the standing complaints

**Price is the number one dislike industry-wide: 61.5% average across products**, with Drake the sole exception at 8.2% (85.1% of Drake users cited price *favorably*). **Integration with accounting software averaged 3.3 — the lowest-rated dimension in the survey** ([2025 Tax Software Survey](https://www.thetaxadviser.com/issues/2025/aug/2025-tax-software-survey/)).

Representative verbatims, all with job titles attached:

> **UltraTax CS** — "THERE IS NO CUSTOMER SUPPORT AT ALL NOW…HOLD TIME IS IN EXCESS OF 2 HOURS"; "no more than one user may access a clients file" ([G2](https://www.g2.com/products/ultratax-cs/reviews))
> **Lacerte** — "Full licenses of other software are under $2,000. I just got a REP bill for $895 for like 8 clients"; the software "does not carryover the K-1s from business to personal and breaks and allocates it down by state" (Senior Tax Accountant) ([G2](https://www.g2.com/products/lacerte-tax/reviews))
> **ProSeries** — a 20-year customer: the software "can take 5+ minutes just to open" ([G2](https://www.g2.com/products/intuit-proseries-tax/reviews))
> **Drake** — "The data flow from the federal 1040 to the more complex state returns isn't always seamless"; "Sometimes it's impossible to clear errors for e-filing so the return has to be mailed" (Enrolled Agent) ([G2](https://www.g2.com/products/drake-tax/reviews))
> **TaxDome** — "Price has gone up to $1,200/user/year…practically wipes us out" (Managing Partner); "I would rate TD's ability to handle jobs and recurring work at a 3 on a scale of 1-10" (Tax Strategist) ([G2](https://www.g2.com/products/taxdome/reviews))

**Interpretation.** This is not a market waiting for another suite. It is a market of people who already pay $6–7k a year and are annoyed about it. That is the price discipline every concept below has to respect.

### What the open-source landscape actually contains

Targeted searching found a real but narrow set: the IRS's own **[direct-file](https://github.com/IRS-Public/direct-file)** (4.6k stars) and **[fact-graph](https://github.com/IRS-Public/fact-graph)** (410 stars, Scala — a genuinely reusable declarative tax-rules engine); **[habutax](https://github.com/habutax/habutax)** (42 stars, GPL-2.0, an explicitly partial 1040 solver); **[sdj0/fire-1099](https://github.com/sdj0/fire-1099)** (58 stars, MIT) — which **targets the FIRE format the IRS is retiring in November 2026**; and consumer/policy calculators (UsTaxes, PSLmodels/Tax-Calculator).

Repeated targeted searches returned **zero** open-source projects for: IRS transcript parsing, e-file acknowledgement/reject triage, Form 8879 tracking, tax workpaper PDF bookmarking and tickmarking, organizer generation and response tracking, shareholder/partner basis rollforward, a maintained standalone MACRS depreciation library, IRS notice parsing, or IRIS-native 1099 tooling. Every one of those is commercial-only today. *(Caveat: GitHub's search API was proxy-blocked, so these are null results across many queries rather than an exhaustive enumeration.)*

### What IRS data a small tool can legally and technically obtain

This constrains every concept below, so it is worth stating precisely:

- **Transcript Delivery System (TDS)** serves EROs and Circular 230 practitioners holding a **Form 2848 or Form 8821**, delivering account/wage-and-income/return transcripts to a Secure Object Repository mailbox ([IRS TDS](https://www.irs.gov/tax-professionals/transcript-delivery-system-tds)). **There is no public API and no documented bulk access.** Practitioner Priority Service allows "up to 30 TDS transcripts per client" and "transcripts for up to five clients per call" ([IR-2021-226](https://www.irs.gov/newsroom/tax-professionals-can-now-order-more-transcripts-from-the-irs)). **A tool must therefore operate on transcripts the practitioner has already downloaded — PDF in, structured data out.** That is legal, technically tractable, and exactly the gap.
- **Wage & Income transcript timing is the binding constraint on its usefulness.** W-2s post late January–February but are fully available April–May; financial 1099s post in February and complete May–July; 1099-K completes June–August. "The safest time to rely on Wage & Income data is **after July 1**" ([RefundTalk](https://refundtalk.com/wage-income-transcripts-when-the-irs-posts-w-2s-1099s/)). W&I also caps at roughly **85 documents** per taxpayer-year. Transcripts are near-useless for a February completeness check and genuinely valuable for the **extended-return population filed after July** — a narrower but real wedge. They are also not authoritative in both directions: a practitioner reports "the wife's 1099-SSN wasn't in the transcript. Nor her withholding on the 1099. But I had a copy of the 1099 issued in my sweaty little palm" ([ATX Community](https://www.atxcommunity.com/topic/34831-wage-and-income-transcript-does-not-include-a-1099r-income/)).
- **Modernized e-File (MeF)** narrative publications (Pub 4164, Pub 1436) are freely downloadable, but becoming a transmitter requires an EFIN, an ETIN, and Assurance Testing System passage. **A small tool can read and act on the published reject taxonomy; it cannot become a transmitter.**
- **IRIS Application-to-Application (A2A)** is the one real, publicly documented IRS API a small developer can integrate: REST over HTTPS, OAuth 2.0 + JWT, an X.509 certificate (**"You are not allowed to use self-signed certificates"**), XML payload attachments capped at 100MB, and an application that takes "up to 45 calendar days" ([Pub 5718, PDF](https://www.irs.gov/pub/irs-pdf/p5718.pdf)). The barriers are administrative, not technical.
- **Where's My Refund has no public API.** Scraping it is fragile and terms-dubious. Don't build on it.

---

## 4. Application opportunities

### C1 — Rollforward Open-Items Generator

*Derive the document request from last year's return, then keep scoring what's still missing.*

**Intended user.** Preparer or admin at a 1–15 person firm.

**Problem solved.** P1 and P2. The missing-items list is composed from memory and never re-derived.

**Current workflow.** Roll forward in tax software → mail a generic organizer or 2-page checklist → client sends a partial pile → preparer starts → hits a gap → writes a free-text email → sets the return down → repeats.

**Proposed workflow.** Import a prior-year return export (or a prior-year return PDF) → the tool emits a per-client **expected-document list** (each W-2 employer, each 1099 payer, each K-1 entity, each Schedule E property, each brokerage) → mark items received as they arrive → the tool regenerates a dated, numbered open-items list with a one-click client-ready version → each partial response advances the list instead of resetting it.

**Inputs.** Prior-year return PDF or tax-software client export; a received-documents checklist maintained by the user.
**Outputs.** Expected-document list; dated open-items list (client-facing PDF/email text and internal version); a per-client "% complete" figure that makes WIP aging visible.

**Essential features.** Entity-level extraction from the prior-year return; received/not-received/not-applicable tri-state; "new this year" and "gone this year" flags; regeneration with change-highlighting; export to email text.
**Deliberately excluded from v1.** Client portal, file storage, e-signature, messaging, billing, any integration that requires vendor cooperation.

**AI:** Optional, not required. Structured export → deterministic parsing. AI is worth it only for the PDF-import path (reading a scanned prior-year return), and even there it should be a fallback, not the primary path.

**Why a spreadsheet won't do.** A spreadsheet can hold the checklist but cannot *derive* it from the prior-year return, which is the entire value. Once derived, the state tracking is spreadsheet-simple — which is why v1 should be small.

**Complexity:** Medium. **Learning difficulty:** Low (15 minutes).
**Value.** If it eliminates one re-touch on 30% of returns at 20 minutes each, a 400-return firm recovers ~40 hours per season, ~$7,300 at the $182 average rate.

**Risks.** PII everywhere — must be local-first with no cloud round-trip by default. Export formats differ by package; supporting three packages properly beats supporting seven badly. **Biggest risk is scope discipline:** this concept has strong gravity toward becoming a portal, at which point it dies against TaxDome.
**Substitutes.** TaxCaddy Custom DRL (locked in SurePrep/Thomson Reuters, per-return pricing), UltraTax's inward-facing diagnostic, Lacerte Missing Client Data Utility, StanfordTax (Free tier $0; Premium $18/user/month — [Capterra](https://www.capterra.com/p/10031536/StanfordTax/)), Karbon's StanfordTax-powered organizers.
**Why still attractive.** ~940 unshipped votes over 20 years; the incumbents' versions face inward or require buying an entire stack; and no free, local, package-agnostic option exists at all.
**Customization potential.** High — firm-specific document taxonomies, niche client types (clergy, truckers, traders, expats), and firm letterhead output.

---

### C2 — E-File Control Log and Acknowledgement Reconciler

*Prove that every return you think you filed was actually accepted.*

**Intended user.** The owner or admin who transmits, especially in deadline week.

**Problem solved.** P3, plus the AICPA "due date control logs" requirement.

**Current workflow.** Scroll a status column in the tax software; hope nothing was missed. Verbatim: *"I want to be sure that I didn't miss an efile reject… I don't want to check each return as that is time consuming."*

**Proposed workflow.** Export the e-file status report from the tax package (all major packages produce one) plus the client master list → the tool reconciles them and produces a **control log** with explicit states: not started / prepared-not-authorized / **8879 outstanding** / transmitted-awaiting-ack / **accepted** / **rejected (with plain-English reason)** / **never transmitted** / extended-and-due. Plus a red list of anything with a deadline inside N days, and — critically — **anything in the client list that appears nowhere in the e-file report at all.**

**Inputs.** E-file status/acknowledgement export (CSV/PDF); client master list (CSV).
**Outputs.** Control log (screen + CSV + printable PDF); exception list; reject-code decode with the IRS/vendor-published cause and standard remedy; per-deadline countdown.

**Essential features.** Multi-package importers; a reject-code dictionary built from the published Drake and TaxSlayer Pro catalogs; the **three-day 8879 transmission clock** as a first-class alert; a signed, dated, archivable log that satisfies the AICPA control-log requirement.
**Deliberately excluded.** Transmitting anything (impossible without EFIN/ETIN/ATS), preparing returns, client communication, billing.

**AI:** Inappropriate. This is a join, a state machine, and a lookup table. Adding AI would reduce trust in exactly the artifact whose value is being trustworthy.

**Why a spreadsheet won't do.** Firms already do this in a spreadsheet — that is the documented status quo, and it fails because it is manually maintained and therefore diverges from reality. The value is *automatic reconciliation against the machine's own record*, which is not a spreadsheet operation.

**Complexity:** Small. **Learning difficulty:** Very low (under 15 minutes).
**Value.** One prevented missed filing pays for the tool for a decade. Filing errors are the leading cause of loss in tax malpractice claims, and missed-due-date claims are rising.

**Risks.** Export format drift between software versions — mitigated by a declarative, user-editable column-mapping file. Reject-code dictionary needs annual refresh. Low privacy exposure: names, IDs and statuses only, no return data, and it runs locally.
**Substitutes.** The tax software's own status view (documented as inadequate); TaxDome/Canopy job pipelines (bundled into $800–1,200/seat suites, and one reviewer rates TaxDome's job handling "a 3 on a scale of 1-10").
**Why still attractive.** No standalone product, zero open source, an explicit professional-standards requirement, a verbatim practitioner complaint, and carrier claim data quantifying the downside. Also the easiest thing on this list to build correctly.
**Customization potential.** Moderate-to-high — firm-specific state definitions, multi-office rollups, state-specific deadline calendars, integration with a firm's existing WIP spreadsheet.

---

### C3 — Pre-Transmission Identity Preflight

*Catch the reject before the IRS does.*

**Intended user.** Whoever clicks transmit.

**Problem solved.** P4. The dominant reject families are non-computational identity data.

**Current workflow.** Transmit, wait, get a reject, decode it, chase the client, re-transmit — sometimes with a new 8879.

**Proposed workflow.** Before transmission, run a checklist against the return's identity fields: name-control derivation vs. SSN records, IP PIN present-this-year vs. present-last-year, dependent SSNs against a firm-wide duplicate check, 8879 signature date within the current processing year (IND-689-01), EFIN status confirmed current, prior-year AGI/PIN present for signature validation, Form 8862 required flag where EIC was previously disallowed.

**Inputs.** Return summary export; prior-year return data; firm EFIN status (user-entered, annually).
**Outputs.** A pass/warn/fail preflight sheet with the specific reject code each item would trigger.

**Essential features.** The reject-code mapping; the year-over-year IP PIN carry flag (the 27-vote request); firm-wide dependent SSN duplicate detection.
**Excluded.** Anything requiring an IRS lookup — name control cannot actually be validated against the IRS database without transmitting, so the tool checks *derivation rules and internal consistency*, not IRS truth. This limitation must be stated honestly in the UI.

**AI:** Inappropriate. Pure rules.
**Why not a spreadsheet.** Cross-return duplicate detection and year-over-year flags aren't spreadsheet-shaped at 400 clients.
**Complexity:** Small. **Learning:** Very low.
**Value.** Moderate but real: each avoided reject saves a re-touch and, near a deadline, real risk.
**Risks.** Over-promising. If practitioners expect it to eliminate rejects and it catches 60%, they'll stop trusting it. Positioning matters more than features here.
**Substitutes.** Software diagnostics (which do not cover IP PIN carryforward or cross-client dependent duplicates).
**Customization.** Low-to-moderate.

*Honest note: C3 overlaps C2 substantially and is probably better shipped as a module of C2 than as a separate product.*

---

### C4 — IRS Transcript Parser and Income Reconciler

*Turn a downloaded Wage & Income transcript into a structured comparison against the return.*

**Intended user.** Preparers working **extended returns after 1 July**, and anyone doing back-year cleanup, non-filer work, or notice response.

**Problem solved.** The last-mile completeness check, and the total absence of transcript tooling outside expensive suites.

**Current workflow.** Pull the transcript through TDS (five clients per call, 30 transcripts per client), read the PDF by eye, compare mentally to the return.

**Proposed workflow.** Drop the downloaded transcript PDFs into the tool → structured extraction of every income document (payer, EIN, type, amounts, withholding) → side-by-side reconciliation against the return's income items → an exception list: on transcript but not on return, on return but not on transcript, amount mismatches.

**Inputs.** W&I and Account transcript PDFs already obtained via TDS under a 2848/8821; return income summary.
**Outputs.** Structured JSON/CSV of transcript documents; a reconciliation exception report; optional Account transcript transaction-code timeline.

**Essential features.** Robust parsing of the fixed-width transcript layouts (they are stable and machine-generated, which makes this tractable); reconciliation; clear labelling of the timing caveat.
**Excluded.** Automated transcript retrieval — there is no public API and automating e-Services login would be both fragile and inadvisable. **This must be explicit: the practitioner brings the file.**

**AI:** Optional. Deterministic parsing should handle native-text transcripts. AI/OCR is a fallback for scanned or degraded copies only.
**Why not a spreadsheet.** Parsing is the product; a spreadsheet is the output.
**Complexity:** Medium. **Learning:** Low.
**Value.** High per use, moderate in frequency. Highest for the extended-return population and for representation/back-year work.

**Risks.** (a) **Timing** — the tool is honest only if it states that W&I data is incomplete before roughly July. (b) **Transcripts are not authoritative in both directions**; the ATX Community example of a missing 1099-R proves it. Overstating reliability creates liability. (c) PII — must be local-only, no upload, no telemetry. (d) §7216 implications if transcript data is ever transmitted anywhere.
**Substitutes.** THS/Tax Help Software (NATP promo **$249 for three months** of the Executive license — [taxhelpsoftware.com](https://taxhelpsoftware.com/natp/)), Canopy transcripts, TaxStatus, TaxNow, IRS Solutions. All are subscription suites; none publish transcript-module pricing.
**Why still attractive.** **Zero open source exists.** The practitioner already has the file legally; the barrier is purely parsing. This is the highest-differentiation item on the list.
**Customization.** Very high — bulk processing for representation practices, custom reconciliation rules, integration into a firm's notice-response workflow.

---

### C5 — Carryover and Basis Continuity Register

*A carryforward ledger that survives your software change.*

**Intended user.** Preparer/reviewer at a firm with S-corp, partnership, rental, or investment clients; acutely, any firm switching software.

**Problem solved.** P5. Sixteen-plus categories of carryover data that silently do not migrate, plus basis tracking that already lives in spreadsheets.

**Current workflow.** Trust the software's carryforward; re-key by hand on conversion; keep basis in an Excel file that may or may not be found next year.

**Proposed workflow.** At the end of each season, extract each client's carryforward inventory — NOL, capital loss, §1231, foreign tax credit, charitable, business-use-of-home, IRA basis, §179 carryover, passive suspended losses by activity, general business credit, investment interest, installment sale data, estimated payments and overpayment applied, prior-year AGI/liability — into a **software-independent register**. Next season, diff the new return's carryforwards against the register and flag anything that vanished, changed without explanation, or failed to be used.

**Inputs.** Return export or carryforward report; prior register.
**Outputs.** Per-client carryforward register (portable CSV/JSON + printable); year-over-year diff report with an explanation field; conversion checklist keyed to the vendor-documented non-converting categories.

**Essential features.** The full category taxonomy taken from the published conversion documentation; the diff with an "explained/unexplained" flag; shareholder and partner basis rollforward (7203/K-1) as a first-class object; a conversion mode that prints exactly what must be re-keyed.
**Excluded.** Computing the carryforwards. The tax software does that; this tool *watches* them.

**AI:** Inappropriate for the register itself. Possibly useful in a later version to read a prior-year return PDF when no export exists.
**Why not a spreadsheet.** Firms already use spreadsheets, one per client, unstandardized, unversioned, and undiffed. The diff-across-years is the value and it is not a spreadsheet operation at scale.
**Complexity:** Medium. **Learning:** Low-to-moderate (the concept is instantly intuitive; the taxonomy takes a session to absorb).
**Value.** Low frequency, very high severity. One preserved NOL or capital loss carryover is worth many years of subscription. Also a direct hedge against "filing error," the leading tax-claim loss cause.
**Risks.** Requires discipline at end of season — the moment when firms have the least discipline. Mitigation: make the extraction a single import, not data entry.
**Substitutes.** Vendor conversion checklists (a one-time PDF, not a register), Excel basis templates, the tax software's own carryforward (which is precisely what fails on conversion).
**Customization.** Very high — client-type-specific taxonomies, multi-entity groups, family-group rollups.

---

### C6 — Review Note and Tickmark Tracker

*Give the review a data structure.*

**Intended user.** The reviewer, and the preparer clearing points, at firms of roughly 4+ where the roles separate.

**Problem solved.** P6. No review-note object exists in mainstream tax software.

**Current workflow.** Acrobat stamps, Excel "control totals," pen on a printed return, or email. Points are cleared verbally and no record survives.

**Proposed workflow.** Reviewer creates points against a form/line/workpaper reference, each typed (content error / input error / missing information / question for client / open item), assigned and dated. Preparer clears with a response. The return cannot be marked review-complete with open points. On completion, the point log is archived as the return's QC record.

**Inputs.** Return identifier and form/line references; reviewer typing.
**Outputs.** Review point list; cleared/open status; archived QC record per return; **the metric nobody currently has — points per return, by type, by preparer, over time.**

**Essential features.** The typed point object; clear-with-response; the completion gate; the archive; simple per-preparer trend reporting (this is the coaching value, and it is what turns the tool from admin into management insight).
**Excluded.** PDF annotation (Acrobat already does it), workpaper storage, chat.

**AI:** Optional at best. A later version could suggest a point type from the note text; that is a nicety, not the product.
**Why not a spreadsheet.** A spreadsheet can hold points but cannot gate completion, and the multi-user clear-and-respond loop degrades immediately with two people in one file.
**Complexity:** Small. **Learning:** Very low.
**Value.** Two effects. Direct: fewer lost review points and less verbal-only clearing. Indirect and larger: **the points-per-return metric is currently unmeasured industry-wide** — a firm that can see which preparer generates which error types can target training, and the reviewer bottleneck is the firm's binding capacity constraint.
**Risks.** Adoption. Reviewers are the busiest people in the building and will not adopt anything that adds keystrokes. The tool must be faster than a pen. Also: point logs are discoverable in litigation — the design should let firms set a retention policy, and the documentation should say so plainly.
**Substitutes.** SPbinder/SurePrep (priced for larger firms), Acrobat stamps, TaxDome/Canopy task comments (generic, not tied to form/line).
**Why still attractive.** Two standing vendor feature requests, zero open source, mechanically simple, and it generates a metric the whole industry lacks.
**Customization.** Moderate-to-high — firm-specific point taxonomies, integration with a firm's existing checklist library (AICPA Annual Tax Compliance Kit provides 26 checklist variants free to members).

---

### C7 — Compliance Evidence Binder (8867 / §7216 / §10.29 / 8879 / engagement letter)

*One packet per engagement, four clocks, all defensible.*

**Intended user.** The owner or firm administrator responsible for compliance, at any size.

**Problem solved.** P8. Four separate retention obligations with different clocks tracked in four different places, plus the 56%-no-engagement-letter finding.

**Current workflow.** Engagement letters in one folder, 8867 worksheets inside the tax software, §7216 consents in whatever form the outsourcing vendor supplied, conflict consents rarely documented at all. Nothing tells you what is missing until something goes wrong.

**Proposed workflow.** Per client per year, the tool maintains a required-items matrix driven by the engagement's characteristics: refundable credits claimed → 8867 package required with its five-item record; outsourced or offshore preparation → §7216 consent with correct duration and required language; related-party engagement → §10.29 conflict consent with the 36-month clock; e-filed → 8879 with the three-day transmission date and three-year retention; always → signed engagement letter dated before work began. Dashboard shows what is missing, what expires when, and what may be purged.

**Inputs.** Client list; engagement characteristics; document receipt dates.
**Outputs.** Per-engagement compliance packet manifest; a missing-items dashboard; a retention/disposition calendar; an audit-ready index if the IRS or a carrier asks.

**Essential features.** The four clocks computed correctly; a contemporaneous, timestamped Q&A note log for 8867 due diligence (the IRS's own instruction is to document questions and answers *at the time of the interview*); the **engagement-letter gate** the AICPA explicitly recommends — block return finalization until it is signed.
**Excluded.** Drafting the documents. Templates exist free (Pub 5708 for WISP, AICPA Annual Tax Compliance Kit for engagement letters, Rev. Proc. 2013-14 for §7216 language). **This tool tracks and evidences; it does not author.** That distinction keeps it small and keeps it out of unauthorized-practice territory.

**AI:** Inappropriate for the tracking. Marginal case for summarizing an interview note into a structured record — but the requirement is *contemporaneous documentation*, and AI-generated compliance evidence is precisely the wrong place to introduce doubt.
**Why not a spreadsheet.** The clocks are the point, and four different retention rules with four different trigger events applied per-engagement is genuinely error-prone by hand.
**Complexity:** Small-to-medium. **Learning:** Moderate (the compliance model takes explaining; the UI should not).
**Value.** Directly quantified: $650 per 8867 failure, up to $2,600 per return; $50 per 8879 violation to $25,500/year; criminal exposure under §7216; and 56% of tax claims lacked an engagement letter.
**Risks.** It must not read as legal advice. Every clock should cite its source so the firm's own advisor can verify it. Regulatory drift — the 8867 penalty is indexed annually and must be updatable by the user without a code release.
**Substitutes.** Practice-management suites track documents but not these specific clocks; compliance consultants sell templates, not tracking; nothing free exists.
**Customization.** Very high — state-board requirements, firm-specific retention policies, additional clocks (PTIN renewal, CPE, E&O renewal, EFIN revalidation).

---

### C8 — IRIS 1099 Preparer

*Turn messy client vendor lists into IRIS-conformant files before FIRE goes dark.*

**Intended user.** The staff member who does the January information-return run for 20–80 small business clients.

**Problem solved.** P9. A hard deadline (**19 November 2026**), a 100-record/single-form-type CSV constraint, and an OSS ecosystem pointed at the system being switched off.

**Current workflow.** Collect W-9s and QuickBooks vendor exports of varying quality; hand-clean; key into a portal or a commercial service; discover TIN mismatches after filing.

**Proposed workflow.** Import client vendor exports (QuickBooks, Xero, CSV) plus a W-9 register → normalize names, TINs, addresses and amounts → validate against IRIS field rules → flag missing TINs, malformed EINs/SSNs, and address problems → **split output into IRIS-conformant CSVs: ≤100 records, one form type, one tax year, multiple payers permitted** → produce recipient copies.

**Inputs.** Vendor/contractor exports; W-9 data; payer information.
**Outputs.** IRIS-ready CSV batches; an exception report; recipient copies; a per-client filing manifest.

**Essential features.** Format normalization; the IRIS field-rule validator; the record-count and form-type splitter; the aggregate-10 threshold calculator per payer (so the firm knows which clients are now mandatory e-filers).
**Excluded from v1.** Transmitting. A v2 could implement IRIS A2A (REST, OAuth 2.0, X.509, TCC, 45-day application), but transmission is a separate, administratively gated product decision — and the free IRIS portal already accepts the CSVs this tool produces.

**AI:** Inappropriate. Deterministic mapping and validation.
**Why not a spreadsheet.** The splitting and validation rules are fiddly and repeated across dozens of clients under time pressure; a formula error here means a rejected filing, not a wrong cell.
**Complexity:** Small. **Learning:** Very low.
**Value.** Compresses the single most compressed week of the tax-office year. Money savings are modest (Avalara is $3.10/form at low volume) but January labor savings are real, and the FIRE cutover forces every current FIRE filer to change something anyway.
**Risks.** IRIS specifications will evolve; the validator must be a data file, not hardcoded. TIN matching still requires the IRS TIN Matching service — the tool can format the request but cannot perform the match.
**Substitutes.** Avalara/Track1099, Tax1099, tax-software 1099 modules, the free IRIS portal, QuickBooks. The paid options are cheap; the free portal is constrained.
**Why still attractive.** A dated forcing event, a documented constraint the incumbents don't solve for multi-client firms, and the only existing open source aims at the retiring system. Narrow, finishable, and immediately demonstrable.
**Customization.** Moderate — client-specific import mappings, state filing variants.

---

### C9 — Passthrough Dependency and Extension Planner

*Show which 1040s are blocked by which entity returns.*

**Intended user.** The firm owner making extension and staffing decisions in March and August.

**Problem solved.** P7. Blocked returns are tracked as the word "waiting," with no link to the blocker.

**Current workflow.** A spreadsheet status column; the owner reconstructs dependencies from memory.

**Proposed workflow.** Record which individual returns depend on which entity returns (in-house or third-party) → the tool renders the dependency graph, shows the critical path, and flags every 1040 whose blocker is itself extended or externally sourced → produces the extension list and a per-entity "who is waiting on this" view that turns entity scheduling into an explicit priority decision.

**Inputs.** Client list with entity relationships (a one-time setup that rolls forward); K-1 received dates; entity return status.
**Outputs.** Dependency graph; blocked-returns list ranked by downstream impact; extension recommendation list; a per-source K-1 chase list.

**Essential features.** The relationship model (client ↔ entity ↔ preparer, in-house or external); "downstream count" ranking so the entity blocking six 1040s gets prioritized over the one blocking one; a K-1 expected/received log.
**Excluded.** Return preparation, document storage, client messaging.

**AI:** Inappropriate. This is a directed graph.
**Why not a spreadsheet.** The relationship is many-to-many and multi-level; the ranking-by-downstream-impact is a graph traversal, not a filter.
**Complexity:** Small. **Learning:** Low.
**Value.** Better sequencing of the scarcest resource in the building during the exact weeks it is scarcest. Also a defensible answer to "why is my return not done" — the client can be shown the blocker.
**Risks.** Setup cost in year one. Mitigation: import relationships from K-1 entities already present in the prior-year returns (shares the C1 extraction), then roll forward.
**Substitutes.** None found. Practice-management job pipelines model *stages*, not *dependencies between clients*.
**Why still attractive.** ~30.2 million partnership K-1s, September delivery for tiered structures, the number-one busy-season complaint naming late K-1s explicitly, and no tool models the relationship.
**Customization.** Moderate-to-high — firms with heavy real-estate or fund clients would pay for deeper tiering.

---

### Considered and deliberately not recommended

- **A WISP generator.** The obligation is real and enforced by a perjury-adjacent PTIN attestation (Form W-12 line 11), and the 2024 Safeguards update expanded MFA to "anyone accessing any information system" ([IRS Pub 5708](https://www.irs.gov/pub/irs-pdf/p5708.pdf), [University of Illinois Tax School](https://taxschool.illinois.edu/post/applying-the-updated-wisp-requirements/)). But the IRS already publishes a free 28-page fill-in template, and a generator would mostly duplicate it. The *tracking* half — annual review attestation, MFA verification evidence — is better folded into C7 than shipped alone.
- **An AI return preparer.** Black Ore, Filed, Juno and others already occupy this, with capital. Practitioner sentiment is skeptical and the honest reading of the field is Ellen Choi's: "This only works for very constrained, simpler cases, i.e. tax prep for less complex 1040s," alongside Wesley Hartman's "There is still a high level of distrust of AI doing the work" ([Accounting Today](https://www.accountingtoday.com/list/ai-thought-leaders-survey-2026-process-predictions)). Even the vendor comparison concedes "none of these numbers has been independently benchmarked."
- **Another scan-and-populate engine.** SurePrep and GruntWorx are mature, and the practitioner verdict is that verification is irreducible: "**Review of every GruntWorx return is required!**"… "Sometimes 5s are entered as 8s. There are a few times where we found a form entered twice" ([Wealthy Accountant](https://www.wealthyaccountant.com/2022/07/10/gruntworx-review/)). Scan-and-populate compresses *keying*, not *chasing* — and chasing is the actual bottleneck.
- **A practice-management suite.** TaxDome and Canopy exist, cost $800–1,800 per seat per year, and are already the target of price complaints. Entering here means competing on breadth with funded incumbents.

---

## 5. Opportunity ranking

Scored 1–5 on each criterion; 50 maximum.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of build | Stays narrow | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| **C2** | **E-File Control Log & Ack Reconciler** | 4 | 5 | 5 | 5 | 5 | 5 | 4 | 4 | 4 | 5 | **46** |
| **C6** | **Review Note & Tickmark Tracker** | 4 | 5 | 4 | 5 | 5 | 5 | 4 | 4 | 5 | 4 | **45** |
| **C8** | **IRIS 1099 Preparer** | 4 | 3 | 5 | 5 | 5 | 5 | 4 | 4 | 5 | 5 | **45** |
| **C7** | **Compliance Evidence Binder** | 5 | 4 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 5 | **44** |
| **C9** | **Passthrough Dependency Planner** | 4 | 4 | 4 | 5 | 5 | 5 | 5 | 4 | 4 | 4 | **44** |
| **C1** | **Rollforward Open-Items Generator** | 5 | 5 | 5 | 5 | 3 | 3 | 3 | 5 | 4 | 5 | **43** |
| **C4** | **IRS Transcript Parser & Reconciler** | 5 | 4 | 5 | 4 | 3 | 4 | 5 | 5 | 3 | 5 | **43** |
| **C5** | **Carryover & Basis Continuity Register** | 5 | 4 | 5 | 4 | 3 | 4 | 5 | 5 | 3 | 5 | **43** |
| **C3** | **Pre-Transmission Identity Preflight** | 4 | 5 | 4 | 5 | 4 | 5 | 4 | 3 | 3 | 4 | **41** |

### The top three explained

**C2 — E-File Control Log and Acknowledgement Reconciler (46).** It wins not because it is the most valuable idea but because it is the most *certain* one. Every dimension lines up: a verbatim practitioner complaint about the exact failure ("I want to be sure that I didn't miss an efile reject"), a vendor limitation admitted in a public review ("I do not receive any special alerts"), a professional standard that already requires the artifact (AICPA due date control logs), carrier data quantifying the downside (filing errors are the leading tax-claim loss cause; missed-due-date claims rising), and zero open-source or standalone commercial competition. It is also the smallest build on the list — CSV in, state machine, log out, no AI, no integration, no cloud. A working version could exist in a weekend and be demonstrated to a practitioner in ninety seconds. **This is the one to build first**, and it is a good Trojan horse: once a firm's client list and status data are in a local tool, C3, C7 and C9 become natural modules rather than new products.

**C6 — Review Note and Tickmark Tracker (45).** The strongest *strategic* concept. The reviewer is the firm's binding capacity constraint — stated explicitly in the leading practitioner text on review — and the market has no data structure for review at all, confirmed by two standing vendor feature requests and a null open-source search. The secondary effect may exceed the primary one: **nobody in this industry publishes review-points-per-return, rework rates, or hours-per-return.** A tool that quietly generates that metric gives a firm owner something no benchmark survey currently sells them, and gives the tool's author a genuinely novel dataset. The risk is honest and specific: reviewers will not adopt anything slower than a pen.

**C8 — IRIS 1099 Preparer (45).** The most *finishable* concept with the clearest deadline. FIRE dies at 3 p.m. Eastern on 19 November 2026; every current FIRE filer must change systems for TY2026 returns; the free IRIS portal imposes a 100-record, single-form-type CSV constraint that is actively hostile to a firm filing for forty clients; and the only existing open-source 1099 tooling targets the format being retired. It is deterministic, testable with synthetic data, demonstrable in one screen, and it solves a problem that arrives on a specific date. Its lower frequency score (once a year) is what keeps it out of first place — but a once-a-year tool that saves a week is still an easy sell.

### What to investigate next

**Build C2 first.** Then reassess in this order:

1. **C1 (Rollforward Open-Items Generator)** has the highest ceiling of anything here — it attacks the number-one reported busy-season problem and sits on ~940 unshipped feature votes — but it scored sixth because of build difficulty and, more importantly, **scope discipline risk**. It wants to become a portal. Before building it, validate that a *non-portal* version (generate the list, hand it to the firm, let them send it however they already send things) is actually wanted. If practitioners say "I'd just want it in TaxDome," the concept is dead as a standalone and should be reconceived as a TaxDome/Canopy-adjacent generator.

2. **C4 (Transcript Parser)** deserves a spike specifically to answer one question: *how stable is the Wage & Income transcript layout across years and formats?* If it parses cleanly and deterministically, C4 jumps the ranking — it has the highest differentiation score on the list (5) and literally zero open-source competition. If parsing turns out to require OCR and heuristics, it becomes a much larger project and should wait.

3. **C5 (Carryover Register)** is the highest-severity, lowest-frequency item. It is the right *second* product for a firm that already trusts you, not a first product for a firm that doesn't.

---

## 6. Validation plan

### Questions to ask practitioners

**On C2 (highest priority):**
- Walk me through the last week before 15 April. How do you confirm every return you intended to file was actually accepted?
- Has a return ever sat unfiled or unnoticed-rejected past a deadline? What happened?
- Where does your "due date control log" live right now? Can you show me the columns?
- Which e-file status export does your software produce, and would you send me a de-identified sample?
- Would you pay $300 a year for a tool that only does this — nothing else?

**On C6:**
- How do you communicate review points to a preparer today? Show me the last one.
- Roughly how many points does a typical 1040 generate? An 1120S? *(Nobody has published this. The first person to collect it owns a number.)*
- Would you want per-preparer trend data, or would that feel like surveillance?

**On C1:**
- How do you decide what to ask a returning client for?
- Do you compare against last year's return, and if so, how — on screen, on paper, from memory?
- If a tool produced the missing-items list but did *not* send it, would that still be useful?

**On C9:**
- How many of your 1040s are blocked on a K-1 in any given April?
- Do you know, right now, which entity return is blocking the most individual returns?

**On C5:**
- Have you ever changed tax software? What broke? What did you have to re-key?
- Where do you keep shareholder basis today?

### Who to interview

Sole practitioner EAs and CPAs (the largest and least-served segment); firm administrators at 5–15 person firms (they own the tracking spreadsheets and will describe them without prompting); a reviewer/partner at a 10–30 person firm (for C6); an enrolled agent doing representation work (for C4 — they are the heaviest transcript users); a firm that switched tax software in the last two years (for C5); and, for credibility calibration, a CAMICO or AICPA/CNA risk consultant. Reachable through NATP and NAEA chapter meetings, state society tax committees, and — once accessible — r/taxpros, where this kind of question gets answered candidly and at length.

### Further research search terms

`"due date control log" CPA firm` · `e-file acknowledgement not received tax software` · `"review notes" tax return preparer clear` · `tax return "open items" list client email template` · `IRS wage and income transcript layout parse` · `IRIS CSV template 1099-NEC multiple payers` · `Form 7203 basis spreadsheet` · `tax software conversion carryover lost` · `K-1 tracking spreadsheet tax firm` · `"points per return" tax review benchmark` · plus targeted r/taxpros and TaxProTalk searches once accessible.

### Sample files and data needed

- De-identified e-file status exports from Drake, ProSeries and UltraTax CS (**this is the single most important artifact for C2** — the whole product is a parser plus a state machine over these files).
- A redacted Wage & Income transcript PDF and a redacted Account transcript (C4).
- A prior-year 1040 PDF and the matching tax-software client export (C1, C5).
- A real (redacted) firm tracking spreadsheet — the artifact being replaced (C2, C9).
- A QuickBooks vendor export and a batch of W-9s (C8).
- The AICPA Annual Tax Compliance Kit checklists as a starting taxonomy for C6.

### Prototypes that would validate

- **C2:** A single Python script that ingests one Drake e-file status CSV plus a client list CSV and prints a four-column exception table: *never transmitted / rejected-not-corrected / 8879 outstanding / accepted*. If a practitioner looks at that output and says "wait, what's that one doing there," the product is validated on the spot.
- **C6:** A local single-page web app with one table — point, form/line, type, assignee, status — and a hard gate on completion. Watch whether a reviewer uses it twice.
- **C8:** A script that takes one messy QuickBooks vendor CSV and emits validated IRIS-conformant CSVs plus an exception list. Validate by uploading the output to the IRIS portal.
- **C4:** A parser spike against three real transcript PDFs from different years. Success criterion: exact field extraction with no OCR.

### Assumptions most likely to make these fail

1. **That practitioners will adopt anything outside their existing software.** The strongest counter-evidence is that they already have — the spreadsheets, logs and drawers documented in §2 are all outside the software. But every concept here must be faster than the spreadsheet it replaces, not merely better.
2. **That e-file status exports are stable and parseable across packages and versions.** If not, C2's build cost triples. **Test this before anything else.**
3. **That the reviewer will tolerate one more keystroke.** C6 lives or dies here.
4. **That "free and open source" reads as trustworthy rather than risky to a profession carrying §7216 criminal exposure and a WISP attestation.** Local-only, no telemetry, no cloud, auditable source is a genuine advantage in this market — but it must be stated loudly and repeatedly, not assumed.
5. **That transcript layouts are machine-stable** (C4).
6. **That firms will do end-of-season data hygiene** (C5) at the moment they least want to.
7. **That the AI vendors won't absorb these features.** Black Ore, Filed and StanfordTax are funded and moving. The defensible ground is the unglamorous, deterministic, liability-adjacent work they are not prioritizing — control logs, evidence binders, dependency graphs — not extraction.

---

## 7. Cross-industry patterns

Patterns from this market that transfer to named backlog markets:

**1. Acknowledgement reconciliation — "prove the thing you submitted was actually accepted."** A submission is transmitted to an external authority, an acknowledgement returns asynchronously, and nothing reconciles the two, so silent non-delivery goes unnoticed until a deadline passes. Transfers to: *Certified payroll and prevailing wage compliance service providers* (WH-347 submissions to multiple agency portals), *Truck permitting and registration service agencies* (IFTA/IRP/state filings across 5–6 cadences), *Multi-state charitable solicitation registration compliance* (~40 state regimes), *Provider credentialing and payer enrollment services*, *Sales tax compliance outsourcing for small multi-state sellers*, and *Community floodplain administration at small municipalities*.

**2. Prior-period rollforward as the source of the request list.** Derive what you need *this* period from what you received *last* period, rather than sending a static generic form. Transfers to: *Small third-party medical billing companies* (recurring documentation per payer), *Bookkeeping firms* (monthly close PBC), *Retirement plan third-party administrators* (annual census requests), *Property tax consulting and assessment appeal firms* (per-parcel evidence), *Fiscal sponsorship organizations*, and *Association management companies running education for multiple client associations*.

**3. The dependency graph between deliverables held by different parties.** Deliverable A cannot complete until deliverable B, held by a different preparer or organization, completes — and the blocking relationship is tracked as a status word rather than a link. Transfers to: *Delegated-design submittal coordination*, *Architectural construction administration desks at small A/E firms*, *Commercial title and escrow for multi-property portfolio closings*, *1031 exchange qualified intermediaries*, and *Aerospace supplier quality clause library administration* (sub-tier flow-downs).

**4. Multiple retention clocks with different trigger events, tracked in different places.** Three to five distinct legal retention obligations attach to one engagement, each starting from a different event, and no single artifact shows what is missing or what may be purged. Transfers to: *Employer immigration compliance and I-9 audit consultancies*, *Consortium/third-party administrators for DOT drug and alcohol programs*, *Radiation safety officer services and portable gauge licensee compliance*, *Personnel certification bodies under ISO/IEC 17024*, and *Third-party COBRA administrators*.

**5. Carry-forward continuity across a system migration.** Cumulative state (balances, basis, credits, histories) silently fails to migrate when an organization changes software, and the loss is discovered years later. Transfers to: *Fire protection service consolidator M&A integration operations* (roll-ups absorbing shops on different systems), *Accounting firm client-book transitions, M&A and succession operations*, *Small bank and trust company trust operations departments*, and *Dental service organization multi-location chart audit*.

**6. The review-point object.** A senior professional's corrections to a junior's work exist only as pen marks, PDF stamps or verbal clearing, so the defect data that would drive training is never captured. Transfers to: *Architectural construction administration desks*, *Small-firm litigation support and paralegal work*, *Offshore and BPO bookkeeping staffing providers* (the review handoff is the entire quality gate), *Environmental laboratories producing regulator EDD deliverables*, and *Legal process outsourcing vendors*.

**7. Regulator-published defect taxonomy as a free product specification.** When an authority publishes its own rejection codes or error statistics, that list is a ready-made checklist a small tool can implement without inventing a rules corpus. Already noted in the ledger for AHJ and plan-check contexts; this cycle confirms it for *IRIS and MeF*, and it transfers to *County recorder offices*, *State licensing board education/CE audit units*, *Mortgage post-closing QC and trailing document vendors*, and *DOL RAPIDS apprenticeship reporting*.

---

## 8. Sources and confidence

### Verified findings (primary or named-attribution sources)

**Market structure and economics**
- [IRS Tax Professional Management Office — federal tax return preparer statistics](https://www.irs.gov/tax-professionals/tax-professional-management-office-federal-tax-return-preparer-statistics) — 879,698 current PTINs (1 Aug 2026); CPAs 208,519; EAs 68,548; AFSP 72,049.
- [IRS filing season statistics, week ending 13 March 2026](https://www.irs.gov/newsroom/filing-season-statistics-for-week-ending-march-13-2026) — professional e-filings down 1.2%, self-prepared up 1.9%.
- [Rosenberg Associates — 2025 MAP Survey](https://rosenbergassoc.com/2025-rosenberg-survey-what-the-numbers-are-telling-us/) — IPP $615k; $2–5M band up ~25%; turnover 11%. *Covers only firms above $2M.*
- [Accounting Today — What do tax preparers charge](https://www.accountingtoday.com/news/what-do-tax-preparers-charge) and [NATP 2025 Fee Study](https://www.natptax.com/news-insights/blog/how-much-do-tax-professionals-charge-in-2025-insights-from-natp-s-fee-study/) — CPA base 1040 $280; hourly average $182.
- [CPA Trendlines — Outlook 2026: tax prep prices surge](https://cpatrendlines.com/2026/01/06/outlook-2026-tax-prep-prices-surge-and-diverge) — $162 → $236 in two years.
- [*Journal of Accountancy* — accounting graduate pipeline](https://www.journalofaccountancy.com/news/2025/oct/the-accounting-graduate-pipeline-where-do-things-stand/).
- [Drake pricing](https://www.drakesoftware.com/pricing/) · [ProSeries pricing](https://accountants.intuit.com/tax-software/proseries/pricing/) · [Lacerte pricing](https://accountants.intuit.com/tax-software/lacerte/pricing/) · [TaxDome pricing](https://www.taxdome.com/pricing/) · [Canopy pricing](https://www.getcanopy.com/pricing) · [Avalara 1099 pricing](https://www.avalara.com/us/en/products/1099/pricing.html) · [GruntWorx variable pricing](https://www.gruntworx.com/pricing/variable-pricing.php).

**Workflow and pain**
- [CPA Trendlines — Busy Season Barometer 2024](https://cpatrendlines.com/tax-and-accounting-professionals-survey-results-busy-season-barometer-2024/) — late/unprepared clients 50%, #1 problem. · [Busy Season 2026](https://cpatrendlines.com/2026/04/09/busy-season-2026-too-much-work-not-enough-time/).
- [Wolters Kluwer survey of 1,983 firms](https://www.businesswire.com/news/home/20221202005484/en/New-Wolters-Kluwer-annual-accounting-survey-reveals-how-technology-is-helping-firms-tackle-top-5-challenges-and-achieve-2023-goals).
- [*Journal of Accountancy* — Maximizing Tax Season Efficiency](https://journalofaccountancy.com/issues/2011/jan/20103384.html) — touches, returns set aside, 20-min/50-min workpaper trade.
- [*Journal of Accountancy* — Tips for a better tax season](https://www.journalofaccountancy.com/issues/2024/jan/tips-for-a-better-tax-season/).
- [ATX Community — Tax Organizers](https://www.atxcommunity.com/topic/34389-tax-organizers/) · [Time to send out tax organizers](https://www.atxcommunity.com/topic/17780-time-to-send-out-tax-organizers/) · [How do you track tax returns thru the in and out cycle](https://www.atxcommunity.com/topic/28486-how-do-you-track-tax-returns-thru-the-in-and-out-cycle-of-the-office/) · [W&I transcript missing a 1099-R](https://www.atxcommunity.com/topic/34831-wage-and-income-transcript-does-not-include-a-1099r-income/).
- [Intuit Accountants Community — e-file reject tracking](https://accountants.intuit.com/community/lacerte-product-discussions-2/e-file-success-reject-need-redundant-process-53413) · [Tax Return Review](https://accountants.intuit.com/community/lacerte-tax-discussions/discussion/tax-return-review/00/101752) · [Best way to review a Lacerte return](https://accountants.intuit.com/community/lacerte-tax-discussions/discussion/what-is-the-best-way-to-review-a-lacerte-tax-return-prepared-by/00/93793).
- [Intuit ProSeries Idea Exchange](https://accountants.intuit.com/community/proseries-tax-idea-exchange/idb-p/603) and [Idea Exchange index](https://accountants.intuit.com/community/ideas) — fillable organizer 610+167+163 votes; consolidated 1099 screen 132; IP PIN diagnostic 27; Schedule F two-year comparison 74. · [Review comments idea](https://proconnect.intuit.com/community/proconnect-tax-idea-exchange/review-comments-on-returns/idi-p/172209) · [Tickmarks idea](https://accountants.intuit.com/community/proconnect-tax-idea-exchange/tickmarks-reviewing-tax-returns/idi-p/305453) · [One-page organizer list idea](https://accountants.intuit.com/community/lacerte-tax-idea-exchange/one-page-organizer-list-of-documents-needed/idi-p/131248).
- [2025 Tax Software Survey — *The Tax Adviser*](https://www.thetaxadviser.com/issues/2025/aug/2025-tax-software-survey/) and [*JofA*](https://www.journalofaccountancy.com/issues/2025/sep/2025-tax-software-survey/) — price 61.5% top dislike; integration 3.3; 71.5% local.
- G2 reviews with job titles: [UltraTax CS](https://www.g2.com/products/ultratax-cs/reviews) · [Lacerte](https://www.g2.com/products/lacerte-tax/reviews) · [ProSeries](https://www.g2.com/products/intuit-proseries-tax/reviews) · [ProConnect](https://www.g2.com/products/intuit-proconnect-tax/reviews) · [Drake](https://www.g2.com/products/drake-tax/reviews) · [TaxDome](https://www.g2.com/products/taxdome/reviews) · [Canopy](https://www.g2.com/products/canopy/reviews).
- [CPA Trendlines — *How to Review Tax Returns*](https://cpatrendlines.com/shop/htrtr/) — the reviewer bottleneck.
- [*The Tax Adviser* — assuming the reviewer role](https://www.thetaxadviser.com/issues/2021/nov/assuming-reviewer-role-professor-prepared-tax-return/) — review-note defect taxonomy.
- [Thomson Reuters — 1040 workflow guide](https://tax.thomsonreuters.com/blog/how-to-efficiently-file-individual-income-tax-returns-a-workflow-guide-for-accounting-firms/) — vendor admission that document gathering is the hardest stage.
- [SurePrep remote 1040 workflow guide, PDF](https://corp.sureprep.com/wp-content/uploads/Guide-to-a-Remote-1040-Tax-Automation-Workflow.pdf) · [1040SCAN verification](https://corp.sureprep.com/learning-center/1040scan/features/verification/) · [TaxCaddy Custom DRL](https://www.thomsonreuters.com/en-us/help/sureprep/taxcaddy/document-requests/create-custom-drl-import-proforma-data).
- [Wealthy Accountant — GruntWorx review](https://www.wealthyaccountant.com/2022/07/10/gruntworx-review/) — "Review of every GruntWorx return is required!"
- [Indeed — Senior Tax Advisor posting](https://to.indeed.com/aalwg26484rl) — Excel in the review-role software stack.

**Errors, liability and regulation**
- [Drake KB 13833 — Top Federal Rejects](https://kb.drakesoftware.com/kb/Drake-Tax/13833.htm) · [TaxSlayer Pro — common 1040 reject codes](https://support.taxslayerpro.com/hc/en-us/articles/360009294953-Common-Form-1040-e-File-Reject-Codes).
- [Intuit Drake→ProConnect conversion guide, PDF](https://digitalasset.intuit.com/render/content/dam/intuit/pcgcs/en_us/cross-product/ty25dataconversion/Drake_to_PTO.pdf) · [Drake KB 10869](https://kb.drakesoftware.com/kb/Drake-Tax/10869.htm) · [Drake 1120-S Basis Wks](https://kb.drakesoftware.com/kb/Drake-Tax/10919.htm) · [Drake 1065 Basis Wks](https://kb.drakesoftware.com/kb/Drake-Tax/10920.htm) · [Drake KB 10855 — Comparison Sheet](https://kb.drakesoftware.com/kb/Drake-Tax/10855.htm).
- [IRS Instructions for Form 7203](https://www.irs.gov/instructions/i7203) — 3 hr 46 min burden for one form.
- [CAMICO — risk management tips for the tax practitioner](https://www.camico.com/blog/risk-management-tips-for-the-tax-practitioner/) — >60% of claims tax-related.
- [*JofA* — malpractice claims 2021](https://www.journalofaccountancy.com/issues/2022/aug/malpractice-claims-2021-future-predictions/) — filing error the leading cause of loss.
- [*JofA* — engagement letters for tax compliance services, Nov 2025](https://www.journalofaccountancy.com/issues/2025/nov/blocking-and-tackling-engagement-letters-for-tax-compliance-services/) — 56% of 2024 tax claims lacked one.
- [Accounting Today — tax season liability risk alert](https://www.accountingtoday.com/news/a-tax-season-liability-risk-alert) — missed-due-date claims rising.
- [IRS — consequences of filing EITC returns incorrectly](https://www.irs.gov/tax-professionals/eitc-central/consequences-of-filing-eitc-returns-incorrectly) and [Instructions for Form 8867](https://www.irs.gov/instructions/i8867) — $650 per failure / $2,600 per return for 2026.
- [*The Tax Adviser* — Form 8879](https://www.thetaxadviser.com/issues/2018/jan/form-8879/) — three-day transmission rule, §6695(a).
- [Rev. Proc. 2013-14, PDF](https://www.irs.gov/pub/irs-drop/rp-13-14.pdf) and [*The Tax Adviser* — implications of Sec. 7216](https://www.thetaxadviser.com/issues/2024/jan/the-many-implications-of-sec-7216/).
- [eCFR 31 CFR Part 10 (Circular 230)](https://www.ecfr.gov/current/title-31/subtitle-A/part-10) — §10.29 36-month consent retention; §10.34.
- [IRS Pub 5708, PDF](https://www.irs.gov/pub/irs-pdf/p5708.pdf) · [IRS Form W-12, PDF](https://www.irs.gov/pub/irs-pdf/fw12.pdf) · [University of Illinois Tax School — updated WISP requirements](https://taxschool.illinois.edu/post/applying-the-updated-wisp-requirements/).
- [AICPA Tax Practice Quality Control Guide, PDF](https://assets.ctfassets.net/rb9cdnjh59cm/4p8klxa4ktw1fQei7xDx77/eb9ab6403944b508b887586c5709f5cc/tax-practice-quality-control-guide.pdf) · [AICPA Annual Tax Compliance Kit](https://www.aicpa-cima.com/resources/landing/annual-tax-compliance-kit).

**IRS systems and data availability**
- [IRS — Transcript Delivery System](https://www.irs.gov/tax-professionals/transcript-delivery-system-tds) · [IR-2021-226 — transcript volume limits](https://www.irs.gov/newsroom/tax-professionals-can-now-order-more-transcripts-from-the-irs) · [IRS — steps to obtain W&I transcripts](https://www.irs.gov/newsroom/steps-for-tax-professionals-to-obtain-wage-and-income-transcripts-needed-for-tax-preparation).
- [IRS Pub 5718 — IRIS A2A, PDF](https://www.irs.gov/pub/irs-pdf/p5718.pdf) · [IRIS FAQs, PDF](https://www.irs.gov/pub/irs-efile/info-returns-intake-system-faqs.pdf) · [IRS — FIRE retirement](https://www.irs.gov/e-file-providers/filing-information-returns-electronically-fire) · [IRS Pub 4164, PDF](https://www.irs.gov/pub/irs-pdf/p4164.pdf).
- [Intuit Tax Pro Center — 10-return e-file mandate](https://accountants.intuit.com/taxprocenter/tax-law-and-news/e-filing-mandate-for-10-info-returns-explained/).
- [IRS SOI — partnership returns TY2023, PDF](https://www.irs.gov/pub/irs-soi/soi-a-copa-id2505.pdf) — 4.5M returns, 30.2M partners.
- Open source surveyed: [IRS-Public/direct-file](https://github.com/IRS-Public/direct-file) · [IRS-Public/fact-graph](https://github.com/IRS-Public/fact-graph) · [habutax](https://github.com/habutax/habutax) · [sdj0/fire-1099](https://github.com/sdj0/fire-1099).

### Strong inferences (reasoned from verified artifacts, not directly stated by practitioners)

- **The workflow's state lives outside the tax software.** Assembled from the ATX tracking thread, the Lacerte control-totals thread, the AICPA control-log requirement, and the Excel-in-the-job-posting datum. No single source says it; every source implies it.
- **The open-items list resets rather than advances on partial client response.** Inferred from the JofA "set aside with one or two open items" finding combined with the free-text-email delivery mechanism. Plausible and consistent, but not directly attested.
- **~940 aggregate votes on one unshipped feature over 20 years is the strongest unmet-need signal in this market.** The vote counts are verified; the interpretation is mine.
- **The $200–800/firm/year or $1–3/return price ceiling.** Derived from published software prices, published fee data, and the 61.5% price-dislike finding. Directionally sound; not validated with any buyer.
- **Wage & Income transcripts are useful mainly for the post-July extended-return population.** The timing data is verified; the product implication is inference.
- **C3 should be a module of C2 rather than a separate product.** Design judgment.

### Tentative hypotheses requiring practitioner validation

- **That e-file status exports are stable and parseable across packages and versions.** This is the load-bearing assumption under the top-ranked concept and it is completely unverified. **Test first.**
- **That reviewers will adopt a review-point tool.** Plausible from the two feature requests; entirely unproven in practice.
- **That firms will maintain an end-of-season carryover register** (C5) during the week they most want to stop working.
- **That "free and open source, runs locally, no telemetry" is a trust advantage rather than a trust liability** in a profession carrying §7216 criminal exposure. Reasonable, untested.
- **Review points per return, rework rates, hours per return, touches per return, organizer completion rates, and the share of extensions caused by missing documents versus late K-1s.** None of these are published anywhere I could find. Every one of them is currently unmeasured, which is simultaneously the biggest evidence gap in this report and, for C6, a product opportunity.
- **Firm-size distribution below $2M revenue.** Rosenberg excludes it; Census SUSB would answer it but requires an API key this session could not obtain. Worth closing before committing to a build.

### Source access limitations affecting this report

`reddit.com` (r/taxpros, r/accounting) and `taxprotalk.com` were blocked by the session proxy on every access method; `api.census.gov` required a registered key; GitHub's search API and commit feeds were proxy-blocked, so the open-source null results in §3 rest on repeated targeted queries rather than exhaustive enumeration. A re-run with Reddit access would materially strengthen the quantitative claims in §3 and the improvised-tooling detail in §2.
