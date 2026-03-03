# Auth / Status / Token / IDOR — Quick Map

## HTTP Status Codes
- 200 → Success
- 400 → Validation error (invalid format/input)
- 401 → Authentication required (not logged in / invalid token)
- 403 → Authorization error (no permission)
- 500 → Server error

## Authentication (Who are you?)
- Login + token verification
- Expired token → 401 Unauthorized

## Authorization (What can you access?)
- Access control checks (e.g. admin panel, other user data)
- Unauthorized access → 403 Forbidden

## Security Controls (Login Protection)
- Rate limiting → limit attempts per time window
- Account lockout → lock after multiple failed attempts
- Progressive delay → increase delay after each failure
- User enumeration protection → generic error messages

## Token Logic
- Access token → short-lived, expires → 401
- Refresh token → long-lived, generates new access token
- Expired token → must not allow access

## IDOR (Insecure Direct Object Reference)
- Changing IDs (user_id / order_id / invoice_id) should NOT expose other users' data
- Missing authorization checks → security vulnerability
