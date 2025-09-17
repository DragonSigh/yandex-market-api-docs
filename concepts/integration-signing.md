---
title: How to sign integrations | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/integration-signing
crawled_at: 2025-09-17T14:23:04.637473
---

How to sign integrations
# How to sign integrations
In the seller's account on the Market on the page **Query log** You can view information on the requests and responses, as well as on the issues related to them. To understand which integration the data belongs to, you need to sign:
  * **Requests** which you are sending to the Yandex.Market API. In the header, specify the name of the integration and its version, if any.
Format: `X-Market-Integration: integration name/version`.
For example, `X-Market-Integration: Bitrix` or `X-Market-Integration: Bitrix/1.0.0`.
  * **Answers** on [API notifications](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification) from Yandex. Market — provide the name of the integration and its version in the response to the request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification) in the parameters `name` and `version`.


The name of the integration is displayed on the page **Query log** in the block **Type of integrations**. You can also use a filter on this page. **Integration**. [Learn more about working with logs](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/debug)
**Name requirements:**
  * The maximum number of characters is 100.
  * ASCII characters only from 


Copied
### Was the article helpful?
YesNo
Previous
[How to use the console](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/console)
Next
[The OpenAPI Specification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi)
