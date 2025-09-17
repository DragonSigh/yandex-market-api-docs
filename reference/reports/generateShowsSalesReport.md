---
title: Sales Analytics Report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateShowsSalesReport
crawled_at: 2025-09-17T14:38:43.328725
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#reportformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body)
    * [ShowsSalesGroupingType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#showssalesgroupingtype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Sales Analytics Report
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of the Sales Analytics report for the specified period. [What kind of report is this](https://yandex.ru/support/marketplace/analytics/shows-sales.html)
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
Explanation of the report columns:
Sheet **Аналитика продаж** (file **sales_funnel_report**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DAY |  day |  День |  string  
MONTH |  month |  Месяц |  string  
YEAR |  year |  Год |  integer  
CATEGORY_NAME |  categoryName |  Категория |  string  
BRAND_NAME |  brandName |  Бренд |  string  
OFFER_ID |  offerId |  Ваш SKU |  string  
OFFER_NAME |  offerName |  Название товара |  string  
BY_MSKU_SHOWS |  byMskuShows |  Показы товаров всех продавцов, шт. |  integer  
VISIBILITY_INDEX |  visibilityIndex |  Индекс видимости, % |  string  
SHOWS |  shows |  Показы моих товаров, шт. |  integer  
SHOWS_WITH_PROMOTION |  showsWithPromotion |  Показы моих товаров с акциями, шт. |  integer  
SHOWS_SHARE |  showsShare |  Доля показов с бустом, % |  number  
CLICKS |  clicks |  Клики по товарам, шт. |  integer  
CLICKS_WITH_PROMOTION |  clicksWithPromotion |  Клики по товарам с акциями, шт. |  integer  
TO_CART_CONVERSION |  toCartConversion |  Конверсия из показа в корзину, % |  number  
TO_CART |  toCart |  Добавления в корзину, шт. |  integer  
TO_CART_WITH_PROMOTION |  toCartWithPromotion |  Добавления в корзину по акциям, шт. |  integer  
TO_CART_SHARE |  toCartShare |  Доля добавлений товаров с бустом в корзину, % |  number  
ORDER_ITEMS |  orderItems |  Заказанные товары, шт. |  integer  
ORDER_ITEMS_WITH_PROMOTION |  orderItemsWithPromotion |  Заказанные товары по акциям, шт. |  integer  
ORDER_ITEMS_TOTAL_AMOUNT |  orderItemsTotalAmount |  Заказано товаров на сумму, ₽ |  integer  
ORDER_ITEMS_TOTAL_AMOUNT_WITH_PROMOTION |  orderItemsTotalAmountWithPromotion |  Заказано товаров с акциями на сумму, ₽ |  integer  
TO_ORDER_CONVERSION |  toOrderConversion |  Конверсия из корзины в заказ, % |  number  
ORDER_ITEMS_SHARE |  orderItemsShare |  Доля заказанных товаров с бустом, % |  number  
ORDER_ITEMS_DELIVERED_COUNT |  orderItemsDeliveredCount |  Доставлено за период, шт. |  integer  
ORDER_ITEMS_DELIVERED_COUNT_WITH_PROMOTION |  orderItemsDeliveredCountWithPromotion |  Доставлено за период по акциям, шт. |  string  
ORDER_ITEMS_DELIVERED_TOTAL_AMOUNT |  orderItemsDeliveredTotalAmount |  Доставлено за период на сумму, ₽ |  integer  
ORDER_ITEMS_DELIVERED_TOTAL_AMOUNT_WITH_PROMOTION |  orderItemsDeliveredTotalAmountWithPromotion |  Доставлено за период по акциям на сумму, ₽ |  integer  
ORDER_ITEMS_DELIVERED_FROM_ORDERED_COUNT |  orderItemsDeliveredFromOrderedCount |  Доставлено из заказанных за период, шт. |  integer  
ORDER_ITEMS_DELIVERED_FROM_ORDERED_TOTAL_AMOUNT |  orderItemsDeliveredFromOrderedTotalAmount |  Доставлено из заказанных на сумму за период, ₽ |  integer  
ORDER_ITEMS_DELIVERED_FROM_ORDERED_TOTAL_AMOUNT_WITH_PROMOTION |  orderItemsDeliveredFromOrderedTotalAmountWithPromotion |  Доставлено из заказанных на сумму за период по акциям, ₽ |  integer  
ORDER_ITEMS_CANCELED_COUNT |  orderItemsCanceledCount |  Отмены и невыкупы, шт. |  integer  
ORDER_ITEMS_RETURNED_COUNT |  orderItemsReturnedCount |  Возвращённые товары, шт. |  integer  
**, Limit:** 10 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/shows-sales/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#reportformattype) The format of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body)Body
application/json
```
{
    "businessId": 0,
    "campaignId": 0,
    "dateFrom": "string",
    "dateTo": "string",
    "grouping": "CATEGORIES"
}

```

**Name** |  **Description**  
---|---  
dateFrom* |  **Type:** string<date> The beginning of the period, inclusive.  
dateTo* |  **Type:** string<date> End of the period, inclusive.  
grouping* |  **Type:** [ShowsSalesGroupingType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#showssalesgroupingtype) Grouping of report data. _Enum:_ `CATEGORIES`, `OFFERS`  
businessId |  **Type:** integer<int64> Cabinet ID. It is indicated if you need to create a report on all stores in the cabinet. The request must contain either `businessId`, or `campaignId` but not both at once.  
campaignId |  **Type:** integer<int64> The campaign ID. It is indicated if you need to create a report on a specific store. The request must contain either `businessId`, or `campaignId` but not both at once. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#showssalesgroupingtype)ShowsSalesGroupingType
Grouping of report data. Possible values:
  * `CATEGORIES` — grouping by category.
  * `OFFERS` — grouping by product.

**Type** |  **Description**  
---|---  
[ShowsSalesGroupingType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#showssalesgroupingtype) |  _Enum:_ `CATEGORIES`, `OFFERS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "businessId": 0, "campaignId": 0, "dateFrom": "string", "dateTo": "string", "grouping": "CATEGORIES" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Closing documents](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport)
Next
[Impression Boost Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsBoostReport)
