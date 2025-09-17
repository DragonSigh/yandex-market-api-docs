---
title: Changing the warehouse status - Warehouses | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/updateWarehouseStatus
crawled_at: 2025-09-17T14:37:07.808583
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body1)
    * [WarehouseStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#warehousestatusdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype)
    * [WarehouseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#warehousestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body6)


# Changing the warehouse status
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Disables or enables the warehouse.
After the warehouse is shut down, the goods that are in it disappear after 15 minutes. After switching on, they return to the showcase in 15 minutes, and if the warehouse has been turned off for 30 days or longer — after 4 hours.
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/warehouse/status

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body)Body
application/json
```
{
    "enabled": false
}

```

**Name** |  **Description**  
---|---  
enabled* |  **Type:** boolean Warehouse status:
  * `true` — enabled.
  * `false` — disabled.

  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#200-ok)200 OK
New warehouse status.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "status": "DISABLED_MANUALLY"
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [WarehouseStatusDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#warehousestatusdto) Information about the status of the warehouse.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#warehousestatusdto)WarehouseStatusDTO
Information about the status of the warehouse.
**Name** |  **Description**  
---|---  
status* |  **Type:** [WarehouseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#warehousestatustype) Warehouse status:
  * `DISABLED_MANUALLY` – disabled by you.
  * `OTHER` – different status. For example, a warehouse is enabled or disabled by Yandex. Market.

_Enum:_ `DISABLED_MANUALLY`, `OTHER`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#warehousestatustype)WarehouseStatusType
Warehouse status:
  * `DISABLED_MANUALLY` – disabled by you.
  * `OTHER` – different status. For example, a warehouse is enabled or disabled by Yandex. Market.

**Type** |  **Description**  
---|---  
[WarehouseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#warehousestatustype) |  _Enum:_ `DISABLED_MANUALLY`, `OTHER`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/updateWarehouseStatus#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "enabled": false }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[List of warehouses](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getPagedWarehouses)
Next
[Market Warehouse Ids (FBY)](https://yandex.ru/dev/market/partner-api/doc/en/reference/warehouses/en/reference/warehouses/getFulfillmentWarehouses)
