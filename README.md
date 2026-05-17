# MIS-311-
Introduction of Business Analytics

Part 1: Data Analysis and Insight

# 1. Dataset Overview

This dataset contains transactional sales records collected from a supermarket retail business. The data is organised in a single worksheet named **sales**.

The dataset consists of **254 rows** and **8 columns**, where each row represents one individual sales transaction.

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

# Purpose of the Dataset

This dataset is useful for performing **descriptive analytics** and **business analytics** to better understand supermarket sales performance and customer purchasing behaviour.

The analysis can help answer questions such as:

- Which product categories generate the highest revenue?
- Which branch or city performs best in sales?
- What type of customer contributes more to total revenue?
- Which products have higher demand?
- Are there any unusual sales patterns or outliers?

The dataset is useful for performing descriptive and business analytics to understand customer purchasing behaviour, sales performance across branches and cities, product demand, and revenue trends. It can support visualisation techniques such as pie charts, box plots, pivot tables, and comparative analysis for decision-making in retail management.

# 2. Data Cleaning

## Descriptive Statistics and Correlation Results

| Statistic | Quantity | Total_price | Revenue |
|---|---:|---:|---:|
| Mean | 10.61 | 123.77 | 1,756.81 |
| Standard Error | 0.38 | 6.48 | 122.91 |
| Median | 11 | 94.17 | 1,061.64 |
| Mode | 2 | 14.08 | 56.32 |
| Standard Deviation | 5.98 | 103.09 | 1,954.94 |
| Sample Variance | 35.75 | 10,627.92 | 3,821,800 |
| Kurtosis | -1.26 | 0.03 | 1.25 |
| Skewness | -0.07 | 0.91 | 1.35 |
| Range | 19 | 424.96 | 8,538.44 |
| Minimum | 1 | 2.18 | 4.36 |
| Maximum | 20 | 427.14 | 8,542.80 |
| Sum | 2,685 | 31,312.78 | 444,472.10 |
| Count | 253 | 253 | 253 |

## Correlation Analysis

The correlation matrix shows the relationship between **quantity**, **total_price**, and **revenue**.

| Variables | Quantity | Total_price | Revenue |
|---|---:|---:|---:|
| Quantity | 1 | 0.722 | 0.785 |
| Total_price | 0.722 | 1 | 0.964 |
| Revenue | 0.785 | 0.964 | 1 |

