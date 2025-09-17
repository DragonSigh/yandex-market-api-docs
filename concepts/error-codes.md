---
title: Types of errors and what to do about them | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/error-codes
crawled_at: 2025-09-17T14:22:45.248489
---

What do the error codes mean?
# Types of errors and what to do about them
  * [What do the error codes mean?](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#codes)
  * [Errors in the query content (400)](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#400)
  * [401 Unauthorized Errors](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#401)
  * [403 Forbidden Errors](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#403)
  * [404 Not Found Errors](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#404)
  * [Errors 405 Method Not Allowed](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#405)
  * [Errors 415 Unsupported Media Type](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#415)
  * [Errors 420 Enhance Your Calm](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#420)
  * [Errors 423 Locked](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#423)
  * [Errors 500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#500)
  * [503 Service Unavailable Errors](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#503)
  * [Example of an error message](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#example)


If the store's request could not be completed, the Market returns the parameter in response. `errors`. It contains error codes (parameter `code`) and their brief descriptions (parameter `message`).
If there are too many errors with a certain code, you will receive a notification about it in your account.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#codes)What do the error codes mean?
**Code** |  **Title** |  **What happened and what to do**  
---|---|---  
[400](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#400) |  `Bad Request` |  Something is wrong with the request content. For example, there is an error in the JSON data format or you are trying to change the status of a cancelled or delivered order. Focus on the error description to understand what exactly is wrong.  
[401](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#401) |  `Unauthorized` |  The authorization token is not specified in the request (or is specified, but not there).  
[403](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#403) |  `Forbidden` | 
  * The authorization token did not work. **For the OAuth token:** most likely, it has expired or you have removed the person for whom the token was issued from the staff.
  * API methods are unavailable due to _inactivity of the store or cabinet_.
  * Another access error.

  
[404](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#404) |  `Not Found` | 
  * The requested resource was not found. Check the request addresses that the store's system uses.
  * The specified parameter was not found. For example, a campaign. Check the correctness of the transmitted data.

  
[405](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#405) |  `Method Not Allowed` |  There is no such method on the specified resource. Check the request addresses that the store's system uses.  
[415](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#415) |  `Unsupported Media Type` |  The requested content type is not supported by the method. Check the correctness of the request.  
[420](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#420) |  `Enhance Your Calm` |  The store exceeded the request limit. Make sure that your system does not send anything superfluous.  
[423](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#423) |  `Locked` |  The method cannot be used for this store. Focus on the error description to understand what exactly is wrong.  
[500](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#500) |  `Internal Server Error` |  Internal error of the Market.  
[503](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#503) |  `Service Unavailable` |  The Yandex.Market server is overloaded.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#400)Errors in the query content (400)
The possible causes of this error depend on the specific request. In the description of many queries, there is a section describing the 400 error options for specific data.
Some error variants with the 400 code are the same for different queries:
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Campaign type is not allowed** |  This method does not support your store's operating model. |  Make sure that you use a method that supports your store's operating model.  
**Collection of field must not be empty** |  The parameter must not be empty. |  Specify at least one element for the parameter.  
**Contract with type MARKETING was signed with the agency** |  The marketing contract has been signed with the agency. |  For information on the closing documents, please contact your agency.  
**Invalid status: 'status'** |  An incorrect status is specified. |  Check the correctness of the transmitted status to filter orders by status.  
**JSON: {message}** |  The JSON data format contains an error. |  Check the correctness of the JSON.  
**Limit exceeded** |  Exceeded the limit on the number of values per page — parameter `limit`. |  Reduce the number of values.  
**Missing field** |  A required parameter is not specified. |  Specify a value for the required parameter.  
**Outlet is disabled for editing by partner** |  You cannot change the information or delete the store's point of sale because you refused to deliver to the Market's pick-up points. Read more about the delivery rules for DBS stores. [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/orders/dbs/settings/pvz#rules). |  Contact customer support if you are ready to enable delivery to the pick-up points of the Market.  
**String (value) is not a valid country code according to ISO 3166-1 alpha-2** |  Invalid country code. |  Specify the country code in the ISO 3166-1 alpha-2 format.  
**The request is too big: {message}** |  The HTTP request size limit has been exceeded. |  The size of the content cannot exceed 512 KB. Split the request into several.  
**Too long time period. Maximum is 'maxPeriod' days** |  The date range is too large. Maximum range — `maxPeriod`. |  Reduce the date range to filter orders by date.  
**Unexpected character 'character': expected a valid value 'values'** |  Invalid character. |  Check the encoding of the request body. The required encoding is UTF-8.  
**Unexpected end of content** |  The request body ends unexpectedly. |  Check the correctness of the format of the data transmitted in the request body.  
**Value / length of field (value) must be between min and max [exclusively]** |  The value (length) of the parameter must be between the values `min` and `max` and it is not equal to them. |  Check the correctness of the parameter value.  
**Value / length of field (value) must be greater / less than [or equal to] limit** |  The value (length) of the parameter must be equal to or greater than (less than) the specified value. `limit`. |  Check the correctness of the parameter value.  
**Value of field has too high scale: 'price'** |  The accuracy is set too high for the parameter. |  Set the parameter value with less precision.  
**Value of field must match the pattern: 'regExp'** |  The parameter value must match a regular expression. |  Check the correctness of the parameter value.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#401)401 Unauthorized Errors
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Api-Key token is invalid** |  The Api Key token is invalid. |  Check the spelling of the Api Key token. If the error persists, get a new token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)  
**Api-Key token is revoked** |  The Api Key token has been deleted. |  Get a new token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)  
**Api-Key token format invalid** |  The Api Key token format is incorrect. The prefix and length of the token are correct. |  Check the spelling of the Api Key token. If the error persists, get a new token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)  
**Api-Key token length invalid** |  Incorrect length of the Api Key token. |  Check the spelling of the Api Key token. If the error persists, get a new token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)  
**Api-Key token prefix invalid** |  Incorrect prefix of the Api Key token. |  Make sure that you do not use a prefix in the header. `Bearer`. [How to transfer an Api Key token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#use) If there is no prefix, check the spelling of the Api Key token. If the error persists, get a new token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)  
**Authorization header has invalid syntax** |  HTTP header format `Authorization` incorrect. |  Make a headline by [Instructions](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use).  
**Credentials are not specified** |  The authorization data is not specified in the request. |  Make a heading according to the instructions:
  * [Api Key token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key#use)
  * [The OAuth token](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use)

  
**OAuth credentials are not specified** |  The authorization data is not specified in the request. |  Make a headline `Authorization` by [Instructions](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use).  
**OAuth token is not specified** |  The request does not specify an OAuth authorization token. |  Make a headline `Authorization` by [Instructions](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use).  
**Unsupported authorization type specified in Authorization header** |  The type of authorization transmitted in the HTTP header `Authorization`, is not supported. |  Make a headline by [Instructions](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0#use).  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#403)403 Forbidden Errors
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Access denied** |  Access is denied. |  Check that the resource is specified correctly, as well as whether the user whose authorization token is used in the request has access rights to it. [More information about access](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0)  
**Access denied for campaign 'campaignId' because it is not active** |  The method is unavailable due to _store inactivity_. |  The option to use the API shows the parameter `apiAvailability` in response to requests:
  * [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/campaigns/getCampaigns);
  * [GET v2/campaigns/{campaignId}](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/reference/campaigns/getCampaign).

Fix the errors that prevent the goods from being returned to the showcase. If you need access to the API for this, contact support. Go to [seller's account on the Market](https://partner.market.yandex.ru/business/any/support) and press the button **Create an appeal**.  
**Access to API denied for the client / campaign** |  Access to the Yandex Market API is prohibited for sellers. |  Contact your agency to provide access to the API.  
**Contact not found for login 'login' and campaignId 'campaignId'** |  The user account whose login was sent to sign the electronic acceptance certificate was not found. |  Select the username of the user that is linked to the account or store.  
**Contacts with available roles for signing not found for login 'login'** |  The user account whose login was transferred to sign the electronic acceptance certificate does not have the necessary access rights. |  Provide the username of the user who is linked to the account or store and has the necessary access rights. [Access to methods by Api Key](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/access)  
**OAuth token is invalid** |  The specified OAuth authorization token is invalid. |  Get a new token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0)  
**OAuth token is invalid (account has been globally logged out)** |  The user used the function ["Get out everywhere"](https://yandex.ru/dev/id/doc/ru/tokens/token-invalidate) in Yandex ID. |  Get a new token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)  
**Restrict access for business 'businessId' because it is not active** |  The method is unavailable due to _cabinet inactivity_. |  Fix the errors that prevent the goods from being returned to the showcase. If you need API access for this, contact customer support. Go to [seller's account on the Market](https://partner.market.yandex.ru/business/any/support) and press the button **Create an appeal**.  
**Scope is invalid** |  The OAuth token was obtained through the app without access to the Market. |  Get a new token. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/oauth-2.0)  
**The method is not supported for Market Yandex Go sellers** |  This method is not available for Yandex Go Market sellers. These restrictions are specified in the description of the methods. |  —  
**Token does not have any of the scopes to access the API method** |  There is no access to the method. |  Get access to at least one group of methods listed in the error text. [How to do it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/api-key)  
**User account is disabled** |  The account of the user for whom the specified authorization token was issued is blocked. |  Contact customer support.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#404)404 Not Found Errors
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Campaign not found: 'campaignId'** |  The campaign specified in the request was not found. |  Check that the transmitted campaign ID is correct.  
**Login not found: 'login'** |  The username specified in the request was not found. |  Check the correctness of the transmitted username.  
**Model not found: 'modelId'** |  The model specified in the request was not found. |  Check that the transmitted model ID is correct.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#405)Errors 405 Method Not Allowed
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Request method 'method' not supported** |  The requested HTTP method is not supported. |  Check the methods that are supported by the resource.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#415)Errors 415 Unsupported Media Type
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Content type 'content-type' not supported** |  The requested content type is not supported. |  Transmit one of the supported content types.  
**Missing Content-Type** |  The content type is not specified. |  Pass the content type.  
**Unknown content-type: 'content-type'** |  The requested content type is unknown. |  Transmit one of the supported content types.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#420)Errors 420 Enhance Your Calm
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Hit rate limit of 'N' parallel requests** |  The global limit on the number of simultaneous requests to the Yandex.Market API for sellers has been exceeded. [What is it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits#global) |  Reduce the number of parallel API requests within a single cabinet or store to `N` requests.  
**Hit rate limit of 'N' requests per 'period' for resource 'R'** |  Exceeded the resource limit on the number of `N` resource requests `R` for the period `period` for the same office or store. [What is it](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits#resource) |  The time limit is specified in the header. `X-RateLimit-Resource-Until`. The use of the resource will become possible after the specified time.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#423)Errors 423 Locked
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Business is in migration** |  Store migrations are taking place in the cabinet. |  Wait for the transfer to finish.  
**Campaign is in business migration** |  The store is in the process of being moved to another account. |  Wait for the transfer to finish.  
**Partner use only default price** |  The cabinet uses prices for all stores. |  You will not be able to set the price for a separate store. Set uniform prices for all stores in the cabinet.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#500)Errors 500 Internal Server Error
Wait for a while and call the method again. If the problem persists, contact customer support. Go to [seller's account on the Market](https://partner.market.yandex.ru/business/any/support) and press the button **Create an appeal**.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#503)503 Service Unavailable Errors
**Description** |  **Translation** |  **What to do**  
---|---|---  
**Service temporarily unavailable. Please, try again later** |  The server is temporarily unavailable due to high load. |  Try to repeat the request after a while. If the problem persists, contact customer support. Go to [seller's account on the Market](https://partner.market.yandex.ru/business/any/support) and press the button **Create an appeal**.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes#example)Example of an error message
Request:
```
GET /campaigns/10003/orders HTTP/1.1
Host: api.partner.market.yandex.ru
Accept: */*
Api-Key: ACMA:I4c4CxCSYaI41RSC2uYWP2qj3Rhhm4knMiBEga5K:151c0664a

```

Answer:
```
{
  "errors": [
    {
      "code": "UNAUTHORIZED",
      "message": "Api-Key token is invalid"
    }
  ],
  "status": "ERROR"
}

```

The store is disabled because it has not placed products in the showcase for more than 90 days.  
  
There is not a single active store in the cabinet.
The store is disabled because it has not placed products in the showcase for more than 90 days.
All stores in the office are disabled, as they have not placed goods in the window for more than 90 days.
Copied
### Was the article helpful?
YesNo
Previous
[Response format](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/result-format)
Next
[Restrictions on requests](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/limits)
