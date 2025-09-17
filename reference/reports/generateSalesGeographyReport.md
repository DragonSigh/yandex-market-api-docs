---
title: Sales Geography Report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateSalesGeographyReport
crawled_at: 2025-09-17T14:39:03.259697
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#reportformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Sales Geography Report
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of a report on the geography of sales. [What kind of report is this](https://yandex.ru/support/marketplace/ru/analytics/sales-geography)
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
Explanation of the report columns:
Sheet **География продаж** (file **sales_geography**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
OFFER_ID |  offerId |  Информация о товарах/Ваш SKU |  string  
OFFER_NAME |  offerName |  Информация о товарах/Название товара |  string  
CATEGORY |  category |  Информация о товарах/Категория |  string  
EXPENSES_ON_DELIVERY_IN_RUSSIA |  expensesOnDeliveryInRussia |  Доля локальных продаж и ваши расходы/Расходы на доставку по России |  number  
LOCAL_SALES |  localSales |  Доля локальных продаж и ваши расходы/Локальных продаж |  integer  
DELIVERED_ITEMS |  deliveredItems |  Доля локальных продаж и ваши расходы/Товаров доставлено |  integer  
CLUSTER_MOSCOW |  clusterMoscow |  Сколько товаров доставлено в конкретные кластеры/Москва |  integer  
CLUSTER_ROSTOV_ON_DON |  clusterRostovOnDon |  Сколько товаров доставлено в конкретные кластеры/Ростов-на-Дону |  integer  
CLUSTER_EKATERINBURG |  clusterEkaterinburg |  Сколько товаров доставлено в конкретные кластеры/Екатеринбург |  integer  
CLUSTER_SAINT_PETERSBURG |  clusterSaintPetersburg |  Сколько товаров доставлено в конкретные кластеры/Санкт-Петербург |  integer  
CLUSTER_SAMARA |  clusterSamara |  Сколько товаров доставлено в конкретные кластеры/Самара |  integer  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/sales-geography/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#reportformattype) The format of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body)Body
application/json
```
{
    "businessId": 0,
    "dateFrom": "string",
    "dateTo": "string",
    "categoryIds": [
        0
    ],
    "offerIds": [
        "string"
    ]
}

```

**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
dateFrom* |  **Type:** string<date> The beginning of the period, inclusive.  
dateTo* |  **Type:** string<date> End of the period, inclusive.  
categoryIds |  **Type:** integer<int32>[] Category IDs.  
_Min value (exclusive):_ `0` _Min items:_ `1` _Max items:_ `1000` _Unique items_  
offerIds |  **Type:** string[] Product IDs.  
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `1000` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateSalesGeographyReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "businessId": 0, "dateFrom": "string", "dateTo": "string", "categoryIds": [ 0 ], "offerIds": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Sales Boost Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateBoostConsolidatedReport)
Next
[Report on the movement of goods (FBY)](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsMovementReport)
