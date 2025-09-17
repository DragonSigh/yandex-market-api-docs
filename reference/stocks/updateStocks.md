---
title: Transfer of leftovers - Balances and turnover | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/updateStocks
crawled_at: 2025-09-17T14:30:21.785528
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body)
    * [UpdateStockDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#updatestockdto)
    * [UpdateStockItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#updatestockitemdto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body1)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body7)


# Transmitting information about balances
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * all-methods — Full account management


Transmits data about the remaining goods in the showcase.
For a group of warehouses, transfer the leftovers only for **one of any warehouse**. The information for the other warehouses in this group will be updated automatically.
Be sure to specify the SKU **Exactly** the way it is listed in the catalog. For example, _557722_ and _0557722_ — these are two different SKUs.
The data in the catalog is not updated instantly
It takes up to a few minutes.
**, Limit:** 100,000 products per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#request)Request
PUT
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offers/stocks

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body)Body
application/json
```
{
    "skus": [
        {
            "sku": "string",
            "items": [
                {
                    "count": 0,
                    "updatedAt": "2022-12-29T18:02:01Z"
                }
            ]
        }
    ]
}

```

**Name** |  **Description**  
---|---  
skus* |  **Type:** [UpdateStockDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#updatestockdto)[] Data on the remaining goods.   
Information about the remains of one product in one of the warehouses. _Min items:_ `1` _Max items:_ `2000`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#updatestockdto)UpdateStockDTO
Information about the remains of one product in one of the warehouses.
**Name** |  **Description**  
---|---  
items* |  **Type:** [UpdateStockItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#updatestockitemdto)[] Information about the remaining goods.   
Information about the remaining goods. _Min items:_ `1` _Max items:_ `1`  
sku* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#updatestockitemdto)UpdateStockItemDTO
Information about the remaining goods.
**Name** |  **Description**  
---|---  
count* |  **Type:** integer<int64> The quantity of the available product. _Min value:_ `0` _Max value:_ `2000000000`  
updatedAt |  **Type:** string<date-time> The date and time of the last update of the balance information.   
  
If you did not pass the parameter `updatedAt`, the current time is used.   
  
Date and time format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:42:42+03:00`.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#200-ok)200 OK
An empty answer.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body1)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "skus": [ { "sku": "string", "items": [ { "count": 0, "updatedAt": "2022-12-29T18:02:01Z" } ] } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Viewing balances and turnover](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks)
Next
[Cost of services](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/tariffs/calculateTariffs)
