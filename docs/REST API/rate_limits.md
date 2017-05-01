# Rate Limits

The Globaldots API utilizes a rate limiting schema with per access token rate limit. If the rate limits are overstepped, requests will fail with a 503 error code. 
The quota is reset daily at UTC 00:00:00

## Access Token Rate Limit

- **Rate limit:** 10 requests per second
- **Burst limit:** 20 requests
- **Daily Quota:** 200 requests
This rate limit is applied per access token. Unauthenticated requests (those without an Authorization header) do not count against this limit. If multiple clients are making requests using the same access token, they will be subject to the same rate limit per token.

## Burst Limits

Burst limits allow clients to make extra requests over the rate limits. Requests made over the rate limit will still be processed immediately, but if the number of extra requests reaches the burst limit, any further requests will fail.
