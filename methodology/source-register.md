# Source Register — EU AI Act Compliance File (Simulated Case)

> **SIMULATION NOTICE.** This project is a fictional compliance file created for
> portfolio and educational purposes. Not legal advice.

## Purpose

Single register of every external source relied on in this project. Every
EXTERNAL LEGAL SOURCE claim in an artifact cites a source ID (S-xx) from this
register. Fictional case evidence is registered separately in
`case/evidence/evidence-index.md` (EV-xx IDs) and is never a source for
statements about the real world.

## Source hierarchy

Sources are used in this order of authority. A claim is only as strong as the
highest-tier source supporting it.

| Tier | Source type | Use |
|---|---|---|
| 1 | Official Journal of the EU / EUR-Lex consolidated texts | Authoritative for what binding law says and when it applies |
| 2 | Official communications of EU institutions (Council, European Parliament, Commission press releases, legislative observatory/train) | Authoritative for legislative status and procedural facts |
| 3 | Final guidance by EU bodies (Commission guidelines, AI Office, EDPB) | Persuasive, non-binding; cite as guidance, never as law |
| 4 | Draft guidance, standards bodies' published material (ISO, CEN-CENELEC) | Context only; flag draft/voluntary status explicitly |
| 5 | Reputable secondary sources (artificialintelligenceact.eu explorer, law-firm analyses, academic commentary) | Convenience/navigation only — never the sole basis for a legal claim; always re-verify at Tier 1–2 |

## Register fields

- **ID** — S-xx, stable once assigned.
- **Source** — full name and URL.
- **Tier** — per hierarchy above.
- **Source status** — e.g. in force / adopted, awaiting OJ publication / final guidance / draft / voluntary standard.
- **Relevant provision(s)** — articles, annex points, or sections relied on.
- **Proposition supported** — what this source is used to establish in this project.
- **Access date** — when last consulted.
- **Verification status** — Verified (consulted directly this project) / Unverified (from memory or secondary source; must be verified before an artifact relies on it).

## Register

| ID | Source | Tier | Source status | Relevant provision(s) | Proposition supported | Access date | Verification status |
|---|---|---|---|---|---|---|---|
| S-01 | Regulation (EU) 2024/1689 (AI Act), OJ L, 12.7.2024 — via EUR-Lex http://data.europa.eu/eli/reg/2024/1689/oj | 1 | In force since 1 Aug 2024; application staggered | Art. 3, 5, 6, 9–15, 17, 25, 26, 27, 50, 111, 113; Annex III | All statements about what the AI Act says | 2026-07-13 | **Verified at Tier 1 (2026-07-13):** the OJ PDF (EUR-Lex, OJ L 2024/1689) was retrieved and text-extracted locally; Art. 3(1)(3)(4)(23)(52), 4, 5(1)(f), 6(2)–(4), 25(1), 26(2)(7)(11), 27(1), 50(1)(3), 111(2), 113 and Annex III pt 4(a)–(b) read verbatim and found consistent with all artifact statements. Enacted text — Omnibus amendments per S-04 |
| S-02 | Council of the EU press release, "Artificial Intelligence: Council gives final green light to simplify and streamline rules", 29 June 2026, consilium.europa.eu | 2 | Official press release | Digital Omnibus on AI — final Council approval | Omnibus adopted by Council 29 Jun 2026; Annex III high-risk obligations deferred to 2 Dec 2027; Annex I embedded to 2 Aug 2028; OJ publication "shortly", entry into force on 3rd day after publication | 2026-07-13 | Verified (via EEAS mirror; consilium.europa.eu blocked automated access — re-check original before publication) |
| S-03 | European Parliament, Legislative Train Schedule, "Digital Omnibus on AI", europarl.europa.eu/legislative-train/package-digital-package/file-digital-omnibus-on-ai | 2 | Legislative tracker (official) | Digital Omnibus procedure | Parliament formal endorsement 16 Jun 2026; procedural history (provisional agreement 6–7 May 2026) | 2026-07-13 | Partially verified (search results; fetch the page directly before relying on procedural details) |
| S-04 | Digital Omnibus on AI — adopted final text **PE-CONS 30/26**, Council public register: data.consilium.europa.eu/doc/document/PE-30-2026-INIT/en/pdf (also REV 1) | 1–2 | **ADOPTED FINAL TEXT — NOT YET IN FORCE; OFFICIAL JOURNAL PUBLICATION PENDING AS OF 13 JULY 2026** | Amended application dates (incl. Annex III → 2 Dec 2027) and any adjustment to Art. 111(2), Art. 50 limb dates | The definitive amended wording, citable now; OJ number and entry-into-force date follow publication | 2026-07-13 | **Provision-level content verified 2026-07-13**: PDF retrieved from the Council register and text-extracted locally (pdftotext); points (13) Art. 27(4)–(5), (39) Art. 111(2)+(4), (40) Art. 113 third para read verbatim; recitals (39)–(40) on the grace period consulted. Extracted text retained in session scratchpad (`pe-cons-30-26.txt`). Note: automated web fetch of consilium.europa.eu fails (403 / raw binary); EP TA-10-2026-0098 HTML returns empty to automated fetch. Replace with OJ citation once published |
| S-05 | Regulation (EU) 2016/679 (GDPR), via EUR-Lex | 1 | In force, applicable | Art. 22, 28, 35 | Automated decision-making, processor contracts, DPIA duties intersecting the case | — | Unverified this project |
| S-06 | Commission Guidelines on prohibited AI practices (Art. 5 AI Act), Feb 2025 | 3 | Final non-binding guidance (adoption status to confirm) | Art. 5 | Interpretive support for prohibited-practices screening in Artifact 1 | — | Unverified this project |
| S-07 | Commission Guidelines on the definition of an AI system (Art. 3(1) AI Act), Feb 2025 | 3 | Final non-binding guidance (adoption status to confirm) | Art. 3(1) | Interpretive support for "is it an AI system" test in Artifact 1 | — | Unverified this project |
| S-08 | ISO/IEC 42001:2023 — AI management systems | 4 | Voluntary standard | Thematic alignment referenced in risk register (Artifact 2) | Thematic governance alignment only — clause-level verification pending; clause numbers are not published in this project | — | Unverified this project (clause-level references removed pending verification against an authorised copy) |
| S-09 | artificialintelligenceact.eu — AI Act Explorer (Future of Life Institute) | 5 | Secondary tracker | Full-text navigation | Convenience navigation to article text only; every claim re-verified at Tier 1 | — | N/A (never sole basis) |
| S-10 | Charter of Fundamental Rights of the EU (2012/C 326/02), via EUR-Lex | 1 | In force (primary law) | Art. 1 (dignity), 7–8 (private life, data protection), 15(1) (right to engage in work), 21 (non-discrimination), 47 (effective remedy) | Rights framework for the FRIA-Plus stakeholder and impact mapping (Artifact 3) | 2026-07-13 | **Verified at Tier 1 (2026-07-13):** article subjects (1 dignity; 7 private life; 8 data protection; 15 work/occupation; 21 non-discrimination; 47 effective remedy) confirmed against the EUR-Lex Charter text |

## Maintenance rules

- Add a row before first citing any new source; never cite an unregistered source.
- Update **access date** and **verification status** whenever a source is consulted.
- A source marked Unverified must be verified before any artifact conclusion rests on it; until then the dependent claim carries **[unverified]**.
- Changes to this register are recorded in the project's internal change log
  (development record).
