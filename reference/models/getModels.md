---
title: Multiple models - Information about models | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/models/getModels
crawled_at: 2025-09-17T14:45:53.609606
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#query-parameters)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#currencytype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body1)
    * [ModelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#modeldto)
    * [ModelPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#modelpricedto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body7)


# Information about multiple models
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


Returns information about product models.
You can get information about up to 100 models in one request.
For methods `GET v2/models`, `GET v2/models/{modelId}` and `POST v2/models` there is a group resource restriction. The limit is imposed on the total number of models, information about which is requested using these methods.
**, Limit:** 100,000 models per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/models

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
regionId* |  **Type:** integer<int64> ID of the region. You can get the region ID using a request [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/regions/searchRegionsByName).  
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#currencytype) The currency in which the prices of offers are displayed on the search results pages. Possible values:
  * `BYN` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.

Default value: the national currency of the store is used (the national currency of the store's country of origin).  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body)Body
application/json
```
{
    "models": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
models* |  **Type:** integer<int64>[] List of models.  
The model ID. _Min value (exclusive):_ `0` _Min items:_ `1` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#200-ok)200 OK
Information about the models.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body1)Body
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
    "regionId": 0
}

```

**Name** |  **Description**  
---|---  
models* |  **Type:** [ModelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#modeldto)[] List of product models.  
The product model.  
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#currencytype) Currency codes:
  * `RUR` — the Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

_Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
regionId |  **Type:** integer<int64> ID of the region for which information about the model's offers (delivered to this region) is displayed. Information about the region by ID can be obtained using a request. [GET v2/regions/{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/regions/searchRegionsById).  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#modeldto)ModelDTO
The product model.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> The product model ID.  
name |  **Type:** string The name of the product model.  
prices |  **Type:** [ModelPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#modelpricedto) Information about prices for the product model.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#modelpricedto)ModelPriceDTO
Information about prices for the product model.
**Name** |  **Description**  
---|---  
avg |  **Type:** number The average offer price for the model in the region.  
max |  **Type:** number The maximum offer price for a model in the region.  
min |  **Type:** number The minimum offer price for the model in the region.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
regionId*:
currency:
Body{ "models": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[One model](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModel)
Next
[One model](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers)
