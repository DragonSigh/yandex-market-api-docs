---
title: Cabinet Settings - Offices and shops | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/getBusinessSettings
crawled_at: 2025-09-17T14:27:42.508462
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body)
    * [GetBusinessSettingsInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#getbusinesssettingsinfodto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype)
    * [BusinessDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#businessdto)
    * [BusinessSettingsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#businesssettingsdto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#currencytype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body6)


# Cabinet Settings
Info
Console
**The method is available for models:[FBY, FBS, Express and DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/pricing_read-only)
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/promotion_read-only)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/finance-and-accounting)
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/communication)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/settings-management)
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about the account settings, the ID of which is specified in the request.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/settings

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#200-ok)200 OK
Cabinet settings.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "info": {
            "id": 0,
            "name": "string"
        },
        "settings": {
            "onlyDefaultPrice": false,
            "currency": "RUR"
        }
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GetBusinessSettingsInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#getbusinesssettingsinfodto) Information about the account and its settings.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#getbusinesssettingsinfodto)GetBusinessSettingsInfoDTO
Information about the account and its settings.
**Name** |  **Description**  
---|---  
info |  **Type:** [BusinessDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#businessdto) Basic information about the cabinet.  
settings |  **Type:** [BusinessSettingsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#businesssettingsdto) Settings at the cabinet level.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#businessdto)BusinessDTO
Information about the cabinet.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> Cabinet ID.  
name |  **Type:** string Business name.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#businesssettingsdto)BusinessSettingsDTO
Cabinet settings.
**Name** |  **Description**  
---|---  
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#currencytype) Currency [in the seller's office on the Market](https://partner.market.yandex.ru/). _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
onlyDefaultPrice |  **Type:** boolean Product price management:
  * `false` — you can set a price that is valid: 
    * in all cabinet stores — [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/business-assortment/updateBusinessPrices);
    * in a specific store — [POST v2/campaigns/{campaignId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/assortment/updatePrices).
  * `true` — you can only set the price that is valid in all stores in the cabinet, — [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/business-assortment/updateBusinessPrices).

  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/businesses/getBusinessSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Store Information](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/campaigns/getCampaign)
Next
[Store Settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/businesses/en/reference/campaigns/getCampaignSettings)
