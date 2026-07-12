# Defect Report

## Defect Information

**Defect ID:** DEFECT-001

**Title:** Invalid Contract Quantity Rejected Without User Feedback

**Status:** Open

**Severity:** Medium

**Priority:** Medium

**Module:** Trading Settings – Ticker Risk

**Discovered By:** Nyelle Allen

**Date Reported:** July 12, 2026

---

# Description

The application prevents an invalid contract quantity value of **0** from being saved.

However, no validation message, warning, or error is displayed to the user.

The settings window closes as though the configuration was successfully saved, which may lead users to believe that the new value was accepted.

Upon reopening the settings, the previous valid value is still present.

---

# Preconditions

- SES Executor running normally
- Trading settings accessible
- Ticker Risk settings opened

---

# Steps to Reproduce

1. Open the SES Executor.
2. Navigate to **Trading → Ticker Risk**.
3. Locate the **Contract Quantity** field.
4. Change the value from a valid number (example: 6) to **0**.
5. Click **Save**.
6. Reopen the **Ticker Risk** settings.

---

# Expected Result

The application should either:

- Reject the value immediately,

**or**

- Display a validation message explaining that contract quantity must be greater than zero.

The user should clearly understand why the configuration was not accepted.

---

# Actual Result

The application allowed the value **0** to be entered.

The **Save** action completed without displaying any warning or validation message.

After reopening the settings, the previous valid value remained unchanged.

The invalid value was silently rejected.

---

# Reproducibility

Repeated multiple times.

Result was consistent.

---

# Business Impact

Users may incorrectly believe their trading configuration has been updated.

This could lead to confusion regarding active trading settings and reduce confidence in application behavior.

---

# Recommendation

Display a validation message when an invalid contract quantity is entered.

Example:

> "Contract Quantity must be greater than 0."

Alternatively, prevent invalid values from being entered in the input control.

---

# Evidence

- TC-004 Execution
- SS-004A – Invalid value entered
- SS-004B – Previous value restored
