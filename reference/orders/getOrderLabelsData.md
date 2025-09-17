---
title: Label manufacturing data - FBS and DBS shortcuts | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/getOrderLabelsData
crawled_at: 2025-09-17T14:33:48.558553
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body)
    * [OrderLabelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#orderlabeldto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype)
    * [ParcelBoxLabelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#parcelboxlabeldto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body6)


# Data for self-label production
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs).**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information on labels that are glued to boxes in the order.
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/delivery/labels/data

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#200-ok)200 OK
Information for printing labels.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "orderId": 0,
        "placesNumber": 0,
        "url": "string",
        "parcelBoxLabels": [
            {
                "url": "string",
                "supplierName": "string",
                "deliveryServiceName": "string",
                "orderId": 0,
                "orderNum": "string",
                "recipientName": "string",
                "boxId": 0,
                "fulfilmentId": "string",
                "place": "string",
                "weight": "string",
                "deliveryServiceId": "string",
                "deliveryAddress": "string",
                "shipmentDate": "string"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OrderLabelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#orderlabeldto) Data for printing the label.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#orderlabeldto)OrderLabelDTO
Data for printing the label.
**Name** |  **Description**  
---|---  
orderId* |  **Type:** integer<int64> The order ID.  
parcelBoxLabels* |  **Type:** [ParcelBoxLabelDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#parcelboxlabeldto)[] Information on the label.  
Information about the label for the box.  
placesNumber* |  **Type:** integer<int32> The number of boxes in the order.  
url* ⦸ |  **Type:** string The URL of the file with label labels for all the boxes in the order. Corresponds to the request URL. [GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/labels](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabels). _Min length:_ `1` _Max length:_ `2000`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#parcelboxlabeldto)ParcelBoxLabelDTO
Information about the label for the box.
**Name** |  **Description**  
---|---  
boxId* |  **Type:** integer<int64> The ID of the box.  
deliveryServiceId* |  **Type:** string The delivery service ID. Information about the delivery service can be obtained by requesting [GET delivery/services](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getDeliveryServices).  
deliveryServiceName* |  **Type:** string The legal name of the delivery service.  
fulfilmentId* |  **Type:** string The ID of the box in the store's information system. Returned in the format: `The order number on the Market is the box number.`. For example, `7206821‑1`, `7206821‑2` and so on .  
orderId* |  **Type:** integer<int64> The order ID in the Market system.  
orderNum* |  **Type:** string The order ID in the store's information system. Matches with `orderId` if the Market does not know the order number in the store's system.  
place* |  **Type:** string The box number in the order. Returned in the format: `seat number/total number of seats`.  
recipientName* |  **Type:** string Last name and initials of the recipient of the order.  
supplierName* |  **Type:** string The legal name of the store.  
url* |  **Type:** string Corresponds to the request URL. [GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/shipments/{shipmentId}/boxes/{boxId}/label](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateOrderLabel). _Min length:_ `1` _Max length:_ `2000`  
weight* ⦸ |  **Type:** string The total weight of all items in the order. Returned in the format: `weight kg`.  
deliveryAddress |  **Type:** string Recipient's address.  
shipmentDate |  **Type:** string Date of shipment in the format `dd.MM.yyyy`.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderLabelsData#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Ready-made labels for multiple orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/generateMassOrderLabelsReport)
Next
[Labels for Trust Acceptance (FBS)](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/shipments/downloadShipmentPalletLabels)
