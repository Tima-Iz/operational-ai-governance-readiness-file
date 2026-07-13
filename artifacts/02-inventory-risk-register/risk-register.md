# AI Risk Register — TalentSift Recruit at Modaretti S.p.A.

> **SIMULATION NOTICE.** Fictional risk register for a fictional case, created
> for portfolio and educational purposes. Not legal advice.

## How to read this register

- **Risk to people** (rights-holders: candidates, workers) is stated
  **separately** from **risk to the organisation** — they are different harms
  to different parties, and collapsing them is how rights-holders disappear
  from risk registers.
- **Scales:** Severity and Likelihood are High / Medium / Low. Severity is
  rated separately for people (P) and organisation (O); anchors: High = harm
  affecting livelihood/rights or major legal-financial-reputational damage;
  Medium = material but recoverable; Low = limited. Likelihood reflects the
  chance of the harm materialising on **current facts and controls**.
- **Residual risk** is rated on existing controls only; the "required
  controls" column is the plan, not the current state.
- **Legal mapping:** each required control cites the AI Act provision it
  serves. Deferred provisions (Annex III regime, from **2 Dec 2027**, orig.
  2 Aug 2026; PE-CONS 30/26, adopted final text — not yet in force) are
  marked ⏲; currently binding law is marked ●.
- **ISO/IEC 42001 thematic alignment — clause-level verification pending.**
  The required controls align thematically with ISO/IEC 42001:2023 (AI
  management systems: governance policies, impact assessment, data
  management, lifecycle and third-party controls, performance evaluation).
  Clause-level references were removed pending verification against an
  authorised copy of the standard (S-08). No formal conformity with, or
  certification against, the standard is implied.
- Labels per `methodology/evidence-rules.md`; evidence as EV-xx; unknowns as
  U-xx (assumptions register).

## Summary

| ID | Risk (short) | Sev P | Sev O | Lik | Residual | Owner | Status |
|---|---|---|---|---|---|---|---|
| R-01 | Discriminatory screening via inherited bias | High | High | Medium-High | **High** | HR Director | Open |
| R-02 | Model unvalidated for the Italian context | High | Medium | Medium-High | **High** | HR Ops Lead | Open |
| R-03 | Fully automated rejection without meaningful human involvement | High | High | High | **High** | HR Ops Lead | Open |
| R-04 | Candidates not informed of AI screening | Medium | High | High | **High** | DPO | Open |
| R-05 | Automation bias / ineffective oversight | Medium | Medium | High | **Medium-High** | HR Ops Lead | Open |
| R-06 | No override logging — oversight unverifiable | Medium | High | High | **High** | HR Ops Lead / Procurement | Open |
| R-07 | Parsing failures penalise atypical CVs | Medium | Medium | Medium | **Medium** | HR Ops Lead | Open |
| R-08 | Silent model updates — unassessed behaviour change | Medium | High | Medium | **Medium-High** | Procurement / HR Ops Lead | Open |
| R-09 | Vendor documentation inadequate for lawful deployment | Medium | High | High | **High** | Procurement | Open |
| R-10 | RSU and workers not informed | Medium | Medium | High | **Medium-High** | HR Director | Open |
| R-11 | DPIA pending — privacy risks unassessed | Medium | High | High | **High** | DPO | Open |
| R-12 | Retention period conflict (24/36 months/unseen schedule) | Low-Medium | Medium | High | **Medium** | DPO / Legal | Open |
| R-13 | Contract fails to allocate AI Act responsibilities | Low | High | High | **High** | Procurement / Legal | Open |
| R-14 | Availability weighting — indirect disparate impact | Medium-High | Medium | Medium | **Medium-High** | HR Ops Lead | Open |

## Governance outcome (2026-07-13, user decision) `[UD: D-015]`

**Posture: continue deployment only under conditions, with auto-rejection
paused.** The conditions:

1. **R-03 gate (immediate):** auto-archive may continue as *triage*, but **no
   rejection e-mail fires until a recruiter has reviewed the application and
   documented the decision** (interim logging per R-06's manual measure).
   Owner: HR Operations Lead.
2. **DPIA started now** (R-11), incorporating the Art. 22 analysis scoped in
   Artifact 1. Owner: DPO.
3. **Candidate privacy notice corrected within weeks** (R-04). Owner: DPO.
4. **RSU and affected workers informed within weeks** (R-10), after the
   Italian-law counsel check. Owner: HR Director.
5. **All vendor-dependent controls (R-01, R-02, R-06, R-08, R-09, R-13) are
   conditions of the October 2026 contract renewal**, assessed via the
   Artifact 4 questionnaire. Owner: Procurement.

*(The indicative "within weeks" timings above were subsequently fixed as
binding deadlines by the FRIA-Plus deployment decision, D-017: notice and
interim review procedure — 2 weeks; contestability route and DPIA — 6 weeks.
See FRIA-Plus §5 and the post-vendor update below for current control
status.)*

Rationale (from the Artifact 2 review): normal continuation ignores two
current-law exposures occurring at volume; full suspension is
disproportionate while a human genuinely decides, and an abrupt return to a
manual process the team cannot staff carries its own risks for applicants;
a pilot framing does not fit a system in full production for six months.
Rejected alternatives and consequences are recorded in the review of
2026-07-13 and re-examined in FRIA-Plus §5.

## Detailed entries

---

### R-01 — Discriminatory screening via bias inherited from historical hiring data

**Risk to people:** candidates from groups disadvantaged in past hiring
decisions (by gender, age, ethnicity, disability — directly or via proxies
such as career gaps, name-derived text features, postcode) receive
systematically lower scores and lose access to employment, at scale and
invisibly. `[AI from CF: EV-04 training data = 2019–2023 client hiring
outcomes]`
**Risk to organisation:** discrimination claims under EU/Italian
equal-treatment law; supervisory-authority attention; reputational damage;
Art. 10 non-compliance once the high-risk regime applies.
**Ratings:** Sev P High · Sev O High · Likelihood Medium-High.
**Existing controls:** vendor removes declared protected attributes at
parsing `[VC: EV-04]`; gender-only statistical-parity check, partly on
*inferred* gender `[CF: EV-04]`. No testing by age, ethnicity, disability, or
intersectionally `[EG]`.
**Required controls:** obtain disaggregated bias testing across protected
grounds and for the Italian applicant population (⏲ Art. 10(2)(f)–(g), Art. 13;
● GDPR Art. 5(1)(a) fairness); deployer-side outcome monitoring by band and demographic once
lawful basis for monitoring data is established (⏲ Art. 26(5); blocked today by U-09 — no applicant demographics).
**Residual risk: High.** **Owner:** HR Director. **Status:** Open — testing
demand goes into the October 2026 renewal (Artifact 4).
**Basis note `[UD: D-015]`:** the Medium-High likelihood rests on analyst
inference from the training-data design, not on observed local outcomes — no
outcome evidence exists either way, and that absence (vendor-withheld) is
itself part of the finding. Disaggregated vendor testing or deployer outcome
monitoring would confirm or revise this rating.

---

### R-02 — Model unvalidated for the Italian deployment context

**Risk to people:** Italian applicants are scored by a model trained on 81%
Netherlands/Belgium data with 3% Italian-language CVs `[CF: EV-04]`; parsing
and scoring quality for them is unproven, so error and exclusion may fall
disproportionately on the very population screened.
**Risk to organisation:** accuracy claims unreliable in production; poor
hires/rejections; ⏲ Art. 15 and Art. 26(4) exposure later.
**Ratings:** Sev P High · Sev O Medium · Likelihood Medium-High.
**Existing controls:** vendor's aggregate stability monitoring `[VC: EV-04]`;
"within acceptable internal thresholds" for Italian parsing — threshold
undisclosed `[VC/EG: EV-04]`.
**Required controls:** vendor validation report on Italian-language,
Italian-market data (⏲ Art. 15(3), Art. 13(3)(b)); deployer spot-check protocol: sample of scored CVs
re-reviewed by recruiters quarterly (⏲ Art. 26(5)).
**Residual risk: High.** **Owner:** HR Ops Lead. **Status:** Open.

---

### R-03 — Fully automated rejection without meaningful human involvement

**Risk to people:** ~31% of applicants per vacancy are rejected without any
human seeing their application (96 of 312, EV-06), with no notice, voice, or
contest route — loss of individual consideration for a livelihood decision.
`[CF: EV-01 §3, EV-06]`
**Risk to organisation:** **prima facie GDPR Art. 22 exposure (current law —
Artifact 1 C9, separate GDPR/DPIA assessment required)**; contradiction with
its own procedure's promises (EV-01 §1) is evidence of governance failure;
⏲ Art. 14/26(1)–(2) once applicable.
**Ratings:** Sev P High · Sev O High · Likelihood High (occurring now, at
volume).
**Existing controls:** recruiters *may* rescue red-band candidates within 14
days `[CF: EV-01 §3]` — in practice rarely exercised for store roles
`[CF: case-definition §3]`, so involvement is plausibly nominal.
**Required controls:** disable auto-archive or interpose documented human
review before any rejection takes effect (● GDPR Art. 22(3); ⏲ Art. 14,
26(2)); align EV-01 §1 wording with actual
practice, whichever direction is chosen.
**Residual risk: High.** **Owner:** HR Ops Lead. **Status:** **Gated by user
decision (D-015, Governance outcome §1):** auto-archive continues as triage
only; no rejection e-mail fires without a documented recruiter review. Action
A1 of Artifact 1; the register's top-priority entry together with R-11.

---

### R-04 — Candidates not informed that AI screening is used

**Risk to people:** candidates cannot exercise information, access, or
contestation rights they do not know they have; the "modern HR software"
notice `[CF: EV-01 §5]` conceals rather than informs.
**Risk to organisation:** ● GDPR Art. 13/14 transparency exposure now;
⏲ Art. 26(11) failure from Dec 2027; complaint-driven supervisory attention.
**Ratings:** Sev P Medium · Sev O High · Likelihood High.
**Existing controls:** none of substance `[EG]`.
**Required controls:** rewrite the candidate privacy notice — state that
automated screening is used, its logic in outline, its role in the decision,
and how to request human review (● GDPR Art. 13/14, 22(3); ⏲ Art. 26(11));
recruiter FAQ updated to match `[CF: EV-01 §5]`.
**Residual risk: High.** **Owner:** DPO. **Status:** Open — action A2.

---

### R-05 — Automation bias: recruiters over-trust the ranking

**Risk to people:** amber/green candidates are effectively pre-judged by the
score; recruiters anchored by bands and highlight phrases rubber-stamp the
model's view, so errors propagate unexamined.
**Risk to organisation:** the human-oversight defence it relies on (EV-01 §1)
is hollow in practice; ⏲ Art. 26(2) competence requirements unmet.
**Ratings:** Sev P Medium · Sev O Medium · Likelihood High.
**Existing controls:** one 45-minute onboarding webinar `[CF: EV-01 §6]`;
vendor materials that *encourage* trust ("scores reflect objective candidate
quality", EV-03 `[VC]`) — an anti-control.
**Required controls:** a proportionate **AI-literacy and oversight training
programme (● Art. 4 — applicable now; ⏲ Art. 26(2))** for HR staff,
recruiters, human reviewers, and system owners, covering: intended use and
system limits; automation bias; parsing failures; what meaningful human
review requires; escalation routes; override and decision documentation; and
candidate contestability (how to handle review requests). Delivered before
the D-017 review procedure goes live, refreshed annually, attendance
recorded. Plus periodic blind re-review of a scored sample to calibrate
trust. Effectiveness test: reviewers can articulate the system's failure
modes and their override authority in a spot-check; override rates are
non-zero and reasoned.
**Residual risk: Medium-High.** **Owner:** HR Ops Lead. **Status:** Open.

---

### R-06 — No override logging: human oversight is unverifiable

**Risk to people:** a candidate rescued or rejected against the ranking has
no record of who decided or why — no trail for remedy, no evidence for a
discrimination claim either way.
**Risk to organisation:** cannot demonstrate its central compliance claim
("human decided") to any authority, court, or auditor; ⏲ Art. 12/26(6)
log-integrity expectations unmet; contradicts the vendor's "full audit trail"
sales claim `[VC: EV-02]`.
**Ratings:** Sev P Medium · Sev O High · Likelihood High (structural).
**Existing controls:** system-event logs only (score produced, e-mail sent)
`[EG: no logging of human actions is described in EV-01 §3 or EV-03; later
confirmed by the vendor's log enumeration, EV-07 E2]`.
**Required controls:** vendor feature request/contract demand: log every
band move, rescue, and shortlist decision with user ID, timestamp, reason
field (⏲ Art. 12(1), 14(4), 26(6)); interim manual measure: recruiters record overrides in the ATS
notes field under a written instruction.
**Residual risk: High.** **Owner:** HR Ops Lead (interim) / Procurement
(vendor demand). **Status:** Open — renewal agenda item.

---

### R-07 — Parsing failures penalise atypical CV formats

**Risk to people:** candidates with unusual CV layouts, older formats, or
non-standard career narratives score low for machine-legibility reasons —
EV-06 row 98: auto-archived at 39 with "CV format not fully parsed;
availability not detected" `[CF]`. Plausibly correlated with age and origin.
**Risk to organisation:** loses genuine candidates in a tight labour market;
accuracy/robustness gap (⏲ Art. 15).
**Ratings:** Sev P Medium · Sev O Medium · Likelihood Medium.
**Existing controls:** none — parsing confidence is not surfaced as a reason
to route to human review `[EG]`.
**Required controls:** vendor: parsing-confidence flag routed to mandatory
human review instead of scoring-as-if-parsed (⏲ Art. 15, 14(4)(a));
deployer: treat "not fully parsed" highlights as an automatic rescue
trigger, documented (⏲ Art. 26(1)); **monitoring control
`[UD: D-015]`:** recruiters tally parse-failure highlight phrases monthly to
establish frequency.
**Residual risk: Medium.** **Owner:** HR Ops Lead. **Status:** Open.
**Evidence note `[UD: D-015]`:** this risk currently rests on a **single
observation** (EV-06 row 98). It is retained as a signal, rated accordingly;
the monitoring control exists to firm up or retire it.

---

### R-08 — Silent model updates change behaviour without assessment

**Risk to people:** the criteria by which candidates are judged can change
overnight, unexamined — fairness properties tested (however thinly) on v4.2
do not carry over automatically.
**Risk to organisation:** cannot maintain a stable compliance position over a
moving system (U-10); clause 10.1 permits change "at any time" `[CF: EV-05]`;
undermines any future reliance on Art. 111(2) (Artifact 1 §4.4 — updates are
not *automatically* significant design changes, but reliance requires a
documented per-update assessment that is impossible without notification).
**Ratings:** Sev P Medium · Sev O High · Likelihood Medium.
**Existing controls:** none — updates are automatic and unannounced
`[CF: EV-03 p.6]`.
**Required controls:** contractual change-notification duty: advance notice
of model updates with a change summary and re-validation statement (⏲ Art. 13,
15, 72); deployer version log + documented significance
assessment per update (⏲ Art. 26(5); Art. 111(2) prudence).
**Residual risk: Medium-High.** **Owner:** Procurement (contract) / HR Ops
Lead (log). **Status:** Open — renewal agenda item.
**Basis note `[UD: D-015]`:** the Medium likelihood is analyst judgment —
that updates *occur* is certain (EV-03), but whether any given update
materially changes behaviour is unobservable without the notification
mechanism this entry demands. A change-notification clause converts this
from judgment to evidence.

---

### R-09 — Vendor documentation inadequate for lawful deployment

**Risk to people:** indirect but foundational — every people-facing safeguard
(oversight, accuracy, bias) depends on documentation the deployer does not
have.
**Risk to organisation:** structurally unable to meet ⏲ Art. 26(1) (use per
instructions that do not exist in substance — EV-03 is a marketing-register
onboarding guide); cannot evaluate vendor performance claims (the marketed
"92% accuracy" is not independently interpretable — task, dataset, threshold
and model version undisclosed, U-01);
paying for a compliance posture ("EU AI Act ready" `[VC: EV-02]`) it cannot
verify (fuller documentation gated behind Enterprise NDA `[CF: EV-04,
EV-05 §3]`).
**Ratings:** Sev P Medium · Sev O High · Likelihood High (present state).
**Existing controls:** one-page validation summary obtained on request
`[CF: EV-04]`.
**Required controls:** demand Art. 13(3)-grade instructions for use —
characteristics, accuracy metrics and their meaning, limitations, foreseeable
misuse, oversight measures, maintenance (⏲ Art. 13);
make provision of the extended documentation pack a renewal condition rather
than an Enterprise upsell (Artifact 4 is the instrument).
**Residual risk: High.** **Owner:** Procurement. **Status:** Open.

---

### R-10 — RSU and workers not informed of the system

**Risk to people (workers):** the RSU `[CF: case-definition §1; D-009]` and
affected workers were never informed or consulted `[CF: EV-05 §3]` —
collective information rights bypassed; recruiters themselves were never told
what the system's limits are (see R-05).
**Risk to organisation:** ⏲ Art. 26(7) failure from Dec 2027 if uncured;
**possible current duties under Italian law (Transparency Decree, d.lgs.
104/2022) — [unverified], priority referral to Italian employment counsel
(Artifact 1 §6.4)**; labour-relations conflict when the RSU learns of the
system from workers or press rather than management.
**Ratings:** Sev P Medium · Sev O Medium · Likelihood High (the omission is a
present fact).
**Existing controls:** none `[EG]`.
**Required controls:** inform the RSU and affected workers now — system,
purpose, role in decisions, safeguards (⏲ Art. 26(7); ● Italian law
[unverified]); verify Italian-law duties with
counsel before framing the communication (● — referral).
**Residual risk: Medium-High.** **Owner:** HR Director. **Status:** Open —
action A3.

---

### R-11 — DPIA pending: privacy risks unassessed on a live system

**Risk to people:** the processing has run since January 2026 with no
systematic assessment of its risks to candidates — the safeguards that a
DPIA would have forced (notice, minimisation, Art. 22 analysis) are the ones
now missing.
**Risk to organisation:** ● GDPR Art. 35 exposure — large-scale evaluation/
profiling of natural persons is a textbook DPIA trigger; the DPO flagged it in
December 2025 and it remained unscheduled `[CF: EV-05 §3; U-05]`.
**Ratings:** Sev P Medium · Sev O High · Likelihood High.
**Existing controls:** GDPR Art. 28 DPA with the processor is signed
`[CF: EV-05 §1]` — necessary, not sufficient.
**Required controls:** conduct the DPIA now, incorporating the full Art. 22
analysis Artifact 1 scoped (gateways, safeguards, legal basis, meaningfulness
of human involvement) (● Art. 35, 22); track
outcomes into this register and the FRIA-Plus (Artifact 3).
**Residual risk: High.** **Owner:** DPO. **Status:** Open — action A2;
top-priority with R-03.

---

### R-12 — Retention-period conflict for candidate data

**Risk to people:** rejected candidates' data may be held longer than lawful
or expected — 24 months per vendor guide `[CF: EV-03]`, 36 months per
contract clause 7.2 `[CF: EV-05]`, and an unseen internal "Legal retention
schedule" `[CF: EV-01 §7]` (U-04). Which applies in practice is unknown.
**Risk to organisation:** ● GDPR Art. 5(1)(e) storage limitation; inability
to answer a simple candidate request accurately.
**Ratings:** Sev P Low-Medium · Sev O Medium · Likelihood High (the
inconsistency is certain; the harm depends on actual practice).
**Existing controls:** contradictory paperwork only.
**Required controls:** reconcile the three sources, fix one period with a
justification, instruct the vendor in writing per clause 7.2's mechanism, and
verify deletion actually runs (● GDPR Art. 5(1)(e), 28).
**Residual risk: Medium.** **Owner:** DPO / Legal. **Status:** Open.

---

### R-13 — Contract fails to allocate AI Act responsibilities

**Risk to people:** indirect — when responsibility is unallocated, safeguards
fall between two organisations.
**Risk to organisation:** clause 9.3 pushes all employment-law compliance to
Modaretti while the vendor controls the model `[CF: EV-05]`; audit rights are
substitutable by a vendor-written summary (clause 13.2); liability capped at
12 months' fees (clause 11.4); no clause addresses AI Act roles, Art. 13
documentation, change notification, or incident cooperation; the promised
"AI Act compliance pack" is roadmap vapour until delivered `[VC: EV-05 §3]`.
**Ratings:** Sev P Low · Sev O High · Likelihood High (the gap is the present
contract).
**Existing controls:** GDPR DPA (Art. 28) — covers data protection roles
only.
**Required controls:** renewal negotiation (Oct 2026): AI Act responsibility
matrix, Art. 13-grade documentation duty, change-notification clause,
genuine audit rights, incident-cooperation clause, and remedy/termination
rights tied to compliance failures (⏲ Art. 13, 25(4) written-agreement logic,
72–73). Artifact 4 supplies the
assessment instrument.
**Residual risk: High.** **Owner:** Procurement / Legal. **Status:** Open —
scheduled to renewal.

---

### R-14 — Availability weighting: indirect disparate impact

**Risk to people:** availability weighting set to "high" for store roles
`[CF: EV-01 §3]` systematically down-ranks candidates with caring
responsibilities, students, people with disabilities, and those with
religious observance constraints — EV-06 shows "no weekend availability
indicated" driving band placement. A facially neutral, deliberately chosen
parameter with a predictable skew (disproportionately affecting women in
caring roles). `[AI — Medium]`
**Risk to organisation:** indirect-discrimination exposure under
equal-treatment law (● — current law); undermines the "objective criteria"
narrative.
**Ratings:** Sev P Medium-High · Sev O Medium · Likelihood Medium.
**Existing controls:** none — the weighting was a scheduling-driven business
choice with no documented equality assessment `[EG]`.
**Required controls:** documented necessity/proportionality assessment of the
weighting (is "high" needed, or does "medium" fill shifts with less
exclusion?) (● equal-treatment law; ⏲ Art. 26(4) input relevance); feed into
FRIA-Plus necessity/proportionality section (Artifact 3).
**Residual risk: Medium-High.** **Owner:** HR Ops Lead. **Status:** Open.
**Basis note `[UD: D-015]`:** the Medium-High people-severity rests on
inference from the weighting choice and general evidence about who holds
availability constraints — Modaretti's applicant demographics are unknown
(U-09). A documented necessity/proportionality assessment with local data
would confirm or revise it.

---

## Register maintenance

Review cadence: monthly by owners until R-03/R-11 close, then quarterly;
full review at contract renewal (Oct 2026) and at Omnibus entry into force.
New risks enter with the next free ID; closures require evidence, not
intention. Cross-references: Artifact 1 actions A1–A6; FRIA-Plus (Artifact 3)
will absorb R-01, R-03, R-04, R-14 as rights-impact analyses; Artifact 4
operationalises R-06, R-08, R-09, R-13 as vendor questions.

---

## Post-vendor-response update (EV-07) `[UD: D-018]`

Short status update following the simulated vendor questionnaire response
(EV-07, Artifact 4). The entries above are unchanged; this section records
what EV-07 changes about their status.

**Vendor-dependent risk entries:**

| Risk | Status after EV-07 |
|---|---|
| R-01 (bias) | **Worse than assumed:** disaggregated testing refused outright (EV-07 B2); vendor's testing philosophy unchanged. Remains High; RC-1 unmet |
| R-02 (Italian validity) | **Worse:** no validation exists; offered only as a *paid* engagement (EV-07 C2). Remains High; RC-2 unmet |
| R-06 (override logging) | **Improved prospect:** system-native logging has a stated date (Q1 2027, EV-07 E1) — counts only once contractualised with the reason field and slippage remedies. RC-3 conditionally achievable |
| R-08 (silent updates) | **Confirmed as fact, no longer inference:** two undisclosed model updates occurred (v4.3 Mar 2026, v4.4 Jun 2026 — EV-07 G1); notification refused (G2). The R-08 basis note's uncertainty about *occurrence* is resolved — updates happen and are not notified; per-update harm remains unknown. RC-4 unmet |
| R-09 (documentation) | **Partly negotiable:** NDA documentation pack conceded (EV-07 A4), but Art. 13-grade instructions still do not exist (A1); compliance pack not yet delivered, due end Q3 2026 — an unresolved evidence dependency. RC-5 unmet as answered |
| R-13 (contract) | **Openings without movement:** responsibility annex "willing to discuss" (H1), audit substitution maintained (H2), service credits offered instead of remedies (H6). RC-6 unmet |

**Renewal-condition status (D-017):** RC-1 unmet · RC-2 unmet · RC-3
conditionally achievable · RC-4 unmet · RC-5 unmet as answered · RC-6 unmet.
Four of six unmet as answered — if unchanged at renewal, the D-017 exit rule
engages.

**Implications of the two undisclosed scoring updates (v4.3, v4.4):**
1. The two undisclosed scoring updates **create uncertainty about whether the
   validation evidence in EV-04 remains applicable to the current production
   version**. TalentSift must provide a documented change-impact assessment,
   version comparison and, where necessary, updated validation evidence.
   EV-04 is accordingly classified: **CURRENT APPLICABILITY NOT
   DEMONSTRATED** — not automatically invalid; the evidence does not
   establish whether the model changes were material.
2. The sample output in evidence (EV-06, 20 Feb 2026) reflects v4.2 scoring;
   whether v4.4 outputs differ materially is unknown.
3. Artifact 1 §4.4's version-management finding is now grounded in fact, not
   scenario: changes occur without the notification needed for any Art.
   111(2) significance assessment.
4. Monitoring table (Artifact 3 §6): the model-version row is active
   retroactively — Modaretti's version log should record v4.2→v4.3→v4.4 with
   a significance assessment attempted for each `[RE — owner: HR Ops Lead]`.

**Governance decision check:** EV-07 does not currently require changing the
selected governance option, **but it confirms material unresolved risks.
Option 2 remains defensible only if the immediate safeguards are implemented,
tested and evidenced. A documented deadline is not itself evidence that a
control is operating effectively.** `[AI — Medium-High]`

Control status as of 2026-07-13 — distinguishing **proposed → implemented →
tested → shown effective**:

| Immediate safeguard (D-017) | Status |
|---|---|
| Auto-rejection disabled | Directed with immediate effect; **implementation evidence (config record) not yet on file** |
| Documented human review before any adverse outcome | **Proposed** — procedure due within 2 weeks; not yet implemented, tested, or shown effective |
| Corrected candidate notice | **Proposed** — due within 2 weeks; not implemented |
| Contestability / human-review route | **Proposed** — due within 6 weeks; not implemented |
| Parse-failure automatic rescue | Directed; **operating evidence (first monthly tally) not yet available** |
| Override logging (interim, ATS notes) | Directed; **compliance rate unmeasured** |
| GDPR DPIA | **Not started** as of reference date; due within 6 weeks |

None of these may be described as a completed control until implementation
evidence exists and the effectiveness tests in FRIA-Plus §4 have been run.
What EV-07 changes is the *renewal outlook*: with four conditions unmet as
answered, the exit rule's restricted mode is the realistic default unless
negotiation moves the vendor. No reopening of FRIA-Plus is triggered before
the scheduled renewal reassessment. The decision itself remains the user's;
any change would be a new recorded decision.

---
**Version: 1.0 — FINAL** (2026-07-13; user review decisions D-015 applied;
post-vendor update appended per D-018).

*Fictional risk register for portfolio/educational purposes only. Not legal advice.*
