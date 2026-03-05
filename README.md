# E-commerce Store Analysis
*Analyzing the data and creating a Dashboard to gain insights about the trends and patterns in Sales.*

## 📖 Table of Contents
- [Project Overview](#-project-overview)
- [Data Source](#-data-source)
- [Tools & Technologies](#-tools--technologies)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [Key Insights](#-key-insights)
- [Recommendations](#-recommendations)
- [How to Use](#-how-to-use)

## 📊 Project Overview
Analyzing the data and creating a Dashboard to gain insights about the trends and patterns in Sales.

## 🗂️ Data Source
Dataset obtained by Web scraping. **Size:** 188 kb. **Key Variables:** Sales ID, Order Date, Customer ID, Product ID, Store ID, Quantity, Unit Price, Discount, Payment Type, Total amount.

## 🛠️ Tools & Technologies
- **Visualization:** MS Excel
- **Documentation:** MS Word

## 🧹 Data Cleaning & Preparation
1.	Replaced “C-“ with “CUST” in Customer ID column in Customer Dim.

2.	Cleaned, Trimmed and Propered Name column in Customer Dim using formula: =PROPER(CLEAN(TRIM(C2)))

3.	Replaced “United States of America” with “USA” for consistency.

4.	Replaced Blank cells with “Unknown” in Loyalty Level column.

5.	Replaced “P-“ with “PROD” in Product ID column in Product Dim.

6.	Formatted “Cost” column to Currency format.

7.	Imputed the blank cells in “Cost” column with average value.

8.	Replaced “stock” column empty cells with “Unknown”.

9.	Replaced blank unit prices with average value in “Sales Fact” sheet using formula: =IF(ISBLANK([@[Unit_Price]]),AVERAGE([Unit_Price]),[@[Unit_Price]])

10.	Imputed blank cells in quantity column using the formula:
=IF(ISBLANK([@Quantity]),ROUNDUP(([@[Total_Amount]]+[@[Discount amount]])/[@[Unit_Price]],0),[@Quantity])
11.	Added a column “Discount amount” for calculation purposes.

## 🔍 Exploratory Data Analysis (EDA)
What were the main questions you explored?
- What is the overall sales trend?
- Is there a correlation between price and customer rating?

> **Tip:** Insert a screenshot of one key visualization here to catch the reader's eye.

## 💡 Key Insights
List your top 3–5 findings in bullet points.
- **Insight 1:** Sales peaked in Q4, primarily driven by holiday promotions.
- **Insight 2:** Customers aged 25-34 have the highest lifetime value.

## 🚀 Recommendations
Translate your insights into actionable business advice.
- "Increase marketing budget for the 25-34 demographic."
- "Re-evaluate the pricing strategy for low-performing regions."

## ⚙️ How to Use
Explain how someone else can run your project.
- List dependencies (e.g., `pip install -r requirements.txt`).
- Provide instructions for running the notebook or script.
