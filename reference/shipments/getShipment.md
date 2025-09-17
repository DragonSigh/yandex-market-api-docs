---
title: Information about a single shipment - FBS Shipments | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/getShipment
crawled_at: 2025-09-17T14:32:46.454838
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body)
    * [ShipmentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype)
    * [ShipmentActionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentactiontype)
    * [SignatureDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#signaturedto)
    * [ShipmentStatusChangeDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentstatuschangedto)
    * [DeliveryServiceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#deliveryservicedto)
    * [PalletsCountDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#palletscountdto)
    * [ShipmentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmenttype)
    * [PartnerShipmentWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#partnershipmentwarehousedto)
    * [ShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentstatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body6)


# Getting information about a single shipment
Info
Console
**The method is available for the[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/overview/fbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about the shipment by its identifier.
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
shipmentId* |  **Type:** integer<int64> Shipment ID.  
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
cancelledOrders |  **Type:** boolean Whether to refund cancelled orders. Default value: `true`. If you do not need to refund cancelled orders, pass the value `false`.   
_Default:_ `true`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#200-ok)200 OK
The found shipment.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "id": 0,
        "planIntervalFrom": "2017-11-21T00:00:00+03:00",
        "planIntervalTo": "2017-11-21T00:00:00+03:00",
        "shipmentType": "IMPORT",
        "warehouse": {
            "id": 0,
            "name": "string",
            "address": "string"
        },
        "warehouseTo": {
            "id": 0,
            "name": "string",
            "address": "string"
        },
        "externalId": "string",
        "deliveryService": {
            "id": 0,
            "name": "string"
        },
        "palletsCount": {
            "planned": 0,
            "fact": 0
        },
        "orderIds": [
            0
        ],
        "draftCount": 0,
        "plannedCount": 0,
        "factCount": 0,
        "signature": {
            "signed": false
        },
        "currentStatus": {
            "status": "OUTBOUND_CREATED",
            "description": "string",
            "updateTime": "2017-11-21T00:00:00+03:00"
        },
        "availableActions": [
            "CONFIRM"
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [ShipmentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentdto) Shipping information.  
Shipping information.  
Shipping information.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentdto)ShipmentDTO
Shipping information.
**Name** |  **Description**  
---|---  
availableActions* |  **Type:** [ShipmentActionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentactiontype)[] Available actions on the shipment.  
Shipping actions:
  * `CONFIRM` — confirm the shipment.
  * `DOWNLOAD_ACT` — download the shipment acceptance and transfer certificate.
  * `DOWNLOAD_INBOUND_ACT` — download the list of accepted orders.
  * `DOWNLOAD_DISCREPANCY_ACT` — download the act of discrepancies.
  * `DOWNLOAD_TRANSPORTATION_WAYBILL` — download the bill of lading.
  * `CHANGE_PALLETS_COUNT` — specify the number of pallets.

_Enum:_ `CONFIRM`, `DOWNLOAD_ACT`, `DOWNLOAD_INBOUND_ACT`, `DOWNLOAD_DISCREPANCY_ACT`, `DOWNLOAD_TRANSPORTATION_WAYBILL`, `CHANGE_PALLETS_COUNT` _Unique items_  
draftCount* |  **Type:** integer<int32> The number of orders that the Market has scheduled for shipment. _Min value:_ `0`  
factCount* |  **Type:** integer<int32> The number of orders accepted at the sorting center or reception point. _Min value:_ `0`  
id* |  **Type:** integer<int64> Shipment ID. _Min value:_ `1`  
orderIds* |  **Type:** integer<int64>[] The IDs of the orders in the shipment.  
_Min value:_ `1` _Unique items_  
planIntervalFrom* |  **Type:** string<date-time> The beginning of the scheduled shipping interval. Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
planIntervalTo* |  **Type:** string<date-time> The end of the planned shipping interval. Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
plannedCount* |  **Type:** integer<int32> The number of orders that the Market has confirmed for shipment. _Min value:_ `0`  
signature* |  **Type:** [SignatureDTO(#signaturedto) Information about the signature of the acceptance certificate.  
currentStatus |  **Type:** [ShipmentStatusChangeDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentstatuschangedto) Shipment status.  
deliveryService |  **Type:** [DeliveryServiceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#deliveryservicedto) The delivery service.  
externalId |  **Type:** string The shipment ID in your system. If you haven't passed the ID yet, the ID from the parameter will be returned. `id`.  
palletsCount |  **Type:** [PalletsCountDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#palletscountdto) Information about the pallets in the shipment.  
shipmentType |  **Type:** [ShipmentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmenttype) The method of shipping orders. _Enum:_ `IMPORT`, `WITHDRAW`  
warehouse |  **Type:** [PartnerShipmentWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#partnershipmentwarehousedto) Information about the shipping warehouse.  
warehouseTo |  **Type:** [PartnerShipmentWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#partnershipmentwarehousedto) Information about the destination warehouse.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentactiontype)ShipmentActionType
Shipping actions:
  * `CONFIRM` — confirm the shipment.
  * `DOWNLOAD_ACT` — download the shipment acceptance and transfer certificate.
  * `DOWNLOAD_INBOUND_ACT` — download the list of accepted orders.
  * `DOWNLOAD_DISCREPANCY_ACT` — download the act of discrepancies.
  * `DOWNLOAD_TRANSPORTATION_WAYBILL` — download the bill of lading.
  * `CHANGE_PALLETS_COUNT` — specify the number of pallets.

**Type** |  **Description**  
---|---  
[ShipmentActionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentactiontype) |  _Enum:_ `CONFIRM`, `DOWNLOAD_ACT`, `DOWNLOAD_INBOUND_ACT`, `DOWNLOAD_DISCREPANCY_ACT`, `DOWNLOAD_TRANSPORTATION_WAYBILL`, `CHANGE_PALLETS_COUNT`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#signaturedto)SignatureDTO
Information about the signature of the acceptance certificate.
**Name** |  **Description**  
---|---  
signed* |  **Type:** boolean Has the acceptance certificate been signed?  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentstatuschangedto)ShipmentStatusChangeDTO
Shipment status.
**Name** |  **Description**  
---|---  
description |  **Type:** string Description of the shipment status.  
status |  **Type:** [ShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentstatustype) Shipment status. _Enum:_ `OUTBOUND_CREATED`, `OUTBOUND_READY_FOR_CONFIRMATION`, `OUTBOUND_CONFIRMED`, `OUTBOUND_SIGNED`, `FINISHED`, `ACCEPTED`, `ACCEPTED_WITH_DISCREPANCIES`, `ERROR`  
updateTime |  **Type:** string<date-time> The time of the last change in the shipment status. Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#deliveryservicedto)DeliveryServiceDTO
The delivery service.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> The delivery service ID.  
name |  **Type:** string The name of the delivery service.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#palletscountdto)PalletsCountDTO
The number of pallets in the shipment.
**Name** |  **Description**  
---|---  
fact |  **Type:** integer<int32> The number of pallets accepted at the sorting center. _Min value:_ `0`  
planned |  **Type:** integer<int32> The number of pallets specified by the seller. _Min value:_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmenttype)ShipmentType
Shipping method of orders:
  * `IMPORT` — you bring your orders to the selected sorting center or order acceptance point on your own.
  * `WITHDRAW` — you ship orders from your warehouse to Yandex Market couriers.

**Type** |  **Description**  
---|---  
[ShipmentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmenttype) |  _Enum:_ `IMPORT`, `WITHDRAW`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#partnershipmentwarehousedto)PartnerShipmentWarehouseDTO
Information about the shipping warehouse.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The ID of the shipping warehouse. _Min value:_ `1`  
address |  **Type:** string The address of the shipping warehouse.  
name |  **Type:** string The name of the shipping warehouse.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentstatustype)ShipmentStatusType
Shipment status:
  * `OUTBOUND_CREATED` — it is being formed.
  * `OUTBOUND_READY_FOR_CONFIRMATION` — it can be processed.
  * `OUTBOUND_CONFIRMED` — confirmed and ready to ship.
  * `OUTBOUND_SIGNED` — an electronic acceptance certificate has been signed for it.
  * `ACCEPTED` — accepted at the sorting center or reception point.
  * `ACCEPTED_WITH_DISCREPANCIES` — accepted with discrepancies.
  * `FINISHED` — completed.
  * `ERROR` — cancelled due to an error.

**Type** |  **Description**  
---|---  
[ShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#shipmentstatustype) |  _Enum:_ `OUTBOUND_CREATED`, `OUTBOUND_READY_FOR_CONFIRMATION`, `OUTBOUND_CONFIRMED`, `OUTBOUND_SIGNED`, `FINISHED`, `ACCEPTED`, `ACCEPTED_WITH_DISCREPANCIES`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
shipmentId*:
Query parameters
cancelledOrders:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Transferring orders to the next shipment](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/transferOrdersFromShipment)
Next
[Information about multiple shipments](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments)
