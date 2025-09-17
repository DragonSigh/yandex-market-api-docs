---
title: Product photos in the return - Non-purchases and refunds | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/getReturnPhoto
crawled_at: 2025-09-17T14:35:51.021055
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body6)


# Receiving photos of items in a refund
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Receives photos of the goods that the buyer has attached to the return request.
**, Limit:** 10,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/{itemId}/image/{imageHash}

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
imageHash* |  **Type:** string Hash of the image link to download.  
itemId* |  **Type:** integer<int64> The product ID in the refund.  
orderId* |  **Type:** integer<int64> The order ID.  
returnId* |  **Type:** integer<int64> ID of a non-purchase or refund.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#200-ok)200 OK
A photo of the goods.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body)Body
application/octet-stream
**Type:** string
**Format:** binary
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
returnId*:
itemId*:
imageHash*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Buyer's statement](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnApplication)
Next
[Transfer and confirmation of the refund decision](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision)
