# Telecom KPI & Self-Service Dashboard – Power BI Portfolio Project

## Project Overview

This project simulates the role of a BI Engineer in a telecommunications company. It focuses on designing a scalable, self-service Power BI dashboard that transforms complex datasets into actionable business insights for product, marketing, and operations teams.

The solution demonstrates capabilities in defining standardized KPIs, creating curated datasets, and building reusable analytics components to support cross-functional decision-making.

## Business Questions Addressed

- What are the key drivers of customer churn?
- Which service plans generate the highest ARPU across regions?
- How does support ticket resolution time impact customer experience?
- What are the most used services and trends by customer type?
- How can stakeholders explore insights without relying on ad-hoc reporting?

## Key Skills Demonstrated

- Data modeling using star schema and role-playing dimensions
- Advanced DAX for KPI creation (e.g., churn rate, ARPU, resolution time)
- Power BI features such as bookmarks, tooltips, field parameters
- Development of curated datasets for self-service analytics
- Dashboard UX focused on simplicity, usability, and performance
- Emphasis on data quality, consistency, and governance principles

## Data Model Summary

| Table            | Description                                  |
|------------------|----------------------------------------------|
| Customers        | Customer demographics and segments           |
| Usage            | Monthly service usage and data consumption   |
| Churn            | Records of customers who discontinued service|
| SupportTickets   | Ticket resolution logs and performance metrics|
| Plans            | Telecom service packages and pricing         |
| Regions          | Regional hierarchy and location mapping      |
| Calendar         | Date table for time-based analysis           |

## Sample KPIs

- Churn Rate = (Churned Customers / Total Customers) × 100
- ARPU = Total Revenue / Active Customers
- Average Ticket Resolution Time = Total Resolution Hours / Total Tickets
- Monthly Usage Trend by Service Type and Region

## Tools and Technologies

- Power BI (DAX, Power Query)
- SQL (data transformation and modeling logic)
- Excel (for synthetic data generation)
- GitHub (version control and documentation)

## Business Impact

- Enables faster, insight-driven decisions across departments
- Reduces reliance on manual and ad-hoc reporting
- Standardizes KPIs for consistent performance tracking
- Enhances stakeholder access to relevant data without requiring technical skills

## Future Improvements

- Integrate real-time data using REST API or data gateway
- Implement row-level security (RLS) and CI/CD deployment
- Expand to include billing and customer feedback datasets
