---
title: Sending a file - Chats | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/sendFileToChat
crawled_at: 2025-09-17T14:41:51.256939
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body1)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body7)


# Sending a file to a chat
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/_auto/scopes_summary/pages/communication)
  * all-methods — Full account management


Sends the file to the chat with the buyer.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/chats/file/send

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
chatId* |  **Type:** integer<int64> The chat ID.  
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body)Body
multipart/form-data
```
{
    "file": null
}

```

**Name** |  **Description**  
---|---  
file* |  **Type:** string<binary> The contents of the file. The maximum file size is 5 MB.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#200-ok)200 OK
An empty answer. Means that the file has been sent.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body1)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendFileToChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
chatId*:
Body
file:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Sending a message](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendMessageToChat)
Next
[List of warehouses](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/warehouses/getPagedWarehouses)
