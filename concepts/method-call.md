---
title: Calling methods | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/method-call
crawled_at: 2025-09-17T14:23:09.791460
---

Calling methods
# Calling methods
Requests to the Yandex.Market API for sellers are transmitted over HTTPS, the timeout is 10 seconds, and Keep-Alive is not supported.
Requests can be set in two formats — with and without specifying the API version. Both formats are equally supported.
Indicating the version
Without specifying the version
```
<http_method> https://api.partner.market.yandex.ru/v<version>/<resource>.<format>?<parameters>

```

where:
  * `<http_method>` ― DELETE, GET, POST or PUT.
  * `<version>` ― the number of the current API version. At the moment, the current version is 2.
  * `<resource>` ― The URL of the resource that the action is being performed on. The names of the resources are given in the description of the corresponding methods.
This is where the path parameters are passed — data that differs depending on the store or cabinet.
Example
```
https://api.partner.market.yandex.ru/campaigns/{campaignId}

```

`/{campaignId}` — the path parameter where you specify your campaign ID.
  * `<format>` ― this is an optional part of the request that affects the way the response is presented. The response format can be specified in the HTTP header. `Accept`. The data is transmitted in JSON format. The description of each method contains examples of requests and responses.
  * `<query parameters>` ― required and optional request parameters.
This is where the key and its value are transmitted, which are needed to refine the request, filter and sort incoming information, and paginate.
The request parameters are separated from the resource URL by a question mark, and an ampersand (&) is used between the key-value pairs.
Example
```
https://api.partner.market.yandex.ru/reports/shows-sales/generate?format=CSV

```

`?format=CSV` — request parameter.


```
<http_method> https://api.partner.market.yandex.ru/<resource>.<format>?<parameters>

```

where:
  * `<http_method>` ― DELETE, GET, POST or PUT.
  * `<resource>` ― The URL of the resource that the action is being performed on. The names of the resources are given in the description of the corresponding methods.
This is where the path parameters are passed — data that differs depending on the store or cabinet.
Example
```
https://api.partner.market.yandex.ru/campaigns/{campaignId}

```

`/{campaignId}` — the path parameter where you specify your campaign ID.
  * `<format>` ― this is an optional part of the request that affects the way the response is presented. The response format can be specified in the HTTP header. `Accept`. The data is transmitted in JSON format. The description of each method contains examples of requests and responses.
  * `<query parameters>` ― required and optional request parameters.
This is where the key and its value are transmitted, which are needed to refine the request, filter and sort incoming information, and paginate.
The request parameters are separated from the resource URL by a question mark, and an ampersand (&) is used between the key-value pairs.
Example
```
https://api.partner.market.yandex.ru/reports/shows-sales/generate?format=CSV

```

`?format=CSV` — request parameter.


**For sellers of the Yandex Go Market:** also read [instructions](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/market-yandex-go-sellers#method-call).
If an error occurs, processing of the request is stopped and information about it is returned. [Types of errors and what to do about them](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes)
Copied
### Was the article helpful?
YesNo
Previous
[OAuth 2.0 (deprecated)](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0)
Next
[Input data format](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/input-format)
