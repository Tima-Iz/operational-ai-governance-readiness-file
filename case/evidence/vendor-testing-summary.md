# EV-04 — TalentSift Model Validation Summary (fictional, provided on request)

> **SIMULATION NOTICE.** Fictional document created for portfolio/educational
> purposes as part of a simulated compliance case. Not a real company or
> product. Not legal advice.

---

**TalentSift B.V. — Model Validation Summary**
Prepared for: Modaretti S.p.A. (Professional tier) — on customer request
Date: 17 February 2026 | Classification: Confidential — customer use only
Length: 1 page

## Model

Recruit Scoring Model v4.2 (deployed to all customers November 2025).
Component architecture: CV parsing module (proprietary NLP pipeline) feeding a
gradient-boosted classification model.

## Training data

Pooled, anonymised application and outcome records from 38 customer
organisations, 2019–2023. Total: approximately 2.1 million applications.
Sector mix: logistics (54%), retail (31%), business services (15%).
Geographic mix: Netherlands and Belgium (81%), Germany (11%), other EU (8%).
Label: progression outcome (shortlisted / interviewed / hired) as recorded in
customer systems.

## Performance

- Holdout AUC: **0.81** (temporal holdout, 2023 applications).
- Calibration: Brier score 0.19 on holdout.
- Performance is monitored on aggregate customer data and has remained stable
  since deployment.

## Fairness testing

- Protected attributes (gender, date of birth, nationality) are excluded from
  model inputs at parsing stage.
- Statistical parity difference for **gender** (inferred where not declared):
  within ±5 percentage points at the green-band threshold on holdout data.
- No statistically significant difference detected at the 5% level.

## Notes and limitations

- Detailed validation methodology, feature documentation, and disaggregated
  results are proprietary and available under NDA to Enterprise-tier
  customers.
- Results reflect the pooled training and holdout population. Customer-specific
  performance may vary with applicant population and role mix.
- Italian-language CVs constitute approximately 3% of the training corpus;
  parsing accuracy for Italian CVs is within acceptable internal thresholds.

*For questions, contact your customer success manager.*

---
*Fictional document — part of a simulated compliance case. Not legal advice.*
