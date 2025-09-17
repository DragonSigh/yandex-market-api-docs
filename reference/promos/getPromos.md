---
title: List of shares - Stocks | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/getPromos
crawled_at: 2025-09-17T14:23:16.629537
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#request)
    * [Path parameters](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#path-parameters)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body)
    * [MechanicsType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#mechanicstype)
    * [PromoParticipationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#promoparticipationtype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body1)
    * [GetPromosResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromosresultdto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype)
    * [GetPromoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromodto)
    * [GetPromoAssortmentInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromoassortmentinfodto)
    * [GetPromoBestsellerInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromobestsellerinfodto)
    * [GetPromoMechanicsInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromomechanicsinfodto)
    * [PromoPeriodDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#promoperioddto)
    * [ChannelType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#channeltype)
    * [GetPromoConstraintsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromoconstraintsdto)
    * [GetPromoPromocodeInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromopromocodeinfodto)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body7)


# Getting a list of shares
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/overview/business).**
Not yet available for Market Yandex Go sellers.
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/_auto/scopes_summary/pages/pricing_read-only)
  * promotion — [Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/_auto/scopes_summary/pages/promotion)
  * promotion:read-only — [View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/_auto/scopes_summary/pages/promotion_read-only)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Returns information about the Market's promotions. It does not return data about the shares that the seller created.
By default, promotions in which the seller participates or may participate are returned.
To get current or completed promotions, pass the parameter `participation`.
Types of shares that are returned in the response:
  * direct discount;
  * flash promotion;
  * discount by promo code.

**, Limit:** 1,000 requests per hour  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/businesses/{businessId}/promos

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#path-parameters)Path parameters
**Name** |  **Description**  
---|---  
businessId* |  **Type:** integer<int64> Cabinet ID. To find out, use the request [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/campaigns/getCampaigns). ℹ️ [What is a cabinet and a store on the Market?](https://yandex.ru/support/marketplace/account/introduction.html)   
_Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body)Body
application/json
```
{
    "participation": "PARTICIPATING_NOW",
    "mechanics": "DIRECT_DISCOUNT"
}

```

**Name** |  **Description**  
---|---  
mechanics |  **Type:** [MechanicsType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#mechanicstype) Filter by promotion type. All stock types are returned by default. _Enum:_ `DIRECT_DISCOUNT`, `BLUE_FLASH`, `MARKET_PROMOCODE`  
participation |  **Type:** [PromoParticipationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#promoparticipationtype) Which promotions will return:
  * `PARTICIPATING_NOW` — current and future promotions in which the seller participates or may participate.
  * `PARTICIPATED` — completed promotions in which the seller participated over the past year. If there were less than 15 of them in a year, the response will show the last 15 shares for all time.

_Enum:_ `PARTICIPATING_NOW`, `PARTICIPATED`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#mechanicstype)MechanicsType
Type of promotion:
  * `DIRECT_DISCOUNT` — direct discount.
  * `BLUE_FLASH` — flash promotion.
  * `MARKET_PROMOCODE` — discount by promo code.

**Type** |  **Description**  
---|---  
[MechanicsType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#mechanicstype) |  _Enum:_ `DIRECT_DISCOUNT`, `BLUE_FLASH`, `MARKET_PROMOCODE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#promoparticipationtype)PromoParticipationType
Which promotions will return:
  * `PARTICIPATING_NOW` — current and future promotions in which the seller participates or may participate.
  * `PARTICIPATED` — completed promotions in which the seller participated over the past year. If there were less than 15 of them in a year, the response will show the last 15 shares for all time.

**Type** |  **Description**  
---|---  
[PromoParticipationType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#promoparticipationtype) |  _Enum:_ `PARTICIPATING_NOW`, `PARTICIPATED`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#200-ok)200 OK
The list of Market shares.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "promos": [
            {
                "id": "string",
                "name": "string",
                "period": {
                    "dateTimeFrom": "2022-12-29T18:02:01Z",
                    "dateTimeTo": "2022-12-29T18:02:01Z"
                },
                "participating": false,
                "assortmentInfo": {
                    "activeOffers": 0,
                    "potentialOffers": 0,
                    "processing": false
                },
                "mechanicsInfo": {
                    "type": "DIRECT_DISCOUNT",
                    "promocodeInfo": {
                        "promocode": "string",
                        "discount": 0
                    }
                },
                "bestsellerInfo": {
                    "bestseller": false,
                    "entryDeadline": "2022-12-29T18:02:01Z",
                    "renewalEnabled": false
                },
                "channels": [
                    "PUSH"
                ],
                "constraints": {
                    "warehouseIds": [
                        0
                    ]
                }
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [GetPromosResultDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromosresultdto) Information about the Market's promotions.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromosresultdto)GetPromosResultDTO
Information about the Market's promotions.
**Name** |  **Description**  
---|---  
promos* |  **Type:** [GetPromoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromodto)[] Yandex. Market promotions.  
Information about the promotion.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromodto)GetPromoDTO
Information about the promotion.
**Name** |  **Description**  
---|---  
assortmentInfo* |  **Type:** [GetPromoAssortmentInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromoassortmentinfodto) Information about the products in the promotion.  
bestsellerInfo* |  **Type:** [GetPromoBestsellerInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromobestsellerinfodto) Information about the "Bestsellers of the Market" promotion.  
id* |  **Type:** string The ID of the promotion.  
mechanicsInfo* |  **Type:** [GetPromoMechanicsInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromomechanicsinfodto) Information about the type of promotion.  
name* |  **Type:** string The name of the promotion.  
participating* |  **Type:** boolean Whether or not the seller participates in this promotion. For current and future promotions, it is returned with the value `true` if there are products in the promotion that were added manually. If the products are not included in the promotion or are added to it automatically, the parameter is returned with the value `false`. For past promotions, it is always returned with the value `true`. Read about the automatic and manual addition of products to the promotion [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/marketing/promos/market/index).  
period* |  **Type:** [PromoPeriodDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#promoperioddto) The time of the promotion.  
channels |  **Type:** [ChannelType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#channeltype)[] A list of product promotion channels.  
Product promotion channels:
  * `PUSH` — push notification from the Yandex Market app.
  * `STRETCH_MAIN` — the top banner is a banner on the main page of Yandex Market.
  * `MAIN_PAGE_CAROUSEL` — a carousel of promotions on the main page of Yandex Market.
  * `PRODUCT_RETAIL_PAGE` — the product is on the retail occasion page.
  * `MAIN_PAGE_CAROUSEL_WEB` — a carousel of promotions on the main page of the web version of Yandex. Market.
  * `PRODUCT_SEPARATE_LANDING` — the product is on the landing page of the promotion.
  * `SUPER_SHELF_CATEGORY` — shelf in categories.
  * `CAROUSEL_RETAIL_PAGE` — a carousel on the retail outlet's landing page.
  * `POPUP_APPLICATION` — a pop-up window in the Yandex Market application.
  * `POST_TELEGRAM` — a post in the Telegram channel of Yandex Market.
  * `CPA` — advertising in the Yandex Market partner network.
  * `WEB_PERFORMANCE_DIRECT` — advertising in Yandex. Direct.
  * `APP_PERFORMANCE` — advertising on the AppStore and Google Play.
  * `BANNER_PICKUP_POINT` — a banner in the Market's PVZ.
  * `BLOGGER_PERFORMANCE` — advertising integration for bloggers.
  * `DIGITAL_CHANNEL_BANNER` — banner in digital channels and social networks VK, Odnoklassniki.
  * `YANDEX_ECOSYSTEM_CHANNELS` — advertising in other Yandex services: GO, Delivery, Food.
  * `PARTNERS_MAIN_BANNER` — banner on the main page mail.ru , auto.ru , ya.ru .
  * `OTHER` — other stuff.

_Enum:_ `PUSH`, `STRETCH_MAIN`, `MAIN_PAGE_CAROUSEL`, `PRODUCT_RETAIL_PAGE`, `MAIN_PAGE_CAROUSEL_WEB`, `PRODUCT_SEPARATE_LANDING`, `SUPER_SHELF_CATEGORY`, `CAROUSEL_RETAIL_PAGE`, `POPUP_APPLICATION`, `POST_TELEGRAM`, `CPA`, `WEB_PERFORMANCE_DIRECT`, `APP_PERFORMANCE`, `BANNER_PICKUP_POINT`, `BLOGGER_PERFORMANCE`, `DIGITAL_CHANNEL_BANNER`, `YANDEX_ECOSYSTEM_CHANNELS`, `PARTNERS_MAIN_BANNER`, `OTHER` _Min items:_ `1` _Unique items_  
constraints |  **Type:** [GetPromoConstraintsDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromoconstraintsdto) Restrictions on promotions.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromoassortmentinfodto)GetPromoAssortmentInfoDTO
Information about the products in the promotion.
**Name** |  **Description**  
---|---  
activeOffers* |  **Type:** integer<int32> The number of products that participate or participated in the promotion. Products that were added automatically are not counted. Read about the automatic and manual addition of products to the promotion [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/marketing/promos/market/index).  
potentialOffers |  **Type:** integer<int32> The number of available products in the promotion. The parameter is returned only for current and future promotions.  
processing |  **Type:** boolean Are there any changes in the product range that have not yet been applied? Saving changes takes some time. The parameter is returned only for current and future promotions.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromobestsellerinfodto)GetPromoBestsellerInfoDTO
Information about the "Bestsellers of the Market" promotion.
**Name** |  **Description**  
---|---  
bestseller* |  **Type:** boolean Is the promotion a "Market Bestseller"? Read more about this promotion [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/marketing/promos/market/bestsellers).  
entryDeadline |  **Type:** string<date-time> By what date can I add an item to the "Bestsellers of the Market" promotion? The parameter is returned only for current and future Bestsellers Market promotions.  
renewalEnabled |  **Type:** boolean Whether the automatic transfer of the assortment between the "Bestsellers of the Market" promotions is enabled. Read about how it works. [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/ru/marketing/promos/market/bestsellers#next). The parameter is returned only for current and future Bestsellers Market promotions.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromomechanicsinfodto)GetPromoMechanicsInfoDTO
Information about the type of promotion.
**Name** |  **Description**  
---|---  
type* |  **Type:** [MechanicsType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#mechanicstype) Type of promotion:
  * `DIRECT_DISCOUNT` — direct discount.
  * `BLUE_FLASH` — flash promotion.
  * `MARKET_PROMOCODE` — discount by promo code.

_Enum:_ `DIRECT_DISCOUNT`, `BLUE_FLASH`, `MARKET_PROMOCODE`  
promocodeInfo |  **Type:** [GetPromoPromocodeInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromopromocodeinfodto) Information for the type `MARKET_PROMOCODE`. The parameter is filled in only for this type of promotion.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#promoperioddto)PromoPeriodDTO
The time of the promotion.
**Name** |  **Description**  
---|---  
dateTimeFrom* |  **Type:** string<date-time> The date and time of the start of the promotion.  
dateTimeTo* |  **Type:** string<date-time> The date and time of the end of the promotion.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#channeltype)ChannelType
Product promotion channels:
  * `PUSH` — push notification from the Yandex Market app.
  * `STRETCH_MAIN` — the top banner is a banner on the main page of Yandex Market.
  * `MAIN_PAGE_CAROUSEL` — a carousel of promotions on the main page of Yandex Market.
  * `PRODUCT_RETAIL_PAGE` — the product is on the retail occasion page.
  * `MAIN_PAGE_CAROUSEL_WEB` — a carousel of promotions on the main page of the web version of Yandex. Market.
  * `PRODUCT_SEPARATE_LANDING` — the product is on the landing page of the promotion.
  * `SUPER_SHELF_CATEGORY` — shelf in categories.
  * `CAROUSEL_RETAIL_PAGE` — a carousel on the retail outlet's landing page.
  * `POPUP_APPLICATION` — a pop-up window in the Yandex Market application.
  * `POST_TELEGRAM` — a post in the Telegram channel of Yandex Market.
  * `CPA` — advertising in the Yandex Market partner network.
  * `WEB_PERFORMANCE_DIRECT` — advertising in Yandex. Direct.
  * `APP_PERFORMANCE` — advertising on the AppStore and Google Play.
  * `BANNER_PICKUP_POINT` — a banner in the Market's PVZ.
  * `BLOGGER_PERFORMANCE` — advertising integration for bloggers.
  * `DIGITAL_CHANNEL_BANNER` — banner in digital channels and social networks VK, Odnoklassniki.
  * `YANDEX_ECOSYSTEM_CHANNELS` — advertising in other Yandex services: GO, Delivery, Food.
  * `PARTNERS_MAIN_BANNER` — banner on the main page mail.ru , auto.ru , ya.ru .
  * `OTHER` — other stuff.

**Type** |  **Description**  
---|---  
[ChannelType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#channeltype) |  _Enum:_ `PUSH`, `STRETCH_MAIN`, `MAIN_PAGE_CAROUSEL`, `PRODUCT_RETAIL_PAGE`, `MAIN_PAGE_CAROUSEL_WEB`, `PRODUCT_SEPARATE_LANDING`, `SUPER_SHELF_CATEGORY`, `CAROUSEL_RETAIL_PAGE`, `POPUP_APPLICATION`, `POST_TELEGRAM`, `CPA`, `WEB_PERFORMANCE_DIRECT`, `APP_PERFORMANCE`, `BANNER_PICKUP_POINT`, `BLOGGER_PERFORMANCE`, `DIGITAL_CHANNEL_BANNER`, `YANDEX_ECOSYSTEM_CHANNELS`, `PARTNERS_MAIN_BANNER`, `OTHER`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromoconstraintsdto)GetPromoConstraintsDTO
Restrictions on promotions.
**Name** |  **Description**  
---|---  
warehouseIds |  **Type:** integer<int64>[] Ids of warehouses for which the promotion is valid. Goods stored in other warehouses will not be sold under the promotion. The parameter is returned only if there is a stock restriction in the terms of the promotion.   
_Min items:_ `1` _Unique items_  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#getpromopromocodeinfodto)GetPromoPromocodeInfoDTO
Information for the type `MARKET_PROMOCODE`.
The parameter is filled in only for this type of promotion.
**Name** |  **Description**  
---|---  
discount* |  **Type:** integer<int32> The discount percentage for the promo code.  
promocode* |  **Type:** string The promo code.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body2)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body3)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body4)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body5)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body6)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#500-internal-server-error)500 Internal Server Error
Internal error in Yandex. Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#body7)Body
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
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromos#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Path parameters
businessId*:
Body{ "participation": "PARTICIPATING_NOW", "mechanics": "DIRECT_DISCOUNT" }
Send
No longer supported, please use an alternative and newer version.
Copied
### Was the article helpful?
YesNo
Previous
[Removal from quarantine for the price in the store](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/assortment/confirmCampaignPrices)
Next
[List of products in the promotion](https://yandex.ru/dev/market/partner-api/doc/en/reference/promos/en/reference/promos/getPromoOffers)
