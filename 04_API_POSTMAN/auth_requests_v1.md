## API-001 - Login with valid credentials

Endpoin:
POST /login

Request Body:
{
 ''email: ''user@test.com'',
 ''password'': ''correct_password''
 }

 Expected Status Code:
 200 

 Response Verification:
 - access_token field exists
 - token type is returned
 - user id exists

 ## API_002 - Login with invalid password

 Endpoint:
 POST /login 

 Requset Body:
 {
  ''email'': ''user@test.com'',
   ''password'': ''wrong_password''
   }

   Expected Status Code
   401

   Response Verification:
   - error message exists
   - login rejected

   ## API_003 - Login with empty email

   Endpoint:
   POST /login

   Request Body:
   {
    ''email'': '''',
    ''password'': ''123456''
    }
    
    Expected Status Code:
    400

    Response Verification:
    - validation error message returned

    ## API_004 - Access protected endpoint without token

    Endpoint:
    GET /admin
    
    Headers:
    Authorization: none

    Expected Status Code:
    401

    Response Verification:
    - acces denied message
