---
title: How order statuses change | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/dbs-order-status-model
crawled_at: 2025-09-17T14:46:12.085590
---

How order statuses change
# How order statuses change
  * [Decoding the scheme](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/dbs-order-status-model#details)
  * [Substates when canceling an order](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/dbs-order-status-model#cancelled-substatuses)


The status change diagram shows the stages that a DBS order goes through and the logic of transitions between statuses. This will help you correlate the statuses of Yandex. Market and your system, set up integration with Yandex.Market correctly, and avoid transmitting unnecessary statuses and sub-statuses.
**Designations:**
  * The diagram shows the order statuses and substates at each stage in the format `Status of the Sub-status`. For example, `PROCESSING STARTED`.
List of substates `CANCELLED` see the section [Substates when canceling an order](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/dbs-order-status-model#cancelled-substatuses).
  * The arrows show the transitions between the stages, and their color indicates when this transition occurs:
    * green — the store has changed its status.
    * The blue Market has changed its status.
    * orange — cancellation of the order by one of the parties;
    * red is an exceptional case.


Transmit the statuses in the order in which they are described in the diagram.
Otherwise, it will lead to an error.
The order has been transferred for delivery
The order is cancelled
The order has been accepted at the pick-up point
The buyer has received the order
The order has been delivered
The order has been delivered
The order is cancelled
The order has been delivered
Delivery time has expired, the buyer has not received the order
Delivery time has expired, the buyer has not received the order
Request is processed
The arbitrator decides on cancellation
DELIVERED DELIVERED_USER_NOT_RECEIVED
CANCELLED Substatus
Request is processed
The arbitrator decides on cancellation
The order has been delivered
DELIVERY DELIVERY_USER_NOT_RECEIVED
CANCELLED Substatus
DELIVERED DELIVERY_SERVICE_DELIVERED
The buyer has created an order
PROCESSING STARTED
DELIVERY DELIVERY_SERVICE_RECEIVED
CANCELLED Substatus
PICKUP PICKUP_SERVICE_RECEIVED
DELIVERY USER_RECEIVED
DELIVERED DELIVERY_SERVICE_DELIVERED
CANCELLED Substatus
DELIVERED DELIVERY_SERVICE_DELIVERED
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/dbs-order-status-model#details)Decoding the scheme
**Status, sub-status, and stage description** |  **Who changes the status** |  **Methods by which the status is changed or information about the order is received in this status**  
---|---|---  
`PROCESSING`  
`STARTED` The store is processing the order. |  Yandex. Market |  [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrders) [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification)  
`DELIVERY`  
`DELIVERY_SERVICE_RECEIVED` The order has been delivered. |  Shop |  [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrders) [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification) [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/updateOrderStatus)  
`DELIVERY`  
`USER_RECEIVED` The customer received the order. It is transmitted only when working through Yandex. Delivery. |  Yandex. Market |  [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrders) [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification)  
`DELIVERY`  
`DELIVERY_USER_NOT_RECEIVED` The delivery time has expired, and the customer has not received the order. Arbitration begins, as a result of which the order can be canceled or transferred to the status `DELIVERED DELIVERY_SERVICE_DELIVERED`. |  Yandex. Market |  [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrders) [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification)  
`PICKUP`  
`PICKUP_SERVICE_RECEIVED` The order has been accepted at the PVZ. |  Shop |  [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/updateOrderStatus)  
`DELIVERED`  
`DELIVERY_SERVICE_DELIVERED` The order has been delivered. It is transmitted automatically when working through Yandex. Delivery. If you are delivering on your own, change the status after the order is delivered. |  Yandex. Market Shop |  [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrders) [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification) [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/updateOrderStatus)  
`DELIVERED`  
`DELIVERED_USER_NOT_RECEIVED` The delivery time has expired, and the customer has not received the order. Arbitration begins, as a result of which the order can be canceled or remain in the same status. |  Yandex. Market |  [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrders) [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification)  
`CANCELLED`  
[Substates](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/dbs-order-status-model#cancelled-substatuses) The order has been cancelled. To cancel an order, pass the sub-status `SHOP_FAILED`. If the order is in the status `DELIVERY` or `PICKUP` and the buyer cancelled it., _confirm the cancellation_. |  Yandex. Market Shop Buyer |  [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrders) [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification) [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/updateOrderStatus)  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/dbs-order-status-model#cancelled-substatuses)Substates when canceling an order
  * `RESERVATION_EXPIRED` — the customer did not complete the reserved order within 10 minutes.
  * `USER_NOT_PAID` — the buyer has not paid for the order (for the type of payment `PREPAID`) for 30 minutes.
  * `USER_UNREACHABLE` — couldn't contact the buyer.
  * `USER_CHANGED_MIND` — the customer cancelled the order for personal reasons.
  * `USER_REFUSED_DELIVERY` — the buyer was not satisfied with the terms of delivery.
  * `USER_REFUSED_PRODUCT` — the product did not fit the buyer.
  * `SHOP_FAILED` — the store cannot complete the order.
  * `USER_REFUSED_QUALITY` — the buyer was not satisfied with the quality of the product.
  * `REPLACING_ORDER` — the buyer decided to replace the product with another one on his own initiative.
  * `PROCESSING_EXPIRED` — the value is no longer used.
  * `PICKUP_EXPIRED` — the storage period of the order in the PVZ has expired.
  * `TOO_MANY_DELIVERY_DATE_CHANGES` — the order has been postponed too many times.
  * `DELIVERY_DATE_CHANGED_TOO_MUCH` — the order has been postponed for too many days.


Other values may also be returned. You don't need to process them.
[PUT v2/campaigns/{campaignId}/orders/{orderId}/cancellation/accept](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/acceptOrderCancellation)
Copied
### Was the article helpful?
YesNo
Previous
[Express orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/step-by-step/express)
Next
[Digital orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/step-by-step/digital)
