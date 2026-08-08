# Unclaimed property and escheat compliance service providers — back-office

**Cycle header**

| Field | Value |
|---|---|
| Market | Unclaimed property and escheat compliance service providers |
| Angle | back-office |
| Claim ID | `542772a3` |
| Date | 2026-08-08 |
| Assignments remaining in backlog after this claim | 399 |

**Why this assignment over the others available.** Every market in the ledger currently has exactly one completed report, so criterion (a) — breadth over depth — did not discriminate; 308 backlog items sat in wholly untouched markets. I chose on criteria (b) and (c). On angle diversity, `back-office` and `narrow-subspecialty` were the two least-covered angles (8 completed each, against 10 core-practitioner-workflow and 9 handoffs-and-qa). On evidence availability, unclaimed property is unusually well-documented in public primary sources: fifty state treasurers publish free, detailed holder reporting manuals with exact dormancy tables, due-diligence thresholds and file-format rules; NAUPA publishes the file format standard and a state-by-state reporting chart; there is a trade association (UPPO) publishing practitioner-authored guidance; and there is reported federal litigation (*Temple-Inland v. Cook*) that puts hard dollar figures on the failure mode. That combination — deterministic published rules plus a documented, expensive failure mode — is exactly the profile of a market where small focused software wins. On catalog composition, the ledger is heavily weighted toward AEC/construction and clinical/medical back offices; a multi-state regulatory-filing market diversifies it. I also passed over several tempting AEC items (special-hazard suppression design, TAB contractors, Title 24 acceptance testing) precisely because the catalog already leans that way.

One caution recorded up front: this is a market where the incumbent free tool (HRS Pro) is genuinely good at the last mile (file formatting) and genuinely absent from the hard part (deciding what is reportable). The opportunities below are deliberately positioned in the gap the free tool documents about itself, not on top of it.

---

## 1. Market examined

**The industry.** Every U.S. state, D.C., Puerto Rico and the U.S. territories operate an unclaimed property (escheat) program. Businesses that hold property belonging to someone else — uncashed payroll and vendor checks, customer credit balances, unredeemed gift cards and stored value, unclaimed insurance proceeds, dormant deposit and brokerage accounts, unclaimed securities and dividends, safe deposit box contents — are "holders" and are legally obliged to identify that property once a state-specified dormancy period elapses, attempt to contact the owner, and then remit the property and a detailed report to the correct state.

The scale of the transfer is large and growing: NAUPA-reported figures cited by *Bloomberg Tax* put roughly **$3 billion per year** flowing to states, with state return rates to actual owners ranging from **8.6% to 59%**. In Delaware — the state of incorporation for a large share of U.S. corporations, and therefore the second-priority claimant on huge volumes of property — unclaimed property collections were **$554.0 million in FY2019**, of which **$114.3 million** went back to owners and **$439.7 million** was retained, making it the state's **third-largest revenue source**. That fiscal dependence is why enforcement is aggressive and why a compliance-services trade exists at all.

**The professionals and organizations.**

- **Independent unclaimed property consultancies and reporting outsourcers.** Firms like UPCR, MarketSphere/Sovos consulting, PEACC, Argent, Clarus, and dozens of one-to-fifteen-person shops. They run annual reporting on behalf of client holders, defend audits, scope voluntary disclosure agreements (VDAs), and sell dormancy/rules research. Typical staffing: 2–25 people, of whom 1–6 are analysts doing the actual data work. This is the primary user for this angle.
- **SALT and accounting-firm unclaimed property practices.** Baker Tilly, BDO, RSM, Aprio, Wipfli, Andersen, Ryan and regional CPA firms run unclaimed property as a small niche practice — often a group of 2–8 specialists inside a much larger firm, operating with the same tooling problems as an independent shop and with less internal IT priority.
- **In-house escheat coordinators.** Inside the holder: an AP manager, treasury analyst, controller, or a dedicated "unclaimed property analyst" (a real, advertised job title, posted in the roughly **$65k–$140k** range). At companies below a few billion in revenue this is a **fraction of one person's job**, performed once or twice a year, often by someone who inherited it without training. This is the secondary user, and the one most likely to download a free tool.
- **Adjacent service providers who acquire the obligation by accident**: payroll bureaus and PEOs holding uncashed wage checks, retirement plan TPAs holding uncashed distribution checks, title and escrow companies, property managers holding tenant deposits, and independent pharmacies and medical practices holding patient credit balances. Several of these are already separate markets in this ledger.

**Organization size most likely to benefit.** Two clusters.

1. Service providers with **3–25 staff** serving **20–300 client holders**, each client filing in **1–50 jurisdictions**. Their economics are hours-per-client-per-season; their peak load is concentrated into two short windows a year.
2. Holder organizations with **$20M–$2B revenue** — large enough to generate reportable property in a dozen or more states, too small to license Sovos UPCS or Kelmar-class enterprise software or to staff a full-time escheat function.

**Type of user.** Accounting-literate, spreadsheet-fluent, not developers. Comfortable with Excel pivot tables, VLOOKUP and CSV; not comfortable with a database, a command line, or a system that requires an implementation project. Highly deadline-driven. Extremely sensitive to PII handling: their working files contain full names, addresses and, for many property types, **Social Security numbers**.

---

## 2. How the work is performed

The annual cycle, as documented in state holder manuals and practitioner guidance, runs roughly as follows.

**(a) Engagement and scoping (service-provider back office).** The provider signs an engagement, gathers the client's entity list (including entities acquired in M&A, which carry inherited liability), determines the client's state of incorporation (for second-priority sourcing), and establishes which states the client has previously filed in. First-time filers are a distinct and risky category — filing a clean current-year report without addressing prior years is itself an audit trigger, because states screen for filing-history gaps and for missing property types typical of the industry.

**(b) Data extraction from the client.** The analyst requests, per entity and per property source: outstanding/stale check registers from AP and payroll, bank reconciliation outstanding items, AR credit balance and unapplied cash agings, customer deposit and gift card/stored-value ledgers, and — increasingly a state focus — **unclaimed electronic payments** (failed ACH, returned direct deposits, wires), which first-time filers routinely omit. What arrives is whatever the client's ERP will export: a mix of Excel workbooks, CSVs, PDF agings, and occasionally a screenshot. Column names, date formats, entity codes and address field structures differ per client and often per system within a client.

**(c) Scrubbing and false-positive removal.** The analyst removes items that are not really outstanding: checks voided and reissued, checks cleared but not reconciled, internal/intercompany items, refunded credits, and items already reported in a prior year. This is where the audit rule bites: Baker Tilly's guidance is that **checks voided more than 30 days after the original issuance date are presumed to be unclaimed property absent documentation of final disposition**. So the analyst must not merely delete voids — they must prove where the money went.

**(d) Jurisdiction sourcing.** Under *Texas v. New Jersey*, 379 U.S. 674 (1965), property escheats **first** to the state of the owner's last known address, and **second** — where no address exists or the address is in a foreign country or a non-claiming jurisdiction — to the **holder's state of incorporation**. Every property row therefore has to be assigned a state by rule, not by guess, and the second-priority bucket is precisely the bucket Delaware is fed by.

**(e) Dormancy determination.** For each row: what NAUPA property type code applies (AC01 checking, MS01 wages, CK-series official checks, and so on), what dormancy period that state applies to that code, and what the "last activity date" is. The variation is severe and not intuitive:

| Property type | Typical dormancy |
|---|---|
| Wages / payroll | **1 year** in most states |
| Court/government distributions (VT) | 1 year |
| Vendor checks, customer credits, general property | 3–5 years (RUUPA default: 3) |
| Safe deposit box contents (VT) | 5 years |
| Money orders (VT) | 7 years |
| Traveler's checks | **15 years** |

**(f) Exemptions and deductions.** Business-to-business exemptions vary from near-total to a mere deferral, and the state groupings are genuinely arbitrary from a holder's point of view: Arizona, Tennessee and Missouri **defer** while a business relationship is active; Indiana, Iowa, Massachusetts, Michigan, North Carolina and Wisconsin exempt **credit balances only**; Illinois, Kansas, Maryland, Ohio and Virginia exempt most ordinary-course property including uncashed checks; Texas and New York operate administrative deferral without a statute. Illinois retroactively **repealed** its B2B exemption in 2017 — so the rule is not even stable over the lookback period. Crucially, "**States will accept any property remitted to them and will not ensure that a B2B exemption is properly applied**" — the state will never tell you that you over-remitted your client's money.

**(g) Statutory due diligence mailing.** Before reporting, the holder must send a compliant letter to the owner's last known address. The rules are per-state and precise:

- **Threshold**: most states $25–$50; **Texas $250+**; **Florida exempts under $10**; **New York** requires outreach regardless of amount.
- **Method**: **Ohio and New York require certified mail above $1,000**; most others allow first-class; some allow electronic if the owner consented.
- **Window**: commonly "no more than 120 and no less than 60 days prior to the report due date"; **Vermont** specifies not more than 180 and not less than 60 days before remittance; **California** requires the notice **6 to 12 months prior to the Notice Report due date** — a completely different clock from everyone else.
- **Content**: California mandates a specific heading — *"THE STATE OF CALIFORNIA REQUIRES US TO NOTIFY YOU THAT YOUR UNCLAIMED PROPERTY MAY BE TRANSFERRED TO THE STATE IF YOU DO NOT CONTACT US"* — plus account reference, escheatment date, a statement that no activity has occurred, and an owner interest form.

IOFM's framing is blunt: due diligence is "**the most difficult unclaimed property requirement for businesses to fulfill**."

**(h) Report assembly and filing.** Output must generally be in the **NAUPA II standard electronic file format** — a fixed-width text layout with HOLDER, PROPERTY, TANGIBLE PROPERTY and SUMMARY record types, in use in all 50 states since 2004. Files containing PII must frequently be encrypted (`.HDE`) or password protected. Deadlines split into a **fall cycle (approximately 41 jurisdictions, Oct 31/Nov 1)** and a **spring/summer cycle (roughly 9–10: Delaware, New York, Connecticut, Pennsylvania, Florida, Illinois, Vermont, Michigan, Texas)**, with life insurers usually on the spring clock. **California and Puerto Rico are two-step**: California requires a **Notice Report before November 1** and then a separate **Remit Report between June 1 and June 15** of the following year — filing the Remit Report without a prior Notice Report is one of the state's own listed common holder errors. Vermont additionally demands a **notarized affidavit** and a hard-copy printout with the electronic file, requires NAUPA format above **10 items**, and permits aggregation only for items **$25 or less** and only for in-state addresses.

**(i) Remittance.** Funds move by check or EFT under per-state thresholds (California: only remittances **under $2,000** may be sent by check; $2,000+ requires EFT registration). The provider must coordinate client funding, timing, and proof of payment across dozens of jurisdictions in a two-week window.

**(j) Post-filing back office.** Negative reports where required. State confirmations and deficiency notices. Owner inquiries routed back to the holder after the state's own outreach. Retention of the evidence file: most states require records for **10 years plus the dormancy period** (RUUPA §404 sets a 10-year minimum), against a corporate norm of seven-year retention — a gap that practitioners describe as the single most consequential documentation failure.

**(k) Notices and enforcement events.** Separately from the annual cycle, states send VDA invitations, self-audit invitations, "verified report" requests, and examination notices. **Delaware ran two VDA invitation mailings in 2026, in April and in August, each carrying a hard 90-day enrollment window**; failure to enroll converts the invitation into a state-initiated audit. RSM characterizes the 2026 posture as a shift to "targeted outreach rather than broad examinations," with California mounting its own outreach campaign.

**Software currently used.**

| Tool | Role | Notable limits |
|---|---|---|
| **HRS Pro** (Wagers & Associates) | The free/near-free NAUPA II report generator that states themselves point holders to. Standard edition free (single user, no export); Enterprise **$499/yr for 3 users**, +$150/user. Produces NAUPA II, cover sheets and due diligence letters. | Self-documented: "**HRS Pro is not set up to determine dormancy period and what is escheatable to the states**." Cannot import NAUPA files back, cannot merge datasets, free tier cannot export. |
| **Sovos UPCS, Kelmar, Ryan Tracker PRO** | Enterprise holder reporting and owner-claims platforms | Priced and implemented for large filers; overkill and unaffordable for a 5-person consultancy or a $50M holder |
| **Excel** | Everything HRS Pro does not do: dormancy determination, scrubbing, exemption analysis, state matrices, calendars, per-client tracking | Fragile, unversioned, undocumented, and the analyst who built it is the only one who understands it |
| **State portals** | Upload and confirmation, one login per state per holder | Each state its own site, its own credential, its own file rules; some still take physical media (Vermont accepts CD/flash drive) |
| **NAUPA state reporting charts, state holder manuals** | The rule source of truth | **Published as web pages and PDFs, not as machine-readable data** — a structural reason nobody has a rules engine |

---

## 3. Most important problems, ranked

### P1 — Reportability determination is unautomated, and the free tool says so out loud

*Who*: every analyst at a service provider, and every in-house escheat coordinator. *When*: on every property row, every season. *Currently handled*: an Excel workbook with a hand-maintained state × property-type dormancy lookup, filled in from PDFs, applied with formulas of varying correctness, and re-verified each year by re-reading state manuals. *Why inadequate*: the determination is the legally consequential step and it is the step with no software. HRS Pro — the tool 50 states endorse — states in its own FAQ that it does **not** determine dormancy or escheatability. Enterprise platforms do it, at enterprise prices. *Frequency*: continuous through both seasons; thousands to millions of rows. *Cost*: under-reporting produces interest and penalties (California: **12% annual interest** from the date the property should have been reported under CCP §1577, penalties up to **$50,000** under §1576, on a lookback of roughly **10 years plus dormancy**). Over-reporting silently gives away client money that no state will return unprompted. *Evidence*: HRS Pro FAQ; state dormancy tables; Baker Tilly practice guidance.

### P2 — Due diligence is the hardest requirement and is governed by three independent per-state variables

*Who*: the analyst preparing the mailing. *When*: 60–365 days before each report deadline, on a different clock per state. *Currently handled*: a spreadsheet of thresholds and dates, plus mail-merge, plus a manual decision about certified vs first class. *Why inadequate*: three variables (threshold, window, method) vary independently across ~53 jurisdictions, plus mandated letter language in some states, plus per-state affidavit/attestation requirements. Miss the window and you cannot legally cure it by mailing late; the compliance defect is baked into the filing. *Frequency*: annual per state per client — for a provider with 100 clients across 20 states, that is up to 2,000 window computations a season. *Cost*: failed due diligence is a named audit finding and undermines VDA eligibility; it also destroys the cheapest possible outcome, which is the owner cashing the check and the property never escheating at all. *Evidence*: IOFM ("the most difficult unclaimed property requirement"); Baker Tilly (60–120 day standard window); California SCO due diligence guidance ($50 threshold, 6–12 month window, mandated heading); Vermont manual (60–180 days, $50, notarized affidavit); Wipfli (TX $250, OH/NY certified over $1,000, FL under $10 exempt).

### P3 — Record gaps convert into state-estimated liability, and nobody maps the gaps in advance

*Who*: the holder, discovered by the provider during audit defense or VDA scoping. *When*: when an examination or VDA arrives, often covering 10–22 years. *Currently handled*: a scramble through archived ERP data, bank statements and boxes; whatever cannot be produced becomes a state estimate. *Why inadequate*: UP retention rules do **not** track IRS/FASB seven-year norms; states expect **10 years plus dormancy**, and practitioners recommend 15. The asymmetry is brutal — the state's estimation methodology fills the gap, and it fills it in the state's favor. *Frequency*: episodic but escalating; Delaware alone issued two VDA invitation waves in 2026. *Cost*: in *Temple-Inland v. Cook* (D. Del.) the audit reached back to **1986** and produced an estimated accounts-payable liability of **$1,176,767.77**, against roughly **$330,252.89** if amounts already reported to other states were credited; the court held the methodology violated substantive due process and described it as "a game of 'gotcha' that shocks the conscience." *Evidence*: Temple-Inland record; MarketSphere retention guidance; RUUPA §404; Journal of Accountancy.

### P4 — Void/reissue reconciliation creates both false positives and audit exposure

*Who*: the analyst scrubbing check registers. *When*: every cycle. *Currently handled*: manual eyeballing of void codes and reissue dates; sometimes a VLOOKUP on amount and payee. *Why inadequate*: a void with no matched reissue and no documented disposition is presumed reportable if it occurred **more than 30 days after issuance**; conversely, a reissued check counted twice inflates the report and hands the state client money. Payee name spellings differ between the void and the reissue, amounts may be netted, and the reissue may sit in a different period or a different system. *Frequency*: every cycle, on every check-issuing client. *Cost*: two-sided — over-remittance is an unrecoverable client loss; under-documented voids are a standard audit adjustment. *Evidence*: Baker Tilly AP guidance.

### P5 — The multi-client, multi-state obligation calendar is a spreadsheet, and the deadlines are structurally irregular

*Who*: the service-provider operations lead. *When*: continuously; two hard peaks. *Currently handled*: a master Excel calendar, Outlook reminders, and institutional memory. *Why inadequate*: the obligation is not "one deadline per state." It is (holder type × state × property type × prior filing history), and it includes California's two-step Notice/Remit split, Puerto Rico's Aug 10/Dec 10 pair, insurer-specific spring dates, and **negative report obligations that persist in some states once you have filed**. Baker Tilly lists "develop a compliance calendar" as a top-ten best practice precisely because missing this is common. *Frequency*: year-round. *Cost*: a missed deadline restarts the penalty/interest clock and can disqualify a client from voluntary relief. *Evidence*: PEACC due-date guidance; Baker Tilly best practices; state manuals.

### P6 — Second-priority sourcing is a mechanical rule applied by hand

*Who*: the analyst. *When*: after address cleanup. *Currently handled*: sort by state column; whatever is blank or foreign gets dumped to the state of incorporation, hopefully. *Why inadequate*: the second-priority bucket is where Delaware's revenue comes from and where auditors focus. Address quality problems (foreign addresses, PO boxes, "RPO" returned-mail flags, multiple entities with different incorporation states) make this non-trivial, and the answer must be reproducible years later. *Frequency*: every row, every cycle. *Cost*: mis-sourcing means remitting to the wrong state, which does not extinguish the correct state's claim — the holder can pay twice. *Evidence*: *Texas v. New Jersey*; Journal of Accountancy; Delaware audit practice.

### P7 — Exemptions are left on the table because applying them requires per-state legal judgment

*Who*: the provider's senior reviewer. *When*: before filing. *Currently handled*: senior-level manual review, or skipped entirely for smaller engagements. *Why inadequate*: the B2B landscape has at least four distinct regimes plus administrative-only states, conditional tests (does the relationship still exist? was the credit later refunded by check?), and at least one retroactive repeal. Third-party software handles standard exemptions; **conditional ones require manual review**. Skipping the analysis costs the client real money and the state will never object. *Frequency*: annual, concentrated in AP/AR-heavy clients. *Cost*: direct, recoverable dollars — the entire fee basis of contingency-priced consulting work. *Evidence*: Baker Tilly B2B analysis; The Tax Adviser; Clearview Group.

### P8 — A format migration is scheduled and the ecosystem is fixed-width

*Who*: everyone who produces a report file. *When*: NAUPA III Phase 1 launches **Spring 2027**, coexisting with NAUPA II during transition. *Currently handled*: not at all yet; holders are on NAUPA II fixed-width. *Why inadequate*: NAUPA itself calls the move "a significant technical and operational challenge" for holders, state vendors and software providers, and split the rollout into two phases (XML infrastructure first, code restructuring second) to soften it. State acceptance will be staggered, so for at least one full cycle, providers will need to produce **both** formats depending on the jurisdiction. *Frequency*: one-time transition with a multi-year tail. *Cost*: rejected filings, missed deadlines, emergency vendor spend. *Evidence*: NAUPA III project page.

### P9 — Enforcement notices arrive with hard clocks at people who are not watching for them

*Who*: the holder's finance function; the provider inherits the emergency. *When*: April and August 2026 for Delaware VDA waves; ad hoc for verified-report and self-audit notices. *Currently handled*: mail room to controller to (eventually) provider. *Why inadequate*: the 90-day enrollment clock runs whether or not the letter reached the right desk, and non-enrollment converts to audit. *Frequency*: rising; RSM describes 2026 as a targeted-outreach year, with California joining. *Cost*: the difference between a penalty-and-interest-waived VDA and a contingency-fee examination with estimation. *Evidence*: RSM 2026 alert; BDO; MarketSphere notices guidance.

---

## 4. Application opportunities

A note on architecture before the list: **concepts A1, A2, A5, A7 and A9 all read from the same artifact** — a versioned, machine-readable state rules matrix (jurisdiction × property code × dormancy × due diligence threshold/window/method × aggregate threshold × deadline × negative-report flag × format/portal), with a citation and effective date on every cell. That file is the durable asset. Build it once; the applications are thin, individually shippable faces on it. That is also the answer to "why hasn't someone done this" — the rules exist only as fifty PDFs and web pages, so the matrix has never been assembled as data in the open.

---

### A1 — **DormancyDesk**: reportability determination engine

- **User**: unclaimed property analyst at a service provider; in-house escheat coordinator.
- **Problem**: P1. The one legally consequential step with no software beneath enterprise pricing.
- **Current workflow**: hand-maintained Excel dormancy lookup, formulas, annual re-verification from PDFs.
- **Proposed workflow**: load a normalized property file → the engine applies (state of sourcing, property code, last activity date, as-of report date) → each row is returned as reportable / not-yet-dormant / exempt-candidate / needs-review, with the governing rule, its citation and its effective date printed alongside.
- **Inputs**: CSV/XLSX of property rows (owner name, address, amount, issue date, last activity date, property type, entity); the rules matrix; a report-as-of date.
- **Outputs**: annotated determination file; a per-state summary with counts and dollars; a "rule application log" suitable for an audit binder; an exceptions worksheet.
- **Essential features**: rules matrix as versioned data with citations; deterministic determination; a diff view when the matrix version changes ("14 rows changed status because Illinois changed X"); property-code mapping assistant.
- **Excluded from v1**: securities and safe deposit boxes (different mechanics, much lower volume for the target user); state filing; any owner-facing portal.
- **AI**: **optional and confined.** Useful for two jobs: (i) proposing a NAUPA property code from a free-text check description or GL account name, human-confirmed once per client and then remembered as a mapping rule; (ii) assisting the *maintainer* in extracting rule changes from newly published state manuals into the matrix, always with human verification. The determination itself must be deterministic code — an AI-decided escheat determination is unauditable and therefore worthless.
- **Why not a spreadsheet**: a spreadsheet cannot version the rules, cannot cite them, cannot show what changed year over year, and cannot be reviewed by anyone but its author. The audit-defense value is precisely in the provenance, which a spreadsheet destroys.
- **Complexity**: medium (the matrix is the work; the engine is small). **Learning**: ~30 minutes.
- **Value**: for a provider running 100 clients, replaces the most error-prone manual step in the season and produces the artifact that defends the filing.
- **Risks/constraints**: rules-accuracy liability — must ship with explicit "not legal advice; verify against the state manual" framing and a per-cell citation so the user can verify. PII: run locally, never upload.
- **Substitutes**: Sovos UPCS, Kelmar (enterprise pricing); Excel. HRS Pro explicitly does not do this.
- **Why still attractive**: the endorsed free tool disclaims the function in writing. That is as clean a gap statement as this catalog is likely to find.
- **Paid customization**: per-client property-code mapping packs; private rules overlays for a firm's own conservative positions; integration with a specific ERP export.

---

### A2 — **DiligenceWindow**: statutory due-diligence window calculator and compliant letter generator

- **User**: the analyst preparing the mailing; also directly usable by a one-person in-house coordinator.
- **Problem**: P2 — the requirement practitioners name as the hardest.
- **Current workflow**: threshold spreadsheet + mail merge + a judgment call on certified mail.
- **Proposed workflow**: feed in the reportable population and the target report deadline → the tool computes, per state, the exact legal mailing window (open date and close date), splits the population by threshold into "must mail / need not mail / must mail certified," generates state-compliant letters including mandated heading language, and emits a mail log plus an attestation/affidavit worksheet for the states that require one.
- **Inputs**: reportable property file; per-state deadline; holder contact block and return address; optional owner-response tracking file.
- **Outputs**: per-state mailing calendar with open/close dates; merged letters (PDF); certified-mail subset with a green-card manifest; mail log CSV; returned-mail (RPO) intake sheet; affidavit worksheet.
- **Essential features**: window arithmetic per state; threshold splitting; mandated-language templates per state; certified-mail flagging (OH/NY >$1,000); response/RPO logging that feeds back into A1 as "owner contacted — remove from report."
- **Excluded from v1**: actually mailing (no print-and-mail integration — export a print-ready file and let the user use their existing mail house); email/electronic notice (consent tracking is a separate problem); skip tracing.
- **AI**: **inappropriate.** Every element is a date computation, a threshold comparison, or a template. Adding a model here adds risk and nothing else.
- **Why not a spreadsheet**: the letter generation, the certified-mail split, and the evidence log are three different outputs from one rule application; a spreadsheet gives you the arithmetic and none of the artifacts. Also, a missed window is uncurable — the value is in never computing it wrong, which is exactly what a tested function does and a formula copied down a column does not.
- **Complexity**: small-to-medium. **Learning**: ~20 minutes.
- **Value**: eliminates the single most-cited compliance failure, and every owner who responds is property that never escheats — a directly measurable, client-visible win.
- **Risks/constraints**: PII in the merge file (local-only); state-specific mandated language must be maintained; letters must not be represented as legally reviewed.
- **Substitutes**: HRS Pro generates due-diligence letters but does not compute per-state windows or thresholds (it does not know what is escheatable). Enterprise platforms do both.
- **Why still attractive**: it is the narrowest possible slice of the rules matrix, ships fastest, and demonstrates the matrix's value immediately.
- **Paid customization**: firm-branded letter templates; per-client escalation rules; integration with a client's mail house file spec.

---

### A3 — **NaupaCheck**: NAUPA II validator and NAUPA III readiness pre-flight

- **User**: anyone who produces a report file — provider analysts and in-house coordinators alike.
- **Problem**: P8 plus routine rejection. The listed common NAUPA errors are mechanical: wrong property or relationship codes, mixed report years or mixed state rules in one file, invalid characters or misaligned columns in fixed-width, missing encryption, skipped validation.
- **Current workflow**: generate in HRS Pro or a vendor tool, upload, and find out from the state whether it parsed.
- **Proposed workflow**: drop in a `.txt`/`.HDE` NAUPA II file → structural validation (record type sequence, field offsets, character legality), semantic validation (valid property and relationship codes, control totals reconciling to the SUMMARY record, single report year, single state), and a NAUPA III readiness report showing which fields will need new or restructured data when Phase 1 XML lands in Spring 2027.
- **Inputs**: NAUPA II file; optional source detail file for reconciliation.
- **Outputs**: line-and-column-referenced error report; a reconciliation of detail-to-summary totals; a NAUPA III gap list; optionally, a NAUPA III XML draft once the Phase 1 schema is published.
- **Essential features**: offline validation; plain-English error messages tied to record/field; totals reconciliation.
- **Excluded from v1**: report generation (HRS Pro already does this well and free — do not duplicate it); state submission; encryption key management beyond detecting whether a file is encrypted.
- **AI**: **inappropriate.** This is a parser.
- **Why not a spreadsheet**: fixed-width validation in Excel is actively painful, and Excel silently mangles leading zeros, long numeric IDs and text alignment — it is the *cause* of several of these errors, not the fix.
- **Complexity**: small-to-medium. **Learning**: ~10 minutes.
- **Value**: converts a state rejection loop (days, at deadline) into a pre-flight check (seconds). The NAUPA III angle gives it a dated reason to exist and a natural marketing window through 2027.
- **Risks/constraints**: NAUPA III Phase 1 schema is not final — build the II validator first and treat III as a readiness report until the schema publishes. Files contain PII and possibly SSNs: strictly local, no telemetry.
- **Substitutes**: state portal validators (post-hoc, per-state, inconsistent); vendor tools (bundled with the expensive part).
- **Why still attractive**: complements rather than competes with the free incumbent, and NAUPA has publicly committed to a disruptive migration with a date on it.
- **Paid customization**: per-state validation profiles; a build-server version for a provider that generates hundreds of files a season.

---

### A4 — **FilingRegister**: multi-client, multi-state obligation and evidence tracker

- **User**: the service provider's operations lead; also the in-house coordinator with 15 states.
- **Problem**: P5 and P9.
- **Current workflow**: master Excel calendar plus Outlook reminders plus memory.
- **Proposed workflow**: define each client entity once (state of incorporation, holder type, states with filing history, negative-report obligations) → the register **derives** the obligation list and its dates from the rules matrix rather than having them typed in → each obligation carries its evidence slots (due diligence completed, file generated, file validated, submitted, confirmation received, remittance sent, remittance cleared) → a season dashboard shows what is open, what is late, and what evidence is missing. Enforcement notices are logged with their type and postmark, and their response deadline is computed (e.g. Delaware VDA invitation + 90 days).
- **Inputs**: client/entity roster; prior filing history; notice intake.
- **Outputs**: derived obligation calendar; per-client filing history one-pager (the artifact a client asks for and an auditor asks for); open-item and overdue lists; notice clock report.
- **Essential features**: obligation derivation from rules, not manual entry; evidence completeness per obligation; negative-report obligations tracked explicitly; notice clocks.
- **Excluded from v1**: time tracking, invoicing, document storage, email integration, client portal. This must not drift into a practice-management system — the moment it stores documents it becomes a document repository and loses.
- **AI**: **inappropriate.**
- **Why not a spreadsheet**: a spreadsheet can hold the calendar but cannot *derive* it, and derivation is the whole point — the failure mode is an obligation nobody knew existed (a negative report, a second-step Remit Report, an insurer spring date), which a hand-maintained list can never surface.
- **Complexity**: medium. **Learning**: ~45 minutes.
- **Value**: prevents missed deadlines across a 100-client book; produces the client-facing compliance history that justifies the fee.
- **Risks/constraints**: scope creep is the primary risk. Store metadata and pointers, never client property data.
- **Substitutes**: Excel; enterprise platforms; generic project management (which cannot derive obligations from law).
- **Why still attractive**: the derivation is the differentiator, and it is only possible because of the rules matrix.
- **Paid customization**: firm-specific workflow states; client-branded compliance history reports; a hosted multi-user deployment.

---

### A5 — **PriorityRule**: jurisdiction sourcing sorter

- **User**: the analyst, immediately after address cleanup.
- **Problem**: P6.
- **Current workflow**: sort by state, sweep the blanks into the incorporation state.
- **Proposed workflow**: load property rows plus an entity table (entity → state of incorporation) → the tool applies first priority (owner's last known address state), then second priority (holder's incorporation state) for missing, foreign, or non-claiming-jurisdiction addresses, flags addresses that are structurally suspect (no state, foreign country, PO-box-only with no city/state, RPO-flagged), and outputs a per-state split with a reconciliation proving that input dollars equal output dollars.
- **Inputs**: property file with address fields; entity-to-incorporation-state table.
- **Outputs**: sourced file with a `priority_rule_applied` column; per-state dollar/count split; suspect-address exception list; dollars-in-equals-dollars-out reconciliation.
- **Essential features**: deterministic rule application with an explicit audit column; address parsing/normalization; reconciliation.
- **Excluded from v1**: address verification against USPS/CASS (a licensed service — allow an optional hook, do not build it); skip tracing.
- **AI**: **optional, narrow.** Address parsing for messy free-text address blobs is a reasonable model use; the priority determination itself must be rules.
- **Why not a spreadsheet**: a spreadsheet can do the sort but not the reconciliation-plus-audit-column combination that makes the result defensible years later, and it silently loses rows.
- **Complexity**: small. **Learning**: ~15 minutes.
- **Value**: prevents remitting to the wrong state, which is a pay-twice error.
- **Risks/constraints**: PII; local-only.
- **Substitutes**: manual; enterprise tools.
- **Why still attractive**: smallest build in the set, and it is a prerequisite for A1 (you cannot apply a state's dormancy rule before you know which state).
- **Paid customization**: per-client entity structures; foreign-address policies.

---

### A6 — **VoidTrace**: void/reissue reconciliation and false-positive filter

- **User**: the analyst scrubbing check registers; also directly valuable to the client's AP manager.
- **Problem**: P4.
- **Current workflow**: manual review of void codes; ad hoc VLOOKUPs.
- **Proposed workflow**: load a check register (issued, cleared, voided, reissued) → the tool matches voids to probable reissues on payee/amount/date proximity with a confidence score, isolates **voids occurring more than 30 days after issuance with no matched reissue** as presumed-reportable, and produces a documented disposition worksheet where a human records and preserves the explanation for each unmatched void.
- **Inputs**: check register export; optional bank outstanding-items file.
- **Outputs**: matched void/reissue pairs; presumed-reportable void list; disposition worksheet (the audit artifact); a summary of dollars removed from and added to the reportable population, with reasons.
- **Essential features**: fuzzy payee matching with a reviewable confidence score; the 30-day rule as an explicit, adjustable parameter; a permanent disposition record.
- **Excluded from v1**: bank statement OCR; ERP connectors; positive-pay integration.
- **AI**: **optional.** Fuzzy name matching is well-served by conventional string-distance algorithms; a model adds little and costs explainability. Recommend rules-and-distance first, and only consider a model if real data shows conventional matching failing.
- **Why not a spreadsheet**: it is done in a spreadsheet today, which is why the disposition rationale is never preserved — and the rationale is the part the auditor wants.
- **Complexity**: small-to-medium. **Learning**: ~30 minutes.
- **Value**: two-sided and quantifiable — dollars kept out of an over-remittance, and voids documented before an auditor presumes them reportable.
- **Risks/constraints**: matching errors in both directions; the tool must present matches for confirmation, never auto-apply.
- **Substitutes**: manual; some ERPs' own void reporting (which does not apply the escheat presumption).
- **Why still attractive**: the 30-day presumption is a bright-line rule that practitioners state plainly and that no general accounting tool implements.
- **Paid customization**: per-ERP register mappings; client-specific void-code taxonomies.

---

### A7 — **ExemptionScreen**: B2B and de minimis exemption candidate screener

- **User**: the provider's senior reviewer.
- **Problem**: P7.
- **Current workflow**: senior manual review, or skipped.
- **Proposed workflow**: over the sourced, dormancy-determined population, the tool flags rows whose (state, property type, owner type) combination falls inside a state's exemption or deferral regime, and asks the reviewer the specific conditional question that state's statute turns on ("is the business relationship ongoing?", "was this credit later refunded by check?"). Output is a per-row exemption memo with citation, plus a dollar total of exemptions claimed.
- **Inputs**: determined property population; owner-type classification (business vs individual); relationship-status answers.
- **Outputs**: exemption candidate list; reviewer question queue; exemption memo per state with citations; dollars-exempted summary.
- **Essential features**: the four-regime B2B taxonomy (full-broad, full-credit-balances-only, deferral, administrative-only) encoded per state with effective dates; conditional prompts; a memo the firm can hand to the client.
- **Excluded from v1**: auto-applying any exemption; gift card/breakage rules (a distinct and litigated area); securities.
- **AI**: **optional, narrow** — classifying an owner name as business vs individual from the name string is a legitimate small model use, human-reviewable. The exemption decision must remain a documented human answer to a coded question.
- **Why not a spreadsheet**: the value is the *conditional interrogation plus the citation memo*, not the lookup.
- **Complexity**: medium. **Learning**: ~1 hour (this is the concept closest to the one-hour ceiling; keep the question set small).
- **Value**: directly recovers client money; for contingency-priced providers it is fee-bearing work.
- **Risks/constraints**: highest professional-liability exposure of the set — an exemption wrongly claimed is an under-report. Ship as "candidates requiring professional judgment," never as a determination. Illinois's retroactive repeal is the standing reminder that effective-dating every rule is mandatory.
- **Substitutes**: enterprise software handles standard exemptions; conditional ones are manual everywhere.
- **Why still attractive**: it is the only concept here with direct dollar recovery, which makes ROI trivial to demonstrate.
- **Paid customization**: firm-specific risk positions; per-client relationship data feeds.

---

### A8 — **RetentionMap**: record-gap map and audit-estimation early warning

- **User**: the provider scoping an engagement, a VDA, or an audit defense; the holder's controller.
- **Problem**: P3.
- **Current workflow**: discovered during the audit, at the worst possible moment.
- **Proposed workflow**: build a grid of (report year × entity × record type: check register, bank statements, AR aging, due diligence letters, returned mail, remittance confirmations, filed reports) and record what exists, where, and in what format. The tool computes the required retention horizon per state (10 years + dormancy, or the state's own rule) and shades the cells where the state can invoke estimation because nothing exists.
- **Inputs**: manual inventory entry or a directory scan manifest; entity list; state list.
- **Outputs**: gap heat map; a prioritized "retrieve or recreate before it ages out" list; an audit-readiness one-pager.
- **Essential features**: retention-horizon computation per state; gap identification; export to a client-facing memo.
- **Excluded from v1**: storing the documents (this is an index, emphatically not a document repository); automated discovery beyond an optional filename manifest.
- **AI**: **inappropriate.**
- **Why not a spreadsheet**: the horizon arithmetic is per-state and changes as years roll; a static grid goes stale immediately and never warns anyone.
- **Complexity**: small. **Learning**: ~20 minutes.
- **Value**: the difference between a documented position and a Temple-Inland-style estimate — a gap measured in high six figures in the reported case.
- **Risks/constraints**: it tells clients uncomfortable things; frame as risk quantification, and be careful that a documented known gap is not itself used against the holder.
- **Substitutes**: none specific to unclaimed property retention horizons.
- **Why still attractive**: it is the cheapest build with the largest single documented dollar consequence, and it is a natural free lead-generation tool for a consulting practice.
- **Paid customization**: per-client retention policy drafting; integration with a records-management index.

---

### A9 — **VDAScope**: voluntary disclosure exposure scoping worksheet

- **User**: the provider's engagement lead, during intake and pricing.
- **Problem**: intake and scoping (P3/P9). Deciding whether to recommend a VDA, and what it will cost, is done today in a bespoke spreadsheet per prospect.
- **Current workflow**: ad hoc.
- **Proposed workflow**: enter the prospect's entities, incorporation states, filing history, revenue and property-source profile → the tool computes each state's lookback reach (years plus dormancy), identifies the years where records are known missing (from A8), estimates exposure ranges from whatever data exists, and prints a decision memo comparing VDA versus wait-for-audit, including the known dated windows (e.g. Delaware's 90-day VDA enrollment clock).
- **Inputs**: entity and history data; available-record inventory; rough property volumes.
- **Outputs**: per-state lookback and exposure range; record-gap overlay; VDA-versus-audit decision memo; engagement scoping estimate.
- **Essential features**: lookback arithmetic per state; scenario ranges rather than false precision; the memo.
- **Excluded from v1**: any claim of a defensible estimate — this is a scoping tool, not an actuarial one.
- **AI**: **inappropriate** for the arithmetic; **optional** for drafting the narrative memo from the computed figures.
- **Why not a spreadsheet**: it is a spreadsheet today; the gain is standardization across engagement leads and reuse of the rules matrix rather than each lead's own assumptions.
- **Complexity**: medium. **Learning**: ~1 hour, and it needs a trained user.
- **Value**: better-priced engagements and fewer under-scoped VDAs; but the value accrues to the firm's margin rather than to a compliance outcome, which caps its ROI clarity.
- **Risks/constraints**: an exposure number in writing is a discoverable document — must be labeled as an estimate for internal scoping only.
- **Substitutes**: each firm's own spreadsheet.
- **Why still attractive**: it is the concept most obviously worth paying for as a customization, even though it scores lowest as a free base product.
- **Paid customization**: this concept is essentially *all* customization — firm-specific pricing models and risk assumptions.

---

## 5. Opportunity ranking

Scores are 1–5 on each of ten criteria; maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of impl. | Narrow scope | Differentiation | Customization | Test data | Evidence confidence | **Total** |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| A2 | DiligenceWindow | 4 | 5 | 5 | 5 | 4 | 5 | 4 | 4 | 4 | 5 | **45** |
| A1 | DormancyDesk | 5 | 5 | 5 | 4 | 3 | 3 | 5 | 5 | 4 | 5 | **44** |
| A3 | NaupaCheck | 4 | 4 | 4 | 5 | 4 | 5 | 4 | 4 | 5 | 5 | **44** |
| A4 | FilingRegister | 4 | 5 | 4 | 5 | 4 | 4 | 3 | 5 | 4 | 5 | **43** |
| A6 | VoidTrace | 5 | 4 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 4 | **43** |
| A5 | PriorityRule | 4 | 4 | 4 | 5 | 5 | 5 | 3 | 3 | 4 | 5 | **42** |
| A8 | RetentionMap | 5 | 3 | 4 | 5 | 4 | 4 | 4 | 4 | 3 | 4 | **40** |
| A7 | ExemptionScreen | 4 | 3 | 4 | 4 | 3 | 4 | 4 | 5 | 3 | 4 | **38** |
| A9 | VDAScope | 4 | 3 | 4 | 3 | 3 | 3 | 4 | 5 | 3 | 3 | **35** |

### The top three

**A2 — DiligenceWindow (45).** It wins not because it is the most valuable function but because it is the best-shaped one. The requirement is the one practitioners themselves name as hardest; the rules are three independent per-state variables plus mandated letter language, all published and verifiable; the arithmetic is deterministic; the deliverables (letters, mail log, affidavit worksheet, certified-mail split) are concrete artifacts a user can hold; and the whole thing is learnable in twenty minutes. It also has the rare property of producing a *positive* outcome rather than only avoiding a negative one — every owner who responds to a letter is property that never escheats, which is the outcome the client actually wants and the one a provider can put in a year-end summary. It is the thinnest viable slice of the rules matrix, so it validates the expensive asset cheaply.

**A1 — DormancyDesk (44).** The highest-value concept and the one with the cleanest gap statement in this entire cycle: the free reporting tool that all fifty states point holders toward says, in its own FAQ, that it does not determine dormancy or escheatability. Everything above that line is enterprise-priced. It loses to A2 only on implementation effort and scope discipline — the rules matrix is a real research undertaking, and the temptation to keep widening it (securities, safe deposit, insurance-specific rules) is the main risk to the project.

**A3 — NaupaCheck (44).** Ties A1 on a different profile: lower ceiling, but the easiest to build, the easiest to explain, the best supplied with free realistic test data (state manuals publish layouts and sample files), and it carries a dated external catalyst in NAUPA III Phase 1 arriving Spring 2027 with staggered state acceptance. It also deliberately does not compete with HRS Pro — it validates what HRS Pro produces, which makes it additive to the incumbent's own user base.

### What to investigate next

**A2 first**, because it is the fastest route to a real user and it forces the first vertical slice of the rules matrix (thresholds, windows, methods, mandated language for a starter set of ten states). **A3 in parallel**, because it shares no dependencies with the matrix and can be built by a different pair of hands. **A1 third**, once the matrix format has been proven by A2 in production. A5 should be folded in as a preprocessing step of A1 rather than shipped alone. A9 should be treated as a paid customization, not a catalog product.

---

## 6. Validation plan

**Questions to ask practitioners**

1. Walk me through last season: how many client-state combinations did you file, and where did the hours actually go?
2. Show me the workbook you use to decide whether a row is reportable. Who built it? What happens if they leave?
3. How do you compute the due-diligence mailing window for a state you file in once a year? Have you ever discovered the window had closed?
4. What proportion of your scrubbing time is voids and reissues? How do you record *why* you removed something?
5. When did a state last reject or query a file? What was wrong with it, and how long did the round trip take?
6. Have you ever discovered you over-remitted — a B2B-exempt item, or a duplicate of a prior year? Did you attempt to recover it?
7. If a Delaware VDA invitation arrived at a client tomorrow, how would you find out, and how many days would you lose?
8. What would you need to see before you would trust a tool's dormancy determination over your own spreadsheet?
9. Would you accept a tool that runs entirely on your own machine and never uploads a file? Is that a requirement or merely a preference?
10. What do you do about NAUPA III? Has any vendor told you a date?

**Professionals and organizations to interview**

- Independent unclaimed property consultancies (UPCR, PEACC, Argent, Clarus, MarketSphere alumni) — the target buyer.
- UPPO members, especially the holder-side committee members who author the association's reporting guides; UPPO's annual conference is the single densest concentration of this population.
- In-house escheat coordinators found through unclaimed property analyst job postings — the job description itself enumerates the workflow.
- State unclaimed property administrators' holder-outreach staff — they see the defect rate across all filers and publish common-error lists (California's is public); they are the highest-information counterparty in the market.
- Wagers & Associates (HRS Pro) — to confirm the boundary of what the free tool will and will not do, and whether a complementary validator is welcome.

**Search terms for further research**

`holder reporting manual [state] unclaimed property 2026`; `NAUPA II record layout specification`; `NAUPA III XML schema phase 1`; `unclaimed property due diligence threshold certified mail [state]`; `B2B exemption unclaimed property [state] statute`; `unclaimed property negative report required`; `voluntary disclosure agreement unclaimed property [state] lookback`; `escheat analyst job description`; `UPPO reporting guide fall spring`; `unclaimed property audit estimation extrapolation`.

**Sample files and data needed**

- Three to five real (de-identified) check registers and AR credit-balance agings from different ERPs, to learn how much column-shape variation the intake layer must absorb.
- Sample NAUPA II files — states publish layouts and some publish samples; HRS Pro can generate valid ones for testing.
- The full set of state holder reporting manuals (free, public PDFs) — this is the raw material for the rules matrix and the largest single research cost.
- A set of real state deficiency/rejection notices, to learn what states actually reject on.

**A prototype that would validate the idea**

A single-page offline HTML application: paste or upload a CSV of reportable property with a state column and an amount column, pick a report deadline, and get back (i) per-state mailing open/close dates, (ii) the population split into must-mail / need-not-mail / must-mail-certified, and (iii) a downloadable merged letter set for three states with genuinely different rules — **California** (6–12 months before Notice Report, $50, mandated heading), **Texas** ($250 threshold), and **Ohio** (certified above $1,000). If an experienced analyst looks at that output and says "that is what I spent Tuesday doing," the matrix thesis is validated. Ten states of rule coverage is enough to prove it; fifty is the product.

**Assumptions most likely to make it fail**

1. **That the rules can be reduced to a matrix at all.** Some state rules are conditional, ambiguous, or contradicted by administrative practice (Texas and New York's B2B posture is guidance, not statute). If the "needs-review" bucket swallows a third of the rows, the tool is a slower spreadsheet.
2. **That maintenance is affordable.** Fifty-three jurisdictions legislate every year. An open-source matrix that goes stale is worse than no matrix, because it is trusted. The project lives or dies on a credible annual update discipline and visible effective-dating.
3. **That providers will trust an outside determination.** This population's professional liability rides on the answer. Mitigation: cite every rule, show the source text, and position output as "determination with provenance," never as advice.
4. **That the free tier does not cannibalize the paid customization.** Less likely here than usual — the customization value is per-client mappings and firm-specific positions, which a generic tool cannot supply.
5. **That NAUPA III arrives roughly on schedule.** A slipped or restructured Phase 1 blunts A3's catalyst, though the NAUPA II validator retains standalone value.

---

## 7. Cross-industry patterns

**Pattern 1 — "Regulatory rules matrix as versioned, cited data."** A jurisdiction × subject grid, published as machine-readable data with a citation and effective date on every cell, driving a deterministic determination and rendering a defensible memo. The scarcity is not the logic — it is that the rules exist only as fifty PDFs. **Transfers to:** *Multi-state charitable solicitation registration compliance* (~40 state regimes, already in backlog); *Multi-state income and franchise tax nexus monitoring for small businesses*; *State unemployment insurance cost control and SUTA experience-rating consultancies*; *Remote online notarization (RON) platform operators and RON-commissioned notaries*; *Consortium/third-party administrators (C-TPAs) for DOT drug and alcohol programs*; *Public adjusting firms* (state-by-state PA licensing and contract regulation).

**Pattern 2 — "Statutory notice window calculator plus compliant letter generator plus evidence log."** Where a law requires a specific notice, to a specific person, in a specific window, in specific words, with proof — compute the window, generate the letter, and keep the evidence. **Transfers to:** *Mortgage servicer payoff and lien release departments* (7-business-day payoff statutes, 30–90 day satisfaction clocks); *DBE/MBE/WBE compliance consultants* (49 CFR 26.53 good-faith-effort solicitation evidence files); *Community association (HOA and condominium) management back office* (statutory assessment and lien notices); *Building permit expediting and code consulting firms*; *Tax representation and IRS collections practices*.

**Pattern 3 — "Fixed-width/EDI pre-flight validator ahead of a scheduled format migration."** Validate the file before the counterparty rejects it, and report readiness for the announced successor format. **Transfers to:** *Home care and home health agency scheduling and EVV back office*; *Non-emergency medical transportation (NEMT) brokers and providers*; *Apprenticeship program sponsors and DOL RAPIDS reporting*; *Dental billing and insurance coordination* (electronic attachment adoption); *Workers' compensation medical billing and state fee schedule compliance* (state e-billing formats).

**Pattern 4 — "Void/reissue and duplicate-disbursement reconciliation with preserved disposition rationale."** Match reversals to their replacements, isolate the unmatched, and force the human explanation to be recorded rather than remembered. **Transfers to:** *Trust accounting and IOLTA three-way reconciliation for law firms*; *Independent pharmacy third-party reconciliation*; *Medical billing and revenue cycle* (refund and credit balance handling); *Small motor carriers back office and settlement*; *Retirement plan TPAs* (uncashed distribution checks).

**Pattern 5 — "Record-gap map that predicts adverse estimation."** Where an examiner may estimate liability for periods you cannot document, map the documentation before the examiner does and quantify the exposure. **Transfers to:** *DCAA-audit-ready incurred cost and indirect rate submissions at small government contractors*; *Workers' compensation class code and premium audit defense*; *Certified payroll and prevailing wage compliance service providers*; *Small defense suppliers navigating CMMC Level 2 compliance*.

---

## 8. Sources and confidence

### Verified findings (primary or authoritative sources, directly quoted or tabulated)

- HRS Pro does **not** determine dormancy or escheatability; free Standard edition is single-user and cannot export; Enterprise is $499/yr for 3 users — [HRS Pro FAQ](https://hrspro.unclaimedproperty.com/home/faq)
- NAUPA II is fixed-width and in use by all 50 states since 2004; NAUPA III moves to XML with **Phase 1 in Spring 2027**, coexisting with NAUPA II, described by NAUPA as "a significant technical and operational challenge" — [NAUPA reporting software and file format](https://unclaimed.org/reporting-software-and-naupa-file-format/), [NAUPA III](https://unclaimed.org/naupa3/), [NAUPA reporting overview](https://unclaimed.org/reporting-overview/)
- California: Notice Report before Nov 1, Remit Report June 1–15; life insurers May 1 / Dec 1–15; due diligence at **$50** and **6–12 months** before the Notice Report with mandated heading language; check remittance only under $2,000 — [California SCO How to Report](https://www.sco.ca.gov/upd_how_to_report.html), [California SCO Holder Due Diligence](https://sco.ca.gov/Files-UPD/upd_duediligence.pdf)
- California interest **12%** (CCP §1577), penalties to **$50,000** (§1576), roughly 10-year-plus-dormancy reach; FTB unclaimed property questions on Forms 100/100S/100W/565/568 — [BDO on California's unclaimed property law](https://www.bdo.com/insights/tax/californias-new-unclaimed-property-law)
- Vermont: May 1 deadline; 1/3/5/7/15-year dormancy by type; due diligence $50 and 60–180 days; $25 aggregate threshold excluding out-of-state addresses; NAUPA required above 10 items; notarized affidavit; **10-year retention** — [Vermont Holder Reporting Manual 2026](https://www.vermonttreasurer.gov/sites/treasurer/files/UnclaimedProperty/unclaimed-property-forms/Holder_Reporting_Manual_FINAL%202026.pdf)
- Due diligence variation: most states $25–$50; **Texas $250**; **Ohio and New York certified mail above $1,000**; **Florida exempts under $10**; ~41 fall states and ~9–10 spring states (DE, NY, CT, PA, FL, IL, MI, TX, VT) — [Wipfli](https://www.wipfli.com/insights/articles/tax-understand-the-rules-related-to-unclaimed-property-in-your-state), [PEACC due dates](https://peacc.com/state-reporting-unclaimed-property-due-dates/)
- Due diligence window standard of "no more than 120 and no less than 60 days prior to the report due date"; checks **voided more than 30 days after issuance** presumed reportable absent documentation; retention recommended at 15 years for a 10-year reach; conditional exemptions require manual review — [Baker Tilly, ten best practices](https://www.bakertilly.com/insights/ten-best-practices-unclaimed-property-compliance), [Baker Tilly, what AP teams need to know](https://www.bakertilly.com/insights/what-accounts-payable-teams-need-to-know)
- B2B exemption taxonomy: deferral (AZ, TN, MO); credit balances only (IN, IA, MA, MI, NC, WI); broad (IL, KS, MD, OH, VA); administrative only (TX, NY); states will not police over-remittance — [Baker Tilly on the B2B exemption](https://www.bakertilly.com/insights/unclaimed-property-unraveling-the-business-to-business-exemption)
- *Texas v. New Jersey*, 379 U.S. 674 (1965) priority rules; payroll dormancy commonly 1 year; RUUPA general 3-year dormancy; seven-year corporate retention versus longer state reach enabling estimation — [Journal of Accountancy](https://www.journalofaccountancy.com/issues/2020/nov/unclaimed-property-laws-risks/), [Texas v. New Jersey](https://supreme.justia.com/cases/federal/us/379/674/)
- Retention: most states 10 years plus dormancy; RUUPA §404 10-year minimum; estimation fills documentation gaps — [MarketSphere on record retention](https://www.unclaimedpropertyspecialists.com/knowledge-vault/record-retention-for-unclaimed-property-why-it-matters-and-how-to-get-it-right/)
- *Temple-Inland v. Cook*: 1986–2007 reach, estimated AP liability $1,176,767.77 versus ~$330,252.89 with other-state credits, "a game of 'gotcha' that shocks the conscience" — [DeCarrera Law case summary](https://decarreralaw.com/unclaimed-property/litigation/temple-inland-delaware/)
- 2026 enforcement: Delaware VDA invitation mailings in **April and August 2026**, each with a **90-day** enrollment window; shift to targeted outreach; California outreach campaign — [RSM, Delaware leads unclaimed property compliance (2026)](https://rsmus.com/insights/tax-alerts/2026/delaware-leads-unclaimed-property-compliance-states-increase-enforcement.html), [BDO on ignoring Delaware's VDA invitation](https://www.bdo.com/insights/tax/ignoring-delawares-unclaimed-property-vda-program-invitation-could-trigger-audit)
- Market size: ~$3B/yr to states; 8.6%–59% returned to owners; Delaware FY2019 $554.0M collected / $114.3M returned / $439.7M retained, third-largest revenue source; Illinois retroactively repealed its B2B exemption in 2017 — [Bloomberg Tax, "Killing the Golden Goose"](https://news.bloombergtax.com/daily-tax-report-state/killing-the-golden-goose-the-declining-health-of-state-unclaimed-property-programs)
- Common NAUPA file errors (wrong codes, mixed years/states, invalid characters and misalignment, missing encryption, skipped validation); required field set — [Eisen, How to create a NAUPA file](https://www.witheisen.com/post/how-to-create-a-naupa-file)
- Outsourced reporting service scope (data collection, dormancy matching, due diligence mailing and RPO handling, report generation and portal filing, legislation tracking) — [UPCR reporting outsourcing](https://www.upcr-llc.com/solutions/unclaimed-property-reporting-outsourcing/)
- First-time filing is itself an audit trigger; electronic payments routinely omitted; M&A liability inherited — [MarketSphere, first-time reporting considerations](https://www.unclaimedpropertyspecialists.com/knowledge-vault/first-time-unclaimed-property-reporting-considerations/)
- State notice types (compliance reminders, examination notices, amnesty/self-audit invitations) and their clocks — [MarketSphere, state notices best practices](https://www.unclaimedpropertyspecialists.com/knowledge-vault/state-unclaimed-property-notices-best-practices/)
- "The most difficult unclaimed property requirement for businesses to fulfill is the obligation to perform due diligence" — [IOFM](https://www.iofm.com/ap/compliance/unclaimed-property/due-diligence-letter-requirements) (headline text visible; detail paywalled)

### Strong inferences (well-supported by the above, but not stated verbatim by a source)

- The primary buyer is a 3–25 person consultancy or a 2–8 person practice group inside a CPA firm. Inferred from the observable firm profiles of UPCR, PEACC, Argent and Clarus and from the structure of the outsourced service offering; not confirmed by headcount data.
- The rules matrix does not exist as open machine-readable data. Inferred from NAUPA publishing state profiles as web pages/PDFs and from the absence of any such dataset in searches; a proprietary matrix certainly exists inside Sovos and Kelmar.
- The provider-side per-season volume (100 clients × up to 20 states = ~2,000 window computations) is arithmetic on plausible book sizes, not a measured figure.
- Excel is the actual system of record for dormancy determination at sub-enterprise scale. Strongly implied by HRS Pro's disclaimed scope and by Baker Tilly's recommendation to build a "state research matrix," but not directly observed.
- Over-remittance is common and unrecovered. Supported by the explicit statement that states accept anything and do not police exemptions, but no measured over-remittance rate was found.

### Tentative hypotheses requiring practitioner validation

- That analysts would adopt a determination engine they did not build. Professional-liability instincts may prove stronger than the time saving. **This is the assumption most likely to kill A1.**
- That a strictly local, no-upload tool is a selling point rather than an inconvenience. Plausible given SSN-bearing files, but untested against a population that already uploads to state portals.
- That NAUPA III readiness is a felt need in 2026 rather than a 2027 problem nobody has budgeted. The catalyst may be real but early.
- That the ~$25–$50 due diligence threshold band and the 60–120/60–180 day windows generalize cleanly. Verified for CA, VT, TX, OH, NY, FL; the remaining ~47 jurisdictions were not individually checked and almost certainly contain surprises. Any build must start by reading all fifty manuals.
- That providers, not in-house coordinators, are the better first users. The in-house coordinator has more acute pain and less budget; the provider has budget and more sophisticated substitutes. Which one adopts first is genuinely unresolved.
