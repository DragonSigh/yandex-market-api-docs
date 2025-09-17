---
title: Application documents - FBY requests | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/getSupplyRequestDocuments
crawled_at: 2025-09-17T14:34:30.098020
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body1)
    * [GetSupplyRequestDocumentsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#getsupplyrequestdocumentsdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype)
    * [SupplyRequestDocumentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#supplyrequestdocumentdto)
    * [SupplyRequestDocumentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#supplyrequestdocumenttype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body7)


# Receipt of documents on the application for delivery, export or disposal
Info
Console
**The method is available for the[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/overview/fby) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns the application documents.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/supply-requests/documents

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body)Body
application/json
```
{
    "requestId": 0
}

```

**Name** |  **Description**  
---|---  
requestId* |  **Type:** integer<int64> The application ID. Used only in the API It will not be possible to find applications in the seller's account on the Market. To do this, use `marketplaceRequestId` or `warehouseRequestId`. _Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#200-ok)200 OK
A list of documents and links to them.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "documents": [
            {
                "type": "SUPPLY",
                "url": "string",
                "createdAt": "2022-12-29T18:02:01Z"
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GetSupplyRequestDocumentsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#getsupplyrequestdocumentsdto) Information about the application documents.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#getsupplyrequestdocumentsdto)GetSupplyRequestDocumentsDTO
Information about the application documents.
**Name** |  **Description**  
---|---  
documents* |  **Type:** [SupplyRequestDocumentDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#supplyrequestdocumentdto)[] A list of documents.  
The application document. _Min items:_ `0`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#supplyrequestdocumentdto)SupplyRequestDocumentDTO
The application document.
**Name** |  **Description**  
---|---  
createdAt* |  **Type:** string<date-time> The date and time when the document was created.  
type* |  **Type:** [SupplyRequestDocumentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#supplyrequestdocumenttype) Document type:
  * **Documents that the store uploads**
    * `SUPPLY` — a list of products.
    * `ADDITIONAL_SUPPLY` — the list of products in the additional delivery.
    * `VIRTUAL_DISTRIBUTION_CENTER_SUPPLY` — list of products in _multi-delivery_.
    * `TRANSFER` — a list of items for recycling.
    * `WITHDRAW` — a list of goods for export.
  * **Delivery of goods**
    * `VALIDATION_ERRORS` — errors in the delivery of goods.
    * `CARGO_UNITS` — labels for cargo locations.
  * **Additional delivery and rejected goods**
    * `ADDITIONAL_SUPPLY_ACCEPTABLE_GOODS` — products that are suitable for additional delivery.
    * `ADDITIONAL_SUPPLY_UNACCEPTABLE_GOODS` — export of rejected goods.
  * **Labeling of goods**
    * `INBOUND_UTD` — incoming UPD.
    * `OUTBOUND_UTD` — outgoing UPD.
    * `IDENTIFIERS` — product labeling codes.
    * `CIS_FACT` — accepted products with labeling codes.
    * `ITEMS_WITH_CISES` — products that need labeling.
    * `REPORT_OF_WITHDRAW_WITH_CISES` — marked goods for export from the warehouse.
    * `SECONDARY_ACCEPTANCE_CISES` — marked goods that are accepted after secondary acceptance.
    * `RNPT_FACT` — accepted goods with the batch registration number (RNPT).
  * **Acts**
    * `ACT_OF_WITHDRAW` — the act of return.
    * `ANOMALY_CONTAINERS_WITHDRAW_ACT` — the act of withdrawal of the rejected goods.
    * `ACT_OF_WITHDRAW_FROM_STORAGE` — the act of writing off from responsible storage.
    * `ACT_OF_RECEPTION_TRANSFER` — acceptance and transfer certificate.
    * `ACT_OF_DISCREPANCY` — the act of discrepancies.
    * `SECONDARY_RECEPTION_ACT` — the act of secondary acceptance.

_Enum:_ `SUPPLY`, `ADDITIONAL_SUPPLY`, `VIRTUAL_DISTRIBUTION_CENTER_SUPPLY`, `TRANSFER`, `INBOUND_UTD`, `OUTBOUND_UTD`, `ADDITIONAL_SUPPLY_ACCEPTABLE_GOODS`, `ADDITIONAL_SUPPLY_UNACCEPTABLE_GOODS`, `VALIDATION_ERRORS`, `WITHDRAW`, `ACT_OF_WITHDRAW`, `ANOMALY_CONTAINERS_WITHDRAW_ACT`, `ACT_OF_WITHDRAW_FROM_STORAGE`, `ACT_OF_RECEPTION_TRANSFER`, `ACT_OF_DISCREPANCY`, `SECONDARY_RECEPTION_ACT`, `CARGO_UNITS`, `IDENTIFIERS`, `CIS_FACT`, `ITEMS_WITH_CISES`, `REPORT_OF_WITHDRAW_WITH_CISES`, `SECONDARY_ACCEPTANCE_CISES`, `RNPT_FACT`  
url* |  **Type:** string Link to the document. _Min length:_ `1` _Max length:_ `2000`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#supplyrequestdocumenttype)SupplyRequestDocumentType
Document type:
  * **Documents that the store uploads**
    * `SUPPLY` — a list of products.
    * `ADDITIONAL_SUPPLY` — the list of products in the additional delivery.
    * `VIRTUAL_DISTRIBUTION_CENTER_SUPPLY` — list of products in _multi-delivery_.
    * `TRANSFER` — a list of items for recycling.
    * `WITHDRAW` — a list of goods for export.
  * **Delivery of goods**
    * `VALIDATION_ERRORS` — errors in the delivery of goods.
    * `CARGO_UNITS` — labels for cargo locations.
  * **Additional delivery and rejected goods**
    * `ADDITIONAL_SUPPLY_ACCEPTABLE_GOODS` — products that are suitable for additional delivery.
    * `ADDITIONAL_SUPPLY_UNACCEPTABLE_GOODS` — export of rejected goods.
  * **Labeling of goods**
    * `INBOUND_UTD` — incoming UPD.
    * `OUTBOUND_UTD` — outgoing UPD.
    * `IDENTIFIERS` — product labeling codes.
    * `CIS_FACT` — accepted products with labeling codes.
    * `ITEMS_WITH_CISES` — products that need labeling.
    * `REPORT_OF_WITHDRAW_WITH_CISES` — marked goods for export from the warehouse.
    * `SECONDARY_ACCEPTANCE_CISES` — marked goods that are accepted after secondary acceptance.
    * `RNPT_FACT` — accepted goods with the batch registration number (RNPT).
  * **Acts**
    * `ACT_OF_WITHDRAW` — the act of return.
    * `ANOMALY_CONTAINERS_WITHDRAW_ACT` — the act of withdrawal of the rejected goods.
    * `ACT_OF_WITHDRAW_FROM_STORAGE` — the act of writing off from responsible storage.
    * `ACT_OF_RECEPTION_TRANSFER` — acceptance and transfer certificate.
    * `ACT_OF_DISCREPANCY` — the act of discrepancies.
    * `SECONDARY_RECEPTION_ACT` — the act of secondary acceptance.

**Type** |  **Description**  
---|---  
[SupplyRequestDocumentType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#supplyrequestdocumenttype) |  _Enum:_ `SUPPLY`, `ADDITIONAL_SUPPLY`, `VIRTUAL_DISTRIBUTION_CENTER_SUPPLY`, `TRANSFER`, `INBOUND_UTD`, `OUTBOUND_UTD`, `ADDITIONAL_SUPPLY_ACCEPTABLE_GOODS`, `ADDITIONAL_SUPPLY_UNACCEPTABLE_GOODS`, `VALIDATION_ERRORS`, `WITHDRAW`, `ACT_OF_WITHDRAW`, `ANOMALY_CONTAINERS_WITHDRAW_ACT`, `ACT_OF_WITHDRAW_FROM_STORAGE`, `ACT_OF_RECEPTION_TRANSFER`, `ACT_OF_DISCREPANCY`, `SECONDARY_RECEPTION_ACT`, `CARGO_UNITS`, `IDENTIFIERS`, `CIS_FACT`, `ITEMS_WITH_CISES`, `REPORT_OF_WITHDRAW_WITH_CISES`, `SECONDARY_ACCEPTANCE_CISES`, `RNPT_FACT`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestDocuments#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "requestId": 0 }
Send
No longer supported, please use an alternative and newer version.
Copied
Read about what it is in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/storage/shipment/application#create).
### Was the article helpful?
YesNo
Previous
[Products in the application](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/supply-requests/getSupplyRequestItems)
Next
[One point of sale](https://yandex.ru/dev/market/partner-api/doc/en/reference/supply-requests/en/reference/outlets/getOutlet)
