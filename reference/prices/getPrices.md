---
title: List of prices - Prices | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/getPrices
crawled_at: 2025-09-17T14:45:22.528292
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body)
    * [OfferPriceListResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#offerpricelistresponsedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype)
    * [OfferPriceResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#offerpriceresponsedto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#forwardscrollingpagerdto)
    * [PriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#pricedto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#currencytype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body6)


# List of prices
Deprecated
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/_auto/scopes_summary/pages/pricing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Which method should I use instead of the outdated one?
[POST v2/campaigns/{campaignId}/offer-prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/assortment/getPricesByOfferIds)
Returns a list of prices that you have set for products in any way: for example, via the API or in a catalog file.
How is the total number of products calculated?
According to the data for the last seven days (not including today), it cannot exceed 2 million.
The methods of setting prices are described [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/assortment/operations/prices.html).
**, Limit:** 150,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offer-prices

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
archived |  **Type:** boolean Filter by location in the archive.  
_Default:_ `false`  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#200-ok)200 OK
A list of all products with set prices.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "offers": [
            {
                "id": "string",
                "price": {
                    "value": 0,
                    "discountBase": 0,
                    "currencyId": "RUR",
                    "vat": 0
                },
                "marketSku": 0,
                "updatedAt": "2022-12-29T18:02:01Z"
            }
        ],
        "paging": {
            "nextPageToken": "string"
        },
        "total": 0
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OfferPriceListResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#offerpricelistresponsedto) A list of product prices.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#offerpricelistresponsedto)OfferPriceListResponseDTO
A list of product prices.
**Name** |  **Description**  
---|---  
offers* |  **Type:** [OfferPriceResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#offerpriceresponsedto)[] The list page.  
Information about the set price for the product.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#forwardscrollingpagerdto) The ID of the next page.  
total |  **Type:** integer<int32> The number of all the store's prices changed via the API.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#offerpriceresponsedto)OfferPriceResponseDTO
Information about the set price for the product.
**Name** |  **Description**  
---|---  
id |  **Type:** string The ID of the offer from the price list.  
marketSku |  **Type:** integer<int64> The ID of the product card on the Market. _Min value:_ `1`  
price |  **Type:** [PriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#pricedto) The price includes the discount, currency, and the time of the last update.  
updatedAt |  **Type:** string<date-time> The date and time of the last update of the product price.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#pricedto)PriceDTO
The price includes the discount, currency, and the time of the last update.
**Name** |  **Description**  
---|---  
currencyId |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#currencytype) The currency in which the price of the product is indicated. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
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
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/prices/getPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
page_token:
limit:
archived:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Viewing matching cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/business-assortment/getSuggestedOfferMappings)
Next
[Prices for promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/prices/en/reference/assortment/getSuggestedPrices)
