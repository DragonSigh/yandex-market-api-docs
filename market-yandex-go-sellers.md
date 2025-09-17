---
title: How to work with the Yandex.Market API for Market Yandex Go sellers | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/market-yandex-go-sellers
crawled_at: 2025-09-17T14:22:10.199103
---

Calling methods
# How to work with the Yandex.Market API for Market Yandex Go sellers
  * [Calling methods](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#method-call)
  * [Methods](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#methods)
  * [Product name and description](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#name-and-description)
  * [Product code](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#commodity-code)
  * [Prices of goods](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#price)
  * [Marking codes](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#cis)
  * [Shortcuts](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#labels)


In the documentation, we describe the interaction of Market sellers with the Yandex.Market API for sellers. On this page, we have collected the specifics of the work for sellers from Uzbekistan who place goods on the Yandex Go Market.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#method-call)Calling methods
In queries, instead of `.ru` use `.net`. Format:
```
<http_method> https://api.partner.market.yandex.net/<resource>.<format>?<parameters>

```

[Learn more about calling methods](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/method-call)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#methods)Methods
If the method is not available for Yandex Go Market sellers, this is indicated in the description.
Example: [POST v2/businesses/{businessId}/promos](https://yandex.ru/dev/market/partner-api/doc/en/en/reference/promos/getPromos)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#name-and-description)Product name and description
When you add products to the catalog using the method [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/en/reference/business-assortment/updateOfferMappings), specify the parameter values `name` and `description` in Russian. In order for them to be displayed in a different language on the showcase, make the request again, where specify:
  * the language in the parameter `language`;
  * parameter values `name` and `description` in the specified language.


You do not need to retransmit the remaining product characteristics.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#commodity-code)Product code
Send the product codes and their type. `IKPU_CODE` in the parameters `code` and `type` — method [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/en/reference/business-assortment/updateOfferMappings).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#price)Prices of goods
Methods for transmitting product prices:
  * [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/en/reference/business-assortment/updateOfferMappings) — adding products and transmitting prices;
  * [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/en/reference/business-assortment/updateBusinessPrices) — transfer prices for all stores;
  * [POST v2/campaigns/{campaignId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/en/reference/assortment/updatePrices) — transfer prices in a specific store.


Specify prices in the national currency in the parameter `value` and the currency itself in `currencyId`. When receiving information, for example about orders, prices are returned in the currency that was set when adding the product.
You do not need to transfer VAT (parameter `vat`).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#cis)Marking codes
In the method [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/en/reference/orders/setOrderBoxLayout) send the product labeling codes in the system `cis`.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/market-yandex-go-sellers#labels)Shortcuts
Other shortcuts are available for Market Yandex Go sellers:
The label `A9_HORIZONTALLY`
![An image of a horizontal label in A9 format for Market Yandex Go sellers](https://yandex.ru/dev/market/partner-api/doc/en/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A9-horizontally-uz.png)
The label `A9`
![An image of an A9 vertical label for Market Yandex Go sellers](https://yandex.ru/dev/market/partner-api/doc/en/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A9-uz.png)
The label `A7`
![An image of an A7 format label for Market Yandex Go sellers](https://yandex.ru/dev/market/partner-api/doc/en/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/labels/label-A7-uz.png)
[Methods for working with labels](https://yandex.ru/dev/market/partner-api/doc/en/en/overview/comparison#yarlyki-fbs-i-dbs)
Copied
### Was the article helpful?
YesNo
Previous
[The OpenAPI Specification](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/openapi)
Next
[Step-by-step instructions](https://yandex.ru/dev/market/partner-api/doc/en/en/step-by-step/)
