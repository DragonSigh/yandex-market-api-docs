---
title: Lists of product characteristics by category - Products | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/content/getCategoryContentParameters
crawled_at: 2025-09-17T14:29:21.211214
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body)
    * [CategoryContentParametersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categorycontentparametersdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype)
    * [CategoryParameterDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categoryparameterdto)
    * [ParameterType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametertype)
    * [ParameterValueConstraintsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametervalueconstraintsdto)
    * [OfferCardRecommendationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#offercardrecommendationtype)
    * [CategoryParameterUnitDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categoryparameterunitdto)
    * [ValueRestrictionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#valuerestrictiondto)
    * [ParameterValueOptionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametervalueoptiondto)
    * [UnitDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#unitdto)
    * [OptionValuesLimitedDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#optionvalueslimiteddto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body6)


# Lists of product characteristics by category
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns a list of characteristics with acceptable values for a given _The leaf category_.
**, Limit:** 100 categories per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/category/{categoryId}/parameters

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
categoryId* |  **Type:** integer<int64> The ID of the category on the Market. To find out the ID of the category to which the product you are interested in belongs, use the request [POST v2/categories/tree](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/categories/getCategoriesTree).   
_Min value (exclusive):_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
businessId |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/campaigns/getCampaigns). Pass the parameter to get the characteristics that are the features of the product variant in this cabinet.   
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#200-ok)200 OK
A list of product characteristics from the specified category.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "categoryId": 0,
        "parameters": [
            {
                "id": 0,
                "name": "string",
                "type": "TEXT",
                "unit": {
                    "defaultUnitId": 0,
                    "units": [
                        {
                            "id": 0,
                            "name": "кг",
                            "fullName": "килограмм"
                        }
                    ]
                },
                "description": "string",
                "recommendationTypes": [
                    "HAS_VIDEO"
                ],
                "required": false,
                "filtering": false,
                "distinctive": false,
                "multivalue": false,
                "allowCustomValues": false,
                "values": [
                    {
                        "id": 0,
                        "value": "string",
                        "description": "string"
                    }
                ],
                "constraints": {
                    "minValue": 0,
                    "maxValue": 0,
                    "maxLength": 0
                },
                "valueRestrictions": [
                    {
                        "limitingParameterId": 0,
                        "limitedValues": [
                            {
                                "limitingOptionValueId": 0,
                                "optionValueIds": [
                                    0
                                ]
                            }
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
result |  **Type:** [CategoryContentParametersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categorycontentparametersdto) Information about the category parameters.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categorycontentparametersdto)CategoryContentParametersDTO
Information about the category parameters.
**Name** |  **Description**  
---|---  
categoryId* |  **Type:** integer<int32> The ID of the category on the Market. When changing the category, make sure that the product characteristics and their values in the parameter `parameterValues` you are submitting for a new category. You can get a list of Market categories using a request. [POST v2/categories/tree](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/categories/getCategoriesTree). _Min value (exclusive):_ `0`  
parameters |  **Type:** [CategoryParameterDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categoryparameterdto)[] A list of characteristics.  
Product characteristics. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categoryparameterdto)CategoryParameterDTO
Product characteristics.
**Name** |  **Description**  
---|---  
allowCustomValues* |  **Type:** boolean Is it possible to pass a custom value that is not in the list of Market options? Only for type characteristics `ENUM`.  
distinctive* |  **Type:** boolean Whether the characteristic is a feature of the variant.  
filtering* |  **Type:** boolean Whether the characteristic is used in the filter.  
id* |  **Type:** integer<int64> The identifier of the characteristic. _Min value:_ `1`  
multivalue* |  **Type:** boolean Is it possible to pass multiple values at once?  
required* |  **Type:** boolean Mandatory characteristics.  
type* |  **Type:** [ParameterType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametertype) The type of data. _Enum:_ `TEXT`, `ENUM`, `BOOLEAN`, `NUMERIC`  
constraints |  **Type:** [ParameterValueConstraintsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametervalueconstraintsdto) Restrictions on values. Only for type characteristics `TEXT` and `NUMERIC`.  
description |  **Type:** string Description of the characteristic.  
name |  **Type:** string The name of the characteristic.  
recommendationTypes |  **Type:** [OfferCardRecommendationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#offercardrecommendationtype)[] A list of possible recommendations for filling out the card, to which this characteristic applies.  
A recommendation for adding or replacing content. It is not refunded for cards that are filled with the Market or contain used goods. Some of the recommendations relate to **the main parameters** , which are available for products of any category. Others belong to those **characteristics** which the product has because it belongs to a certain category. **1. Recommendations related to the main parameters** Each such recommendation applies to **the only parameter**. To fill in this parameter, use the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/business-assortment/updateOfferMappings). Recommendations for filling in the parameters in `updateOfferMappings`:
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

_Enum:_ `HAS_VIDEO`, `RECOGNIZED_VENDOR`, `MAIN`, `ADDITIONAL`, `DISTINCTIVE`, `FILTERABLE`, `PICTURE_COUNT`, `HAS_DESCRIPTION`, `HAS_BARCODE`, `FIRST_PICTURE_SIZE`, `TITLE_LENGTH`, `DESCRIPTION_LENGTH`, `AVERAGE_PICTURE_SIZE`, `FIRST_VIDEO_SIZE`, `FIRST_VIDEO_LENGTH`, `AVERAGE_VIDEO_SIZE`, `VIDEO_COUNT` _Min items:_ `1` _Unique items_  
unit |  **Type:** [CategoryParameterUnitDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categoryparameterunitdto) Units of measurement of product characteristics.  
valueRestrictions |  **Type:** [ValueRestrictionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#valuerestrictiondto)[] Restrictions on values imposed by other characteristics. Only for type characteristics `ENUM`.  
A restriction on possible values imposed by another characteristic. If the limiting characteristic takes on a certain value, the list of possible values of the limited characteristic is reduced. **Example** Characteristic **size** It can take nine different values by itself.: `S`, `M`, `L`, `44`, `46`, `48`, `42/164`, `46/176`, `44S`. If the limiting characteristic is **The size grid** takes the value `RU`, the list of possible size values is reduced to `44`, `46`, `48`. _Min items:_ `1`  
values |  **Type:** [ParameterValueOptionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametervalueoptiondto)[] A list of acceptable parameter values. Only for type characteristics `ENUM`.  
The value of the characteristic. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametertype)ParameterType
Data type:
  * `TEXT` — the text.
  * `ENUM` — a list of possible values.
  * `BOOLEAN` — `true` or `false`.
  * `NUMERIC` — the number.

**Type** |  **Description**  
---|---  
[ParameterType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametertype) |  _Enum:_ `TEXT`, `ENUM`, `BOOLEAN`, `NUMERIC`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametervalueconstraintsdto)ParameterValueConstraintsDTO
Restrictions on the values of characteristics.
**Name** |  **Description**  
---|---  
maxLength |  **Type:** integer<int32> The maximum length of the text.  
maxValue |  **Type:** number<double> The maximum number.  
minValue |  **Type:** number<double> The minimum number.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#offercardrecommendationtype)OfferCardRecommendationType
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
[OfferCardRecommendationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#offercardrecommendationtype) |  _Enum:_ `HAS_VIDEO`, `RECOGNIZED_VENDOR`, `MAIN`, `ADDITIONAL`, `DISTINCTIVE`, `FILTERABLE`, `PICTURE_COUNT`, `HAS_DESCRIPTION`, `HAS_BARCODE`, `FIRST_PICTURE_SIZE`, `TITLE_LENGTH`, `DESCRIPTION_LENGTH`, `AVERAGE_PICTURE_SIZE`, `FIRST_VIDEO_SIZE`, `FIRST_VIDEO_LENGTH`, `AVERAGE_VIDEO_SIZE`, `VIDEO_COUNT`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#categoryparameterunitdto)CategoryParameterUnitDTO
Units of measurement of product characteristics.
**Name** |  **Description**  
---|---  
defaultUnitId* |  **Type:** integer<int64> The default unit of measurement.  
units* |  **Type:** [UnitDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#unitdto)[] Acceptable units of measurement.  
Unit of measurement.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#valuerestrictiondto)ValueRestrictionDTO
A restriction on possible values imposed by another characteristic.
If the limiting characteristic takes on a certain value, the list of possible values of the limited characteristic is reduced.
**Example**
Characteristic **size** It can take nine different values by itself.: `S`, `M`, `L`, `44`, `46`, `48`, `42/164`, `46/176`, `44S`.
If the limiting characteristic is **The size grid** takes the value `RU`, the list of possible size values is reduced to `44`, `46`, `48`.
**Name** |  **Description**  
---|---  
limitedValues* |  **Type:** [OptionValuesLimitedDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#optionvalueslimiteddto)[] The values of the limiting characteristic and the corresponding allowable values of the current characteristic.  
The value of the limiting characteristic and the list of acceptable values of the limited characteristic.  
limitingParameterId* |  **Type:** integer<int64> ID of the limiting characteristic. _Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#parametervalueoptiondto)ParameterValueOptionDTO
The value of the characteristic.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> ID of the value.  
value* |  **Type:** string Meaning.  
description |  **Type:** string Description of the value.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#unitdto)UnitDTO
Unit of measurement.
**Name** |  **Description**  
---|---  
fullName* |  **Type:** string The full name of the unit of measurement. _Example:_ `kilogram`  
id* |  **Type:** integer<int64> ID of the unit of measurement.  
name* |  **Type:** string The abbreviated name of the unit of measurement. _Example:_ `kg`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#optionvalueslimiteddto)OptionValuesLimitedDTO
The value of the limiting characteristic and the list of acceptable values of the limited characteristic.
**Name** |  **Description**  
---|---  
limitingOptionValueId* |  **Type:** integer<int64> ID of the value of the limiting characteristic.  
optionValueIds* |  **Type:** integer<int64>[] Ids of acceptable values of the restricted characteristic.   
_Min value:_ `1` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
categoryId*:
Query parameters
businessId:
Send
No longer supported, please use an alternative and newer version.
Copied
A category that has no children.
### Was the article helpful?
YesNo
Previous
[The category tree](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/categories/getCategoriesTree)
Next
[Adding products and changing information](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/business-assortment/updateOfferMappings)
