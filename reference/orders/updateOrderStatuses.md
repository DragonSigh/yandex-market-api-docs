---
title: Massive changes in order statuses - Changing the order | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/updateOrderStatuses
crawled_at: 2025-09-17T14:30:42.650099
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body)
    * [OrderStateDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderstatedto)
    * [OrderStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderstatustype)
    * [OrderSubstatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#ordersubstatustype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body1)
    * [UpdateOrderStatusesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#updateorderstatusesdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype)
    * [UpdateOrderStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#updateorderstatusdto)
    * [OrderUpdateStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderupdatestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body7)


# Changing the statuses of multiple orders
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Changes the statuses of several orders.
Possible status changes:
  * If the store has confirmed and prepared the order for shipment, then the order from the status `"status": "PROCESSING"`and the processing stage `"substatus": "STARTED"` it needs to be converted to the status `"status": "PROCESSING"` and the processing stage `"substatus": "READY_TO_SHIP"`.
  * If the store has confirmed the order, but cannot fulfill it (for example, the product is listed in the database, but is not in stock or does not have the desired color), then the order status is `"status": "PROCESSING"` and the processing stage `"substatus": "STARTED"` it needs to be converted to the status `"status": "CANCELLED"` with the reason for the cancellation of the order `"substatus": "SHOP_FAILED"`.
  * If the store has prepared an order for shipment, but cannot complete it (for example, the last item was damaged or defective), then the order status is `"status": "PROCESSING"` and the processing stage `"substatus": "READY_TO_SHIP"` it needs to be converted to the status `"status": "CANCELLED"` with the reason for the cancellation of the order `"substatus": "SHOP_FAILED"`.

**, Limit:** 100,000 orders per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/status-update

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body)Body
application/json
```
{
    "orders": [
        {
            "id": 0,
            "status": "PLACING",
            "substatus": "RESERVATION_EXPIRED"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
orders* |  **Type:** [OrderStateDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderstatedto)[] The list of orders.  
Order information. _Min items:_ `1` _Max items:_ `30`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderstatedto)OrderStateDTO
Order information.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The order ID.  
status* |  **Type:** [OrderStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderstatustype) Order status:
  * `PLACING` — it is being processed, preparing for the reservation.
  * `RESERVED` — reserved, but under-booked.
  * `UNPAID` — issued, but not yet paid (if payment is selected at checkout).
  * `PROCESSING` — it is under processing.
  * `DELIVERY` — transferred to the delivery service.
  * `PICKUP` — delivered to the pick-up point.
  * `DELIVERED` — received by the buyer.
  * `CANCELLED` — cancelled.
  * `PENDING` — awaiting processing by the seller.
  * `PARTIALLY_RETURNED` — partially returned.
  * `RETURNED` — returned in full.
  * `UNKNOWN` — unknown status.

Other values may also be returned. You don't need to process them. _Enum:_ `PLACING`, `RESERVED`, `UNPAID`, `PROCESSING`, `DELIVERY`, `PICKUP`, `DELIVERED`, `CANCELLED`, `PENDING`, `PARTIALLY_RETURNED`, `RETURNED`, `UNKNOWN`  
substatus |  **Type:** [OrderSubstatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#ordersubstatustype) The stage of order processing (if it has the status `PROCESSING`) or the reason for the cancellation of the order (if it has the status `CANCELLED`).
  * Order values in the status `PROCESSING`:
    * `STARTED` — the order has been confirmed, and it can be processed.
    * `READY_TO_SHIP` — the order is collected and ready for shipment.
  * Order values in the status `CANCELLED`:
    * `RESERVATION_EXPIRED` — the customer did not complete the reserved order within 10 minutes.
    * `USER_NOT_PAID` — the buyer has not paid for the order (for the type of payment `PREPAID`) for 30 minutes.
    * `USER_UNREACHABLE` — couldn't contact the buyer. To cancel with this reason, the following conditions must be met:
      * at least 3 calls from 8 to 21 in the buyer's time zone;
      * the break between the first and third calls is at least 90 minutes;
      * the connection is no shorter than 5 seconds.
If at least one of these conditions is not met (except when the number is unavailable), you will not be able to cancel the order. A response with the error code 400 will be returned.
    * `USER_CHANGED_MIND` — the customer cancelled the order for personal reasons.
    * `USER_REFUSED_DELIVERY` — the buyer was not satisfied with the terms of delivery.
    * `USER_REFUSED_PRODUCT` — the product did not fit the buyer.
    * `SHOP_FAILED` — the store cannot complete the order.
    * `USER_REFUSED_QUALITY` — the buyer was not satisfied with the quality of the product.
    * `REPLACING_ORDER` — the buyer decided to replace the product with another one on his own initiative.
    * `PROCESSING_EXPIRED` — the value is no longer used.
    * `PICKUP_EXPIRED` — the storage period of the order in the PVZ has expired.
    * `TOO_MANY_DELIVERY_DATE_CHANGES` — the order has been postponed too many times.
    * `TOO_LONG_DELIVERY` — the order is taking too long to be delivered.
    * `INCORRECT_PERSONAL_DATA` — incorrect personal data has been entered.
  * `TECHNICAL_ERROR` — a technical error on the Market's side. Contact support.

Other values may also be returned. You don't need to process them. _Enum:_ `RESERVATION_EXPIRED`, `USER_NOT_PAID`, `USER_UNREACHABLE`, `USER_CHANGED_MIND`, `USER_REFUSED_DELIVERY`, `USER_REFUSED_PRODUCT`, `SHOP_FAILED`, `USER_REFUSED_QUALITY`, `REPLACING_ORDER`, `PROCESSING_EXPIRED`, `PENDING_EXPIRED`, `SHOP_PENDING_CANCELLED`, `PENDING_CANCELLED`, `USER_FRAUD`, `RESERVATION_FAILED`, `USER_PLACED_OTHER_ORDER`, `USER_BOUGHT_CHEAPER`, `MISSING_ITEM`, `BROKEN_ITEM`, `WRONG_ITEM`, `PICKUP_EXPIRED`, `DELIVERY_PROBLEMS`, `LATE_CONTACT`, `CUSTOM`, `DELIVERY_SERVICE_FAILED`, `WAREHOUSE_FAILED_TO_SHIP`, `DELIVERY_SERVICE_UNDELIVERED`, `PREORDER`, `AWAIT_CONFIRMATION`, `STARTED`, `PACKAGING`, `READY_TO_SHIP`, `SHIPPED`, `ASYNC_PROCESSING`, `WAITING_USER_INPUT`, `WAITING_BANK_DECISION`, `BANK_REJECT_CREDIT_OFFER`, `CUSTOMER_REJECT_CREDIT_OFFER`, `CREDIT_OFFER_FAILED`, `AWAIT_DELIVERY_DATES_CONFIRMATION`, `SERVICE_FAULT`, `DELIVERY_SERVICE_RECEIVED`, `USER_RECEIVED`, `WAITING_FOR_STOCKS`, `AS_PART_OF_MULTI_ORDER`, `READY_FOR_LAST_MILE`, `LAST_MILE_STARTED`, `ANTIFRAUD`, `DELIVERY_USER_NOT_RECEIVED`, `DELIVERY_SERVICE_DELIVERED`, `DELIVERED_USER_NOT_RECEIVED`, `USER_WANTED_ANOTHER_PAYMENT_METHOD`, `USER_RECEIVED_TECHNICAL_ERROR`, `USER_FORGOT_TO_USE_BONUS`, `DELIVERY_SERVICE_NOT_RECEIVED`, `DELIVERY_SERVICE_LOST`, `SHIPPED_TO_WRONG_DELIVERY_SERVICE`, `DELIVERED_USER_RECEIVED`, `WAITING_TINKOFF_DECISION`, `COURIER_SEARCH`, `COURIER_FOUND`, `COURIER_IN_TRANSIT_TO_SENDER`, `COURIER_ARRIVED_TO_SENDER`, `COURIER_RECEIVED`, `COURIER_NOT_FOUND`, `COURIER_NOT_DELIVER_ORDER`, `COURIER_RETURNS_ORDER`, `COURIER_RETURNED_ORDER`, `WAITING_USER_DELIVERY_INPUT`, `PICKUP_SERVICE_RECEIVED`, `PICKUP_USER_RECEIVED`, `CANCELLED_COURIER_NOT_FOUND`, `COURIER_NOT_COME_FOR_ORDER`, `DELIVERY_NOT_MANAGED_REGION`, `INCOMPLETE_CONTACT_INFORMATION`, `INCOMPLETE_MULTI_ORDER`, `INAPPROPRIATE_WEIGHT_SIZE`, `TECHNICAL_ERROR`, `SORTING_CENTER_LOST`, `COURIER_SEARCH_NOT_STARTED`, `LOST`, `AWAIT_PAYMENT`, `AWAIT_LAVKA_RESERVATION`, `USER_WANTS_TO_CHANGE_ADDRESS`, `FULL_NOT_RANSOM`, `PRESCRIPTION_MISMATCH`, `DROPOFF_LOST`, `DROPOFF_CLOSED`, `DELIVERY_TO_STORE_STARTED`, `USER_WANTS_TO_CHANGE_DELIVERY_DATE`, `WRONG_ITEM_DELIVERED`, `DAMAGED_BOX`, `AWAIT_DELIVERY_DATES`, `LAST_MILE_COURIER_SEARCH`, `PICKUP_POINT_CLOSED`, `LEGAL_INFO_CHANGED`, `USER_HAS_NO_TIME_TO_PICKUP_ORDER`, `DELIVERY_CUSTOMS_ARRIVED`, `DELIVERY_CUSTOMS_CLEARED`, `FIRST_MILE_DELIVERY_SERVICE_RECEIVED`, `AWAIT_AUTO_DELIVERY_DATES`, `AWAIT_USER_PERSONAL_DATA`, `NO_PERSONAL_DATA_EXPIRED`, `CUSTOMS_PROBLEMS`, `AWAIT_CASHIER`, `WAITING_POSTPAID_BUDGET_RESERVATION`, `AWAIT_SERVICEABLE_CONFIRMATION`, `POSTPAID_BUDGET_RESERVATION_FAILED`, `AWAIT_CUSTOM_PRICE_CONFIRMATION`, `READY_FOR_PICKUP`, `TOO_MANY_DELIVERY_DATE_CHANGES`, `TOO_LONG_DELIVERY`, `DEFERRED_PAYMENT`, `POSTPAID_FAILED`, `INCORRECT_PERSONAL_DATA`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderstatustype)OrderStatusType
Order status:
  * `PLACING` — it is being processed, preparing for the reservation.
  * `RESERVED` — reserved, but under-booked.
  * `UNPAID` — issued, but not yet paid (if payment is selected at checkout).
  * `PROCESSING` — it is under processing.
  * `DELIVERY` — transferred to the delivery service.
  * `PICKUP` — delivered to the pick-up point.
  * `DELIVERED` — received by the buyer.
  * `CANCELLED` — cancelled.
  * `PENDING` — awaiting processing by the seller.
  * `PARTIALLY_RETURNED` — partially returned.
  * `RETURNED` — returned in full.
  * `UNKNOWN` — unknown status.


Other values may also be returned. You don't need to process them.
**Type** |  **Description**  
---|---  
[OrderStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderstatustype) |  _Enum:_ `PLACING`, `RESERVED`, `UNPAID`, `PROCESSING`, `DELIVERY`, `PICKUP`, `DELIVERED`, `CANCELLED`, `PENDING`, `PARTIALLY_RETURNED`, `RETURNED`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#ordersubstatustype)OrderSubstatusType
The stage of order processing (if it has the status `PROCESSING`) or the reason for the cancellation of the order (if it has the status `CANCELLED`).
  * Order values in the status `PROCESSING`:
    * `STARTED` — the order has been confirmed, and it can be processed.
    * `READY_TO_SHIP` — the order is collected and ready for shipment.
  * Order values in the status `CANCELLED`:
    * `RESERVATION_EXPIRED` — the customer did not complete the reserved order within 10 minutes.
    * `USER_NOT_PAID` — the buyer has not paid for the order (for the type of payment `PREPAID`) for 30 minutes.
    * `USER_UNREACHABLE` — couldn't contact the buyer. To cancel with this reason, the following conditions must be met:
      * at least 3 calls from 8 to 21 in the buyer's time zone;
      * the break between the first and third calls is at least 90 minutes;
      * the connection is no shorter than 5 seconds.
If at least one of these conditions is not met (except when the number is unavailable), you will not be able to cancel the order. A response with the error code 400 will be returned.
    * `USER_CHANGED_MIND` — the customer cancelled the order for personal reasons.
    * `USER_REFUSED_DELIVERY` — the buyer was not satisfied with the terms of delivery.
    * `USER_REFUSED_PRODUCT` — the product did not fit the buyer.
    * `SHOP_FAILED` — the store cannot complete the order.
    * `USER_REFUSED_QUALITY` — the buyer was not satisfied with the quality of the product.
    * `REPLACING_ORDER` — the buyer decided to replace the product with another one on his own initiative.
    * `PROCESSING_EXPIRED` — the value is no longer used.
    * `PICKUP_EXPIRED` — the storage period of the order in the PVZ has expired.
    * `TOO_MANY_DELIVERY_DATE_CHANGES` — the order has been postponed too many times.
    * `TOO_LONG_DELIVERY` — the order is taking too long to be delivered.
    * `INCORRECT_PERSONAL_DATA` — incorrect personal data has been entered.
  * `TECHNICAL_ERROR` — a technical error on the Market's side. Contact support.


Other values may also be returned. You don't need to process them.
**Type** |  **Description**  
---|---  
[OrderSubstatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#ordersubstatustype) |  _Enum:_ `RESERVATION_EXPIRED`, `USER_NOT_PAID`, `USER_UNREACHABLE`, `USER_CHANGED_MIND`, `USER_REFUSED_DELIVERY`, `USER_REFUSED_PRODUCT`, `SHOP_FAILED`, `USER_REFUSED_QUALITY`, `REPLACING_ORDER`, `PROCESSING_EXPIRED`, `PENDING_EXPIRED`, `SHOP_PENDING_CANCELLED`, `PENDING_CANCELLED`, `USER_FRAUD`, `RESERVATION_FAILED`, `USER_PLACED_OTHER_ORDER`, `USER_BOUGHT_CHEAPER`, `MISSING_ITEM`, `BROKEN_ITEM`, `WRONG_ITEM`, `PICKUP_EXPIRED`, `DELIVERY_PROBLEMS`, `LATE_CONTACT`, `CUSTOM`, `DELIVERY_SERVICE_FAILED`, `WAREHOUSE_FAILED_TO_SHIP`, `DELIVERY_SERVICE_UNDELIVERED`, `PREORDER`, `AWAIT_CONFIRMATION`, `STARTED`, `PACKAGING`, `READY_TO_SHIP`, `SHIPPED`, `ASYNC_PROCESSING`, `WAITING_USER_INPUT`, `WAITING_BANK_DECISION`, `BANK_REJECT_CREDIT_OFFER`, `CUSTOMER_REJECT_CREDIT_OFFER`, `CREDIT_OFFER_FAILED`, `AWAIT_DELIVERY_DATES_CONFIRMATION`, `SERVICE_FAULT`, `DELIVERY_SERVICE_RECEIVED`, `USER_RECEIVED`, `WAITING_FOR_STOCKS`, `AS_PART_OF_MULTI_ORDER`, `READY_FOR_LAST_MILE`, `LAST_MILE_STARTED`, `ANTIFRAUD`, `DELIVERY_USER_NOT_RECEIVED`, `DELIVERY_SERVICE_DELIVERED`, `DELIVERED_USER_NOT_RECEIVED`, `USER_WANTED_ANOTHER_PAYMENT_METHOD`, `USER_RECEIVED_TECHNICAL_ERROR`, `USER_FORGOT_TO_USE_BONUS`, `DELIVERY_SERVICE_NOT_RECEIVED`, `DELIVERY_SERVICE_LOST`, `SHIPPED_TO_WRONG_DELIVERY_SERVICE`, `DELIVERED_USER_RECEIVED`, `WAITING_TINKOFF_DECISION`, `COURIER_SEARCH`, `COURIER_FOUND`, `COURIER_IN_TRANSIT_TO_SENDER`, `COURIER_ARRIVED_TO_SENDER`, `COURIER_RECEIVED`, `COURIER_NOT_FOUND`, `COURIER_NOT_DELIVER_ORDER`, `COURIER_RETURNS_ORDER`, `COURIER_RETURNED_ORDER`, `WAITING_USER_DELIVERY_INPUT`, `PICKUP_SERVICE_RECEIVED`, `PICKUP_USER_RECEIVED`, `CANCELLED_COURIER_NOT_FOUND`, `COURIER_NOT_COME_FOR_ORDER`, `DELIVERY_NOT_MANAGED_REGION`, `INCOMPLETE_CONTACT_INFORMATION`, `INCOMPLETE_MULTI_ORDER`, `INAPPROPRIATE_WEIGHT_SIZE`, `TECHNICAL_ERROR`, `SORTING_CENTER_LOST`, `COURIER_SEARCH_NOT_STARTED`, `LOST`, `AWAIT_PAYMENT`, `AWAIT_LAVKA_RESERVATION`, `USER_WANTS_TO_CHANGE_ADDRESS`, `FULL_NOT_RANSOM`, `PRESCRIPTION_MISMATCH`, `DROPOFF_LOST`, `DROPOFF_CLOSED`, `DELIVERY_TO_STORE_STARTED`, `USER_WANTS_TO_CHANGE_DELIVERY_DATE`, `WRONG_ITEM_DELIVERED`, `DAMAGED_BOX`, `AWAIT_DELIVERY_DATES`, `LAST_MILE_COURIER_SEARCH`, `PICKUP_POINT_CLOSED`, `LEGAL_INFO_CHANGED`, `USER_HAS_NO_TIME_TO_PICKUP_ORDER`, `DELIVERY_CUSTOMS_ARRIVED`, `DELIVERY_CUSTOMS_CLEARED`, `FIRST_MILE_DELIVERY_SERVICE_RECEIVED`, `AWAIT_AUTO_DELIVERY_DATES`, `AWAIT_USER_PERSONAL_DATA`, `NO_PERSONAL_DATA_EXPIRED`, `CUSTOMS_PROBLEMS`, `AWAIT_CASHIER`, `WAITING_POSTPAID_BUDGET_RESERVATION`, `AWAIT_SERVICEABLE_CONFIRMATION`, `POSTPAID_BUDGET_RESERVATION_FAILED`, `AWAIT_CUSTOM_PRICE_CONFIRMATION`, `READY_FOR_PICKUP`, `TOO_MANY_DELIVERY_DATE_CHANGES`, `TOO_LONG_DELIVERY`, `DEFERRED_PAYMENT`, `POSTPAID_FAILED`, `INCORRECT_PERSONAL_DATA`, `UNKNOWN`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#200-ok)200 OK
Information about updated order statuses is returned.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "orders": [
            {
                "id": 0,
                "status": "PLACING",
                "substatus": "RESERVATION_EXPIRED",
                "updateStatus": "OK",
                "errorDetails": "string"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [UpdateOrderStatusesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#updateorderstatusesdto) The list of orders whose status has been updated.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#updateorderstatusesdto)UpdateOrderStatusesDTO
The list of orders whose status has been updated.
**Name** |  **Description**  
---|---  
orders* |  **Type:** [UpdateOrderStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#updateorderstatusdto)[] A list with updated orders.  
The list of orders.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#updateorderstatusdto)UpdateOrderStatusDTO
The list of orders.
**Name** |  **Description**  
---|---  
errorDetails |  **Type:** string Error when changing the order status. It contains a description of the error and the order ID. Returned if the parameter `updateStatus` takes the value `ERROR`.  
id |  **Type:** integer<int64> The order ID.  
status |  **Type:** [OrderStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderstatustype) Order status:
  * `PLACING` — it is being processed, preparing for the reservation.
  * `RESERVED` — reserved, but under-booked.
  * `UNPAID` — issued, but not yet paid (if payment is selected at checkout).
  * `PROCESSING` — it is under processing.
  * `DELIVERY` — transferred to the delivery service.
  * `PICKUP` — delivered to the pick-up point.
  * `DELIVERED` — received by the buyer.
  * `CANCELLED` — cancelled.
  * `PENDING` — awaiting processing by the seller.
  * `PARTIALLY_RETURNED` — partially returned.
  * `RETURNED` — returned in full.
  * `UNKNOWN` — unknown status.

Other values may also be returned. You don't need to process them. _Enum:_ `PLACING`, `RESERVED`, `UNPAID`, `PROCESSING`, `DELIVERY`, `PICKUP`, `DELIVERED`, `CANCELLED`, `PENDING`, `PARTIALLY_RETURNED`, `RETURNED`, `UNKNOWN`  
substatus |  **Type:** [OrderSubstatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#ordersubstatustype) The stage of order processing (if it has the status `PROCESSING`) or the reason for the cancellation of the order (if it has the status `CANCELLED`).
  * Order values in the status `PROCESSING`:
    * `STARTED` — the order has been confirmed, and it can be processed.
    * `READY_TO_SHIP` — the order is collected and ready for shipment.
  * Order values in the status `CANCELLED`:
    * `RESERVATION_EXPIRED` — the customer did not complete the reserved order within 10 minutes.
    * `USER_NOT_PAID` — the buyer has not paid for the order (for the type of payment `PREPAID`) for 30 minutes.
    * `USER_UNREACHABLE` — couldn't contact the buyer. To cancel with this reason, the following conditions must be met:
      * at least 3 calls from 8 to 21 in the buyer's time zone;
      * the break between the first and third calls is at least 90 minutes;
      * the connection is no shorter than 5 seconds.
If at least one of these conditions is not met (except when the number is unavailable), you will not be able to cancel the order. A response with the error code 400 will be returned.
    * `USER_CHANGED_MIND` — the customer cancelled the order for personal reasons.
    * `USER_REFUSED_DELIVERY` — the buyer was not satisfied with the terms of delivery.
    * `USER_REFUSED_PRODUCT` — the product did not fit the buyer.
    * `SHOP_FAILED` — the store cannot complete the order.
    * `USER_REFUSED_QUALITY` — the buyer was not satisfied with the quality of the product.
    * `REPLACING_ORDER` — the buyer decided to replace the product with another one on his own initiative.
    * `PROCESSING_EXPIRED` — the value is no longer used.
    * `PICKUP_EXPIRED` — the storage period of the order in the PVZ has expired.
    * `TOO_MANY_DELIVERY_DATE_CHANGES` — the order has been postponed too many times.
    * `TOO_LONG_DELIVERY` — the order is taking too long to be delivered.
    * `INCORRECT_PERSONAL_DATA` — incorrect personal data has been entered.
  * `TECHNICAL_ERROR` — a technical error on the Market's side. Contact support.

Other values may also be returned. You don't need to process them. _Enum:_ `RESERVATION_EXPIRED`, `USER_NOT_PAID`, `USER_UNREACHABLE`, `USER_CHANGED_MIND`, `USER_REFUSED_DELIVERY`, `USER_REFUSED_PRODUCT`, `SHOP_FAILED`, `USER_REFUSED_QUALITY`, `REPLACING_ORDER`, `PROCESSING_EXPIRED`, `PENDING_EXPIRED`, `SHOP_PENDING_CANCELLED`, `PENDING_CANCELLED`, `USER_FRAUD`, `RESERVATION_FAILED`, `USER_PLACED_OTHER_ORDER`, `USER_BOUGHT_CHEAPER`, `MISSING_ITEM`, `BROKEN_ITEM`, `WRONG_ITEM`, `PICKUP_EXPIRED`, `DELIVERY_PROBLEMS`, `LATE_CONTACT`, `CUSTOM`, `DELIVERY_SERVICE_FAILED`, `WAREHOUSE_FAILED_TO_SHIP`, `DELIVERY_SERVICE_UNDELIVERED`, `PREORDER`, `AWAIT_CONFIRMATION`, `STARTED`, `PACKAGING`, `READY_TO_SHIP`, `SHIPPED`, `ASYNC_PROCESSING`, `WAITING_USER_INPUT`, `WAITING_BANK_DECISION`, `BANK_REJECT_CREDIT_OFFER`, `CUSTOMER_REJECT_CREDIT_OFFER`, `CREDIT_OFFER_FAILED`, `AWAIT_DELIVERY_DATES_CONFIRMATION`, `SERVICE_FAULT`, `DELIVERY_SERVICE_RECEIVED`, `USER_RECEIVED`, `WAITING_FOR_STOCKS`, `AS_PART_OF_MULTI_ORDER`, `READY_FOR_LAST_MILE`, `LAST_MILE_STARTED`, `ANTIFRAUD`, `DELIVERY_USER_NOT_RECEIVED`, `DELIVERY_SERVICE_DELIVERED`, `DELIVERED_USER_NOT_RECEIVED`, `USER_WANTED_ANOTHER_PAYMENT_METHOD`, `USER_RECEIVED_TECHNICAL_ERROR`, `USER_FORGOT_TO_USE_BONUS`, `DELIVERY_SERVICE_NOT_RECEIVED`, `DELIVERY_SERVICE_LOST`, `SHIPPED_TO_WRONG_DELIVERY_SERVICE`, `DELIVERED_USER_RECEIVED`, `WAITING_TINKOFF_DECISION`, `COURIER_SEARCH`, `COURIER_FOUND`, `COURIER_IN_TRANSIT_TO_SENDER`, `COURIER_ARRIVED_TO_SENDER`, `COURIER_RECEIVED`, `COURIER_NOT_FOUND`, `COURIER_NOT_DELIVER_ORDER`, `COURIER_RETURNS_ORDER`, `COURIER_RETURNED_ORDER`, `WAITING_USER_DELIVERY_INPUT`, `PICKUP_SERVICE_RECEIVED`, `PICKUP_USER_RECEIVED`, `CANCELLED_COURIER_NOT_FOUND`, `COURIER_NOT_COME_FOR_ORDER`, `DELIVERY_NOT_MANAGED_REGION`, `INCOMPLETE_CONTACT_INFORMATION`, `INCOMPLETE_MULTI_ORDER`, `INAPPROPRIATE_WEIGHT_SIZE`, `TECHNICAL_ERROR`, `SORTING_CENTER_LOST`, `COURIER_SEARCH_NOT_STARTED`, `LOST`, `AWAIT_PAYMENT`, `AWAIT_LAVKA_RESERVATION`, `USER_WANTS_TO_CHANGE_ADDRESS`, `FULL_NOT_RANSOM`, `PRESCRIPTION_MISMATCH`, `DROPOFF_LOST`, `DROPOFF_CLOSED`, `DELIVERY_TO_STORE_STARTED`, `USER_WANTS_TO_CHANGE_DELIVERY_DATE`, `WRONG_ITEM_DELIVERED`, `DAMAGED_BOX`, `AWAIT_DELIVERY_DATES`, `LAST_MILE_COURIER_SEARCH`, `PICKUP_POINT_CLOSED`, `LEGAL_INFO_CHANGED`, `USER_HAS_NO_TIME_TO_PICKUP_ORDER`, `DELIVERY_CUSTOMS_ARRIVED`, `DELIVERY_CUSTOMS_CLEARED`, `FIRST_MILE_DELIVERY_SERVICE_RECEIVED`, `AWAIT_AUTO_DELIVERY_DATES`, `AWAIT_USER_PERSONAL_DATA`, `NO_PERSONAL_DATA_EXPIRED`, `CUSTOMS_PROBLEMS`, `AWAIT_CASHIER`, `WAITING_POSTPAID_BUDGET_RESERVATION`, `AWAIT_SERVICEABLE_CONFIRMATION`, `POSTPAID_BUDGET_RESERVATION_FAILED`, `AWAIT_CUSTOM_PRICE_CONFIRMATION`, `READY_FOR_PICKUP`, `TOO_MANY_DELIVERY_DATE_CHANGES`, `TOO_LONG_DELIVERY`, `DEFERRED_PAYMENT`, `POSTPAID_FAILED`, `INCORRECT_PERSONAL_DATA`, `UNKNOWN`  
updateStatus |  **Type:** [OrderUpdateStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderupdatestatustype) Update status. _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderupdatestatustype)OrderUpdateStatusType
Has the order status changed:
  * `OK` — the status has been changed.
  * `ERROR` — the status has not been changed. In this case, an error message will appear in the parameter `errorDetails`.

**Type** |  **Description**  
---|---  
[OrderUpdateStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#orderupdatestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body2)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body3)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body4)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body5)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body6)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#body7)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "orders": [ { "id": 0, "status": "PLACING", "substatus": "RESERVATION_EXPIRED" } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Changing the status of an order](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatus)
Next
[Transmission of marking codes](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers)
