---
title: How to use the console | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/console
crawled_at: 2025-09-17T14:27:05.607559
---

How to log in to the dashboard
# How to use the console
  * [How to log in to the dashboard](https://yandex.ru/dev/market/partner-api/doc/en/en/console#authorization)
  * [To send a request](https://yandex.ru/dev/market/partner-api/doc/en/en/console#send-request)


There are two tabs on the description page for each request.: **Info** and **Console**.
The console allows you to manually make requests and see what the Market responds to.
You can't send integration names in the console.
Therefore, the integration type is displayed on the logs page for such requests. **Documentation Console** , not its name.
[Learn more about working with logs](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/debug)
##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/console#authorization)How to log in to the dashboard
  1. Click the button **Authorization**.
  2. Select the token you are using, — **apiKey** or **oauth2**.
  3. Enter the token in the format:
     * `ACMA:I4c4CxCSYaI41RSC2uYWP2qj3Rhhm4knMiBEga5K:151c0664` — for the Api Key.
     * `Bearer y0_BfRRRRRV2L8sWWvNkSNNNNSrLHaNXg4cCMswFbL6MWab9lktL2KPsMw` — for OAuth.


Learn more about getting and using the token:
  * [API-Key](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/api-key)
  * [OAuth 2.0](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/oauth-2.0)


##  [](https://yandex.ru/dev/market/partner-api/doc/en/en/console#send-request)To send a request
All requests sent to the console and its responses are real
For example, if you try to cancel an existing order, it will actually be canceled.
  1. Open the page with the description of the required method and go to the tab **Console**.
  2. Fill in the form **Path params** , **Header params** and **Body**. If you need a description of the parameter, go back to the tab **Info** and look at it there — the already entered data will not be lost.
  3. Click **Send**.


Copied
### Was the article helpful?
YesNo
Previous
[Test orders](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/sandbox)
Next
[Signature of integrations](https://yandex.ru/dev/market/partner-api/doc/en/en/concepts/integration-signing)
