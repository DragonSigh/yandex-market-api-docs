---
title: Removal - Licenses | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/deleteOutletLicenses
crawled_at: 2025-09-17T14:35:22.787184
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body6)


# Removing licenses for points of sale
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/overview/dbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/_auto/scopes_summary/pages/settings-management)
  * all-methods — Full account management


Deletes information about licenses for points of sale.
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#request)Request
DELETE
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/outlets/licenses

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
ids* |  **Type:** integer<int64>[] The list of license IDs that need to be deleted. The identifiers are separated by commas. The license ID is assigned by Yandex.Market. Do not confuse it with the license number.   
_Min items:_ `1` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#200-ok)200 OK
An empty answer.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
ids*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Creation and modification](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/updateOutletLicenses)
Next
[List of non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/orders/getReturns)
