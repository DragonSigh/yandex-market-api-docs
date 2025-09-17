---
title: Processing orders from legal entities | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/business-info
crawled_at: 2025-09-17T14:43:11.257788
---

Processing orders from legal entities
# Processing orders from legal entities
  * [How to determine that an order is from a legal entity](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/business-info#business-buyer)
  * [How to get customer information](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/business-info#buyer-info)
  * [How to get information about documents](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/business-info#documents-info)


The specifics of working with such orders are in the requests [PUT v2/campaigns/{campaignId}/orders/{orderId}/identifiers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/provideOrderItemIdentifiers) or [PUT v2/campaigns/{campaignId}/orders/{orderId}/boxes](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/setOrderBoxLayout):
  * Transfer the marking codes in the system to "_An honest sign_ ", if such labeling is provided for the product.
  * When selling goods **from abroad** specify:
    * Batch registration number — `rnpt`.
    * Number of the cargo customs declaration — `gtd`.
    * Country of manufacture code — `countryCode`. [How to get](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/regions/getRegionsCodes)


Through the API, you can also get information about the buyer, who is a legal entity, and about the documents for his order:
  * UPD;
  * UKD;
  * the waybill;
  * the invoice;
  * the adjustment invoice.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/business-info#business-buyer)How to determine that an order is from a legal entity
Make a request [GET v2/campaigns/{campaignId}/orders/{orderId}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrder) or [GET v2/campaigns/{campaignId}/orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/getOrders).
Signs of an order from a legal entity:
  * in `order` the nested parameter is returned `buyer` and the field `type` with the type of payer `BUSINESS`;
  * parameter `paymentMethod` will return with the value `B2B_ACCOUNT_PREPAYMENT` (the organization has paid for the order) or `B2B_ACCOUNT_POSTPAYMENT` (the organization will pay for the order after delivery).


Please note that the parameters `shipmentDate` and `shipmentTime` They will not be returned until the delivery date is agreed with the buyer.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/business-info#buyer-info)How to get customer information
Yandex MarketYour storeYandex MarketYour storeReceiving buyer informationPOST v2/campaigns/{campaignId}/orders/{orderId}/business-buyerIf order status isPROCESSING, DELIVERY,PICKUP or DELIVERED,prepares buyerinformation.OK: buyer information.
You can receive the data only if the order is in the status `PROCESSING`, `DELIVERY`, `PICKUP` or `DELIVERED`.
To find out the buyer's information, make a request [POST v2/campaigns/{campaignId}/orders/{orderId}/business-buyer](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/order-business-information/getOrderBusinessBuyerInfo).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/business-info#documents-info)How to get information about documents
Yandex MarketYour storeYandex MarketYour storeReceiving document informationPOST v2/campaigns/{campaignId}/orders/{orderId}/documentsIf order status is DELIVERED,prepares informationabout documents.OK: document information.
You can receive the data after the order status changes. `DELIVERED`.
To request information about the documents, make a request [POST v2/campaigns/{campaignId}/orders/{orderId}/documents](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/order-business-information/getOrderBusinessDocumentsInfo).
Honest Sign is a state system for labeling and tracking goods. [To learn more](https://yandex.ru/support/marketplace/orders/cz.html)
Copied
### Was the article helpful?
YesNo
Previous
[Digital orders](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/digital)
Next
[FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/supplies)
