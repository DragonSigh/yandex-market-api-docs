---
title: Creation - Point of sale management | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/createOutlet
crawled_at: 2025-09-17T14:34:50.770413
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body)
    * [OutletAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletaddressdto)
    * [OutletType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outlettype)
    * [OutletWorkingScheduleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletworkingscheduledto)
    * [OutletDeliveryRuleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletdeliveryruledto)
    * [OutletVisibilityType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletvisibilitytype)
    * [OutletWorkingScheduleItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletworkingscheduleitemdto)
    * [DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#dayofweektype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body1)
    * [OutletResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletresponsedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#400-bad-request)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apierrordto)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body6)


# Creating a point of sale
Info
Console
**The method is available for the[DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/overview/dbs) model.**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/_auto/scopes_summary/pages/settings-management)
  * all-methods — Full account management


Creates a store's point of sale on the Market.
**, Limit:** 100,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/outlets

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports.   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body)Body
application/json
```
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
    "storagePeriod": 0
}

```

**Name** |  **Description**  
---|---  
address* |  **Type:** [OutletAddressDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletaddressdto) The address of the point of sale.  
name* |  **Type:** string The name of the point of sale.  
phones* |  **Type:** string[] The phone numbers of the point of sale. Send in the format: `+7 (999) 999-99-99`.   
_Min length:_ `1` _Min items:_ `1` _Unique items_  
type* |  **Type:** [OutletType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outlettype) The type of point of sale. Possible values:
  * `DEPOT` — order pick-up point.
  * `MIXED` — a mixed type of point of sale (sales floor and order pick-up point).
  * `RETAIL` — retail point of sale (sales floor).
  * `NOT_DEFINED` — unknown type of point of sale. An error occurred when determining the type.

_Enum:_ `DEPOT`, `MIXED`, `RETAIL`, `NOT_DEFINED`  
workingSchedule* |  **Type:** [OutletWorkingScheduleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletworkingscheduledto) The list of operating modes of the point of sale.  
coords |  **Type:** string Coordinates of the point of sale. Format: longitude, latitude. Delimiters: comma and/or space. For example, `20.4522144, 54.7104264`. If no parameter is passed, the coordinates will be determined by the values of the parameters nested in `address`.  
deliveryRules |  **Type:** [OutletDeliveryRuleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletdeliveryruledto)[] Information about the terms of delivery for this point of sale. Required parameter if the parameter `type=DEPOT` or `type=MIXED`.   
Information about the terms of delivery for this point of sale. _Min items:_ `1`  
isMain |  **Type:** boolean Indicates the main point of sale. Possible values:
  * `false` — non-primary point of sale.
  * `true` — the main point of sale.

  
shopOutletCode |  **Type:** string The ID of the point of sale assigned by the store.  
storagePeriod |  **Type:** integer<int64> The storage period of the order at its own order pick-up point. It is calculated in days.  
visibility |  **Type:** [OutletVisibilityType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletvisibilitytype) The status of the point of sale. Possible values:
  * `HIDDEN` — the point of sale is disabled.
  * `VISIBLE` — the point of sale is enabled.
  * `UNKNOWN` — unknown condition of the point of sale. An error occurred when determining the status.

_Enum:_ `HIDDEN`, `VISIBLE`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletaddressdto)OutletAddressDTO
The address of the point of sale.
**Name** |  **Description**  
---|---  
regionId* |  **Type:** integer<int64> ID of the region. You can get the ID using a request [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/regions/searchRegionsByName). Types of regions when creating and editing points of sale Specify only the following types of regions `TOWN` (city), `CITY` (large city) and `REPUBLIC_AREA` (district of the subject of the federation). The type of the region is specified in the output parameters `type` requests [GET v2/regions](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/regions/searchRegionsByName) and [GET v2/regions/{regionId}](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/regions/searchRegionsById).  
additional |  **Type:** string Additional information.  
block |  **Type:** string Building number. _Max length:_ `16`  
building |  **Type:** string Building number. _Max length:_ `16`  
city ⦸ |  **Type:** string In the responses, cities and towns are returned in the parameter `regionId`. _Max length:_ `200`  
estate |  **Type:** string Ownership number. _Max length:_ `16`  
km |  **Type:** integer<int32> The ordinal number of the kilometer of the road where the point of sale is located, if there is no street.  
number |  **Type:** string The house number. _Max length:_ `256`  
street |  **Type:** string Street. _Max length:_ `512`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outlettype)OutletType
The type of point of sale.
Possible values:
  * `DEPOT` — order pick-up point.
  * `MIXED` — a mixed type of point of sale (sales floor and order pick-up point).
  * `RETAIL` — retail point of sale (sales floor).
  * `NOT_DEFINED` — unknown type of point of sale. An error occurred when determining the type.

**Type** |  **Description**  
---|---  
[OutletType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outlettype) |  _Enum:_ `DEPOT`, `MIXED`, `RETAIL`, `NOT_DEFINED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletworkingscheduledto)OutletWorkingScheduleDTO
The list of operating modes of the point of sale.
**Name** |  **Description**  
---|---  
scheduleItems* |  **Type:** [OutletWorkingScheduleItemDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletworkingscheduleitemdto)[] A list of the point of sale's opening hours.   
The opening hours of the point of sale. _Min items:_ `1`  
workInHoliday |  **Type:** boolean Indicates whether the point of sale is open on public holidays. Possible values:
  * `false` — the point of sale is closed on public holidays.
  * `true` — the point of sale is open on public holidays.

  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletdeliveryruledto)OutletDeliveryRuleDTO
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
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletvisibilitytype)OutletVisibilityType
The status of the point of sale.
Possible values:
  * `HIDDEN` — the point of sale is disabled.
  * `VISIBLE` — the point of sale is enabled.
  * `UNKNOWN` — unknown condition of the point of sale. An error occurred when determining the status.

**Type** |  **Description**  
---|---  
[OutletVisibilityType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletvisibilitytype) |  _Enum:_ `HIDDEN`, `VISIBLE`, `UNKNOWN`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletworkingscheduleitemdto)OutletWorkingScheduleItemDTO
The opening hours of the point of sale.
**Name** |  **Description**  
---|---  
endDay* |  **Type:** [DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#dayofweektype) Day of the week:
  * `MONDAY` — Monday.
  * `TUESDAY` "Tuesday."
  * `WEDNESDAY` — Wednesday.
  * `THURSDAY` — Thursday.
  * `FRIDAY` — It's Friday.
  * `SATURDAY` "Saturday."
  * `SUNDAY` "Sunday."

_Enum:_ `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`  
endTime* |  **Type:** string The point of sale is open until the specified hour. Format: `HH:MM`. _Example:_ `23:59` _Pattern:_ `^([0-1][0-9]<code>&#124;</code>2[0-3]):[0-5][0-9]$`  
startDay* |  **Type:** [DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#dayofweektype) Day of the week:
  * `MONDAY` — Monday.
  * `TUESDAY` "Tuesday."
  * `WEDNESDAY` — Wednesday.
  * `THURSDAY` — Thursday.
  * `FRIDAY` — It's Friday.
  * `SATURDAY` "Saturday."
  * `SUNDAY` — Sunday.

_Enum:_ `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`  
startTime* |  **Type:** string The point of sale is open starting from the specified hour. Format: `HH:MM`. _Example:_ `09:59` _Pattern:_ `^([0-1][0-9]<code>&#124;</code>2[0-3]):[0-5][0-9]$`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#dayofweektype)DayOfWeekType
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
[DayOfWeekType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#dayofweektype) |  _Enum:_ `MONDAY`, `TUESDAY`, `WEDNESDAY`, `THURSDAY`, `FRIDAY`, `SATURDAY`, `SUNDAY`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#200-ok)200 OK
Information about the created point of sale.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "id": 0
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [OutletResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletresponsedto) The result of the query execution. Output if `status="OK"`.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#outletresponsedto)OutletResponseDTO
The result of the query execution. Output if `status="OK"`.
**Name** |  **Description**  
---|---  
id |  **Type:** integer<int64> The ID of the point of sale assigned by Yandex.Market.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#400-bad-request)400 Bad Request
**Description** | **Explanation** | **Solution methods**  
---|---|---  
**datediff-is-to-big-local** | For delivery in your region, the difference between the maximum and minimum delivery time should not exceed two days. | Make sure that the difference between `maxDeliveryDays` and `minDeliveryDays` not more than two days.  
**datediff-is-to-big-remote** | For delivery to other regions, the difference between the maximum and minimum delivery time should not exceed four days. | Make sure that the difference between `maxDeliveryDays` and `minDeliveryDays` not more than four days.  
**datediff-is-to-big-long-period** | When delivering to other regions where the minimum delivery time is more than 18 days, the difference between the maximum and minimum delivery time should not exceed the minimum time. | Make sure that the difference between `maxDeliveryDays` and `minDeliveryDays` does not exceed `minDeliveryDays`.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/createOutlet#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Body{ "name": "string", "type": "DEPOT", "coords": "string", "isMain": false, "shopOutletCode": "string", "visibility": "HIDDEN", "address": { "regionId": 0, "street": "string", "number": "string", "building": "string", "estate": "string", "block": "string", "additional": "string", "km": 0, "city": "string" }, "phones": [ "string" ], "workingSchedule": { "workInHoliday": false, "scheduleItems": [ { "startDay": "MONDAY", "endDay": "MONDAY", "startTime": "09:59", "endTime": "23:59" } ] }, "deliveryRules": [ { "minDeliveryDays": 0, "maxDeliveryDays": 0, "deliveryServiceId": 0, "orderBefore": 0, "priceFreePickup": 0, "unspecifiedDeliveryInterval": false } ], "storagePeriod": 0 }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Multiple points of sale](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/getOutlets)
Next
[Change](https://yandex.ru/dev/market/partner-api/doc/en/reference/outlets/en/reference/outlets/updateOutlet)
