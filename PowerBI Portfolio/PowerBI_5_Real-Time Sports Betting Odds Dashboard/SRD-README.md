# System Requirement Document (SRD) – Real-Time Sports Betting Odds Dashboard

## Overview

This SRD outlines the technical specifications, interface requirements, and non-functional expectations for a Power BI dashboard project that visualizes real-time sports betting odds via REST APIs. The document is intended to serve as a blueprint for development, data modeling, integration, and deployment.

---

## 1. Introduction

### 1.1 Product Scope

The platform connects to external REST APIs to extract sports betting odds in real time. It transforms and models the data for visualization in Power BI to support trading, marketing, and compliance decision-making.

### 1.2 Product Value

It helps identify arbitrage windows, market inefficiencies, and bookmaker competitiveness using real-time odds data.

### 1.3 Intended Audience

* BI Developers
* Data Engineers
* Sports Analysts
* Marketing Teams
* Risk & Compliance Officers

### 1.4 Intended Use

* Visual comparison of odds across bookmakers
* KPI monitoring (overround, arbitrage, implied probability)
* Historical odds tracking and trend analysis

### 1.5 General Description

A Power BI dashboard supported by a clean star schema, pulling and transforming semi-structured JSON data from sports odds APIs.

---

## 2. Functional Requirements

* Connect to one or more REST APIs to pull JSON data
* Flatten and clean API responses in Power Query
* Build calculated metrics in DAX (probability, margin, arbitrage)
* Enable filtering by sport, league, bookmaker, and time
* Display real-time odds in table, chart, and KPI card formats

---

## 3. External Interface Requirements

### 3.1 User Interface

* Interactive Power BI dashboard
* Matrix visual for odds comparison
* Line charts for odds trend
* Export capability to CSV or Excel

### 3.2 Hardware Interface

* Client systems require modern browsers
* Secure gateway for Power BI Service data refresh

### 3.3 Software Interface

* REST APIs from providers (e.g., The Odds API, Betfair)
* Power BI Desktop & Power BI Service
* Optional integration with Power Automate for scheduled refresh

### 3.4 Communication Interface

* API calls via HTTPS GET requests
* Authentication using API keys in headers or parameters

---

## 4. Non-Functional Requirements

### 4.1 Security

* API credentials encrypted or stored securely
* Power BI workspace access is role-based

### 4.2 Capacity

* Up to 10,000 events daily; must support concurrent processing

### 4.3 Compatibility

* Supports JSON data with nested structures
* Compatible with Power BI Desktop and Power BI Service

### 4.4 Reliability

* Must refresh without errors every 15 mins or on manual request

### 4.5 Scalability

* Architecture must allow for additional APIs and data sources

### 4.6 Maintainability

* Maintainable code structure and data models
* Documented API endpoints and DAX logic

### 4.7 Usability

* Dashboards must be intuitive for non-technical users
* Use standard design patterns and consistent formatting

### 4.8 Other Non-Functional

* Monitor API usage limits and handle rate limiting gracefully

---

## 5. Glossary

* **API**: Application Programming Interface
* **DAX**: Data Analysis Expressions
* **Overround**: Combined implied probabilities exceeding 100%
* **Implied Probability**: Inverse of decimal odds (1 / odds)
* **Arbitrage**: Simultaneous bets to exploit odds discrepancies

---

For full documentation, refer to `README`, dataset schema, and Power BI file in this repository.
