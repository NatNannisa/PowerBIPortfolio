\# 📊 Retail Sales Insights Dashboard – Power BI Portfolio Project (Level 2)



\## 🔍 Project Overview



This project simulates the role of a \*\*Business Intelligence Analyst\*\* for a retail chain. The goal is to design an interactive Power BI dashboard that provides executives with \*\*sales insights\*\*, \*\*customer segmentation\*\*, and \*\*store performance\*\* analytics using multiple related data sources.



You’ll find use of data modeling, DAX measures, calculated columns, and relationship management across multiple tables — with realistic data generated using Python/Faker.



---



\## 🎯 Business Questions Solved



\- What are the \*\*top-performing stores\*\*, products, and customer segments?

\- How does \*\*profitability vary across regions and categories\*\*?

\- Which \*\*products have the highest return rates\*\*, and why?

\- What are the \*\*monthly sales and profit trends\*\*?

\- Which age group or customer segment is most valuable?



---



\## 🧩 Data Model



| Table        | Description |

|--------------|-------------|

| `Sales`      | Transactional data including order ID, product ID, quantity, and amount |

| `Products`   | Product details including category, sub-category, and unit cost |

| `Customers`  | Customer demographics and segmentation |

| `Stores`     | Store-level metadata |

| `Returns`    | Returned orders and reasons |

| `Calendar`   | Auto-generated calendar table for time intelligence |



Relational structure follows a \*\*star schema\*\*.



---



\## ⚙️ Tools Used



\- \*\*Power BI Desktop\*\*

\- \*\*DAX (Data Analysis Expressions)\*\*

\- \*\*Python (Faker + pandas for data generation)\*\*

\- \*\*GitHub for portfolio versioning\*\*



---



\## 📐 Key DAX Measures



```DAX

Total Sales = SUM(Sales\[Sales\_Amount])

Total Profit = SUM(Sales\[Profit])

Avg Order Value = DIVIDE(\[Total Sales], DISTINCTCOUNT(Sales\[Order\_ID]))

Profit Margin = DIVIDE(\[Total Profit], \[Total Sales])

Return Rate = DIVIDE(COUNT(Returns\[Return\_ID]), DISTINCTCOUNT(Sales\[Order\_ID]))



