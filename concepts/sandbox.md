---
title: Test orders | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/sandbox
crawled_at: 2025-09-17T14:42:54.076679
---

Test orders
# Test orders
  * [Limitations](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#limitations)
  * [How to debug](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#how-to)
    * [1. Create a new order](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#new-order)
    * [2. Send the order](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#accept)
    * [3. Process the order](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#process)
    * [4. Cancel the order](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#cancel)


On Yandex. Market, you can test the store and its API on test orders before you start working with real ones. You can emulate the following processes:
  * making an order on behalf of the buyer — add items to the cart, choose payment methods and delivery terms;
  * cancellation of the order.


Yandex. Market does not charge for such orders. And errors in working with them do not affect the checks and are not used in calculating the quality index.
To go to the debugging interface, click on the name of your business in the lower-left corner of the cabinet and select **Debugging** → **Test orders**. From the same page, you can access the debugging information by clicking on the link **API log for test orders**.
All orders created in the debugging interface are sent to the store with the value `true` the parameter `fake`, which allows the store to distinguish such orders from the real ones.
Data on test orders
If you have API notifications enabled, yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/reference/sendNotification) with information about _events_ also for test orders. [How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/push-notifications/)
However, methods that return information on orders do not include data on test orders by default. To get them, pass the value `true` in the parameter `fake`.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#limitations)Limitations
Information about test orders and request logs are stored for 10 days.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#how-to)How to debug
###  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#new-order)1. Create a new order
On the page **Debugging** → **Test orders** :
  1. Choose **Create in your personal account**.
  2. Add products to the shopping cart by clicking ![](https://yandex.ru/dev/market/partner-api/doc/en/concepts/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/sandbox-button.png) close to the right ones.
  3. In the block **Basket** click **Check availability**.


![](https://yandex.ru/dev/market/partner-api/doc/en/concepts/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/concepts/sandbox-order.png)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#accept)2. Send the order
In the third block:
  1. Specify the shipping and payment method. Since this is a test order, select payment upon receipt.
The store has just been created
Configured delivery services may not be available. In this case, select the test service.
  2. Enter the buyer's test data (address, first and last name, phone number, etc.).
  3. Click **Send an order**.


After that, a notification about the creation of a new order and its number will appear on the page.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#process)3. Process the order
Check the log after each request.
If the integration is not configured correctly, you will see errors in the log that need to be fixed. To view the log, click on the name of your business in the lower-left corner of your account and open the page **Query log**.
  1. Send a request [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrder) and save the parcel ID (`id` in `shipments`) from the response.
  2. Send a request [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/setOrderBoxLayout), where to transmit:
     * the received ID.
     * information about the distribution of goods from the order by boxes;
     * if there are products that are subject to labeling, then the labeling codes for these products.
  3. Confirm that you are ready for shipment by sending the status `PROCESSING` with a sub-status `READY_TO_SHIP` using a request [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/updateOrderStatus).
  4. If in the future you will ship orders to a sorting center or a pick-up point or transfer them to Market couriers from your warehouse, send a request [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/updateOrderStatus). Send the status in it `PROCESSING` with a sub-status `SHIPPED`.


###  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/sandbox#cancel)4. Cancel the order
Send a request [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/updateOrderStatus) and send the status `CANCELLED` with the reason for cancellation `SHOP_FAILED`. A test order can only be cancelled before it is upgraded to the status `PROCESSING` with a sub-status:
  * `SHIPPED` if in the future you will ship orders to a sorting center or a pick-up point or transfer them to Market couriers from your warehouse;
  * `READY_TO_SHIP` if your store is connected to express delivery and you will ship orders to couriers 


Check for errors. In the cabinet in the lower left corner, click on the name of your business and open the page **Query log** — and fix them.
Events for which Yandex.Market sends notifications:
  * creating a new order;
  * changing the order;
  * changing the order status;
  * creating a new chat with a customer;
  * adding a new chat message;
  * the beginning of the dispute;
  * ending the dispute;
  * creating a new product review;
  * creating a new review comment;
  * creating an order cancellation request;
  * order cancellation;
  * creating a new non-purchase or refund;
  * changing the non-purchase or refund status.


Copied
### Was the article helpful?
YesNo
Previous
[Query log](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/debug)
Next
[How to use the console](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/console)
