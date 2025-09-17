---
title: Implementation Report - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateGoodsRealizationReport
crawled_at: 2025-09-17T14:40:02.644518
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#reportformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Implementation Report
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of the implementation report for the specified period. [What kind of report is this](https://yandex.ru/support/marketplace/ru/accounting/transactions#sales-report)
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
FBY, FBS, Express
DBS
Explanation of the report columns:
Sheet **Items handed over for delivery** (file **transferred_to_delivery**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Product name |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
TRANSFERRED_TO_DELIVERY_COUNT |  transferredToDeliveryCount |  Orders/Number transferred for delivery, items |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
TRANSFERRED_TO_DELIVERY_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  transferredToDeliveryPriceSumWithVatAndNoDiscounts |  Orders/The cost of all delivered pieces with VAT excluding discounts |  number  
TRANSFERRED_TO_DELIVERY_DISCOUNT_SUM |  transferredToDeliveryDiscountSum |  Orders/The sum of all discounts for delivered pieces |  number  
TRANSFERRED_TO_DELIVERY_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  transferredToDeliveryPriceSumWithVatAndDiscounts |  Orders/The cost of all delivered pieces with VAT, including all discounts |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Documents/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Documents/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Documents/UPD number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Documents/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Documents/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Documents/UKD number |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
Sheet **Products delivered** (file **delivered**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Product name |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
TRANSFERRED_TO_DELIVERY_COUNT |  transferredToDeliveryCount |  Orders/Number transferred for delivery, items |  integer  
DELIVERED_COUNT |  deliveredCount |  Orders/Delivered, items |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
DELIVERED_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  deliveredPriceSumWithVatAndNoDiscounts |  Orders/The cost of all delivered pieces with VAT excluding discounts |  number  
DELIVERED_DISCOUNT_SUM |  deliveredDiscountSum |  Orders/The sum of all discounts for delivered pieces |  number  
DELIVERED_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  deliveredPriceSumWithVatAndDiscounts |  Orders/The cost of all delivered pieces with VAT, including all discounts |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
UPD_STATUS |  updStatus |  Продажи бизнесу/Документы/Статус УПД |  string  
UPD_DATE |  updDate |  Продажи бизнесу/Документы/Дата УПД |  string  
UPD_NUMBER |  updNumber |  Продажи бизнесу/Документы/Номер УПД |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
Sheet **Unpurchased items** (file **unredeemed**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Product name |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
TRANSFERRED_TO_DELIVERY_COUNT |  transferredToDeliveryCount |  Orders/Number transferred for delivery, items |  integer  
UNREDEEMED_COUNT |  unredeemedCount |  Orders/Unpurchased, items |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
UNREDEEMED_WAREHOUSE_OR_SC_ACCEPT_DATE |  unredeemedWarehouseOrScAcceptDate |  Orders/Date of acceptance of the non-purchase by the warehouse or sorting center |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
UNREDEEMED_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  unredeemedPriceSumWithVatAndNoDiscounts |  Orders/The cost of all non-purchased pieces with VAT excluding discounts |  number  
UNREDEEMED_DISCOUNT_SUM |  unredeemedDiscountSum |  Orders/The sum of all discounts for non-purchased pieces |  number  
UNREDEEMED_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  unredeemedPriceSumWithVatAndDiscounts |  Orders/Стоимость всех невыкупленных штук с НДС с учётом всех скидок |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Electronic document management/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Electronic document management/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Electronic document management/UKD number |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
ADJUSTMENT_INVOICE_DATE |  adjustmentInvoiceDate |  Sales to businesses/Paper document management/Adjustment invoice date |  string  
ADJUSTMENT_INVOICE_NUMBER |  adjustmentInvoiceNumber |  Sales to businesses/Paper document management/Adjustment invoice number |  string  
REDEEMED_PRICE |  redeemedPrice |  Sales to businesses/The cost of the purchased product |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Documents/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Documents/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Documents/UPD number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Documents/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Documents/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Documents/UKD number |  string  
REDEEMED_PRICE |  redeemedPrice |  Sales to businesses/Documents/The cost of the purchased product |  string  
Sheet **Returned items** (file **returned**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Product name |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
DELIVERED_COUNT |  deliveredCount |  Orders/Quantity, items |  integer  
RETURNED_COUNT |  returnedCount |  Orders/Returned, items |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
RETURN_WAREHOUSE_OR_SC_ACCEPT_DATE |  returnWarehouseOrScAcceptDate |  Orders/Return acceptance date by the warehouse or sorting center |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
RETURN_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  returnPriceSumWithVatAndNoDiscounts |  Orders/The cost of all returned pieces with VAT excluding discounts |  number  
RETURN_DISCOUNT_SUM |  returnDiscountSum |  Orders/The sum of all discounts for returned pieces |  number  
RETURN_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  returnPriceSumWithVatAndDiscounts |  Orders/The cost of all returned pieces with VAT, including all discounts |  number  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Documents/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Documents/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Documents/UPD number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Documents/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Documents/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Documents/UKD number |  string  
REDEEMED_PRICE |  redeemedPrice |  Sales to businesses/Documents/The cost of the purchased product |  number  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Electronic document management/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Electronic document management/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Electronic document management/UKD number |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
ADJUSTMENT_INVOICE_DATE |  adjustmentInvoiceDate |  Sales to businesses/Paper document management/Adjustment invoice date |  string  
ADJUSTMENT_INVOICE_NUMBER |  adjustmentInvoiceNumber |  Sales to businesses/Paper document management/Adjustment invoice number |  string  
REDEEMED_PRICE |  redeemedPrice |  Sales to businesses/The cost of the purchased product |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
Sheet **Lost items** (file **lost_items**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Product name |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
TRANSFERRED_TO_DELIVERY_COUNT |  transferredToDeliveryCount |  Orders/Number transferred for delivery, items |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
TRANSFERRED_TO_DELIVERY_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  transferredToDeliveryPriceSumWithVatAndNoDiscounts |  Orders/The cost of all delivered pieces with VAT excluding discounts |  number  
TRANSFERRED_TO_DELIVERY_DISCOUNT_SUM |  transferredToDeliveryDiscountSum |  Orders/The sum of all discounts for delivered pieces |  number  
TRANSFERRED_TO_DELIVERY_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  transferredToDeliveryPriceSumWithVatAndDiscounts |  Orders/The cost of all delivered pieces with VAT, including all discounts |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
COMPENSATION_DATE |  compensationDate |  Compensations/Autocompensation date |  string  
COMPENSATION_AMOUNT |  compensationAmount |  Compensations/The amount of auto compensation |  number  
LOST_RETURN_RECEIVED_DATE |  lostReturnReceivedDate |  Compensations/Warehouse acceptance or merchant pickup date |  string  
DECOMPENSATION_DATE |  decompensationDate |  Compensations/Decompensation date |  string  
DECOMPENSATION_AMOUNT |  decompensationAmount |  Compensations/The amount of decompensation |  number  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Electronic document management/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Electronic document management/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Electronic document management/UKD number |  string  
ADJUSTMENT_INVOICE_DATE |  adjustmentInvoiceDate |  Sales to businesses/Paper document management/Adjustment invoice date |  string  
ADJUSTMENT_INVOICE_NUMBER |  adjustmentInvoiceNumber |  Sales to businesses/Paper document management/Adjustment invoice number |  string  
Explanation of the report columns:
Sheet **Sent for delivery** (file **transferred_to_delivery**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Title |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
TRANSFERRED_TO_DELIVERY_COUNT |  transferredToDeliveryCount |  Orders/Number transferred for delivery, items |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
TRANSFERRED_TO_DELIVERY_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  transferredToDeliveryPriceSumWithVatAndNoDiscounts |  Orders/The cost of all delivered pieces with VAT excluding discounts |  number  
TRANSFERRED_TO_DELIVERY_DISCOUNT_SUM |  transferredToDeliveryDiscountSum |  Orders/The sum of all discounts for delivered pieces |  number  
TRANSFERRED_TO_DELIVERY_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  transferredToDeliveryPriceSumWithVatAndDiscounts |  Orders/The cost of all delivered pieces with VAT, including all discounts |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Documents/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Documents/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Documents/UPD number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Documents/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Documents/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Documents/UKD number |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
Sheet **Delivered** (file **delivered**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Title |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
TRANSFERRED_TO_DELIVERY_COUNT |  transferredToDeliveryCount |  Orders/Number transferred for delivery, items |  integer  
DELIVERED_COUNT |  deliveredCount |  Orders/Delivered, items |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
DELIVERED_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  deliveredPriceSumWithVatAndNoDiscounts |  Orders/The cost of all delivered pieces with VAT excluding discounts |  number  
DELIVERED_DISCOUNT_SUM |  deliveredDiscountSum |  Orders/The sum of all discounts for delivered pieces |  number  
DELIVERED_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  deliveredPriceSumWithVatAndDiscounts |  Orders/The cost of all delivered pieces with VAT, including all discounts |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
UPD_STATUS |  updStatus |  Продажи бизнесу/Документы/Статус УПД |  string  
UPD_DATE |  updDate |  Продажи бизнесу/Документы/Дата УПД |  string  
UPD_NUMBER |  updNumber |  Продажи бизнесу/Документы/Номер УПД |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
Sheet **Unbought** (file **unredeemed**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Title |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
TRANSFERRED_TO_DELIVERY_COUNT |  transferredToDeliveryCount |  Orders/Number transferred for delivery, items |  integer  
UNREDEEMED_COUNT |  unredeemedCount |  Orders/Not redeemed, PCs. |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
UNREDEEMED_WAREHOUSE_OR_SC_ACCEPT_DATE |  unredeemedWarehouseOrScAcceptDate |  Orders/Date of acceptance of the non-purchase by the warehouse or sorting center |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
UNREDEEMED_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  unredeemedPriceSumWithVatAndNoDiscounts |  Orders/The cost of all non-purchased pieces with VAT excluding discounts |  number  
UNREDEEMED_DISCOUNT_SUM |  unredeemedDiscountSum |  Orders/The sum of all discounts for non-purchased pieces |  number  
UNREDEEMED_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  unredeemedPriceSumWithVatAndDiscounts |  Orders/Стоимость всех невыкупленных штук с НДС с учётом всех скидок |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Electronic document management/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Electronic document management/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Electronic document management/UKD number |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
ADJUSTMENT_INVOICE_DATE |  adjustmentInvoiceDate |  Sales to businesses/Paper document management/Adjustment invoice date |  string  
ADJUSTMENT_INVOICE_NUMBER |  adjustmentInvoiceNumber |  Sales to businesses/Paper document management/Adjustment invoice number |  string  
REDEEMED_PRICE |  redeemedPrice |  Sales to businesses/The cost of the purchased product |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Documents/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Documents/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Documents/UPD number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Documents/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Documents/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Documents/UKD number |  string  
REDEEMED_PRICE |  redeemedPrice |  Sales to businesses/Documents/The cost of the purchased product |  string  
Sheet **Returned** (file **returned**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
ORDER_ID |  orderId |  Orders/Order number |  integer  
YOUR_ORDER_ID |  yourOrderId |  Orders/Your order number |  string  
ORDER_TYPE |  orderType |  Orders/Order type |  string  
OFFER_NAME |  offerName |  Orders/Title |  string  
YOUR_SKU |  yourSku |  Orders/Your SKU |  string  
SHOP_SKU |  shopSku |  Orders/$ |  string  
DELIVERED_COUNT |  deliveredCount |  Orders/Quantity, items |  integer  
RETURNED_COUNT |  returnedCount |  Orders/Returned, items |  integer  
ORDER_CREATION_DATE |  orderCreationDate |  Orders/Order creation date |  string  
TRANSFERRED_TO_DELIVERY_DATE |  transferredToDeliveryDate |  Orders/Date goods were handed over for delivery |  string  
DELIVERY_DATE |  deliveryDate |  Orders/Product delivery date |  string  
RETURN_WAREHOUSE_OR_SC_ACCEPT_DATE |  returnWarehouseOrScAcceptDate |  Orders/Date of issue of the refund to you |  string  
PAYMENT_TYPE |  paymentType |  Orders/Payment method |  string  
VAT |  vat |  Orders/VAT rate |  string  
PRICE_WITH_VAT_AND_NO_DISCOUNT |  priceWithVatAndNoDiscount |  Orders/The price includes VAT without discounts per piece. |  number  
SHOP_MARKETPLACE_DISCOUNT |  shopMarketplaceDiscount |  Orders/Your discount on the marketplace promotion is 1 pc. |  number  
SPASIBO_DISCOUNT |  spasiboDiscount |  Orders/Your discount on Savings bonuses is only (per piece) for 1 piece. |  number  
YANDEX_PLUS_DISCOUNT |  yandexPlusDiscount |  Orders/Your discount on Yandex points.Advantages per 1 pc . |  number  
PRICE_WITH_VAT_AND_ALL_DISCOUNTS |  priceWithVatAndAllDiscounts |  Orders/Price with VAT, including all discounts per piece. |  number  
RETURN_PRICE_SUM_WITH_VAT_AND_NO_DISCOUNTS |  returnPriceSumWithVatAndNoDiscounts |  Orders/The cost of all returned pieces with VAT excluding discounts |  number  
RETURN_DISCOUNT_SUM |  returnDiscountSum |  Orders/The sum of all discounts for returned pieces |  number  
RETURN_PRICE_SUM_WITH_VAT_AND_DISCOUNTS |  returnPriceSumWithVatAndDiscounts |  Orders/The cost of all returned pieces with VAT, including all discounts |  number  
ORGANIZATION |  organization |  Sales to businesses/Information about buyer/Organization name |  string  
INN |  inn |  Sales to businesses/Information about buyer/INN (taxpayer identification number) |  string  
KPP |  kpp |  Sales to businesses/Information about buyer/KPP (Tax Registration Reason Code) |  string  
ORGANIZATION_JUR_ADDRESS |  organizationJurAddress |  Sales to businesses/Information about buyer/Legal address |  string  
UPD_STATUS |  updStatus |  Sales to businesses/Documents/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Documents/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Documents/UPD number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Documents/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Documents/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Documents/UKD number |  string  
REDEEMED_PRICE |  redeemedPrice |  Sales to businesses/Documents/The cost of the purchased product |  number  
UPD_STATUS |  updStatus |  Sales to businesses/Electronic document management/UPD status |  string  
UPD_DATE |  updDate |  Sales to businesses/Electronic document management/UPD date |  string  
UPD_NUMBER |  updNumber |  Sales to businesses/Electronic document management/UPD number |  string  
UKD_STATUS |  ukdStatus |  Sales to businesses/Electronic document management/UKD status |  string  
UKD_DATE |  ukdDate |  Sales to businesses/Electronic document management/UKD date |  string  
UKD_NUMBER |  ukdNumber |  Sales to businesses/Electronic document management/UKD number |  string  
CONSIGNMENT_NOTE_DATE |  consignmentNoteDate |  Sales to businesses/Paper document management/Packing list date |  string  
CONSIGNMENT_NOTE_NUMBER |  consignmentNoteNumber |  Sales to businesses/Paper document management/Packing list number |  string  
INVOICE_DATE |  invoiceDate |  Sales to businesses/Paper document management/Invoice date |  string  
INVOICE_NUMBER |  invoiceNumber |  Sales to businesses/Paper document management/Invoice number |  string  
ADJUSTMENT_INVOICE_DATE |  adjustmentInvoiceDate |  Sales to businesses/Paper document management/Adjustment invoice date |  string  
ADJUSTMENT_INVOICE_NUMBER |  adjustmentInvoiceNumber |  Sales to businesses/Paper document management/Adjustment invoice number |  string  
REDEEMED_PRICE |  redeemedPrice |  Sales to businesses/The cost of the purchased product |  number  
RNPT |  rnpt |  Orders/Registration number of the customs declaration or the Registration Number of Batch of Products subject to tracking (RNBP) |  string  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/goods-realization/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#reportformattype) The format of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body)Body
application/json
```
{
    "campaignId": 0,
    "year": 2025,
    "month": 12
}

```

**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
month* |  **Type:** integer<int32> The month number. _Example:_ `12` _Min value:_ `1` _Max value:_ `12`  
year* |  **Type:** integer<int32> Year. _Example:_ `2025`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "campaignId": 0, "year": 2025, "month": 12 }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Shelf Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateShelfsStatisticsReport)
Next
[Report on the cost of services](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport)
