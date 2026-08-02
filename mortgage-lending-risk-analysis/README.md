# Mortgage Lending Pipeline: Risk Modelling & Cashflow Simulation

**Prepared for:** Chief Financial Officer (coursework brief, MN50755 Data Mining & Machine Learning)
**Tools:** Python (Pandas, scikit-learn, statsmodels), SQL, Matplotlib

## Business Problem

A mortgage lender's approved-application pipeline faces two problems: not knowing which approved deals will actually complete, and not knowing when the rest will fund. Treasury needs a reliable near-term cashflow forecast to plan liquidity.

## Data

Three years of approved mortgage applications (Q3 2021–Q3 2024), covering loan size, property valuation, location, business channel, applicant demographics and property characteristics. 11,207 observations after cleaning.

## Key Data Issues Resolved

- **Right-censoring:** Q3 2024 completion rate registered an artificially low 27.6% because recent approvals hadn't had time to complete. These observations were stripped from training data to avoid teaching the model that recent approvals are inherently riskier.
- **Non-random missingness:** ~10% of records had no recorded property age. Rather than imputing zero (which would falsely imply a newly built property), a binary missingness flag was added — itself a statistically meaningful predictor.
- **Baseline model flaws:** The original analyst model used only 3 weak features (country, business source, loan amount) and contained a code bug that meant the "timing model" was actually predicting a boolean completion flag rather than days to completion.

## Modelling Approach

- **Completion probability:** Improved logistic regression (AUC 0.773) and a calibrated Random Forest (AUC 0.772) — both dramatically outperforming the analyst baseline (AUC 0.568). Property age was the dominant signal (72% of Random Forest feature importance).
- **Time-to-completion:** Gradient Boosting model (RMSE 10.73 days) vs corrected baseline (RMSE 13.52 days), with LTV as the dominant driver (55% importance) — a reversal from the completion model, validating that completion risk and funding speed have different drivers.
- **Cashflow simulation:** A 2,000-iteration bootstrap simulation over the open pipeline (3,885 applications, £649.6M) produced a base-case forecast of **£80.7M** expected advances over a 2-month window, with a 90% confidence interval of £76.0M–£85.5M.

## Key Result

| Scenario | Expected Cashflow |
|---|---|
| Stress (−10pp completion) | £69.8M |
| Base case | £80.7M |
| Upside (+5pp completion) | £85.0M |

**Recommendation:** A liquidity buffer of **£10.9M** to cover the stress scenario gap.

## Business Impact

- Improved completion-prediction accuracy by ~36 percentage points of AUC over the existing baseline.
- Replaced a single point-estimate forecast with a full distribution, enabling treasury to plan around stress scenarios rather than an unreliable single number.
- Flagged model limitations transparently (no macroeconomic variables, training data cutoff) to avoid overconfidence in the recommendation.
