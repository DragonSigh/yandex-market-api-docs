---
title: In the shop - Deleting products | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/deleteCampaignOffers
crawled_at: 2025-09-17T14:29:43.654737
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body1)
    * [DeleteCampaignOffersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#deletecampaignoffersdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body6)
  * [423 Locked](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#423-locked)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body7)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body8)


# Removing items from the store's assortment
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * all-methods — Full account management


Deletes the specified products from the specified store.
The request deletes products from a specific store
It does not affect sales in other stores or the availability of goods in the general catalog.
You will not be able to delete the product if it is stored in the Market warehouses.
**, Limit:** 10,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offers/delete

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body)Body
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
offerIds* |  **Type:** string[] Product IDs in the catalog.  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `500` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#200-ok)200 OK
If not all products were deleted, the 200 response returns a list of those that were in the request but remained in the store.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "notDeletedOfferIds": [
            "string"
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [DeleteCampaignOffersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#deletecampaignoffersdto) A list of products that could not be deleted because they were not found or are stored in the Market warehouse.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#deletecampaignoffersdto)DeleteCampaignOffersDTO
A list of products that could not be deleted because they were not found or are stored in the Market warehouse.
**Name** |  **Description**  
---|---  
notDeletedOfferIds |  **Type:** string[] List of SKUs.  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#423-locked)423 Locked
The specified method cannot be applied to the resource. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#423)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#body8)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/deleteCampaignOffers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "offerIds": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[In the office](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/business-assortment/deleteOffers)
Next
[Viewing hidden goods](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getHiddenOffers)
