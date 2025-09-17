---
title: Report on convergence with closing documents - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateClosureDocumentsDetalizationReport
crawled_at: 2025-09-17T14:36:43.280997
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#reportformattype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body)
    * [ClosureDocumentsContractType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#closuredocumentscontracttype)
    * [ClosureDocumentsMonthOfYearDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#closuredocumentsmonthofyeardto)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Report on convergence with closing documents
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Starts the generation of a report on convergence with closing documents, depending on the type of contract.
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
Placement agreement
Promotion agreement
Marketing agreement
Explanation of the report columns:
Sheet **Order execution report** (file **period_closure_income_summary**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
PAYMENTS |  payments |  Report payments |  string  
PAYMENTS_DESCRIPTION |  paymentsDescription |  What are these payments? |  string  
PAYMENT_SUM |  paymentSum |  Payment amount* |  number  
Sheet **Received from consumers** (file **period_closure_income_payments**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Returned to consumers** (file **period_closure_income_refunds**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Sold on behalf of the customer** (file **period_closure_income_sold_refunds**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Returned sold items** (file **period_closure_income_sold_defect_refunds**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Withheld for Yandex Market services** (file **period_closure_income_fees**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Fines withheld** (file **period_closure_income_fines**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Compensation from Yandex Market** (file **period_closure_income_compensations**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Premium** (file **period_closure_income_netting**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Premium correction** (file **period_closure_income_premium_correction**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **To be transferred to you** (file **period_closure_income_will_be_paid**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Transferred to your account** (file **period_closure_income_paid**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Explanation of the report columns:
Sheet **Certificate of promotion services** (file **period_closure_outcome_summary**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
SERVICES |  services |  Services in the certificate |  string  
SERVICES_DESCRIPTION |  servicesDescription |  Compensation for this service |  string  
SERVICES_SUM |  servicesSum |  Service cost* |  number  
Sheet **Marketplace discounts** (file **period_closure_outcome_subsidy**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Yandex Plus points** (file **period_closure_outcome_plus**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Bonus for completing challenge** (file **period_closure_outcome_benefits**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Sheet **Marketplace discounts on delivery** (file **period_closure_outcome_delivery**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
MODEL |  model |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
SHOP_NAME |  shopName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
TRANSACTION_DATE |  transactionDate |  Payment information/Transaction date |  string  
TRANSACTION_ID |  transactionId |  Payment information/Transaction ID |  string  
ORDER_ID |  orderId |  Payment information/Number of order or certificate of services rendered |  integer  
SHOP_ORDER_ID |  shopOrderId |  Payment information/Your order number |  string  
ORDER_CREATION_DATE |  orderCreationDate |  Payment information/The date of the order or certificate of services rendered |  string  
CLAIM_NUMBER |  claimNumber |  Payment information/Claim number and date |  string  
ORDER_TYPE |  orderType |  Payment information/Order type |  string  
OFFER_ID |  offerId |  Payment information/Your SKU |  string  
OFFER_NAME |  offerName |  Payment information/Product name |  string  
COUNT |  count |  Payment information/Quantity, units |  integer  
TRANSACTION_SUM |  transactionSum |  Payment information/Transaction amount |  number  
TRANSACTION_TYPE |  transactionType |  Payment information/Transaction type |  string  
TRANSACTION_SOURCE |  transactionSource |  Payment information/Transaction source |  string  
PAYMENT_STATUS |  paymentStatus |  Payment information/Status |  string  
BANK_ORDER_DATE |  bankOrderDate |  Payment information/Payment order date |  string  
BANK_ORDER_ID |  bankOrderId |  Payment information/Payment order number |  integer  
BANK_ORDER_SUM |  bankOrderSum |  Payment information/Payment order amount or the amount withheld for services |  number  
Explanation of the report columns:
Sheet **Полки** (file **advertiser_operations_shelf**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
DEDUCTED_BONUSES |  deductedBonuses |  Списано бонусов |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Буст продаж, оплата за показы** (file **advertiser_operations_cpm_boost**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
DEDUCTED_BONUSES |  deductedBonuses |  Списано бонусов |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Буст продаж, оплата за продажи** (file **advertiser_operations_cpa_auction_promotion**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
DEDUCTED_BONUSES |  deductedBonuses |  Списано бонусов |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Баннеры (бронирование)** (file **advertiser_operations_package_banners**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
DEDUCTED_BONUSES |  deductedBonuses |  Списано бонусов |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Баннеры (аукцион)** (file **advertiser_operations_auction_banners**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
DEDUCTED_BONUSES |  deductedBonuses |  Списано бонусов |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Пуши (бронирование)** (file **advertiser_operations_package_pushes**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Пуши (аукцион)** (file **advertiser_operations_auction_pushes**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Поп-ап уведомления (бронировани** (file **advertiser_operations_package_popups**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Поп-ап уведомления (аукцион)** (file **advertiser_operations_auction_popups**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Полки с оплатой по дням** (file **advertiser_operations_cpd_promotion**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Рекламно-информационные материа** (file **advertiser_operations_marketing_promo_yandex_market**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
SERVICE_TYPE |  serviceType |  Тип услуги |  string  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Реклама на внешних площадках** (file **advertiser_operations_marketing_promo_web**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
SERVICE_TYPE |  serviceType |  Тип услуги |  string  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **ТВ реклама** (file **advertiser_operations_marketing_promo_tv**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
SERVICE_TYPE |  serviceType |  Тип услуги |  string  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Информационная рассылка по зада** (file **advertiser_operations_marketing_promo_mailing**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
SERVICE_TYPE |  serviceType |  Тип услуги |  string  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Организация и проведение маркет** (file **advertiser_operations_marketing_promo_for_sales**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
SERVICE_TYPE |  serviceType |  Тип услуги |  string  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Специальные размещения** (file **advertiser_operations_marketing_promo_adfox**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
SERVICE_TYPE |  serviceType |  Тип услуги |  string  
CAMPAIGN_NAME |  campaignName |  Кампания |  string  
OPERATION_TYPE |  operationType |  Тип операции |  string  
CABINET_TYPE |  cabinetType |  Тип кабинета |  string  
CABINET_NAME |  cabinetName |  Название кабинета |  string  
Sheet **Отзывы за баллы** (file **advertiser_operations_paid_opinion**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
DATE |  date |  Дата |  string  
SUM |  sum |  Сумма (с НДС), ₽ |  number  
BRAND |  brand |  Бренд |  string  
CATEGORY |  category |  Категория |  string  
MODEL |  model |  Товар |  string  
MARKET_URL |  marketUrl |  Ссылка на Маркет |  string  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/closure-documents/detalization/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#reportformattype) The format of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body)Body
application/json
```
{
    "campaignId": 0,
    "monthOfYear": {
        "year": 2025,
        "month": 12
    },
    "contractType": "INCOME"
}

```

**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.  
contractType* |  **Type:** [ClosureDocumentsContractType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#closuredocumentscontracttype) Type of agreement:
  * `INCOME` — the accommodation agreement.
  * `OUTCOME` — a promotion agreement.
  * `MARKETING` — a marketing contract.

_Enum:_ `INCOME`, `OUTCOME`, `MARKETING`  
monthOfYear* |  **Type:** [ClosureDocumentsMonthOfYearDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#closuredocumentsmonthofyeardto) The month for which the necessary closing documents were generated.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#closuredocumentscontracttype)ClosureDocumentsContractType
Type of agreement:
  * `INCOME` — the accommodation agreement.
  * `OUTCOME` — a promotion agreement.
  * `MARKETING` — a marketing contract.

**Type** |  **Description**  
---|---  
[ClosureDocumentsContractType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#closuredocumentscontracttype) |  _Enum:_ `INCOME`, `OUTCOME`, `MARKETING`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#closuredocumentsmonthofyeardto)ClosureDocumentsMonthOfYearDTO
Month and year.
**Name** |  **Description**  
---|---  
month* |  **Type:** integer<int32> The month number. _Example:_ `12` _Min value:_ `1` _Max value:_ `12`  
year* |  **Type:** integer<int32> Year. _Example:_ `2025`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
Body{ "campaignId": 0, "monthOfYear": { "year": 2025, "month": 12 }, "contractType": "INCOME" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Report on the cost of services](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport)
Next
[Product Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/assortment/getGoodsStats)
