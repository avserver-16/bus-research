# Bus Route Market Intelligence & Analytics

## Overview

This project is a data-driven analytics platform built to identify profitable intercity bus routes, analyze market competition, evaluate pricing opportunities, and uncover expansion possibilities in the Indian bus transportation ecosystem.

Using a Pan-India bus routes dataset, the system performs route-level intelligence analysis by processing:

* Route frequency
* AC vs Non-AC demand
* Bus type categorization
* Seat analysis
* Pricing intelligence
* Competition analysis
* Expansion opportunity detection

The project transforms raw transportation data into actionable business insights for:

* Bus operators
* Fleet management companies
* Travel startups
* Transportation analysts
* Mobility investors
* Route planning teams

---

# Features

## Data Cleaning & Processing

The system automatically:

* Extracts AC / Non-AC classification
* Detects Sleeper / Semi-Sleeper / Seater buses
* Extracts seat counts from bus descriptions
* Handles missing values using statistical techniques
* Removes noisy and low-frequency routes

---

# Dataset Attributes

The processed dataset contains:

| Column              | Description                            |
| ------------------- | -------------------------------------- |
| From                | Origin city                            |
| To                  | Destination city                       |
| Operator            | Bus operator name                      |
| Distance            | Route distance in KM                   |
| Duration            | Travel duration                        |
| Departure           | Departure timing                       |
| Arrival             | Arrival timing                         |
| AC                  | 1 = AC, 0 = Non-AC                     |
| Type                | Sleeper / Semi Sleeper / Seater        |
| No_of_Seats         | Total seat capacity                    |
| Pricing             | Estimated ticket pricing               |
| Route               | Combined route identifier              |
| Frequency           | Number of buses operating on the route |
| No_of_Bus_Operators | Total unique operators on the route    |

---

# Pricing Engine

Dynamic pricing rules were created using:

* Distance
* AC availability

Pricing slabs:

| Distance Range | AC    | Non-AC |
| -------------- | ----- | ------ |
| 0–500 KM       | ₹1000 | ₹600   |
| 500–1500 KM    | ₹2500 | ₹1500  |
| 1500–2500 KM   | ₹4000 | ₹2000  |
| 2500+ KM       | ₹5500 | ₹2500  |

---

# Analytics Performed

## 1. Route Frequency Analysis

Identifies:

* Most traveled routes
* High-demand corridors
* Transport hubs

---

## 2. Competition Analysis

Calculates:

* Number of unique operators per route
* Market saturation
* Competitive intensity

---

## 3. Opportunity Detection

Detects:

* Under-served routes
* High-demand low-competition markets
* High-margin expansion opportunities

### Opportunity Formula

Opportunity Score =

(Pricing × Frequency) / Number of Operators

Higher score indicates:

* Better profitability
* Strong demand
* Lower competition

---

## 4. Expansion Intelligence

Generated:

* Top 10 routes in every pricing category
* Best routes for business expansion
* Low competition corridors

---

## 5. Route Segmentation

Routes are segmented into:

* Budget routes
* Mid-range routes
* Premium routes
* Long-distance premium corridors

---

# Output Files Generated

| File                              | Purpose                                   |
| --------------------------------- | ----------------------------------------- |
| Cleaned_Bus_Routes.csv            | Final cleaned dataset                     |
| Top_10_Routes.xlsx                | Top opportunity routes by pricing segment |
| UnderServed_HighDemand_Routes.csv | Best expansion opportunities              |

---


# Core Algorithms Used

## Data Extraction

* Regex-based seat extraction
* String parsing for AC detection
* Bus type classification

## Statistical Processing

* Mean imputation
* Mode imputation
* Frequency analysis
* GroupBy aggregation

## Business Intelligence

* Opportunity scoring
* Competition analysis
* Pricing segmentation
* Market demand estimation

---

# Business Use Cases

This project can be extended into:

## Fleet Expansion Engine

Identify:

* Which cities to expand into
* Which routes generate maximum returns
* Which corridors are under-served

---

## Dynamic Pricing Platform

Implement airline-style pricing strategies based on:

* Demand
* Competition
* Distance
* Bus type

---

# How to Run

## Install Dependencies

```bash
pip install pandas numpy openpyxl
```

---

## Run Analysis

```bash
python research.py
```

---

# Project Structure

```bash
bus-research/
│
├── Pan-India_Bus_Routes.csv
├── Cleaned_Bus_Routes.csv
├── UnderServed_HighDemand_Routes.csv
├── Top_10_Routes.xlsx
├── research.ipynb
├── research.py
└── README.md
```

---

# Vision

The long-term vision of this project is to build a complete Bus Market Intelligence Platform capable of:

* Predicting profitable routes
* Optimizing fleet deployment
* Assisting operators in expansion decisions
* Creating dynamic pricing strategies
* Delivering real-time transportation analytics

---

# Author

## Avish Vijay Shetty

Bus Transportation Analytics & Market Intelligence Project
