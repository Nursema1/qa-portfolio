# API Authentication Intro — Day 15

## Concepts (Kavramlar)
- Authentication (Kimlik doğrulama): Who are you?
- Authorization (Yetkilendirme): Are you allowed?

## Practice (Uygulama)
Request: GET https://httpbin.org/headers
Header added: x-api-key: test123
Expected: Response should echo the header back under "headers".

## Status codes (Durum kodları)
- 401 Unauthorized (Yetkisiz / kimlik doğrulama yok/başarısız)
- 403 Forbidden (Erişim yasak / yetki yok)
