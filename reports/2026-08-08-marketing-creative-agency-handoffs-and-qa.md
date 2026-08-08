# Marketing and Creative Agency Account and Production Management — Handoffs and QA

**Market research cycle report — Borg LLC free/open-source business application catalog**

---

## 0. Cycle header

| Field | Value |
|---|---|
| **Market** | Marketing and creative agency account and production management |
| **Angle** | handoffs-and-qa (client-facing deliverable exchange, review and QA, coordination with outside organizations) |
| **Claim ID** | `31eace6d` |
| **Date** | 2026-08-08 |
| **Assignments remaining in backlog after this cycle** | 349 |

### Why this assignment was chosen

The ledger held 350 available assignments across roughly 200 markets with zero completed entries, so the "prefer untouched markets" rule did not discriminate on its own. Three tiebreakers decided it.

**Catalog breadth at the sector level.** Of the 28 completed reports, seven sit in architecture/engineering/construction (fire sprinkler design, MEP/HVAC, land surveying, geotechnical and materials testing, construction submittals, flood/FEMA consulting, fire ITM), three in legal, three in healthcare revenue cycle, two each in insurance, transportation, real estate, accounting and staffing/HR. **Marketing and creative services — one of the largest SMB professional-services sectors in the United States — had zero coverage.** Promethean Research's 2024 industry census counts roughly 46,000 digital agencies in the US and Canada, of which 64% have fewer than 10 employees and 27% have 10–49 — a population sitting almost entirely inside the catalog's target band and entirely absent from the catalog. The four seed angles for this market were all still unclaimed, meaning the whole market was unexamined.

**Angle diversity.** Completed angles run core-practitioner-workflow 9, back-office 7, narrow-subspecialty 6, handoffs-and-qa 6. `handoffs-and-qa` is tied for least-covered, and it is also the angle where this particular market is most interesting: an agency is, structurally, an organization whose entire product crosses an organizational boundary. Almost everything that goes wrong at an agency goes wrong at a handoff.

**Expected evidence quality.** I expected — correctly — that the review-and-approval half of this market would be documented mainly by vendor surveys of questionable independence, and that the regulatory half (pharma MLR, FINRA/SEC, FTC, SAG-AFTRA, stock licensing) would be documented by primary regulatory and case sources. That mix is workable: it lets the report anchor its strongest recommendations on primary law and case law rather than on marketing statistics.

**What I deliberately did not choose.** "General contractor preconstruction and estimating / handoffs-and-qa" was the strongest runner-up — sub-bid leveling and scope-gap analysis is a famously unsolved, spreadsheet-bound problem with clear dollar consequences. I passed on it because it would have been the eighth AEC report in a 29-report catalog. It should be claimed next cycle; it does not need to wait long.

### Evidence health warning, stated up front

Three structural problems with the published record in this market shape everything below.

1. **Reddit and Stack Exchange were unreachable from this environment (HTTP 403).** The richest practitioner-forum evidence base for agency operations could not be sampled. I substituted Creative COW forums, Adobe community threads, verified-reviewer complaints on G2/Capterra/TrustRadius (which turn out to be the single best practitioner-voice source available for tool gaps), named practitioner blogs, and professional-indemnity insurers' published claim files.
2. **Nearly all quantified creative-workflow data is vendor-sponsored, and much of it surveys *in-house* creative teams, not agencies.** The two longitudinal surveys with real sample sizes (InSource/inMotionNow, n=400–600; Filestage, n=263) are flagged individually below. I have not silently transferred in-house numbers onto agencies.
3. **The web is now heavily polluted with AI-generated SEO content in this vertical.** Roughly a dozen domains returning confident-sounding agency statistics had no methodology, no sample, and no source. They are excluded and named in section 8.

Where the evidence is thin I say so rather than filling the gap. Two of the ten opportunities below are recommended *because* their underlying facts come from statute, contract text and court records rather than from surveys.

---

## 1. Market examined

**Industry.** Marketing services: full-service and digital agencies, brand and design studios, video and content production shops, B2B demand-generation agencies, PR firms, and the specialist agencies serving regulated verticals (healthcare/pharma, financial services, legal, government).

**Professional roles this report is about.** The people who own the boundary between the agency and everyone outside it:

- **Account manager / account director** — the IPA's own definition describes the role as "the bridge between the client and the agency," responsible for presenting creative work, "handl[ing] approval processes," and ensuring materials comply with regulatory codes. Notably, neither the IPA description nor US recruiter job descriptions name *consolidating feedback* as a discrete task — at 5–75 people, it is unowned work that falls to whoever is on the account.
- **Project / traffic manager** — routes files, chases approvals, assembles delivery packages.
- **Producer / production manager** — owns vendor coordination, print and broadcast delivery, talent and music paperwork.
- **Creative director and designers/editors** — absorb the rework.
- **Agency principal** — in a shop under 25 people, this is frequently the same person as one or more of the above, and is the person who signs the contract that carries the liability.

**Organization size most likely to benefit.** 5–75 employees, with the sharpest fit at **8–40**. Below ~5 people the owner holds everything in their head and any tool is overhead; above ~75 the agency starts to be able to justify Workamajig ($45–49/user/month, 2–3 month implementation) or an enterprise DAM. The 5–75 band is large: Promethean's census puts 64% of ~46,000 US/CA digital agencies under 10 employees and 27% at 10–49; SparkToro's 2025 State of Digital Agencies survey (n=376) found 84% of respondents at 1–25 people and ~15% at 26–100.

**Type of user.** Non-technical to moderately technical. Comfortable with Adobe CC, Google Workspace, a project tool (Asana/ClickUp/Monday/Notion), a time tracker, and spreadsheets. Will not install a database, will not stand up a server, and — critically — **cannot compel their clients to log into anything.** Any tool whose value depends on client-side adoption is dead on arrival at this scale.

**Financial shape that determines what they will pay for.** Agency margin at this size is a function of hours: production staff utilization targets of 75–85% against realization of 75–95%, meaning an effective billing rate well below the nominal rate. Ignition's 2025 Agency Pricing & Cash Flow Report (n=273 agency managers and executives across branding, creative, digital, marketing, PR, social and web) found **57% of agencies lose $1,000–$5,000 per month on unbilled projects and tasks, 30% exceed $5,000/month, and 78% "rarely or only sometimes charge for out-of-scope work."** Australian coverage of the same dataset reports 52% of agency leaders over-servicing "all the time" and 14% putting the cost at $20,000–30,000/month. Drew McLellan of the Agency Management Institute uses ~20% of the monthly retainer as the benchmark over-service level.

That is the buying context: a business that already knows it is leaking money at the boundary, has no per-seat budget, and is chronically short of the one thing a new tool costs — attention.

---

## 2. How the work is performed

### 2.1 The shape of a job

A typical engagement at this size runs: brief → client materials collected → concepts → internal review → client review round 1 → revisions → round 2 → (rounds 3–5 in practice) → approval → production/adaptation → deliverable spec conformance → handoff to an outside organization (printer, publisher, broadcaster, platform, developer) → live → measurement and reporting → archive → eventual takedown or renewal.

The angle of this report covers everything after "client review round 1," plus the inbound collection step, plus the terminal archive/takedown step that almost nobody performs.

### 2.2 The review round, as actually practiced

**Who is involved.** On the agency side, the account manager presents and the project manager routes; the creative director gatekeeps. On the client side the picture is worse: InSource/inMotionNow found **85% of creatives serve 10 or more stakeholders**, and Ziflow/AMA's 2023 survey found 39% of creative team members work with 7+ clients or stakeholder groups simultaneously. Peter Kang, co-founder of the New York digital agency Barrel, names new stakeholders appearing mid-project as his third-ranked cause of delay — "especially those looking to make their mark," who "second-guess decisions" — and describes the standard failure: "What initially started as a promise to provide aggregated feedback… could be pushed out by a few days or even weeks."

**What moves, and how.** PDF is the default deliverable, because it "shows placement clearly in the layout." The channels that carry feedback back, documented by a 25-year practitioner (Colleen Gratzer, Design Domination), are: Acrobat "Send for Comments," Dropbox comments on the PDF, email, InDesign Share for Review — and, from clients, "a whole new Word document — and usually without tracked changes," photographs of pages marked up by hand, illegible handwriting, and overlapping comments that become indistinguishable. Round tracking is filename numbering, done by hand.

Filestage's 2021 survey of 263 advertising and marketing professionals found **53% had to consolidate feedback from multiple sources or channels**, and **71% of project managers had arranged a meeting purely to clarify feedback**. In enterprise pharma, where the discipline is highest, one study of digital-operations leads counted **twelve distinct feedback channels in simultaneous use**: Jira, email, spreadsheets, slide decks, Word docs, Veeva PromoMats, PDFs, meetings, Slack/Teams, SharePoint, screen recordings, and annotated screenshots. If that is the enterprise state, the 15-person shop is not doing better.

**How many rounds.** This is the report's central numerical tension and it is well-attested on both sides:

- **Contracts say two.** Creative COW practitioners, agency-published policies (Trillion Creative: "Most of our projects include two rounds of revisions. Beyond that, we invoice hourly"), and the Law Insider clause corpus ("The Company is entitled to two (2) design revisions during the development process at no additional cost") converge on two rounds as the contracted norm at small-shop scale.
- **Practice is three to five.** InSource/inMotionNow (n=566) found **61% experience 3–5 rounds, 19% require 5–10, 4% need 10+, and only 16% finish in 1–2**.

Every round past the second is, by the agency's own paperwork, unbilled. That is the mechanism that produces the over-servicing numbers in section 1.

**Approval turnaround.** 78% of projects receive final approval within a week; 15% take 6–7 days, 13% take 8–14 days, and **8% take more than two weeks**. 49% of Filestage respondents said delayed reviewer feedback slowed progress, 48% had to chase reviewers, 38% postponed deadlines, and 8% had projects cancelled because approvals never arrived.

### 2.3 The outbound handoff to outside organizations

This is where the report finds its hardest facts, because the receiving organizations publish their requirements.

**To a printer.** Print-ready PDF with bleed ≥0.125", safe area ≥0.25" inside trim, 300 DPI at final size, CMYK, embedded or outlined fonts, PDF/X-1a or PDF/X-4, and total ink coverage inside the limit for the press and stock (320–340% sheetfed coated, 300–320% heatset web, 240–260% non-heatset uncoated). The Ghent Workgroup — the industry's actual preflight standard — defines **14 variants** on top of ISO PDF/X-4, with a 260-file certification test suite. And the liability is contractual: trade printers explicitly transfer responsibility to the file supplier ("The reprint comes out of your budget").

**To a broadcaster.** The AICP file deliverable standard is ProRes 422 HQ in QuickTime, three permitted formats, PCM 48 kHz 24-bit audio, **−24 LKFS with true peak below −2 dBFS** per ATSC A/85, a 5-second slate then 2 seconds of black then content and *no extra frames*, and an Ad-ID with "H" appended for HD. CBS's own 2024–25 Commercial Integration Manual demands an 8-second slate (a conflict with AICP's 5), a filename of exactly 20 alphanumeric characters plus "H", and a deadline ladder: **files to Standards & Practices 5 business days before scheduling; traffic instructions in writing 3 working days before first airdate; billboards 7–14 days out; sectionals 10 business days out.** Its rejection language is unambiguous: "Commercials sent with missing or misspelled captioning cannot be corrected by CBS and will be returned for re-editing." Unaired commercials are **purged from inventory after 80 days** and must be resubmitted.

**To a platform or ad server.** IAB fixed-size units carry gzipped weight caps from 50 KB (mobile banner) to 250/500 KB (billboard), a maximum of 10 file requests on initial load, and a 30% CPU ceiling. Google Ads display: 150 KB static, HTML5 ZIP ≤600 KB and ≤40 files, animated GIF ≤30s and slower than 5 FPS. DV360 CTV: MP4 only, at least one asset at ≥15 Mbps, **duplicate frames not allowed** (which rejects many conformed exports), and separate asynchronous publisher approval — FreeWheel requires pre-approval before the creative can receive bid requests at all. Extreme Reach requires **filenames of 12 characters or fewer, letters and numbers only, "to avoid potential rejections."** DOOH runs at **25.00 fps progressive** — a frame rate used nowhere else in the same campaign — with 30-minute-to-overnight transcode latency during which the first plays are skipped.

**To a media vendor.** The IAB/4A's Standard Terms & Conditions v3.0 govern the insertion order: the media company must flag damaged or non-compliant materials within two business days, **late creative is billed pro-rata from the IO start date regardless**, and sequential liability protects the agency from the advertiser's non-payment *only if the IO says so*.

**To a client's regulated review system.** For a pharma client, the agency assembles the MLR package — annotated copy with every claim linked to a source, a reference pack, static PDFs, screenshots of every web state, video transcripts — and submits it into **the client's** Veeva vault, which the agency does not own, cannot export from, and cannot use for its own tracking. The only sanctioned agency entry point Veeva publishes is a **$500 per person per year certification** to work inside someone else's vault. An agency with three pharma clients is operating in three systems it does not control.

### 2.4 What software is actually in use

- **Project/PM:** Asana ($10.99–24.99/user/mo; proofing requires the Advanced tier), ClickUp ($7–12/user/mo; unlimited proofing on Business+), Monday ($9–19/seat, 3-seat minimum, proofing not a priced feature), Notion, Trello, Basecamp.
- **Proofing/review:** Ziflow (free tier of 2 billable users; $199–329/mo plans), Filestage (free tier capped at 1 active project and 5 files/month; $199–329/mo), Frame.io ($15–25/user/mo), Markup.io ($79/mo unlimited users), BugHerd ($50–150/mo by member pack), ReviewStudio ($15–25/user/mo, free tier capped at 3 active reviews *total*), Approval Studio ($60–300/mo), PageProof ($249–399/mo), GoVisually ($16–33/user/mo), Dropbox Replay ($10/user/mo add-on). Unlimited free external reviewers is now table stakes across essentially all of them.
- **Agency management:** Workamajig ($45–49/user/mo, 10-user minimum, 2–3 month implementation), Productive ($10–25/user/mo — with **no proofing or creative-review feature anywhere in its pricing matrix**), Scoro, Teamwork.
- **Onboarding/intake:** Content Snare ($35–215/mo), Leadsie ($59–299/mo priced *per new client onboarded*), AgencyAccess, Dubsado ($335–525/yr), HoneyBook ($29–129/mo), Ignition ($39–399/mo).
- **Reporting:** AgencyAnalytics ($20–25/client/mo → $500–625/mo at 25 clients), Swydo ($49/mo + per-source), DashThis ($44–429/mo by dashboard and source count), Whatagraph (**€699/mo annual minimum**), Looker Studio + Supermetrics ($44–222/mo, capped at 3–6 sources).
- **Preflight and QA:** Adobe Acrobat Pro ($287.88/yr per seat — which, per practitioners on PrintPlanet, *is* the callas pdfToolbox engine under the hood, licensed by Adobe), Enfocus PitStop Pro ($480/yr), Enfocus Connect YOU ($150 one-time), GTM Preview/Debug (free), the free axe browser extension.
- **Everything else:** Google Sheets, email, Slack, WeTransfer, Dropbox, and memory.

---

## 3. Most important problems, ranked

### P1 — Nobody can prove a comment was addressed, and no tool tries

**Who and when.** The designer or editor, on every version after the first; the account manager, immediately before sending version *n+1* back.

**Currently handled by:** eyeballing two panes. Filestage's own help documentation describes the process plainly — the comments sidebar "doubles as a to-do list for collaborators… for creatives (who use it as a to-do list while working on the next version) or managers (to verify that everyone's feedback has been met)." Gratzer's manual method is to use Acrobat's comment filters (read/unread, checked/unchecked, by commenter, by type) and tick items off one at a time "even in hundred-page documents." Her stated failure: "a few clients pointed out some edits I had missed that I really shouldn't have missed. I hadn't checked my work."

**Why inadequate.** Comments are bound to the version they were made on. Ziflow customers report "Comments stay on the old version, not updating to the new one, which can be confusing." Two customers of two *different* products independently request the identical missing feature — Filestage: "It would be nice if there were a way to transfer unresolved comments from one version over to the next version"; Ziflow: "I would love open items to migrate to the new version if they're not complete."

**Confirmation from the vendors themselves.** Ziflow's ReviewAI launch lists **"change verification," "automated revision comparisons," and "review summaries"** as future/in-development capabilities in Enterprise public preview — i.e. the category leader publicly concedes it does not ship this. What *does* ship is visual comparison only: Ziflow side-by-side, Frame.io's Comparison Viewer with pixel-difference mode, Filestage's automatic text diff. A pixel diff tells you pixels moved; it does not tell you that comment #7 was satisfied.

**Frequency and cost.** Every round of every job — call it 3–5 times per deliverable, at 60% of projects. The cost is a mix of unbillable re-review time and the specific, expensive failure of a missed comment surviving into production.

**Evidence grade: VERIFIED.** Vendor help docs, vendor roadmap, and two independent verified-reviewer feature requests.

---

### P2 — Usage rights expire on schedules nobody is tracking, and the downside is six figures

**Who and when.** The producer or account lead, 13 weeks and then 24 months after a shoot; the agency principal, when a letter arrives.

**The arithmetic that has to be right.** Under the SAG-AFTRA 2025 Commercials Contract (in force 1 April 2025 through 31 March 2028), a single spot generates at least two independent, non-aligned clocks:

- **Holding fees** run in fixed **13-week cycles**, the first beginning on the first day of production, and buy performer exclusivity.
- The **Maximum Period of Use is now 24 months**, computed as "10 business days from the first production day plus 2 years minus one day." SAG-AFTRA's own worked example: production starting 19 Aug 2025 → MPU ends **2 Sept 2027**. That is not a date any calendar tool will compute for you.
- Use must be paid through the MPU, and **commercials cannot remain accessible on social or streaming after use-cycle payments expire even if the MPU has not been reached.**
- Digital replicas require consent ≥48 hours in advance, a minimum of 1.5 session fees, and **24-month retention renewals**.
- Late payment penalties accrue at $3.85/business day to a $96.30 cap per performer — and under the 2025 contract, liquidated damages accrue without pause, "A Producer has to pay regardless of notice. **Notice is not the trigger**," and **if one performer sends notice, escalated damages apply to every performer on the spot.**
- Where the agency is the signatory, **the agency is the Producer** and carries the payment obligation.

**Then the other rights on the same asset run on different rules.** Music sync licenses are term × territory × media, and rights owners charge the full annual fee even for six non-consecutive four-week bursts because the track is "tied up with your brand" across the whole span; pre-negotiated renewal options cap at roughly +10%, and without one you renegotiate from zero leverage. Shutterstock's license (effective 19 Jan 2026) imposes **numeric** thresholds — ≤500,000 print reproductions, <500,000 OOH impressions, video production budgets ≤$10,000 for a Standard license — which are checked once at asset selection and then quietly invalidated by campaign success, with Shutterstock's indemnity capped at $10,000 against statutory copyright damages reaching $150,000 per work. Photography usage is licensed by term, territory and media, with agency-side pricing guidance of +50–75% over one-time use for unlimited use and +100–150% for a buyout.

**Currently handled by:** a "usage rights" tab in the campaign spreadsheet, PDF licenses in a Drive folder named after the shoot, calendar reminders set by whoever remembered, signed releases photographed on someone's phone, and a "kill list" email at campaign end.

**What it costs when it fails.** *Olive v. General Nutrition Centers* (Cal. Ct. App. 2d Dist., decided 27 Dec 2018, affirmed 31 Jan 2019): a one-year print license with a renewal option; GNC kept using the images after expiry and admitted the violation. Verdict **$213,000 license damages plus $910,000 emotional distress — $1,123,000 total.** The underlying failure was not a judgment call. It was a calendar entry nobody made, and the emotional-distress component was 4.3× the license damages. On the music side: *Beastie Boys v. Monster Energy* produced a **$1.7M jury verdict plus $667,849 in attorneys' fees** where a remix had been cleared only for free promotional use; the Chili's/"Sabotage" suit filed July 2024 settled 21 May 2025.

**Frequency.** Every produced asset with a person, a song, a stock image, or a location in it — which at a video- or campaign-producing agency is most of them.

**Evidence grade: VERIFIED** (union contract text, published court decisions, licensor terms of service). This is the single best-evidenced problem in the report, and the one where the evidence is least dependent on anyone's survey.

---

### P3 — The approval of record — the artifact that transfers liability — is priced for enterprises

**Who and when.** The agency principal, six weeks after a job shipped with an error.

**Why it matters, in the industry's own vocabulary.** Print has had a word for this for a century: **AA (author's alteration) versus PE (printer's error)**. The sign-off event is what reassigns cost. Peter Bowerman, a commercial copywriter writing about a typo that reached 5,000 brochures, states the mechanism exactly: "With a formal written sign-off, if an error is discovered after the fact, even if it's the writer's fault, he/she can't be held liable since the client approved it." (His actual response, worth noting as the representative small-shop outcome, was that he and the designer "decided on a vow of silence.")

**What it costs when it's missing.** Professional-indemnity insurers publish the claims:
- A marketing firm **omitted a digit from a client's phone number and left out the web address** in a printed advert; reprinted at its own cost; **£21,995** claim (PolicyBee).
- A design studio made late amendments to a client's annual report, the file corrupted and the changes did not save, and **5,000 copies printed with a duplicated name and a wrong index**; reprint quoted at **~£14,000**, settled at **just over £9,000** by the PI insurer. The broker's own lesson: get sign-off *on last-minute amendments specifically*, because that is where liability transfer breaks (PolicyBee).
- A flyer campaign printer error cost **£1,000 in reprint plus event cancellation fees**, and the insurer's position was that the client holds the designer responsible regardless of where the error originated, "because the freelancer is their point of contact" (With Jack).

**For regulated clients, the approval record is not optional, it is the rule.** FINRA Rule 2210(b)(4)(A), read with SEA Rule 17a-4(b), requires a firm to retain a copy of each retail communication, **"the dates of first and (if applicable) last use,"** the **name of the registered principal who approved it and the date**, and **"information concerning the source of any statistical table, chart, graph or other illustration."** The SEC Marketing Rule's recordkeeping provisions (Rule 204-2(a)(11), (15), (16), (19)) require the advertisement, the substantiation, the performance working papers, and a record of the **intended audience** — retained **not less than five years, the first two in an appropriate office of the adviser.**

**Why the current tools don't solve it for this segment.** Audit trails, e-signature and compliance export are **Enterprise-tier features** at Ziflow, Filestage and PageProof alike. The 5–75-person agency — which is precisely the party carrying the liability in every insurance claim above — is priced out of the artifact that would discharge it.

**Evidence grade: VERIFIED** (insurer claim files, FINRA rule text, eCFR, vendor pricing pages).

---

### P4 — Every destination has incompatible technical specs, and the failures are either loud and expensive or silent and worse

**Who and when.** The producer or designer, at the moment of export, under deadline.

**The structural finding.** The problem is not the *number* of specs. It is that the constraint families are mutually irreconcilable within one campaign. Frame rate (23.98 broadcast vs 25 DOOH vs 29.97 vs 30 platform), colour space (CMYK print vs RGB DOOH at 72 ppi vs Rec.709 broadcast), filename length (12 alphanumeric characters for Extreme Reach display, 20+H for CBS, unconstrained elsewhere), weight caps spanning five orders of magnitude (50 KB IAB mobile banner to 5 GB XR upload), audio loudness (−24 LKFS broadcast vs muted-by-default display), and safe-zone geometry (TikTok LTR vs RTL template zips vs DOOH physical inches vs broadcast title-safe). **No export preset satisfies two of these simultaneously**, so every deliverable set requires a per-destination human check.

**What it costs.** Rejections are loud but the clock is unforgiving: CBS's 5-business-day S&P window, DV360's separate asynchronous publisher approval, DOOH's 30-minute-to-overnight transcode with skipped first plays. A caption typo is a full return-to-post round trip. Missing a flight date on a bought media placement is not recoverable — and under the IAB/4A's standard T&Cs, late creative is billed pro-rata from the IO start date anyway.

**Frequency.** Every campaign, every flight, every adaptation cycle.

**A note on what we could not establish:** **no ad platform publishes creative rejection rates,** and no print trade body publishes a preflight failure rate. Every "30–40% of files get rejected" figure in circulation traces to prepress-outsourcing vendor marketing with no methodology. The honest statement is that rejection *frequency* is undocumented while rejection *consequence* (the deadline ladders above) is precisely documented.

**Evidence grade: VERIFIED** for the specs and deadlines; **explicit gap** on frequency.

---

### P5 — Tracking taxonomy failures are silent, and they destroy the measurement the client is paying for

**Who and when.** The media or performance lead, at campaign launch; the account manager, at the monthly report, wondering why a channel shows nothing.

**The mechanism, from Google's own documentation.** GA4 UTM parameter values are case-sensitive: `utm_source=google` and `utm_source=Google` are different, and "SpringSale and Spring_Sale are considered distinct." GA4's default channel groups then apply exact-match and regex rules: Email requires medium exactly `email|e-mail|e_mail|e mail`; Organic Social requires medium in `('social','social-network','social-media','sm')`; Paid Search requires a medium matching `^(.*cp.*|ppc|retargeting|paid.*)$` *and* a recognised search source. So `utm_medium=newsletter` lands in **Unassigned**. `utm_medium=paid_social` lands in **Unassigned**. `utm_medium=Social` fails the list. Google's own official remedy is procedural, not technical: "maintain a strict, case-sensitive naming convention for all fields." **There is no platform-side validation.** Two of GA4's own accepted parameters — `utm_creative_format` and `utm_marketing_tactic` — are accepted but not reported, which is silent data loss by design.

**Why this is worse than a rejected ad.** A rejected ad announces itself. A misfiled UTM produces a link that works perfectly, a campaign that runs perfectly, and a report that is wrong — discovered, if ever, weeks later when a channel's spend cannot be attributed and the client asks why.

**Currently handled by:** a shared Google Sheet — which is the literal implementation of Google's own written guidance.

**Tooling reality.** GTM Preview/Debug is free but is a manual, per-page, per-session check with no debug interface for mobile app, AMP or server-side containers; it does not sweep a site or diff against an expected tag inventory. The commercial tag-governance category is entirely **quote-gated**: ObservePoint's "pricing" page contains no figures, no tiers and no terms, and utm.io's pricing URL redirects to a dead page. For a 20-person agency, quote-gating is not an expense problem; it is a de facto exclusion mechanism.

**Evidence grade: VERIFIED** on the mechanism (Google documentation) and the tool pricing wall (verified absence); **INFERRED** on small-agency behaviour, since practitioner forums were unreachable.

---

### P6 — Rounds are contracted at two and delivered at four, and 78% of agencies never bill the difference

**Who and when.** The agency principal, monthly, looking at realization.

**Currently handled by:** the awkward conversation, or more often its absence. Ignition's survey of professional-services practitioners found **90% (US) have had work go unbilled for out-of-scope requests**, 43% absorb the cost personally, 89% have delayed or avoided the conversation, 67% say avoiding it damaged the relationship, and 30% reported staff resignations as a consequence. That survey is accountants, not agencies — I flag it as adjacent-vertical, and note that **the absence of an agency-specific equivalent is itself a finding.** The agency-specific data we do have is Ignition's 2025 agency report (57% losing $1–5k/month, 78% rarely charging for out-of-scope) and PMI's cross-industry Pulse (n=4,455): **52% of projects experienced scope creep, 33% among top performers versus 69% among underperformers.**

**Why current handling fails.** The evidence needed to bill an overage — that round 3 was requested after approval of round 2, in writing, by someone with authority — exists only as scattered email. Creative COW practitioner Ned Miller states the failure exactly: "I am not interfacing with the final decision maker… they come back with changes, that should be an additional cost… I have to eat the cost or start arguing with the client." His workaround is to require the request by email and later cite "As per your email of…" — a manual, memory-dependent audit trail.

**Evidence grade: VERIFIED** on the practitioner mechanism and the round-count mismatch; **VENDOR-SURVEY (adjacent vertical)** on the dollar figures.

---

### P7 — "Final files" is a bundle of components with different transferability rules, and nothing checks it

**Who and when.** The designer, at handover; the agency, when a client's new vendor calls asking for the fonts.

**The rules, from the licensors.** Adobe's own documentation states the Adobe Fonts terms "don't allow copying or moving the files," and that fonts "may only be embedded in a document for viewing or printing existing content" — so **`File > Package` in InDesign, the standard agency handoff move, silently produces an incomplete and non-compliant package whenever Adobe Fonts are used.** Flattened output (PDF/JPEG/PNG with embedded or rasterised font data) is fine; anything the client needs to *edit* triggers a licensing event. Shutterstock: "Standard and Enhanced Licenses do not allow for content to be transferred in whole to another party" — only Premier permits transfer. Photography is licensed by term, territory and media. And post-*CCNV v. Reid*, **freelancer contributions belong to the freelancer** absent a signed written assignment — meaning an agency that promised the client ownership but never papered the freelancer has sold something it does not own.

**What the reference contract says.** The AIGA Standard Form of Agreement distinguishes **§1.6 "Final Deliverables"** from **§1.13 "Working Files"** as separate defined terms, offers four mutually exclusive IP options of which only work-made-for-hire conveys rights in preliminary works, and conditions transfer on payment in full (§3.4). §9.1(c) puts responsibility for third-party licenses on the client. §5 requires the client to supply content "in a form suitable for reproduction… without further preparation" — the contractual hook for the asset chase, routinely unenforced.

**What it costs when it fails.** Michael Janda documents an agency demanding **$40,000 to release source files** after a relationship ended; the client paid, then damaged the agency by word of mouth. On the access side, *DSPT International v. Nahum* (9th Cir. 2010) held that using a domain to get leverage in a business dispute violates the ACPA — **~$152,000 in damages** — and no published UDRP decision supports a developer holding a client domain over non-payment.

**Evidence grade: VERIFIED** (licensor terms, AIGA SFA text, case law); **INFERRED** on prevalence.

---

### P8 — For regulated clients, the agency assembles the compliance record but does not own the system that holds it

**Who and when.** The account lead on a pharma, financial-services, health or supplement account, on every deliverable, forever.

**The asymmetry.** The legal obligation — the FDA Form 2253 submission under 21 CFR 314.81(b)(3)(i), the FINRA principal approval, the SEC substantiation record — sits on the sponsor, the broker-dealer or the adviser. **The artifact that satisfies it is assembled by the agency.** The agency carries operational and contractual risk without the regulatory license, and works inside client-owned systems it cannot export from.

**The enforcement environment is not theoretical.** FDA OPDP issued **44 untitled letters on a single day (9 Sept 2025)** following a presidential memorandum, against a baseline of 8 untitled letters in the ~21 months since the CCN rule was finalised; 2026 letters continue at pace (Sanofi, Viatris, Lundbeck, Bayer, Pfizer, Novo Nordisk ×2, Janssen, argenx ×2 in the first seven months). The SEC's Marketing Rule sweeps charged 5 advisers **$200,000** total in April 2024 and 9 advisers **$1,240,000** total in September 2024 — and the violations were overwhelmingly *documentation* failures, not creative ones: no written promoter agreement, a third-party rating missing its date and period, a disclosure placed behind a hyperlink, an unsubstantiated "conflict-free" claim. The SEC's December 2025 Risk Alert names hyperlinked disclosures explicitly: they "fail to meet the 'clear and prominent' obligation."

**Agencies are directly reachable.** FTC Endorsement Guides **§255.1(f)** makes intermediaries "including advertising agencies and PR firms" responsible for endorsements they create or disseminate where they "know or should know" these are deceptive. The 2024 Consumer Reviews and Testimonials Rule (16 CFR Part 465, effective 21 Oct 2024) reaches "advertising agencies, PR firms, review brokers, and reputation management companies" on a knew-or-should-have-known standard, with civil penalties of **up to $53,088 per violation**; the FTC warned ten companies in December 2025. The named-agency precedents are real if old: **TBWA Worldwide** was a named respondent alongside Nissan in 2014, and **Creaxion Corporation** was charged in 2018 *without* the advertiser being named.

**And the clocks are short.** A NAD challenge lands with a **15-business-day** response window and requires the complete substantiation file for every challenged claim — files the agency may hold and the client may not.

**Currently handled by:** a "legal/claims" tab in the campaign deck, a substantiation folder on Drive, a compliance-log spreadsheet, screenshots of influencer posts taken sometimes, and email chains standing in for approval records.

**Evidence grade: VERIFIED** (eCFR, FDA letter list, SEC press releases and Risk Alert, FTC rule text and penalty schedule, NAD procedures).

---

### P9 — Client reporting is unbilled labour that most clients do not read

AgencyAnalytics' benchmark study (n=121 agencies, 46% of them 6–20 employees — dead centre of this report's band) found **58% report monthly**, with **2.5–5 hours per report before automation** and 52% under 30 minutes after. **96% of agencies do not charge separately for reporting.** And only **5% of clients read the report "all of the time"** (29% "most of the time"; 54% average email open rate). A 15-person agency with 25 monthly-reporting clients at the pre-automation figure is spending **62–125 hours a month** assembling documents two-thirds of clients do not reliably read, at zero revenue.

The reporting tool category is mature and reasonably priced, so this is *not* a recommended build target — but note what none of them do: the *narrative*, weekly **status** reporting (project state, blockers, what we're waiting on from you) as distinct from **performance** reporting, offline channels, and getting the result into the client's own deck template.

**Evidence grade: VERIFIED** (real survey with disclosed sample and geography; note the respondent base is a vendor's own customers, which biases toward already-automated agencies and makes the time figures a floor).

---

### P10 — The asset chase at kickoff

Access collection alone cost one named agency "at least half a day" per client, run as "very much a back-and-forth email discussion" with a customised up-to-100-slide onboarding document. A client complained about lack of progress "during the two weeks it took them to get asset access." Content is the deeper stall: one practitioner describes sites finished and waiting, "weeks and months go by. When (if) the content finally arrives, my timeline is thrown off. And depending on the amount of time that's passed (sometimes years!), the design needs updating!"

This problem is real but **already served** at reasonable prices (Content Snare from $35/mo, Leadsie from $49/mo). It is ranked last for that reason, and the recommendation below addresses only the specific sliver — offboarding revocation — that those tools do not cover. Note also: **no independent survey quantifies agency project delay attributable to missing client assets at kickoff.** Every number in circulation is vendor-sourced.

---

## 4. Application opportunities

Ten concepts, small and medium complexity. Each is scoped to be free and open-source in its base version, with paid client-specific customisation as the commercial layer.

---

### A1 — Comment Ledger (feedback reconciliation and resolution sheet)

**Intended user.** Project manager or designer at a 5–40 person agency, on every revision round.

**Problem solved.** P1. Feedback arrives from three or four channels bound to a version that no longer exists, and nobody can prove each item was addressed.

**Current workflow.** Export Acrobat comments or read them in the proofing tool; retype into a checklist or work straight from the sidebar; tick items off by memory; hope.

**Proposed workflow.** Drop in the sources — an exported PDF annotation set (FDF/XFDF or the PDF itself), a pasted email thread, a pasted Slack export, a marked-up Word doc — and the tool emits one numbered, deduplicated **comment register** for that version, with each item classified (copy / layout / factual / scope-change / question), attributed to a commenter, and **flagged where two comments contradict each other**. The designer marks each item done / not done / needs-client-decision / out-of-scope. On the next version, the tool emits a **resolution sheet** that ships alongside the file: "24 comments received, 21 addressed, 2 conflict — please pick, 1 out of contracted scope — see change order."

**Inputs.** PDF/FDF/XFDF annotations; pasted email or Slack text; optional CSV export from a proofing tool.
**Outputs.** Comment register (CSV + PDF); resolution sheet (PDF) for client delivery; carry-forward list of unresolved items.

**Essential features.** Deduplication of the same note from three people; conflict detection; carry-forward of unresolved items to the next round; out-of-scope tagging that feeds A9.
**Excluded from initial scope.** Being a proofing tool. It does not host files, does not render previews, does not accept client logins. It sits *behind* whatever the client already uses.

**AI: optional-to-useful.** Rules handle deduplication of near-identical text and extraction of PDF annotations. An LLM materially helps with two things conventional code cannot do: turning "the blue feels a bit corporate, and can we look at the headline again?" into two discrete action items, and detecting that reviewer A's "make it bigger" contradicts reviewer B's "too heavy, dial it back." Ship the rules-only version first; the AI layer should be optional and local-model-capable, because client copy is confidential.

**Why not a spreadsheet.** The register itself is spreadsheet-shaped. What is not: extracting annotations from PDFs, carrying unresolved items across versions, and generating the client-facing resolution sheet. The spreadsheet is what agencies use today and it is exactly where the retyping cost lives.

**Complexity: medium. Learning: 20 minutes.**
**Value.** If it removes one round from 30% of jobs, at a contracted two-round allowance and 3–5 rounds actual, it converts unbilled rework directly into capacity. More reliably: it produces the resolution sheet, which is a client-facing artifact that visibly changes the conversation about round counts.

**Risks.** Client copy is confidential — an AI layer must be optional and offline-capable. Over-scoping into a proofing tool is the obvious failure mode.
**Substitutes.** Ziflow, Filestage, Frame.io, PageProof — all of which *collect* feedback well and none of which reconcile it. Ziflow lists change verification on its roadmap in Enterprise preview.
**Customisation potential.** High: per-agency comment taxonomies, scope-clause language, integration with the agency's PM tool.

---

### A2 — Sign-Off Certificate (approval of record)

**Intended user.** Agency principal or account manager, on every deliverable that leaves the building.

**Problem solved.** P3. The artifact that transfers liability at sign-off is behind an enterprise paywall, and insurers' claim files show exactly what it costs to lack it.

**Current workflow.** An email that says "looks good, go ahead" — from someone who may not be the decision-maker — filed nowhere in particular.

**Proposed workflow.** Point the tool at the exact file being approved. It computes a content hash, captures the version label, the approver's name/role/email, the timestamp, the delivery channel, and a short statement of what is being approved (and explicitly what is not — e.g. "colour on press not yet verified"). It emails a one-click confirmation link; on confirmation it emits a **signed PDF certificate** embedding the hash and a thumbnail, and files it in a per-client register. A **first-use / last-use** field is captured at publish and takedown, and a retention clock (3 years FINRA, 5 years SEC, 3 years ABPI, or a custom term) is started.

**Inputs.** The approved file; approver contact; optional regulatory profile.
**Outputs.** Signed certificate PDF; per-client approval register (CSV); retention/expiry report.

**Essential features.** Content hash so nobody can argue about which version; explicit scope-of-approval text; first-use and last-use date fields; retention clock; export of the whole register.
**Excluded.** Legally binding e-signature under eIDAS/ESIGN in v1 (a hash-plus-email-confirmation record is what actually gets used in a dispute at this scale); workflow routing; multi-stage approval chains.

**AI: inappropriate.** This is a hashing, dates and records problem. Adding a model would weaken it.

**Why not a spreadsheet.** A spreadsheet cannot bind the record to the bytes of the file. The hash is the whole point: it is what distinguishes "the client approved *this*" from "the client approved something we called v4."

**Complexity: small. Learning: 10 minutes.**
**Value.** Direct: the PolicyBee claims run £9,000–£21,995 and are exactly the shape of dispute a sign-off record resolves. Indirect: for financial-services clients, the first-use/last-use field is *mandatory* under FINRA 2210(b)(4)(A) and, per the research, is a field literally nobody's project tool has.

**Risks.** Must not be marketed as legal advice or as a qualified electronic signature. Retention periods vary by regime and must be configurable, not hardcoded.
**Substitutes.** Ziflow/Filestage/PageProof audit trails and e-signature — all Enterprise-tier. DocuSign, which is built for contracts, not for deliverables, and prices per envelope.
**Customisation potential.** High: regime-specific certificate templates (FINRA, SEC, ABPI, FDA 2253 transmittal), agency branding, PM-tool integration.

---

### A3 — Rights & Usage Expiry Ledger

**Intended user.** Producer, account director, or principal at any agency that produces original content with people, music, stock or licensed footage in it.

**Problem solved.** P2. Multiple non-aligned expiry clocks per asset, computed by rules no calendar tool implements, with six-figure downside.

**Current workflow.** A spreadsheet tab, PDFs in a Drive folder, and calendar reminders set by whoever remembered.

**Proposed workflow.** Register each *element* inside a deliverable — performer, music track, stock image, footage, location, likeness, font — with rights holder, license type, license document, territory, permitted media, term start, numeric caps (print run, OOH impressions, production budget), renewal option and its cap, and release status. The tool computes the correct end date **per rule type**, including:

- SAG-AFTRA **MPU**: first production day + 10 business days + 2 years − 1 day (verified against SAG-AFTRA's own worked example: 19 Aug 2025 → 2 Sept 2027)
- **13-week holding fee cycles** from first production day, tracked independently of the MPU
- Music sync terms by term × territory × media, including the full-annual-fee rule for non-consecutive flighting
- Stock license **numeric thresholds**, re-checked whenever the media plan changes

It then produces (a) advance warnings at configurable intervals, (b) a **takedown checklist** enumerating every live placement of an expiring asset, and (c) an evidence bundle — licenses, releases, payment records — when a claim arrives.

**Inputs.** Per-element license metadata; the media plan (for numeric caps); a placement list.
**Outputs.** Expiry calendar (with ICS export); takedown checklist; per-asset rights dossier PDF.

**Essential features.** Rule-based date computation (this is the differentiator — a plain date field is useless here); numeric-threshold tracking against actual buy volumes; the takedown checklist; the evidence bundle.
**Excluded.** Payment processing, union filing, contract negotiation, DAM/asset storage. It tracks rights, not files.

**AI: inappropriate for the core; optional at the edge.** The date arithmetic must be deterministic and auditable — an LLM here is a liability. An optional assist for extracting terms from an uploaded license PDF is reasonable, provided every extracted field is presented for human confirmation.

**Why not a spreadsheet.** Because the arithmetic is not calendar arithmetic. "+10 business days, +2 years, −1 day" is not a formula anyone gets right by hand twice, the 13-week cycles do not align with the MPU, and the numeric caps are invalidated by events (a media plan change) rather than by time. A spreadsheet also cannot generate the takedown checklist, which is the thing that actually prevents the loss.

**Complexity: medium (small if scoped to SAG + stock only in v1). Learning: 30–45 minutes for the concepts, 10 for the interface.**
**Value.** *Olive v. GNC* is $1,123,000 against a missed calendar entry. *Beastie Boys v. Monster* is $1.7M plus $667,849 in fees. SAG-AFTRA late-payment liquidated damages accrue without notice, and one performer's notice escalates damages for every performer on the spot. This is the highest-consequence, lowest-complexity problem in the entire report.

**Risks.** Getting a rule wrong is worse than having no tool — every computed date must show its working and cite the governing clause, and the tool must carry a clear "not legal advice, verify against your contract" posture. Union agreements change on a three-year cycle (the current one runs to 31 Mar 2028), so the rule set needs versioning and dating.
**Substitutes.** Essentially none at this tier. Enterprise talent-payment houses (Extreme Reach, Cast & Crew, Talent Partners) handle payments for their own clients but do not give the agency a cross-vendor ledger. A 2023 US patent application for an "automated talent usage rights negotiation & management tool" (US20230010020A1) confirms the problem is recognised and unserved.
**Customisation potential.** Very high: per-agency rule packs (SAG vs non-union vs UK Equity), integration with a payroll house's export, per-client media-plan feeds.

---

### A4 — Destination Spec Gate

**Intended user.** Producer, editor, or designer, at export, on every campaign.

**Problem solved.** P4. Mutually incompatible destination specs, checked by hand under deadline.

**Current workflow.** A spec PDF from the media partner, opened in another window, checked by eye; a rejection email two days later.

**Proposed workflow.** Maintain a **destination profile library** as plain YAML/JSON — IAB fixed sizes with gzipped weight caps, Google Ads display, DV360 CTV bitrate ladder and no-duplicate-frames, LinkedIn, TikTok (including the LTR/RTL safe-zone templates), YouTube durations, Extreme Reach display and broadcast, CBS-style broadcast, DOOH at 25 fps, and print (bleed, safe area, DPI, colour space, total ink coverage by press/stock). Point the tool at a folder of finished files, tick the destinations, and it runs the actual technical checks — dimensions, duration, container and codec, bitrate, frame rate, duplicate-frame detection, gzipped byte size, filename length and character set, loudness in LKFS, true peak, colour space, embedded fonts, bleed box, ink coverage — and emits a pass/fail matrix with the specific failing value and the required value, plus suggested compliant filenames.

**Inputs.** A folder of deliverables; a destination selection; optionally a client-specific profile.
**Outputs.** Pass/fail matrix (HTML + CSV); rename script; a delivery manifest listing what is being sent where, to which spec, on what date.

**Essential features.** The profile library as editable text (so agencies can add a client's or a publisher's own spec sheet without touching code); the checks that require real tooling — ffprobe/ffmpeg for loudness, true peak, frame rate and duplicate frames; ImageMagick for raster; a PDF library plus Ghostscript for ink coverage and boxes; gzip for real transfer weight.
**Excluded.** Transcoding, resizing, or fixing anything. It is a gate, not a converter — this keeps it small, keeps it trustworthy, and avoids competing with the entire encoding industry.

**AI: inappropriate.** Every one of these checks is a deterministic measurement against a published number.

**Why not a spreadsheet.** A spreadsheet can hold the specs (the Ghent Workgroup literally distributes its own specification as a spreadsheet) but cannot measure the file. The measurement is the product.

**Complexity: medium. Learning: 15 minutes.**
**Value.** A single missed broadcast S&P window (5 business days at CBS) or a rejected CTV asset waiting on FreeWheel publisher approval can cost a flight. Under the IAB/4A's T&Cs, late creative is billed pro-rata from the IO start date regardless — so the media is paid for whether or not it runs.

**Risks.** Spec drift. Platform specs change without notice, and a stale profile that says PASS is worse than no tool. Mitigation: date-stamp every profile, show its age prominently, and treat profile maintenance as the community contribution surface — which is a genuine argument for the open-source model here.
**Substitutes.** Acrobat Pro's preflight (which *is* the callas pdfToolbox engine, already owned at $287.88/yr and rarely opened), Enfocus PitStop Pro ($480/yr, print only), and ad-server-side rejection (which is the current, expensive gate). Nothing spans print + broadcast + digital + DOOH in one pass.
**Customisation potential.** Very high: per-client and per-publisher profiles are the natural paid service.

---

### A5 — Claim & Substantiation Register

**Intended user.** Account lead or copywriter on a regulated account — pharma, medical device, financial services, supplements, health, and any client making performance or comparative claims.

**Problem solved.** P8. The agency assembles the compliance record inside systems it does not own, and the record is the thing regulators actually examine.

**Current workflow.** A Word table, an Acrobat comment layer, a Drive folder, and a hope that whoever knew where the source document lived is still on the account.

**Proposed workflow.** For a given deliverable, register every claim: claim text, location in the piece, supporting source (document, page, figure), source date, who approved it, and the required disclosure and **where it is physically placed** (in-copy versus behind a hyperlink — the exact distinction the SEC's December 2025 Risk Alert flags as a failure). The tool then emits an **annotated PDF plus reference bundle** ready to hand into the client's Veeva vault or compliance review, tracks which claims changed between versions (the "superscript lost between MLR-approved and live" failure mode is a diff problem), starts the retention clock, and can assemble the whole substantiation file on demand against a **15-business-day NAD clock** or an FTC CID.

**Inputs.** Deliverable copy; source documents; approver identities.
**Outputs.** Annotated PDF; reference bundle (zip); claim register (CSV); a change report between versions.

**Essential features.** Claim-to-source-page linkage that survives the Word → design → digital-adaptation handoff; disclosure-placement field; version diff on the claim set; retention clock.
**Excluded.** Being a DMS or a review platform. It prepares packages for someone else's system.

**AI: genuinely useful, optional.** Extracting *candidate* claims from copy — identifying which sentences assert a fact, a comparison, a performance figure or a health benefit — is a real language task that rules do poorly. Every extracted claim must be human-confirmed. Never let a model decide whether substantiation is adequate; that is a regulated judgement.

**Why not a spreadsheet.** The register is spreadsheet-shaped; the annotated PDF, the bundle assembly and the cross-version claim diff are not, and the diff is where the documented failures happen.

**Complexity: medium. Learning: 45 minutes (the concepts are unfamiliar to non-regulated staff).**
**Value.** SEC Marketing Rule penalties ran $60,000–$325,000 per adviser in the 2024 sweeps, overwhelmingly for documentation failures. FTC penalties reach $53,088 per violation under 16 CFR 465, and the FTC states explicitly that agencies are covered on a knew-or-should-have-known standard.

**Risks.** Confidentiality is acute — pharma copy is pre-launch material. Local-first architecture is not a nicety here, it is a requirement. Also: the tool must never present itself as a compliance determination.
**Substitutes.** Veeva Vault PromoMats (no public price; third-party estimates $600–$2,400/user/yr plus $10k–$50k implementation; licensed to the sponsor, not the agency — the agency's only sanctioned entry is a **$500/person/yr certification**), Vodori Pepper Flow and Aprimo (~$20,000/yr entry by Aprimo's own published statement). Ten leading MLR tools surveyed: none discloses pricing.
**Customisation potential.** Very high, and this is arguably the best paid-services opportunity in the report: per-client claim taxonomies, per-vault export formats, and a cross-client tracker showing which asset sits in which client's system, at which round, with which reviewer, since when — something no vendor sells because vendors sell to sponsors, one vault at a time.

---

### A6 — Campaign Taxonomy Validator

**Intended user.** Media/performance lead or account manager, at every campaign launch.

**Problem solved.** P5. Silent tracking failures caused by case sensitivity and non-matching channel-group values.

**Current workflow.** A shared Google Sheet, which is the literal implementation of Google's own written guidance.

**Proposed workflow.** Define the agency's taxonomy once (allowed sources, mediums, campaign name segments, separators, case rules). Paste or import a list of destination URLs and campaign metadata; the tool builds the tagged URLs, **validates every `utm_medium` against GA4's actual default channel-group rules** and warns explicitly when a value will land in Unassigned, normalises case, detects near-duplicates that will fragment a campaign across report rows (`SpringSale` vs `Spring_Sale`), warns on parameters that are accepted but not reported (`utm_creative_format`, `utm_marketing_tactic`), and exports a QA sheet plus the final link set.

**Inputs.** Destination URLs; campaign metadata; a taxonomy definition file.
**Outputs.** Tagged URL set (CSV); validation report; a per-client taxonomy document.

**Essential features.** The GA4 channel-group rule set as data (versioned and dated, since Google changes it — an AI Assistants channel was added recently); near-duplicate detection; the taxonomy definition as a shareable file so a client's in-house team and the agency use the same one.
**Excluded.** Link shortening, click tracking, redirects, analytics. It produces correct strings and refuses incorrect ones.

**AI: inappropriate.** Regex and string normalisation.

**Why not a spreadsheet.** A spreadsheet can build the string. It cannot tell you the string will silently fail GA4's channel rules, which is the actual failure mode.

**Complexity: small. Learning: 15 minutes.**
**Value.** Prevents a category of failure that is invisible until the monthly report, at which point the spend for a channel is unattributable and cannot be reconstructed. Also directly improves the reporting deliverable in P9.

**Risks.** GA4 rules change; the rule set must be dated and easy to update. Low ceiling on value per incident, offset by very low cost.
**Substitutes.** Google's own Campaign URL Builder (builds, does not validate), dozens of free UTM builders (same), ObservePoint (no public pricing at all), utm.io (pricing page dead). **This is the concept with the weakest differentiation** — the honest positioning is "the free builder everyone uses, plus the one validation step Google documents but does not implement."
**Customisation potential.** Moderate: per-client taxonomies, CRM/CMS naming alignment.

---

### A7 — Handoff Manifest & License Auditor

**Intended user.** Designer or producer at final delivery; the principal at contract close-out.

**Problem solved.** P7. "Final files" is a bundle whose components have different transferability rules, and one folder handoff can breach three licenses at once.

**Current workflow.** `File > Package`, zip, WeTransfer, hope.

**Proposed workflow.** Point the tool at the delivery folder or an InDesign package. It inventories the components, cross-references a per-agency **license register** (fonts and their source, stock assets and their license tier, photography and its usage terms, freelancer contributions and whether an assignment is on file), and flags what cannot be transferred as-is: Adobe Fonts (per Adobe's own terms, the files may not be copied or moved), Shutterstock Standard/Enhanced assets (non-transferable; only Premier permits transfer), photography outside its licensed media, freelancer work with no signed assignment. It then emits a **delivery manifest** stating, item by item, what is being transferred and under what terms — a document that both protects the agency and tells the client exactly what they must license themselves.

**Inputs.** The delivery folder or package; the agency's license register.
**Outputs.** Delivery manifest PDF; exceptions list; a "flattened-only" packaging recommendation where editable transfer is not permitted.

**Essential features.** Font source detection (Adobe Fonts vs licensed desktop vs open-source); asset-to-license matching; the manifest.
**Excluded.** Reading and interpreting license PDFs automatically in v1; DAM functionality; rights *expiry* (that is A3, and the two should share a data model).

**AI: optional and marginal.** Matching a filename to a license record is fuzzy string matching. Reading a license PDF to extract terms is an AI task, but it is also the one where a wrong answer is most dangerous.

**Why not a spreadsheet.** The register is a spreadsheet. Walking the folder, identifying the fonts actually used, and producing the manifest is not.

**Complexity: medium. Learning: 30 minutes.**
**Value.** Prevents a specific, documented, silent compliance breach (the InDesign package with Adobe Fonts in it) and creates the manifest that pre-empts the "$40,000 for the source files" fight.

**Risks.** License terms change (Shutterstock's current ToS is dated 19 Jan 2026); the rules must be dated. Font detection across the Adobe ecosystem is fiddly.
**Substitutes.** None found. No agency-facing tool checks licensing at export.
**Customisation potential.** High: agency-specific license registers and manifest templates.

---

### A8 — Access Register & Offboarding Verifier

**Intended user.** Operations lead or principal, at onboarding and — critically — at offboarding.

**Problem solved.** The offboarding sliver of P10 that Leadsie and AgencyAccess do not cover: proving that access was actually and completely revoked.

**Current workflow.** A password manager, a mental list, and a hope that nothing was missed.

**Proposed workflow.** Maintain a per-client register of every access grant: platform, asset (Page, Instagram account, ad account, pixel, catalog, property, container, MCC link), grant type, who holds it, when granted. At offboarding, generate a **revocation checklist** derived from that register — including the specific traps: Meta partner removal is **asset-by-asset**, not one action, and staff holding direct "People" access must be removed separately from the partner removal; Google Ads has exactly **one owner manager account** and ownership must be explicitly transferred; GA4 properties inside an agency-controlled account must be *moved*, not re-permissioned. Then capture confirmation of each revocation and emit a dated **access closure record** for the client file.

**Inputs.** The access register; the offboarding date.
**Outputs.** Revocation checklist; access closure record PDF; an asset-ownership summary for the client.

**Essential features.** The platform-specific gotcha library (this is the value — the checklists, not the storage); the closure record.
**Excluded.** Storing credentials (never), OAuth grant automation (Leadsie does this well at $49–299/mo), password management.

**AI: inappropriate.**

**Why not a spreadsheet.** Mostly it could be — the honest answer. The differentiator is the maintained platform-gotcha library and the closure record. This is the weakest "why not a spreadsheet" case in the report and is scored accordingly.

**Complexity: small. Learning: 15 minutes.**
**Value.** Reduces a real security and professional-liability exposure (residual partner access on a pixel after "offboarding" is complete) and pre-empts ownership disputes — the domain-hostage version of which produced ~$152,000 in damages in *DSPT v. Nahum*.

**Risks.** Platform UIs and permission models change constantly; the gotcha library ages fast.
**Substitutes.** Leadsie and AgencyAccess (onboarding-side grants), password managers (credentials, not grants).
**Customisation potential.** Moderate.

---

### A9 — Round Counter & Overage Notice

**Intended user.** Account manager and principal, continuously.

**Problem solved.** P6. Two contracted rounds, four delivered, 78% never billed, and no evidence assembled at the moment it would have been easy to assemble.

**Current workflow.** Nothing, then an awkward conversation, then absorption.

**Proposed workflow.** Record the contracted allowance per job (rounds, or hours, or both). Log each round with its date, the requester, and the source of the request. When an incoming request would exceed the allowance, or arrives after an approval was captured by A2, the tool flags it and drafts an **overage notice** citing the evidence — "as per your approval of v3 on 14 July and your request of 22 July" — with the change-order amount computed from the agency's rate card. It also tracks **client feedback latency**, so the agency can show that its own delays were not the cause of the schedule slip.

**Inputs.** Contracted allowance; round log (ideally fed from A1 and A2 rather than typed).
**Outputs.** Overage notice draft; per-job round and latency summary; a portfolio view of over-servicing by client.

**Essential features.** The evidence-citing draft (the thing that makes the conversation possible); the client latency record; the portfolio view that shows *which* client is the problem.
**Excluded.** Invoicing, time tracking, contract management. It produces a notice; the agency's existing systems bill it.

**AI: optional.** Drafting the notice in the agency's tone is a reasonable LLM task; the arithmetic and the evidence are not.

**Why not a spreadsheet.** The counting is spreadsheet work, but nobody does it, because it has to happen at the moment of the request rather than at month-end. The value is in the trigger, not the tally.

**Complexity: small. Learning: 20 minutes.**
**Value.** Ignition's agency data: 57% of agencies lose $1,000–$5,000/month on unbilled work, 30% lose more than $5,000. Recovering even a third of that is $4,000–$20,000/year for a small shop.

**Risks.** Cultural, not technical. An agency that will not have the conversation will not use the tool — and the Ignition data says 89% delay or avoid it. Mitigation: the strongest framing is not "bill more" but "show the client their own decision history," which is the same artifact.
**Substitutes.** Ignition's Instant Bill (accounting-vertical-first, $39–399/mo), Productive/Scoro/Workamajig budget alerts (which fire on hours, not on rounds, and only for agencies already running full agency-management software).
**Customisation potential.** High: rate cards, contract clause language, PM-tool integration.

---

### A10 — Accessible Delivery Gate (PDF and web deliverables)

**Intended user.** Designer or production lead delivering to public-sector, education, healthcare, or accessibility-conscious clients.

**Problem solved.** Client-bound PDFs and pages that fail WCAG, discovered after delivery, remediated at $5–25 per page.

**Current workflow.** Nothing, or Acrobat's built-in accessibility checker run once by whoever knows it exists.

**Proposed workflow.** Run the delivery set through structural checks — document tags, reading order, alt text presence, document language, heading hierarchy, colour contrast, table headers, bookmark structure — and emit both a **remediation to-do list** for the designer and a short **conformance summary** for the client stating what was checked, against which standard version, on what date.

**Inputs.** PDFs or a URL set; the target standard (WCAG 2.1 AA or 2.2 AA).
**Outputs.** Remediation list; conformance summary PDF.

**Essential features.** The client-facing conformance summary (the differentiator — existing checkers produce developer output, not a deliverable); correct handling of the **2.1-versus-2.2 gap**, since both binding US rules mandate WCAG **2.1 AA** while most client language now says 2.2.
**Excluded.** Automated remediation, VPAT/ACR authoring, screen-reader testing (which is inherently manual).

**AI: optional.** Drafting candidate alt text is a legitimate assist that must be human-reviewed. Everything structural is deterministic.

**Why not a spreadsheet.** It is a file-inspection problem.

**Complexity: medium. Learning: 45 minutes (the standard is the hard part, not the tool).**
**Value.** Remediation runs $5–25/page by vendor estimate — a 40-page brochure is $200–1,000, frequently more than the fee for the export step and almost never scoped. Federal website-accessibility filings hit **3,117 in 2025, up 27% year over year**.

**Regulatory note, and this matters because most published guidance is now stale:** the ADA Title II web rule deadlines were **extended by DOJ interim final rule on 20 April 2026** — entities serving populations ≥50,000 move from 24 Apr 2026 to **26 Apr 2027**, smaller entities and special districts to **26 Apr 2028**. HHS followed on **7 May 2026**, moving its Section 504 web/mobile deadlines from 11 May 2026 to **11 May 2027** (15+ employees) and to **10 May 2028** (under 15). Both mandate **WCAG 2.1 AA**. Two of the research threads for this report disagreed on the HHS date; I verified it directly against the HHS press release. Note that the extension moves the enforcement floor, not the contractual ceiling — procurement language written against the original dates is already in market, and private ADA litigation is unaffected.

**Risks.** Automated checks cover perhaps 30–40% of WCAG criteria; over-claiming conformance would be worse than saying nothing. The summary must state precisely what was and was not machine-checkable.
**Substitutes.** Acrobat Pro's accessibility checker (already owned), PAC (free), the free axe extension, Deque's axe DevTools Pro and Equidox/CommonLook (all quote-gated with no public pricing).
**Customisation potential.** Moderate-to-high for agencies with recurring public-sector work.

---

## 5. Opportunity ranking

Each concept scored 1–5 on ten criteria; maximum 50.

| # | Concept | Severity | Frequency | ROI clarity | Ease of learning | Ease of build | Stays narrow | Differentiation | Customisation | Test data | Evidence confidence | **Total** |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **A3** | **Rights & Usage Expiry Ledger** | 5 | 4 | 4 | 5 | 5 | 5 | 5 | 5 | 4 | 5 | **47** |
| **A2** | **Sign-Off Certificate** | 4 | 5 | 4 | 5 | 5 | 5 | 4 | 4 | 5 | 5 | **46** |
| **A4** | **Destination Spec Gate** | 4 | 5 | 5 | 5 | 4 | 4 | 4 | 5 | 5 | 5 | **46** |
| **A1** | **Comment Ledger** | 5 | 5 | 4 | 4 | 4 | 4 | 5 | 4 | 4 | 5 | **44** |
| **A6** | **Campaign Taxonomy Validator** | 3 | 5 | 4 | 5 | 5 | 5 | 3 | 4 | 5 | 5 | **44** |
| **A5** | **Claim & Substantiation Register** | 5 | 3 | 4 | 4 | 4 | 4 | 5 | 5 | 3 | 5 | **42** |
| **A9** | **Round Counter & Overage Notice** | 4 | 5 | 5 | 5 | 4 | 4 | 3 | 4 | 3 | 4 | **41** |
| **A7** | **Handoff Manifest & License Auditor** | 4 | 4 | 3 | 4 | 3 | 4 | 5 | 4 | 3 | 4 | **38** |
| **A8** | **Access Register & Offboarding Verifier** | 4 | 3 | 3 | 5 | 4 | 4 | 3 | 4 | 3 | 4 | **37** |
| **A10** | **Accessible Delivery Gate** | 3 | 3 | 3 | 4 | 3 | 4 | 2 | 4 | 4 | 4 | **34** |

### The top three explained

**A3 — Rights & Usage Expiry Ledger (47).** This is the strongest opportunity in the report and it is not close on the dimensions that matter most. The problem is documented by union contract text, licensor terms of service and published court decisions rather than by anyone's survey — *Olive v. GNC* is a $1,123,000 judgment against a missed calendar entry, and the emotional-distress component was over four times the license damages. The build is a database, a rule engine and a notification schedule; there is no AI, no integration surface, and no dependency on client adoption. Differentiation is near-total: the enterprise talent-payment houses serve their own payment workflow, not the agency's cross-vendor ledger, and a 2023 patent application confirms the problem is recognised and unserved. The only scoring deductions are frequency (a produced-content agency touches it constantly; a pure digital shop rarely) and test-data availability (the rules are public; real client licenses are not).

**A2 — Sign-Off Certificate (46).** The cheapest thing to build in the report and the one with the clearest artifact. Every deliverable that leaves the building needs one; every professional-indemnity claim in the research turns on whether one existed; and for financial-services clients the first-use/last-use fields it captures are legally mandatory under FINRA 2210(b)(4)(A) and, per the research, exist in no project tool anyone sells. The strategic value is higher than its score suggests, because it is the natural data spine for A1, A5 and A9 — build it first and the others get their event log for free.

**A4 — Destination Spec Gate (46).** The most immediately demonstrable. It produces a red-and-green matrix in thirty seconds against files an agency already has, which makes it the easiest of the ten to validate with a practitioner in a single conversation. Its scores are held down only by ongoing spec maintenance — the one real risk — which is also the best argument for the open-source model, since profile contributions are exactly what a community can supply and a solo developer cannot.

### What should be investigated next

**A3 first**, and specifically the SAG-AFTRA MPU and holding-fee arithmetic, because it is the narrowest slice with the largest consequence and can be validated against SAG-AFTRA's own published worked examples before speaking to a single practitioner. **A2 in parallel**, because it is a weekend build and is the shared substrate for three other concepts. **A4 third**, as the demo that opens conversations.

Deprioritise **A10** — the automated-check ceiling is low, the incumbents are free or already owned, and the differentiation rests on a document rather than on a capability. **A6** is worth building anyway despite its differentiation score, purely because it is a day of work and improves the reporting deliverable that 96% of agencies give away.

---

## 6. Validation plan

### Questions to ask practitioners

**For A3 (rights):**
- Walk me through the last spot you produced with union talent. Who computed the MPU end date, and where is it written down today?
- Has an asset ever stayed live past its window? What happened? *(Expect deflection; ask instead: "do you know anyone this happened to?")*
- When the client scales a buy, who re-checks whether the stock licenses still cover it?
- Who gets the call when a performer's agent asks about a holding fee — you or the client?

**For A2 (sign-off):**
- Show me the last approval you relied on. What form is it in?
- Has an error ever shipped? Who paid? Was there a written approval, and did it matter?
- For your regulated clients, where do you record who approved a piece and when it was first used?

**For A4 (spec gate):**
- How many times in the last quarter did a file come back rejected or fail QC at a vendor? What did it cost?
- Who keeps your spec sheets, and how do you know they are current?

**For A1 (comments):**
- After you send v3, how do you know every comment from v2 was handled?
- What do you do when two people on the client side ask for opposite things?

### Who to interview

Production managers and executive producers at 10–50 person video/content shops (highest A3 exposure); studio managers at design firms doing print (A2 and A4); account directors at healthcare and financial-services agencies (A5 and A2); freelance producers who work across several agencies and see multiple systems; a talent payroll house account rep (Extreme Reach, Cast & Crew, Talent Partners) to learn what agencies ask them that they cannot answer; a professional-indemnity broker serving creative firms (PolicyBee and With Jack both publish claim narratives and are natural first calls); the Agency Management Institute and Bureau of Digital communities; and a SAG-AFTRA business representative for a sanity check on the MPU rule implementation.

### Search terms for further research

`SAG-AFTRA holding fee missed`, `maximum period of use expired commercial`, `usage rights spreadsheet agency`, `stock license print run exceeded`, `sync license renewal option agency`, `"approval of record" advertising liability`, `client approved wrong version reprint`, `preflight failed missed air date`, `Extreme Reach filename rejected`, `DV360 CTV creative rejected duplicate frames`, `utm_medium unassigned GA4 fix`, `MLR submission package checklist agency`, `agency revision round change order template`, `InDesign package Adobe Fonts client`. On forums: r/agency, r/advertising, r/editors, r/PPC, r/analytics, Creative COW, PrintPlanet, the Measure Slack — **all of which were unreachable in this research environment and represent the highest-value unexplored evidence source.**

### Sample files and data needed

- A real (or realistic) set of campaign deliverables: 8 IAB display sizes with HTML5 bundles, a 30s spot in ProRes and MP4, social cutdowns at 16:9/1:1/4:5/9:16, a print PDF, a DOOH file. Needed for A4; largely constructible from public spec documents.
- An exported PDF annotation set (XFDF) from a real review round, plus the corresponding email thread. Needed for A1; the hardest artifact to obtain because it is client-confidential — anonymised or synthetic is acceptable for a prototype.
- SAG-AFTRA's published contract, FAQs and worked examples (public); Shutterstock's current ToS (public, effective 19 Jan 2026); a real music sync license (hard).
- A GA4 property with messy historical UTM data, for A6.

### Prototypes that would validate

- **A3:** a single-file script that takes a first-production-day date and prints the MPU end date, the 13-week holding fee cycle dates, and the release-from-exclusivity events. Validate the output against SAG-AFTRA's own worked example (19 Aug 2025 → 2 Sept 2027) before writing any interface. If a producer looks at that output and says "that's the thing I get wrong," the concept is confirmed in one meeting.
- **A2:** a 200-line script that hashes a file, sends a confirmation email, and emits a certificate PDF. Show it to a principal who has had a reprint dispute.
- **A4:** an ffprobe/ImageMagick wrapper reading one YAML profile, run live against an agency's own delivery folder. The demo *is* the validation.

### Assumptions most likely to make these fail

1. **That agencies will maintain a register.** All of A3, A7 and A8 depend on someone entering data at the moment an asset is licensed — before there is any felt pain. This is the single largest risk across the report. Mitigation: the entry point must be the moment the license PDF arrives (drag it in, confirm four fields) rather than a separate discipline.
2. **That the pain is felt by the buyer.** For A3, the catastrophic loss lands on whoever is the signatory — sometimes the advertiser, not the agency. If the agency is never the signatory, its motivation drops sharply. This must be tested early: ask what proportion of their work they sign for.
3. **That "we've never had a problem" is not disqualifying.** Silent-failure tools are hard to sell to people who have not yet failed. A3's demo must lead with *Olive*, not with features.
4. **That spec profiles can be kept current** without a paid maintainer (A4).
5. **That an agency will act on an overage flag** (A9) when 89% of practitioners report delaying or avoiding the conversation.
6. **That AI extraction is accurate enough to trust** (A1, A5). If the register needs full human verification anyway, the AI saves less than it appears to.

---

## 7. Cross-industry patterns

Patterns from this market that transfer to specific backlog markets:

1. **Approval-of-record as a liability artifact.** A hash-bound, timestamped record of who approved exactly which version, when, and with what scope caveats. Transfers to: *Small architectural studios (specification writing)*, *Structural engineering firms 5-30 staff*, *Commercial dental laboratories (case intake and Rx clarification)*, *Ready-mix concrete producer QC departments*, and *Building envelope and roofing consultants*. Anywhere a professional's deliverable is approved by a client and then executed by a third party, the sign-off event is what reassigns cost.

2. **Multi-clock expiry ledger with rule-based date computation.** Where an obligation's end date is computed by a domain-specific rule rather than by calendar arithmetic, and multiple non-aligned clocks attach to one object. Transfers to: *Welding inspection (AWS CWI) and NDT providers under ASTM E543/SNT-TC-1A* (personnel certification and vision-test cycles), *Calibration and metrology service providers* (gage recall intervals), *Radiation safety officer services and portable gauge licensee compliance* (leak tests, dosimetry), *Multi-state charitable solicitation registration compliance* (~40 separate renewal regimes), and *Property tax consulting and assessment appeal firms* (county-by-county deadline arithmetic).

3. **Destination-profile conformance gate.** A library of receiving-organization specs held as editable data, with deterministic measurement of the actual artifact against the selected profile. Transfers to: *Environmental laboratories producing regulator EDD deliverables (EQuIS and state formats)*, *Certified payroll and prevailing wage compliance service providers* (WH-347, DIR eCPR, LCPtracker formats), *Information return (1099/W-2) filing service providers*, and *Pipe and duct fabrication shops serving mechanical and fire protection trades*.

4. **Comment-to-resolution reconciliation across document versions.** Proving each reviewer comment was addressed in the next revision, with conflict detection between reviewers. Transfers to: *Small architectural studios*, *Civil / land development engineering and entitlement consulting* (plan-check comment responses), *County surveyor and municipal plan-check offices* (the reviewer side of the same loop), and *Court probate examiner and clerk offices*.

5. **Claim-to-source substantiation register.** Every assertion in a deliverable linked to a source document, page, date and approver, with a version diff and a retention clock. Transfers to: *Aerospace materials testing laboratories under Nadcap AC7101*, *Contract manufacturers serving FDA-regulated medical devices (ISO 13485 / QMSR)*, *Fiduciary and forensic accountants producing court accountings*, and *Independent legal nurse consultant practices* (medical chronologies are claim-to-record mappings by another name).

6. **Silent-failure taxonomy validation.** Validating identifiers and codes against the exact-match rules of a downstream system that will accept bad input without erroring and produce wrong output. Transfers to: *Medical billing and revenue cycle* (modifier and code combinations), *Workers' compensation medical billing and state fee schedule compliance*, and *Freight bill audit and payment for small shippers*.

7. **Transferability manifest at handover.** An itemised statement of what is being delivered and under what terms, where the bundle's components have different ownership and licensing rules. Transfers to: *Small architectural studios*, *UAS / drone mapping and reality-capture service providers* (data rights on captured imagery), and *Title abstracting and independent title search contractors*.

8. **Quote-gating as a market-structure signal.** Where an entire tool category publishes no pricing (ObservePoint, Equidox, CommonLook, callas pdfToolbox, Veeva, Vodori, 8 of 10 major DAM vendors), small firms are structurally excluded regardless of budget, because the sales cycle itself is disqualifying. This is a *sourcing heuristic* rather than an application pattern: in any market, the presence of a fully quote-gated tool category is a reliable indicator of an unserved small-firm segment. Applies to every market in the backlog.

---

## 8. Sources and confidence

### Verified findings — primary, regulatory, case law, or first-party practitioner

**Rights, talent and licensing**
- SAG-AFTRA 2025 Commercials Contract MOA and Joint FAQs (term 1 Apr 2025 – 31 Mar 2028; MPU arithmetic; 13-week holding cycles) — https://www.sagaftra.org/sites/default/files/2025-05/2025%20Commercials%20Contract%20MOA.pdf · https://www.sagaftra.org/sites/default/files/sa_documents/2025%20Commercials%20Contracts%20Joint%20FAQs.pdf
- SAG-AFTRA Producer's Guide (agency-as-signatory liability) — https://www.sagaftra.org/sites/default/files/producers_guide_commercials_9_43_0.pdf
- SAG-AFTRA late payment penalties ("Notice is not the trigger") — https://www.sagaftra.org/what-are-penalties-if-my-check-paid-late · https://www.sagaftra.org/what-are-holding-fees
- *Olive v. General Nutrition Centers* — $213,000 + $910,000 = $1,123,000; Cal. Ct. App. 2d Dist., 27 Dec 2018, affirmed 31 Jan 2019 — https://www.lgt-law.com/blog/2019/01/models-11-million-jury-award-for-license-violation-upheld/ *(verified directly during this cycle)*
- *Beastie Boys v. Monster Energy* — $1.7M verdict + $667,849 fees — https://www.venable.com/insights/publications/2015/05/beastie-boys-win-17-million-verdict-underscoring-t
- Shutterstock license terms effective 19 Jan 2026 (numeric caps; non-transferability; indemnity caps) — https://www.shutterstock.com/license
- Adobe Fonts packaging prohibition — https://helpx.adobe.com/fonts/using/package-font-files.html
- 17 U.S.C. §504(c) statutory damages — https://www.law.cornell.edu/uscode/text/17/504
- Music sync term × territory × media practice — https://resilientmusic.com/usage-term-territory-media/

**Regulatory**
- FINRA Rule 2210 (principal approval; recordkeeping incl. first/last use, principal name, source of statistics) — https://www.finra.org/rules-guidance/rulebooks/finra-rules/2210
- FINRA Regulatory Notice 26-14 (proposed risk-based supervision; comment closes 11 Sept 2026 — **proposed, not effective**) — https://www.finra.org/rules-guidance/notices/26-14
- SEC Advisers Act Rule 204-2 recordkeeping (5 years, first 2 on-site) — https://www.ecfr.gov/current/title-17/chapter-II/part-275/section-275.204-2
- SEC Marketing Rule Risk Alert, 16 Dec 2025 (hyperlinked disclosures fail "clear and prominent") — https://www.sec.gov/files/exams-riskalert-mrkt-rule-2512-508.pdf
- SEC enforcement sweeps: 12 Apr 2024 ($200,000 / 5 advisers) — https://www.sec.gov/newsroom/press-releases/2024-46 · 9 Sept 2024 ($1,240,000 / 9 advisers) — https://www.sec.gov/newsroom/press-releases/2024-121
- FTC Endorsement Guides, 16 CFR Part 255 — §255.1(f) agency liability — https://www.ecfr.gov/current/title-16/chapter-I/subchapter-B/part-255
- FTC Consumer Reviews and Testimonials Rule, 16 CFR Part 465, effective 21 Oct 2024 — https://www.ecfr.gov/current/title-16/chapter-I/subchapter-D/part-465 · penalty $53,088/violation per 16 CFR 1.98 — https://www.ecfr.gov/current/title-16/chapter-I/subchapter-A/part-1/subpart-L/section-1.98
- FTC v. Nissan/TBWA Worldwide (agency named respondent, 2014) — https://www.ftc.gov/legal-library/browse/cases-proceedings/122-3010-tbwa-worldwide-inc-matter
- FDA OPDP untitled letters list — https://www.fda.gov/drugs/warning-letters-and-notice-violation-letters-pharmaceutical-companies/untitled-letters
- 21 CFR 314.81(b)(3)(i) Form FDA-2253 obligation — https://www.ecfr.gov/current/title-21/chapter-I/subchapter-D/part-314/subpart-B/section-314.81
- NAD/NARB Procedures revised effective 16 Mar 2026 (15-business-day response) — https://bbbprograms.org/getmedia/133fded6-5046-44de-a30e-f0890377480c/NAD-NARB-Procedures.pdf
- ADA Title II compliance date extension, DOJ interim final rule, 20 Apr 2026 → 26 Apr 2027 / 26 Apr 2028 — https://www.federalregister.gov/documents/2026/04/20/2026-07663/extension-of-compliance-dates-for-nondiscrimination-on-the-basis-of-disability-accessibility-of-web
- HHS Section 504 deadline extension, 7 May 2026 → 11 May 2027 / 10 May 2028 — https://www.hhs.gov/press-room/hhs-extends-mobile-and-web-accessibility-deadline.html *(verified directly during this cycle to resolve a conflict between research threads)*
- WCAG 2.2 (W3C Recommendation, updated 12 Dec 2024) — https://www.w3.org/TR/WCAG22/

**Technical specifications**
- IAB New Ad Portfolio fixed-size specs and weight caps — https://www.iab.com/wp-content/uploads/2019/04/IABNewAdPortfolio_LW_FixedSizeSpec.pdf
- Google Ads display specs — https://support.google.com/google-ads/answer/1722096
- DV360 CTV creative requirements (≥15 Mbps mezzanine; no duplicate frames; FreeWheel pre-approval) — https://support.google.com/displayvideo/answer/14175098
- LinkedIn ads guide — https://business.linkedin.com/advertise/ads/ads-guide
- TikTok in-feed ad specs — https://ads.tiktok.com/help/article/tiktok-auction-in-feed-ads
- Extreme Reach display and broadcast specs (12-character filenames; −24 LKFS) — https://helpcenter.xr.global/hc/en-us/articles/39719565197716-Digital-Ad-Serving-Display-Specifications · https://helpcenter.xr.global/hc/en-us/articles/5758928813332-North-America-Broadcast-Specifications-and-Requirements
- AICP file deliverable specifications — https://aicp.com/assets/editor/AICP_File_Deliverable_Specifications.pdf
- CBS Commercial Integration Manual 2024–2025 (deadline ladder; 80-day purge; caption-typo return) — https://www.paramount.com/files/documents/2024-2025%20CBS%20Commercial%20Integration%20Manual.pdf
- DMI/DPAA DOOH creative specs (25.00 fps) and programmatic latency — https://www.dmi-org.com/download/DMI_Standards_DOOH_Creative_Specs.pdf · http://dmi-org.com/downloads/DPAA-Programmatic-Technical-Specs-v.9.11.pdf
- Ghent Workgroup preflight compliance (14 variants, 260-file test suite) — https://gwg.org/ghent-pdf-preflight-compliancy/
- Total ink coverage limits — https://www.prepressure.com/design/basics/tic
- GA4 UTM reference and default channel group definitions — https://support.google.com/analytics/answer/10917952 · https://support.google.com/analytics/answer/9756891
- IAB/4A's Standard Terms & Conditions v3.0 — https://www.iab.com/wp-content/uploads/2015/06/IAB_4As-tsandcs-FINAL.pdf

**Practitioner and liability evidence**
- PolicyBee PI claim narratives (£21,995 phone-number error; ~£14,000 quoted / ~£9,000 settled corrupted-file reprint) — https://www.policybee.co.uk/blog/professional-indemnity-claims-examples · https://www.policybee.co.uk/blog/professional-indemnity-insurance-claims-the-case-of-the-corrupted-file
- With Jack (printer error, designer held responsible) — https://withjack.co.uk/printers-mistake-has-cost-thousands-of-pounds-help/
- Colleen Gratzer, "How to manage client revisions to design proofs" — https://creative-boost.com/how-to-manage-client-revisions-to-design-proofs/
- Creative COW, "Defining rounds of revisions" (Ned Miller, Todd Terry, Greg Ball, Rich Rubasch) — https://creativecow.net/forums/thread/defining-rounds-of-revisions/
- Peter Kang (Barrel), "8 ways client projects get delayed" — https://www.peterkang.com/8-ways-client-projects-get-delayed-and-how-to-avoid-them/
- Peter Bowerman on written sign-off and liability — https://wellfedwriter.com/your-typo-gets-printed-in-5000-brochures-what-do-you-do/
- AA vs PE (author's alteration / printer's error) — https://printwiki.org/Author's_Alteration
- C17 Media, "Why print files fail" (liability transfer to the file supplier) — https://c17media.com/why-print-files-fail/
- PrintPlanet thread: Acrobat's preflight is the callas pdfToolbox engine — https://printplanet.com/threads/pdftoolbox-alternatives.277624/
- AIGA Standard Form of Agreement, 2022 update (§1.6, §1.13, §3.4, §5, §9.1(c)) — https://www.aiga.org/sites/default/files/2023-11/Standardformofagreement_2022update.pdf
- Second Wind, "Agencies, Clients and Copyright Issues" — https://www.secondwindonline.com/library/public/powerpack/AgenciesClientsandCopyrightIssues.pdf
- Michael Janda on source files (the $40,000 release demand) — https://michaeljanda.com/blog/should-you-deliver-source-files-to-clients/
- Bill Hartzer on domain hostage; *DSPT International v. Nahum* (9th Cir. 2010), ~$152,000 — https://www.billhartzer.com/domain-names/when-developer-holds-domain-hostage/
- Meta partner removal is asset-by-asset — https://www.graphed.com/blog/how-to-remove-access-from-meta-business-suite
- Google Ads MCC single-owner model — https://support.google.com/google-ads/answer/7456532
- PPC Hero on account access and the withheld negative keyword list — https://ppchero.com/who-owns-your-ppc-ads-account/
- Ziflow ReviewAI announcement (change verification listed as future) — https://www.ziflow.com/blog/introducing-reviewai-more-efficient-reviews-powered-by-ai
- Filestage help: verifying feedback has been met (manual side-by-side) — https://help.filestage.io/en/articles/9113215-how-to-verify-that-everyone-s-feedback-has-been-met
- Verified-reviewer feature requests and complaints — https://www.capterra.com/p/162035/Filestage/reviews/ · https://www.trustradius.com/products/ziflow/reviews · https://www.g2.com/products/ziflow/reviews · https://www.capterra.com/p/178111/Ziflow/reviews/
- Vendor pricing pages (all fetched 8 Aug 2026): https://www.ziflow.com/pricing · https://filestage.io/pricing/ · https://frame.io/pricing · https://www.markup.io/pricing/ · https://bugherd.com/pricing · https://www.reviewstudio.com/pricing/ · https://approval.studio/pricing/ · https://pageproof.com/pricing/ · https://www.workamajig.com/pricing · https://www.productive.io/pricing/ · https://www.adobe.com/acrobat/pricing/business.html · https://www.enfocus.com/en/pitstop-pro/buy-now · https://agencyanalytics.com/pricing · https://www.swydo.com/pricing/ · https://dashthis.com/pricing/ · https://whatagraph.com/pricing · https://contentsnare.com/pricing/ · https://www.leadsie.com/pricing
- Veeva VPRAC agency certification, $500/person/yr — https://www.veeva.com/meet-veeva/partners/content/vprac/
- Aprimo's own published entry price (~$20,000/yr, "medium to large enterprises") — https://www.aprimo.com/blog/how-much-does-a-digital-asset-management-system-cost
- US patent application US20230010020A1, automated talent usage rights management — https://patents.google.com/patent/US20230010020A1/en

### Strong inferences — reasoned from verified inputs, not directly stated by a source

- **Constraint-family incompatibility, not spec count, is the binding problem** in outbound delivery (arithmetic over the verified specs; not a sourced statistic).
- **Failures split into loud and silent, and agencies only systematically defend against the loud ones.** Rejections and QC returns announce themselves; UTM misfiling, overprint-on-white, a wrong-version PDF and untagged PDFs do not. The silent class is where the money is.
- **Liability is contractually pushed onto the agency at every handoff** — trade printers, CBS's return-for-re-editing rule, DV360's "work directly with the publisher," SAG-AFTRA signatory status. The agency is the residual risk-holder by design.
- **Quote-gating functions as a small-agency exclusion mechanism**, independent of budget.
- **The agency assembles the compliance record but never owns the system of record**, and is the only party holding the whole picture with no tool for it.
- **The contracted round count (2) and the observed round count (3–5) differ**, and that delta is the mechanism behind the documented over-servicing figures.

### Tentative hypotheses requiring practitioner validation

- That agencies will actually maintain a rights register at the moment of licensing rather than at the moment of pain (**the largest risk in the report**).
- That the agency, rather than the advertiser, is the SAG signatory often enough for A3's buyer and victim to be the same party.
- That small agencies use shared spreadsheets for UTM taxonomy — strongly implied by Google's own guidance and by the absence of affordable tooling, but not directly evidenced here because practitioner forums were unreachable.
- That credential sharing is the SMB default — supported only by vendor framing and by the market existence of Leadsie (545,647 accounts connected, 202,827 clients onboarded since 2020) as circumstantial evidence.
- That an agency will act on an overage flag, given that 89% of surveyed practitioners report delaying or avoiding the conversation.

### Numbers deliberately excluded

- **"30–40% of print files are rejected before prepress intervention," "67% of print production errors trace to prepress," "$8.4 billion annual cost to the printing industry"** — uncited, published by a prepress outsourcing vendor. No credible industry-wide print rejection rate is published.
- **Ad platform creative rejection rates** — do not exist publicly. Meta's Integrity Reports cover organic enforcement, not ad disapprovals. Every circulating figure is content-farm output.
- **Ziflow's "90% of marketers say approval delays are the top reason for missed deadlines"** — attributed to "Simple.io research" that could not be located; the cited pages contain no such statistic.
- **Filestage's "$152,851.92/yr saved for a 15-person team"** — a self-derived figure from the vendor's own n=263 user survey, quoted to the cent.
- **MLR cost-per-asset ($2,500–$5,000) and cycle time (21 days, 3 rounds)** — vendor-published with no disclosed methodology, and explicitly rejected by practitioners in the field ("every single pharma company has different protocols… anything that groups all elements under one average is going to be implicitly incorrect").
- **Roughly a dozen AI-generated SEO domains** returning confident agency statistics with no methodology, sample, or source.

### Two corrections to guidance currently in circulation

1. **ADA Title II and HHS Section 504 web accessibility deadlines were both extended in spring 2026.** Any material citing April 2026 or May 2026 compliance dates is stale. The correct dates are 26 Apr 2027 / 26 Apr 2028 (Title II) and 11 May 2027 / 10 May 2028 (Section 504), both against **WCAG 2.1 AA** — not 2.2.
2. **The FTC Green Guides have not been substantively revised since 1 October 2012**, despite widespread assumption otherwise. Do not describe them as recently updated.

---

*Report produced 2026-08-08 · claim `31eace6d` · market "Marketing and creative agency account and production management" · angle `handoffs-and-qa`*
