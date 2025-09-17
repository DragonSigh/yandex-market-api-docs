---
title: Adding and editing products | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/assortment-add-goods
crawled_at: 2025-09-17T14:37:33.583447
---

Adding and editing products
# Adding and editing products
  * [Add new products to the catalog](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#add)
  * [Change product categories](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#change-category)
  * [Change product characteristics](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#change-parameters)
  * [Delete product characteristics](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#delete)
  * [Combine products on a card](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#combine-variants)


Using a request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateOfferMappings) you can add products to the catalog and transfer:
  * their _leaf categories_ on the Market and categorical characteristics;
  * main features;
  * prices of goods in the cabinet.


You can also combine products on the card, edit and delete information about already added products, including prices in the cabinet and product categories.
To find out the source and time of the information update:
  1. In the seller's account on the Market, go to the page **Products** → **Catalog**.
  2. Click on the product you are interested in.
  3. In the upper-right corner, click ![](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/wheel-button.png) and enable the option **Data source**.
Information about the data transfer will appear under the corresponding characteristics. ![](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/docs-assets/dev-market-partner-api/rev/r17524636/en/_images/data-source.png)


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#add)Add new products to the catalog
To add products to the catalog and place them in the store, you need to make several consecutive requests to the Market:
Yandex MarketYour storeYandex MarketYour storeRetrieving the list of Market categoriesRetrieving product attributes required for their categoryAdding products to the catalogCalculating Market service costsopt​Retrieving a list of suitable modelsSubmitting product placement termsChecking statuses of added productsPOST v2/categories/treeOK: category tree.Market category ID for the productPOST v2/category/{categoryId}/parametersOK: list of attributes for products in this category.Matches their product attributeswith Market attributes.Product informationPOST v2/businesses/{businessId}/offer-mappings/updateVerifies product informationand adds them to the store catalog.OKProduct parameters for cost calculationPOST v2/tariffs/calculateOK: service costs for products with specified parameters.Requests a list of available business modelsPOST v2/businesses/{businessId}/offer-mappingsPrepares the product list.OK: product list with recommended models.Placement termsPOST v2/campaigns/{campaignId}/offers/updateVerifies and acceptsplacement terms.Publishes products on the marketplace.OKProduct listPOST v2/campaigns/{campaignId}/offersVerifies the product list.OK: product list with statuses and error information.
  1. Get a list of Market categories by making a request [POST v2/categories/tree](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/categories/getCategoriesTree).
  2. For each _The leaf category_ request a list of required characteristics using [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/getCategoryContentParameters).
For characteristics that have units of measurement, in the parameter `unit` They will return:
     * acceptable values (`units`);
     * default value (`defaultUnitId`).
  3. Call the method [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateOfferMappings), where:
     * Provide information about the products (names, descriptions, photos, etc.), prices, _leaf categories_ on the Market and characteristics.
     * If necessary, change the identifier of the unit of measurement of characteristics — parameter `unitId` in `parameterValues`. If it is not passed, the default units of measurement will be used (`defaultUnitId`).
**For sellers of the Yandex Go Market:** also read [instructions](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/market-yandex-go-sellers).
  4. If necessary, look at the cost of Market services for specific products. To do this, pass their parameters in the request. [POST v2/tariffs/calculate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/tariffs/calculateTariffs).
  5. Get a list of models from Yandex. Market for which you can sell each of the added products using a query. [POST v2/businesses/{businessId}/offer-mappings](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/getOfferMappings). [What is a work model and what models are there?](https://yandex.ru/support/marketplace/introduction/models.html)
  6. Set the conditions for product placement using a query [POST v2/campaigns/{campaignId}/offers/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/updateCampaignOffers). The terms of the placement are the minimum order quantity, sales quota and VAT. If you use the DBS model, the same query sets the delivery parameters.
  7. Make sure that the products have appeared in the showcase by using a request [POST v2/campaigns/{campaignId}/offers](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/assortment/getCampaignOffers). You will find detailed explanations of the product statuses. [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/assortment/add/statuses.html).


Each added product will receive a card on the Market
Each of the products you have added will be placed on the corresponding card page. To understand how the cards are arranged on the Market, read [an article in the Help of the Market for sellers](https://yandex.ru/support/marketplace/assortment/content/index.html).
In the request [POST v2/businesses/{businessId}/offer-mappings](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/getOfferMappings) you can check the current binding of the product to the card.
When transmitting the card ID in the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateOfferMappings) Yandex.Market will consider your offer for linking, but based on the results of verification, it can link the product to a more suitable card.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#change-category)Change product categories
Yandex MarketYour storeYandex MarketYour storeRetrieving the list of Market categoriesUpdating product categoriesPOST v2/categories/treeOK: Market category tree.New categories and product attributesPOST v2/businesses/{businessId}/offer-mappings/updateUpdates product categoriesand their attributesin the store catalog.OK
  1. Get a list of Market categories using a request [POST v2/categories/tree](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/categories/getCategoriesTree).
  2. To change the categories of products that you have already added to the catalog, in the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateOfferMappings) send:
     * Their IDs — `offerId`.
     * Ids of new ones _leaf categories_ — `marketCategoryId`.
     * Product characteristics and their meanings for new categories — `parameterValues`. The values of the common characteristics for the old and new categories will remain, and you do not need to transfer them.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#change-parameters)Change product characteristics
To change the characteristics of products that you have already added to the catalog, in the request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateOfferMappings) retransmit:
  * Their IDs — `offerId`.
  * Ids _leaf categories_ — `marketCategoryId`. If you don't send it, you will receive a warning in the response (parameter `warnings`).
  * New characteristics and their meanings — `parameterValues`. If you don't pass it `parameterValues` and `marketCategoryId`, information from outdated parameters will be used `params` and `category`, and `marketCategoryId` it will be detected automatically.


If necessary, change the identifier of the unit of measurement of characteristics — parameter `unitId` in `parameterValues`. If it is not passed, the default units of measurement will be used (`defaultUnitId`).
You don't need to transmit parameters where nothing changes.
Product characteristics by category can be obtained using a request. [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/getCategoryContentParameters).
You can also change the categorical characteristics using [Instructions](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#delete)Delete product characteristics
To delete previously transmitted product characteristics, use a request [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateOfferMappings) — in `deleteParameters` specify the values of the parameters that you want to delete.
You can pass multiple values at once.
For parameters with the type `string` you can also pass an empty value.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods#combine-variants)Combine products on a card
To combine product options on one card:
  1. Make a request [POST v2/category/{categoryId}/parameters](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/getCategoryContentParameters). The characteristics that are the features of the product variant may depend on the cabinet. To find them out, pass the parameter `businessId`.
If the category supports combining options:
     * Among the characteristics will be the following:
Parameter | Meaning  
---|---  
id | 200  
name | Name of the group of options  
     * The characteristics will be returned with the value `true` in the field `distinctive`.
  2. Add each option to the catalog individually.
  3. Pass the categorical characteristics for them as a parameter. `parameterValues` in the method [POST v2/businesses/{businessId}/offer-mappings/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/business-assortment/updateOfferMappings) or [POST v2/businesses/{businessId}/offer-cards/update](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/content/updateOfferContent).


Follow the following rules:
  * The name of the group of options should be **the same** for all products that need to be displayed as options on a single card.
  * The name of a group of variants can be a sequence of any characters up to 255 characters long.
  * Each option should be different from all the others in `distinctive`- characteristics.
  * All other characteristics must have the same values.
**Example.** In some category, there are three characteristics — the features of the options (`distinctive`: `true`): **the color for the filter** , **size** and **availability of Wi-Fi**. And more features **material** and **series** , which are not features of the variants.
✅ Right
❌ Wrong
| The color for the filter | Size | There is Wi-Fi | Material | Series  
---|---|---|---|---|---  
Option 1 | Red | XL | Yes | Tree | "Jupiter"  
Option 2 | Red | XL | — | Tree | "Jupiter"  
Option 3 | Green | S | Yes | Tree | "Jupiter"  
Each option has its own set `distinctive`- characteristics, and the rest match.
| The color for the filter | Size | There is Wi-Fi | Material | Series  
---|---|---|---|---|---  
Option 1 | Red | XL | Yes | Tree | "Jupiter"  
Option 2 | Red | XL | Yes | Tree | "Jupiter"  
Option 3 | Green | S | Yes | Tree | "Jupiter"  
Option 1 and option 2 have the same features.
* * *
| The color for the filter | Size | There is Wi-Fi | Material | Series  
---|---|---|---|---|---  
Option 1 | Red | XL | Yes | Tree | "Jupiter"  
Option 2 | Red | XL | — | Tree | "Jupiter"  
Option 3 | Green | S | Yes | Steel | "Mars"  
Option 3 has different characteristics that are not specific to the option.


For more information on how to work with product options, see [Help](https://yandex.ru/support/marketplace/assortment/content/combine.html).
Also read the instructions
  * [Changing categorical characteristics](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change)
  * [Yandex.Market recommendations for cards](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/recommendations)
  * [Managing goods in the archive](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-archive)


A category that has no children.
Categories that have no children.
Copied
### Was the article helpful?
YesNo
Previous
[Setting up integration from scratch in JavaScript](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js)
Next
[Changing categorical characteristics](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/content-change)
