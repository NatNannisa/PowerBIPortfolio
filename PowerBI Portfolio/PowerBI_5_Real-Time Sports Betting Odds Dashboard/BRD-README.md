## Business Requirement Document

### Project Title:

Real-Time Sports Betting Odds Dashboard

### Project Owner:

BI Analyst / Data Consultant

### Project Description:

This project aims to create a real-time Power BI dashboard for monitoring betting odds from multiple bookmakers using REST APIs. The dashboard will assist the sports trading, marketing, and compliance teams in identifying arbitrage opportunities, monitoring bookmaker margins, and responding to market volatility.

### Business Problem:

Stakeholders currently use siloed or delayed odds reports, limiting their ability to act on high-margin or low-risk opportunities in real-time. This results in reduced trading performance and increased exposure to market inefficiencies.

### Business Objectives:

* Integrate a REST API providing real-time sports odds.
* Create a dashboard that compares odds across bookmakers.
* Highlight arbitrage gaps and bookmaker spread in real time.
* Support data-driven decision-making for risk, trading, and marketing teams.

### Business Requirements

| Priority | Criteria     | Requirement Description                               |
| -------- | ------------ | ----------------------------------------------------- |
| High     | Must-Have    | Integrate with a REST API to pull real-time odds data |
| High     | Must-Have    | Clean and model API data for Power BI ingestion       |
| High     | Must-Have    | Display implied probabilities and overround metrics   |
| Medium   | Should-Have  | Visualize arbitrage opportunities between bookmakers  |
| Medium   | Should-Have  | Include filters by sport, league, and bookmaker       |
| Low      | Nice-to-Have | Enable data export for further analysis in Excel      |
| Low      | Nice-to-Have | Add trend lines to compare odds changes over time     |

### Key Stakeholders and Responsibilities

| Stakeholder Role          | Name/Dept             | Duties/Responsibilities                  |
| ------------------------- | --------------------- | ---------------------------------------- |
| Project Sponsor           | Director of Analytics | Approve scope, budget, and KPIs          |
| Product Owner             | BI Analyst            | Lead development, documentation, testing |
| Sports Trading Manager    | Trading Dept.         | Define KPI needs, validate output        |
| Marketing Analyst         | Marketing Dept.       | Use output for campaign planning         |
| Risk & Compliance Officer | Compliance Team       | Ensure data legality and integrity       |
| IT Support Engineer       | Tech Team             | Assist with API access, automation       |

### Project Scope

**In Scope:**

* Connect to external REST APIs
* Clean and transform nested/delimited JSON
* Develop Power BI dashboard with key KPIs and visuals
* Document requirements, logic, and visual outputs
* Share dashboard through secure internal workspace

**Out of Scope:**

* User authentication or bet placement
* Full historical warehousing
* Complex predictive modeling

### Project Constraints

* Free API access may limit refresh frequency and data completeness
* Data refresh schedules may not meet true real-time demands (e.g., every 15 minutes)
* Complex nested JSON may require pre-processing (Python or Power Automate)
* No access to premium betting feeds without paid subscriptions

### Success Criteria

* Dashboard updates on schedule without errors
* Key KPIs (arbitrage %, implied probability, overround) visible and accurate
* At least three stakeholder groups actively use insights weekly
* Functional for at least three sports and four bookmakers

### Cost-Benefit Analysis

| Item                    | Cost Estimate (AUD)   | Description                                         |
| ----------------------- | --------------------- | --------------------------------------------------- |
| API Access (Premium)    | \$100/month           | Optional for frequent refresh and broader access    |
| Power BI Pro License    | \$20/month            | Required for publishing and sharing dashboards      |
| Developer Time          | \$2,000 one-time      | Includes setup, modeling, and dashboard development |
| Testing Tools (Postman) | Free                  | For API testing and validation                      |
| **Total Cost**          | **\$2,120 (Month 1)** | Initial investment including setup and licensing    |

| Benefit Type           | Description                                                              |
| ---------------------- | ------------------------------------------------------------------------ |
| Operational Efficiency | Enables faster response to arbitrage and market changes                  |
| Competitive Advantage  | Provides deeper insight compared to slower traditional reporting methods |
| Risk Reduction         | Identifies overround anomalies and high-risk odds scenarios              |
| Decision Support       | Assists trading and marketing with live, reliable data                   |

**Expected ROI:** Based on improved odds pricing and campaign targeting, an estimated 5x return on investment is projected within the first three months.
