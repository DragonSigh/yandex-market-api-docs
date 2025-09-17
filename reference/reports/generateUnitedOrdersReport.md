---
title: Order Report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateUnitedOrdersReport
crawled_at: 2025-09-17T14:39:10.704573
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#reportformattype)
    * [ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#reportlanguagetype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Order Report
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/promotion)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of a report on orders for a specified period. [What kind of report is this](https://yandex.ru/support/marketplace/ru/accounting/transactions#get-report)
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
Explanation of the report columns:
Sheet **Order and product transactions** (file **orders_and_offers_transactions**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Information about orders/Order number |  integer  
PARTNER_ORDER_ID |  partnerOrderId |  Information about orders/Your order number |  string  
CREATION_DATE |  creationDate |  Information about orders/Creation date |  string  
ORDER_TYPE |  orderType |  Information about orders/Order type |  string  
SHOP_SKU |  shopSku |  Information about orders/Your SKU |  string  
OFFER_NAME |  offerName |  Information about orders/Product name |  string  
PARTNER_PRICE_FOR_DELIVERY |  partnerPriceForDelivery |  Information about orders/Your price (per item) |  number  
BILLING_PRICE |  billingPrice |  Information about orders/Sale price (per item) |  number  
COFINANCE_TRESHOLD |  cofinanceTreshold |  Information about orders/Your price reduction threshold for participating in co-financing at the time of ordering (per item) |  number  
COFINANCE_VALUE |  cofinanceValue |  Information about orders/Your discount if the product was co-financed (per item) |  number  
COFINANCE_SUBSIDY |  cofinanceSubsidy |  Information about orders/Yandex Market discount if item was co-financed |  number  
MARKETPLACE_SUBSIDY |  marketplaceSubsidy |  Information about orders/Other Yandex Market discounts (per item) |  number  
SPASIBO |  spasibo |  Information about orders/Payment in Sberbank bonuses (per item) |  number  
YANDEX_PLUS |  yandexPlus |  Information about orders/Payment by Yandex Plus points (per item) |  number  
TRANSFERRED_FOR_DELIVERY |  transferredForDelivery |  Information about orders/Transferred for delivery |  integer  
DELIVERED_OR_RETURNED |  deliveredOrReturned |  Information about orders/Delivered or returned |  integer  
DELIVERY_DATE |  deliveryDate |  Information about orders/Order delivery date |  string  
OFFER_STATUS |  offerStatus |  Information about orders/Product status |  string  
STATUS_CHANGED |  statusChanged |  Information about orders/Status changed |  string  
PAYMENT_TYPE |  paymentType |  Information about orders/Payment method |  string  
SHIPMENT_WAREHOUSE |  shipmentWarehouse |  Information about orders/Shipment warehouse |  string  
SHIPMENT_DATE |  shipmentDate |  Information about orders/Shipping date |  string  
DELIVERY_REGION |  deliveryRegion |  Information about orders/Delivery region |  string  
BUYER_PAYMENT_AMOUNT |  buyerPaymentAmount |  Buyer payment/Payment amount |  number  
BUYER_PAYMENT_BANK_ORDER_ID |  buyerPaymentBankOrderId |  Buyer payment/Payment order number |  string  
BUYER_PAYMENT_BANK_ORDER_DATE |  buyerPaymentBankOrderDate |  Buyer payment/Payment order date |  string  
BUYER_PAYMENT_ID |  buyerPaymentId |  Buyer payment/Payment ID |  string  
BUYER_PAYMENT_HANDLING_TIME |  buyerPaymentHandlingTime |  Buyer payment/Payment register date |  string  
MARKETPLACE_DISCOUNT_PAYMENT_AMOUNT |  marketplaceDiscountPaymentAmount |  Payment for a Yandex Market discount/Payment amount |  number  
MARKETPLACE_DISCOUNT_PAYMENT_BANK_ORDER_ID |  marketplaceDiscountPaymentBankOrderId |  Payment for a Yandex Market discount/Payment order number |  string  
MARKETPLACE_DISCOUNT_PAYMENT_BANK_ORDER_DATE |  marketplaceDiscountPaymentBankOrderDate |  Payment for a Yandex Market discount/Payment order date |  string  
MARKETPLACE_DISCOUNT_PAYMENT_ID |  marketplaceDiscountPaymentId |  Payment for a Yandex Market discount/Payment ID |  string  
MARKETPLACE_DISCOUNT_PAYMENT_HANDLING_TIME |  marketplaceDiscountPaymentHandlingTime |  Payment for a Yandex Market discount/Payment register date |  string  
SPASIBO_PAYMENT_AMOUNT |  spasiboPaymentAmount |  Payment for the discount with SberSpasibo bonus points/Payment amount |  number  
SPASIBO_PAYMENT_BANK_ORDER_ID |  spasiboPaymentBankOrderId |  Payment for the discount with SberSpasibo bonus points/Payment order number |  string  
SPASIBO_PAYMENT_BANK_ORDER_DATE |  spasiboPaymentBankOrderDate |  Payment for the discount with SberSpasibo bonus points/Payment order date |  string  
SPASIBO_PAYMENT_ID |  spasiboPaymentId |  Payment for the discount with SberSpasibo bonus points/Payment ID |  string  
SPASIBO_PAYMENT_HANDLING_TIME |  spasiboPaymentHandlingTime |  Payment for the discount with SberSpasibo bonus points/Payment register date |  string  
YANDEX_PLUS_PAYMENT_AMOUNT |  yandexPlusPaymentAmount |  Payment for Yandex Plus discount/Payment amount |  number  
YANDEX_PLUS_PAYMENT_BANK_ORDER_ID |  yandexPlusPaymentBankOrderId |  Payment for Yandex Plus discount/Payment order number |  string  
YANDEX_PLUS_PAYMENT_BANK_ORDER_DATE |  yandexPlusPaymentBankOrderDate |  Payment for Yandex Plus discount/Payment order date |  string  
YANDEX_PLUS_PAYMENT_ID |  yandexPlusPaymentId |  Payment for Yandex Plus discount/Payment ID |  string  
YANDEX_PLUS_PAYMENT_HANDLING_TIME |  yandexPlusPaymentHandlingTime |  Payment for Yandex Plus discount/Payment register date |  string  
REFUND_BUYER_PAYMENT_AMOUNT |  refundBuyerPaymentAmount |  Refund of buyer payment/Refund amount |  number  
REFUND_BUYER_PAYMENT_BANK_ORDER_ID |  refundBuyerPaymentBankOrderId |  Refund of buyer payment/Payment order number |  string  
REFUND_BUYER_PAYMENT_BANK_ORDER_DATE |  refundBuyerPaymentBankOrderDate |  Refund of buyer payment/Payment order date |  string  
REFUND_BUYER_PAYMENT_ID |  refundBuyerPaymentId |  Refund of buyer payment/Payment ID |  string  
REFUND_BUYER_PAYMENT_HANDLING_TIME |  refundBuyerPaymentHandlingTime |  Refund of buyer payment/Payment register date |  string  
REFUND_MARKETPLACE_DISCOUNT_PAYMENT_AMOUNT |  refundMarketplaceDiscountPaymentAmount |  Refund of payment for Yandex Market discount/Refund amount |  number  
REFUND_MARKETPLACE_DISCOUNT_PAYMENT_BANK_ORDER_ID |  refundMarketplaceDiscountPaymentBankOrderId |  Refund of payment for Yandex Market discount/Payment order number |  string  
REFUND_MARKETPLACE_DISCOUNT_PAYMENT_BANK_ORDER_DATE |  refundMarketplaceDiscountPaymentBankOrderDate |  Refund of payment for Yandex Market discount/Payment order date |  string  
REFUND_MARKETPLACE_DISCOUNT_PAYMENT_ID |  refundMarketplaceDiscountPaymentId |  Refund of payment for Yandex Market discount/Payment ID |  string  
REFUND_MARKETPLACE_DISCOUNT_PAYMENT_HANDLING_TIME |  refundMarketplaceDiscountPaymentHandlingTime |  Refund of payment for Yandex Market discount/Payment register date |  string  
REFUND_SPASIBO_PAYMENT_AMOUNT |  refundSpasiboPaymentAmount |  Refund of the payment for the discount with SberSpasibo bonus points/Refund amount |  number  
REFUND_SPASIBO_PAYMENT_BANK_ORDER_ID |  refundSpasiboPaymentBankOrderId |  Refund of the payment for the discount with SberSpasibo bonus points/Payment order number |  string  
REFUND_SPASIBO_PAYMENT_BANK_ORDER_DATE |  refundSpasiboPaymentBankOrderDate |  Refund of the payment for the discount with SberSpasibo bonus points/Payment order date |  string  
REFUND_SPASIBO_PAYMENT_ID |  refundSpasiboPaymentId |  Refund of the payment for the discount with SberSpasibo bonus points/Payment ID |  string  
REFUND_SPASIBO_PAYMENT_HANDLING_TIME |  refundSpasiboPaymentHandlingTime |  Refund of the payment for the discount with SberSpasibo bonus points/Payment register date |  string  
REFUND_YANDEX_PLUS_PAYMENT_AMOUNT |  refundYandexPlusPaymentAmount |  Refund of payment for Yandex Plus discount/Refund amount |  number  
REFUND_YANDEX_PLUS_PAYMENT_BANK_ORDER_ID |  refundYandexPlusPaymentBankOrderId |  Refund of payment for Yandex Plus discount/Payment order number |  string  
REFUND_YANDEX_PLUS_PAYMENT_BANK_ORDER_DATE |  refundYandexPlusPaymentBankOrderDate |  Refund of payment for Yandex Plus discount/Payment order date |  string  
REFUND_YANDEX_PLUS_PAYMENT_ID |  refundYandexPlusPaymentId |  Refund of payment for Yandex Plus discount/Payment ID |  string  
REFUND_YANDEX_PLUS_PAYMENT_HANDLING_TIME |  refundYandexPlusPaymentHandlingTime |  Refund of payment for Yandex Plus discount/Payment register date |  string  
DEFECT_REFUND_PAYMENT_AMOUNT |  defectRefundPaymentAmount |  Reimbursement of expenses to the buyer if products of substandard quality are returned/Amount withheld |  number  
DEFECT_REFUND_PAYMENT_BANK_ORDER_ID |  defectRefundPaymentBankOrderId |  Reimbursement of expenses to the buyer if products of substandard quality are returned/Payment order number |  string  
DEFECT_REFUND_PAYMENT_BANK_ORDER_DATE |  defectRefundPaymentBankOrderDate |  Reimbursement of expenses to the buyer if products of substandard quality are returned/Payment order date |  string  
DEFECT_REFUND_PAYMENT_ID |  defectRefundPaymentId |  Reimbursement of expenses to the buyer if products of substandard quality are returned/Payment ID |  string  
DEFECT_REFUND_PAYMENT_HANDLING_TIME |  defectRefundPaymentHandlingTime |  Reimbursement of expenses to the buyer if products of substandard quality are returned/Payment register date |  string  
NETTING_AMOUNT |  nettingAmount |  Points for Market discounts and Yandex Plus discounts/Bonuses amount |  number  
NETTING_TRANSACTION_STATUS |  nettingTransactionStatus |  Points for Market discounts and Yandex Plus discounts/Status (for reference) |  string  
Sheet **Order services and margin** (file **services_and_orders_margin**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Information about orders/Order number |  integer  
PARTNER_ORDER_ID |  partnerOrderId |  Information about orders/Your order number |  string  
ORDER_STATUS |  orderStatus |  Information about orders/Order status |  string  
CREATION_DATE |  creationDate |  Information about orders/Creation date |  string  
ORDER_TYPE |  orderType |  Information about orders/Order type |  string  
SUMMARY_COMMISSION |  summaryCommission |  Information about funds/All Yandex Market services for orders |  number  
SUM_BILLING_PRICE_OF_ITEMS |  sumBillingPriceOfItems |  Information about funds/Sale price (per item) |  number  
INCOME_WITHOUT_SERVICES |  incomeWithoutServices |  Information about funds/Revenue after deducting Yandex Market services |  number  
BUYER_PAYMENT |  buyerPayment |  Information about funds/Buyer payment, excluding Yandex Market discounts and Plus points |  number  
BUYER_PAYMENT_STATUS |  buyerPaymentStatus |  Information about funds/Buyer payment status |  string  
BANK_ORDER_ID |  bankOrderId |  Information about funds/Payment order number |  string  
SALE_COMMISSION |  saleCommission |  Service information/Product placement on the showcase |  number  
WAREHOUSE_PROCESSING |  warehouseProcessing |  Service information/Warehouse processing |  number  
LOYALTY_PROGRAM |  loyaltyProgram |  Service information/Participation in loyalty program |  number  
BOOST |  boost |  Service information/Sales boosts |  number  
INSTALLMENT |  installment |  Service information/Installment plan |  number  
BUYER_DELIVERY |  buyerDelivery |  Service information/Delivery to buyer |  number  
BUYER_EXPRESS_DELIVERY |  buyerExpressDelivery |  Service information/Express delivery |  number  
BUYER_PAYMENT_ACCEPT |  buyerPaymentAccept |  Service information/Acceptance of buyer payment |  number  
BUYER_PAYMENT_TRANSFER |  buyerPaymentTransfer |  Service information/Transfer of buyer payment |  number  
ORDER_PROCESSING |  orderProcessing |  Service information/Order processing |  number  
RESUPPLY_HANDLING |  resupplyHandling |  Service information/Storage of unpurchased goods and returns |  number  
RETURN_RESUPPLY |  returnResupply |  Service information/Return of unpurchased items |  number  
ORDER_INTAKE |  orderIntake |  Service information/Order pickup arrangement |  number  
EXPROPRIATION_RESALE |  expropriationResale |  Service information/Expropriated goods sale commission |  number  
Sheet **Orders with smart pricing** (file **services_with_decoupling**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Information about orders/Order number |  integer  
SHOP_ORDER_ID |  shopOrderId |  Information about orders/Your order number |  string  
ORDER_STATUS |  orderStatus |  Information about orders/Order status |  string  
CREATION_DATE |  creationDate |  Information about orders/Creation date |  string  
ORDER_TYPE |  orderType |  Information about orders/Order type |  string  
SHOP_SKU |  shopSku |  Information about orders/Your SKU |  string  
OFFER_NAME |  offerName |  Information about orders/Product name |  string  
COUNT |  count |  Information about orders/Quantity |  integer  
SHOP_PRICE |  shopPrice |  Information about funds/Your price (per item) |  number  
SELLING_PRICE |  sellingPrice |  Information about funds/Sale price (per item) |  number  
BUYER_PAYMENT |  buyerPayment |  Information about funds/Buyer payment, excluding Yandex Market discounts and Plus points |  number  
EXTRA_INCOME |  extraIncome |  Information about funds/Difference between your price and sale price |  number  
SUMMARY_COMMISSION |  summaryCommission |  Information about funds/All Yandex Market services for orders |  number  
INCOME_WITHOUT_SERVICES |  incomeWithoutServices |  Information about funds/Revenue after deducting Yandex Market services |  number  
EXTRA_DECOUPLING_MARGIN |  extraDecouplingMargin |  Information about funds/Additional turnover from smart offer |  number  
NET_DECOUPLING_GAIN |  netDecouplingGain |  Information about funds/Additional revenue from smart offer |  number  
SALE_COMMISSION |  saleCommission |  Service information/Product placement on the showcase |  number  
EXTRA_DECOUPLING_SALE_COMMISSION |  extraDecouplingSaleCommission |  Service information/Smart offer (additional rate for placement) |  number  
WAREHOUSE_HANDLING |  warehouseHandling |  Service information/Warehouse processing |  number  
LOYALTY_PROGRAM |  loyaltyProgram |  Service information/Participation in loyalty program |  number  
BOOST |  boost |  Service information/Sales boosts |  number  
INSTALLMENT |  installment |  Service information/Installment plan |  number  
DELIVERY |  delivery |  Service information/Delivery to buyer |  number  
EXPRESS_DELIVERY |  expressDelivery |  Service information/Express delivery |  number  
PAYMENT_ACCEPTING |  paymentAccepting |  Service information/Acceptance of buyer payment |  number  
PAYMENT_TRANSFER |  paymentTransfer |  Service information/Transfer of buyer payment |  number  
ORDER_PROCESSING |  orderProcessing |  Service information/Order processing |  number  
RESUPPLY_STORAGE |  resupplyStorage |  Service information/Storage of unpurchased goods and returns |  number  
RESUPPLY_RETURN |  resupplyReturn |  Service information/Return of unpurchased items |  number  
ORDER_INTAKE |  orderIntake |  Service information/Order pickup arrangement |  number  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/united-orders/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#reportformattype) The format of the report or document.  
language |  **Type:** [ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#reportlanguagetype) The language of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#reportlanguagetype)ReportLanguageType
Language of the report:
  * `RU` — Russian language.
  * `EN` — English language.

**Type** |  **Description**  
---|---  
[ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#reportlanguagetype) |  _Enum:_ `RU`, `EN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body)Body
application/json
```
{
    "businessId": 0,
    "dateFrom": "string",
    "dateTo": "string",
    "campaignIds": [
        0
    ],
    "promoId": "string"
}

```

**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
dateFrom* |  **Type:** string<date> The beginning of the period, inclusive.  
dateTo* |  **Type:** string<date> End of the period, inclusive. The maximum period is 1 year.  
campaignIds |  **Type:** integer<int64>[] The list of campaign IDs of those stores that are needed in the report. You can find them using a query. [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not use store IDs instead, which are listed in the seller's account on the Market next to the store name and in some reports.   
_Min items:_ `1` _Unique items_  
promoId |  **Type:** string The ID of the promotion that the products from are needed in the report.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "reportId": "string",
        "estimatedGenerationTime": 0
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedOrdersReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
language:
Body{ "businessId": 0, "dateFrom": "string", "dateTo": "string", "campaignIds": [ 0 ], "promoId": "string" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Report on the movement of goods (FBY)](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsMovementReport)
Next
[Jewelry Order Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateJewelryFiscalReport)
