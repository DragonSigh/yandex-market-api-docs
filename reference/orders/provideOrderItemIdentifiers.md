---
title: Transmission of marking codes - Labeling of goods | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/provideOrderItemIdentifiers
crawled_at: 2025-09-17T14:30:49.814576
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body)
    * [OrderItemInstanceModificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderiteminstancemodificationdto)
    * [BriefOrderItemInstanceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#brieforderiteminstancedto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body1)
    * [OrderItemsModificationResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderitemsmodificationresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype)
    * [BriefOrderItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#brieforderitemdto)
    * [OrderItemInstanceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderiteminstancedto)
    * [OrderVatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#ordervattype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body7)


# Transfer of unit marking codes
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/overview/dbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * all-methods — Full account management


If you work according to the FBS model
Use the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/setOrderBoxLayout).
Transmits the labeling codes for the product units in the specified order to the Market.
Labeling of goods in the system **optional** for orders from individuals, but **required** for business orders.
The following types of codes are accepted:
  * Codes in the system 
  * WIN for jewelry.
  * RNPT and GTD for imported traceable goods.


Before working with this method
Be sure to read it [an article about working with labeled goods](https://yandex.ru/support/marketplace/orders/cz.html).
For each item in the order that requires labeling, you need to send a list of codes, one for each item. For example, if there are two pairs of slippers and one pair of shoes in the order, you will get a list of two codes for the first position and a list of one code for the second.
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#request)Request
PUT
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/orders/{orderId}/identifiers

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
orderId* |  **Type:** integer<int64> The order ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body)Body
application/json
```
{
    "items": [
        {
            "id": 0,
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

```

**Name** |  **Description**  
---|---  
items* |  **Type:** [OrderItemInstanceModificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderiteminstancemodificationdto)[] A list of items that require labeling.   
An item in the shopping cart that requires labeling.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderiteminstancemodificationdto)OrderItemInstanceModificationDTO
An item in the shopping cart that requires labeling.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> The product ID in the order. It comes in response to a request [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrder) — parameter `id` in `items`.  
instances* |  **Type:** [BriefOrderItemInstanceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#brieforderiteminstancedto)[] A list of item labeling codes.   
Product unit ID. Fill in only one field, depending on which system the product is labeled in. Detailed information about working with labeled goods is provided [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/orders/cz.html).  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#brieforderiteminstancedto)BriefOrderItemInstanceDTO
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
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#200-ok)200 OK
Answer `200` indicates that the codes were successfully recorded. The response contains brief information about the marked products.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "items": [
            {
                "id": 0,
                "vat": "NO_VAT",
                "count": 0,
                "price": 0,
                "offerName": "string",
                "offerId": "string",
                "instances": [
                    {
                        "cis": "string",
                        "cisFull": "string",
                        "uin": "string",
                        "rnpt": "string",
                        "gtd": "string",
                        "countryCode": "RU"
                    }
                ]
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OrderItemsModificationResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderitemsmodificationresultdto) Brief information about the marked goods. The parameter is returned if the response is `OK`.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderitemsmodificationresultdto)OrderItemsModificationResultDTO
Brief information about the marked goods. The parameter is returned if the response is `OK`.
**Name** |  **Description**  
---|---  
items* |  **Type:** [BriefOrderItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#brieforderitemdto)[] The list of items in the order to be marked.  
Information about the labeled product.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#brieforderitemdto)BriefOrderItemDTO
Information about the labeled product.
**Name** |  **Description**  
---|---  
count |  **Type:** integer<int32> The number of product units.  
id |  **Type:** integer<int64> The product ID in the order. Allows you to identify the product within the scope of this order.  
instances |  **Type:** [OrderItemInstanceDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderiteminstancedto)[] The marking codes you provided.  
The marking or fault codes you have provided for this position. The "Honest Sign" codes are returned in two versions — with and without a cryptotail. _Min items:_ `1`  
offerId |  **Type:** string Your product ID. _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
offerName |  **Type:** string Product name.  
price |  **Type:** number The price of the product. It is specified in the currency that was specified in the catalog. The separator of the whole and fractional parts is a dot.  
vat |  **Type:** [OrderVatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#ordervattype) Value added tax (VAT) on the product:
  * `NO_VAT` — VAT is not charged, it is used only for certain types of services.
  * `VAT_0` — 0% VAT. For example, it is used for the sale of goods exported in the customs procedure of export, or for the provision of services for the international transportation of goods.
  * `VAT_10` — 10% VAT. For example, it is used in the sale of certain food and medical products.
  * `VAT_10_110` — VAT 10/110. 10% VAT, applicable only for prepayment.
  * `VAT_20` — 20% VAT. Basic VAT starting in 2019.
  * `VAT_20_120` — VAT 20/120. VAT is 20%, applicable only for prepayment.
  * `VAT_18` — VAT 18%. Basic VAT until 2019.
  * `VAT_18_118` — VAT 18/118. VAT was used until January 1, 2019 for prepayment.
  * `VAT_12` — 12% VAT. It is used only in Uzbekistan.
  * `VAT_05` — 5% VAT. VAT for the simplified taxation system (USN).
  * `VAT_07` — 7% VAT. VAT for the simplified taxation system (USN).
  * `UNKNOWN_VALUE` — unknown type.

Used only in conjunction with the parameter `payment-method=YANDEX`. _Enum:_ `NO_VAT`, `VAT_0`, `VAT_10`, `VAT_10_110`, `VAT_20`, `VAT_20_120`, `VAT_18`, `VAT_18_118`, `VAT_12`, `VAT_05`, `VAT_07`, `UNKNOWN_VALUE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#orderiteminstancedto)OrderItemInstanceDTO
The marking or fault codes you have provided for this position. The "Honest Sign" codes are returned in two versions — with and without a cryptotail.
**Name** |  **Description**  
---|---  
cis |  **Type:** string The unit identification code in the system   
cisFull |  **Type:** string The unit identification code in the system   
countryCode |  **Type:** string The country of manufacture is in the ISO 3166-1 alpha-2 format. [How to get](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/regions/getRegionsCodes) _Example:_ `RU` _Min length:_ `2` _Max length:_ `2` _Pattern:_ `^[A-Z]{2}$`  
gtd |  **Type:** string Cargo customs declaration. It is a string of three numbers separated by a slash: XXXXXXXXXX/XXXXXXXX/XXXXXXXX. The first part is the code of the customs office that registered the declaration for imported goods. Next is the date and number of the declaration.  
rnpt |  **Type:** string The registration number of the product batch. It is a string of four numbers separated by slashes: XXXXXXXXXX/XXXXXXXX/XXXXXXXX/XXX. The first part is the code of the customs office that registered the declaration for the shipment. Next is the date, the number of the declaration and the number of the marked product in the declaration.  
uin |  **Type:** string Jewelry's UIN (16-digit code) The manufacturer receives the UIN when he registers the product in the system of control over the turnover of precious metals and stones — GIIS DMDK.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#ordervattype)OrderVatType
Value added tax (VAT) on the product:
  * `NO_VAT` — VAT is not charged, it is used only for certain types of services.
  * `VAT_0` — 0% VAT. For example, it is used for the sale of goods exported in the customs procedure of export, or for the provision of services for the international transportation of goods.
  * `VAT_10` — 10% VAT. For example, it is used in the sale of certain food and medical products.
  * `VAT_10_110` — VAT 10/110. 10% VAT, applicable only for prepayment.
  * `VAT_20` — 20% VAT. Basic VAT starting in 2019.
  * `VAT_20_120` — VAT 20/120. VAT is 20%, applicable only for prepayment.
  * `VAT_18` — VAT 18%. Basic VAT until 2019.
  * `VAT_18_118` — VAT 18/118. VAT was used until January 1, 2019 for prepayment.
  * `VAT_12` — 12% VAT. It is used only in Uzbekistan.
  * `VAT_05` — 5% VAT. VAT for the simplified taxation system (USN).
  * `VAT_07` — 7% VAT. VAT for the simplified taxation system (USN).
  * `UNKNOWN_VALUE` — unknown type.


Used only in conjunction with the parameter `payment-method=YANDEX`.
**Type** |  **Description**  
---|---  
[OrderVatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#ordervattype) |  _Enum:_ `NO_VAT`, `VAT_0`, `VAT_10`, `VAT_10_110`, `VAT_20`, `VAT_20_120`, `VAT_18`, `VAT_18_118`, `VAT_12`, `VAT_05`, `VAT_07`, `UNKNOWN_VALUE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/provideOrderItemIdentifiers#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
orderId*:
Body{ "items": [ { "id": 0, "instances": [ { "cis": "string", "uin": "string", "rnpt": "string", "gtd": "string", "countryCode": "RU" } ] } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Massive changes in order statuses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/updateOrderStatuses)
Next
[LOGIN verification Statuses](https://yandex.ru/dev/market/partner-api/doc/en/reference/orders/en/reference/orders/getOrderIdentifiersStatus)
