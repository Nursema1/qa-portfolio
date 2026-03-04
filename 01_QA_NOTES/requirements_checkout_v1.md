# Checkout Reqirements ( Ödeme Gereksinimleri )

## Functional Requirements

1. Card number must not be empty 
(Kart numarası boş bırakılamaz)

2. Cart number must follow valid format
(Kart numarası geçerli formatta olmalıdır)

3. Expired cards must be rejected
(Süresi dolmuş kartlar reddedilmelidir)

4. İnvalid card number must not be accepted
(Geçersiz kart numarası kabul edilmemelidir) 

5. Payment request must be processed only for authenticated users
( Ödeme isteği sadece giriş yapmış kullanıcılar için çalışmalıdır.

---

## Validation Rules

6. Card number lenght must be validated
(Kart numarası uzunluğu kontrol edilmelidir)

7. Required fields must not empty 
(Zorunlu alanlar boş bırakılmaz)

---

## Security Expectations

8. Payment attempts must be logged 
(Ödeme denemeleri loglanmalıdır)

9. Sensitive payment data must not be exposed in error messages
( Hassas ödeme verileri hata mesajlarında gösterilmelidir)

10. Pyment endpoint must return correct HTTP status codes
    (Ödeme endpointi doğru HTTP status kodları döndürmelidir)
