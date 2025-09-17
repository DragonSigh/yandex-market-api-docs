---
title: Ready-made labels for multiple orders - FBS and DBS shortcuts | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/generateMassOrderLabelsReport
crawled_at: 2025-09-17T14:33:42.805183
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#query-parameters)
    * [PageFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#pageformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body)
    * [LabelsSortingType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#labelssortingtype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body6)


# Ready‑made labels-stickers for all boxes in several orders
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Starts the generation of a PDF file with shortcuts for transferred orders. Details about why they are needed and what they look like are described [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/orders/fbs/packaging/marking.html).
You can find out the generation status and get a link to the finished file using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/reports/getReportInfo).
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/documents/labels/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [PageFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#pageformattype) Setting up the placement of shortcuts on the page. If there is no parameter, a PDF with labels in A7 format is returned.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#pageformattype)PageFormatType
Placement of labels on the PDF file page:
  * `A9_HORIZONTALLY` — a 58 ×40 mm borderless label, close to the A9 format.
An example of a label for Market sellers
![An image of a horizontal label in A9 format for Market sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A9-horizontally.png)
An example of a shortcut for Market Yandex Go sellers
![An image of a horizontal label in A9 format for Market Yandex Go sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A9-horizontally-uz.png)
  * `A9` — the label is 40x58 mm in size without margins, close to the A9 format.
An example of a label for Market sellers
![An image of a vertical label in A9 format for Market sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A9.png)
An example of a shortcut for Market Yandex Go sellers
![An image of an A9 vertical label for Market Yandex Go sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A9-uz.png)
  * `A7` — the label is 75 × 120 mm (80.4 × 125.6 mm including margins), close to the A7 format.
An example of a label for Market sellers
![An image of an A7 format label for Market sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A7.jpg)
An example of a shortcut for Market Yandex Go sellers
![An image of an A7 format label for Market Yandex Go sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A7-uz.png)
  * `A4` — on the A4 sheet there is a label of the format that is selected in the seller's office on the Market — go to the page **Orders** → **Orders and shipments** → on the tab of the desired work model, click **Label format**.

**Type** |  **Description**  
---|---  
[PageFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#pageformattype) |  _Enum:_ `A9_HORIZONTALLY`, `A9`, `A7`, `A4`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body)Body
application/json
```
{
    "businessId": 0,
    "orderIds": [
        0
    ],
    "sortingType": "SORT_BY_GIVEN_ORDER"
}

```

**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
orderIds* |  **Type:** integer<int64>[] List of order IDs.  
The order ID. _Min items:_ `1` _Max items:_ `1000` _Unique items_  
sortingType |  **Type:** [LabelsSortingType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#labelssortingtype) The type of sorting shortcuts in the file. _Enum:_ `SORT_BY_GIVEN_ORDER`, `SORT_BY_ORDER_CREATED_AT`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#labelssortingtype)LabelsSortingType
Label sorting type:
  * `SORT_BY_GIVEN_ORDER` — The order labels will be arranged in the same order as the order IDs were transmitted in the request.
  * `SORT_BY_ORDER_CREATED_AT` — The labels will be arranged according to the date the order was created and grouped by stores.


If no parameter is specified, the labels are sorted by creation date.
**Type** |  **Description**  
---|---  
[LabelsSortingType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#labelssortingtype) |  _Enum:_ `SORT_BY_GIVEN_ORDER`, `SORT_BY_ORDER_CREATED_AT`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished file.
If a part of the orders could not be found during the generation, the sub-status will be returned in response to the request to receive the finished file. `RESOURCE_NOT_FOUND`.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "businessId": 0, "orderIds": [ 0 ], "sortingType": "SORT_BY_GIVEN_ORDER" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Ready-made labels for one order](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabels)
Next
[Label manufacturing data](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData)
