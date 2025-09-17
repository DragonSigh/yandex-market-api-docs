---
title: Processing orders with digital goods | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/digital
crawled_at: 2025-09-17T14:44:05.607438
---

Processing orders with digital goods
# Processing orders with digital goods
  1. Get a list of orders using the method [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrders). If the order contains digital goods, in the shipping information `delivery` in the parameter `type` the value will return `DIGITAL`.
  2. After the order status changes `PROCESSING` within 30 minutes, use the method [POST v2/campaigns/{campaignId}/orders/{orderId}/deliverDigitalGoods](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/provideOrderDigitalCodes).
After completing the request, yandex.Market will send the buyer an email with the keys and description. If the email could not be delivered (for example, the buyer provided an incorrect email address), yandex.Market will send the keys to the buyer via chat. The order will be transferred to the final status `DELIVERED`.


Enable API notifications
Yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/reference/sendNotification) when a new order appears and its status changes.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/)
Copied
### Was the article helpful?
YesNo
Previous
[Order statuses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/concepts/dbs-order-status-model)
Next
[Business orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/business-info)
