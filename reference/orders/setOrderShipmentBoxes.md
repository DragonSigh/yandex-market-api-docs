---
title: Transfer of quantity by cargo. - Orders | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/setOrderShipmentBoxes
crawled_at: 2025-09-17T14:45:16.098844
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body)
    * [ParcelBoxRequestDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#parcelboxrequestdto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body1)
    * [ShipmentBoxesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#shipmentboxesdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype)
    * [ParcelBoxDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#parcelboxdto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body7)


# Transfer of the number of cargo spaces in the order
Deprecated
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Which method should I use instead of the outdated one?
[PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout)
An order shipped to the Market may not fit into one box or package. In this case, it turns out that it takes up several cargo spaces.
The number of cargo spaces must be transferred to the Market if it is not equal to 1. This is done before transferring it to the status **Ready for shipment**. For more information about what needs to be transmitted at what point, see [step-by-step instructions](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/step-by-step/fbs).
The method is slightly non-standard: the number is set by the length of the array of empty objects.
Previously, the method required transmitting more data. Queries based on the old pattern work, but it's better to do it in a new way.
How it was before
The structure of the PUT request body:
```
{
  "boxes":
  [
    {
      "fulfilmentId": "{string}",
      "weight": {int64},
      "width": {int64},
      "height": {int64},
      "depth": {int64},
      "items":
      [
        {
          "id": {int64},
          "count": {int32}
        },
        ...
      ]
    },
    ...
  ]
}

```

**Parameter** | **Type** | **Meaning**  
---|---|---  
`boxes` |  | List of cargo locations.  
**Parameters nested in`boxes`**
**Parameter** | **Type** | **Meaning**  
---|---|---  
`fulfilmentId` | String | The identifier of the cargo space in the store's information system. Create an identifier based on a template: `The order number on the Market is the number of the cargo place.`. For example, `7206821‑1, 7206821‑2` and so on .  
`weight` | Int64 | The gross weight of the cargo area (the total weight of the package and contents) in grams.  
`width` | Int64 | The width of the cargo area in centimeters.  
`height` | Int64 | The height of the cargo area in centimeters.  
`depth` | Int64 | The depth of the cargo area in centimeters.  
`items` | Int64 | The list of goods in the cargo area.  
**Parameters nested in`items`**
**Parameter** | **Type** | **Meaning**  
---|---|---  
`id` | Int64 | The identifier of the product within the order.  
`count` | Int32 | The number of items in the cargo area.  
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#request)Request
PUT
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/delivery/shipments/{shipmentId}/boxes

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
shipmentId* |  **Type:** integer<int64> Pass any number to get a valid URL. The cargo location ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body)Body
application/json
```
{
    "boxes": [
        {
            "fulfilmentId": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
boxes* |  **Type:** [ParcelBoxRequestDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#parcelboxrequestdto)[] List of cargo locations. The Market determines the number of places based on its length.  
The parameter displays one cargo location. Nested fields are no longer used, pass the parameter empty. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#parcelboxrequestdto)ParcelBoxRequestDTO
The parameter displays one cargo location. Nested fields are no longer used, pass the parameter empty.
**Name** |  **Description**  
---|---  
fulfilmentId ⦸ |  **Type:** string Do not use this option. _Pattern:_ `^[\p{Alnum}- ]*$`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#200-ok)200 OK
Only the type of response matters. If the answer is `ok`, the amount of cargo is not recorded.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "boxes": [
            {
                "id": 0,
                "fulfilmentId": "string"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [ShipmentBoxesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#shipmentboxesdto) In the response, the Market returns the list of cargo locations you provided. Don't pay any attention to this field.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#shipmentboxesdto)ShipmentBoxesDTO
In the response, the Market returns the list of cargo locations you provided. Don't pay any attention to this field.
**Name** |  **Description**  
---|---  
boxes* |  **Type:** [ParcelBoxDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#parcelboxdto)[] List of cargo locations. The Market determined the number of seats based on its length.   
The parameter displays one cargo location.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#parcelboxdto)ParcelBoxDTO
The parameter displays one cargo location.
**Name** |  **Description**  
---|---  
fulfilmentId ⦸ |  **Type:** string Do not use this option. _Pattern:_ `^[\p{Alnum}- ]*$`  
id |  **Type:** integer<int64> The ID of the box in the order.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderShipmentBoxes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
shipmentId*:
Body{ "boxes": [ { "fulfilmentId": "string" } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Transfer of "Fair Sign" codes](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemCis)
Next
[Making a Return Decision (DBS)](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setReturnDecision)
