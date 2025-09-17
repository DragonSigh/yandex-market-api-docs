---
title: Adding products to a promotion/changing their prices - Stocks | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/updatePromoOffers
crawled_at: 2025-09-17T14:38:32.406787
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body)
    * [UpdatePromoOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferdto)
    * [UpdatePromoOfferParamsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferparamsdto)
    * [UpdatePromoOfferDiscountParamsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferdiscountparamsdto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body1)
    * [UpdatePromoOffersResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromooffersresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype)
    * [RejectedPromoOfferUpdateDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#rejectedpromoofferupdatedto)
    * [WarningPromoOfferUpdateDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#warningpromoofferupdatedto)
    * [RejectedPromoOfferUpdateReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#rejectedpromoofferupdatereasontype)
    * [PromoOfferUpdateWarningDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#promoofferupdatewarningdto)
    * [PromoOfferUpdateWarningCodeType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#promoofferupdatewarningcodetype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body7)


# Adding products to a promotion or changing their prices
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/overview/business).**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/_auto/scopes_summary/pages/pricing)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/_auto/scopes_summary/pages/promotion)
  * all-methods — Full account management


Adds products to the promotion or changes the prices of the products that participate in the promotion.
The changes begin to take effect within 4-6 hours.
**, Limit:** 10,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/promos/offers/update

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body)Body
application/json
```
{
    "promoId": "string",
    "offers": [
        {
            "offerId": "string",
            "params": {
                "discountParams": {
                    "price": 0,
                    "promoPrice": 0
                }
            }
        }
    ]
}

```

**Name** |  **Description**  
---|---  
offers* |  **Type:** [UpdatePromoOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferdto)[] Products that need to be added to the promotion or whose prices need to be changed.  
Description of the products that participate in the promotion. _Min items:_ `1` _Max items:_ `500`  
promoId* |  **Type:** string The ID of the promotion.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferdto)UpdatePromoOfferDTO
Description of the products that participate in the promotion.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
params |  **Type:** [UpdatePromoOfferParamsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferparamsdto) The parameters of the product that participates in the promotion.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferparamsdto)UpdatePromoOfferParamsDTO
The parameters of the product that participates in the promotion.
**Name** |  **Description**  
---|---  
discountParams |  **Type:** [UpdatePromoOfferDiscountParamsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferdiscountparamsdto) Product parameters in the promotion with the type `DIRECT_DISCOUNT` or `BLUE_FLASH`. A required parameter for stocks with these types.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromoofferdiscountparamsdto)UpdatePromoOfferDiscountParamsDTO
Product parameters in the promotion with the type `DIRECT_DISCOUNT` or `BLUE_FLASH`.
A required parameter for stocks with these types.
**Name** |  **Description**  
---|---  
price |  **Type:** integer<int64> The crossed—out price is the one at which the product was sold before the promotion. Indicated in rubles. The number must be an integer. _Min value:_ `1`  
promoPrice |  **Type:** integer<int64> The share price is the one at which you want to sell the product. Indicated in rubles. The number must be an integer. _Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#200-ok)200 OK
The result of adding products to the promotion or updating their prices.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body1)Body
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
        ],
        "warningOffers": [
            {
                "offerId": "string",
                "warnings": [
                    {
                        "code": "DEEP_DISCOUNT_OFFER",
                        "campaignIds": [
                            0
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
result |  **Type:** [UpdatePromoOffersResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromooffersresultdto) Errors and warnings that appeared when adding products to the promotion.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#updatepromooffersresultdto)UpdatePromoOffersResultDTO
Errors and warnings that appeared when adding products to the promotion.
**Name** |  **Description**  
---|---  
rejectedOffers |  **Type:** [RejectedPromoOfferUpdateDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#rejectedpromoofferupdatedto)[] Changes that were rejected. It is returned only if there are rejected changes.   
Description of the rejected change. _Min items:_ `1`  
warningOffers |  **Type:** [WarningPromoOfferUpdateDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#warningpromoofferupdatedto)[] Changes that have warnings. They inform you about possible problems. The product information will be updated. It is returned only if there are warnings.   
Description of the warning that appeared when adding the product. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#rejectedpromoofferupdatedto)RejectedPromoOfferUpdateDTO
Description of the rejected change.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
reason* |  **Type:** [RejectedPromoOfferUpdateReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#rejectedpromoofferupdatereasontype) The reason for rejecting the change:
  * `OFFER_DOES_NOT_EXIST` — there is no product with such a SKU in the cabinet.
  * `OFFER_DUPLICATION` — the same product has been transferred several times.
  * `OFFER_NOT_ELIGIBLE_FOR_PROMO` — the product does not meet the terms of the promotion.
  * `OFFER_PROMOS_MAX_BYTE_SIZE_EXCEEDED` — the product was not added to the promotion due to technical reasons.
  * `DEADLINE_FOR_FOCUS_PROMOS_EXCEEDED` — the deadline for adding products to the promotion has expired.
  * `EMPTY_OLD_PRICE` — the crossed-out price is not indicated.
  * `EMPTY_PROMO_PRICE` — the share price is not specified.
  * `MAX_PROMO_PRICE_EXCEEDED` — the share price exceeds the maximum possible price for participation in the promotion.
  * `PROMO_PRICE_BIGGER_THAN_MAX` — the share price is more than 95% of the crossed-out price.
  * `PROMO_PRICE_SMALLER_THAN_MIN` — the share price is less than 1% of the crossed-out price.

_Enum:_ `OFFER_DOES_NOT_EXIST`, `OFFER_DUPLICATION`, `OFFER_NOT_ELIGIBLE_FOR_PROMO`, `OFFER_PROMOS_MAX_BYTE_SIZE_EXCEEDED`, `DEADLINE_FOR_FOCUS_PROMOS_EXCEEDED`, `EMPTY_OLD_PRICE`, `EMPTY_PROMO_PRICE`, `MAX_PROMO_PRICE_EXCEEDED`, `PROMO_PRICE_BIGGER_THAN_MAX`, `PROMO_PRICE_SMALLER_THAN_MIN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#warningpromoofferupdatedto)WarningPromoOfferUpdateDTO
Description of the warning that appeared when adding the product.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
warnings* |  **Type:** [PromoOfferUpdateWarningDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#promoofferupdatewarningdto)[] Warnings that appear when adding an item to a promotion or changing its prices.  
A warning that appeared when adding an item to the promotion or changing its prices.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#rejectedpromoofferupdatereasontype)RejectedPromoOfferUpdateReasonType
The reason for rejecting the change:
  * `OFFER_DOES_NOT_EXIST` — there is no product with such a SKU in the cabinet.
  * `OFFER_DUPLICATION` — the same product has been transferred several times.
  * `OFFER_NOT_ELIGIBLE_FOR_PROMO` — the product does not meet the terms of the promotion.
  * `OFFER_PROMOS_MAX_BYTE_SIZE_EXCEEDED` — the product was not added to the promotion due to technical reasons.
  * `DEADLINE_FOR_FOCUS_PROMOS_EXCEEDED` — the deadline for adding products to the promotion has expired.
  * `EMPTY_OLD_PRICE` — the crossed-out price is not specified.
  * `EMPTY_PROMO_PRICE` — the share price is not specified.
  * `MAX_PROMO_PRICE_EXCEEDED` — the share price exceeds the maximum possible price for participation in the promotion.
  * `PROMO_PRICE_BIGGER_THAN_MAX` — the share price is more than 95% of the crossed-out price.
  * `PROMO_PRICE_SMALLER_THAN_MIN` — the share price is less than 1% of the crossed-out price.

**Type** |  **Description**  
---|---  
[RejectedPromoOfferUpdateReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#rejectedpromoofferupdatereasontype) |  _Enum:_ `OFFER_DOES_NOT_EXIST`, `OFFER_DUPLICATION`, `OFFER_NOT_ELIGIBLE_FOR_PROMO`, `OFFER_PROMOS_MAX_BYTE_SIZE_EXCEEDED`, `DEADLINE_FOR_FOCUS_PROMOS_EXCEEDED`, `EMPTY_OLD_PRICE`, `EMPTY_PROMO_PRICE`, `MAX_PROMO_PRICE_EXCEEDED`, `PROMO_PRICE_BIGGER_THAN_MAX`, `PROMO_PRICE_SMALLER_THAN_MIN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#promoofferupdatewarningdto)PromoOfferUpdateWarningDTO
A warning that appeared when adding an item to the promotion or changing its prices.
**Name** |  **Description**  
---|---  
code* |  **Type:** [PromoOfferUpdateWarningCodeType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#promoofferupdatewarningcodetype) The warning that appeared when adding the product:
  * `DEEP_DISCOUNT_OFFER` — there is a big difference with the price in the catalog. Check if there is an error.
  * `CATALOG_PRICE_IS_LOWER_THAN_PROMO` — the price that is valid in all stores is lower than the price of the promotion. The product price will not be displayed for the promotion.
  * `SHOP_PRICES_ARE_LOWER_THAN_PROMO` — the price in a separate store is lower than the price of the promotion. The product in the promotion will display the price in the store. The promotion price will apply to all other stores.
  * `SHOP_OFFER_NOT_ELIGIBLE_FOR_PROMO` — the product in a separate store does not meet the terms of the promotion.

_Enum:_ `DEEP_DISCOUNT_OFFER`, `CATALOG_PRICE_IS_LOWER_THAN_PROMO`, `SHOP_PRICES_ARE_LOWER_THAN_PROMO`, `SHOP_OFFER_NOT_ELIGIBLE_FOR_PROMO`  
campaignIds |  **Type:** integer<int64>[] The campaign IDs of those stores for which warnings were received. It is not refunded if the warnings are valid for all stores in the cabinet.   
The campaign ID. _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#promoofferupdatewarningcodetype)PromoOfferUpdateWarningCodeType
The warning that appeared when adding the product:
  * `DEEP_DISCOUNT_OFFER` — there is a big difference with the price in the catalog. Check if there is an error.
  * `CATALOG_PRICE_IS_LOWER_THAN_PROMO` — the price that is valid in all stores is lower than the price of the promotion. The product price will not be displayed for the promotion.
  * `SHOP_PRICES_ARE_LOWER_THAN_PROMO` — the price in a separate store is lower than the price of the promotion. The product in the promotion will display the price in the store. The promotion price will apply to all other stores.
  * `SHOP_OFFER_NOT_ELIGIBLE_FOR_PROMO` — the product in a separate store does not meet the terms of the promotion.

**Type** |  **Description**  
---|---  
[PromoOfferUpdateWarningCodeType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#promoofferupdatewarningcodetype) |  _Enum:_ `DEEP_DISCOUNT_OFFER`, `CATALOG_PRICE_IS_LOWER_THAN_PROMO`, `SHOP_PRICES_ARE_LOWER_THAN_PROMO`, `SHOP_OFFER_NOT_ELIGIBLE_FOR_PROMO`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/updatePromoOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "promoId": "string", "offers": [ { "offerId": "string", "params": { "discountParams": { "price": 0, "promoPrice": 0 } } } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
The price that is valid in all stores.
### Was the article helpful?
YesNo
Previous
[List of products in the promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromoOffers)
Next
[Removing products from the promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/deletePromoOffers)
