---
title: Overview of methods | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/overview
crawled_at: 2025-09-17T14:22:24.018403
---

Cabinet-level methods
# Overview of methods
  * [Cabinet-level methods](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#businesses)
  * [Methods at the store level](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#campaigns)
  * [Methods for getting reports](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#reports)
  * [Reference methods](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#common)
  * [How to get cabinet and campaign IDs](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#get-id)


##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#businesses)Cabinet-level methods
Some of the methods from [the list](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business) — for example, product catalog managers work at the level of **cabinet** regardless of which models are connected and used. [What is a cabinet?](https://yandex.ru/support/marketplace/account/introduction.html)
The cabinet ID is passed in the path parameters. — `businessId`. Example: `POST v2/businesses/{businessId}/settings`
[How to get the cabinet ID](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#get-id)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#campaigns)Methods at the store level
There are methods that work with individual **shops** inside the office. [What is a store on the Market?](https://yandex.ru/support/marketplace/account/add-shop.html)
To call them, you need a campaign ID. `campaignId`. Example: `GET v2/campaigns/{campaignId}/orders/{orderId}`
[How to get the campaign ID](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#get-id)
Some of these methods are listed in [the general list](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business) some work only for certain placement models:
  * [FBY](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fby)
  * [FBS](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/fbs)
  * [Express](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/express)
  * [DBS](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/dbs)


[Comparison of methods by models](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/comparison)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#reports)Methods for getting reports
Resource `reports` allows you to request and receive reports on your work on the Market. Example: `POST v2/reports/shows-sales/generate`
Depending on the type of report, you may need both `businessId`, so and `campaignId`. [How to get](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#get-id)
For example, to start generating a turnover report — [POST v2/reports/goods-turnover/generate](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/reports/generateGoodsTurnoverReport), the campaign ID is required — `campaignId`.
[Requests to reports](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business#otchety)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#common)Reference methods
No identifiers are required in queries that provide general information that is not specific to a particular business. `businessId` or`campaignId`.
**Shared resources** | **The information they return**  
---|---  
`auth` | Api Key Token information  
`categories` | Market categories  
`models` | product models  
`regions` | how the region is represented in the geobase of the Market  
`tariffs` | Yandex.Market rates  
`warehouses` | Market warehouses  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/#get-id)How to get cabinet and campaign IDs
To get the IDs `businessId` and `campaignId`, make a request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/reference/campaigns/getCampaigns). It returns all the IDs that the specified authorization token allows access to.
The campaign ID can also be found in the seller's account on the Market. Click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.


Copied
### Was the article helpful?
YesNo
Previous
[Warehouses](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/step-by-step/warehouses)
Next
[Common methods](https://yandex.ru/dev/market/partner-api/doc/en/overview/en/overview/business)
