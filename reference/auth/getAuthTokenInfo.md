---
title: Information about the authorization token - Reference books | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/getAuthTokenInfo
crawled_at: 2025-09-17T14:22:59.198492
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#request)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body)
    * [TokenDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#tokendto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype)
    * [ApiKeyDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apikeydto)
    * [ApiKeyScopeType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apikeyscopetype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body3)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body4)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body5)


# Getting information about the authorization token
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/pricing_read-only)
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/promotion_read-only)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/finance-and-accounting)
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/communication)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/settings-management)
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


The method is only available for the Api Key token.
Returns information about the transmitted authorization token.
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/auth/token

```

##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#200-ok)200 OK
Information about the authorization token.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body)Body
application/json
```
{
    "status": "OK",
    "result": {
        "apiKey": {
            "name": "string",
            "authScopes": [
                "ALL_METHODS"
            ]
        }
    }
}

```

**Name** |  **Description**  
---|---  
result* |  **Type:** [TokenDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#tokendto) Information about the authorization token.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#tokendto)TokenDTO
Information about the authorization token.
**Name** |  **Description**  
---|---  
apiKey* |  **Type:** [ApiKeyDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apikeydto) Information about the Api Key token.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apikeydto)ApiKeyDTO
Information about the Api Key token.
**Name** |  **Description**  
---|---  
authScopes* |  **Type:** [ApiKeyScopeType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apikeyscopetype)[] Access to methods using the Api Key token.  
Access to methods:
  * `ALL_METHODS` — full cabinet management.
  * `ALL_METHODS_READ_ONLY` — view all information in the cabinet.
  * `INVENTORY_AND_ORDER_PROCESSING` — order processing and accounting of goods.
  * `INVENTORY_AND_ORDER_PROCESSING_READ_ONLY` — view information about orders.
  * `PRICING` — price management.
  * `PRICING_READ_ONLY` — view prices.
  * `OFFERS_AND_CARDS_MANAGEMENT` — management of goods and cards.
  * `OFFERS_AND_CARDS_MANAGEMENT_READ_ONLY` — view products and cards.
  * `PROMOTION` — product promotion.
  * `PROMOTION_READ_ONLY` — view information about product promotions.
  * `FINANCE_AND_ACCOUNTING` — View financial information and statements.
  * `COMMUNICATION` — communication with customers.
  * `SETTINGS_MANAGEMENT` — setting up stores.
  * `SUPPLIES_MANAGEMENT_READ_ONLY` — receiving information on FBY applications.

_Enum:_ `ALL_METHODS`, `ALL_METHODS_READ_ONLY`, `INVENTORY_AND_ORDER_PROCESSING`, `INVENTORY_AND_ORDER_PROCESSING_READ_ONLY`, `PRICING`, `PRICING_READ_ONLY`, `OFFERS_AND_CARDS_MANAGEMENT`, `OFFERS_AND_CARDS_MANAGEMENT_READ_ONLY`, `PROMOTION`, `PROMOTION_READ_ONLY`, `FINANCE_AND_ACCOUNTING`, `COMMUNICATION`, `SETTINGS_MANAGEMENT`, `SUPPLIES_MANAGEMENT_READ_ONLY` _Unique items_  
name* |  **Type:** string The name of the token. _Min length:_ `1` _Max length:_ `100`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apikeyscopetype)ApiKeyScopeType
Access to methods:
  * `ALL_METHODS` — full cabinet management.
  * `ALL_METHODS_READ_ONLY` — view all information in the cabinet.
  * `INVENTORY_AND_ORDER_PROCESSING` — order processing and accounting of goods.
  * `INVENTORY_AND_ORDER_PROCESSING_READ_ONLY` — view information about orders.
  * `PRICING` — price management.
  * `PRICING_READ_ONLY` — view prices.
  * `OFFERS_AND_CARDS_MANAGEMENT` — management of goods and cards.
  * `OFFERS_AND_CARDS_MANAGEMENT_READ_ONLY` — view products and cards.
  * `PROMOTION` — product promotion.
  * `PROMOTION_READ_ONLY` — view information about product promotions.
  * `FINANCE_AND_ACCOUNTING` — View financial information and statements.
  * `COMMUNICATION` — communication with customers.
  * `SETTINGS_MANAGEMENT` — setting up stores.
  * `SUPPLIES_MANAGEMENT_READ_ONLY` — receiving information on FBY applications.

**Type** |  **Description**  
---|---  
[ApiKeyScopeType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apikeyscopetype) |  _Enum:_ `ALL_METHODS`, `ALL_METHODS_READ_ONLY`, `INVENTORY_AND_ORDER_PROCESSING`, `INVENTORY_AND_ORDER_PROCESSING_READ_ONLY`, `PRICING`, `PRICING_READ_ONLY`, `OFFERS_AND_CARDS_MANAGEMENT`, `OFFERS_AND_CARDS_MANAGEMENT_READ_ONLY`, `PROMOTION`, `PROMOTION_READ_ONLY`, `FINANCE_AND_ACCOUNTING`, `COMMUNICATION`, `SETTINGS_MANAGEMENT`, `SUPPLIES_MANAGEMENT_READ_ONLY`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/auth/getAuthTokenInfo#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Market Warehouse Ids (FBY)](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/warehouses/getFulfillmentWarehouses)
Next
[Directory of delivery services](https://yandex.ru/dev/market/partner-api/doc/en/reference/auth/en/reference/orders/getDeliveryServices)
