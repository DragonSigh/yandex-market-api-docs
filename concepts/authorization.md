---
title: Authorization | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/authorization
crawled_at: 2025-09-17T14:22:52.055668
---

Yandex.Market API Tokens
# Authorization
To work with Yandex.Market via the API, you need to get an API Key token. We do not recommend using an OAuth token, as this authorization method is outdated.
Do I need to switch to an Api Key token immediately?
You can use the already generated OAuth token until the end of its validity period, or switch to working with the API Key token immediately.
[How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)
During the transition period from one token to another, you can transfer both:
  * [How to transfer an API Key token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#use)
  * [How to transfer an OAuth token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use)


##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/authorization#token-types)Yandex.Market API Tokens
|  [**Api-Key**](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key) |  [**OAuth**](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0) (outdated)  
---|---|---  
**Binding** |  To the account where the token was created. |  To the user who created the token.  
**Method of receipt** |  In the seller's office on the Market. [Instruction manual](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key) |  By creating an OAuth application. [Instruction manual](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0)  
**Access to stores** |  All shops are in the cabinet. |  Only those that the user has access to.  
**Is it possible to configure access to certain groups of methods** |  Yes. [Instruction manual](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key) |  No.  
**Transmission header** |  `Api-Key`. [How to transfer a token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#use) |  `Authorization`. [How to transfer a token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use)  
**The validity period of the token** |  Unlimited. |  1 year.  
Copied
### Was the article helpful?
YesNo
Previous
[Introduction](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/)
Next
[Api-Key](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)
