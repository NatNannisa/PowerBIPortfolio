\# Level 3: Logistics and Inventory Performance Dashboard



\## Project Overview

This Power BI dashboard simulates a real-world business intelligence scenario within a retail logistics environment. It enables operations and supply chain teams to monitor stock levels, evaluate delivery performance, and identify inefficiencies across warehouses and suppliers. The dashboard is designed to support data-driven decision-making for inventory planning and logistics optimization.

---



\## Key Skills Practiced

\- Data modeling using star schema and role-playing dimensions

\- Advanced DAX functions for KPI creation, including USERELATIONSHIP and time intelligence

\- Development of interactive Power BI visuals: slicers, matrix tables, KPI cards, and trend charts

\- Practical application of supply chain performance metrics

\- Communication of actionable insights using clean and intuitive dashboard design

---



\## Data Sources

Synthetic data generated using Excel and Mockaroo. The following tables are included:

\- Sales: OrderID, ProductID, Quantity, OrderDate, ShipDate, WarehouseID

\- Inventory: ProductID, CurrentStock, SafetyStock, WarehouseID, LastRestockDate

\- Products: ProductID, Category, SubCategory, SupplierID

\- Suppliers: SupplierID, SupplierName, SLA\_Days

\- Warehouses: WarehouseID, Location, Region

\- Calendar: Date, Year, Month, Week, FiscalMonth

---



\## Key Metrics

\- Inventory Turnover Ratio

\- Stock-Out Rate (products below safety stock)

\- Average Days to Ship

\- On-Time Delivery Rate

\- SLA Compliance by Supplier

\- Warehouse Utilization Rate

---



\## Data Model Summary



| Table        | Description |

|--------------|-------------|

| `Sales`      | Transactional data including order ID, product ID, quantity sold, ship dates, and warehouse ID |

| `Inventory`  | Stock-level data including current quantity, safety stock, and restock dates |

| `Products`   | Product metadata including category, sub-category, and supplier ID |

| `Suppliers`  | Supplier-level data including supplier name and SLA delivery expectations |

| `Warehouses` | Warehouse details such as location, region, and warehouse ID |

| `Calendar`   | Auto-generated calendar table used for time intelligence and rolling period analysis |

---



\## Key Insights

* **Warehouse 6 (Nancyfort)** had the highest number of stock-out alerts (22.91%), indicating potential inventory replenishment delays or demand surges in that location.
* **Suppliers such as Dyer LLC and Foster, Woods \& Co.** demonstrated average delivery times above the global benchmark of 2.48 days, contributing to a higher risk of SLA non-compliance.
* **Monthly delivery performance fluctuated,** with a dip in shipping efficiency during July, signaling possible logistics constraints or delayed restocking post-June
* **Warehouse 8 consistently maintained lower stock-out alerts,** suggesting more effective inventory control or better alignment between supply and demand.
* **Sales volume peaked in March and May**, while declining sharply in July, highlighting potential seasonality or reduced promotional activity mid-year.

---



\## Strategic Recommendations

* Prioritize Replenishment Strategies in High-Risk Warehouses

Focus on Nancyfort (Warehouse 6) by setting stock-out prevention thresholds and auto-alerts to trigger earlier restocking.

* Review Supplier SLA Compliance and Lead Times

Negotiate performance improvements with suppliers exceeding average delivery time, or diversify vendors for time-sensitive products.

* Deploy Seasonal Demand Forecasting Models

Prepare for mid-year sales drops by forecasting demand and initiating targeted campaigns in Q2 and Q3.

* Replicate Best Practices from High-Performing Warehouses

Use insights from Warehouse 8 to inform cross-warehouse process improvements, such as inventory turnover rate optimization.

* Introduce SLA Monitoring Dashboard for Suppliers

Track average delivery time and compliance per supplier to enhance procurement decisions and vendor accountability.

* Integrate Sales and Inventory Trends for Proactive Planning

Link stock-out patterns with sales volume trends to improve purchasing decisions and reduce overstock or understock scenarios.

---



\## Use Cases

\- \*\*Operations Managers\*\* can use the dashboard to track inventory risk and supplier reliability.

\- \*\*Logistics Analysts\*\* can monitor delivery performance and warehouse throughput.

\- \*\*Strategic Planners\*\* can leverage insights to improve inventory forecasting and supplier management.





