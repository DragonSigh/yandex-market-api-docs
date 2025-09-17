---
title: Recommended rates - Sales Boost | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/getBidsRecommendations
crawled_at: 2025-09-17T14:40:56.215980
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body1)
    * [GetBidsRecommendationsResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#getbidsrecommendationsresponsedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype)
    * [SkuBidRecommendationItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#skubidrecommendationitemdto)
    * [BidRecommendationItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#bidrecommendationitemdto)
    * [PriceRecommendationItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#pricerecommendationitemdto)
    * [BenefitType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#benefittype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body7)


# Recommended bids for specified products
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/overview/business).**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/_auto/scopes_summary/pages/pricing_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/_auto/scopes_summary/pages/promotion_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns recommended bids for specified products, which provides your offers with a certain percentage of impressions and additional promotion tools.
One recommended bid or several may be returned for a single product. In the second case, different bids are designed to achieve a different percentage of impressions and obtain additional promotion tools.
If the product has just been added to the catalog, but is not yet on sale, there will be no recommended bid for it.
A single request can contain a maximum of 1,500 products.
**, Limit:** 1,000 requests per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/bids/recommendations

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body)Body
application/json
```
{
    "skus": [
        "string"
    ]
}

```

**Name** |  **Description**  
---|---  
skus* |  **Type:** string[] A list of products for which you need to get recommendations on rates.   
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `1500` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#200-ok)200 OK
Recommended bids for the specified products.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "recommendations": [
            {
                "sku": "string",
                "bid": 570,
                "bidRecommendations": [
                    {
                        "bid": 570,
                        "showPercent": 0,
                        "benefits": [
                            "BESTS"
                        ]
                    }
                ],
                "priceRecommendations": [
                    {
                        "campaignId": 0,
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
result |  **Type:** [GetBidsRecommendationsResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#getbidsrecommendationsresponsedto) A list of products with recommended rates.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#getbidsrecommendationsresponsedto)GetBidsRecommendationsResponseDTO
A list of products with recommended rates.
**Name** |  **Description**  
---|---  
recommendations* |  **Type:** [SkuBidRecommendationItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#skubidrecommendationitemdto)[] A list of products with recommended rates.  
A list of products with recommended rates.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#skubidrecommendationitemdto)SkuBidRecommendationItemDTO
A list of products with recommended rates.
**Name** |  **Description**  
---|---  
bid* |  **Type:** integer<int32> The value of the recommended bid for the product from the parameter `sku`, from 50 to 9999. It is indicated as a percentage of the cost of the product and multiplied by 100. For example, the 5% rate is indicated as 500. The response is not empty. `bidRecommendations` Don't pay attention to this field. _Example:_ `570` _Min value:_ `0` _Max value:_ `9999`  
sku* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
bidRecommendations |  **Type:** [BidRecommendationItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#bidrecommendationitemdto)[] A list of recommended bids with the corresponding impression shares and available additional promotion tools. The higher the bid, the greater the share of impressions it helps to get and the more additional promotion tools are available.   
The recommended bid, the possible percentage of impressions, and the additional promotion tools available. _Min items:_ `1`  
priceRecommendations ⦸ |  **Type:** [PriceRecommendationItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#pricerecommendationitemdto)[] Recommended prices.  
The recommended price. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#bidrecommendationitemdto)BidRecommendationItemDTO
The recommended bid, the possible percentage of impressions, and the additional promotion tools available.
**Name** |  **Description**  
---|---  
bid* |  **Type:** integer<int32> The value of the recommended bid for the product from the parameter `sku`, from 50 to 9999. It is indicated as a percentage of the cost of the product and multiplied by 100. For example, the 5% rate is indicated as 500. _Example:_ `570` _Min value:_ `0` _Max value:_ `9999`  
showPercent* |  **Type:** integer<int64> The percentage of impressions. _Min value:_ `0` _Max value:_ `100`  
benefits |  **Type:** [BenefitType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#benefittype)[] A list of available subsidies. To get the necessary promotion tool, set the bid that will be recommended for this tool or higher.   
Types of additional promotion tools:
  * `BESTS` — participation in the "Best Sellers of the Market" campaign.
  * `SPLIT_0_0_4` — the possibility of payment with a Split for a period of 4 months.
  * `SPLIT_0_0_6` — the possibility of payment with a split for a period of 6 months.
  * `SPLIT_0_0_12` — the possibility of payment with a Split for a period of 12 months.
  * `MARKET_SUBSIDY_1_4` — discount from the Market from 1 to 4%.
  * `MARKET_SUBSIDY_5_9` — discount from the Market from 5 to 9%.
  * `MARKET_SUBSIDY_10` — discount from the Market starting from 10%.

_Enum:_ `BESTS`, `SPLIT_0_0_4`, `SPLIT_0_0_6`, `SPLIT_0_0_12`, `MARKET_SUBSIDY_1_4`, `MARKET_SUBSIDY_5_9`, `MARKET_SUBSIDY_10` _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#pricerecommendationitemdto)PriceRecommendationItemDTO
The recommended price.
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
price* |  **Type:** number<decimal> The recommended price of the product. In order for the promotion to work well, the price of the product should not be higher than this value. [More information about recommended prices](https://yandex.ru/support/marketplace/marketing/campaigns.html#prices) _Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#benefittype)BenefitType
Types of additional promotion tools:
  * `BESTS` — participation in the "Best Sellers of the Market" campaign.
  * `SPLIT_0_0_4` — the possibility of payment with a Split for a period of 4 months.
  * `SPLIT_0_0_6` — the possibility of paying with a Split for a period of 6 months.
  * `SPLIT_0_0_12` — the ability to pay with a Split for a period of 12 months.
  * `MARKET_SUBSIDY_1_4` — discount from the Market from 1 to 4%.
  * `MARKET_SUBSIDY_5_9` — discount from the Market from 5 to 9%.
  * `MARKET_SUBSIDY_10` — discount from the Market starting from 10%.

**Type** |  **Description**  
---|---  
[BenefitType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#benefittype) |  _Enum:_ `BESTS`, `SPLIT_0_0_4`, `SPLIT_0_0_6`, `SPLIT_0_0_12`, `MARKET_SUBSIDY_1_4`, `MARKET_SUBSIDY_5_9`, `MARKET_SUBSIDY_10`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "skus": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Set rates](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness)
Next
[Store Quality Index](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/ratings/getQualityRatings)
