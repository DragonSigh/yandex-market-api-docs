---
title: OAuth 2.0 (deprecated) - Authorization | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/oauth-2.0
crawled_at: 2025-09-17T14:26:33.968053
---

  * [Create an application](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#application)
  * [Create a token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#token)
  * [Transfer the token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use)
  * [It may be useful](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#read-more)


Authorization using an OAuth token
We do not recommend using an OAuth token, as this authorization method is outdated.
You can use the already generated token until the end of its validity period or create an API Key token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)
# Creating and using an OAuth token
The OAuth 2.0 protocol is used for authorization. To work with Yandex.Market via the API:
  1. Create an application on the oauth website.yandex.ru. If you already have an app with access `market:partner-api` You don't need to create a new one — you can use one for all stores and business accounts.
  2. Create a token in the name of an employee who has access to the store's data.
  3. Insert the token into the headers of Market requests.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#application)Create an application
  1. Log in to the Yandex account that your system will use to access the Yandex.Market API.
Pay attention to the account selection.
This must be an account:
     * Which the business will not lose access to.
     * Who will not lose access to the business — for example, when an employee is fired.
  
It is best to use an account protected by two-factor authentication and owned by the business owner.   
  

**You will need to receive the token again.**
If the Yandex ID user who created it is:
     * It will log out from all devices in the Yandex account.
     * will change the password;
     * enables or disables two-factor authentication.
     * it will restore access.
For more information about token revocation, see [Yandex ID Help](https://yandex.ru/dev/id/doc/ru/tokens/token-invalidate).
  2. Open the page **[oauth.yandex.ru/client/new](https://oauth.yandex.ru/client/new)**. , Use this particular link. If you just click the create application button on the Yandex ID website, nothing will work.
  3. In the field **The name of your service** write whatever you want. If you have a lot of applications and it is important for you to navigate them, enter the business name.
  4. You don't need to add an icon.
  5. Choose a platform **Web services**.
  6. In the field **Redirect URI** Click the button **Substitute the URL for debugging** , which is located in the popup hint to the field. ![Screenshot](https://yandex.ru/dev/market/partner-api/doc/en/concepts/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/concepts/oauth-url.png)
  7. , In the field **Access to data** enter `market:partner-api` and select **Yandex.Market API / Product search for partners** in the drop-down list.
Why can't I see the "Data Access" field?
You probably didn't follow the link. **[oauth.yandex.ru/client/new](https://oauth.yandex.ru/client/new)** , and they clicked the app creation button on the Yandex ID website. You need exactly the application creation form that opens via the link.
  8. Specify the business address in the field **Contact email**.
  9. Click **Create an application**.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#token)Create a token
After creating the application, you need to get a token.
Is it possible to use an account other than the one used to create the app to receive the token?
May. It must also meet the same requirements. If the Yandex ID for which the token is issued loses access to the business, the API will stop working.
  1. Open [oauth.yandex.ru](https://oauth.yandex.ru/) and click on the created app to access the Market.
  2. Copy it **ClientID** this application.
  3. Insert the identifier into this link:
```
https://oauth.yandex.ru/authorize?response_type=token&client_id=<ClientID>

```

It will turn out something like this:
```
https://oauth.yandex.ru/authorize?response_type=token&client_id=5473335а275a5nb8e2648q12n8r378l7

```

Click on the resulting link.
  4. Confirm the login.
  5. You will see the token. Copy it.


This token is valid for a year
When the year comes to an end, create an API Key token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use)Transfer the token
Insert the received token into the header `Authorization` according to the following scheme:
```
Authorization: Bearer <token>

```

As a result, the title will look like this:
```
Authorization: Bearer y0_BfRRRRRV2L8sWWvNkSNNNNSrLHaNXg4cCMswFbL6MWab9lktL2KPsMw

```

If the request is received without a header with a valid token, the Market returns an error. `401 Unauthorized`.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#read-more)It may be useful
  * [Help from the Yandex ID authorization service](https://yandex.ru/dev/id/doc/ru/)
  * [Description of errors returned by the Yandex.Market API](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes)


Copied
### Was the article helpful?
YesNo
Previous
[Getting information on FBY applications](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/_auto/scopes_summary/pages/supplies-management_read-only)
Next
[Calling methods](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/method-call)
