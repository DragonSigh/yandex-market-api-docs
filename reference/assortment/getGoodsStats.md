---
title: Product Report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/getGoodsStats
crawled_at: 2025-09-17T14:36:50.723644
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body1)
    * [GoodsStatsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype)
    * [GoodsStatsGoodsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsgoodsdto)
    * [TariffDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tariffdto)
    * [GoodsStatsWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatswarehousedto)
    * [GoodsStatsWeightDimensionsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsweightdimensionsdto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#currencytype)
    * [TariffParameterDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tariffparameterdto)
    * [TariffType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tarifftype)
    * [WarehouseStockDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#warehousestockdto)
    * [WarehouseStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#warehousestocktype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body7)


# Product Report
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/overview/comparison).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns a detailed report on the products that you have placed on the Market. You can use the report to find out, for example, about stock balances, storage conditions for your goods, and so on.
**, Limit:** 5,000 items per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/stats/skus

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body)Body
application/json
```
{
    "shopSkus": [
        "string"
    ]
}

```

**Name** |  **Description**  
---|---  
shopSkus* |  **Type:** string[] A list of your SKU IDs.   
Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$` _Min items:_ `1` _Max items:_ `500` _Unique items_  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#200-ok)200 OK
Product report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "shopSkus": [
            {
                "shopSku": "string",
                "marketSku": 0,
                "name": "string",
                "price": 0,
                "categoryId": 0,
                "categoryName": "string",
                "weightDimensions": {
                    "length": 0,
                    "width": 0,
                    "height": 0,
                    "weight": 0
                },
                "warehouses": [
                    {
                        "id": 0,
                        "name": "string",
                        "stocks": [
                            {
                                "type": "FIT",
                                "count": 0
                            }
                        ]
                    }
                ],
                "tariffs": [
                    {
                        "type": "AGENCY_COMMISSION",
                        "percent": 0,
                        "amount": 0,
                        "currency": "RUR",
                        "parameters": [
                            {
                                "name": "string",
                                "value": "string"
                            }
                        ]
                    }
                ],
                "pictures": [
                    "string"
                ]
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GoodsStatsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsdto) Product report.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsdto)GoodsStatsDTO
Product report.
**Name** |  **Description**  
---|---  
shopSkus* |  **Type:** [GoodsStatsGoodsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsgoodsdto)[] The list of products.  
Product information.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsgoodsdto)GoodsStatsGoodsDTO
Product information.
**Name** |  **Description**  
---|---  
categoryId |  **Type:** integer<int64> The identifier of the product category on the Market.  
categoryName |  **Type:** string The name of the product category on the Market.  
marketSku |  **Type:** integer<int64> The ID of the product card on the Market. _Min value:_ `1`  
name |  **Type:** string Product name.  
pictures |  **Type:** string[] Links (URLs) of product images in good quality.  
_Min length:_ `1` _Max length:_ `2000` _Min items:_ `1` _Unique items_  
price |  **Type:** number The price of the product in the currency that is set [in the seller's office on the Market](https://partner.market.yandex.ru/).  
shopSku |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
tariffs |  **Type:** [TariffDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tariffdto)[] Information about the tariffs that you need to pay for Yandex.Market services. For some services, several different values may be returned. For example, in the FBS model, the cost of a service is `SORTING` (order processing) depends on the shipping method and the number of orders in the shipment. Read more about the tariffs for services [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/introduction/rates/models/).   
Information about the tariffs that you need to pay for Yandex.Market services. _Min items:_ `1`  
warehouses |  **Type:** [GoodsStatsWarehouseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatswarehousedto)[] Information about the warehouses where the goods are stored. The parameter is not received if the product is not in any warehouse.   
Information about the warehouse. _Min items:_ `1`  
weightDimensions |  **Type:** [GoodsStatsWeightDimensionsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsweightdimensionsdto) Information about the weight and dimensions of the product. If the product is already linked to the card (`marketSku`), the response will return the dimensions from the Market card, not the dimensions that you provide.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tariffdto)TariffDTO
Information about the tariffs that you need to pay for Yandex.Market services.
**Name** |  **Description**  
---|---  
amount* |  **Type:** number The value of the tariff.  
currency* |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#currencytype) The currency in which the tariff value is indicated. _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
parameters* |  **Type:** [TariffParameterDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tariffparameterdto)[] Tariff calculation parameters.  
Details of the calculation of a specific Market service.  
type* |  **Type:** [TariffType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tarifftype) The Market service for which the tariff is calculated. _Enum:_ `AGENCY_COMMISSION`, `PAYMENT_TRANSFER`, `STORAGE`, `WITHDRAW`, `SURPLUS`, `FEE`, `DELIVERY_TO_CUSTOMER`, `CROSSREGIONAL_DELIVERY`, `CROSSREGIONAL_DELIVERY_RETURN`, `DISPOSAL`, `SORTING_CENTER_STORAGE`, `EXPRESS_DELIVERY`, `FF_XDOC_SUPPLY_BOX`, `FF_XDOC_SUPPLY_PALLET`, `SORTING`, `MIDDLE_MILE`, `RETURN_PROCESSING`, `EXPRESS_CANCELLED_BY_PARTNER`, `CROSSBORDER_DELIVERY`, `INTAKE_SORTING_BULKY_CARGO`, `INTAKE_SORTING_SMALL_GOODS`, `INTAKE_SORTING_DAILY`, `FF_STORAGE_BILLING`, `CANCELLED_ORDER_FEE_QI`, `LATE_ORDER_EXECUTION_FEE_QI`  
percent ⦸ |  **Type:** number The tariff value is expressed as a percentage.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatswarehousedto)GoodsStatsWarehouseDTO
Information about the warehouse.
**Name** |  **Description**  
---|---  
stocks* |  **Type:** [WarehouseStockDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#warehousestockdto)[] Information about the remaining goods in the warehouse.  
Information about the remaining goods.  
id |  **Type:** integer<int64> The warehouse ID.  
name |  **Type:** string The name of the warehouse.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#goodsstatsweightdimensionsdto)GoodsStatsWeightDimensionsDTO
Information about the weight and dimensions of the product.
If the product is already linked to the card (`marketSku`), the response will return the dimensions from the Market card, not the dimensions that you provide.
**Name** |  **Description**  
---|---  
height |  **Type:** number The height of the product in centimeters.  
length |  **Type:** number The length of the product in centimeters.  
weight |  **Type:** number The weight of the product in kilograms.  
width |  **Type:** number The width of the product in centimeters.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tariffparameterdto)TariffParameterDTO
Details of the calculation of a specific Market service.
**Name** |  **Description**  
---|---  
name* |  **Type:** string The name of the parameter.  
value* |  **Type:** string The value of the parameter.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tarifftype)TariffType
A Market service or an additional tariff to the placement service:
  * `AGENCY_COMMISSION` — acceptance of the buyer's payment.
  * `PAYMENT_TRANSFER` — transfer of the buyer's payment.
  * `STORAGE` — storage of goods in the Market warehouse during the day.
  * `SURPLUS` — excess storage in the Market warehouse.
  * `WITHDRAW` — export of goods from the Market warehouse.
  * `FEE` — product placement on the Market.
  * `DELIVERY_TO_CUSTOMER` — delivery to the buyer.
  * `CROSSREGIONAL_DELIVERY` — delivery to the federal district, city or town.
  * `CROSSREGIONAL_DELIVERY_RETURN` — delivery of non-purchases and refunds.
  * `DISPOSAL` — disposal.
  * `SORTING_CENTER_STORAGE` — storage of non-purchases and refunds.
  * `EXPRESS_DELIVERY` — express delivery to the buyer.
  * `FF_XDOC_SUPPLY_BOX` — delivery of goods through a transit warehouse (per box).
  * `FF_XDOC_SUPPLY_PALLET` — delivery of goods through a transit warehouse (per pallet).
  * `SORTING` — order processing.
  * `MIDDLE_MILE` — the average mile.
  * `RETURN_PROCESSING` — processing of non-purchases and refunds.
  * `EXPRESS_CANCELLED_BY_PARTNER` — cancellation of an order with express delivery.
  * `CROSSBORDER_DELIVERY` — delivery from abroad.
  * `INTAKE_SORTING_BULKY_CARGO` — sorting orders with bulky items that the Market has picked up from the seller's warehouse.
  * `INTAKE_SORTING_SMALL_GOODS` — sorting orders with small-sized goods that the Market has taken from the seller's warehouse.
  * `INTAKE_SORTING_DAILY` — organization of picking up orders from the seller's warehouse.
  * `FF_STORAGE_BILLING` — storage of goods in a warehouse.
  * `CANCELLED_ORDER_FEE_QI` — cancellation of the order is the fault of the seller.
  * `LATE_ORDER_EXECUTION_FEE_QI` — late shipment or delivery.


Read more about Yandex.Market services [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/introduction/rates/index.html).
**Type** |  **Description**  
---|---  
[TariffType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#tarifftype) |  _Enum:_ `AGENCY_COMMISSION`, `PAYMENT_TRANSFER`, `STORAGE`, `WITHDRAW`, `SURPLUS`, `FEE`, `DELIVERY_TO_CUSTOMER`, `CROSSREGIONAL_DELIVERY`, `CROSSREGIONAL_DELIVERY_RETURN`, `DISPOSAL`, `SORTING_CENTER_STORAGE`, `EXPRESS_DELIVERY`, `FF_XDOC_SUPPLY_BOX`, `FF_XDOC_SUPPLY_PALLET`, `SORTING`, `MIDDLE_MILE`, `RETURN_PROCESSING`, `EXPRESS_CANCELLED_BY_PARTNER`, `CROSSBORDER_DELIVERY`, `INTAKE_SORTING_BULKY_CARGO`, `INTAKE_SORTING_SMALL_GOODS`, `INTAKE_SORTING_DAILY`, `FF_STORAGE_BILLING`, `CANCELLED_ORDER_FEE_QI`, `LATE_ORDER_EXECUTION_FEE_QI`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#warehousestockdto)WarehouseStockDTO
Information about the remaining goods.
**Name** |  **Description**  
---|---  
count* |  **Type:** integer<int64> The value of the leftovers.  
type* |  **Type:** [WarehouseStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#warehousestocktype) The type of leftovers. _Enum:_ `FIT`, `FREEZE`, `AVAILABLE`, `QUARANTINE`, `UTILIZATION`, `DEFECT`, `EXPIRED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#warehousestocktype)WarehouseStockType
The type of remaining goods in the warehouse:
  * `AVAILABLE` (corresponds to the "Available to order" type in the "Stock balances" report in the seller's office on the Market) — an item available for sale.
  * `DEFECT` (corresponds to the "Marriage" type) — a defective product.
  * `EXPIRED` (corresponds to the "Expired" type) — an expired product.
  * `FIT` (corresponds to the "Fit" type) — an item that is available for sale or has already been reserved.
  * `FREEZE` — the product that is reserved for orders.
  * `QUARANTINE` (corresponds to the "Quarantine" type) — a product that is temporarily unavailable for sale (for example, the product is being moved from one warehouse to another).
  * `UTILIZATION` — the product that will be disposed of.

**Type** |  **Description**  
---|---  
[WarehouseStockType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#warehousestocktype) |  _Enum:_ `FIT`, `FREEZE`, `AVAILABLE`, `QUARANTINE`, `UTILIZATION`, `DEFECT`, `EXPIRED`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/assortment/getGoodsStats#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "shopSkus": [ "string" ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Report on convergence with closing documents](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/reports/generateClosureDocumentsDetalizationReport)
Next
[The Prices Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/assortment/en/reference/reports/generateGoodsPricesReport)
