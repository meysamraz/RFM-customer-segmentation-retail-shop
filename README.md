# RFM Customer Segmentation for a Retail Shop
An e-commerce company wants to segment its customers and determine marketing strategies according to these segments. To this end, we will define customers' behavior and create groups according to clusters in these behaviors. In other words, we will include those who exhibit common behaviors in the same groups and we will try to develop special sales and marketing techniques for these groups.

I'm going to use RFM which stands for Recency, Frequency, and Monetary Value. It is a marketing framework that is used to analyze customer behavior and segment customers into groups based on their past purchasing habits.

The RFM analysis is based on the following three metrics:

Recency - How recently a customer has made a purchase.
Frequency - How often a customer makes purchases.
Monetary Value - How much a customer spends on each purchase.

The RFM formula involves assigning a score to each metric, which is then used to segment customers into different groups. The scores are typically ranked on a scale of 1 to 5, with 5 being the highest score.

The RFM formula can be written as follows:

RFM Score = (R Score * 100) + (F Score * 10) + M Score

Where:
R Score = a score based on how recently the customer made a purchase (e.g., 5 for most recent, 1 for least recent)
F Score = a score based on how frequently the customer makes purchases (e.g., 5 for most frequent, 1 for least frequent)
M Score = a score based on how much the customer spends on each purchase (e.g., 5 for highest spend, 1 for lowest spend)

By segmenting customers into different groups based on their RFM scores, businesses can tailor their marketing strategies and offers to better meet the needs and preferences of each group, ultimately leading to increased customer loyalty and revenue.


- ## Dataset 
    - InvoiceNo: Invoice number. Nominal. A 6-digit integral number is uniquely assigned to each transaction. If this code starts with the letter 'c', it indicates a ---cancellation.
    - StockCode: Product (item) code. Nominal. A 5-digit integral number is uniquely assigned to each specific product.
    - Description: Product (item) name. Nominal.
    - Quantity: The quantities of each product (item) per transaction. Numeric.
    - InvoiceDate: Invoice date and time. Numeric. The day and time when a transaction was generated.
    - UnitPrice: Unit price. Numeric. Product price per unit in sterling ( £).
    - CustomerID: Customer number. Nominal. A 5-digit integral number is uniquely assigned to each customer.
    - Country: Country name. Nominal. The name of the country where a customer resides.
 
## Project Overview

### 1 -  Exploring Dataset
   - Check data shape
   - Check data type
   - See if there is any null values
   - See if customers have frequency in their purchases
   - Check the first and last recorded purchases

### 2 - Data Preprocessing
- Drop null values 
- Only keep recoreds with real purchasing
- Create a new column call ***TotalAmount*** shows total amount of money customer spent on order
- Reformat InvoiceDate to datetime

## 3 - Calculating RFM Score
- Calculating Recency
- Calculating Frequency
- Calculating Monetary
- Score R and F and M based on their quantile
- Segment customers based on their RFM score max = 555 and min = 111

## 4 - Analyzing Segments
- How many customers belong to each Segment?
- AVG customers total amount spent
- What's Yearly total amount and quantity sold?
- What country are the customers from?
- What country are the champion customers from?
- Most Frequently bought product by customers of each segment

### 5 - Reporting Analysis
In this report, I summarize the analysis that has been made in this notebook + Explaining each segment and marketing strategy for them.
- ####  https://docs.google.com/document/d/1usBhCDgDJz3gsrSh9Ve0VTt8pMpNhxd3zg-5kaotyBk/edit?usp=sharing
