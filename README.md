# Sales_Insights_Tableau

## Sales Insights - Brick and Motor Business [Tableau | SQL]

- Designed a Tableau dashboard to understand AtliQ hardware goods sales trend.
- The final dashboard was effective at displaying the sales trend of AtliQ hardware, allowing users to understand the data and make informed decisions.
- This dashboard could help in increasing the revenue at least by 7% in the next quarter.

### Sales Insights Overview: 

![alt text](https://github.com/RathanRaju/Sales_Insights_Tableau/blob/main/Dashboard_Overview.png "Dashboard Overview")


### Profit Analysis Overview:

![alt text](https://github.com/RathanRaju/Sales_Insights_Tableau/blob/main/Profit_Analysis.png "Profit Analysis Overview")


## Data Analysis Using SQL

SQL queries used within MySQL for data exploration

1. Show all customer records
```
    SELECT * FROM customers;
```
2. Show total number of customers
```
    SELECT count(*) FROM customers;
```
3. Show transactions for Chennai market (market code for chennai is Mark001
```
    SELECT * FROM transactions where market_code='Mark001';
```
4. Show distrinct product codes that were sold in chennai
```
    SELECT distinct product_code FROM transactions where market_code='Mark001';
```
5. Show transactions where currency is US dollars
```
    SELECT * from transactions where currency="USD"
```
6. Show transactions in 2020 join by date table
```
    SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;
```
7. Show total revenue in year 2020,
```
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and       transactions.currency="INR\r" or transactions.currency="USD\r";
```
8. Show total revenue in year 2020, January Month,
```
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and and   date.month_name="January" and (transactions.currency="INR\r" or transactions.currency="USD\r");
```
9. Show total revenue in year 2020 in Chennai
```
    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
```
