# Coffee Orders Sales Analysis Dashboard ☕

A end-to-end data analysis project built entirely in Microsoft Excel — from raw messy data to a fully interactive sales dashboard. This project covers real-world data cleaning techniques and business-focused visualizations that help answer key sales questions at a glance.

---

## 🔍 Project Background

This project was built around a coffee retail dataset containing order transactions, customer details, and product information. The raw data had missing values, inconsistent formats, and required multiple tables to be linked together — pretty much what you'd encounter working with real business data.

The goal was simple: clean everything up and turn it into something a business stakeholder could actually use to make decisions.

---

## 🗂️ What's Inside the Excel File

The workbook is organized into the following sheets:

| Sheet | Description |
|---|---|
| `Dashboard` | Interactive dashboard with slicers and charts |
| `orders` | Main orders table with all cleaned and enriched data |
| `customers` | Customer details including country and loyalty status |
| `products` | Product catalogue with pricing and profit margins |
| `TotalSales` | Pivot table — sales breakdown by coffee type over time |
| `CountryBarChart` | Pivot table — total sales by country |
| `Top5Customers` | Pivot table — top 5 customers by revenue |

---

## 🧹 Data Cleaning & Preparation

The raw orders sheet only had basic fields like Order ID, Customer ID, and Product ID. Here's what was done to get it analysis-ready:

- **Pulled in customer data** (name, email, country, loyalty card status) using `XLOOKUP` from the customers table
- **Pulled in product data** (coffee type, roast type, size, unit price) using `INDEX MATCH` from the products table
- **Calculated total sales** by multiplying unit price with quantity ordered
- **Expanded abbreviations** into full readable labels using nested `IF` statements:
  - Coffee types: `Rob → Robusta`, `Exc → Excelsa`, `Ara → Arabica`, `Lib → Liberica`
  - Roast types: `M → Medium`, `L → Light`, `D → Dark`
- **Handled blank email fields** — used `IF` with `XLOOKUP` to return empty string instead of 0 for customers without emails
- **Formatted date and size columns** for consistency

---

## 📈 Dashboard Features

The dashboard was designed to give a quick but comprehensive view of sales performance:

- **Total Sales Over Time** — line chart showing monthly revenue trends broken down by coffee type
- **Sales by Country** — horizontal bar chart comparing revenue across the US, Ireland, and the UK
- **Top 5 Customers** — bar chart highlighting the highest-spending customers
- **Interactive Slicers** — filter the entire dashboard by roast type, package size, and loyalty card status
- **Timeline Filter** — drill into any specific time period with a dynamic date slicer

---

## 🛠️ Tools & Techniques Used

- **Microsoft Excel** — the only tool used, start to finish
- `XLOOKUP` — for joining customer data to the orders table
- `INDEX MATCH` — for pulling product details dynamically
- Nested `IF` statements — for label formatting and handling blanks
- **Pivot Tables** — for aggregating sales by time, country, and customer
- **Pivot Charts** — for all dashboard visualizations
- **Slicers & Timeline** — for interactivity

---

## 💡 Key Insights

- The **United States** drives the majority of total revenue compared to Ireland and the United Kingdom
- **Liberica and Excelsa** show noticeable sales spikes during certain months, suggesting seasonal demand
- A small group of **top 5 customers** contribute a significant share of overall revenue — typical of retail patterns
- Customers with a **loyalty card** tend to appear more frequently in high-value orders

---

## 🚀 How to Use This File

1. Download `coffeeOrdersProject.xlsx`
2. Open it in **Microsoft Excel** (2016 or later recommended for full XLOOKUP support)
3. Head to the **Dashboard** sheet
4. Use the **slicers on the right** to filter by roast type, size, or loyalty card
5. Use the **timeline at the top** to zoom into a specific date range

---

## 📁 Repository Structure

```
coffee-orders-project/
│
├── coffeeOrdersProject.xlsx    # Main Excel workbook
├── dashboard.png               # Dashboard screenshot
└── README.md                   # You are here
```

---

## 🙋‍♂️ About This Project

This is a self-initiated data analytics project aimed at practising real-world Excel skills — specifically around data cleaning, formula-based data enrichment, pivot analysis, and dashboard design. The dataset was sourced for learning purposes and all analysis was done independently.

If you have any feedback or suggestions, feel free to open an issue or reach out directly.
