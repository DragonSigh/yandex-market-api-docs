---
title: Chats with customers | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/chats
crawled_at: 2025-09-17T14:42:36.546076
---

How to start a chat
# Chats with customers
  * [How to start a chat](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats#create)
  * [How to reply to a message](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats#answer)
  * [How to check if there are new chats or messages](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats#check)


The Yandex.Market API allows you to communicate with your customers in chats.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats#create)How to start a chat
Yandex MarketYour storeYandex MarketYour storeCheck if there is a chat with the buyerCreate a chat if it doesn't existSend a messageSend a fileChat type and order or return IDPOST v2/businesses/{businessId}/chatsChecks if there is a chatwith the buyer.OK: chat information if it exists.POST v2/businesses/{businessId}/chats/newCreates a chatwith the user.OK: chat ID.MessagePOST v2/businesses/{businessId}/chats/messageSends the message.OKFilePOST v2/businesses/{businessId}/chats/file/sendSends the file.OK
  1. Check if there is a chat with the buyer. — [POST v2/businesses/{businessId}/chats](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChats). In the request, specify the chat type and the ID of the order or refund to which it relates.
If there is no chat, create it using a request. [POST v2/businesses/{businessId}/chats/new](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/createChat).
How to start a test chat
In the debugging interface, create a test order, and then click **Create a test chat** or make a request [POST v2/businesses/{businessId}/chats/new](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/createChat).
[Learn more about working with test orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/concepts/sandbox)
Please note:
     * such a chat can only be created for an order, not a refund;
     * There are no customer responses in the test chats.
  2. Send a message with a request [POST v2/businesses/{businessId}/chats/message](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/sendMessageToChat). If you need to send a file to the buyer, for example, an additional photo of the product, use a request. [POST v2/businesses/{businessId}/chats/file/send](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/sendFileToChat).
  3. Check new messages from the buyer. — [POST v2/businesses/{businessId}/chats/history](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChatHistory). Use a filter based on the ID of the last message in the request to receive only new messages and not re-upload those that you already have.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats#answer)How to reply to a message
Yandex MarketYour storeYandex MarketYour storeSearch for chats requiring a response from the storeRetrieving message historySending a messageSending a file"statuses": ["WAITING_FOR_PARTNER"]POST v2/businesses/{businessId}/chatsCompiles a list of chats.OK: list of chats.Chat IDPOST v2/businesses/{businessId}/chats/historyCompiles a list of messages.OK: chat messages.MessagePOST v2/businesses/{businessId}/chats/messageSends the message.OKFilePOST v2/businesses/{businessId}/chats/file/sendSends the file.OK
  1. Find the chats where your answer is needed. To do this, make a request [POST v2/businesses/{businessId}/chats](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChats). In the request, send the status "Store response needed" ("statuses": ["WAITING_FOR_PARTNER"]).
  2. To get the chat message history, use a request [POST v2/businesses/{businessId}/chats/history](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChatHistory), where pass the chat ID.
  3. Send a message using a request [POST v2/businesses/{businessId}/chats/message](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/sendMessageToChat). If you need to send a file to the buyer, for example, an additional photo of the product, use a request. [POST v2/businesses/{businessId}/chats/file/send](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/sendFileToChat).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats#check)How to check if there are new chats or messages
Enable API notifications
Yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/reference/sendNotification) when a new chat or message appears.
[How to work with notifications](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/push-notifications/)
To receive chats or messages, use the following methods:
  * [GET v2/businesses/{businessId}/chat](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChat) — for one chat;
  * [POST v2/businesses/{businessId}/chats](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChats) — for the chat list;
  * [GET v2/businesses/{businessId}/chats/message](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChatMessage) — for the message;
  * [POST v2/businesses/{businessId}/chats/history](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/chats/getChatHistory) — for the message history.


### Was the article helpful?
YesNo
Previous
[Quality index](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/ratings)
Next
[Warehouses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/warehouses)
