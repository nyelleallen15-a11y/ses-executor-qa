# TC-006 — Maximum Contract Cap Enforcement

## Test Information

**Test Case ID:** TC-006

**Module:** Risk Management

**Priority:** Critical

**Risk Level:** Critical

**Tester:** Nyelle Allen

**Execution Date:** July 12, 2026

**Status:** PASS

---

## Objective

Verify that the configured Maximum Contract Cap is enforced during order execution, even when the configured Contract Quantity exceeds the allowed maximum.

---

## Preconditions

- SES Executor running normally
- Connected to trading environment
- Max Contract Cap configured to **10**
- Contract Quantity configured to **999**

---

## Test Steps

1. Launch the SES Executor.
2. Verify Contract Quantity is set to **999**.
3. Verify Maximum Contract Cap is set to **10**.
4. Trigger a trade under safe testing conditions.
5. Observe the quantity submitted by the execution engine.
6. Review application logs.

---

## Expected Result

The executor should limit the submitted order quantity to **10 contracts**, regardless of the configured Contract Quantity.

---

## Actual Result

The configured Contract Quantity was intentionally set to **999**.

The configured Maximum Contract Cap remained set to **10**.

During execution, the order quantity was limited to **10 contracts**, confirming that the risk management layer correctly enforced the configured maximum contract limit.

No unexpected behavior or execution failures were observed.

---

## Result

**PASS**

---

## Risk Assessment

This test validates a critical trading safety mechanism that prevents oversized order execution due to accidental configuration or user error.

---

## Evidence

- SS-006A — Contract Quantity = 999
- SS-006B — Max Contract Cap = 10
- SS-006C — Order executed with capped quantity
