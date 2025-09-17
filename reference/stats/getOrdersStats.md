---
title: Detailed information on orders - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/getOrdersStats
crawled_at: 2025-09-17T14:36:03.262804
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body)
    * [OrderStatsStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#orderstatsstatustype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body1)
    * [OrdersStatsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype)
    * [OrdersStatsOrderDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsorderdto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#forwardscrollingpagerdto)
    * [OrdersStatsCommissionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatscommissiondto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#currencytype)
    * [OrdersStatsItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsitemdto)
    * [OrdersStatsPaymentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentdto)
    * [OrdersStatsDeliveryRegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdeliveryregiondto)
    * [OrdersStatsOrderPaymentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsorderpaymenttype)
    * [OrdersStatsSubsidyDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidydto)
    * [OrdersStatsCommissionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatscommissiontype)
    * [OrdersStatsDetailsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdetailsdto)
    * [OrdersStatsPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspricedto)
    * [OrdersStatsWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatswarehousedto)
    * [OrdersStatsPaymentOrderDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentorderdto)
    * [OrdersStatsPaymentSourceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentsourcetype)
    * [OrdersStatsPaymentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymenttype)
    * [OrdersStatsSubsidyOperationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidyoperationtype)
    * [OrdersStatsSubsidyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidytype)
    * [OrdersStatsItemStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsitemstatustype)
    * [OrdersStatsStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsstocktype)
    * [OrdersStatsPriceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspricetype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body7)


# Detailed information on orders
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about orders on the Market that contain your products.
You can use it to collect statistics on your orders and find out, for example, which of the products are most often returned by customers, which, on the contrary, are in high demand, etc.
Information on created or updated orders may appear with a delay of up to 40 minutes.
To get the data without delay, use [the method of obtaining information about orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/orders/getOrders).
You can get information on up to 200 orders in one request.
**, Limit:** 1,000,000 orders per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/stats/orders

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body)Body
application/json
```
{
    "dateFrom": "string",
    "dateTo": "string",
    "updateFrom": "string",
    "updateTo": "string",
    "orders": [
        0
    ],
    "statuses": [
        "CANCELLED_BEFORE_PROCESSING"
    ],
    "hasCis": false
}

```

**Name** |  **Description**  
---|---  
dateFrom |  **Type:** string<date> The initial date when the order was generated. Date format: `YYYY‑MM‑DD`. Cannot be used together with parameters `updateFrom` and `updateTo`.  
dateTo |  **Type:** string<date> The end date when the order was generated. Date format: `YYYY‑MM‑DD`. Cannot be used together with parameters `updateFrom` and `updateTo`.  
hasCis |  **Type:** boolean Do I need to return only those orders that contain at least one item with an identification code in the system? 
  * `true` - yes.
  * `false` - no. Such codes are assigned to products that are subject to labeling and belong to certain categories.

  
orders |  **Type:** integer<int64>[] List of order IDs.  
The list of products in the order after possible changes. During order processing, yandex.Market can delete items from it in case of problems in the warehouse or at the user's initiative.
  * If all items are deleted from the order, it will not be in the list. `items` — only in the list `initialItems`.
  * If there is at least one item left in the order, it will be in the list. `items` (with a reduced number of units `count`), and in the list `initialItems` (with the initial number of units `initialCount`).

_Min items:_ `1` _Unique items_  
statuses |  **Type:** [OrderStatsStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#orderstatsstatustype)[] List of order statuses.  
Current order status:
  * `CANCELLED_BEFORE_PROCESSING` — the order was cancelled before it was processed.
  * `CANCELLED_IN_DELIVERY` — the order is cancelled during its delivery.
  * `CANCELLED_IN_PROCESSING` — the order is cancelled during its processing.
  * `DELIVERY` — the order has been transferred to the delivery service.
  * `DELIVERED` — the order has been delivered.
  * `PARTIALLY_DELIVERED` — the order has been partially delivered. The order status can change to `PARTIALLY_DELIVERED` Not immediately If there was a non-purchase in the delivered order, the status will change only after the order is received at the Market warehouse.
  * `PARTIALLY_RETURNED` — the order has been partially refunded by the buyer.
  * `PENDING` — the order is awaiting confirmation.
  * `PICKUP` — the order has been delivered to the pick-up point.
  * `PROCESSING` — the order is in processing.
  * `RESERVED` — the product is reserved in the warehouse.
  * `RETURNED` — the order has been fully refunded by the buyer.
  * `UNKNOWN` — unknown order status.
  * `UNPAID` — an order from a legal entity is awaiting payment.
  * `LOST` — the order is lost.

_Enum:_ `CANCELLED_BEFORE_PROCESSING`, `CANCELLED_IN_DELIVERY`, `CANCELLED_IN_PROCESSING`, `DELIVERY`, `DELIVERED`, `PARTIALLY_DELIVERED`, `PARTIALLY_RETURNED`, `PENDING`, `PICKUP`, `PROCESSING`, `RESERVED`, `RETURNED`, `UNKNOWN`, `UNPAID`, `LOST` _Min items:_ `1` _Unique items_  
updateFrom |  **Type:** string<date> The start date of the period for which changes were made to the order (for example, status or payment information). Date format: `YYYY‑MM‑DD`. Cannot be used together with parameters `dateFrom` and `dateTo`.  
updateTo |  **Type:** string<date> The end date of the period for which the order was changed (for example, the status or payment information). Date format: `YYYY‑MM‑DD`. Cannot be used together with parameters `dateFrom` and `dateTo`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#orderstatsstatustype)OrderStatsStatusType
Current order status:
  * `CANCELLED_BEFORE_PROCESSING` — the order was cancelled before it was processed.
  * `CANCELLED_IN_DELIVERY` — the order is cancelled during its delivery.
  * `CANCELLED_IN_PROCESSING` — the order is cancelled during its processing.
  * `DELIVERY` — the order has been transferred to the delivery service.
  * `DELIVERED` — the order has been delivered.
  * `PARTIALLY_DELIVERED` — the order has been partially delivered.
The order status can change to `PARTIALLY_DELIVERED` Not immediately
If there was a non-purchase in the delivered order, the status will change only after the order is received at the Market warehouse.
  * `PARTIALLY_RETURNED` — the order was partially returned by the buyer.
  * `PENDING` — the order is awaiting confirmation.
  * `PICKUP` — the order has been delivered to the pick-up point.
  * `PROCESSING` — the order is in processing.
  * `RESERVED` — the product is reserved in the warehouse.
  * `RETURNED` — the order has been fully refunded by the buyer.
  * `UNKNOWN` — unknown order status.
  * `UNPAID` — an order from a legal entity is awaiting payment.
  * `LOST` — the order is lost.

**Type** |  **Description**  
---|---  
[OrderStatsStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#orderstatsstatustype) |  _Enum:_ `CANCELLED_BEFORE_PROCESSING`, `CANCELLED_IN_DELIVERY`, `CANCELLED_IN_PROCESSING`, `DELIVERY`, `DELIVERED`, `PARTIALLY_DELIVERED`, `PARTIALLY_RETURNED`, `PENDING`, `PICKUP`, `PROCESSING`, `RESERVED`, `RETURNED`, `UNKNOWN`, `UNPAID`, `LOST`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#200-ok)200 OK
Information about orders.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "orders": [
            {
                "id": 0,
                "creationDate": "string",
                "statusUpdateDate": "2022-12-29T18:02:01Z",
                "status": "CANCELLED_BEFORE_PROCESSING",
                "partnerOrderId": "string",
                "paymentType": "POSTPAID",
                "fake": false,
                "deliveryRegion": {
                    "id": 0,
                    "name": "string"
                },
                "items": [
                    {
                        "offerName": "string",
                        "marketSku": 0,
                        "shopSku": "string",
                        "count": 0,
                        "prices": [
                            {
                                "type": "BUYER",
                                "costPerItem": 0,
                                "total": 0
                            }
                        ],
                        "warehouse": {
                            "id": 0,
                            "name": "string"
                        },
                        "details": [
                            {
                                "itemStatus": "REJECTED",
                                "itemCount": 0,
                                "updateDate": "string",
                                "stockType": "FIT"
                            }
                        ],
                        "cisList": [
                            "string"
                        ],
                        "initialCount": 0,
                        "bidFee": 570,
                        "cofinanceThreshold": 0,
                        "cofinanceValue": 0
                    }
                ],
                "initialItems": [
                    {
                        "offerName": "string",
                        "marketSku": 0,
                        "shopSku": "string",
                        "count": 0,
                        "prices": [
                            {
                                "type": "BUYER",
                                "costPerItem": 0,
                                "total": 0
                            }
                        ],
                        "warehouse": {
                            "id": 0,
                            "name": "string"
                        },
                        "details": [
                            {
                                "itemStatus": "REJECTED",
                                "itemCount": 0,
                                "updateDate": "string",
                                "stockType": "FIT"
                            }
                        ],
                        "cisList": [
                            "string"
                        ],
                        "initialCount": 0,
                        "bidFee": 570,
                        "cofinanceThreshold": 0,
                        "cofinanceValue": 0
                    }
                ],
                "payments": [
                    {
                        "id": "string",
                        "date": "string",
                        "type": "PAYMENT",
                        "source": "BUYER",
                        "total": 0,
                        "paymentOrder": {
                            "id": "string",
                            "date": "string"
                        }
                    }
                ],
                "commissions": [
                    {
                        "type": "FEE",
                        "actual": 0
                    }
                ],
                "subsidies": [
                    {
                        "operationType": "ACCRUAL",
                        "type": "YANDEX_CASHBACK",
                        "amount": 0
                    }
                ],
                "currency": "RUR"
            }
        ],
        "paging": {
            "nextPageToken": "string"
        }
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OrdersStatsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdto) Information about orders.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdto)OrdersStatsDTO
Information about orders.
**Name** |  **Description**  
---|---  
orders* |  **Type:** [OrdersStatsOrderDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsorderdto)[] The list of orders.  
Order information.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsorderdto)OrdersStatsOrderDTO
Order information.
**Name** |  **Description**  
---|---  
commissions* |  **Type:** [OrdersStatsCommissionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatscommissiondto)[] Information about the cost of services.  
Information about the cost of services.  
currency* |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#currencytype) The currency in which the prices in the order are indicated. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
items* |  **Type:** [OrdersStatsItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsitemdto)[] The list of products in the order after possible changes. The order delivery information is added as a separate element in the array `items`— parameter `offerName` with the value `Delivery`.   
The list of products in the order after possible changes. During order processing, yandex.Market can delete items from it in case of problems in the warehouse or at the user's initiative.
  * If all the items are deleted from the order, it will not be in the list. `items` — only in the list `initialItems`.
  * If there is at least one item left in the order, it will be in the list. `items` (with a reduced number of units `count`), and in the list `initialItems` (with the initial number of units `initialCount`).

  
payments* |  **Type:** [OrdersStatsPaymentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentdto)[] Information about money transfers by order. It may return empty if there is no transfer data. For example, the order is canceled or payment is selected upon receipt (for the DBS model).   
Information about money transfers by order.  
creationDate |  **Type:** string<date> The date the order was created. Date format: `YYYY-MM-DD`.  
deliveryRegion |  **Type:** [OrdersStatsDeliveryRegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdeliveryregiondto) Information about the delivery region.  
fake |  **Type:** boolean Order type:
  * `false` — the real customer's order.
  * `true` — [test](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/concepts/sandbox) the Market order.

  
id |  **Type:** integer<int64> The order ID.  
initialItems |  **Type:** [OrdersStatsItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsitemdto)[] The list of products in the order. It is returned only if there has been a change in the quantity of goods.   
The list of products in the order after possible changes. During order processing, yandex.Market can delete items from it in case of problems in the warehouse or at the user's initiative.
  * If all items are deleted from the order, it will not be in the list. `items` — only in the list `initialItems`.
  * If there is at least one item left in the order, it will be in the list. `items` (with a reduced number of units `count`), and in the list `initialItems` (with the initial number of units `initialCount`).

_Min items:_ `1`  
partnerOrderId |  **Type:** string The order ID in the store's information system.  
paymentType |  **Type:** [OrdersStatsOrderPaymentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsorderpaymenttype) The type of payment for the order. _Enum:_ `POSTPAID`, `PREPAID`, `UNKNOWN`  
status |  **Type:** [OrderStatsStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#orderstatsstatustype) Current order status:
  * `CANCELLED_BEFORE_PROCESSING` — the order was cancelled before it was processed.
  * `CANCELLED_IN_DELIVERY` — the order is cancelled during its delivery.
  * `CANCELLED_IN_PROCESSING` — the order is cancelled during its processing.
  * `DELIVERY` — the order has been transferred to the delivery service.
  * `DELIVERED` — the order has been delivered.
  * `PARTIALLY_DELIVERED` — the order has been partially delivered. The order status can change to `PARTIALLY_DELIVERED` Not immediately If there was a non-purchase in the delivered order, the status will change only after the order is received at the Market warehouse.
  * `PARTIALLY_RETURNED` — the order was partially returned by the buyer.
  * `PENDING` — the order is awaiting confirmation.
  * `PICKUP` — the order has been delivered to the pick-up point.
  * `PROCESSING` — the order is in processing.
  * `RESERVED` — the product is reserved in the warehouse.
  * `RETURNED` — the order has been fully refunded by the buyer.
  * `UNKNOWN` — unknown order status.
  * `UNPAID` — an order from a legal entity is awaiting payment.
  * `LOST` — the order is lost.

_Enum:_ `CANCELLED_BEFORE_PROCESSING`, `CANCELLED_IN_DELIVERY`, `CANCELLED_IN_PROCESSING`, `DELIVERY`, `DELIVERED`, `PARTIALLY_DELIVERED`, `PARTIALLY_RETURNED`, `PENDING`, `PICKUP`, `PROCESSING`, `RESERVED`, `RETURNED`, `UNKNOWN`, `UNPAID`, `LOST`  
statusUpdateDate |  **Type:** string<date-time> The date and time when the order status was last changed. Date and time format: ISO 8601. For example, `2017-11-21T00:00:00`. The time zone is UTC+03:00 (Moscow).  
subsidies |  **Type:** [OrdersStatsSubsidyDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidydto)[] Accrual of points that are used to reduce the cost of placement, and their deduction in case of non-purchase or refund.  
Information about the accrual of points that are used to reduce the cost of placement, and their deduction in case of non-purchase or refund. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatscommissiondto)OrdersStatsCommissionDTO
Information about the cost of services.
**Name** |  **Description**  
---|---  
actual |  **Type:** number The amount that was billed at the time the order was created and that needs to be paid. The precision is two decimal places.  
type |  **Type:** [OrdersStatsCommissionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatscommissiontype) Service. _Enum:_ `FEE`, `FULFILLMENT`, `LOYALTY_PARTICIPATION_FEE`, `AUCTION_PROMOTION`, `INSTALLMENT`, `DELIVERY_TO_CUSTOMER`, `EXPRESS_DELIVERY_TO_CUSTOMER`, `AGENCY`, `PAYMENT_TRANSFER`, `RETURNED_ORDERS_STORAGE`, `SORTING`, `INTAKE_SORTING`, `RETURN_PROCESSING`, `ILLIQUID_GOODS_SALE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsitemdto)OrdersStatsItemDTO
The list of products in the order after possible changes.
During order processing, yandex.Market can delete items from it in case of problems in the warehouse or at the user's initiative.
  * If all the items are deleted from the order, it will not be in the list. `items` — only in the list `initialItems`.
  * If there is at least one item left in the order, it will be in the list. `items` (with a reduced number of units `count`), and in the list `initialItems` (with the initial number of units `initialCount`).

**Name** |  **Description**  
---|---  
bidFee |  **Type:** integer<int32> The deducted bid of the nearest competitor. It is indicated as a percentage of the cost of the product and multiplied by 100. For example, the 5% rate is indicated as 500. _Example:_ `570` _Min value:_ `0` _Max value:_ `10000`  
cisList |  **Type:** string[] List of product identification codes in the system   
_Min items:_ `1` _Unique items_  
cofinanceThreshold |  **Type:** number The threshold for discounts with Yandex.Market at the time of placing the order. [What is it?](https://yandex.ru/support/marketplace/marketing/smart-pricing.html#sponsored-discounts) The precision is two decimal places.  
cofinanceValue |  **Type:** number Discount with Yandex. Market. [What is it?](https://yandex.ru/support/marketplace/marketing/smart-pricing.html#sponsored-discounts) The precision is two decimal places.  
count |  **Type:** integer<int32> The number of product units, including deleted units. If all items are removed from the order, it will only be included in the list. `initialItems`.  
details |  **Type:** [OrdersStatsDetailsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdetailsdto)[] Information about the removal of the product from the order.  
Information about the removal of the product from the order. _Min items:_ `1`  
initialCount |  **Type:** integer<int32> The initial number of product units.  
marketSku |  **Type:** integer<int64> The ID of the product card on the Market. _Min value:_ `1`  
offerName |  **Type:** string Product name.  
prices |  **Type:** [OrdersStatsPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspricedto)[] The price or discounts on the product.  
The price or discounts on the product. _Min items:_ `1`  
shopSku |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
warehouse |  **Type:** [OrdersStatsWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatswarehousedto) Information about the warehouse where the product is stored.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentdto)OrdersStatsPaymentDTO
Information about money transfers by order.
**Name** |  **Description**  
---|---  
date |  **Type:** string<date> Date of the money transfer. Date format: `YYYY-MM-DD`.  
id |  **Type:** string The money transfer ID.  
paymentOrder |  **Type:** [OrdersStatsPaymentOrderDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentorderdto) Information about the payment order.  
source |  **Type:** [OrdersStatsPaymentSourceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentsourcetype) The money transfer method. _Enum:_ `BUYER`, `CASHBACK`, `MARKETPLACE`, `SPLIT`  
total |  **Type:** number The amount of the money transfer. The precision is two decimal places.  
type |  **Type:** [OrdersStatsPaymentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymenttype) The type of money transfer. _Enum:_ `PAYMENT`, `REFUND`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdeliveryregiondto)OrdersStatsDeliveryRegionDTO
Information about the delivery region.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> The identifier of the delivery region.  
name |  **Type:** string The name of the delivery region.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsorderpaymenttype)OrdersStatsOrderPaymentType
Order payment type:
  * `POSTPAID` — the order is paid after it has been received.
  * `PREPAID` — the order was paid for before it was received.
  * `UNKNOWN` — unknown type of payment. Most likely, the buyer canceled or returned the order, or there was no payment for it.

**Type** |  **Description**  
---|---  
[OrdersStatsOrderPaymentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsorderpaymenttype) |  _Enum:_ `POSTPAID`, `PREPAID`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidydto)OrdersStatsSubsidyDTO
Information about the accrual of points that are used to reduce the cost of placement, and their deduction in case of non-purchase or refund.
**Name** |  **Description**  
---|---  
amount* |  **Type:** number The number of points that are used to reduce the cost of placement, accurate to two decimal places.  
operationType* |  **Type:** [OrdersStatsSubsidyOperationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidyoperationtype) The type of operation with points that are used to reduce the cost of placement. _Enum:_ `ACCRUAL`, `DEDUCTION`  
type* |  **Type:** [OrdersStatsSubsidyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidytype) The source of the points that are used to reduce the cost of placement. _Enum:_ `YANDEX_CASHBACK`, `SUBSIDY`, `DELIVERY`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatscommissiontype)OrdersStatsCommissionType
Service:
  * `FEE` — product placement on the Market.
  * `FULFILLMENT` — warehouse handling. Non-refundable since January 1, 2024.
  * `LOYALTY_PARTICIPATION_FEE` — participation in the loyalty program and feedback for points.
  * `AUCTION_PROMOTION` — boost sales with pay-per-sales.
  * `INSTALLMENT` — installments. It has not been returned since February 24, 2022.
  * `DELIVERY_TO_CUSTOMER` — delivery to the buyer (FBY, FBS). For DBS and Express, if the order is returned through Yandex.Market logistics.
  * `EXPRESS_DELIVERY_TO_CUSTOMER` — express delivery to the buyer (Express).
  * `AGENCY` — acceptance of the buyer's payment.
  * `PAYMENT_TRANSFER` — transfer of the buyer's payment.
  * `RETURNED_ORDERS_STORAGE` — storage of non-purchases and refunds (FBS). For DBS and Express, if the order is returned through Yandex.Market logistics.
  * `SORTING` — order processing (FBS).
  * `INTAKE_SORTING` — organization of picking up orders from the seller's warehouse (FBS).
  * `RETURN_PROCESSING` — Warehouse Order processing (FBS). For DBS and Express, if the order is returned through Yandex.Market logistics.
  * `ILLIQUID_GOODS_SALE` — remuneration for the sale of non-imported goods.

**Type** |  **Description**  
---|---  
[OrdersStatsCommissionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatscommissiontype) |  _Enum:_ `FEE`, `FULFILLMENT`, `LOYALTY_PARTICIPATION_FEE`, `AUCTION_PROMOTION`, `INSTALLMENT`, `DELIVERY_TO_CUSTOMER`, `EXPRESS_DELIVERY_TO_CUSTOMER`, `AGENCY`, `PAYMENT_TRANSFER`, `RETURNED_ORDERS_STORAGE`, `SORTING`, `INTAKE_SORTING`, `RETURN_PROCESSING`, `ILLIQUID_GOODS_SALE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsdetailsdto)OrdersStatsDetailsDTO
Information about the removal of the product from the order.
**Name** |  **Description**  
---|---  
itemCount |  **Type:** integer<int64> The quantity of the product with the status specified in the parameter `itemStatus`.  
itemStatus |  **Type:** [OrdersStatsItemStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsitemstatustype) The status of the product. _Enum:_ `REJECTED`, `RETURNED`  
stockType |  **Type:** [OrdersStatsStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsstocktype) Product type. _Enum:_ `FIT`, `DEFECT`, `EXPIRED`  
updateDate |  **Type:** string<date> The date when the product received the status specified in the parameter `itemStatus`. Date format: `YYYY-MM-DD`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspricedto)OrdersStatsPriceDTO
The price or discounts on the product.
**Name** |  **Description**  
---|---  
costPerItem |  **Type:** number The price or discount per unit in the order. The precision is two decimal places. Includes VAT.  
total |  **Type:** number The total price or discount for all items in the order. The precision is two decimal places. Includes VAT.  
type |  **Type:** [OrdersStatsPriceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspricetype) The type of discount or the price of the product. _Enum:_ `BUYER`, `CASHBACK`, `MARKETPLACE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatswarehousedto)OrdersStatsWarehouseDTO
Information about the warehouse where the product is stored.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> The warehouse ID.  
name |  **Type:** string The name of the warehouse.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentorderdto)OrdersStatsPaymentOrderDTO
Information about the payment order.
**Name** |  **Description**  
---|---  
date |  **Type:** string<date> The date of the payment order. Date format: `YYYY‑MM‑DD`.  
id |  **Type:** string The number of the payment order.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentsourcetype)OrdersStatsPaymentSourceType
Money transfer method:
  * `BUYER` — payment or refund in cash.


Outdated methods:
  * `CASHBACK`.
  * `MARKETPLACE`.
  * `SPLIT`.

**Type** |  **Description**  
---|---  
[OrdersStatsPaymentSourceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymentsourcetype) |  _Enum:_ `BUYER`, `CASHBACK`, `MARKETPLACE`, `SPLIT`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymenttype)OrdersStatsPaymentType
Type of money transfer:
  * `PAYMENT` — payment.
  * `REFUND` — refund.

**Type** |  **Description**  
---|---  
[OrdersStatsPaymentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspaymenttype) |  _Enum:_ `PAYMENT`, `REFUND`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidyoperationtype)OrdersStatsSubsidyOperationType
The type of operation with points that are used to reduce the cost of placement:
  * `ACCRUAL` — scoring points.
  * `DEDUCTION` — deduction of points.

**Type** |  **Description**  
---|---  
[OrdersStatsSubsidyOperationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidyoperationtype) |  _Enum:_ `ACCRUAL`, `DEDUCTION`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidytype)OrdersStatsSubsidyType
The source of the points that are used to reduce the cost of placement:
  * `YANDEX_CASHBACK` — discount on Yandex Plus subscription.
  * `SUBSIDY` — Yandex. Market discount (for promotions, promo codes, coupons, etc.)
  * `DELIVERY` — discount for shipping (DBS).

**Type** |  **Description**  
---|---  
[OrdersStatsSubsidyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatssubsidytype) |  _Enum:_ `YANDEX_CASHBACK`, `SUBSIDY`, `DELIVERY`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsitemstatustype)OrdersStatsItemStatusType
Product status:
  * `REJECTED` — the product was added to the created order, but was not paid for.
  * `RETURNED` — the product has been returned.

**Type** |  **Description**  
---|---  
[OrdersStatsItemStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsitemstatustype) |  _Enum:_ `REJECTED`, `RETURNED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsstocktype)OrdersStatsStockType
Product Type:
  * `FIT` — the product is of good quality.
  * `DEFECT` — the product is defective.
  * `EXPIRED` — expired product.

**Type** |  **Description**  
---|---  
[OrdersStatsStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatsstocktype) |  _Enum:_ `FIT`, `DEFECT`, `EXPIRED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspricetype)OrdersStatsPriceType
Discount type or product price:
  * `BUYER` — the price of the product, including discounts, including coupons.
  * `CASHBACK` — Plus points.
  * `MARKETPLACE` — coupons.

**Type** |  **Description**  
---|---  
[OrdersStatsPriceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#ordersstatspricetype) |  _Enum:_ `BUYER`, `CASHBACK`, `MARKETPLACE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/stats/getOrdersStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
page_token:
limit:
Body{ "dateFrom": "string", "dateTo": "string", "updateFrom": "string", "updateTo": "string", "orders": [ 0 ], "statuses": [ "CANCELLED_BEFORE_PROCESSING" ], "hasCis": false }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Transfer and confirmation of the refund decision](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/orders/submitReturnDecision)
Next
[Closing documents](https://yandex.ru/dev/market/partner-api/doc/en/reference/stats/en/reference/reports/generateClosureDocumentsReport)
