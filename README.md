# 📊 Ecommerce Sales Dashboard (Power BI)

### 📌 Project Overview
This project analyzes **E-commerce sales performance** using **PostgreSQL** and **Power BI**. The objective is to track **YTD performance, YoY trends, profitability**, and identify key drivers across **categories, regions, shipping types, and products** through an interactive dashboard.

### 🛠️ Tools Used
- PostgreSQL
- SQL
- Power BI (DAX, Data Modeling)
- Excel (source data)

### 📂 Data & Modeling
- Imported 2 Excel files into PostgreSQL and connected Power BI to the database
- Tables used:
  - `ecommerce_orders`
  - `us_state_long_lat`
- Created a **Date (Calendar) table** to support time intelligence (YTD, PYTD, YoY)
- Connected Calendar table to `order_date`

### 📅 Date Table (Key Columns)
- Calendar = CALENDAR(MIN(ecommerce_orders[order_date]), MAX(ecommerce_orders[order_date]))
- Year = YEAR(Calendar[Date])
- Month = FORMAT(Calendar[Date], "MMMM")
- Month Number = MONTH(Calendar[Date])

### 📊 Dashboard Highlights
- YTD Sales: $11.53M (–0.83% YoY)
- YTD Profit: $1.34M (+4.5% YoY)
- YTD Quantity: 107.2K (–7.29% YoY)
- Profit Margin: 11.58% (+5.37% YoY)

Conditional formatting and icons were applied to YoY KPIs to highlight positive and negative trends.

### Key Insights
- Profitability improved despite lower sales and quantity
- **Furniture** shows YoY growth, while **Technology** and **Office Supplies** declined
- **West region** is the top revenue contributor
- **Standard Class shipping** generates the highest revenue
- Top & Bottom products help identify strong and weak performers

### 💡 Key Learnings
- Importance of Date tables for time-based analysis
- Using DAX for YoY and YTD calculations
- Designing dashboards for both high-level and detailed insights

### 📬 Contact
Vinuta Nadiger

📧 vinuta.nadiger1@gmail.com | https://www.linkedin.com/in/vinutasnadiger/

💼 Data Analyst | Power BI | SQL | Excel
