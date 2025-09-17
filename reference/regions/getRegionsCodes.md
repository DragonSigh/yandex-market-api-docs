---
title: List of country codes - Regions | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/getRegionsCodes
crawled_at: 2025-09-17T14:28:53.032401
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#request)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body)
    * [CountryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#countrydto)
    * [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#regiondto)
    * [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#regiontype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apiresponsestatustype)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body2)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body3)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body4)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body5)


# List of valid country codes
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


Returns a list of countries with their codes in the ISO 3166-1 alpha-2 format.
Country of manufacture `countryCode` it will be needed when selling goods from abroad for business. [Instruction manual](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/step-by-step/business-info)
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/regions/countries

```

##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#200-ok)200 OK
A list of countries with their codes in the ISO 3166-1 alpha-2 format.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body)Body
application/json
```
{
    "countries": [
        {
            "region": {
                "id": 0,
                "name": "string",
                "type": "OTHER"
            },
            "countryCode": "RU"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
countries* |  **Type:** [CountryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#countrydto)[] A list of countries with their codes in the ISO 3166-1 alpha-2 format.  
The country and its code are in the ISO 3166-1 alpha-2 format.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#countrydto)CountryDTO
The country and its code are in the ISO 3166-1 alpha-2 format.
**Name** |  **Description**  
---|---  
countryCode* |  **Type:** string The country of manufacture is in the ISO 3166-1 alpha-2 format. [How to get](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes) _Example:_ `RU` _Min length:_ `2` _Max length:_ `2` _Pattern:_ `^[A-Z]{2}$`  
region* |  **Type:** [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#regiondto) The delivery region.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#regiondto)RegionDTO
The delivery region.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> ID of the region.  
name* |  **Type:** string The name of the region.  
type* |  **Type:** [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#regiontype) The type of region. Possible values:
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
parent |  **Type:** [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#regiondto) The delivery region.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#regiontype)RegionType
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
[RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#regiontype) |  _Enum:_ `OTHER`, `CONTINENT`, `REGION`, `COUNTRY`, `COUNTRY_DISTRICT`, `REPUBLIC`, `CITY`, `VILLAGE`, `CITY_DISTRICT`, `SUBWAY_STATION`, `REPUBLIC_AREA`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/getRegionsCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Directory of delivery services](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/orders/getDeliveryServices)
Next
[Search for a region](https://yandex.ru/dev/market/partner-api/doc/en/reference/regions/en/reference/regions/searchRegionsByName)
