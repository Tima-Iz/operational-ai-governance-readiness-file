# Voluntary FRIA-Plus: Rights-Impact and Deployment Decision Assessment — TEMPLATE
## A thesis-derived, deployer-side extension of Article 27 FRIA for high-risk AI governance

> **SIMULATION NOTICE.** Part of a fictional portfolio project. Not legal
> advice.

> **STATUS OF THIS METHODOLOGY.** FRIA-Plus is a **voluntary governance
> instrument derived from the author's MA thesis** on the EU AI Act and human
> rights due diligence. It extends the structure of Art. 27 AI Act with
> elements drawn from HRDD practice — ongoing monitoring,
> necessity/proportionality reasoning, contestability and remedy pathways,
> and an Ethical Justification Record. **These additional elements are not AI
> Act requirements. FRIA-Plus is not an official, certified, or legally
> recognised methodology**, and completing it does not establish legal
> conformity. Its purpose is a **defensible, documented deployment decision**.
> Sections marked ✚ are thesis-derived additions beyond the Art. 27 baseline.

## How to use this template

Complete after (and using) the applicability assessment and risk register —
FRIA-Plus *selects and deepens* the material rights impacts; it does not
repeat the full register. Every finding cites evidence (EV-xx) and risk
(R-xx) IDs; every control has an owner, deadline, and effectiveness test.
Where the deployer is not legally obliged to conduct an Art. 27 FRIA, say so
and state why the assessment is nonetheless being done. Keep it
decision-oriented: the output is Section 5's deployment decision, prepared
but **not taken** by the assessor.

---

## 1. Scope and deployment context

State briefly: system and intended purpose · deployment context · affected
process · provider and deployer · affected persons (categories and annual
scale) · assessment boundaries (what is out of scope and why) · evidence
limitations · relationship with the GDPR DPIA (Art. 27(4) as amended by
PE-CONS 30/26 permits cross-referencing; mirror this voluntarily — do not
duplicate the DPIA) · **why the assessment is voluntary** (legal position on
Art. 27(1) applicability, with citation).

## 2. Stakeholder and rights mapping

Two short tables. **Stakeholders:** who is affected or involved, their stake,
their current visibility into the system. **Rights:** for each relevant right
(equality/non-discrimination; access to employment; privacy and data
protection; dignity and autonomy; transparency; meaningful human review;
contestability and remedy — cite the instrument), the potential impact on
these facts, and whether the impact pathway is **evidenced** (EV-xx) or
**plausible but unverified** (state what would verify it). Do not list rights
that nothing in the case touches.

## 3. Material rights-impact scenarios

Select the **4–6 most material scenarios** from the risk register — the test
is materiality to *rights-holders*, not to the organisation. Per scenario:

| Field | Guidance |
|---|---|
| Scenario ID / title | FR-xx |
| Affected persons | Who, and roughly how many per year |
| Causal pathway | Mechanism from system behaviour to harm, step by step |
| Supporting evidence | EV-xx (+ what a fictional/real file would still need) |
| Risk-register link | R-xx |
| Nature of harm | The right(s) affected and how |
| Severity | On the rights-holder, not the organisation |
| Scale and scope | How many affected, how broadly |
| Remediability | Can the harm be undone once it occurs? |
| Likelihood / uncertainty | Honest — and **do not discount a severe impact because likelihood is unproven**; unverifiable likelihood is itself a finding ✚ |
| Existing controls | What operates today, with evidence |
| Control weaknesses | Why existing controls underperform |
| Evidence gaps | What is still missing, and who holds it |

## 4. Required actions and controls

Per scenario: **interim safeguard** (implementable now) · **permanent
control** · owner · deadline · evidence of implementation · **effectiveness
test** (how you would know it works — a measurable check, not an intention) ·
vendor dependency · contract-amendment dependency · escalation or suspension
trigger.

Then separate into three lists: (a) controls the deployer can implement
directly; (b) controls requiring the provider; (c) **risks that cannot
currently be adequately controlled** — naming them is the point.

## 5. Ethical Justification Record ✚

The EJR is FRIA-Plus's documented answer to "should this system be deployed
(or remain deployed) at all?" — part of this methodology, not a separate or
official framework. Work through three tests **in prose, not scores**; a
numerical cost-benefit shortcut is expressly rejected.

**Necessity:** the problem the system solves · whether the claimed benefit is
evidenced (vendor claims are not evidence) · non-AI or less intrusive
alternatives · whether each *function* is separately necessary (ranking ≠
auto-rejection — test them separately) · whether the objective is achievable
with lower rights risk.

**Proportionality:** expected benefits and to whom · severity and
reversibility of remaining harms and who carries them (name the asymmetry) ·
whether safeguards materially reduce risk · whether a less harmful
configuration exists · whether residual risk is acceptable, and on what
conditions.

**Contestability:** notification · explanation of AI's role · access to a
human reviewer · timeliness · **reviewer's authority to change the outcome** ·
record preservation · complaint and remedy pathway · accessibility.

**Deployment options.** Present exactly four: (1) continue normal deployment;
(2) continue only under specified conditions; (3) limited pilot with enhanced
monitoring; (4) pause / do not deploy. For each: supporting reasons ·
unresolved risks · required conditions · consequences for applicants ·
consequences for the deployer · vendor dependencies. Give the assessor's
preliminary recommendation with reasons — then mark the final decision
**USER JUDGMENT REQUIRED** (or the accountable owner's judgment, in a real
organisation). The record must also answer, explicitly: can the most
automated function be justified; can operation continue before provider
evidence gaps close; which controls are mandatory before continued use;
which issues become contract-renewal conditions.

## 6. Monitoring and reopening ✚

FRIA-Plus is an ongoing process, not a one-time checklist. One concise table:
what is monitored (candidate outcomes; subgroup outcomes when lawfully
possible; overrides and human-review rates; complaints and appeals; parsing
errors; model versions and updates) · metric · owner · cadence · **the
threshold that reopens this assessment or suspends the system**. Add
reopening triggers that are events, not metrics: vendor notifications, legal
changes (entry into force, guidance), contract changes, incidents, scheduled
reassessment date.

## Sign-off

Assessor · reviewer (per the project review checklist) · decision-maker and
decision (from Section 5) · date · next scheduled reassessment.

---
*Template — fictional portfolio project. Thesis-derived methodology; not an
official instrument. Not legal advice.*
