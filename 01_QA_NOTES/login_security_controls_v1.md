# LOGIN SECURITY CONTROLS

Purpose:
Define security protections required for login systems.

Common security controls:

1. Rate limiting (İstek sınırlama)
Prevents too many login attempts in a short time.

2. Account lockout (Hesap kilitleme)
Account temporarily locked after multiple failed login attempts.

3. Progressive delay (Kademeli gecikme)
Each failed attempt increases waiting time.

4. Generic error messages (Genel hata mesajı)
System should not reveal whether email or password is incorrect.

Example:
Instead of:
"Password incorrect"

Use:
"Invalid credentials"
