# Data Source and Preparation

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
