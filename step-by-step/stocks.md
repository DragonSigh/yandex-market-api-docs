---
title: Transfer of balances via API | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/stocks
crawled_at: 2025-09-17T14:42:30.038467
---

What needs to be ready before you get started
# Transfer of balances via API
  * [What needs to be ready before you get started](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#before-you-start)
  * [How does the transfer of leftovers work?](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#details)
  * [Integration development](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#getting-it-done)
    * [How to check the functionality of the integration](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#check)
    * [What number should I send](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#count)
  * [How to transfer leftovers for a group of warehouses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#warehouse-group)


In order for the Market to receive up-to-date information about balances, use the method [PUT v2/campaigns/{campaignId}/offers/stocks](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/stocks/updateStocks).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#before-you-start)What needs to be ready before you get started
Before setting up order processing via the API, you need to add products to the Market and set up assortment updates. You don't have to do this via the API. Choose any method that is convenient for you. All the necessary instructions are available in [Yandex.Market Help](https://yandex.ru/support/marketplace/assortment/index.html).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#details)How does the transfer of leftovers work?
It is important for Yandex.Market to know how many items are left in the store's warehouse. Otherwise, it may turn out that the customer places an order and the product does not turn out to be there. The only exception is the FBY model, because the goods are stored in the Market's warehouse and he can count them himself.
To transfer the leftovers correctly, be sure to read [an article in the Help of the Market for sellers](https://yandex.ru/support/marketplace/assortment/operations/stocks.html). All the general rules for transferring balances apply to the API too.
Is it possible to use the API and other balance transfer methods at the same time?
Yes, you can transfer leftovers according to this instruction using the method [PUT v2/campaigns/{campaignId}/offers/stocks](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/stocks/updateStocks) and in the office via YML or through Excel files.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#getting-it-done)Integration development
Using a request [PUT v2/campaigns/{campaignId}/offers/stocks](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/stocks/updateStocks) You can transfer leftovers at any time.
Each entry includes:
  * Your SKU of the product for which you need to update the balances.
  * Date and time — the moment at which the new value is relevant.
  * The value of the leftovers itself.


###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#check)How to check the functionality of the integration
  1. Hide the items using [POST v2/campaigns/{campaignId}/hidden-offers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/addHiddenOffers).
  2. Make a request [PUT v2/campaigns/{campaignId}/offers/stocks](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/stocks/updateStocks) to transfer the leftovers.
  3. Resume showing hidden goods — [POST v2/campaigns/{campaignId}/hidden-offers/delete](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/deleteHiddenOffers).


###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#count)What number should I send
The remaining product is the number of units, **available for ordering on the Market**.
When a customer places an order, the number of available items decreases, so the leftovers do too. For example, if there were 20 and someone ordered 2 units, the remainder would be 18.
Both on-Market and off-market sales are taken into account
It doesn't matter where the product was purchased: on the Market or, for example, directly in an offline store. In any case, immediately reduce the remaining product.
For example:
**Event** |  **Changing balances**  
---|---  
10 units of new goods were brought to the warehouse |  0 → 10  
The buyer ordered 2 units on the Market |  10 → 8  
The supplier brought 10 more pieces. |  8 → 18  
Visitor _offline stores_ I bought 3 pieces |  18 → 15  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks#warehouse-group)How to transfer leftovers for a group of warehouses
Transfer leftovers only for **one of any warehouse**. The information for the other warehouses in this group will be updated automatically.
It is assumed that the offline store sells with **The same warehouse** , the same as the store on the Market.
### Was the article helpful?
YesNo
Previous
[Product Archive](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-archive)
Next
[Price changes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-change-prices)
