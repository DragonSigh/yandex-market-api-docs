---
title: How to receive reports and documents | Yandex.Market API for sellers
url: https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/reports
crawled_at: 2025-09-17T14:43:22.992731
---

How to order a report or document
# How to receive reports and documents
  * [How to order a report or document](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports#generate)
  * [How do I know if a report or document is ready?](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports#status)
  * [How to get a ready-made report or document](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports#get)


The Yandex.Market API allows you to receive reports and documents. [Their types](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports#generate)
Generation takes time, so first you need to make a request for the generation itself, and then to receive the finished report or document.
Yandex MarketYour storeYandex MarketYour storeReceiving a report or documentOptional stepChecking generation statusopt​Retrieving the generated report or document after the estimatedGenerationTime has passedPOST v2/reports/<report_name>/generatePlaces the report or documentin the generation queue.OK: identifier to retrieve the generated report or document,along with the estimated generation time(reportId + estimatedGenerationTime).GET v2/reports/info/<report_id>OK: status and remaining time(status + estimatedGenerationTime).GET v2/reports/info/<report_id>OK: status and download link.If generation succeeded — status = DONE + file.If generation failed — status = FAILED or status = NODATA.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports#generate)How to order a report or document
Make a request that matches the type of report or document you need. In the request, set the settings and filters, and specify the format in which you want to get the result. The available formats are specified in the description of each method.
**Type of report or document** |  **How to start generation**  
---|---  
Closing documents |  [POST v2/reports/closure-documents/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateClosureDocumentsReport)  
Assembly Sheet |  [POST v2/reports/documents/shipment-list/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/shipments/generateShipmentListDocumentReport)  
Sales Analytics Report |  [POST v2/reports/shows-sales/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateShowsSalesReport)  
Impression Boost Report |  [POST v2/reports/shows-boost/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateShowsBoostReport)  
Sales Boost Report |  [POST v2/reports/boost-consolidated/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateBoostConsolidatedReport)  
Sales Geography Report |  [POST v2/reports/sales-geography/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateSalesGeographyReport)  
Report on the movement of goods |  [POST v2/reports/goods-movement/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateGoodsMovementReport)  
Order Report |  [POST v2/reports/united-orders/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateUnitedOrdersReport)  
Jewelry Order Report |  [POST v2/reports/jewelry-fiscal/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateJewelryFiscalReport)  
Report on key indicators |  [POST v2/reports/key-indicators/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateKeyIndicatorsReport)  
Competitive Position Report |  [POST v2/reports/competitors-position/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateCompetitorsPositionReport)  
Report on non-purchases and refunds |  [POST v2/reports/united-returns/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateUnitedReturnsReport)  
Turnover Report |  [POST v2/reports/goods-turnover/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateGoodsTurnoverReport)  
Warehouse balance report |  [POST v2/reports/stocks-on-warehouses/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateStocksOnWarehousesReport)  
Product Reviews Report |  [POST v2/reports/goods-feedback/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateGoodsFeedbackReport)  
Coverage Promotion Report |  [POST v2/reports/banners-statistics/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateBannersStatisticsReport)  
Payment report:
  * about payments for the period;
  * about the payment order;
  * about Yandex. Market points.

|  [POST v2/reports/united-netting/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateUnitedNettingReport)  
Shelf Report |  [POST v2/reports/shelf-statistics/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateShelfsStatisticsReport)  
Implementation Report |  [POST v2/reports/goods-realization/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateGoodsRealizationReport)  
Report on the cost of services:
  * by the date of service accrual;
  * by the date of the act's formation.

|  [POST v2/reports/united-marketplace-services/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateUnitedMarketplaceServicesReport)  
Report on convergence with closing documents |  [POST v2/reports/closure-documents/detalization/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateClosureDocumentsDetalizationReport)  
The Prices Report |  [POST v2/reports/goods-prices/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/generateGoodsPricesReport)  
Labels for all boxes in multiple orders |  [POST v2/reports/documents/labels/generate](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/orders/generateMassOrderLabelsReport)  
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports#status)How do I know if a report or document is ready?
Make a request [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/getReportInfo).
You will receive the status of the report or document generation and the estimated time remaining until the generation is completed.
##  [](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/reports#get)How to get a ready-made report or document
After the generation time is over, repeat the request. [GET v2/reports/info/{reportId}](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/reference/reports/getReportInfo).  
  
If the report or document has been generated, you will receive a link to download it.
### Was the article helpful?
YesNo
Previous
[DBS Refund statuses](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/dbs-return-status-model)
Next
[Product Reviews](https://yandex.ru/dev/market/partner-api/doc/en/step-by-step/en/step-by-step/goods-feedback)
