---
title: Creating and using an API Key token | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/api-key
crawled_at: 2025-09-17T14:21:59.468629
---

Create a token
# Creating and using an API Key token
  * [Create a token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#new-token)
  * [Edit the token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#edit-token)
  * [Delete a token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#delete-token)
  * [Transfer the token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#use)
  * [It may be useful](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#read-more)


To work with Yandex.Market via the API:
  1. Create a token with access to certain groups of methods. This way, employees will be able to call only the methods they need for their work. [What types of access are available](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/access)
  2. Insert the token in the header of the Yandex.Market request.


Only the cabinet owner and cabinet manager can create and manage tokens. For more information about what roles are available, read [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/account/permissions/roles).
The maximum number of tokens for the cabinet is 30.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#new-token)Create a token
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **Modules and APIs**.
  2. In the block **Authorization token** Click the button **To create** or **Create a new token** if you have already received it.
![Screenshot](https://yandex.ru/dev/market/partner-api/doc/en/concepts/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/concepts/api-token.jpg)
  3. In the window that opens:
    1. Specify the unique name of the token.
    2. Select one or more access points for this token.
    3. Click the button **To create**.
![Screenshot](https://yandex.ru/dev/market/partner-api/doc/en/concepts/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/concepts/access.jpg)


##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#edit-token)Edit the token
Before editing
Make sure that your integration will continue to work with the modified token.
You can change access rights, as well as the name of the token. To do this:
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **Modules and APIs**.
  2. In the block **Authorization tokens** find the one you need, tap the three dots next to it and select **Edit**.
  3. Change the required information.
  4. Click **Save**.


The information will be updated within 10 minutes.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#delete-token)Delete a token
Before deleting
Make sure that your integration will continue to work without this token.
  1. In the cabinet in the lower left corner, click on the name of your business and go to the page **Modules and APIs**.
  2. In the block **Authorization tokens** find the one you need, tap the three dots next to it and select **Remove**.
  3. Confirm the deletion.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#use)Transfer the token
Insert the received token into the header `Api-Key` according to the following scheme:
```
Api-Key: <token>

```

As a result, the title will look like this:
```
Api-Key: ACMA:I4c4CxCSYaI41RSC2uYWP2qj3Rhhm4knMiBEga5K:151c0664

```

If the request is received without a header with a valid token, the Market returns an error. `401 Unauthorized`.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#read-more)It may be useful
  * [The method of obtaining information about the transferred authorization token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/auth/getAuthTokenInfo)
  * [Description of errors returned by the Yandex.Market API](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes)


Copied
### Was the article helpful?
YesNo
Previous
[Authorization](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/authorization)
Next
[Access to methods by Api Key](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/access)
