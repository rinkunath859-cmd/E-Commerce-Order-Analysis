# 📊 Sales Performance Dashboard using Power BI

An interactive **Power BI Sales Performance Dashboard** developed to analyze sales transactions, customer behavior, and sales target achievement across multiple countries. This project demonstrates end-to-end Business Intelligence development, including data cleaning with Power Query, data modeling, DAX calculations, and interactive dashboard design.

---

## 📌 Project Overview

Organizations generate large volumes of sales data that require meaningful analysis to support strategic decision-making. This project transforms raw sales, customer, and sales target data into actionable insights through interactive dashboards.

The dashboard enables users to:

- Monitor sales performance
- Compare actual sales against targets
- Evaluate Sales Managers and Sales Teams
- Analyze customer demographics
- Identify country-wise sales trends
- Track order sources and purchasing behavior

---

## 🎯 Business Problem

A company operating across **14 countries** records customer orders through multiple sales channels such as Website, App, WhatsApp, and Others.

Due to a system bug at the beginning of the financial year, several **Order Source** values were missing. The company required a Business Intelligence solution to:

- Clean and validate the data
- Handle missing values
- Track sales performance
- Compare actual sales against targets
- Identify top-performing managers and sales teams
- Provide interactive reports for decision-making

---

# 📂 Dataset

The project consists of **three datasets**.

### Orders

Contains transaction-level information.

**Columns**

- Order ID
- Customer ID
- Customer Country
- Order Datetime
- Order Source
- Sales POC
- Order Value

---

### Customers

Contains customer information.

**Columns**

- Customer ID
- Gender
- Age
- Country
- Category

---

### Sales Targets

Contains target allocation and reporting hierarchy.

**Columns**

- Sales POC
- Sales Manager
- Sales Team
- Annual Sales Target

---

# 🛠 Tools & Technologies

- Microsoft Power BI Desktop
- Power Query
- DAX (Data Analysis Expressions)
- Microsoft Excel
- GitHub

---

# 🔄 Power Query (ETL Process)

The following data preparation steps were performed:

- Imported Excel workbook
- Verified data types
- Removed duplicate records
- Identified missing Order Source values
- Filled missing values using appropriate imputation
- Merged Sales Manager First Name and Last Name
- Validated Customer IDs
- Validated Sales POC mapping
- Checked for inconsistent data
- Loaded cleaned data into Power BI

---

# ⭐ Data Model

Relationships created:

Customers (1) ─────▶ Orders (Many)

Sales Targets (1) ─▶ Orders (Many)

Relationship Keys

- Customer ID
- Sales POC

---

# 📈 DAX Measures

The dashboard includes several calculated measures:

- Total Sales
- Total Orders
- Total Customers
- Average Order Value
- Sales Target
- Target Achievement %
- Sales Gap
- Target Status

---

# 📊 Dashboard Pages

## 1️⃣ Executive Dashboard

Features:

- Total Sales
- Total Orders
- Total Customers
- Average Order Value
- Monthly Sales Trend
- Country-wise Sales
- Sales Target Achievement

---

## 2️⃣ Sales Target Dashboard

Features:

- Target vs Actual Sales
- Sales Team Performance
- Sales Manager Performance
- Target Achievement %
- Sales Gap Analysis

---

## 3️⃣ Customer Insights

Features:

- Customer Categories
- Gender Distribution
- Average Age
- Customers Without Orders
- Customer Segmentation

---

## 4️⃣ Country Analysis

Features:

- Sales by Country
- Orders by Country
- Average Order Value
- Top Sales Managers

---

## 5️⃣ Order Analysis

Features:

- Order Source Analysis
- Monthly Orders
- Order Trends
- Country Comparison

---

# 📷 Dashboard Preview

## Executive Dashboard

<img src="Images/Executive_Dashboard.png" width="100%">

---

## Sales Target Dashboard

<img src="Images/Sales_Target_Page.png" width="100%">

---

## Customer Insights

<img src="Images/Customer_Insights.png" width="100%">

---

## Country Analysis

<img src="Images/Country_Analysis.png" width="100%">

---

## Order Analysis

<img src="Images/Order_Analysis.png" width="100%">

---

## Data Model

<img src="Images/Data_Model.png" width="100%">

---

# 📌 Key Insights

- Identified the most profitable countries based on total sales.
- Compared actual sales against annual sales targets.
- Evaluated the performance of Sales Managers and Sales Teams.
- Analyzed customer demographics and purchasing behavior.
- Identified the most frequently used order channels.
- Tracked monthly sales and order trends.
- Highlighted underperforming sales regions.
- Measured average order value across countries.

---

# 💡 Business Recommendations

- Focus marketing efforts on high-performing sales channels.
- Improve support for underperforming sales teams.
- Expand successful sales strategies across regions.
- Retain high-value customers through loyalty programs.
- Monitor data quality to prevent missing transaction information.
- Review and optimize sales targets regularly.

---

# 🚀 Dashboard Features

- Interactive KPI Cards
- Dynamic Slicers
- Drill-through Pages
- Bookmarks
- Q&A Visual
- Maps
- Conditional Formatting
- Mobile Layout
- Responsive Design

---

# 📁 Project Structure

```
Sales-Performance-Dashboard/
│
├── Dashboard/
│   └── Sales_Performance_Dashboard.pbix
│
├── Data/
│   └── Sales_Dataset.xlsx
│
├── Documentation/
│   ├── Project_Report.pdf
│   ├── Power_Query_Steps.md
│   ├── DAX_Measures.md
│   ├── Business_Insights.md
│   └── Data_Cleaning.md
│
├── Images/
│   ├── Executive_Dashboard.png
│   ├── Sales_Target_Page.png
│   ├── Customer_Insights.png
│   ├── Country_Analysis.png
│   ├── Order_Analysis.png
│   ├── Mobile_View.png
│   └── Data_Model.png
│
├── README.md
├── LICENSE
└── requirements.md
```

---

# 📌 Skills Demonstrated

- Business Intelligence
- Data Cleaning
- Power Query
- Data Modeling
- DAX
- Dashboard Design
- KPI Development
- Data Visualization
- Analytical Thinking
- Business Analysis
- Storytelling with Data

---

# 🔮 Future Enhancements

- Publish to Power BI Service
- Configure Scheduled Refresh
- Implement Row-Level Security (RLS)
- Connect to SQL Server or Azure SQL Database
- Add Sales Forecasting
- Build Real-Time Dashboards

---

# 👤 Author

**Rinku Nath**

**Aspiring Data Analyst | Power BI | SQL | Python | Excel**

GitHub: https://github.com/rinkunath859-cmd

LinkedIn: *(Add your LinkedIn profile link here)*

---

## ⭐ If you found this project useful, consider giving it a star on GitHub!
