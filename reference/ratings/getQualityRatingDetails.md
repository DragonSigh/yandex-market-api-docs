---
title: Orders that affected the quality index - Quality index | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/getQualityRatingDetails
crawled_at: 2025-09-17T14:37:02.362881
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body)
    * [QualityRatingDetailsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#qualityratingdetailsdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype)
    * [QualityRatingAffectedOrderDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#qualityratingaffectedorderdto)
    * [AffectedOrderQualityRatingComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#affectedorderqualityratingcomponenttype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body6)


# Orders that affected the quality index
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/_auto/scopes_summary/pages/settings-management)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns a list of orders that affected the store's quality index. To find out the value of the quality index, make a request [POST v2/businesses/{businessId}/ratings/quality](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings).
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/ratings/quality/details

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#200-ok)200 OK
Information about orders that affected the quality index.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "affectedOrders": [
            {
                "orderId": 0,
                "description": "string",
                "componentType": "DBS_CANCELLATION_RATE"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [QualityRatingDetailsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#qualityratingdetailsdto) Information about orders that affected the quality index.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#qualityratingdetailsdto)QualityRatingDetailsDTO
Information about orders that affected the quality index.
**Name** |  **Description**  
---|---  
affectedOrders* |  **Type:** [QualityRatingAffectedOrderDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#qualityratingaffectedorderdto)[] A list of orders that affected the quality index.  
Information about the order that affected the quality index.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#qualityratingaffectedorderdto)QualityRatingAffectedOrderDTO
Information about the order that affected the quality index.
**Name** |  **Description**  
---|---  
componentType* |  **Type:** [AffectedOrderQualityRatingComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#affectedorderqualityratingcomponenttype) The type of component of the quality index. _Enum:_ `DBS_CANCELLATION_RATE`, `DBS_LATE_DELIVERY_RATE`, `FBS_CANCELLATION_RATE`, `FBS_LATE_SHIP_RATE`  
description* |  **Type:** string Description of the problem.  
orderId* |  **Type:** integer<int64> The order ID. _Min value:_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#affectedorderqualityratingcomponenttype)AffectedOrderQualityRatingComponentType
The components of the quality index.
**For the DBS model:**
  * `DBS_CANCELLATION_RATE` — the proportion of cancelled items.
  * `DBS_LATE_DELIVERY_RATE` — the percentage of orders delivered after the scheduled date.


**For the FBS and Express models:**
  * `FBS_CANCELLATION_RATE` — the proportion of cancelled items.
  * `FBS_LATE_SHIP_RATE` — the proportion of orders shipped on time.

**Type** |  **Description**  
---|---  
[AffectedOrderQualityRatingComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#affectedorderqualityratingcomponenttype) |  _Enum:_ `DBS_CANCELLATION_RATE`, `DBS_LATE_DELIVERY_RATE`, `FBS_CANCELLATION_RATE`, `FBS_LATE_SHIP_RATE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Store Quality Index](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings)
Next
[Message history](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/chats/getChatHistory)
