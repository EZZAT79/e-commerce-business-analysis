## Product Performance & Inventory Analysis

In this analysis, I explored retail sales performance to uncover revenue drivers, profit margin trends, seasonal demand, and inventory efficiency. Through this analysis, I applied dbt-style modeling conventions in BigQuery to transform raw data into a scalable Star Schema, and built an interactive Power BI dashboard to provide actionable insights for supply chain and marketing teams.

## Executive Summary:

Using SQL in BigQuery, my team and I modeled raw transaction and inventory data into a clean Star Schema (Fact and Dimension tables). By analyzing the data in Power BI, we found that while the platform generated €10.55M in total revenue with a healthy 51.89% profit margin, there is a significant inventory challenge: 63% of stocked items are never sold. Furthermore, while top items like "Jeans" drive high volume, "Outerwear & Coats" generate the highest average sale price (€144.65). We recommended targeted seasonal marketing for high-margin swimwear in August and a clearance strategy for the 308K items currently sitting in stock.

## Business Problem:

The business wants to understand why certain products perform better than others and how to optimize inventory. The company has data on sales transactions, product categories, and stock levels, but it is unclear which categories are actually driving the most profit versus just sitting on shelves. Our team's analysis identifies these key drivers to help the operations team reduce dead stock, improve profit margins, and better time their seasonal campaigns.

## Methodology

1. Data Preparation: Explored and cleaned raw e-commerce data (orders, products, and inventory) using SQL in BigQuery to remove timestamps, trim spaces, and round pricing.
2. Data Modeling: Applied dbt-style modeling conventions to organize data into raw, staging, intermediate, and mart layers. The final model uses a Star Schema (two Fact tables: fact_sales and fact_inventory, plus dim_products and dim_date).
3. Data Analysis (Power BI): Analyzed revenue by category, units sold vs. total profit, and monthly seasonality trends (e.g., the August peak for Swimwear).
4. Inventory Optimization: Created a flag (is_in_stock) to identify items that were stocked but never sold, helping the business see exactly how much dead stock is accumulating.
