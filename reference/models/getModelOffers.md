---
title: One model - List of offers for models | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/models/getModelOffers
crawled_at: 2025-09-17T14:46:00.342918
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#query-parameters)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#currencytype)
    * [SortOrderType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#sortordertype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body)
    * [EnrichedModelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#enrichedmodeldto)
    * [ModelOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#modelofferdto)
    * [ModelPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#modelpricedto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body6)


# List of offers for one model
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


Returns information about the first ten offers located on the model's card.
Offers are issued for a specific region and are arranged in the same order in which they are shown in the Market output on the model card.
This method is not supported for group models. The ID of the group model is ignored.
For methods `GET v2/models/{modelId}/offers` and `POST v2/models/offers` The group resource limit is in effect. The limit is imposed on the total number of models, information about which is requested using these methods.
**, Limit:** 100,000 offers per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/models/{modelId}/offers

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
modelId* |  **Type:** integer<int64> The product model ID.  
_Min value (exclusive):_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
regionId* |  **Type:** integer<int64> ID of the region. You can get the region ID using a request [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/regions/searchRegionsByName).  
count |  **Type:** integer<int32> The number of suggestions on the response page.  
_Default:_ `10`  
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#currencytype) The currency in which the prices of offers are displayed on the search results pages. Possible values:
  * `BYN` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.

Default value: the national currency of the store is used (the national currency of the store's country of origin).  
orderByPrice |  **Type:** [SortOrderType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#sortordertype) The direction of sorting by price. Possible values:
  * `ASC` — sort in ascending order.
  * `DESC` — sort in descending order.

Default value: the sentences are displayed in any order.  
page |  **Type:** integer<int32> If the method has `page_token` Use it instead of the parameter `page`. [Learn more about the types of pagination and their use](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/pagination) The number of the results page. Used together with the parameter `pageSize`. `page` ignored if specified `page_token` or `limit`.   
_Default:_ `1` _Max value:_ `10000`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#sortordertype)SortOrderType
Sorting direction:
  * `ASC` — sort in ascending order.
  * `DESC` — sort in descending order.

**Type** |  **Description**  
---|---  
[SortOrderType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#sortordertype) |  _Enum:_ `ASC`, `DESC`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#200-ok)200 OK
A list of suggestions for the model.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body)Body
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
            },
            "offers": [
                {
                    "discount": 0,
                    "name": "string",
                    "pos": 0,
                    "preDiscountPrice": 0,
                    "price": 0,
                    "regionId": 0,
                    "shippingCost": 0,
                    "shopName": "string",
                    "shopRating": 0,
                    "inStock": 0
                }
            ],
            "offlineOffers": 0,
            "onlineOffers": 0
        }
    ],
    "currency": "RUR",
    "regionId": 0
}

```

**Name** |  **Description**  
---|---  
models* |  **Type:** [EnrichedModelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#enrichedmodeldto)[] List of product models.  
The product model.  
The product model.  
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#currencytype) Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

_Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
regionId |  **Type:** integer<int64> ID of the region for which information about the model's offers (delivered to this region) is displayed. You can get information about the region by ID using a request. [GET v2/regions/{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/regions/searchRegionsById).  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#enrichedmodeldto)EnrichedModelDTO
The product model.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> The product model ID.  
name |  **Type:** string The name of the product model.  
offers |  **Type:** [ModelOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#modelofferdto)[] A list of the first ten offers located on the model's card. In response to the request, offers from various stores are returned. If there are several offers from the same store, the response displays only one, the most relevant of them.   
Information about the offer. _Min items:_ `1`  
offlineOffers |  **Type:** integer<int32> The total number of offers in retail stores in the region. All offers from each store are taken into account.  
onlineOffers |  **Type:** integer<int32> The total number of offers in online stores in the region. All offers from each store are taken into account.  
prices |  **Type:** [ModelPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#modelpricedto) Information about prices for the product model.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#modelofferdto)ModelOfferDTO
Information about the offer.
**Name** |  **Description**  
---|---  
discount |  **Type:** integer<int32> Percentage discount on the offer.  
inStock ⦸ |  **Type:** integer<int32> Do not use this option.  
name |  **Type:** string The name of the offer.  
pos |  **Type:** integer<int32> The position of the offer in the Market output on the model card.  
preDiscountPrice |  **Type:** number The offer price without the store's discount.  
price |  **Type:** number The offer price without the discount that the buyer receives when paying via Yandex Pay.  
regionId |  **Type:** integer<int64> The identifier of the region of the offer (the region from where the product is delivered). First, the offers delivered from the region specified in the request parameter are shown. `regionId`. Offers delivered from other regions are shown after them.  
shippingCost |  **Type:** number The cost of shipping the product to the region:
  * `0` — you don't need to pay for the delivery.
  * `-1` — the store does not deliver this product (pickup).

If the shipping cost is unknown, the parameter is not displayed.  
shopName |  **Type:** string The name of the store (as displayed on the Market).  
shopRating |  **Type:** integer<int32> The store's rating. Possible values:
  * `-1` — for stores that have recently appeared on the Market, the rating does not appear immediately. The value is returned for such stores until the rating appears. `-1`.
  * `1`.
  * `2`.
  * `3`.
  * `4`.
  * `5`.

  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#modelpricedto)ModelPriceDTO
Information about prices for the product model.
**Name** |  **Description**  
---|---  
avg |  **Type:** number The average offer price for the model in the region.  
max |  **Type:** number The maximum offer price for a model in the region.  
min |  **Type:** number The minimum offer price for the model in the region.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
modelId*:
Query parameters
regionId*:
currency:
orderByPrice:
count:
page:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Multiple models](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModels)
Next
[Multiple models](https://yandex.ru/dev/market/partner-api/doc/en/reference/models/en/reference/models/getModelsOffers)
