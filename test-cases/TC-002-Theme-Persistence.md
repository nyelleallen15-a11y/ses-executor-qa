# TC-002 — Theme Persistence

## Test Information

**Test Case ID:** TC-002

**Module:** Settings & Persistence

**Priority:** High

**Tester:** Nyelle Allen

**Execution Date:** July 11, 2026

**Status:** PASS

---

## Objective

Verify that the selected application theme persists after the application is closed and reopened.

---

## Preconditions

- SES Executor is running.
- Settings menu is accessible.
- Multiple themes are available.

---

## Test Steps

1. Launch the SES Executor.
2. Navigate to the Settings tab.
3. Locate the Theme section.
4. Record the current theme.
5. Change the theme to **SES Gold**.
6. Apply the new theme.
7. Close the application normally.
8. Reopen the application.
9. Verify the selected theme remains **SES Gold**.

---

## Expected Result

The selected theme should automatically load after the application is restarted.

---

## Actual Result

The SES Executor was launched successfully.

The Settings panel was opened and the current theme was configured using the **"Make Theme From Background"** option.

The application theme was changed to **SES Gold** and applied successfully without errors.

The application was closed and reopened.

Upon restart, the **SES Gold** theme loaded automatically without additional user interaction.

The selected theme persisted successfully across the application restart.

---

## Result

**PASS**

---

## Evidence

- SS-002A — Theme selected before restart
- SS-002B — Theme persisted after restart
