---
title: Competitive Position Report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateCompetitorsPositionReport
crawled_at: 2025-09-17T14:39:28.393751
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#reportformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Competitive Position Report
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/promotion)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of the "Competitive Position" report for the specified period. [What kind of report is this](https://yandex.ru/support2/marketplace/ru/analytics/competitors.html)
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
The -1 value in the report
If in the CSV file in the column **POSITION** it is -1, there were no orders for items in the specified category on that day.
Explanation of the report columns:
Sheet **Конкурентная позиция** (file **competitors_position**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DAY |  day |  День |  string  
SELLERS_COUNT |  sellersCount |  Продавцов в категории |  integer  
POSITION |  position |  Ваша позиция |  integer  
TOTAL_GMV |  totalGmv |  Общий оборот в категории, ₽ |  number  
GMV |  gmv |  Ваш оборот в категории, ₽ |  number  
AVG_TOTAL_GMV |  avgTotalGmv |  Средний оборот в категории, ₽ |  number  
SHARE |  share |  Ваша доля, % |  number  
AVG_GMV_OF_TOP_FIVE_PERCENT_SELLERS |  avgGmvOfTopFivePercentSellers |  Средний оборот 5% лидеров, ₽ |  number  
NEAREST_COMPETITOR_GMV |  nearestCompetitorGmv |  Оборот ближайшего конкурента, ₽ |  number  
**, Limit:** 10 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/competitors-position/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#reportformattype) The format of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body)Body
application/json
```
{
    "businessId": 0,
    "categoryId": 0,
    "dateFrom": "string",
    "dateTo": "string"
}

```

**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
categoryId* |  **Type:** integer<int64> The category ID.  
dateFrom* |  **Type:** string<date> The beginning of the period, inclusive.  
dateTo* |  **Type:** string<date> End of the period, inclusive.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "businessId": 0, "categoryId": 0, "dateFrom": "string", "dateTo": "string" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Report on key indicators](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport)
Next
[Report on non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedReturnsReport)
