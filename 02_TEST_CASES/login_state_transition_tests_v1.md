TC-015
Title:
Verify user can login from logged out state

Steps:
1 open login page
2 enter valid email and password
3 click login

Expected result:
User is successfully logged in
State changes to Logged In


TC-016
Title:
Verify invalid login keeps user in logged out state

Steps:
1 open login page
2 enter valid email
3 enter wrong password
4 click login

Expected result:
Login fails
User remains in Logged Out state


TC-017
Title:
Verify user can logout from logged in state

Steps:
1 login successfully
2 click logout

Expected result:
User is logged out
State changes to Logged Out


TC-018
Title:
Verify account becomes locked after 5 failed attempts

Steps:
1 enter wrong password 5 times

Expected result:
Account becomes locked
State changes to Locked


TC-019
Title:
Verify locked account cannot login

Steps:
1 lock account with 5 failed attempts
2 attempt login with correct password

Expected result:
Login is rejected
Account remains in Locked state
