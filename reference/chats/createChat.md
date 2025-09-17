---
title: Creating a new chat - Chats | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/createChat
crawled_at: 2025-09-17T14:41:35.020033
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body)
    * [ChatContextDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#chatcontextdto)
    * [ChatContextIdentifiableType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#chatcontextidentifiabletype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body1)
    * [CreateChatResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#createchatresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body7)


# Creating a new chat with a customer
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/_auto/scopes_summary/pages/communication)
  * all-methods — Full account management


Creates a new chat with the customer.
Types of chats:
  * by orders;
  * for refunds (available only for FBY, FBS, and Express stores).


You can't create a chat with the type `DIRECT`. Read more about customer messages in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/with-users).
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/chats/new

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body)Body
application/json
```
{
    "orderId": 0,
    "context": {
        "type": "ORDER",
        "id": 0
    }
}

```

**Name** |  **Description**  
---|---  
context |  **Type:** [ChatContextDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#chatcontextdto) Information about the order or refund for which the chat was started.  
orderId ⦸ |  **Type:** integer<int64> The order ID on the Market.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#chatcontextdto)ChatContextDTO
Information about the order or refund for which the chat was started.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The order or refund ID. _Min value:_ `1`  
type* |  **Type:** [ChatContextIdentifiableType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#chatcontextidentifiabletype) Chat type:
  * `ORDER` — on orders. Read more about order chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `RETURN` — for refunds (FBY, FBS and Express). Read more about refund chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).

_Enum:_ `ORDER`, `RETURN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#chatcontextidentifiabletype)ChatContextIdentifiableType
Chat type:
  * `ORDER` — on orders. Read more about order chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `RETURN` — for refunds (FBY, FBS and Express). Read more about refund chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).

**Type** |  **Description**  
---|---  
[ChatContextIdentifiableType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#chatcontextidentifiabletype) |  _Enum:_ `ORDER`, `RETURN`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#200-ok)200 OK
Everything worked out: the chat was created.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "chatId": 0
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [CreateChatResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#createchatresultdto) Information about the created chat.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#createchatresultdto)CreateChatResultDTO
Information about the created chat.
**Name** |  **Description**  
---|---  
chatId* |  **Type:** integer<int64> The chat ID. _Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/createChat#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "orderId": 0, "context": { "type": "ORDER", "id": 0 } }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Receiving a message](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatMessage)
Next
[Sending a message](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/sendMessageToChat)
