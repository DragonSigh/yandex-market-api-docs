---
title: Bill of lading - FBS Shipments | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/downloadShipmentTransportationWaybill
crawled_at: 2025-09-17T14:33:19.566056
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body6)


# Receipt of the bill of lading
Info
Console
**The method is available for the[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/overview/fbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Returns the bill of lading for the specified shipment if the Market picks up the goods from your warehouse. Read more about this shipping method. [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/ru/orders/fbs/settings/shipment#at-your-warehouse).
The invoice will not be refunded if you bring the goods to the warehouse or sorting center.
**, Limit:** 200 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/transportation-waybill

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
shipmentId* |  **Type:** integer<int64> Shipment ID.  
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#200-ok)200 OK
The bill of lading is in XLSX format.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body)Body
application/vnd.ms-excel
**Type:** string
**Format:** binary
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentTransportationWaybill#apiresponsestatustype) The type of response. Possible values:
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
[Assembly Sheet](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/generateShipmentListDocumentReport)
Next
[The actual act of acceptance and transfer](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentInboundAct)
