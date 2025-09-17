---
title: LOGIN verification Statuses - Labeling of goods | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/getOrderIdentifiersStatus
crawled_at: 2025-09-17T14:28:03.668841
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body)
    * [GetOrderIdentifiersStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#getorderidentifiersstatusdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype)
    * [OrderItemValidationStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#orderitemvalidationstatusdto)
    * [UinDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#uindto)
    * [UinStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#uinstatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body6)


# LOGIN verification Statuses
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/fbs) and [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/express).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns verification statuses _Win_ in the order.
An order that contains jewelry will change to the status `READY_TO_SHIP`, only when:
  1. You will transfer the price points for each piece of jewelry in the order to the Market — method [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout).
  2. All plugins will be successfully verified.

**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/identifiers/status

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#200-ok)200 OK
Information on checking the UINs.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "items": [
            {
                "id": 0,
                "uin": [
                    {
                        "value": "string",
                        "status": "OK"
                    }
                ]
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GetOrderIdentifiersStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#getorderidentifiersstatusdto) A list of product IDs and LOGin verification statuses.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#getorderidentifiersstatusdto)GetOrderIdentifiersStatusDTO
A list of product IDs and LOGin verification statuses.
**Name** |  **Description**  
---|---  
items* |  **Type:** [OrderItemValidationStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#orderitemvalidationstatusdto)[] A list of product IDs and LOGin verification statuses.  
The product ID and the verification status of its LOGIN.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#orderitemvalidationstatusdto)OrderItemValidationStatusDTO
The product ID and the verification status of its LOGIN.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The product ID in the order.  
uin |  **Type:** [UinDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#uindto)[] LOGIN verification statuses.  
The status of the UIN check. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#uindto)UinDTO
The status of the UIN check.
**Name** |  **Description**  
---|---  
status* |  **Type:** [UinStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#uinstatustype) LOGIN verification status:
  * `FAILED` — failed verification.
  * `IN_PROGRESS` — in the process of checking.
  * `NOT_ON_VALIDATION` — The WIN has not been sent for verification or not all the WINs in the order have been transferred.
  * `OK` — the check was successfully completed.

_Enum:_ `OK`, `IN_PROGRESS`, `FAILED`, `NOT_ON_VALIDATION`  
value* |  **Type:** string WIN the product.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#uinstatustype)UinStatusType
LOGIN verification status:
  * `FAILED` — failed verification.
  * `IN_PROGRESS` — in the process of checking.
  * `NOT_ON_VALIDATION` — The WIN has not been sent for verification or not all the WINs in the order have been transferred.
  * `OK` — the check was successfully completed.

**Type** |  **Description**  
---|---  
[UinStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#uinstatustype) |  _Enum:_ `OK`, `IN_PROGRESS`, `FAILED`, `NOT_ON_VALIDATION`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus#apiresponsestatustype) The type of response. Possible values:
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
A unique identification number for jewelry.  
  
The manufacturer receives the UIN when he registers the product in the system of control over the turnover of precious metals and stones — GIIS DMDK.
### Was the article helpful?
YesNo
Previous
[Transmission of marking codes](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers)
Next
[Sending the confirmation code](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac)
