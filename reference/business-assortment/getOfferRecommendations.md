---
title: Yandex.Market Recommendations - Prices | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/getOfferRecommendations
crawled_at: 2025-09-17T14:27:32.346267
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body)
    * [PriceCompetitivenessType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#pricecompetitivenesstype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body1)
    * [OfferRecommendationsResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationsresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype)
    * [OfferRecommendationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationdto)
    * [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#scrollingpagerdto)
    * [OfferForRecommendationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerforrecommendationdto)
    * [OfferRecommendationInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationinfodto)
    * [BasePriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#basepricedto)
    * [PriceCompetitivenessThresholdsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#pricecompetitivenessthresholdsdto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#currencytype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body7)


# Yandex.Market's recommendations regarding prices
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/overview/business).**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/_auto/scopes_summary/pages/pricing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


The method returns several types of recommendations.
  1. The threshold for an attractive price.
  2. Evaluation of the attractiveness of prices in the showcase.


The recommendations show you what prices you need to set in order to attract a buyer.
Filters can be used in the request. The results are returned page by page.
**, Limit:** 100 requests per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/offers/recommendations

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body)Body
application/json
```
{
    "offerIds": [
        "string"
    ],
    "competitivenessFilter": "OPTIMAL"
}

```

**Name** |  **Description**  
---|---  
competitivenessFilter |  **Type:** [PriceCompetitivenessType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#pricecompetitivenesstype) A filter that displays products with attractive, moderate, and unattractive prices. _Enum:_ `OPTIMAL`, `AVERAGE`, `LOW`  
offerIds |  **Type:** string[] The IDs of the products that information is needed about. , Do not use this field at the same time as the other filters. If you want to use filters, leave the field empty.  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#pricecompetitivenesstype)PriceCompetitivenessType
The attractiveness of the price:
  * `OPTIMAL` — attractive.
  * `AVERAGE` — moderate.
  * `LOW` "Unattractive."

**Type** |  **Description**  
---|---  
[PriceCompetitivenessType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#pricecompetitivenesstype) |  _Enum:_ `OPTIMAL`, `AVERAGE`, `LOW`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#200-ok)200 OK
A list of products with recommendations.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "paging": {
            "nextPageToken": "string",
            "prevPageToken": "string"
        },
        "offerRecommendations": [
            {
                "offer": {
                    "offerId": "string",
                    "price": {
                        "value": 0,
                        "currencyId": "RUR"
                    },
                    "competitiveness": "OPTIMAL",
                    "shows": 0
                },
                "recommendation": {
                    "offerId": "string",
                    "competitivenessThresholds": {
                        "optimalPrice": {
                            "value": 0,
                            "currencyId": "RUR"
                        },
                        "averagePrice": {
                            "value": 0,
                            "currencyId": "RUR"
                        }
                    }
                }
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OfferRecommendationsResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationsresultdto) A list of products with recommendations.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationsresultdto)OfferRecommendationsResultDTO
A list of products with recommendations.
**Name** |  **Description**  
---|---  
offerRecommendations* |  **Type:** [OfferRecommendationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationdto)[] The product list page.  
Information about the price status and recommendations.  
paging |  **Type:** [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#scrollingpagerdto) Information about the result pages.  
The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationdto)OfferRecommendationDTO
Information about the price status and recommendations.
**Name** |  **Description**  
---|---  
offer |  **Type:** [OfferForRecommendationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerforrecommendationdto) Information about the price status.  
recommendation |  **Type:** [OfferRecommendationInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationinfodto) Recommendations.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#scrollingpagerdto)ScrollingPagerDTO
Information about the result pages.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
prevPageToken |  **Type:** string ID of the previous results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerforrecommendationdto)OfferForRecommendationDTO
Information about the price status of the product.
**Name** |  **Description**  
---|---  
competitiveness |  **Type:** [PriceCompetitivenessType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#pricecompetitivenesstype) The attractiveness of the product price. _Enum:_ `OPTIMAL`, `AVERAGE`, `LOW`  
offerId |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
price |  **Type:** [BasePriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#basepricedto) The price of the product.  
shows |  **Type:** integer<int64> The number of product card impressions in the last 7 days.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#offerrecommendationinfodto)OfferRecommendationInfoDTO
Recommendations regarding the price of the product.
**Name** |  **Description**  
---|---  
competitivenessThresholds |  **Type:** [PriceCompetitivenessThresholdsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#pricecompetitivenessthresholdsdto) The maximum price values at which it is attractive or moderate.  
offerId |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#basepricedto)BasePriceDTO
The price of the product.
**Name** |  **Description**  
---|---  
currencyId* |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#currencytype) Currency. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
value* |  **Type:** number The price of the product. _Min value (exclusive):_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#pricecompetitivenessthresholdsdto)PriceCompetitivenessThresholdsDTO
The maximum price values at which it is attractive or moderate.
**Name** |  **Description**  
---|---  
averagePrice |  **Type:** [BasePriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#basepricedto) The price of the product.  
optimalPrice |  **Type:** [BasePriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#basepricedto) The price of the product.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#currencytype)CurrencyType
Currency codes:
  * `RUR` — the Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getOfferRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
page_token:
limit:
Body{ "offerIds": [ "string" ], "competitivenessFilter": "OPTIMAL" }
Send
No longer supported, please use an alternative and newer version.
Copied
If you have such a price set or lower, it is considered attractive.
### Was the article helpful?
YesNo
Previous
[In the shop](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/assortment/getPricesByOfferIds)
Next
[Viewing quarantine at the price in the cabinet](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/getBusinessQuarantineOffers)
