---
title: The OpenAPI Specification | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/concepts/openapi
crawled_at: 2025-09-17T14:22:04.606974
---

How to generate a Yandex.Market API client for sellers
# The OpenAPI Specification
  * [How to generate a Yandex.Market API client for sellers](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi#how-to)
    * [Get the specification via git](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi#git)
    * [Installing the OpenAPI generator via package managers](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi#package-managers)
    * [Customer Generation](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi#client-generation)


The OpenAPI specification for store-to-Market requests is available 
##  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi#how-to)How to generate a Yandex.Market API client for sellers
The specification will help you generate client files in any language or framework that the OpenAPI generator supports. This can greatly simplify integration with Yandex.Market via the API.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi#git)Get the specification via git
There are two ways:
  1. Run the command `git clone https://github.com/yandex-market/yandex-market-partner-api.git`
  2. Download the archive from the repository via GitHub web-ui: click the green button in the upper-right corner `Code` and in the drop-down list, select `Download ZIP`.


###  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi#package-managers)Installing the OpenAPI generator via package managers
Generator Documentation: 
**For npm (any OS)** `npm install @openapitools/openapi-generator-cli -g`
**For Homebrew (macOS)** `brew install openapi-generator`
**For Scoop (Windows)** `scoop install openapi-generator-cli`
###  [](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/openapi#client-generation)Customer Generation
**For npm (any OS)**
```
npx @openapitools/openapi-generator-cli generate -i <path_to_openapi.yaml> -g <lang> -o <output_path>

```

**For other package managers**
```
openapi-generator generate -i <path_to_openapi.yaml> -g <lang> -o <output_path>

```

The values of the query parts:
`<lang>` — generator parameter for the selected language or framework.
`<output_path>` — the output directory where the generated client code will be placed.
`<path_to_openapi.yaml>` — the path to the openapi.yaml file of this specification.
Examples of generators:
  * go
  * java
  * javascript
  * kotlin
  * php
  * python
  * ruby


The full list of generators is available at the link: 
Copied
### Was the article helpful?
YesNo
Previous
[Signature of integrations](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/concepts/integration-signing)
Next
[For sellers of the Yandex Go Market](https://yandex.ru/dev/market/partner-api/doc/en/concepts/en/market-yandex-go-sellers)
