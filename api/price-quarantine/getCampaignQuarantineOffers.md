---
title: Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/getCampaignQuarantineOffers
crawled_at: 2025-09-17T14:43:02.781107
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body)
    * [OfferCardStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#offercardstatustype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body1)
    * [GetQuarantineOffersResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#getquarantineoffersresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype)
    * [QuarantineOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#quarantineofferdto)
    * [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#scrollingpagerdto)
    * [BasePriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#basepricedto)
    * [PriceQuarantineVerdictDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictdto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#currencytype)
    * [PriceQuarantineVerdictParameterDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictparameterdto)
    * [PriceQuarantineVerdictType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdicttype)
    * [PriceQuarantineVerdictParamNameType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictparamnametype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body7)


# List of quarantined products by price in the store
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/_auto/scopes_summary/pages/pricing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns a list of products that are in quarantine at the price set in the specified store.
Check the price of each of the quarantined items. If there is no error and the price is correct, confirm it with a request. [POST v2/campaigns/{campaignId}/price-quarantine/confirm](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/reference/assortment/confirmCampaignPrices). If the price is really wrong, set the correct price using a query. [POST v2/campaigns/{campaignId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/reference/assortment/updatePrices).
What is quarantine?
A product is quarantined if its price changes too sharply or differs too much from the market price. [More detailed](https://yandex.ru/support/marketplace/assortment/operations/prices.html#quarantine)
Filters can be used in the request.
The results are returned page by page.
**, Limit:** 10,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/price-quarantine

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body)Body
application/json
```
{
    "offerIds": [
        "string"
    ],
    "cardStatuses": [
        "HAS_CARD_CAN_NOT_UPDATE"
    ],
    "categoryIds": [
        0
    ],
    "vendorNames": [
        "string"
    ],
    "tags": [
        "string"
    ]
}

```

**Name** |  **Description**  
---|---  
cardStatuses |  **Type:** [OfferCardStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#offercardstatustype)[] Filter by card status. [What is a product card?](https://yandex.ru/support/marketplace/assortment/content/index.html)   
Product card status:
  * `HAS_CARD_CAN_NOT_UPDATE` — The Market card.
  * `HAS_CARD_CAN_UPDATE` — It can be supplemented.
  * `HAS_CARD_CAN_UPDATE_ERRORS` — The changes have not been accepted.
  * `HAS_CARD_CAN_UPDATE_PROCESSING` — Changes are under review.
  * `NO_CARD_NEED_CONTENT` — Create a card.
  * `NO_CARD_MARKET_WILL_CREATE` — Creates a Marketplace.
  * `NO_CARD_ERRORS` — It wasn't created because of a mistake.
  * `NO_CARD_PROCESSING` — We check the data.
  * `NO_CARD_ADD_TO_CAMPAIGN` — Place the product in the store.

_Enum:_ `HAS_CARD_CAN_NOT_UPDATE`, `HAS_CARD_CAN_UPDATE`, `HAS_CARD_CAN_UPDATE_ERRORS`, `HAS_CARD_CAN_UPDATE_PROCESSING`, `NO_CARD_NEED_CONTENT`, `NO_CARD_MARKET_WILL_CREATE`, `NO_CARD_ERRORS`, `NO_CARD_PROCESSING`, `NO_CARD_ADD_TO_CAMPAIGN` _Min items:_ `1` _Unique items_  
categoryIds |  **Type:** integer<int32>[] Filter by category on the Market.  
_Min value (exclusive):_ `0` _Min items:_ `1` _Unique items_  
offerIds |  **Type:** string[] The IDs of the products that information is needed about.   
  
Do not use this field at the same time as filters based on card statuses, categories, brands, or tags. If you want to use filters, leave the field empty.   
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `500` _Unique items_  
tags |  **Type:** string[] Filter by tags.  
_Min items:_ `1` _Unique items_  
vendorNames |  **Type:** string[] Filter by brand.  
_Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#offercardstatustype)OfferCardStatusType
Product card status:
  * `HAS_CARD_CAN_NOT_UPDATE` — The Market card.
  * `HAS_CARD_CAN_UPDATE` — It can be supplemented.
  * `HAS_CARD_CAN_UPDATE_ERRORS` — The changes have not been accepted.
  * `HAS_CARD_CAN_UPDATE_PROCESSING` — Changes are under review.
  * `NO_CARD_NEED_CONTENT` — Create a card.
  * `NO_CARD_MARKET_WILL_CREATE` — Creates a Marketplace.
  * `NO_CARD_ERRORS` — It wasn't created because of a mistake.
  * `NO_CARD_PROCESSING` — We check the data.
  * `NO_CARD_ADD_TO_CAMPAIGN` — Place the product in the store.

**Type** |  **Description**  
---|---  
[OfferCardStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#offercardstatustype) |  _Enum:_ `HAS_CARD_CAN_NOT_UPDATE`, `HAS_CARD_CAN_UPDATE`, `HAS_CARD_CAN_UPDATE_ERRORS`, `HAS_CARD_CAN_UPDATE_PROCESSING`, `NO_CARD_NEED_CONTENT`, `NO_CARD_MARKET_WILL_CREATE`, `NO_CARD_ERRORS`, `NO_CARD_PROCESSING`, `NO_CARD_ADD_TO_CAMPAIGN`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#200-ok)200 OK
The list of products in quarantine.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "paging": {
            "nextPageToken": "string",
            "prevPageToken": "string"
        },
        "offers": [
            {
                "offerId": "string",
                "currentPrice": {
                    "value": 0,
                    "currencyId": "RUR"
                },
                "lastValidPrice": {
                    "value": 0,
                    "currencyId": "RUR"
                },
                "verdicts": [
                    {
                        "type": "PRICE_CHANGE",
                        "params": [
                            {
                                "name": "CURRENT_PRICE",
                                "value": "string"
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
result |  **Type:** [GetQuarantineOffersResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#getquarantineoffersresultdto) The list of products in quarantine.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#getquarantineoffersresultdto)GetQuarantineOffersResultDTO
The list of products in quarantine.
**Name** |  **Description**  
---|---  
offers* |  **Type:** [QuarantineOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#quarantineofferdto)[] The page of the list of products in quarantine.  
The product is in quarantine.  
paging |  **Type:** [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#scrollingpagerdto) Information about the result pages.  
The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#quarantineofferdto)QuarantineOfferDTO
The product is in quarantine.
**Name** |  **Description**  
---|---  
currentPrice ⦸ |  **Type:** [BasePriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#basepricedto) The price of the product.  
lastValidPrice ⦸ |  **Type:** [BasePriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#basepricedto) The price of the product.  
offerId |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
verdicts |  **Type:** [PriceQuarantineVerdictDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictdto)[] The reasons for the product being quarantined.  
The reason for the product being quarantined. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#scrollingpagerdto)ScrollingPagerDTO
Information about the result pages.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
prevPageToken |  **Type:** string ID of the previous results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#basepricedto)BasePriceDTO
The price of the product.
**Name** |  **Description**  
---|---  
currencyId* |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#currencytype) Currency. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
value* |  **Type:** number The price of the product. _Min value (exclusive):_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictdto)PriceQuarantineVerdictDTO
The reason for the product being quarantined.
**Name** |  **Description**  
---|---  
params* |  **Type:** [PriceQuarantineVerdictParameterDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictparameterdto)[] The price that caused the product to be quarantined, and the values for comparison. The specific set of parameters depends on the type of quarantine.  
The quarantine parameter.  
type |  **Type:** [PriceQuarantineVerdictType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdicttype) The type of quarantine. _Enum:_ `PRICE_CHANGE`, `LOW_PRICE`, `LOW_PRICE_PROMO`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#currencytype)CurrencyType
Currency codes:
  * `RUR` — the Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictparameterdto)PriceQuarantineVerdictParameterDTO
The quarantine parameter.
**Name** |  **Description**  
---|---  
name* |  **Type:** [PriceQuarantineVerdictParamNameType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictparamnametype) The name of the parameter. _Enum:_ `CURRENT_PRICE`, `LAST_VALID_PRICE`, `MIN_PRICE`, `CURRENCY`  
value* |  **Type:** string The value of the parameter.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdicttype)PriceQuarantineVerdictType
Types of quarantine:
  * `PRICE_CHANGE` — the new price differs too much from the previous one. In the field `params` There will be a new price `CURRENT_PRICE` and the last price before being quarantined `LAST_VALID_PRICE`.
  * `LOW_PRICE` — the set price differs too much from the market price. In the field `params` the price will be set by you `CURRENT_PRICE` and the quarantine threshold `MIN_PRICE`.
  * `LOW_PRICE_PROMO` — the price after applying the shares differs too much from the market price. In the field `params` there will be a price after applying the shares `CURRENT_PRICE` and the quarantine threshold `MIN_PRICE`.

**Type** |  **Description**  
---|---  
[PriceQuarantineVerdictType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdicttype) |  _Enum:_ `PRICE_CHANGE`, `LOW_PRICE`, `LOW_PRICE_PROMO`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictparamnametype)PriceQuarantineVerdictParamNameType
The name of the parameter for the reason for hiding the product by price.
  * `CURRENT_PRICE` — the price that caused the product to be quarantined.
  * `LAST_VALID_PRICE` — the last price before entering quarantine (only for quarantine type `PRICE_CHANGE`).
  * `MIN_PRICE` — quarantine threshold (only for quarantine types `LOW_PRICE` and `LOW_PRICE_PROMO`).
  * `CURRENCY` — currency.

**Type** |  **Description**  
---|---  
[PriceQuarantineVerdictParamNameType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#pricequarantineverdictparamnametype) |  _Enum:_ `CURRENT_PRICE`, `LAST_VALID_PRICE`, `MIN_PRICE`, `CURRENCY`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/api/price-quarantine/en/api/price-quarantine/getCampaignQuarantineOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
page_token:
limit:
Body{ "offerIds": [ "string" ], "cardStatuses": [ "HAS_CARD_CAN_NOT_UPDATE" ], "categoryIds": [ 0 ], "vendorNames": [ "string" ], "tags": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
