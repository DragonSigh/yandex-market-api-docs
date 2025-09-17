---
title: Information about multiple shipments - FBS Shipments | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/searchShipments
crawled_at: 2025-09-17T14:32:53.638198
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body)
    * [ShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmentstatustype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body1)
    * [SearchShipmentsResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#searchshipmentsresponsedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype)
    * [ShipmentInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmentinfodto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#forwardscrollingpagerdto)
    * [SignatureDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#signaturedto)
    * [DeliveryServiceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#deliveryservicedto)
    * [PalletsCountDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#palletscountdto)
    * [ShipmentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmenttype)
    * [PartnerShipmentWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#partnershipmentwarehousedto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body7)


# Getting information about multiple shipments
Info
Console
**The method is available for the[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/overview/fbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about shipments based on the specified parameters:
  * date.
  * status;
  * order IDs.


The results are returned page by page.
Restriction for the parameter `limit`
Do not transmit a value greater than 30.
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#request)Request
PUT
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/first-mile/shipments

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body)Body
application/json
```
{
    "dateFrom": "string",
    "dateTo": "string",
    "statuses": [
        "OUTBOUND_CREATED"
    ],
    "orderIds": [
        0
    ],
    "cancelledOrders": true
}

```

**Name** |  **Description**  
---|---  
dateFrom* |  **Type:** string<date> The starting date for filtering by shipment date (inclusive). Date format: `DD-MM-YYYY`.  
dateTo* |  **Type:** string<date> The end date for filtering by shipment date (inclusive). Date format: `DD-MM-YYYY`.  
cancelledOrders |  **Type:** boolean Whether to refund cancelled orders. Default value: `true`. If you do not need to refund cancelled orders, pass the value `false`. _Default:_ `true`  
orderIds |  **Type:** integer<int64>[] A list of order IDs from shipments.  
The order ID. _Min items:_ `1` _Unique items_  
statuses |  **Type:** [ShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmentstatustype)[] List of shipment statuses.  
Shipment status _Enum:_ `OUTBOUND_CREATED`, `OUTBOUND_READY_FOR_CONFIRMATION`, `OUTBOUND_CONFIRMED`, `OUTBOUND_SIGNED`, `FINISHED`, `ACCEPTED`, `ACCEPTED_WITH_DISCREPANCIES`, `ERROR` _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmentstatustype)ShipmentStatusType
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
[ShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmentstatustype) |  _Enum:_ `OUTBOUND_CREATED`, `OUTBOUND_READY_FOR_CONFIRMATION`, `OUTBOUND_CONFIRMED`, `OUTBOUND_SIGNED`, `FINISHED`, `ACCEPTED`, `ACCEPTED_WITH_DISCREPANCIES`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#200-ok)200 OK
Shipments found.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "shipments": [
            {
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
                "status": "OUTBOUND_CREATED",
                "statusDescription": "string",
                "statusUpdateTime": "2017-11-21T00:00:00+03:00"
            }
        ],
        "paging": {
            "nextPageToken": "string"
        }
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [SearchShipmentsResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#searchshipmentsresponsedto) Information about shipments.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#searchshipmentsresponsedto)SearchShipmentsResponseDTO
Information about shipments.
**Name** |  **Description**  
---|---  
shipments* |  **Type:** [ShipmentInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmentinfodto)[] A list with information about shipments.  
A list with information about shipments.  
Shipping information.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#forwardscrollingpagerdto) Pages with search results.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmentinfodto)ShipmentInfoDTO
A list with information about shipments.
**Name** |  **Description**  
---|---  
draftCount* |  **Type:** integer<int32> The number of orders that the Market has scheduled for shipment. _Min value:_ `0`  
factCount* |  **Type:** integer<int32> The number of orders accepted at the sorting center or reception point. _Min value:_ `0`  
id* |  **Type:** integer<int64> Shipment ID. _Min value:_ `1`  
orderIds* |  **Type:** integer<int64>[] The IDs of the orders in the shipment.  
_Min value:_ `1` _Unique items_  
planIntervalFrom* |  **Type:** string<date-time> The beginning of the scheduled shipping interval. Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
planIntervalTo* |  **Type:** string<date-time> The end of the planned shipping interval. Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
plannedCount* |  **Type:** integer<int32> The number of orders that the Market has confirmed for shipment. _Min value:_ `0`  
signature* |  **Type:** [SignatureDTO(#signaturedto) Information about the signature of the acceptance certificate.  
deliveryService |  **Type:** [DeliveryServiceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#deliveryservicedto) The delivery service.  
externalId |  **Type:** string The shipment ID in your system. If you haven't passed the ID yet, the ID from the parameter will be returned. `id`.  
palletsCount |  **Type:** [PalletsCountDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#palletscountdto) Information about the pallets in the shipment.  
shipmentType |  **Type:** [ShipmentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmenttype) The method of shipping orders. _Enum:_ `IMPORT`, `WITHDRAW`  
status |  **Type:** [ShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmentstatustype) Shipment status. _Enum:_ `OUTBOUND_CREATED`, `OUTBOUND_READY_FOR_CONFIRMATION`, `OUTBOUND_CONFIRMED`, `OUTBOUND_SIGNED`, `FINISHED`, `ACCEPTED`, `ACCEPTED_WITH_DISCREPANCIES`, `ERROR`  
statusDescription |  **Type:** string Description of the shipment status.  
statusUpdateTime |  **Type:** string<date-time> The time of the last change in the shipment status Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
warehouse |  **Type:** [PartnerShipmentWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#partnershipmentwarehousedto) Information about the shipping warehouse.  
warehouseTo |  **Type:** [PartnerShipmentWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#partnershipmentwarehousedto) Information about the destination warehouse.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#signaturedto)SignatureDTO
Information about the signature of the acceptance certificate.
**Name** |  **Description**  
---|---  
signed* |  **Type:** boolean Has the acceptance certificate been signed?  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#deliveryservicedto)DeliveryServiceDTO
The delivery service.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> The delivery service ID.  
name |  **Type:** string The name of the delivery service.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#palletscountdto)PalletsCountDTO
The number of pallets in the shipment.
**Name** |  **Description**  
---|---  
fact |  **Type:** integer<int32> The number of pallets accepted at the sorting center. _Min value:_ `0`  
planned |  **Type:** integer<int32> The number of pallets specified by the seller. _Min value:_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmenttype)ShipmentType
Shipping method of orders:
  * `IMPORT` — you bring your orders to the selected sorting center or order acceptance point on your own.
  * `WITHDRAW` — you ship orders from your warehouse to Yandex Market couriers.

**Type** |  **Description**  
---|---  
[ShipmentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#shipmenttype) |  _Enum:_ `IMPORT`, `WITHDRAW`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#partnershipmentwarehousedto)PartnerShipmentWarehouseDTO
Information about the shipping warehouse.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The ID of the shipping warehouse. _Min value:_ `1`  
address |  **Type:** string The address of the shipping warehouse.  
name |  **Type:** string The name of the shipping warehouse.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/searchShipments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
page_token:
limit:
Body{ "dateFrom": "string", "dateTo": "string", "statuses": [ "OUTBOUND_CREATED" ], "orderIds": [ 0 ], "cancelledOrders": true }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Information about a single shipment](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/getShipment)
Next
[Acceptance and transfer certificate](https://yandex.ru/dev/market/partner-api/doc/en/reference/shipments/en/reference/shipments/downloadShipmentAct)
