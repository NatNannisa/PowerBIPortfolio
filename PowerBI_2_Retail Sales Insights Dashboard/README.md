# Retail Sales Insights Dashboard – Power BI Portfolio Project (Level 2)

## Project Overview

This project simulates the role of a Business Intelligence Analyst for a retail chain. The goal is to design an interactive Power BI dashboard that provides executives with sales insights, customer segmentation, and store performance analytics, using multiple related data sources.

The solution demonstrates skills in data modeling, DAX measures, calculated columns, and relationship management across multiple tables. All data used in the project was generated using Python and Faker to simulate a realistic retail environment.

---

## Business Questions Addressed

- Which stores, products, and customer segments are performing best?
- How does profitability vary across different regions and categories?
- Which product types experience the highest return rates, and why?
- What are the trends in monthly sales and profit performance?
- Which customer demographics generate the most value?

---

## Data Model Summary

| Table      | Description |
|------------|-------------|
| `Sales`    | Transactional data including order ID, product ID, quantity, sales amount |
| `Products` | Product metadata including category, sub-category, and unit cost |
| `Customers`| Demographic and segmentation data |
| `Stores`   | Store-level information such as location and region |
| `Returns`  | Records of product returns and reasons |
| `Calendar` | Auto-generated calendar table used for time intelligence |

This project follows a star schema with `Sales` as the fact table and others serving as dimensions.

---

## Tools and Technologies Used

- Power BI Desktop
- DAX (Data Analysis Expressions)
- Python (pandas, Faker – for data generation)
- GitHub (version control and portfolio documentation)

---

## Key DAX Measures

```DAX
Total Sales = SUM(Sales[Sales_Amount])

Total Profit = SUM(Sales[Profit])

Avg Order Value = DIVIDE([Total Sales], DISTINCTCOUNT(Sales[Order_ID]))

Profit Margin = DIVIDE([Total Profit], [Total Sales])

Return Rate = DIVIDE(COUNT(Returns[Return_ID]), DISTINCTCOUNT(Sales[Order_ID]))
