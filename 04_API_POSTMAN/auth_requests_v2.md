API-001

request_id: API-001
module: Auth
request_name: Login with valid credentials
method: POST
endpoint: /api/login
request_purpose: Verify that a registered user can log in successfully with valid credentials
request_data: valid email + valid password
expected_status_code: 200 OK
response_checks: Response should include success indication, authenticated user data, or token/session information
negative_or_positive: Positive
notes: Core authentication happy path

API-002

request_id: API-002
module: Auth
request_name: Login with invalid password
method: POST
endpoint: /api/login
request_purpose: Verify that the system rejects login when the password is incorrect
request_data: valid email + invalid password
expected_status_code: 401 Unauthorized
response_checks: Response should return an authentication error and should not create session/token
negative_or_positive: Negative
notes: Invalid credential handling

API-003

request_id: API-003
module: Auth
request_name: Login with empty email field
method: POST
endpoint: /api/login
request_purpose: Verify that the system validates required fields before processing login
request_data: empty email + valid password
expected_status_code: 400 Bad Request
response_checks: Response should return validation error for missing email and should not proceed with authentication
negative_or_positive: Negative
notes: Required field validation

API-004

request_id: API-004
module: Auth
request_name: Access protected resource without authentication
method: GET
endpoint: /api/user/profile
request_purpose: Verify that unauthorized users cannot access protected resources without valid authentication
request_data: no token / no session
expected_status_code: 401 Unauthorized
response_checks: Response should deny access and should not expose protected user information
negative_or_positive: Negative
notes: Authorization gate must block unauthenticated access

API-005

request_id: API-005
module: Checkout
request_name: Submit checkout with invalid input
method: POST
endpoint: /api/checkout
request_purpose: Verify that the checkout process rejects invalid input data and does not complete the transaction
request_data: invalid card number or invalid zip code
expected_status_code: 400 Bad Request
response_checks: Response should return validation error and should not approve payment/order creation
negative_or_positive: Negative
notes: Input validation in payment-critical flow
