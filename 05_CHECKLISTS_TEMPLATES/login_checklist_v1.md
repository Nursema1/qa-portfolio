# Login Test Checklist

## Input Validation
- Email field is not empty
- Password field is not empty
- Email format is valid
- No spaces-only input allowed

## Authentication
- Valid login works
- Invalid password is rejected
- Invalid email is rejected

## Security
- Account locks after multiple failed attempts
- Error messages are generic (no info leak)

## State Handling
- Locked account cannot login
- User remains logged out after failed login

## Session
- User stays logged in after login
- Logout works correctly
