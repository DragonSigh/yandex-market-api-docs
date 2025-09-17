---
title: The category tree - Products | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/getCategoriesTree
crawled_at: 2025-09-17T14:29:10.780742
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body)
    * [LanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#languagetype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body1)
    * [CategoryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#categorydto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body7)


# The category tree
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/pricing_read-only)
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/promotion_read-only)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/finance-and-accounting)
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/communication)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/settings-management)
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns the category tree of the Market.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/categories/tree

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body)Body
application/json
```
{
    "language": "RU"
}

```

**Name** |  **Description**  
---|---  
language |  **Type:** [LanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#languagetype) The language of the categories. _Enum:_ `RU`, `EN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#languagetype)LanguageType
Language:
  * `RU` — Russian.
  * `EN` — English.

**Type** |  **Description**  
---|---  
[LanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#languagetype) |  _Enum:_ `RU`, `EN`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#200-ok)200 OK
Market categories.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "id": 0,
        "name": "string",
        "children": [
            null
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [CategoryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#categorydto) Information about the category. A category is considered a leaf category if it has no child categories.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#categorydto)CategoryDTO
Information about the category.
A category is considered a leaf category if it has no child categories.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The category ID.  
name* |  **Type:** string The name of the category.  
children |  **Type:** [CategoryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#categorydto)[] Child categories.  
Information about the category. A category is considered a leaf category if it has no child categories. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/categories/getCategoriesTree#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Body{ "language": "RU" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Store Settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/campaigns/getCampaignSettings)
Next
[Lists of product characteristics by category](https://yandex.ru/dev/market/partner-api/doc/en/reference/categories/en/reference/content/getCategoryContentParameters)
