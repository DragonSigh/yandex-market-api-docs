---
title: In the shop - Setting prices | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/updatePrices
crawled_at: 2025-09-17T14:23:34.314304
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body)
    * [OfferPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#offerpricedto)
    * [PriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#pricedto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#currencytype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body1)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body6)
  * [423 Locked](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#423-locked)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body7)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body8)


# Setting prices for products in a specific store
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/pricing)
  * all-methods — Full account management


Sets the prices of the goods in the store. To get the Market's recommendations regarding prices, make a request [POST v2/businesses/{businessId}/offers/recommendations](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/business-assortment/getOfferRecommendations).
The method is only for individual stores
This method is available to you if it is possible to set unique prices in individual stores in the seller's office on the Market. How to check it is in the method [POST v2/businesses/{businessId}/settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/businesses/getBusinessSettings) in the parameter `onlyDefaultPrice` the value is returned `false`.
Otherwise, use the price management method that applies in all stores., — [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/business-assortment/updateBusinessPrices).
The data in the catalog is not updated instantly
It takes up to a few minutes.
**, Limit:** 10,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offer-prices/updates

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body)Body
application/json
```
{
    "offers": [
        {
            "offerId": "string",
            "price": {
                "value": 0,
                "discountBase": 0,
                "currencyId": "RUR",
                "vat": 0
            }
        }
    ]
}

```

**Name** |  **Description**  
---|---  
offers* |  **Type:** [OfferPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#offerpricedto)[] The list of products.  
An item with information about the new price for it. _Min items:_ `1` _Max items:_ `2000`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#offerpricedto)OfferPriceDTO
An item with information about the new price for it.
**Name** |  **Description**  
---|---  
offerId |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
price |  **Type:** [PriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#pricedto) The price includes the discount, currency, and the time of the last update.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#pricedto)PriceDTO
The price includes the discount, currency, and the time of the last update.
**Name** |  **Description**  
---|---  
currencyId |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#currencytype) The currency in which the price of the product is indicated. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
discountBase |  **Type:** number The crossed-out price. The number must be an integer. You can specify a price with a discount from 5 to 99%. Pass this parameter every time the price is updated if you provide a discount on the product. _Min value (exclusive):_ `0`  
value |  **Type:** number The price of the product. _Min value (exclusive):_ `0`  
vat |  **Type:** integer<int32> The VAT identifier used for the product:
  * `2` — 10% VAT. For example, it is used in the sale of certain food and medical products.
  * `5` — 0% VAT. For example, it is used when selling goods exported in the customs procedure of export, or when providing services for the international transportation of goods.
  * `6` — VAT is not charged, it is used only for certain types of services.
  * `7` — 20% VAT. Basic VAT starting in 2019.
  * `10` — 5% VAT. VAT for the simplified taxation system (USN).
  * `11` — 7% VAT. VAT for the simplified taxation system (USN).

If the parameter is omitted, the VAT set in the cabinet is used. **For sellers of the Yandex Go Market** transfer and receipt of VAT is not available.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#200-ok)200 OK
The market has accepted information about the new prices.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body1)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#423-locked)423 Locked
The specified method cannot be applied to the resource. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#423)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#body8)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "offers": [ { "offerId": "string", "price": { "value": 0, "discountBase": 0, "currencyId": "RUR", "vat": 0 } } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[In the office](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/business-assortment/updateBusinessPrices)
Next
[In the office](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/prices/getDefaultPrices)
