---
title: Prices for promotion - Prices | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/getSuggestedPrices
crawled_at: 2025-09-17T14:46:33.434504
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body)
    * [SuggestOfferPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#suggestofferpricedto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body1)
    * [SuggestPricesResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#suggestpricesresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype)
    * [PriceSuggestOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggestofferdto)
    * [PriceSuggestDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggestdto)
    * [PriceSuggestType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggesttype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body7)


# Prices for product promotion
Deprecated
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/pricing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Which method should I use instead of the outdated one?
[POST v2/reports/goods-prices/generate](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/reports/generateGoodsPricesReport)
The method is only for some stores
This method is only suitable for those stores that set prices for goods in rubles.
Returns prices for the promotion of products that you place on the Market.
The products for which prices need to be obtained are transmitted in the body of the POST request.
The prices for the promotion depend on the prices set for products by other stores. If several stores supply the same product, the lower-priced product is sold on the Market first. When the low-price product runs out, the higher-price product will start selling.
The output data contains several prices for each product, corresponding to different types of promotion.
You can set prices for products using a request. [POST v2/campaigns/{campaignId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/updatePrices) or in other ways: for example, specify them in a file with a directory. You can also use strategies to automatically set recommended prices or minimum prices on the Market.
Detailed information about automatic price management is provided [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/marketing/prices.html).
**, Limit:** 100,000 products per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offer-prices/suggestions

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body)Body
application/json
```
{
    "offers": [
        {
            "offerId": "string",
            "marketSku": 0
        }
    ]
}

```

**Name** |  **Description**  
---|---  
offers* |  **Type:** [SuggestOfferPriceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#suggestofferpricedto)[] The list of products.  
The product for which you need to get prices for promotion. _Max items:_ `1000`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#suggestofferpricedto)SuggestOfferPriceDTO
The product for which you need to get prices for promotion.
**Name** |  **Description**  
---|---  
marketSku |  **Type:** integer<int64> The ID of the product card on the Market. _Min value:_ `1`  
offerId |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#200-ok)200 OK
A list of prices for promotion on the Market.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "offers": [
            {
                "marketSku": 0,
                "offerId": "string",
                "priceSuggestion": [
                    {
                        "type": "BUYBOX",
                        "price": 0
                    }
                ]
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [SuggestPricesResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#suggestpricesresultdto) The result of a price request for promotion.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#suggestpricesresultdto)SuggestPricesResultDTO
The result of a price request for promotion.
**Name** |  **Description**  
---|---  
offers* |  **Type:** [PriceSuggestOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggestofferdto)[] A list of products with prices for promotion.  
An item with prices for promotion.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggestofferdto)PriceSuggestOfferDTO
An item with prices for promotion.
**Name** |  **Description**  
---|---  
marketSku |  **Type:** integer<int64> The ID of the product card on the Market. _Min value:_ `1`  
offerId |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
priceSuggestion |  **Type:** [PriceSuggestDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggestdto)[] Prices for promotion.   
The type of price. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggestdto)PriceSuggestDTO
The type of price.
**Name** |  **Description**  
---|---  
price |  **Type:** number The price is in rubles.  
type |  **Type:** [PriceSuggestType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggesttype) The type of price. _Enum:_ `BUYBOX`, `DEFAULT_OFFER`, `MIN_PRICE_MARKET`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggesttype)PriceSuggestType
Price type:
  * `BUYBOX` — the lowest price of the product at which it is currently being sold. This price is updated in real time. If you set the price lower, your offer will start showing. If for this value in the parameter `price` the price shown is the same as yours, which means that your product is already being shown in the window. If other sellers besides you sell this product at the same price, their offers will also be displayed along with yours in turn.
  * `DEFAULT_OFFER` — the price recommended by the Market, which attracts buyers. It is calculated only for popular products on the service and is updated every four hours.
  * `MIN_PRICE_MARKET` — the minimum price on the Market. The lowest price among all product offers on the Market in all regions, including those that are not visible in the showcase. This price is updated in real time and provides more impressions on the Market than the lowest or recommended price.

**Type** |  **Description**  
---|---  
[PriceSuggestType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#pricesuggesttype) |  _Enum:_ `BUYBOX`, `DEFAULT_OFFER`, `MIN_PRICE_MARKET`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getSuggestedPrices#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "offers": [ { "offerId": "string", "marketSku": 0 } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[List of prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/prices/getPrices)
Next
[Transfer of "Fair Sign" codes](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/orders/provideOrderItemCis)
