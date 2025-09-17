---
title: Transfer and confirmation of the refund decision - Non-purchases and refunds | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/submitReturnDecision
crawled_at: 2025-09-17T14:35:56.713000
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body)
    * [ReturnItemDecisionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnitemdecisiondto)
    * [ReturnRequestDecisionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnrequestdecisiontype)
    * [ReturnRequestDecisionReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnrequestdecisionreasontype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body1)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body7)


# Transfer and confirmation of the refund decision
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Allows you to perform one of the following operations:
  * **For all models:** send a list of refund solutions and confirm them.
  * **For the DBS model:** confirm the decision submitted to [POST v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setReturnDecision). To do this, use a request without a body.

**, Limit:** 10,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/submit

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
returnId* |  **Type:** integer<int64> ID of a non-purchase or refund.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body)Body
application/json
```
{
    "returnItemDecisions": [
        {
            "returnItemId": 0,
            "decisionType": "FAST_REFUND_MONEY",
            "decisionReasonType": "ISSUE_WITH_THE_PRODUCT_WAS_NOT_CONFIRMED",
            "comment": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
returnItemDecisions* |  **Type:** [ReturnItemDecisionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnitemdecisiondto)[] Decisions on goods in return.  
Product decisions need to be returned. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnitemdecisiondto)ReturnItemDecisionDTO
Product decisions need to be returned.
**Name** |  **Description**  
---|---  
decisionType* |  **Type:** [ReturnRequestDecisionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnrequestdecisiontype) The decision on the product needs to be returned. _Enum:_ `FAST_REFUND_MONEY`, `REFUND_MONEY`, `REFUND_MONEY_INCLUDING_SHIPMENT`, `REPAIR`, `REPLACE`, `SEND_TO_EXAMINATION`, `DECLINE_REFUND`, `OTHER_DECISION`  
returnItemId* |  **Type:** integer<int64> The product ID in the refund.  
comment |  **Type:** string Comment on the solution. Specify:
  * for `REFUND_MONEY_INCLUDING_SHIPMENT`— the cost of the return shipment.
  * for `REPAIR` — when you eliminate the defects of the product.
  * for `DECLINE_REFUND` — the reason for the refusal.
  * for `OTHER_DECISION` — what solution do you propose?

  
decisionReasonType |  **Type:** [ReturnRequestDecisionReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnrequestdecisionreasontype) The reason for the refusal. _Enum:_ `ISSUE_WITH_THE_PRODUCT_WAS_NOT_CONFIRMED`, `MECHANICAL_DAMAGE`, `WARRANTY_PERIOD_HAS_EXPIRED`, `CONFIGURATION_OR_PACKAGING_COMPROMISED`, `PRODUCT_APPEARANCE_COMPROMISED`, `WARRANTY_TERMS_VIOLATED`, `DEVICE_ACTIVATED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnrequestdecisiontype)ReturnRequestDecisionType
Refund decision:
  * `FAST_REFUND_MONEY` — return the money to the buyer without returning the product.
  * `REFUND_MONEY` — refund the buyer's money for the product.
  * `REFUND_MONEY_INCLUDING_SHIPMENT` — refund the buyer's money for the product and return shipment.
  * `REPAIR` — repair the product.
  * `REPLACE` — replace the product.
  * `SEND_TO_EXAMINATION` — take the product for examination.
  * `DECLINE_REFUND` — refuse to refund.
  * `OTHER_DECISION` — another solution.

**Type** |  **Description**  
---|---  
[ReturnRequestDecisionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnrequestdecisiontype) |  _Enum:_ `FAST_REFUND_MONEY`, `REFUND_MONEY`, `REFUND_MONEY_INCLUDING_SHIPMENT`, `REPAIR`, `REPLACE`, `SEND_TO_EXAMINATION`, `DECLINE_REFUND`, `OTHER_DECISION`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnrequestdecisionreasontype)ReturnRequestDecisionReasonType
Reason for refusal:
  * `ISSUE_WITH_THE_PRODUCT_WAS_NOT_CONFIRMED` — the problem with the product has not been confirmed.
  * `MECHANICAL_DAMAGE` — there is mechanical damage to the product.
  * `WARRANTY_PERIOD_HAS_EXPIRED` — the warranty period has expired.
  * `CONFIGURATION_OR_PACKAGING_COMPROMISED` — the package or packaging is broken.
  * `PRODUCT_APPEARANCE_COMPROMISED` — the presentation has been violated.
  * `WARRANTY_TERMS_VIOLATED` — the warranty conditions have been violated.
  * `DEVICE_ACTIVATED` — the device is activated.

**Type** |  **Description**  
---|---  
[ReturnRequestDecisionReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#returnrequestdecisionreasontype) |  _Enum:_ `ISSUE_WITH_THE_PRODUCT_WAS_NOT_CONFIRMED`, `MECHANICAL_DAMAGE`, `WARRANTY_PERIOD_HAS_EXPIRED`, `CONFIGURATION_OR_PACKAGING_COMPROMISED`, `PRODUCT_APPEARANCE_COMPROMISED`, `WARRANTY_TERMS_VIOLATED`, `DEVICE_ACTIVATED`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#200-ok)200 OK
The status of the operation.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body1)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/submitReturnDecision#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
returnId*:
Body{ "returnItemDecisions": [ { "returnItemId": 0, "decisionType": "FAST_REFUND_MONEY", "decisionReasonType": "ISSUE_WITH_THE_PRODUCT_WAS_NOT_CONFIRMED", "comment": "string" } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Product photos in the return](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getReturnPhoto)
Next
[Detailed information on orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/stats/getOrdersStats)
