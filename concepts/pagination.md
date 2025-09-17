---
title: Pagination in requests to the Yandex.Market API for sellers | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/pagination
crawled_at: 2025-09-17T14:42:05.944798
---

Pagination with the page ID
# Pagination in requests to the Yandex.Market API for sellers
  * [Pagination with the page ID](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/pagination#page-toke)
  * [Pagination with the page number](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/pagination#page)


Some queries do not return the result in its entirety, but page by page. To get the full result, run several consecutive queries. In each new query, pass the parameter with the next page of results.
Depending on which parameter needs to be passed, pagination can be of two types:
  * with the page ID, the parameter `page_token`;
  * with the page number — parameter `page`.


If both types of pagination are available in the method, use **page ID** (`page_token`), not her number.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/pagination#page-toke)Pagination with the page ID
Examples of methods:
  * [POST v2/businesses/{businessId}/offer-cards](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/content/getOfferCardsContentStatus)
  * [POST v2/campaigns/{campaignId}/offer-prices](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/assortment/getPricesByOfferIds)
  * [GET v2/campaigns/{campaignId}/returns](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getReturns)


To get the full result:
  1. Make a request where:
     * Don't pass it on `page_token`.
     * If desired, send `limit`. Then this parameter will need to be passed in each subsequent request.
The response will return the parameter `paging`.
  2. If in `paging` the parameter returned `nextPageToken` so, there is the next page of the result. Repeat the request, where pass the value `nextPageToken` in the parameter `page_token`.
Parameter value `nextPageToken`
This is not a page number, but a string that needs to be passed in the request.
If there is no parameter, then the last page is returned. Make more requests **no need**.
  3. Keep executing requests until it returns `nextPageToken`.


Some methods in the parameter `paging` They are returning `prevPageToken`
This is the ID of the previous results page.
To get the previous page, pass its ID in the parameter `page_token`. For the first page `prevPageToken` It doesn't come back.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/pagination#page)Pagination with the page number
Some of the methods with this type of pagination are already outdated
The rest will be marked obsolete in the future.
Examples of methods:
  * [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/campaigns/getCampaigns)
  * [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/orders/getOrders)
  * [GET v2/regions/{regionId}/children](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/regions/searchRegionChildren)


To get the full result:
  1. Make a request where:
     * Don't pass it on `page`.
     * If desired, send `pageSize`. Then this parameter will need to be passed in each subsequent request.
The response will return the parameter `pager` with the number of result pages `pagesCount`.
  2. If in `pagesCount` more than one page returned, repeat the requests — in the parameter `page` send the page numbers (`2`, `3` and to the last one).


Copied
### Was the article helpful?
YesNo
Previous
[Restrictions on requests](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits)
Next
[Query log](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/debug)
