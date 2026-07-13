# Evidence Rules — EU AI Act Compliance File (Simulated Case)

> **SIMULATION NOTICE.** This project is a fictional compliance file created for
> portfolio and educational purposes. Not legal advice.

## Purpose

These rules govern how every artifact in this repository separates categories of
claim. They are adapted from the evidence rules of the author's previous project
(NGO Policy Briefing Agent) to fit a legal-compliance context, where the main
risks are **misstating the law**, **treating vendor claims as facts**, and
**blurring the line between what the law requires and what the analyst
recommends**.

---

## 1. Claim taxonomy

Every substantive claim in an artifact belongs to exactly one of the following
eight categories. The label must be visible wherever a reader could mistake one
category for another. In tables, use the short codes.

### CASE FACT `[CF]`

A statement about the fictional case established in `case/case-definition.md`
or the frozen evidence pack in `case/evidence/` (cited by evidence ID, e.g.
EV-01). Within the simulation, these documents are the only sources of case
facts. What a *fictional company document asserts* is a CASE FACT about what
the document says — not a fact that the assertion is true.

Example:
- Modaretti's HR procedure (EV-01) states that all hiring decisions are taken
  by people.

### EXTERNAL LEGAL SOURCE `[LS]`

A statement about what a real legal or standards text says, verified against
the authoritative source (see `methodology/source-register.md` hierarchy), with
a precise citation (article/paragraph/annex point) and a source-register ID.

Example:
- Article 26(7) AI Act requires deployers who are employers to inform workers'
  representatives and affected workers before putting a high-risk AI system
  into service at the workplace. [S-01]

### VENDOR CLAIM `[VC]`

An assertion made by TalentSift (in marketing, documentation, testing
summaries, or contract negotiations) that has **not been independently
evidenced**. Vendor claims are never promoted to facts, however confident their
wording. Record the claim, its source document, and what evidence would
substantiate it.

Example:
- TalentSift claims "92% screening accuracy" (EV-02); no metric definition,
  dataset, or methodology has been provided to support this figure.

### ANALYST INTERPRETATION `[AI]`

A conclusion about how the law applies to the case facts. It requires legal
reasoning, and a competent authority or court could reach a different view.
Every interpretation states its reasoning in 2–4 sentences, cites the legal
sources it rests on, and carries a confidence level (section 3).

Example:
- TalentSift Recruit likely falls under Annex III point 4(a) because it is
  intended for filtering applications and evaluating candidates. (Confidence:
  high.)

### ASSUMPTION `[AS]`

A condition the analysis needs but which neither the case evidence nor a
verified legal source settles. All assumptions are registered in
`methodology/assumptions-and-unknowns.md` with an ID and referenced by that ID.

Example:
- The analysis assumes Modaretti has no works council agreement covering
  algorithmic management tools (A-03).

### EVIDENCE GAP `[EG]`

Information a real compliance exercise would demand and which is missing —
usually from the vendor. State what is missing, why it matters, and who should
provide it.

Example:
- No bias-testing results disaggregated by age, ethnicity, or disability have
  been provided (EV-04 covers gender only).

### RECOMMENDATION `[RE]`

A proposed action for a named actor. A recommendation must never be phrased as
a legal obligation unless the obligation is separately established as an
EXTERNAL LEGAL SOURCE plus ANALYST INTERPRETATION.

Example:
- Modaretti's HR operations lead should disable auto-archiving until human
  review of red-band candidates is resourced and logged.

### USER DECISION `[UD]`

A determination made by the project owner (the user) that the analysis treats
as settled — e.g. approval of the case definition, the evidence freeze, scope
choices, or resolution of an ambiguity the analyst escalated. All user
decisions are recorded with an ID and date in the project's internal decision
log — a development record that is not part of the public repository — and
public documents reference decisions by that ID (D-xx).

Example:
- The case evidence pack was frozen at version 1.0 on the user's instruction
  (D-007).

---

## 2. Source and citation discipline

- Authoritative sources and their hierarchy are defined in
  `methodology/source-register.md`. **Official EU sources (EUR-Lex / Official
  Journal, Council, Parliament, Commission) are authoritative** for what the
  law says and its status; artificialintelligenceact.eu and similar trackers
  are convenience references only and never the sole basis for a claim.
- The legal status of every instrument relied on (in force, not yet applicable,
  adopted but unpublished, draft, non-binding, voluntary) is tracked in
  `methodology/legal-status-register.md` and must be checked before citing.
- Cite the **specific article and paragraph** (e.g. "Art. 26(7)", "Annex III
  point 4(a)"), never just the instrument.
- Never state what a provision says from memory alone. Verify against the
  registered source before writing. Anything not verified this way is marked
  **[unverified]**.
- Distinguish binding text from recitals, final guidance, draft guidance, and
  commentary, and say which one a claim rests on.
- **Timelines:** give both the original AI Act application dates and the
  Digital Omnibus-revised dates, with the Omnibus adoption status as recorded
  (and dated) in the legal-status register.
- No legal advice: artifacts state how the law *appears to apply to the
  fictional case* and flag where a real organisation would need counsel.

---

## 3. Evidence confidence levels

Applied to ANALYST INTERPRETATION and, where useful, to EVIDENCE GAP severity.

| Label | Meaning | Use when |
|---|---|---|
| High | Directly supported | The legal text or case evidence supports the conclusion with little interpretive distance |
| Medium | Reasonably supported, needs interpretation | The conclusion follows but a reviewer should check the reasoning |
| Low | Weakly supported or unsettled | The law is ambiguous, guidance is missing, or the case evidence is thin |
| Not supported | No support | Do not assert; present only as a question, assumption, or evidence gap |

---

## 4. Wording rules

Prefer:
- "Article X provides that..."
- "The vendor claims... ; this has not been evidenced."
- "On these facts, the better view is..."
- "This likely qualifies as... because..."
- "It is unsettled whether..."
- "A supervisory authority could take the view that..."

Avoid:
- "This proves..." / "It is certain that..."
- "The system is compliant" / "This guarantees compliance"
- "The law clearly requires..." unless the text is genuinely unambiguous and verified
- "TalentSift is liable for..." — liability findings belong to courts and authorities
- Repeating vendor marketing language without the VENDOR CLAIM label
- Hype of any kind ("cutting-edge", "robust framework", "best-in-class")

---

## 5. Recommendation rules

Every recommendation answers:

1. **Who** should act (named role, not "the organisation")?
2. **What** should they do, concretely?
3. **Why** — which legal obligation, risk, or gap drives it?
4. **Which evidence** (case fact by EV-ID, legal source by S-ID, gap) supports it?
5. **What uncertainty remains** after acting?

Generic recommendations ("improve transparency", "strengthen governance") are
not acceptable without actor, action, reason, and pathway.

---

## 6. Simulation integrity

- Every document carries the simulation notice and "not legal advice" header.
- Case facts may only come from `case/case-definition.md` and the frozen
  evidence pack in `case/evidence/`. If an artifact needs a fact the case does
  not settle, either register an ASSUMPTION or escalate for a USER DECISION —
  never silently invent it.
- After the evidence freeze, the evidence pack changes only by recorded USER
  DECISION with a version bump.
- Weaknesses present in the case evidence must surface as findings; artifacts
  must not sand them away or resolve them by assumption.
- The fictional evidence contains **no analyst legal conclusions**. Compliance
  language inside evidence documents (e.g. "EU AI Act ready") is a VENDOR
  CLAIM to be tested, not a finding.

---

## 7. Final rule

If unsure, say so clearly. A compliance file that shows its uncertainty is more
credible — and more useful as a portfolio piece — than one that fakes
confidence.
