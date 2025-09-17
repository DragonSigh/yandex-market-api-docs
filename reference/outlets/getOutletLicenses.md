---
title: Information about licenses - Licenses | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/getOutletLicenses
crawled_at: 2025-09-17T14:35:10.163672
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body)
    * [OutletLicensesResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#outletlicensesresponsedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype)
    * [FullOutletLicenseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#fulloutletlicensedto)
    * [LicenseType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#licensetype)
    * [LicenseCheckStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#licensecheckstatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body6)


# Information about licenses for points of sale
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/overview/dbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/_auto/scopes_summary/pages/settings-management)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about licenses for points of sale.
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/outlets/licenses

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
ids |  **Type:** integer<int64>[] A list of license IDs to get information about. The identifiers are separated by commas. The license ID is assigned by Yandex.Market. Do not confuse it with the license number. The request must contain either the parameter `outletIds`, or the parameter `ids`. A request with or without both parameters will result in an error.   
_Min value:_ `1` _Unique items_  
outletIds |  **Type:** integer<int64>[] A list of IDs of points of sale for which you need to get information about licenses. The identifiers are separated by commas. The request must contain either the parameter `outletIds`, or the parameter `ids`. A request with or without both parameters will result in an error.   
_Min value:_ `1` _Min items:_ `1` _Max items:_ `500` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#200-ok)200 OK
The found licenses of your own points of sale.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "licenses": [
            {
                "id": 0,
                "outletId": 0,
                "licenseType": "ALCOHOL",
                "number": "string",
                "dateOfIssue": "2017-11-13T00:00:00+03:00",
                "dateOfExpiry": "2022-11-20T00:00:00+03:00",
                "checkStatus": "NEW",
                "checkComment": "string"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OutletLicensesResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#outletlicensesresponsedto) Response to a request for information about licenses for points of sale.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#outletlicensesresponsedto)OutletLicensesResponseDTO
Response to a request for information about licenses for points of sale.
**Name** |  **Description**  
---|---  
licenses* |  **Type:** [FullOutletLicenseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#fulloutletlicensedto)[] List of licenses.  
License information.  
License information.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#fulloutletlicensedto)FullOutletLicenseDTO
License information.
**Name** |  **Description**  
---|---  
dateOfExpiry* |  **Type:** string<date-time> The license expiration date. Date format: ISO 8601 with an offset relative to UTC. It is necessary to transmit the date indicated on the license, the time `00:00:00` and the time zone corresponding to the region of the point of sale. For example, if the license for a point of sale in Moscow ends on November 20, 2022, then the parameter should have the value `2022-11-20T00:00:00+03:00`. It cannot be earlier than the issue date specified in the parameter `dateOfIssue`. _Example:_ `2022-11-20T00:00:00+03:00`  
dateOfIssue* |  **Type:** string<date-time> The date the license was issued. Date format: ISO 8601 with an offset relative to UTC. It is necessary to transmit the date indicated on the license, the time `00:00:00` and the time zone corresponding to the region of the point of sale. For example, if the license for a point of sale in Moscow was issued on November 13, 2017, then the parameter should have the value `2017-11-13T00:00:00+03:00`. It cannot be later than the expiration date specified in the parameter. `dateOfExpiry`. _Example:_ `2017-11-13T00:00:00+03:00`  
licenseType* |  **Type:** [LicenseType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#licensetype) License type:
  * `ALCOHOL` — a license for the retail sale of alcoholic beverages.
  * `UNKNOWN` — unknown license type.

_Enum:_ `ALCOHOL`, `UNKNOWN`  
number* |  **Type:** string License number.  
outletId* |  **Type:** integer<int64> ID of the point of sale for which the license is valid. _Min value:_ `1`  
checkComment |  **Type:** string The reason why the license failed verification. The parameter is returned only if the parameter `checkStatus` it matters `FAIL`.  
checkStatus |  **Type:** [LicenseCheckStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#licensecheckstatustype) License verification status:
  * `NEW` — the license is being checked.
  * `SUCCESS` — the license has been verified.
  * `FAIL` — the license failed verification.
  * `REVOKE` — the license has been revoked by the quality service.
  * `DONT_WANT` — it is not checked.
  * `FAIL_MANUAL` — the license has not passed the quality control check.

_Enum:_ `NEW`, `SUCCESS`, `FAIL`, `REVOKE`, `DONT_WANT`, `FAIL_MANUAL`  
id |  **Type:** integer<int64> The license ID. This parameter is specified only if you need to change the information about an existing license. You can find out its ID using a request. [GET v2/campaigns/{campaignId}/outlets/licenses](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses). When transmitting information about the new license, you do not need to specify the ID. The license ID is assigned by Yandex.Market. Do not confuse it with the license number: it is passed in the parameter `number`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#licensetype)LicenseType
License type:
  * `ALCOHOL` — a license for the retail sale of alcoholic beverages.
  * `UNKNOWN` — unknown license type.

**Type** |  **Description**  
---|---  
[LicenseType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#licensetype) |  _Enum:_ `ALCOHOL`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#licensecheckstatustype)LicenseCheckStatusType
License verification status:
  * `NEW` — the license is being checked.
  * `SUCCESS` — the license has been verified.
  * `FAIL` — the license failed verification.
  * `REVOKE` — the license has been revoked by the quality service.
  * `DONT_WANT` — it is not checked.
  * `FAIL_MANUAL` — the license has not passed the quality control check.

**Type** |  **Description**  
---|---  
[LicenseCheckStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#licensecheckstatustype) |  _Enum:_ `NEW`, `SUCCESS`, `FAIL`, `REVOKE`, `DONT_WANT`, `FAIL_MANUAL`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutletLicenses#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
outletIds:
ids:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Removal](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/deleteOutlet)
Next
[Creation and modification](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/updateOutletLicenses)
