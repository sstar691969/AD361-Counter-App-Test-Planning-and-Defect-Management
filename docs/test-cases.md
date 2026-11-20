
# Test Cases – Counter Application

## TC-001: Verify Initial Counter Value

- **Starting State:** Counter application is loaded.
- **Actions:**
  1. Open the Counter application in Chrome.
  2. Observe the displayed counter value.
- **Expected Result:** The counter displays its default initial value of 0.

## TC-002: Verify Increment Functionality

- **Starting State:** Counter displays 0.
- **Actions:**
  1. Click the Increment button once.
- **Expected Result:** The counter increases from 0 to 1.

## TC-003: Verify Decrement Functionality

- **Starting State:** Counter displays 0.
- **Actions:**
  1. Click the Decrement button once.
- **Expected Result:** The counter decreases from 0 to -1.
- **Potential Defect:** The button may increase the counter instead of decreasing it.

## TC-004: Verify Sequential Counter Operations

- **Starting State:** Counter displays 0.
- **Actions:**
  1. Click Increment twice.
  2. Click Decrement once.
  3. Click Reset once.
- **Expected Result:** The counter changes from 0 to 1, then 2, then 1, and finally returns to 0.