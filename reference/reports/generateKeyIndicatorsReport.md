---
title: Report on key indicators - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateKeyIndicatorsReport
crawled_at: 2025-09-17T14:39:22.338726
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#reportformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body)
    * [KeyIndicatorsReportDetalizationLevelType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#keyindicatorsreportdetalizationleveltype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Report on key indicators
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/promotion)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of a report on key indicators. [What kind of report is this](https://yandex.ru/support/marketplace/ru/analytics/key-metrics)
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
Explanation of the report columns:
Sheet **Основные** (file **key_indicators_summary**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
PERIOD |  period |  Период |  string  
GMV |  gmv |  Выручка, ₽ |  number  
ORDERS_DELIVERED |  ordersDelivered |  Доставленные заказы, шт. |  integer  
ORDERS_AVG_PRICE |  ordersAvgPrice |  Средний чек заказа, ₽ |  number  
TOTAL_SUBSIDY |  totalSubsidy |  Все платежи за скидки, ₽ |  number  
SERVICES_WITHOUT_PROMOTION |  servicesWithoutPromotion |  Стоимость всех услуг Маркета без продвижения, ₽ |  number  
PROMOTION_SERVICES |  promotionServices |  Стоимость услуг продвижения, ₽ |  number  
Sheet **Выручка** (file **key_indicators_revenue**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
PERIOD |  period |  Период |  string  
GMV |  gmv |  Выручка, ₽ |  number  
TOTAL_SUBSIDY |  totalSubsidy |  Все платежи за скидки, ₽ |  number  
YANDEX_PLUS |  yandexPlus |  Платежи за скидки по баллам Яндекс Плюса, ₽ |  number  
SUBSIDY |  subsidy |  Платежи за скидки маркетплейса, ₽ |  number  
Sheet **Показатели продаж** (file **key_indicators_sales**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
PERIOD |  period |  Период |  string  
SHOWS |  shows |  Показы товаров |  integer  
TO_CART_CONVERSION |  toCartConversion |  Конверсия добавления в корзину, % |  number  
TO_ORDER_CONVERSION |  toOrderConversion |  Конверсия из корзины в заказ, % |  number  
ORDERS_DELIVERED |  ordersDelivered |  Доставленные заказы, шт. |  integer  
GMV |  gmv |  Выручка, ₽ |  number  
ORDERS_AVG_PRICE |  ordersAvgPrice |  Средний чек заказа, ₽ |  number  
ORDER_ITEMS_DELIVERED |  orderItemsDelivered |  Доставленные товары, шт |  integer  
ORDER_ITEM_AVG_PRICE |  orderItemAvgPrice |  Средняя стоимость доставленного товара, ₽ |  number  
Sheet **Расходы** (file **key_indicators_expenses**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
PERIOD |  period |  Период |  string  
SERVICES_WITHOUT_PROMOTION |  servicesWithoutPromotion |  Стоимость всех услуг Маркета без продвижения, ₽ |  number  
FEE |  fee |  Стоимость размещения товаров на витрине, ₽ |  number  
PAYMENT_ACCEPTANCE_AND_TRANSFER |  paymentAcceptanceAndTransfer |  Приём и перевод платежа покупателя, ₽ |  number  
LOGISTIC_SERVICES |  logisticServices |  Стоимость услуг логистики, ₽ |  number  
WAREHOUSE_SERVICES |  warehouseServices |  Стоимость услуг склада, ₽ |  number  
PROMOTION_SERVICES |  promotionServices |  Стоимость услуг продвижения, ₽ |  number  
BOOST |  boost |  Расходы на буст продаж, ₽ |  number  
PROMOTION_WITH_SHOWS |  promotionWithShows |  Расходы на продвижение с оплатой за показы, ₽ |  number  
LOYALTY_PARTICIPATION_FEE |  loyaltyParticipationFee |  Участие в программе лояльности и отзывы, ₽ |  number  
EXTENDED_ACCESS_PAYMENT |  extendedAccessPayment |  Расширенный доступ к сервисам Маркетплейса, ₽ |  number  
Sheet **Все** (file **key_indicators_full**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
PERIOD |  period |  Период |  string  
SHOWS |  shows |  Показы товаров |  integer  
TO_CART_CONVERSION |  toCartConversion |  Конверсия добавления в корзину, % |  number  
TO_ORDER_CONVERSION |  toOrderConversion |  Конверсия из корзины в заказ, % |  number  
ORDERS_DELIVERED |  ordersDelivered |  Доставленные заказы, шт. |  integer  
GMV |  gmv |  Выручка, ₽ |  number  
ORDERS_AVG_PRICE |  ordersAvgPrice |  Средний чек заказа, ₽ |  number  
ORDER_ITEMS_DELIVERED |  orderItemsDelivered |  Доставленные товары, шт |  integer  
ORDER_ITEM_AVG_PRICE |  orderItemAvgPrice |  Средняя стоимость доставленного товара, ₽ |  number  
TOTAL_SUBSIDY |  totalSubsidy |  Все платежи за скидки, ₽ |  number  
YANDEX_PLUS |  yandexPlus |  Платежи за скидки по баллам Яндекс Плюса, ₽ |  number  
SUBSIDY |  subsidy |  Платежи за скидки маркетплейса, ₽ |  number  
SERVICES_WITHOUT_PROMOTION |  servicesWithoutPromotion |  Стоимость всех услуг Маркета без продвижения, ₽ |  number  
FEE |  fee |  Стоимость размещения товаров на витрине, ₽ |  number  
PAYMENT_ACCEPTANCE_AND_TRANSFER |  paymentAcceptanceAndTransfer |  Приём и перевод платежа покупателя, ₽ |  number  
LOGISTIC_SERVICES |  logisticServices |  Стоимость услуг логистики, ₽ |  number  
WAREHOUSE_SERVICES |  warehouseServices |  Стоимость услуг склада, ₽ |  number  
PROMOTION_SERVICES |  promotionServices |  Стоимость услуг продвижения, ₽ |  number  
BOOST |  boost |  Расходы на буст продаж, ₽ |  number  
PROMOTION_WITH_SHOWS |  promotionWithShows |  Расходы на продвижение с оплатой за показы, ₽ |  number  
LOYALTY_PARTICIPATION_FEE |  loyaltyParticipationFee |  Участие в программе лояльности и отзывы, ₽ |  number  
EXTENDED_ACCESS_PAYMENT |  extendedAccessPayment |  Расширенный доступ к сервисам Маркетплейса, ₽ |  number  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/key-indicators/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#reportformattype) The format of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body)Body
application/json
```
{
    "businessId": 0,
    "campaignId": 0,
    "detalizationLevel": "WEEK"
}

```

**Name** |  **Description**  
---|---  
detalizationLevel* |  **Type:** [KeyIndicatorsReportDetalizationLevelType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#keyindicatorsreportdetalizationleveltype) For which period the details are needed. _Enum:_ `WEEK`, `MONTH`  
businessId |  **Type:** integer<int64> Cabinet ID. It is indicated if you need to create a report on all stores in the cabinet. The request must contain either `businessId`, or `campaignId` but not both at once.  
campaignId |  **Type:** integer<int64> The campaign ID. It is indicated if you need to create a report on a specific store. The request must contain either `businessId`, or `campaignId` but not both at once. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#keyindicatorsreportdetalizationleveltype)KeyIndicatorsReportDetalizationLevelType
For which period the details are needed:
  * `WEEK` — by the week.
  * `MONTH` — by month.

**Type** |  **Description**  
---|---  
[KeyIndicatorsReportDetalizationLevelType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#keyindicatorsreportdetalizationleveltype) |  _Enum:_ `WEEK`, `MONTH`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateKeyIndicatorsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "businessId": 0, "campaignId": 0, "detalizationLevel": "WEEK" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Jewelry Order Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateJewelryFiscalReport)
Next
[Competitive Position Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateCompetitorsPositionReport)
