# Third-Party AI Vendor Assessment Questionnaire — TalentSift Recruit Renewal
## Deployer-side procurement instrument, October 2026 contract renewal

> **SIMULATION NOTICE.** Fictional instrument for a fictional case, created
> for portfolio and educational purposes. Not legal advice.

## Purpose and design

This questionnaire is **not generic**: every question exists to close an
evidence or contractual gap already identified in this compliance file
(Artifacts 1–3) and is traceable to it. It operationalises the renewal
conditions set by the FRIA-Plus decision `[UD: D-017]` and the risk register's
governance outcome `[UD: D-015]`. It is written from the deployer's
(Modaretti's) perspective for the October 2026 renewal negotiation.

**How to use.** Send as a written questionnaire with a response deadline
ahead of renewal negotiation; require answers in writing, attributable, and
attachable as a contract annex. Assess each answer against the **red-flag
column** — a red-flag answer on any question marked ★ (renewal condition)
means the corresponding D-017 renewal condition is unmet, engaging the exit
rule. Where the vendor cites confidentiality: the question asks for evidence
of *governance*, not source code; an NDA is acceptable, a refusal is not.

**Legal references.** Provisions of the Annex III high-risk regime apply from
**2 Dec 2027** (orig. 2 Aug 2026; PE-CONS 30/26, adopted final text — not yet
in force) — they are cited here as the standard the vendor must demonstrably
be approaching, and as contract content now. GDPR and Art. 5 AI Act apply
today. ISO/IEC 42001: thematic alignment only — clause-level verification
pending (see Artifact 2).

**Renewal conditions (D-017) this instrument tests:**
RC-1 disaggregated bias testing (FR-02/R-01) · RC-2 Italian-market validation
+ parsing-confidence flag (FR-03/R-02/R-07) · RC-3 system-native
override/decision logging (FR-05/R-06) · RC-4 change-notification and
re-validation duty (FR-06/R-08) · RC-5 Art. 13-grade documentation (R-09) ·
RC-6 genuine audit rights and AI Act responsibility allocation (R-13).

---

## A. Documentation and instructions for use — RC-5

| # | Question | Motivation | Red-flag answer looks like |
|---|---|---|---|
| A1 ★ | Provide the complete instructions for use for Recruit, covering: intended purpose, characteristics, capabilities and limitations, foreseeable misuse, accuracy metrics and their meaning, human oversight measures, and maintenance expectations. | Art. 13(3); R-09; EV-03 is a 6-page onboarding guide with none of this | "See the Getting Started Guide" / marketing PDF resubmitted |
| A2 | State the system's intended purpose in one paragraph, including what it must **not** be used for. | Art. 3(12), 13; Artifact 1 §1 divergence | No misuse statement; purpose described only in benefit language |
| A3 | Which document tells deployers how to configure thresholds/auto-workflows responsibly, and what risks each configuration carries? | Art. 13(3)(b); FR-01 arose from an undocumented feature | "Thresholds are customer preference"; no risk guidance |
| A4 | Provide the technical documentation summary (Annex IV level) you will make available to deployers, and under what terms. | Art. 11; R-09 | Everything Enterprise/NDA-gated with no committed scope or date |
| A5 | Identify the omitted content of your user documentation (e.g. pages 3–4 of the guide extract) and provide it. | EV-03 partial extract; U-07 | Refusal or silence |

## B. Training data and bias testing — RC-1

| # | Question | Motivation | Red-flag answer looks like |
|---|---|---|---|
| B1 | Describe the training data: sources, period, volumes, sector and geographic composition, and the label used. | Art. 10(2); EV-04 discloses this partially — confirm and complete | Refusal to confirm composition already partially disclosed |
| B2 ★ | Provide bias-testing results disaggregated by sex, age band, nationality/ethnic origin proxies, and disability where testable — with methodology, metrics, thresholds, and dates. | Art. 10(2)(f)–(g); FR-02; EV-04 tested gender only | Gender-only results restated; "protected attributes are removed" as a substitute for testing |
| B3 ★ | Which candidate features actually drive scores? Provide feature-importance documentation, specifically addressing career gaps, language inferences, commute distance, and education origin. | U-02; EV-06 proxies; Art. 13(3)(b) | "Proprietary" with no governance-level disclosure offered |
| B4 | How do you test for proxy discrimination (features correlated with protected characteristics), and what were the last results? | Art. 10(2)(f); FR-02 pathway | Attribute removal described as making proxy testing unnecessary |
| B5 | Was Modaretti's or other customers' production data used to retrain or tune models since 2023? Under what legal basis? | U-03; GDPR Art. 28; clause 10.1 | Evasive on whether customer data enters training |
| B6 | What remediation follows if disparate impact is found — for the model, and for candidates already scored? | Art. 10; FR-02 remediability | Model-only answer; affected candidates never addressed |

## C. Accuracy and robustness evidence — RC-2

| # | Question | Motivation | Red-flag answer looks like |
|---|---|---|---|
| C1 ★ | For the marketed "92% screening accuracy" figure, disclose: the prediction task, outcome definition, denominator, evaluation dataset, class balance, threshold, confidence intervals, subgroup performance, and whether it concerns the production model — and state its relationship to the reported holdout AUC 0.81. | U-01; EV-02 and EV-04 each present a figure that is not independently interpretable; Art. 15(3) declared metrics | Cannot define the 92% figure, or restates both numbers without the disclosures that would make either interpretable |
| C2 ★ | Provide validation results for Italian-language CVs and the Italian retail/logistics labour market, with sample sizes. | FR-03; EV-04: 3% Italian corpus, "acceptable internal thresholds" undisclosed | Restates "acceptable thresholds" without numbers |
| C3 ★ | What is the CV parsing failure/partial-parse rate, how is parse confidence measured, and will you surface a parse-confidence flag to recruiters? | FR-03/R-07; EV-06 row 98 | No failure-rate data; flag "not on roadmap" |
| C4 | How does scoring behave on atypical inputs (non-standard formats, career changers, long histories)? Provide robustness test results. | Art. 15(1); EV-06 row 98 highlights | Anecdote instead of testing |
| C5 | What accuracy metrics will you commit to declaring in the instructions for use, per Art. 13(3)(b)(ii)? | Art. 13, 15; R-09 | Refusal to declare any metric contractually |

## D. Human oversight support — supports the D-017 operating mode

| # | Question | Motivation | Red-flag answer looks like |
|---|---|---|---|
| D1 ★ | Can the workflow enforce that no adverse action (archive → rejection e-mail) executes without a recorded human review step? If not, when? | FR-01; D-017 operating mode; Art. 14(4) | "Human review is the customer's process responsibility" — pure procedural deflection |
| D2 | What information does the interface give reviewers to *disagree* with a score (e.g. parse quality, feature drivers, confidence)? | Art. 14(4)(a)–(d); R-05 automation bias | "Scores reflect objective candidate quality" register (EV-03) |
| D3 | Do your training materials address automation bias and known failure modes? Provide them. | Art. 14(4)(b), Art. 4 (applies now); R-05 | Marketing webinar only (EV-01 §6) |
| D4 | Confirm there are no current or roadmap features inferring emotion, personality, or affect from any input; commit to advance notice before any such feature. | Art. 5(1)(f) (applies now); Artifact 1 §3 trigger | Hedged answer; no notice commitment |

## E. Logging and record-keeping — RC-3

| # | Question | Motivation | Red-flag answer looks like |
|---|---|---|---|
| E1 ★ | Will you provide system-native logging of every human action on a candidate (band moves, rescues, shortlist decisions: who, what, when, stated reason)? Committed date? | FR-05/R-06; Art. 12, 14(4)(e), 26(6) | "On the roadmap" with no date; "full audit trail" claim (EV-02) restated without the feature |
| E2 | Enumerate the events currently auto-logged, retention of those logs, and deployer export access. | Art. 12(1), 26(6); EV-03 silence | Cannot enumerate own logging |
| E3 | Can logs reconstruct an individual candidate's outcome end-to-end (versions, scores, actions, notifications)? Demonstrate on a test case. | FR-05 remedy pathway; Art. 12 | Reconstruction impossible or requires vendor "investigation" |
| E4 | Reconcile the retention statements: 24 months (guide) vs 36 months (clause 7.2). Which is operative, and will you implement our written instruction? | R-12/U-04; GDPR Art. 5(1)(e), 28 | Cannot say which retention its own systems apply |

## F. Incident handling

| # | Question | Motivation | Red-flag answer looks like |
|---|---|---|---|
| F1 | Define your process and timelines for notifying deployers of malfunctions, scoring anomalies, or data incidents affecting candidates. | Art. 26(5), 73 readiness; GDPR Art. 33 | Support-ticket SLA presented as incident process |
| F2 | Has any incident affecting scoring correctness or fairness occurred since Jan 2026? Describe your disclosure standard. | R-08; U-10; candour test | "No incidents" with no definition of what would count |
| F3 | Will you contractually commit to cooperate in our serious-incident reporting once Art. 73 applies? | Art. 73; RC-6 | Refusal to pre-commit cooperation |

## G. Post-market monitoring, updates, and versioning — RC-4

| # | Question | Motivation | Red-flag answer looks like |
|---|---|---|---|
| G1 ★ | Provide the full model version history applied to our tenant since 12 Jan 2026, with change summaries. | FR-06/U-10; clause 10.1 | Cannot produce tenant-level version history |
| G2 ★ | Will you commit to advance notice of model/scoring changes, with a change summary and re-validation statement per significant update? | FR-06/R-08; Art. 72; Art. 111(2) significance assessment (Artifact 1 §4.4) | "Updates are seamless; no customer action needed" |
| G3 | Define what you treat as a "significant change in design" and how you will support our documented per-update significance assessment. | Art. 111(2) as amended (PE-CONS 30/26 pt 39, verified); Artifact 1 §4.4 | Concept unrecognised; no support offered |
| G4 | Describe your post-market monitoring plan (Art. 72 level): what you monitor, thresholds, and what deployers receive. | Art. 72; EV-04 "aggregate monitoring" claim | Aggregate-stability sentence restated without plan |
| G5 | How will fairness properties be re-verified after each model update? | FR-02 continuity; Art. 10, 72 | Fairness tested once historically, not per version |

## H. Contractual allocation and compliance readiness — RC-6

| # | Question | Motivation | Red-flag answer looks like |
|---|---|---|---|
| H1 ★ | Will you agree an AI Act responsibility matrix annex (provider vs deployer duties, per article), replacing the blanket customer-responsibility clause 9.3? | R-13; Art. 25(4) written-specification logic | Clause 9.3 defended as sufficient |
| H2 ★ | Will you amend clause 13.2 to genuine audit rights (right to conduct, not vendor-substitutable by a summary report), NDA acceptable? | R-13; RC-6 | Summary-report substitution maintained |
| H3 | Substantiate "EU AI Act ready" (your product sheet): what has been done, against which provisions, assessed by whom? | VC in EV-02; Artifact 1 C5 gaps | Restated slogan; only the "compliance pack planned Q3 2026" roadmap |
| H4 | State your conformity-assessment plan and timeline for 2 Dec 2027 (Art. 43 route, harmonised standards or common specifications you will rely on). | Art. 43; C5 | No plan; "waiting for standards" with no interim position |
| H5 | Confirm your intention and timeline to register Recruit in the EU database. | Art. 49; U-08 | Unfamiliar with the obligation |
| H6 | Will you commit that failure to deliver RC-1–RC-5 items by agreed dates gives Modaretti remedy and termination rights without penalty? | D-017 exit rule; R-13 liability cap | No remedy linkage; 12-month liability cap presented as the answer |

---

**38 questions; ★ = tied to a D-017 renewal condition.** Failure on any ★
question means the corresponding renewal condition is unmet; per the D-017
exit rule, use then moves automatically to restricted, non-adverse
decision-support mode with enhanced monitoring, with pause as the next step
if concerns remain uncontrolled.

---
**Version: 1.0 — FINAL** (2026-07-13; D-018).

*Fictional instrument for portfolio/educational purposes only. Not legal advice.*
