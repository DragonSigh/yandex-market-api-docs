---
title: View order information | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only
crawled_at: 2025-09-17T14:25:36.460400
---

Orders
# View order information
  * [Orders](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#orders)
  * [FBS Shipments](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#fbs-shipments)
  * [FBS and DBS shortcuts](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#fbs-and-dbs-shortcuts)
  * [Non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#non-purchases-and-refunds)
  * [Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#reports-and-documents)
  * [Quality index](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#quality-index)
  * [Warehouses](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#warehouses)
  * [Viewing additional information](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#common)


The name of the access in the OpenAPI specification: inventory-and-order-processing:read-only.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#orders)Orders
**Method** |  **Method description**  
---|---  
[GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrder) |  Information about a single order  
[GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrders) |  Information about multiple orders  
[POST v2/campaigns/{campaignId}/orders/{orderId}/identifiers/status](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrderIdentifiersStatus) |  LOGIN verification Statuses  
[GET v2/campaigns/{campaignId}/orders/{orderId}/buyer](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrderBuyerInfo) |  Information about the buyer — an individual  
[POST v2/campaigns/{campaignId}/orders/{orderId}/business-buyer](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/order-business-information/getOrderBusinessBuyerInfo) |  Information about the buyer — a legal entity  
[POST v2/campaigns/{campaignId}/orders/{orderId}/documents](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/order-business-information/getOrderBusinessDocumentsInfo) |  Information about documents  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#fbs-shipments)FBS Shipments
**Method** |  **Method description**  
---|---  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/getShipment) |  Getting information about a single shipment  
[PUT v2/campaigns/{campaignId}/first-mile/shipments](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/searchShipments) |  Getting information about multiple shipments  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#fbs-and-dbs-shortcuts)FBS and DBS shortcuts
**Method** |  **Method description**  
---|---  
[GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/labels/data](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrderLabelsData) |  Data for self-label production  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/orders/info](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/getShipmentOrdersInfo) |  Getting information about the ability to print labels  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#non-purchases-and-refunds)Non-purchases and refunds
**Method** |  **Method description**  
---|---  
[GET v2/campaigns/{campaignId}/returns](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getReturns) |  List of non-purchases and refunds  
[GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getReturn) |  Information about non-purchase or refund  
[GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/application](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getReturnApplication) |  Receiving a refund request  
[GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/{itemId}/image/{imageHash}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getReturnPhoto) |  Receiving photos of items in a refund  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#reports-and-documents)Reports and documents
**Method** |  **Method description**  
---|---  
[POST v2/campaigns/{campaignId}/stats/orders](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/stats/getOrdersStats) |  Detailed information on orders  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#quality-index)Quality index
**Method** |  **Method description**  
---|---  
[POST v2/businesses/{businessId}/ratings/quality](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/ratings/getQualityRatings) |  Store Quality Index  
[POST v2/campaigns/{campaignId}/ratings/quality/details](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/ratings/getQualityRatingDetails) |  Orders that affected the quality index  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#warehouses)Warehouses
**Method** |  **Method description**  
---|---  
[POST v2/businesses/{businessId}/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/warehouses/getPagedWarehouses) |  List of warehouses  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only#common)Viewing additional information
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
[Order processing and accounting of goods](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing)
Next
[Price management](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/pricing)
