---
title: Working with a sales boost | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/boost
crawled_at: 2025-09-17T14:46:44.331111
---

How to get the recommended rates
# Working with a sales boost
  * [How to get the recommended rates](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#recommendations)
  * [How to create a campaign](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#new-boost)
  * [How to get the set rates](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#get-bids)
  * [How to change campaign data](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#change-boost)
    * [Update bids](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#change-bids)
    * [Add new products to the campaign](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#add-goods)
    * [Remove products from the campaign](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#delete-goods)
  * [How to get a sales boost report](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#get-report)


Through the API, you can launch a sales boost — create and enable a single campaign for all business account stores, add products to it and set bids for them. You can manage such a campaign — add, update, delete, and receive bids for products — only through the API.
You can make other changes to the campaign created via the API in the dashboard:
  * Disable or enable the campaign.
  * Change its name.
  * Disable or enable the pricing strategy. Read more about the pricing strategy in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/marketing/campaigns.html#price-strategy).


You will not be able to manage the campaigns that you created in your account via the API.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#recommendations)How to get the recommended rates
To find out the recommended rates, make a request [POST v2/businesses/{businessId}/bids/recommendations](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/bids/getBidsRecommendations).
Yandex MarketYour storeYandex MarketYour storeReceiving recommended bidsPOST v2/businesses/{businessId}/bids/recommendationsCompiles a listof recommended bids.OK: list of recommended bids.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#new-boost)How to create a campaign
Send information about the products (SKUs) and their bids using a request [PUT v2/businesses/{businessId}/bids](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/bids/putBidsForBusiness). A new campaign is created the first time a request is used, or when it is repeated if you deleted a previously created campaign through the API in your account.
Yandex MarketYour storeYandex MarketYour storeTransferring product information and their bidsPUT v2/businesses/{businessId}/bidsCreates a campaign,adds products to itwith specified bids,enables pricing strategy for them,and starts promotion.OK
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#get-bids)How to get the set rates
To find out the values of the bids set via the API, make a request [POST v2/businesses/{businessId}/bids/info](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/bids/getBidsInfoForBusiness).
You will not be able to get information on campaigns created in the cabinet.
The response returns only the values of the rates that you set through the request. [PUT v2/businesses/{businessId}/bids](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/bids/putBidsForBusiness).
Yandex MarketYour storeYandex MarketYour storeRetrieving set bid valuesPOST v2/businesses/{businessId}/bids/infoOK: list of set bids.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#change-boost)How to change campaign data
You can update bids, add or remove products from a campaign created via the API using a request. [PUT v2/businesses/{businessId}/bids](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/bids/putBidsForBusiness). You can perform several actions in a single request, for example, add new products to the campaign and delete old ones.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#change-bids)Update bids
To update the bids for the products in the created campaign, make a request [PUT v2/businesses/{businessId}/bids](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/bids/putBidsForBusiness), where pass the new bid values.
Yandex MarketYour storeYandex MarketYour storeUpdating bidsProduct and bid informationPUT v2/businesses/{businessId}/bidsUpdates bid informationfor products in the campaign.OK
###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#add-goods)Add new products to the campaign
To add new products to the campaign, make a request [PUT v2/businesses/{businessId}/bids](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/bids/putBidsForBusiness), where you can send information about new products (SKUs) and their bids.
Yandex MarketYour storeYandex MarketYour storeAdding new productsInformation about new products and their bidsPUT v2/businesses/{businessId}/bidsAdds information about new productsand their bids to the campaign.OK
###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#delete-goods)Remove products from the campaign
To stop the promotion of certain products, make a request [PUT v2/businesses/{businessId}/bids](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/bids/putBidsForBusiness), where pass the zero bid in the field `bid` for those products that need to be removed from the campaign.
Yandex MarketYour storeYandex MarketYour storeRemoving products from the campaignProduct information,to be removed from the campaignPUT v2/businesses/{businessId}/bidsStops promotionand removes specified productsfrom the campaign.OK
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/boost#get-report)How to get a sales boost report
For information on how to receive reports, see [step-by-step instructions](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports).
Copied
### Was the article helpful?
YesNo
Previous
[Product Reviews](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback)
Next
[Quality index](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/ratings)
