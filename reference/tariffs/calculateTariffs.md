---
title: Cost of services - Prices | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/calculateTariffs
crawled_at: 2025-09-17T14:38:16.780102
---

  * [Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body)
    * [CalculateTariffsOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsofferdto)
    * [CalculateTariffsParametersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsparametersdto)
    * [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#currencytype)
    * [PaymentFrequencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#paymentfrequencytype)
    * [SellingProgramType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#sellingprogramtype)
  * [Responses](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#responses)
  * [200 OK](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#200-ok)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body1)
    * [CalculateTariffsResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsresponsedto)
    * [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype)
    * [CalculateTariffsOfferInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsofferinfodto)
    * [CalculatedTariffDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatedtariffdto)
    * [TariffParameterDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#tariffparameterdto)
    * [CalculatedTariffType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatedtarifftype)
  * [400 Bad Request](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#400-bad-request)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body2)
    * [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apierrordto)
  * [401 Unauthorized](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#401-unauthorized)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body3)
  * [403 Forbidden](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#403-forbidden)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body4)
  * [404 Not Found](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#404-not-found)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body5)
  * [420 Method Failure](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#420-method-failure)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body6)
  * [500 Internal Server Error](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#500-internal-server-error)
    * [Body](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body7)


# Service Cost Calculator
Info
Console
**The method is available for[all models](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/overview/business).**
**If you are using an API Key token, one of the accesses in the list is required to call the method**
  * pricing — [Manage prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/_auto/scopes_summary/pages/pricing)
  * pricing:read-only — [View prices](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/_auto/scopes_summary/pages/pricing_read-only)
  * finance-and-accounting — [View financial data and reports](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/_auto/scopes_summary/pages/finance-and-accounting)
  * all-methods — Full account management
  * all-methods:read-only — View all data


Calculates the cost of Market services for products with the specified parameters. The order of the items in the request and response is saved to determine, for which product the cost of the service is calculated.
Please note: the calculator performs approximate calculations. The final cost for each order depends on the services provided.
In the request, you can specify either the parameter `campaignId`, or `sellingProgram`. Sharing the parameters will result in an error.
**, Limit:** 100 requests per minute  
---  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#request)Request
POST
```
https://api.partner.market.yandex.ru/v2/tariffs/calculate

```

###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body)Body
application/json
```
{
    "parameters": {
        "campaignId": 0,
        "sellingProgram": "FBY",
        "frequency": "DAILY",
        "currency": "RUR"
    },
    "offers": [
        {
            "categoryId": 0,
            "price": 0,
            "length": 0,
            "width": 0,
            "height": 0,
            "weight": 0,
            "quantity": 1
        }
    ]
}

```

**Name** |  **Description**  
---|---  
offers* |  **Type:** [CalculateTariffsOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsofferdto)[] Products for which you need to calculate the cost of services.  
The parameters of the product for which you need to calculate the cost of services. _Min items:_ `1` _Max items:_ `200`  
parameters* |  **Type:** [CalculateTariffsParametersDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsparametersdto) Parameters for calculating the cost of services.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsofferdto)CalculateTariffsOfferDTO
The parameters of the product for which you need to calculate the cost of services.
**Name** |  **Description**  
---|---  
categoryId* |  **Type:** integer<int64> The identifier of the product category on the Market. To calculate the cost of services, you must specify the identifier _The leaf category_ the product. To find out the ID of the category to which the product belongs, use the request [POST v2/categories/tree](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/categories/getCategoriesTree). _Min value (exclusive):_ `0`  
height* |  **Type:** number The height of the product in centimeters. _Min value (exclusive):_ `0`  
length* |  **Type:** number The length of the product in centimeters. _Min value (exclusive):_ `0`  
price* |  **Type:** number The price of the product in rubles. _Min value (exclusive):_ `0`  
weight* |  **Type:** number The weight of the product in kilograms. _Min value (exclusive):_ `0`  
width* |  **Type:** number The width of the product in centimeters. _Min value (exclusive):_ `0`  
quantity |  **Type:** integer<int32> The sales quantum is the number of product units in one product offer. _Default:_ `1` _Min value:_ `1`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsparametersdto)CalculateTariffsParametersDTO
Parameters for calculating the cost of services.
**Name** |  **Description**  
---|---  
campaignId |  **Type:** integer<int64> The campaign ID. You can find it using a query [GET v2/campaigns](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/campaigns/getCampaigns) or find it in the seller's office on the Market — click on the name of your business and go to the page:
  * **Modules and APIs** → block **Sending data to Yandex.Market**.
  * **Query log** → drop-down list in the block **Show logs**.

, Do not send the store ID instead, which is indicated in the seller's account on the Market next to the store name and in some reports. The user who executes the request must have access to this campaign. Use the parameter `campaignId`, if you have already completed the activation of the store on the Market. Otherwise, an empty list will be returned. Required parameter, if no parameter is specified `sellingProgram`. Sharing the parameters will result in an error. _Min value:_ `1`  
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#currencytype) Currency codes:
  * `RUR` — the Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

_Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
frequency |  **Type:** [PaymentFrequencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#paymentfrequencytype) The frequency of payments. _Enum:_ `DAILY`, `WEEKLY`, `BIWEEKLY`, `MONTHLY`  
sellingProgram |  **Type:** [SellingProgramType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#sellingprogramtype) The placement model. **For sellers of the Yandex Go Market** The DBS and Express models are not available. Required parameter if no parameter is specified `campaignId`. Sharing the parameters will result in an error. _Enum:_ `FBY`, `FBS`, `DBS`, `EXPRESS`, `LAAS`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#currencytype)CurrencyType
Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

**Type** |  **Description**  
---|---  
[CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#currencytype) |  _Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#paymentfrequencytype)PaymentFrequencyType
Frequency of payments:
  * `DAILY` — daily.
  * `WEEKLY` — once a week.
  * `BIWEEKLY` — once every two weeks.
  * `MONTHLY` — once a month.


Read more about the payment schedule. [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/introduction/rates/acquiring.html).
**Type** |  **Description**  
---|---  
[PaymentFrequencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#paymentfrequencytype) |  _Enum:_ `DAILY`, `WEEKLY`, `BIWEEKLY`, `MONTHLY`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#sellingprogramtype)SellingProgramType
Placement model:
  * `FBY` — FBY.
  * `FBS` — FBS.
  * `DBS` — DBS.
  * `EXPRESS` — Express.

**Type** |  **Description**  
---|---  
[SellingProgramType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#sellingprogramtype) |  _Enum:_ `FBY`, `FBS`, `DBS`, `EXPRESS`, `LAAS`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#responses)Responses
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#200-ok)200 OK
The cost of services.
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body1)Body
application/json
```
{
    "status": "OK",
    "result": {
        "offers": [
            {
                "offer": {
                    "categoryId": 0,
                    "price": 0,
                    "length": 0,
                    "width": 0,
                    "height": 0,
                    "weight": 0,
                    "quantity": 1
                },
                "tariffs": [
                    {
                        "type": "AGENCY_COMMISSION",
                        "amount": 0,
                        "currency": "RUR",
                        "parameters": [
                            {
                                "name": "string",
                                "value": "string"
                            }
                        ]
                    }
                ]
            }
        ]
    }
}

```

**Name** |  **Description**  
---|---  
result |  **Type:** [CalculateTariffsResponseDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsresponsedto) The cost of services.  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsresponsedto)CalculateTariffsResponseDTO
Calculation of the cost of services.
**Name** |  **Description**  
---|---  
offers* |  **Type:** [CalculateTariffsOfferInfoDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsofferinfodto)[] The cost of services.  
The cost of services.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype)ApiResponseStatusType
The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

**Type** |  **Description**  
---|---  
[ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype) |  _Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsofferinfodto)CalculateTariffsOfferInfoDTO
The cost of services.
**Name** |  **Description**  
---|---  
offer* |  **Type:** [CalculateTariffsOfferDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatetariffsofferdto) The parameters of the product for which you need to calculate the cost of services.  
tariffs* |  **Type:** [CalculatedTariffDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatedtariffdto)[] The list of services and their cost. For some services, several different values may be returned. For example, in the FBS model, the cost of a service is `SORTING` (order processing) depends on the shipping method and the number of orders in the shipment. Read more about the tariffs for services [in the Help of the Market for sellers](https://yandex.ru/support2/marketplace/ru/introduction/rates/models/).   
Information about Yandex. Market services.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatedtariffdto)CalculatedTariffDTO
Information about Yandex. Market services.
**Name** |  **Description**  
---|---  
parameters* |  **Type:** [TariffParameterDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#tariffparameterdto)[] Tariff calculation parameters.  
Details of the calculation of a specific Market service.  
type* |  **Type:** [CalculatedTariffType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatedtarifftype) The Market service. _Enum:_ `AGENCY_COMMISSION`, `PAYMENT_TRANSFER`, `FEE`, `DELIVERY_TO_CUSTOMER`, `CROSSREGIONAL_DELIVERY`, `EXPRESS_DELIVERY`, `SORTING`, `MIDDLE_MILE`  
amount |  **Type:** number The cost of the service is in rubles.  
currency |  **Type:** [CurrencyType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#currencytype) Currency codes:
  * `RUR` — Russian ruble.
  * `UAH` — the Ukrainian hryvnia.
  * `BYR` — Belarusian ruble.
  * `KZT` — Kazakhstani tenge.
  * `UZS` — Uzbek sum.

_Enum:_ `RUR`, `USD`, `EUR`, `UAH`, `AUD`, `GBP`, `BYR`, `BYN`, `DKK`, `ISK`, `KZT`, `CAD`, `CNY`, `NOK`, `XDR`, `SGD`, `TRY`, `SEK`, `CHF`, `JPY`, `AZN`, `ALL`, `DZD`, `AOA`, `ARS`, `AMD`, `AFN`, `BHD`, `BGN`, `BOB`, `BWP`, `BND`, `BRL`, `BIF`, `HUF`, `VEF`, `KPW`, `VND`, `GMD`, `GHS`, `GNF`, `HKD`, `GEL`, `AED`, `EGP`, `ZMK`, `ILS`, `INR`, `IDR`, `JOD`, `IQD`, `IRR`, `YER`, `QAR`, `KES`, `KGS`, `COP`, `CDF`, `CRC`, `KWD`, `CUP`, `LAK`, `LVL`, `SLL`, `LBP`, `LYD`, `SZL`, `LTL`, `MUR`, `MRO`, `MKD`, `MWK`, `MGA`, `MYR`, `MAD`, `MXN`, `MZN`, `MDL`, `MNT`, `NPR`, `NGN`, `NIO`, `NZD`, `OMR`, `PKR`, `PYG`, `PEN`, `PLN`, `KHR`, `SAR`, `RON`, `SCR`, `SYP`, `SKK`, `SOS`, `SDG`, `SRD`, `TJS`, `THB`, `TWD`, `BDT`, `TZS`, `TND`, `TMM`, `UGX`, `UZS`, `UYU`, `PHP`, `DJF`, `XAF`, `XOF`, `HRK`, `CZK`, `CLP`, `LKR`, `EEK`, `ETB`, `RSD`, `ZAR`, `KRW`, `NAD`, `TL`, `UE`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#tariffparameterdto)TariffParameterDTO
Details of the calculation of a specific Market service.
**Name** |  **Description**  
---|---  
name* |  **Type:** string The name of the parameter.  
value* |  **Type:** string The value of the parameter.  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatedtarifftype)CalculatedTariffType
The Market service:
  * `AGENCY_COMMISSION` — acceptance of the buyer's payment.
  * `PAYMENT_TRANSFER` — transfer of the buyer's payment.
  * `FEE` — product placement on the Market.
  * `DELIVERY_TO_CUSTOMER` — delivery to the buyer.
  * `CROSSREGIONAL_DELIVERY` — delivery to the federal district, city or town.
  * `EXPRESS_DELIVERY` — express delivery to the buyer.
  * `SORTING` — order processing.
  * `MIDDLE_MILE` — the average mile.


Read more about Yandex.Market services [in the Help of the Market for sellers](https://yandex.ru/support/marketplace/introduction/rates/index.html).
**Type** |  **Description**  
---|---  
[CalculatedTariffType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#calculatedtarifftype) |  _Enum:_ `AGENCY_COMMISSION`, `PAYMENT_TRANSFER`, `FEE`, `DELIVERY_TO_CUSTOMER`, `CROSSREGIONAL_DELIVERY`, `EXPRESS_DELIVERY`, `SORTING`, `MIDDLE_MILE`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#400-bad-request)400 Bad Request
The request contains incorrect data. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/concepts/error-codes#400)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body2)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apierrordto)ApiErrorDTO
The general error format.
**Name** |  **Description**  
---|---  
code* |  **Type:** string The error code.  
message |  **Type:** string Description of the error.  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#401-unauthorized)401 Unauthorized
The authorization data is not specified in the request. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/concepts/error-codes#401)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body3)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#403-forbidden)403 Forbidden
The authorization data is incorrect or access to the resource is prohibited. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/concepts/error-codes#403)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body4)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#404-not-found)404 Not Found
The requested resource was not found. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/concepts/error-codes#404)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body5)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#420-method-failure)420 Method Failure
The resource access limit has been exceeded. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/concepts/error-codes#420)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body6)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#500-internal-server-error)500 Internal Server Error
Internal error of the Market. [More information about the error](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/concepts/error-codes#500)
###  [](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#body7)Body
application/json
```
{
    "status": "OK",
    "errors": [
        {
            "code": "string",
            "message": "string"
        }
    ]
}

```

**Name** |  **Description**  
---|---  
errors |  **Type:** [ApiErrorDTO](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apierrordto)[] A list of errors.  
The general error format. _Min items:_ `1`  
status |  **Type:** [ApiResponseStatusType](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/tariffs/calculateTariffs#apiresponsestatustype) The type of response. Possible values:
  * `OK` — there are no mistakes.
  * `ERROR` — an error occurred while processing the request.

_Enum:_ `OK`, `ERROR`  
Authorization
Body{ "parameters": { "campaignId": 0, "sellingProgram": "FBY", "frequency": "DAILY", "currency": "RUR" }, "offers": [ { "categoryId": 0, "price": 0, "length": 0, "width": 0, "height": 0, "weight": 0, "quantity": 1 } ] }
Send
No longer supported, please use an alternative and newer version.
Copied
A category that has no children.
### Was the article helpful?
YesNo
Previous
[Transfer of leftovers](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/stocks/updateStocks)
Next
[In the office](https://yandex.ru/dev/market/partner-api/doc/en/reference/tariffs/en/reference/business-assortment/updateBusinessPrices)
