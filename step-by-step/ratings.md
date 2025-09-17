---
title: Quality index | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/ratings
crawled_at: 2025-09-17T14:46:56.303633
---

Quality index
# Quality index
You can use the API to find out:
  * the value of the store quality index and its components;
  * information about orders that affected the quality index.


Read more about the quality index. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/quality/score/).
Yandex MarketYour storeYandex MarketYour storeRetrieving the quality index valueRetrieving orders that affected the quality indexCampaign IDsPOST v2/businesses/{businessId}/ratings/qualityOK: store quality index value and its components.Campaign IDPOST v2/campaigns/{campaignId}/ratings/quality/detailsOK: list of orders that affected the quality index.
  1. To find out the value of the quality index, pass the campaign IDs in the request. [POST v2/businesses/{businessId}/ratings/quality](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/ratings/getQualityRatings).
  2. To get information about orders that affected the store's quality index, use a request [POST v2/campaigns/{campaignId}/ratings/quality/details](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/ratings/getQualityRatingDetails).


### Was the article helpful?
YesNo
Previous
[Sales Boost](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost)
Next
[Chats with customers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats)
