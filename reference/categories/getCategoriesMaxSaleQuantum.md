---
title: The limit on setting the quantum and minimum quantity of goods - Products | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/getCategoriesMaxSaleQuantum
crawled_at: 2025-09-17T14:44:50.104032
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body1)
    * [MaxSaleQuantumDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#maxsalequantumdto)
    * [CategoryErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#categoryerrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype)
    * [CategoryErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#categoryerrortype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body7)


# The limit for setting the sales quantum and the minimum number of items in an order
Deprecated
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns the installation limit _The quantum_ and the minimum number of products in the order that you can specify for the products of the specified categories.
If you pass the value of the quantum or the minimum quantity of goods above the limit set by the Market, the goods will be hidden from the showcase.
For more information on how to sell products in several pieces, read [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/fields/quantum).
**, Limit:** 5,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/categories/max-sale-quantum

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body)Body
application/json
```
{
    "marketCategoryIds": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
marketCategoryIds* |  **Type:** integer<int64>[] Ids _leaf categories_ on the Market.  
_Min items:_ `1` _Max items:_ `1500` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#200-ok)200 OK
The limit for setting the quantum and minimum quantity of goods.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body1)Body
application/json
```
{
    "status": "OK",
    "results": [
        {
            "id": 0,
            "name": "string",
            "maxSaleQuantum": 0
        }
    ],
    "errors": [
        {
            "categoryId": 0,
            "type": "UNKNOWN_CATEGORY"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
results* |  **Type:** [MaxSaleQuantumDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#maxsalequantumdto)[] Categories and the limit for setting the quantity and minimum quantity of goods.  
The limit for setting the quantum and the minimum number of products by category.  
errors |  **Type:** [CategoryErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#categoryerrordto)[] Errors that appeared due to the passed categories.  
The error text. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#maxsalequantumdto)MaxSaleQuantumDTO
The limit for setting the quantum and the minimum number of products by category.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The category ID.  
maxSaleQuantum |  **Type:** integer The limit for setting the quantum and minimum quantity of goods.  
name |  **Type:** string The name of the category.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#categoryerrordto)CategoryErrorDTO
The error text.
**Name** |  **Description**  
---|---  
categoryId |  **Type:** integer<int64> The category ID.  
type |  **Type:** [CategoryErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#categoryerrortype) Types of errors:
  * `UNKNOWN_CATEGORY` — an unknown category is specified.
  * `CATEGORY_IS_NOT_LEAF` — a non-leaf category is specified. Specify the one that has no child categories.

_Enum:_ `UNKNOWN_CATEGORY`, `CATEGORY_IS_NOT_LEAF`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#categoryerrortype)CategoryErrorType
Types of errors:
  * `UNKNOWN_CATEGORY` — an unknown category is specified.
  * `CATEGORY_IS_NOT_LEAF` — a non-leaf category is specified. Specify the one that has no child categories.

**Type** |  **Description**  
---|---  
[CategoryErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#categoryerrortype) |  _Enum:_ `UNKNOWN_CATEGORY`, `CATEGORY_IS_NOT_LEAF`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesMaxSaleQuantum#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Body{ "marketCategoryIds": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
If a sales quantum is set, the buyer will be able to add only a multiple of the number of products to the order.  
  
For example, if the sales quantum is 5, the buyer will be able to add 5, 10, 15, etc. items to the basket, but 1, 2, or 7 will not be able to.
Categories that have no children.
### Was the article helpful?
YesNo
Previous
[List of products](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/offer-mappings/getOfferMappingEntries)
Next
[Recommended cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/offer-mappings/getSuggestedOfferMappingEntries)
