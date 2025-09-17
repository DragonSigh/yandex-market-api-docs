---
title: Acceptance and transfer certificate - FBS Shipments | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/downloadShipmentAct
crawled_at: 2025-09-17T14:33:00.031820
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body6)


# Receipt of the acceptance certificate
Info
Console
**The method is available for the[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/overview/fbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Express delivery
If your store is connected to express delivery and you ship orders to couriers 
The request generates an act of acceptance and transfer of orders included in the shipment, and returns the act in PDF format. The report contains orders that have been collected and are ready for shipment.
When forming an act, the Market automatically finds and inserts the following data into the template:
The data from which the Market generates the report
**Data in the report** |  **Description**  
---|---  
Date |  The date of the request.  
Sender |  The name of your legal entity indicated in the seller's account on the Market.  
Executor |  The name of the legal entity of the sorting center or delivery service.  
Shipment number in the customer's system |  The field is no longer in use Your order ID, which you provided in the response to the request `POST order/accept` from the Market.  
Shipment number in the contractor's (subcontractor's) system |  The ID of the order on the Market, as in the request output [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/orders/getOrders).  
Declared value |  The total amount of the order excluding the shipping cost, as shown in the request output [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/orders/getOrders) or [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/orders/getOrder).  
Weight |  The gross weight of the cargo area (the total weight of the package and contents), as in the request output [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/orders/getOrders) or [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/orders/getOrder).  
Number of seats |  The number of cargo spaces in the order, as shown in the request output [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/orders/getOrders) or [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/orders/getOrder).  
In the printed statement, specify the sender and the contractor. They must sign the act and indicate their last name and initials next to the signature. If necessary, also fill in the details of the power of attorney.
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/act

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
shipmentId* |  **Type:** integer<int64> Shipment ID.  
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#200-ok)200 OK
Acceptance and transfer certificate for shipment in PDF format.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body)Body
application/pdf
**Type:** string
**Format:** binary
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
shipmentId*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Information about multiple shipments](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments)
Next
[The act of discrepancies](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct)
