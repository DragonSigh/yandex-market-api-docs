---
title: Express order processing | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/express
crawled_at: 2025-09-17T14:45:41.162488
---

Step 1. Getting information about orders
# Express order processing
  * [Step 1. Getting information about orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#new-orders)
    * [Notifications are enabled](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#with-notifications)
    * [Notifications are not enabled](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#without-notifications)
  * [Step 2. Transmission of marking codes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#marking-codes)
  * [Step 3. Label printing and "Ready for shipment" status transmission](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#label)
  * [Step 4. Sending the confirmation code and the order to the courier](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#verifyOrderEac)
  * [If the product is not enough: cancel and shorten the order](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#cancel-by-seller)


The Yandex.Market API allows you to perform all the same actions that are performed in the cabinet: view new orders, get labels for them, change something in them if necessary, and so on.
To understand how everything happens
Read it [an article about order fulfillment](https://yandex.ru/support/marketplace/ru/orders/express/process).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#new-orders)Step 1. Getting information about orders
Set up notifications, as you need to know about new orders instantly. [Instruction manual](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/)
About notifications in the app **Yandex Market for sellers** , by mail or Telegram , read in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/express/notifications).
###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#with-notifications)Notifications are enabled
Yandex MarketYour storeYandex MarketYour storeReceiving a new order notificationRetrieving new order informationPOST notificationGET v2/campaigns/{campaignId}/orders/{orderId}OK: order information.Checks availabilityof ordered items.
  1. Get detailed information about the order by making a request [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrder).
  2. Make sure that all the items are in stock. If everything is in order, proceed to step 2. If something is missing, read the instructions first. [Cancellation and reduction of the order](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#cancel-by-seller).


###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#without-notifications)Notifications are not enabled
Yandex MarketYour storeYandex MarketYour storeReceiving a list of new ordersGET v2/campaigns/{campaignId}/ordersOK: list of orders.Checks availabilityof ordered items.
  1. Check regularly to see if there are any new orders. — request [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrders). Do this at least once every 5-10 minutes.
Use a range of delivery dates — parameters `fromDate` and `toDate`. If you don't pass it `toDate`, the current date will be indicated.
To get information about orders that have been modified
Use filters `updatedAtFrom` and `updatedAtTo`. If you don't pass it `updatedAtTo`, the current date will be indicated.
  2. Make sure that all the items are in stock. If everything is in order, proceed to step 2. If something is missing, read the instructions first. [Cancellation and reduction of the order](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#cancel-by-seller).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#marking-codes)Step 2. Transmission of marking codes
Labeling of goods in the system 
Yandex MarketYour storeYandex MarketYour storeTransfer of marking codes, if applicableOptional stepRetrieving UIN verification statusesopt​PUT v2/campaigns/{campaignId}/orders/{orderId}/boxesOKPOST v2/campaigns/{campaignId}/orders/{orderId}/identifiers/statusOK: UIN verification information.
If the product is marked in "_An honest sign_ " or other labeling systems, give the Market the code of each sold copy.
This information is transmitted by request [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/setOrderBoxLayout).
For orders that contain jewelry
After you transfer the bitcoins, the Market will start checking them. [How to get LOGin verification statuses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrderIdentifiersStatus)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#label)Step 3. Label printing and "Ready for shipment" status transmission
Yandex MarketYour storeYandex MarketYour storeReceiving labelsUpdating status to "Ready to ship" ("status": "PROCESSING" "substatus": "READY_TO_SHIP")GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/labelsOK: labels.Attaches labelsto the order.PUT v2/campaigns/{campaignId}/orders/{orderId}/statusOK
  1. Pack the assembled order according to the rules described in detail in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/express/packaging/rules).
  2. Get shortcuts using a request [GET v2/campaigns/{campaignId}/orders/{orderId}/delivery/labels](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/generateOrderLabels) and stick them on the packaged order.
  3. Set the order to the status **Ready for shipment** (`"status": "PROCESSING" "substatus": "READY_TO_SHIP"`) — request [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/updateOrderStatus).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#verifyOrderEac)Step 4. Sending the confirmation code and the order to the courier
Yandex MarketYour storeYandex MarketYour storeConfirmation code transferReceives code from courier.PUT v2/campaigns/{campaignId}/orders/{orderId}/verifyEacOKHands over the order to the courier.
  1. Send the confirmation code that the courier gave you in the request. [PUT v2/campaigns/{campaignId}/orders/{orderId}/verifyEac](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/verifyOrderEac).
  2. If the code verification is successful, send the order to the courier.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/express#cancel-by-seller)If the product is not enough: cancel and shorten the order
If, during the preparation of an order, you find that one or more items are missing, cancel it in whole or in part. This is done by separate requests.
Yandex MarketYour storeYandex MarketYour storeOptional stepsIf the warehouse is missing many required items, you can cancel the orderIf the warehouse is missing individual items, you can remove them from the orderopt​"status": "CANCELLED", "substatus": "SHOP_FAILED"PUT v2/campaigns/{campaignId}/orders/{orderId}/statusOKPUT v2/campaigns/{campaignId}/orders/{orderId}/boxesOK
**Order action** |  **Request**  
---|---  
Complete cancellation of the order |  [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/updateOrderStatus). Transfer the order to `"status":"CANCELLED"` `"substatus": "SHOP_FAILED"`.  
Exclusion of the product from the order |  [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/setOrderBoxLayout)  
You can't do that often.
Any of these actions will lower the _quality index_ the store. When the quality index decreases, the store faces limitations.
The quality index is a number from 0 to 100. If the store operates according to the FBY model, the quality index shows how well the seller makes deliveries to the Market's warehouses, and in the FBS, DBS, and Express models, the index evaluates the work with orders. [To learn more](https://yandex.ru/support/marketplace/quality/score/index.html)
Honest Sign is a state system for labeling and tracking goods. [To learn more](https://yandex.ru/support/marketplace/orders/cz.html)
Copied
### Was the article helpful?
YesNo
Previous
[FBS orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs)
Next
[Order statuses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/concepts/dbs-order-status-model)
