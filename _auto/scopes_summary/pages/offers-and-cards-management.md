---
title: Manage products and cards | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/offers-and-cards-management
crawled_at: 2025-09-17T14:25:53.731466
---

Products
# Manage products and cards
  * [Products](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management#products)
  * [Balances and turnover](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management#balances-and-turnover)
  * [Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management#reports-and-documents)
  * [Viewing additional information](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management#common)


The name of the access in the OpenAPI specification: offers-and-cards-management.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management#products)Products
**Method** |  **Method description**  
---|---  
[POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/content/getCategoryContentParameters) |  Lists of product characteristics by category  
[POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/business-assortment/updateOfferMappings) |  Adding products to the catalog and changing information about them  
[POST v2/campaigns/{campaignId}/offers/update](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/updateCampaignOffers) |  Changing the terms of sale of goods in the store  
[POST v2/businesses/{businessId}/offer-cards](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/content/getOfferCardsContentStatus) |  Getting information about the fullness of store cards  
[POST v2/businesses/{businessId}/offer-cards/update](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/content/updateOfferContent) |  Editing product category characteristics  
[POST v2/businesses/{businessId}/offer-mappings](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/business-assortment/getOfferMappings) |  Information about the products in the catalog  
[POST v2/campaigns/{campaignId}/offers](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/getCampaignOffers) |  Information about the products that are placed in the specified store  
[POST v2/businesses/{businessId}/offer-mappings/delete](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/business-assortment/deleteOffers) |  Removing products from the catalog  
[POST v2/campaigns/{campaignId}/offers/delete](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/deleteCampaignOffers) |  Removing items from the store's assortment  
[GET v2/campaigns/{campaignId}/hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/getHiddenOffers) |  Information about the goods you have hidden  
[POST v2/campaigns/{campaignId}/hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/addHiddenOffers) |  Hiding products and hiding settings  
[POST v2/campaigns/{campaignId}/hidden-offers/delete](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/deleteHiddenOffers) |  Resuming product display  
[POST v2/businesses/{businessId}/offer-mappings/archive](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/business-assortment/addOffersToArchive) |  Adding products to the archive  
[POST v2/businesses/{businessId}/offer-mappings/unarchive](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/business-assortment/deleteOffersFromArchive) |  Deleting products from the archive  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management#balances-and-turnover)Balances and turnover
**Method** |  **Method description**  
---|---  
[POST v2/campaigns/{campaignId}/offers/stocks](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/stocks/getStocks) |  Information about balances and turnover  
[PUT v2/campaigns/{campaignId}/offers/stocks](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/stocks/updateStocks) |  Transmitting information about balances  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management#reports-and-documents)Reports and documents
**Method** |  **Method description**  
---|---  
[POST v2/reports/goods-movement/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateGoodsMovementReport) |  Report on the movement of goods  
[POST v2/reports/goods-turnover/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateGoodsTurnoverReport) |  Turnover Report  
[POST v2/reports/stocks-on-warehouses/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateStocksOnWarehousesReport) |  Warehouse balance report  
[POST v2/campaigns/{campaignId}/stats/skus](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/getGoodsStats) |  Product Report  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management#common)Viewing additional information
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
[Viewing prices](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only)
Next
[Viewing products and cards](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
