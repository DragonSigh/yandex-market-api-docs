---
title: Working with warehouses | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/warehouses
crawled_at: 2025-09-17T14:24:49.899065
---

Find out warehouse statuses
# Working with warehouses
  * [Find out warehouse statuses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/warehouses#status)
  * [Find out the groups of warehouses for transferring leftovers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/warehouses#group)
  * [Disable or enable storage](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/warehouses#update-status)


The Yandex.Market API allows you to get information about warehouses, as well as disable them to temporarily hide goods from the showcase, and turn them back on.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/warehouses#status)Find out warehouse statuses
Yandex MarketYour storeYandex MarketYour storeReceiving warehouse statusesCampaign IDsand components parameter with STATUS valuePOST v2/businesses/{businessId}/warehousesOK: status of each warehouse.
Make a request [POST v2/businesses/{businessId}/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/warehouses/getPagedWarehouses) where to specify:
  * campaign IDs — `campaignIds`;
  * The warehouse property is a parameter `components` with the value `STATUS`.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/warehouses#group)Find out the groups of warehouses for transferring leftovers
If the warehouses are grouped, you need to transfer the leftovers only for **any one** warehouse — information for the other warehouses in this group will be updated automatically. [What are warehouse groups and why are they needed?](https://yandex.ru/support/marketplace/ru/assortment/operations/stocks.html#unified-stocks)
Yandex MarketYour storeYandex MarketYour storeRetrieving warehouses grouped togetherCampaign IDsPOST v2/businesses/{businessId}/warehousesOK: warehouse information.
To find out which warehouses are grouped, get information about all warehouses. To do this, make a request [POST v2/businesses/{businessId}/warehouses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/warehouses/getPagedWarehouses) where to specify the campaign IDs — `campaignIds`. Parameter `components` You don't need to transmit it.
If the warehouse's response is:
  * There is no parameter `groupInfo` — he's not in the band. Transfer the leftovers by specifying the campaign ID of the store that is associated with the warehouse.
  * The parameter returned `groupInfo` — the warehouse is grouped together. Warehouses with the same name `id` in `WarehouseGroupInfoDTO` they belong to the same group. Transfer the leftovers by specifying the campaign ID of any store in this group.


[How to transfer leftovers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/stocks)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/warehouses#update-status)Disable or enable storage
Yandex MarketYour storeYandex MarketYour storeEnabling or disabling a warehouseParameter enabledPOST v2/campaigns/{campaignId}/warehouse/statusDisablesor enables the warehouse.OK: warehouse status.
If you want to temporarily remove goods from the showcase, disconnect the warehouse where they are located. To do this, make a request [POST v2/campaigns/{campaignId}/warehouse/status](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/warehouses/updateWarehouseStatus), where pass the parameter `enabled` with the value `false`. The goods will be hidden from the showcase in 15 minutes.
To enable the warehouse, make the same request, but the parameter `enabled` must take the value `true`. After switching on, the goods will return to the showcase in 15 minutes, and if the warehouse has been turned off for 30 days or longer — after 4 hours.
Copied
### Was the article helpful?
YesNo
Previous
[Chats with customers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/chats)
Next
[Overview of methods](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/overview/)
