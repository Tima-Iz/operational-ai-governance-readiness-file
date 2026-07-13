# AI Inventory — Modaretti S.p.A. (deployer perspective)

> **SIMULATION NOTICE.** Fictional inventory for a fictional case, created for
> portfolio and educational purposes. Not legal advice.

## Purpose and field definitions

The inventory is the anchor document of AI governance: no obligation can be
managed for a system the organisation does not know it operates. One row per
AI system. Fields:

| Field | Meaning |
|---|---|
| System ID | Stable internal identifier |
| System / version | Product name and the version actually in operation |
| Purpose | What the system is used for, in operational terms |
| Role | Organisation's AI Act role for this system (provider / deployer / both), with counterparty |
| Risk classification | AI Act classification, with the assessment it rests on |
| Lifecycle stage | Planned / procurement / pilot / in operation / suspended / retired |
| Vendor criticality | Internal vendor-management tier |
| Owner(s) | Named accountable roles — business, privacy, contract |
| Review date | Next scheduled review + standing re-review triggers |
| Key references | Evidence and assessments on file |

## Inventory (as at 2026-07-13)

| Field | AI-INV-001 |
|---|---|
| System ID | AI-INV-001 |
| System / version | TalentSift Recruit — scoring model v4.2 (SaaS; vendor-updated automatically) `[CF: EV-04, EV-03]` |
| Purpose | Screening and ranking of job applications for store and logistics roles; produces 0–100 match score, colour band, ranked shortlist, highlight phrases `[CF: EV-01 §2]` |
| Role | **Deployer** (Art. 3(4)). Provider: TalentSift B.V. (NL). No Art. 25 re-qualification on current facts — Artifact 1 §5, C4 |
| Risk classification | **High-risk — Annex III point 4(a)**; Art. 6(3) derogation unavailable (profiling, Art. 3(52)) — Artifact 1 §4, C3. High-risk obligations apply from **2 Dec 2027** (orig. 2 Aug 2026; PE-CONS 30/26, adopted final text — not yet in force); GDPR and AI Act Art. 4–5 apply **now** |
| Lifecycle stage | In operation since 12 Jan 2026 `[CF: EV-05]` |
| Vendor criticality | **Critical (highest tier)** — Annex III system affecting access to livelihoods `[UD: D-012]` |
| Owner(s) | Business: HR Operations Lead · Privacy: DPO · Contract: Procurement Manager · Executive sponsor: HR Director |
| Review date | **October 2026** (contract renewal — the leverage point) · then semi-annual · standing triggers: vendor feature/model-update notices, Omnibus entry into force, new guidance, any incident, **and any breach of the D-015 gate conditions (no rejection without documented recruiter review; DPIA progress; notice and RSU information delivered)** — see risk register §Governance outcome |
| Key references | EV-01–EV-06 (frozen pack v1.0); Artifact 1 v1.0; risk register R-01–R-14 |

## Completeness note `[EG]`

This inventory records the system in scope of this compliance file. **No
organisation-wide survey of Modaretti's software estate has been performed**
— HR, marketing, logistics, or security tooling may embed AI functions
(scheduling, forecasting, monitoring) that belong here, and Annex III 4(b)
(workforce management) would be the first classification question for several
of them. Action for the HR Director and IT: run a structured
AI-identification survey before the October 2026 review, and add every
identified system to this inventory with at least a preliminary
classification. `[RE]`

---
**Version: 1.0 — FINAL** (2026-07-13; user review decisions D-015 applied).

*Fictional inventory for portfolio/educational purposes only. Not legal advice.*
