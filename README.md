# Customer Complaints & Privacy Risk Analytics Platform

## Overview

This project builds an end-to-end analytics platform to analyze financial customer complaints related to privacy and identity theft in a regulated environment.

The objective is to automate root-cause analysis, identify high-risk regulatory complaints, and provide a self-service dashboard for compliance and operations teams, simulating the work of a Global Complaints & Privacy Analytics team (such as at American Express).

---

## Architecture

The solution follows a simplified Medallion-style pipeline:

Bronze Layer  
- Raw complaint extraction from the CFPB public dataset using SQL in Google BigQuery  

Silver Layer  
- Data cleaning and PII masking applied to sensitive text fields  

Gold Layer  
- AI-enriched dataset generated in Python with automated complaint category and risk classification  

Presentation Layer  
- Executive-grade Power BI dashboard for monitoring and investigation  

Although implemented in a single SQL script for simplicity, the logic clearly separates ingestion and governance steps.

---

## Tech Stack

- Google BigQuery  
- SQL (Filtering, Regex, Data Cleaning)  
- Python (Pandas, Rule-based NLP)  
- Power BI  
- Medallion Architecture (Bronze, Silver, Gold)  

---

## Key Features

- Domain-focused extraction of credit card, privacy, and identity-theft complaints  
- PII masking for emails and phone numbers in a regulated data context  
- Automated complaint categorization and regulatory risk scoring  
- Executive KPIs for compliance monitoring  
- High-risk investigation panel for operations teams  

---

## Dashboard and Pipeline Screenshots

### Power BI Dashboard

![Power BI Dashboard](https://github.com/Adarsh-Singh-codes/customer-complaints-privacy-analytics/blob/main/screenshots/Screenshot%20(329).png)

This dashboard provides executive KPIs, category distribution, risk distribution, and a high-risk investigation panel for compliance monitoring.

---

### Python NLP Processing

![Python NLP](https://github.com/Adarsh-Singh-codes/customer-complaints-privacy-analytics/blob/main/screenshots/py.png)

This notebook performs automated complaint categorization and regulatory risk classification using rule-based NLP in Python.

---

### BigQuery SQL Pipeline

![BigQuery Pipeline](https://github.com/Adarsh-Singh-codes/customer-complaints-privacy-analytics/blob/main/screenshots/gcp.png)

This shows the Bronze and Silver layer SQL pipeline implemented in Google BigQuery, including domain filtering and PII masking.

---

## KPIs and Analytics

The dashboard provides the following key metrics and views:

- Total Complaints  
- High Risk Complaints  
- High Risk Percentage  
- Complaints by Category  
- Risk Level Distribution (High, Medium, Low)  
- High-Risk Complaints Investigation Table  

---

## Repository Structure

