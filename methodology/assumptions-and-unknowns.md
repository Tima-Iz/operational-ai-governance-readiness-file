# Assumptions & Unknowns Register — Simulated Case

> **SIMULATION NOTICE.** Fictional compliance case for portfolio/educational
> purposes. Not legal advice.

Living register. Artifacts reference entries by ID (A-xx / U-xx). An assumption
is a condition the analysis *adopts* without evidence; an unknown is a question
the analysis *leaves open*. Converting either into a settled point requires
either new frozen evidence or a USER DECISION (D-xx).

## Assumptions (adopted for analysis unless the user directs otherwise)

| ID | Assumption | Why needed | Basis / evidence silence | Status |
|---|---|---|---|---|
| A-01 | Modaretti uses TalentSift Recruit as delivered: no retraining, no modification of intended purpose beyond vendor-provided configuration options (thresholds, weightings, auto-archive toggle) | Provider/deployer role analysis (Art. 25) in Artifact 1 | case-definition §1; EV-01 §3 lists only vendor-supported configuration | Proposed |
| A-02 | TalentSift places the system on the EU market under its own name and trademark | Provider determination (Art. 3(3)) | case-definition §1; EV-02 | Proposed |
| A-03 | ~~Modaretti has no works council or trade-union agreement covering algorithmic tools~~ **RESOLVED by D-009 (2026-07-13): Modaretti HAS an RSU** (case-definition §1, frozen v1.0). Note: the RSU exists but was not consulted about the tool (EV-05 §3) | Scope of worker-information analysis (Art. 26(7); Italian labour-law context) | USER DECISION D-009 | Resolved |
| A-04 | All candidates are natural persons located in the EU applying for roles in Italy | Territorial scope (Art. 2) and GDPR analysis kept simple | Evidence silent; consistent with case scope | Proposed |
| A-05 | The recruitment volumes, band thresholds, and configuration in EV-01/EV-06 remained materially unchanged from go-live (12 Jan 2026) to the register date | Artifacts assess a stable system state | EV-01 v1.2 (Mar 2026) matches EV-06 (Feb 2026) | Proposed |
| A-06 | Modaretti is a private company that does not provide public services | Art. 27 FRIA applicability analysis in Artifacts 1 and 3 | case-definition §1 (retail chain); evidence silent on any public-service activity | **Confirmed by D-010** (FRIA-Plus framed as voluntary, beyond formal compliance) |

## Unknowns (open questions the artifacts must treat as unresolved)

| ID | Unknown | Why it matters | Where it surfaces |
|---|---|---|---|
| U-01 | Basis of the "92% screening accuracy" claim — metric, dataset, relationship to the AUC 0.81 in EV-04 | Accuracy evidence (Art. 15); vendor credibility | EV-02 vs EV-04 |
| U-02 | Which candidate attributes the scoring model actually uses as features (e.g. whether commute distance, career gaps, or language inferences feed the score or only the highlight phrases) | Bias/proxy analysis; transparency to candidates | EV-04 (withheld feature documentation); EV-06 highlights |
| U-03 | Whether TalentSift uses customers' production data — including Modaretti's — to retrain or update models | GDPR roles, contract adequacy, model drift responsibility | EV-03 §Updates; EV-05 clause 10.1; EV-04 (training data ends 2023) |
| U-04 | Which candidate-data retention period actually applies: 24 months (EV-03) or 36 months (EV-05 clause 7.2) — and what Modaretti's own retention schedule (EV-01 §7) says | Data governance finding; storage limitation | EV-01 / EV-03 / EV-05 |
| U-05 | Whether the DPIA flagged as "pending" in January 2026 was ever performed | GDPR Art. 35 compliance; input for FRIA-Plus | EV-05 §3 |
| U-06 | Whether any recruiter in practice reviews auto-archived red-band candidates before the scheduled rejection e-mail | Effectiveness of human involvement | case-definition §3; EV-06 footer |
| U-07 | Content of the omitted pages 3–4 of the Getting Started Guide | Completeness of the instructions-for-use assessment | EV-03 |
| U-08 | Whether TalentSift has prepared for provider high-risk obligations (risk management system, technical documentation, EU database registration) ahead of 2 Dec 2027 | Vendor readiness; procurement leverage | EV-05 §3 (roadmap promise only) |
| U-09 | Demographic composition of Modaretti's actual applicant pool | Any deployer-side fairness monitoring would need it | Not in evidence |
| U-10 | Whether the automatic model updates (EV-03) have changed scoring behaviour since go-live, and whether Modaretti would be notified | Stability of the assessed system; clause 10.1 allows silent change | EV-03 / EV-05 |

## Maintenance

- New entries get the next free ID; IDs are never reused.
- Resolution is recorded here (with the resolving D-xx or EV reference) and in
  the project's internal change log; resolved entries are struck through, not
  deleted.
