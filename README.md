# MIS-311-
# Introduction of Business Analytics

# Part 1: Data Analysis and Insight

# 1. Dataset Overview

This dataset contains transactional sales records collected from a supermarket retail business. The data is organised in a single worksheet named sales. The dataset consists of *254 rows* and *8 columns*, where each row represents one individual sales transaction.

**Variables Description**

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

Three duplicate rows were identified in the dataset and removed to prevent repeated sales transactions from affecting the analysis results. After removing duplicate records, the dataset became more reliable and suitable for descriptive statistics and correlation analysis. Because the same transaction may be counted more than once, duplicate rows might skew the analysis's findings and produce erroneous revenue, averages, and business insights.

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

<img width="1878" height="966" alt="image" src="https://github.com/user-attachments/assets/4d606605-acf7-439f-8688-4545c5c73d8f" />

The descriptive statistics table provides an overview of the supermarket’s sales performance through three key variables: Quantity, Total_price, and Revenue. The results show that the average quantity purchased per transaction was approximately 10.61 items, with quantities ranging from 1 to 20 items, indicating a relatively balanced purchasing behavior among customers. The average total price per transaction was around $123.77, while the average revenue generated reached approximately $1,756.81. In particular, Revenue has the highest standard deviation (1954.943), showing that revenue values varied significantly across transactions, meaning some transactions generated exceptionally high sales compared to others. Additionally, the positive skewness values for Total_price (0.91) and Revenue (1.35) indicate that the data distribution is right-skewed, where a small number of transactions contributed disproportionately high values.

Moreover, the correlation matrix demonstrates strong positive relationships between the variables. Quantity and Total_price have a correlation coefficient of 0.722, suggesting that purchasing more items generally increases the transaction value. Revenue also shows a very strong correlation with Total_price (0.964), meaning that higher transaction values directly contribute to greater revenue generation. These findings imply that increasing product purchases and encouraging higher-value transactions could significantly improve supermarket revenue performance.

**3.1. Revenue Distribution by Product Category Analysis**

<img width="1271" height="755" alt="image" src="https://github.com/user-attachments/assets/44c5ab47-681a-4cf5-a5fe-c971538b835f" />

The Pareto chart illustrates the revenue contribution of each product category in the supermarket dataset. Among all categories, Fruits generated the highest revenue at $113,690.98, followed by Stationery with $96,477.07 and Beverages with $95,533.38. These three categories are the major contributors to total sales revenue. Meanwhile, Household and Personal Care showed moderate performance with revenues above $60,000, while the final category contributed only $7,791.74, representing the smallest share of revenue. The cumulative percentage line also indicates that the top three categories account for approximately 70% of total revenue, demonstrating a strong concentration of sales in a few product groups.

The analysis suggests that customers primarily spend on essential and frequently purchased products such as fruits, beverages, and stationery items. Since these categories contribute the majority of total revenue, the supermarket should prioritize them in inventory management, promotional campaigns, and shelf placement strategies to maximize profitability. In contrast, low-performing categories may require further evaluation to determine whether improvements in marketing, pricing, or product assortment are necessary. Additionally, the heavy dependence on a few categories indicates potential business risk if demand for these products declines, so diversification strategies may help maintain stable long-term revenue growth.

Overall, the Pareto analysis reveals that a small number of product categories generate most of the supermarket’s revenue. By focusing on high-performing categories while improving or optimizing weaker categories, the business can enhance operational efficiency, customer satisfaction, and overall financial performance.

**3.2. Average Transaction Value by Customer Type Analysis**

<img width="1358" height="413" alt="image" src="https://github.com/user-attachments/assets/329c5244-eac8-4ef9-81c7-a31aee627f9a" />

The chart presents the average transaction value based on customer type. The results show that Member customers have a higher average transaction value of approximately $133.88, while Normal customers spend an average of $112.38 per transaction. The overall average transaction value across all customers is $123.77. This indicates that member customers tend to spend significantly more per purchase compared to non-member customers.

The higher spending behaviour of member customers suggests that the membership program is effective in encouraging customer loyalty and increasing purchase value. Given that, members may be motivated by benefits such as discounts, reward points, or personalised promotions, leading them to make larger purchases. Therefore, the supermarket should continue strengthening its loyalty program by offering exclusive promotions and personalised marketing campaigns to retain high-value customers. Additionally, the company can encourage normal customers to register for membership programs to increase their spending behaviour and improve long-term customer retention.

In conclusion, the analysis demonstrates that member customers contribute greater value per transaction than normal customers. This highlights to show the importance of customer loyalty programs in enhancing sales performance and generating higher revenue for the business.

**3.3 Revenue Percentage by Customer Type Analysis**

<img width="1143" height="463" alt="image" src="https://github.com/user-attachments/assets/6161ba17-d216-487d-b6d9-8cfafa3f4d59" />

The pie chart illustrates the percentage contribution of revenue by customer type. The results indicate that Member customers contribute the majority of total revenue, accounting for 58.82%, while Normal customers contribute 41.18%. This shows that member customers generate a significantly larger share of the supermarket’s total sales revenue compared to non-member customers.

The higher revenue contribution from member customers suggests that loyalty programs are highly effective in increasing customer spending and encouraging repeat purchases. Members likely shop more frequently and spend more per transaction due to benefits such as discounts, reward points, and personalised offers. Therefore, the supermarket should continue investing in membership programs and customer relationship management strategies to retain loyal customers. In addition, the business should develop promotional campaigns to convert more existing customers into members, which could further increase long-term revenue and customer retention.

In short, the analysis demonstrates that member customers are the key drivers of the supermarket’s revenue performance. Strengthening customer loyalty programs and improving member engagement can help the business maintain stable revenue growth and enhance overall profitability.

# 4. Conclusion and Implications

This analysis provides and supports valuable insights into supermarket sales performance, customer purchasing behaviour, and product demand trends. The descriptive statistics show that the supermarket generated a considerable amount of revenue, with noticeable variations in transaction values and purchasing quantities among customers. Additionally, the correlation analysis indicates a strong positive relationship between quantity purchased, total price, and revenue, suggesting that higher purchasing volumes significantly contribute to overall sales performance. From a business perspective, these findings can support better decision-making in inventory management, pricing strategies, and marketing activities. Product categories with high sales and revenue should receive greater inventory support and promotional focus to maintain customer demand. Meanwhile, categories with lower performance may require pricing adjustments, bundle promotions, or targeted marketing campaigns to improve sales. Therefore, the analysis helps supermarket managers identify business opportunities, optimise operational efficiency, and enhance customer satisfaction through data-driven strategies.
