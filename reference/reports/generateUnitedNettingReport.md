---
title: Payment Report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateUnitedNettingReport
crawled_at: 2025-09-17T14:39:47.984959
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#reportformattype)
    * [ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#reportlanguagetype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body)
    * [MonthOfYearDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#monthofyeardto)
    * [PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#placementtype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may change.
# Payment Report
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of the payment report for the specified period. [What kind of report is this](https://yandex.ru/support/marketplace/ru/accounting/transactions#all-pay)
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
The type of report depends on which fields are filled in in the request:
**Report type** |  **What fields are needed?**  
---|---  
About payments for the period |  `dateFrom` and `dateTo`  
About the payment order |  `bankOrderId` and `bankOrderDateTime`  
_About Yandex.Market points_ |  `monthOfYear`  
You cannot order multiple types of reports with a single request.
Explanation of the report columns:
Sheet **Payment report** (file **transaction_date**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Order number |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/Order creation date |  string  
ORDER_DELIVERY_DATE |  orderDeliveryDate |  Payment information/Order delivery date |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
SHOP_SKU |  shopSku |  Payment information/Your SKU |  string  
ACT_ID |  actId |  Payment information/Certificate of services rendered number |  integer  
ACT_DATE |  actDate |  Payment information/Date of the сertificate of services rendered |  string  
OFFER_OR_SERVICE_NAME |  offerOrServiceName |  Payment information/Product name (for accrual) or service (for withholding) |  string  
COUNT |  count |  Payment information/Quantity |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BONUS_ACCOUNT_YEAR_MONTH |  bonusAccountYearMonth |  Payment information/The billing period of the bonus for participation in joint promotions |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_SUM |  bankSum |  Payment information/Payment order amount or the amount withheld for services |  number  
COMMENTS |  comments |  Payment information/Comments |  string  
Sheet **Payment order report** (file **netting_report_accruals**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Information about accruals/Order number |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Information about accruals/Order creation date |  string  
ORDER_DELIVERY_DATE |  orderDeliveryDate |  Information about accruals/Order delivery date |  string  
CLAIM_NUMBER |  claimNumber |  Information about accruals/Claim number and date |  string  
ORDER_TYPE |  orderType |  Information about accruals/Order type |  string  
SHOP_SKU |  shopSku |  Information about accruals/Your SKU |  string  
OFFER_NAME |  offerName |  Information about accruals/Product name |  string  
COUNT |  count |  Information about accruals/Quantity |  integer  
TRANSACTION_SUM |  transactionSum |  Information about accruals/Transaction amount |  number  
TRANSACTION_SOURCE |  transactionSource |  Information about accruals/Transaction source |  string  
ACT_ID |  actId |  Information about accruals/Certificate of services rendered number |  integer  
ACT_DATE |  actDate |  Information about accruals/Date of the сertificate of services rendered |  string  
TRANSACTION_DATE |  transactionDate |  Information about accruals/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Information about accruals/Transaction ID |  string  
Sheet **Payment order report** (file **netting_report_returns_and_compensations**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Information about buyer refunds and compensation/Order number |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Information about buyer refunds and compensation/Creation date |  string  
ORDER_DELIVERY_DATE |  orderDeliveryDate |  Information about buyer refunds and compensation/Order delivery date |  string  
ORDER_TYPE |  orderType |  Information about buyer refunds and compensation/Order type |  string  
SHOP_SKU |  shopSku |  Information about buyer refunds and compensation/Your SKU |  string  
OFFER_NAME |  offerName |  Information about buyer refunds and compensation/Product name |  string  
COUNT |  count |  Information about buyer refunds and compensation/Quantity |  integer  
TRANSACTION_SUM |  transactionSum |  Information about buyer refunds and compensation/Transaction amount |  number  
TRANSACTION_SOURCE |  transactionSource |  Information about buyer refunds and compensation/Transaction source |  string  
TRANSACTION_DATE |  transactionDate |  Information about buyer refunds and compensation/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Information about buyer refunds and compensation/Transaction ID |  string  
Sheet **Payment order report** (file **netting_report_retentions**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ACT_ID |  actId |  Information about withheld amounts/Certificate of services rendered number |  integer  
ACT_DATE |  actDate |  Information about withheld amounts/Date of the сertificate of services rendered |  string  
SERVICE_NAME |  serviceName |  Information about withheld amounts/Name of service to be withheld |  string  
TRANSACTION_SUM |  transactionSum |  Information about withheld amounts/Transaction amount |  number  
TRANSACTION_SOURCE |  transactionSource |  Information about withheld amounts/Transaction source |  string  
TRANSACTION_DATE |  transactionDate |  Information about withheld amounts/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Information about withheld amounts/Transaction ID |  string  
Sheet **Bonuses report** (file **netting_bonuses**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
ORDER_ID |  orderId |  Payment information/Order number |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/Order creation date |  string  
ORDER_DELIVERY_DATE |  orderDeliveryDate |  Payment information/Order delivery date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
SHOP_SKU |  shopSku |  Payment information/Your SKU |  string  
OFFER_OR_SERVICE_NAME |  offerOrServiceName |  Payment information/Product name (for accrual) or service (for withholding) |  string  
COUNT |  count |  Payment information/Quantity |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
COMMENTS |  comments |  Payment information/Comments |  string  
BONUS_ACCOUNT_YEAR_MONTH |  bonusAccountYearMonth |  Payment information/The month of the premium formation for participation in joint promotions |  string  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/united-netting/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#reportformattype) The format of the report or document.  
language |  **Type:** [ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#reportlanguagetype) The language of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#reportlanguagetype)ReportLanguageType
Language of the report:
  * `RU` — Russian language.
  * `EN` — English language.

**Type** |  **Description**  
---|---  
[ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#reportlanguagetype) |  _Enum:_ `RU`, `EN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body)Body
application/json
```
{
    "businessId": 0,
    "dateTimeFrom": "2022-12-29T18:02:01Z",
    "dateTimeTo": "2022-12-29T18:02:01Z",
    "dateFrom": "string",
    "dateTo": "string",
    "bankOrderId": 0,
    "bankOrderDateTime": "2022-12-29T18:02:01Z",
    "monthOfYear": {
        "year": 2025,
        "month": 12
    },
    "placementPrograms": [
        "FBS"
    ],
    "inns": [
        "string"
    ],
    "campaignIds": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
bankOrderDateTime |  **Type:** string<date-time> The date of the payment order.  
bankOrderId |  **Type:** integer<int64> The number of the payment order.  
campaignIds |  **Type:** integer<int64>[] The list of campaign IDs of those stores that are needed in the report. You can find them using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not use store IDs instead, which are listed in the seller's account on the Market next to the store name and in some reports.   
_Min items:_ `1` _Unique items_  
dateFrom |  **Type:** string<date> The beginning of the period, inclusive.  
dateTimeFrom ⦸ |  **Type:** string<date-time> The beginning of the period, inclusive.  
dateTimeTo ⦸ |  **Type:** string<date-time> End of the period, inclusive. The maximum period is 3 months.  
dateTo |  **Type:** string<date> End of the period, inclusive. The maximum period is 3 months.  
inns |  **Type:** string[] The list of INN's that are needed in the report.  
_Min items:_ `1` _Unique items_  
monthOfYear |  **Type:** [MonthOfYearDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#monthofyeardto) The month for which the report on the Market points is needed.  
placementPrograms |  **Type:** [PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#placementtype)[] The list of models that are needed in the report.   
The model that the store uses:
  * `FBS` — FBS or Express.
  * `FBY` — FBY.
  * `DBS` — DBS.

_Enum:_ `FBS`, `FBY`, `DBS`, `LAAS` _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#monthofyeardto)MonthOfYearDTO
The month for which the report on the Market points is needed.
**Name** |  **Description**  
---|---  
month* |  **Type:** integer<int32> The month number. _Example:_ `12` _Min value:_ `1` _Max value:_ `12`  
year* |  **Type:** integer<int32> Year. _Example:_ `2025`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#placementtype)PlacementType
The model that the store uses:
  * `FBS` — FBS or Express.
  * `FBY` — FBY.
  * `DBS` — DBS.

**Type** |  **Description**  
---|---  
[PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#placementtype) |  _Enum:_ `FBS`, `FBY`, `DBS`, `LAAS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedNettingReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
language:
Body{ "businessId": 0, "dateTimeFrom": "2022-12-29T18:02:01Z", "dateTimeTo": "2022-12-29T18:02:01Z", "dateFrom": "string", "dateTo": "string", "bankOrderId": 0, "bankOrderDateTime": "2022-12-29T18:02:01Z", "monthOfYear": { "year": 2025, "month": 12 }, "placementPrograms": [ "FBS" ], "inns": [ "string" ], "campaignIds": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
Read about what it is in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/accounting/market-points).
### Was the article helpful?
YesNo
Previous
[Coverage Promotion Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateBannersStatisticsReport)
Next
[Shelf Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport)
