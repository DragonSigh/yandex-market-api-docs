---
title: Market Warehouse Ids (FBY) - Warehouses | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/getFulfillmentWarehouses
crawled_at: 2025-09-17T14:26:55.650253
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body)
    * [FulfillmentWarehousesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#fulfillmentwarehousesdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype)
    * [FulfillmentWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#fulfillmentwarehousedto)
    * [WarehouseAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#warehouseaddressdto)
    * [GpsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#gpsdto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body6)


# Market Warehouse IDs
Info
Console
**The method is available for the[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/overview/fby) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/pricing_read-only)
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/promotion_read-only)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/finance-and-accounting)
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/communication)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/settings-management)
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Retrieves a list of Market warehouses with their IDs.
**, Limit:** 100 requests per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/warehouses

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
campaignId |  **Type:** integer<int64> The campaign ID. It is indicated if you need to return all the Market warehouses that are linked to a specific campaign. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#200-ok)200 OK
List of warehouses.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "warehouses": [
            {
                "id": 0,
                "name": "string",
                "address": {
                    "city": "string",
                    "street": "string",
                    "number": "string",
                    "building": "string",
                    "block": "string",
                    "gps": {
                        "latitude": 0,
                        "longitude": 0
                    }
                }
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [FulfillmentWarehousesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#fulfillmentwarehousesdto) List of Market warehouses (FBY).  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#fulfillmentwarehousesdto)FulfillmentWarehousesDTO
List of Market warehouses (FBY).
**Name** |  **Description**  
---|---  
warehouses* |  **Type:** [FulfillmentWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#fulfillmentwarehousedto)[] List of Market warehouses (FBY).  
Market Warehouse (FBY).  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#fulfillmentwarehousedto)FulfillmentWarehouseDTO
Market Warehouse (FBY).
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The warehouse ID.  
name* |  **Type:** string The name of the warehouse.  
address |  **Type:** [WarehouseAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#warehouseaddressdto) Warehouse address.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#warehouseaddressdto)WarehouseAddressDTO
Warehouse address.
**Name** |  **Description**  
---|---  
city* |  **Type:** string City. _Max length:_ `200`  
gps* |  **Type:** [GpsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#gpsdto) GPS coordinates of latitude and longitude.  
block |  **Type:** string Building number. _Max length:_ `16`  
building |  **Type:** string Building number. _Max length:_ `16`  
number |  **Type:** string The house number. _Max length:_ `256`  
street |  **Type:** string Street. _Max length:_ `512`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#gpsdto)GpsDTO
GPS coordinates of latitude and longitude.
**Name** |  **Description**  
---|---  
latitude* |  **Type:** number<decimal> Width.  
longitude* |  **Type:** number<decimal> Longitude.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
campaignId:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Changing the warehouse status](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus)
Next
[Information about the authorization token](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/auth/getAuthTokenInfo)
