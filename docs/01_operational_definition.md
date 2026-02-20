# Operational Definition

---

## Business Context

The company operates a subscription-based digital financial advisory service offering newsletters, webinars, and investment recommendations.

From a business perspective, **churn** represents the loss of an active paying subscriber.

---

## Analytical Definition

For this project, **churn** is operationally defined as:

- A customer is considered **churned** if cancel date time **IS NOT NULL**.
- Customers with a **null** cancel date time are considered **active** at the end of the observation period.

This definition is strictly structural and does not incorporate engagement or behavioral signals, as such data is not available in the dataset.

