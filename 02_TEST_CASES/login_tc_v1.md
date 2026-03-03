## TC-001 — Login with valid credentials

**Precondition:**
- User is registered
- User is on login page

**Test Data:**
- Email: valid_user@example.com
- Password: CorrectPassword123

**Steps:**
1. Enter valid email
2. Enter valid password
3. Click "Login"

**Expected Result:**
- User is successfully logged in
- Redirect to dashboard
- HTTP response status = 200


---

## TC-002 — Login with invalid password

**Precondition:**
- User is registered
- User is on login page

**Test Data:**
- Email: valid_user@example.com
- Password: WrongPassword123

**Steps:**
1. Enter valid email
2. Enter invalid password
3. Click "Login"

**Expected Result:**
- Login is rejected
- Generic error message is displayed (e.g. "Invalid credentials")
- No sensitive information exposed
- HTTP response status = 401
