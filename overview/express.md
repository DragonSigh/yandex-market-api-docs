---
title: List of methods used in the Express model | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/overview/express
crawled_at: 2025-09-17T14:24:20.610657
---

Offices and shops
# List of methods used in the Express model
  * [Offices and shops](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#offices-and-shops)
  * [Products](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#products)
  * [Balances and turnover](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#balances-and-turnover)
  * [Prices](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#prices)
  * [Orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#orders)
  * [FBS and DBS shortcuts](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#fbs-and-dbs-shortcuts)
  * [Non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#non-purchases-and-refunds)
  * [Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#reports-and-documents)
  * [Quality index](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#quality-index)
  * [Warehouses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#warehouses)
  * [Reference books](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#reference-books)


If you use the Express model, couriers come directly to your warehouse or point of sale, pick up packaged orders and immediately deliver them to customers. Read more about the model in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/introduction/models#express).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#offices-and-shops)Offices and shops
**Method** |  **Method description**  
---|---  
[GET v2/​campaigns](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaigns) |  User's Store List  
[GET v2/​campaigns/​{campaignId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaign) |  Store Information  
[GET v2/​campaigns/​{campaignId}/​settings](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaignSettings) |  Store Settings  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#products)Products
**Method** |  **Method description**  
---|---  
[POST v2/​categories/​tree](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/categories/getCategoriesTree) |  The category tree  
[POST v2/​category/​{categoryId}/​parameters](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/content/getCategoryContentParameters) |  Lists of product characteristics by category  
[POST v2/​campaigns/​{campaignId}/​offers/​update](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/updateCampaignOffers) |  Changing the terms of sale of goods in the store  
[POST v2/​campaigns/​{campaignId}/​offers](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getCampaignOffers) |  Information about the products that are placed in the specified store  
[POST v2/​campaigns/​{campaignId}/​offers/​delete](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/deleteCampaignOffers) |  Removing items from the store's assortment  
[GET v2/​campaigns/​{campaignId}/​hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getHiddenOffers) |  Information about the goods you have hidden  
[POST v2/​campaigns/​{campaignId}/​hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/addHiddenOffers) |  Hiding products and hiding settings  
[POST v2/​campaigns/​{campaignId}/​hidden-offers/​delete](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/deleteHiddenOffers) |  Resuming product display  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#balances-and-turnover)Balances and turnover
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​offers/​stocks](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/stocks/getStocks) |  Information about balances and turnover  
[PUT v2/​campaigns/​{campaignId}/​offers/​stocks](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/stocks/updateStocks) |  Transmitting information about balances  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#prices)Prices
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​offer-prices/​updates](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/updatePrices) |  Setting prices for products in a specific store  
[POST v2/​campaigns/​{campaignId}/​offer-prices](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getPricesByOfferIds) |  View prices for specified products in a specific store  
[POST v2/​campaigns/​{campaignId}/​price-quarantine](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getCampaignQuarantineOffers) |  List of quarantined products by price in the store  
[POST v2/​campaigns/​{campaignId}/​price-quarantine/​confirm](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/confirmCampaignPrices) |  Removing an item from quarantine for the price in the store  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#orders)Orders
**Method** |  **Method description**  
---|---  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrder) |  Information about a single order  
[GET v2/​campaigns/​{campaignId}/​orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrders) |  Information about multiple orders  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​boxes](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/setOrderBoxLayout) |  Order preparation  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​external-id](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/updateExternalOrderId) |  Transmitting an external order ID  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​status](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/updateOrderStatus) |  Changing the status of an order  
[POST v2/​campaigns/​{campaignId}/​orders/​status-update](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/updateOrderStatuses) |  Changing the statuses of multiple orders  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​identifiers/​status](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrderIdentifiersStatus) |  LOGIN verification Statuses  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​verifyEac](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/verifyOrderEac) |  Sending the confirmation code  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​business-buyer](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/order-business-information/getOrderBusinessBuyerInfo) |  Information about the buyer — a legal entity  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/order-business-information/getOrderBusinessDocumentsInfo) |  Information about documents  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#fbs-and-dbs-shortcuts)FBS and DBS shortcuts
**Method** |  **Method description**  
---|---  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​shipments/​{shipmentId}/​boxes/​{boxId}/​label](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/generateOrderLabel) |  Ready‑made label-sticker for the box in the order  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​labels](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/generateOrderLabels) |  Ready‑made labels-stickers for all boxes in one order  
[POST v2/​reports/​documents/​labels/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/generateMassOrderLabelsReport) |  Ready‑made labels-stickers for all boxes in several orders  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​labels/​data](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrderLabelsData) |  Data for self-label production  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#non-purchases-and-refunds)Non-purchases and refunds
**Method** |  **Method description**  
---|---  
[GET v2/​campaigns/​{campaignId}/​returns](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturns) |  List of non-purchases and refunds  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturn) |  Information about non-purchase or refund  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​application](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturnApplication) |  Receiving a refund request  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​decision/​{itemId}/​image/​{imageHash}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturnPhoto) |  Receiving photos of items in a refund  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​decision/​submit](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/submitReturnDecision) |  Transfer and confirmation of the refund decision  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#reports-and-documents)Reports and documents
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​stats/​orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/stats/getOrdersStats) |  Detailed information on orders  
[POST v2/​reports/​closure-documents/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateClosureDocumentsReport) |  Closing documents  
[POST v2/​reports/​united-returns/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateUnitedReturnsReport) |  Report on non-purchases and refunds  
[POST v2/​reports/​stocks-on-warehouses/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateStocksOnWarehousesReport) |  Warehouse balance report  
[POST v2/​reports/​united-marketplace-services/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateUnitedMarketplaceServicesReport) |  Report on the cost of services  
[POST v2/​reports/​closure-documents/​detalization/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateClosureDocumentsDetalizationReport) |  Report on convergence with closing documents  
[POST v2/​campaigns/​{campaignId}/​stats/​skus](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getGoodsStats) |  Product Report  
[GET v2/​reports/​info/​{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/getReportInfo) |  Getting a given report or document  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#quality-index)Quality index
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​ratings/​quality/​details](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/ratings/getQualityRatingDetails) |  Orders that affected the quality index  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#warehouses)Warehouses
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​warehouse/​status](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/warehouses/updateWarehouseStatus) |  Changing the warehouse status  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express#reference-books)Reference books
**Method** |  **Method description**  
---|---  
[POST v2/​auth/​token](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/auth/getAuthTokenInfo) |  Getting information about the authorization token  
[GET v2/​delivery/​services](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getDeliveryServices) |  Directory of delivery services  
[POST v2/​regions/​countries](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/getRegionsCodes) |  List of valid country codes  
[GET v2/​regions](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionsByName) |  Search for regions by their name  
[GET v2/​regions/​{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionsById) |  Information about the region  
[GET v2/​regions/​{regionId}/​children](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionChildren) |  Information about child regions  
### Was the article helpful?
YesNo
Previous
[FBS](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fbs)
Next
[DBS](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/dbs)
