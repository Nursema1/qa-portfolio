# API Assertions — Day 16 (GitHub)

## Endpoint
GET https://api.github.com/users/defunkt

## Assertions (Doğrulamalar)
- Status code is 200 (Durum kodu 200)
- type is "User" (type alanı "User")
- user_view_type exists (user_view_type alanı var)
- site_admin is boolean (site_admin true/false)
- name is a string or null (name string veya null olabilir)
- email can be null (email null olabilir — private/public setting)

## Notes (Notlar)
Null values are not always bugs; they can be expected based on privacy settings.
(null değerler her zaman bug değildir; gizlilik ayarlarından kaynaklanabilir)
