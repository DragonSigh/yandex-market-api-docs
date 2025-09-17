---
title: Adding and editing products - Products | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/updateOfferMappingEntries
crawled_at: 2025-09-17T14:43:32.215082
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body)
    * [UpdateOfferMappingEntryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#updateoffermappingentrydto)
    * [OfferMappingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offermappingdto)
    * [MappingsOfferInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#mappingsofferinfodto)
    * [OfferAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offeravailabilitystatustype)
    * [TimePeriodDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeperioddto)
    * [OfferProcessingStateDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingstatedto)
    * [DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#dayofweektype)
    * [OfferWeightDimensionsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerweightdimensionsdto)
    * [TimeUnitType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeunittype)
    * [OfferProcessingNoteDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingnotedto)
    * [OfferProcessingStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingstatustype)
    * [OfferProcessingNoteType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingnotetype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body1)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body6)
  * [423 Locked](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#423-locked)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body7)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body8)


# Adding and editing products in the catalog
Deprecated
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * all-methods — Full account management


Which method should I use instead of the outdated one?
[POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/business-assortment/updateOfferMappings)
Adds the products specified in the request to your product catalog and edits existing products.
Information about the products must be transmitted in the body of the POST request.
Each product must have your SKU, a unique code that you use to identify the product:
  * To add a new product to the catalog, specify in the parameter `shopSku` your SKU, which is not yet in the catalog.
  * To edit an item from the catalog, specify in the parameter `shopSku` your SKU of this product is in the catalog.


In both cases, you need to provide the full product description in the request, even if you only want to change a few characteristics.
If you know which product card on the Market corresponds to your product, specify its identifier (SKU on the Market) in the input parameter. `mapping`. You can get the SKU on the Market of the recommended product card through the account. If the SKU is not specified on the Market, the Market staff will select or create a suitable product card themselves, or it will have a status `NEED_CONTENT` (you need to find the card or create it yourself) in the request output [POST v2/businesses/{businessId}/offer-mappings](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/business-assortment/getOfferMappings).
The products are moderated before publication. If an error is found in one of the sent products, the response to the request will have the HTTP code 400 Bad Request, and none of the products will be sent for moderation. However, if you do not pass all the required parameters for any product, it will have the status after moderation. `NEED_INFO` (there is not enough information in the product description) in the request output [POST v2/businesses/{businessId}/offer-mappings](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/business-assortment/getOfferMappings).
You can add up to 500 products per request.
The data in the catalog is not updated instantly
It takes up to a few minutes.
**, Limit:** 5,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offer-mapping-entries/updates

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body)Body
application/json
```
{
    "offerMappingEntries": [
        {
            "offer": {
                "name": "Ударная дрель Makita HP1630, 710 Вт",
                "shopSku": "string",
                "category": "string",
                "vendor": "LEVENHUK",
                "vendorCode": "VNDR-0005A",
                "description": "string",
                "id": "string",
                "feedId": 0,
                "barcodes": [
                    46012300000000
                ],
                "urls": [
                    "string"
                ],
                "pictures": [
                    "string"
                ],
                "manufacturer": "string",
                "manufacturerCountries": [
                    "string"
                ],
                "minShipment": 0,
                "transportUnitSize": 0,
                "quantumOfSupply": 0,
                "deliveryDurationDays": 0,
                "boxCount": 0,
                "customsCommodityCodes": [
                    "string"
                ],
                "weightDimensions": {
                    "length": 65.55,
                    "width": 50.7,
                    "height": 20,
                    "weight": 1.001
                },
                "supplyScheduleDays": [
                    "MONDAY"
                ],
                "shelfLifeDays": 0,
                "lifeTimeDays": 0,
                "guaranteePeriodDays": 0,
                "processingState": {
                    "status": "UNKNOWN",
                    "notes": [
                        {
                            "type": "ASSORTMENT",
                            "payload": "string"
                        }
                    ]
                },
                "availability": "ACTIVE",
                "shelfLife": {
                    "timePeriod": 0,
                    "timeUnit": "HOUR",
                    "comment": "string"
                },
                "lifeTime": {
                    "timePeriod": 0,
                    "timeUnit": "HOUR",
                    "comment": "string"
                },
                "guaranteePeriod": {
                    "timePeriod": 0,
                    "timeUnit": "HOUR",
                    "comment": "string"
                },
                "certificate": "string"
            },
            "mapping": {
                "marketSku": 0,
                "modelId": 0,
                "categoryId": 0
            },
            "awaitingModerationMapping": {
                "marketSku": 0,
                "modelId": 0,
                "categoryId": 0
            },
            "rejectedMapping": {
                "marketSku": 0,
                "modelId": 0,
                "categoryId": 0
            }
        }
    ]
}

```

**Name** |  **Description**  
---|---  
offerMappingEntries* |  **Type:** [UpdateOfferMappingEntryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#updateoffermappingentrydto)[] Information about the products in the catalog.  
The list of products.   
Information about the product card. _Min items:_ `1` _Max items:_ `500`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#updateoffermappingentrydto)UpdateOfferMappingEntryDTO
The list of products.
**Name** |  **Description**  
---|---  
awaitingModerationMapping |  **Type:** [OfferMappingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offermappingdto) Information about the product profile on the Market that is undergoing moderation for this product  
mapping |  **Type:** [OfferMappingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offermappingdto) Information about the product card on the Market. If the parameter is not specified, the Market staff will select or create a suitable product card themselves, or it will have the status `NEED_CONTENT` (you need to find the card or create it yourself) in the request output [POST v2/businesses/{businessId}/offer-mappings](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/business-assortment/getOfferMappings).  
offer |  **Type:** [MappingsOfferInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#mappingsofferinfodto) Product information from the catalog.  
rejectedMapping |  **Type:** [OfferMappingDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offermappingdto) Information about the last product card on the Market that was rejected during moderation for this product  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offermappingdto)OfferMappingDTO
Information about the current product profile on the Market.
**Name** |  **Description**  
---|---  
categoryId |  **Type:** integer<int64> The category ID for the current product profile on the Market.  
marketSku |  **Type:** integer<int64> SKU on the Market is the identifier of the product card on the Market. At the first request `marketSku` binds the product to the Market card. In the future, you cannot change the SKU by sending a request. To do this, contact customer support. _Min value:_ `1`  
modelId |  **Type:** integer<int64> The model ID for the current product profile on the Market. For example, two blades of different colors have different SKUs on the Market (parameter `marketSku`), but the same product model ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#mappingsofferinfodto)MappingsOfferInfoDTO
Basic information about the products in the catalog.
**Name** |  **Description**  
---|---  
availability |  **Type:** [OfferAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offeravailabilitystatustype) Delivery plans:
  * `ACTIVE` — there will be supplies.
  * `INACTIVE` — there will be no deliveries: the product is in stock, but you no longer plan to deliver it. 60 days after the product runs out of stock, this status will change to `DELISTED`.
  * `DELISTED` — archive: the product has run out of stock, and there will be no more deliveries. If the product is returned to the warehouse (for example, the customer returns the order), this status will change to `INACTIVE`.

_Enum:_ `ACTIVE`, `INACTIVE`, `DELISTED`  
barcodes |  **Type:** string[] Specify it as a sequence of numbers. Suitable codes are EAN-13, EAN-8, UPC-A, UPC-E or Code 128. For books, specify the ISBN. For products  _What is GTIN?_   
_Example:_ `46012300000000` _Min items:_ `1` _Unique items_  
boxCount |  **Type:** integer<int32> How many seats (if more than one) the product occupies. The parameter is specified only if the product occupies more than one place (for example, the air conditioner occupies two places: an external and an internal unit in two boxes). If the product occupies one place, do not specify this parameter.  
category ⦸ |  **Type:** string Instead, use `marketCategoryId`. The product category in your store.  
certificate |  **Type:** string The document number for the product. Before specifying the number, the document must be uploaded to the seller's account on the Market. [Instruction manual](https://yandex.ru/support/marketplace/assortment/restrictions/certificates.html)  
customsCommodityCodes |  **Type:** string[] The list of product codes in the unified Commodity nomenclature of foreign economic activity (HS). A mandatory parameter if the product is subject to special accounting (for example, in the Mercury system as products of animal origin or in the Honest SIGN system). It can contain only one nested HS code.   
_Min items:_ `1` _Unique items_  
deliveryDurationDays |  **Type:** integer<int32> The period for which the seller delivers the goods to the warehouse, in days.  
description |  **Type:** string Detailed product description: for example, its advantages and features. Do not provide installation and assembly instructions in the description. Do not use the words "discount", "sale", "cheap", "gift" (except gift categories), "free", "special offer", "special price", "novelty", "new", "analog", "order", "hit". Do not provide any contact information or links. You can use HTML tags to format the text:
  * <h>, <h1>, <h2> and so on — for headings;
  * <br> and <p> — for line breaks.
  * <ol> — for a numbered list.
  * <ul> — for a bulleted list.
  * <li> — to create list items (must be inside <ol> or <ul>);
  * <div> — supported, but does not affect the text display.

The optimal length is 400-600 characters. [Recommendations and rules](https://yandex.ru/support/marketplace/assortment/fields/description.html) _Max length:_ `6000`  
feedId |  **Type:** integer<int64> The feed ID.  
guaranteePeriod |  **Type:** [TimePeriodDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeperioddto) Information about the warranty period: during which period (in years, months, days, weeks, or hours) maintenance and repair of the product or a refund are possible, and the manufacturer or seller will be responsible for the defects of the product. A required parameter if the product has a warranty period. The product has a warranty period, but you won't specify it. The product will be hidden from the Market.  
guaranteePeriodDays |  **Type:** integer<int32> Product warranty period: how many days is it possible to service and repair the product or refund money, and the manufacturer or seller will be responsible for the defects of the product.  
id |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
lifeTime |  **Type:** [TimePeriodDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeperioddto) Service life information: for what period (in years, months, days, weeks, or hours) The product will perform its function properly, and the manufacturer will be responsible for its significant shortcomings. A required parameter if the product has a service life. The product has a service life, but you don't specify it. The product will be hidden from the Market.  
lifeTimeDays ⦸ |  **Type:** integer<int32> Instead, use `lifeTime`. Using both parameters together will result in an error. Service life: how many days the product will properly perform its function, and the manufacturer will be responsible for its significant shortcomings.  
manufacturer |  **Type:** string Product manufacturer: the company that produced the product, its address and registration number (if any). Optional parameter.  
manufacturerCountries |  **Type:** string[] A list of countries where the product is manufactured. Required parameter. It must contain at least one, but not more than 5 countries.   
_Min items:_ `1` _Max items:_ `5` _Unique items_  
minShipment |  **Type:** integer<int32> The minimum number of items that you deliver to the warehouse. For example, if you supply baby food in batches of at least 10 boxes, and each box contains 6 jars, specify the value 60.  
name |  **Type:** string Make up the name according to the scheme: type + brand or manufacturer + model + features, if any (for example, color, size or weight) and quantity in the package. Do not include emotional characteristics ("hit", "super", etc.) in the name of the terms of sale (for example, "discount", "free shipping", etc.). Do not write words in capital letters, except for the established names of brands and models. The optimal length is 50-60 characters. [Recommendations and rules](https://yandex.ru/support/marketplace/assortment/fields/title.html) _Example:_ `Impact drill Makita HP1630, 710 W` _Max length:_ `256`  
pictures |  **Type:** string[] Links (URLs) of product images in good quality. You can specify up to 30 links. In this case, the image on the first link will be the main one. It is used as a product image in the Market search and on the product card. Other product images are available in the enlarged image view.   
_Min length:_ `1` _Max length:_ `2000` _Min items:_ `1` _Max items:_ `30` _Unique items_ `false`  
processingState |  **Type:** [OfferProcessingStateDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingstatedto) Information about the publication status of the product on the Market.  
quantumOfSupply ⦸ |  **Type:** integer<int32> Additional batch: how many items can be added to the minimum quantity `minShipment`. For example, if you supply baby food in batches of at least 10 boxes and want to add 2 boxes to the minimum batch, with 6 jars in each box, specify the value 12.  
shelfLife |  **Type:** [TimePeriodDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeperioddto) Expiration date information: after what time (in years, months, days, weeks, or hours) the product will become unusable. For example, categories such as food and medicines have expiration dates. A required parameter if the product has an expiration date. The product has an expiration date, but you don't specify it. The product will be hidden from the Market.  
shelfLifeDays ⦸ |  **Type:** integer<int32> Instead, use `shelfLife`. Using both parameters together will result in an error. Expiration date: after how many days the product will become unusable.  
shopSku |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
supplyScheduleDays |  **Type:** [DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#dayofweektype)[] The days of the week on which the seller delivers the goods to the warehouse.  
Day of the week:
  * `MONDAY` — Monday.
  * `TUESDAY` "Tuesday."
  * `WEDNESDAY` — Wednesday.
  * `THURSDAY` — Thursday.
  * `FRIDAY` — It's Friday.
  * `SATURDAY` "Saturday."
  * `SUNDAY` — Sunday.

_Enum:_ `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY` _Min items:_ `1` _Unique items_  
transportUnitSize |  **Type:** integer<int32> The number of items in one package that you deliver to the warehouse. For example, if you supply baby food in boxes of 6 cans, specify the value 6.  
urls |  **Type:** string[] The URL of the product photo or description page on your website. The transmitted data will not be displayed on the showcase, but it will help the Market specialists find a card for your product. Must contain one nested parameter. `url`.   
_Min length:_ `1` _Max length:_ `2000` _Min items:_ `1` _Unique items_  
vendor |  **Type:** string The name of the brand or manufacturer. It should be written the way the brand itself writes it. _Example:_ `LEVENHUK`  
vendorCode |  **Type:** string The article of the product from the manufacturer. _Example:_ `VNDR-0005A`  
weightDimensions |  **Type:** [OfferWeightDimensionsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerweightdimensionsdto) The dimensions of the package and the weight of the product.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offeravailabilitystatustype)OfferAvailabilityStatusType
Delivery plans:
  * `ACTIVE` — there will be supplies.
  * `INACTIVE` — there will be no deliveries: the product is in stock, but you no longer plan to deliver it. 60 days after the product runs out of stock, this status will change to `DELISTED`.
  * `DELISTED` — archive: the product has run out of stock, and there will be no more deliveries. If the product is returned to the warehouse (for example, the customer returns the order), this status will change to `INACTIVE`.

**Type** |  **Description**  
---|---  
[OfferAvailabilityStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offeravailabilitystatustype) |  _Enum:_ `ACTIVE`, `INACTIVE`, `DELISTED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeperioddto)TimePeriodDTO
A time period with a comment. The requirements for the comment content depend on the context of the parameter usage and are specified in the description of the field that contains it.
**Name** |  **Description**  
---|---  
timePeriod* |  **Type:** integer Duration in the specified units.  
timeUnit* |  **Type:** [TimeUnitType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeunittype) Unit of measurement. _Enum:_ `HOUR`, `DAY`, `WEEK`, `MONTH`, `YEAR`  
comment |  **Type:** string Comment. _Max length:_ `500`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingstatedto)OfferProcessingStateDTO
Information about the publication status of the product on the Market.
**Name** |  **Description**  
---|---  
notes |  **Type:** [OfferProcessingNoteDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingnotedto)[] The reasons why the product failed moderation.  
The reasons why the product failed moderation. _Min items:_ `1`  
status |  **Type:** [OfferProcessingStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingstatustype) Product publication status:
  * `UNKNOWN` — unknown status.
  * `READY` — the product has passed moderation. To place it on the Market, set a price for it.
  * `IN_WORK` — the product is undergoing moderation. It takes a few days.
  * `NEED_INFO` — the product failed moderation due to errors or missing information in the product description. Information about the reasons for the deviation is returned in the parameter `notes`.
  * `NEED_MAPPING` — you can't create a card for a product.
  * `NEED_CONTENT` — for a product without a SKU on the Market (`marketSku`) you need to find the card yourself (via the API or the seller's account on the Market) or create it if the product is not yet on sale on the Market.
  * `CONTENT_PROCESSING` — the product is under moderation.
  * `SUSPENDED` — the product has not passed moderation, as the Market does not yet place such products.
  * `REJECTED` — the product has not passed moderation, as the Market does not plan to post such products.
  * `REVIEW` — a decision is being made on the placement of the product.
  * `CREATE_ERROR` — the product profile could not be created.
  * `UPDATE_ERROR` — the product card has unused changes.

_Enum:_ `UNKNOWN`, `READY`, `IN_WORK`, `NEED_INFO`, `NEED_MAPPING`, `NEED_CONTENT`, `CONTENT_PROCESSING`, `SUSPENDED`, `REJECTED`, `REVIEW`, `CREATE_ERROR`, `UPDATE_ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#dayofweektype)DayOfWeekType
Day of the week:
  * `MONDAY` — Monday.
  * `TUESDAY` "Tuesday."
  * `WEDNESDAY` — Wednesday.
  * `THURSDAY` — Thursday.
  * `FRIDAY` — Friday.
  * `SATURDAY` "Saturday."
  * `SUNDAY` — Sunday.

**Type** |  **Description**  
---|---  
[DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#dayofweektype) |  _Enum:_ `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerweightdimensionsdto)OfferWeightDimensionsDTO
The dimensions of the package and the weight of the product.
If the product takes up several boxes, fold them compactly before measuring the dimensions.
![Multi-seat cargo measurement scheme](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/reference/boxes-measure.png)
**Name** |  **Description**  
---|---  
height* |  **Type:** number Package height in cm. _Example:_ `20` _Min value:_ `0`  
length* |  **Type:** number Package length in cm. _Example:_ `65.55` _Min value:_ `0`  
weight* |  **Type:** number The weight of the product in kg, including packaging (gross). _Example:_ `1.001` _Min value:_ `0`  
width* |  **Type:** number Package width in cm. _Example:_ `50.7` _Min value:_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeunittype)TimeUnitType
Time measurement unit:
  * `HOUR` "An hour."
  * `DAY` — a day.
  * `WEEK` — a week.
  * `MONTH` — a month.
  * `YEAR` — a year.

**Type** |  **Description**  
---|---  
[TimeUnitType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#timeunittype) |  _Enum:_ `HOUR`, `DAY`, `WEEK`, `MONTH`, `YEAR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingnotedto)OfferProcessingNoteDTO
The reasons why the product failed moderation.
**Name** |  **Description**  
---|---  
payload |  **Type:** string Additional information about the reason for the product rejection.  
type |  **Type:** [OfferProcessingNoteType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingnotetype) The type of reason why the product failed moderation. _Enum:_ `ASSORTMENT`, `CANCELLED`, `CONFLICTING_INFORMATION`, `OTHER`, `DEPARTMENT_FROZEN`, `INCORRECT_INFORMATION`, `LEGAL_CONFLICT`, `NEED_CLASSIFICATION_INFORMATION`, `NEED_INFORMATION`, `NEED_PICTURES`, `NEED_VENDOR`, `NO_CATEGORY`, `NO_KNOWLEDGE`, `NO_PARAMETERS_IN_SHOP_TITLE`, `NO_SIZE_MEASURE`, `SAMPLE_LINE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingstatustype)OfferProcessingStatusType
Product publication status:
  * `UNKNOWN` — unknown status.
  * `READY` — the product has passed moderation. To place it on the Market, set a price for it.
  * `IN_WORK` — the product is undergoing moderation. It takes a few days.
  * `NEED_INFO` — the product failed moderation due to errors or missing information in the product description. Information about the reasons for the deviation is returned in the parameter `notes`.
  * `NEED_MAPPING` — you can't create a card for a product.
  * `NEED_CONTENT` — for a product without a SKU on the Market (`marketSku`) you need to find the card yourself (via the API or the seller's account on the Market) or create it if the product is not yet on sale on the Market.
  * `CONTENT_PROCESSING` — the product is under moderation.
  * `SUSPENDED` — the product has not passed moderation, as the Market does not yet place such products.
  * `REJECTED` — the product has not passed moderation, as the Market does not plan to post such products.
  * `REVIEW` — a decision is being made on the placement of the product.
  * `CREATE_ERROR` — the product profile could not be created.
  * `UPDATE_ERROR` — the product card has unused changes.

**Type** |  **Description**  
---|---  
[OfferProcessingStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingstatustype) |  _Enum:_ `UNKNOWN`, `READY`, `IN_WORK`, `NEED_INFO`, `NEED_MAPPING`, `NEED_CONTENT`, `CONTENT_PROCESSING`, `SUSPENDED`, `REJECTED`, `REVIEW`, `CREATE_ERROR`, `UPDATE_ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingnotetype)OfferProcessingNoteType
The type of reason why the product failed moderation:
  * `ASSORTMENT` — the product is produced in different versions. Each of them should be described as a separate product (parameter `offerMappings` in the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/business-assortment/updateOfferMappings) or a line in the catalog if you upload products through the seller's account on the Market).
  * `CANCELLED` — the product was withdrawn from moderation on your initiative.
  * `CONFLICTING_INFORMATION` _(previously wrongly`CONFLICTING`)_ — you provided conflicting information about the product. The parameters that need to be fixed are specified in the parameter `payload`.
  * `OTHER` — the product did not pass moderation for another reason. Contact customer support or your manager.
  * `DEPARTMENT_FROZEN` — the rules for placing products in this category are being processed, so the product cannot pass moderation yet.
  * `INCORRECT_INFORMATION` — the product information you provided contradicts the description from the manufacturer. The parameters that need to be fixed are specified in the parameter `payload`.
  * `LEGAL_CONFLICT` — the product did not pass moderation for legal reasons. For example, it is not officially sold in Russia or you do not have a permit to sell it.
  * `NEED_CLASSIFICATION_INFORMATION` — the information about the product that you provided is not enough to classify it. Make sure that you have correctly specified the name, category, manufacturer, and country of manufacture of the product, as well as the URLs of images or description pages that can be used to identify the product.
  * `NEED_INFORMATION` — the product has not been sold in Russia before and is not yet available on the Market. You can create a card for it. For more information, see the section [Working with the product card](https://yandex.ru/support/marketplace/assortment/content/index.html) Yandex. Market help for sellers.
  * `NEED_PICTURES` — to identify a product, you need its images. Send the URL of the product images in the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/business-assortment/updateOfferMappings) or download the updated catalog through the seller's account on the Market.
  * `NEED_VENDOR` — the manufacturer of the product is incorrectly specified.
  * `NO_CATEGORY`, `NO_KNOWLEDGE` — products from the specified category are not yet placed on the Market. If the category appears, the product will be sent for moderation again.
  * `NO_PARAMETERS_IN_SHOP_TITLE` — the product is produced in different versions, and it is not clear from the name indicated which one it is about. The parameters to be added to the product name are specified in the parameter `payload`.
  * `NO_SIZE_MEASURE` — this product requires a size grid. Send it to the support service or your manager. The size grid requirements are specified in the parameter `payload`.
  * `SAMPLE_LINE` — the product did not pass moderation because of an extra line.

**Type** |  **Description**  
---|---  
[OfferProcessingNoteType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#offerprocessingnotetype) |  _Enum:_ `ASSORTMENT`, `CANCELLED`, `CONFLICTING_INFORMATION`, `OTHER`, `DEPARTMENT_FROZEN`, `INCORRECT_INFORMATION`, `LEGAL_CONFLICT`, `NEED_CLASSIFICATION_INFORMATION`, `NEED_INFORMATION`, `NEED_PICTURES`, `NEED_VENDOR`, `NO_CATEGORY`, `NO_KNOWLEDGE`, `NO_PARAMETERS_IN_SHOP_TITLE`, `NO_SIZE_MEASURE`, `SAMPLE_LINE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#200-ok)200 OK
The status of the operation.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body1)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#423-locked)423 Locked
The specified method cannot be applied to the resource. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/concepts/error-codes#423)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#body8)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/updateOfferMappingEntries#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "offerMappingEntries": [ { "offer": { "name": "Ударная дрель Makita HP1630, 710 Вт", "shopSku": "string", "category": "string", "vendor": "LEVENHUK", "vendorCode": "VNDR-0005A", "description": "string", "id": "string", "feedId": 0, "barcodes": [ 46012300000000 ], "urls": [ "string" ], "pictures": [ "string" ], "manufacturer": "string", "manufacturerCountries": [ "string" ], "minShipment": 0, "transportUnitSize": 0, "quantumOfSupply": 0, "deliveryDurationDays": 0, "boxCount": 0, "customsCommodityCodes": [ "string" ], "weightDimensions": { "length": 65.55, "width": 50.7, "height": 20, "weight": 1.001 }, "supplyScheduleDays": [ "MONDAY" ], "shelfLifeDays": 0, "lifeTimeDays": 0, "guaranteePeriodDays": 0, "processingState": { "status": "UNKNOWN", "notes": [ { "type": "ASSORTMENT", "payload": "string" } ] }, "availability": "ACTIVE", "shelfLife": { "timePeriod": 0, "timeUnit": "HOUR", "comment": "string" }, "lifeTime": { "timePeriod": 0, "timeUnit": "HOUR", "comment": "string" }, "guaranteePeriod": { "timePeriod": 0, "timeUnit": "HOUR", "comment": "string" }, "certificate": "string" }, "mapping": { "marketSku": 0, "modelId": 0, "categoryId": 0 }, "awaitingModerationMapping": { "marketSku": 0, "modelId": 0, "categoryId": 0 }, "rejectedMapping": { "marketSku": 0, "modelId": 0, "categoryId": 0 } } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
**What is GTIN?**  
GTIN is a unique number assigned to a product in a single international database.   
  
**How to make sure that the product is in the database**  
You can check the code on   
  
**How to get a GTIN for your products**  
To receive GTIN codes, the manufacturer needs to join the GS1 association and register the products.
### Was the article helpful?
YesNo
Previous
[Information about child regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/regions/searchRegionChildren)
Next
[List of products](https://yandex.ru/dev/market/partner-api/doc/en/reference/offer-mappings/en/reference/offer-mappings/getOfferMappingEntries)
