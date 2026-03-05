# E-commerce Store Analysis

## 📖 Table of Contents
- [Project Overview](#-project-overview)
- [Data Source](#-data-source)
- [Tools & Technologies](#-tools--technologies)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [Key Insights](#-key-insights)

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
•	While analyzing the sales numbers based on category, the Sports category has the highest sales and the Beauty category has the lowest as shown in the chart below:

<img width="718" height="449" alt="image" src="https://github.com/user-attachments/assets/5cbd646e-e120-43f9-bd22-dce1bcc73ee3" />

●	The total sales in the West region is the lowest compared to others. As the sales in the West region is comparatively lower, better strategies are required in this region.

●	By observing the quarterly sales trends, it appears to be linear. The dip in 2025 quarter 4 might be due to the fact that it was the current quarter while the data was prepared. So the overall trend is good by which the future sales will have good numbers.

●	The beauty products has the least share and the sports products has the highest share.

●	The loyalty wise sales chart indicates that the Platinum members provided the highest revenue comparatively.

●	The shares of each payment method used which indicates all of them are used more or less equally.

## 💡 Key Insights
The analysis shows that the sales trend is good and the existing strategies showed consistent results. However, attention is required in the West region as there is a significant difference in sales between this region and others. 
