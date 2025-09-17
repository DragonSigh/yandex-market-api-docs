---
title: Information about child regions - Regions | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/searchRegionChildren
crawled_at: 2025-09-17T14:37:23.003909
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body)
    * [FlippingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#flippingpagerdto)
    * [RegionWithChildrenDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regionwithchildrendto)
    * [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiontype)
    * [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiondto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body6)


# Information about child regions
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/pricing_read-only)
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/promotion_read-only)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/finance-and-accounting)
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/communication)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/settings-management)
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about regions that are children of the region whose ID is specified in the request.
For methods `GET v2/regions`, `GET v2/regions/{regionId}` and `GET v2/regions/{regionId}/children` there is a group resource restriction. The limit is imposed on the total number of regions, information about which is requested using these methods (no more than 100,000 regions).
The volume of requests to the resource that can be completed during the day depends on the total number of regions.
**, Limit:** 50,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/regions/{regionId}/children

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
regionId* |  **Type:** integer<int64> ID of the region. You can get the region ID using a request [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionsByName).  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
page |  **Type:** integer<int32> If the method has `page_token` Use it instead of the parameter `page`. [Learn more about the types of pagination and their use](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/pagination) The number of the results page. Used together with the parameter `pageSize`. `page` ignored if specified `page_token` or `limit`.   
_Default:_ `1` _Max value:_ `10000`  
pageSize |  **Type:** integer<int32> Page size. Used together with the parameter `page`. `pageSize` ignored if specified `page_token` or `limit`.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#200-ok)200 OK
Regions that are children of the one specified in the request.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body)Body
application/json
```
{
    "pager": {
        "total": 0,
        "from": 0,
        "to": 0,
        "currentPage": 0,
        "pagesCount": 0,
        "pageSize": 0
    },
    "regions": {
        "id": 0,
        "name": "string",
        "type": "OTHER",
        "parent": {
            "id": 0,
            "name": "string",
            "type": "OTHER"
        },
        "children": [
            {
                "id": 0,
                "name": "string",
                "type": "OTHER"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
pager |  **Type:** [FlippingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#flippingpagerdto) A model for pagination.  
regions |  **Type:** [RegionWithChildrenDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regionwithchildrendto) Information about the parent and child regions.  
The delivery region.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#flippingpagerdto)FlippingPagerDTO
A model for pagination.
**Name** |  **Description**  
---|---  
currentPage |  **Type:** integer<int32> The current page.  
from |  **Type:** integer<int32> The initial number of the found element on the page.  
pageSize |  **Type:** integer<int32> Page size.  
pagesCount |  **Type:** integer<int32> The total number of pages.  
to |  **Type:** integer<int32> The final number of the found element on the page.  
total |  **Type:** integer<int32> How many items were found in total.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regionwithchildrendto)RegionWithChildrenDTO
Information about the parent and child regions.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> ID of the region.  
name* |  **Type:** string The name of the region.  
type* |  **Type:** [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiontype) The type of region. Possible values:
  * `CITY_DISTRICT` — the area of the city.
  * `CITY` — a large city.
  * `CONTINENT` — the continent.
  * `COUNTRY_DISTRICT` — area.
  * `COUNTRY` — country.
  * `REGION` — region.
  * `REPUBLIC_AREA` — district of the subject of the federation.
  * `REPUBLIC` — the subject of the Federation.
  * `SUBWAY_STATION` — the metro station.
  * `VILLAGE` — the city.
  * `OTHER` — unknown region.

_Enum:_ `OTHER`, `CONTINENT`, `REGION`, `COUNTRY`, `COUNTRY_DISTRICT`, `REPUBLIC`, `CITY`, `VILLAGE`, `CITY_DISTRICT`, `SUBWAY_STATION`, `REPUBLIC_AREA`  
children |  **Type:** [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiondto)[] Child regions.  
The delivery region. _Min items:_ `1`  
parent |  **Type:** [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiondto) The delivery region.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiontype)RegionType
The type of region.
Possible values:
  * `CITY_DISTRICT` — the area of the city.
  * `CITY` — a large city.
  * `CONTINENT` — the continent.
  * `COUNTRY_DISTRICT` — area.
  * `COUNTRY` — country.
  * `REGION` — region.
  * `REPUBLIC_AREA` — district of the subject of the federation.
  * `REPUBLIC` — the subject of the Federation.
  * `SUBWAY_STATION` — the metro station.
  * `VILLAGE` — the city.
  * `OTHER` — unknown region.

**Type** |  **Description**  
---|---  
[RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiontype) |  _Enum:_ `OTHER`, `CONTINENT`, `REGION`, `COUNTRY`, `COUNTRY_DISTRICT`, `REPUBLIC`, `CITY`, `VILLAGE`, `CITY_DISTRICT`, `SUBWAY_STATION`, `REPUBLIC_AREA`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiondto)RegionDTO
The delivery region.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> ID of the region.  
name* |  **Type:** string The name of the region.  
type* |  **Type:** [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiontype) The type of region. Possible values:
  * `CITY_DISTRICT` — the area of the city.
  * `CITY` — a large city.
  * `CONTINENT` — the continent.
  * `COUNTRY_DISTRICT` — area.
  * `COUNTRY` — country.
  * `REGION` — region.
  * `REPUBLIC_AREA` — district of the subject of the federation.
  * `REPUBLIC` — the subject of the Federation.
  * `SUBWAY_STATION` — the metro station.
  * `VILLAGE` — the city.
  * `OTHER` — unknown region.

_Enum:_ `OTHER`, `CONTINENT`, `REGION`, `COUNTRY`, `COUNTRY_DISTRICT`, `REPUBLIC`, `CITY`, `VILLAGE`, `CITY_DISTRICT`, `SUBWAY_STATION`, `REPUBLIC_AREA`  
parent |  **Type:** [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#regiondto) The delivery region.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionChildren#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
regionId*:
Query parameters
page:
pageSize:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Information about the region](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionsById)
Next
[Adding and editing products](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/offer-mappings/updateOfferMappingEntries)
