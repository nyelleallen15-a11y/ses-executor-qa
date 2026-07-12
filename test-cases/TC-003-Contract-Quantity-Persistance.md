# TC-003 — Contract Quantity Persistence

## Test Information

**Test Case ID:** TC-003

**Module:** Trading Settings & Persistence

**Priority:** High

**Risk Level:** High

**Tester:** Nyelle Allen

**Execution Date:** July 12, 2026

**Status:** PASS

---

## Objective

Verify that the configured contract quantity persists after the application is closed and reopened.

---

## Preconditions

- SES Executor is running normally.
- User is authenticated.
- Trading settings are accessible.
- No active trade execution is performed during testing.

---

## Test Steps

1. Launch the SES Executor.
2. Allow the application to connect normally.
3. Navigate to the **Trading** tab.
4. Open the **Ticker Risk** settings.
5. Record the current contract quantity.
6. Change the contract quantity from **6** to **3**.
7. Select **Save**.
8. Close the application normally.
9. Reopen the SES Executor.
10. Return to **Trading → Ticker Risk**.
11. Verify the contract quantity.

---

## Expected Result

The application should retain the updated contract quantity after restarting.

---

## Actual Result

The SES Executor launched successfully and connected normally.

The **Ticker Risk** settings page was opened and the configured contract quantity was recorded as **6**.

The value was changed to **3** and the configuration was saved successfully.

The application was closed using the normal shutdown procedure and reopened.

After returning to **Trading → Ticker Risk**, the contract quantity remained set to **3**, confirming that the setting persisted correctly across the application restart.

No unexpected behavior, crashes, or configuration loss were observed.

---

## Result

**PASS**

---

## Evidence

- SS-003A — Contract quantity before modification
- SS-003B — Updated contract quantity saved
- SS-003C — Contract quantity persisted after restart
