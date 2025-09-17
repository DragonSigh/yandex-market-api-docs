---
title: Multiple points of sale - Information about points of sale | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/getOutlets
crawled_at: 2025-09-17T14:34:43.858407
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#path-parameters)
    * [Query parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#query-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body)
    * [FullOutletDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#fulloutletdto)
    * [FlippingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#flippingpagerdto)
    * [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#scrollingpagerdto)
    * [OutletAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletaddressdto)
    * [OutletType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outlettype)
    * [OutletWorkingScheduleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletworkingscheduledto)
    * [OutletDeliveryRuleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletdeliveryruledto)
    * [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#regiondto)
    * [OutletStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletstatustype)
    * [OutletVisibilityType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletvisibilitytype)
    * [OutletWorkingScheduleItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletworkingscheduleitemdto)
    * [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#regiontype)
    * [DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#dayofweektype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body6)


# Information about multiple points of sale
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/overview/dbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/_auto/scopes_summary/pages/settings-management)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Retrieves the list of the store's points of sale.
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/outlets

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#query-parameters)Query parameters
**Name** |  **Description**  
---|---  
limit |  **Type:** integer<int32> The number of values per page.   
_Min value:_ `1`   
Example: `20`  
page_token |  **Type:** string ID of the results page. If the parameter is omitted, the first page is returned. We recommend transmitting the value of the output parameter `nextPageToken`, received during the last request. If set `page_token` and the request has parameters `page` and `pageSize` they are ignored.   
Example: `eyBuZXh0SWQ6IDIzNDIgfQ==`  
regionId ⦸ |  **Type:** integer<int64> Instead, use `region_id`.  
region_id |  **Type:** integer<int64> ID of the region. If you set the ID of the parent region at any level, the output data will display the points of sale of all child regions. You can get the region ID using the method [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/regions/searchRegionsByName).  
shop_outlet_code |  **Type:** string The ID of the point of sale assigned by the store.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#200-ok)200 OK
Information about points of sale.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body)Body
application/json
```
{
    "outlets": [
        {
            "name": "string",
            "type": "DEPOT",
            "coords": "string",
            "isMain": false,
            "shopOutletCode": "string",
            "visibility": "HIDDEN",
            "address": {
                "regionId": 0,
                "street": "string",
                "number": "string",
                "building": "string",
                "estate": "string",
                "block": "string",
                "additional": "string",
                "km": 0,
                "city": "string"
            },
            "phones": [
                "string"
            ],
            "workingSchedule": {
                "workInHoliday": false,
                "scheduleItems": [
                    {
                        "startDay": "MONDAY",
                        "endDay": "MONDAY",
                        "startTime": "09:59",
                        "endTime": "23:59"
                    }
                ]
            },
            "deliveryRules": [
                {
                    "minDeliveryDays": 0,
                    "maxDeliveryDays": 0,
                    "deliveryServiceId": 0,
                    "orderBefore": 0,
                    "priceFreePickup": 0,
                    "unspecifiedDeliveryInterval": false
                }
            ],
            "storagePeriod": 0,
            "id": 0,
            "status": "AT_MODERATION",
            "region": {
                "id": 0,
                "name": "string",
                "type": "OTHER"
            },
            "shopOutletId": "string",
            "workingTime": "string",
            "moderationReason": "string"
        }
    ],
    "paging": {
        "nextPageToken": "string",
        "prevPageToken": "string"
    },
    "pager": {
        "total": 0,
        "from": 0,
        "to": 0,
        "currentPage": 0,
        "pagesCount": 0,
        "pageSize": 0
    }
}

```

**Name** |  **Description**  
---|---  
outlets* |  **Type:** [FullOutletDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#fulloutletdto)[] Information about points of sale.  
Information about the point of sale.  
Information about the point of sale.  
pager |  **Type:** [FlippingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#flippingpagerdto) A model for pagination.  
paging |  **Type:** [ScrollingPagerDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#scrollingpagerdto) Information about the result pages.  
The ID of the next page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#fulloutletdto)FullOutletDTO
Information about the point of sale.
**Name** |  **Description**  
---|---  
address* |  **Type:** [OutletAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletaddressdto) The address of the point of sale.  
id* |  **Type:** integer<int64> The ID of the point of sale assigned by Yandex.Market.  
name* |  **Type:** string The name of the point of sale.  
phones* |  **Type:** string[] The phone numbers of the point of sale. Send in the format: `+7 (999) 999-99-99`.   
_Min length:_ `1` _Min items:_ `1` _Unique items_  
type* |  **Type:** [OutletType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outlettype) The type of point of sale. Possible values:
  * `DEPOT` — order pick-up point.
  * `MIXED` — a mixed type of point of sale (sales floor and order pick-up point).
  * `RETAIL` — retail point of sale (sales floor).
  * `NOT_DEFINED` — unknown type of point of sale. An error occurred when determining the type.

_Enum:_ `DEPOT`, `MIXED`, `RETAIL`, `NOT_DEFINED`  
workingSchedule* |  **Type:** [OutletWorkingScheduleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletworkingscheduledto) The list of operating modes of the point of sale.  
coords |  **Type:** string Coordinates of the point of sale. Format: longitude, latitude. Delimiters: comma and/or space. For example, `20.4522144, 54.7104264`. If no parameter is passed, the coordinates will be determined by the values of the parameters nested in `address`.  
deliveryRules |  **Type:** [OutletDeliveryRuleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletdeliveryruledto)[] Information about the terms of delivery for this point of sale. Required parameter if the parameter `type=DEPOT` or `type=MIXED`.   
Information about the terms of delivery for this point of sale. _Min items:_ `1`  
isMain |  **Type:** boolean Indicates the main point of sale. Possible values:
  * `false` — non-primary point of sale.
  * `true` — the main point of sale.

  
moderationReason |  **Type:** string The moderation status.  
region |  **Type:** [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#regiondto) The delivery region.  
shopOutletCode |  **Type:** string The ID of the point of sale assigned by the store.  
shopOutletId ⦸ |  **Type:** string Instead, use `shopOutletCode`. The ID of the point of sale set by the store.  
status |  **Type:** [OutletStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletstatustype) The status of the point of sale. Possible values:
  * `AT_MODERATION` — it's being checked.
  * `FAILED` — failed verification and was rejected by the moderator.
  * `MODERATED` — tested and approved.
  * `NONMODERATED` — a new point, needs to be checked.
  * `UNKNOWN` — the status is not specified. An error occurred when determining the status.

_Enum:_ `AT_MODERATION`, `FAILED`, `MODERATED`, `NONMODERATED`, `UNKNOWN`  
storagePeriod |  **Type:** integer<int64> The storage period of the order at its own order pick-up point. It is calculated in days.  
visibility |  **Type:** [OutletVisibilityType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletvisibilitytype) The status of the point of sale. Possible values:
  * `HIDDEN` — the point of sale is disabled.
  * `VISIBLE` — the point of sale is enabled.
  * `UNKNOWN` — unknown condition of the point of sale. An error occurred when determining the status.

_Enum:_ `HIDDEN`, `VISIBLE`, `UNKNOWN`  
workingTime ⦸ |  **Type:** string Instead, use `workingSchedule`. Working hours.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#flippingpagerdto)FlippingPagerDTO
A model for pagination.
**Name** |  **Description**  
---|---  
currentPage |  **Type:** integer<int32> The current page.  
from |  **Type:** integer<int32> The initial number of the found element on the page.  
pageSize |  **Type:** integer<int32> Page size.  
pagesCount |  **Type:** integer<int32> The total number of pages.  
to |  **Type:** integer<int32> The final number of the found element on the page.  
total |  **Type:** integer<int32> How many items were found in total.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#scrollingpagerdto)ScrollingPagerDTO
Information about the result pages.
**Name** |  **Description**  
---|---  
nextPageToken |  **Type:** string ID of the next results page.  
prevPageToken |  **Type:** string ID of the previous results page.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletaddressdto)OutletAddressDTO
The address of the point of sale.
**Name** |  **Description**  
---|---  
regionId* |  **Type:** integer<int64> ID of the region. You can get the ID using a request [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/regions/searchRegionsByName). Types of regions when creating and editing points of sale Specify only the following types of regions `TOWN` (city), `CITY` (large city) and `REPUBLIC_AREA` (district of the federal subject). The type of the region is specified in the output parameters `type` requests [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/regions/searchRegionsByName) and [GET v2/regions/{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/regions/searchRegionsById).  
additional |  **Type:** string Additional information.  
block |  **Type:** string Building number. _Max length:_ `16`  
building |  **Type:** string Building number. _Max length:_ `16`  
city ⦸ |  **Type:** string In the responses, cities and towns are returned in the parameter `regionId`. _Max length:_ `200`  
estate |  **Type:** string Ownership number. _Max length:_ `16`  
km |  **Type:** integer<int32> The ordinal number of the kilometer of the road where the point of sale is located, if there is no street.  
number |  **Type:** string The house number. _Max length:_ `256`  
street |  **Type:** string Street. _Max length:_ `512`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outlettype)OutletType
The type of point of sale.
Possible values:
  * `DEPOT` — order pick-up point.
  * `MIXED` — a mixed type of point of sale (sales floor and order pick-up point).
  * `RETAIL` — retail point of sale (sales floor).
  * `NOT_DEFINED` — unknown type of point of sale. An error occurred when determining the type.

**Type** |  **Description**  
---|---  
[OutletType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outlettype) |  _Enum:_ `DEPOT`, `MIXED`, `RETAIL`, `NOT_DEFINED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletworkingscheduledto)OutletWorkingScheduleDTO
The list of operating modes of the point of sale.
**Name** |  **Description**  
---|---  
scheduleItems* |  **Type:** [OutletWorkingScheduleItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletworkingscheduleitemdto)[] A list of the point of sale's opening hours.   
The opening hours of the point of sale. _Min items:_ `1`  
workInHoliday |  **Type:** boolean Indicates whether the point of sale is open on public holidays. Possible values:
  * `false` — the point of sale is closed on public holidays.
  * `true` — the point of sale is open on public holidays.

  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletdeliveryruledto)OutletDeliveryRuleDTO
Information about the terms of delivery for this point of sale.
**Name** |  **Description**  
---|---  
deliveryServiceId |  **Type:** integer<int64> ID of the product delivery service to the point of sale. Information about the delivery service can be obtained by requesting [GET delivery/services](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/orders/getDeliveryServices).  
maxDeliveryDays |  **Type:** integer<int32> The maximum delivery time for goods to the point of sale. It is specified in business days. Minimum value: `0` — delivery on the day of the order. Maximum value: `60`. Acceptable delivery time (the difference between `minDeliveryDays` and `maxDeliveryDays`) depend on the region. For delivery in your region, the difference should not exceed two days. For example, if `minDeliveryDays` is equal to 1, then for `maxDeliveryDays` values from 1 to 3 are allowed. For delivery to other regions:
  * If `minDeliveryDays` up to 18 days, the difference should not exceed four days. For example, if `minDeliveryDays` is equal to 10, then for `maxDeliveryDays` values from 10 to 14 are allowed.
  * If `minDeliveryDays` more than 18 days, the difference should not be more than twice. For example, if `minDeliveryDays` is equal to 21, then for `maxDeliveryDays` values from 21 to 42 are allowed.

Required parameter if `type="DEPOT"` or `type="MIXED"`. Mutually exclusive with the parameter `unspecifiedDeliveryInterval`. _Min value:_ `0` _Max value:_ `60`  
minDeliveryDays |  **Type:** integer<int32> The minimum delivery time for goods to the point of sale. It is specified in business days. Minimum value: `0` — delivery on the day of the order. Maximum value: `60`. Acceptable delivery time (the difference between `minDeliveryDays` and `maxDeliveryDays`) depend on the region. For delivery in your region, the difference should not exceed two days. For example, if `minDeliveryDays` is equal to 1, then for `maxDeliveryDays` values from 1 to 3 are allowed. For delivery to other regions:
  * If `minDeliveryDays` up to 18 days, the difference should not exceed four days. For example, if `minDeliveryDays` is equal to 10, then for `maxDeliveryDays` values from 10 to 14 are allowed.
  * If `minDeliveryDays` more than 18 days, the difference should not be more than twice. For example, if `minDeliveryDays` is equal to 21, then for `maxDeliveryDays` values from 21 to 42 are allowed.

Required parameter if `type="DEPOT"` or `type="MIXED"`. Mutually exclusive with the parameter `unspecifiedDeliveryInterval`. _Min value:_ `0` _Max value:_ `60`  
orderBefore |  **Type:** integer<int32> The hour before which the customer needs to place the order so that it can be delivered to the point of sale on time from `minDeliveryDays` before `maxDeliveryDays`. If the customer places the order after the specified hour, it will be delivered on time from `minDeliveryDays` + 1 business day before `maxDeliveryDays` + 1 working day. Default value: `24`. _Min value:_ `0` _Max value:_ `24`  
priceFreePickup |  **Type:** number The price of the product, starting from which the free pickup of the product from the point of sale is valid.  
unspecifiedDeliveryInterval |  **Type:** boolean Indicates the delivery of goods to the point of sale on order. This flag is set if:
  * the exact delivery time to the point of sale is unknown in advance (for example, if the store collects several orders for shipment to the point or locality).
  * all products are made or delivered to order.

Possible values:
  * `true` — the goods are delivered to the point of sale on order.

The parameter is specified only with the value `true`. Mutually exclusive with parameters `minDeliveryDays` and `maxDeliveryDays`.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#regiondto)RegionDTO
The delivery region.
**Name** |  **Description**  
---|---  
id* |  **Type:** integer<int64> ID of the region.  
name* |  **Type:** string The name of the region.  
type* |  **Type:** [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#regiontype) The type of region. Possible values:
  * `CITY_DISTRICT` — the area of the city.
  * `CITY` — a large city.
  * `CONTINENT` — the continent.
  * `COUNTRY_DISTRICT` — area.
  * `COUNTRY` — country.
  * `REGION` — region.
  * `REPUBLIC_AREA` — district of the subject of the federation.
  * `REPUBLIC` — the subject of the Federation.
  * `SUBWAY_STATION` — the metro station.
  * `VILLAGE` — the city.
  * `OTHER` — unknown region.

_Enum:_ `OTHER`, `CONTINENT`, `REGION`, `COUNTRY`, `COUNTRY_DISTRICT`, `REPUBLIC`, `CITY`, `VILLAGE`, `CITY_DISTRICT`, `SUBWAY_STATION`, `REPUBLIC_AREA`  
parent |  **Type:** [RegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#regiondto) The delivery region.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletstatustype)OutletStatusType
The status of the point of sale.
Possible values:
  * `AT_MODERATION` — it's being checked.
  * `FAILED` — failed verification and was rejected by the moderator.
  * `MODERATED` — tested and approved.
  * `NONMODERATED` — a new point, needs to be checked.
  * `UNKNOWN` — the status is not specified. An error occurred when determining the status.

**Type** |  **Description**  
---|---  
[OutletStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletstatustype) |  _Enum:_ `AT_MODERATION`, `FAILED`, `MODERATED`, `NONMODERATED`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletvisibilitytype)OutletVisibilityType
The status of the point of sale.
Possible values:
  * `HIDDEN` — the point of sale is disabled.
  * `VISIBLE` — the point of sale is enabled.
  * `UNKNOWN` — unknown condition of the point of sale. An error occurred when determining the status.

**Type** |  **Description**  
---|---  
[OutletVisibilityType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletvisibilitytype) |  _Enum:_ `HIDDEN`, `VISIBLE`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#outletworkingscheduleitemdto)OutletWorkingScheduleItemDTO
The opening hours of the point of sale.
**Name** |  **Description**  
---|---  
endDay* |  **Type:** [DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#dayofweektype) Day of the week:
  * `MONDAY` — Monday.
  * `TUESDAY` "Tuesday."
  * `WEDNESDAY` — Wednesday.
  * `THURSDAY` — Thursday.
  * `FRIDAY` — Friday.
  * `SATURDAY` "Saturday."
  * `SUNDAY` "Sunday."

_Enum:_ `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`  
endTime* |  **Type:** string The point of sale is open until the specified hour. Format: `HH:MM`. _Example:_ `23:59` _Pattern:_ `^([0-1][0-9]<code>&#124;</code>2[0-3]):[0-5][0-9]$`  
startDay* |  **Type:** [DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#dayofweektype) Day of the week:
  * `MONDAY` — Monday.
  * `TUESDAY` "Tuesday."
  * `WEDNESDAY` — Wednesday.
  * `THURSDAY` — Thursday.
  * `FRIDAY` — It's Friday.
  * `SATURDAY` "Saturday."
  * `SUNDAY` — Sunday.

_Enum:_ `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`  
startTime* |  **Type:** string The point of sale is open starting from the specified hour. Format: `HH:MM`. _Example:_ `09:59` _Pattern:_ `^([0-1][0-9]<code>&#124;</code>2[0-3]):[0-5][0-9]$`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#regiontype)RegionType
The type of region.
Possible values:
  * `CITY_DISTRICT` — the area of the city.
  * `CITY` — a large city.
  * `CONTINENT` — the continent.
  * `COUNTRY_DISTRICT` — area.
  * `COUNTRY` — country.
  * `REGION` — region.
  * `REPUBLIC_AREA` — district of the subject of the federation.
  * `REPUBLIC` — the subject of the Federation.
  * `SUBWAY_STATION` — the metro station.
  * `VILLAGE` — the city.
  * `OTHER` — unknown region.

**Type** |  **Description**  
---|---  
[RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#regiontype) |  _Enum:_ `OTHER`, `CONTINENT`, `REGION`, `COUNTRY`, `COUNTRY_DISTRICT`, `REPUBLIC`, `CITY`, `VILLAGE`, `CITY_DISTRICT`, `SUBWAY_STATION`, `REPUBLIC_AREA`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#dayofweektype)DayOfWeekType
Day of the week:
  * `MONDAY` — Monday.
  * `TUESDAY` "Tuesday."
  * `WEDNESDAY` — Wednesday.
  * `THURSDAY` — Thursday.
  * `FRIDAY` — It's Friday.
  * `SATURDAY` "Saturday."
  * `SUNDAY` — Sunday.

**Type** |  **Description**  
---|---  
[DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#dayofweektype) |  _Enum:_ `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body1)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body2)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body3)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body4)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body5)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#body6)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Query parameters
page_token:
limit:
region_id:
shop_outlet_code:
regionId:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[One point of sale](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlet)
Next
[Creation](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet)
