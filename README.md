# KMS-COMPANY-ANALYSIS
### https://ibb.co/fY2ZwgqB
## Table of Contents
+ [Project Overview](#Project-Overview)
+ [Dataset Description](#Dataset-Description)
+ [Objectives](#Objectives)
+ [Tools Used](#Tools-Used)
+ [Analysis and Insight](#Analysis-and-Insight)   
  1. [Excel Dashboard](#excel-dashboard)
2.[SQL Queries](#sql-queries)
3.[PowerBi Dashboard](#PowerBi-Dashboard)
+ [Findings](#Findings)

## Project Overview
#### This Project analyses the KMS COMPANY  which contains detailed information sales transaction data. Each row represents a sales order record, and the dataset contains detailed information about order processing, customer demographics, product categories, pricing, shipping methods, and profitability.
---

## Data Description
| **Column**            | **Description**                                                                |
| --------------------- | ------------------------------------------------------------------------------ |
| `Row ID`              | Unique index for each entry in the dataset.                                    |
| `Order ID`            | Unique order identifier.                                                       |
| `Order Date`          | The date the order was placed.                                                 |
| `Order Priority`      | Priority level of the order (e.g., Low, Medium, High, Critical).               |
| `Sales`               | Total revenue from the order.                                                  |
| `Quantity Ordered`    | Number of items purchased.                                                     |
| `Discount`            | Discount applied to the order (as a decimal).                                  |
| `Ship Mode`           | Shipping method used (e.g., Regular Air, Express Air).                         |
| `Profit`              | Net profit from the order (can be negative for losses).                        |
| `Unit Price`          | Price per unit of the product.                                                 |
| `Shipping Cost`       | Cost of shipping for the order.                                                |
| `Customer Name`       | Name of the customer who placed the order.                                     |
| `Province` & `Region` | Location details of the customer (mostly shown as **Nunavut** in this sample). |
| `Customer Segment`    | Type of customer (e.g., Consumer, Corporate, Home Office).                     |
| `Product Category`    | Category of the product sold (e.g., Office Supplies, Furniture).               |
| `Product Name`        | Specific name of the product.                                                  |
| `Product Container`   | Packaging or container type used (e.g., Small Box, Wrap Bag).                  |
| `Product Base Margin` | Profit margin before additional costs/discounts.                               |
| `Ship Date`           | Date when the product was shipped.                                             |

---

## Objectives
+ sales performance
+ customer behavior
+ product profitability 
+ shipping efficiency  
+ optimizing operations

---
## Tools Used
+ MICROSOFT EXCEL
+ POWER BI
+ SQL
---
  
  
# Analysis and Insight 
## 1.Excel Dashboard
#### https://ibb.co/4nZ2njZP
#### https://ibb.co/VW5VkBRC

## 2.SQL Queries
#### --- Product Category with the highest sales---
SELECT Product_Category ,Sales FROM [dbo].[KMS Sql Case Study]
ORDER BY Product_Category DESC;

#### ---What are the Top 3 and Bottom 3 regions in terms of sales?---
SELECT TOP 3 * FROM [dbo].[KMS Sql Case Study]
ORDER BY Region DESC;

#### SELECT TOP 3 * FROM [dbo].[KMS Sql Case Study]
     ORDER BY Region ASC;


#### --- What were the total sales of appliances in Ontario?--
SELECT Region = 'Ontario',Product_Sub_Category='Appliances', SUM(Sales)  AS total_sales FROM [dbo].[KMS Sql Case Study]
GROUP BY Region  , Product_Sub_Category
ORDER BY Region  ,Product_Sub_Category;


#### --- KMS incurred the most shipping cost using which shipping method--
SELECT TOP 1 * FROM [dbo].[KMS Sql Case Study]
ORDER BY Ship_Mode;

 #### ---Who are the most valuable customers, and what products or services do they typically purchase?---
SELECT TOP 1 Customer_Name,Product_Category , MAX(Sales) Most_Valuable_Customer FROM [dbo].[KMS Sql Case Study]
GROUP BY Customer_Name,Product_Category
ORDER BY Customer_Name,Product_Category DESC;

#### ---Which small business customer had the highest sales?---
SELECT TOP 1 Customer_Name, Customer_Segment = 'Small Business',  MAX(Sales)  FROM [dbo].[KMS Sql Case Study]
GROUP BY Customer_Name, Customer_Segment
ORDER BY Customer_Name,Customer_Segment ;

#### ---Which Corporate Customer placed the most number of orders in 2009 – 2012?---
SELECT  TOP 1 Customer_Name, Order_Date  FROM [dbo].[KMS Sql Case Study]
WHERE [Order_Date]>= '2009' AND [Order_Date]<= '2012'
ORDER BY Customer_Name,Order_Date DESC;

## 3.Power Bi Dashboard
#### https://ibb.co/Ng9Cw3DF
#### https://ibb.co/rRTKCHzx
---
# Findings

 ### 1. The dataset includes historical orders dating as far back as 2011 and 2012, which allows for long-term trend analysis.

### 2. All customer entries shown are from Nunavut, indicating either a filtered view or a regional focus for the analysis.

### 3. The most common shipping method is "Regular Air", followed by "Express Air", suggesting a preference for faster delivery services.

### 4. Several orders show negative profit values, indicating that some sales were made at a loss—possibly due to high discounts or shipping costs.

### 5. Discounts are applied at various rates (e.g., 0.03 to 0.25), which could be linked to customer segment, order priority, or promotional offers.

### 6.The dataset includes a wide range of product categories such as Office Supplies, Furniture, and Technology—each with specific product names and packaging types.

### 7.Orders have different priorities such as Low, High, Medium, Not Specified, andCritical, which may influence delivery timelines and profit margins.

### 8. Sales amounts and quantity ordered vary significantly, showing a mix of small and large orders, possibly from both individuals and businesses.





