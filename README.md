# 📊 AMAZON PRODUCT REVIEW - Capstone Project

This project was created as part of my final certification for the **Digital SkillUp Africa (DSA) Incubator Program**. It demonstrates my practical expertise using **Microsoft Excel** to analyze product and customer review data from Amazon to generate insights that can guide product improvement, marketing strategies, and customer engagement.

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

This Amazon product review analytics project analyzes data scraped from Amazon product listings, including:
- Product details (name, category, actual and discounted prices, ratings)
- Customer engagement (review counts and scores)

Each row represents a unique product, and the dataset contains:
- **1,465 records**
- **16 fields**

The project aims to generate business insights for **RetailTech Insights**, a company focused on e-commerce analytics.

---

## 📂 Data Sources

- `Amazon case study.xlsx` (provided as part of the capstone task)

---

## 🛠 Tools Used

- Excel ([Download](https://apps.microsoft.com/detail/9N4JH8NGJR9B?hl=en-us&gl=NG&ocid=pdpshare))

---

## 🧹 Data Preparation

Key actions taken:
- Removed missing/null values and unnecessary columns
- Separated and capitalized joined product categories (e.g., `Computers&Accessories` → `Computers & Accessories`)
- Converted data into a structured Excel Table (`Ctrl + T`)
- Added calculated columns:
  - **Rating Score** = Rating × Review Count
  - **Price Bucket** = `<₹200`, `₹200–₹500`, `>₹500`
  - **Potential Revenue** = Actual Price × Review Count

---

## 📊 Exploratory Data Analysis (EDA)

The following 14 business questions were addressed using PivotTables and formulas:

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

**Examples of Excel formulas and tools used:**

- **Extract Product Category**:  
  `=PROPER(SUBSTITUTE(LEFT(C2, FIND("|", C2)-1), "&", " & "))`

- **Convert Formula Output to Text**:  
  Copy → Paste as Values

- **Create Table**:  
  `Ctrl + T`

- **Insert Pivot Table**:  
  `Alt + N + V`

- **Custom Format for Revenue**:  
  `$#,##0.00,, "M"`

- **Calculated Columns**:
  - `Potential Revenue`: `=F2 * H2`
  - `Rating Score`: `=G2 * H2`
  - `Price Bucket`: `=IF(D2<200,"<₹200",IF(D2<=500,"₹200–₹500",">₹500"))`

- **Review and Discount Filters**:  
  `=COUNTIF(F2:F1465, ">=0.5")`  
  `=COUNTIF(H2:H1465, "<1000")`

---

## 🧠 Business Insights

- **751 products** had discounts of **50% or more**
- **327 products** had fewer than **1,000 reviews**
- **Categories with highest average discounts**:
  - Computers & Accessories: 94%
  - Electronics: 91%
  - Home & Kitchen: 90%
- **Top 5 high-performing categories** by combined ratings and reviews:
  - Computers & Accessories
  - Electronics
  - Home & Kitchen
  - Office Products
  - Home Improvement

---

## 📷 Dashboard Previews



---

## ✅ Recommendations

- Focus marketing on top-performing categories (e.g., Computers & Electronics)
- Re-target underperforming products with high discounts but low reviews
- Encourage more reviews for high-rating products with fewer than 1,000 ratings
- Consider adjusting pricing strategies for products in low-revenue buckets

---

## ⚠️ Limitations

- Only aggregated review data was provided; detailed review text was not analyzed
- Static Excel analysis; automation not implemented
- Regional differences in customer behavior not accounted for

---

## 📚 References

- Source: Amazon product dataset (DSA Capstone)
- Program: Digital SkillUp Africa – DSA Incubator Program

---

> Created by **Adeleke Olusegun** | Data Analytics Capstone Project | 2025
