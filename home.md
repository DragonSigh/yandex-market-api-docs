---
title: Yandex.Market API for sellers | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en
crawled_at: 2025-09-17T14:21:54.117586
---

How to set up integration
# Yandex.Market API for sellers
The yandex.Market API helps sellers manage product ranges and prices, process orders, update balances, and solve many other tasks.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/#start)How to set up integration
  1. Read the page [Creating and using an API Key token](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/api-key). It tells you how to log in to access resources.
  2. Read it [instructions for connecting the OpenAPI specification](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/openapi).
  3. **For sellers of the Yandex Go Market:** Read the instructions [How to work with the Yandex.Market API](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers).
  4. See the section [Step-by-step instructions](https://yandex.ru/dev/market/partner-api/doc/en/en/step-by-step/) — if there are instructions for your task, start with it.
  5. Open [overview of API methods](https://yandex.ru/dev/market/partner-api/doc/en/en/overview/) for the desired model and select the ones that are needed to solve the problem.
  6. Read the detailed description of each method and implement the integration.
  7. If necessary, enable API notifications and yandex.Market will send you a request with information about _events_ when it happens.
This is an optional integration. However, with the help of notifications, you will be able to quickly respond to changes in orders, non-purchases and refunds, as well as to requests for cancellation of the order.
[How to enable API notifications](https://yandex.ru/dev/market/partner-api/doc/en/en/push-notifications/#how-to-start)


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
### Was the article helpful?
YesNo
