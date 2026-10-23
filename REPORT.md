# Olist Delivery Analysis

Caio Bergamo

[Download PDF](https://github.com/caiocbergamo/Olist_Delivery_Analysis/raw/refs/heads/main/Olist-Delivery-Analysis.pdf) · [Back to project overview](README.md)

## Project Objective

I wanted to understand whether late deliveries were associated with lower customer review scores. Online reviews act as digital word-of-mouth, and the delivery experience may influence how customers evaluate a purchase. This led me to investigate how average review scores and the share of low ratings (1–2 stars) differed between early, on-time, and late deliveries. I also compared delivery volumes and late-delivery rates across months and customer states to identify seasonal patterns and regional differences in performance.

## Audience and Decisions

Companies selling through the Olist marketplace, logistics teams, and third-party delivery providers could use these findings to support capacity planning, investigate regional delays, review delivery estimates, and monitor delivery-partner performance. Comparing order volumes and late-delivery rates across months and states helps identify where further investigation is needed. For example, the higher evaluated order volumes in November and December could prompt an assessment of staffing, fulfillment capacity, and potential seasonal demand around Black Friday and Christmas. The analysis identifies patterns worth investigating but does not establish what caused them.

## Data and Scope

This analysis uses the [Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce), available on Kaggle. Three source files were selected: orders, customers, and reviews. The analysis covers all orders purchased in 2017, including those delivered or reviewed in later years. This cohort contains 45,101 orders, of which 43,426 had sufficient information to evaluate delivery timing; 43,098 of those had a review. The original source files retain records from 2016 through 2018, while the analysis is filtered to the full 2017 purchase year.

## Preparation and Methodology

I used Excel to prepare and check the data before building the Power BI report. I checked order and customer IDs, missing dates, and customer matches. Deliveries were classified as Early, On time, or Late by comparing the actual and estimated delivery dates, using calendar days. Orders without enough information to assess delivery timing were kept as Not evaluated and excluded from delivery-performance rates.

For orders with multiple reviews, I kept the review with the latest review-answer timestamp so each order had only one score. Missing reviews were excluded from review averages and low-score rates. I used formulas and PivotTables to summarize monthly and regional delivery performance and compare review scores across delivery classifications.

I then imported the prepared Orders and Customers tables into Power BI, added a calendar table, and connected the tables through their matching IDs and purchase dates. I created DAX measures for the report metrics and checked the results against Excel. Finally, I built interactive report pages for delivery performance, regional comparisons, and customer reviews, with a separate page explaining the sources and methodology.

## Key Findings

Overall, 94.35% of evaluated deliveries arrived by the estimated date, while 5.65% were late. November recorded the highest evaluated order volume of the year, with 7,288 orders, and the highest late-delivery rate at 12.40%, compared with the annual rate of 5.65%. December’s late rate fell to 7.46%, but remained above the annual rate.

![Delivery performance for orders purchased in 2017.](delivery-overview.png)

*Figure 1 — Delivery performance for orders purchased in 2017.*

Regionally, São Paulo had the most late deliveries (650), but its late rate of 3.81% was below the overall rate of 5.65%. São Paulo and Rio de Janeiro together accounted for 51.94% of late deliveries. Alagoas recorded the highest late rate at 20.71%, with 41 late deliveries out of 198 evaluated orders. Roraima had the second-highest rate at 16.67%, but this was based on only 3 late deliveries out of 18 evaluated orders, so the result requires additional caution.

![Regional delivery performance by customer state.](regional-performance.png)

*Figure 2 — Regional delivery performance by customer state.*

There were 43,098 reviewed orders with evaluated delivery timing. Of those, 5,214 (12.10%) received 1–2 stars. The overall average review score was 4.17, compared with 4.29 for early deliveries, 3.86 for on-time deliveries, and 2.32 for late deliveries. Low-score shares were 9.14% for early, 15.20% for on-time, and 61.54% for late deliveries. These results show an association between late deliveries and poorer customer reviews, but do not establish causation.

![Customer review scores by delivery classification.](customer-reviews.png)

*Figure 3 — Customer review scores by delivery classification.*

## Recommendations and Limitations

Based on these findings, I recommend reviewing fulfillment and delivery capacity before periods with higher order volumes, particularly November and December. São Paulo and Rio de Janeiro deserve attention because they accounted for more than half of late deliveries, while Alagoas warrants investigation because of its high late-delivery rate. Sellers and logistics teams could monitor delivery-partner performance by month and region and check whether estimated delivery dates reflect actual performance. These actions should be investigated and tested before deciding on changes, since the analysis does not identify the causes of the delays.

This analysis covers orders purchased in 2017 within the Olist dataset, so the findings may not reflect current performance or the wider Brazilian e-commerce market. Orders classified as Not evaluated were excluded from delivery-performance rates, and missing reviews were excluded from review averages and low-score rates. States with small samples, such as Roraima, require cautious interpretation. The analysis also does not account for factors such as product category, seller, delivery distance, or carrier, which could help explain differences in delivery performance and customer reviews. The results show associations and patterns, but do not establish causation.
