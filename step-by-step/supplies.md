---
title: FBY-requests for the delivery of goods to the warehouse, export or disposal | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/supplies
crawled_at: 2025-09-17T14:44:56.061215
---

Get information about applications
# FBY-requests for the delivery of goods to the warehouse, export or disposal
  * [Get information about applications](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#get-requests)
    * [What are the types of applications?](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#request-types)
  * [Get a list of products in the application and information about them](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#get-items)
  * [Get the application documents](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#get-documents)
  * [It may be useful](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#read-more)


For information on how to create an application and deliver the goods to the warehouse, see [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/storage/shipment/).
The Yandex.Market API allows you to:
  * receive information about orders for supply, export or disposal and about the goods in the application;
  * download documents on request.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#get-requests)Get information about applications
Yandex MarketYour storeYandex MarketYour storeReceiving application informationCampaign IDPOST v2/campaigns/{campaignId}/supply-requestsOK: application information.
Make a request [POST v2/campaigns/{campaignId}/supply-requests](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/supply-requests/getSupplyRequests), where specify the campaign ID `campaignId` and the necessary parameters for filtering and sorting.
Application status `status` reflects its status at the time of the request
It can change.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#request-types)What are the types of applications?
  * Types of applications:
    * `SUPPLY` — delivery of goods to the warehouse;
    * `WITHDRAW` — export of goods from the warehouse;
    * `UTILIZATION ` — disposal of goods.
[Subtypes of applications](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/supply-requests/getSupplyRequests#supplyrequestsubtype)
  * Parent and child, if there was:
    * delivery to the storage warehouse;
    * _multi-delivery_ ;
    * additional delivery;
    * disposal or removal of rejected goods.
In this case, the parameters will be returned `parentLink` (link to the parent application) and `childrenLinks` (links to child applications).
  * Depending on the logistics:
    * For supplies that go directly to the storage warehouse. The parameter will be returned `targetLocation` — information about the storage warehouse or PVZ.
    * With goods that go through the transit warehouse. The parameter will also be returned `transitLocation` — information about the transit warehouse or PVZ.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#get-items)Get a list of products in the application and information about them
Yandex MarketYour storeYandex MarketYour storeReceiving product information in the requestCampaign and request IDPOST v2/campaigns/{campaignId}/supply-requests/itemsOK: product information in the request.
Make a request [POST v2/campaigns/{campaignId}/supply-requests/items](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/supply-requests/getSupplyRequestItems), where specify the campaign ID (`campaignId`) and applications (`requestId`).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#get-documents)Get the application documents
Yandex MarketYour storeYandex MarketYour storeReceiving application documentsCampaign and application IDPOST v2/campaigns/{campaignId}/supply-requests/documentsOK: application documents.
Make a request [POST v2/campaigns/{campaignId}/supply-requests/documents](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/supply-requests/getSupplyRequestDocuments), where specify the campaign ID (`campaignId`) and applications (`requestId`).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies#read-more)It may be useful
**Report or API method** |  **What information does it give**  
---|---  
[Turnover Report](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateGoodsTurnoverReport) |  How your products are sold from the Market's warehouses. Deliver goods that are running out to the warehouse on time, and pick up those that are being sold out slowly.  
[Report on the movement of goods](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateGoodsMovementReport) |  How many items have been delivered, ordered, returned by customers, moved to another warehouse, or taken out by you.  
[Warehouse balance report](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateStocksOnWarehousesReport) |  The remaining items in all Market warehouses, as well as how many items are available for order, how many defective items, etc.  
[Store Quality Index](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/ratings/getQualityRatings) |  The value of the store quality index and its components.  
Read about what it is in [Yandex.Market Help for sellers](https://yandex.ru/support/marketplace/ru/storage/shipment/application#create).
Copied
### Was the article helpful?
YesNo
Previous
[Business orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/business-info)
Next
[Non-purchases and refunds](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/returns)
