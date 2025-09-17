---
title: Restrictions on requests | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/limits
crawled_at: 2025-09-17T14:26:38.513107
---

Global restrictions
# Restrictions on requests
  * [Global restrictions](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits#global)
  * [Resource constraints](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits#resource)
  * [Functional limitations](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits#functional)


Restrictions for requests to the Yandex.Market API for sellers are divided into the following types:
  * global restrictions (limits on the number of simultaneous requests);
  * resource restrictions (restrictions on the number of requests to the same resource over a long period of time, for example, per day);
  * functional limitations (restrictions on the amount of data to be sent or returned in a single request).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits#global)Global restrictions
They apply to the number of simultaneous (parallel) requests from a single login. It is allowed to run no more than two simultaneous requests.
If the limit is exceeded, the server returns a special HTTP code. `420 Enhance Your Calm` with an explanatory message:
```
Hit rate limit of 2 parallel requests

```

##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits#resource)Resource constraints
They affect the volume of requests to the same API resource over a long period of time from a single login. Query volume refers to the number of requests and the amount of data sent or returned per request.
For most resources, the restrictions apply only to the number of requests. These restrictions are individual for each resource.
For other resources, restrictions apply to the total amount of data sent or returned in requests to the same resource. These limits are calculated individually for each cabinet or store. The criteria for calculating restrictions are specified in the descriptions of such resources. Restrictions are recalculated with a delay of two to eight hours.
Some resources are grouped into groups with a common resource limit. In this case, restrictions apply to the volume of requests to any of the group's resources over a long period of time.
In each response to the request, the server returns special HTTP headers that indicate the status of the resource limit for the cabinet or store:
  * heading `X-RateLimit-Resource-Limit` contains the numeric value of the restriction.
  * heading `X-RateLimit-Resource-Until` contains the date until which the restriction applies, in the format `RFC822` (for example, `Thu, 10 Jul 2018 00:42:42 GMT`);
  * heading `X-RateLimit-Resource-Remaining` contains the numeric value of the amount of requests to this resource remaining before the limit is exceeded.


If the limit is exceeded, the server issues a special HTTP code. `420 Enhance Your Calm` with an explanatory message, for example:
```
Hit rate limit of 10 000 points per 1 day for resource /regions/{regionId}.json

```

##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits#functional)Functional limitations
They affect the amount of data sent or returned for a resource per request. The restrictions are individual for each resource, and their values are specified in the descriptions of the methods themselves.
In addition, there is a common restriction for all requests: the maximum size of the request body is 512 KB. If the volume is larger, split the request into several.
If the limit is exceeded, the server issues a special HTTP code. `400 Bad Request` with an explanatory message.
Copied
### Was the article helpful?
YesNo
Previous
[Types of errors and what to do about them](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes)
Next
[Pagination in queries](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/pagination)
