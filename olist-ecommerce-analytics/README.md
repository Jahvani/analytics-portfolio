# Olist E-Commerce Analytics

A Power BI report analyzing ~99,000 orders from **Olist**, Brazil's largest department-store marketplace — covering revenue, sales trends, product categories, delivery operations, and customer satisfaction, with all financial values converted to **USD**.

**[View the full report (PDF)](Olist-Report.pdf)**

---

## Overview

Olist connects small businesses across Brazil to customers through a single marketplace. This report turns the platform's raw order, payment, and review data into a dashboard that answers the questions an operator would actually ask: Where is revenue coming from? Which categories and states drive the business? And is delivery speed affecting customer satisfaction?

Built in Power BI Desktop: data cleaning and transformation in Power Query, a relational data model, and DAX measures including time intelligence (a rolling 3-month average and a same-months prior-year comparison).

**Scope:** Revenue figures cover delivered orders and count item prices only (shipping excluded), converted at a fixed 0.1916 USD per BRL. The data runs from September 2016 to August 2018, so 2016 and 2018 are partial years.

## Key Insights

- **Scale & growth:** Delivered orders generated **$2.53M** in revenue across **~96,000 orders**, an average order value of **$26.26**. Monthly revenue peaked near **$190K in November 2017** (Black Friday), and January–August 2018 revenue was **141% higher** than the same months of 2017.
- **Fulfillment:** **96,478 of 99,441 orders (97%)** reached delivered status, and only 625 (0.6%) were canceled.
- **Category concentration:** **Health & beauty, watches & gifts, and bed/bath/table** lead revenue, ahead of a long tail of smaller categories.
- **Geographic concentration:** **São Paulo alone generated $0.97M (38%)** of revenue, and the top five states (SP, RJ, MG, RS, PR) about three-quarters of it.
- **Delivery & shipping:** São Paulo orders arrive in **8.7 days** on average, versus **29 days in Roraima** (12.5 platform-wide). Shipping costs follow the same pattern: **13.9% of revenue** in São Paulo versus **28.3%** in Roraima (16.6% overall).
- **Customer satisfaction:** The average review score was **4.14** in 2018 (4.17 in 2017). By state, scores tend to drop as delivery times lengthen — São Paulo, the fastest state, has the highest score — though Amapá and Amazonas score well despite some of the slowest deliveries (26–27 days).

## Report Pages

1. **Executive Summary** — average order value, 2018 revenue vs. the same months of 2017, average review score, and scope notes.
2. **Trends & Time-Series** — monthly revenue with a rolling 3-month average.
3. **Categorical Analysis** — review score and order value by state, top and bottom states by revenue, and revenue by product category.
4. **Geo Analysis** — revenue, delivered orders, shipping cost as a share of revenue, and average delivery time by state.
5. **Outliers** — delivery time vs. customer satisfaction by state, and shipping cost vs. product price.
6. **State Performance Detail** — average delivery time, order status distribution, and a state-by-state breakdown of shipping cost.

## Tools & Techniques

- **Power BI Desktop** — report design and data modeling
- **Power Query** — data cleaning, type handling, BRL→USD conversion, splitting orders by status
- **Data model** — order, item, payment, customer, seller, product, and `Date` tables linked by relationships
- **DAX** — revenue, order, delivery, and shipping measures, plus time intelligence

## Key Measures Built

- **Revenue** (delivered orders, item prices in USD), **Delivered Orders**, **Average Order Value**
- **Rolling 3-Month Average Revenue** and **Revenue for the Same Months of the Prior Year** (time intelligence)
- **Average Review Score**, **Average Delivery Days**, **Shipping % of Revenue**
- **Average Product Price**, **Average Shipping Cost**

## Dataset

[Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle) — ~99,000 orders placed between 2016 and 2018, spanning order status, pricing, freight, payments, customer and seller location, product attributes, and review scores.
