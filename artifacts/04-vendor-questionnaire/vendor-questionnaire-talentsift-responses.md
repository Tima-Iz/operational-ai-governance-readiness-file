# EV-07 — Vendor Questionnaire: TalentSift's Responses and Modaretti's Assessment
## Completed instrument (fictional), October 2026 renewal preparation

> **SIMULATION NOTICE.** Fictional document for portfolio/educational
> purposes. Not legal advice.

> **EVIDENCE STATUS — EV-07: Simulated Post-Freeze Vendor Questionnaire
> Response** `[UD: D-018]`. The vendor responses below are **new simulated
> evidence generated after the Version 1.0 evidence freeze**; they do **not
> amend or overwrite EV-01–EV-06**. Created per the project brief (D-001:
> "fill in TalentSift's fictional answers including red flags consistent with
> the case definition") and extrapolated strictly from the frozen pack's
> established vendor posture (EV-02–EV-05) — no new vendor facts beyond what
> those documents make plausible. Registered in
> `case/evidence/evidence-index.md`.

**Simulated post-assessment vendor response — exact date not material.** The
project's legal-status "as of" date remains **13 July 2026**.
Assessor: HR Ops Lead / DPO / Procurement (fictional roles) ·
Assessment scale: **Acceptable · Concern · RED FLAG** (red flag on a ★
question = the linked D-017 renewal condition is unmet as answered).

---

## A. Documentation and instructions for use (RC-5)

| # | TalentSift response (fictional, summarised) | Assessment |
|---|---|---|
| A1 ★ | "Please refer to the Getting Started Guide v3.2 (attached), which reflects our current documentation standard. A dedicated AI Act compliance pack, including expanded instructions for use, is planned for Q3 2026 and will be provided when released." *(The attached v3.2 is materially identical to EV-03.)* | **RED FLAG.** The Art. 13 content requested (limitations, misuse, metrics, oversight, maintenance) still does not exist. The promised compliance pack **has not yet been delivered and remains due by the end of Q3 2026** — not overdue as of the project's 13 July 2026 reference date, but an **unresolved evidence dependency**: RC-5 cannot be assessed as met on a promise (EV-05 §3). RC-5 unmet as answered |
| A2 | "Recruit is intended to support recruitment teams in identifying promising candidates efficiently. It is not intended to replace human decision-making." | Concern. No misuse statement; no boundary conditions (e.g. volumes, role types, languages) |
| A3 | "Threshold configuration reflects each customer's process preferences. Our customer success team advises during onboarding." | Concern. Configuration risk remains undocumented — the mechanism behind FR-01 is still treated as a preference |
| A4 | "As a renewal accommodation, we can extend the Enterprise documentation pack (model factsheet, validation methodology summary) to Modaretti under NDA at no additional cost." | Acceptable **with conditions** — a genuine concession; value depends on delivered content. Review against Art. 13/Annex IV expectations before crediting RC-5 |
| A5 | Pages 3–4 supplied: pipeline-view and e-mail template screenshots. | Acceptable. Closes U-07 — nothing material was omitted |

## B. Training data and bias testing (RC-1)

| # | TalentSift response (fictional, summarised) | Assessment |
|---|---|---|
| B1 | Confirms EV-04 composition (2019–23, ~2.1M applications, 38 organisations; 81% NL/BE; logistics 54%/retail 31%/services 15%; progression-outcome label). | Acceptable as confirmation — the composition itself remains the RC-2 problem |
| B2 ★ | "Protected attributes are excluded at parsing. Our standard fairness assurance covers gender parity (±5pp at the green threshold). Further disaggregated analyses form part of our proprietary methodology and are available to Enterprise customers under NDA; we do not produce customer-specific fairness studies." | **RED FLAG.** Refuses disaggregated testing; re-offers attribute removal as a substitute for measurement — the exact position that created FR-02. RC-1 unmet as answered |
| B3 ★ | "Top-level feature families (experience relevance, tenure patterns, availability match, skills alignment) can be shared under the NDA pack. Feature-level detail is proprietary." | Concern. Family-level is progress but cannot answer whether career gaps, language inference, commute distance, or education origin drive scores (U-02 stays open) |
| B4 | "Removing protected attributes at source prevents the model from using them. We additionally monitor gender parity as described." | Concern. Proxy discrimination unaddressed as a concept — testing philosophy has not moved since EV-04 |
| B5 | "Aggregated, anonymised interaction data may be used for model improvement under clause 10.1. Customers may opt out in writing; opt-out does not affect service quality." | Concern → action: exercise the written opt-out immediately and record it (closes U-03 going forward; historical use remains unclear) |
| B6 | "In the unlikely event of a confirmed issue, a model correction would be deployed to all customers in the next release cycle." | Concern. Candidates already scored are not contemplated at all (FR-02 remediability) |

## C. Accuracy and robustness evidence (RC-2)

| # | TalentSift response (fictional, summarised) | Assessment |
|---|---|---|
| C1 ★ | "The 92% figure derives from an internal 2024 benchmark of shortlist agreement with experienced recruiters on a curated sample; AUC 0.81 refers to holdout prediction of progression outcomes. The two measure different things and are both accurate in context." | **RED FLAG — inadequate substantiation, not a numerical contradiction.** The two figures are indeed different kinds of metric; the problem is that the 92% claim is **not independently interpretable or verifiable**, because the vendor has not disclosed: the prediction task; the outcome definition; the denominator; the evaluation dataset; class balance; the threshold used; confidence intervals; subgroup performance; or whether the result concerns the production model. A marketed headline figure that cannot be interpreted is a metric-transparency failure (Art. 13/15); the declared-metrics question (C5) becomes contractually essential |
| C2 ★ | "Recruit performs within our global quality thresholds across supported languages, including Italian. Market-specific validation studies are not part of our standard offering; we would consider a paid professional-services engagement." | **RED FLAG.** No Italian validation exists; the vendor proposes the customer *pay* to learn whether the product works on its population. RC-2 unmet as answered |
| C3 | "Parse completeness is monitored internally; tenant-level rates are not currently reported. A parse-quality indicator is under consideration for the 2027 roadmap." | Concern. No number, no date; Modaretti's own monthly tally (D-015) remains the only measurement |
| C4 | "The parser is tested against a broad corpus of real CVs and handles most common formats." | Concern. "Most common formats" concedes the atypical-CV exposure (EV-06 row 98) without quantifying it |
| C5 | "We would be open to including headline performance indicators in future documentation, format to be defined." | Concern. Non-committal; must be converted into a contractual annex at renewal |

## D. Human oversight support

| # | TalentSift response (fictional, summarised) | Assessment |
|---|---|---|
| D1 ★ | "A mandatory-review workflow step (adverse actions require a recorded reviewer confirmation) is available as part of the Enterprise workflow module. It can be enabled for Modaretti as part of a renewal package." | Concern, negotiable. **This is a vendor offering, not an existing control for Modaretti** — the current subscription is Professional (EV-05). Treat as a **proposed remediation** requiring, before it counts as a control: commercial and contractual agreement; configuration and implementation; testing; user training; and **evidence that adverse outcomes cannot bypass meaningful human review**. Priority renewal item, since D-017's operating mode depends on this capability |
| D2 | "Reviewers see the score, band, and highlight phrases, which summarise the model's assessment." | Concern. Highlights are the model's own advocacy, not disagreement-support (R-05); no confidence or parse-quality signal |
| D3 | Onboarding webinar deck supplied; no content on failure modes or automation bias. | Concern. Art. 4 (current law) literacy remains Modaretti's own task to build |
| D4 | "No emotion- or personality-inference features exist or are in development. We will inform customers of major new features through our release communications." | Acceptable **in substance**, weak on mechanism — "release communications" is not advance notice; fold into the G2 notification clause |

## E. Logging and record-keeping (RC-3)

| # | TalentSift response (fictional, summarised) | Assessment |
|---|---|---|
| E1 ★ | "User-action logging (candidate moves, restores, shortlist actions, with user ID and timestamp) is scheduled for general availability in Q1 2027. A reason-code field is under evaluation." | Concern, conditionally acceptable: a real feature with a real date, **but** it lands after renewal and before the Dec 2027 regime — contractualise the date, the reason field, and remedies for slippage. RC-3 conditionally met **only if contractualised** |
| E2 | Enumerates current logs: score events, band assignments, e-mail dispatch, exports; retained 12 months; export via support request. | Acceptable as disclosure — confirms the R-06 gap precisely; 12-month log retention itself needs review against Art. 26(6) |
| E3 | "End-to-end reconstruction is possible for system events. Human actions are reconstructable only from Q1 2027 onward." | Concern. Confirms FR-05: the pre-2027 record cannot support individual remedy |
| E4 | "Clause 7.2 (36 months) is operative; the guide's 24-month statement is outdated and will be corrected. We will implement a written instruction for a shorter period." | Acceptable. Resolves U-04/R-12 — action: DPO issues the written instruction and verifies deletion |

## F. Incident handling

| # | TalentSift response (fictional, summarised) | Assessment |
|---|---|---|
| F1 | "Service incidents are communicated per the status page and support SLA. Data incidents follow the DPA's notification terms." | Concern. Scoring-correctness/fairness anomalies fall between "service" and "data" — exactly the gap; needs a defined incident class in the contract |
| F2 | "No incidents affecting scoring correctness have occurred." | Concern. No definition of what would count; candour untestable (U-10 pattern) |
| F3 | "We expect to support customers' regulatory obligations as they take effect." | Concern. Non-committal; convert to a cooperation clause (Art. 73) at renewal |

## G. Post-market monitoring, updates, versioning (RC-4)

| # | TalentSift response (fictional, summarised) | Assessment |
|---|---|---|
| G1 ★ | Version list supplied: v4.2 (Nov 2025) → v4.3 (Mar 2026, "parser improvements") → v4.4 (Jun 2026, "scoring refinements"). No change summaries beyond these phrases. | Concern. **Two unnotified model changes occurred during this compliance file's own period** — confirming FR-06/U-10 in fact. The updates create uncertainty about whether EV-04's validation evidence (which describes v4.2) remains applicable to the production version: a documented change-impact assessment, version comparison and, where necessary, updated validation evidence is required |
| G2 ★ | "Continuous improvement is core to our SaaS model. Updates are applied seamlessly and do not require customer action. We do not offer per-update notifications, as this would fragment the customer experience." | **RED FLAG.** Direct refusal of the change-notification condition. RC-4 unmet as answered |
| G3 | "We are following the regulatory discussion on design changes and will align with guidance when available." | Concern. No support for the Art. 111(2) significance assessment (Artifact 1 §4.4); Modaretti's version log remains blind without G2 |
| G4 | "Model stability is monitored continuously on aggregate customer data by our ML team." | Concern. EV-04's sentence restated; no plan, thresholds, or deployer reporting |
| G5 | "Fairness metrics are reviewed as part of our annual model governance cycle." | Concern. Annual review vs multiple silent updates per year — the cadence mismatch is the risk |

## H. Contractual allocation and readiness (RC-6)

| # | TalentSift response (fictional, summarised) | Assessment |
|---|---|---|
| H1 ★ | "We are willing to discuss a responsibility annex as part of renewal, based on our standard allocation: TalentSift is responsible for the platform; customers are responsible for their use of it." | Concern. "Willing to discuss" plus a restatement of clause 9.3's philosophy — a starting position, not an offer. Draft annex to be tabled by Modaretti's Legal |
| H2 ★ | "Our audit provisions (clause 13.2) reflect industry standard practice and protect all customers' data. The annual summary report is prepared to a consistent methodology." | **RED FLAG.** Summary-report substitution maintained verbatim. RC-6 unmet as answered |
| H3 | "Recruit is designed with the AI Act's principles in mind, and our compliance pack will document alignment in detail." | Concern. The EV-02 slogan restated; nothing assessed, by no one, against no provision |
| H4 | "We are monitoring the harmonised standards work and will finalise our conformity approach when standards stabilise; an internal readiness plan is targeted for H1 2027." | Concern. "Waiting for standards" with a paper plan one year before the deadline; demand the plan as a renewal deliverable |
| H5 | "We will register our systems as and when the database obligations take effect." | Acceptable (minimal). Correct in law; no earlier commitment offered |
| H6 | "We could discuss service credits for documented delivery delays as part of the renewal package." | Concern. Service credits ≠ remedy/termination rights; the 12-month liability cap (clause 11.4) remains untouched |

---

## Renewal-condition scorecard (as answered — simulated post-assessment response)

| RC | Condition (D-017) | Verdict on responses | Basis |
|---|---|---|---|
| RC-1 | Disaggregated bias testing | **UNMET — red flag** | B2 refusal; B4 philosophy unchanged |
| RC-2 | Italian validation + parse flag | **UNMET — two red flags** | C2 (pay-to-validate), C1 (metric confusion); C3 no date |
| RC-3 | System-native override logging | **Conditionally achievable** | E1 real feature, Q1 2027 — contractualise date + reason field + remedies |
| RC-4 | Change notification + re-validation | **UNMET — red flag** | G2 refusal; G1 shows two silent updates already |
| RC-5 | Art. 13-grade documentation | **UNMET as answered; partially negotiable** | A1 red flag; A4 NDA-pack concession to be content-reviewed |
| RC-6 | Audit rights + responsibility allocation | **UNMET — red flag** | H2 refusal; H1/H6 openings exist |

**Six red flags total** (A1, B2, C1, C2, G2, H2), each consistent with the
vendor posture established in the frozen evidence (EV-02's marketing claims,
EV-04's NDA gating, EV-05's clause 13.2 and roadmap promise).

**Assessment for the renewal decision `[AI — High on the mapping; the
negotiation outcome is unknowable]`:** as answered, four of six renewal
conditions are unmet. If this position does not move materially in
negotiation, the **D-017 exit rule engages at renewal**: use moves
automatically to restricted, non-adverse decision-support mode with enhanced
monitoring, with pause as the next step. The genuine openings — D1 (a
mandatory-review workflow exists as a vendor offering, subject to the
remediation conditions stated there), E1 (logging has a date), A4
(documentation concession) — are where negotiation effort should
concentrate, because they are the capabilities the D-017 operating mode
actually depends on.

---
**Version: 1.0 — FINAL** (2026-07-13; user corrections applied, D-018).

*Fictional document for portfolio/educational purposes only. EV-07: simulated
post-freeze evidence per D-001/D-018; does not amend EV-01–EV-06. Not legal
advice.*
