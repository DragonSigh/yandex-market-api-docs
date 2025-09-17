---
title: Products in the application - FBY requests | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/getSupplyRequestItems
crawled_at: 2025-09-17T14:34:20.699330
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body1)
    * [GetSupplyRequestItemsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#getsupplyrequestitemsdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype)
    * [SupplyRequestItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#supplyrequestitemdto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#forwardscrollingpagerdto)
    * [SupplyRequestItemCountersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#supplyrequestitemcountersdto)
    * [CurrencyValueDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#currencyvaluedto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#currencytype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body7)


# Receipt of goods in an application for delivery, export or disposal
Info
Console
**The method is available for the[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/overview/fby) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns the list of products in the application and information about them.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/supply-requests/items

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body)Body
application/json
```
{
    "requestId": 0
}

```

**Name** |  **Description**  
---|---  
requestId* |  **Type:** integer<int64> The application ID. Used only in the API It will not be possible to find applications in the seller's account on the Market. To do this, use `marketplaceRequestId` or `warehouseRequestId`. _Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#200-ok)200 OK
The list of products in the application and information about them.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "items": [
            {
                "offerId": "string",
                "name": "string",
                "price": {
                    "value": 0,
                    "currencyId": "RUR"
                },
                "counters": {
                    "planCount": 0,
                    "factCount": 0,
                    "surplusCount": 0,
                    "shortageCount": 0,
                    "defectCount": 0
                }
            }
        ],
        "paging": {
            "nextPageToken": "string"
        }
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GetSupplyRequestItemsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#getsupplyrequestitemsdto) Information about the products in the application.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#getsupplyrequestitemsdto)GetSupplyRequestItemsDTO
Information about the products in the application.
**Name** |  **Description**  
---|---  
items* |  **Type:** [SupplyRequestItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#supplyrequestitemdto)[] The list of products.  
Information about the product in the application. _Min items:_ `0` _Max items:_ `100`  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#supplyrequestitemdto)SupplyRequestItemDTO
Information about the product in the application.
**Name** |  **Description**  
---|---  
counters* |  **Type:** [SupplyRequestItemCountersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#supplyrequestitemcountersdto) The number of products in the application.  
name* |  **Type:** string Product name.  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
price |  **Type:** [CurrencyValueDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#currencyvaluedto) Currency and its value.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#supplyrequestitemcountersdto)SupplyRequestItemCountersDTO
The number of products in the application.
**Name** |  **Description**  
---|---  
defectCount |  **Type:** integer<int32> The number of defective products. _Min value:_ `0`  
factCount |  **Type:** integer<int32> The number of items that are accepted in the warehouse. _Min value:_ `0`  
planCount |  **Type:** integer<int32> The number of items in the delivery request. _Min value:_ `0`  
shortageCount |  **Type:** integer<int32> The number of defective products. _Min value:_ `0`  
surplusCount |  **Type:** integer<int32> The number of extra items. _Min value:_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#currencyvaluedto)CurrencyValueDTO
Currency and its value.
**Name** |  **Description**  
---|---  
currencyId* |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#currencytype) Currency. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
value* |  **Type:** number Meaning.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
page_token:
limit:
Body{ "requestId": 0 }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Information about applications](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequests)
Next
[Application documents](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments)
