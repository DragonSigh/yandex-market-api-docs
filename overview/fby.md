---
title: List of methods used in the FBY model | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/overview/fby
crawled_at: 2025-09-17T14:24:08.563062
---

Offices and shops
# List of methods used in the FBY model
  * [Offices and shops](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#offices-and-shops)
  * [Products](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#products)
  * [Balances and turnover](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#balances-and-turnover)
  * [Prices](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#prices)
  * [Orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#orders)
  * [FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#fby-requests)
  * [Non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#non-purchases-and-refunds)
  * [Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#reports-and-documents)
  * [Warehouses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#warehouses)
  * [Reference books](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#reference-books)


If you use the FBY model, yandex.Market takes care of all the work with orders, from storage to delivery. All you have to do is make sure that your goods in the Market warehouse do not run out, and deliver new batches. Read more about the model in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/introduction/models#fby).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#offices-and-shops)Offices and shops
**Method** |  **Method description**  
---|---  
[GET v2/​campaigns](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaigns) |  User's Store List  
[GET v2/​campaigns/​{campaignId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaign) |  Store Information  
[GET v2/​campaigns/​{campaignId}/​settings](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaignSettings) |  Store Settings  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#products)Products
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
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#balances-and-turnover)Balances and turnover
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​offers/​stocks](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/stocks/getStocks) |  Information about balances and turnover  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#prices)Prices
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​offer-prices/​updates](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/updatePrices) |  Setting prices for products in a specific store  
[POST v2/​campaigns/​{campaignId}/​offer-prices](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getPricesByOfferIds) |  View prices for specified products in a specific store  
[POST v2/​campaigns/​{campaignId}/​price-quarantine](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getCampaignQuarantineOffers) |  List of quarantined products by price in the store  
[POST v2/​campaigns/​{campaignId}/​price-quarantine/​confirm](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/confirmCampaignPrices) |  Removing an item from quarantine for the price in the store  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#orders)Orders
**Method** |  **Method description**  
---|---  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrder) |  Information about a single order  
[GET v2/​campaigns/​{campaignId}/​orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrders) |  Information about multiple orders  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​business-buyer](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/order-business-information/getOrderBusinessBuyerInfo) |  Information about the buyer — a legal entity  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/order-business-information/getOrderBusinessDocumentsInfo) |  Information about documents  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#fby-requests)FBY requests
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​supply-requests](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/supply-requests/getSupplyRequests) |  Receiving information about orders for delivery, removal and disposal  
[POST v2/​campaigns/​{campaignId}/​supply-requests/​items](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/supply-requests/getSupplyRequestItems) |  Receipt of goods in an application for delivery, export or disposal  
[POST v2/​campaigns/​{campaignId}/​supply-requests/​documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/supply-requests/getSupplyRequestDocuments) |  Receipt of documents on the application for delivery, export or disposal  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#non-purchases-and-refunds)Non-purchases and refunds
**Method** |  **Method description**  
---|---  
[GET v2/​campaigns/​{campaignId}/​returns](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturns) |  List of non-purchases and refunds  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturn) |  Information about non-purchase or refund  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​application](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturnApplication) |  Receiving a refund request  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​decision/​{itemId}/​image/​{imageHash}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturnPhoto) |  Receiving photos of items in a refund  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​decision/​submit](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/submitReturnDecision) |  Transfer and confirmation of the refund decision  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#reports-and-documents)Reports and documents
**Method** |  **Method description**  
---|---  
[POST v2/​campaigns/​{campaignId}/​stats/​orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/stats/getOrdersStats) |  Detailed information on orders  
[POST v2/​reports/​closure-documents/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateClosureDocumentsReport) |  Closing documents  
[POST v2/​reports/​goods-movement/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateGoodsMovementReport) |  Report on the movement of goods  
[POST v2/​reports/​united-returns/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateUnitedReturnsReport) |  Report on non-purchases and refunds  
[POST v2/​reports/​goods-turnover/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateGoodsTurnoverReport) |  Turnover Report  
[POST v2/​reports/​stocks-on-warehouses/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateStocksOnWarehousesReport) |  Warehouse balance report  
[POST v2/​reports/​united-marketplace-services/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateUnitedMarketplaceServicesReport) |  Report on the cost of services  
[POST v2/​reports/​closure-documents/​detalization/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateClosureDocumentsDetalizationReport) |  Report on convergence with closing documents  
[POST v2/​campaigns/​{campaignId}/​stats/​skus](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getGoodsStats) |  Product Report  
[GET v2/​reports/​info/​{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/getReportInfo) |  Getting a given report or document  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#warehouses)Warehouses
**Method** |  **Method description**  
---|---  
[GET v2/​warehouses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/warehouses/getFulfillmentWarehouses) |  Market Warehouse IDs  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby#reference-books)Reference books
**Method** |  **Method description**  
---|---  
[POST v2/​auth/​token](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/auth/getAuthTokenInfo) |  Getting information about the authorization token  
[POST v2/​regions/​countries](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/getRegionsCodes) |  List of valid country codes  
[GET v2/​regions](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionsByName) |  Search for regions by their name  
[GET v2/​regions/​{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionsById) |  Information about the region  
[GET v2/​regions/​{regionId}/​children](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionChildren) |  Information about child regions  
### Was the article helpful?
YesNo
Previous
[Common methods](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business)
Next
[FBS](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fbs)
