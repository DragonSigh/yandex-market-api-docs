---
title: List of stores - Offices and shops | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/getCampaigns
crawled_at: 2025-09-17T14:24:44.575014
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body)
    * [CampaignDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#campaigndto)
    * [FlippingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#flippingpagerdto)
    * [ApiAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiavailabilitystatustype)
    * [BusinessDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#businessdto)
    * [PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#placementtype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body6)


# User's Store List
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/pricing_read-only)
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/promotion_read-only)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/finance-and-accounting)
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/communication)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/settings-management)
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


**For the Api Key Token:** returns the list of stores in the account for which the token was issued. You cannot get a list of only subagency stores.
**For the OAuth token:** returns a list of stores that the user who owns the authorization token used in the request has access to. For agency users, the list consists of subagency stores.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
page |  **Type:** integer<int32> If the method has `page_token` Use it instead of the parameter `page`. [Learn more about the types of pagination and their use](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/pagination) The number of the results page. Used together with the parameter `pageSize`. `page` ignored if specified `page_token` or `limit`.   
_Default:_ `1` _Max value:_ `10000`  
pageSize |  **Type:** integer<int32> Page size. Used together with the parameter `page`. `pageSize` ignored if specified `page_token` or `limit`.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#200-ok)200 OK
The user's stores.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body)Body
application/json
```
{
    "campaigns": [
        {
            "domain": "string",
            "id": 0,
            "clientId": 0,
            "business": {
                "id": 0,
                "name": "string"
            },
            "placementType": "FBS",
            "apiAvailability": "AVAILABLE"
        }
    ],
    "pager": {
        "total": 0,
        "from": 0,
        "to": 0,
        "currentPage": 0,
        "pagesCount": 0,
        "pageSize": 0
    }
}

```

**Name** |  **Description**  
---|---  
campaigns* |  **Type:** [CampaignDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#campaigndto)[] A list with information for each store.  
Information about the store.  
pager |  **Type:** [FlippingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#flippingpagerdto) A model for pagination.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#campaigndto)CampaignDTO
Information about the store.
**Name** |  **Description**  
---|---  
apiAvailability |  **Type:** [ApiAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiavailabilitystatustype) The ability to use the API:
  * `AVAILABLE` — API methods are available for executing requests.
  * `DISABLED_BY_INACTIVITY` — API methods are unavailable due to _inactivity of the store or cabinet_.

_Enum:_ `AVAILABLE`, `DISABLED_BY_INACTIVITY`  
business |  **Type:** [BusinessDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#businessdto) Information about the cabinet.  
clientId ⦸ |  **Type:** integer<int64> The payer's ID in Yandex.Balance.  
domain |  **Type:** string The store's name.  
id |  **Type:** integer<int64> The campaign ID. You can also find it in the seller's account on the Market. Click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.  
placementType |  **Type:** [PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#placementtype) The model that the store uses:
  * `FBS` — FBS or Express.
  * `FBY` — FBY.
  * `DBS` — DBS.

_Enum:_ `FBS`, `FBY`, `DBS`, `LAAS`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#flippingpagerdto)FlippingPagerDTO
A model for pagination.
**Name** |  **Description**  
---|---  
currentPage |  **Type:** integer<int32> The current page.  
from |  **Type:** integer<int32> The initial number of the found element on the page.  
pageSize |  **Type:** integer<int32> Page size.  
pagesCount |  **Type:** integer<int32> The total number of pages.  
to |  **Type:** integer<int32> The final number of the found element on the page.  
total |  **Type:** integer<int32> How many items were found in total.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiavailabilitystatustype)ApiAvailabilityStatusType
The ability to use the API:
  * `AVAILABLE` — API methods are available for executing requests.
  * `DISABLED_BY_INACTIVITY` — API methods are unavailable due to _inactivity of the store or cabinet_.

**Type** |  **Description**  
---|---  
[ApiAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiavailabilitystatustype) |  _Enum:_ `AVAILABLE`, `DISABLED_BY_INACTIVITY`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#businessdto)BusinessDTO
Information about the cabinet.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> Cabinet ID.  
name |  **Type:** string Business name.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#placementtype)PlacementType
The model that the store uses:
  * `FBS` — FBS or Express.
  * `FBY` — FBY.
  * `DBS` — DBS.

**Type** |  **Description**  
---|---  
[PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#placementtype) |  _Enum:_ `FBS`, `FBY`, `DBS`, `LAAS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
page:
pageSize:
Send
No longer supported, please use an alternative and newer version.
Copied
The store is disabled because it has not placed products in the showcase for more than 90 days.  
  
There is not a single active store in the cabinet.
### Was the article helpful?
YesNo
Previous
[All updates](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/changelog/all)
Next
[Store Information](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign)
