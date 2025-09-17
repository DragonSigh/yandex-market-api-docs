---
title: Removing products from the promotion - Stocks | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/deletePromoOffers
crawled_at: 2025-09-17T14:38:38.082204
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body1)
    * [DeletePromoOffersResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#deletepromooffersresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype)
    * [RejectedPromoOfferDeleteDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#rejectedpromoofferdeletedto)
    * [RejectedPromoOfferDeleteReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#rejectedpromoofferdeletereasontype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body7)


# Removing products from the promotion
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/overview/business).**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/_auto/scopes_summary/pages/pricing)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/_auto/scopes_summary/pages/promotion)
  * all-methods — Full account management


Removes products from the promotion.
The changes begin to take effect within 4-6 hours.
**, Limit:** 10,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/promos/offers/delete

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body)Body
application/json
```
{
    "promoId": "string",
    "deleteAllOffers": false,
    "offerIds": [
        "string"
    ]
}

```

**Name** |  **Description**  
---|---  
promoId* |  **Type:** string The ID of the promotion.  
deleteAllOffers |  **Type:** boolean To remove all products from the promotion and no longer participate in it, pass the value `true` and don't pass the parameter. `offerIds`.  
offerIds |  **Type:** string[] Products that need to be removed from the promotion.  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `500` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#200-ok)200 OK
The result of removing products from the promotion.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "rejectedOffers": [
            {
                "offerId": "string",
                "reason": "OFFER_DOES_NOT_EXIST"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [DeletePromoOffersResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#deletepromooffersresultdto) The result of removing products from the promotion. Returned only if the parameter was passed in the request. `offerIds`.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#deletepromooffersresultdto)DeletePromoOffersResultDTO
The result of removing products from the promotion.
Returned only if the parameter was passed in the request. `offerIds`.
**Name** |  **Description**  
---|---  
rejectedOffers |  **Type:** [RejectedPromoOfferDeleteDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#rejectedpromoofferdeletedto)[] Products that were deleted with errors. It is refunded only if there are such items.   
Information about the product and errors that appeared when it was deleted. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#rejectedpromoofferdeletedto)RejectedPromoOfferDeleteDTO
Information about the product and errors that appeared when it was deleted.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
reason* |  **Type:** [RejectedPromoOfferDeleteReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#rejectedpromoofferdeletereasontype) Error description:
  * `OFFER_DOES_NOT_EXIST` — there is no product with this SKU in the cabinet.

_Enum:_ `OFFER_DOES_NOT_EXIST`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#rejectedpromoofferdeletereasontype)RejectedPromoOfferDeleteReasonType
Error description:
  * `OFFER_DOES_NOT_EXIST` — there is no product with this SKU in the cabinet.

**Type** |  **Description**  
---|---  
[RejectedPromoOfferDeleteReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#rejectedpromoofferdeletereasontype) |  _Enum:_ `OFFER_DOES_NOT_EXIST`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "promoId": "string", "deleteAllOffers": false, "offerIds": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Adding products to a promotion/changing their prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers)
Next
[About one order](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/orders/getOrder)
