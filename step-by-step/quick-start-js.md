---
title: Launching integration in JavaScript | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/quick-start-js
crawled_at: 2025-09-17T14:23:55.801727
---

Download the OpenAPI specification
# Launching integration in JavaScript
  * [Download the OpenAPI specification](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#download)
  * [Generate a client](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#generate)
  * [Create a project](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#create-project)
  * [Prepare the data for access](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#token)
  * [Make a request](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#code)


This guide will help you set up the simplest test integration in JavaScript from scratch for store requests to the Market. You will be able to request a list of stores and receive a response.
You will need a Node.js and Java version 11 or higher
Set them up in advance.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#download)Download the OpenAPI specification
Via git
Just a browser
  1. Open the folder where you want to save the specification. In this manual, it will be referred to as `<project_directory>`.
  2. Run the command prompt in it.
  3. Write a command:
```
git clone https://github.com/yandex-market/yandex-market-partner-api.git

```



  1. Download 
  2. Unzip the archive to the folder where you want to save the specification. In this manual, it will be referred to as `<project_directory>`.


##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#generate)Generate a client
  1. Open the folder `yandex-market-partner-api`, which appeared in the previous step.
  2. Run the command prompt in it.
  3. Write a command:


```
npx @openapitools/openapi-generator-cli generate -i <path_to_openapi.yaml> -g javascript -o <output_path>

```

As a **output path** specify the folder where your project will be located.
If **openapitools** until it is installed, agree to the installation. In the folder **output path** the client's files will appear.
> **Example**
> Let's say you downloaded an archive and unpacked it. The specification is in the folder `<project_directory>/yandex-market-partner-api`.
> Do you want to place the project in a folder `<project_directory>/market-integration`.
> 1. Open the folder `<project_directory>/yandex-market-partner-api`.
> 2. Run the command prompt in it.
> 3. In the console that opens, write:
> ```
npx @openapitools/openapi-generator-cli generate -i openapi/openapi.yaml -g javascript -o ../market-integration

```

> 4. If you are prompted to install the generator, enter **Y** and click **Enter**.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#create-project)Create a project
  1. Open the folder where the client's files are located. In the example above, this is `<project_directory>/market-integration`.
  2. Run the command prompt in it.
  3. Write a command:
```
npm install
npm run build

```



##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#token)Prepare the data for access
Get an authorization token by [Instructions](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/concepts/api-key).
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/quick-start-js#code)Make a request
To perform [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/campaigns/getCampaigns):
  1. Open the created project in the IDE.
  2. Create in the root of the project (folder `<project_directory>/market-integration`) file `index.js`.
  3. Create an instance `CampaignsApi` and refer to the method `getCampaigns`. To do this, write to `index.js` here is the code:
```
const { CampaignsApi } = require('./dist');

const campaignsApi = new CampaignsApi();
campaignsApi.apiClient.authentications['ApiKey'].apiKey = '<token>';

campaignsApi.getCampaigns(undefined, function (error, data) {
    console.log(JSON.stringify(data, null, 4));
});

```

As a `<token>` use the token you received in the previous step.
  4. Write to the console `node index.js`.


The console will display the result of the query: the names of all stores, placement models, IDs, and more:
```
{
    "campaigns": [
        {
            "domain": "Shop 1",
            "id": 12345678,
            "clientId": 87654321,
            "business": {
                "id": 123456,
                "name": "My shop"
            },
            "placementType": "FBS"
        },
        {
            "domain": "Shop 2",
            "id": 23456789,
            "clientId": 98765432,
            "business": {
                "id": 123456,
                "name": "My shop"
            },
            "placementType": "DBS"
        },
        {
            "domain": "GoodShop",
            "id": 34567891,
            "clientId": 19876543,
            "business": {
                "id": 123456,
                "name": "My shop"
            },
            "placementType": "FBY"
        },
    ],
    "pager": {
        "total": 3,
        "from": 1,
        "to": 3,
        "currentPage": 1,
        "pagesCount": 1,
        "pageSize": 3
    }
}

```

Copied
### Was the article helpful?
YesNo
Previous
[Step-by-step instructions](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/)
Next
[Adding and editing products](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/assortment-add-goods)
