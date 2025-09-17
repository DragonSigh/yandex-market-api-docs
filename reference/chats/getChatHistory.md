---
title: Message history - Chats | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/getChatHistory
crawled_at: 2025-09-17T14:41:09.474469
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body1)
    * [ChatMessagesResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagesresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype)
    * [ChatFullContextDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatfullcontextdto)
    * [ChatMessageDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagedto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#forwardscrollingpagerdto)
    * [ChatContextType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatcontexttype)
    * [ChatMessageSenderType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagesendertype)
    * [ChatMessagePayloadDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagepayloaddto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body7)


# Getting the chat message history
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/_auto/scopes_summary/pages/communication)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns the history of messages in the chat with the buyer.
**, Limit:** 10,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/chats/history

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
chatId* |  **Type:** integer<int64> The chat ID.  
_Min value:_ `1`  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body)Body
application/json
```
{
    "messageIdFrom": 0
}

```

**Name** |  **Description**  
---|---  
messageIdFrom |  **Type:** integer<int64> The ID of the message to receive all subsequent messages from. _Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#200-ok)200 OK
Message history.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "orderId": 0,
        "context": {
            "type": "ORDER",
            "orderId": 0,
            "returnId": 0
        },
        "messages": [
            {
                "messageId": 0,
                "createdAt": "2017-11-21T00:00:00+03:00",
                "sender": "PARTNER",
                "message": "string",
                "payload": [
                    {
                        "name": "string",
                        "url": "string",
                        "size": 0
                    }
                ]
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
result |  **Type:** [ChatMessagesResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagesresultdto) Information about messages.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagesresultdto)ChatMessagesResultDTO
Information about messages.
**Name** |  **Description**  
---|---  
context* |  **Type:** [ChatFullContextDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatfullcontextdto) Information about the order or refund for which the chat was started.  
messages* |  **Type:** [ChatMessageDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagedto)[] Information about messages.  
Information about the message.  
orderId ⦸ |  **Type:** integer<int64> The order ID.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatfullcontextdto)ChatFullContextDTO
Information about the order or refund for which the chat was started.
**Name** |  **Description**  
---|---  
type* |  **Type:** [ChatContextType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatcontexttype) Chat type:
  * `ORDER` — on orders. Read more about order chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `RETURN` — for refunds (FBY, FBS and Express). Read more about refund chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `DIRECT` — the chat that the customer started. Read more about this type in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/with-users).

_Enum:_ `ORDER`, `RETURN`, `DIRECT`  
orderId |  **Type:** integer<int64> The order ID. It is returned for orders and refunds. _Min value:_ `1`  
returnId |  **Type:** integer<int64> The refund ID. It is returned only for refunds. _Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagedto)ChatMessageDTO
Information about the message.
**Name** |  **Description**  
---|---  
createdAt* |  **Type:** string<date-time> The date and time when the message was created. Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
messageId* |  **Type:** integer<int64> The ID of the message. _Min value:_ `1`  
sender* |  **Type:** [ChatMessageSenderType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagesendertype) Sender. _Enum:_ `PARTNER`, `CUSTOMER`, `MARKET`, `SUPPORT`  
message |  **Type:** string The text of the message. Optional parameter if the parameter is returned `payload`.  
payload |  **Type:** [ChatMessagePayloadDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagepayloaddto)[] Information about the files attached to the message. Optional parameter if the parameter is returned `message`.   
Information about the files attached to the message. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatcontexttype)ChatContextType
Chat type:
  * `ORDER` — on orders. Read more about order chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `RETURN` — for refunds (FBY, FBS and Express). Read more about refund chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `DIRECT` — the chat that the customer started. Read more about this type in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/with-users).

**Type** |  **Description**  
---|---  
[ChatContextType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatcontexttype) |  _Enum:_ `ORDER`, `RETURN`, `DIRECT`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagesendertype)ChatMessageSenderType
Who sent the message:
  * `PARTNER` — the store.
  * `CUSTOMER` — the buyer.
  * `MARKET` — The market.
  * `SUPPORT` — a Yandex. Market support employee.

**Type** |  **Description**  
---|---  
[ChatMessageSenderType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagesendertype) |  _Enum:_ `PARTNER`, `CUSTOMER`, `MARKET`, `SUPPORT`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#chatmessagepayloaddto)ChatMessagePayloadDTO
Information about the files attached to the message.
**Name** |  **Description**  
---|---  
name* |  **Type:** string The file name.  
size* |  **Type:** integer<int32> The file size in bytes.  
url* |  **Type:** string The link to download the file. _Min length:_ `1` _Max length:_ `2000`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatHistory#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
chatId*:
page_token:
limit:
Body{ "messageIdFrom": 0 }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Orders that affected the quality index](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/ratings/getQualityRatingDetails)
Next
[Getting a single chat](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChat)
