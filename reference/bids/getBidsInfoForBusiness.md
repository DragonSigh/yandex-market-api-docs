---
title: Set rates - Sales Boost | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/getBidsInfoForBusiness
crawled_at: 2025-09-17T14:40:49.961906
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body1)
    * [GetBidsInfoResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#getbidsinforesponsedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype)
    * [SkuBidItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#skubiditemdto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#forwardscrollingpagerdto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body7)


# Information about the set rates
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


Returns the bid values for the specified products.
You will not be able to get information on campaigns created in the cabinet.
The response returns only the values of the rates that you set through the request. [PUT v2/businesses/{businessId}/bids](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness).
A single request can contain a maximum of 1,500 products.
**, Limit:** 1,000 requests per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/bids/info

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body)Body
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
skus |  **Type:** string[] A list of products for which you need to get bid values. If the list is not specified, all products with bids are returned page by page. If a list is specified, the results are returned in one page, and the parameters are `page_token` and `limit` they are ignored.   
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `1500` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#200-ok)200 OK
Bid values for the specified products. The response includes only products for which bids are set.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "bids": [
            {
                "sku": "string",
                "bid": 570
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
result |  **Type:** [GetBidsInfoResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#getbidsinforesponsedto) A list of products with the specified bids.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#getbidsinforesponsedto)GetBidsInfoResponseDTO
A list of products with the specified bids.
**Name** |  **Description**  
---|---  
bids* |  **Type:** [SkuBidItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#skubiditemdto)[] The product list page.  
A list of products and bids for them.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#skubiditemdto)SkuBidItemDTO
A list of products and bids for them.
**Name** |  **Description**  
---|---  
bid* |  **Type:** integer<int32> The bid value for the product from the parameter `sku`, from 50 to 9999. It is indicated as a percentage of the cost of the product and multiplied by 100. For example, the 5% rate is indicated as 500. _Example:_ `570` _Min value:_ `0` _Max value:_ `9999`  
sku* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsInfoForBusiness#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
page_token:
limit:
Body{ "skus": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Enabling a sales boost and setting bids](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/putBidsForBusiness)
Next
[Recommended rates](https://yandex.ru/dev/market/partner-api/doc/en/reference/bids/en/reference/bids/getBidsRecommendations)
