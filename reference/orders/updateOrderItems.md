---
title: Removing items from an order - DBS orders | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/updateOrderItems
crawled_at: 2025-09-17T14:31:05.625265
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body)
    * [OrderItemModificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#orderitemmodificationdto)
    * [OrderItemsModificationRequestReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#orderitemsmodificationrequestreasontype)
    * [BriefOrderItemInstanceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#brieforderiteminstancedto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#200-ok)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body6)


# Removing items from an order or reducing their number
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


If you work according to the FBS model
Use the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout).
Deletes one or more items from the order if the store cannot deliver them all.
The order must have the status `"status": "PROCESSING"` the processing stage `"substatus": "STARTED"`. The composition cannot be changed after the transfer of the status. `"substatus": "READY_TO_SHIP"`.
Reduce the number of identical products
Pass the updated value in the parameter `count`.
Delete an item from an order
Pass the value `0` in the parameter `count` or don't pass it on `item`.
You cannot delete or reduce the quantity of an item if it:
  * added by special offer;
  * amounts to 99% of the order value;
  * the only product in the order.


In this case, cancel the order in the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatus) send the order status `CANCELLED` with the reason for cancellation `SHOP_FAILED`.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#money)How will the money be refunded
If the customer paid for the product at checkout, the Market will refund the money for the items removed from the order within two days:
  * when paying with a bank card — from the moment when the store transfers the order to the status `SHIPPED`;
  * when paying via Apple Pay or Google Pay — from the moment when the store removes the product from the order.

**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#request)Request
PUT
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/items

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body)Body
application/json
```
{
    "items": [
        {
            "id": 0,
            "count": 0,
            "instances": [
                {
                    "cis": "string",
                    "uin": "string",
                    "rnpt": "string",
                    "gtd": "string",
                    "countryCode": "RU"
                }
            ]
        }
    ],
    "reason": "PARTNER_REQUESTED_REMOVE"
}

```

**Name** |  **Description**  
---|---  
items* |  **Type:** [OrderItemModificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#orderitemmodificationdto)[] The list of products in the order. If the store has not provided information about the product in the input data, it will be removed from the order. Required parameter.   
The list of products in the order. If the store has not provided information about the product in the input data, it will be removed from the order. Required parameter. _Min items:_ `1`  
reason |  **Type:** [OrderItemsModificationRequestReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#orderitemsmodificationrequestreasontype) The reason why the order composition has been updated:
  * `PARTNER_REQUESTED_REMOVE` — the store has deleted the product.
  * `USER_REQUESTED_REMOVE` — the buyer asked to delete the product.

_Enum:_ `PARTNER_REQUESTED_REMOVE`, `USER_REQUESTED_REMOVE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#orderitemmodificationdto)OrderItemModificationDTO
The list of products in the order.
If the store has not provided information about the product in the input data, it will be removed from the order.
Required parameter.
**Name** |  **Description**  
---|---  
count* |  **Type:** integer<int32> The new quantity of the product. _Min value:_ `0`  
id* |  **Type:** integer<int64> The identifier of the product within the order. You can get the ID using resources [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrders) or [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrder). Required parameter.  
instances |  **Type:** [BriefOrderItemInstanceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#brieforderiteminstancedto)[] Information about the labeling of product units. In the request, specify all the items to be labeled. A required parameter if the order from the business contains products that are subject to labeling in the system.   
Product unit ID. Fill in only one field, depending on which system the product is labeled in. Detailed information about working with labeled products is provided [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/orders/cz.html). _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#orderitemsmodificationrequestreasontype)OrderItemsModificationRequestReasonType
The reason why the order composition has been updated:
  * `PARTNER_REQUESTED_REMOVE` — the store has deleted the product.
  * `USER_REQUESTED_REMOVE` — the buyer asked to delete the product.

**Type** |  **Description**  
---|---  
[OrderItemsModificationRequestReasonType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#orderitemsmodificationrequestreasontype) |  _Enum:_ `PARTNER_REQUESTED_REMOVE`, `USER_REQUESTED_REMOVE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#brieforderiteminstancedto)BriefOrderItemInstanceDTO
Product unit ID.
Fill in only one field, depending on which system the product is labeled in.
Detailed information about working with labeled goods is provided [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/orders/cz.html).
**Name** |  **Description**  
---|---  
cis |  **Type:** string The unit identification code in the system  Meaning `cis` must match the regular expression: `^(?=.{1,256}$)\u001D?(\(?01\)?\d{14}\(?21\)?([!-~]{6}<code>&#124;</code>[!-~]{8}<code>&#124;</code>[!-~]{13}<code>&#124;</code>[!-~]{20})(\u001D\(?240\)?.{1,30})?\u001D\(?9[1,3]\)?.+)$`. Without the cryptotail — `^(?=[!-~]{1,256}$)(\(?01\)?\d{14}\(?21\)?(.{6}<code>&#124;</code>.{8}<code>&#124;</code>.{13}<code>&#124;</code>.{20}))$`. Do not escape the slash in the separator character code. `\u001d` ✅ `01030410947874432155Qbag!\u001d93Zjqw` ❌ `01030410947874432155Qbag!\\u001d93Zjqw` Escape slashes and quotation marks in other places according to the JSON rules.: `\\` and `\"`  
countryCode |  **Type:** string The country of manufacture is in the ISO 3166-1 alpha-2 format. [How to get](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/regions/getRegionsCodes) _Example:_ `RU` _Min length:_ `2` _Max length:_ `2` _Pattern:_ `^[A-Z]{2}$`  
gtd |  **Type:** string Cargo customs declaration. It is a string of three numbers separated by a slash: XXXXXXXXXX/XXXXXXXX/XXXXXXXX. The first part is the code of the customs office that registered the declaration for imported goods. Next is the date and number of the declaration.  
rnpt |  **Type:** string The registration number of the product batch. It is a string of four numbers separated by slashes: XXXXXXXXXX/XXXXXXXX/XXXXXXXX/XXX. The first part is the code of the customs office that registered the declaration for the shipment. Next is the date, the number of the declaration and the number of the marked product in the declaration.  
uin |  **Type:** string The unique identification number of the jewelry. It is a 16-digit number.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#200-ok)200 OK
Yandex. Market has successfully processed your request. No output is expected.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderItems#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
Body{ "items": [ { "id": 0, "count": 0, "instances": [ { "cis": "string", "uin": "string", "rnpt": "string", "gtd": "string", "countryCode": "RU" } ] } ], "reason": "PARTNER_REQUESTED_REMOVE" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Sending the confirmation code](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/verifyOrderEac)
Next
[Sending the parcel's track number](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderDeliveryTrackCode)
