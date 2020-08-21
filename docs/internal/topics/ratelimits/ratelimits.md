---
title: Ratelimits
noTOC: true
---

The HTTP API implements a process for limiting and preventing spam requests. API users that regularly hit and ignore the limit will be blocked from our platform. These rate limits are in place to help prevent the abuse and overload of our services.
Rate limits are applied globally on all routes

###### Rate Limits Structure
| Route	| Request | Requests Allowed Per Minute | Punishment if Exceeded
|--------------|----------|--------------|--------------|
/bots/*	| ANY	| 60	| 1 Hour Block

---

## Exceeding a Rate Limit
If you exceed the set rate limit for the API you will receive a HTTP 429 and be blocked from posting to the API for one hour.

---

###### Rate Limit Response Structure
Field	| Type | Description
|--------------|----------|--------------|
retry-after	| integer	| Indicates how long the timeout period is/when you will be able to send requests again
