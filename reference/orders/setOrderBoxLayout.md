---
title: Order preparation - Changing the order | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/setOrderBoxLayout
crawled_at: 2025-09-17T14:23:41.493563
---

  * [How to send information about the distribution of goods](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#how-to-send-information-about-the-distribution-of-goods)
  * [How to transfer marking codes](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#how-to-transfer-marking-codes)
  * [How to remove an item from an order](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#how-to-remove-an-item-from-an-order)
  * [Examples](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#examples)
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body)
    * [OrderBoxLayoutDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutdto)
    * [OrderBoxLayoutItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutitemdto)
    * [BriefOrderItemInstanceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#brieforderiteminstancedto)
    * [OrderBoxLayoutPartialCountDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutpartialcountdto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body1)
    * [OrderBoxesLayoutDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxeslayoutdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype)
    * [EnrichedOrderBoxLayoutDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#enrichedorderboxlayoutdto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body7)


# Order preparation
Info
Console
**The method is available for models:[FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


It is also suitable for DBS
The query is designed to work with FBS orders, but you can use it to process DBS orders if it is convenient.
Allows you to perform three operations:
  * send information about the distribution of goods by boxes to the Market;
  * send the labeling codes for the products to the Market;
  * remove an item from the order if it is not in stock.


If you need to correct something in the transmitted data, simply repeat the request. You can do this as many times as you want before the order status is changed. **Ready for shipment**. If you change the layout after printing and pasting the labels, do not forget to reprint them and paste them again.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#how-to-send-information-about-the-distribution-of-goods)How to send information about the distribution of goods
In this request, you need to send the Market a list of boxes and specify which products are in each of them. There are two types of boxes:
  * **Containing the entire product.** Such a box can contain any number of items of any kind.
  * **Containing a part of the product.** Such boxes contain one part of each product. For example, one contains an external air conditioner unit, and the other contains an internal unit.


One box cannot contain both the whole goods and parts of the goods.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#how-to-transfer-marking-codes)How to transfer marking codes
Labeling of goods in the system 
For business orders, you still need to send the labeling codes.
If the order contains products subject to labeling, the corresponding unique codes must be provided in the request. [What is labeling?](https://yandex.ru/support/marketplace/orders/cz.html)
The following types of codes are accepted:
  * Codes in the system 
  * WIN for jewelry.
  * RNPT and GTD for imported traceable goods.


For each item in the order that requires labeling, you need to send a list of codes, one for each item. For example, if there are two pairs of slippers and one pair of shoes in the order, you will get a list of two codes for the first position and a list of one code for the second.
If the product is traveling in several boxes, the labeling code must be transmitted for each of them.
For orders that contain jewelry
The order status will change to `READY_TO_SHIP`, only when:
  1. You will give the Store the blame for each piece of jewelry in the order.
  2. All plugins will be successfully verified. [How to get LOGin verification statuses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus)


##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#how-to-remove-an-item-from-an-order)How to remove an item from an order
To remove an item from an order:
  1. Add to the request `allowRemove: true`.
  2. Transfer the distribution to boxes without the item to be removed.


Deletion cannot be undone
This operation is irreversible: the buyer will immediately receive a notification, and the order composition will change.
To delete an entire position, do not pass the corresponding `OrderBoxLayoutItemDTO`. To reduce the quantity of the product, pass the reduced value in the field `fullCount`.
You cannot delete or reduce the quantity of an item if it:
  * added by special offer;
  * amounts to 99% of the order value;
  * the only product in the order.


If you are unable to ship such an item, cancel the order. To do this, send a request using the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatus) and send the order status `CANCELLED` with the reason for cancellation `SHOP_FAILED`.
You can't increase the order
You cannot use a query to increase the number of identical items, add new items to an order, or replace one item with another.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#examples)Examples
The product fits in a box
This is what the request will look like if they are traveling in the same box:
  * three units of the same product that require labeling;
  * one unit of another product that does not require labeling.


```
{
    "boxes": [
        {
            "items": [
                {
                    "id": 123456,
                    "fullCount": 3,
                    "instances": [
                        {
                            "cis": "01030410947874432155Qbag!\u001d93Zjqw"
                        },
                        {
                            "cis": "010304109478gftJ14545762!\u001dhGt264"
                        },
                        {
                            "cis": "010304109478fRs28323ks23!\u001dhet201"
                        }
                    ]
                },
                {
                    "id": 654321,
                    "fullCount": 1
                }
            ]
        }
    ]
}

```

The goods are traveling in different boxes
This is what the request will look like if the product comes in two boxes:
```
{
    "boxes": [
        {
            "items": [
                {
                    "id": 123456,
                    "partialCount": {
                        "current": 1,
                        "total": 2
                    },
                    "instances": [
                        {
                            "cis": "01030410947874432155Qbag!\u001d93Zjqw"
                        }
                    ]
                }
            ]
        },
        {
            "items": [
                {
                    "id": 123456,
                    "partialCount": {
                        "current": 2,
                        "total": 2
                    },
                    "instances": [
                        {
                            "cis": "01030410947874432155Qbag!\u001d93Zjqw"
                        }
                    ]
                }
            ]
        }
    ]
}

```

Identical goods, where everyone travels in several boxes
This is what the request will look like if each of the two identical products travels in two boxes:
```
{
    "boxes": [
        {
            "items": [
                {
                    "id": 123456,
                    "partialCount": {
                        "current": 1,
                        "total": 2
                    },
                    "instances": [
                        {
                            "cis": "01030410947874432155Qbag!\u001d93Zjqw"
                        }
                    ]
                }
            ]
        },
        {
            "items": [
                {
                    "id": 123456,
                    "partialCount": {
                        "current": 2,
                        "total": 2
                    },
                    "instances": [
                        {
                            "cis": "01030410947874432155Qbag!\u001d93Zjqw"
                        }
                    ]
                }
            ]
        },
        {
            "items": [
                {
                    "id": 123456,
                    "partialCount": {
                        "current": 1,
                        "total": 2
                    },
                    "instances": [
                        {
                            "cis": "01030410947874432155Qbag!\u001d93Zjqw"
                        }
                    ]
                }
            ]
        },
        {
            "items": [
                {
                    "id": 123456,
                    "partialCount": {
                        "current": 2,
                        "total": 2
                    },
                    "instances": [
                        {
                            "cis": "01030410947874432155Qbag!\u001d93Zjqw"
                        }
                    ]
                }
            ]
        }
    ]
}

```

**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#request)Request
PUT
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/boxes

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body)Body
application/json
```
{
    "boxes": [
        {
            "items": [
                {
                    "id": 0,
                    "fullCount": 0,
                    "partialCount": {
                        "current": 0,
                        "total": 0
                    },
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
            ]
        }
    ],
    "allowRemove": false
}

```

**Name** |  **Description**  
---|---  
boxes* |  **Type:** [OrderBoxLayoutDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutdto)[] A list of boxes.  
Information about the box. _Min items:_ `1`  
allowRemove |  **Type:** boolean Pass it on `true` if you are going to remove some of the items from the order. _Default:_ `false`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutdto)OrderBoxLayoutDTO
Information about the box.
**Name** |  **Description**  
---|---  
items* |  **Type:** [OrderBoxLayoutItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutitemdto)[] The list of products in the box. If there is a part of a large product in the box, there can be only one item in the list.   
Information about the product in the box. _Min items:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutitemdto)OrderBoxLayoutItemDTO
Information about the product in the box.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The product ID in the order. It comes in response to a request [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrder) — parameter `id` in `items`.  
fullCount |  **Type:** integer<int32> The number of items in a box. Use this field if there are whole items in the box that are not divided into parts. Do not use this field at the same time as `partialCount`. _Min value:_ `1`  
instances |  **Type:** [BriefOrderItemInstanceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#brieforderiteminstancedto)[] The marking codes you provided.  
Product unit ID. Fill in only one field, depending on which system the product is labeled in. Detailed information about working with labeled goods is provided [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/orders/cz.html). _Min items:_ `1`  
partialCount |  **Type:** [OrderBoxLayoutPartialCountDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutpartialcountdto) Part of the product is in the box. Use this field if a part of a large item is in the box. Do not use this field at the same time as `fullCount`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#brieforderiteminstancedto)BriefOrderItemInstanceDTO
Product unit ID.
Fill in only one field, depending on which system the product is labeled in.
Detailed information about working with labeled products is provided [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/orders/cz.html).
**Name** |  **Description**  
---|---  
cis |  **Type:** string The unit identification code in the system  Meaning `cis` must match the regular expression: `^(?=.{1,256}$)\u001D?(\(?01\)?\d{14}\(?21\)?([!-~]{6}<code>&#124;</code>[!-~]{8}<code>&#124;</code>[!-~]{13}<code>&#124;</code>[!-~]{20})(\u001D\(?240\)?.{1,30})?\u001D\(?9[1,3]\)?.+)$`. Without the cryptotail — `^(?=[!-~]{1,256}$)(\(?01\)?\d{14}\(?21\)?(.{6}<code>&#124;</code>.{8}<code>&#124;</code>.{13}<code>&#124;</code>.{20}))$`. Do not escape the slash in the separator character code. `\u001d` ✅ `01030410947874432155Qbag!\u001d93Zjqw` ❌ `01030410947874432155Qbag!\\u001d93Zjqw` Escape slashes and quotation marks in other places according to the JSON rules.: `\\` and `\"`  
countryCode |  **Type:** string The country of manufacture is in the ISO 3166-1 alpha-2 format. [How to get](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/regions/getRegionsCodes) _Example:_ `RU` _Min length:_ `2` _Max length:_ `2` _Pattern:_ `^[A-Z]{2}$`  
gtd |  **Type:** string Cargo customs declaration. It is a string of three numbers separated by a slash: XXXXXXXXXX/XXXXXXXX/XXXXXXXX. The first part is the code of the customs office that registered the declaration for imported goods. Next is the date and number of the declaration.  
rnpt |  **Type:** string The registration number of the product batch. It is a string of four numbers separated by a slash: XXXXXXXXXX/XXXXXXXX/XXXXXXXX/XXX. The first part is the code of the customs office that registered the declaration for the shipment. Next is the date, the number of the declaration and the number of the marked product in the declaration.  
uin |  **Type:** string The unique identification number of the jewelry. It is a 16-digit number.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutpartialcountdto)OrderBoxLayoutPartialCountDTO
Information about the part of the product in the box.
**Name** |  **Description**  
---|---  
current* |  **Type:** integer<int32> The part number, starting from 1. _Min value:_ `1`  
total* |  **Type:** integer<int32> The total number of parts the product is divided into. _Min value:_ `2`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#200-ok)200 OK
In response, you will receive the transmitted layout with the box IDs. You will need them to request labels.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "boxes": [
            {
                "items": [
                    {
                        "id": 0,
                        "fullCount": 0,
                        "partialCount": {
                            "current": 0,
                            "total": 0
                        },
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
                "boxId": 0
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OrderBoxesLayoutDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxeslayoutdto) Distribution of goods by boxes.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxeslayoutdto)OrderBoxesLayoutDTO
Distribution of goods by boxes.
**Name** |  **Description**  
---|---  
boxes* |  **Type:** [EnrichedOrderBoxLayoutDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#enrichedorderboxlayoutdto)[] A list of boxes.  
Information about the box.  
Information about the box.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#enrichedorderboxlayoutdto)EnrichedOrderBoxLayoutDTO
Information about the box.
**Name** |  **Description**  
---|---  
items* |  **Type:** [OrderBoxLayoutItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#orderboxlayoutitemdto)[] The list of products in the box. If there is a part of a large product in the box, there can be only one item in the list.   
Information about the product in the box. _Min items:_ `1`  
boxId |  **Type:** integer<int64> The ID of the box.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
Body{ "boxes": [ { "items": [ { "id": 0, "fullCount": 0, "partialCount": { "current": 0, "total": 0 }, "instances": [ { "cis": "string", "uin": "string", "rnpt": "string", "gtd": "string", "countryCode": "RU" } ] } ] } ], "allowRemove": false }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[About the order list](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrders)
Next
[Transmitting an external order ID](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateExternalOrderId)
