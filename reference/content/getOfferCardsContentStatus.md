---
title: Information about card occupancy - Product cards | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/content/getOfferCardsContentStatus
crawled_at: 2025-09-17T14:37:39.772189
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body)
    * [OfferCardStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardstatustype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body1)
    * [OfferCardsContentStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardscontentstatusdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype)
    * [OfferCardDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercarddto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#forwardscrollingpagerdto)
    * [OfferCardContentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardcontentstatustype)
    * [OfferErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offererrordto)
    * [GetMappingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#getmappingdto)
    * [ParameterValueDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#parametervaluedto)
    * [OfferCardRecommendationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardrecommendationdto)
    * [OfferCardRecommendationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardrecommendationtype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body7)


# Getting information about the fullness of store cards
Info
Console
**The method is available for models:[FBY, FBS, Express and DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about the content status for the specified products:
  * whether a product card has been created and what is its status.
  * The rating of the card is how many percent it is filled.
  * transmitted product characteristics;
  * are there any errors or warnings related to the content;
  * recommendations for filling out the card.

**, Limit:** 600 requests per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/offer-cards

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body)Body
application/json
```
{
    "offerIds": [
        "string"
    ],
    "cardStatuses": [
        "HAS_CARD_CAN_NOT_UPDATE"
    ],
    "categoryIds": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
cardStatuses |  **Type:** [OfferCardStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardstatustype)[] Filter by card status. [What is a product card?](https://yandex.ru/support/marketplace/assortment/content/index.html)   
Product card status:
  * `HAS_CARD_CAN_NOT_UPDATE` — The Market card.
  * `HAS_CARD_CAN_UPDATE` — It can be supplemented.
  * `HAS_CARD_CAN_UPDATE_ERRORS` — The changes have not been accepted.
  * `HAS_CARD_CAN_UPDATE_PROCESSING` — Changes are under review.
  * `NO_CARD_NEED_CONTENT` — Create a card.
  * `NO_CARD_MARKET_WILL_CREATE` — Creates a Marketplace.
  * `NO_CARD_ERRORS` — It wasn't created because of a mistake.
  * `NO_CARD_PROCESSING` — We check the data.
  * `NO_CARD_ADD_TO_CAMPAIGN` — Place the product in the store.

_Enum:_ `HAS_CARD_CAN_NOT_UPDATE`, `HAS_CARD_CAN_UPDATE`, `HAS_CARD_CAN_UPDATE_ERRORS`, `HAS_CARD_CAN_UPDATE_PROCESSING`, `NO_CARD_NEED_CONTENT`, `NO_CARD_MARKET_WILL_CREATE`, `NO_CARD_ERRORS`, `NO_CARD_PROCESSING`, `NO_CARD_ADD_TO_CAMPAIGN` _Min items:_ `1` _Unique items_  
categoryIds |  **Type:** integer<int32>[] Filter by category on the Market.  
The ID of the category on the Market. When changing the category, make sure that the product characteristics and their values in the parameter `parameterValues` you are submitting for a new category. You can get a list of Market categories using a request. [POST v2/categories/tree](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/categories/getCategoriesTree). _Min value (exclusive):_ `0` _Min items:_ `1` _Max items:_ `200` _Unique items_  
offerIds |  **Type:** string[] The IDs of the products that information is needed about.   
  
Do not use this field at the same time as filters based on card statuses, categories, brands, or tags. If you want to use filters, leave the field empty.   
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `200` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardstatustype)OfferCardStatusType
Product card status:
  * `HAS_CARD_CAN_NOT_UPDATE` — The Market card.
  * `HAS_CARD_CAN_UPDATE` — It can be supplemented.
  * `HAS_CARD_CAN_UPDATE_ERRORS` — The changes have not been accepted.
  * `HAS_CARD_CAN_UPDATE_PROCESSING` — Changes are under review.
  * `NO_CARD_NEED_CONTENT` — Create a card.
  * `NO_CARD_MARKET_WILL_CREATE` — Creates a Marketplace.
  * `NO_CARD_ERRORS` — It wasn't created because of a mistake.
  * `NO_CARD_PROCESSING` — We check the data.
  * `NO_CARD_ADD_TO_CAMPAIGN` — Place the product in the store.

**Type** |  **Description**  
---|---  
[OfferCardStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardstatustype) |  _Enum:_ `HAS_CARD_CAN_NOT_UPDATE`, `HAS_CARD_CAN_UPDATE`, `HAS_CARD_CAN_UPDATE_ERRORS`, `HAS_CARD_CAN_UPDATE_PROCESSING`, `NO_CARD_NEED_CONTENT`, `NO_CARD_MARKET_WILL_CREATE`, `NO_CARD_ERRORS`, `NO_CARD_PROCESSING`, `NO_CARD_ADD_TO_CAMPAIGN`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#200-ok)200 OK
Information about the cards of the specified products.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "offerCards": [
            {
                "offerId": "string",
                "mapping": {
                    "marketSku": 0,
                    "marketSkuName": "string",
                    "marketModelId": 0,
                    "marketModelName": "string",
                    "marketCategoryId": 0,
                    "marketCategoryName": "string"
                },
                "parameterValues": [
                    {
                        "parameterId": 0,
                        "unitId": 0,
                        "valueId": 0,
                        "value": "string"
                    }
                ],
                "cardStatus": "HAS_CARD_CAN_NOT_UPDATE",
                "contentRating": 0,
                "averageContentRating": 0,
                "contentRatingStatus": "UPDATING",
                "recommendations": [
                    {
                        "type": "HAS_VIDEO",
                        "percent": 0,
                        "remainingRatingPoints": 0
                    }
                ],
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
        ],
        "paging": {
            "nextPageToken": "string"
        }
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OfferCardsContentStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardscontentstatusdto) A list of products with information about the status of the cards.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardscontentstatusdto)OfferCardsContentStatusDTO
A list of products with information about the status of the cards.
**Name** |  **Description**  
---|---  
offerCards* |  **Type:** [OfferCardDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercarddto)[] The product list page with information about the status of the cards.  
Information about the status of the product card. If the field `mapping` missing in the response, the Market has not yet managed to process the product information. To determine the category of such an item, repeat the request in a few minutes.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercarddto)OfferCardDTO
Information about the status of the product card.
If the field `mapping` missing in the response, the Market has not yet managed to process the product information. To determine the category of such an item, repeat the request in a few minutes.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
averageContentRating |  **Type:** integer<int32> The average rating of the card for products of the category indicated in `marketCategoryId`.  
cardStatus |  **Type:** [OfferCardStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardstatustype) Product card status:
  * `HAS_CARD_CAN_NOT_UPDATE` — The Market card.
  * `HAS_CARD_CAN_UPDATE` — It can be supplemented.
  * `HAS_CARD_CAN_UPDATE_ERRORS` — The changes have not been accepted.
  * `HAS_CARD_CAN_UPDATE_PROCESSING` — Changes are under review.
  * `NO_CARD_NEED_CONTENT` — Create a card.
  * `NO_CARD_MARKET_WILL_CREATE` — Creates a Marketplace.
  * `NO_CARD_ERRORS` — It wasn't created because of a mistake.
  * `NO_CARD_PROCESSING` — We check the data.
  * `NO_CARD_ADD_TO_CAMPAIGN` — Place the product in the store.

_Enum:_ `HAS_CARD_CAN_NOT_UPDATE`, `HAS_CARD_CAN_UPDATE`, `HAS_CARD_CAN_UPDATE_ERRORS`, `HAS_CARD_CAN_UPDATE_PROCESSING`, `NO_CARD_NEED_CONTENT`, `NO_CARD_MARKET_WILL_CREATE`, `NO_CARD_ERRORS`, `NO_CARD_PROCESSING`, `NO_CARD_ADD_TO_CAMPAIGN`  
contentRating |  **Type:** integer<int32> The rating of the card.  
contentRatingStatus |  **Type:** [OfferCardContentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardcontentstatustype) The status of calculating the card's rating and recommendations. _Enum:_ `UPDATING`, `ACTUAL`  
errors |  **Type:** [OfferErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offererrordto)[] Errors in the content that prevent the product from being placed in the showcase.  
An error message related to the product placement. _Min items:_ `1`  
mapping |  **Type:** [GetMappingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#getmappingdto) Basic information about the product card.  
The ID of the card on the Market. Shows the current product link to the card. It may not be included in the response if the product is not linked to the card yet. Check the card's status or correct any errors.  
parameterValues |  **Type:** [ParameterValueDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#parametervaluedto)[] A list of characteristics with their values.   
The value of the characteristic. You can specify multiple values for the same characteristic, provided that:
  * Type of feature — `ENUM`.
  * In response to the request [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters) this characteristic has a field `multivalue` it matters `true`.

To do this, in `parameterValues` pass each value separately — multiple objects with parameters `parameterId`, `valueId` and `value`. Parameter `parameterId` it must be the same. _Min items:_ `1`  
recommendations |  **Type:** [OfferCardRecommendationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardrecommendationdto)[] A list of recommendations for filling out the card. Yandex.Market recommendations help you fill out the card so that it is easier for customers to find your product and decide to make a purchase.   
Recommendation for filling out the product card. _Min items:_ `1`  
warnings |  **Type:** [OfferErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offererrordto)[] Content-related warnings that do not prevent the product from being placed in the showcase.  
An error message related to the product placement. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardcontentstatustype)OfferCardContentStatusType
The status of calculating the rating of the product card and recommendations:
  * `UPDATING` — the rating is updated.
  * `ACTUAL` — the rating is current.

**Type** |  **Description**  
---|---  
[OfferCardContentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardcontentstatustype) |  _Enum:_ `UPDATING`, `ACTUAL`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offererrordto)OfferErrorDTO
An error message related to the product placement.
**Name** |  **Description**  
---|---  
comment |  **Type:** string Explanation.  
message |  **Type:** string The type of error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#getmappingdto)GetMappingDTO
Information about the products in the catalog.
**Name** |  **Description**  
---|---  
marketCategoryId |  **Type:** integer<int64> ID of the category on the Market that the product belongs to. It may be missing from the response if the Market has not yet determined the product category.  
marketCategoryName |  **Type:** string The name of the card's category on the Market. It may be missing from the response if the Market has not yet determined the product category.  
marketModelId ⦸ |  **Type:** integer<int64> The ID of the model on the Market. It may not be included in the response if the product is not linked to the card yet.  
marketModelName ⦸ |  **Type:** string The name of the model on the Market. It may not be included in the response if the product is not linked to the card yet.  
marketSku |  **Type:** integer<int64> The ID of the card on the Market. _Min value:_ `1`  
marketSkuName |  **Type:** string The name of the product card. It may not be included in the response if the product is not linked to the card yet.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#parametervaluedto)ParameterValueDTO
The value of the characteristic.
You can specify multiple values for the same characteristic, provided that:
  * Type of feature — `ENUM`.
  * In response to the request [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters) this characteristic has a field `multivalue` it matters `true`.


To do this, in `parameterValues` pass each value separately — multiple objects with parameters `parameterId`, `valueId` and `value`. Parameter `parameterId` it must be the same.
**Name** |  **Description**  
---|---  
parameterId* |  **Type:** integer<int64> The identifier of the characteristic. _Min value:_ `1`  
unitId |  **Type:** integer<int64> ID of the unit of measurement. If you did not pass the parameter `unitId`, the default unit of measurement is used.  
value |  **Type:** string Meaning. For type characteristics `ENUM` transmit along with `valueId`.  
valueId |  **Type:** integer<int64> ID of the value. Be sure to specify the identifier if you are transmitting a value from the list of acceptable values received from the Market. Transmit along with `value`. Only for type characteristics `ENUM`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardrecommendationdto)OfferCardRecommendationDTO
Recommendation for filling out the product card.
**Name** |  **Description**  
---|---  
type* |  **Type:** [OfferCardRecommendationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardrecommendationtype) A recommendation for adding or replacing content. It is not refunded for cards that are filled with the Market or contain used goods. Some of the recommendations relate to **the main parameters** , which are available for products of any category. Others belong to those **characteristics** which the product has because it belongs to a certain category. **1. Recommendations related to the main parameters** Each such recommendation applies to **the only parameter**. To fill in this parameter, use the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/business-assortment/updateOfferMappings). Recommendations for filling in the parameters in `updateOfferMappings`:
  * `RECOGNIZED_VENDOR` — write the manufacturer's name as the manufacturer himself writes it (parameter `vendor`).
  * `PICTURE_COUNT` — add images (parameter `pictures`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/images) The percentage of its completion is sent for the recommendation.
  * `FIRST_PICTURE_SIZE`— replace the first image with a larger one (parameter `pictures`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/images)
  * `TITLE_LENGTH` — change the name (parameter `name`). Make a name according to the scheme: type + brand or manufacturer + model + features, if any (size, weight, color). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/title)
  * `DESCRIPTION_LENGTH` — add a description of the recommended size (parameter `description`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/description)
  * `AVERAGE_PICTURE_SIZE` — replace all images with high-quality images (parameter `pictures`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/images)
  * `FIRST_VIDEO_LENGTH` — add the first video of the recommended length (parameter `videos`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/video)
  * `FIRST_VIDEO_SIZE` — replace the first video with a high-quality video (parameter `videos`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/video)
  * `AVERAGE_VIDEO_SIZE` — replace all videos with high-quality videos (parameter `videos`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/video)
  * `VIDEO_COUNT` — add at least one video (parameter `videos`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/video) The percentage of its completion is sent for the recommendation.

**2. Recommendations related to characteristics by category** Each such recommendation involves filling out **one or more characteristics**. To find out exactly which characteristics you need to fill out, use the request [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters). For example, if you have received a recommendation `MAIN`, you need to fill in the characteristics that have `MAIN` in the array `recommendationTypes`. Recommendations:
  * `MAIN` — fill in the key product characteristics that are used in the search and filters. The percentage of its completion is sent for the recommendation.
  * `ADDITIONAL` — fill in additional product specifications. The percentage of its completion is sent for the recommendation.
  * `DISTINCTIVE` — fill in the characteristics that distinguish the product options from each other. The percentage of its completion is sent for the recommendation.

**3. Outdated recommendations**
  * `HAS_VIDEO`.
  * `FILTERABLE`.
  * `HAS_DESCRIPTION`.
  * `HAS_BARCODE`.

_Enum:_ `HAS_VIDEO`, `RECOGNIZED_VENDOR`, `MAIN`, `ADDITIONAL`, `DISTINCTIVE`, `FILTERABLE`, `PICTURE_COUNT`, `HAS_DESCRIPTION`, `HAS_BARCODE`, `FIRST_PICTURE_SIZE`, `TITLE_LENGTH`, `DESCRIPTION_LENGTH`, `AVERAGE_PICTURE_SIZE`, `FIRST_VIDEO_SIZE`, `FIRST_VIDEO_LENGTH`, `AVERAGE_VIDEO_SIZE`, `VIDEO_COUNT`  
percent |  **Type:** integer<int32> Percentage of implementation of the recommendation. Specified for certain types of recommendations:
  * `PICTURE_COUNT`.
  * `VIDEO_COUNT`.
  * `MAIN`.
  * `ADDITIONAL`.
  * `DISTINCTIVE`.

_Min value:_ `0` _Max value (exclusive):_ `100`  
remainingRatingPoints |  **Type:** integer<int32> The maximum number of card rating points that can be obtained for following recommendations. _Min value:_ `1` _Max value:_ `100`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardrecommendationtype)OfferCardRecommendationType
A recommendation for adding or replacing content. It is not refunded for cards that are filled with the Market or contain used goods.
Some of the recommendations relate to **the main parameters** , which are available for products of any category. Others belong to those **characteristics** which the product has because it belongs to a certain category.
**1. Recommendations related to the main parameters**
Each such recommendation applies to **the only parameter**. To fill in this parameter, use the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/business-assortment/updateOfferMappings).
Recommendations for filling in the parameters in `updateOfferMappings`:
  * `RECOGNIZED_VENDOR` — write the manufacturer's name as the manufacturer himself writes it (parameter `vendor`).
  * `PICTURE_COUNT` — add images (parameter `pictures`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/images)
The percentage of its completion is sent for the recommendation.
  * `FIRST_PICTURE_SIZE`— replace the first image with a larger one (parameter `pictures`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/images)
  * `TITLE_LENGTH` — change the name (parameter `name`). Make a name according to the scheme: type + brand or manufacturer + model + features, if any (size, weight, color). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/title)
  * `DESCRIPTION_LENGTH` — add a description of the recommended size (parameter `description`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/description)
  * `AVERAGE_PICTURE_SIZE` — replace all images with high-quality images (parameter `pictures`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/images)
  * `FIRST_VIDEO_LENGTH` — add the first video of the recommended length (parameter `videos`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/video)
  * `FIRST_VIDEO_SIZE` — replace the first video with a high-quality video (parameter `videos`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/video)
  * `AVERAGE_VIDEO_SIZE` — replace all videos with high-quality videos (parameter `videos`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/video)
  * `VIDEO_COUNT` — add at least one video (parameter `videos`). [Requirements](https://yandex.ru/support2/marketplace/ru/assortment/fields/video)
The percentage of its completion is sent for the recommendation.


**2. Recommendations related to characteristics by category**
Each such recommendation involves filling out **one or more characteristics**. To find out exactly which characteristics you need to fill out, use the request [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters). For example, if you have received a recommendation `MAIN`, you need to fill in the characteristics that have `MAIN` in the array `recommendationTypes`.
Recommendations:
  * `MAIN` — fill in the key product characteristics that are used in the search and filters.
The percentage of its completion is sent for the recommendation.
  * `ADDITIONAL` — fill in additional product specifications.
The percentage of its completion is sent for the recommendation.
  * `DISTINCTIVE` — fill in the characteristics that distinguish the product options from each other.
The percentage of its completion is sent for the recommendation.


**3. Outdated recommendations**
  * `HAS_VIDEO`.
  * `FILTERABLE`.
  * `HAS_DESCRIPTION`.
  * `HAS_BARCODE`.

**Type** |  **Description**  
---|---  
[OfferCardRecommendationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#offercardrecommendationtype) |  _Enum:_ `HAS_VIDEO`, `RECOGNIZED_VENDOR`, `MAIN`, `ADDITIONAL`, `DISTINCTIVE`, `FILTERABLE`, `PICTURE_COUNT`, `HAS_DESCRIPTION`, `HAS_BARCODE`, `FIRST_PICTURE_SIZE`, `TITLE_LENGTH`, `DESCRIPTION_LENGTH`, `AVERAGE_PICTURE_SIZE`, `FIRST_VIDEO_SIZE`, `FIRST_VIDEO_LENGTH`, `AVERAGE_VIDEO_SIZE`, `VIDEO_COUNT`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
page_token:
limit:
Body{ "offerIds": [ "string" ], "cardStatuses": [ "HAS_CARD_CAN_NOT_UPDATE" ], "categoryIds": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Changing the terms of sale](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/assortment/updateCampaignOffers)
Next
[Editing product category characteristics](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent)
