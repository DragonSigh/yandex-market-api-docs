---
title: How to change product prices | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/assortment-change-prices
crawled_at: 2025-09-17T14:46:22.527268
---

How to change product prices
# How to change product prices
You can change the price that is valid in all stores, or the price for an individual store.
The method is available to you [POST v2/campaigns/{campaignId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/updatePrices) if there is an opportunity to set unique prices in individual stores in the seller's office on the Market. How to check it is in the method [POST v2/businesses/{businessId}/settings](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/businesses/getBusinessSettings) in the parameter `onlyDefaultPrice` the value is returned `false`.
Otherwise, use the price management method that applies in all stores., — [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateBusinessPrices).
Too sudden a price change will result in the product falling into the **quarantine**
Quarantine is necessary so that the product does not end up in the window with the wrong price due to a technical error.
The quarantine threshold can be set in the cabinet. Read about how to do this. [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/assortment/operations/prices.html#quarantine).
Price for all stores
The price for a separate store
Yandex MarketYour storeYandex MarketYour storeCalculation of Market service feesSubmitting new pricesOptional stepSubmitting VATopt​Checking if any products were placed in quarantinealt[Quarantine is not empty, and there are price errors][Quarantine is not empty, but all prices are correct]Product parametersPOST v2/tariffs/calculateOK: service fees for products with specified parameters.Updated pricesPOST v2/businesses/{businessId}/offer-prices/updatesValidates and either applies pricesor places the product in quarantine.OKVAT in the vat parameterPOST v2/campaigns/{campaignId}/offers/updateAppliesthe submitted VAT.OKPOST v2/businesses/{businessId}/price-quarantineOK: list of products in quarantine.Corrected pricesPOST v2/businesses/{businessId}/offer-prices/updatesValidatesand applies prices.OKPOST v2/businesses/{businessId}/price-quarantine/confirmRemoves productsfrom quarantine.OK
  1. To find out the cost of Yandex.Market services for specific products, pass their parameters in the request. [POST v2/tariffs/calculate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/tariffs/calculateTariffs).
  2. Send the new prices for all stores using a request [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateBusinessPrices).
[How to get the set prices](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/prices/getDefaultPrices)
  3. If necessary, pass the VAT parameter. `vat` in the request [POST v2/campaigns/{campaignId}/offers/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/updateCampaignOffers).
  4. Make sure that none of the products are quarantined using a request. [POST v2/businesses/{businessId}/price-quarantine](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/getBusinessQuarantineOffers).
  5. If the quarantine is not empty, check the prices of the goods. Incorrectly set prices for all stores can be corrected with a request. [POST v2/businesses/{businessId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateBusinessPrices).
  6. After only the correct prices remain in quarantine, confirm them with a request. [POST v2/businesses/{businessId}/price-quarantine/confirm](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/confirmBusinessPrices). If false alarms of quarantine occur frequently, consider changing its threshold by [Instructions](https://yandex.ru/support/marketplace/assortment/operations/prices.html#quarantine).


Yandex MarketYour storeYandex MarketYour storeCalculating Yandex Market service feesSubmitting new pricesChecking if any products were quarantinedalt[Quarantine is not empty, and there are price errors][Quarantine is not empty, but all prices are correct]Product parametersPOST v2/tariffs/calculateOK: service fees for products with specified parameters.Updated pricesPOST v2/campaigns/{campaignId}/offer-prices/updatesVerifies and either applies pricesor places the product in quarantine.OKPOST v2/businesses/{businessId}/price-quarantineOK: list of quarantined products.Corrected pricesPOST v2/businesses/{businessId}/offer-prices/updatesVerifiesand updates prices.OKPOST v2/businesses/{businessId}/price-quarantine/confirmRemoves productsfrom quarantine.OK
  1. To find out the cost of Yandex.Market services for specific products, pass their parameters in the request. [POST v2/tariffs/calculate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/tariffs/calculateTariffs).
  2. Send new prices for a specific store using a request [POST v2/campaigns/{campaignId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/updatePrices).
[How to get the set prices](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/getPricesByOfferIds)
  3. Make sure that none of the products are quarantined using a request. [POST v2/campaigns/{campaignId}/price-quarantine](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/getCampaignQuarantineOffers).
  4. If the quarantine is not empty, check the prices of the goods. Incorrectly set prices for a particular store can be corrected with a request. [POST v2/campaigns/{campaignId}/offer-prices/updates](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/updatePrices).
  5. After only the correct prices remain in quarantine, confirm them with a request. [POST v2/campaigns/{campaignId}/price-quarantine/confirm](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/confirmCampaignPrices). If false alarms of quarantine occur frequently, consider changing its threshold by [Instructions](https://yandex.ru/support/marketplace/assortment/operations/prices.html#quarantine).


Copied
### Was the article helpful?
YesNo
Previous
[Transfer of leftovers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks)
Next
[Stock management](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/promos)
