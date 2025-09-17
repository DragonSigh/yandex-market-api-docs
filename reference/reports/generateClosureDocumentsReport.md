---
title: Closing documents - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateClosureDocumentsReport
crawled_at: 2025-09-17T14:36:08.391019
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body)
    * [ClosureDocumentsMonthOfYearDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#closuredocumentsmonthofyeardto)
    * [ClosureDocumentsContractType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#closuredocumentscontracttype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body6)


# Closing documents
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns a ZIP archive with closing documents in PDF format for the specified month.
The composition of the documents depends on the type of contract
  * **Placement agreement**
    * _the act of rendered services_
    * _the invoice_
    * _summary report on statistics data_
    * _report on the execution of the assignment and on the settlement of mutual claims_ (agent's report)
  * **Promotion agreement** (not concluded in Russia after September 30, 2024)
    * _the act of rendering services_
    * _the invoice_ if the tax scheme requires it
  * **Marketing agreement**
    * _the act of rendered services_
    * _the invoice_
    * _advance payment invoice_
    * _personal account statement_
    * _details of the report_


You can find out the generation status and get a link to the archive using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/closure-documents/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body)Body
application/json
```
{
    "campaignId": 0,
    "monthOfYear": {
        "year": 2025,
        "month": 12
    },
    "contractTypes": [
        "INCOME"
    ]
}

```

**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.  
monthOfYear* |  **Type:** [ClosureDocumentsMonthOfYearDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#closuredocumentsmonthofyeardto) The month for which the closing documents are needed.  
contractTypes |  **Type:** [ClosureDocumentsContractType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#closuredocumentscontracttype)[] Types of contracts that require closing documents. If you do not specify them, the archive with documents for all found contracts will be returned.   
Type of agreement:
  * `INCOME` — the accommodation agreement.
  * `OUTCOME` — a promotion agreement.
  * `MARKETING` — a marketing contract.

_Enum:_ `INCOME`, `OUTCOME`, `MARKETING` _Min items:_ `1` _Max items:_ `3` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#closuredocumentsmonthofyeardto)ClosureDocumentsMonthOfYearDTO
Month and year.
**Name** |  **Description**  
---|---  
month* |  **Type:** integer<int32> The month number. _Example:_ `12` _Min value:_ `1` _Max value:_ `12`  
year* |  **Type:** integer<int32> Year. _Example:_ `2025`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#closuredocumentscontracttype)ClosureDocumentsContractType
Type of agreement:
  * `INCOME` — the accommodation agreement.
  * `OUTCOME` — a promotion agreement.
  * `MARKETING` — a marketing contract.

**Type** |  **Description**  
---|---  
[ClosureDocumentsContractType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#closuredocumentscontracttype) |  _Enum:_ `INCOME`, `OUTCOME`, `MARKETING`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#200-ok)200 OK
A ZIP archive with closing documents in PDF format.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Body{ "campaignId": 0, "monthOfYear": { "year": 2025, "month": 12 }, "contractTypes": [ "INCOME" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
It lists all the services that the Market has provided to the seller over the past month.  
  
Read more about the act in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/accounting/acts/main/act).
It lists all the services that the Market has provided to the seller over the past month.
This is a mandatory document regulated by a special Government decree.  
  
The invoice contains the same information as in the certificate of services rendered. It is more convenient to use an act for accounting and analysis.
This is a mandatory document regulated by a special Government decree.  
  
The invoice contains the same information as the service delivery certificate. It is more convenient to use an act for accounting and analysis.
The store's accountant needs a summary report to reflect the sale of goods in accounting.  
  
The report is compiled for stores operating under the FBY and FBS models. It indicates how many items and for what amount:
  * sent to customers;
  * delivered to customers;
  * The buyers did not buy back;
  * the buyers returned it.

The report is in the same PDF file as the certificate of services rendered.  
  
Read more about the report in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/accounting/acts/main/report).
The report shows how much money the Market has received from customers, how much it has already transferred to the seller, and how much it still owes.  
  
Read more about the report in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/accounting/acts/main/agent).
The act states:
  * the total amount of all discounts on products that the Market has provided to customers;
  * the total amount of all shipping discounts that the Market has provided to customers (only for the DBS model);
  * the total amount of payments in Plus points.


Shows the amount on the balance at the beginning of the month that the seller has not spent yet. The document is useful for an accountant.
Shows the seller's balance — expenses and the balance at the end of the month.
Shows the services provided by all the brands of the seller or advertiser. The details are useful for accounting purposes.
### Was the article helpful?
YesNo
Previous
[Detailed information on orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/stats/getOrdersStats)
Next
[Sales Analytics Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShowsSalesReport)
