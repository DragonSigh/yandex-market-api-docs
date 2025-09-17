---
title: Methods common to all models | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/overview/business
crawled_at: 2025-09-17T14:24:02.092216
---

Offices and shops
# Methods common to all models
  * [Offices and shops](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#offices-and-shops)
  * [Products](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#products)
  * [Prices](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#prices)
  * [Stocks](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#stocks)
  * [Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#reports-and-documents)
  * [Product Reviews](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#product-reviews)
  * [Sales Boost](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#sales-boost)
  * [Quality index](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#quality-index)
  * [Chats](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#chats)
  * [Warehouses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#warehouses)


##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#offices-and-shops)Offices and shops
**Method** |  **Method description**  
---|---  
[POST v2/​businesses/​{businessId}/​settings](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/businesses/getBusinessSettings) |  Cabinet Settings  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#products)Products
**Method** |  **Method description**  
---|---  
[POST v2/​businesses/​{businessId}/​offer-mappings/​update](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/updateOfferMappings) |  Adding products to the catalog and changing information about them  
[POST v2/​businesses/​{businessId}/​offer-cards](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/content/getOfferCardsContentStatus) |  Getting information about the fullness of store cards  
[POST v2/​businesses/​{businessId}/​offer-cards/​update](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/content/updateOfferContent) |  Editing product category characteristics  
[POST v2/​businesses/​{businessId}/​offer-mappings](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/getOfferMappings) |  Information about the products in the catalog  
[POST v2/​businesses/​{businessId}/​offer-mappings/​delete](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/deleteOffers) |  Removing products from the catalog  
[POST v2/​businesses/​{businessId}/​offer-mappings/​archive](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/addOffersToArchive) |  Adding products to the archive  
[POST v2/​businesses/​{businessId}/​offer-mappings/​unarchive](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/deleteOffersFromArchive) |  Deleting products from the archive  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#prices)Prices
**Method** |  **Method description**  
---|---  
[POST v2/​tariffs/​calculate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/tariffs/calculateTariffs) |  Service Cost Calculator  
[POST v2/​businesses/​{businessId}/​offer-prices/​updates](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/updateBusinessPrices) |  Setting product prices for all stores  
[POST v2/​businesses/​{businessId}/​offer-prices](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/prices/getDefaultPrices) |  View prices for specified products in all stores  
[POST v2/​businesses/​{businessId}/​offers/​recommendations](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/getOfferRecommendations) |  Yandex.Market's recommendations regarding prices  
[POST v2/​businesses/​{businessId}/​price-quarantine](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/getBusinessQuarantineOffers) |  List of quarantined products by price in the cabinet  
[POST v2/​businesses/​{businessId}/​price-quarantine/​confirm](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/business-assortment/confirmBusinessPrices) |  Removing an item from quarantine based on the price in the cabinet  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#stocks)Stocks
**Method** |  **Method description**  
---|---  
[POST v2/​businesses/​{businessId}/​promos](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/promos/getPromos) |  Getting a list of shares  
[POST v2/​businesses/​{businessId}/​promos/​offers](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/promos/getPromoOffers) |  Getting a list of products that participate or may participate in the promotion  
[POST v2/​businesses/​{businessId}/​promos/​offers/​update](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/promos/updatePromoOffers) |  Adding products to a promotion or changing their prices  
[POST v2/​businesses/​{businessId}/​promos/​offers/​delete](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/promos/deletePromoOffers) |  Removing products from the promotion  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#reports-and-documents)Reports and documents
**Method** |  **Method description**  
---|---  
[POST v2/​reports/​shows-sales/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateShowsSalesReport) |  Sales Analytics Report  
[POST v2/​reports/​shows-boost/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateShowsBoostReport) |  Impression Boost Report  
[POST v2/​reports/​boost-consolidated/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateBoostConsolidatedReport) |  Sales Boost Report  
[POST v2/​reports/​sales-geography/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateSalesGeographyReport) |  Sales Geography Report  
[POST v2/​reports/​united-orders/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateUnitedOrdersReport) |  Order Report  
[POST v2/​reports/​jewelry-fiscal/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateJewelryFiscalReport) |  Jewelry Order Report  
[POST v2/​reports/​key-indicators/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateKeyIndicatorsReport) |  Report on key indicators  
[POST v2/​reports/​competitors-position/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateCompetitorsPositionReport) |  Competitive Position Report  
[POST v2/​reports/​goods-feedback/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateGoodsFeedbackReport) |  Product Reviews Report  
[POST v2/​reports/​banners-statistics/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateBannersStatisticsReport) |  Coverage Promotion Report  
[POST v2/​reports/​united-netting/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateUnitedNettingReport) |  Payment Report  
[POST v2/​reports/​shelf-statistics/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateShelfsStatisticsReport) |  Shelf Report  
[POST v2/​reports/​goods-realization/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateGoodsRealizationReport) |  Implementation Report  
[POST v2/​reports/​goods-prices/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateGoodsPricesReport) |  The Prices Report  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#product-reviews)Product Reviews
**Method** |  **Method description**  
---|---  
[POST v2/​businesses/​{businessId}/​goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/goods-feedback/getGoodsFeedbacks) |  Getting reviews of the seller's products  
[POST v2/​businesses/​{businessId}/​goods-feedback/​comments](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/goods-feedback/getGoodsFeedbackComments) |  Getting comments on a review  
[POST v2/​businesses/​{businessId}/​goods-feedback/​comments/​update](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/goods-feedback/updateGoodsFeedbackComment) |  Adding a new or changing a created comment  
[POST v2/​businesses/​{businessId}/​goods-feedback/​skip-reaction](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/goods-feedback/skipGoodsFeedbacksReaction) |  Skipping reactions to reviews  
[POST v2/​businesses/​{businessId}/​goods-feedback/​comments/​delete](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/goods-feedback/deleteGoodsFeedbackComment) |  Deleting a review comment  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#sales-boost)Sales Boost
**Method** |  **Method description**  
---|---  
[PUT v2/​businesses/​{businessId}/​bids](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/bids/putBidsForBusiness) |  Enabling a sales boost and setting bids  
[POST v2/​businesses/​{businessId}/​bids/​info](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/bids/getBidsInfoForBusiness) |  Information about the set rates  
[POST v2/​businesses/​{businessId}/​bids/​recommendations](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/bids/getBidsRecommendations) |  Recommended bids for specified products  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#quality-index)Quality index
**Method** |  **Method description**  
---|---  
[POST v2/​businesses/​{businessId}/​ratings/​quality](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/ratings/getQualityRatings) |  Store Quality Index  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#chats)Chats
**Method** |  **Method description**  
---|---  
[POST v2/​businesses/​{businessId}/​chats/​history](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/chats/getChatHistory) |  Getting the chat message history  
[GET v2/​businesses/​{businessId}/​chat](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/chats/getChat) |  Getting a chat by ID  
[POST v2/​businesses/​{businessId}/​chats](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/chats/getChats) |  Getting available chats  
[GET v2/​businesses/​{businessId}/​chats/​message](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/chats/getChatMessage) |  Receiving a chat message  
[POST v2/​businesses/​{businessId}/​chats/​new](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/chats/createChat) |  Creating a new chat with a customer  
[POST v2/​businesses/​{businessId}/​chats/​message](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/chats/sendMessageToChat) |  Sending a message to a chat  
[POST v2/​businesses/​{businessId}/​chats/​file/​send](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/chats/sendFileToChat) |  Sending a file to a chat  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#warehouses)Warehouses
**Method** |  **Method description**  
---|---  
[POST v2/​businesses/​{businessId}/​warehouses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/warehouses/getPagedWarehouses) |  List of warehouses  
### Was the article helpful?
YesNo
Previous
[Overview of methods](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/)
Next
[FBY](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby)
