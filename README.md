E Commerce Sales Performance Dashboard (Power BI)

Overview

This project is an interactive Power BI dashboard built on a transactional e commerce dataset for 2023.
It analyzes sales performance across sales managers, sales teams, product categories, customer segments, and countries to support data driven revenue and performance decisions.

Business Problem
• Monitor how effectively each sales manager, sales POC, and team is meeting or exceeding their annual sales targets.
• Identify high value countries, channels, and product categories driving order volume and revenue.
• Detect underperforming areas (low target completion, negative variance to target) for timely corrective action.

Repository Structure
├── data
│   └── E-Commerce-Data.xlsx              # Raw e commerce dataset
├── reports
│   └── E-Commerce_Sales_Dashboard.pbix   # Power BI report
└── README.md                             # Project documentation

• data/E-Commerce-Data.xlsx: Source dataset used for modeling and visuals.
• reports/E-Commerce_Sales_Dashboard.pbix: Final Power BI dashboard.

Dataset

The raw Excel file contains one sheet (Sheet1) with the following key columns:
• Customer Country
• Gender
• Age
• Category (A–E)
• Order ID
• Order Datetime
• Order Source (Website, App, WhatsApp, Other)
• Sales POC
• Order Value
• Sales Team (e.g., Alpha, Beta, Gamma, Delta, Epsilon)
• 2023 Sales Target
• Sales Manager
• Customer ID

Each row represents a single order, combining customer profile, order info, and sales ownership details.

Data Model & Measures

In Power BI, the dataset is modeled and enriched with DAX measures such as:
• Total Sales = sum of Order Value
• Total Target / 2023 Sales Target
• % Target Completion = Total Sales / Total Target
• Sales Difference = Total Sales − Total Target
• Average Order Value and other supporting KPIs
These measures are used across visuals to compare performance by manager, team, category, country, and time.

Dashboard Features

• Manager & Team Performance
• Visuals showing Total Sales, Total Target, and % Target Completion by Sales Manager and Sales Team.
• Tables and charts to quickly see who is under  or over achieving their targets.
• Customer & Category Insights
• Analysis of Category (A–E) by Order Value, number of customers, and demographics (Gender, Age).
• Identification of top performing categories and segments.
• Country & Channel Analysis
• Orders and Average Order Value by Customer Country to rank markets.
• Distribution of orders and customers across Order Sources (Website, App, WhatsApp, Other).
• Time series & Seasonality
• Monthly Count of Orders and Sum of Order Value for 2023 to understand seasonality.
• Trend of sales vs target over time for strategic monitoring.
Tools & Technologies
• Power BI Desktop for data modeling, DAX, and visualization.
• Microsoft Excel (E Commerce Data.xlsx) as the source dataset.
• DAX for KPI definitions and performance calculations.

How to Use

1. Clone this repository:
bash
git clone https://github.com/<your-username>/ecommerce-sales-dashboard.git
cd ecommerce-sales-dashboard
2. Open reports/E-Commerce_Sales_Dashboard.pbix in Power BI Desktop.
3. If prompted to locate the data source, browse to data/E-Commerce-Data.xlsx.
4. Click Refresh to load the latest data and explore the report using slicers for Sales Manager, Sales Team, Country, Category, and Order Source.

