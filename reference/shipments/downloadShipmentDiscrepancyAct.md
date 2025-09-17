---
title: The act of discrepancies - FBS Shipments | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/downloadShipmentDiscrepancyAct
crawled_at: 2025-09-17T14:33:07.824684
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body6)


# Receiving a certificate of discrepancies
Info
Console
**The method is available for the[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/overview/fbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Returns the act of discrepancies for the specified shipment.
**, Limit:** 200 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/discrepancy-act

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
shipmentId* |  **Type:** integer<int64> Shipment ID.  
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#200-ok)200 OK
The act of discrepancies in XLSX format.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body)Body
application/vnd.ms-excel
**Type:** string
**Format:** binary
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentDiscrepancyAct#apiresponsestatustype) The type of response. Possible values:
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
[Acceptance and transfer certificate](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct)
Next
[Assembly Sheet](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/generateShipmentListDocumentReport)
