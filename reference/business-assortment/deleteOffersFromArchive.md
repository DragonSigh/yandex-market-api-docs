---
title: Deleting from the archive - Product Archive | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/deleteOffersFromArchive
crawled_at: 2025-09-17T14:38:10.140464
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body1)
    * [DeleteOffersFromArchiveDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#deleteoffersfromarchivedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body6)
  * [423 Locked](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#423-locked)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body7)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body8)


# Deleting products from the archive
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * all-methods — Full account management


Restores items from the archive.
**, Limit:** 10,000 products per minute, no more than 200 products per request  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/offer-mappings/unarchive

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body)Body
application/json
```
{
    "offerIds": [
        "string"
    ]
}

```

**Name** |  **Description**  
---|---  
offerIds* |  **Type:** string[] A list of products that need to be restored from the archive.  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `200` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#200-ok)200 OK
If some items could not be restored from the archive, the 200 response will contain a list of them.
The list of successfully restored items is not returned.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "notUnarchivedOfferIds": [
            "string"
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [DeleteOffersFromArchiveDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#deleteoffersfromarchivedto) Items that could not be restored from the archive.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#deleteoffersfromarchivedto)DeleteOffersFromArchiveDTO
Items that could not be restored from the archive.
**Name** |  **Description**  
---|---  
notUnarchivedOfferIds |  **Type:** string[] A list of products that could not be restored from the archive.  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#423-locked)423 Locked
The specified method cannot be applied to the resource. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#423)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#body8)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "offerIds": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Adding products](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive)
Next
[Viewing balances and turnover](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/stocks/getStocks)
