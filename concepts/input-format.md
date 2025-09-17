---
title: Input data format | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/input-format
crawled_at: 2025-09-17T14:27:11.099350
---

Find out more
# Input data format
The input data structures of the POST method are passed in the request body.
The input data format is JSON.
The format of the input data is specified in the HTTP header. `Content-Type`: `application/json`.
The input data format must match [the response format](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/result-format). Therefore, in the title `Content-Type` set the same format as in the header. `Accept` or in the request URL (extension `.json`).
Required encoding of the request: UTF-8.
If the request does not specify a header `Content-Type` The Market automatically detects the data format. The service returns the HTTP status `400 Bad Request` in the following cases:
  * the transmitted data is invalid.
  * the data structure contains errors.
  * the request body uses an incorrect encoding (other than UTF-8).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/input-format#read-more)Find out more
Copied
### Was the article helpful?
YesNo
Previous
[Calling methods](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/method-call)
Next
[Response format](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/result-format)
