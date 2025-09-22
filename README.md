# Mobile_Sales_Analysis

## Overview:
**This is a sales report for Mobile Sales products**

---

## Contents
 [Project Overview](#Project-Overview)| +[Data Source](#Data-Source)| + [Data Source](#Data-Source)| + [Tables Used](#Tool-Used)| + [Table-Outlay](#Table-Outlay)| + [Query Languages)](#Query-Languages)| + [Visualization](#Visualization)| +|[Findings](#Findings)| +[Summary](#Summary)| +[Conclusion](#Conclusion)

---


## Project Overview:

>>The Mobile Sales Analysis Project focuses on exploring sales data from a mobile phone retail business to  uncover  trends, patterns, and insights that can support better decision-making, using Sales distribution by various attributes such as Brands, Customer Gender and Payment Method, Using Pivot tables, I explored metrics like total sales by payment method and gender, average income of buyers, gender distribution, and overall revenue. This analysis helps to understand the key factors driving sales in the dataset provided.

## Data Source:
www.kaggle.com/dataset

Tools Used:
 ## Tools Used:
+ Pivot Table/Charts
+ PowerBi
+ SQL

## Table Outlay:
  First Three Columns

|TransactionID|	Date	|MobileModel	|Brand	|Price	|UnitsSold|	TotalRevenue	|CustomerAge	|CustomerGender	|Location	|PaymentMethod|
|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|-------|
|79397f68-61ed-4ea8-bcb2-f918d4e6c05b	|1/6/2024|	direction	|Green Inc|	1196.95|	85	|28002.8	|32	|Female	|Port Erik|	Online|
|4f87d114-f522-4ead-93e3-f336402df6aa|	4/5/2024|right|	Thomas-Thompson	|1010.34	64	2378.82	55	|Female|	East |Linda|	Credit Card|
|6750b7d6-dcc5-48c5-a76a-b6fc9d540fe1|	2/13/2024|	summer|	Sanchez-Williams|	400.8|	95	|31322.56|	57|	Male|	East| Angelicastad|	Online|
|7da7de95-f772-4cc2-bce0-b0873f98233e|	4/17/2024	|keep|	Greer and Sons|	338.6	79|	31159.75|	46|	Other	|East| Kevin|	Cash|

## Query Languages: (SQL)
some of the query languages to retieve records are displayed here

```SQL
--- Categorise the data into Gold, Silver and Diamond---

SELECT Price,
CASE
WHEN Price <=100 THEN 'Silver'
WHEN Price >= 900  THEN 'Gold'
ELSE 'Diamond'
END AS Category
FROM[dbo].[mobile_sales1];

```

```SQL
--- 1. Customers that buys product  btw 900 and 1000---
SELECT * FROM[dbo].[mobile_sales1] 
WHERE price BETWEEN 900 and 1000;
SELECT * FROM[dbo].[mobile_sales1];
```

```SQL
---2. Retrieve the sales by payment method, arranging from largest to smallest amount---
SELECT (PaymentMethod), SUM (TotalRevenue) AS Sales FROM [dbo].[mobile_sales1]
GROUP BY (PaymentMethod)
ORDER BY Sales DESC;

```

```SQL
---3. Retrieve the most expensive brand---
SELECT MAX (Price) AS 'expensive brand', Brand FROM [dbo].[mobile_sales1]
GROUP BY Brand
ORDER BY 'Expensive brand' DESC;

```

```SQL
---4. How many brands are there?---
SELECT  COUNT (Distinct Brand) AS Number_of_brands FROM [dbo].[mobile_sales1];

```

```SQL
--- 5.Calculate Total Revenue by Payment method---
SELECT Payment method, SUM (Price) AS Total Revenue
FROM [mobile_sales1]
GROUP BY payment method
ORDER BY Total Revenue DESC;

```

## Visualization
## Pivot Tables


  ![PIVOT REAL]<img width="922" height="618" alt="Mobile sales Pivot Table " src="https://github.com/user-attachments/assets/0cb2797f-88d0-4e76-b99d-4f46e44e2d5c" />



  
<img width="1283" height="609" alt="Mobile Sales Chat" src="https://github.com/user-attachments/assets/0ade27f7-ac32-404d-ae06-76495ec4fe4e" />


### Power Bi Dashboard


<img width="1108" height="656" alt="power bi dashbord" src="https://github.com/user-attachments/assets/7dc04406-9982-408d-bdf1-04aadd74bad7" />

<img width="920" height="567" alt="power bi 3" src="https://github.com/user-attachments/assets/014fc7d4-945b-4a5f-b7df-230c6bd0a57b" />

## Findings

From the analysis of the Mobile Sales Dataset, key insights include:
+ We have more Female Customer sale
+ West Micheal is the highest sales location.
+ figure has the highest sales.

## Summary.
This project explored mobile phone sales using SQL, Excel, and Power BI to uncover business insights. The workflow included:
Database Design & Cleaning → Structured sales, customer, dealer, and product tables.
SQL Analysis → Wrote queries to calculate revenue, best-selling brands, customer loyalty, and seasonal trends.
Excel Pivot Tables → Used for quick validation and trend exploration.
Power BI Dashboard → Built interactive visualizations showing KPIs, revenue trends, and customer insights.
The analysis provided actionable insights into customer preferences, dealer performance, and revenue growth opportunities.

## Conclusion.
This Mobile Sales Analysis Project demonstrates my ability to:
Build and query relational databases for structured analysis.
Extract meaningful business insights using SQL.
Use Excel for validation and quick exploration.
Design effective Power BI dashboards for data storytelling.
The findings show how data-driven insights can help businesses:
Identify top-performing brands and models.
Optimize dealer and regional strategies.
Understand customer buying behavior.
Forecast demand based on seasonal patterns.
this project is a strong addition to my Data Analytics Portfolio, showcasing end-to-end skills from data cleaning to visualization.

