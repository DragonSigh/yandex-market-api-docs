---
title: Sending the confirmation code - Express orders | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/verifyOrderEac
crawled_at: 2025-09-17T14:30:57.338935
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body1)
    * [EacVerificationResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#eacverificationresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype)
    * [EacVerificationStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#eacverificationstatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body7)


# Sending the confirmation code
Info
Console
**The method is available for the[Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/express) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Sends the confirmation code to the Market to verify it.
**If the store is configured to work with confirmation codes:**
In requests [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrder), [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrders), [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatus) in the parameter `delivery`, embedded in `order`, the parameter is returned `eacType` with the type `Enum` — the type of confirmation code for the transfer of the order.
Possible values:
  * `MERCHANT_TO_COURIER` (temporarily non—refundable) - the seller transmits the code to the courier to receive a non-purchase;
  * `COURIER_TO_MERCHANT` — the courier transmits the code to the seller to receive the order.


Parameter `eacType` returned for order statuses `COURIER_FOUND`, `COURIER_ARRIVED_TO_SENDER` and `DELIVERY_SERVICE_UNDELIVERED`. If the order has other statuses, the parameter may be omitted.
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#request)Request
PUT
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/verifyEac

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body)Body
application/json
```
{
    "code": "string"
}

```

**Name** |  **Description**  
---|---  
code* |  **Type:** string The code for confirming the EAPP.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#200-ok)200 OK
The code verification was completed successfully.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "verificationResult": "ACCEPTED",
        "attemptsLeft": 0
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [EacVerificationResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#eacverificationresultdto) The result of the request execution.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#eacverificationresultdto)EacVerificationResultDTO
The result of the request execution.
**Name** |  **Description**  
---|---  
attemptsLeft |  **Type:** integer<int32> The number of remaining code verification attempts. It is refunded if the store has sent an incorrect code. When all attempts are exhausted, the code will be updated.  
verificationResult |  **Type:** [EacVerificationStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#eacverificationstatustype) The verification status of the confirmation code. _Enum:_ `ACCEPTED`, `REJECTED`, `NEED_UPDATE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#eacverificationstatustype)EacVerificationStatusType
Verification status of the confirmation code:
  * `ACCEPTED` — the code is correct.
  * `REJECTED` — the code is incorrect.
  * `NEED_UPDATE` — The market will send a new code. The value is returned if the number of attempts to send the code is exceeded.

**Type** |  **Description**  
---|---  
[EacVerificationStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#eacverificationstatustype) |  _Enum:_ `ACCEPTED`, `REJECTED`, `NEED_UPDATE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
Body{ "code": "string" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[LOGIN verification Statuses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus)
Next
[Removing items from an order](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems)
