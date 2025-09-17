---
title: Stock management | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/promos
crawled_at: 2025-09-17T14:46:27.796889
---

Add products to the promotion
# Stock management
  * [Add products to the promotion](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos#add-goods)
  * [Change the price of products that have already been added to the promotion](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos#change-price)
  * [Remove products from the promotion](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos#delete-goods)
  * [View the results of participation in the promotion](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos#promo-results)


The Yandex.Market API allows you to receive information about Yandex. Market promotions and participate in them.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos#add-goods)Add products to the promotion
You already know the IDs of the list of stocks and products.
Skip the steps to get them.
Yandex MarketYour storeYandex MarketYour storeGetting the list of promotionsGetting the list of products eligible for the promotionAdding products to the promotionAccount IDPOST v2/businesses/{businessId}/promosOK: current and upcoming Market promotions.Promotion IDPOST v2/businesses/{businessId}/promos/offersOK: products eligible for the promotion.Promotion ID and products to addPOST v2/businesses/{businessId}/promos/offers/updateAddsproducts to the promotion.OK: result of adding products to the promotion.
  1. Get a list of Yandex.Market shares using a request [POST v2/businesses/{businessId}/promos](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/getPromos).
  2. Pass the stock ID in the request [POST v2/businesses/{businessId}/promos/offers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/getPromoOffers) to find out which products can participate in the promotion.
  3. Make a request [POST v2/businesses/{businessId}/promos/offers/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/updatePromoOffers), where pass the ID of the promotion and the products that need to be added.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos#change-price)Change the price of products that have already been added to the promotion
You already know the IDs of the list of stocks and products.
Skip the steps to get them.
Yandex MarketYour storeYandex MarketYour storeGetting the list of promotionsGetting the list of products added to the promotionUpdating prices for products in the promotionAccount IDPOST v2/businesses/{businessId}/promosOK: current and upcoming Market promotions.Promotion IDand statusType parameter with value MANUALLY_ADDEDPOST v2/businesses/{businessId}/promos/offersOK: products added to the promotion.Product SKUs and their new pricesPOST v2/businesses/{businessId}/promos/offers/updateUpdates pricesfor products in the promotion.OK: price update result.
  1. Get a list of Yandex.Market shares using a request [POST v2/businesses/{businessId}/promos](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/getPromos).
  2. Pass the promotion ID and the parameter `statusType` with the value `MANUALLY_ADDED` in the request [POST v2/businesses/{businessId}/promos/offers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/getPromoOffers) to find out which products have been added to the promotion.
  3. Send the SKU of the products and their new prices — request [POST v2/businesses/{businessId}/promos/offers/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/updatePromoOffers).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos#delete-goods)Remove products from the promotion
You already know the IDs of the list of stocks and products.
Skip the steps to get them.
Yandex MarketYour storeYandex MarketYour storeGet promotions listGet list of products added to promotionRemove products from promotionAccount IDPOST v2/businesses/{businessId}/promosOK: current and upcoming Market promotions.Promotion IDand statusType parameter with value MANUALLY_ADDEDPOST v2/businesses/{businessId}/promos/offersOK: products added to the promotion.deleteAllOffers parameter with value trueor product SKUs in offerIds parameterPOST v2/businesses/{businessId}/promos/offers/deleteRemovesproducts from promotion.OK: result of product removal.
  1. Get a list of Yandex.Market shares using a request [POST v2/businesses/{businessId}/promos](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/getPromos).
  2. Pass the promotion ID and the parameter `statusType` with the value `MANUALLY_ADDED` in the request [POST v2/businesses/{businessId}/promos/offers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/getPromoOffers) to find out which products have been added to the promotion.
  3. Make a request [POST v2/businesses/{businessId}/promos/offers/delete](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/promos/deletePromoOffers) to remove from the promotion:
     * All products are a parameter `deleteAllOffers` with the value `true`;
     * Some products are a parameter `offerIds`.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos#promo-results)View the results of participation in the promotion
You can download a report with all orders that contain products sold under the promotion. For information on how to receive reports, see [step-by-step instructions](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports).
Copied
### Was the article helpful?
YesNo
Previous
[Price changes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-change-prices)
Next
[FBS orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/fbs)
