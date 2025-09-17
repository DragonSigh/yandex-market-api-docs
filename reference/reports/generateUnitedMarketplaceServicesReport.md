---
title: Report on the cost of services - Reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/generateUnitedMarketplaceServicesReport
crawled_at: 2025-09-17T14:36:34.425841
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#request)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#query-parameters)
    * [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#reportformattype)
    * [ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#reportlanguagetype)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body)
    * [PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#placementtype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body1)
    * [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#generatereportdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body6)


The structure and content of the reports are subject to change without prior notice.
For example, a new column may be added or the name of the sheet may be changed.
# Report on the cost of services
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management


Starts the generation of a report on the cost of services for a specified period. [What kind of report is this](https://yandex.ru/support/marketplace/ru/accounting/transactions#reports)
The type of report depends on which fields are filled in in the request:
**Report type** | **What fields are needed?**  
---|---  
By the date of service accrual |  `dateFrom` and `dateTo`  
By the date of the act formation |  `year` and `month`  
You cannot order both types of reports with a single request.
You can find out the generation status and get a link to the finished report using a request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/getReportInfo).
Explanation of the report columns:
Sheet **Product placement on the showcase** (file **placement**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Order and product information/Order number |  integer  
ORDER_CREATION_DATE_TIME |  orderCreationDateTime |  Order and product information/Order creation date |  string  
SHOP_SKU |  shopSku |  Order and product information/Your SKU |  string  
OFFER_NAME |  offerName |  Order and product information/Product name |  string  
TURBO_GOODS |  turboGoods |  Order and product information/Product type |  string  
PRICE |  price |  Order and product information/Your price per item |  number  
DECOUPLING_MARKUP |  decouplingMarkup |  Order and product information/Difference between your price and sale price |  number  
COUNT |  count |  Order and product information/Quantity, units |  integer  
BATCH_SIZE |  batchSize |  Order and product information/Sale quantum |  integer  
BATCH_COUNT |  batchCount |  Order and product information/Quanta in the order |  integer  
BATCH_PRICE |  batchPrice |  Order and product information/Price per quantum |  number  
WEIGHT |  weight |  Order and product information/Weight, kg |  number  
LENGTH |  length |  Order and product information/Length, cm |  number  
WIDTH |  width |  Order and product information/Width, cm |  number  
HEIGHT |  height |  Order and product information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Order and product information/Sum of three dimensions, cm |  number  
PAYMENT_TYPE |  paymentType |  Order and product information/Payment acceptance method |  string  
QUALITY_INDEX |  qualityIndex |  Order and product information/Quality index value |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF_TERMS |  tariffTerms |  Service information/Tariff conditions |  string  
TARIFF |  tariff |  Service information/Rate per item |  number  
UNIT |  unit |  Service information/Unit of measurement |  string  
MIN_TARIFF |  minTariff |  Service information/Minimum rate per item |  number  
MAX_TARIFF |  maxTariff |  Service information/Maximum rate per item |  number  
SERVICE_BEFORE_TARIFF |  serviceBeforeTariff |  Service information/Service price up to minimum rate |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
AMOUNT_WITHOUT_BONUSES |  amountWithoutBonuses |  Service information/Price of service without discounts and surcharges |  number  
FEE_BENEFIT_TARIFF |  feeBenefitTariff |  Service price decrease (discount) and increase/Removals and rewards/Rate, % |  number  
FEE_BENEFIT_DISCOUNT |  feeBenefitDiscount |  Service price decrease (discount) and increase/Removals and rewards/Discount based on the minimum tariff |  number  
DAYS_OF_DELAY |  daysOfDelay |  Service price decrease (discount) and increase/Cancellations due to seller's fault, late shipment or delivery/Delay in shipment or delivery, days |  integer  
LATE_ORDER_EXECUTION_FEE_TARIFF |  lateOrderExecutionFeeTariff |  Service price decrease (discount) and increase/Cancellations due to seller's fault, late shipment or delivery/Rate for late shipment or delivery, % of placement rate |  number  
CANCELLATION_ORDER_FEE_TARIFF |  cancellationOrderFeeTariff |  Service price decrease (discount) and increase/Cancellations due to seller's fault, late shipment or delivery/Rate when canceled due to seller's fault, % of placement rate |  number  
QUALITY_INDEX_MIN_TARIFF |  qualityIndexMinTariff |  Service price decrease (discount) and increase/Cancellations due to seller's fault, late shipment or delivery/Min price per item |  number  
QUALITY_INDEX_MAX_TARIFF |  qualityIndexMaxTariff |  Service price decrease (discount) and increase/Cancellations due to seller's fault, late shipment or delivery/Max price per item |  number  
QUALITY_INDEX_AMOUNT |  qualityIndexAmount |  Service price decrease (discount) and increase/Cancellations due to seller's fault, late shipment or delivery/Service price change |  number  
DECOUPLING_TARIFF |  decouplingTariff |  Service price decrease (discount) and increase/Smart offer/Rate, % |  number  
DECOUPLING_PRICE_CHANGE |  decouplingPriceChange |  Service price decrease (discount) and increase/Smart offer/Service price change |  number  
INDIVIDUAL_DISCOUNT |  individualDiscount |  Service price decrease (discount) and increase/Other discounts/Custom discount for service |  number  
LOYALTY_DISCOUNT |  loyaltyDiscount |  Service price decrease (discount) and increase/Other discounts/Loyalty discount |  number  
NETTING |  netting |  Service price decrease (discount) and increase/Other discounts/Discount for participation in joint promotions |  number  
TOTAL_AMOUNT |  totalAmount |  Service cost |  number  
Sheet **Warehouse processing** (file **warehouse_processing**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Order and product information/Order number |  integer  
SHOP_SKU |  shopSku |  Order and product information/Your SKU |  string  
OFFER_NAME |  offerName |  Order and product information/Product name |  string  
PRICE |  price |  Order and product information/Your price per item |  number  
COUNT |  count |  Order and product information/Quantity, units |  integer  
BATCH_SIZE |  batchSize |  Order and product information/Sale quantum |  integer  
BATCH_COUNT |  batchCount |  Order and product information/Quanta in the order |  integer  
BATCH_PRICE |  batchPrice |  Order and product information/Price per quantum |  number  
WEIGHT |  weight |  Order and product information/Weight, kg |  number  
LENGTH |  length |  Order and product information/Length, cm |  number  
WIDTH |  width |  Order and product information/Width, cm |  number  
HEIGHT |  height |  Order and product information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Order and product information/Sum of three dimensions, cm |  number  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate per item |  number  
UNIT |  unit |  Service information/Unit of measurement |  string  
MIN_TARIFF |  minTariff |  Service information/Minimum rate per item |  number  
MAX_TARIFF |  maxTariff |  Service information/Maximum rate per item |  number  
SERVICE_PRICE_BEFORE_TARIFF |  servicePriceBeforeTariff |  Service information/Service price without rate restrictions |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Acceptance of supply** (file **goods_acceptance**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
FF_REEQUEST_ID |  ffReequestId |  Service information/Yandex Market delivery number |  string  
WMS_ID |  wmsId |  Service information/Supply number in warehouse |  string  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
WEIGHT |  weight |  Service information/Weight, kg |  number  
LENGTH |  length |  Service information/Length, cm |  number  
WIDTH |  width |  Service information/Width, cm |  number  
HEIGHT |  height |  Service information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Service information/Sum of three dimensions, cm |  number  
CARGO_PLACE_TYPE |  cargoPlaceType |  Service information/Type of cargo space or goods |  string  
COUNT |  count |  Service information/Quantity, units |  integer  
ACCEPTANCE_STAGE |  acceptanceStage |  Service information/Stage |  string  
TARIFF |  tariff |  Service information/Rate per item |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Loyalty program and reviews** (file **loyalty_and_reviews**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
PRICE |  price |  Service information/Your price per item |  number  
CLIENT_PRICE |  clientPrice |  Service information/User paid |  number  
COUNT |  count |  Service information/Quantity, units |  integer  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
REVIEW_ID |  reviewId |  Service information/Review ID |  string  
UNIT |  unit |  Service information/Unit of measurement |  string  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
TARIFF_OR_PRICE_FOR_REVIEW |  tariffOrPriceForReview |  Service information/Rate per item/Seller price per review |  number  
Sheet **Sales boost, payment for sales** (file **boost**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
CATEGORY |  category |  Service information/Category |  string  
PRICE |  price |  Service information/Your price per item |  number  
COUNT |  count |  Service information/Quantity, units |  integer  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
BET |  bet |  Service information/Effective bid, % of sale price |  number  
PREPAID |  prepaid |  Service information/Prepayment |  number  
POSTPAID |  postpaid |  Service information/Post-payment |  number  
BONUS_PAID |  bonusPaid |  Service information/Payment in bonuses |  number  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
Sheet **Installment plan** (file **installment_plan**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
PRICE |  price |  Service information/Your price per item |  number  
COUNT |  count |  Service information/Quantity, units |  integer  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate per item (applied to product price before discounts) |  number  
UNIT |  unit |  Service information/Unit of measurement |  string  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
TYPE |  type |  Service information/Record type |  string  
Sheet **Shelves** (file **shelf**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ADVERTISER_ID |  advertiserId |  Service information/Advertiser ID |  integer  
LIMIT_TYPE |  limitType |  Service information/Budget type |  string  
CAMPAIGN_ID |  campaignId |  Service information/Campaign number |  integer  
CAMPAIGN_NAME |  campaignName |  Service information/Campaign name |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
EVENTS_COUNT |  eventsCount |  Service information/Number of impressions |  string  
DAILY_LIMIT |  dailyLimit |  Service information/Budget |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
COUPON_AMOUNT |  couponAmount |  Service information/Bonuses spent |  number  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Boost sales with pay-per-views** (file **cpm-boost**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ADVERTISER_ID |  advertiserId |  Service information/Advertiser ID |  integer  
CAMPAIGN_ID |  campaignId |  Service information/Campaign number |  integer  
CAMPAIGN_NAME |  campaignName |  Service information/Campaign name |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
EVENTS_COUNT |  eventsCount |  Service information/Number of impressions |  integer  
DAILY_LIMIT |  dailyLimit |  Service information/Budget |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Banners** (file **banners**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ADVERTISER_ID |  advertiserId |  Service information/Advertiser ID |  integer  
CAMPAIGN_ID |  campaignId |  Service information/Campaign number |  integer  
CAMPAIGN_NAME |  campaignName |  Service information/Campaign name |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
EVENTS_COUNT |  eventsCount |  Service information/Number of impressions |  integer  
DAILY_LIMIT |  dailyLimit |  Service information/Budget |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
LIMIT_TYPE |  limitType |  Service information/Budget type |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Push-notifications** (file **pushes**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ADVERTISER_ID |  advertiserId |  Service information/Advertiser ID |  integer  
CAMPAIGN_ID |  campaignId |  Service information/Campaign number |  integer  
CAMPAIGN_NAME |  campaignName |  Service information/Campaign name |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
EVENTS_COUNT |  eventsCount |  Service information/Number of impressions |  integer  
DAILY_LIMIT |  dailyLimit |  Service information/Budget |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
LIMIT_TYPE |  limitType |  Service information/Budget type |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Pop-up notifications** (file **popups**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ADVERTISER_ID |  advertiserId |  Service information/Advertiser ID |  integer  
CAMPAIGN_ID |  campaignId |  Service information/Campaign number |  integer  
CAMPAIGN_NAME |  campaignName |  Service information/Campaign name |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
EVENTS_COUNT |  eventsCount |  Service information/Number of impressions |  integer  
DAILY_LIMIT |  dailyLimit |  Service information/Budget |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
LIMIT_TYPE |  limitType |  Service information/Budget type |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Delivery to buyer** (file **delivery**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Order and product information/Order number |  integer  
SHOP_SKU |  shopSku |  Order and product information/Your SKU |  string  
OFFER_NAME |  offerName |  Order and product information/Product name |  string  
PRICE |  price |  Order and product information/Your price per item |  number  
COUNT |  count |  Order and product information/Quantity, units |  integer  
BATCH_SIZE |  batchSize |  Order and product information/Sale quantum |  integer  
BATCH_COUNT |  batchCount |  Order and product information/Quanta in the order |  integer  
BATCH_PRICE |  batchPrice |  Order and product information/Price per quantum |  number  
WEIGHT |  weight |  Order and product information/Weight, kg |  number  
DIMENSIONAL_WEIGHT |  dimensionalWeight |  Order and product information/Volumetric weight, kg |  number  
LENGTH |  length |  Order and product information/Length, cm |  number  
WIDTH |  width |  Order and product information/Width, cm |  number  
HEIGHT |  height |  Order and product information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Order and product information/Sum of three dimensions, cm |  number  
LOCALITY_INDEX |  localityIndex |  Order and product information/Share of local sales, % |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
FROM |  from |  Service information/From |  string  
TO |  to |  Service information/Destination |  string  
TARIFF |  tariff |  Service information/Rate per item |  number  
UNIT |  unit |  Service information/Unit of measurement |  string  
MIN_TARIFF |  minTariff |  Service information/Minimum rate per item |  number  
MAX_TARIFF |  maxTariff |  Service information/Maximum rate per item |  number  
SERVICE_PRICE_BEFORE_TARIFF |  servicePriceBeforeTariff |  Service information/Service price without rate restrictions |  number  
LOCALITY_COEFFICIENT |  localityCoefficient |  Service information/Locality coefficient |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Express delivery** (file **express_delivery**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Order and product information/Order number |  integer  
SHOP_SKU |  shopSku |  Order and product information/Your SKU |  string  
OFFER_NAME |  offerName |  Order and product information/Product name |  string  
PRICE |  price |  Order and product information/Your price per item |  number  
COUNT |  count |  Order and product information/Quantity, units |  integer  
BATCH_SIZE |  batchSize |  Order and product information/Sale quantum |  integer  
BATCH_COUNT |  batchCount |  Order and product information/Quanta in the order |  integer  
BATCH_PRICE |  batchPrice |  Order and product information/Price per quantum |  number  
WEIGHT |  weight |  Order and product information/Weight, kg |  number  
LENGTH |  length |  Order and product information/Length, cm |  number  
WIDTH |  width |  Order and product information/Width, cm |  number  
HEIGHT |  height |  Order and product information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Order and product information/Sum of three dimensions, cm |  number  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate per order/item |  number  
UNIT |  unit |  Service information/Unit of measurement |  string  
MIN_TARIFF |  minTariff |  Service information/Minimum rate per item |  number  
MAX_TARIFF |  maxTariff |  Service information/Maximum rate per item |  number  
SERVICE_PRICE_BEFORE_TARIFF |  servicePriceBeforeTariff |  Service information/Service price without rate restrictions |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Delivery from abroad** (file **delivery_from_abroad**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Order information/Order number |  integer  
PARCELS_COUNT |  parcelsCount |  Order information/Number of products in the order (items) |  integer  
WEIGHT |  weight |  Order information/Total weight of items in the order, kg |  number  
WEIGHT_ROUNDED |  weightRounded |  Order information/Weight after rounding, kg |  number  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
FROM |  from |  Service information/From |  string  
TO |  to |  Service information/Destination |  string  
SHIPPING_TARIFF |  shippingTariff |  Service information/Rate for shipment |  number  
TARIFF_FOR_WEIGHT |  tariffForWeight |  Service information/Rate per 1 kg |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Payment acceptance** (file **payment_accepting**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
BUYER_PAID |  buyerPaid |  Service information/Paid by buyer |  number  
TARIFF |  tariff |  Service information/Rate per item |  number  
UNIT |  unit |  Service information/Unit of measurement |  string  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
RECORD_TYPE |  recordType |  Service information/Record type |  string  
Sheet **Payment transfer** (file **payment_transfer**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
BUYER_PAID |  buyerPaid |  Service information/Paid by buyer |  number  
TARIFF_FOR_TRANSFER |  tariffForTransfer |  Service information/Transfer rate, % of paid amount |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
RECORD_TYPE |  recordType |  Service information/Record type |  string  
Sheet **Paid storage through May 31, 2022** (file **paid_storage_before_31-05-22**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
MARKET_SKU |  marketSku |  Service information/SKU in Yandex |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
COUNT |  count |  Service information/Quantity, units |  integer  
WEIGHT |  weight |  Service information/Weight, kg |  number  
LENGTH |  length |  Service information/Length, cm |  number  
WIDTH |  width |  Service information/Width, cm |  number  
HEIGHT |  height |  Service information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Service information/Sum of three dimensions, cm |  number  
TARIFF |  tariff |  Service information/Rate per item |  number  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Paid storage from June 1, 2022** (file **paid_storage_after_01-06-22**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
CATEGORY |  category |  Service information/Category |  string  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
WAREHOUSE |  warehouse |  Service information/Warehouse or cluster |  string  
AVG_STOCK_LITERS |  avgStockLiters |  Service information/Average daily volume of goods in stock, liters |  number  
AVG_SOLD_LITERS |  avgSoldLiters |  Service information/Average daily volume of goods sold, liters |  number  
TURNOVER_DAYS |  turnoverDays |  Service information/Turnover, days |  string  
LENGTH_PRODUCT_M |  lengthProductM |  Service information/Length of the product unit, m |  string  
WIDTH_PRODUCT_M |  widthProductM |  Service information/Product unit width, m |  string  
HEIGHT_PRODUCT_M |  heightProductM |  Service information/The height of the product unit, m |  string  
COUNT_PRODUCT_UNIT |  countProductUnit |  Service information/Number of product units, pcs. |  string  
VOLUME_UNITS_OF_GOODS |  volumeUnitsOfGoods |  Service information/The volume of all units of goods, cubic meters |  string  
MEASUREMENT_UNIT |  measurementUnit |  Service information/Unit of measurement |  string  
TARIFF |  tariff |  Service information/Rate |  number  
TRANSACTION_TYPE |  transactionType |  Service information/Transaction type |  string  
STORAGE_PERIOD |  storagePeriod |  Service information/Number of storage days according to rate |  integer  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
PAID_STORAGE |  paidStorage |  Service information/Cost of paid storage |  number  
Sheet **Supply via transit warehouse** (file **delivery_via_transit_warehouse**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
MARKET_DELIVERY_ID |  marketDeliveryId |  Service information/Yandex Market delivery number |  string  
WAREHOUSE_DELIVERY_ID |  warehouseDeliveryId |  Service information/Supply number in warehouse |  integer  
SERVICES_COLUMN_MANY_WAREHOUSES_SUPPLY |  servicesColumnManyWarehousesSupply |  Service information/Supply for multiple warehouses |  string  
SERVICES_COLUMN_VDC_DIRECTIONS_COUNT |  servicesColumnVdcDirectionsCount |  Service information/The number of destinations reached in the supply |  integer  
IS_BOX |  isBox |  Service information/Pallet or box |  string  
TURBO_PERCENTAGE |  turboPercentage |  Service information/The share of turbo in the supply, % |  number  
TARIFF |  tariff |  Service information/Rate per item |  number  
BOX_COUNT |  boxCount |  Service information/Number of pallets or boxes |  integer  
DISCOUNT_PERCENT |  discountPercent |  Service information/Discount, % |  number  
DISCOUNT_AMOUNT |  discountAmount |  Service information/Discount |  number  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Acceptance of surplus products at warehouse** (file **reception_of_surplus**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
MARKET_DELIVERY_ID |  marketDeliveryId |  Service information/Yandex Market delivery number |  string  
WAREHOUSE_DELIVERY_ID |  warehouseDeliveryId |  Service information/Supply number in warehouse |  integer  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
TARIFF |  tariff |  Service information/Rate per item |  number  
COUNT |  count |  Service information/Quantity, units |  integer  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
PAYMENT_TYPE |  paymentType |  Service information/Accrual type |  string  
Sheet **Applying the marking sign** (file **product_marking**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
MARKET_DELIVERY_ID |  marketDeliveryId |  Service information/Yandex Market delivery number |  integer  
WAREHOUSE_DELIVERY_ID |  warehouseDeliveryId |  Service information/Supply number in warehouse |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate per item |  number  
COUNT |  count |  Service information/Quantity, units |  integer  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Removal from warehouse, sorting center, order pickup point** (file **export_from_warehouse**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
MARKET_REQUEST_ID |  marketRequestId |  Service information/Yandex Market request number |  string  
WAREHOUSE_REQUEST_ID |  warehouseRequestId |  Service information/Request number in warehouse |  string  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
STOCK |  stock |  Service information/Stock |  string  
ESTIMATED_COST |  estimatedCost |  Service information/Estimated price |  number  
COUNT |  count |  Service information/Quantity, units |  integer  
WEIGHT |  weight |  Service information/Weight, kg |  number  
LENGTH |  length |  Service information/Length, cm |  number  
WIDTH |  width |  Service information/Width, cm |  number  
HEIGHT |  height |  Service information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Service information/Sum of three dimensions, cm |  number  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate per item |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Order pickup arrangement** (file **intake_logistics**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
OFFER_NAME |  offerName |  Service information/Product name |  string  
GOODS_COUNT |  goodsCount |  Service information/Number of products (items) |  integer  
CARGO_TYPE |  cargoType |  Service information/Product type |  string  
WEIGHT |  weight |  Service information/Weight, kg |  number  
DIMENSIONAL_WEIGHT |  dimensionalWeight |  Service information/Volumetric weight, kg |  number  
LENGTH |  length |  Service information/Length, cm |  number  
WIDTH |  width |  Service information/Width, cm |  number  
HEIGHT |  height |  Service information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Service information/Sum of three dimensions, cm |  number  
ORDER_COUNT |  orderCount |  Service information/Order quantity |  integer  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
UNIT_NAME |  unitName |  Service information/What the rate is applied to |  string  
TARIFF |  tariff |  Service information/Rate per order/item |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
RECORD_TYPE |  recordType |  Service information/Record type |  string  
Sheet **Processing orders in the sorting center or order pickup point** (file **order_processing**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
BOX_EXTERNAL_ID |  boxExternalId |  Service information/Return package number (box bar code) |  string  
LOCATION |  location |  Service information/Place of order shipment |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate per order or shipment |  number  
MIN_AMOUNT |  minAmount |  Service information/Minimum amount |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
RECORD_TYPE |  recordType |  Service information/Record type |  string  
Sheet **Processing orders in the warehouse** (file **order_processing_on_warehouse**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
BOX_EXTERNAL_ID |  boxExternalId |  Service information/Return package number (box bar code) |  string  
TARIFF |  tariff |  Service information/Rate for shipment |  number  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Storage of unpurchased goods and returns** (file **storage_of_returns**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
RESUPPLY_TYPE |  resupplyType |  Service information/Return or non-purchase |  string  
ORDER_ID |  orderId |  Service information/Order number |  integer  
RETURN_ID |  returnId |  Service information/Return number |  integer  
RETURN_COUNT |  returnCount |  Service information/Number of returned products (items) |  integer  
UNREDEEMED_ORDER_TARIFF |  unredeemedOrderTariff |  Service information/Rate for storing unpurchased order |  number  
RETURN_TARIFF |  returnTariff |  Service information/Rate for storing return |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
RECORD_TYPE |  recordType |  Service information/Record type |  string  
Sheet **Resale commission** (file **expropriation**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
ORDER_NUMBER |  orderNumber |  Order and product information/Order number |  integer  
SKU |  sku |  Order and product information/Your SKU |  string  
PRODUCT_NAME |  productName |  Order and product information/Product name |  string  
MERCHANT_PRICE |  merchantPrice |  Order and product information/Your price |  number  
SELL_PRICE |  sellPrice |  Order and product information/Sale price |  number  
SERVICE |  service |  Service information/Service |  string  
TARIFF_PER_ITEM |  tariffPerItem |  Service information/Rate per item |  number  
MEASUREMENT_UNIT |  measurementUnit |  Service information/Unit of measurement |  string  
DATE_TIME |  dateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
FULL_PRICE |  fullPrice |  Service information/Service price |  number  
Sheet **Disposal arrangement** (file **utilization**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
UTILIZATION_REQUEST_ID |  utilizationRequestId |  Service information/Disposal request number |  string  
UTILIZATION_REQUEST_DATE_TIME |  utilizationRequestDateTime |  Service information/Date and time of disposal request creation |  string  
SHOP_SKU |  shopSku |  Service information/Your SKU |  string  
OFFER_NAME |  offerName |  Service information/Product name |  string  
COUNT |  count |  Service information/Quantity, units |  integer  
WEIGHT |  weight |  Service information/Weight, kg |  number  
LENGTH |  length |  Service information/Length, cm |  number  
WIDTH |  width |  Service information/Width, cm |  number  
HEIGHT |  height |  Service information/Height, cm |  number  
DIMENSIONS_SUM |  dimensionsSum |  Service information/Sum of three dimensions, cm |  number  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate |  number  
SERVICE_DATE_TIME |  serviceDateTime |  Service information/Service date and time |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Extended access to services** (file **extended_service_access**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
SECURITY_PAYMENT_ID |  securityPaymentId |  Service information/Security payment number |  string  
SECURITY_PAYMENT_DATE |  securityPaymentDate |  Service information/Security payment date |  string  
SECURITY_PAYMENT_AMOUNT |  securityPaymentAmount |  Service information/Security payment amount |  number  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
Sheet **Personal manager** (file **personal_manager**)
**CSV column name** |  **JSON column name** |  **XLSX column name** |  **Value type**  
---|---|---|---  
BUSINESS_ID |  businessId |  Business information/Business account ID |  integer  
PLACEMENT_MODEL |  placementModel |  Business information/Operation models |  string  
PARTNER_ID |  partnerId |  Business information/Store IDs |  integer  
PARTNER_NAME |  partnerName |  Business information/Store names |  string  
INN |  inn |  Business information/INN (taxpayer identification number) |  string  
PLACEMENT_CONTRACT |  placementContract |  Business information/Agreement numbers for placement |  string  
PROMOTION_CONTRACT |  promotionContract |  Business information/Agreement numbers for promotion |  string  
SERVICE_NAME |  serviceName |  Service information/Service |  string  
TARIFF |  tariff |  Service information/Rate per month |  number  
SERVICE_DATE |  serviceDate |  Service information/Service date |  string  
ACT_DATE |  actDate |  Service information/Certificate creation date |  string  
SERVICE_PRICE |  servicePrice |  Service information/Service price |  number  
COMMENTARY |  commentary |  Service information/Commentary |  string  
**, Limit:** 100 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/reports/united-marketplace-services/generate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
format |  **Type:** [ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#reportformattype) The format of the report or document.  
language |  **Type:** [ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#reportlanguagetype) The language of the report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#reportformattype)ReportFormatType
Report format:
  * `FILE` — a spreadsheet file (XLSX).
  * `CSV` — ZIP archive with CSV files for each report sheet.
  * `JSON` — ZIP archive with JSON files for each report sheet.

**Type** |  **Description**  
---|---  
[ReportFormatType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#reportformattype) |  _Default:_ `FILE` _Enum:_ `FILE`, `CSV`, `JSON`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#reportlanguagetype)ReportLanguageType
Language of the report:
  * `RU` — Russian language.
  * `EN` — English language.

**Type** |  **Description**  
---|---  
[ReportLanguageType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#reportlanguagetype) |  _Enum:_ `RU`, `EN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body)Body
application/json
```
{
    "businessId": 0,
    "dateTimeFrom": "2022-12-29T18:02:01Z",
    "dateTimeTo": "2022-12-29T18:02:01Z",
    "dateFrom": "string",
    "dateTo": "string",
    "yearFrom": 2025,
    "monthFrom": 12,
    "yearTo": 2025,
    "monthTo": 12,
    "placementPrograms": [
        "FBS"
    ],
    "inns": [
        "string"
    ],
    "campaignIds": [
        0
    ]
}

```

**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
campaignIds |  **Type:** integer<int64>[] The list of campaign IDs of those stores that are needed in the report. You can find them using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not use store IDs instead, which are listed in the seller's account on the Market next to the store name and in some reports.   
_Min items:_ `1` _Unique items_  
dateFrom |  **Type:** string<date> The beginning of the period, inclusive.  
dateTimeFrom ⦸ |  **Type:** string<date-time> The beginning of the period, inclusive.  
dateTimeTo ⦸ |  **Type:** string<date-time> End of the period, inclusive. The maximum period is 3 months.  
dateTo |  **Type:** string<date> End of the period, inclusive. The maximum period is 3 months.  
inns |  **Type:** string[] The list of INN's that are needed in the report.  
_Min items:_ `1` _Unique items_  
monthFrom |  **Type:** integer<int32> The month number. _Example:_ `12` _Min value:_ `1` _Max value:_ `12`  
monthTo |  **Type:** integer<int32> The month number. _Example:_ `12` _Min value:_ `1` _Max value:_ `12`  
placementPrograms |  **Type:** [PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#placementtype)[] The list of models that are needed in the report.   
The model that the store uses:
  * `FBS` — FBS or Express.
  * `FBY` — FBY.
  * `DBS` — DBS.

_Enum:_ `FBS`, `FBY`, `DBS`, `LAAS` _Min items:_ `1` _Unique items_  
yearFrom |  **Type:** integer<int32> Year. _Example:_ `2025`  
yearTo |  **Type:** integer<int32> Year. _Example:_ `2025`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#placementtype)PlacementType
The model that the store uses:
  * `FBS` — FBS or Express.
  * `FBY` — FBY.
  * `DBS` — DBS.

**Type** |  **Description**  
---|---  
[PlacementType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#placementtype) |  _Enum:_ `FBS`, `FBY`, `DBS`, `LAAS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#200-ok)200 OK
In response, you receive an identifier that allows you to find out the generation status and download the finished report.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body1)Body
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
result |  **Type:** [GenerateReportDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#generatereportdto) The ID that will be needed to track the generation status and receive the finished report or document.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#generatereportdto)GenerateReportDTO
The ID that will be needed to track the generation status and receive the finished report or document.
**Name** |  **Description**  
---|---  
estimatedGenerationTime* |  **Type:** integer<int64> Expected generation time in milliseconds.  
reportId* |  **Type:** string The ID that will be needed to track the generation status and receive the finished report or document.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateUnitedMarketplaceServicesReport#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Query parameters
format:
language:
Body{ "businessId": 0, "dateTimeFrom": "2022-12-29T18:02:01Z", "dateTimeTo": "2022-12-29T18:02:01Z", "dateFrom": "string", "dateTo": "string", "yearFrom": 2025, "monthFrom": 12, "yearTo": 2025, "monthTo": 12, "placementPrograms": [ "FBS" ], "inns": [ "string" ], "campaignIds": [ 0 ] }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Implementation Report](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateGoodsRealizationReport)
Next
[Report on convergence with closing documents](https://yandex.ru/dev/market/partner-api/doc/en/reference/reports/en/reference/reports/generateClosureDocumentsDetalizationReport)
