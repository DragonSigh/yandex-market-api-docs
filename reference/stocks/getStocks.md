---
title: Viewing balances and turnover - Balances and turnover | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/getStocks
crawled_at: 2025-09-17T14:30:14.578995
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body1)
    * [GetWarehouseStocksDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#getwarehousestocksdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype)
    * [WarehouseOffersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehouseoffersdto)
    * [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#scrollingpagerdto)
    * [WarehouseOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehouseofferdto)
    * [WarehouseStockDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehousestockdto)
    * [TurnoverDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#turnoverdto)
    * [WarehouseStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehousestocktype)
    * [TurnoverType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#turnovertype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body6)


# Information about balances and turnover
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns data on the remaining items (for all models) and about _turnover_ products (for the FBY model).
By default, the turnover data is not returned.
To have them in the response, send `true` in the field `withTurnover`.
**For the FBY model:** information about balances can be returned from several Market warehouses, which will have different `warehouseId`. To get a list of Market warehouses, use the method [GET v2/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/warehouses/getFulfillmentWarehouses).
Restriction for the parameter `limit`
Do not pass a value greater than 200.
**, Limit:** 100,000 products per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offers/stocks

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body)Body
application/json
```
{
    "stocksWarehouseId": 0,
    "hasStocks": false,
    "withTurnover": false,
    "archived": false,
    "offerIds": [
        "string"
    ]
}

```

**Name** |  **Description**  
---|---  
archived |  **Type:** boolean Filter by location in the archive. Pass it on `true` to get information about the remaining items that are archived. If the filter is not filled or passed `false` the response returns information about products that are not archived.  
hasStocks |  **Type:** boolean Filter by product availability. Use only together with `stocksWarehouseId`. Pass it on `false` to get information about products that are not available. With the value `true` The data about the goods that are in the specified warehouse is returned.  
offerIds |  **Type:** string[] Filter by your product SKUs. Information is returned about the balances of all transferred SKUs, including the items in the archive. This list is returned only in its entirety. If you are requesting information on specific SKUs, do not fill in:
  * `page_token`
  * `limit`
  * `archived`
  * `stocksOnWarehouse`

  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `500` _Unique items_  
stocksWarehouseId |  **Type:** integer<int64> The warehouse ID. If the parameter is specified, only the goods in the transferred warehouse are returned. **For the FBY model:** to get a list of Market warehouses, use the method [GET v2/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/warehouses/getFulfillmentWarehouses). _Min value:_ `1`  
withTurnover |  **Type:** boolean **Only for the FBY model** Whether to return the turnover information. Default value: `false`. If the information is needed, pass the value `true`. _Default:_ `false`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#200-ok)200 OK
Remnants of goods in warehouses.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "paging": {
            "nextPageToken": "string",
            "prevPageToken": "string"
        },
        "warehouses": [
            {
                "warehouseId": 0,
                "offers": [
                    {
                        "offerId": "string",
                        "turnoverSummary": {
                            "turnover": "LOW",
                            "turnoverDays": 0
                        },
                        "stocks": [
                            {
                                "type": "FIT",
                                "count": 0
                            }
                        ],
                        "updatedAt": "2022-12-29T18:02:01Z"
                    }
                ]
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GetWarehouseStocksDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#getwarehousestocksdto) A list of warehouses with information about the balances on each of them.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#getwarehousestocksdto)GetWarehouseStocksDTO
A list of warehouses with information about the balances on each of them.
**Name** |  **Description**  
---|---  
warehouses* |  **Type:** [WarehouseOffersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehouseoffersdto)[] The warehouse list page.  
Information about the remaining goods in the warehouse.  
paging |  **Type:** [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#scrollingpagerdto) Information about the result pages.  
The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehouseoffersdto)WarehouseOffersDTO
Information about the remaining goods in the warehouse.
**Name** |  **Description**  
---|---  
offers* |  **Type:** [WarehouseOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehouseofferdto)[] Information about balances.  
Information about the remaining goods.  
warehouseId* |  **Type:** integer<int64> The warehouse ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#scrollingpagerdto)ScrollingPagerDTO
Information about the result pages.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
prevPageToken |  **Type:** string ID of the previous results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehouseofferdto)WarehouseOfferDTO
Information about the remaining goods.
**Name** |  **Description**  
---|---  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
stocks* |  **Type:** [WarehouseStockDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehousestockdto)[] Information about balances.  
Information about the remaining goods.  
turnoverSummary |  **Type:** [TurnoverDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#turnoverdto) Information about turnover.  
updatedAt |  **Type:** string<date-time> The date and time of the last update of the balance information. Date and time format: ISO 8601 with an offset relative to UTC. For example, `2023-11-21T00:42:42+03:00`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehousestockdto)WarehouseStockDTO
Information about the remaining goods.
**Name** |  **Description**  
---|---  
count* |  **Type:** integer<int64> The value of the leftovers.  
type* |  **Type:** [WarehouseStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehousestocktype) The type of leftovers. _Enum:_ `FIT`, `FREEZE`, `AVAILABLE`, `QUARANTINE`, `UTILIZATION`, `DEFECT`, `EXPIRED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#turnoverdto)TurnoverDTO
Information about the turnover of the product.
Read more about the storage and turnover of goods in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/storage/logistics#turnover).
**Name** |  **Description**  
---|---  
turnover* |  **Type:** [TurnoverType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#turnovertype) Evaluation of turnover. _Enum:_ `LOW`, `ALMOST_LOW`, `HIGH`, `VERY_HIGH`, `NO_SALES`, `FREE_STORE`  
turnoverDays |  **Type:** number<double> The value is in days.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehousestocktype)WarehouseStockType
The type of remaining goods in the warehouse:
  * `AVAILABLE` (corresponds to the "Available to order" type in the "Stock balances" report in the seller's office on the Market) — an item available for sale.
  * `DEFECT` (corresponds to the "Marriage" type) — a defective product.
  * `EXPIRED` (corresponds to the "Expired" type) — an expired product.
  * `FIT` (corresponds to the "Fit" type) — an item that is available for sale or has already been reserved.
  * `FREEZE` — the product that is reserved for orders.
  * `QUARANTINE` (corresponds to the "Quarantine" type) — a product that is temporarily unavailable for sale (for example, the product is being moved from one warehouse to another).
  * `UTILIZATION` — the product that will be disposed of.

**Type** |  **Description**  
---|---  
[WarehouseStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#warehousestocktype) |  _Enum:_ `FIT`, `FREEZE`, `AVAILABLE`, `QUARANTINE`, `UTILIZATION`, `DEFECT`, `EXPIRED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#turnovertype)TurnoverType
Evaluation of turnover.
enum | Turnover range | Comment  
---|---|---  
`LOW` |  `turnoverDays` ≥ 120 |   
`ALMOST_LOW` | 100 ≤ `turnoverDays` < 120 |   
`HIGH` | 45 ≤ `turnoverDays` < 100 |   
`VERY_HIGH` | 0 ≤ `turnoverDays` < 45 |   
`NO_SALES` | — | There are no sales.  
`FREE_STORE` | Any value. | There is no need to pay for the storage of goods in this category.  
**Type** |  **Description**  
---|---  
[TurnoverType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#turnovertype) |  _Enum:_ `LOW`, `ALMOST_LOW`, `HIGH`, `VERY_HIGH`, `NO_SALES`, `FREE_STORE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/getStocks#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
page_token:
limit:
Body{ "stocksWarehouseId": 0, "hasStocks": false, "withTurnover": false, "archived": false, "offerIds": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
The average number of days for which the product is sold. Detailed information about turnover is provided [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/analytics/turnover.html).
### Was the article helpful?
YesNo
Previous
[Deleting from the archive](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/business-assortment/deleteOffersFromArchive)
Next
[Transfer of leftovers](https://yandex.ru/dev/market/partner-api/doc/en/reference/stocks/en/reference/stocks/updateStocks)
