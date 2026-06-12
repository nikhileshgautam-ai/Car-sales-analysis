
# Car Sales Dashboard — Power BI

> An interactive, data-driven dashboard for tracking and analyzing car dealership sales performance in real time.

---

## Overview

This project delivers a fully dynamic **Car Sales Dashboard** built in Power BI for a car dealership looking to modernize its sales tracking. The dashboard surfaces critical KPIs and visual trends that empower stakeholders to make faster, smarter, data-driven decisions.

---

## Objectives

- Monitor year-to-date, month-to-date, and year-over-year sales performance
- Analyze average pricing and unit volume across time periods
- Identify top-performing regions, body styles, colors, and companies
- Provide an at-a-glance executive view alongside a granular detail grid

---

## KPI Metrics

### Sales Overview

| Metric | Value | DAX Formula |
|---|---|---|
| YTD Total Sales | $371.2M | `TOTALYTD(SUM('Car Data'[Price ($)]), 'Calendar Table'[Date])` |
| MTD Total Sales | $54.28M | `CALCULATE(SUM('Car Data'[Price ($)]), DATESMTD('Calendar Table'[Date]))` |
| YOY Growth | +23.6% | `[Sales Difference] / [PTYD Total Sales]` |
| YTD vs PTYD Difference | +$70.8M | `[YTD Car Sales] - [PTYD Car Sales]` |

### Average Price Analysis

| Metric | Value | DAX Formula |
|---|---|---|
| YTD Avg Price | $28.0K | `TOTALYTD([Avg Price], 'Calendar Table'[Date])` |
| MTD Avg Price | $28.26K | `TOTALMTD([Avg Price], 'Calendar Table'[Date])` |
| YOY Growth | -0.79% | `[Avg Price Diff] / [PTYD Avg Price]` |
| YTD vs PTYD Difference | -$0.22K | `[YTD Avg Price] - [PTYD Avg Price]` |

### Cars Sold Metrics

| Metric | Value | DAX Formula |
|---|---|---|
| YTD Cars Sold | 13.3K | `TOTALYTD(COUNT('Car Data'[Car ID]), 'Calendar Table'[Date])` |
| MTD Cars Sold | 1.92K | `CALCULATE(COUNT('Car Data'[Car ID]), DATESMTD('Calendar Table'[Date]))` |
| YOY Growth | +19.73% | `[Cars Sold Diff] / [PTYD Car Solds]` |
| YTD vs PTYD Difference | +3K units | `[YTD Car Solds] - [PTYD Car Solds]` |

---

## Dashboard Visuals

### 1. YTD Sales Weekly Trend *(Line Chart)*
Tracks weekly fluctuations in total sales across the year, allowing teams to spot seasonality and performance dips at a glance.

![WeeklyTrend](https://github.com/nikhileshgautam-ai/Car_sale_analysis/blob/main/Screenshots/YTD%20Sales%20Weekly.png?raw=true)

---

### 2. YTD Total Sales by Body Style *(Pie Chart)*
Breaks down revenue contribution by vehicle body type — SUV, Sedan, Hatchback, and more — to reveal product mix insights.

![YTDTotalSalesByBodyStyle](https://github.com/nikhileshgautam-ai/Car_sale_analysis/blob/main/Screenshots/YTD%20Total%20Sales%20by%20body%20style.png?raw=true)

---

### 3. YTD Total Sales by Color *(Pie Chart)*
Highlights which vehicle colors drive the most revenue, supporting smarter inventory planning decisions.

![YTDTotalSalesByColor](https://github.com/nikhileshgautam-ai/Car_sale_analysis/blob/main/Screenshots/YTD%20Total%20Sales%20by%20color.png?raw=true)

---

### 4. YTD Cars Sold by Dealer Region *(Map Chart)*
A geographic heatmap of unit sales by dealer region, helping regional managers benchmark performance across locations.

![DealerRegion](https://github.com/nikhileshgautam-ai/Car_sale_analysis/blob/main/Screenshots/MAP.png?raw=true)

---

### 5. Company-Wise Sales Trend *(Grid Table)*
A structured tabular view ranking each car company by their YTD sales figures — ideal for partner and brand-level reviews.

![CompanySalesTrend](https://github.com/nikhileshgautam-ai/Car_sale_analysis/blob/main/Screenshots/Company%20wise%20sales.png?raw=true)

---

### 6. Full Sales Details Grid *(Detail Table)*
A comprehensive record-level table covering all sale attributes: car model, body style, color, price, dealer region, date, and more.

![DetailGrid](https://github.com/nikhileshgautam-ai/Car_sale_analysis/blob/main/Screenshots/Details%20table.png?raw=true)

---

## Data Model

### Car Data Table
Fields include: `Car ID`, `Date`, `Customer Name`, `Gender`, `Annual Income`, `Dealer Name`, `Company`, `Model`, `Engine`, `Transmission`, `Color`, `Price ($)`, `Dealer No`, `Body Style`, `Phone`, `Dealer Region`

### Calendar Table *(Calculated)*
Fields include: `Date`, `Month`, `Week`, `Year`

> The Calendar Table enables time-intelligence functions (YTD, MTD, YOY) across all visuals.

---

## Dashboard Preview

![Dashboard Home 1](https://github.com/nikhileshgautam-ai/Car_sale_analysis/blob/main/Screenshots/Dash1.png?raw=true)
![Dashboard Home 2](https://github.com/nikhileshgautam-ai/Car_sale_analysis/blob/main/Screenshots/Dash2.png?raw=true)

---

## Tools & Technologies

- **Power BI Desktop** — Dashboard design and publishing
- **DAX (Data Analysis Expressions)** — KPI calculations and time-intelligence measures
- **Power Query** — Data transformation and modeling

---

## Author

**Nikhilesh Gautam**
[GitHub Profile](https://github.com/nikhileshgautam-ai)
