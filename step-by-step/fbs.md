---
title: Processing of FBS orders | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/fbs
crawled_at: 2025-09-17T14:45:35.408902
---

Step 1. Regular checking of new orders
# Processing of FBS orders
  * [Step 1. Regular checking of new orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#new-orders)
  * [Step 2. Generating an assembly sheet](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#shipment-list)
  * [Step 3. Transfer of labeling codes and distribution of goods by boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#order-info)
    * [Marking codes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#marking-codes)
    * [Distribution by boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#boxes)
  * [Step 4. Label printing and "Ready for shipment" status transmission](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#fulfillment)
  * [Step 5. Handling the shipment](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#shipment)
  * [If the product is not enough: postponement, cancellation and reduction of the order](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#cancel-by-seller)


The Yandex.Market API allows you to perform all the same actions that are performed in the cabinet: view new orders, get labels for them, change something in them if necessary, and so on.
To understand how everything happens
Read it [an article about order processing](https://yandex.ru/support/marketplace/orders/fbs/process.html).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#new-orders)Step 1. Regular checking of new orders
Use API notifications instead of this step.
Yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/reference/sendNotification) when a new order appears.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/)
Yandex MarketYour storeYandex MarketYour storeThe store regularly requests a list of new ordersGET v2/campaigns/{campaignId}/ordersOK: list of orders.Checks availabilityof ordered items.
  1. Check regularly to see if there are any new orders. — request [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrders). Do this at least once an hour.
Use a range of delivery dates — parameters `fromDate` and `toDate`. If you don't pass it `toDate`, the current date will be indicated.
To get information about orders that have been modified
Use filters `updatedAtFrom` and `updatedAtTo`. If you don't pass it `updatedAtTo`, the current date will be indicated.
  2. Make sure that all the items are in stock. If everything is in order, proceed to step 2. If something is missing, read the instructions first. [Postponement, cancellation and reduction of the order](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#cancel-by-seller).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#shipment-list)Step 2. Generating an assembly sheet
Generation takes time, so first you need to make a request for the generation itself, and then to get the finished assembly sheet.
Yandex MarketYour storeYandex MarketYour storeReceiving the packing listOptional stepChecking generation statusopt​Retrieving the ready packing list after the estimatedGenerationTime has passedPOST v2/reports/documents/shipment-list/generatePlaces the packing listin the generation queue.OK: identifier to retrieve the ready packing list,as well as the estimated generation time(reportId + estimatedGenerationTime).GET v2/reports/info/<report_id>OK: status and estimated time remaining(status + estimatedGenerationTime).GET v2/reports/info/<report_id>OK: status and link.If generation succeeded — status = DONE + file.If generation failed — status = FAILED or status = NODATA.
  1. Make a request [POST v2/reports/documents/shipment-list/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/shipments/generateShipmentListDocumentReport).
  2. To find out if the build sheet is ready, make a request [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/getReportInfo). You will receive the generation status and the estimated time remaining until it is completed.
  3. After the generation time is over, repeat the request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/getReportInfo). If the build sheet has been generated, you will receive a link to download it.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#order-info)Step 3. Transfer of labeling codes and distribution of goods by boxes
This information is transmitted simultaneously in a single request.: [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/setOrderBoxLayout).
Yandex MarketYour storeYandex MarketYour storeTransfer of marking codes, if they are required for specific items,and distribution of items into boxesOptional stepRetrieving UIN verification statusesopt​PUT v2/campaigns/{campaignId}/orders/{orderId}/boxesOKPOST v2/campaigns/{campaignId}/orders/{orderId}/identifiers/statusOK: UIN verification information.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#marking-codes)Marking codes
Labeling of goods in the system 
If the product is marked in "_An honest sign_ " or other labeling systems, give the Market the code of each sold copy.
For example, if a person ordered three pairs of identical slippers, three codes must be provided for this item in the order.
For orders that contain jewelry
After you transfer the bitcoins, the Market will start checking them. [How to get LOGin verification statuses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrderIdentifiersStatus)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#boxes)Distribution by boxes
Before shipping the order, you need to provide the Market with information about how the goods are distributed in boxes. This information is sometimes needed if something goes wrong.
What should I do if I need to change the order information?
By request [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/setOrderBoxLayout) you can use it as many times as you want until the order status changes **Ready for shipment**. Each new request replaces the data transmitted with the previous request.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#fulfillment)Step 4. Label printing and "Ready for shipment" status transmission
Labels for a single order
Shortcuts for multiple orders
Yandex MarketYour storeYandex MarketYour storeReceiving labelsUpdating status to "Ready to ship" ("status": "PROCESSING" "substatus": "READY_TO_SHIP")GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/labelsOK: order labels.Packages orders.PUT v2/campaigns/{campaignId}/orders/{orderId}/statusorPOST v2/campaigns/{campaignId}/orders/status-updateOK
Yandex MarketYour storeYandex MarketYour storeReceiving labels for multiple ordersOptional stepChecking generation statusopt​Retrieving labels after the estimatedGenerationTime has passedUpdating status to "Ready to ship" ("status": "PROCESSING" "substatus": "READY_TO_SHIP")POST v2/reports/documents/labels/generatePlaces labelsin the generation queue.OK: identifier to retrieve the labels,and the estimated generation time (reportId + estimatedGenerationTime).GET v2/reports/info/<report_id>OK: status and estimated time remaining(status + estimatedGenerationTime).GET v2/reports/info/<report_id>OK: status and link.If generation succeeded — status = DONE + file.If generation failed — status = FAILED or status = NODATA.Packages the orders.PUT v2/campaigns/{campaignId}/orders/{orderId}/statusorPOST v2/campaigns/{campaignId}/orders/status-updateOK
The collected order must be packed. This is done according to the rules described in detail. [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/orders/fbs/packaging/index.html).
A special standard label with a number, barcodes and other information is affixed to the packaged order. Delivery services use it to determine where to take the parcel. You can get a shortcut via the API using a request:
  * [GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/labels](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/generateOrderLabels) — for one order.
  * [POST v2/reports/documents/labels/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/generateMassOrderLabelsReport) — for multiple orders.


After you have prepared the order, set it to the status **Ready for shipment** (`"status": "PROCESSING" "substatus": "READY_TO_SHIP"` ). This is done using queries. [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/updateOrderStatus) (if you want to transfer one order at a time) or [POST v2/campaigns/{campaignId}/orders/status-update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/updateOrderStatuses) (if you want to transmit it en masse).
By converting the order to the status **Ready for shipment** , you confirm to Yandex. Market that the product is there and will be shipped. Products in the status **Ready for shipment** they are included in the acceptance and transfer certificate.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#shipment)Step 5. Handling the shipment
Yandex MarketYour storeYandex MarketYour storeShipment processingOptional stepsFor shipping goods without recountingReceiving labelsopt​Receiving the acceptance certificate and confirming shipmentNumber of boxes or palletsPUT v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/palletsOKGET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/pallet/labelsOK: labels for boxes or pallets.GET v2/campaigns/{campaignId}/shipments/reception-transfer-actOK
To ship orders, the driver will need an acceptance certificate. Using a request [GET v2/campaigns/{campaignId}/shipments/reception-transfer-act](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/shipments/downloadShipmentReceptionTransferAct) You can:
  1. Receive and sign the acceptance certificate via the API. For information on how to enable work with electronic acceptance certificates, see [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/start/models/fbs#manual).
  2. Confirm the shipment. There is no such step when working in the office, but when working through the API— there is.


When can I receive the report and confirm the shipment?
Only after all orders have been converted to the status **Ready for shipment**. If there are unconfirmed orders in the shipment, an error message with a list of orders will be sent in response to the request.
Planned _confidential acceptance_
Send the number of boxes or pallets using a request [PUT v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/pallets](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/shipments/setShipmentPalletsCount).
To get shortcuts for them, use a request [GET v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/pallet/labels](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/shipments/downloadShipmentPalletLabels).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs#cancel-by-seller)If the product is not enough: postponement, cancellation and reduction of the order
During the preparation of an order, your warehouse may discover that one or more items are missing. If this happens, you will have to postpone the delivery of the order or cancel it in whole or in part.
The postponement of the delivery date and the complete cancellation of the order are made by separate requests.
To change the order composition, use [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/setOrderBoxLayout) — the same request that transmits the labeling codes and the distribution of goods in boxes.
Yandex MarketYour storeYandex MarketYour storeOptional stepsIf the warehouse doesn't have many needed items, you can cancel the orderIf the warehouse is missing certain items, you can remove them from the orderIf the item is already on its way to the warehouse, you can postpone the delivery dateopt​"status": "CANCELLED", "substatus": "SHOP_FAILED"PUT v2/campaigns/{campaignId}/orders/{orderId}/statusOKPUT v2/campaigns/{campaignId}/orders/{orderId}/boxesOKPOST v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/orders/transferOK
**Order action** | **Request**  
---|---  
Transfer to the next shipment | [POST v2/campaigns/{campaignId}/first-mile/shipments/{shipmentId}/orders/transfer](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/shipments/transferOrdersFromShipment)  
Complete cancellation of the order | Request [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/updateOrderStatus). (Transfer the order to `"status":"CANCELLED"` `"substatus": "SHOP_FAILED"`.)  
Exclusion of the product from the order | [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/setOrderBoxLayout)  
You can't do that often.
Any of these actions will lower the _quality index_ the store. When the quality index decreases, the store faces limitations.
Trust acceptance is the transfer of orders to the Market without recalculation in a common container. [To learn more](https://yandex.ru/support/marketplace/orders/fbs/process.html#by-places)
The quality index is a number from 0 to 100. If the store operates according to the FBY model, the quality index shows how well the seller makes deliveries to the Market's warehouses, and in the FBS, DBS, and Express models, the index evaluates the work with orders. [To learn more](https://yandex.ru/support/marketplace/quality/score/index.html)
Honest Sign is a state system for labeling and tracking goods. [To learn more](https://yandex.ru/support/marketplace/orders/cz.html)
Copied
### Was the article helpful?
YesNo
Previous
[Stock management](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos)
Next
[Express orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express)
