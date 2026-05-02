# Power BI Sales Dashboard Project

## Project Overview
This project demonstrates an end-to-end **Power BI Sales Dashboard** development process, from data cleaning to interactive visualization.

It includes:
- Data cleaning using Power Query
- Handling missing values using DAX
- Creating calculated columns
- Building interactive dashboards
- Generating business insights from sales data

---

## Files Included

| File Name | Description |
|------------|-------------|
| `Data Cleaning (Power Query).pbix` | Contains data cleaning and transformation steps |
| `My First Dashboard.pbix` | Final dashboard with visualizations |
| `README.md` | Project documentation |

---

## Data Transformation

### Orders Table

#### 1. Order Date Formatting
Formatted the `order_date` column into `DD/MM/YYYY` format for better readability.

#### 2. Sales Formatting
Formatted sales values with comma separators.

Examples:
- `1000 → 1,000`
- `25000 → 25,000`

---

## Customer Table

### 1. Handling Missing Values Using DAX
Replaced null values in the `score` column with `0`.

Created a calculated column:

```DAX
clean_score = COALESCE(customers[score], 0)
