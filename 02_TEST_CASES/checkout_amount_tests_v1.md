TC-010
Title:
Verify checkout amount accepts valid minimum value

Steps:
1 open checkout
2 enter amount 1
3 submit payment

Expected result:
Payment accepted

TC-011
Title:
Verify checkout amount accepts valid maximum value

Steps:
1 open checkout
2 enter amount 10000
3 submit payment

Expected result:
Payment accepted

TC-012
Title:
Verify checkout rejects amount below minimum value

Steps:
1 open checkout
2 enter amount 0
3 submit payment

Expected result:
System displays validation error 
Payment is not processed
Error message indicates minimum amount requirement

TC-013
Title:
Verify checkout rejects amount above maximum value

Steps:
1 open checkout
2 enter amount 10001
3 submit payment

Expected result:
Payment not accepted

TC-014
Title:
Title:
Verify checkout rejects non-numeric input for amount field

Steps:
1 open checkout
2 enter amount abc
3 submit payment

Expected result:
Payment not accepted
