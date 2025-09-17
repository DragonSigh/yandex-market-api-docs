---
title: Resuming the display - Hidden Goods | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/deleteHiddenOffers
crawled_at: 2025-09-17T14:30:07.660357
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body)
    * [HiddenOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#hiddenofferdto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body1)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body6)
  * [423 Locked](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#423-locked)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body7)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body8)


# Resuming product display
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * all-methods — Full account management


Resumes displaying the store's hidden items on the Market.
The data in the catalog is not updated instantly
It takes up to a few minutes.
**, Limit:** 10,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/hidden-offers/delete

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body)Body
application/json
```
{
    "hiddenOffers": [
        {
            "offerId": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
hiddenOffers* |  **Type:** [HiddenOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#hiddenofferdto)[] A list of hidden goods.   
Information about hiding. _Min items:_ `1` _Max items:_ `500`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#hiddenofferdto)HiddenOfferDTO
Information about hiding.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#200-ok)200 OK
The product display has resumed.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body1)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#423-locked)423 Locked
The specified method cannot be applied to the resource. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#423)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#body8)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteHiddenOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "hiddenOffers": [ { "offerId": "string" } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Hiding goods](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/addHiddenOffers)
Next
[Adding products](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/business-assortment/addOffersToArchive)
