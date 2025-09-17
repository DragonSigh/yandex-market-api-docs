---
title: Information about the buyer - Business orders | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/getOrderBusinessBuyerInfo
crawled_at: 2025-09-17T14:31:58.602515
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body)
    * [OrderBusinessBuyerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#orderbusinessbuyerdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body6)


# Information about the buyer — a legal entity
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about the customer by the order ID.
How to get information about a buyer who is an individual
Use the request [GET v2/campaigns/{campaignId}/orders/{orderId}/buyer](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/orders/getOrderBuyerInfo).
You can receive the data only if the order is in the status `PROCESSING`, `DELIVERY`, `PICKUP` or `DELIVERED`.
**, Limit:** 3,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/business-buyer

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#200-ok)200 OK
Information about the buyer.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "inn": "string",
        "kpp": "string",
        "organizationName": "string",
        "organizationJurAddress": "string"
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OrderBusinessBuyerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#orderbusinessbuyerdto) Information about the buyer.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#orderbusinessbuyerdto)OrderBusinessBuyerDTO
Information about the buyer.
**Name** |  **Description**  
---|---  
inn |  **Type:** string INN.  
kpp |  **Type:** string Checkpoint.  
organizationJurAddress |  **Type:** string Legal address.  
organizationName |  **Type:** string Name of the legal entity.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessBuyerInfo#apiresponsestatustype) The type of response. Possible values:
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
[Transfer of digital goods keys](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/orders/provideOrderDigitalCodes)
Next
[Information about documents](https://yandex.ru/dev/market/partner-api/doc/en/reference/order-business-information/en/reference/order-business-information/getOrderBusinessDocumentsInfo)
