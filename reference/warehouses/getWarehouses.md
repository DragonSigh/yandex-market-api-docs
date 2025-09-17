---
title: List of warehouses - Outdated methods | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/getWarehouses
crawled_at: 2025-09-17T14:46:06.676070
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body)
    * [WarehousesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousesdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype)
    * [WarehouseGroupDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousegroupdto)
    * [WarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousedto)
    * [WarehouseAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehouseaddressdto)
    * [GpsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#gpsdto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body6)


# List of warehouses and warehouse groups
Deprecated
Info
Console
**The method is available for models:[FBS, Express and DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Which method should I use instead of the outdated one?
[POST v2/businesses/{businessId}/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses)
Returns a list of warehouses and, if warehouses are combined, a list of warehouse groups. [What are warehouse groups and why are they needed?](https://yandex.ru/support/marketplace/assortment/operations/stocks.html#unified-stocks)
Among other things, the request allows you to determine the identifier to be used when transferring balances for a group of warehouses.
**, Limit:** 100 requests per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/warehouses

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#200-ok)200 OK
A list of warehouses and groups of warehouses.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "warehouses": [
            {
                "id": 0,
                "name": "string",
                "campaignId": 0,
                "express": false,
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
        ],
        "warehouseGroups": [
            {
                "name": "string",
                "mainWarehouse": {
                    "id": 0,
                    "name": "string",
                    "campaignId": 0,
                    "express": false,
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
                },
                "warehouses": [
                    {
                        "id": 0,
                        "name": "string",
                        "campaignId": 0,
                        "express": false,
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
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [WarehousesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousesdto) Information about warehouses and groups of warehouses.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousesdto)WarehousesDTO
Information about warehouses and groups of warehouses.
**Name** |  **Description**  
---|---  
warehouseGroups* |  **Type:** [WarehouseGroupDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousegroupdto)[] List of warehouse groups.  
Information about the warehouse group.  
warehouses* |  **Type:** [WarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousedto)[] A list of warehouses that are not included in the groups.  
Information about the warehouse.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousegroupdto)WarehouseGroupDTO
Information about the warehouse group.
**Name** |  **Description**  
---|---  
mainWarehouse* |  **Type:** [WarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousedto) Information about the warehouse.  
name* |  **Type:** string The name of the warehouse group.  
warehouses* |  **Type:** [WarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousedto)[] The list of warehouses included in the group.  
Information about the warehouse.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehousedto)WarehouseDTO
Information about the warehouse.
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
express* |  **Type:** boolean Is Express delivery possible?  
id* |  **Type:** integer<int64> The warehouse ID.  
name* |  **Type:** string The name of the warehouse.  
address |  **Type:** [WarehouseAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehouseaddressdto) Warehouse address.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#warehouseaddressdto)WarehouseAddressDTO
Warehouse address.
**Name** |  **Description**  
---|---  
city* |  **Type:** string City. _Max length:_ `200`  
gps* |  **Type:** [GpsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#gpsdto) GPS coordinates of latitude and longitude.  
block |  **Type:** string Building number. _Max length:_ `16`  
building |  **Type:** string Building number. _Max length:_ `16`  
number |  **Type:** string The house number. _Max length:_ `256`  
street |  **Type:** string Street. _Max length:_ `512`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#gpsdto)GpsDTO
GPS coordinates of latitude and longitude.
**Name** |  **Description**  
---|---  
latitude* |  **Type:** number<decimal> Width.  
longitude* |  **Type:** number<decimal> Longitude.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Market Prices Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/reports/generatePricesReport)
Next
[One model](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/models/getModel)
