# Olist E-Commerce Analytics

An end-to-end Power BI report analyzing ~99,000 orders from **Olist**, Brazil's largest department-store marketplace — covering revenue, sales trends, product categories, seller distribution, delivery operations, and customer satisfaction, with all financial values normalized to **USD**.

---

## Overview

Olist connects small businesses across Brazil to customers through a single marketplace. This report turns the platform's raw order, payment, and review data into a decision-ready dashboard that answers the questions an operator would actually ask: Where is revenue coming from? Which categories and sellers drive the business? And is delivery speed affecting customer satisfaction?

Built end-to-end in Power BI Desktop — data cleaning and transformation in Power Query, a star-schema data model, and a layer of DAX measures including time-intelligence and target-vs-actual tracking.

## Key Insights

- **Scale & growth:** The platform delivered **$2.53M** in revenue across **~99,000 orders** (2016–2018) at an average order value of **$25.47**. Monthly revenue grew steadily, peaking near **$190K in November 2017** (Black Friday) and holding above $160K/month through 2018.
- **Operational reliability:** **~97% of orders were successfully delivered** (96K of ~99K), with cancellations under 1% — a healthy fulfillment pipeline.
- **Category concentration:** The top 3 categories — **health & beauty, watches & gifts, and bed/bath/table** — drove roughly **26%** of revenue, with a long tail of smaller categories behind them.
- **Geographic concentration:** Demand is heavily skewed to the Southeast. **São Paulo state alone generated 38.3%** of revenue and the Southeast region (SP, RJ, MG, ES) **65.4%**. São Paulo also enjoys the lowest shipping cost (13.9% of revenue) and fastest delivery (8.7 days, vs ~29 days for far-northern states).
- **Delivery drives satisfaction:** Review scores fall steadily as delivery times lengthen — **on-time orders averaged 4.29 stars versus 2.57 for late ones**. Overall satisfaction still held at **4.14**, beating the 4.0 target, but delivery speed is the clearest lever to protect it.
- **Seller long tail:** Across ~3,000 sellers, the top performers each generate ~$36–43K while the smallest earn barely $1 — an extreme long tail in which **no single seller accounts for even 2% of revenue**.

## Dashboard Walkthrough

**Executive Summary** — top-line KPIs against targets: revenue, order volume, average order value, and review score.
![Executive Summary](Dashboard%20Screenshots/01-executive-summary.png.png)

**Trends & Time-Series** — monthly revenue with a rolling 3-month average, showing steady growth and the November 2017 peak.
![Trends and Time-Series](Dashboard%20Screenshots/02-trends.png.png)

**Categorical Analysis** — revenue by product category (treemap) alongside review score and order cost by state.
![Categorical Analysis](Dashboard%20Screenshots/03-categorical.png.png)

**Seller Revenue Distribution** — top vs. bottom sellers, illustrating the marketplace's long tail.
![Seller Revenue Distribution](Dashboard%20Screenshots/04-seller%20distribution.png.png)

**Geo Analysis** — revenue distribution across Brazil, with shipping cost and delivery time broken out by state.
![Geo Analysis](Dashboard%20Screenshots/05-geo.png.png)

**Outliers** — delivery time vs. customer satisfaction, and shipping cost vs. product price, surfacing the relationships behind the headline numbers.
![Outliers](Dashboard%20Screenshots/06-outliers.png.png)

**State Performance Detail** — order lifecycle distribution and delivery performance drill-down by state.
![State Performance Detail](Dashboard%20Screenshots/07-state%20performance.png.png)

## Tools & Techniques

- **Power BI Desktop** — report design and data modeling
- **Power Query** — data cleaning, type handling, BRL→USD conversion, splitting orders by status
- **Star-schema data model** — fact tables (`order_items`, `order_payments`) joined to dimensions (`customers`, `sellers`, `products`, `geolocation`, `Date`)
- **DAX** — time intelligence, rolling averages, and target-vs-actual measures

## Key Measures Built

- **Total Revenue**, **Revenue Per Order**, **Revenue Growth Rate**
- **Rolling 3-Month Revenue** and **Previous Year Revenue** (time intelligence)
- **Revenue / Orders / Review-Score targets** with gauge tracking
- **Cancellation Rate**, **Avg Delivery Days**, **Shipping % of Revenue**
- **Avg Product Price**, **Avg Shipping Cost**

## Dataset

[Olist Brazilian E-Commerce Public Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce) (Kaggle) — ~99,000 orders placed between 2016 and 2018, spanning order status, pricing, freight, payments, customer and seller location, product attributes, and review scores.
