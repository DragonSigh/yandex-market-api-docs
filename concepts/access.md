---
title: Access to methods by Api Key | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/access
crawled_at: 2025-09-17T14:22:38.302832
---

What types of access are available
# Access to methods by Api Key
To allow employees to perform only the methods they need for their work, create a token with access to certain groups of methods.
[How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#new-token)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/access#method-groups)What types of access are available
You can get the list of accesses using the passed Api Key token using the method [POST v2/auth/token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/auth/getAuthTokenInfo).
**Access** |  **The name of the access in the OpenAPI specification**  
---|---  
_Full account management_ |  all-methods  
_View all data_ |  all-methods:read-only  
[Order processing and inventory](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/inventory-and-order-processing) |  inventory-and-order-processing  
[View order information](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/inventory-and-order-processing_read-only) |  inventory-and-order-processing:read-only  
[Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/pricing) |  pricing  
[View prices](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/pricing_read-only) |  pricing:read-only  
[Manage products and cards](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/offers-and-cards-management) |  offers-and-cards-management  
[View products and cards](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/offers-and-cards-management_read-only) |  offers-and-cards-management:read-only  
[Product promotion](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/promotion) |  promotion  
[View promotion information](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/promotion_read-only) |  promotion:read-only  
[View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/finance-and-accounting) |  finance-and-accounting  
[Customer communication](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/communication) |  communication  
[Store settings](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/settings-management) |  settings-management  
[View FBY requests](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/supplies-management_read-only) |  supplies-management:read-only  
All requests to the Market
All requests to receive and view data
### Was the article helpful?
YesNo
Previous
[Api-Key](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)
Next
[Order processing and accounting of goods](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/inventory-and-order-processing)
