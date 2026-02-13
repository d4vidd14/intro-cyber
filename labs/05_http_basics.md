# Lab: Basic HTTP observations

## Check headers + status code
curl -I https://example.com

## Test GET vs POST (example with httpbin)
curl -X GET "https://httpbin.org/get?user=test"
curl -X POST "https://httpbin.org/post" -d "user=test&pass=123"

## Notes
- Observe status codes and response headers.
- Do not send real credentials in tests.
