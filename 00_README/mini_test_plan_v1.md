# Mini Test Plan — Auth & Checkout

## 1. Objective
The purpose of this test plan is to verify the functionality, security, and reliability of the Authentication (Login) and Checkout modules.

---

## 2. Scope

### In Scope:
- Login functionality
- Input validation
- Authentication logic
- Error handling
- Checkout process
- Payment input validation

### Out of Scope:
- UI/UX visual design testing
- Performance testing
- Third-party payment gateway internal systems

---

## 3. Test Approach

Testing will be conducted using:

- Functional Testing
- Negative Testing
- Boundary Value Analysis
- Risk-Based Testing

Priority will be given to high-risk areas such as:
- Login security
- Payment processing

---

## 4. Test Environment

- Platform: Web Application
- Browser: Google Chrome (latest version)
- Tools:
  - Jira (Test Management / Bug Tracking)
  - Postman (API Testing)

---

## 5. Entry Criteria

- Requirements are defined
- Test cases are prepared
- Test environment is accessible

---

## 6. Exit Criteria

- All critical test cases are executed
- High severity bugs are reported
- No blocking issues remain

---

## 7. Risk Areas

### Authentication Risks:
- Unlimited login attempts (no rate limiting)
- Weak password validation
- Token/session issues

### Checkout Risks:
- Invalid payment inputs accepted
- Incorrect total price calculation
- Duplicate transactions

---

## 8. Deliverables

- Test Cases
- Bug Reports
- API Test Collections
- Execution Summary

---

## 9. Test Scenarios Overview

### Login Module:
- Valid login
- Invalid credentials
- Empty input fields
- Boundary input values
- Multiple failed login attempts

### Checkout Module:
- Valid payment
- Invalid card number
- Invalid zip code
- Checkout flow interruption
- Quantity update issues

---

## 10. Success Criteria

- Core flows (login & checkout) work correctly
- Errors are handled properly
- System prevents invalid or risky actions
