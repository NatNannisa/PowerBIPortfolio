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


## Key Insights

- Beauty and Electronics were the highest-performing categories, highlighting strong demand in self-care and technology products.
- Store 6 achieved high sales with a comparatively low return rate, indicating operational efficiency or better customer satisfaction.
- Home & Garden products had the lowest total profit, suggesting pricing challenges or higher-than-average return rates.
- Nutricosmetic-style products (e.g., Beauty) were most popular among younger customers aged 25–39.
- A noticeable decline in sales was observed between May and July, suggesting a seasonal dip or the absence of effective promotions during that period.

## Strategic Recommendations

- Improve profitability in underperforming categories (e.g., Home & Garden) by analyzing product return reasons and revisiting inventory or supplier strategies.
- Identify and replicate the success factors of Store 6 (e.g., customer service, store layout, or localized campaigns) in lower-performing locations.
- Implement seasonal campaigns in mid-year months (June–July) to address the identified dip in consumer spending.
- Allocate marketing budgets toward Beauty and Electronics, the top drivers of revenue and customer engagement.
- Enhance customer segmentation by offering loyalty programs tailored to high-value age groups (25–39) and developing email-based campaigns for higher-income segments.
- Use return rate patterns to refine product recommendations and inventory stocking, particularly for high-return categories like Clothing and Toys.

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

