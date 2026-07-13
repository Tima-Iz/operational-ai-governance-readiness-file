# Case Definition: TalentSift at Modaretti

> **SIMULATION NOTICE.** This document describes a **fictional** case created for
> portfolio and educational purposes. "TalentSift B.V." and "Modaretti S.p.A."
> do not exist; any resemblance to real companies or products is coincidental.
> Nothing in this project is legal advice.

> **CASE EVIDENCE FROZEN — VERSION 1.0** (2026-07-13, USER DECISION D-008).
> This document and `case/evidence/` are the sole sources of case facts for
> Artifacts 01–04. Changes only by recorded USER DECISION with a version bump
> in the project's internal change log.

## 1. The two parties

**TalentSift B.V.** (fictional) is a software company incorporated in Rotterdam,
the Netherlands (~60 employees). Its single product, **TalentSift Recruit**, is a
cloud-based (SaaS) AI tool for CV screening and candidate ranking, sold by
subscription to employers across the EU. TalentSift develops the underlying
models, hosts the service, and places it on the EU market under its own name.

**Modaretti S.p.A.** (fictional) is a mid-size Italian retail chain headquartered
in Bologna, operating ~140 clothing and home-goods stores plus two distribution
centres, with approximately **2,800 employees**. Modaretti receives 30,000–40,000
job applications per year, concentrated in high-turnover **store roles** (sales
assistants, cashiers, floor supervisors) and **logistics roles** (warehouse
operatives, pickers, shift leads). In January 2026 Modaretti licensed TalentSift
Recruit to filter and rank applications for these roles. Its HR department
(central team of 9, plus store managers with hiring duties) uses the tool as
delivered — Modaretti has not modified the system, retrained it, or changed its
intended purpose.

Modaretti's workforce is unionised at a level typical for Italian retail:
employees are covered by the national collective agreement for the tertiary
sector, and a **Rappresentanza Sindacale Unitaria (RSU)** — elected workplace
union representation — is in place at headquarters and at the distribution
centres, alongside store-level union delegates. (Added at freeze per USER
DECISION D-009.)

## 2. The system, in plain English

**What it does.** TalentSift Recruit ingests job applications, extracts
structured information from each CV, compares candidates against a job profile,
and produces a **suitability score and ranked shortlist** for each vacancy.

**Inputs.**
- The candidate's CV/résumé (PDF or Word) and the answers given on the online
  application form (work history, education, availability, languages,
  right-to-work confirmation).
- A "job profile" per vacancy: the employer selects a role template (e.g.
  "Sales Assistant — Fashion Retail") and can adjust weightings for experience,
  education, and skills.
- No video, audio, social-media, or psychometric data is used.

**Outputs.**
- A **match score from 0 to 100** per candidate per vacancy.
- A **ranked list** of candidates, with a colour band (green ≥ 70, amber 40–69,
  red < 40).
- Three to five auto-generated "highlight" phrases per candidate (e.g.
  "2+ years cashier experience", "no weekend availability indicated").

**Model type (plain-English level).** The product combines two components:
(1) a **language-processing component** that parses free-text CVs into
structured fields (jobs held, durations, skills, education); and (2) a
**statistical scoring model** — a machine-learning classifier — that predicts a
candidate's suitability. The scoring model was **trained on historical hiring
outcomes**: several years of anonymized records, pooled from TalentSift's early
client base, of which applicants were shortlisted, interviewed, and hired for
comparable roles. In effect, the system learns to imitate past human hiring
decisions. TalentSift markets this as "learning what great hires look like".

## 3. How Modaretti's HR uses it

1. A candidate applies through Modaretti's careers portal; the application flows
   automatically into TalentSift Recruit.
2. The system scores and ranks all applicants for the vacancy, updating as new
   applications arrive.
3. A **central HR recruiter** opens the ranked list. Per current configuration,
   candidates scoring **below 40 ("red band") are
   automatically moved to a "Not proceeding" folder** and receive a templated
   rejection email after 14 days unless a recruiter intervenes. Recruiters
   report that in practice they review the red folder "when volume allows",
   which for store roles is rarely.
4. The recruiter reviews the green and amber bands, selects candidates for a
   phone screen, and forwards a shortlist (typically 5–8 names) to the hiring
   **store manager or warehouse shift lead**, who conducts interviews and makes
   the final hiring decision.
5. **Who sees what:** recruiters see scores, rankings, colour bands, and
   highlight phrases. Hiring managers see only the forwarded shortlist (names
   and CVs, no scores). Candidates see neither their score nor any indication
   that automated screening was used — the careers portal privacy notice says
   only that applications are processed "using modern HR software".

## 4. Why this case (context for the reader)

Employment is an Annex III high-risk area under the EU AI Act precisely because
screening tools shape access to livelihoods at scale, invisibly, and with
feedback loops from past discrimination. This case is deliberately *ordinary*:
a competent mid-market vendor, a reasonable HR team under volume pressure, and
a handful of small design choices — none obviously unlawful on its face — that
together create material compliance gaps and human rights risks. The full
evidence sits in `case/evidence/` (EV-01 to EV-06); the four artifacts in this
repository work the case end to end: classification (01), inventory and risk
register (02), FRIA-Plus (03), and vendor assessment (04).

---
*Fictional case for portfolio/educational purposes only. Not legal advice.*
