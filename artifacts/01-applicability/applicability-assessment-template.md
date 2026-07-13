# AI Act Applicability & High-Risk Classification Assessment — TEMPLATE

> **SIMULATION NOTICE.** This template is part of a fictional portfolio
> project. It is a working tool for structuring an assessment, not legal
> advice. Adapt it with qualified counsel before real-world use.

## How to use this template

Complete the steps **in order** — each step's conclusion gates the next. For
every conclusion: cite the specific article/paragraph/annex point, state the
reasoning in 2–4 sentences, assign a confidence level (High / Medium / Low),
and label the claim type per the project taxonomy (`[CF]` case fact, `[LS]`
external legal source, `[VC]` vendor claim, `[AI]` analyst interpretation,
`[AS]` assumption, `[EG]` evidence gap, `[RE]` recommendation, `[UD]` user
decision). Where the law is genuinely ambiguous, say so — do not pick the
convenient reading. Check the legal-status register for what is applicable
*today* versus later before phrasing any obligation as current.

---

## 0. Document control

| Field | Entry |
|---|---|
| System assessed | |
| Organisations covered | |
| Assessor / date / version | |
| Evidence relied on (IDs) | |
| Legal texts version (incl. pending amendments) | |
| Review date / re-assessment triggers | |

---

## 1. System identification

Describe, citing evidence: what the system does; inputs; outputs; who operates
it; who is affected by it; the **intended purpose as stated by the provider**
(Art. 3(12): drawn from instructions for use, promotional materials, and
technical documentation — collect all three, they may conflict); and the
deployment context. Note any gap between intended purpose and actual use.

---

## 2. Step 1 — Is it an "AI system"? (Art. 3(1))

Test each element of the definition against evidence:

| Element (Art. 3(1)) | Finding | Evidence |
|---|---|---|
| Machine-based system | | |
| Designed to operate with varying levels of autonomy | | |
| May exhibit adaptiveness after deployment *(indicative, not required)* | | |
| Infers, from input received, how to generate outputs (predictions, content, recommendations, decisions) | | |
| Outputs can influence physical or virtual environments | | |

*Guidance:* the inference element is the usual dividing line from ordinary
software; a system executing only human-defined rules with no learned or
inferred behaviour may fall outside. Consult the Commission guidelines on the
AI system definition (non-binding) for edge cases. **Conclusion + confidence:**

---

## 3. Step 2 — Prohibited practices screen (Art. 5)

Screen every Art. 5(1) practice, even the obviously inapplicable ones — the
value of the screen is the documented "no". For each: applicable / not
applicable, with one-line reasoning; expand where the answer is not obvious.

| Art. 5(1) | Practice (short) | Applies? | Reasoning |
|---|---|---|---|
| (a) | Subliminal / purposefully manipulative techniques | | |
| (b) | Exploitation of vulnerabilities (age, disability, social/economic situation) | | |
| (c) | Social scoring with detrimental treatment in unrelated contexts or disproportionate to the behaviour | | |
| (d) | Criminal-offence risk prediction based solely on profiling/personality | | |
| (e) | Untargeted facial-image scraping | | |
| (f) | **Emotion inference in workplace or education** (exc. medical/safety) | | |
| (g) | Biometric categorisation to deduce protected characteristics | | |
| (h) | Real-time remote biometric identification for law enforcement | | |

*Guidance for employment tools:* (f) is the live risk — video-interview
analytics, "engagement" scoring, or sentiment features cross the line. Also
record **trigger conditions**: planned vendor features that would change any
"no" to "yes". Art. 5 applies since **2 Feb 2025** — a prohibited practice is
not deferred by the high-risk timeline. **Conclusion + confidence:**

---

## 4. Step 3 — High-risk classification (Art. 6 + Annex III)

### 4.1 Annex I route (Art. 6(1))
Is the system a product/safety component under Annex I harmonisation
legislation requiring third-party conformity assessment? (For standalone
software tools this is usually No — document it anyway.)

### 4.2 Annex III route (Art. 6(2))
Identify the Annex III point(s) engaged and quote the operative language.
For employment: point 4(a) (recruitment/selection: targeted ads, analysing
and filtering applications, evaluating candidates) and 4(b) (decisions on
terms, promotion, termination, task allocation, monitoring/evaluation).
Match the system's **intended purpose** — not its marketing framing — to the
wording.

### 4.3 Derogation test (Art. 6(3))
Only reach this if an Annex III point is engaged. The derogation requires
**no significant risk** to health, safety, or fundamental rights (including by
not materially influencing decision outcomes), AND at least one of:

| Condition | Met? | Reasoning |
|---|---|---|
| (a) narrow procedural task | | |
| (b) improves the result of a previously completed human activity | | |
| (c) detects decision-making patterns/deviations, no replacement of or influence on human assessment without proper review | | |
| (d) preparatory task to an assessment | | |

**Profiling carve-out:** a system that performs profiling of natural persons
(GDPR Art. 4(4) meaning) is **always** high-risk when Annex III applies — the
derogation is unavailable. Test profiling first; it often disposes of the
derogation entirely. If a provider claims the derogation, it must document the
assessment and register the system (Art. 6(4)) — ask for that documentation.

### 4.4 Legacy-system check (Art. 111(2))
If the system was placed on the market / put into service **before the
high-risk application date**, the Regulation applies to its operators only if
the system undergoes **significant changes in design** after that date.
Document: when the system was placed on the market; when put into service by
this deployer; whether continuous updates/retraining make the carve-out
unstable. This is often decisive for real timelines — and often ambiguous;
say so.

**Classification conclusion + confidence:**

---

## 5. Step 4 — Role determination (Art. 3(3), 3(4), Art. 25)

For **each** organisation:

| Question | Finding |
|---|---|
| Does it develop the system, or have it developed, and place it on the market / put into service under its own name or trademark (Art. 3(3) provider)? | |
| Does it use the system under its authority in a professional context (Art. 3(4) deployer)? | |
| Art. 25(1)(a): has it put its name/trademark on an existing high-risk system? | |
| Art. 25(1)(b): has it made a **substantial modification** (Art. 3(23): change not foreseen in the provider's conformity assessment affecting compliance or purpose)? | |
| Art. 25(1)(c): has it modified the intended purpose so a non-high-risk system becomes high-risk? | |

*Guidance:* deployer configuration *within vendor-provided options* is
normally foreseen and therefore not a substantial modification — but assess
the **aggregate effect** of configuration against the stated intended purpose
(e.g. converting decision support into automated decisions). Record the
question even where the answer is "probably not"; this is a known grey zone.

---

## 6. Step 5 — Obligation mapping per role

### 6.1 Provider obligations (once high-risk rules apply)
Map each to evidence of readiness; note gaps:
Art. 9 (risk management system) · Art. 10 (data & data governance, incl. bias
examination) · Art. 11 + Annex IV (technical documentation) · Art. 12
(record-keeping/automatic logs) · Art. 13 (transparency & instructions for
use to deployers) · Art. 14 (human oversight by design) · Art. 15 (accuracy,
robustness, cybersecurity — incl. declared accuracy metrics) · Art. 16–17
(provider duties incl. quality management system) · Art. 43 (conformity
assessment) · Art. 49 (EU database registration) · Art. 72 (post-market
monitoring) · Art. 73 (serious-incident reporting).

### 6.2 Deployer obligations (once high-risk rules apply)
Art. 26(1) (use per instructions, technical/organisational measures) ·
Art. 26(2) (human oversight: competence, training, authority, support) ·
Art. 26(4) (input data relevance/representativeness where deployer controls
it) · Art. 26(5) (monitor operation; suspend on risk; report incidents) ·
Art. 26(6) (retain auto-generated logs ≥ 6 months) · **Art. 26(7)** (employers:
inform workers' representatives and affected workers **before** putting into
service at the workplace) · Art. 26(11) (inform natural persons subject to
decisions) · Art. 27 (FRIA — check 27(1) scope carefully: bodies governed by
public law, private providers of public services, and deployers under Annex
III points 5(b)–(c) only).

### 6.3 Transparency duties (Art. 50) — applies on its own timeline
50(1) direct interaction with natural persons (provider duty) · 50(2)
synthetic-content marking (provider) · 50(3) emotion recognition / biometric
categorisation disclosure (deployer) · 50(4) deepfakes/AI text (deployer).

### 6.4 Duties applicable now, regardless of the high-risk timeline
Art. 5 (since 2 Feb 2025) · Art. 4 AI literacy (since 2 Feb 2025) · **GDPR in
full** (esp. Art. 22 automated decisions, Art. 13/14 transparency, Art. 35
DPIA, Art. 28 processor terms) · national employment/labour law information
duties, if any (verify per jurisdiction).

---

## 7. Step 6 — Timeline determination

State, with the legal-status register as source: which obligations apply
**now**; which apply from the (deferred) high-risk application date, giving
**both the original and the amended date** and the amendment's adoption
status; how Art. 111(2) interacts with the deployment date; and what changes
if pending amendments do not enter into force as expected.

---

## 8. Conclusions, ambiguities, actions

1. **Conclusions table** — one row per determination (AI system? / prohibited?
   / high-risk? / roles / key obligations / timeline), each with citation,
   confidence, and claim label.
2. **Open ambiguities** — where the law is genuinely unsettled; what would
   resolve each (guidance, OJ text, counsel).
3. **Actions** — each with actor, action, driver (article/risk/gap), evidence
   reference, and remaining uncertainty.
4. **Sign-off** — assessor; reviewer per `methodology/review-checklist.md`;
   re-assessment triggers (vendor feature changes, model updates, amendment
   entry into force, guidance issued).

---
*Template — fictional portfolio project. Not legal advice.*
