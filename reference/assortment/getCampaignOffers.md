---
title: In the shop - Viewing products | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/getCampaignOffers
crawled_at: 2025-09-17T14:29:37.199632
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body)
    * [OfferCampaignStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offercampaignstatustype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body1)
    * [GetCampaignOffersResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getcampaignoffersresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype)
    * [GetCampaignOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getcampaignofferdto)
    * [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#scrollingpagerdto)
    * [GetPriceWithDiscountDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getpricewithdiscountdto)
    * [GetPriceWithVatDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getpricewithvatdto)
    * [OfferErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offererrordto)
    * [QuantumDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#quantumdto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#currencytype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body7)


# Information about the products that are placed in the specified store
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns a list of products that are placed in the specified store. The placement parameters are specified for each product.
**, Limit:** 10,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offers

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body)Body
application/json
```
{
    "offerIds": [
        "string"
    ],
    "statuses": [
        "PUBLISHED"
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
categoryIds |  **Type:** integer<int32>[] Filter by category on the Market.  
_Min value (exclusive):_ `0` _Min items:_ `1` _Unique items_  
offerIds |  **Type:** string[] The IDs of the products that information is needed about. This list is returned only in its entirety. Do not use this field at the same time as filters based on card statuses, categories, brands, or tags. If you want to use filters, leave the field empty. If you are requesting information on specific SKUs, do not fill in:
  * `page_token`
  * `limit`

  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `200` _Unique items_  
statuses |  **Type:** [OfferCampaignStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offercampaignstatustype)[] Filter by product status.   
Product status:
  * `PUBLISHED` — Ready for sale.
  * `CHECKING` — On inspection.
  * `DISABLED_BY_PARTNER` — Hidden by you.
  * `REJECTED_BY_MARKET` — Rejected.
  * `DISABLED_AUTOMATICALLY` — Fix the errors.
  * `CREATING_CARD` — A card is being created.
  * `NO_CARD` — I need a card.
  * `NO_STOCKS` — Not in stock.
  * `ARCHIVED` — In the archive.

[What does each of the statuses mean?](https://yandex.ru/support/marketplace/assortment/add/statuses.html) _Enum:_ `PUBLISHED`, `CHECKING`, `DISABLED_BY_PARTNER`, `DISABLED_AUTOMATICALLY`, `REJECTED_BY_MARKET`, `CREATING_CARD`, `NO_CARD`, `NO_STOCKS`, `ARCHIVED` _Min items:_ `1` _Unique items_  
tags |  **Type:** string[] Filter by tags.  
_Min items:_ `1` _Unique items_  
vendorNames |  **Type:** string[] Filter by brand.  
_Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offercampaignstatustype)OfferCampaignStatusType
Product status:
  * `PUBLISHED` — Ready for sale.
  * `CHECKING` — On inspection.
  * `DISABLED_BY_PARTNER` — Hidden by you.
  * `REJECTED_BY_MARKET` — Rejected.
  * `DISABLED_AUTOMATICALLY` — Fix the errors.
  * `CREATING_CARD` — A card is being created.
  * `NO_CARD` — I need a card.
  * `NO_STOCKS` — Not in stock.
  * `ARCHIVED` — In the archive.


[What does each of the statuses mean?](https://yandex.ru/support/marketplace/assortment/add/statuses.html)
**Type** |  **Description**  
---|---  
[OfferCampaignStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offercampaignstatustype) |  _Enum:_ `PUBLISHED`, `CHECKING`, `DISABLED_BY_PARTNER`, `DISABLED_AUTOMATICALLY`, `REJECTED_BY_MARKET`, `CREATING_CARD`, `NO_CARD`, `NO_STOCKS`, `ARCHIVED`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#200-ok)200 OK
A list of products placed in the specified store.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body1)Body
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
                "quantum": {
                    "minQuantity": 0,
                    "stepQuantity": 0
                },
                "available": false,
                "basicPrice": {
                    "value": 0,
                    "currencyId": "RUR",
                    "discountBase": 0,
                    "updatedAt": "2022-12-29T18:02:01Z"
                },
                "campaignPrice": {
                    "value": 0,
                    "discountBase": 0,
                    "currencyId": "RUR",
                    "vat": 0,
                    "updatedAt": "2022-12-29T18:02:01Z"
                },
                "status": "PUBLISHED",
                "errors": [
                    {
                        "message": "string",
                        "comment": "string"
                    }
                ],
                "warnings": [
                    {
                        "message": "string",
                        "comment": "string"
                    }
                ]
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GetCampaignOffersResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getcampaignoffersresultdto) The list of products in the specified store.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getcampaignoffersresultdto)GetCampaignOffersResultDTO
The list of products in the specified store.
**Name** |  **Description**  
---|---  
offers* |  **Type:** [GetCampaignOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getcampaignofferdto)[] The product list page.  
Product placement parameters in the store.  
Information about the new product price.  
paging |  **Type:** [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#scrollingpagerdto) Information about the result pages.  
The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getcampaignofferdto)GetCampaignOfferDTO
Product placement parameters in the store.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
available ⦸ |  **Type:** boolean Instead, use methods to hide goods from the showcase.
  * [GET v2/campaigns/{campaignId}/hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getHiddenOffers) — view hidden goods;
  * [POST v2/campaigns/{campaignId}/hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/addHiddenOffers) — hiding of goods;
  * [POST v2/campaigns/{campaignId}/hidden-offers/delete](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers) — resumption of the show.

Whether the product is on sale.  
basicPrice |  **Type:** [GetPriceWithDiscountDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getpricewithdiscountdto) The price of the product for all stores.  
Price with discount indication.  
The time of the last update.  
campaignPrice |  **Type:** [GetPriceWithVatDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getpricewithvatdto) The price set in a separate store.  
The price includes the discount, currency, and the time of the last update.  
The time of the last update.  
errors |  **Type:** [OfferErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offererrordto)[] Errors that prevent the product from being placed in the showcase.   
An error message related to the product placement. _Min items:_ `1`  
quantum ⦸ |  **Type:** [QuantumDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#quantumdto) Setting up a quantum sale. [What does it mean?](https://yandex.ru/support/marketplace/assortment/fields/quantum.html)  
status |  **Type:** [OfferCampaignStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offercampaignstatustype) Product status:
  * `PUBLISHED` — Ready for sale.
  * `CHECKING` — On inspection.
  * `DISABLED_BY_PARTNER` — Hidden by you.
  * `REJECTED_BY_MARKET` — Rejected.
  * `DISABLED_AUTOMATICALLY` — Fix the errors.
  * `CREATING_CARD` — A card is being created.
  * `NO_CARD` — I need a card.
  * `NO_STOCKS` — Not in stock.
  * `ARCHIVED` — In the archive.

[What does each of the statuses mean?](https://yandex.ru/support/marketplace/assortment/add/statuses.html) _Enum:_ `PUBLISHED`, `CHECKING`, `DISABLED_BY_PARTNER`, `DISABLED_AUTOMATICALLY`, `REJECTED_BY_MARKET`, `CREATING_CARD`, `NO_CARD`, `NO_STOCKS`, `ARCHIVED`  
warnings |  **Type:** [OfferErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offererrordto)[] Warnings that do not prevent the product from being placed in the showcase.   
An error message related to the product placement. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#scrollingpagerdto)ScrollingPagerDTO
Information about the result pages.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
prevPageToken |  **Type:** string ID of the previous results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getpricewithdiscountdto)GetPriceWithDiscountDTO
The price includes the currency, discount, and the time of the last update.
**Name** |  **Description**  
---|---  
updatedAt* |  **Type:** string<date-time> The time of the last update.  
currencyId |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#currencytype) Currency. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
discountBase |  **Type:** number The crossed-out price. The number must be an integer. You can specify a price with a discount from 5 to 99%. Pass this parameter every time the price is updated if you provide a discount on the product. _Min value (exclusive):_ `0`  
value |  **Type:** number The price of the product. _Min value (exclusive):_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#getpricewithvatdto)GetPriceWithVatDTO
The price includes VAT and the time of the last update.
**Name** |  **Description**  
---|---  
updatedAt* |  **Type:** string<date-time> The time of the last update.  
currencyId |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#currencytype) The currency in which the price of the product is indicated. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
discountBase |  **Type:** number The crossed-out price. The number must be an integer. You can specify a price with a discount from 5 to 99%. Pass this parameter every time the price is updated if you provide a discount on the product. _Min value (exclusive):_ `0`  
value |  **Type:** number The price of the product. _Min value (exclusive):_ `0`  
vat |  **Type:** integer<int32> The VAT identifier used for the product:
  * `2` — 10% VAT. For example, it is used in the sale of certain food and medical products.
  * `5` — 0% VAT. For example, it is used for the sale of goods exported in the customs procedure of export, or for the provision of services for the international transportation of goods.
  * `6` — VAT is not charged, it is used only for certain types of services.
  * `7` — 20% VAT. Basic VAT starting in 2019.
  * `10` — 5% VAT. VAT for the simplified taxation system (USN).
  * `11` — 7% VAT. VAT for the simplified taxation system (USN).

If the parameter is omitted, the VAT set in the cabinet is used. **For sellers of the Yandex Go Market** transfer and receipt of VAT is not available.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#offererrordto)OfferErrorDTO
An error message related to the product placement.
**Name** |  **Description**  
---|---  
comment |  **Type:** string Explanation.  
message |  **Type:** string The type of error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#quantumdto)QuantumDTO
Setting up a quantum sale.
To reset the previously set values, pass an empty parameter `quantum`.
Example
```
{
  "offers": [
    {
      "offerId": "08e35dc1-89a2-11e3-8055-0015e9b8c48d",
      "quantum": {}
    }
  ]
}

```

**Name** |  **Description**  
---|---  
minQuantity |  **Type:** integer<int32> The minimum number of product units in the order. For example, if you specify 10, the customer will be able to add at least 10 items to the cart. If the quantity of goods in stock is less than the specified quantity, the restriction will not work and the buyer will be able to order it. _Min value:_ `1`  
stepQuantity |  **Type:** integer<int32> By how many units the buyer will be able to increase the quantity of goods in the basket. For example, if you set 5, the buyer will be able to add only 5, 10, 15, ... items to the order. If the quantity of goods in stock does not reach the quantum, the restriction will not work and the buyer will be able to order a quantity that is not a multiple of the quantum. _Min value:_ `1` _Max value:_ `100`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#currencytype)CurrencyType
Currency codes:
  * `RUR` — the Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
page_token:
limit:
Body{ "offerIds": [ "string" ], "statuses": [ "PUBLISHED" ], "categoryIds": [ 0 ], "vendorNames": [ "string" ], "tags": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[In the office](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/business-assortment/getOfferMappings)
Next
[In the office](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/business-assortment/deleteOffers)
