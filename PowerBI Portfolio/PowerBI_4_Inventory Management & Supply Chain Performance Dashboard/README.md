# Level 4: Inventory & Supplier Performance Dashboard

## Project Overview

This Power BI dashboard represents a real-world inventory and supply chain performance solution for a retail or distribution business. It empowers operations teams to monitor stock levels, track supplier delivery efficiency, and detect potential bottlenecks using interactive visuals and DAX-powered KPIs. The model incorporates a Calendar table for time intelligence and a bridge relationship to model complex supply chain data effectively.

---

## Key Skills Practiced

* Data modeling using star schema and bridge table (`Delivery_Logs`) for many-to-many relationships
* Custom DAX measures for KPIs: stock aging, reorder flags, SLA compliance
* Calendar table integration and `USERELATIONSHIP` for delivery vs expected date comparisons
* Delivery performance analytics across multiple suppliers and regions
* Design of a clean, interactive, and stakeholder-friendly dashboard

---

## Data Sources

Synthetic data was generated using Mockaroo and Excel for realism. Tables used include:

* Inventory: ProductID, WarehouseID, Quantity, Last\_Updated
* Products: ProductID, Category, Product\_Name, Unit\_Cost
* Suppliers: SupplierID, SupplierName, SLA\_Percentage, Region
* Delivery\_Logs: ProductID, SupplierID, Delivery\_Date, Expected\_Date
* Calendar: Date, Year, Month, MonthNum, YearMonth

---

## Key Metrics

* Inventory Turnover Ratio
* Stock Aging (in days)
* Reorder Needed Flag
* On-Time Delivery Rate (per supplier)
* SLA Compliance
* Monthly Delivery Trends
* Delivery Delay Days

---

## Data Model Summary

| Table           | Description                                                                    |
| --------------- | ------------------------------------------------------------------------------ |
| `Inventory`     | Tracks product quantity by warehouse and last update date                      |
| `Products`      | Contains product metadata such as name, category, and unit cost                |
| `Suppliers`     | Supplier records with regional SLA delivery expectations                       |
| `Delivery_Logs` | Delivery transactions including delivery and expected dates for SLA comparison |
| `Calendar`      | Used for time-based calculations and visuals                                   |

---

## Key Insights

* Stock Aging Warning: Some products have been in inventory for over 90 days, increasing holding costs.
* Reorder Alerts: Approximately 15% of SKUs fall below the reorder threshold, with Warehouse 2 and 4 showing the highest urgency.
* Supplier SLA Issues: Supplier S017 and S023 consistently delivered late, with an average of 2.7 days delay.
* On-Time Delivery Trends: Overall on-time delivery is 98.8%, but performance fluctuated during peak season in Q2.
* Top Performing Supplier: Supplier S005 had 100% on-time delivery over the last 60 days.

---

## Strategic Recommendations

* Automate Restocking Alerts for SKUs that fall below reorder levels using DAX-based flags.
* Review Supplier Contracts for those breaching SLA thresholds and consider vendor diversification.
* Monitor Aging Stock and apply discounts or promotions for products held over 90 days.
* Integrate Sales Trends with inventory restock planning for more accurate demand forecasting.
* Use Delivery Logs to regularly track actual vs expected delivery trends across regions.

---

## Use Cases

* Procurement Managers: Identify late suppliers and optimize contracts.
* Inventory Controllers: Monitor low stock and aging inventory in real-time.
* Logistics Managers: Track supplier delivery performance and warehouse health.
* BI Analysts: Connect transactional delivery data with supplier SLAs and inventory levels.
