---
title: Store Quality Index - Quality index | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/getQualityRatings
crawled_at: 2025-09-17T14:41:02.455265
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body1)
    * [CampaignsQualityRatingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#campaignsqualityratingdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype)
    * [CampaignQualityRatingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#campaignqualityratingdto)
    * [QualityRatingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingdto)
    * [QualityRatingComponentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingcomponentdto)
    * [QualityRatingComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingcomponenttype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body7)


# Store Quality Index
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/_auto/scopes_summary/pages/settings-management)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns the value of the store quality index and its components.
Read more about the quality index. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/quality/score/).
**, Limit:** 10,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/ratings/quality

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body)Body
application/json
```
{
    "dateFrom": "string",
    "dateTo": "string",
    "campaignIds": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
campaignIds* |  **Type:** integer<int64>[] A list of campaign IDs. You can find them using a query. [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not use store IDs instead, which are listed in the seller's account on the Market next to the store name and in some reports.   
The campaign list of those stores for which you need to get information. _Min items:_ `1` _Max items:_ `50` _Unique items_  
dateFrom |  **Type:** string<date> The beginning of the period. Date format: `YYYY‑MM‑DD`. It cannot be earlier than 30 days from the current date.  
dateTo |  **Type:** string<date> End of the period. Date format: `YYYY‑MM‑DD`. It cannot be later than the current date.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#200-ok)200 OK
The value of the store quality index and its components.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "campaignRatings": [
            {
                "campaignId": 0,
                "ratings": [
                    {
                        "rating": 0,
                        "calculationDate": "string",
                        "components": [
                            {
                                "value": 0,
                                "componentType": "DBS_CANCELLATION_RATE"
                            }
                        ]
                    }
                ]
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [CampaignsQualityRatingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#campaignsqualityratingdto) Information about the quality index of stores.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#campaignsqualityratingdto)CampaignsQualityRatingDTO
Information about the quality index of stores.
**Name** |  **Description**  
---|---  
campaignRatings* |  **Type:** [CampaignQualityRatingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#campaignqualityratingdto)[] A list of stores with information about their quality index.  
Information about the store's quality index.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#campaignqualityratingdto)CampaignQualityRatingDTO
Information about the store's quality index.
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
ratings* |  **Type:** [QualityRatingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingdto)[] A list of quality index values.  
Information about the quality index.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingdto)QualityRatingDTO
Information about the quality index.
**Name** |  **Description**  
---|---  
calculationDate* |  **Type:** string<date> Date of calculation. Date format: `YYYY‑MM‑DD`.  
components* |  **Type:** [QualityRatingComponentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingcomponentdto)[] The components of the quality index.  
A component of the quality index.  
rating* |  **Type:** integer<int64> The value of the quality index. _Min value:_ `0` _Max value:_ `100`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingcomponentdto)QualityRatingComponentDTO
A component of the quality index.
**Name** |  **Description**  
---|---  
componentType* |  **Type:** [QualityRatingComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingcomponenttype) The type of component. _Enum:_ `DBS_CANCELLATION_RATE`, `DBS_LATE_DELIVERY_RATE`, `FBS_CANCELLATION_RATE`, `FBS_LATE_SHIP_RATE`, `FBY_LATE_DELIVERY_RATE`, `FBY_CANCELLATION_RATE`, `FBY_DELIVERY_DIFF_RATE`, `FBY_LATE_EDITING_RATE`  
value* |  **Type:** number<double> The value of the component as a percentage. _Min value:_ `0` _Max value:_ `100`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingcomponenttype)QualityRatingComponentType
The components of the quality index.
**For the DBS model:**
  * `DBS_CANCELLATION_RATE` — the proportion of cancelled items.
  * `DBS_LATE_DELIVERY_RATE` — the percentage of orders delivered after the scheduled date.


**For the FBS and Express models:**
  * `FBS_CANCELLATION_RATE` — the proportion of cancelled items.
  * `FBS_LATE_SHIP_RATE` — the proportion of orders shipped on time.


**For the FBY model:**
  * `FBY_LATE_DELIVERY_RATE` — the proportion of goods that arrived at the warehouse late.
  * `FBY_CANCELLATION_RATE` — the percentage of cancelled or undelivered items.
  * `FBY_DELIVERY_DIFF_RATE` — the proportion of goods that did not arrive with the delivery or that were not accepted.
  * `FBY_LATE_EDITING_RATE` — the percentage of products that were removed from the application late.

**Type** |  **Description**  
---|---  
[QualityRatingComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#qualityratingcomponenttype) |  _Enum:_ `DBS_CANCELLATION_RATE`, `DBS_LATE_DELIVERY_RATE`, `FBS_CANCELLATION_RATE`, `FBS_LATE_SHIP_RATE`, `FBY_LATE_DELIVERY_RATE`, `FBY_CANCELLATION_RATE`, `FBY_DELIVERY_DIFF_RATE`, `FBY_LATE_EDITING_RATE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "dateFrom": "string", "dateTo": "string", "campaignIds": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Recommended rates](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/bids/getBidsRecommendations)
Next
[Orders that affected the quality index](https://yandex.ru/dev/market/partner-api/doc/en/reference/ratings/en/reference/ratings/getQualityRatingDetails)
