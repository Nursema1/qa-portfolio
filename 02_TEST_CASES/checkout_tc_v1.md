## TC-003 — Checkout with empty card number

**Precondition:**
- User is logged in
- User is on checkout page

**Test Data:**
- Card number: empty

**Steps:**
1. Navigate to checkout page
2. Leave card number field empty
3. Click "Pay"

**Expected Result:**
- Payment must not be processed
- Validation error message is displayed
- HTTP response status = 400

## TC-004 — Checkout with incomplete card number

**Precondition:**
- User is logged in
- User is on checkout page

**Test Data:**
- Card number: 12345678

**Steps:**
1. Navigate to checkout page
2. Enter incomplete card number
3. Click "Pay"

**Expected Result:**
- Payment must be rejected
- Validation error message displayed
- HTTP response status = 400

## TC-005 — Checkout with valid card format

**Precondition:**
- User is logged in
- User is on checkout page

**Test Data:**
- Card number: 4111111111111111

**Steps:**
1. Navigate to checkout page
2. Enter valid card number format
3. Click "Pay"

**Expected Result:**
- Payment request is accepted for processing
- System proceeds to next payment step
- HTTP response status = 200
