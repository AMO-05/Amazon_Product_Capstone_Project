# 📊 AMAZON PRODUCT REVIEW - Capstone Project

This project is part of my final certification for the **Digital SkillUp Africa (DSA) Incubator Program**, designed to demonstrate my practical expertise in using **EXCEL** to analyze product and customer review data to generate insights that can guide product improvement, marketing strategies, and customer engagement.

---

## 📑 Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools Used](#tools-used)
- [Data Preparation](#data-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis & EXCEL Function Examples](#data-analysis--excel-function-examples)
- [Business Insights](#business-insights)
- [Dashboard Previews](#dashboard-previews)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

---

## 📌 Project Overview

This Amazon Product Review analytics project analyzes information scraped from Amazon product pages, including:
- Product details: name, category, price, discount, and ratings
- Customer engagement: user reviews, titles, and content
- Each row represents a unique product, with aggregated reviewer data stored as comma-separated values
- Total Records: 1,465 rows, Total Fields: 16 columns

The goal is to review the data to generate insights that can guide product improvement, marketing strategies, and customer engagement for **RetailTech Insights**, a company that provides e-commerce analytics solutions.

---

## 📂 Data Sources

- `Amazon case study.xlsx` – dataset details  

---

## 🛠 Tools Used

- Excel ([Download](https://apps.microsoft.com/detail/9N4JH8NGJR9B?hl=en-us&gl=NG&ocid=pdpshare))

---

## 🧹 Data Preparation

Key actions taken:
- Cleaned null/missing values
- Removal of irrelevant columns
- Formatting of joined text into properly spaced and capitalized text
- Convert data to table: 'Ctrl + T', to have a functional Excel Table
- Created calculated columns: `Rating_score`, `Price Bucket`, `Potential Revenue`

---

## 📊 Exploratory Data Analysis (EDA)

Questions answered:
- What is the average discount percentage by product category?
- How many products are listed under each category?
- What is the total number of reviews per category?
- Which products have the highest average ratings?
- What is the average actual price vs the discounted price by category?
- Which products have the highest number of reviews?
- How many products have a discount of 50% or more?
- What is the distribution of product ratings (e.g., how many products are rated 3.0, 4.0, etc.)?
- What is the total potential revenue (actual_price × rating_count) by category?
- What is the number of unique products per price range bucket (e.g., <₹200, ₹200–₹500, >₹500)?
- How does the rating relate to the level of discount?
- How many products have fewer than 1,000 reviews?
- Which categories have products with the highest discounts?
- Identify the top 5 products in terms of rating and number of reviews combined.

---

## 🧮 Data Analysis & DAX Expressions

**Key measures used in the analysis:**

- **Convert data to table**: Data table was converted to Functional Excel Table, ('Ctrl + T')
- **Product Category**: Extract text before the first pipe sign (=PROPER(SUBSTITUTE(LEFT(C2, FIND("|", C2)-1), "&", " & ")))
- **Product Category**: Convert Formula Output to Static Text (Paste as Values, C2:C1465) 
- **Pivot Table creation**: Creating a Pivot Table for data analysis via the Ribbon Method or shortcut, ('Alt + N + V')
- **Discount Percentage by Product Category**: PivotTable Field List - Row: Product Category, Value: Discount_percetage
- **Custom Format Code**: Formatting of values to reduce the millions represented thus - ('$#,##0.00,,, "k"') 
- **Potential Revenue**: '(actual_price × rating_count)', ('=F2 * H2')
- **Rating Score**: '(rating × rating_count)', ('=G2 * H2')
- **Price Bucket**: '(=IF(D2<200,"<₹200",IF(D2<=500,"₹200–₹500",">₹500"))'
- **Discount of 50% or more**: '(=COUNTIF(F2:F1465, ">=0.5"))'
- **Fewer than 1000 reviews**: '(=COUNTIF(H2:H1465, "<1000"))'
- **Sort & Filter**: Top 5 Products, highest numbers of reviews, products having discount 50% or more
- **Pivot Table**: Average discount percentage, Products count, Total review count, Average actual price vs Average discounted price, Products listed under each Category, Total number of reviews by Category,Distribution of Products rating
- **Charts** Bar Chart: Ave. discount by category, Column chart: Product count per category, Scatter plot: Rating vs Discount, Price bucket: Pie chart

---

## 🧠 Business Insights

- Discount of 50% or more: **751 Products** 
- Fewer than 1000 reviews: **327 products**
- Products with highest discounts: **Computer & Accessories (0.94), Electoronic (0.91); Home & Kitchen (0.90)**
- Top 5 products in rating & reviews: **Computer & Accessories, Electoronic; Home & Kitchen; Office Products; & Home Improvement**

---

## 📷 Dashboard Previews



---

## ✅ Recommendations



---

## ⚠️ Limitations



---

## 📚 References

- Amazon Excel file
- Digital SkillUp Africa – DSA Incubator Program

---

> Created by **Adeleke Olusegun** | Data Analytics Capstone Project | 2025
