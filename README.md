# Walmart Sales Data Analysis

## About

This project aims to explore the Walmart Sales data to understand top performing branches anda products, sales trend of different products, customer behaviour. The aims is to study how sales strategies can be improved and optimized. The dataset was obtained from the [Kaggle Walmart Sales Forecasting Competition](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting).

"In this recruiting competition, job-seekers are provided with historical sales data for 45 Walmart stores located in different regions. Each store contains many departments, and participants must project the sales for each department in each store. To add to the challenge, selected holiday markdown events are included in the dataset. These markdowns are known to affect sales, but it is challenging to predict which departments are affected and the extent of the impact." [source](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting)

## Purposes Of The Project

The major aim of this project is to gain insight into the sales data of Walmart to understand the different factors that affect sales of the different branches.

## About Data

The dataset was obtained from the [Kaggle Walmart Sales Forecasting Competition](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting). This dataset contains sales transactions from a three different branches of Walmart, respectively located in Mandalay, Yangon and Naypyitaw. The data contains 17 columns and 1000 rows:

| Column                  | Description                             | Data Type      |
| :---------------------- | :-------------------------------------- | :------------- |
| invoice_id              | Invoice of the sales made               | VARCHAR(30)    |
| branch                  | Branch at which sales were made         | VARCHAR(5)     |
| city                    | The location of the branch              | VARCHAR(30)    |
| customer_type           | The type of customer                | VARCHAR(30)    |
| gender                  | Gender of the customer making purchase  | VARCHAR(10)    |
| product_line            | Product line of the product solf        | VARCHAR(100)   |
| unit_price              | The price of each product               | DECIMAL(10, 2) |
| quantity                | The amount of the product sold          | INT            |
| VAT                 | The amount of tax on the purchase       | FLOAT(6, 4)    |
| total                   | The total cost of the purchase          | DECIMAL(10, 2) |
| date                    | The date on which the purchase was made | DATE           |
| time                    | The time at which the purchase was made | TIMESTAMP      |
| payment_method                 | The total amount paid                   | DECIMAL(10, 2) |
| cogs                    | Cost Of Goods sold                      | DECIMAL(10, 2) |
| gross_margin_percentage | Gross margin percentage                 | FLOAT(11, 9)   |
| gross_income            | Gross Income                            | DECIMAL(10, 2) |
| rating                  | Rating                                  | FLOAT(2, 1)    |

### Analysis List

1. Product Analysis

> Conduct analysis on the data to understand the different product lines, the products lines performing best and the product lines that need to be improved.

2. Sales Analysis

> This analysis aims to answer the question of the sales trends of product. The result of this can help use measure the effectiveness of each sales strategy the business applies and what modificatoins are needed to gain more sales.

3. Customer Analysis

> This analysis aims to uncover the different customers segments, purchase trends and the profitability of each customer segment.

## Approach Used

1. **Data Wrangling:** This is the first step where inspection of data is done to make sure **NULL** values and missing values are detected and data replacement methods are used to replace, missing or **NULL** values.

> i. Build a database
> ii. Create table and insert the data.
> iii. Select columns with null values in them. There are no null values in our database as in creating the tables, we set **NOT NULL** for each field, hence null values are filtered out.

2. **Feature Engineering:** This will help generate some new columns from existing ones.

> i. Add a new column named `time_of_day` to give insight of sales in the Morning, Afternoon and Evening. This will help answer the question on which part of the day most sales are made.

> ii. Add a new column named `day_name` that contains the extracted days of the week on which the given transaction took place (Mon, Tue, Wed, Thur, Fri). This will help answer the question on which week of the day each branch is busiest.

> iii. Add a new column named `month_name` that contains the extracted months of the year on which the given transaction took place (Jan, Feb, Mar). Help determine which month of the year has the most sales and profit.

2. **Exploratory Data Analysis (EDA):** Exploratory data analysis is done to answer the listed questions and aims of this project.

3. **Conclusion:**

## Business Questions To Answer

### Generic Question

1. How many unique cities does the data have?
2. In which city is each branch?

### Product

1. How many unique product lines does the data have?
2. What is the most selling product line?
4. What is the total revenue by month?
5. What month had the largest COGS?
6. What product line had the largest revenue?
5. What is the city with the largest revenue?
6. What product line had the largest VAT?


### Sales

1. Number of sales made in each time of the day per weekday
2. Which of the customer types brings the most revenue?
3. Which city has the largest tax percent/ VAT (**Value Added Tax**)?
4. Which customer type pays the most in VAT?

### Customer

1. How many unique customer types does the data have?
2. How many unique payment methods does the data have?
3. What is the most common customer type?
4. Which customer type buys the most?
5. What is the gender of most of the customers?
6. Which time of the day do customers give most ratings per branch?
7. Which day fo the week has the best avg ratings?
8. Which day of the week has the best average ratings per branch?


# Insights and Recommendations

## Product Analysis
1. **Most Selling Product Line:**
   - **Insight:** Fashion accessories (178 sales)
   - **Recommendation:** Focus marketing efforts on fashion accessories to leverage their popularity.
2. **Total Revenue by Month:**
   - **Insight:** January ($116,291.87), March ($108,867.15), February ($95,727.38)
   - **Recommendation:** Analyze what drives high sales in January and replicate those strategies in other months.
3. **Product Line with the Largest Revenue:**
   - **Insight:** Food and beverages ($56,144.84)
   - **Recommendation:** Prioritize inventory and promotions for food and beverages to maximize revenue.
4. **City with the Largest Revenue:**
   - **Insight:** Naypyitaw ($110,490.78)
   - **Recommendation:** Invest in marketing and infrastructure in Naypyitaw to sustain and increase revenue.
5. **Average Rating of Each Product Line:**
   - **Insight:** Highest rating for Food and beverages (7.11)
   - **Recommendation:** Focus on improving product lines with lower ratings through customer feedback and quality enhancements.

## Sales Analysis
1. **Sales by Time of Day on Sunday:**
   - **Insight:** Evening (58), Afternoon (52), Morning (22)
   - **Recommendation:** Increase staff and resources in the evening and afternoon on Sundays to manage higher sales volumes effectively.
2. **City with Highest VAT:**
   - **Insight:** Naypyitaw (16.09%)
   - **Recommendation:** Investigate why Naypyitaw has the highest VAT and see if there are opportunities to optimize costs or if it reflects a premium market willing to pay more.
3. **Customer Type Paying the Most VAT:**
   - **Insight:** Member (15.61%)
   - **Recommendation:** Evaluate if the VAT structure for Members is justified and consider if adjustments or benefits can be provided to offset their higher tax contributions.

## Customer Analysis
1. **Unique Customer Types:**
   - **Answer:** Normal, Member
   - **Recommendation:** Develop specific engagement strategies for each customer type to cater to their unique needs.
2. **Unique Payment Methods:**
   - **Answer:** Credit card, E-wallet, Cash
   - **Recommendation:** Ensure all payment methods are easy to use and offer promotions for less-used methods to balance usage.
3. **Most Common Customer Type:**
   - **Answer:** Member (499 purchases)
   - **Recommendation:** Enhance loyalty programs and offer exclusive benefits to Members
4. **Customer Type Buying the Most:**
   - **Answer:** Member (499 purchases)
   - **Recommendation:** Focus on retaining Members and converting Normal customers to Members through incentives.
5. **Gender Distribution:**
   - **Answer:** Male (498), Female (497)
   - **Recommendation:** Create gender-neutral marketing campaigns to appeal equally to both male and female customers.
6. **Time of the Day with Most Ratings per Branch:**
   - **Answer:**
     - Branch A: Afternoon (7.19)
     - Branch B: Morning (6.84)
     - Branch C: Evening (7.10)
   - **Recommendation:** Tailor service improvements and staffing during peak rating times for each branch.
7. **Best Average Ratings by Day of the Week:**
   - **Answer:** Monday (7.13), Friday (7.06), Tuesday (7.00)
   - **Recommendation:** Focus on maintaining high service quality on these days and replicate successful strategies on other days.
8. **Total Sales per Day of the Week per Branch:**
   - **Answer:**
     - Branch A: Sunday (52), Tuesday (51), Friday (50)
     - Branch B: Saturday (60), Tuesday (53), Friday (51)
     - Branch C: Tuesday (54), Saturday (54), Wednesday (50)
   - **Recommendation:** Optimize inventory and staffing for peak sales days in each branch to ensure smooth operations and customer satisfaction.


## Code

For the rest of the code, check the [sales_query.sql](https://github.com/Oladapo-Oluwadarasimi/Walmart_Sales_Analysis/blob/main/sales_query.sql) file

```sql
-- Create database
CREATE DATABASE WalmartSales;

-- Create table
CREATE TABLE sales(
	invoice_id VARCHAR(30) NOT NULL PRIMARY KEY,
    branch VARCHAR(5) NOT NULL,
    city VARCHAR(30) NOT NULL,
    customer_type VARCHAR(30) NOT NULL,
    gender VARCHAR(30) NOT NULL,
    product_line VARCHAR(100) NOT NULL,
    unit_price DECIMAL(10, 2) NOT NULL,
    quantity INT NOT NULL,
    VAT FLOAT(6, 4) NOT NULL,
    total DECIMAL(12, 4) NOT NULL,
    date DATETIME NOT NULL,
    time TIME NOT NULL,
    payment VARCHAR(15) NOT NULL,
    cogs DECIMAL(10, 2) NOT NULL,
    gross_margin_pct FLOAT(11, 9),
    gross_income DECIMAL(12, 4),
    rating FLOAT(2, 1)
);
```
