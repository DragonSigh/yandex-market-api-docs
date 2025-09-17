---
title: Getting a list of chats - Chats | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/getChats
crawled_at: 2025-09-17T14:41:22.617921
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#query-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body)
    * [ChatContextDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontextdto)
    * [ChatStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatstatustype)
    * [ChatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chattype)
    * [ChatContextIdentifiableType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontextidentifiabletype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body1)
    * [GetChatsInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#getchatsinfodto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype)
    * [GetChatInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#getchatinfodto)
    * [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#forwardscrollingpagerdto)
    * [ChatFullContextDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatfullcontextdto)
    * [ChatContextType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontexttype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body7)


# Getting available chats
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/_auto/scopes_summary/pages/communication)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns chats with customers.
Enable API notifications
Yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/push-notifications/reference/sendNotification) when a new chat or message appears.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/push-notifications/)
Restriction for the parameter `limit`
Do not pass a value greater than 20.
**, Limit:** 10,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/chats

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body)Body
application/json
```
{
    "orderIds": [
        0
    ],
    "contexts": [
        {
            "type": "ORDER",
            "id": 0
        }
    ],
    "types": [
        "CHAT"
    ],
    "statuses": [
        "NEW"
    ]
}

```

**Name** |  **Description**  
---|---  
contexts |  **Type:** [ChatContextDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontextdto)[] Filter by orders or refunds for which chats have been started.  
Information about the order or refund for which the chat was started. _Min items:_ `1` _Unique items_  
orderIds ⦸ |  **Type:** integer<int64>[] Filter by order IDs on the Market.  
_Min items:_ `1` _Unique items_  
statuses |  **Type:** [ChatStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatstatustype)[] Filter by chat statuses.  
Chat status:
  * `NEW` — new chat.
  * `WAITING_FOR_CUSTOMER` — we need a buyer's response.
  * `WAITING_FOR_PARTNER` — we need the store's response.
  * `WAITING_FOR_ARBITER` — we need an arbitrator's answer.
  * `WAITING_FOR_MARKET` — we need a response from Yandex. Market.
  * `FINISHED` — the chat is over.

_Enum:_ `NEW`, `WAITING_FOR_CUSTOMER`, `WAITING_FOR_PARTNER`, `WAITING_FOR_ARBITER`, `WAITING_FOR_MARKET`, `FINISHED` _Min items:_ `1` _Unique items_  
types |  **Type:** [ChatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chattype)[] Filter by chat types.  
Chat type:
  * `CHAT` — chat with the buyer.
  * `ARBITRAGE` — an argument.

_Enum:_ `CHAT`, `ARBITRAGE` _Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontextdto)ChatContextDTO
Information about the order or refund for which the chat was started.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The order or refund ID. _Min value:_ `1`  
type* |  **Type:** [ChatContextIdentifiableType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontextidentifiabletype) Chat type:
  * `ORDER` — on orders. Read more about order chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `RETURN` — for refunds (FBY, FBS and Express). Read more about refund chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).

_Enum:_ `ORDER`, `RETURN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatstatustype)ChatStatusType
Chat status:
  * `NEW` — new chat.
  * `WAITING_FOR_CUSTOMER` — we need a buyer's response.
  * `WAITING_FOR_PARTNER` — we need the store's response.
  * `WAITING_FOR_ARBITER` — we need an arbitrator's answer.
  * `WAITING_FOR_MARKET` — we need a response from Yandex. Market.
  * `FINISHED` — the chat is over.

**Type** |  **Description**  
---|---  
[ChatStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatstatustype) |  _Enum:_ `NEW`, `WAITING_FOR_CUSTOMER`, `WAITING_FOR_PARTNER`, `WAITING_FOR_ARBITER`, `WAITING_FOR_MARKET`, `FINISHED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chattype)ChatType
Chat type:
  * `CHAT` — chat with the buyer.
  * `ARBITRAGE` — an argument.

**Type** |  **Description**  
---|---  
[ChatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chattype) |  _Enum:_ `CHAT`, `ARBITRAGE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontextidentifiabletype)ChatContextIdentifiableType
Chat type:
  * `ORDER` — on orders. Read more about order chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `RETURN` — for refunds (FBY, FBS and Express). Read more about refund chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).

**Type** |  **Description**  
---|---  
[ChatContextIdentifiableType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontextidentifiabletype) |  _Enum:_ `ORDER`, `RETURN`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#200-ok)200 OK
A list of chats.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "chats": [
            {
                "chatId": 0,
                "orderId": 0,
                "context": {
                    "type": "ORDER",
                    "orderId": 0,
                    "returnId": 0
                },
                "type": "CHAT",
                "status": "NEW",
                "createdAt": "2017-11-21T00:00:00+03:00",
                "updatedAt": "2017-11-21T00:00:00+03:00"
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
result |  **Type:** [GetChatsInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#getchatsinfodto) A list of chats.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#getchatsinfodto)GetChatsInfoDTO
A list of chats.
**Name** |  **Description**  
---|---  
chats* |  **Type:** [GetChatInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#getchatinfodto)[] Information about chats.  
Information about the chat.  
paging |  **Type:** [ForwardScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#forwardscrollingpagerdto) The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#getchatinfodto)GetChatInfoDTO
Information about the chat.
**Name** |  **Description**  
---|---  
chatId* |  **Type:** integer<int64> The chat ID. _Min value:_ `1`  
context* |  **Type:** [ChatFullContextDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatfullcontextdto) Information about the order or refund for which the chat was started.  
createdAt* |  **Type:** string<date-time> Date and time when the chat was created. Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
status* |  **Type:** [ChatStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatstatustype) Chat status:
  * `NEW` — new chat.
  * `WAITING_FOR_CUSTOMER` — we need a buyer's response.
  * `WAITING_FOR_PARTNER` — we need the store's response.
  * `WAITING_FOR_ARBITER` — we need an arbitrator's answer.
  * `WAITING_FOR_MARKET` — we need a response from Yandex. Market.
  * `FINISHED` — the chat is over.

_Enum:_ `NEW`, `WAITING_FOR_CUSTOMER`, `WAITING_FOR_PARTNER`, `WAITING_FOR_ARBITER`, `WAITING_FOR_MARKET`, `FINISHED`  
type* |  **Type:** [ChatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chattype) Chat type:
  * `CHAT` — chat with the buyer.
  * `ARBITRAGE` — an argument.

_Enum:_ `CHAT`, `ARBITRAGE`  
updatedAt* |  **Type:** string<date-time> The date and time of the last message in the chat. Date format: ISO 8601 with an offset relative to UTC. _Example:_ `2017-11-21T00:00:00+03:00`  
orderId ⦸ |  **Type:** integer<int64> The order ID. _Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#forwardscrollingpagerdto)ForwardScrollingPagerDTO
The ID of the next page.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatfullcontextdto)ChatFullContextDTO
Information about the order or refund for which the chat was started.
**Name** |  **Description**  
---|---  
type* |  **Type:** [ChatContextType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontexttype) Chat type:
  * `ORDER` — on orders. Read more about order chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `RETURN` — for refunds (FBY, FBS and Express). Read more about refund chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `DIRECT` — the chat that the customer started. Read more about this type in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/with-users).

_Enum:_ `ORDER`, `RETURN`, `DIRECT`  
orderId |  **Type:** integer<int64> The order ID. It is returned for orders and refunds. _Min value:_ `1`  
returnId |  **Type:** integer<int64> The refund ID. It is returned only for refunds. _Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontexttype)ChatContextType
Chat type:
  * `ORDER` — on orders. Read more about order chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `RETURN` — for refunds (FBY, FBS and Express). Read more about refund chats in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/about-orders).
  * `DIRECT` — the chat that the customer started. Read more about this type in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/communication/with-users).

**Type** |  **Description**  
---|---  
[ChatContextType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#chatcontexttype) |  _Enum:_ `ORDER`, `RETURN`, `DIRECT`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Query parameters
page_token:
limit:
Body{ "orderIds": [ 0 ], "contexts": [ { "type": "ORDER", "id": 0 } ], "types": [ "CHAT" ], "statuses": [ "NEW" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Getting a single chat](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChat)
Next
[Receiving a message](https://yandex.ru/dev/market/partner-api/doc/en/reference/chats/en/reference/chats/getChatMessage)
