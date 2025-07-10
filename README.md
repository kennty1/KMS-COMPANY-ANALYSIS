# KMS-COMPANY-ANALYSIS
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
#### This Project analyses the employee Data which contains detailed information on education level, joining year, city, payment tier, age, gender, bench history, experience, and leave status, revealing that most employees hold Bachelor's degrees, are primarily based in Bangalore, and typically fall in the 20s to 30s age range, with a varied mix of experience levels, bench history, and a significant portion indicating prior intent to leave.
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
 + To analyze employee attributes 
 + To understand the factors influencing employee attrition  
 + To predict whether an employee is likely to leave the company based on demographics, experience, and job-related features.
---
## Tools Used
+ MICROSOFT EXCEL
+ POWER BI
+ SQL
---
  
  
# Analysis and Insight 
## 1.Excel Dashboard
#### https://ibb.co/pvsTBPvH

## 2.SQL Queries
#### https://ibb.co/CpWj0mjK

## 3.Power Bi Dashboard
#### https://ibb.co/QvszvFk3
---
# Findings
 ### 1. Majority Education Level: Most employees have a Bachelors degree.
### 2. Common Cities: The majority of employees are located in Bangalore, followed by Pune and New Delhi.
### 3. Payment Tier Distribution: Most employees are in PaymentTier 3, indicating a concentration in the highest pay level.
### 4. Age Range: Employees' ages range from early 20s to late 30s, with many in their 30s.
### 5. Gender Representation: The dataset includes both Male and Female employees, with a slight male majority.
### 6. Experience Levels: Experience varies widely, from 0 to 5 years prior to joining.
### 7. Employee Attrition (LeaveOrNot): There are both leavers (`1`) and stayers (`0`), allowing for predictive modeling on attrition behavior.


