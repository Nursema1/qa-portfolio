# BR-001 — Missing Account Lockout After Multiple Failed Login Attempts

## Summary
Login system does not temporarily lock the account after multiple failed login attempts.

## Environment
Web Application  
Browser: Chrome (latest)  
Environment: Test / Staging

## Preconditions
- Valid user account exists
- Login page is accessible

## Steps to Reproduce
1. Open login page
2. Enter valid email
3. Enter incorrect password
4. Repeat login attempt multiple times (example: 5–10 attempts)

## Expected Result
- System temporarily locks the account after defined number of failed attempts
- User cannot login for a defined period
- System shows message such as: "Account temporarily locked"

## Actual Result
- System allows unlimited login attempts
- No account lockout mechanism triggered

## Severity
High

## Priority
P1

## Status
NEW

## Evidence
(To be added: screenshot / log / request capture)

## Notes
Missing account lockout increases risk of brute force attacks.

---

## TR Açıklama

Özet:
Çok sayıda başarısız login denemesinden sonra hesap kilitlenmiyor.

Risk:
Bu durum brute force saldırılarını mümkün kılar.

Beklenen:
Belirli sayıda başarısız girişten sonra hesap geçici olarak kilitlenmelidir.
