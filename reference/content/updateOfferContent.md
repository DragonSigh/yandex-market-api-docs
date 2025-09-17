---
title: Editing product category characteristics - Product cards | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/content/updateOfferContent
crawled_at: 2025-09-17T14:37:45.597579
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body)
    * [OfferContentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontentdto)
    * [ParameterValueDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#parametervaluedto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body1)
    * [UpdateOfferContentResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#updateoffercontentresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype)
    * [OfferContentErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontenterrordto)
    * [OfferContentErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontenterrortype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body6)
  * [423 Locked](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#423-locked)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body7)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body8)


# Editing product category characteristics
Info
Console
**The method is available for models:[FBY, FBS, Express and DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * all-methods — Full account management


Edits product characteristics that are specific to the category it belongs to.
Here is only what belongs to a specific category.
If you need to change the main parameters of the product (name, description, images, video, manufacturer, barcode), use the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/business-assortment/updateOfferMappings).
To remove the characteristics that are set in the parameters with the type `string`, pass an empty value.
The data in the catalog is not updated instantly
It takes up to a few minutes.
**, Limit:** 10,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/offer-cards/update

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body)Body
application/json
```
{
    "offersContent": [
        {
            "offerId": "string",
            "categoryId": 0,
            "parameterValues": [
                {
                    "parameterId": 0,
                    "unitId": 0,
                    "valueId": 0,
                    "value": "string"
                }
            ]
        }
    ]
}

```

**Name** |  **Description**  
---|---  
offersContent* |  **Type:** [OfferContentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontentdto)[] A list of products with the specified characteristics.  
An item with the specified characteristics. _Min items:_ `1` _Max items:_ `100`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontentdto)OfferContentDTO
An item with the specified characteristics.
**Name** |  **Description**  
---|---  
categoryId* |  **Type:** integer<int32> The ID of the category on the Market. When changing the category, make sure that the product characteristics and their values in the parameter `parameterValues` you are submitting for a new category. You can get a list of Market categories using a request. [POST v2/categories/tree](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/categories/getCategoriesTree). _Min value (exclusive):_ `0`  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
parameterValues* |  **Type:** [ParameterValueDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#parametervaluedto)[] A list of characteristics with their values. By **change** pass only those characteristics whose value needs to be updated. If in `categoryId` you are changing the category, the values of the common characteristics for the old and new categories will remain, and you do not need to transfer them. To **delete** the value of the specified characteristic, pass it on `parameterId` with an empty `value`.   
The value of the characteristic. You can specify multiple values of the same characteristic, provided that:
  * Type of feature — `ENUM`.
  * In response to the request [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters) this characteristic has a field `multivalue` it matters `true`.

To do this, in `parameterValues` pass each value separately — multiple objects with parameters `parameterId`, `valueId` and `value`. Parameter `parameterId` it must be the same. _Min items:_ `1` _Max items:_ `300`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#parametervaluedto)ParameterValueDTO
The value of the characteristic.
You can specify multiple values of the same characteristic, provided that:
  * Type of feature — `ENUM`.
  * In response to the request [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters) this characteristic has a field `multivalue` it matters `true`.


To do this, in `parameterValues` pass each value separately — multiple objects with parameters `parameterId`, `valueId` and `value`. Parameter `parameterId` it must be the same.
**Name** |  **Description**  
---|---  
parameterId* |  **Type:** integer<int64> The identifier of the characteristic. _Min value:_ `1`  
unitId |  **Type:** integer<int64> ID of the unit of measurement. If you did not pass the parameter `unitId`, the default unit of measurement is used.  
value |  **Type:** string Meaning. For type characteristics `ENUM` transmit along with `valueId`.  
valueId |  **Type:** integer<int64> ID of the value. Be sure to specify the identifier if you are transmitting a value from the list of acceptable values received from the Market. Transmit along with `value`. Only for type characteristics `ENUM`.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#200-ok)200 OK
The request was executed correctly, and the data has been processed.
Answer `200` by itself, it does not mean that the values passed are correct.
Be sure to look at the details of the response.: `status` and a list of errors, if any.
Even if an error is made in the characteristics of just one product, no changes from the request will be included in the catalog.
If in `status` It's back `ERROR`, make sure that:
  * All required specifications are filled in.
  * the characteristics actually exist in the specified categories;
  * the values correspond to the characteristics;
  * your own values have the desired data type.


Fields will help you find problems. `errors` and `warnings`.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body1)Body
application/json
```
{
    "status": "OK",
    "results": [
        {
            "offerId": "string",
            "errors": [
                {
                    "type": "OFFER_NOT_FOUND",
                    "parameterId": 0,
                    "message": "string"
                }
            ],
            "warnings": [
                {
                    "type": "OFFER_NOT_FOUND",
                    "parameterId": 0,
                    "message": "string"
                }
            ]
        }
    ]
}

```

**Name** |  **Description**  
---|---  
results |  **Type:** [UpdateOfferContentResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#updateoffercontentresultdto)[] Errors and warnings that appeared when processing the transmitted values. Each item in the list corresponds to one product. If there are no errors or warnings, the field is not passed.   
Errors and warnings that appeared due to the transmitted characteristics. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#updateoffercontentresultdto)UpdateOfferContentResultDTO
Errors and warnings that appeared due to the transmitted characteristics.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
errors |  **Type:** [OfferContentErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontenterrordto)[] Mistakes. If there is an error for at least one product, the information in the catalog will not be updated for all transferred products.   
The text of the error or warning. _Min items:_ `1`  
warnings |  **Type:** [OfferContentErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontenterrordto)[] Warnings. The information in the catalog will be updated.   
The text of the error or warning. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontenterrordto)OfferContentErrorDTO
The text of the error or warning.
**Name** |  **Description**  
---|---  
message* |  **Type:** string The text of the error or warning.  
type* |  **Type:** [OfferContentErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontenterrortype) Types of errors and warnings:
  * `OFFER_NOT_FOUND` — there is no such product in the catalog.
  * `UNKNOWN_CATEGORY` — an unknown category is specified.
  * `INVALID_CATEGORY` — a non-leaf category is specified. Specify the one that has no child categories.
  * `UNKNOWN_PARAMETER` — a characteristic has been transmitted that is not among the characteristics of the category.
  * `UNEXPECTED_BOOLEAN_VALUE` — something else is passed instead of the boolean value.
  * `NUMBER_FORMAT` — a string was passed that does not represent a number, instead of a number.
  * `INVALID_UNIT_ID` — a unit of measurement that is unacceptable for the characteristic has been passed.
  * `INVALID_GROUP_ID_LENGTH` — the name exceeds the allowed character value of 255.
  * `INVALID_GROUP_ID_CHARACTERS` — transferred _invalid characters_.

You can check which category characteristics are available for a given category and get their settings using a request. [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters). _Enum:_ `OFFER_NOT_FOUND`, `UNKNOWN_CATEGORY`, `INVALID_CATEGORY`, `UNKNOWN_PARAMETER`, `UNEXPECTED_BOOLEAN_VALUE`, `NUMBER_FORMAT`, `INVALID_UNIT_ID`, `INVALID_GROUP_ID_LENGTH`, `INVALID_GROUP_ID_CHARACTERS`  
parameterId |  **Type:** integer<int64> ID of the feature that the error or warning is associated with.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontenterrortype)OfferContentErrorType
Types of errors and warnings:
  * `OFFER_NOT_FOUND` — there is no such product in the catalog.
  * `UNKNOWN_CATEGORY` — an unknown category is specified.
  * `INVALID_CATEGORY` — a non-leaf category is specified. Specify the one that has no child categories.
  * `UNKNOWN_PARAMETER` — a characteristic has been transmitted that is not among the characteristics of the category.
  * `UNEXPECTED_BOOLEAN_VALUE` — something else is passed instead of the boolean value.
  * `NUMBER_FORMAT` — a string was passed that does not represent a number, instead of a number.
  * `INVALID_UNIT_ID` — a unit of measurement that is unacceptable for the characteristic has been passed.
  * `INVALID_GROUP_ID_LENGTH` — the name exceeds the allowed character value of 255.
  * `INVALID_GROUP_ID_CHARACTERS` — transferred _invalid characters_.


You can check which category characteristics are available for a given category and get their settings using a request. [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getCategoryContentParameters).
**Type** |  **Description**  
---|---  
[OfferContentErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#offercontenterrortype) |  _Enum:_ `OFFER_NOT_FOUND`, `UNKNOWN_CATEGORY`, `INVALID_CATEGORY`, `UNKNOWN_PARAMETER`, `UNEXPECTED_BOOLEAN_VALUE`, `NUMBER_FORMAT`, `INVALID_UNIT_ID`, `INVALID_GROUP_ID_LENGTH`, `INVALID_GROUP_ID_CHARACTERS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#423-locked)423 Locked
The specified method cannot be applied to the resource. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#423)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#body8)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/updateOfferContent#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "offersContent": [ { "offerId": "string", "categoryId": 0, "parameterValues": [ { "parameterId": 0, "unitId": 0, "valueId": 0, "value": "string" } ] } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
ASCII characters 0 through 31 (except 9) and 127 are prohibited. 
### Was the article helpful?
YesNo
Previous
[Information about card occupancy](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/content/getOfferCardsContentStatus)
Next
[In the office](https://yandex.ru/dev/market/partner-api/doc/en/reference/content/en/reference/business-assortment/getOfferMappings)
