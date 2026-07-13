# Evidence Index — Simulated Case Evidence Pack

> **SIMULATION NOTICE.** All evidence is fictional, created for
> portfolio/educational purposes. Not legal advice.

> **CASE EVIDENCE FROZEN — VERSION 1.0**
> Date: 2026-07-13 · Authorised by: project owner (USER DECISION D-008)
> Scope: `case/case-definition.md` and `case/evidence/` (EV-01–EV-06 + this index).
> Effect: these documents are the sole sources of case facts for Artifacts
> 01–04. Any change requires a recorded USER DECISION (D-xx), a version bump
> in the project's internal change log (a development record, not part of the
> public repository), and a note of which artifacts must be re-checked.

Artifacts cite evidence by ID (e.g. "EV-04 §Fairness testing"). Case facts may
come only from these documents and `case/case-definition.md`. What a document
*asserts* is a fact about the assertion — vendor claims remain VENDOR CLAIMS
until independently evidenced (see `methodology/evidence-rules.md`).

| ID | Document | Fictional author / origin | Fictional date | Perspective | Reliability notes for analysis |
|---|---|---|---|---|---|
| EV-01 | [hr-process-description.md](hr-process-description.md) — Internal HR procedure for screening with TalentSift Recruit (HR-PROC-2026-04 v1.2) | Modaretti HR Operations | 9 Mar 2026 | Deployer, internal | Authoritative for intended process and configuration; describes espoused process, which may diverge from practice |
| EV-02 | [vendor-product-description.md](vendor-product-description.md) — Product overview, sales edition | TalentSift marketing | Q1 2026 | Provider, promotional | Marketing document; all performance and compliance statements are unsubstantiated VENDOR CLAIMS |
| EV-03 | [instructions-for-use-extract.md](instructions-for-use-extract.md) — "Getting Started Guide" v3.1, extract (pp. 1–2, 5–6 of 6) | TalentSift customer success | Jan 2026 | Provider, operational | The closest document to "instructions for use" supplied; partial extract — pages 3–4 not reproduced |
| EV-04 | [vendor-testing-summary.md](vendor-testing-summary.md) — Model validation summary (1 page, on request) | TalentSift | 17 Feb 2026 | Provider, technical | Most substantive vendor evidence on file; self-reported, methodology withheld (Enterprise/NDA). **CURRENT APPLICABILITY NOT DEMONSTRATED**: describes model v4.2; two subsequent undisclosed scoring updates (v4.3, v4.4 — EV-07 G1) create uncertainty about applicability to the production version, pending a vendor change-impact assessment |
| EV-05 | [procurement-and-contract-notes.md](procurement-and-contract-notes.md) — Procurement file note + contract clause extracts (PROC-2025-311) | Modaretti Procurement | 20 Jan 2026 | Deployer, contractual | Authoritative for contract terms quoted and procurement chronology; "open items" reflect status at 20 Jan 2026 only |
| EV-06 | [sample-system-output.md](sample-system-output.md) — Pipeline export for vacancy VAC-2026-0187 | TalentSift Recruit (system-generated), exported by Modaretti recruiter | 20 Feb 2026 | System artefact | Direct evidence of outputs recruiters actually see; single vacancy, single date — not necessarily representative |

## Post-freeze simulated evidence

| ID | Document | Status |
|---|---|---|
| EV-07 | **Simulated Post-Freeze Vendor Questionnaire Response** — [artifacts/04-vendor-questionnaire/vendor-questionnaire-talentsift-responses.md](../../artifacts/04-vendor-questionnaire/vendor-questionnaire-talentsift-responses.md) | **New simulated evidence generated after the Version 1.0 evidence freeze** (registered by USER DECISION D-018). It does **not amend or overwrite EV-01–EV-06**; the frozen pack remains unchanged. EV-07 exists to complete Artifact 4 per the project brief (D-001) and is extrapolated strictly from the vendor posture established in EV-02–EV-05. Simulated post-assessment response — exact date not material; the project's legal-status reference date remains 13 July 2026 |

## Companion registers

- Assumptions and unknowns: `methodology/assumptions-and-unknowns.md`
- User decisions (D-xx) and pack versioning are tracked in the project's
  internal decision and change logs — development records that are not part
  of the public repository.
