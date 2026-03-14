# Login Test Covarage Map

Feature: Login

Coverage Areas

1. Valid login
2. Invalid password
3. Invalid email format
4. Empty email
5. Empty password
6. Account lock after failed attempts
7. Logout
8. Locked account login attempts


# Login Test Coverage Map

Feature: Login

Description:
This coverage map identifies the key functional areas that must be tested in the login feature to ensure adequate test coverage.

---

## Coverage Areas

1. Valid Login  
Verify user can login with correct email and password.

2. Invalid Password  
Verify login fails when incorrect password is entered.

3. Invalid Email Format  
Verify system rejects improperly formatted email addresses.

4. Empty Email Field  
Verify login fails when email field is empty.

5. Empty Password Field  
Verify login fails when password field is empty.

6. Account Lock After Failed Attempts  
Verify account becomes locked after defined number of failed login attempts.

7. Logout Functionality  
Verify user can logout successfully after login.

8. Locked Account Login Attempt  
Verify login is rejected when account is locked.

---

## Purpose

The purpose of this coverage map is to ensure that critical login functionality and edge cases are included in the test suite and no important area is missed during testing.
