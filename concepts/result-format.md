---
title: Response format | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/result-format
crawled_at: 2025-09-17T14:26:43.963457
---

Response format
# Response format
The Yandex.Market API for sellers returns responses in UTF-8 encoding. Responses can only be in JSON format.
To set the response format, specify the selected format after the method name in the request URL. For example, as a result of executing the following query, you will receive a list of products in the catalog in JSON format:
```
GET https://api.partner.market.yandex.ru/v2/campaigns/{campaignId}/offer-mapping-entries.json

```

You can also set the response format when calling methods using the HTTP header. `Accept`. Possible header value: `application/json`.
The response format must match [the format of the input data](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/input-format). Therefore, in the title `Accept` or in the request URL (extension `.json` ) set the same format as in the header `Content-Type`.
When calling DELETE methods, the result format must be specified to ensure compatibility with libraries that are used to work with data.
Some Market systems remove spaces at the beginning and end of a line.
For example, the string `" example "` can be saved as `"example"`.
If you have lines with such spaces, consider this feature. For example, remove spaces before passing lines to Yandex.Market and before data reconciliation.
Copied
### Was the article helpful?
YesNo
Previous
[Input data format](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/input-format)
Next
[Types of errors and what to do about them](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/error-codes)
