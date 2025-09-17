---
title: Transfer of digital goods keys - Digital DBS orders | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/provideOrderDigitalCodes
crawled_at: 2025-09-17T14:31:51.587997
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body)
    * [OrderDigitalItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#orderdigitalitemdto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body1)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body7)


# Transfer of digital goods keys
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs) model.**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


Transfers the keys of the digital goods that the buyer ordered and paid for. After completing the request, yandex.Market will send him an email with the keys and activation instructions. If the email is delivered, yandex.Market will transfer the order to the final status. `DELIVERED`.
After sending the code to the buyer, the order status will not change immediately.
Enable API notifications, and yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/push-notifications/reference/sendNotification) When the order status changes to `DELIVERED`.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/push-notifications/)
The key must be transferred within 30 minutes after the order status changes. `PROCESSING`.
If one order includes several keys, send them all in one request.
Each product has a unique `id` pass it as a separate element in the array. `items`, and the product keys are in the array `codes`.
Example
```
{
  "items": [
    {
      "id": 1,
      "codes": [
        "code1", "code2", "code3"
      ],
      "slip": "slip",
      "activate_till": "2025-02-18"
    },
    {
      "id": 2,
      "codes": [
        "code4", "code5", "code6"
      ],
      "slip": "slip",
      "activate_till": "2025-02-18"
    }
  ]
}

```

Products with the same `id` you can also pass different elements in the array. `items`.
Example
```
{
  "items": [
    {
      "id": 1,
      "codes": [
        "code1", "code2"
      ],
      "slip": "slip",
      "activate_till": "2025-02-18"
    },
    {
      "id": 1,
      "codes": [
        "code3"
      ],
      "slip": "slip",
      "activate_till": "2025-02-18"
    }
  ]
}

```

**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/deliverDigitalGoods

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body)Body
application/json
```
{
    "items": [
        {
            "id": 0,
            "code": "string",
            "codes": [
                "string"
            ],
            "slip": "string",
            "activate_till": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
items* |  **Type:** [OrderDigitalItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#orderdigitalitemdto)[] The list of products sold. If there are several items in the order **identical** products (for example, multiple keys to the same subscription), pass the keys as an array to this product. Parameter `id` these elements should have the same one.   
A digital product. _Min items:_ `1` _Max items:_ `100`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#orderdigitalitemdto)OrderDigitalItemDTO
A digital product.
**Name** |  **Description**  
---|---  
activate_till* |  **Type:** string<date> The date before which you need to activate the keys. If the keys are valid indefinitely, specify any date in the distant future. Date format: `YYYY-MM-DD`.  
id* |  **Type:** integer<int64> The product ID in the order. It comes in response to a request [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrder) — parameter `id` in `items`.  
slip* |  **Type:** string Activation instructions. You can use HTML tags to format the text:
  * <h>, <h1>, <h2> and so on — for headings;
  * <br> and <p> — for line breaks.
  * <ol> — for a numbered list.
  * <ul> — for a bulleted list.
  * <li> — to create list items (must be inside <ol> or <ul>);
  * <div> — supported, but does not affect the text display.

_Max length:_ `10000`  
code ⦸ |  **Type:** string Instead, use `codes` Using both parameters together will result in an error. The key itself.  
codes |  **Type:** string[] Keys related to the product.  
_Min items:_ `1` _Max items:_ `5000` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#200-ok)200 OK
An empty answer.
Answer `200` By itself, it does not mean that the keys have been transferred to the buyer.
If the email with the keys was delivered, yandex.Market will transfer the order to the final status. `DELIVERED`.
The order status can be found using the method [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrder) or [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrders).
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body1)Body
application/json
```
{
    "status": "OK"
}

```

**Name** |  **Description**  
---|---  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderDigitalCodes#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
Body{ "items": [ { "id": 0, "code": "string", "codes": [ "string" ], "slip": "string", "activate_till": "string" } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Cancellation of the order by the buyer](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/acceptOrderCancellation)
Next
[Information about the buyer](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/order-business-information/getOrderBusinessBuyerInfo)
