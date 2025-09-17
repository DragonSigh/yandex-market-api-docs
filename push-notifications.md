---
title: Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/push-notifications
crawled_at: 2025-09-17T14:22:31.332848
---

  * [Enabling integration](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#how-to-start)
    * [Checking the integration](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#check)
  * [Response to the request](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#how-to-response)
    * [The store's API is not responding](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#no-answer)
  * [Notification Management](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#manage)


API notifications are not related to the push api, the old scheme of working with Yandex.Market.
# How to work with notifications
You can enable API notifications and Yandex.Market will send you a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/reference/sendNotification) with information about _events_ every time it happens.
This is an optional integration, you don't have to enable notifications. However, with their help, you will be able to quickly respond to changes in orders, non-purchases and refunds, as well as to requests for cancellation of the order.
The market exchanges data only with stores that operate over HTTPS using an SSL certificate. It must be signed by an official certification authority, a self-signed certificate will not work. Information about certification authorities can be found on the Internet.
Check each request against IP address ranges.
The security of your integration depends on this. This way you will make sure that the request came from Yandex.Market.
Ranges of IP addresses used by the Market:
  * _5.45.207.0/25_
  * _141.8.142.0/25_
  * _5.255.253.0/25_


##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#how-to-start)Enabling integration
![Screenshot of enabling integration](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/new-notification.png)
To receive notifications from Yandex.Market:
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **API notifications**.
  2. Click the button **Plug** or **Enable more notifications** if you have already created them.
  3. Specify the name of the notification. You will only need it to search for the notification in the list.
  4. Select whether you are setting up notifications for your merchant profile or store:
  
|  **Notifications are coming** |  **The role required to configure the notification** [What are the roles?](https://yandex.ru/support2/marketplace/ru/account/permissions/roles)  
---|---|---  
office |  for all cabinet stores |  cabinet owner or cabinet manager  
shop |  for a specific store |  any role other than a content manager  
  5. Select the types of notifications you want to receive:
**Notification** | **Comes for the cabinet** | **It comes for the store**  
---|---|---  
creating an order | ✔️ | ✔️  
changing the order | ✔️ | ✔️  
changing the order status | ✔️ | ✔️  
order cancellation | ✔️ | ✔️  
creating an order cancellation request | ✔️ | ✔️  
making a refund or non-purchase | ✔️ | ✔️  
changing the refund or non-purchase status | ✔️ | ✔️  
new review | ✔️ |   
new review comment | ✔️ |   
new chat with the buyer | ✔️ |   
new message in the chat | ✔️ |   
the beginning of the dispute | ✔️ |   
ending the dispute | ✔️ |   
If order-related notifications are configured for the cabinet, they are also sent for FBY orders.
  6. Enter the link where Yandex.Market will send notifications. Specify it in its entirety, including the HTTPS protocol.
  7. Click the button **Plug**. The created notifications will appear in the dashboard immediately, but they will start arriving. **within 2 minutes**.


###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#check)Checking the integration
To check the functionality of the integration, yandex.Market will send a request [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/reference/sendNotification) where there will be a verification notification in the body with the type `PING`.
Request body example
```
{
  "notificationType": "PING",
  "time": "2025-01-16T10:09:49.759084017Z"
}

```

Return the response with the code `200` and information about notification processing within 10 seconds. Integration will not be enabled if another code, incorrect or insufficient data is transmitted. [Possible errors](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/concepts/error-codes#shop-errors)
Example of the response body
```
{
  "version": "1.0.0",
  "name": "name",
  "time": "2025-01-16T10:09:49.759084017Z"
}

```

##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#how-to-response)Response to the request
The response time is 10 seconds.
  * If the request was correct, return the code `200` with information about notification processing. [Response body](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/reference/sendNotification#200-ok)
  * If the Market has sent an incorrect notification, return the code. `400` with a description of the error. The market will analyze such responses and refine the API on its part. [Response body](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/reference/sendNotification#400-bad-request)
  * If a technical error has occurred on your side, please return the code. `500`. [Response body](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/reference/sendNotification#500-internal-server-error)


Detailed information on requests and responses, including errors, can be viewed on the logs page on the tab **API notifications**. Read more about this in the section [Query log](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/concepts/debug).
[Possible errors](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/concepts/error-codes#shop-errors)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#no-answer)The store's API is not responding
If the store does not meet the ten-second timeout or the request [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/reference/sendNotification) returns an error except `400`, The Market repeats the requests:
  1. Every minute for the first hour.
  2. Every 15 minutes during the first day.
  3. Then once an hour.


If the store's API is unavailable within 14 days of sending the first notification, the store is disabled. **from integration** , but continues to host and sell products. Yandex.Market will cancel all notifications that it could not send before disconnecting, and will not send new ones.
To continue receiving notifications, connect them again. For more information on how to do this, see [Notification Management](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#manage).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/#manage)Notification Management
After changing the notification
The information in the dashboard will be updated immediately, but notifications will start coming or turn off. **within 2 minutes**.
![Screenshot of connected integrations](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/all-notifications.png)
To change
You can edit the name and types of notifications, as well as the link to send them. To do this:
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **API notifications**.
  2. Find the notification you need, tap the three dots next to it and select **Edit**.
  3. Change the required information.
  4. Click **Plug**.


Unplug
You can disable sending notifications without deleting them. To do this:
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **API notifications**.
  2. Find the notification you need, tap the three dots next to it and select **Unplug**.


Plug
To make the disabled notification work again:
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **API notifications**.
  2. Find the notification you need, tap the three dots next to it and select **Plug**.
  3. If notifications were disabled by Yandex.Market, you will receive a request. [POST notification](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/reference/sendNotification) where there will be a verification notification in the body with the type `PING`. Return the response with the code `200` and information about the notification processing within 10 seconds.


Duplicate settings
To avoid creating notifications for the store from scratch, duplicate the settings you have already created for another store:
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **API notifications**.
  2. Find the notification you need, tap the three dots next to it and select **Duplicate settings**.
  3. Specify the desired store.
  4. Click **Duplicate**.


Remove
To delete a notification:
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **API notifications**.
  2. Find the notification you need, tap the three dots next to it and select **Remove**.
  3. Confirm the deletion.


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

Notifications will also be sent for test orders.
Addresses from 5.45.207.0 to 5.45.207.127
Addresses from 141.8.142.0 to 141.8.142.127
Addresses from 5.255.253.0 to 5.255.253.127
Copied
### Was the article helpful?
YesNo
Previous
[Product model search](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/reference/models/searchModels)
Next
[Integration on Node.js Express](https://yandex.ru/dev/market/partner-api/doc/en/push-notifications/en/push-notifications/concepts/quick-start-notifications-node-express)
