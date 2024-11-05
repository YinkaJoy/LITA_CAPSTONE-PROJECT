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

[Recommendations](#recommendations)



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

### Basic statistics about the dataset:
Total Sales: ₦2,101,090
Total unit Price: ₦290,260
Average Sales: ₦212
Total Quantity Sold: 68,461 items
Number of Product Category: 6

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

 - Top selling products in descending order;

```SQL
SELECT product, SUM(total_sale) AS highestsellingproduct
FROM [dbo].[SalesData_Capstone]
GROUP BY product
ORDER BY highestsellingproduct DESC
```
   
### Data Visualization
---

![SALES OVERVIEW 1](https://github.com/user-attachments/assets/03046fd4-e906-48c7-80ec-d0e9ab73f988)

 1. Top Selling Products: The store has six different products across four regions. The products include shirts, shoes, hat, socks, jacket and gloves. The data suggests
   
## Insights:
 - From the total sales of ₦2,101,090 (over 2 million naira) based on my analysis **shoes** are the most popular product, with a total sales of ₦613,380 followed by shirt, hat, gloves, jacket and socks accordingly. 
   This could be due to a wide customer segment and moderate seasonality.
 - According to my findings;
     1. Shirt and Jacket have medium popularity, with high seasonality due to changing weather conditions.
     2. Hat and Gloves are niche products with low popularity, primarily appealing to outdoor enthusiasts and athletes.
     3. Socks have least popularity, with low seasonality due to consistent demand.

 - However in terms of quantity sold, **hat** became the most popular product having sold 15,929 quantity.

 2. Regional Performance: My research indicates four regions; North, South, East, West were involved in the sales of the products.
## Insights:
 - The analysis identify the **South** as the region with the highest revenue (total sales) with only three(3) out of the six products sold in the region.
 - It was also discovered that the product **shoe** made more revenue with a total sales of ₦546,300 amounting to 58.88% aproximately 59% of the total sales.
 - Refering to the dashboard below, **East** is the next popular region in term of revenue with shirt having the highest sales of 49%.
 - This data points that there is a strong correlation between Shoes and Shirt.

![SALES OVERVIEW2](https://github.com/user-attachments/assets/bd882047-95b2-4e6f-a3e1-8b575f7b43f1)

3. Yearly and monthly trend: This analysis identified a pattern of increased sales in the year 2023. The decline in sales in the year 2024 could be due to a number of factors affecting the economy as a whole.
## Insights: 
 - The graph below highlights the inconstitency in the trend of sales, showing February as the month with the highest sales and September with the lowest sale per product.

![MONTHLY TREND2](https://github.com/user-attachments/assets/ffc0394c-1d97-4d80-b615-54b3af3b8771)


 - Based on the analysis, I see an upward trend in sales in the first quarter of both year. However, a pattern of decrease in sales can be identify in the second quarter of both year.
   

![QUARTERLY TREND](https://github.com/user-attachments/assets/6547e393-9636-4c47-a811-88d22e706dca)


### Recommendations
---
 - Market Opportunities:
    1. Expand shoe offerings to cater to specific customer segments (e.g., athletic, fashion, outdoor).
    2. Develop complementary products (e.g., shoe care, accessories) to increase average order value.
    3. Target niche markets for hats and gloves through targeted marketing campaigns.

 - Product Development Strategies:
    1. Collaborate with influencers and designers to create limited-edition shoe collections.
    2. Introduce sustainable, eco-friendly sock options.
    3. Explore innovative materials and designs for hats and gloves.

 - Pricing Strategies:
    1. Maintain competitive pricing for shoes.
    2. Offer discounts for bundled products.
    3. Value-based pricing for socks.

 - Marketing Strategies:
    1. Social media campaigns targeting shoe enthusiasts.
    2. Influencer partnerships for shirts and jackets.
    3. Loyalty programs to retain customers.

### Conclusion
---
This sales data analysis highlights opportunities for growth and optimization for Deyinuad Ventures. By leveraging data insights, informed decisions can be made to drive business success."




