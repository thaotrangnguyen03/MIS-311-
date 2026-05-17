# MIS-311-
Introduction of Business Analytics

Part 1: Data Analysis and Insight

# 1. Dataset Overview

This dataset contains transactional sales records collected from a supermarket retail business. The data is organised in a single worksheet named sales. The dataset consists of *254 rows* and *8 columns*, where each row represents one individual sales transaction.

# Variables Description

The dataset includes the following variables:

| Variable | Description |
|---|---|
| sale_id | Unique identification number for each sales transaction |
| branch | Supermarket branch where the transaction occurred |
| city | City where the branch is located |
| customer_type | Type of customer, such as Member or Regular |
| product_name | Name of the product purchased |
| product_category | Category of the product |
| quantity | Number of items purchased |
| total_price | Total revenue generated from the transaction |

This dataset is useful for performing *descriptive analytics* and *business analytics and insights* to better understand supermarket sales performance and customer purchasing behaviour.

The analysis can help answer questions such as:

- Which product categories generate the highest revenue?
- Which branch or city performs best in sales?
- What type of customer contributes more to total revenue?
- Which products have higher demand?
- Are there any unusual sales patterns or outliers?

The dataset is useful for performing descriptive and business analytics to understand customer purchasing behaviour, sales performance across branches and cities, product demand, and revenue trends. It can support visualisation techniques such as pie charts, box plots, pivot tables, and comparative analysis for decision-making in retail management.

# 2. Data Cleaning

Three duplicate rows were identified in the dataset and removed to prevent repeated sales transactions from affecting the analysis results. After removing duplicate records, the dataset became more reliable and suitable for descriptive statistics and correlation analysis.

Because the same transaction may be counted more than once, duplicate rows might skew the analysis's findings and produce erroneous revenue, averages, and business insights.

<img width="1878" height="966" alt="image" src="https://github.com/user-attachments/assets/4d606605-acf7-439f-8688-4545c5c73d8f" />

This step focused on examining the dataset to identify missing values, duplicate records, and inconsistencies before conducting further analysis and building summary tables. After the inspection process, the dataset contained 3 missing values in the customer_type column, 6 missing values in the product_category column, and 3 missing values in the quantity column, resulting in a total of 12 missing data points. In addition, 3 duplicate rows were identified and removed to improve data accuracy and reliability.

Firstly, missing values in the customer_type field were addressed using the Mode Imputation method. Out of 253 observations, only 3 records were missing customer type information. Based on the frequency distribution, the number of Member customers (131 records) was slightly higher than Regular customers (119 records). Therefore, the missing values were replaced with “Member” in order to preserve the dataset size while maintaining the overall distribution of customer categories with minimal distortion.  

Secondly, inconsistencies were identified in the product_category field due to incorrect or inconsistent classification between product names and their assigned categories. For example, “Shampoo” appeared under multiple categories such as stationery, household goods, and personal care; “Orange Juice” was incorrectly categorized as household goods instead of beverages; and “Detergent” was mistakenly classified as a beverage in several records. To resolve these issues, a new variable named Cleaned_Product_Category was created to standardize product classifications and ensure data consistency. Each product was reassigned into a more appropriate category based on logical retail grouping rules, including:
•	Apple → Fruits 
•	Orange Juice → Beverages 
•	Detergent → Household 
•	Shampoo → Personal Care 
•	Notebook → Stationery 

Thirdly, missing values in the quantity field were handled using the Median Imputation method. Since quantity in a supermarket dataset should represent the number of units sold, all values must remain as whole numbers. The median value of the dataset was identified as 11, and all three missing records were replaced with this value. Although the mean quantity was approximately 10.6, using the mean would generate decimal values, which are unrealistic in a retail transaction context because products are typically sold in whole units. Therefore, the median was considered a more suitable and practical replacement value.

Overall, the data cleaning process significantly improved dataset quality by removing duplicate transactions, correcting inconsistent classifications, and handling incomplete records. After cleaning, 239 valid and reliable observations remained in the dataset. These improvements help ensure more accurate descriptive statistics, visualization, and further analytical processes such as correlation analysis in subsequent stages.

# 3. Descriptive Statistics

