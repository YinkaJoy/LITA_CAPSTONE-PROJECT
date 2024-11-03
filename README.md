# LITA_CAPSTONE-PROJECT
This is where I documented my first project on Data Analysis with the Incubator Hub.

### Project Title: Deyinuad Ventures Sales Performance Analysis

### Project Outline
---

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Analysis](#data-analysis)

[Data Visualization](#data-visualization)



### Project Overview
---
This project aim to analyze sales data to identify trends (such as top-selling products, regional performance, yearly and monthly sales trends), strengths, weaknesses and provide actionable insights to improve sales performance. With respect to the data gathered, I plan to develop recommendations for sales strategy adjustments.

### Data Sources
---
The primary source of Data used is the sales report provided by the sales team.

### Tools Used
---
- Microsoft Excel [Download Here](https://1drv.ms/x/c/aad348901d0848c9/ESF61RwGbDRPsMRtHpPAAg8B4I0nxZayuGCSASdE9G5hhw)
  1. For Data cleaning
  2. For Analysis.
- SQL - Structured Query Language for querying of Data [Download Here](https://sqlfiddle.com/sql-server/online-compiler?id=53b7e911-8fb7-4874-bbec-c46c06a247a3)
- PBI - Microsoft PowerBI for visualization.
- GitHub for portfolio building.

### Data Cleaning and Preparation
---
 In the intial phase when I got the data, I performed the following action;
  1. Data loading and Inspection
  2. Removed duplicates
  3. Data Cleaning and Formatting

### Exploratory Data Analysis
---
 In exploring data for effective analysis, the following questions were asked;
 - What is the total sales for each product category?
 - What is the number of sales transactions in each region?
 - Which product is the highest-selling product by total sales value?
 - What is the total revenue per product?
 - What is the monthly sales totals for the current year.
 - Who are the top 5 customers by total purchase amount?
 - What is the percentage of total sales contributed by each region?
 - Which products have no sales in the last quarter?

### Data Analysis
---
Included are some basic lines of code or queries or even some of the DAX expressions that were used during my analysis;  

 - To retrieve the total sales for each product category;

```SQL
SELECT *FROM [dbo].[SalesData_Capstone]
select product, sum(total_sale) as Totalsale from [dbo].[SalesData_Capstone]
group by product;
```

 - To find the number of sales transactions in each region;

```SQL
SELECT Region,COUNT(OrderID) AS No_of_Salestransaction FROM [dbo].[SalesData_Capstone] 
group by region;
```
   
### Data Visualization

![SALES OVERVIEW 1](https://github.com/user-attachments/assets/03046fd4-e906-48c7-80ec-d0e9ab73f988)

 1. Top Selling Products: The store has six different products across four regions. The products include shirts, shoes, hat, socks, jacket and gloves.
   
## Insights:
 - From the total sales of ₦2,101,090 (over 2 million naira) shoes sold more with a total sales of ₦613,380 followed by shirt, hat, gloves, jacket and socks accordingly.
 - In terms of quantity sold, hat became the most popular product having sold 15,929 quantity.

![SALES OVERVIEW2](https://github.com/user-attachments/assets/bd882047-95b2-4e6f-a3e1-8b575f7b43f1)



