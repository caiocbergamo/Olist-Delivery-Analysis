# Data Source and Methodology

Source: [Brazilian E-Commerce Public Dataset by Olist](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), published by Olist.

Source license: [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Source Files Used

- `olist_orders_dataset.csv`
- `olist_customers_dataset.csv`
- `olist_order_reviews_dataset.csv`

Download the original CSV files from the source page. Unused source tables are not required for this analysis.

## Changes Made for This Project

Caio Bergamo prepared the data in Excel, checked identifiers and joins, retained one review per order using the latest review-answer timestamp, and added delivery classifications and review helper fields. The prepared Orders and Customers tables were imported into Power BI, where a calendar table, relationships, and DAX measures support the report.

The workbook retains records across the source years. The report analyzes orders purchased in 2017, including deliveries and reviews recorded later. Delivery timing is evaluated only for delivered orders with both actual and estimated delivery dates.

The project files contain data derived from the Olist dataset. Olist is credited as the original data provider. This independent portfolio project is not endorsed by Olist.

## Metric definitions

| Metric | Definition |
| --- | --- |
| Evaluated delivery | Delivered order with actual and estimated delivery dates |
| Late-delivery rate | Late orders ÷ orders with evaluated delivery timing |
| Delivered by estimated date | Early plus on-time orders ÷ evaluated orders |
| Average review score | Mean retained score across reviewed orders in the selection |
| Low-score share | Reviewed orders with 1–2 stars ÷ reviewed orders in the selection |

The report cohort is selected using purchase dates in 2017. Calendar dates determine early/on-time/late classification. Review comparisons use reviewed orders with evaluated delivery timing.

## Validation and limitations

The release workbook reconciles to 45,101 orders purchased in 2017, 43,426 evaluated deliveries, and 43,098 reviewed evaluated orders. Delivery classifications, latest-review selection, and the reported month/state/review comparisons were independently recomputed. Power BI model relationships and measure definitions were inspected. Native Power BI rendering and interactive refresh were not rerun during the repository review.

The results describe an observational historical cohort. Excluded delivery/review records and small state samples affect interpretation, and the analysis does not establish causation.

[Back to project overview](README.md) · [Read the analysis report](REPORT.md)
