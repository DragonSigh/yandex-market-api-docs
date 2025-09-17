---
title: List of warehouses - Warehouses | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/getPagedWarehouses
crawled_at: 2025-09-17T14:42:00.195141
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body)
    * [WarehouseComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousecomponenttype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body1)
    * [PagedWarehousesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#pagedwarehousesdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype)
    * [WarehouseDetailsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousedetailsdto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#forwardscrollingpagerdto)
    * [WarehouseAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehouseaddressdto)
    * [WarehouseGroupInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousegroupinfodto)
    * [WarehouseStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousestatusdto)
    * [GpsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#gpsdto)
    * [WarehouseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body6)


# List of warehouses
Info
Console
**The method is available for models:[FBS, Express and DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns a list of warehouses and information about them.
Restriction for the parameter `limit`
Do not transmit a value greater than 25.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/warehouses

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body)Body
application/json
```
{
    "components": [
        "ADDRESS"
    ],
    "campaignIds": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
campaignIds |  **Type:** integer<int64>[] A list of campaign IDs of those stores whose warehouses need to be returned. You can find them using a query. [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not use store IDs instead, which are listed in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1` _Min items:_ `1` _Max items:_ `25` _Unique items_  
components |  **Type:** [WarehouseComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousecomponenttype)[] Properties of warehouses that need to be returned. If some parameter value is omitted, this information will not be included in the response. Pass the parameter only if you need the information it returns. You can pass multiple values at once.   
Properties of warehouses that need to be returned:
  * `ADDRESS` — the address of the warehouse.
  * `STATUS` — warehouse status.

_Enum:_ `ADDRESS`, `STATUS` _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousecomponenttype)WarehouseComponentType
Properties of warehouses that need to be returned:
  * `ADDRESS` — the address of the warehouse.
  * `STATUS` — warehouse status.

**Type** |  **Description**  
---|---  
[WarehouseComponentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousecomponenttype) |  _Enum:_ `ADDRESS`, `STATUS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#200-ok)200 OK
The list of warehouses and their properties that you requested.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body1)Body
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
                "groupInfo": {
                    "name": "string",
                    "id": 0
                },
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
                },
                "status": {
                    "status": "DISABLED_MANUALLY"
                }
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
result |  **Type:** [PagedWarehousesDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#pagedwarehousesdto) Information about warehouses in the cabinet.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#pagedwarehousesdto)PagedWarehousesDTO
Information about warehouses in the cabinet.
**Name** |  **Description**  
---|---  
warehouses* |  **Type:** [WarehouseDetailsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousedetailsdto)[] List of warehouses.  
Information about the warehouse.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousedetailsdto)WarehouseDetailsDTO
Information about the warehouse.
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID of the store that is associated with the warehouse. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.  
express* |  **Type:** boolean Is delivery possible for the Express model?  
id* |  **Type:** integer<int64> The warehouse ID.  
name* |  **Type:** string The name of the warehouse.  
address |  **Type:** [WarehouseAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehouseaddressdto) Warehouse address. Returned only if the parameter is specified in the request `components` takes the value `ADDRESS`.  
groupInfo |  **Type:** [WarehouseGroupInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousegroupinfodto) Information about the group to which the warehouse belongs. It is returned only for warehouses in groups. [What are warehouse groups and why are they needed?](https://yandex.ru/support/marketplace/assortment/operations/stocks.html#unified-stocks)  
status |  **Type:** [WarehouseStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousestatusdto) The status of the warehouse. Returned only if the parameter is specified in the request `components` takes the value `STATUS`. The status of the warehouse received via the API may not match the status in the cabinet. For example, first the Market disabled the warehouse, and then you use the method [POST v2/campaigns/{campaignId}/warehouse/status](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus). Status in the cabinet — **Disabled by Yandex.Market** , and it will return via the API **DISABLED_MANUALLY** (disabled by you).  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehouseaddressdto)WarehouseAddressDTO
Warehouse address.
**Name** |  **Description**  
---|---  
city* |  **Type:** string City. _Max length:_ `200`  
gps* |  **Type:** [GpsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#gpsdto) GPS coordinates of latitude and longitude.  
block |  **Type:** string Building number. _Max length:_ `16`  
building |  **Type:** string Building number. _Max length:_ `16`  
number |  **Type:** string The house number. _Max length:_ `256`  
street |  **Type:** string Street. _Max length:_ `512`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousegroupinfodto)WarehouseGroupInfoDTO
Information about the group to which the warehouse belongs.
It is returned only for warehouses in groups.
[What are warehouse groups and why are they needed?](https://yandex.ru/support/marketplace/assortment/operations/stocks.html#unified-stocks)
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> ID of the warehouse group.  
name* |  **Type:** string The name of the group that the warehouse belongs to.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousestatusdto)WarehouseStatusDTO
Information about the status of the warehouse.
**Name** |  **Description**  
---|---  
status* |  **Type:** [WarehouseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousestatustype) Warehouse status:
  * `DISABLED_MANUALLY` – disabled by you.
  * `OTHER` – different status. For example, a warehouse is enabled or disabled by Yandex. Market.

_Enum:_ `DISABLED_MANUALLY`, `OTHER`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#gpsdto)GpsDTO
GPS coordinates of latitude and longitude.
**Name** |  **Description**  
---|---  
latitude* |  **Type:** number<decimal> Width.  
longitude* |  **Type:** number<decimal> Longitude.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousestatustype)WarehouseStatusType
Warehouse status:
  * `DISABLED_MANUALLY` – disabled by you.
  * `OTHER` – different status. For example, a warehouse is enabled or disabled by Yandex. Market.

**Type** |  **Description**  
---|---  
[WarehouseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#warehousestatustype) |  _Enum:_ `DISABLED_MANUALLY`, `OTHER`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
page_token:
limit:
Body{ "components": [ "ADDRESS" ], "campaignIds": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Sending a file](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/chats/sendFileToChat)
Next
[Changing the warehouse status](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus)
