# Olist Delivery Analysis

An independent portfolio project by Caio Bergamo, using Excel and Power BI to explore delivery performance and customer reviews.

## Explore the Project

- [Read the full project write-up online](REPORT.md).
- [Download the project write-up (PDF)](https://github.com/caiocbergamo/Olist_Delivery_Analysis/raw/refs/heads/main/Olist-Delivery-Analysis.pdf).
- [Download the complete project package](https://github.com/caiocbergamo/Olist_Delivery_Analysis/releases/download/v1.0/Olist-Delivery-Analysis-Project.zip), including the Excel workbook, Power BI report, editable Word write-up, PDF, and dashboard screenshots.
- [Data source and attribution](DATA_SOURCE.md).

### Delivery Overview

![Delivery overview for orders purchased in 2017](delivery-overview.png)

### Regional Performance

![Regional delivery performance by customer state](regional-performance.png)

### Customer Reviews

![Customer review scores and low-score shares by delivery classification](customer-reviews.png)

## Project Objective

I wanted to understand whether late deliveries were associated with lower customer review scores. I also compared order volumes and late-delivery rates across months and customer states to identify patterns worth investigating.

## Tools Used

- Excel: data cleaning, validation, formulas, and PivotTables.
- Power Query: importing and preparing data for Power BI.
- Power BI and DAX: data modeling, measures, and interactive reporting.

## Data and Scope

Source: [Olist Brazilian E-Commerce Public Dataset on Kaggle](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), provided by Olist.

The analysis uses orders, customers, and customer reviews. It covers orders purchased in 2017, including those delivered or reviewed in later years.

- 45,101 total orders.
- 43,426 orders with evaluated delivery timing.
- 43,098 evaluated orders with a review.

## Preparation and Methodology

I checked IDs, missing dates, customer matches, and review records in Excel before building the Power BI report.

Deliveries were classified as early, on time, or late by comparing actual and estimated delivery dates, using calendar dates. Orders without sufficient delivery information were excluded from delivery-performance rates.

One review was retained per order, using the latest review-answer timestamp. Low scores were defined as 1–2 stars, and missing scores were excluded from review calculations.

## Key Findings

- 94.35% of evaluated orders arrived by the estimated date; 5.65% arrived late.
- November had the highest evaluated order volume (7,288) and late-delivery rate (12.40%).
- São Paulo and Rio de Janeiro together accounted for 51.94% of late deliveries.
- Alagoas had the highest late-delivery rate: 20.71%, based on 41 late deliveries out of 198 evaluated orders.
- Reviewed late deliveries averaged 2.32 stars, compared with 4.29 for early deliveries and 3.86 for on-time deliveries.
- Among reviewed late deliveries, 61.54% received 1–2 stars.

## Report Pages

1. Delivery Overview
2. Regional Performance
3. Customer Reviews
4. Sources and Methodology

## Recommendations and Limitations

The findings support investigating delivery capacity during busy months, regional delays, and delivery-partner performance.

Rates should be considered alongside order volumes. For example, Roraima's 16.67% late rate came from only 3 late deliveries out of 18 evaluated orders.

This analysis describes historical Olist purchases from 2017. It does not represent the entire Brazilian e-commerce market or establish that delivery timing caused review scores.


## Open and Refresh the Files

Download and extract the complete project package.

- `excel/Olist Analysis.xlsx`: prepared data, checks, formulas, PivotTables, and Excel analysis.
- `powerbi/Olist-Delivery-Analysis.pbix`: the four-page interactive report. Open it in Power BI Desktop on Windows.
- `Olist-Delivery-Analysis.pdf`: the complete project write-up.
- `Olist-Delivery-Analysis.docx`: the editable write-up.
- The three PNG files: dashboard previews.

The Power BI report includes imported data, so it can be explored without refreshing first. To refresh on another computer, go to **Transform data > Data source settings**, select the Excel source, and use **Change Source** to choose your extracted `excel/Olist Analysis.xlsx`. Apply the changes and refresh. Both Orders and Customers use this workbook.

The report covers purchases in 2017. Interactive selections change the relevant visuals; the findings labeled **Full Year 2017** remain fixed.

## Attribution and Reuse

The source dataset is provided by Olist on Kaggle under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/). The cleaned data and analytical adaptations are shared under the same license. See [data source details](DATA_SOURCE.md) and [license information](LICENSE.md).
