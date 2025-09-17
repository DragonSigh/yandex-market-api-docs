---
title: Product model search - Product models | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/models/searchModels
crawled_at: 2025-09-17T14:25:23.729670
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#query-parameters)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#currencytype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body)
    * [ModelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#modeldto)
    * [FlippingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#flippingpagerdto)
    * [ModelPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#modelpricedto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body6)


# Product model search
Deprecated
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/overview/dbs) model.**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about models that meet the search conditions specified in the query.
You can get information about up to 100 models in one request.
For methods `GET v2/models`, `GET v2/models/{modelId}` and `POST v2/models` The group resource limit is in effect. The limit is imposed on the total number of models, information about which is requested using these methods.
**, Limit:** 100,000 models per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/models

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
query* |  **Type:** string A search query for the product model name.  
regionId* |  **Type:** integer<int64> ID of the region. You can get the region ID using a request [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/regions/searchRegionsByName).  
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#currencytype) The currency in which the prices of offers are displayed on the search results pages. Possible values:
  * `BYN` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `RUR` — the Russian ruble.
  * `UAH` — the Ukrainian hryvnia.

Default value: the national currency of the store is used (the national currency of the store's country of origin).  
page |  **Type:** integer<int32> If the method has `page_token` Use it instead of the parameter `page`. [Learn more about the types of pagination and their use](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/pagination) The number of the results page. Used together with the parameter `pageSize`. `page` ignored if specified `page_token` or `limit`.   
_Default:_ `1` _Max value:_ `10000`  
pageSize |  **Type:** integer<int32> Page size. Used together with the parameter `page`. `pageSize` ignored if specified `page_token` or `limit`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#200-ok)200 OK
Information about the models.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body)Body
application/json
```
{
    "models": [
        {
            "id": 0,
            "name": "string",
            "prices": {
                "avg": 0,
                "max": 0,
                "min": 0
            }
        }
    ],
    "currency": "RUR",
    "regionId": 0,
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
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#currencytype) Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

_Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
models |  **Type:** [ModelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#modeldto)[] List of product models.  
The product model.  
pager |  **Type:** [FlippingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#flippingpagerdto) A model for pagination.  
regionId |  **Type:** integer<int64> ID of the region for which information about the model's offers (delivered to this region) is displayed. You can get information about the region by ID using a request. [GET v2/regions/{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/regions/searchRegionsById).  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#modeldto)ModelDTO
The product model.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> The product model ID.  
name |  **Type:** string The name of the product model.  
prices |  **Type:** [ModelPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#modelpricedto) Information about prices for the product model.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#flippingpagerdto)FlippingPagerDTO
A model for pagination.
**Name** |  **Description**  
---|---  
currentPage |  **Type:** integer<int32> The current page.  
from |  **Type:** integer<int32> The initial number of the found element on the page.  
pageSize |  **Type:** integer<int32> Page size.  
pagesCount |  **Type:** integer<int32> The total number of pages.  
to |  **Type:** integer<int32> The final number of the found element on the page.  
total |  **Type:** integer<int32> How many items were found in total.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#modelpricedto)ModelPriceDTO
Information about prices for the product model.
**Name** |  **Description**  
---|---  
avg |  **Type:** number The average offer price for the model in the region.  
max |  **Type:** number The maximum offer price for a model in the region.  
min |  **Type:** number The minimum offer price for the model in the region.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/searchModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
query*:
regionId*:
currency:
page:
pageSize:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Multiple models](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelsOffers)
Next
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/push-notifications/)
