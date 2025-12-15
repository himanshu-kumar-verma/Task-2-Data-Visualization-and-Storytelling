# Task-2-Data-Visualization-and-Storytelling
Creating visualizations that convey a compelling story from superstore sales data.


# 📊 Superstore Sales Analysis — Power BI Dashboard Project

- This repository contains a complete end to end Business Intelligence project using Microsoft Power BI.

- The goal is to analyze Superstore sales data, identify key insights, and develop a fully interactive dashboard for business decision making.


# 📂 Project Files Included:

- superstore_final_dataset.xlsx — final cleaned dataset used for Power BI

- Superstore_PowerBI.pbix — Power BI dashboard file

- Screenshot:
  Overview dashboard
  Sales trend
  Category analysis
  Map visuals
  Customer segment visuals


# 🧾 Project Overview: 

- This project explores 4 years of Superstore data to uncover trends in:

  Sales

  Orders

  Customers

  Shipping performance

  Regional performance

  Products & profitability


# 🧹 Data Cleaning & Preparation (Power BI + Excel)

- Fixed incorrect date formats

- Mixed DMY and MDY formats corrected

- Added fields:

  Order_Date_Fixed

  Ship_Date_Fixed

  Shipping_Days

- Replaced missing values:

 - Removed orders with invalid dates

 - Filled nulls where needed


- Standardized text fields:

  Trimmed spaces

  Applied proper casing

  Corrected inconsistent state/city names


- Created a Date Table in Power BI:

  Using DAX:

DateTable = CALENDAR(MIN('Orders'[Order_Date_Fixed]), MAX('Orders'[Order_Date_Fixed]))

- Added:

  Year

  Month Name

  Shipping Days


- Created relationships in the data model:

  Orders → Customers

  Orders → Products

  Orders → Date Table


# 📈 DAX Measures Created:

  🧮 Core Measures:

Total Sales = SUM(Orders[Sales])

Total Orders = DISTINCTCOUNT(Orders[Order_ID])

Average Order Value = [Total Sales] / [Total Orders]

  📅 Time Intelligence:

YOY Sales = CALCULATE([Total Sales], DATEADD('DateTable'[Date], -1, YEAR))

  🚚 Shipping Analysis:

Average Shipping Days = AVERAGE(Orders[Shipping_Days])


# 📊 Power BI Visualizations Created:

- Dashboard Pages

- Overview Dashboard

1. KPI Cards:

  Total Sales

  Total Orders

  Average Shipping Days


- Line chart: Sales by Month and Year

- Donut: Sales by Category

- Donut: Customer Segment Performance


2. Regional Performance Dashboard:

- Filled Map:

- Sales by State

- State level tooltips

- Donut: Sales by Region


3. Product Insights Dashboard:

- Bar Chart: Top 05 Products

- Donut: Sales by Sub Category


4. Customer Segment Dashboard:

- Donut: Segment comparison Analysis



5. Shipping Analytics Dashboard:

- Avg Shipping Days by Region

- Ship Mode distribution

- Delay/negative shipping detection


# 🔍 Key Insights:

  📅 Trend Insights:

  Strong YOY growth from 2015 → 2018

  Seasonal peaks in November–December

  Lowest sales in Q1 each year


  🌎 Regional Insights: 

  West region dominates sales

  California is the top performing state

  Central and South regions underperform


  🛍️ Category Insights:

  Technology yields highest revenue

  Furniture often low margin

  Office Supplies highest order volume


  👤 Customer Segments:

  Consumer segment largest contributor

  Corporate segment highest AOV

  Home Office segment shows lowest performance


  🚚 Shipping Insights:

  Standard Class most commonly used

  Same Day shipping rarely used

  Avg shipping: 4 days


# 🎯 Recommendations Based on Insights:

🟢 Growth Opportunities:

  Focus on expanding in high performing states (CA, NY, TX)

  Invest in Technology and Office Supplies categories

  Increase marketing for Consumer and Corporate segments


🟡 Improvement Areas:

  Address Furniture profitability issues

  Improve shipping speed in Central & South regions

  Target Home Office with personalized offers


🔴 Risks to Monitor:

  Heavy dependence on a few states

  Price sensitivity in Furniture products
  
  Underutilization of Same Day shipping

