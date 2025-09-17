---
title: Product promotion | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/promotion
crawled_at: 2025-09-17T14:26:03.617160
---

Stocks
# Product promotion
  * [Stocks](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion#stocks)
  * [Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion#reports-and-documents)
  * [Sales Boost](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion#sales-boost)
  * [Viewing additional information](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion#common)


The name of the access in the OpenAPI specification: promotion.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion#stocks)Stocks
**Method** |  **Method description**  
---|---  
[POST v2/businesses/{businessId}/promos](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/promos/getPromos) |  Getting a list of shares  
[POST v2/businesses/{businessId}/promos/offers](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/promos/getPromoOffers) |  Getting a list of products that participate or may participate in the promotion  
[POST v2/businesses/{businessId}/promos/offers/update](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/promos/updatePromoOffers) |  Adding products to a promotion or changing their prices  
[POST v2/businesses/{businessId}/promos/offers/delete](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/promos/deletePromoOffers) |  Removing products from the promotion  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion#reports-and-documents)Reports and documents
**Method** |  **Method description**  
---|---  
[POST v2/reports/shows-boost/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateShowsBoostReport) |  Impression Boost Report  
[POST v2/reports/boost-consolidated/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateBoostConsolidatedReport) |  Sales Boost Report  
[POST v2/reports/united-orders/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateUnitedOrdersReport) |  Order Report  
[POST v2/reports/key-indicators/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateKeyIndicatorsReport) |  Report on key indicators  
[POST v2/reports/competitors-position/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateCompetitorsPositionReport) |  Competitive Position Report  
[POST v2/reports/banners-statistics/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateBannersStatisticsReport) |  Coverage Promotion Report  
[POST v2/reports/shelf-statistics/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateShelfsStatisticsReport) |  Shelf Report  
[POST v2/reports/goods-prices/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateGoodsPricesReport) |  The Prices Report  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion#sales-boost)Sales Boost
**Method** |  **Method description**  
---|---  
[PUT v2/businesses/{businessId}/bids](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/bids/putBidsForBusiness) |  Enabling a sales boost and setting bids  
[POST v2/businesses/{businessId}/bids/info](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/bids/getBidsInfoForBusiness) |  Information about the set rates  
[POST v2/businesses/{businessId}/bids/recommendations](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/bids/getBidsRecommendations) |  Recommended bids for specified products  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion#common)Viewing additional information
**Method** |  **Method description**  
---|---  
[GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/campaigns/getCampaigns) |  User's Store List  
[GET v2/campaigns/{campaignId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/campaigns/getCampaign) |  Store Information  
[POST v2/businesses/{businessId}/settings](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/businesses/getBusinessSettings) |  Cabinet Settings  
[GET v2/campaigns/{campaignId}/settings](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/campaigns/getCampaignSettings) |  Store Settings  
[POST v2/categories/tree](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/categories/getCategoriesTree) |  The category tree  
[GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/getReportInfo) |  Getting a given report or document  
[GET v2/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/warehouses/getFulfillmentWarehouses) |  Market Warehouse IDs  
[POST v2/auth/token](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/auth/getAuthTokenInfo) |  Getting information about the authorization token  
[GET v2/delivery/services](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getDeliveryServices) |  Directory of delivery services  
[POST v2/regions/countries](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/regions/getRegionsCodes) |  List of valid country codes  
[GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/regions/searchRegionsByName) |  Search for regions by their name  
[GET v2/regions/{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/regions/searchRegionsById) |  Information about the region  
[GET v2/regions/{regionId}/children](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/regions/searchRegionChildren) |  Information about child regions  
### Was the article helpful?
YesNo
Previous
[Viewing products and cards](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
Next
[Viewing information about product promotions](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/promotion_read-only)
