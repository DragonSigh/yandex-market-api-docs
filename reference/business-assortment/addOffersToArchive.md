---
title: Adding products - Product Archive | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/addOffersToArchive
crawled_at: 2025-09-17T14:38:04.692250
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body1)
    * [AddOffersToArchiveDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchivedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype)
    * [AddOffersToArchiveErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchiveerrordto)
    * [AddOffersToArchiveErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchiveerrortype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body6)
  * [423 Locked](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#423-locked)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body7)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body8)


# Adding products to the archive
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * all-methods — Full account management


Puts the products in the archive. The items stored in the archive are hidden from the display case in all the cabinet stores.
You cannot send an item stored in a Market warehouse to the archive.
First, such goods need to be sold or exported.
**, Limit:** 10,000 products per minute, no more than 200 products per request  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/offer-mappings/archive

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body)Body
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
offerIds* |  **Type:** string[] A list of products that need to be archived.  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `200` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#200-ok)200 OK
If some products could not be added to the archive, the 200 response will contain a list of them.
The list of successfully added products is not returned.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "notArchivedOffers": [
            {
                "offerId": "string",
                "error": "OFFER_HAS_STOCKS"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [AddOffersToArchiveDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchivedto) Items that could not be archived.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchivedto)AddOffersToArchiveDTO
Items that could not be archived.
**Name** |  **Description**  
---|---  
notArchivedOffers |  **Type:** [AddOffersToArchiveErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchiveerrordto)[] A list of products that could not be archived.  
An item that could not be archived. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchiveerrordto)AddOffersToArchiveErrorDTO
An item that could not be archived.
**Name** |  **Description**  
---|---  
error* |  **Type:** [AddOffersToArchiveErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchiveerrortype) The reason why the product could not be archived. _Enum:_ `OFFER_HAS_STOCKS`, `UNKNOWN`  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchiveerrortype)AddOffersToArchiveErrorType
The reason why the product could not be archived:
  * `OFFER_HAS_STOCKS` — the product is stored in the Market warehouse.
  * `UNKNOWN` — unknown error cause. Most likely, there was a failure on the Market side. If the error persists for a long time, contact support.

**Type** |  **Description**  
---|---  
[AddOffersToArchiveErrorType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#addofferstoarchiveerrortype) |  _Enum:_ `OFFER_HAS_STOCKS`, `UNKNOWN`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#423-locked)423 Locked
The specified method cannot be applied to the resource. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#423)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#body8)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/addOffersToArchive#apiresponsestatustype) The type of response. Possible values:
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
[Resuming the display](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/assortment/deleteHiddenOffers)
Next
[Deleting from the archive](https://yandex.ru/dev/market/partner-api/doc/en/reference/business-assortment/en/reference/business-assortment/deleteOffersFromArchive)
