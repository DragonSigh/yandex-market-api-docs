---
title: Store Information - Offices and shops | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/getCampaign
crawled_at: 2025-09-17T14:26:49.824335
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body)
    * [CampaignDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#campaigndto)
    * [ApiAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiavailabilitystatustype)
    * [BusinessDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#businessdto)
    * [PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#placementtype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body6)


# Store Information
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


Returns information about the store.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#200-ok)200 OK
Information about the store.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body)Body
application/json
```
{
    "campaign": {
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
}

```

**Name** |  **Description**  
---|---  
campaign |  **Type:** [CampaignDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#campaigndto) Information about the store.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#campaigndto)CampaignDTO
Information about the store.
**Name** |  **Description**  
---|---  
apiAvailability |  **Type:** [ApiAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiavailabilitystatustype) The ability to use the API:
  * `AVAILABLE` — API methods are available for executing requests.
  * `DISABLED_BY_INACTIVITY` — API methods are unavailable due to _inactivity of the store or cabinet_.

_Enum:_ `AVAILABLE`, `DISABLED_BY_INACTIVITY`  
business |  **Type:** [BusinessDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#businessdto) Information about the cabinet.  
clientId ⦸ |  **Type:** integer<int64> The payer's ID in Yandex.Balance.  
domain |  **Type:** string The store's name.  
id |  **Type:** integer<int64> The campaign ID. You can also find it in the seller's account on the Market. Click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
placementType |  **Type:** [PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#placementtype) The model that the store uses:
  * `FBS` — FBS or Express.
  * `FBY` — FBY.
  * `DBS` — DBS.

_Enum:_ `FBS`, `FBY`, `DBS`, `LAAS`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiavailabilitystatustype)ApiAvailabilityStatusType
The ability to use the API:
  * `AVAILABLE` — API methods are available for executing requests.
  * `DISABLED_BY_INACTIVITY` — API methods are unavailable due to _inactivity of the store or cabinet_.

**Type** |  **Description**  
---|---  
[ApiAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiavailabilitystatustype) |  _Enum:_ `AVAILABLE`, `DISABLED_BY_INACTIVITY`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#businessdto)BusinessDTO
Information about the cabinet.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> Cabinet ID.  
name |  **Type:** string Business name.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#placementtype)PlacementType
The model that the store uses:
  * `FBS` — FBS or Express.
  * `FBY` — FBY.
  * `DBS` — DBS.

**Type** |  **Description**  
---|---  
[PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#placementtype) |  _Enum:_ `FBS`, `FBY`, `DBS`, `LAAS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaign#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Send
No longer supported, please use an alternative and newer version.
Copied
The store is disabled because it has not placed products in the showcase for more than 90 days.  
  
There is not a single active store in the cabinet.
### Was the article helpful?
YesNo
Previous
[List of stores](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns)
Next
[Cabinet Settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/businesses/getBusinessSettings)
