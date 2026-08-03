# Machine Shops / Job Shops — Handoffs and QA

**Market research cycle · 3 August 2026**

---

## 0. Cycle header

| | |
|---|---|
| **Market claimed** | Machine shop / job shop quoting and production control |
| **Angle claimed** | handoffs-and-qa |
| **Claim ID** | `868d73ee` |
| **Date** | 2026-08-03 |
| **Claim attempts** | 1 (no push conflict) |
| **Backlog at time of claim** | 141 assignments remaining |

### Why this assignment over the others available

The ledger held 4 completed entries and 142 open assignments at clone time, with **zero active claims**. The completed set covered immigration law, fire protection, insurance agencies (back-office), and land surveying.

Applying the brief's ordering:

1. **Zero-coverage market.** Four markets had coverage; machine shops had none. This eliminated the covered four but left ~24 candidates.
2. **Angle diversity — this was the deciding factor.** Of four completed reports, **three** were `core-practitioner-workflow` and one was `back-office`. Both `narrow-subspecialty` and `handoffs-and-qa` had **zero** coverage across the entire catalog. Claiming a `handoffs-and-qa` assignment corrects the catalog's biggest structural blind spot, and it does so at the point where the brief's opportunity criteria bite hardest — handoffs are where documents cross organizational boundaries, which is exactly where narrow document-processing tools earn their keep.
3. **Expected evidence density, adjusted for a known environmental constraint.** A prior cycle in this repository established that **reddit.com is unreachable from this environment**. That fact should shape market selection, not just be reported afterward. Machine shops are one of the few markets whose practitioner discourse lives almost entirely *outside* reddit: **Practical Machinist** and the **Elsmar Cove** quality forum are both long-running, open, and populated by named practitioners posting under real professional identities. Elsmar in particular is the largest quality-management practitioner forum in existence and is precisely on-angle. I selected a market whose evidence I could actually reach.

A secondary consideration, mirroring the ALTA timing in the prior land-surveying cycle: this market is sitting inside **three simultaneous regulatory transitions** — AS9102 Rev C with no mandated transition date, FDA's QMSR effective 2 February 2026, and the CMMC phase-in — each of which creates dated, checkable requirements that narrow software can encode.

### Scope discipline: what "handoffs-and-qa" means here

This report deliberately excludes machining, toolpaths, work scheduling, and shop-floor production control. It covers only the boundary between the shop and the outside world: **inbound** customer RFQ packages, drawings, revisions and purchase-order quality clauses; **outbound** first article inspection reports, certificate packages and shipped documentation; and **lateral** coordination with outside processing vendors, plus the nonconformance and corrective-action traffic that runs in both directions.

### Evidence limitations, stated up front

- **reddit.com blocked** (confirmed again this cycle; not retried at length).
- **practicalmachinist.com returns HTTP 403 to automated fetching.** Its threads were reachable only through a text proxy. Quotations attributed to Practical Machinist below came through that route and carry slightly lower transcription confidence than the Elsmar material, which was parsed from raw HTML.
- **No neutral benchmark exists** for characteristics-per-print or hours-per-FAIR. Every quantitative claim in that area is either a practitioner's own estimate or vendor marketing. Both are labelled as such throughout.
- Job-posting evidence is thin this cycle — the available job-search tooling returned few results per query.

---

## 1. Market examined

**Industry.** Machine shops, NAICS 332710. US Census data reports **17,530 establishments and 209,280 employees** — an average of roughly **12 employees per establishment**. ([NAICSList / Census](https://naicslist.com/naics/332710)) The SBA small-business threshold for the industry is 500 employees, which tells you the entire industry is small by federal definition and overwhelmingly small in practice.

**Target organization size.** **5 to 75 employees.** Below five, the owner does everything and buys nothing. Above roughly 75, a dedicated quality department exists with budget authority and the shop is a candidate for High QA or Net-Inspect at list price. The 5–75 band is where a single quality manager — frequently the only one — owns first articles, cert packages, gage calibration, customer audits, corrective action, and the ERP's quality module simultaneously.

The scope of that one role is documented directly. A shop owner with **four shop-floor employees and about a dozen jobs a month**, hiring his first quality lead, described the job as *"the authority on GD&T, CMM programming, reporting and documentation, inspection scheduling and basically run every step of the way"* and was prepared to pay *"up to 6 figures."* A respondent added the rest of the bundle: *"The paperwork, FIA's, keeping up with metrology equipment certs, etc all fits under that window."* ([Practical Machinist](https://www.practicalmachinist.com/forum/threads/hiring-someone-to-run-a-quality-department.415601/))

**Roles at the handoff boundary.**

| Role | What they do at the boundary | Tools |
|---|---|---|
| **Owner / GM** | Accepts the contract, including its quality obligations — often without reading them | Email, PDF, quoting software |
| **Quality manager** | FAIRs, cert packages, CofC signature, corrective action responses, customer audits, approved-vendor records | Excel, fillable PDF, scanner, ERP |
| **Inspector / CMM programmer** | Measures, records results, feeds the FAIR | CMM software, calipers, paper, Excel |
| **Estimator** | Quotes the job — typically without pricing the quality requirements | Quoting software, spreadsheets |
| **Buyer / purchasing** | Issues outside-processing POs carrying flowed-down specs | ERP, email |
| **Shipping clerk** | Assembles and ships the paperwork packet | Printer, filing cabinet, ERP |

**Customer mix.** Aerospace and defense (AS9100 / AS9102 / ITAR / DFARS / CMMC), automotive (IATF 16949 / PPAP), medical (ISO 13485 / FDA QMSR), and general industrial. Many shops serve several of these at once, which is the origin of a large share of the pain in Section 3 — the same physical part must be documented in three different dialects.

---

## 2. How the work is performed

### 2.1 Inbound: RFQ and contract review

An RFQ arrives as email with attached PDFs — usually 2D drawings, frequently scanned, frequently old. The estimator quotes from the print. Quality requirements ride along in the purchase order and in referenced clause documents, and this is where the first structural failure occurs, described plainly by a supplier-side quality practitioner:

> *"Some P.O.s call it all out in the P.O. itself, and others also reference additional documents. **Often nobody has read all these requirements, and there may be surprises.**… We make computer gear, and I routinely receive aircraft engine repair specs as parts of P.O.s, as well as nuclear reactor and other N/A language."* — normzone, [Elsmar](https://elsmar.com/elsmarqualityforum/threads/purchase-order-quality-clauses.71375/)

The volume problem is real in both directions. From the same thread: *"If we included every non applicable thing that was thrown out for flowdown our PO could easily reach **20 - 50 pages on every single job. Even for something as simple as zinc phosphate.**"* (Eredhel). And clauses attach to the *customer-plus-product* combination, not to the vendor — *"a PO for steel for that customer may not get a specialty metals PO code, but a PO for a different customer for the same steel from the same vendor may get such a code"* (Mike S.).

The recognized remedy is a formal contract review before acceptance. Wes Bucey's framing on Elsmar is that a cross-functional team must examine *"the niggledy piggledy points… **BEFORE** accepting the contract."* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/ppap-including-fai-parts-customer-is-requiring-5000-measurements.45712/)) What actually happens is described in the same thread by TShepherd: *"Many of the people that do the quote process **don't take quality into consideration** and then you get into a corner because you need a gage or an exceptional layout… in order to ship parts and get paid."*

### 2.2 Production and the first article

For a new part, AS9102 First Article Inspection is the gate. **AS9102 Rev C is current, published June 2023** ([SAE](https://www.sae.org/standards/as9102c-aerospace-series-first-article-inspection-requirements/), [Accuris](https://store.accuristech.com/standards/sae-as9102c?product_id=2568218)) — and critically, **there is no industry-mandated transition date**; adoption is customer-by-customer, so shops maintain Rev B and Rev C form sets simultaneously ([AUVA](https://auva.com/2024/04/23/as9102-revision-c-noteworthy-changes-and-implications/)).

The three forms: **Form 1** part number accountability (Rev C renamed "FAIR Number" to "FAIR Identifier", made field 14 "Reason for Full/Partial FAI" mandatory for *all* FAIs, and changed field 17 from "Part Serial Number" to "Part Type"); **Form 2** product accountability — every material and special process backed by a specific certificate; **Form 3** characteristic accountability — one row per ballooned characteristic with requirement, result, and specific measurement method. Rev C removed the signature fields from Forms 2 and 3, so signing Form 1 locks all three into one record, and Form 1 is signed **last**. ([Net-Inspect Rev B vs C](https://www.net-inspect.com/blog/as9102-rev-b-vs-rev-c/), [QualityEngineer.ai](https://app.qualityengineer.ai/blog/as9102-fai-form-1-2-3))

The work itself, described step by step by a quality manager at a shop pursuing AS9100:

> *"1. Bubbling the characteristics on the drawing (could be anywhere from **5 to 500** depending on the part being made. 2. Transferring all the characteristic and requirement data from the drawings to our AS9102 based FAI forms (**this is a manual typed process on a fillable pdf form**). 3. Inspector fills out the results sections… **It can take 4-5 hours to get one part processed!** Is that a normal amount of time for an FAI?"*
> — CanadianQA, [Elsmar](https://elsmar.com/elsmarqualityforum/threads/as9100-clause-8-5-1-3-first-article-inspection-costs.73620/)

And the business consequence, from the same post: *"My General Manager had a bit of a freak out today about **'how we're supposed to make money when we have to FAI every new part'.**"*

A rule of thumb offered in reply gives a costing basis: *"each feature takes approximately **2 minutes** - based on complexity - so do the math"* (dsanabria). Characteristic counts corroborate: one practitioner built a custom workbook because *"when there are **200-300 measurements**, it makes it a heck of a lot easier for the inspector to know where problems are"*; another posts a template with *"**500 rows**, tis a small one."* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/as9102-fai-first-article-inspection-form-example.20933/))

### 2.3 Measurement and result capture

Results come off CMMs, calipers, micrometers and gages. Getting them into the customer-facing form is largely retyping. Quality Magazine's own how-to instructs readers to *"**Avoid retyping printed CMM data into a FAIR.** It's time consuming and error-prone"* ([qualitymag.com](https://www.qualitymag.com/articles/95613-how-to-create-an-as9102-first-article-inspection-report)) — advice that only exists because retyping is the default. Ideagen states the baseline directly: *"Filling out Form 3 by hand means **retyping every balloon number, characteristic and measurement** into a spreadsheet."* ([InspectionXpert](https://www.inspectionxpert.com/blog/how-to-fill-out-an-as9102-first-article-inspection-report-with-excel))

**CMM data import is a paid upgrade in both major products** — InspectionXpert gates it behind Advanced ($235/mo vs Standard $125/mo, [SoftwareSuggest](https://www.softwaresuggest.com/inspectionxpert)) and SOLIDWORKS gates it behind Inspection Professional, with only Standard publicly priced at **$599/yr** ([Design & Process](https://designandprocess.com/product/solidworks-inspection-standard/)).

### 2.4 Outside processing

Heat treat, plating, anodize, NDT and coatings go out. Nadcap covers **24 critical-process accreditation programs** with 60+ subscribing OEM members ([PRI](https://www.p-r-i.org/nadcap)), and customer flow-downs make approved-processor status a hard gate: General Dynamics Mission Systems requires the supplier to ensure it is approved for the process *"**PRIOR TO shipment of any product**"* whether performed in-house or outsourced ([GDMS](https://gdmissionsystems.com/-/media/general-dynamics/suppliers/terms-and-conditions/gdms-specialprocesses.ashx)).

Third-party estimates put Nadcap accreditation at $2,500–$3,000 application per process, $10,000+ minimum on-site audit, $3,000–$5,000 annual maintenance, and 12–18 months total ([AQM Auditing](https://aqmauditing.com/cost-timeframe-for-gaining-nadcap-certification/)) — which is why a 5–75 person shop sends the work out and inherits the paperwork burden instead.

That burden is described as structurally backwards by the people carrying it:

> *"Boeing has recently updated D1-4426 Addendum… This has required all processes to have PSD's called out for all high level specifications on purchase orders. **We too (aerospace machine shop) are having many problems with this** and flowing the PSD's down to the processors. There is no flow down from our customer, only Boeing. **It is forcing us non plating/heat treat experts to tell our processors what they need to do. It is completely backwards from how it should be.**"* — erinpristel, [Elsmar](https://elsmar.com/elsmarqualityforum/threads/nadcap-processor-po-purchase-order-requirements.60813/)

Scale, from the same thread: *"For Boeing you need to know the aircraft type and which division the part is going to so that you can make sure you are using the applicable departures from the base spec… **Some specs can have 20 or more departures**"* — and, critically, *"This is an ongoing issue that **has resulted in escapes** so is getting some visibility"* (andygr).

### 2.5 The cert package and shipment

Parts ship with paperwork. There is **no industry-standard name for it**, which is itself diagnostic. A newly promoted assistant quality manager asked what to call it and got four different answers — "cert package," "the paperwork," "shipping docs," "doc package," "Tool Inspection Package" — with Mike S. noting *"**there is no standardized term I know of**. Sometimes it is just one page… **Sometimes it can be dozens of pages**."* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/documentation-accompanying-an-aerospace-part.84250/)) The contents, per a practitioner in the same thread: *"Certificate of Conformance / AS 9102 Inspection Documentation / All Material(s) and Outside Process Certifications. **Always read the Purchase Order for any other Quality Requirements. Also see if there is a Source Inspection Requirements.**"*

Required CofC content is dictated by each customer. Lockheed Martin Aero's Appendix QX specifies seller facility name and address, date, PO/contract number, part number, traceability data, quantity, variance/deviation numbers, special handling notes, and an authorized signature (electronic accepted) ([LM Aero App QX](https://www.lockheedmartin.com/content/dam/lockheed-martin/aero/documents/scm/Quality-Requirements/Quality-Appendices/AppQX_rev10.pdf)). A smaller shop's own supplier flow-down requires raw-material certs *from the original product manufacturer* with manufacture date, production lot, batch and **heat lot**, and for coatings the **average coating thickness documented** ([Global Machine Works](https://globalmachineworks.com/wp-content/uploads/2025/09/Supplier-Quality-Requirements-Rev-9_17_2025.pdf)).

How the final control actually works:

> *"when a product is ready to be shipped, the shipping manager/clerk comes to me, the Quality Manager, to sign off on the CofC… **I don't actually confirm anything** w/ respects to the product being shipped… **I basically 'blindly' sign the CofC.** Second, **it wastes so much time for shipping to run up & down the hall looking for someone to sign the CofC before they can actually ship product out the door.**"* — SLSHappy, quality manager at a ~50-employee FAA-regulated manufacturer, [Elsmar](https://elsmar.com/elsmarqualityforum/threads/certificate-of-conformance-compliance-cofc-share-your-best-business-practices.15686/)

Veteran aerospace auditor Sidney Vianna, in the same thread: *"**In my experience, many people signing on a CoC have no idea of what they are signing for.**"*

### 2.6 Nonconformance and corrective action

Clocks are contractual and short. Lockheed Martin Aero: potential quality escape notification within **3 business days**, supplementary information within 5; **flight-safety or counterfeit concern within 24 hours**; approved corrective action on a SCAR within **30 calendar days**. Global Machine Works requires escape notice within **one business day** of a nonconformance being determined *or suspected* on delivered product.

The supplier-side experience: *"I have been on the receiving end of a Scar with **triplex 8D required within two weeks for individual isolated defects**, and that is not a fun place to be. **We actually charge those customers more now** due to the extra work."* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/suppliers-not-responding-to-supplier-corrective-action-requests-scar.69081/)) And from a quality manager at a supplier: *"at least **half of our top customer's RCCA requests turn out to be not our fault**, but they are the customer and I owe them the professional courtesy of a response."*

### 2.7 Software actually in use

| Category | Products | Pricing where published |
|---|---|---|
| Ballooning / FAI | Ideagen Quality Control (ex-InspectionXpert), High QA, DISCUS, SOLIDWORKS Inspection, Net-Inspect, 1factory, QA-CAD, Balloonist.io, GroundControl | Ideagen **$125–$235/mo**; SW Inspection Standard **$599/yr**; 1factory **$75/user/mo, 5 min**; QA-CAD **$1,195 perpetual**; Balloonist **$30/user/mo**; Net-Inspect from **$500/mo**. High QA, DISCUS, Verisurf, ETQ: **quote only** |
| Job shop ERP | E2 Shop, JobBOSS², ProShop, Global Shop, Fulcrum, MIE Trak, Realtrac, Steelhead | E2 **$45–$100/user/mo**, implementation $5k–$60k; Global Shop **$65–$200/user/mo**, implementation $20k–$250k; Fulcrum **$6k–$18k/yr unlimited users** |
| Quoting | Paperless Parts, MIE Trak, Machine Research | No published pricing; no free trial at Paperless Parts |
| CMM / SPC | PC-DMIS, Calypso, Prolink QC-CALC, Verisurf | QC-CALC Real-Time **$1,950** |
| Cert management | — | **No category leader exists** |

Sources: [ERP Research E2](https://www.erpresearch.com/pricing/e2-shop-system), [ERP Research Global Shop](https://www.erpresearch.com/pricing/global-shop-solutions), [Software Connect Fulcrum](https://softwareconnect.com/reviews/fulcrum-pro/), [1factory pricing](https://www.1factory.com/pricing.html), [QA-CAD](https://www.guthcad.com/order_qacad.htm), [Balloonist](https://balloonist.io/), [Capterra Net-Inspect](https://www.capterra.com/p/88288/Quality-Improvement-Software/), [MSI Viking QC-CALC](https://www.msi-viking.com/Prolink-QC-CALC-Real-Time-Data-Collection-Softw)

Two structural facts about this landscape matter more than any individual price:

**No ERP in this market advertises drawing ballooning or AS9102 form generation as a native capability.** The ballooning vendors exist because that gap is universal. Conversely, MIE Trak reviewers report *"The quality module is limited"* and *"Limited document control capabilities compared to enterprise alternatives"* ([Capterra](https://www.capterra.com/p/161558/MIE-Trak-Pro/)).

**A search for "certificate of conformance software" returns almost entirely free Word and PDF templates, not products.** There is no category leader for the single most frequent outbound document in this market.

---

## 3. Most important problems — ranked

### Problem 1 — The cert package is assembled by hand, gates shipment, and the final control is a signature nobody stands behind

**Who.** Quality manager and shipping clerk. **When.** Every shipment. **Frequency.** Daily.

**How handled now.** Someone collects the CofC, the FAIR if applicable, material certs, and every outside-process cert; staples or PDFs them together; walks it down the hall for a signature. Storage underneath is folders and scans: one shop describes *"we scan every one of them and store them under the customer name then the parts number then the order number and date. This saved us 4 filing cabinets of paperwork"* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/qms-and-iso-9001-for-a-single-person-machine-shop.68746/)).

**Why inadequate.** Three independent failures compound. (1) **The composition varies by customer and nobody has it written down** — hence the "what do you even call this" thread and four different answers. (2) **The verification step is theatrical**: the quality manager signing the CofC states plainly that he *"doesn't actually confirm anything"* and signs *"blindly."* (3) **It blocks revenue** — shipping cannot release product while hunting for a signature.

**Cost.** Direct: shipping delay per shipment, plus the quality manager's interruption. Indirect and much larger: **missing or incomplete material certificates on Form 2 are cited as the single most frequent cause of FAIR rejection** ([Unitek Kiwa](https://www.unitek-kiwa.com/blog/as9102-first-article-inspection-guide/), [QualityEngineer.ai](https://app.qualityengineer.ai/blog/as9102-fai-form-1-2-3)). A rejection means the parts are delivered but not accepted, which means not paid.

**Evidence strength: high.** Multiple named practitioners, a veteran auditor's corroboration, two customer supplier-quality manuals specifying required content, and a documented absence of any software category serving it.

---

### Problem 2 — Purchase-order quality clauses are not read until they are breached

**Who.** Owner/estimator at quote, quality manager at execution. **When.** Contract acceptance. **Frequency.** Every new customer and every new PO from an existing one.

**How handled now.** Nothing systematic. The quotes go out priced on machining. The clauses are discovered later.

**Why inadequate.** The failure mode is documented at both ends. At quote: *"Many of the people that do the quote process don't take quality into consideration and then you get into a corner because you need a gage or an exceptional layout… in order to ship parts and get paid."* At execution, the worst documented case: a machine-shop quality manager discovered post-award that his customer wanted **50 nest positions × 5 repetitions × 20 dimensions = 5,000 measurements**, all hand-written onto customer-supplied forms — with **no PPAP charge agreed**, because *"They started this project before I took this job."* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/ppap-including-fai-parts-customer-is-requiring-5000-measurements.45712/))

**Cost.** Unbounded on the downside, because it is discovered after the price is fixed. At 2 minutes per characteristic, 5,000 measurements is ~167 hours of unpriced inspection labor on one job.

**Evidence strength: high.** Named practitioners at three different shops describing the same failure, plus a documented catastrophic instance.

---

### Problem 3 — Ballooning and FAIR production consume hours per part, and most of the output is never read

**Who.** Quality manager and inspector. **When.** Every new part number, and again on many revision changes.

**How handled now.** Balloon the print (5 to 500 characteristics), retype every characteristic into a fillable PDF or Excel, fill in results by hand. Practitioner-reported: **4–5 hours per part**, with a **~2 minutes per feature** rule of thumb. The tools that exist are either expensive, disliked, or both — Capterra reviewers on Ideagen: *"The cost is not budget friendly and it is very costly for us to renew each year"*; *"OCR can be glitchy"*; *"an old-fashioned interface and limited user-friendliness"* making it *"a tedious tool to use regularly"* ([Capterra](https://www.capterra.com/p/210181/Ideagen-Quality-Control/)). High QA's per-seat model draws *"I wish the pricing was per organization, and not per user"* ([Capterra](https://www.capterra.com/p/248001/High-QA-Inspection-Manager/)).

Auto-ballooning has a hard accuracy ceiling: a vendor comparison puts it at **85–90% on clean drawings**, with **1–3 hours of manual correction on complex drawings**, and residual failures concentrated in datum references, ISO 2768 blanket tolerances, fit-class expansion and cross-sheet duplicates ([Mavlon](https://mavlon.co/post/auto-ballooning-software-aerospace-fai-compared)). And the input is usually bad: a practitioner notes *"the majority of the prints we receive here are older and are usually in PDF format"* requiring you to *"double check the OCR on some older scanned prints"* ([Practical Machinist](https://www.practicalmachinist.com/forum/threads/first-article-inspection-software-or-documentation.382354/)).

**The part that reframes the whole problem:**

> *"I have done probably **1000 FAI's since 2005**. I would estimate that **95% of those received no response from the customer**. Out of about 50-75 customers involved, **I can count on one hand the number who actually seem to review these.** Interestingly, **Boeing is one who never responds**."* — Jimw1954, [Elsmar](https://elsmar.com/elsmarqualityforum/threads/am-i-allowed-to-ship-parts-without-fai-approval-from-the-customer.67821/)

Corroborated in the same thread: *"I have probably done about **150 FAIR's over the last 3 years** and I think I have got about **6 returned signed**… Sometimes **3-4 months go by** and I will receive an e-mail asking me to change/fix/update a FAIR that I did (typo typically)."* (Michael_M)

**Why this matters for opportunity selection.** The FAIR is a mandatory artifact that is mostly unread but occasionally rejected months later — often for a typo. That profile argues **against** building another ballooning tool (the space has 10+ entrants) and **for** building something that makes the artifact correct on the first submission at near-zero marginal effort.

**Cost.** 4–5 hours per new part number, at a role paid toward six figures in some shops.

**Evidence strength: high on effort and tooling; medium on the 95%-no-response figure** — it is one experienced practitioner's estimate, corroborated in magnitude by a second, but it is not measured data.

---

### Problem 4 — Drawing revisions arrive mid-job, and most of them are not technical

**Who.** Programmer, quality manager, production manager. **When.** Unpredictably. **Frequency.** Constant.

**Evidence, both directions.** Money lost to a stale revision: *"the end customer **changed the drawing with an updated revision AFTER they sent the parts out to get made. They never told our customer and they never told us. They just rejected the parts when they came in.**"* Exposure quantified by the poster: *"1750 in material about 3 days of waterjet time and about a week of spindle time."* ([Practical Machinist](https://www.practicalmachinist.com/forum/threads/custom-sent-wrong-drawing-who-should-pay.369452/))

Revision landing mid-operation: *"I am currently in the middle of a part that is on Revision E and **they sent a new Revision F while I was running the first operation**"* — with the poster noting his workaround leaves *"the possibility to accidentally select features from outdated revisions."* A second: *"I deal with rev changes all the time midstream and it is super annoying… Last time a big change happened I was **halfway through programming about 150 toolpaths**." ([Practical Machinist](https://www.practicalmachinist.com/forum/threads/how-do-you-deal-with-revision-changes.395938/)) Controls in use are physical: *"I stamp the print 'Void' and attach the new print with a form"*; *"the old print is shredded."*

And the redundant-paperwork half, from a fastener supplier holding *"**Well over 2000**"* first articles:

> *"another drawing change for Airbus where they changed the drawing ownership (name on top of print) from Aerospatiale to EADS… **There was absolutely no technical changes**… **We get revision changes like this all the time and it's rather frustrating.**"* — TRBOKEV, [Elsmar](https://elsmar.com/elsmarqualityforum/threads/as9102-fair-customer-drawing-revision-change.59211/)

With a fellow practitioner adding: *"More paper does not make the FAI better for these type of changes and IMO is mainly done for **those who value format over function**."*

**Why inadequate.** The shop cannot cheaply answer the two questions that matter: *did anything I machine to actually change?* and *does this trigger a full or partial FAI?* AS9102's triggers are documented — a change in manufacturing source, process, inspection method, location, tooling or materials *"that can potentially affect fit, form or function"*; a two-year production lapse normally requires a **full** FAI ([IAQG AS9102 FAQ](https://endevco.com/contentstore/mktgcontent/endevco/uploads/2019/02/AS9102-frequently-asked-questions1.pdf)) — but applying them requires knowing what changed.

**Cost.** One documented instance: material plus ~8 machine-days. Plus recurring FAIR rework for changes with no technical content.

**Evidence strength: high.**

---

### Problem 5 — Outside-processing flow-down is performed by people who are not the process experts, and it produces escapes

**Who.** Buyer and quality manager. **When.** Every outside-processing PO. **Frequency.** Most aerospace jobs.

**How handled now.** Homegrown discipline. One shop's control: *"We give the special process house an operation sheet with all requirements, and **reference 'Op50 RevC 9/12/11' on the PO, so the purchasing dept doesn't miss something.**"* Required cert content is enumerated by hand — one practitioner lists aircraft model, P/N, model revision, spec revision, serial number, date performed per operation, accept/reject per operation, main cert date, *"and in extreme cases i have seen called out primer batch and sol gel batch # as well as certs from the distributor (not the processing house)."* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/nadcap-processor-po-purchase-order-requirements.60813/))

**Why inadequate.** Twenty-plus departures per specification, applied by non-specialists, with an explicitly acknowledged consequence — *"has resulted in escapes."* Meanwhile approved-vendor records rot: a new quality engineer found *"**several vendors the company had been using for years that were never approved or had any records at all**,"* including a *"critical sole source vendor"* who would not respond, while buyers *"will not help me"* and his supervisor insisted he approve them *"by any means necessary."* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/approved-vendor-list-non-responsive-vendors-requiring-approval.92003/)) A colleague's workaround for confirming a vendor still existed: *"We looked them up on **Google Maps and called the business located in the building next door**."*

Parts also get damaged out there and nobody counts it. A startup lost 19 of 200 anodized parts (9.5%); the veteran response was *"You will be lucky to get them to pay for the material… **This is why the shop that made the parts left you to deal with the plating shop. Happens all the time**"* and *"You always need make extras… finisher mess a few up etc."* ([Practical Machinist](https://www.practicalmachinist.com/forum/threads/what-should-happen-when-a-metal-finishing-shop-ruins-parts.253525/)) *(Inference: shops absorb this as a scrap allowance rather than as vendor performance data.)*

**Evidence strength: high on flow-down and approved-vendor decay; medium on the scrap-absorption inference.**

---

### Problem 6 — Material traceability breaks between the certificate and the finished part

**Who.** Receiving, production, shipping. **When.** Continuously. **Frequency.** Every material lot.

**How handled now.** A quality consultant documenting real shops found: a **Dropbox folder organized by supplier and date**; a **filing cabinet organized by PO number**; and certs **zip-tied to the bar stock** — *"unzip the tie, pull the bars, and zip it back."* Their diagnosis is precise: *"**the gap is the link between each certificate and the specific finished part it became**,"* broken at three points — receiving→storage lot commingling, storage→production with heat lot undocumented, and production→shipment where multi-lot jobs cannot be recalled ([Kaizen ISO Consulting](https://kaizenisoconsulting.com/articles/material-traceability-beyond-certification-shuffle)).

A shop describing its own method on Elsmar: *"we would print out a copy of the goods receipt paperwork and **attach it to the top billet with sellotape**. If they sit a while the paper can become ripped or loose and **we can lose traceability**."* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/raw-material-traceability-in-a-machine-shop-aluminium-billets.91539/))

**Why inadequate.** The regulatory demands are specific and the sellotape does not meet them. DFARS **252.225-7008** requires specialty metal *"melted or produced in the United States or its outlying areas"*; **252.225-7009** extends to articles containing specialty metals with a qualifying-country allowance and a **2%-by-weight de minimis** ([acquisition.gov](https://www.acquisition.gov/dfars/252.225-7008-restriction-acquisition-specialty-metals.), [Cornell LII](https://www.law.cornell.edu/cfr/text/48/252.225-7009)). Customers require *"lot traceability to the melt"* ([Sensata/Kavlico](https://www.sensata.com/sites/default/files/a/kavlico-supplier-quality-requirements-manual-ap0425.pdf)). Counterfeit-materiel controls per **AS6174** — the non-electronic standard that actually applies to bar stock and hardware — must be flowed to sub-tiers. And LM Aero requires record retention of **3 years, or 7 for special-process work**.

**Cost.** Latent until a recall or an audit finding, at which point it is existential.

**Evidence strength: high** — practitioner accounts, a consultant's field observations, and primary regulatory text.

---

### Problem 7 — Every customer wants the same information in a different format

**Who.** Quality manager. **When.** Every FAIR and every inspection report. **Frequency.** Constant.

**Evidence.** On the FAI form itself: a shop had a FAIR **rejected** over Form 2 Field 8 (Special Process Supplier Code) — a code the *customer* assigns and had never provided — requiring *"much deliberation"* before acceptance. Another practitioner in the same thread: *"**Many of my customers have unique requirements when it comes to how they want these things filled out, which is a bit frustrating as it seems to go against the whole idea.**"* ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/as9102-rev-c-form-2-supplier-code.89114/)) And: *"Although Boeing and most subs I deal with insist this is a uniform process, **I have not found that to be true. Each company has their own requirements.**"*

On inspection reports, the transcription tax is described exactly:

> *"Several of our clients have different formats, and each one passes through the shop and/or Inspection Room in **hard-copy filled out in pen and ink, then someone transcribes the pen and ink to the electronic version** that was originally e-mailed to us, then that file is sent back to the client. This means **we have no real managed method of producing Inspection Reports other than grinding pen and ink**."* — ttrager, [Practical Machinist](https://practicalmachinist.com/forum/threads/how-do-you-handle-inspection-reporting-with-your-clients.369863/)

His own fix, built himself: a **VBA-coded Excel workbook with wireless caliper capture** that *"auto-shades measurements that are out of spec"* and has *"auto-reporting to match customer formats where that can happen"* — but for revision-controlled customer spreadsheets he still *"collect[s] the data in the tool I'm prototyping, then **copy those cells out to the Customer report**."* ([page 2](https://www.practicalmachinist.com/forum/threads/how-do-you-handle-inspection-reporting-with-your-clients.369863/page-2))

There is also a structural aggravator: **AS9102 mandates no digital data-interchange format.** ([DISCUS](https://www.discussoftware.com/news/as9102-rev-c-what-you-need-to-know/)) The standard specifies forms, not a schema. Everything is PDF and Excel by default.

**Evidence strength: high.**

---

### Problem 8 — Corrective-action responses are burdensome, often misdirected, and usually badly written

**Who.** Quality manager. **When.** On customer complaint. **Frequency.** Episodic but clock-driven.

**Evidence.** Turnaround pressure: *"triplex 8D required within two weeks for individual isolated defects."* Misdirection: *"at least half of our top customer's RCCA requests turn out to be not our fault."* Quality: a receiving-side quality lead reports *"**rejecting most of the CA responses. All are poorly written with insufficient data**"* and is explicitly looking for training in *how to write* one, not for software ([Elsmar](https://elsmar.com/elsmarqualityforum/threads/formal-written-response-to-a-corrective-action.72834/)).

The customer's view is worth recording because it defines the target: *"the information that goes into the 8D is **all in this pile of emails you sent me** (making more work for me). Why didn't you just consolidate this all together and fill out the 8D?… And it is ALWAYS true."*

**Evidence strength: high, but note the caution it implies** — the receiving-side practitioner wanted *training*, not a tool. A template generator that does not improve reasoning quality will produce faster bad responses.

---

### Problem 9 — Compliance overlay constrains what software is even permissible

Not a pain point to solve, but the architectural constraint every opportunity below must respect.

**ITAR.** 22 CFR **120.54** (effective 25 March 2020) is the operative carve-out: unclassified technical data is not an export if end-to-end encrypted at FIPS 140-2 or comparable ≥128-bit strength, kept encrypted until decrypted by the authorized recipient with **no means of decryption provided to any third party including the cloud provider**, and not stored in a §126.1 proscribed country or Russia ([Dinsmore analysis](https://www.dinsmore.com/publications/new-itar-end-to-end-encryption-rule-will-promote-efficient-defense-technical-data-storage-and-transmission-but-some-risks-remain/)).

**CMMC.** The 48 CFR acquisition rule became effective **10 November 2025**, putting CMMC clauses into DoD contracts. Phase 1 (to 31 Oct 2026) allows Level 1/Level 2 **self-assessment**; Phase 2 was scheduled to make Level 2 C3PAO certification the default for CUI contracts. As of early 2026 the reported state was **98 authorized C3PAOs and ~1,042 certified organizations against an estimated ~76,598 needing certification**, with assessments at **$35,000–$75,000** and waits reported *"eight months out."* **One source carries an editor's note that the Phase 2 transition is "currently on hold," which could not be independently confirmed from a primary DoD source — treat the Phase 2 date as uncertain.** ([PreVeil](https://www.preveil.com/blog/cmmc-final-rule-published/), [Secureframe](https://secureframe.com/blog/cmmc-phase-2-preparation), [PKF O'Connor Davies](https://www.pkfod.com/insights/no-certification-no-contract-cmmc-rule-48-cfr-7021-takes-effect-november-10-2025/))

**The consequence for this catalog is favorable and specific.** A DoD print is simultaneously ITAR technical data and CUI, and the obligations are cumulative. Small shops respond by keeping prints on paper travelers and local shared folders — *"printed travelers/drawings with CUI migrate across work centers, get annotated, and are hard to track/recall"* ([Allen CIO](https://www.allencio.com/the-challenges-faced-by-machine-shops-with-cmmc/)) — which is exactly the practice that breaks traceability. **A local-first, offline, no-telemetry open-source tool is not a compromise in this market. It is the compliant architecture, and it is a selling point.** One commercial entrant already markets on precisely this, claiming *"Drawings are processed entirely in your browser and are never uploaded"* ([Balloonist](https://balloonist.io/)).

---

### Problem 10 — There is no open-source foundation to build on

Worth recording because it shapes build estimates. The search for open-source tooling in this space came back essentially empty:

- **engineering-drawing-extractor** — OpenCV + Tesseract, extracts *title block fields only*. **85 stars, 4 commits, no releases.** ([GitHub](https://github.com/Bakkopi/engineering-drawing-extractor))
- **FreeCAD STEP AP242 PMI export** — an **open issue, not implemented**, blocked because *"the OCCT commercial PMI Visualization Component"* is required for graphical PMI while the open-source path needs manual tessellated polyline generation ([FreeCAD #29797](https://github.com/freecad/freecad/issues/29797))
- **STEPcode** provides AP242 schema tooling but **no PMI semantics layer** ([STEPcode](https://stepcode.github.io/docs/home/))
- **werk24-python** is a thin client to a paid SaaS backend

**No open-source AS9102 form generator, PDF balloon-placement engine, or GD&T feature-control-frame parser surfaced in any search.** The only free artifacts are vendor lead-magnet Excel templates. *(Caveat: GitHub's search API was blocked in this environment, so coverage relied on web search plus direct repo fetches. Absence of evidence is weaker here than elsewhere in this report.)*

**Implication:** concepts that require reading geometry or GD&T from a drawing are materially more expensive than concepts that read *forms, tables and text*. The ranking in Section 5 reflects this.

---

## 4. Application opportunities

### Opportunity A — Cert Package Assembler and Completeness Gate

**Working title:** `PackShip`
**Intended user:** Quality manager and shipping clerk.
**Problem solved:** Problem 1, with a direct assist to Problems 5 and 6.

**Current workflow:** Collect documents by memory, staple, walk down the hall for a blind signature, ship.

**Proposed workflow:** Each customer has a **requirements profile** — a plain-text file listing what their packages must contain and what each document must show. At shipment, the tool takes the job's documents (material certs, outside-process certs, FAIR, inspection report) and runs a **completeness and consistency gate**: is every required document present; does the part number, revision, PO number and quantity agree across all of them; is the material cert traceable to the heat lot on the job; do any certificate dates fall **after** the FAI signature date; are all outside processes on Form 2 backed by a returned cert. It then produces a single paginated PDF with a generated cover CofC carrying the customer's required fields, and a signature page that states **what was actually checked**.

**Inputs:** Job record (part, rev, PO, qty, heat lot); the document set; the customer profile.
**Outputs:** Assembled package PDF; a pass/fail gate report; a CofC populated to the customer's required content; an archive manifest.

**Essential features:** customer profiles as human-readable, diffable text; cross-document field matching; **date-logic checking** (certificates dated after the FAI signature is a documented FAIR rejection cause); explicit listing of unverifiable items; never modifies source documents.
**Excluded from v1:** Document storage/DMS, ERP integration, e-signature, generating any certificate the shop does not already have.

**AI:** **Optional and confined to field extraction** from heterogeneous supplier certificates — mill certs and plating certs have no common layout, and regex alone will not generalize. The *gate logic itself must be deterministic*; an LLM deciding a package is complete is worthless as a control. Extraction results must be shown for confirmation before the gate runs.

**Would a spreadsheet suffice?** No. The value is reading and cross-checking the PDFs themselves and refusing to release when they disagree. A spreadsheet checklist is what shops have; it is why the signature is blind.

**Complexity:** Medium. **Learning difficulty:** ~1 hour, mostly writing the first customer profile.
**Value:** Turns a theatrical control into a real one, unblocks shipping, and attacks the **most frequently cited FAIR rejection cause** before the package leaves the building.
**Risks:** A false "pass" is worse than no tool — hence the requirement that the signature page enumerate what was and was not verified. Data sensitivity is high (ITAR/CUI), so it must run entirely locally.
**Existing products:** **None.** ERP quality modules store documents; ballooning tools build FAIRs; nothing assembles and gates the shipped package. The search for "certificate of conformance software" returns templates, not products.
**Why attractive:** Highest-frequency handoff in the market, zero incumbents, a documented and quotable admission that the current control does not work, and a failure mode that costs money directly.
**Paid customization:** Per-customer profiles (an obvious, repeatable engagement — LM Aero, Boeing, GD each have published requirements), ERP export hooks, firm CofC templates.

---

### Opportunity B — FAIR Pre-Submission Validator

**Working title:** `FAIRCheck`
**Intended user:** Quality manager, before submitting a FAIR.
**Problem solved:** Problem 3's rejection tail and Problem 7's per-customer variance — **without competing in the crowded ballooning market**.

**Current workflow:** Fill out the forms, send, and find out three to four months later that a typo needs fixing.

**Proposed workflow:** Load a completed AS9102 form set (Excel or fillable PDF, Rev B or Rev C). The tool runs the documented rejection causes as deterministic checks: every balloon number on the print appears exactly once in Form 3 and vice versa; every special process and material on Form 2 references a specific certificate rather than a procedure number; **no certificate is dated after the Form 1 signature**; Form 1 field 14 (reason for full/partial) is populated — **mandatory for all FAIs under Rev C**, not just partials; field 17 Part Type is populated; all COTS and standard catalog items appear on Form 1; measurement methods are specific ("CMM program FAI-12345 rev 2") rather than generic ("CMM"); the documented-nonconformance flag is consistent with the results; surface-finish and note-derived characteristics are accounted for rather than left narrative. Plus a **customer overlay**: this customer requires a ballooned print attached; this customer requires Rev B forms; this customer assigns Special Process Supplier Codes you must request.

**Inputs:** Completed form set; optionally the ballooned print; customer profile.
**Outputs:** A findings list with severity and the specific rule; a clean/blocked verdict; a submission checklist.

**Essential features:** Rev B **and** Rev C rule sets, selectable — there is no mandated transition date, so both are live indefinitely; rules cite their source; balloon-to-row reconciliation; date-logic checking; customer overlays as text files.
**Excluded from v1:** Ballooning, OCR of prints, generating forms, submitting to customer portals.

**AI:** **Inappropriate for the checking** — every rule above is a field, set-membership or date comparison. AI is **optional** as an authoring aid to convert a customer's written FAI requirements into a draft overlay for human review.

**Would a spreadsheet suffice?** Partly — practitioners have already built exactly this halfway, including a workbook that red-highlights out-of-tolerance values across 200–300 measurements. What a spreadsheet cannot do is reconcile balloons against a print, check dates across attached certificates, or carry per-customer overlays.

**Complexity:** Small-to-medium — it reads structured forms, not geometry, which per Problem 10 is the cheap side of this market. **Learning difficulty:** ~30 minutes.
**Value:** Converts a months-long rejection loop into a pre-send check. Given that a large majority of FAIRs are never reviewed but the ones that are come back over typos, the expected value is concentrated exactly where this tool operates.
**Risks:** Rule sets must be versioned against the form revision. Must never claim a FAIR is "approved" — only that listed checks passed.
**Existing products:** The ballooning vendors generate FAIRs; **none validate a finished one against rejection causes**, and Net-Inspect users complain the portal creates *"double work"* rather than checking their existing Excel FAIR.
**Why attractive:** Sharply scoped, deterministic, complements rather than competes with the 10+ ballooning entrants, and slots into whatever the shop already uses.
**Paid customization:** Customer overlays; shop-specific rules; batch validation for high-FAIR-volume shops (one practitioner holds *"well over 2000"*).

---

### Opportunity C — Purchase-Order Quality Clause Extractor

**Working title:** `ClauseSheet`
**Intended user:** Estimator at quote; quality manager at job release.
**Problem solved:** Problem 2.

**Current workflow:** Nobody reads the clauses. Surprises surface during execution.

**Proposed workflow:** Drop in the PO and any referenced quality-clause documents. The tool extracts and classifies the obligations that change what the shop must *do*, and emits a one-page **job requirements sheet** for the traveler: FAI required (full or partial, which form revision, ballooned print required)? PPAP level? Source inspection or customer witness? Which certifications must ship? DFARS specialty-metal melt-source restriction? Counterfeit-materiel flow-down? Approved-processor constraint on special processes? Retention period? Escape-notification clock? Packaging and labeling? Anything it cannot classify goes in an explicit **"unclassified — human review"** section rather than being dropped.

**Inputs:** PO PDF, clause documents, optionally a customer profile from prior jobs.
**Outputs:** One-page requirements sheet; a structured record feeding Opportunities A, B and D; a diff against this customer's last PO, flagging new or changed clauses.

**Essential features:** the diff-against-last-PO (cheap and high value — it turns a 50-page document into "three things changed"); explicit unclassified bucket; every extracted item linked back to its source page and clause number; local operation.
**Excluded from v1:** Legal interpretation, contract negotiation, pricing.

**AI:** **Necessary, and this is the strongest legitimate AI case in the report.** Clause documents are unstructured prose in hundreds of house styles, referencing thousands of specs. Rules and regex will not generalize. But AI's role is *retrieval and classification with citation* — surfacing the clause and where it came from — never deciding whether the shop complies. The "unclassified" bucket is the safety mechanism that keeps hallucination from becoming silent omission.

**Would a spreadsheet suffice?** No.

**Complexity:** Medium. **Learning difficulty:** ~30 minutes.
**Value:** The documented worst case is 5,000 unpriced measurements on a single job. Even catching that class of surprise once justifies the tool.
**Risks:** **A missed clause is the exact failure the tool claims to prevent**, so it must be positioned as "read this in five minutes instead of not at all," never as assurance of completeness. ITAR/CUI content means it must run locally or on shop-controlled infrastructure — which rules out most commodity LLM APIs and pushes toward local models. That is a genuine engineering constraint, not a footnote.
**Existing products:** Paperless Parts' "Wingman" extracts specs, threads and materials at quote time and detects CUI/ITAR markings ([announcement](https://www.paperlessparts.com/press/paperless-parts-launches-wingman-the-companys-new-ai-powered-automation-tool-to-make-quoting-from-prints-faster-and-less-error-prone/)) — but it reads **prints**, for **pricing**, inside a closed commercial quoting platform. Nothing reads the **PO and clause documents** to produce a shop-floor requirements sheet.
**Paid customization:** Customer clause libraries; local model deployment; integration with quoting or ERP.

---

### Opportunity D — CMM Output to Form 3 Mapper

**Working title:** `Form3Feed`
**Intended user:** Inspector and quality manager.
**Problem solved:** The retyping half of Problem 3 and the format half of Problem 7.

**Current workflow:** Read numbers off a CMM printout or screen, type them into Form 3 or a customer spreadsheet. Or pay for a tool tier that does it.

**Proposed workflow:** Map once, reuse forever. The user associates CMM output columns (PC-DMIS, Calypso, QC-CALC exports) with balloon numbers for a given part; thereafter, a new results file auto-populates Form 3 actuals, flags out-of-tolerance values, and exports to Form 3, a customer-specific spreadsheet layout, or CSV. Mappings are saved per part number and versioned with the drawing revision.

**Inputs:** CMM/gage output file; a balloon-to-characteristic mapping; target output template.
**Outputs:** Populated Form 3; populated customer template; out-of-tolerance exception list.

**Essential features:** read the common export formats; persistent per-part mappings tied to drawing revision; out-of-tolerance highlighting; multiple output templates; **no re-keying anywhere in the path**.
**Excluded from v1:** Measuring anything, CMM programming, SPC/capability analysis, ballooning.

**AI:** **Inappropriate.** This is column mapping and arithmetic.

**Would a spreadsheet suffice?** A practitioner has already built the VBA version of this, with wireless caliper capture and auto-shading of out-of-spec values — and still ends up copying cells into customer reports. That homemade tool is the proof of demand and the specification simultaneously.

**Complexity:** Small-to-medium; format coverage is the work. **Learning difficulty:** ~1 hour for the first mapping, minutes thereafter.
**Value:** Directly targets the step both Quality Magazine and Ideagen name as the error-prone bottleneck. **The commercial signal is unusually clean: CMM import is the exact capability both major vendors gate behind their upper tier** — Ideagen Standard→Advanced ($125→$235/mo) and SOLIDWORKS Inspection Standard→Professional. A free tool doing only that, and working alongside whatever else the shop owns, is well-targeted.
**Risks:** Silent mis-mapping produces a plausible, wrong report. Mitigation: show the mapping and the source value next to every populated field on first run, and re-verify when the drawing revision changes.
**Existing products:** Bundled inside the paid tiers above; QC-CALC does data collection and SPC but requires **one license per CMM** and draws complaints about incompatible data files after parameter changes ([Hexagon community](https://nexus.hexagon.com/community/public/pc-dmis/f/pc-dmis-for-cmms/105378/qc-calc)).
**Why attractive:** Narrowest scope in the report, clearest ROI, no geometry parsing required, and it strengthens rather than threatens the tools shops already bought.
**Paid customization:** Additional CMM/gage formats; customer report templates; per-shop mapping libraries.

---

### Opportunity E — Outside-Processing Packet Builder and Cert Chaser

**Working title:** `OutsideOps`
**Intended user:** Buyer and quality manager.
**Problem solved:** Problem 5.

**Current workflow:** An operation sheet, a PO with a hand-typed revision reference, and memory.

**Proposed workflow:** For a given special process and end customer, the tool builds the **outbound packet** — the specification with its applicable revision and departures, the required cert content list, the approved-processor check, and a PO reference block with an explicit revision stamp — then **tracks the parts out and back**: due date, quantity sent, quantity returned, and quantity damaged. On return it checks the processor's certificate against the required content list (processes performed, dates per operation, accept/reject per operation, coating thickness, lot/batch numbers, sub-tier certs) and flags what is missing before the parts move to shipping.

**Inputs:** Job, process, end customer, processor; the customer's approved-processor list; a required-cert-content profile.
**Outputs:** Outbound packet PDF; an open-at-vendor tracker; a returned-cert findings list; a cumulative vendor damage/loss record.

**Essential features:** specification-plus-departures as maintainable text; explicit revision stamping on every outbound reference; approved-processor gate with an expiry date on the approval record; cert content check; **vendor loss tracking** — the one thing nobody currently does, which converts "always make extras" from folklore into a number.
**Excluded from v1:** Being a purchasing system, EDI, or a supplier portal.

**AI:** **Optional**, for extracting fields from returned certificates (same rationale and same confirm-first constraint as Opportunity A). Inappropriate for the flow-down content, which must be exact.

**Would a spreadsheet suffice?** Partly for tracking; not for packet generation or cert checking. Shops already run the spreadsheet version and still produce escapes.

**Complexity:** Medium. **Learning difficulty:** ~1 hour.
**Value:** Attacks a failure class a practitioner states *"has resulted in escapes,"* and puts an expiry date on approved-vendor records that a new quality engineer found had rotted for years.
**Risks:** The specification/departure content is the shop's own responsibility and the tool must not appear to certify it. Keeping departure libraries current is a real maintenance burden — likely the leading paid-customization line.
**Existing products:** None found. ERPs issue POs; none carry process specifications with departures or check returned certificates.
**Paid customization:** Customer-specific spec and departure libraries (Boeing D1-4426 alone is a substantial engagement); processor onboarding profiles.

---

### Opportunity F — Drawing Revision Diff and FAI Re-Accomplishment Advisor

**Working title:** `RevGate`
**Intended user:** Programmer, quality manager, production manager.
**Problem solved:** Problem 4.

**Current workflow:** Stamp the old print "Void," shred it, and hope nothing was in process.

**Proposed workflow:** Register every print in work with its revision. When a new revision arrives, the tool produces a **visual overlay diff** of the two PDFs plus a **text/title-block diff**, and classifies the change: title-block or ownership only; note or specification change; dimensional or tolerance change; added or removed feature. It then answers the two operative questions: **which ballooned characteristics changed** (so the FAIR can be a *partial* rather than a full re-accomplishment), and **is anything currently in WIP against the superseded revision**.

**Inputs:** Old and new PDF; optionally the balloon-to-characteristic map from Opportunity D; open job list.
**Outputs:** Overlay diff PDF; a changed-characteristics list; a WIP exposure alert; a suggested full/partial FAI determination **with the AS9102 trigger cited** and a required human confirmation.

**Essential features:** raster and vector overlay diff robust to rescaling and re-plotting; title-block field extraction; changed-characteristic mapping; explicit "cosmetic change — no technical content detected" classification; never auto-decides the FAI scope.
**Excluded from v1:** CAD model comparison, 3D, automatic FAIR regeneration.

**AI:** **Optional and narrow** — classifying whether a note change is technical or editorial is a genuine judgment task where AI helps. The **diff itself must be deterministic image and text comparison**; an AI that "thinks" nothing changed is a liability.

**Would a spreadsheet suffice?** No.

**Complexity:** **Medium, and the hardest build in this report.** Real-world prints are scanned, rotated, rescaled and re-plotted between revisions; naive pixel diffs produce noise. This is the concept most likely to be under-estimated.
**Learning difficulty:** ~30 minutes.
**Value:** One documented instance cost material plus roughly eight machine-days. Separately, it addresses the *"absolutely no technical changes"* complaint from a shop holding 2,000+ first articles — the cosmetic-change classification alone could eliminate a recurring paperwork cycle.
**Risks:** A missed change is catastrophic and the tool would carry the blame. It must present the diff for human review rather than issuing a verdict. Scanned-print alignment may prove harder than the value justifies — **validate on real revision pairs before committing.**
**Existing products:** Bluebeam Revu does document comparison well ($260–$590/user/yr) but knows nothing about balloons, characteristics, or AS9102 triggers. That gap — general diff vs. FAI-aware diff — is the whole opportunity, and also the reason a shop already owning Bluebeam may see this as marginal.
**Paid customization:** Title-block templates per customer; ERP WIP integration.

---

### Opportunity G — Heat-Lot Traceability Ledger

**Working title:** `LotLink`
**Intended user:** Receiving, production, shipping.
**Problem solved:** Problem 6.

**Current workflow:** Sellotape.

**Proposed workflow:** At receiving, register the material: supplier, PO, mill cert file, heat/melt lot, form and size, DFARS melt-source status, quantity. The tool prints a durable **lot tag with a barcode or QR code**. At job issue, scan the tag against the work order — the link is now recorded rather than remembered. At shipment, the tool answers both directions: *which heat lots are in this shipment* (for the CofC and Form 2) and *which shipments contain heat lot X* (for a recall or an audit).

**Inputs:** Receiving data and mill cert PDFs; scans at issue and shipment.
**Outputs:** Lot tags; a per-shipment lot statement for the CofC; a reverse recall query; a retention-compliant archive.

**Essential features:** the two-way query — this is the entire product; barcode/QR generation printable on ordinary label stock; DFARS melt-source flagging; partial-lot and multi-lot job handling (the documented third breakpoint); export of the lot statement into Opportunity A's package.
**Excluded from v1:** Inventory management, purchasing, MRP, bin locations. **The moment this becomes inventory software it has lost.**

**AI:** **Optional** for reading heat numbers and chemistry off mill certs at receiving (varied layouts). Inappropriate anywhere else.

**Would a spreadsheet suffice?** A spreadsheet can hold the data. It cannot print tags, cannot be scanned at the saw, and — critically — is not maintained, which is why certs end up zip-tied to bar stock.

**Complexity:** Small-to-medium. **Learning difficulty:** ~30 minutes.
**Value:** Closes the gap a consultant identified as *"the link between each certificate and the specific finished part it became."* Satisfies DFARS melt-source documentation and AS6174 counterfeit-materiel flow-down. Turns a recall from a filing-cabinet archaeology project into a query.
**Risks:** Adoption depends entirely on the scan taking under five seconds at the saw. If it is slower than sellotape it will not be used — this is a shop-floor ergonomics problem more than a software problem, and it should be prototyped with a real barcode scanner before any code is polished.
**Existing products:** ERPs track material lots but reviewers report weak serialization; the practitioner accounts show shops not using those modules. Steelhead's "Spec Management" add-on is the only product found that even names certification digitization.
**Paid customization:** Label formats and printer support; ERP receiving integration; customer-specific lot statement wording.

---

### Opportunity H — Escape and Corrective-Action Clock Tracker

**Working title:** `EscapeClock`
**Intended user:** Quality manager.
**Problem solved:** The deadline half of Problem 8.

**Current workflow:** Email, memory, and hoping the 24-hour one was not a flight-safety item.

**Proposed workflow:** On discovering a nonconformance or suspected escape, select the affected customer and the category. The tool computes every applicable contractual deadline from a per-customer profile — Lockheed Martin Aero: 24 hours for flight-safety or counterfeit concerns, 3 business days for potential escape notification, 5 business days for supplementary information, 30 calendar days for SCAR corrective action; Global Machine Works: 1 business day for escape notice on delivered product — and generates the initial notification with the required content fields populated. It then tracks open items against their clocks.

**Inputs:** Event date/time, customer, category, affected parts and shipments (from Opportunity G).
**Outputs:** A deadline sheet; a drafted notification; an open-items dashboard; a closure record.

**Essential features:** per-customer profiles with the clause cited; **business-day versus calendar-day arithmetic done correctly** (LM Aero mixes both); affected-shipment lookup; nothing requiring a server.
**Excluded from v1:** Root cause analysis, 8D authoring, CAPA management. This tool answers *who must be told, by when, and what must the notice contain.*

**AI:** **Inappropriate.** Date arithmetic against cited contract clauses.

**Would a spreadsheet suffice?** For the arithmetic, arguably. Not for the per-customer clause library or the affected-shipment lookup.

**Complexity:** Small. **Learning difficulty:** Minutes.
**Value:** Risk elimination on obligations with 24-hour clocks and contractual force.
**Risks:** Must never be presented as legal advice; every computed date cites its clause.
**Existing products:** None found; generic task managers do not know the clauses.

**A deliberate exclusion worth stating.** I considered an **8D/corrective-action response generator** and rejected it. The evidence points the wrong way: the receiving-side quality lead rejecting most responses said they were *"poorly written with insufficient data"* and went looking for **training**, not a tool. A generator that does not improve reasoning quality produces faster bad responses and would make the reviewer's problem worse. This is a case where the pain is real and the obvious software answer is wrong.

---

### Opportunity I — Quote-Time Quality Cost Estimator

**Working title:** `QualityLine`
**Intended user:** Estimator and owner.
**Problem solved:** The pricing half of Problem 2 — and the bridge between this market's name (quoting) and this report's angle (QA).

**Current workflow:** Quote the machining. Discover the quality burden later. Absorb it.

**Proposed workflow:** Consuming the requirements sheet from Opportunity C (or manual entry), the tool estimates the quality cost of the job as a line item: characteristic count × minutes per characteristic (the practitioner rule of thumb is ~2 min/feature, calibrated over time against the shop's own actuals), plus FAI preparation, plus gages or fixtures that must be bought or made, plus source-inspection wait time, plus PPAP elements if automotive, plus cert-package assembly. Output is a defensible quality cost line for the quote and an internal note of what drives it.

**Inputs:** Characteristic count (from a balloon map if available, else estimated); requirements sheet; shop rate and historical actuals.
**Outputs:** A quality cost line with its assumptions itemized; a quote note; a variance report comparing estimate to actual once the job closes.

**Essential features:** the **variance loop** — this is what makes it more than a calculator, because it calibrates the shop's own minutes-per-characteristic instead of inheriting a forum rule of thumb; assumptions visible on the output so the number can be defended to a customer.
**Excluded from v1:** Machining time estimation, material cost, full quoting. It produces one line.

**AI:** **Inappropriate.** Arithmetic over a requirements list.

**Would a spreadsheet suffice?** This is the concept where a spreadsheet comes closest to sufficing, and the honest answer is that a good one nearly does. The differentiators are the variance loop and consuming the requirements sheet automatically.

**Complexity:** Small. **Learning difficulty:** Minutes.
**Value:** Directly addresses *"you get into a corner because you need a gage or an exceptional layout… in order to ship parts and get paid."*
**Risks:** Garbage in — if the characteristic count is guessed, the estimate is guessed. Most valuable when paired with Opportunity C or an existing balloon map.
**Existing products:** Quoting platforms price machining; Paperless Parts can *"add an inspection step to all relevant parts"* as a cost rule, but that is a flag, not an estimate.
**Paid customization:** Shop rate structures; integration with existing quoting software.

---

## 5. Opportunity ranking

Scored 1–5 on ten criteria. Maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of implementation | Stays narrow | Differentiation | Customization potential | Test data available | Evidence confidence | **Total** |
|---|---|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| **A** | Cert Package Assembler and Completeness Gate | 5 | 5 | 5 | 4 | 3 | 4 | 5 | 5 | 4 | 5 | **45** |
| **B** | FAIR Pre-Submission Validator | 4 | 4 | 4 | 5 | 4 | 5 | 5 | 4 | 4 | 5 | **44** |
| **D** | CMM Output to Form 3 Mapper | 4 | 5 | 5 | 4 | 4 | 5 | 4 | 4 | 3 | 5 | **43** |
| **C** | Purchase-Order Quality Clause Extractor | 5 | 5 | 4 | 4 | 3 | 3 | 5 | 5 | 4 | 5 | **43** |
| **E** | Outside-Processing Packet Builder & Cert Chaser | 5 | 4 | 4 | 4 | 3 | 4 | 5 | 5 | 3 | 4 | **41** |
| **H** | Escape and Corrective-Action Clock Tracker | 4 | 2 | 3 | 5 | 5 | 5 | 4 | 4 | 4 | 5 | **41** |
| **I** | Quote-Time Quality Cost Estimator | 4 | 4 | 4 | 5 | 4 | 4 | 4 | 4 | 3 | 4 | **40** |
| **G** | Heat-Lot Traceability Ledger | 4 | 5 | 4 | 4 | 3 | 4 | 4 | 4 | 3 | 4 | **39** |
| **F** | Drawing Revision Diff & FAI Advisor | 5 | 4 | 4 | 4 | 2 | 4 | 5 | 4 | 3 | 4 | **39** |

### The top three explained

**1. A — Cert Package Assembler and Completeness Gate (45).** It wins on the rarest combination in this report: the highest-frequency handoff in the market, a total absence of incumbents, and a practitioner admission that the existing control is fake. Every shipment carries this package. The quality manager who signs the certificate of conformance says he *"doesn't actually confirm anything"* and signs *"blindly"* — and a veteran aerospace auditor confirms *"many people signing on a CoC have no idea of what they are signing for."* Meanwhile the shipping clerk is running down the hall to find him, holding the shipment. And the single most-cited cause of FAIR rejection is exactly what this tool checks: missing or incomplete material certificates.

The clinching evidence is negative: a search for "certificate of conformance software" returns free Word templates. For the most frequent outbound document in a 17,530-establishment industry, no product category exists. That is either an enormous oversight or a signal that shops will not pay for it — and the first validation question in Section 6 is designed to tell those apart.

Its weakness is honest: reading heterogeneous supplier certificates is genuinely hard, and if extraction is unreliable the gate is unreliable. Mitigation is confirm-before-gate and an explicit list of what could not be verified.

**2. B — FAIR Pre-Submission Validator (44).** The best-scoped concept in the report, and the one I would build first if the goal were a shipped artifact rather than a market beachhead. It reads structured forms rather than geometry — which per Problem 10 is the difference between a few weeks and a few months of work — and every one of its rules comes from a published rejection-cause list. It also sidesteps the report's most crowded market: there are ten-plus ballooning entrants and nothing that checks a finished FAIR before submission.

The evidence profile is unusual and favorable. Most FAIRs are never reviewed — one practitioner reports 95% no response across 1,000 submissions — but the ones that come back arrive three to four months later over a typo. A tool that costs nothing per use and eliminates the typo class is well-matched to that distribution.

It ranks second only because its per-use value is lower than A's. It prevents a delayed correction; A unblocks a held shipment.

**3. D — CMM Output to Form 3 Mapper (43).** The narrowest concept here and the one with the cleanest commercial signal. **CMM data import is precisely the capability that both major vendors gate behind their upper pricing tier** — Ideagen Standard→Advanced, SOLIDWORKS Inspection Standard→Professional. When two independent vendors independently choose the same feature as their upsell, they have told you what customers will pay for. A free tool doing only that, interoperating with whatever the shop already owns, is a strong opening move.

It also has a built-in specification: a practitioner has already constructed the VBA version, wireless calipers and all, and still ends up copying cells into customer report templates. That workaround is both the proof of demand and the requirements document.

**C (43) ties D on total but ranks below it** because its narrowness score is lower and its ITAR/CUI constraint forces local model deployment — a real engineering cost. It has the highest ceiling of anything in the report and the clearest customization revenue, and it is the one I would pursue immediately after a beachhead exists.

### What should be investigated next

**B first, then A.** B is the cheapest credible build, produces a shareable artifact, and is the natural pretext for practitioner conversations — which is exactly what A's validation needs, since A's central question ("would you pay for this, or is its absence telling us something?") cannot be answered from a desk. Use B to earn the conversations that de-risk A.

**F should be validated before it is built, not after.** It has the highest severity score in the report and the lowest implementation score. Scanned, rotated, re-plotted prints may defeat the diff entirely. Test the alignment problem on twenty real revision pairs first; if it works, F is a strong product, and if it does not, the effort belongs in E.

**Do not build a general ballooning tool.** Ten-plus entrants, an 85–90% accuracy ceiling that nobody has beaten, and the hardest technical problem in the market. Every opportunity above was chosen to sit adjacent to that fight rather than in it.

---

## 6. Validation plan

### Questions to ask practitioners

**On the cert package (A) — the decisive line of questioning:**
1. Walk me through the last shipment. What documents went with it, and who assembled them?
2. Who signs your certificates of conformance, and what do they actually check before signing?
3. Has a shipment ever been held waiting for a signature or a missing cert? How often?
4. Have you had a FAIR or a shipment rejected for a missing or wrong certificate? What happened?
5. **Is there a reason you have not bought software for this?** *(This is the single most important question in the plan. No product category exists for the most frequent document in the market. Either nobody built it, or shops will not buy it. Ask directly.)*

**On FAIRs (B):**
6. How many new part numbers a year, and how long does a FAIR take you?
7. When a FAIR comes back rejected, what is it usually for? How long after submission?
8. What fraction of your FAIRs get any response at all?
9. Do you keep both Rev B and Rev C form sets? Which customers want which?

**On CMM data (D):**
10. How do measured values get from the CMM into the customer's report? Show me.
11. Do you pay for the tier of your inspection software that imports CMM data? If not, why not?

**On clauses (C):**
12. Show me the last purchase order with quality clauses. Who read it, and when?
13. Has a quality requirement ever surfaced after you quoted? What did it cost?

**Cross-cutting:**
14. **What spreadsheet, macro, or database have you built yourself for any of this?** *(Highest-yield question in the plan — every homemade tool is a proven unmet need with demonstrated willingness to invest effort.)*
15. What would you never allow software to do in your quality system?
16. Are you subject to ITAR or CMMC? Would that stop you using a cloud tool?

### Who to interview

- **Quality managers at 10–50 person AS9100 shops** — the primary buyer for A, B, E and H. Recruit on Elsmar and Practical Machinist, where these people already post under professional identities.
- **A shop owner at 5–15 employees without a dedicated quality manager** — tests whether these tools are relief or overhead at the small end.
- **A supplier quality engineer at a prime or Tier 1** — the highest-leverage interview available. They author the flow-downs, reject the FAIRs, and can state the actual rejection reasons and rates, which no supplier-side source can. One is already on record describing what makes a response acceptable.
- **A Nadcap-accredited plating or heat treat shop** — the counterparty for E; they see the flow-down chaos from the receiving end.
- **An AS9100 registrar auditor or consultant** — can state what they find in audits, which is a proxy for what is actually broken.
- **A shop serving both aerospace and automotive** — tests the dual-dialect hypothesis behind C.

### Search terms for further research

`site:elsmar.com "cert package"` · `elsmar "certificate of conformance" software` · `practicalmachinist FAI software` · `"first article" rejected "material cert"` · `AS9102 rejection reasons customer` · `"quality clause" flowdown machine shop PO` · `heat lot traceability machine shop barcode` · `Nadcap processor purchase order departures` · `"supplier quality manual" filetype:pdf machining certificate of conformance` *(prime supplier manuals are the richest and most under-used source in this market — LM Aero, GDMS, Sensata and Global Machine Works all publish theirs)* · `AS9145 APQP PPAP aerospace` · `CMMC machine shop CUI traveler`

### Sample files and data needed

- **A real cert package** from a completed aerospace job, redacted — CofC, material cert, two outside-process certs, FAIR. This single artifact is the specification for Opportunity A.
- **Five to ten completed AS9102 form sets**, ideally including at least two that were rejected, with the rejection reason. Vendor-published free Rev C Excel templates make a usable starting corpus.
- **CMM output files** from PC-DMIS, Calypso and QC-CALC for the same part, to scope D's format coverage.
- **Three to five purchase orders with quality clause documents** from different primes.
- **Twenty real drawing revision pairs**, including at least five cosmetic-only changes — the make-or-break dataset for F.
- **A prime's supplier quality manual** — several are public and were used in this report.

### Prototypes that would validate

- **B:** A script that reads a completed AS9102 Excel form set and runs six checks — balloon/row reconciliation, cert-date-versus-signature, Form 1 field 14 populated, Part Type populated, generic measurement methods, unreferenced special processes. Run it against ten real FAIRs. **If it finds problems in half of them, the concept is confirmed.**
- **A:** A checker that takes four PDFs plus a job record and verifies part number, revision, PO and quantity agreement plus date logic. Two days. Show it to five quality managers and watch whether they ask for a copy.
- **D:** A single-format mapper — QC-CALC CSV to Form 3 — for one real part. If the mapping survives a revision change without silent breakage, the design is sound.
- **F:** No code. Take twenty revision pairs and test whether an off-the-shelf image-alignment library can register them reliably. **This is a two-hour feasibility test that decides whether F is a product or a trap.**

### Assumptions most likely to make these fail

1. **A: that the absence of a product category reflects an oversight rather than an unwillingness to pay.** The single biggest risk in the report, and question 5 is designed to settle it.
2. **A and E: that supplier certificate extraction is reliable enough** across mill certs, plating certs and heat treat certs to make a gate trustworthy.
3. **C: that a shop will run a local language model.** Cloud is likely off the table for ITAR/CUI content, and local inference is real infrastructure for a 20-person shop.
4. **F: that scanned, rescaled, re-plotted prints can be registered reliably.** Probably the single most likely technical failure.
5. **G: that a scan at the saw is faster than sellotape.** A shop-floor ergonomics question that no amount of good software design can answer from a desk.
6. **B and D: that shops will adopt a tool that does not replace what they own.** Complementary positioning is a strength commercially and a friction point operationally — it is one more thing to open.
7. **Across all: distribution.** These buyers find software through Practical Machinist, Elsmar, IMTS, and their ERP vendor — not GitHub. As in the prior land-surveying cycle, distribution may be a harder problem than engineering, and it recurs across markets often enough now to deserve treatment as a catalog-level question rather than a per-market footnote.

---

## 7. Cross-industry patterns

**Pattern 1 — Counterparty requirement extraction from unstructured contract documents.** Obligations that change what the work must produce are buried in prose nobody reads until breach; extract, classify, cite the source, and emit a one-page working sheet with an explicit "unclassified" bucket. Evidenced here by 20–50 page PO quality clause flow-downs. *Transfers to:* **General contractor preconstruction and estimating** (Division 01 and bid-document obligations), **Construction submittal, RFI, and closeout coordination**, **Fire protection / fire sprinkler design subcontractors** (specification sections and AHJ submittal requirements), **Nonprofit grant management and compliance** (grant conditions and allowable-cost rules), **Freight brokerage and dispatch operations** (carrier and shipper contract terms, accessorial schedules).

**Pattern 2 — Deliverable package assembly with a pre-release completeness and consistency gate.** A delivery must carry a document set whose composition varies by counterparty; verify presence, cross-field agreement and date logic before release rather than after rejection. Evidenced here by the cert package. *Transfers to:* **Construction submittal, RFI, and closeout coordination** (closeout packages — O&M manuals, warranties, as-builts), **Title, escrow, and real estate closing**, **Medical billing and revenue cycle for small practices** (claim plus attachments), **Immigration law practice** (petition packets), **Small CPA tax preparation practices** (return plus supporting schedules).

**Pattern 3 — Pre-submission validation against a published rejection-cause list.** A receiving authority rejects for a known, enumerable set of reasons; check before sending instead of learning months later. Evidenced here by AS9102 FAIR rejection causes. *Transfers to:* **Immigration law practice** (RFE triggers), **Medical billing and revenue cycle** (denial codes), **Civil / land development engineering and entitlement consulting** (plan-check comments), **Nonprofit grant management and compliance** (report rejection), **Structural engineering firms** (permit review comments). *Note: this pattern also appeared in the land surveying cycle as the recorded-map pre-submittal checker — its second independent appearance, which raises confidence that it is a genuine cross-market shape rather than a one-off.*

**Pattern 4 — Revision diff with downstream impact classification.** A controlled document is reissued; determine whether the change is substantive and which downstream artifacts must be redone. Evidenced here by drawing revisions triggering full versus partial FAI. *Transfers to:* **Small architectural studios** (drawing and specification revisions), **Mechanical (HVAC) design engineering at small MEP consulting firms**, **Structural engineering firms**, **Fire protection / fire sprinkler design subcontractors**, **Construction submittal, RFI, and closeout coordination**.

**Pattern 5 — Chain-of-custody ledger linking an input batch to a delivered unit, queryable in both directions.** Evidenced here by heat-lot traceability. *Transfers to:* **Geotechnical and environmental consulting / materials testing labs** (sample chain of custody — a near-exact analogue with its own regulatory teeth), **Dental and specialty clinic practice administration** (implant and device lot tracking), **Freight brokerage and dispatch operations** (shipment custody), **Medical billing** only weakly — noted and set aside.

**Pattern 6 — Counterparty-specific response clock calculator triggered by an event.** An incident starts multiple contractual clocks that differ per counterparty and mix business and calendar days. Evidenced here by escape and SCAR clocks. *Transfers to:* **Independent property and casualty claims adjusting**, **Independent insurance agencies - commercial lines**, **Immigration law practice**, **Estate planning and probate practice**, **Electrical or plumbing trade subcontractor field operations** (preliminary notice and lien deadlines). *Note: this is a close cousin of the statutory-deadline pattern recorded in the land surveying cycle; the distinction is that clocks here are contractual and per-customer rather than statutory and per-jurisdiction, which changes who maintains the rule library.*

**Pattern 7 — Instrument-output-to-counterparty-form mapper.** Measurement or system output arrives in the producing tool's native layout; the counterparty requires a specific form; the mapping is currently performed by retyping, and vendors gate the automation behind an upgrade tier. Evidenced here by CMM output to AS9102 Form 3. *Transfers to:* **Geotechnical and environmental consulting / materials testing labs** (lab instrument output to client report — the closest analogue found in this catalog), **Bookkeeping and outsourced accounting firms** (bank and POS exports to ledger format), **Medical billing and revenue cycle** (EHR output to claim format), **Land surveying firms** (already covered; the total-station-to-plat parallel is direct).

### New backlog markets discovered

| Market | Why it looks promising |
|---|---|
| Metal finishing, plating, heat treat and NDT job shops (special-process suppliers) | The counterparty in Pattern 1 and Opportunity E; Nadcap-accredited, cert-generating, and receiving flow-down chaos from non-expert customers. A market defined by producing documents. |
| Contract manufacturers serving FDA-regulated medical devices (ISO 13485 / QMSR) | FDA's QMSR incorporated ISO 13485:2016 into 21 CFR Part 820 effective 2 February 2026 — a fresh, dated regulatory transition affecting every device contract manufacturer. |
| Small defense suppliers navigating CMMC Level 2 | ~1,042 organizations certified against an estimated ~76,598 needing certification, assessments at $35k–$75k with eight-month waits. Enormous compliance gap at exactly this catalog's target size. |
| Calibration and metrology service providers / in-house gage management | Gage calibration recall, certificates, ISO 17025; named by a practitioner as part of the quality manager's bundle; document-driven and currently spreadsheet-run. |
| Supplier quality engineering at OEMs and primes (the receiving side) | They author the flow-downs and reject the deliverables. Building for the receiving side of any Pattern 2 or 3 tool doubles the addressable market and validates the supplier-side rules. |
| Industrial distributors and service centers issuing material test reports | Cert generation at the source of the traceability chain; the upstream half of Pattern 5. |

---

## 8. Sources and confidence

### Verified findings (primary sources or multiply corroborated)

**Standards and regulation:**
- AS9102 Rev C, published June 2023, no mandated transition date — [SAE](https://www.sae.org/standards/as9102c-aerospace-series-first-article-inspection-requirements/), [Accuris](https://store.accuristech.com/standards/sae-as9102c?product_id=2568218), [Net-Inspect Rev B vs C](https://www.net-inspect.com/blog/as9102-rev-b-vs-rev-c/), [AUVA](https://auva.com/2024/04/23/as9102-revision-c-noteworthy-changes-and-implications/), independently corroborated by [High QA](https://www.highqa.com/high-qa-blog-as9102-rev-c/) and [DISCUS](https://www.discussoftware.com/as9102-standard/)
- FAI re-accomplishment triggers — [IAQG AS9102 FAQ](https://endevco.com/contentstore/mktgcontent/endevco/uploads/2019/02/AS9102-frequently-asked-questions1.pdf)
- FAIR rejection causes — [Unitek Kiwa](https://www.unitek-kiwa.com/blog/as9102-first-article-inspection-guide/), [QualityEngineer.ai](https://app.qualityengineer.ai/blog/as9102-fai-form-1-2-3)
- AS9102 mandates no digital interchange format — [DISCUS](https://www.discussoftware.com/news/as9102-rev-c-what-you-need-to-know/)
- DFARS specialty metals — [252.225-7008](https://www.acquisition.gov/dfars/252.225-7008-restriction-acquisition-specialty-metals.), [252.225-7009 (Cornell LII)](https://www.law.cornell.edu/cfr/text/48/252.225-7009)
- Customer supplier-quality requirements (CofC content, retention, escape clocks, approved processors) — [Lockheed Martin Aero Appendix QX](https://www.lockheedmartin.com/content/dam/lockheed-martin/aero/documents/scm/Quality-Requirements/Quality-Appendices/AppQX_rev10.pdf), [General Dynamics Mission Systems](https://gdmissionsystems.com/-/media/general-dynamics/suppliers/terms-and-conditions/gdms-specialprocesses.ashx), [Sensata/Kavlico](https://www.sensata.com/sites/default/files/a/kavlico-supplier-quality-requirements-manual-ap0425.pdf), [Global Machine Works](https://globalmachineworks.com/wp-content/uploads/2025/09/Supplier-Quality-Requirements-Rev-9_17_2025.pdf)
- Nadcap scope — [PRI](https://www.p-r-i.org/nadcap)
- ITAR 22 CFR 120.54 encryption carve-out — [Dinsmore](https://www.dinsmore.com/publications/new-itar-end-to-end-encryption-rule-will-promote-efficient-defense-technical-data-storage-and-transmission-but-some-risks-remain/)
- CMMC 48 CFR rule effective 10 Nov 2025 and phase structure — [PreVeil](https://www.preveil.com/blog/cmmc-final-rule-published/), [PKF O'Connor Davies](https://www.pkfod.com/insights/no-certification-no-contract-cmmc-rule-48-cfr-7021-takes-effect-november-10-2025/)
- IATF 16949 Rules 6th Edition eligibility — [IATF Global Oversight](https://www.iatfglobaloversight.org/wp/wp-content/uploads/2024/12/Rules-6th-QA-Document_English-December-2024.pdf)
- FDA QMSR effective 2 February 2026 — [FDA](https://www.fda.gov/medical-devices/postmarket-requirements-devices/quality-management-system-regulation-qmsr)
- Market size — [NAICS 332710: 17,530 establishments, 209,280 employees](https://naicslist.com/naics/332710)

**Practitioner evidence (named posters, professional forums):**
- FAIR effort, characteristic counts, GM reaction — [Elsmar FAI costs](https://elsmar.com/elsmarqualityforum/threads/as9100-clause-8-5-1-3-first-article-inspection-costs.73620/), [Elsmar FAI form example](https://elsmar.com/elsmarqualityforum/threads/as9102-fai-first-article-inspection-form-example.20933/)
- FAIRs unread / unreturned — [Elsmar ship without FAI approval](https://elsmar.com/elsmarqualityforum/threads/am-i-allowed-to-ship-parts-without-fai-approval-from-the-customer.67821/)
- Cert package naming, contents, blind CofC signing — [Elsmar documentation accompanying an aerospace part](https://elsmar.com/elsmarqualityforum/threads/documentation-accompanying-an-aerospace-part.84250/), [Elsmar CofC best practices](https://elsmar.com/elsmarqualityforum/threads/certificate-of-conformance-compliance-cofc-share-your-best-business-practices.15686/)
- PO quality clause flow-down — [Elsmar PO quality clauses](https://elsmar.com/elsmarqualityforum/threads/purchase-order-quality-clauses.71375/)
- The 5,000-measurement PPAP and the contract-review gap — [Elsmar](https://elsmar.com/elsmarqualityforum/threads/ppap-including-fai-parts-customer-is-requiring-5000-measurements.45712/)
- Outside-processing flow-down and escapes — [Elsmar Nadcap processor PO requirements](https://elsmar.com/elsmarqualityforum/threads/nadcap-processor-po-purchase-order-requirements.60813/)
- Approved-vendor record decay — [Elsmar AVL non-responsive vendors](https://elsmar.com/elsmarqualityforum/threads/approved-vendor-list-non-responsive-vendors-requiring-approval.92003/)
- Per-customer FAI format variance and Form 2 field 8 rejection — [Elsmar AS9102 Rev C Form 2 supplier code](https://elsmar.com/elsmarqualityforum/threads/as9102-rev-c-form-2-supplier-code.89114/)
- Non-technical revision churn on 2,000+ FAIs — [Elsmar FAIR customer drawing revision change](https://elsmar.com/elsmarqualityforum/threads/as9102-fair-customer-drawing-revision-change.59211/)
- SCAR/8D burden and response quality — [Elsmar SCAR](https://elsmar.com/elsmarqualityforum/threads/suppliers-not-responding-to-supplier-corrective-action-requests-scar.69081/), [Elsmar formal written CA response](https://elsmar.com/elsmarqualityforum/threads/formal-written-response-to-a-corrective-action.72834/)
- Material traceability practice — [Elsmar raw material traceability](https://elsmar.com/elsmarqualityforum/threads/raw-material-traceability-in-a-machine-shop-aluminium-billets.91539/), [Elsmar single-person shop QMS](https://elsmar.com/elsmarqualityforum/threads/qms-and-iso-9001-for-a-single-person-machine-shop.68746/), [Kaizen ISO Consulting field observations](https://kaizenisoconsulting.com/articles/material-traceability-beyond-certification-shuffle)
- Ballooning tool substitutes and pricing complaint — [Elsmar ballooning software](https://elsmar.com/elsmarqualityforum/threads/software-suggestions-for-ballooning-drawings.52925/)
- Revision changes mid-job, wrong-rev cost, inspection report transcription, quality department scope, vendor-damaged parts, ERP fit — Practical Machinist threads [369452](https://www.practicalmachinist.com/forum/threads/custom-sent-wrong-drawing-who-should-pay.369452/), [395938](https://www.practicalmachinist.com/forum/threads/how-do-you-deal-with-revision-changes.395938/), [369863](https://practicalmachinist.com/forum/threads/how-do-you-handle-inspection-reporting-with-your-clients.369863/), [415601](https://www.practicalmachinist.com/forum/threads/hiring-someone-to-run-a-quality-department.415601/), [253525](https://www.practicalmachinist.com/forum/threads/what-should-happen-when-a-metal-finishing-shop-ruins-parts.253525/), [382354](https://www.practicalmachinist.com/forum/threads/first-article-inspection-software-or-documentation.382354/), [411796](https://www.practicalmachinist.com/forum/threads/erp-jobboss-2-vs-proshop-vs-something-actually-good.411796/)

**Software landscape and pricing:** [Ideagen/InspectionXpert](https://www.inspectionxpert.com/) and [Capterra reviews](https://www.capterra.com/p/210181/Ideagen-Quality-Control/) · [SoftwareSuggest pricing](https://www.softwaresuggest.com/inspectionxpert) · [High QA Capterra](https://www.capterra.com/p/248001/High-QA-Inspection-Manager/) · [DISCUS licensing](https://www.discussoftware.com/trybuy/licensing-options/) · [SOLIDWORKS Inspection](https://designandprocess.com/product/solidworks-inspection-standard/) · [1factory pricing](https://www.1factory.com/pricing.html) · [QA-CAD](https://www.guthcad.com/order_qacad.htm) · [Balloonist](https://balloonist.io/) · [Net-Inspect via Capterra](https://www.capterra.com/p/88288/Quality-Improvement-Software/) and [Northrop Grumman supplier notice](https://cdn.northropgrumman.com/-/media/Supplier-Documents/Announcements/2025_NetInspectRequiredFAIRSubmissionsApprovals.pdf) · [E2 Shop pricing](https://www.erpresearch.com/pricing/e2-shop-system) · [Global Shop pricing](https://www.erpresearch.com/pricing/global-shop-solutions) · [Fulcrum pricing](https://softwareconnect.com/reviews/fulcrum-pro/) · [MIE Trak Capterra](https://www.capterra.com/p/161558/MIE-Trak-Pro/) · [ProShop Capterra](https://www.capterra.com/p/155436/ProShop/reviews/) · [Paperless Parts G2](https://www.g2.com/products/paperless-parts/reviews) and [Wingman announcement](https://www.paperlessparts.com/press/paperless-parts-launches-wingman-the-companys-new-ai-powered-automation-tool-to-make-quoting-from-prints-faster-and-less-error-prone/) · [QC-CALC pricing](https://www.msi-viking.com/Prolink-QC-CALC-Real-Time-Data-Collection-Softw) and [Hexagon community thread](https://nexus.hexagon.com/community/public/pc-dmis/f/pc-dmis-for-cmms/105378/qc-calc) · [Werk24 pricing](https://werk24.io/pricing?lang=en) · [Retyping as the baseline — Quality Magazine](https://www.qualitymag.com/articles/95613-how-to-create-an-as9102-first-article-inspection-report) and [Ideagen](https://www.inspectionxpert.com/blog/how-to-fill-out-an-as9102-first-article-inspection-report-with-excel) · [Open-source gaps: FreeCAD #29797](https://github.com/freecad/freecad/issues/29797), [engineering-drawing-extractor](https://github.com/Bakkopi/engineering-drawing-extractor), [STEPcode](https://stepcode.github.io/docs/home/) · [CMMC constraint on shop practice](https://www.allencio.com/the-challenges-faced-by-machine-shops-with-cmmc/)

### Strong inferences (reasoned from verified evidence, not directly stated)

1. **The absence of a "cert package" product category is a genuine market gap rather than a search failure.** Supported by the naming-confusion thread, the template-only search results, and the absence of the capability from every ERP checked — but absence of evidence is weaker than evidence of absence, and validation question 5 exists to test it.
2. **Concepts that read forms and text are materially cheaper to build than concepts that read geometry.** Follows from the open-source survey: no GD&T parser, no balloon-placement engine, FreeCAD PMI export unimplemented and blocked on a commercial component. Caveat: GitHub's search API was blocked, so this survey is less complete than the rest of the report.
3. **A local-first, offline architecture is a selling point rather than a limitation in this market.** Follows from ITAR §120.54's no-third-party-decryption requirement plus CMMC's cost and queue, and is corroborated by a commercial entrant already marketing on browser-only processing.
4. **Shops absorb outside-processing losses as a scrap allowance rather than tracking them as vendor performance.** Inferred from "always make extras" and "happens all the time"; no practitioner stated the absence of tracking.
5. **The FAIR's low read-rate concentrates value in first-time correctness rather than in production speed.** Follows from the 95%-no-response estimate combined with three-to-four-month typo-driven rejections — but it rests on one practitioner's estimate.
6. **Distribution, not engineering, may be the binding constraint on this catalog.** This is the second consecutive cycle in which the target buyers were found to discover software through trade forums, conferences and dealers rather than through open-source channels. Two markets is a pattern worth naming; it is not yet proof.

### Tentative hypotheses requiring practitioner validation

1. **That shops will pay for cert package assembly.** The central unknown behind the top-ranked concept.
2. **That supplier certificate extraction can be made reliable enough to gate a shipment.** Untested; mill, plating and heat treat certs have no common layout.
3. **That the 4–5 hour FAIR and ~2 minutes per characteristic figures generalize.** Two practitioners, one shop each, no measured data — and no neutral benchmark exists publicly, which the standards research confirmed explicitly.
4. **That drawing revision pairs can be reliably registered and diffed.** The decisive technical unknown for Opportunity F.
5. **That a 20-person shop would run a local language model** for Opportunity C.
6. **That the reported CMMC Phase 2 "hold" is real.** One source carries an editor's note to that effect; it could not be confirmed from a primary DoD source. Any concept whose value depends on CMMC timing should verify this first.

### Known evidence gaps

- **reddit.com unreachable** (confirmed again this cycle). r/machinists and r/CNC were not mined. Given that Elsmar and Practical Machinist proved rich, the loss is smaller here than in the land-surveying cycle — but it is real.
- **practicalmachinist.com blocks automated fetching (HTTP 403).** All PM material came via a text proxy; transcription confidence is slightly lower than for Elsmar material.
- **GitHub search API blocked**, weakening the open-source survey in Section 3, Problem 10.
- **No neutral benchmark for FAIR effort or characteristic counts exists in public sources.** Confirmed explicitly by the standards research, not merely unfound.
- **No published FAIR rejection *rate*.** Rejection *causes* are documented; frequency is not. A supplier quality engineer at a prime could supply this in one conversation.
- **Job-posting evidence is thin** this cycle owing to tooling limits; the role definitions in Section 1 lean on forum accounts more than on postings.
- **Oxebridge**, expected to be a candid source on AS9100/AS9102, produced no FAI-specific material.

---

*Prepared by the market research cycle, claim `868d73ee`, 3 August 2026.*
