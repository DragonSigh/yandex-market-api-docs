---
title: Enabling a sales boost and setting bids - Sales Boost | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/putBidsForBusiness
crawled_at: 2025-09-17T14:40:43.679348
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body)
    * [SkuBidItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#skubiditemdto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body1)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body7)


# Enabling a sales boost and setting bids
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/overview/business).**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/_auto/scopes_summary/pages/pricing)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/_auto/scopes_summary/pages/promotion)
  * all-methods — Full account management


Launches a sales boost — creates and activates a campaign, adds products to it and assigns bids on them.
What does a campaign created via the API look like in the dashboard?
![](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/api-boost.png)
When using the query for the first time, Market: creates a single campaign for all business account stores, adds products with the specified rates to it, includes a pricing strategy for them, and launches promotion. Reusing the query will allow you to update the bids for the products in this campaign or add new ones. Read more about the pricing strategy in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/marketing/campaigns.html#price-strategy).
If there is no product with the specified SKU, it will be ignored. If an item with this SKU appears in the catalog in the future, it will automatically be added to the campaign with the specified bid.
The request always works with the same campaign created via the API. If you delete it in your account, the Market will create a new one the next time you make a request. You will not be able to manage other campaigns via the API. A campaign created through the API always has the highest priority over the others — it cannot be changed.
Query execution includes the campaign and pricing strategy, if they have been disabled.
You can make other changes to the campaign created via the API in the dashboard:
  * disable or enable the campaign.
  * change its name;
  * disable or enable the pricing strategy.


To stop the promotion of individual products and remove them from the campaign, pass a zero bid for them in the parameter `bid`.
Read more about how the sales boost works in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/marketing/campaigns.html).
You can find out the cost of a sales boost by making a request [POST v2/campaigns/{campaignId}/stats/orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/stats/getOrdersStats). The amount is contained in the field `bidFee`.
The data is not updated instantly
It takes up to a few minutes.
**, Limit:** 1,000 requests per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#request)Request
PUT
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/bids

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body)Body
application/json
```
{
    "bids": [
        {
            "sku": "string",
            "bid": 570
        }
    ]
}

```

**Name** |  **Description**  
---|---  
bids* |  **Type:** [SkuBidItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#skubiditemdto)[] A list of products and the bids to be placed on them for promotion.  
A list of products and bids for them. _Min items:_ `1` _Max items:_ `1500`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#skubiditemdto)SkuBidItemDTO
A list of products and bids for them.
**Name** |  **Description**  
---|---  
bid* |  **Type:** integer<int32> The bid value for the product from the parameter `sku`, from 50 to 9999. It is indicated as a percentage of the cost of the product and multiplied by 100. For example, the 5% rate is indicated as 500. _Example:_ `570` _Min value:_ `0` _Max value:_ `9999`  
sku* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#200-ok)200 OK
Everything worked out: the bids were set or updated. If necessary, new products have been added and a campaign has been launched.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body1)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "bids": [ { "sku": "string", "bid": 570 } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Deleting a comment](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/goods-feedback/deleteGoodsFeedbackComment)
Next
[Set rates](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness)
