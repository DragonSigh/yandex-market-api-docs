---
title: Warehouse balance report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateStocksOnWarehousesReport
crawled_at: 2025-09-17T14:36:25.017280
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#reportformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Warehouse balance report
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * all-methods — Full account management


Starts the generation of a report on inventory balances. [What kind of report is this](https://yandex.ru/support/marketplace/ru/storage/logistics#remains-history)
**What information will be returned:**
  * For the FBY model, if you specify `campaignId`- about the leftovers in the Market warehouses.
  * For other models, if you specify `campaignId`, — about the leftovers in the store's corresponding warehouse.
  * For other models, if you specify `businessId`— about the leftovers in all store warehouses in the cabinet, except for FBY. Use a filter `campaignIds` to specify specific stores.


, Do not transmit at the same time `campaignId` and `businessId`.
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
Market Warehouse
Store Warehouse
All store warehouses in the cabinet, except FBY
Explanation of the report columns:
Sheet **Остатки на складе** (file **stocks_on_warehouses**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
SHOP_SKU |  shopSku |  SSKU |  string  
ARTICLE |  article |  Ваш SKU |  string  
MARKET_SKU |  marketSku |  SKU на Яндексе |  integer  
PRODUCT_NAME |  productName |  Название товара |  string  
VALID |  valid |  Годный |  integer  
RESERVED |  reserved |  Резерв |  integer  
AVAILABLE_FOR_ORDER |  availableForOrder |  Доступно для заказа |  integer  
QUARANTINE |  quarantine |  Карантин |  integer  
UTILIZATION |  utilization |  Передан на утилизацию |  integer  
DEFECT |  defect |  Брак |  integer  
EXPIRED |  expired |  Просрочен |  integer  
LENGTH |  length |  Длина, см |  integer  
WIDTH |  width |  Ширина, см |  integer  
HEIGHT |  height |  Высота, см |  integer  
WEIGHT |  weight |  Вес, кг |  number  
WAREHOUSE |  warehouse |  Склад |  string  
SELLING_STATUS |  sellingStatus |  Статус продаж |  string  
RECOMMENDATIONS |  recommendations |  Рекомендации |  string  
Explanation of the report columns:
Sheet **Report** (file **mass_shared_stocks**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ERRORS |  errors |  log-message |  string  
WARNINGS |  warnings |  info-message |  string  
SHOP_SKU |  shopSku |  id |  string  
PRODUCT_NAME |  productName |  name |  string  
COUNT |  count |  count |  integer  
Explanation of the report columns:
Sheet **Report** (file **stocks_business**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ERRORS |  errors |  log-message |  string  
SHOP_SKU |  shopSku |  id |  string  
PRODUCT_NAME |  productName |  name |  string  
PLACEMENT_TYPE |  placementType |  placement_type |  string  
WAREHOUSE_AND_SHOP |  warehouseAndShop |  warehouse_and_shop |  string  
COUNT |  count |  count |  integer  
RESERVE |  reserve |  reserve |  integer  
PRICE |  price |  price |  string  
STATUS |  status |  status |  string  
COMMENT |  comment |  comment |  string  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/stocks-on-warehouses/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#reportformattype) The format of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body)Body
application/json
```
{
    "campaignId": 0,
    "businessId": 0,
    "warehouseIds": [
        0
    ],
    "reportDate": "string",
    "categoryIds": [
        0
    ],
    "hasStocks": false,
    "campaignIds": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
businessId |  **Type:** integer<int64> **Only for DBS, FBS and Express models** The ID of the cabinet for which the report should be generated (except for FBY stores). Do not transmit together with `campaignId`.  
campaignId |  **Type:** integer<int64> This parameter will soon become unavailable for the DBS, FBS, and Express models. To receive information about the store's stock balances, send `businessId` and the ID of the required store in `campaignIds`. The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports. Do not transmit together with `businessId`.  
campaignIds |  **Type:** integer<int64>[] Filter by stores for the cabinet report (except for the FBY model). Transmit along with `businessId`.   
The campaign list of those stores for which you need to get information. You can find them using a query. [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not use store IDs instead, which are listed in the seller's account on the Market next to the store name and in some reports. _Min items:_ `1` _Unique items_  
categoryIds |  **Type:** integer<int32>[] Filter by category on the Market (except for the FBY model).  
_Min value (exclusive):_ `0` _Min items:_ `1` _Unique items_  
hasStocks |  **Type:** boolean Filter by the presence of residues (except for the FBY model).  
reportDate |  **Type:** string<date> Filter by date (for the FBY model). The report will include data for **the previous one** Good afternoon.  
warehouseIds |  **Type:** integer<int64>[] Filter by warehouse IDs (FBY model only). To find out the ID, use the request [GET v2/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/warehouses/getFulfillmentWarehouses).  
_Min items:_ `1` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#200-ok)200 OK
An identifier is sent in response, which allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "reportId": "string",
        "estimatedGenerationTime": 0
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateStocksOnWarehousesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "campaignId": 0, "businessId": 0, "warehouseIds": [ 0 ], "reportDate": "string", "categoryIds": [ 0 ], "hasStocks": false, "campaignIds": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Turnover Report (FBY)](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsTurnoverReport)
Next
[Product Reviews Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsFeedbackReport)
