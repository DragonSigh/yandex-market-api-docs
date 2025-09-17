---
title: Store Settings - Offices and shops | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/getCampaignSettings
crawled_at: 2025-09-17T14:29:01.729816
---

Request
  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#path-parameters)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body)
    * [CampaignSettingsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsdto)
    * [CampaignSettingsLocalRegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingslocalregiondto)
    * [CampaignSettingsDeliveryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsdeliverydto)
    * [CampaignSettingsScheduleSourceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsschedulesourcetype)
    * [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#regiontype)
    * [CampaignSettingsScheduleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsscheduledto)
    * [CampaignSettingsTimePeriodDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingstimeperioddto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body1)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apierrordto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body2)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body3)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body4)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body5)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body6)


# Store Settings
Info
Console
**The method is available for models:[FBY](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/overview/fby), [FBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/overview/fbs), [Express](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/overview/express) and [DBS](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/overview/dbs).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * inventory-and-order-processing — [Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/inventory-and-order-processing)
  * inventory-and-order-processing:read-only — [View order information](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only)
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/pricing_read-only)
  * offers-and-cards-management — [Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/offers-and-cards-management)
  * offers-and-cards-management:read-only — [View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/promotion_read-only)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/finance-and-accounting)
  * communication — [Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/communication)
  * settings-management — [Store settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/settings-management)
  * supplies-management:read-only — [View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/_auto/scopes_summary/pages/supplies-management_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about the settings of the store whose ID is specified in the request.
**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#request)Request
GET
```
https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/settings

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
campaignId* |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store's ID instead, which is indicated in the seller's account on the Market next to the store's name and in some reports.   
_Min value:_ `1`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#200-ok)200 OK
Store settings.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body)Body
application/json
```
{
    "settings": {
        "countryRegion": 0,
        "shopName": "string",
        "showInContext": false,
        "showInPremium": false,
        "useOpenStat": false,
        "localRegion": {
            "id": 0,
            "name": "string",
            "type": "OTHER",
            "deliveryOptionsSource": "WEB",
            "delivery": {
                "schedule": {
                    "availableOnHolidays": false,
                    "customHolidays": [
                        "23-09-2022"
                    ],
                    "customWorkingDays": [
                        "23-09-2022"
                    ],
                    "period": {
                        "fromDate": "23-09-2022",
                        "toDate": "23-09-2022"
                    },
                    "totalHolidays": [
                        "23-09-2022"
                    ],
                    "weeklyHolidays": [
                        0
                    ]
                }
            }
        }
    }
}

```

**Name** |  **Description**  
---|---  
settings |  **Type:** [CampaignSettingsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsdto) Store settings.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsdto)CampaignSettingsDTO
Store settings.
**Name** |  **Description**  
---|---  
countryRegion |  **Type:** integer<int64> ID of the region where the store is located.  
localRegion |  **Type:** [CampaignSettingsLocalRegionDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingslocalregiondto) Information about your store's region.  
shopName |  **Type:** string The name of the store on Yandex Market. If the name is missing, the parameter value is output — `null`.  
showInContext ⦸ |  **Type:** boolean Indicates whether the store is located on the websites of Yandex Distribution partners. Possible values:
  * `false` — the store is not hosted on the websites of Yandex Distribution partners.
  * `true` — the store is hosted on the websites of Yandex Distribution partners.

  
showInPremium ⦸ |  **Type:** boolean Indicates whether the store's offers are displayed in the block above the search results (special placement). Possible values:
  * `false` — offers are not shown in the special placement section.
  * `true` — offers are shown in the special placement section.

  
useOpenStat ⦸ |  **Type:** boolean Indicates the use of external Internet statistics. Possible values:
  * `false` — external Internet statistics are not used.
  * `true` — external internet statistics are used.

  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingslocalregiondto)CampaignSettingsLocalRegionDTO
Information about your store's region.
**Name** |  **Description**  
---|---  
delivery |  **Type:** [CampaignSettingsDeliveryDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsdeliverydto) Information about delivery in your store's region.  
deliveryOptionsSource |  **Type:** [CampaignSettingsScheduleSourceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsschedulesourcetype) The source of information about the delivery service's schedule. Possible values:
  * `WEB` — the information is obtained from the settings of the merchant's account on the Market.
  * `YML` — the information is obtained from the price list of the store.

_Enum:_ `WEB`, `YML`  
id |  **Type:** integer<int64> ID of the region.  
name |  **Type:** string The name of the region.  
type |  **Type:** [RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#regiontype) The type of region. Possible values:
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
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsdeliverydto)CampaignSettingsDeliveryDTO
Information about delivery in your store's region.
**Name** |  **Description**  
---|---  
schedule |  **Type:** [CampaignSettingsScheduleDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsscheduledto) The delivery service's schedule in your region.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsschedulesourcetype)CampaignSettingsScheduleSourceType
The source of information about the delivery service's schedule. Possible values:
  * `WEB` — the information is obtained from the settings of the merchant's account on the Market.
  * `YML` — the information is obtained from the price list of the store.

**Type** |  **Description**  
---|---  
[CampaignSettingsScheduleSourceType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsschedulesourcetype) |  _Enum:_ `WEB`, `YML`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#regiontype)RegionType
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
[RegionType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#regiontype) |  _Enum:_ `OTHER`, `CONTINENT`, `REGION`, `COUNTRY`, `COUNTRY_DISTRICT`, `REPUBLIC`, `CITY`, `VILLAGE`, `CITY_DISTRICT`, `SUBWAY_STATION`, `REPUBLIC_AREA`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingsscheduledto)CampaignSettingsScheduleDTO
The delivery service's schedule in your region.
**Name** |  **Description**  
---|---  
customHolidays* |  **Type:** string<date-dd-MM-yyyy>[] A list of days when the delivery service is closed. The store's days are indicated in the seller's office on the Market.  
Date format: `DD-MM-YYYY`. _Example:_ `23-09-2022` _Unique items_  
customWorkingDays* |  **Type:** string<date-dd-MM-yyyy>[] A list of weekends and holidays on which the delivery service operates. The store's days are indicated in the seller's office on the Market.  
Date format: `DD-MM-YYYY`. _Example:_ `23-09-2022` _Unique items_  
totalHolidays* |  **Type:** string<date-dd-MM-yyyy>[] The final list of non-working days of the delivery service. The list is calculated taking into account weekends, non-working days and public holidays. The store indicates information about them in the seller's account on the Market.  
Date format: `DD-MM-YYYY`. _Example:_ `23-09-2022` _Unique items_  
weeklyHolidays* |  **Type:** integer<int32>[] A list of days off and public holidays.  
The number of the day of the week. Possible values:
  * `1` — Monday.
  * `2` "Tuesday."
  * `3` — Wednesday.
  * `4` — Thursday.
  * `5` — It's Friday.
  * `6` "Saturday."
  * `7` — Sunday.

For the JSON format, the day number is output as a number. _Min value:_ `1` _Max value:_ `7` _Unique items_  
availableOnHolidays |  **Type:** boolean Indicates that the delivery service is open on public holidays. Possible values.
  * `false` — The delivery service is closed on public holidays.
  * `true` — the delivery service is open on public holidays.

  
period |  **Type:** [CampaignSettingsTimePeriodDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingstimeperioddto) The period for which the final list of non-working days of the delivery service is calculated.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#campaignsettingstimeperioddto)CampaignSettingsTimePeriodDTO
The period for which the final list of non-working days of the delivery service is calculated.
**Name** |  **Description**  
---|---  
fromDate |  **Type:** string<date-dd-MM-yyyy> Date format: `DD-MM-YYYY`. _Example:_ `23-09-2022`  
toDate |  **Type:** string<date-dd-MM-yyyy> Date format: `DD-MM-YYYY`. _Example:_ `23-09-2022`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body1)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#500-internal-server-error)500 Internal Server Error
Internal error of Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/campaigns/getCampaignSettings#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
campaignId*:
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Cabinet Settings](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/businesses/getBusinessSettings)
Next
[The category tree](https://yandex.ru/dev/market/partner-api/doc/en/reference/campaigns/en/reference/categories/getCategoriesTree)
