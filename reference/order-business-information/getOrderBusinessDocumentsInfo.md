---
title: Information about documents - Business orders | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/getOrderBusinessDocumentsInfo
crawled_at: 2025-09-17T14:32:07.423108
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body)
    * [OrderBusinessDocumentsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#orderbusinessdocumentsdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype)
    * [DocumentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#documentdto)
    * [OrderDocumentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#orderdocumentstatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body6)


# Information about documents
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about documents by order ID.
You can receive the data after the order status changes. `DELIVERED`.
**, Limit:** 3,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/documents

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#200-ok)200 OK
Information about the documents.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "upd": {
            "status": "READY",
            "number": "string",
            "date": "string"
        },
        "ukd": {
            "status": "READY",
            "number": "string",
            "date": "string"
        },
        "torgTwelve": {
            "status": "READY",
            "number": "string",
            "date": "string"
        },
        "sf": {
            "status": "READY",
            "number": "string",
            "date": "string"
        },
        "ksf": {
            "status": "READY",
            "number": "string",
            "date": "string"
        }
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OrderBusinessDocumentsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#orderbusinessdocumentsdto) Information about the documents.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#orderbusinessdocumentsdto)OrderBusinessDocumentsDTO
Information about the documents.
**Name** |  **Description**  
---|---  
ksf |  **Type:** [DocumentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#documentdto) Information about the adjustment invoice.  
sf |  **Type:** [DocumentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#documentdto) Information about the invoice.  
torgTwelve |  **Type:** [DocumentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#documentdto) Information about the consignment note.  
ukd |  **Type:** [DocumentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#documentdto) Information about UKD-1 or UKD-2.  
upd |  **Type:** [DocumentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#documentdto) Information about UPD-1 or UPD-2.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#documentdto)DocumentDTO
Information about the document.
**Name** |  **Description**  
---|---  
date |  **Type:** string<date> The date the document was created.  
number |  **Type:** string Document number.  
status |  **Type:** [OrderDocumentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#orderdocumentstatustype) The status of the document. _Enum:_ `READY`, `NOT_READY`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#orderdocumentstatustype)OrderDocumentStatusType
Document status:
  * `READY` "I'm ready."
  * `NOT_READY` "I'm not ready."

**Type** |  **Description**  
---|---  
[OrderDocumentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#orderdocumentstatustype) |  _Enum:_ `READY`, `NOT_READY`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Information about the buyer](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo)
Next
[Transfer of the number of packages](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/shipments/setShipmentPalletsCount)
