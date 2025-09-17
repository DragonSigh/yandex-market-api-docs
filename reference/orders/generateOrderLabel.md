---
title: Ready-made label for the box - FBS and DBS shortcuts | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/generateOrderLabel
crawled_at: 2025-09-17T14:33:31.679713
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#query-parameters)
    * [PageFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#pageformattype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body6)


# Ready‑made label-sticker for the box in the order
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Generates a label sticker for the box in the order and returns the label in a PDF file.
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/delivery/shipments/{shipmentId}/boxes/{boxId}/label

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
boxId* |  **Type:** integer<int64> The ID of the box.  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
shipmentId* ⦸ |  **Type:** integer<int64> Pass any number to get a valid URL. The cargo location ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [PageFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#pageformattype) Setting up the placement of shortcuts on the page. If there is no parameter, a PDF with labels in A7 format is returned.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#pageformattype)PageFormatType
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
![Image of a vertical label in A9 format for Market Yandex Go sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A9-uz.png)
  * `A7` — the label is 75 × 120 mm (80.4 × 125.6 mm including margins), close to the A7 format.
An example of a label for Market sellers
![An image of an A7 format label for Market sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A7.jpg)
An example of a shortcut for Market Yandex Go sellers
![An image of an A7 format label for Market Yandex Go sellers](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A7-uz.png)
  * `A4` — on the A4 sheet there is a label of the format that is selected in the seller's office on the Market — go to the page **Orders** → **Orders and shipments** → on the tab of the desired work model, click **Label format**.

**Type** |  **Description**  
---|---  
[PageFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#pageformattype) |  _Enum:_ `A9_HORIZONTALLY`, `A9`, `A7`, `A4`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#200-ok)200 OK
A PDF file with labels for the box. The file contains one page with a shortcut.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body)Body
application/pdf
**Type:** string
**Format:** binary
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
shipmentId*:
boxId*:
Query parameters
format:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[The actual act of acceptance and transfer](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/shipments/downloadShipmentInboundAct)
Next
[Ready-made labels for one order](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabels)
