---
title: Shelf Report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateShelfsStatisticsReport
crawled_at: 2025-09-17T14:39:54.026054
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#reportformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body)
    * [StatisticsAttributionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#statisticsattributiontype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Shelf Report
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/promotion)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of a summary report on shelves — advertising blocks with a banner or video and a set of products. Read more about them [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/marketing/shelf).
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
Explanation of the report columns:
Sheet **Общий отчет** (file **shelfs_statistics_summary**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
INCUT_ID |  incutId |  ID кампании |  integer  
TITLE |  title |  Название кампании |  string  
IMPRESSIONS |  impressions |  Показы, шт. |  integer  
COVERAGE |  coverage |  Охват, чел. |  integer  
CLICKS |  clicks |  Клики, шт. |  integer  
CTR |  ctr |  CTR, % |  number  
AVERAGE_IMPRESSION_FREQUENCY |  averageImpressionFrequency |  Частота показа |  number  
TO_CART |  toCart |  Добавления в корзину, шт. |  integer  
ORDERED |  ordered |  Заказанные товары, шт. |  integer  
CONVERSION |  conversion |  Конверсия в заказы, % |  number  
ORDERED_AMOUNT |  orderedAmount |  Стоимость заказанных товаров, ₽ |  number  
CPO |  cpo |  СРО, ₽ |  number  
COST |  cost |  Расчётные расходы, ₽ |  number  
CPM |  cpm |  CPM, ₽ |  number  
DRR |  drr |  Доля расчётных расходов от выручки с полкой |  number  
REAL_COST |  realCost |  Фактические расходы (с НДС), ₽ |  number  
DEDUCTED_BONUSES |  deductedBonuses |  Списано бонусов |  number  
Sheet **Таргетинг по категориям** (file **shelfs_statistics_by_category**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
INCUT_ID |  incutId |  ID кампании |  integer  
TITLE |  title |  Название кампании |  string  
SHOW_CATEGORY_NAME |  showCategoryName |  Категория показа полки |  string  
IMPRESSIONS |  impressions |  Показы, шт. |  integer  
COVERAGE |  coverage |  Охват, чел. |  integer  
CLICKS |  clicks |  Клики, шт. |  integer  
CTR |  ctr |  CTR, % |  number  
AVERAGE_IMPRESSION_FREQUENCY |  averageImpressionFrequency |  Частота показа |  number  
TO_CART |  toCart |  Добавления в корзину, шт. |  integer  
ORDERED |  ordered |  Заказанные товары, шт. |  integer  
CONVERSION |  conversion |  Конверсия в заказы, % |  number  
ORDERED_AMOUNT |  orderedAmount |  Стоимость заказанных товаров, ₽ |  number  
CPO |  cpo |  СРО, ₽ |  number  
COST |  cost |  Расчётные расходы, ₽ |  number  
CPM |  cpm |  CPM, ₽ |  number  
DRR |  drr |  Доля расчётных расходов от выручки с полкой |  number  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/shelf-statistics/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#reportformattype) The format of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body)Body
application/json
```
{
    "businessId": 0,
    "dateFrom": "string",
    "dateTo": "string",
    "attributionType": "CLICKS"
}

```

**Name** |  **Description**  
---|---  
attributionType* |  **Type:** [StatisticsAttributionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#statisticsattributiontype) The type of attribution. _Enum:_ `CLICKS`, `SHOWS`  
businessId* |  **Type:** integer<int64> Cabinet ID.  
dateFrom* |  **Type:** string<date> The beginning of the period, inclusive.  
dateTo* |  **Type:** string<date> End of the period, inclusive.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#statisticsattributiontype)StatisticsAttributionType
Attribution type:
  * `CLICKS` — by clicks.
  * `SHOWS` — according to the impressions.   
  



For information about which data in the report depends and does not depend on the type of attribution, read [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/marketing/shelf#stats).
**Type** |  **Description**  
---|---  
[StatisticsAttributionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#statisticsattributiontype) |  _Enum:_ `CLICKS`, `SHOWS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "businessId": 0, "dateFrom": "string", "dateTo": "string", "attributionType": "CLICKS" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Payment Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport)
Next
[Implementation Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport)
