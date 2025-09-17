---
title: Comparison of methods by models | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/overview/comparison
crawled_at: 2025-09-17T14:23:50.373298
---

Offices and shops
# Comparison of methods by models
  * [Offices and shops](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#offices-and-shops)
  * [Products](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#products)
  * [Balances and turnover](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#balances-and-turnover)
  * [Prices](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#prices)
  * [Orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#orders)
  * [FBS Shipments](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#fbs-shipments)
  * [FBS and DBS shortcuts](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#fbs-and-dbs-shortcuts)
  * [FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#fby-requests)
  * [DBS-delivery](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#dbs-delivery)
  * [Non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#non-purchases-and-refunds)
  * [Reports and documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#reports-and-documents)
  * [Quality index](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#quality-index)
  * [Warehouses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#warehouses)
  * [Reference books](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#reference-books)


##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#offices-and-shops)Offices and shops
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[GET v2/​campaigns](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaigns) |  User's Store List |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaign) |  Store Information |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​settings](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaignSettings) |  Store Settings |  ✔️ |  ✔️ |  ✔️ |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#products)Products
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[POST v2/​categories/​tree](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/categories/getCategoriesTree) |  The category tree |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​category/​{categoryId}/​parameters](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/content/getCategoryContentParameters) |  Lists of product characteristics by category |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​offers/​update](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/updateCampaignOffers) |  Changing the terms of sale of goods in the store |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​offers](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getCampaignOffers) |  Information about the products that are placed in the specified store |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​offers/​delete](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/deleteCampaignOffers) |  Removing items from the store's assortment |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getHiddenOffers) |  Information about the goods you have hidden |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/addHiddenOffers) |  Hiding products and hiding settings |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​hidden-offers/​delete](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/deleteHiddenOffers) |  Resuming product display |  ✔️ |  ✔️ |  ✔️ |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#balances-and-turnover)Balances and turnover
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[POST v2/​campaigns/​{campaignId}/​offers/​stocks](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/stocks/getStocks) |  Information about balances and turnover |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[PUT v2/​campaigns/​{campaignId}/​offers/​stocks](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/stocks/updateStocks) |  Transmitting information about balances |  |  ✔️ |  ✔️ |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#prices)Prices
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[POST v2/​campaigns/​{campaignId}/​offer-prices/​updates](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/updatePrices) |  Setting prices for products in a specific store |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​offer-prices](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getPricesByOfferIds) |  View prices for specified products in a specific store |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​price-quarantine](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getCampaignQuarantineOffers) |  List of quarantined products by price in the store |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​price-quarantine/​confirm](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/confirmCampaignPrices) |  Removing an item from quarantine for the price in the store |  ✔️ |  ✔️ |  ✔️ |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#orders)Orders
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrder) |  Information about a single order |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrders) |  Information about multiple orders |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​boxes](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/setOrderBoxLayout) |  Order preparation |  |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​external-id](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/updateExternalOrderId) |  Transmitting an external order ID |  |  ✔️ |  ✔️ |  ✔️  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​status](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/updateOrderStatus) |  Changing the status of an order |  |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​orders/​status-update](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/updateOrderStatuses) |  Changing the statuses of multiple orders |  |  ✔️ |  ✔️ |  ✔️  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​identifiers](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/provideOrderItemIdentifiers) |  Transfer of unit marking codes |  |  |  |  ✔️  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​identifiers/​status](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrderIdentifiersStatus) |  LOGIN verification Statuses |  |  ✔️ |  ✔️ |   
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​verifyEac](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/verifyOrderEac) |  Sending the confirmation code |  |  |  ✔️ |   
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​items](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/updateOrderItems) |  Removing items from an order or reducing their number |  |  |  |  ✔️  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​track](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/setOrderDeliveryTrackCode) |  Sending the parcel's track number |  |  |  |  ✔️  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​date](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/setOrderDeliveryDate) |  Changing the order delivery date |  |  |  |  ✔️  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​storage-limit](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/updateOrderStorageLimit) |  Order retention period extension |  |  |  |  ✔️  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​buyer](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrderBuyerInfo) |  Information about the buyer — an individual |  |  |  |  ✔️  
[PUT v2/​campaigns/​{campaignId}/​orders/​{orderId}/​cancellation/​accept](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/acceptOrderCancellation) |  Cancellation of the order by the buyer |  |  |  |  ✔️  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​deliverDigitalGoods](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/provideOrderDigitalCodes) |  Transfer of digital goods keys |  |  |  |  ✔️  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​business-buyer](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/order-business-information/getOrderBusinessBuyerInfo) |  Information about the buyer — a legal entity |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/order-business-information/getOrderBusinessDocumentsInfo) |  Information about documents |  ✔️ |  ✔️ |  ✔️ |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#fbs-shipments)FBS Shipments
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[PUT v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​pallets](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/setShipmentPalletsCount) |  Transfer of the number of packages in the shipment |  |  ✔️ |  |   
[POST v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​confirm](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/confirmShipment) |  Shipment confirmation |  |  ✔️ |  |   
[GET v2/​campaigns/​{campaignId}/​shipments/​reception-transfer-act](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/downloadShipmentReceptionTransferAct) |  Confirmation of the nearest shipment and receipt of the acceptance certificate for it |  |  ✔️ |  |   
[POST v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​orders/​transfer](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/transferOrdersFromShipment) |  Transferring orders to the next shipment |  |  ✔️ |  |   
[GET v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/getShipment) |  Getting information about a single shipment |  |  ✔️ |  |   
[PUT v2/​campaigns/​{campaignId}/​first-mile/​shipments](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/searchShipments) |  Getting information about multiple shipments |  |  ✔️ |  |   
[GET v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​act](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/downloadShipmentAct) |  Receipt of the acceptance certificate |  |  ✔️ |  |   
[GET v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​discrepancy-act](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/downloadShipmentDiscrepancyAct) |  Receiving a certificate of discrepancies |  |  ✔️ |  |   
[POST v2/​reports/​documents/​shipment-list/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/generateShipmentListDocumentReport) |  Getting the Assembly sheet |  |  ✔️ |  |   
[GET v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​transportation-waybill](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/downloadShipmentTransportationWaybill) |  Receipt of the bill of lading |  |  ✔️ |  |   
[GET v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​inbound-act](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/downloadShipmentInboundAct) |  Receiving the actual acceptance and transfer certificate |  |  ✔️ |  |   
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#fbs-and-dbs-shortcuts)FBS and DBS shortcuts
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​shipments/​{shipmentId}/​boxes/​{boxId}/​label](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/generateOrderLabel) |  Ready‑made label-sticker for the box in the order |  |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​labels](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/generateOrderLabels) |  Ready‑made labels-stickers for all boxes in one order |  |  ✔️ |  ✔️ |  ✔️  
[POST v2/​reports/​documents/​labels/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/generateMassOrderLabelsReport) |  Ready‑made labels-stickers for all boxes in several orders |  |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​delivery/​labels/​data](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getOrderLabelsData) |  Data for self-label production |  |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​pallet/​labels](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/downloadShipmentPalletLabels) |  Labels for trust acceptance |  |  ✔️ |  |   
[GET v2/​campaigns/​{campaignId}/​first-mile/​shipments/​{shipmentId}/​orders/​info](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/shipments/getShipmentOrdersInfo) |  Getting information about the ability to print labels |  |  ✔️ |  |   
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#fby-requests)FBY requests
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[POST v2/​campaigns/​{campaignId}/​supply-requests](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/supply-requests/getSupplyRequests) |  Receiving information about orders for delivery, removal and disposal |  ✔️ |  |  |   
[POST v2/​campaigns/​{campaignId}/​supply-requests/​items](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/supply-requests/getSupplyRequestItems) |  Receipt of goods in an application for delivery, export or disposal |  ✔️ |  |  |   
[POST v2/​campaigns/​{campaignId}/​supply-requests/​documents](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/supply-requests/getSupplyRequestDocuments) |  Receipt of documents on the application for delivery, export or disposal |  ✔️ |  |  |   
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#dbs-delivery)DBS-delivery
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[GET v2/​campaigns/​{campaignId}/​outlets/​{outletId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/outlets/getOutlet) |  Information about a single point of sale |  |  |  |  ✔️  
[GET v2/​campaigns/​{campaignId}/​outlets](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/outlets/getOutlets) |  Information about multiple points of sale |  |  |  |  ✔️  
[POST v2/​campaigns/​{campaignId}/​outlets](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/outlets/createOutlet) |  Creating a point of sale |  |  |  |  ✔️  
[PUT v2/​campaigns/​{campaignId}/​outlets/​{outletId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/outlets/updateOutlet) |  Changing information about the point of sale |  |  |  |  ✔️  
[DELETE v2/​campaigns/​{campaignId}/​outlets/​{outletId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/outlets/deleteOutlet) |  Deleting a point of sale |  |  |  |  ✔️  
[GET v2/​campaigns/​{campaignId}/​outlets/​licenses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/outlets/getOutletLicenses) |  Information about licenses for points of sale |  |  |  |  ✔️  
[POST v2/​campaigns/​{campaignId}/​outlets/​licenses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/outlets/updateOutletLicenses) |  Creating and changing licenses for points of sale |  |  |  |  ✔️  
[DELETE v2/​campaigns/​{campaignId}/​outlets/​licenses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/outlets/deleteOutletLicenses) |  Removing licenses for points of sale |  |  |  |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#non-purchases-and-refunds)Non-purchases and refunds
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[GET v2/​campaigns/​{campaignId}/​returns](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturns) |  List of non-purchases and refunds |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturn) |  Information about non-purchase or refund |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​application](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturnApplication) |  Receiving a refund request |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​decision/​{itemId}/​image/​{imageHash}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getReturnPhoto) |  Receiving photos of items in a refund |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​orders/​{orderId}/​returns/​{returnId}/​decision/​submit](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/submitReturnDecision) |  Transfer and confirmation of the refund decision |  ✔️ |  ✔️ |  ✔️ |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#reports-and-documents)Reports and documents
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[POST v2/​campaigns/​{campaignId}/​stats/​orders](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/stats/getOrdersStats) |  Detailed information on orders |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​reports/​closure-documents/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateClosureDocumentsReport) |  Closing documents |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​reports/​goods-movement/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateGoodsMovementReport) |  Report on the movement of goods |  ✔️ |  |  |   
[POST v2/​reports/​united-returns/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateUnitedReturnsReport) |  Report on non-purchases and refunds |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​reports/​goods-turnover/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateGoodsTurnoverReport) |  Turnover Report |  ✔️ |  |  |   
[POST v2/​reports/​stocks-on-warehouses/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateStocksOnWarehousesReport) |  Warehouse balance report |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​reports/​united-marketplace-services/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateUnitedMarketplaceServicesReport) |  Report on the cost of services |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​reports/​closure-documents/​detalization/​generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateClosureDocumentsDetalizationReport) |  Report on convergence with closing documents |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[POST v2/​campaigns/​{campaignId}/​stats/​skus](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/assortment/getGoodsStats) |  Product Report |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​reports/​info/​{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/getReportInfo) |  Getting a given report or document |  ✔️ |  ✔️ |  ✔️ |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#quality-index)Quality index
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[POST v2/​campaigns/​{campaignId}/​ratings/​quality/​details](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/ratings/getQualityRatingDetails) |  Orders that affected the quality index |  |  ✔️ |  ✔️ |  ✔️  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#warehouses)Warehouses
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[POST v2/​campaigns/​{campaignId}/​warehouse/​status](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/warehouses/updateWarehouseStatus) |  Changing the warehouse status |  |  ✔️ |  ✔️ |  ✔️  
[GET v2/​warehouses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/warehouses/getFulfillmentWarehouses) |  Market Warehouse IDs |  ✔️ |  |  |   
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison#reference-books)Reference books
**Method** |  **Method description** |  **FBY** |  **FBS** |  **Express** |  **DBS**  
---|---|---|---|---|---  
[POST v2/​auth/​token](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/auth/getAuthTokenInfo) |  Getting information about the authorization token |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​delivery/​services](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/orders/getDeliveryServices) |  Directory of delivery services |  |  ✔️ |  ✔️ |  ✔️  
[POST v2/​regions/​countries](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/getRegionsCodes) |  List of valid country codes |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​regions](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionsByName) |  Search for regions by their name |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​regions/​{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionsById) |  Information about the region |  ✔️ |  ✔️ |  ✔️ |  ✔️  
[GET v2/​regions/​{regionId}/​children](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/regions/searchRegionChildren) |  Information about child regions |  ✔️ |  ✔️ |  ✔️ |  ✔️  
### Was the article helpful?
YesNo
Previous
[DBS](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/dbs)
Next
[Feedback](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/feedback)
