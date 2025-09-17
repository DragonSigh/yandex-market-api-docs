---
title: Request and response data format | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/concepts/data-format
crawled_at: 2025-09-17T14:45:02.051949
---

Find out more
# Request and response data format
The Market's requests to the store use only data in the JSON format. The store's response data must be presented in the same format.
The data format is specified in the HTTP header. `Content-Type: application/json`.
Required encoding of the request and response: UTF-8.
Request body example
```
{
  "notificationType": "PING",
  "time": "2025-01-16T10:09:49.759084017Z"
}

```

Example of the response body
```
{
  "version": "1.0.0",
  "name": "name",
  "time": "2025-01-16T10:09:49.759084017Z"
}

```

##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/concepts/en/push-notifications/concepts/data-format#read-more)Find out more
Copied
### Was the article helpful?
YesNo
Previous
[Integration on Node.js Express](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/concepts/en/push-notifications/concepts/quick-start-notifications-node-express)
Next
[Error messages](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/concepts/en/push-notifications/concepts/error-codes)
