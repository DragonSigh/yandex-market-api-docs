---
title: Non-purchases and refunds | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/returns
crawled_at: 2025-09-17T14:44:30.496298
---

How to deal with non-purchases and refunds
# Non-purchases and refunds
  * [How to deal with non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/returns#new-return)
  * [How to calculate the cost of such orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/returns#cost)
  * [How to get a report on non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/returns#report)


The buyer has the right to cancel the order until the order is received. He can cancel it in the office at the Market, come to the pick-up point and not pick up the goods, refuse to receive them when the courier arrives, or simply not come to the pick-up point. Such orders become **non-bribes** They are sent to the seller, and when placed using the FBY model, they are sent to the nearest Market warehouse in the region of sale, and then returned to the showcase.
The buyer can also cancel the entire purchase or part of it after delivery and receipt of the order — then registration is required. **Refund policy**.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/returns#new-return)How to deal with non-purchases and refunds
Yandex MarketYour storeYandex MarketYour storeRetrieving a list of undelivered and returned itemsOptional stepRetrieving order informationopt​Optional stepRetrieving a return applicationopt​Optional stepRetrieving photos of returned itemsopt​Optional stepFor FBY, FBS, and Express stores: creating a chatopt​Submitting and confirming the return decisionCampaign IDGET v2/campaigns/{campaignId}/returnsChecks if there areundelivered or returned items.OK: list of undelivered and returned items, if any.Campaign IDGET v2/campaigns/{campaignId}/ordersOK: order information.GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/applicationOK: return application.GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/{itemId}/image/{imageHash}OK: item photos.Account IDPOST v2/businesses/{businessId}/chats/newCreates a chatwith the user.OK: chat ID.POST v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/submitOK: operation status.
How refund statuses change
For models [FBY, FBS and Express](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fby-fbs-express-return-status-model) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/dbs-return-status-model).
  1. Check if there are any new non-purchases and refunds., — [GET campaigns/{campaignId}/returns](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getReturns).
To get refunds that require a solution, pass the parameter `statuses` with the value `PREMODERATION_DECISION_WAITING` for FBY, FBS and Express orders and `WAITING_FOR_DECISION` for DBS orders.
Use API notifications instead of this step.
Yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/reference/sendNotification) when there is a new non-purchase or refund.
Send the received message `returnId` in the method [GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getReturn) to get information about non-purchase or refund.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/)
There may be several refunds per order. This happens when the customer returns the items one at a time.
**Partial non-purchase**
When the buyer refuses a part of the goods, the order status is returned. `DELIVERED`.
To find out which items the buyer picked up, compare _list of products in the order_ and _list of non-purchased products_.
**Quick Return**
If you have enabled the option **A quick refund for a cheap marriage** , parameter `fastReturn` will return with the value `true`.
Read more about the option in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/orders/returns/decision#let-it-be).
  2. If necessary, get information about orders — request [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrders).
For products that you excluded from the order yourself, the parameter `count` will return with the value `0`.
  3. If necessary, request a return request and photos of the items in the refund using the following methods:
     * [GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/application](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getReturnApplication).
     * [GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/{itemId}/image/{imageHash}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getReturnPhoto).
  4. **For FBY, FBS, and Express stores:** You can discuss the refund details with the buyer. To do this, create a chat — [POST v2/businesses/{businessId}/chats/new](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/createChat). For more information on how to work with chats, see [Instructions](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats).
  5. Submit the refund decision and confirm it within 48 hours after creating the application. — [POST v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision/submit](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/submitReturnDecision).
**For DBS stores:** use this method instead of the outdated one. [POST v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}/decision](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/setReturnDecision).
**For FBY, FBS, and Express stores:** if the buyer does not agree with the decision, he can open a dispute. After that:
     * The refund status will change to `PREMODERATION_DISPUTE`.
     * If you use API notifications, you will receive notifications with the type `ORDER_RETURN_STATUS_UPDATED` and `CHAT_ARBITRAGE_STARTED`.
     * A chat with the referee will appear. [Getting available chats](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChats)


There were marked items in the non-purchase or return
Put such products into circulation. Read more about labeling on 
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/returns#cost)How to calculate the cost of such orders
In the request [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrders) The cost of the goods in the order is refunded, but it does not include non-purchased and returned goods.
To calculate correctly, subtract from _the cost of the order_ _refund amount_.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/returns#report)How to get a report on non-purchases and refunds
For information on how to receive reports, see [step-by-step instructions](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports).
Parameter `items` in the request [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrders).
Copied
Parameter `items` in the request [GET v2/campaigns/{campaignId}/returns](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getReturns).
Copied
Parameter `buyerItemsTotalBeforeDiscount` in the request [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrders).
Copied
Parameter `amount` in the request [GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getReturn).
Copied
Copied
### Was the article helpful?
YesNo
Previous
[FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies)
Next
[FBY, FBS, and Express Refund statuses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fby-fbs-express-return-status-model)
