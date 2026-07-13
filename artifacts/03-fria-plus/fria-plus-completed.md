# Voluntary FRIA-Plus: Rights-Impact and Deployment Decision Assessment
## A thesis-derived, deployer-side extension of Article 27 FRIA for high-risk AI governance
### COMPLETED ASSESSMENT — TalentSift Recruit at Modaretti S.p.A.

> **SIMULATION NOTICE.** Fictional assessment of a fictional case, for
> portfolio and educational purposes. Not legal advice.

> **STATUS.** Modaretti is **not legally required** to perform an Art. 27
> FRIA: Art. 27(1) obliges only bodies governed by public law, private
> entities providing public services, and deployers under Annex III points
> 5(b)–(c) — a private retailer deploying an employment system is outside all
> three (Artifact 1 C7, verified against the enacted text and unchanged by
> PE-CONS 30/26 point (13)). **FRIA-Plus is a voluntary governance measure
> beyond minimum AI Act compliance**, derived from the author's MA thesis and
> informed by human rights due diligence. Its additional elements (marked ✚)
> are **not formal AI Act requirements**, and this is **not an official,
> certified, or legally recognised methodology**. Its purpose is to support a
> **defensible deployment decision** — not to claim legal conformity.

Assessor: portfolio author (AI-assisted) · Date: 2026-07-13 ·
**Version 1.0 — FINAL** (deployment decision D-017 recorded; user's targeted
corrections applied)
Inputs: frozen evidence pack v1.0 (EV-01–EV-06) · Artifact 1 v1.0 ·
Artifact 2 v1.0 · legal sources S-01–S-10 · decisions D-001–D-017.

---

## 1. Scope and deployment context

**System and intended purpose.** TalentSift Recruit v4.2: CV screening and
candidate ranking (0–100 score, colour bands, highlight phrases), intended by
the provider as decision support for recruitment `[CF: EV-02, EV-03, EV-06;
Artifact 1 §1]`. High-risk under Annex III 4(a) (Artifact 1 C3).

**Deployment context and affected process.** Modaretti S.p.A. (Italian
retail, ~2,800 employees), hiring for store and logistics roles; 30,000–
40,000 applications/year flow through the system since 12 January 2026
`[CF: case-definition §1; EV-05]`. Provider: TalentSift B.V. (NL). Deployer:
Modaretti (roles per Artifact 1 C4).

**Affected persons.** External job applicants (the overwhelming majority);
internal candidates applying through the portal are treated identically and
are not separately tracked `[EG — evidence silent; treated with applicants]`;
recruiters and hiring managers as system operators; the RSU and workforce as
collective stakeholders `[CF: case-definition §1; D-009]`.

**Assessment boundaries.** Covers the recruitment screening use only (the
sole use in evidence). Out of scope: any future workforce-management use
(would engage Annex III 4(b) and a new assessment); TalentSift's own
provider-side obligations except as they constrain Modaretti's controls.

**Evidence limitations.** Vendor evidence is thin and self-reported (EV-04 is
one page; methodology withheld — R-09); applicant demographics unknown
(U-09); actual override practice unlogged (R-06). Findings below distinguish
what is evidenced from what is plausible but unverified.

**Relationship with the GDPR DPIA.** The DPIA is **pending** (R-11; EV-05
§3). Art. 27(4), as amended by PE-CONS 30/26 point (13) (adopted final text —
not yet in force), lets a FRIA cross-reference the DPIA; this voluntary
assessment mirrors that: Section 3 findings feed the DPIA, and the DPIA's
Art. 22 analysis (scoped in Artifact 1 §6.4) will feed back into Section 5.
Neither document substitutes for the other.

**Why this assessment is voluntary.** Beyond the legal position above: the
deployment decides access to livelihoods for tens of thousands of people a
year on the basis of a system whose key properties its deployer cannot
currently verify. That is precisely the situation the thesis argues requires
rights-based due diligence *because* the law does not yet compel it — the
core demonstration of this portfolio `[UD: D-010]`.

---

## 2. Stakeholder and rights mapping

**Stakeholders.**

| Stakeholder | Stake | Current visibility into the system |
|---|---|---|
| Job applicants (~30–40k/yr) | Access to employment; fair, explicable treatment | None — told only "modern HR software" `[CF: EV-01 §5]` |
| Internal candidates | As applicants, plus workplace relationship | Same as applicants `[AS — evidence silent]` |
| Recruiters (4 FTE) | Workload relief; responsibility for decisions they may not control in substance | Scores, bands, highlights; no model documentation `[CF: EV-01 §4]` |
| Hiring managers | Quality of shortlists | Shortlist only, no scores `[CF: EV-01 §4]` |
| RSU / workforce | Collective information rights; precedent for algorithmic management | Not informed `[CF: EV-05 §3; D-009]` |
| Modaretti decision-makers (HR Director, DPO, Procurement) | Accountability for the deployment decision | Full internal visibility; no vendor transparency (R-09) |
| TalentSift B.V. | Revenue; controls the model, documentation, and logging capability | Full — the asymmetry this assessment works around |

**Rights impacts** (instrument: EU Charter, S-10 — *article numbers cited at
heading level; verify wording before publication*).

| Right | Potential impact on these facts | Evidenced vs plausible |
|---|---|---|
| Equality / non-discrimination (Charter Art. 21) | Systematically lower scores for groups disadvantaged in the 2019–23 training outcomes; proxy features visible in outputs | **Pathway evidenced** (EV-04 training design; EV-06 proxies); **magnitude unverified** — no disaggregated testing exists (R-01) |
| Access to employment (Charter Art. 15(1)) | Rejection without human consideration for ~31% of applicants pre-gate | **Evidenced** (EV-06: 96/312 auto-archived; EV-01 §3) |
| Privacy / data protection (Charter Art. 7–8) | Solely-automated decision concerns; retention confusion; opaque processing | **Evidenced** as prima facie (Artifact 1 C9; R-12); breach question expressly open pending DPIA |
| Dignity and autonomy (Charter Art. 1) | Being judged by an unexplained score with no voice; rejection e-mail that conceals the process | **Plausible, unverified as experienced harm** — no candidate testimony in evidence; structural conditions for it are evidenced (EV-01 §5) |
| Transparency | Candidates cannot know AI was involved | **Evidenced** (EV-01 §5) |
| Meaningful human review | Red-band review "when volume allows… rarely"; review unlogged | **Evidenced** (case-definition §3; R-06) |
| Contestability and remedy (Charter Art. 47 by analogy — private context) | No route to challenge a score or request review exists | **Evidenced by absence** — no pathway appears in any evidence document `[EG]` |

---

## 3. Material rights-impact scenarios ✚ (selection from the risk register — not a repetition of it)

Six scenarios selected on materiality to rights-holders. Register risks not
carried into FRIA-Plus (R-05, R-10, R-11, R-12, R-13 and the organisational
faces of the rest) remain managed in Artifact 2.

### FR-01 — Automatic rejection without meaningful human review
**Affected:** **ANALYST ESTIMATE — not stated in any evidence document:**
roughly 9,200–12,300 applicants/yr, calculated as 30,000–40,000
applications/yr `[CF: case-definition §1]` × ~30.8% auto-archived on scoring
(96 of 312 in the single pipeline export in evidence, EV-06). Assumption: the
one-vacancy, one-date snapshot is representative across roles and seasons
`[AS]` — actual rates by role are unknown ·
**Pathway:** score <40 → auto-archive → templated rejection after 14 days;
recruiter review of the red folder rare `[CF: EV-01 §3; EV-06;
case-definition §3]` · **Risk link:** R-03 · **Harm:** loss of access to
employment and of any individual consideration (Charter 15(1), 1) ·
**Severity:** High — a categorical exclusion, not an inconvenience ·
**Scale:** the largest of any scenario · **Remediability:** Low — vacancies
fill; the lost opportunity does not return · **Likelihood:** Certain
(pre-gate, it was the operating design, not a risk) · **Existing controls:**
the **D-015 gate** (since 2026-07-13): auto-archive is triage only; no
rejection e-mail without documented recruiter review · **Weaknesses:** the
gate is days old, manual, and unverified in practice; documentation relies on
the interim ATS-notes workaround (R-06) · **Evidence gaps:** no data yet on
gate compliance; U-06 (actual review behaviour).

### FR-02 — Reproduction of historical hiring bias
**Affected:** applicants from groups under-selected in 2019–23 client
decisions; not identifiable individually — that is part of the harm ·
**Pathway:** model learns past shortlisting/hiring patterns (EV-04) →
proxies (career gaps, inferred language, non-EU education — EV-06) carry
group membership → scores reproduce and scale the pattern; deployer-chosen
availability weighting (R-14) compounds it for carers and students ·
**Risk link:** R-01, R-14 · **Harm:** indirect discrimination (Charter 21) ·
**Severity:** High · **Scale:** structural — affects every scored
application · **Remediability:** Low at individual level (harm invisible to
its victims); Medium at system level (retraining/reweighting possible) ·
**Likelihood:** **Unverifiable on current evidence — and per this
methodology, a severe impact is not discounted for unproven likelihood ✚;**
the vendor's own testing (gender only, ±5pp, partly inferred labels — EV-04)
is too weak to exclude it · **Existing controls:** attribute removal
`[VC: EV-04]`; gender parity check `[CF: EV-04]` · **Weaknesses:** proxies
remain untested; "bias-free by design" is marketing `[VC: EV-02]` ·
**Evidence gaps:** disaggregated testing (age, ethnicity, disability,
intersectional); U-02 (which features actually drive scores); U-09.

### FR-03 — Unproven performance for Italian applicants and subgroups
**Affected:** potentially all applicants scored by the model. The disclosed
validation evidence rests on training data that is 81% Netherlands/Belgium
with ~3% Italian-language CVs, and no Italy-specific validation results have
been provided `[CF: EV-04]` — so performance for Italian-language and
Italian-market applicants is undemonstrated in either direction; the vendor's
"within acceptable internal thresholds" is unverifiable `[VC: EV-04]` · **Pathway:** distribution shift →
elevated error for precisely this population → wrongful low scores →
rejection (via FR-01's mechanism) · **Risk link:** R-02, R-07 · **Harm:**
arbitrary exclusion (Charter 15(1)); compounds FR-02 where errors correlate
with subgroups · **Severity:** Medium-High · **Scale:** population-wide
exposure; realised harm unknown · **Remediability:** Medium — correctable by
validation and rescue routes · **Likelihood:** Unknown — the vendor's
"acceptable internal thresholds" claim is unverifiable `[VC: EV-04]`; one
parsing-failure rejection is documented (EV-06 row 98, single observation —
R-07 evidence note) · **Existing controls:** none beyond the D-015 gate
catching what a human notices · **Weaknesses:** recruiters have no parsing-
confidence signal to notice · **Evidence gaps:** Italian-market validation;
parse-failure frequency (monitoring control now running, D-015).

### FR-04 — No notice, explanation, or contest route for candidates
**Affected:** all applicants · **Pathway:** privacy notice conceals automated
screening (EV-01 §5) → candidates cannot request review, correct parsing
errors, or complain → errors and biases (FR-01–FR-03) go unchallenged and
invisible · **Risk link:** R-04 · **Harm:** transparency, dignity/autonomy,
and remedy (Charter 1, 47 by analogy); also disables the safeguards GDPR
already requires · **Severity:** Medium-High — a *gateway* harm that locks in
the others ✚ · **Scale:** all applicants · **Remediability:** High — entirely
within Modaretti's power, cheaply · **Likelihood:** Certain (present state) ·
**Existing controls:** none · **Weaknesses:** — · **Evidence gaps:** none;
this one is fully evidenced.

### FR-05 — Overrides and decisions untraceable
**Affected:** any candidate whose outcome involved human discretion — and
Modaretti itself when asked to prove its process · **Pathway:** system logs
only machine events `[EG: no logging of human actions is described in EV-01
§3 or EV-03; confirmed by the vendor's own log enumeration, EV-07 E2]` → no
record of who
overrode what, or why → review promised by the D-015 gate cannot be
evidenced; discrimination cannot be proven *or* disproven · **Risk link:**
R-06 · **Harm:** remedy and accountability (Charter 47 by analogy) ·
**Severity:** Medium · **Scale:** all human touchpoints · **Remediability:**
High prospectively; retrospectively, the absence of override and decision
logging **materially limits reconstruction, investigation, and individual
remedy** for the roughly five months of decisions since go-live ✚ ·
**Likelihood:** Certain (structural) ·
**Existing controls:** interim ATS-notes instruction (D-015) ·
**Weaknesses:** manual, unaudited, outside the system of record ·
**Evidence gaps:** compliance rate with the interim instruction.

### FR-06 — Unnotified model updates shift the basis of decisions
**Affected:** applicants scored under different model versions without anyone
knowing · **Pathway:** automatic updates `[CF: EV-03 p.6]` + contractual
right to modify at any time (clause 10.1, EV-05) → scoring behaviour changes
silently → validations, fairness checks, and this assessment silently expire ·
**Risk link:** R-08 · **Harm:** undermines every other safeguard; fairness
across time (identical candidates, different outcomes by version) ·
**Severity:** Medium · **Scale:** episodic but system-wide · **Remediability:**
Medium · **Likelihood:** updates certain; per-update harm unknown (R-08 basis
note) · **Existing controls:** none · **Weaknesses:** — · **Evidence gaps:**
update history since go-live; U-10.

---

## 4. Required actions and controls

Per scenario (owner · deadline · evidence of implementation · effectiveness
test · dependencies · escalation trigger):

| # | Interim safeguard (now) | Permanent control | Owner / deadline | Evidence of implementation | Effectiveness test | Vendor / contract dependency | Escalation or suspension trigger |
|---|---|---|---|---|---|---|---|
| FR-01 | **Auto-rejection disabled immediately (D-017)**; auto-archive remains triage only — no adverse outcome without documented review | Auto-rejection **retired for the current deployment and configuration (D-017)**; interim documented human-review procedure formalised **within 2 weeks**; system-enforced review workflow sought at renewal | HR Ops Lead / disable: **immediate**; procedure: 2 weeks; system-enforced: Oct 2026 | Config change record; written procedure; weekly report: rejections vs documented reviews | **100% of rejection e-mails preceded by a review record; monthly audit of a 5% sample for review substance** (time spent, reason stated) | System-enforced version needs TalentSift; contract amendment desirable | Any week <95% documented-review rate → suspend auto-archive entirely |
| FR-02 | Gate (a human sees what the model rejects); recruiter briefing on proxy patterns | Disaggregated bias testing (age, sex, ethnicity, disability; Italian population) as **renewal condition**; outcome monitoring by band once lawful basis established | HR Director / renewal Oct 2026; monitoring design by Dec 2026 | Vendor test report on file; monitoring protocol approved by DPO | Test report reproduces methodology (not conclusions only); monitoring detects a seeded synthetic disparity in dry-run ✚ | **High — vendor holds data and model**; contract amendment required | Vendor refuses testing at renewal → renewal condition unmet; D-017 exit rule applies (Section 5) |
| FR-03 | Parse-failure highlights = automatic rescue to human review (extends D-015 monitoring) | Italian-market validation report as **renewal condition**; parsing-confidence flag surfaced to recruiters | HR Ops Lead / rescue rule now; validation at renewal | Written rescue instruction; monthly parse-failure tally (running, D-015) | Zero auto-rejections carrying parse-failure phrases; tally trend reviewed quarterly | Validation and flag need TalentSift | Parse-failure rate >2% of applications without vendor fix → escalate to HR Director |
| FR-04 | Corrected privacy notice + FAQ | Notice + explanation of AI's role + named human-review request route + complaint pathway, integrated in the portal | DPO / notice: **within 2 weeks**; full contestability and human-review route: **within 6 weeks** (D-017) | Published notice; review-request mailbox live; FAQ updated | Test request processed end-to-end within 10 working days; candidate-facing text passes plain-language review | None — fully deployer-side | Missed deadline → HR Director informed; this control conditions continued deployment |
| FR-05 | Interim ATS-notes override log (D-015) | System-native override/decision logging (who, what, why, when) as **renewal condition** | HR Ops Lead / interim now; system-native at renewal | Instruction issued; monthly export of notes | Sampled overrides all have a note with a reason; reconciliation of notes vs outcome changes | **High — logging is a product feature** | Interim compliance <90% in monthly sample → recruiters retrained; repeat → gate tightened |
| FR-06 | Written request to vendor: update history since Jan 2026 + advance notice of next update | Contractual change-notification + re-validation duty per significant update; deployer version log with documented significance assessment (Artifact 1 §4.4) | Procurement / request now; clause at renewal | Vendor letter; version log opened | Every update in the log within 5 working days of deployment; each has a significance assessment | **Contract amendment required** | Unnotified material update discovered → reassessment reopened (Section 6) |

**Separation of controls:**
- **Modaretti can implement directly:** the gate and its audit (FR-01);
  notice, explanation, review route, complaints (FR-04); interim override log
  (FR-05); parse-failure rescue rule (FR-03 interim); version log (FR-06
  deployer side).
- **Requiring TalentSift:** disaggregated bias testing (FR-02);
  Italian-market validation and parsing-confidence flag (FR-03); system-native
  logging (FR-05); change notification and re-validation (FR-06);
  system-enforced review workflow (FR-01 permanent).
- **Cannot currently be adequately controlled ✚:** the *magnitude* of FR-02
  (bias) and FR-03 (Italian validity) — no deployer-side measure can
  substitute for vendor testing and validation, and no lawful demographic
  outcome-monitoring exists yet (U-09). Temporary continuation despite these
  two risks is defensible **not because they are time-boxed, but because of
  the conditions under which continuation occurs (D-017):** auto-rejection is
  disabled; every adverse outcome receives meaningful, documented human
  review; parsing failures are automatically rescued; candidate notice and
  contestability are implemented on fixed deadlines; outcome and subgroup
  monitoring are activated; and the unresolved risks carry a hard escalation
  deadline (October 2026) with an automatic consequence (the D-017 exit
  rule). Naming them is a design feature of this methodology, not an
  admission to hide.

---

## 5. Ethical Justification Record ✚

*Part of FRIA-Plus (thesis-derived); not a separate or official framework. In
prose by design — a numerical cost-benefit score would fabricate precision
these facts do not support.*

### Necessity

**The problem is real and evidenced:** 30–40k applications/yr against 4
central recruiters; 19-day average time-to-shortlist; need raised by the HR
Director in Oct 2025 `[CF: EV-05 §1]`. **The claimed benefit is not
evidenced:** "70% faster" and "92% accuracy" are marketing `[VC: EV-02]`;
no before/after measurement at Modaretti is in evidence `[EG]`.
**Alternatives:** temporary recruiter headcount and a competing tool were
considered but not formally evaluated `[CF: EV-05 §1]`; a **rule-based
knockout on declared form fields** (availability, right-to-work) is a less
intrusive, transparent, deterministic option for volume relief that was never
assessed `[AI — Medium]`. **Function-by-function:** *triage/ranking* at this
volume is defensibly necessary — some ordering mechanism is unavoidable and
a learned ranking is not obviously worse than an ad-hoc human skim, provided
its risks are controlled. ***Automatic rejection* is not necessary:** the
D-015 gate demonstrates the same volume relief is achievable with human
confirmation of every adverse outcome — the objective is achievable at lower
rights risk, which is the necessity test failed.

### Proportionality

**Benefits** accrue mainly to Modaretti (recruiter capacity) and partly to
high-scoring candidates (speed). **Harms** fall on the lowest-scored — which
includes, indistinguishably, the genuinely weakest applications *and* the
model's mistakes (parsing failures, unvalidated subgroups, inherited bias:
FR-01–FR-03). **The asymmetry is stark: the party carrying the residual risk
(candidates) receives the least benefit and has the least information.**
Safeguards materially change the balance: the gate converts categorical
exclusion into human-confirmed decisions; notice and review routes (FR-04)
give harm a path to surface; logging (FR-05) makes the human role provable.
**A less harmful configuration exists and is partly adopted:** gate +
corrected notice + parse-failure rescue + a re-examined availability
weighting (R-14 — its necessity assessment is itself outstanding). **Residual
risk is acceptable only under the D-017 conditions:** auto-rejection
disabled; documented, meaningful human review of every adverse outcome;
automatic parse-failure rescue; notice and contestability delivered on their
deadlines; monitoring active; and a hard escalation deadline for the
vendor-dependent evidence. Absent those conditions — or if the October 2026
renewal fails to deliver the evidence — the unverifiable bias magnitude
(FR-02) tips proportionality against continued use and the exit rule
applies.

### Contestability

On current facts the deployment fails almost every element: no notification
`[CF: EV-01 §5]`, no explanation of AI's role, no advertised access to a human
reviewer, no timeliness standard, review authority informal and unlogged
(FR-05), records not preserved for reconstruction, no complaint pathway in
evidence, accessibility never considered `[EG]`. The FR-04/FR-05 controls are
the build-out; their effectiveness tests (Section 4) are the acceptance
criteria. **Until the FR-04 controls are live, contestability is the weakest
pillar of this deployment.**

### Deployment options

| Option | Supporting reasons | Unresolved risks | Required conditions | Consequences: applicants | Consequences: Modaretti | Vendor dependencies |
|---|---|---|---|---|---|---|
| 1. Continue normal deployment | Volume problem is real; system operational | FR-01–FR-06 all unresolved; two current-law exposures (Artifact 1 C9, R-11) continue at volume | None imposed — that is the problem | ~10k/yr continue to be rejected unseen; no notice or remedy | Prima facie GDPR exposure persists; indefensible against the evidence it itself holds | None acknowledged |
| 2. **Continue only under specified conditions** | Preserves evidenced volume relief; harms concentrate in the automated leg, which the conditions remove; retains a **dated, enforceable route (the renewal conditions) to obtain the evidence that candidates' rights protection depends on** | FR-02/FR-03 magnitude unknown until renewal delivers testing; interim logging is manual | Section 4 deployer-side controls on their deadlines; renewal conditions contractualised in Oct 2026; monitoring per Section 6 | Human-confirmed decisions; notice and review route within weeks | Carries a defined, documented residual risk under strict conditions; must actually resource the review workload | Bias testing, validation, logging, change notice — all deadline-bound at renewal |
| 3. Limited pilot with enhanced monitoring | Honest response to unvalidated performance | Awkward fit: the system has run in full production for six months — a "pilot" restriction means *shrinking* live use (e.g. logistics roles only) | Scope restriction + all Option 2 conditions + intensified sampling | Fewer applicants exposed; two-track treatment raises its own fairness question | Loses most volume relief; renewal conditions remain enforceable | Same as Option 2 |
| 4. Pause / do not deploy | Only option that fully eliminates FR-01–FR-06 pending evidence | The recruitment-capacity problem returns immediately | Manual process resourced (~4 FTE insufficient; EV-05) | No algorithmic exposure; but an under-staffed manual process carries its own risks for applicants — slower handling and more arbitrary, unrecorded human skimming `[AI — Medium]` | 30–40k applications/yr handled manually with 4 central recruiters | None — that is its virtue |

### The four questions, answered explicitly

1. **Can automatic rejection be justified?** No — for the current deployment
   and configuration it fails the necessity test: the same volume relief is
   demonstrably achievable with human confirmation of every adverse outcome.
   **Auto-rejection is retired (D-017).** This is not a claim that it could
   never be reconsidered under any future circumstances: any proposed
   reintroduction would constitute a **new governance decision**, requiring
   new supporting evidence; a new or reopened FRIA-Plus; a revised DPIA; a
   renewed necessity and proportionality assessment; evidence of effective
   contestability and human oversight; and explicit approval by the
   responsible governance authority. **It must not return automatically
   following a vendor update or an improved test result.**
2. **Can the system continue operating before the vendor evidence gaps are
   resolved?** Conditionally yes — under Option 2 logic: the gaps (FR-02,
   FR-03) are severe but their exposure is materially reduced by the D-017
   conditions (auto-rejection disabled, meaningful review, rescue, notice,
   monitoring), *and* they carry a hard deadline (October 2026 renewal). If
   the renewal does not deliver the evidence, **the D-017 exit rule applies**
   (see Decision below).
3. **Which controls are mandatory before continued use?** The deployer-side
   set, on the D-017 deadlines: auto-rejection disabled (immediate); interim
   documented human-review procedure (2 weeks); corrected candidate notice
   (2 weeks); full contestability and human-review route (6 weeks); interim
   override logging (FR-05, immediate instruction); parse-failure rescue rule
   (FR-03, immediate); completion of the GDPR DPIA (R-11 — within 6 weeks,
   with interim safeguards operating immediately).
4. **Which unresolved issues become contract-renewal conditions?**
   Disaggregated bias testing (FR-02); Italian-market validation and
   parsing-confidence flag (FR-03); system-native override logging (FR-05);
   change-notification and re-validation duty (FR-06); Art. 13-grade
   documentation (R-09); genuine audit rights (R-13). Artifact 4 is the
   instrument.

### Decision

**Preliminary recommendation of the assessor: Option 2 — continue only under
specified conditions** — because it is the only option that simultaneously
(i) removes the element that fails the necessity test (auto-rejection),
(ii) retains a dated, enforceable route — the renewal conditions — to obtain
the evidence that candidates' rights protection depends on, and (iii) is
honest about what it cannot yet control, with a defined exit if the gaps
don't close. The reasons for not preferring Option 4 are rights-based, not
commercial: with auto-rejection disabled and meaningful human review
restored, the identified harm pathways are interrupted, while an abrupt
return to a manual process the team demonstrably cannot staff (EV-05 §1)
carries its own risks for applicants of slower and more arbitrary,
unrecorded screening. Option 1 is indefensible on the file's own evidence.

## FINAL DEPLOYMENT DECISION (USER, 2026-07-13) `[UD: D-017]`

**Option 2 — Continue only under specified conditions.**

**Meaning of "continued deployment":** TalentSift Recruit may be used **only
as decision support or triage**. No applicant may be rejected, archived, or
sent an adverse notification solely on the basis of the system output
without documented, meaningful human review.

**Auto-rejection policy:** auto-rejection is **retired for the current
deployment and configuration**. Any proposed reintroduction constitutes a
new governance decision subject to the six requirements stated in answer 1
above; it must not return automatically following a vendor update or an
improved test result.

**Implementation deadlines (D-017):** disable auto-rejection — immediate ·
interim documented human-review procedure — 2 weeks · corrected candidate
notice — 2 weeks · full contestability and human-review route — 6 weeks ·
GDPR DPIA completed — 6 weeks, with interim safeguards operating
immediately.

**Exit rule (D-017):**
1. If the October 2026 renewal conditions are not met, use **automatically
   moves to a restricted, non-adverse decision-support mode with enhanced
   monitoring**.
2. If the system cannot operate safely and meaningfully in that restricted
   mode, or if material discrimination, validity, or parsing concerns remain
   uncontrolled, **deployment must be paused**.
3. Any continuation beyond that point requires a **new documented decision**,
   not an informal extension.

---

## 6. Monitoring and reopening ✚

FRIA-Plus is an ongoing process; this assessment expires on its triggers, not
merely on its calendar.

| What | Metric | Owner | Cadence | Reopen / suspend threshold |
|---|---|---|---|---|
| Candidate outcomes | Rejections with documented review (gate compliance) | HR Ops Lead | Weekly | <95% any week → suspend auto-archive |
| Subgroup outcomes | Band distribution by demographic — **once lawful basis exists** (U-09; DPO-approved design) | HR Director / DPO | Quarterly (once live) | Material unexplained disparity → reopen FRIA-Plus |
| Overrides / human review | Override rate; notes completeness (sample) | HR Ops Lead | Monthly | Notes <90% → retrain; repeat → tighten gate |
| Complaints & appeals | Review requests received / resolved in 10 working days | DPO | Monthly | Any substantiated discrimination complaint → reopen |
| Parsing errors | Parse-failure highlight tally (D-015) | HR Ops Lead | Monthly | >2% of applications → escalate to vendor, rescue-audit |
| Model versions | Version log; significance assessment per update | HR Ops Lead | Per update | Unnotified material update discovered → reopen |
| Vendor notifications | Feature announcements (esp. emotion/video — Artifact 1 §3 trigger) | Procurement | Continuous | Any emotion-inference feature → **do not enable; Art. 5 assessment first** |
| Legal changes | Omnibus entry into force (OJ); Art. 6(5)-type guidance; Italian-law advice received | DPO | Continuous | Entry into force → re-run Artifact 1 timeline §7 |
| Scheduled reassessment | Full FRIA-Plus re-run | HR Director | At Oct 2026 renewal, then annually | Renewal conditions unmet → **automatic move to restricted, non-adverse decision-support mode with enhanced monitoring**; if that mode cannot operate safely and meaningfully, or material discrimination/validity/parsing concerns remain uncontrolled → **pause**; continuation beyond that only by a new documented decision (D-017 exit rule) |

## Sign-off

Assessor: portfolio author (AI-assisted) · Reviewer: pending
(`methodology/review-checklist.md`) · **Decision-maker: the user — Option 2
recorded 2026-07-13 (D-017)** · Next reassessment: October 2026 (contract
renewal).

---
*Fictional assessment for portfolio/educational purposes. FRIA-Plus is a
thesis-derived voluntary methodology, not an official or legally required
instrument. Not legal advice.*
