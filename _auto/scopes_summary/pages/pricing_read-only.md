---
title: View prices | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/pricing_read-only
crawled_at: 2025-09-17T14:25:47.678191
---

Prices
# View prices
  * [Prices](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only#prices)
  * [Stocks](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only#stocks)
  * [Sales Boost](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only#sales-boost)
  * [Viewing additional information](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only#common)


The name of the access in the OpenAPI specification: pricing:read-only.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only#prices)Prices
**Method** |  **Method description**  
---|---  
[POST v2/tariffs/calculate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/tariffs/calculateTariffs) |  Service Cost Calculator  
[POST v2/businesses/{businessId}/offer-prices](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/prices/getDefaultPrices) |  View prices for specified products in all stores  
[POST v2/campaigns/{campaignId}/offer-prices](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/getPricesByOfferIds) |  View prices for specified products in a specific store  
[POST v2/businesses/{businessId}/offers/recommendations](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/business-assortment/getOfferRecommendations) |  Yandex.Market's recommendations regarding prices  
[POST v2/businesses/{businessId}/price-quarantine](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/business-assortment/getBusinessQuarantineOffers) |  List of quarantined products by price in the cabinet  
[POST v2/campaigns/{campaignId}/price-quarantine](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/assortment/getCampaignQuarantineOffers) |  List of quarantined products by price in the store  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only#stocks)Stocks
**Method** |  **Method description**  
---|---  
[POST v2/businesses/{businessId}/promos](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/promos/getPromos) |  Getting a list of shares  
[POST v2/businesses/{businessId}/promos/offers](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/promos/getPromoOffers) |  Getting a list of products that participate or may participate in the promotion  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only#sales-boost)Sales Boost
**Method** |  **Method description**  
---|---  
[POST v2/businesses/{businessId}/bids/info](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/bids/getBidsInfoForBusiness) |  Information about the set rates  
[POST v2/businesses/{businessId}/bids/recommendations](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/bids/getBidsRecommendations) |  Recommended bids for specified products  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing_read-only#common)Viewing additional information
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
[Price management](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing)
Next
[Product and card management](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/offers-and-cards-management)
