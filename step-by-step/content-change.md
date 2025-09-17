---
title: Changing categorical characteristics | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/content-change
crawled_at: 2025-09-17T14:43:45.658756
---

The products belong to a new category for the store
# Changing categorical characteristics
  * [The products belong to a new category for the store](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change#edit-card)
  * [The products belong to a well-known and customized category](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change#known-category)
  * [How to check and update the comparison of characteristics on the Market and in the store](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change#check-and-update-comparison)


Through the API, you can manage the content on product cards, including transmitting characteristics specific to a specific product category.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change#edit-card)The products belong to a new category for the store
Yandex MarketYour storeYandex MarketYour storeRetrieving card statuses and previously submitted product informationRetrieving product attributes required for their categoryFilling out cardsChecking resultsPOST v2/businesses/{businessId}/offer-cardsCompilesa list of products.OK: list of products with card statuses and filling recommendations.Market category ID for the productPOST v2/category/{categoryId}/parametersOK: list of attributes for products in this category.Matches their product attributeswith Market attributes.Attribute values for each productPOST v2/businesses/{businessId}/offer-cards/updateAnalyzes the received contentand, if valid,adds it to the cards.OKPOST v2/businesses/{businessId}/offer-cardsVerifies the product list.OK: list of products with statuses and filling recommendations.
  1. Get the information that you previously provided for product cards, as well as card statuses and recommendations for filling them out using [POST v2/businesses/{businessId}/offer-cards](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/getOfferCardsContentStatus).
In response, you will receive the following:
     * To which categories the products belong on the Market. The Market determines the product category automatically based on the data provided by you.
     * What is the status of the product cards?
     * Transmitted product characteristics.
     * Recommendations for filling out the cards. [How to use the recommendations](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change#recommendations)
  2. For each _The leaf category_ request a list of required characteristics using [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/getCategoryContentParameters).
For characteristics that have units of measurement, in the parameter `unit` They will return:
     * acceptable values (`units`);
     * default value (`defaultUnitId`).
  3. Compare the characteristics expected by Yandex.Market with the characteristics available in the store's database.
**Example.** For soup plates, the Market expects, among others, the "Color for filter" characteristic. In the store's database, the same characteristic is called "Color". You need to set up the integration so that:
     * the value of the "Color" characteristic was transmitted to the Market as the "Color for filter" characteristic;
     * Each value of the "Color" characteristic was assigned an acceptable value of the "Color for filter" characteristic.
  4. Transmit the product characteristics using [POST v2/businesses/{businessId}/offer-cards/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/updateOfferContent).
Always convey the full set of characteristics.
Passing empty values will erase what was entered on the cards earlier.
If necessary, change the identifier of the unit of measurement of characteristics — parameter `unitId` in `parameterValues`. If it is not passed, the default units of measurement will be used (`defaultUnitId`).


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change#known-category)The products belong to a well-known and customized category
Follow the instructions for the new category, but skip the step of configuring the comparison of Market and store characteristics.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change#check-and-update-comparison)How to check and update the comparison of characteristics on the Market and in the store
The lists of characteristics required for products of various categories do not remain unchanged. Gadgets have additional functions, new materials are becoming fashionable. Sometimes the Market simply makes a more detailed list of characteristics on the product card to make it easier for customers to compare and choose.
For each of the configured categories, check regularly to see if the mapping needs to be updated.
Yandex MarketYour storeYandex MarketYour storeChecking category settingsCategory ID on the Market that was configured long agoPOST v2/category/{categoryId}/parametersOK: list of attributes for products in this category.Verifies the mapping of product attributeswith the attributes on the Market.
Also read the instructions
  * [Adding and editing products](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods)
  * [Yandex.Market recommendations for cards](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/recommendations)
  * [Managing goods in the archive](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-archive)


A category that has no children.
Copied
### Was the article helpful?
YesNo
Previous
[Adding and editing products](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods)
Next
[Recommendations for cards](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/recommendations)
