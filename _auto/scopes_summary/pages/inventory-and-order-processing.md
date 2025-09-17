---
title: Order processing and inventory | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/inventory-and-order-processing
crawled_at: 2025-09-17T14:25:29.553223
---

Orders
# Order processing and inventory
  * [Orders](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#orders)
  * [FBS Shipments](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#fbs-shipments)
  * [FBS and DBS shortcuts](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#fbs-and-dbs-shortcuts)
  * [Non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#non-purchases-and-refunds)
  * [Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#reports-and-documents)
  * [Quality index](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#quality-index)
  * [Warehouses](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#warehouses)
  * [Viewing additional information](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#common)


The name of the access in the OpenAPI specification: inventory-and-order-processing.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#orders)Orders
**Method** |  **Method description**  
---|---  
[GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrder) |  Information about a single order  
[GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrders) |  Information about multiple orders  
[PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/setOrderBoxLayout) |  Order preparation  
[POST v2/campaigns/{campaignId}/orders/{orderId}/external-id](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/updateExternalOrderId) |  Transmitting an external order ID  
[PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/updateOrderStatus) |  Changing the status of an order  
[POST v2/campaigns/{campaignId}/orders/status-update](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/updateOrderStatuses) |  Changing the statuses of multiple orders  
[PUT v2/campaigns/{campaignId}/orders/{orderId}/identifiers](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/provideOrderItemIdentifiers) |  Transfer of unit marking codes  
[POST v2/campaigns/{campaignId}/orders/{orderId}/identifiers/status](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrderIdentifiersStatus) |  LOGIN verification Statuses  
[PUT v2/campaigns/{campaignId}/orders/{orderId}/verifyEac](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/verifyOrderEac) |  Sending the confirmation code  
[PUT v2/campaigns/{campaignId}/orders/{orderId}/items](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/updateOrderItems) |  Removing items from an order or reducing their number  
[POST v2/campaigns/{campaignId}/orders/{orderId}/delivery/track](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/setOrderDeliveryTrackCode) |  Sending the parcel's track number  
[PUT v2/campaigns/{campaignId}/orders/{orderId}/delivery/date](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/setOrderDeliveryDate) |  Changing the order delivery date  
[PUT v2/campaigns/{campaignId}/orders/{orderId}/delivery/storage-limit](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/updateOrderStorageLimit) |  Order retention period extension  
[GET v2/campaigns/{campaignId}/orders/{orderId}/buyer](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrderBuyerInfo) |  Information about the buyer — an individual  
[PUT v2/campaigns/{campaignId}/orders/{orderId}/cancellation/accept](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/acceptOrderCancellation) |  Cancellation of the order by the buyer  
[POST v2/campaigns/{campaignId}/orders/{orderId}/deliverDigitalGoods](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/provideOrderDigitalCodes) |  Transfer of digital goods keys  
[POST v2/campaigns/{campaignId}/orders/{orderId}/business-buyer](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/order-business-information/getOrderBusinessBuyerInfo) |  Information about the buyer — a legal entity  
[POST v2/campaigns/{campaignId}/orders/{orderId}/documents](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/order-business-information/getOrderBusinessDocumentsInfo) |  Information about documents  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#fbs-shipments)FBS Shipments
**Method** |  **Method description**  
---|---  
[PUT v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/pallets](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/setShipmentPalletsCount) |  Transfer of the number of packages in the shipment  
[POST v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/confirm](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/confirmShipment) |  Shipment confirmation  
[GET v2/campaigns/{campaignId}/shipments/reception-transfer-act](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/downloadShipmentReceptionTransferAct) |  Confirmation of the nearest shipment and receipt of the acceptance certificate for it  
[POST v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/orders/transfer](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/transferOrdersFromShipment) |  Transferring orders to the next shipment  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/getShipment) |  Getting information about a single shipment  
[PUT v2/campaigns/{campaignId}/first-mile/shipments](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/searchShipments) |  Getting information about multiple shipments  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/act](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/downloadShipmentAct) |  Receipt of the acceptance certificate  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/discrepancy-act](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/downloadShipmentDiscrepancyAct) |  Receiving a certificate of discrepancies  
[POST v2/reports/documents/shipment-list/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/generateShipmentListDocumentReport) |  Getting the Assembly sheet  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/transportation-waybill](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/downloadShipmentTransportationWaybill) |  Receipt of the bill of lading  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/inbound-act](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/downloadShipmentInboundAct) |  Receiving the actual acceptance and transfer certificate  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#fbs-and-dbs-shortcuts)FBS and DBS shortcuts
**Method** |  **Method description**  
---|---  
[GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/shipments/{shipmentId}/boxes/{boxId}/label](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/generateOrderLabel) |  Ready‑made label-sticker for the box in the order  
[GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/labels](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/generateOrderLabels) |  Ready‑made labels-stickers for all boxes in one order  
[POST v2/reports/documents/labels/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/generateMassOrderLabelsReport) |  Ready‑made labels-stickers for all boxes in several orders  
[GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/labels/data](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getOrderLabelsData) |  Data for self-label production  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/pallet/labels](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/downloadShipmentPalletLabels) |  Labels for trust acceptance  
[GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/orders/info](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/shipments/getShipmentOrdersInfo) |  Getting information about the ability to print labels  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#non-purchases-and-refunds)Non-purchases and refunds
**Method** |  **Method description**  
---|---  
[GET v2/campaigns/{campaignId}/returns](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getReturns) |  List of non-purchases and refunds  
[GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getReturn) |  Information about non-purchase or refund  
[GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/application](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getReturnApplication) |  Receiving a refund request  
[GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/{itemId}/image/{imageHash}](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/getReturnPhoto) |  Receiving photos of items in a refund  
[POST v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/submit](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/orders/submitReturnDecision) |  Transfer and confirmation of the refund decision  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#reports-and-documents)Reports and documents
**Method** |  **Method description**  
---|---  
[POST v2/campaigns/{campaignId}/stats/orders](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/stats/getOrdersStats) |  Detailed information on orders  
[POST v2/reports/goods-movement/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateGoodsMovementReport) |  Report on the movement of goods  
[POST v2/reports/united-orders/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateUnitedOrdersReport) |  Order Report  
[POST v2/reports/jewelry-fiscal/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateJewelryFiscalReport) |  Jewelry Order Report  
[POST v2/reports/united-returns/generate](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/reports/generateUnitedReturnsReport) |  Report on non-purchases and refunds  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#quality-index)Quality index
**Method** |  **Method description**  
---|---  
[POST v2/businesses/{businessId}/ratings/quality](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/ratings/getQualityRatings) |  Store Quality Index  
[POST v2/campaigns/{campaignId}/ratings/quality/details](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/ratings/getQualityRatingDetails) |  Orders that affected the quality index  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#warehouses)Warehouses
**Method** |  **Method description**  
---|---  
[POST v2/businesses/{businessId}/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/warehouses/getPagedWarehouses) |  List of warehouses  
[POST v2/campaigns/{campaignId}/warehouse/status](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/reference/warehouses/updateWarehouseStatus) |  Changing the warehouse status  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing#common)Viewing additional information
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
[Access to methods by Api Key](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/concepts/access)
Next
[Viewing information about orders](https://yandex.ru/dev/market/partner-api/doc/en/_auto/scopes_summary/pages/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
