# Analytical Framework

---

## 1. Unit of Analysis

The unit of analysis is one row per customer.
In this dataset, each customer corresponds to a single subscription lifecycle. Therefore, customer-level and subscription-level analysis are equivalent.

---

## 2. Observation Cutoff Date

Since some customers remain active at the time of data extraction, the dataset is right-censored.

An analysis cutoff date is defined as:
The maximum lifecycle date observed across the dataset (considering both sign-up and cancellation timestamps).

All duration-based calculations are computed relative to this cutoff date.

---

## 3. Tenure Definition

Observed tenure is calculated as:

For churned customers:
cancel_date_time - signup_date_time

For active customers:
cutoff_date - signup_date_time

This represents observed tenure, not true lifetime tenure.

---

## 4. Revenue Measurement

Revenue is measured only over the observed period.
Because the dataset does not include transaction-level billing records, revenue is estimated using subscription price and billing cycle assumptions.
No projected lifetime revenue is estimated in the initial analysis phase.

---

## 5. Support Case Variables

Support-related variables are treated as behavioral signals, not causal drivers.

Key derived variables include:

- total_cases_lifetime
- cases_last_30_days_before_churn
- had_case_last_30_days
- cases_per_month_observed
- days_from_last_case_to_cancel

These variables are constructed carefully to avoid data leakage (i.e., using information that occurs after churn).

---

## 6. Churn Interpretation Principles

The analysis follows these principles:

- Associations do not imply causation.
- Exposure time must be considered when comparing customers.
- Churn early in the lifecycle may signal onboarding or activation issues.
- Support activity may correlate with churn but does not necessarily cause churn.
- Some churn may occur due to unobservable factors (e.g., perceived value, financial constraints).

---

## 7. Right-Censoring Considerations

Active customers have incomplete lifetime information at the time of analysis

Therefore:

- Observed tenure underestimates true lifetime for active customers.
- Revenue and support metrics for active customers are right-censored.
- Comparisons between churned and active customers must account for exposure time.

---

## 8. Analytical Focus

The project aims to:

- Quantify churn structurally
- Identify temporal patterns
- Compare churn across billing cycles
- Evaluate the association between support interactions and cancellation
- Explore early vs late churn dynamics
- The project does not aim to build a predictive model.

