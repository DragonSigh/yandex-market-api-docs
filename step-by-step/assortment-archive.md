---
title: Managing goods in the archive | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/assortment-archive
crawled_at: 2025-09-17T14:43:59.087554
---

Managing goods in the archive
# Managing goods in the archive
You can archive products so that they disappear from the storefronts in all stores.
You cannot send an item stored in a Market warehouse to the archive.
First, such goods need to be sold or exported.
  1. To archive products, use a request [POST v2/businesses/{businessId}/offer-mappings/archive](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/addOffersToArchive). If the items could not be archived, they will be returned in the request response.
  2. To view the products in the archive, use a filter. `archived` in the request [POST v2/businesses/{businessId}/offer-mappings](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/getOfferMappings).
  3. To restore an item from the archive, use a request [POST v2/businesses/{businessId}/offer-mappings/unarchive](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/deleteOffersFromArchive).


Also read the instructions
  * [Adding and editing products](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods)
  * [Changing categorical characteristics](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change)
  * [Yandex.Market recommendations for cards](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/recommendations)


Copied
### Was the article helpful?
YesNo
Previous
[Recommendations for cards](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/recommendations)
Next
[Transfer of leftovers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks)
