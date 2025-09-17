---
title: In the office - Viewing prices | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/getDefaultPrices
crawled_at: 2025-09-17T14:27:53.735919
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body1)
    * [OfferDefaultPriceListResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpricelistresponsedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype)
    * [OfferDefaultPriceResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpriceresponsedto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#forwardscrollingpagerdto)
    * [OfferDefaultPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpricedto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#currencytype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body7)


# View prices for specified products in all stores
Info
Console
**The method is available for models:[FBY, FBS, Express and DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/_auto/scopes_summary/pages/pricing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns a list of prices that you have set for all stores using any method. For example, through the API or using an Excel template.
Read about the ways to set prices [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/assortment/operations/prices.html).
**, Limit:** 10,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/offer-prices

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body)Body
application/json
```
{
    "offerIds": [
        "string"
    ],
    "archived": false
}

```

**Name** |  **Description**  
---|---  
archived |  **Type:** boolean Whether the product is in the archive.  
offerIds |  **Type:** string[] The IDs of the products that information is needed about.   
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `200` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#200-ok)200 OK
A list of all products with set prices.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "offers": [
            {
                "offerId": "string",
                "price": {
                    "minimumForBestseller": 0,
                    "excludedFromBestsellers": false,
                    "value": 0,
                    "currencyId": "RUR",
                    "discountBase": 0,
                    "updatedAt": "2022-12-29T18:02:01Z"
                }
            }
        ],
        "paging": {
            "nextPageToken": "string"
        }
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OfferDefaultPriceListResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpricelistresponsedto) A list of product prices.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpricelistresponsedto)OfferDefaultPriceListResponseDTO
A list of product prices.
**Name** |  **Description**  
---|---  
offers* |  **Type:** [OfferDefaultPriceResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpriceresponsedto)[] The list of products.  
Information about the set price for the product.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpriceresponsedto)OfferDefaultPriceResponseDTO
Information about the set price for the product.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
price |  **Type:** [OfferDefaultPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpricedto) A price indicating the currency, discount, and time of the last update, as well as the minimum price for entry into the "Best Sellers of the Market" promotion.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#offerdefaultpricedto)OfferDefaultPriceDTO
A price indicating the currency, discount, and time of the last update, as well as the minimum price for entry into the "Best Sellers of the Market" promotion.
**Name** |  **Description**  
---|---  
currencyId |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#currencytype) Currency. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
discountBase |  **Type:** number The crossed-out price. The number must be an integer. You can specify a price with a discount from 5 to 99%. Pass this parameter every time the price is updated if you provide a discount on the product. _Min value (exclusive):_ `0`  
excludedFromBestsellers |  **Type:** boolean A sign that the product is not included in the "Best Sellers of the Market" promotion. Read more about the promotion [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/marketing/promos/market/bestsellers). If the value is `true`, in the method [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/business-assortment/updateBusinessPrices) parameter `minimumForBestseller` ignored.  
minimumForBestseller |  **Type:** number The minimum price of the product to be included in the "Best Sellers of the Market" promotion. Read more about this method of participation. [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/ru/marketing/promos/market/bestsellers#minimum). Passed in the method [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/business-assortment/updateBusinessPrices). _Min value (exclusive):_ `0` _Max value:_ `100000000`  
updatedAt |  **Type:** string<date-time> The time of the last update.  
value |  **Type:** number The price of the product. _Min value (exclusive):_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getDefaultPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
page_token:
limit:
Body{ "offerIds": [ "string" ], "archived": false }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[In the shop](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/assortment/updatePrices)
Next
[In the shop](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/assortment/getPricesByOfferIds)
