# LOGIN SECURITY TEST CASES

Purpose:
Verify security protections implemented for login functionality.

---

## TC-006 — Account Lockout After Multiple Failed Attempts

Precondition:
User account exists

Steps:
1. Open login page
2. Enter valid email
3. Enter incorrect password
4. Repeat login attempt multiple times (example: 5 attempts)

Expected Result:
- Account is temporarily locked
- User cannot login for a defined period
- System shows a message such as "Account temporarily locked"

TR Açıklama:
Bir kullanıcı çok sayıda yanlış giriş yaparsa sistem hesabı geçici olarak kilitlemelidir.

---

## TC-007 — Rate Limiting on Login Requests

Precondition:
Login endpoint is available

Steps:
1. Send multiple login requests quickly
2. Repeat login attempts within a short time

Expected Result:
- System slows down login attempts
- System blocks or limits requests
- Too many attempts response may be returned

TR Açıklama:
Kısa sürede çok fazla login isteği gönderilirse sistem bunu sınırlamalıdır.

---

## TC-008 — Generic Error Message for Invalid Credentials

Precondition:
Login page is accessible

Steps:
1. Enter incorrect email
2. Enter incorrect password
3. Submit login request

Expected Result:
- System returns a generic error message
Example:
"Invalid credentials"

System must NOT reveal:
- whether email exists
- whether password is incorrect

TR Açıklama:
Sistem email mi yanlış password mü yanlış olduğunu söylememelidir.

---

## TC-009 — Password With Leading or Trailing Spaces

Precondition:
User account exists

Steps:
1. Enter valid email
2. Enter password with spaces at beginning or end
Example:
" password123 "

Expected Result:
- System either trims spaces
OR
- Rejects password as invalid format

TR Açıklama:
Şifre başında veya sonunda boşluk olduğunda sistem bunu doğru şekilde işlemelidir.

---

## TC-010 — Progressive Delay After Failed Attempts

Precondition:
Login page accessible

Steps:
1. Enter valid email
2. Enter incorrect password
3. Repeat login attempts multiple times

Expected Result:
- Each failed login attempt increases waiting time
Example:
Attempt 1 → no delay  
Attempt 2 → 2 seconds  
Attempt 3 → 5 seconds

TR Açıklama:
Her başarısız girişten sonra bekleme süresi artmalıdır.
