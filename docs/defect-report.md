
# Defect Report – Counter Application

## DEF-001: Decrement Button Increases Counter Instead of Decreasing

**Related Test Case:** TC-003 – Verify Decrement Functionality

**Environment:**
- Operating System: macOS
- Application: React Counter Application
- Browser: Google Chrome
- Development Server: Vite

**Precondition:**
The Counter application is running.

**Steps to Reproduce:**

**Scenario 1 – Starting at Zero**
1. Open the Counter application in Chrome.
2. Confirm the counter displays 0.
3. Click the Decrement button once.
4. Observe the displayed counter value.

**Scenario 2 – Starting at 40**
1. Reset the counter to 0.
2. Click the Increment button 40 times until the counter displays 40.
3. Click the Decrement button once.
4. Observe the displayed counter value.

**Expected Results:**
- Scenario 1: The counter should decrease from 0 to -1.
- Scenario 2: The counter should decrease from 40 to 39.

**Actual Results:**
- Scenario 1: The counter increases from 0 to 1.
- Scenario 2: The counter increases from 40 to 41.

**Severity:** Medium

**Priority:** High

**Status:** Open – Awaiting Fix

**Reproducibility:** The incorrect increment behavior has been observed at both 0 and 40. Further repeat testing should confirm consistency.

**Technical Observation:**
The Decrement button's event handler uses `setCount(count + 1)`, which increases the counter instead of decreasing it. The expected operation is `setCount(count - 1)`.

**Impact:**
Users cannot correctly decrease the counter using the Decrement button. The application produces incorrect results regardless of whether the counter starts at zero or a larger positive value.
