# Day 9 — API Requests

## Request 1
GET https://api.github.com
Status: 200
Check: API root data returned

## Request 2 (Negative)
GET https://api.github.com/users/this_user_does_not_exist_123456
Status: 404
Check: User not found response returned
