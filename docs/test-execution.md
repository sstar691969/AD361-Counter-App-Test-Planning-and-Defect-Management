
# Test Execution Report – Counter Application

## 1. Test Environment

- Operating System: macOS
- Application: React Counter Application
- Runtime: Node.js
- Package Manager: npm
- Development Server: Vite
- Browser: Google Chrome
- Test Method: Manual Functional Testing

## 2. Test Execution Results

| Test ID | Test Description | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TC-001 | Verify Initial Counter Value | Counter displays 0 | Counter displayed 0 when application loaded | Pass |
| TC-002 | Verify Increment Functionality | Counter increases from 0 to 1 | Counter increased from 0 to 1 | Pass |
| TC-003 | Verify Decrement Functionality | Counter decreases from 0 to -1 | Counter increased from 0 to 1 | Fail |
| TC-004 | Verify Sequential Counter Operations | Sequence: 0 → 1 → 2 → 1 → 0 | Actual sequence: 0 → 1 → 2 → 3 → 0 | Fail |

## 3. Defect Reproducibility

The Decrement button produced incorrect results in multiple scenarios:

- Starting at 0, clicking Decrement increased the counter to 1.
- Starting at 40, clicking Decrement increased the counter to 41.
- During sequential testing, the counter increased from 2 to 3 instead of decreasing to 1.

These observations demonstrate the same defect across different starting values and interaction sequences.

## 4. Test Summary

- Total Test Cases: 4
- Passed: 2
- Failed: 2
- Not Run: 0
- Defects Identified: 1

## 5. Final Assessment

The Counter application successfully loads, displays its initial value, increments correctly, and resets to zero.

However, the Decrement button does not perform its intended operation. It increases the counter instead of decreasing it. This defect affects both individual and sequential counter operations.

The identified defect is documented separately in `docs/defect-report.md` as DEF-001.