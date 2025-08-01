# Real-Time Sports Betting Odds Dashboard

## Project Overview

This Power BI project simulates a real-world business intelligence scenario in the gambling industry. It involves building a real-time dashboard that visualizes sports betting odds from multiple bookmakers using a REST API. The objective is to support stakeholders—such as trading analysts, compliance teams, and marketers—in identifying arbitrage opportunities, monitoring bookmaker performance, and ensuring risk mitigation through data-driven decisions.

---

## Business Questions Answered

* Which bookmaker is offering the most competitive odds per event?
* Are there arbitrage opportunities between two or more bookmakers?
* What is the bookmaker's overround margin over time?
* How do implied probabilities vary across events and sports?
* Which leagues or sports present the highest arbitrage potential?

---

## Key Skills Practiced

* REST API integration and JSON data transformation in Power BI
* Handling dirty and semi-structured data using Power Query
* Data modeling with star schema and calculated tables
* Advanced DAX calculations (implied probability, overround, arbitrage flags)
* Dashboard design with slicers, matrix tables, KPI cards, and trend charts
* Requirements gathering and documentation (BRD & SRD)

---

## Tools & Technologies

* Power BI Desktop
* REST API (The Odds API or equivalent)
* Postman (for API testing)
* Power Query
* Power BI Service (optional, for deployment)

---

## Data Source

* Public REST API delivering live or mock sports betting odds in JSON format.
* Simulated dirty data injected via Power Query (nulls, inconsistent timestamps, string-encoded numbers).

---

## Data Model Summary

| Table            | Description                                               |
| ---------------- | --------------------------------------------------------- |
| `Fact_Odds`      | Betting odds data (home/draw/away) by bookmaker and event |
| `Dim_Events`     | Event metadata (teams, league, sport, time)               |
| `Dim_Bookmakers` | Bookmaker names, region, and platform                     |
| `Dim_Sports`     | Sport categories (e.g., Soccer, Basketball)               |
| `Dim_Date`       | Calendar table used for time intelligence                 |

---

## DAX Measures & KPIs

* `Implied Probability = 1 / Odds`
* `Overround = SUM(1 / Home) + SUM(1 / Draw) + SUM(1 / Away)`
* `Arbitrage Indicator` (Flag events with cross-bookmaker margin < 100%)
* `Bookmaker Spread = MAX(Odds) - MIN(Odds)`

---

## Dashboard Features

* Filters by sport, league, event, bookmaker, and time window
* KPI cards showing average overround and arbitrage count
* Matrix visual comparing odds across bookmakers per match
* Line charts for tracking odds changes over time
* Clean layout with export options for compliance use

---

## Expected Output

* Power BI `.pbix` dashboard file
* GitHub documentation (README.md, BRD.md, SRD.md)
* PDF exports for BRD and SRD for stakeholder sharing
* Cleaned and modeled dataset for reuse

---

## License

MIT or Attribution-ShareAlike (depending on data provider terms).
