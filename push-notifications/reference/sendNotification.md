---
title: Receiving notifications - API notifications | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/sendNotification
crawled_at: 2025-09-17T14:24:58.640018
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#body)
    * [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype)
    * [PingNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#pingnotificationdto)
    * [OrderCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercreatednotificationdto)
    * [OrderStatusUpdatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderstatusupdatednotificationdto)
    * [OrderCancelledNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercancellednotificationdto)
    * [OrderCancellationRequestNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercancellationrequestnotificationdto)
    * [OrderReturnCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderreturncreatednotificationdto)
    * [OrderReturnStatusUpdatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderreturnstatusupdatednotificationdto)
    * [OrderUpdatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderupdatednotificationdto)
    * [GoodsFeedbackCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#goodsfeedbackcreatednotificationdto)
    * [GoodsFeedbackCommentCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#goodsfeedbackcommentcreatednotificationdto)
    * [ChatCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatcreatednotificationdto)
    * [ChatMessageSentNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatmessagesentnotificationdto)
    * [ChatArbitrageStartedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatarbitragestartednotificationdto)
    * [ChatArbitrageFinishedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatarbitragefinishednotificationdto)
    * [NotificationOrderItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationorderitemdto)
    * [OrderStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderstatustype)
    * [OrderSubstatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordersubstatustype)
    * [NotificationReturnItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationreturnitemdto)
    * [ReturnType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#returntype)
    * [NotificationUpdatedReturnStatusesDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationupdatedreturnstatusesdto)
    * [OrderUpdateType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderupdatetype)
    * [RefundStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#refundstatustype)
    * [ReturnShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#returnshipmentstatustype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#body1)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#body2)
    * [NotificationApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationapierrordto)
    * [NotificationApiErrorType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationapierrortype)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#body3)


# Receiving notifications
The market sends notifications about events to the store:
  * creating a new order;
  * order modification;
  * order status change;
  * create a new chat with the customer;
  * adding a new message in the chat;
  * the beginning of a dispute;
  * the end of the dispute;
  * creating a new product review;
  * creating a new review comment;
  * creating an order cancellation request;
  * cancellation of the order;
  * creating a new non-purchase or refund;
  * changing the non-purchase or refund status.


Keep these features in mind when working with notifications.
  * Yandex.Market can send multiple notifications for the same event.
In some cases, this is normal behavior. For example, there may be several notifications with a change in the order status due to the search for a courier.
  * The time in the notification, in the response to a request to the Market, and in your system may vary.
This is due to the fact that at the time the notification is sent, the order status may already be different.
In the request `POST notification` the time of the event comes in `createdAt`, `updatedAt` or `cancelledAt`. The choice of the parameter depends on the type of notification.


Consider the later time of the event to be relevant. It can be in a notification, returned in response to a request to the Market, or stored in your system.
Timeout for receiving a response: 10 seconds.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#request)Request
POST
```
/notification

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#body)Body
application/json
```
{
    "notificationType": "PING",
    "time": "2022-12-29T18:02:01Z"
}

```

**Name** |  **Description**  
---|---  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
...rest |  **oneOf** [PingNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#pingnotificationdto) Verification notification. `notificationType` = `PING`  
...rest |  **oneOf** [OrderCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercreatednotificationdto) Notification of the creation of a new order. `notificationType` = `ORDER_CREATED` To get detailed information about the order Use the method [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/getOrder).  
...rest |  **oneOf** [OrderStatusUpdatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderstatusupdatednotificationdto) Notification of a change in the order status. `notificationType` = `ORDER_STATUS_UPDATED` To change the order status Use the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/updateOrderStatus).  
...rest |  **oneOf** [OrderCancelledNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercancellednotificationdto) Notification of order cancellation. `notificationType` = `ORDER_CANCELLED`  
...rest |  **oneOf** [OrderCancellationRequestNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercancellationrequestnotificationdto) Notification of the creation of an order cancellation request (for DBS stores). `notificationType` = `ORDER_CANCELLATION_REQUEST` To confirm or reject an application Use the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/cancellation/accept](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/acceptOrderCancellation).  
...rest |  **oneOf** [OrderReturnCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderreturncreatednotificationdto) Notification of the creation of a new non-purchase or refund. `notificationType` = `ORDER_RETURN_CREATED` To get detailed information about non-purchase or refund Use the method [GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/getReturn).  
...rest |  **oneOf** [OrderReturnStatusUpdatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderreturnstatusupdatednotificationdto) Notification of a change in the non-purchase or refund status. `notificationType` = `ORDER_RETURN_STATUS_UPDATED` To get detailed information about non-purchase or refund Use the method [GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/getReturn).  
...rest |  **oneOf** [OrderUpdatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderupdatednotificationdto) Notification of order changes. `notificationType` = `ORDER_UPDATED` To get detailed information about the order Use the method [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/getOrder).  
...rest |  **oneOf** [GoodsFeedbackCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#goodsfeedbackcreatednotificationdto) Notification of the creation of a new product review. `notificationType` = `GOODS_FEEDBACK_CREATED` Yandex.Market sends notifications about reviews only when they have been moderated and published. To get detailed information about reviews Use the method [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/goods-feedback/getGoodsFeedbacks) where specify their IDs in the parameter `feedbackIds`. You will not be able to get the information if the customer or the Market has deleted the review.  
...rest |  **oneOf** [GoodsFeedbackCommentCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#goodsfeedbackcommentcreatednotificationdto) Notification of the creation of a new review comment. `notificationType` = `GOODS_FEEDBACK_COMMENT_CREATED` To get detailed information about the comments to the review Use the method [POST v2/businesses/{businessId}/goods-feedback/comments](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/goods-feedback/getGoodsFeedbackComments) where specify their IDs in the parameter `commentIds`. You will not be able to receive information if the user or the Market has deleted a comment or review to which it was added.  
...rest |  **oneOf** [ChatCreatedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatcreatednotificationdto) Notification of the creation of a new chat with the buyer. `notificationType` = `CHAT_CREATED` To get a chat with a customer Use the method [GET v2/businesses/{businessId}/chat](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/chats/getChat) where specify the chat ID in the parameter `chatId`.  
...rest |  **oneOf** [ChatMessageSentNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatmessagesentnotificationdto) Notification of a new message in the chat. `notificationType` = `CHAT_MESSAGE_SENT` To receive a message from the buyer Use the method [GET v2/businesses/{businessId}/chats/message](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/chats/getChatMessage) where to specify the IDs:
  * chat rooms — `chatId`;
  * messages — `messageId`.

  
...rest |  **oneOf** [ChatArbitrageStartedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatarbitragestartednotificationdto) Notification of the beginning of the dispute. `notificationType` = `CHAT_ARBITRAGE_STARTED`  
...rest |  **oneOf** [ChatArbitrageFinishedNotificationDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatarbitragefinishednotificationdto) Notification of the end of the dispute. `notificationType` = `CHAT_ARBITRAGE_FINISHED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype)NotificationType
Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

**Type** |  **Description**  
---|---  
[NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) |  _Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#pingnotificationdto)PingNotificationDTO
Verification notification.
`notificationType` = `PING`
**Name** |  **Description**  
---|---  
notificationType |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
time |  **Type:** string<date-time> The date and time when the notification was processed by the store. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercreatednotificationdto)OrderCreatedNotificationDTO
Notification of the creation of a new order.
`notificationType` = `ORDER_CREATED`
To get detailed information about the order
Use the method [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/getOrder).
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. It can be found using the method [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
createdAt* |  **Type:** string<date-time> Date and time of the order creation. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
items* |  **Type:** [NotificationOrderItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationorderitemdto)[] The list of products in the order.  
Information about the product in the order.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
orderId* |  **Type:** integer<int64> The order ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderstatusupdatednotificationdto)OrderStatusUpdatedNotificationDTO
Notification of a change in the order status.
`notificationType` = `ORDER_STATUS_UPDATED`
To change the order status
Use the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/status](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/updateOrderStatus).
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. It can be found using the method [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
orderId* |  **Type:** integer<int64> The order ID.  
status* |  **Type:** [OrderStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderstatustype) Order status:
  * `PLACING` — it is being processed, preparing for the reservation.
  * `RESERVED` — reserved, but under-booked.
  * `UNPAID` — issued, but not yet paid (if payment is selected at checkout).
  * `PROCESSING` — it is under processing.
  * `DELIVERY` — transferred to the delivery service.
  * `PICKUP` — delivered to the pick-up point.
  * `DELIVERED` — received by the buyer.
  * `CANCELLED` — cancelled.
  * `PENDING` — awaiting processing by the seller.
  * `PARTIALLY_RETURNED` — partially returned.
  * `RETURNED` — returned in full.
  * `UNKNOWN` — unknown status.

Other values may also be returned. You don't need to process them. _Enum:_ `PLACING`, `RESERVED`, `UNPAID`, `PROCESSING`, `DELIVERY`, `PICKUP`, `DELIVERED`, `CANCELLED`, `PENDING`, `PARTIALLY_RETURNED`, `RETURNED`, `UNKNOWN`  
substatus* |  **Type:** [OrderSubstatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordersubstatustype) The stage of order processing (if it has the status `PROCESSING`) or the reason for the cancellation of the order (if it has the status `CANCELLED`).
  * Order values in the status `PROCESSING`:
    * `STARTED` — the order has been confirmed, and it can be processed.
    * `READY_TO_SHIP` — the order is collected and ready for shipment.
  * Order values in the status `CANCELLED`:
    * `RESERVATION_EXPIRED` — the customer did not complete the reserved order within 10 minutes.
    * `USER_NOT_PAID` — the buyer has not paid for the order (for the type of payment `PREPAID`) for 30 minutes.
    * `USER_UNREACHABLE` — couldn't contact the buyer. To cancel with this reason, the following conditions must be met:
      * at least 3 calls from 8 to 21 in the buyer's time zone;
      * the break between the first and third calls is at least 90 minutes;
      * the connection is no shorter than 5 seconds.
If at least one of these conditions is not met (except when the number is unavailable), you will not be able to cancel the order. A response with the error code 400 will be returned.
    * `USER_CHANGED_MIND` — the customer cancelled the order for personal reasons.
    * `USER_REFUSED_DELIVERY` — the buyer was not satisfied with the terms of delivery.
    * `USER_REFUSED_PRODUCT` — the product did not fit the buyer.
    * `SHOP_FAILED` — the store cannot complete the order.
    * `USER_REFUSED_QUALITY` — the buyer was not satisfied with the quality of the product.
    * `REPLACING_ORDER` — the buyer decided to replace the product with another one on his own initiative.
    * `PROCESSING_EXPIRED` — the value is no longer used.
    * `PICKUP_EXPIRED` — the storage period of the order in the PVZ has expired.
    * `TOO_MANY_DELIVERY_DATE_CHANGES` — the order has been postponed too many times.
    * `TOO_LONG_DELIVERY` — the order is taking too long to be delivered.
    * `INCORRECT_PERSONAL_DATA` — incorrect personal data has been entered.
  * `TECHNICAL_ERROR` — a technical error on the Market's side. Contact support.

Other values may also be returned. You don't need to process them. _Enum:_ `RESERVATION_EXPIRED`, `USER_NOT_PAID`, `USER_UNREACHABLE`, `USER_CHANGED_MIND`, `USER_REFUSED_DELIVERY`, `USER_REFUSED_PRODUCT`, `SHOP_FAILED`, `USER_REFUSED_QUALITY`, `REPLACING_ORDER`, `PROCESSING_EXPIRED`, `PENDING_EXPIRED`, `SHOP_PENDING_CANCELLED`, `PENDING_CANCELLED`, `USER_FRAUD`, `RESERVATION_FAILED`, `USER_PLACED_OTHER_ORDER`, `USER_BOUGHT_CHEAPER`, `MISSING_ITEM`, `BROKEN_ITEM`, `WRONG_ITEM`, `PICKUP_EXPIRED`, `DELIVERY_PROBLEMS`, `LATE_CONTACT`, `CUSTOM`, `DELIVERY_SERVICE_FAILED`, `WAREHOUSE_FAILED_TO_SHIP`, `DELIVERY_SERVICE_UNDELIVERED`, `PREORDER`, `AWAIT_CONFIRMATION`, `STARTED`, `PACKAGING`, `READY_TO_SHIP`, `SHIPPED`, `ASYNC_PROCESSING`, `WAITING_USER_INPUT`, `WAITING_BANK_DECISION`, `BANK_REJECT_CREDIT_OFFER`, `CUSTOMER_REJECT_CREDIT_OFFER`, `CREDIT_OFFER_FAILED`, `AWAIT_DELIVERY_DATES_CONFIRMATION`, `SERVICE_FAULT`, `DELIVERY_SERVICE_RECEIVED`, `USER_RECEIVED`, `WAITING_FOR_STOCKS`, `AS_PART_OF_MULTI_ORDER`, `READY_FOR_LAST_MILE`, `LAST_MILE_STARTED`, `ANTIFRAUD`, `DELIVERY_USER_NOT_RECEIVED`, `DELIVERY_SERVICE_DELIVERED`, `DELIVERED_USER_NOT_RECEIVED`, `USER_WANTED_ANOTHER_PAYMENT_METHOD`, `USER_RECEIVED_TECHNICAL_ERROR`, `USER_FORGOT_TO_USE_BONUS`, `DELIVERY_SERVICE_NOT_RECEIVED`, `DELIVERY_SERVICE_LOST`, `SHIPPED_TO_WRONG_DELIVERY_SERVICE`, `DELIVERED_USER_RECEIVED`, `WAITING_TINKOFF_DECISION`, `COURIER_SEARCH`, `COURIER_FOUND`, `COURIER_IN_TRANSIT_TO_SENDER`, `COURIER_ARRIVED_TO_SENDER`, `COURIER_RECEIVED`, `COURIER_NOT_FOUND`, `COURIER_NOT_DELIVER_ORDER`, `COURIER_RETURNS_ORDER`, `COURIER_RETURNED_ORDER`, `WAITING_USER_DELIVERY_INPUT`, `PICKUP_SERVICE_RECEIVED`, `PICKUP_USER_RECEIVED`, `CANCELLED_COURIER_NOT_FOUND`, `COURIER_NOT_COME_FOR_ORDER`, `DELIVERY_NOT_MANAGED_REGION`, `INCOMPLETE_CONTACT_INFORMATION`, `INCOMPLETE_MULTI_ORDER`, `INAPPROPRIATE_WEIGHT_SIZE`, `TECHNICAL_ERROR`, `SORTING_CENTER_LOST`, `COURIER_SEARCH_NOT_STARTED`, `LOST`, `AWAIT_PAYMENT`, `AWAIT_LAVKA_RESERVATION`, `USER_WANTS_TO_CHANGE_ADDRESS`, `FULL_NOT_RANSOM`, `PRESCRIPTION_MISMATCH`, `DROPOFF_LOST`, `DROPOFF_CLOSED`, `DELIVERY_TO_STORE_STARTED`, `USER_WANTS_TO_CHANGE_DELIVERY_DATE`, `WRONG_ITEM_DELIVERED`, `DAMAGED_BOX`, `AWAIT_DELIVERY_DATES`, `LAST_MILE_COURIER_SEARCH`, `PICKUP_POINT_CLOSED`, `LEGAL_INFO_CHANGED`, `USER_HAS_NO_TIME_TO_PICKUP_ORDER`, `DELIVERY_CUSTOMS_ARRIVED`, `DELIVERY_CUSTOMS_CLEARED`, `FIRST_MILE_DELIVERY_SERVICE_RECEIVED`, `AWAIT_AUTO_DELIVERY_DATES`, `AWAIT_USER_PERSONAL_DATA`, `NO_PERSONAL_DATA_EXPIRED`, `CUSTOMS_PROBLEMS`, `AWAIT_CASHIER`, `WAITING_POSTPAID_BUDGET_RESERVATION`, `AWAIT_SERVICEABLE_CONFIRMATION`, `POSTPAID_BUDGET_RESERVATION_FAILED`, `AWAIT_CUSTOM_PRICE_CONFIRMATION`, `READY_FOR_PICKUP`, `TOO_MANY_DELIVERY_DATE_CHANGES`, `TOO_LONG_DELIVERY`, `DEFERRED_PAYMENT`, `POSTPAID_FAILED`, `INCORRECT_PERSONAL_DATA`, `UNKNOWN`  
updatedAt* |  **Type:** string<date-time> Date and time of the order status change. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercancellednotificationdto)OrderCancelledNotificationDTO
Notification of order cancellation.
`notificationType` = `ORDER_CANCELLED`
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. It can be found using the method [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
cancelledAt* |  **Type:** string<date-time> Date and time of cancellation of the order. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
items* |  **Type:** [NotificationOrderItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationorderitemdto)[] The list of products in the order.  
Information about the product in the order.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
orderId* |  **Type:** integer<int64> The order ID.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordercancellationrequestnotificationdto)OrderCancellationRequestNotificationDTO
Notification of the creation of an order cancellation request (for DBS stores).
`notificationType` = `ORDER_CANCELLATION_REQUEST`
To confirm or reject an application
Use the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/cancellation/accept](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/acceptOrderCancellation).
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. It can be found using the method [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
orderId* |  **Type:** integer<int64> The order ID.  
requestedAt* |  **Type:** string<date-time> The date and time when the cancellation request was created. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderreturncreatednotificationdto)OrderReturnCreatedNotificationDTO
Notification of the creation of a new non-purchase or refund.
`notificationType` = `ORDER_RETURN_CREATED`
To get detailed information about non-purchase or refund
Use the method [GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/getReturn).
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. It can be found using the method [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
createdAt* |  **Type:** string<date-time> The date and time when the non-purchase or refund was created. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
items* |  **Type:** [NotificationReturnItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationreturnitemdto)[] A list of items that have not been purchased or returned.  
Information about the product in non-purchase or return.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the status of non-purchase or refund has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
orderId* |  **Type:** integer<int64> The order ID.  
returnId* |  **Type:** integer<int64> ID of a non-purchase or refund.  
returnType* |  **Type:** [ReturnType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#returntype) Order type for filtering:
  * `UNREDEEMED` — non-purchase.
  * `RETURN` — refund.

If you do not specify it, the response will include both non-purchases and refunds. _Enum:_ `UNREDEEMED`, `RETURN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderreturnstatusupdatednotificationdto)OrderReturnStatusUpdatedNotificationDTO
Notification of a change in the non-purchase or refund status.
`notificationType` = `ORDER_RETURN_STATUS_UPDATED`
To get detailed information about non-purchase or refund
Use the method [GET v2/campaigns/{campaignId}/orders/{orderId}/returns/{returnId}](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/getReturn).
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. It can be found using the method [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
orderId* |  **Type:** integer<int64> The order ID.  
returnId* |  **Type:** integer<int64> ID of a non-purchase or refund.  
statuses* |  **Type:** [NotificationUpdatedReturnStatusesDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationupdatedreturnstatusesdto) Information about updating the non-purchase or refund status. Only the status that was changed is returned. For non-purchases, only `shipmentStatus`. Parameter `shipmentStatus` does not arrive for refunds with the option **A quick refund for a cheap marriage** , when the product remains with the buyer.  
updatedAt* |  **Type:** string<date-time> The date and time when the non-purchase or refund status was changed. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderupdatednotificationdto)OrderUpdatedNotificationDTO
Notification of order changes.
`notificationType` = `ORDER_UPDATED`
To get detailed information about the order
Use the method [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/orders/getOrder).
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. It can be found using the method [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
orderId* |  **Type:** integer<int64> The order ID.  
updateType* |  **Type:** [OrderUpdateType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderupdatetype) The type of order change. _Enum:_ `SHIPMENT_DATE_UPDATED`, `DELIVERY_DATE_UPDATED`, `UNKNOWN`  
updatedAt* |  **Type:** string<date-time> Date and time of the order change. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#goodsfeedbackcreatednotificationdto)GoodsFeedbackCreatedNotificationDTO
Notification of the creation of a new product review.
`notificationType` = `GOODS_FEEDBACK_CREATED`
Yandex.Market sends notifications about reviews only when they have been moderated and published.
To get detailed information about reviews
Use the method [POST v2/businesses/{businessId}/goods-feedback](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/goods-feedback/getGoodsFeedbacks) where specify their IDs in the parameter `feedbackIds`.
You will not be able to get the information if the customer or the Market has deleted the review.
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
createdAt* |  **Type:** string<date-time> The date and time when the review was created. It may differ from the information in `publishedAt`, since the review has been undergoing moderation for some time. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
feedbackId* |  **Type:** integer<int64> The review ID.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
publishedAt* |  **Type:** string<date-time> Date and time of publication of the review. It may differ from the information in `createdAt`, since the review has been undergoing moderation for some time. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#goodsfeedbackcommentcreatednotificationdto)GoodsFeedbackCommentCreatedNotificationDTO
Notification of the creation of a new review comment.
`notificationType` = `GOODS_FEEDBACK_COMMENT_CREATED`
To get detailed information about the comments to the review
Use the method [POST v2/businesses/{businessId}/goods-feedback/comments](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/goods-feedback/getGoodsFeedbackComments) where specify their IDs in the parameter `commentIds`.
You will not be able to receive information if the user or the Market has deleted a comment or review to which it was added.
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
commentId* |  **Type:** integer<int64> ID of the review comment.  
createdAt* |  **Type:** string<date-time> Date and time when the comment was created. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatcreatednotificationdto)ChatCreatedNotificationDTO
Notification of the creation of a new chat with the buyer.
`notificationType` = `CHAT_CREATED`
To get a chat with a customer
Use the method [GET v2/businesses/{businessId}/chat](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/chats/getChat) where specify the chat ID in the parameter `chatId`.
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
chatId* |  **Type:** integer<int64> The chat ID.  
createdAt* |  **Type:** string<date-time> Date and time when the chat was created. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — a new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatmessagesentnotificationdto)ChatMessageSentNotificationDTO
Notification of a new message in the chat.
`notificationType` = `CHAT_MESSAGE_SENT`
To receive a message from the buyer
Use the method [GET v2/businesses/{businessId}/chats/message](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/reference/chats/getChatMessage) where to specify the IDs:
  * chat rooms — `chatId`;
  * messages — `messageId`.


**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
chatId* |  **Type:** integer<int64> The chat ID.  
messageId* |  **Type:** string The ID of the message.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — a new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
sentAt* |  **Type:** string<date-time> The date and time when the message was sent. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatarbitragestartednotificationdto)ChatArbitrageStartedNotificationDTO
Notification of the beginning of the dispute.
`notificationType` = `CHAT_ARBITRAGE_STARTED`
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
chatId* |  **Type:** integer<int64> The chat ID.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
startedAt* |  **Type:** string<date-time> The date and time of the beginning of the dispute. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#chatarbitragefinishednotificationdto)ChatArbitrageFinishedNotificationDTO
Notification of the end of the dispute.
`notificationType` = `CHAT_ARBITRAGE_FINISHED`
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID.  
chatId* |  **Type:** integer<int64> The chat ID.  
finishedAt* |  **Type:** string<date-time> The date and time of the end of the dispute. Date format: ISO 8601 with an offset relative to UTC. For example, `2017-11-21T00:00:00.213Z`.  
notificationType* |  **Type:** [NotificationType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationtype) Notification type:
  * `PING` — verification notification.
  * `ORDER_CREATED` — a new order has been created.
  * `ORDER_CANCELLED` — the order has been cancelled.
  * `ORDER_STATUS_UPDATED` — the order status has been changed.
  * `ORDER_RETURN_CREATED` — a new non-purchase or refund has been created.
  * `ORDER_CANCELLATION_REQUEST` — an order cancellation request has been created (for DBS stores).
  * `ORDER_RETURN_STATUS_UPDATED` — the non-purchase or refund status has been changed.
  * `ORDER_UPDATED` — the order has been changed.
  * `GOODS_FEEDBACK_CREATED` — a new product review has been created.
  * `GOODS_FEEDBACK_COMMENT_CREATED` — A new product review comment has been created.
  * `CHAT_CREATED` — a new chat with the buyer has been created.
  * `CHAT_MESSAGE_SENT` — A new chat message has been added.
  * `CHAT_ARBITRAGE_STARTED` — at the request of the buyer, a dispute began.
  * `CHAT_ARBITRAGE_FINISHED` — the dispute is over.

_Enum:_ `PING`, `ORDER_CREATED`, `ORDER_CANCELLED`, `ORDER_STATUS_UPDATED`, `ORDER_RETURN_CREATED`, `ORDER_CANCELLATION_REQUEST`, `ORDER_RETURN_STATUS_UPDATED`, `ORDER_UPDATED`, `GOODS_FEEDBACK_CREATED`, `GOODS_FEEDBACK_COMMENT_CREATED`, `CHAT_CREATED`, `CHAT_MESSAGE_SENT`, `CHAT_ARBITRAGE_STARTED`, `CHAT_ARBITRAGE_FINISHED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationorderitemdto)NotificationOrderItemDTO
Information about the product in the order.
**Name** |  **Description**  
---|---  
count* |  **Type:** integer The quantity of the product.  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderstatustype)OrderStatusType
Order status:
  * `PLACING` — it is being processed, preparing for the reservation.
  * `RESERVED` — reserved, but under-booked.
  * `UNPAID` — issued, but not yet paid (if payment is selected at checkout).
  * `PROCESSING` — it is under processing.
  * `DELIVERY` — transferred to the delivery service.
  * `PICKUP` — delivered to the pick-up point.
  * `DELIVERED` — received by the buyer.
  * `CANCELLED` — cancelled.
  * `PENDING` — awaiting processing by the seller.
  * `PARTIALLY_RETURNED` — partially returned.
  * `RETURNED` — returned in full.
  * `UNKNOWN` — unknown status.


Other values may also be returned. You don't need to process them.
**Type** |  **Description**  
---|---  
[OrderStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderstatustype) |  _Enum:_ `PLACING`, `RESERVED`, `UNPAID`, `PROCESSING`, `DELIVERY`, `PICKUP`, `DELIVERED`, `CANCELLED`, `PENDING`, `PARTIALLY_RETURNED`, `RETURNED`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordersubstatustype)OrderSubstatusType
The stage of order processing (if it has the status `PROCESSING`) or the reason for the cancellation of the order (if it has the status `CANCELLED`).
  * Order values in the status `PROCESSING`:
    * `STARTED` — the order has been confirmed, and it can be processed.
    * `READY_TO_SHIP` — the order is collected and ready for shipment.
  * Order values in the status `CANCELLED`:
    * `RESERVATION_EXPIRED` — the customer did not complete the reserved order within 10 minutes.
    * `USER_NOT_PAID` — the buyer has not paid for the order (for the type of payment `PREPAID`) for 30 minutes.
    * `USER_UNREACHABLE` — couldn't contact the buyer. To cancel with this reason, the following conditions must be met:
      * at least 3 calls from 8 to 21 in the buyer's time zone;
      * the break between the first and third calls is at least 90 minutes;
      * the connection is no shorter than 5 seconds.
If at least one of these conditions is not met (except when the number is unavailable), you will not be able to cancel the order. A response with the error code 400 will be returned.
    * `USER_CHANGED_MIND` — the customer cancelled the order for personal reasons.
    * `USER_REFUSED_DELIVERY` — the buyer was not satisfied with the terms of delivery.
    * `USER_REFUSED_PRODUCT` — the product did not fit the buyer.
    * `SHOP_FAILED` — the store cannot complete the order.
    * `USER_REFUSED_QUALITY` — the buyer was not satisfied with the quality of the product.
    * `REPLACING_ORDER` — the buyer decided to replace the product with another one on his own initiative.
    * `PROCESSING_EXPIRED` — the value is no longer used.
    * `PICKUP_EXPIRED` — the storage period of the order in the PVZ has expired.
    * `TOO_MANY_DELIVERY_DATE_CHANGES` — the order has been postponed too many times.
    * `TOO_LONG_DELIVERY` — the order is taking too long to be delivered.
    * `INCORRECT_PERSONAL_DATA` — incorrect personal data has been entered.
  * `TECHNICAL_ERROR` — a technical error on the Market's side. Contact support.


Other values may also be returned. You don't need to process them.
**Type** |  **Description**  
---|---  
[OrderSubstatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#ordersubstatustype) |  _Enum:_ `RESERVATION_EXPIRED`, `USER_NOT_PAID`, `USER_UNREACHABLE`, `USER_CHANGED_MIND`, `USER_REFUSED_DELIVERY`, `USER_REFUSED_PRODUCT`, `SHOP_FAILED`, `USER_REFUSED_QUALITY`, `REPLACING_ORDER`, `PROCESSING_EXPIRED`, `PENDING_EXPIRED`, `SHOP_PENDING_CANCELLED`, `PENDING_CANCELLED`, `USER_FRAUD`, `RESERVATION_FAILED`, `USER_PLACED_OTHER_ORDER`, `USER_BOUGHT_CHEAPER`, `MISSING_ITEM`, `BROKEN_ITEM`, `WRONG_ITEM`, `PICKUP_EXPIRED`, `DELIVERY_PROBLEMS`, `LATE_CONTACT`, `CUSTOM`, `DELIVERY_SERVICE_FAILED`, `WAREHOUSE_FAILED_TO_SHIP`, `DELIVERY_SERVICE_UNDELIVERED`, `PREORDER`, `AWAIT_CONFIRMATION`, `STARTED`, `PACKAGING`, `READY_TO_SHIP`, `SHIPPED`, `ASYNC_PROCESSING`, `WAITING_USER_INPUT`, `WAITING_BANK_DECISION`, `BANK_REJECT_CREDIT_OFFER`, `CUSTOMER_REJECT_CREDIT_OFFER`, `CREDIT_OFFER_FAILED`, `AWAIT_DELIVERY_DATES_CONFIRMATION`, `SERVICE_FAULT`, `DELIVERY_SERVICE_RECEIVED`, `USER_RECEIVED`, `WAITING_FOR_STOCKS`, `AS_PART_OF_MULTI_ORDER`, `READY_FOR_LAST_MILE`, `LAST_MILE_STARTED`, `ANTIFRAUD`, `DELIVERY_USER_NOT_RECEIVED`, `DELIVERY_SERVICE_DELIVERED`, `DELIVERED_USER_NOT_RECEIVED`, `USER_WANTED_ANOTHER_PAYMENT_METHOD`, `USER_RECEIVED_TECHNICAL_ERROR`, `USER_FORGOT_TO_USE_BONUS`, `DELIVERY_SERVICE_NOT_RECEIVED`, `DELIVERY_SERVICE_LOST`, `SHIPPED_TO_WRONG_DELIVERY_SERVICE`, `DELIVERED_USER_RECEIVED`, `WAITING_TINKOFF_DECISION`, `COURIER_SEARCH`, `COURIER_FOUND`, `COURIER_IN_TRANSIT_TO_SENDER`, `COURIER_ARRIVED_TO_SENDER`, `COURIER_RECEIVED`, `COURIER_NOT_FOUND`, `COURIER_NOT_DELIVER_ORDER`, `COURIER_RETURNS_ORDER`, `COURIER_RETURNED_ORDER`, `WAITING_USER_DELIVERY_INPUT`, `PICKUP_SERVICE_RECEIVED`, `PICKUP_USER_RECEIVED`, `CANCELLED_COURIER_NOT_FOUND`, `COURIER_NOT_COME_FOR_ORDER`, `DELIVERY_NOT_MANAGED_REGION`, `INCOMPLETE_CONTACT_INFORMATION`, `INCOMPLETE_MULTI_ORDER`, `INAPPROPRIATE_WEIGHT_SIZE`, `TECHNICAL_ERROR`, `SORTING_CENTER_LOST`, `COURIER_SEARCH_NOT_STARTED`, `LOST`, `AWAIT_PAYMENT`, `AWAIT_LAVKA_RESERVATION`, `USER_WANTS_TO_CHANGE_ADDRESS`, `FULL_NOT_RANSOM`, `PRESCRIPTION_MISMATCH`, `DROPOFF_LOST`, `DROPOFF_CLOSED`, `DELIVERY_TO_STORE_STARTED`, `USER_WANTS_TO_CHANGE_DELIVERY_DATE`, `WRONG_ITEM_DELIVERED`, `DAMAGED_BOX`, `AWAIT_DELIVERY_DATES`, `LAST_MILE_COURIER_SEARCH`, `PICKUP_POINT_CLOSED`, `LEGAL_INFO_CHANGED`, `USER_HAS_NO_TIME_TO_PICKUP_ORDER`, `DELIVERY_CUSTOMS_ARRIVED`, `DELIVERY_CUSTOMS_CLEARED`, `FIRST_MILE_DELIVERY_SERVICE_RECEIVED`, `AWAIT_AUTO_DELIVERY_DATES`, `AWAIT_USER_PERSONAL_DATA`, `NO_PERSONAL_DATA_EXPIRED`, `CUSTOMS_PROBLEMS`, `AWAIT_CASHIER`, `WAITING_POSTPAID_BUDGET_RESERVATION`, `AWAIT_SERVICEABLE_CONFIRMATION`, `POSTPAID_BUDGET_RESERVATION_FAILED`, `AWAIT_CUSTOM_PRICE_CONFIRMATION`, `READY_FOR_PICKUP`, `TOO_MANY_DELIVERY_DATE_CHANGES`, `TOO_LONG_DELIVERY`, `DEFERRED_PAYMENT`, `POSTPAID_FAILED`, `INCORRECT_PERSONAL_DATA`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationreturnitemdto)NotificationReturnItemDTO
Information about the product in non-purchase or return.
**Name** |  **Description**  
---|---  
count* |  **Type:** integer The quantity of the product.  
offerId* |  **Type:** string Your SKU is the product identifier in your system. SKU Usage Rules:
  * Each product must have its own SKU.
  * An already set SKU cannot be released and reused for another product. Each product should receive a new identifier that has never been used in your catalog before.

The SKU of the product can be changed in the seller's account on the Market. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/assortment/operations/edit-sku). [What is a SKU and how to assign it](https://yandex.ru/support/marketplace/assortment/add/index.html#fields) _Min length:_ `1` _Max length:_ `255` _Pattern:_ `^(?=.*\S.*)[^\x00-\x08\x0A-\x1f\x7f]{1,255}$`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#returntype)ReturnType
Order type for filtering:
  * `UNREDEEMED` — non-purchase.
  * `RETURN` — refund.


If you do not specify it, the response will include both non-purchases and refunds.
**Type** |  **Description**  
---|---  
[ReturnType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#returntype) |  _Enum:_ `UNREDEEMED`, `RETURN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationupdatedreturnstatusesdto)NotificationUpdatedReturnStatusesDTO
Information about updating the non-purchase or refund status.
Only the status that was changed is returned.
For non-purchases, only `shipmentStatus`.
Parameter `shipmentStatus` does not arrive for refunds with the option **A quick refund for a cheap marriage** , when the product remains with the buyer.
**Name** |  **Description**  
---|---  
refundStatus |  **Type:** [RefundStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#refundstatustype) Refund status:
  * `STARTED_BY_USER` — created by the client from his personal account.
  * `REFUND_IN_PROGRESS` — awaiting a decision on a refund.
  * `REFUNDED` — the money has been returned.
  * `FAILED` — it is impossible to make a refund to the buyer.
  * `WAITING_FOR_DECISION` — awaiting a decision (DBS).
  * `DECISION_MADE` — a decision has been made on the refund (DBS).
  * `REFUNDED_WITH_BONUSES` — the refund is made with Bonus points or a promo code.
  * `REFUNDED_BY_SHOP` — the store made a refund on its own.
  * `COMPLETE_WITHOUT_REFUND` — No refund is required.
  * `CANCELLED` — the refund has been canceled.
  * `REJECTED` — the refund was rejected by moderation or by the PVZ.
  * `PREMODERATION_DISPUTE` — there is a dispute on the refund (FBY, FBS and Express).
  * `PREMODERATION_DECISION_WAITING` — awaiting a decision (FBY, FBS and Express).
  * `PREMODERATION_DECISION_MADE` — a decision has been made on the refund (FBY, FBS and Express).
  * `PREMODERATION_SELECT_DELIVERY` — The user selects the delivery method (FBY, FBS and Express).
  * `UNKNOWN` — unknown status.

_Enum:_ `STARTED_BY_USER`, `REFUND_IN_PROGRESS`, `REFUNDED`, `FAILED`, `WAITING_FOR_DECISION`, `DECISION_MADE`, `REFUNDED_WITH_BONUSES`, `REFUNDED_BY_SHOP`, `CANCELLED`, `REJECTED`, `COMPLETE_WITHOUT_REFUND`, `PREMODERATION_DISPUTE`, `PREMODERATION_DECISION_WAITING`, `PREMODERATION_DECISION_MADE`, `PREMODERATION_SELECT_DELIVERY`, `UNKNOWN`  
shipmentStatus |  **Type:** [ReturnShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#returnshipmentstatustype) Refund transfer status:
  * `CREATED` — refund has been created.
  * `RECEIVED` — accepted from the buyer.
  * `IN_TRANSIT` — return on the way.
  * `READY_FOR_PICKUP` — the refund is ready to be issued to the store.
  * `PICKED` — a refund has been issued to the store.
  * `LOST` — the refund is lost during transportation.
  * `EXPIRED` — The buyer did not bring the goods for return on time.
  * `CANCELLED` — the refund has been canceled.
  * `FULFILMENT_RECEIVED` — the refund is accepted at the Market warehouse.
  * `PREPARED_FOR_UTILIZATION` — the return has been disposed of.
  * `NOT_IN_DEMAND` — the refund was not picked up from the post office.
  * `UTILIZED` — the refund has been disposed of.
  * `READY_FOR_EXPROPRIATION` — the items in the return are sent for resale.
  * `RECEIVED_FOR_EXPROPRIATION` — Items in the return are accepted for resale.
  * `UNKNOWN` — unknown status.

_Enum:_ `CREATED`, `RECEIVED`, `IN_TRANSIT`, `READY_FOR_PICKUP`, `PICKED`, `LOST`, `EXPIRED`, `CANCELLED`, `FULFILMENT_RECEIVED`, `PREPARED_FOR_UTILIZATION`, `NOT_IN_DEMAND`, `UTILIZED`, `READY_FOR_EXPROPRIATION`, `RECEIVED_FOR_EXPROPRIATION`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderupdatetype)OrderUpdateType
Type of order change:
  * `SHIPMENT_DATE_UPDATED` — change of the shipment date.
  * `DELIVERY_DATE_UPDATED` — change of the delivery date.
  * `UNKNOWN` — unknown type.

**Type** |  **Description**  
---|---  
[OrderUpdateType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#orderupdatetype) |  _Enum:_ `SHIPMENT_DATE_UPDATED`, `DELIVERY_DATE_UPDATED`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#refundstatustype)RefundStatusType
Refund status:
  * `STARTED_BY_USER` — created by the client from his personal account.
  * `REFUND_IN_PROGRESS` — awaiting a decision on a refund.
  * `REFUNDED` — the money has been returned.
  * `FAILED` — it is impossible to make a refund to the buyer.
  * `WAITING_FOR_DECISION` — awaiting a decision (DBS).
  * `DECISION_MADE` — a decision has been made on the refund (DBS).
  * `REFUNDED_WITH_BONUSES` — the refund is made with Plus points or a promo code.
  * `REFUNDED_BY_SHOP` — the store made a refund on its own.
  * `COMPLETE_WITHOUT_REFUND` — No refund is required.
  * `CANCELLED` — the refund has been canceled.
  * `REJECTED` — the refund was rejected by moderation or by the PVZ.
  * `PREMODERATION_DISPUTE` — there is a dispute on the refund (FBY, FBS and Express).
  * `PREMODERATION_DECISION_WAITING` — awaiting a decision (FBY, FBS and Express).
  * `PREMODERATION_DECISION_MADE` — a decision has been made on the refund (FBY, FBS and Express).
  * `PREMODERATION_SELECT_DELIVERY` — The user selects the delivery method (FBY, FBS and Express).
  * `UNKNOWN` — unknown status.

**Type** |  **Description**  
---|---  
[RefundStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#refundstatustype) |  _Enum:_ `STARTED_BY_USER`, `REFUND_IN_PROGRESS`, `REFUNDED`, `FAILED`, `WAITING_FOR_DECISION`, `DECISION_MADE`, `REFUNDED_WITH_BONUSES`, `REFUNDED_BY_SHOP`, `CANCELLED`, `REJECTED`, `COMPLETE_WITHOUT_REFUND`, `PREMODERATION_DISPUTE`, `PREMODERATION_DECISION_WAITING`, `PREMODERATION_DECISION_MADE`, `PREMODERATION_SELECT_DELIVERY`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#returnshipmentstatustype)ReturnShipmentStatusType
Refund transfer status:
  * `CREATED` — refund has been created.
  * `RECEIVED` — accepted from the buyer.
  * `IN_TRANSIT` — return on the way.
  * `READY_FOR_PICKUP` — the refund is ready to be issued to the store.
  * `PICKED` — a refund has been issued to the store.
  * `LOST` — the refund is lost during transportation.
  * `EXPIRED` — The buyer did not bring the goods for return on time.
  * `CANCELLED` — the refund has been canceled.
  * `FULFILMENT_RECEIVED` — the refund is accepted at the Market warehouse.
  * `PREPARED_FOR_UTILIZATION` — the return has been disposed of.
  * `NOT_IN_DEMAND` — the refund was not picked up from the post office.
  * `UTILIZED` — the refund has been disposed of.
  * `READY_FOR_EXPROPRIATION` — the items in the return are sent for resale.
  * `RECEIVED_FOR_EXPROPRIATION` — Items in the return are accepted for resale.
  * `UNKNOWN` — unknown status.

**Type** |  **Description**  
---|---  
[ReturnShipmentStatusType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#returnshipmentstatustype) |  _Enum:_ `CREATED`, `RECEIVED`, `IN_TRANSIT`, `READY_FOR_PICKUP`, `PICKED`, `LOST`, `EXPIRED`, `CANCELLED`, `FULFILMENT_RECEIVED`, `PREPARED_FOR_UTILIZATION`, `NOT_IN_DEMAND`, `UTILIZED`, `READY_FOR_EXPROPRIATION`, `RECEIVED_FOR_EXPROPRIATION`, `UNKNOWN`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#200-ok)200 OK
A response to a valid request with information about notification processing.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#body1)Body
application/json
```
{
    "version": "string",
    "name": "string",
    "time": "2022-12-29T18:02:01Z"
}

```

**Name** |  **Description**  
---|---  
name* |  **Type:** string The name of the integration. _Min length:_ `1` _Max length:_ `100`  
time* |  **Type:** string<date-time> The date and time of the start of notification processing in UTC format.  
version* |  **Type:** string The integration version. _Min length:_ `1` _Max length:_ `100`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#400-bad-request)400 Bad Request
If the Market has sent an incorrect notification, return the status `400` with a description of the error.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#body2)Body
application/json
```
{
    "error": {
        "type": "UNKNOWN",
        "message": "string"
    }
}

```

**Name** |  **Description**  
---|---  
error |  **Type:** [NotificationApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationapierrordto) Error when processing the notification.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationapierrordto)NotificationApiErrorDTO
Error when processing the notification.
**Name** |  **Description**  
---|---  
message |  **Type:** string Description of the error.  
type |  **Type:** [NotificationApiErrorType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationapierrortype) Error type:
  * `UNKNOWN` — unknown error.
  * `WRONG_EVENT_FORMAT` — incorrect notification type.
  * `DUPLICATED_EVENT` — duplicate notification.

_Enum:_ `UNKNOWN`, `WRONG_EVENT_FORMAT`, `DUPLICATED_EVENT`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationapierrortype)NotificationApiErrorType
Error type:
  * `UNKNOWN` — unknown error.
  * `WRONG_EVENT_FORMAT` — incorrect notification type.
  * `DUPLICATED_EVENT` — duplicate notification.

**Type** |  **Description**  
---|---  
[NotificationApiErrorType](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationapierrortype) |  _Enum:_ `UNKNOWN`, `WRONG_EVENT_FORMAT`, `DUPLICATED_EVENT`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#500-internal-server-error)500 Internal Server Error
If a technical error has occurred on your side, return the status `500`. [The store's API is not responding](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/#no-answer)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#body3)Body
application/json
```
{
    "error": {
        "type": "UNKNOWN",
        "message": "string"
    }
}

```

**Name** |  **Description**  
---|---  
error |  **Type:** [NotificationApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/reference/sendNotification#notificationapierrordto) Error when processing the notification.  
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Error messages](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/push-notifications/concepts/error-codes)
Next
[For 1C:Company](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/reference/en/modules/1c)
