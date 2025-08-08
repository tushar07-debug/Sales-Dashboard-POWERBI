# 📊 Power BI Sales Dashboard Project

![Power BI Logo](https://upload.wikimedia.org/wikipedia/commons/c/cf/New_Power_BI_Logo.svg)

Welcome to the **Sales Dashboard Power BI Project**! This interactive dashboard leverages **Power BI**, **DAX queries**, and **Sales Forecasting techniques** to provide deep insights into business performance and trends.

---

## 🛠️ Project Overview

This project is designed to analyze, visualize, and forecast sales data using **Power BI Desktop**. It includes:

- Creating data models using **DAX (Data Analysis Expressions)**
- Designing **visually rich interactive dashboards**
- Implementing **time-series sales forecasting**
- Exporting dashboards for sharing and collaboration

> 📁 Tools Used: Power BI Desktop | DAX | Excel | SQL (optional)

---

## 📸 Dashboard Preview

| 📈 Dashboard View | 📅 Forecast Panel 
|------------------|------------------|----------------------|
| ![Main Dashboard](./assets/dashboard-main.png) | ![Forecast](./assets/forecast.png)

---

## ✨ Features

- ✅ **Interactive Filters** for Region, Category, Year
- ✅ **KPI Cards** showing Revenue, Profit, Quantity
- ✅ **Forecasting Model** using built-in forecasting & DAX
- ✅ **Dynamic DAX Tables** & calculated columns
- ✅ **Drill-down Reports** by Product, Sub-category
- ✅ **Responsive Design** for optimal viewing
- ✅ **Export to PDF/PPT** for presentations
- ✅ **Data Refresh** support for real-time reports

---

## 🧠 DAX Queries Used

> Here are some key DAX formulas that power the dashboard:

```dax
-- Total Sales
Total Sales = SUM(Sales[Sales Amount])

-- Profit Margin %
Profit Margin % = DIVIDE(SUM(Sales[Profit]), SUM(Sales[Sales Amount]))

-- Sales Forecasting using DAX (Rolling Average)
Rolling Sales Forecast = 
    AVERAGEX(
        DATESINPERIOD('Date'[Date], LASTDATE('Date'[Date]), -3, MONTH),
        [Total Sales]
    )

-- Dynamic Year Filter
SelectedYear = SELECTEDVALUE('Date'[Year])
