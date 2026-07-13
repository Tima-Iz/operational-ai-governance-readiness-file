# AI Act Applicability & High-Risk Classification Assessment
## TalentSift Recruit at Modaretti S.p.A. — COMPLETED ASSESSMENT

> **SIMULATION NOTICE.** Fictional assessment of a fictional case, created for
> portfolio and educational purposes. Not legal advice. Claim labels and
> confidence levels per `methodology/evidence-rules.md`; evidence cited as
> EV-xx (frozen pack v1.0), legal sources as S-xx, assumptions A-xx, user
> decisions D-xx.

## 0. Document control

| Field | Entry |
|---|---|
| System assessed | TalentSift Recruit, scoring model v4.2 (CV screening and candidate ranking, SaaS) |
| Organisations covered | TalentSift B.V. (NL, vendor); Modaretti S.p.A. (IT, customer) |
| Assessor / date / version | Portfolio author (AI-assisted) / 2026-07-13 / **v1.0 — FINAL** (user corrections of 2026-07-13 applied, D-014) |
| Evidence relied on | case-definition v1.0; EV-01–EV-06 |
| Legal texts version | **Currently operative law:** Regulation (EU) 2024/1689 as enacted, provisions verified 2026-07-13 (S-01). **Amending act:** Digital Omnibus on AI, PE-CONS 30/26 — **ADOPTED FINAL TEXT — NOT YET IN FORCE; OFFICIAL JOURNAL PUBLICATION PENDING AS OF 13 JULY 2026** (S-04); provision-level content of points (13) Art. 27, (39) Art. 111, (40) Art. 113 verified 2026-07-13 against text extracted from the Council-register PDF. The adopted future application date for the Annex III high-risk regime is 2 December 2027 |
| Re-assessment triggers | Omnibus OJ publication; any TalentSift feature/model change; Art. 6(5)-type classification guidance; contract renewal (Oct 2026) |

---

## 1. System identification

TalentSift Recruit ingests CVs and application-form data, parses them with an
NLP component, and scores candidates 0–100 against a configurable job profile
using a gradient-boosted classifier trained on pooled 2019–2023 client hiring
outcomes (~2.1M applications, 81% Netherlands/Belgium) `[CF: EV-04]`. Outputs:
match score, ranked list, colour band (green ≥70 / amber 40–69 / red <40),
and auto-generated highlight phrases `[CF: EV-01 §2, EV-06]`.

**Intended purpose (Art. 3(12), assembled from all three required sources):**
the instructions for use frame Recruit as producing rankings recruiters can
"trust" (EV-03 p.1); promotional material states "your team takes it from
there... it never replaces them" (EV-02); the system's own export footer says
"final decisions rest with you" (EV-06). The stated intended purpose is
therefore **decision support for recruitment screening** `[AI, High]`. Actual
use at Modaretti diverges in one respect: red-band candidates are auto-archived
and auto-rejected after 14 days, with rare recruiter intervention
`[CF: EV-01 §3, EV-06; case-definition §3]` — a gap between intended purpose
and use that recurs throughout this assessment.

Modaretti classifies TalentSift at its **highest/critical vendor tier**
`[UD: D-012]`.

---

## 2. Step 1 — Is it an "AI system"? (Art. 3(1))

| Element | Finding | Evidence |
|---|---|---|
| Machine-based system | Yes — cloud SaaS | `[CF: EV-02, EV-03]` |
| Varying levels of autonomy | Yes — scores, ranks, archives, and schedules rejection e-mails without human involvement per item | `[CF: EV-01 §3, EV-06]` |
| Adaptiveness after deployment (indicative) | Present — "scoring models are updated periodically... applied automatically" | `[CF: EV-03 p.6]` |
| Infers from input to generate outputs | Yes — trained classifier producing predictions (scores) and recommendations (rankings, bands) from CV/form input | `[CF: EV-04]` |
| Outputs influence environments | Yes — outputs determine pipeline placement and trigger rejection workflows | `[CF: EV-01, EV-06]` |

**Conclusion:** TalentSift Recruit is an AI system under Art. 3(1) `[LS: S-01]`.
A learned statistical model inferring suitability predictions from candidate
data sits squarely inside the definition; no element is arguable on these
facts. The Commission guidelines on the AI system definition (S-07,
non-binding, [adoption details unverified]) would only matter for edge cases this
system does not present. **`[AI — Confidence: High]`**

---

## 3. Step 2 — Prohibited practices screen (Art. 5)

Art. 5 has applied since **2 Feb 2025** — this screen concerns current law
(L-02).

| Art. 5(1) | Applies? | Reasoning |
|---|---|---|
| (a) subliminal/manipulative techniques | No | The system evaluates candidates; it does not deploy techniques to distort anyone's behaviour `[CF: case-definition §2]` |
| (b) exploitation of vulnerabilities | No | No targeting of age/disability/social-economic vulnerability to distort behaviour; scoring disadvantage is assessed under Annex III and non-discrimination law instead, which is the correct frame `[AI, High]` |
| (c) social scoring | **No, with analysis** — see below | |
| (d) criminal risk prediction | No | Out of scope of the system's function |
| (e) facial-image scraping | No | No image processing `[CF: case-definition §2]` |
| (f) **emotion inference in workplace** | **No, with a trigger condition** — see below | |
| (g) biometric categorisation | No | No biometric data processed `[CF: case-definition §2]` |
| (h) real-time remote biometric ID | No | Not a law-enforcement system |

**(c) Social scoring.** Recruit evaluates natural persons based partly on
inferred or predicted personal characteristics (career-gap patterns, inferred
language proficiency — EV-06), which touches the first limb of Art. 5(1)(c)
`[LS: S-01]`. The prohibition, however, requires detrimental treatment in
social contexts **unrelated** to the data's original context, or treatment
disproportionate to the behaviour scored. Rejection for the vacancy applied to
is treatment *within* the same context, so the better view is that Art. 5(1)(c)
is not engaged. **`[AI — Confidence: Medium-High]`** — the reasoning would need
revisiting if scores were reused across purposes (e.g. shared between
employers or reused for unrelated vacancies). Whether TalentSift's pooled
model training constitutes such reuse is an open question a supervisory
authority could probe `[EG: no vendor statement on cross-customer score
reuse; U-03]`.

**(f) Emotion inference.** Not engaged: no video, audio, or psychometric
inputs, and no emotion-inference features in evidence `[CF: case-definition
§2; EV-02–EV-04]`. **`[AI — Confidence: High]`** **Trigger condition `[RE]`:**
if TalentSift adds video-interview or sentiment features (its roadmap is not
in evidence), deployment at Modaretti would risk a practice **prohibited
since Feb 2025**, not merely a deferred high-risk issue. Procurement should
subscribe to vendor feature announcements and gate any such feature (owner:
HR Operations Lead; see Artifact 4).

---

## 4. Step 3 — High-risk classification (Art. 6 + Annex III)

### 4.1 Annex I route (Art. 6(1))
Not engaged: standalone SaaS, not a safety component of an Annex I product
`[CF: case-definition §1]`. `[AI — High]`

### 4.2 Annex III route (Art. 6(2))
Annex III point 4(a) covers AI systems "intended to be used for the
recruitment or selection of natural persons, in particular... to analyse and
filter job applications, and to evaluate candidates" `[LS: S-01, verbatim]`.
Recruit's intended purpose — analysing, filtering, and ranking applications —
matches the enumerated examples word for word; no interpretive distance is
required. Point 4(b) (workforce management) is not engaged for the current
recruitment-only use. **Annex III 4(a) applies. `[AI — Confidence: High]`**

### 4.3 Derogation test (Art. 6(3))
The derogation fails on three independent grounds:

1. **Profiling carve-out (dispositive).** "Profiling" under AI Act Art. 3(52)
   carries the GDPR Art. 4(4) meaning: automated processing of personal data
   to *evaluate personal aspects* of a natural person, in particular to
   analyse or predict aspects concerning, among others, that person's
   **performance at work** `[LS: S-01, S-05]`. Not every candidate ranking is
   profiling — a system that merely ordered applicants by a single declared
   criterion (say, stated availability) would evaluate the application, not
   the person. Recruit does more: it is a learned classifier that **predicts
   a person's suitability and likely progression** from patterns across their
   personal data (work history, gaps, education, inferred language level —
   EV-04, EV-06), which is precisely the evaluation-and-prediction of
   work-performance aspects the definition enumerates. Recruit therefore
   performs profiling, and Art. 6(3) makes profiling systems always high-risk
   where Annex III applies `[LS: S-01]`. **`[AI — High]`**
2. **Threshold condition fails.** The derogation requires no significant risk
   to health, safety, or fundamental rights, "including by not materially
   influencing the outcome of decision making". Scores determine who is seen
   by a human at all (96 of 312 applicants auto-archived in one vacancy,
   EV-06); influence on outcomes is not merely material but, for the red band,
   near-total. **`[AI — High]`**
3. **No condition (a)–(d) fits.** Scoring is not a narrow procedural task (a);
   it precedes rather than improves a completed human activity (b); it is not
   pattern-detection over human decisions (c); and it exceeds a "preparatory
   task" (d) because for auto-archived candidates it *is* the assessment.
   **`[AI — High]`**

No Art. 6(4) derogation documentation or registration by TalentSift is in
evidence — consistent with the vendor not claiming the derogation, despite
marketing the product as "EU AI Act ready" `[VC: EV-02]` `[EG]`.

### 4.4 Legacy-system check (Art. 111(2)) — **the honest complication**
Art. 111(2): the Regulation applies to operators of high-risk systems placed
on the market or put into service **before 2 August 2026** "only if, as from
that date, those systems are subject to significant changes in their designs"
`[LS: S-01, verbatim]`. Model v4.2 was deployed to all customers in November
2025 `[CF: EV-04]` and Modaretti put it into service in January 2026
`[CF: EV-05]` — both before the (original) application date.

Three points, honestly stated:
- **The amended wording has been verified at provision level.** PE-CONS 30/26
  (**ADOPTED FINAL TEXT — NOT YET IN FORCE; OFFICIAL JOURNAL PUBLICATION
  PENDING AS OF 13 JULY 2026**), point (39), *replaces* Art. 111(2): the
  Regulation applies to operators of high-risk systems placed on the market
  or put into service before "the date of application of Chapter III referred
  to in Article 113" — i.e. **2 December 2027** for Annex III systems — "only
  if, as from that date, those systems are subject to significant changes in
  their designs" (public-authority systems: compliance by 2 Aug 2030). The
  recitals clarify the grace period operates per **type and model** placed on
  the market before that date, with the decisive criterion being a
  significant design change after it. Verified 2026-07-13 against the text
  extracted from the Council-register PDF `[LS: S-04]`. The currently
  operative law remains Regulation 2024/1689 as enacted.
- **Automatic model updates do not, by themselves, constitute a "significant
  change in design."** The term is undefined and a routine retraining or
  parameter update may well fall short of it. What the updates *do* create is
  a **material version-management risk**: TalentSift applies updates
  automatically and without notification (EV-03; clause 10.1, EV-05), so
  Modaretti currently has no mechanism to know when a change occurs, let
  alone assess its significance. Before Art. 111(2) could be relied on, each
  relevant update would need a **documented assessment** of whether it
  amounts to a significant design change — a capability neither party has
  today (U-10). **`[AI — Confidence: Medium]`** `[EG: no change-notification
  or version-assessment mechanism exists]`
- The prudent planning position for both parties is therefore to treat the
  high-risk regime as applying from **2 December 2027** and not to rely on
  Art. 111(2) absent that documented version-assessment capability. `[RE]`

**Classification conclusion: TalentSift Recruit is a high-risk AI system
(Art. 6(2) + Annex III 4(a)); the Art. 6(3) derogation is unavailable.
`[AI — Confidence: High]`**

---

## 5. Step 4 — Role determination (Art. 3(3), 3(4), Art. 25)

**TalentSift B.V. — provider.** It develops the system and places it on the
market under its own name and trademark, for payment `[CF: EV-02; A-02]`,
meeting every element of Art. 3(3) `[LS: S-01]`. SaaS delivery does not alter
this. **`[AI — High]`**

**Modaretti S.p.A. — deployer.** It uses the system under its authority in a
professional context (Art. 3(4)) `[CF: EV-01]`; the personal-use exception is
irrelevant. **`[AI — High]`**

**Art. 25 re-qualification of Modaretti — worked through:**
- 25(1)(a) name/trademark: No — the system runs under TalentSift branding
  `[CF: EV-01, EV-06]`.
- 25(1)(c) purpose modification making a non-high-risk system high-risk:
  **not the relevant route here** — the system is already high-risk on the
  provider's own intended purpose, so 25(1)(c) has nothing to operate on.
- **25(1)(b) substantial modification:** this route applies **only if
  Modaretti itself makes a substantial modification** within the Art. 3(23)
  meaning — a change *not foreseen* in the provider's conformity assessment
  that affects compliance or intended purpose. Using a **vendor-provided
  configuration option does not, by itself, make a deployer a provider**:
  the auto-archive feature and threshold settings are offered and documented
  by TalentSift in its instructions for use, which describe them as commonly
  enabled `[CF: EV-03 Step 3; EV-01 §3]` — foreseen changes par excellence.
  Modaretti therefore remains a deployer only. **`[AI — Confidence:
  Medium-High]`**

**Distinguish two different legal risks that this configuration creates —
neither of which is provider status:**
1. **Provider-status risk (Art. 25(1)(b))** would arise only from future
   unforeseen changes — e.g. if Modaretti integrated Recruit's scores into a
   downstream automated tool of its own, or repurposed the system beyond
   recruitment. Current facts show nothing of the kind. `[AI — High]`
2. **Deployer misuse / inadequate-oversight risk (Art. 26)** is the live
   issue: operating a decision-support tool ("it never replaces them", EV-02
   `[VC]`) as an automated rejection mechanism for ~30% of applicants sits in
   tension with the intended purpose and will be assessed under Art. 26(1)
   (use per instructions) and Art. 26(2) (effective human oversight) — as
   deployer non-compliance, not re-qualification. This is where the findings
   of Artifacts 2 and 3 attach. `[AI — Medium-High]`

---

## 6. Step 5 — Obligation mapping

### 6.1 TalentSift (provider) — high-risk obligations, applicable from 2 Dec 2027 (orig. 2 Aug 2026)

| Provision | Duty (short) | Readiness signal in evidence |
|---|---|---|
| Art. 9 | Risk management system across lifecycle | None in evidence `[EG]` |
| Art. 10 | Data governance: relevance, representativeness, bias examination of training data | EV-04 shows 81% Benelux data, 3% Italian CVs, gender-only fairness testing — materially short of Art. 10 discipline `[CF/EG]` |
| Art. 11 + Annex IV | Technical documentation | Withheld behind Enterprise NDA `[CF: EV-04, EV-05 §3]` `[EG]` |
| Art. 12 | Automatic event logging enabling traceability | No logging of human actions (overrides, rescues) is described in EV-01 §3 or EV-03; the audit trail appears limited to system events `[EG]` |
| Art. 13 | Instructions for use enabling deployer compliance: characteristics, accuracy incl. metrics, limitations, oversight measures, expected lifetime/maintenance | EV-03 (marketing-register onboarding guide) contains none of the required content — the single largest provider gap `[CF/EG]` |
| Art. 14 | Human oversight by design (effective, not nominal) | Auto-archive feature + "trust the ranking" framing (EV-03) design *against* oversight `[AI — Medium]` |
| Art. 15 | Accuracy, robustness, cybersecurity; declared accuracy metrics | The marketed "92% accuracy" `[VC: EV-02]` is not independently interpretable — prediction task, dataset, threshold, and applicable model version undisclosed (U-01); the AUC 0.81 in EV-04 is a different kind of metric and does not substantiate it; parsing failures visible in output (EV-06 row 98) |
| Art. 16–17 | Provider duties; quality management system | No QMS evidence `[EG]` |
| Art. 43 | Conformity assessment (internal control route available for Annex III 4) | None in evidence; "AI Act ready" is an unsubstantiated `[VC]` |
| Art. 49 | EU database registration | None in evidence `[EG: U-08]` |
| Art. 72–73 | Post-market monitoring; serious-incident reporting | "Performance monitored on aggregate data" `[VC: EV-04]`; no incident process in evidence |

### 6.2 Modaretti (deployer) — high-risk obligations, applicable from 2 Dec 2027 (orig. 2 Aug 2026)

| Provision | Duty (short) | Position on current facts |
|---|---|---|
| Art. 26(1) | Use per instructions for use | Structurally impaired: adequate instructions do not exist (EV-03) — a deployer cannot comply with instructions the provider never wrote `[AI — High]` |
| Art. 26(2) | Human oversight: competence, training, authority, support | One 45-minute webinar (EV-01 §6); red-band review "when volume allows" — falls short of any reasonable reading `[AI — High]` |
| Art. 26(4) | Input data relevance/representativeness (where deployer controls input) | Modaretti controls the application form and role-profile weightings; workable, undocumented `[AI — Medium]` |
| Art. 26(5) | Monitor operation; suspend on risk | No monitoring routine in evidence; no one would currently detect model drift or a silent update (U-10) `[EG]` |
| Art. 26(6) | Retain auto-generated logs ≥ 6 months | Logs exist but omit overrides; retention schedule unclear (U-04) `[EG]` |
| **Art. 26(7)** | Inform workers' representatives and affected workers **before** putting into service | Modaretti has an RSU `[CF: case-definition §1; D-009]` which was **not consulted** (`[CF: EV-05 §3]`). Deployment predates applicability; whether "before putting into service" bites for systems already in service at the application date is a transitional ambiguity `[Uncertainty]`. Prudent course: inform the RSU and workers now, not in 2027 `[RE]` |
| Art. 26(11) | Inform natural persons subject to the system | Candidates currently told only "modern HR software" `[CF: EV-01 §5]` — would fail Art. 26(11) outright `[AI — High]` |
| **Art. 27** | FRIA | **Not obliged.** Art. 27(1) covers bodies governed by public law, private entities providing public services, and deployers under Annex III points 5(b)–(c) only `[LS: S-01]`. A private retailer deploying an employment system is outside all three categories `[A-06]`. **`[AI — Confidence: High]`** This conclusion **survives the Digital Omnibus**: PE-CONS 30/26 point (13) amends only Art. 27(4)–(5) (DPIA cross-referencing; AI Office questionnaire template), leaving the 27(1) scope untouched — verified 2026-07-13 `[LS: S-04]`. Per `[UD: D-010]`, Artifact 3 presents FRIA-Plus as a **voluntary measure going beyond formal compliance** — the deliberate core of this portfolio. The amended 27(4) (FRIA may cross-reference the DPIA) is a design input for Artifact 3 |

### 6.3 Transparency duties (Art. 50)
- 50(1) (provider; systems interacting directly with natural persons): the
  better view is **not engaged** — candidates submit to a portal; the AI runs
  back-office and never converses with them. `[AI — Medium]` (If TalentSift
  adds a candidate-facing chatbot, this changes.)
- 50(2) synthetic-content marking, 50(3) emotion/biometric disclosure, 50(4)
  deepfakes/AI text: not engaged on current facts — rejection e-mails are
  templated, not AI-generated `[CF: EV-01 §3]`. `[AI — High]`
- Candidate-facing information duties therefore flow from **Art. 26(11) (from
  Dec 2027) and GDPR (now)** — not Art. 50. Verified against PE-CONS 30/26
  (adopted final text — not yet in force): Art. 50's substance is unchanged
  for present purposes (only Art. 50(7) is replaced), and a new Art. 111(4)
  requires providers of generative systems marketed before 2 Aug 2026 to
  comply with Art. 50(2) by 2 Dec 2026 — not engaged by this system (L-06,
  S-04).

### 6.4 What binds **today** (13 July 2026) — no deferral applies
1. **GDPR, in full** (L-09). The auto-rejection flow presents a **prima facie,
   high-priority Art. 22 exposure**: auto-archiving plus automatic rejection
   e-mails appears to be a decision based solely on automated processing with
   significant effect on candidates, and candidates are not told automated
   screening exists `[CF: EV-01 §3, §5]`. This assessment does **not** reach a
   breach conclusion — that requires a **separate GDPR/DPIA assessment**
   analysing: (i) the Art. 22(2) gateways, in particular whether automated
   screening is genuinely *necessary* for entering into the employment
   contract; (ii) whether Art. 22(3) safeguards (human intervention,
   expressing a point of view, contesting) exist in substance; (iii) the
   Art. 6 legal basis for the processing; and (iv) whether the recruiters'
   ability to rescue candidates is **genuinely meaningful human involvement**
   — exercised with authority, competence, and actual attention — or nominal,
   given that red-band review happens "when volume allows" (case-definition
   §3). **What can be said now: this is the sharpest current-law issue in the
   file, it is independent of the AI Act timeline, and it makes the pending
   DPIA (GDPR Art. 35; EV-05 §3, U-05) urgent. `[AI — Confidence: Medium-High
   as to prima facie exposure; breach question expressly not determined]`**
2. **AI Act Art. 5** — screened clean above, with the emotion-feature trigger
   condition (§3).
3. **AI Act Art. 4 (AI literacy)** — applicable since 2 Feb 2025: providers
   and deployers must take measures to ensure, to their best extent, a
   sufficient level of AI literacy of staff and other persons operating and
   using AI systems on their behalf, taking account of context and the
   persons affected `[LS: S-01, verified against the OJ text]`. A 45-minute
   onboarding webinar is a thin measure against that standard `[AI —
   Medium]`; see risk register R-05 for the required literacy control.
4. **Italian labour law [flagged, unverified]:** Italy's "Transparency Decree"
   (d.lgs. 104/2022, amending art. 1-bis of d.lgs. 152/1997) imposes
   information duties on employers using automated decision-making or
   monitoring systems in employment — plausibly applicable to this deployment
   **now**, including toward the RSU. Outside this project's verification
   perimeter; in a real engagement this goes to Italian employment counsel
   as a priority. `[EG/Uncertainty]`

---

## 7. Step 6 — Timeline determination

| Obligation set | Original date | Current position (2026-07-13) |
|---|---|---|
| GDPR (all) | 25 May 2018 | **Applies now** |
| AI Act Art. 5 prohibitions; Art. 4 literacy | 2 Feb 2025 | **Applies now** |
| Annex III high-risk regime (Art. 9–17, 25–27, 43, 49) | 2 Aug 2026 | **Deferred to 2 Dec 2027** — PE-CONS 30/26 point (40), verified verbatim: Chapter III sections 1–3 (except Art. 6(5)) apply from 2 Dec 2027 (Annex III) / 2 Aug 2028 (Annex I). **ADOPTED FINAL TEXT — NOT YET IN FORCE; OJ PUBLICATION PENDING AS OF 13 JULY 2026**; entry into force on the third day after publication (S-02–S-04). Operative law today remains Reg. 2024/1689 as enacted |
| Art. 50 transparency | 2 Aug 2026 | Verified against PE-CONS 30/26: substance unchanged for present purposes (50(7) replaced only); new Art. 111(4) sets 2 Dec 2026 for generative systems marketed before 2 Aug 2026 — not engaged on current facts |
| Art. 111(2) legacy carve-out | reference: 2 Aug 2026 | **Replaced by PE-CONS 30/26 point (39)** (verified): reference date becomes the Chapter III application date — 2 Dec 2027 for this system; "significant changes in their designs" test retained. Automatic updates are not automatically significant design changes but create a version-management risk; reliance requires a documented per-update assessment neither party can perform today `[RE]` |

**Why act in 2026 rather than wait for December 2027 `[AI/RE]`:** (i) the GDPR
Art. 22 exposure exists today; (ii) the contract renews in October 2026
(EV-05) — the only real procurement leverage before the deadline; (iii)
retrofitting oversight, logging, and documentation against a live system is
costlier than building it in; (iv) the deferral's own rationale (missing
standards and guidance) does not suspend the underlying fundamental-rights
risks, which are present now.

---

## 8. Conclusions, ambiguities, actions

### 8.1 Conclusions

| # | Determination | Basis | Confidence |
|---|---|---|---|
| C1 | Recruit is an AI system | Art. 3(1) | High |
| C2 | No prohibited practice; emotion-feature trigger documented | Art. 5(1)(a)–(h) | High (Medium-High on (c)) |
| C3 | High-risk: Annex III 4(a); derogation unavailable (profiling; material influence; no condition fits) | Art. 6(2), 6(3) | High |
| C4 | TalentSift = provider; Modaretti = deployer; no Art. 25 re-qualification on current facts | Art. 3(3), 3(4), 25(1) | High / Medium (25(1)(b)) |
| C5 | Provider obligations Art. 9–17, 43, 49, 72–73 from 2 Dec 2027; evidence shows material gaps on 10, 12, 13, 14, 15 | §6.1 | High |
| C6 | Deployer obligations Art. 26(1)–(11) from 2 Dec 2027; Art. 26(2), (7), (11) are the acute gaps | §6.2 | High |
| C7 | **Art. 27 FRIA not obligatory for Modaretti; FRIA-Plus proceeds as voluntary good practice** | Art. 27(1); D-010 | High |
| C8 | Art. 50 not engaged on current facts | Art. 50(1)–(4) | Medium-High |
| C9 | **Prima facie** GDPR Art. 22 exposure on the auto-rejection flow — high-priority adjacent-law issue; separate GDPR/DPIA assessment required before any breach conclusion | GDPR Art. 22 | Medium-High (as to prima facie exposure) |

### 8.2 Open ambiguities (deliberately left open)
1. What counts as a "significant change in design" under Art. 111(2) for
   continuously-updated SaaS — the amended text (PE-CONS 30/26 point (39),
   verified) retains the test and its recitals anchor the grace period to
   type-and-model, but the significance threshold itself remains undefined;
   resolution needs future guidance.
2. Whether aggregate deployer configuration (auto-archive) exceeds intended
   purpose — Art. 26(1) vs Art. 25(1)(b) boundary — would need counsel and
   possibly authority guidance.
3. Transitional operation of Art. 26(7) "before putting into service" for
   systems already in service on the application date.
4. Cross-customer profiling/pooled training vs Art. 5(1)(c) "unrelated
   context" if score reuse ever emerges (U-03).

### 8.3 Actions (carried into Artifacts 2–4)

| # | Actor | Action | Driver | Evidence |
|---|---|---|---|---|
| A1 | Modaretti HR Operations Lead | Disable auto-archive, or interpose documented human review before any rejection takes effect | Prima facie GDPR Art. 22 exposure (now); Art. 14/26 (later) | EV-01 §3, EV-06 |
| A2 | Modaretti DPO | Complete the pending DPIA, including a full Art. 22 analysis (gateways, safeguards, legal basis, meaningfulness of human involvement); fix the candidate privacy notice (drop "modern HR software", state automated screening, its logic, and contestation route) | GDPR Art. 35, 13/14, 22 | EV-05 §3, EV-01 §5 |
| A3 | Modaretti HR Director | Inform the RSU and affected workers about the system, ahead of any legal deadline | Art. 26(7) (forthcoming); Italian law [unverified]; D-009 | EV-05 §3 |
| A4 | Modaretti Procurement | Use the October 2026 renewal to demand Art. 13-grade documentation, bias testing beyond gender, change notification, and audit rights (Artifact 4 is the instrument) | Art. 13, 10, 15 readiness; clause 13.2 inadequacy | EV-05 |
| A5 | TalentSift (via Modaretti pressure) | Produce genuine instructions for use, declared accuracy metrics, and override-logging capability | Art. 13, 15, 12/14 | EV-03, EV-04 |
| A6 | Modaretti HR Operations Lead | Establish a monitoring routine (drift, update detection, override tracking) | Art. 26(5); U-10 | EV-03 p.6 |

### 8.4 Sign-off
Assessor: portfolio author (AI-assisted draft). Review: pending against
`methodology/review-checklist.md`. Re-assessment triggers: per §0.

---
*Fictional assessment for portfolio/educational purposes only. Not legal advice.*
