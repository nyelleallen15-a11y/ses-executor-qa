# TC-004 — Negative Contract Quantity Validation

## Test Information

**Test Case ID:** TC-004

**Module:** Trading Settings – Ticker Risk

**Priority:** High

**Risk Level:** High

**Tester:** Nyelle Allen

**Execution Date:** July 12, 2026

**Status:** PASS

---

## Objective

Verify that the Contract Quantity field prevents negative values from being entered.

---

## Preconditions

- SES Executor is running.
- Trading settings are accessible.

---

## Test Steps

1. Launch the SES Executor.
2. Navigate to **Trading → Ticker Risk**.
3. Select the **Contract Quantity** input field.
4. Attempt to enter **-1**.

---

## Expected Result

The application should prevent negative values from being entered.

---

## Actual Result

The application prevented the minus (`-`) character from being entered into the Contract Quantity field.

Because the negative value could not be entered, the application successfully prevented invalid input before it could be saved.

No errors, crashes, or unexpected behavior were observed.

---

## Result

**PASS**

---

## Evidence

- SS-005A — Attempt to enter a negative value
