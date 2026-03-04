# Bug Database (Bug DB) — v1

> Status values: NEW / TRIAGED / IN_PROGRESS / FIXED / VERIFIED / CLOSED / RISK_NOTED

| bug_id | title | environment | steps_to_reproduce | expected_result | actual_result | severity | priority | evidence_link | status | notes |
|---|---|---|---|---|---|---|---|---|---|---|
| BUG-001 | Invalid password returns 200 instead of 401 | Web / Staging (unknown) | 1) Go to Login 2) Enter valid email 3) Enter wrong password 4) Click Login | Request should be rejected with HTTP 401; user not logged in; generic error shown | Response returns HTTP 200 with “login failed” in body (or similar) | High | P1 | (add link/screenshot later) | NEW | Defect candidate; aligns with Auth rules |
| BUG-002 | Missing/unclear account lockout policy after repeated failed logins | Web / Staging (unknown) | 1) Try wrong password 5+ times for same user 2) Observe behavior | After N failures, account should temporarily lock OR progressive delay should apply; generic messaging | Unlimited attempts allowed OR policy not visible/implemented | Medium | P2 | (add link/screenshot later) | RISK_NOTED | Security control gap (brute-force) |
| BUG-003 | Checkout accepts empty card number | Web / Unknown | 1. Login 2. Go to checkout 3. Leave card number empty 4. Click Pay | System must reject empty card number | Payment request accepted OR no validation shown | High | P1 | (add later) | NEW | Validation rule missing |
| BUG-004 | Checkout accepts incomplete card number | Web / Unknown | 1. Login 2. Go to checkout 3. Enter 12345678 4. Click Pay | System must validate card number format | Payment attempt processed | High | P1 | (add later) | NEW | Card format validation missing |
| BUG-005 | Payment endpoint returns incorrect status code | API / Unknown | 1. Send invalid payment request 2. Observe response | API should return 400 for validation error | API returns 200 | Medium | P2 | (add later) | RISK_NOTED | Status code validation needed |


