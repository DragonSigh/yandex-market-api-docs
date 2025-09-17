---
title: Yandex.Market recommendations for cards | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/recommendations
crawled_at: 2025-09-17T14:43:51.913340
---

Yandex.Market recommendations for cards
# Yandex.Market recommendations for cards
Sometimes in response to [POST v2/businesses/{businessId}/offer-cards](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/getOfferCardsContentStatus) you will receive **recommendations** by filling out the cards in the field `recommendations`.
See the type of recommendation you received in the field `recommendations` → `type`. Find this type in the documentation and see which product fields relate to this type of recommendation:
Main product parameters
Categorical characteristics of the product
  1. See the documentation for the meaning of the recommendation and which parameter needs to be changed or filled in.
  2. Edit the parameter using a request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateOfferMappings).


  1. See the documentation for the meaning of the recommendation.
  2. Make a request [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/getCategoryContentParameters).
  3. Select the characteristics from the response that are in the array `recommendationTypes` there is the right type. For example, if you received a recommendation like `MAIN`, you need characteristics marked `MAIN` in `recommendationTypes`.
  4. Send the values of the characteristics using a request [POST v2/businesses/{businessId}/offer-cards/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/updateOfferContent).


Also read the instructions
  * [Adding and editing products](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods)
  * [Changing categorical characteristics](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change)
  * [Managing goods in the archive](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-archive)


Copied
### Was the article helpful?
YesNo
Previous
[Changing categorical characteristics](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change)
Next
[Product Archive](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-archive)
