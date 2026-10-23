# Olist Delivery Analysis

An independent portfolio project by Caio Bergamo, using Excel and Power BI to explore delivery performance and customer reviews.

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
