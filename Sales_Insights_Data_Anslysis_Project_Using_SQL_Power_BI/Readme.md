<h1>Sales_Insights_Atliq_Hardwares</h1>

<h3>Sales insights project Powerbi Dashboard</h3>
This project I learn from code basics youtube channel.

<h3>Problem Statement</h3> 
AtliQ Hardware is a company with multiple branches across India that provides computer hardware & peripheral components to its customers. The company's sales director is having a lot of trouble comprehending how the business is doing and what challenges it is currently experiencing because sales are not what was anticipated and are really falling progressively. And if he phones the regional managers to enquire about the state of the market and sales, it is clear that this is frustrating because, by nature, individuals are uncomfortable reading data from excel files.

<h3>Solution</h3> 
The sales director of AltiQ hardware made the choice to create a PowerBI Dashboard for turning the data into a visual representation so that decisions could be made based on data. He therefore employed a group of data specialists to finish this project.

<h3>THE DASHBOARD</h3>

<h4>Sales Insights</h4>

![Screenshot AS_1](https://user-images.githubusercontent.com/125251408/232175121-1beb0b4e-e027-4b6a-96aa-4cdd47c77b89.png)

<h4>Product Analysis</h4>

![Screenshot AS_2](https://user-images.githubusercontent.com/125251408/232175200-66705fb9-d058-4969-9d70-cc0f5da99524.png)

<h4>Performance Insights</h4>

![Screenshot AS_3](https://user-images.githubusercontent.com/125251408/232175299-409dc79f-f36c-41ee-be6b-1689a3b0c3e3.png)

<h3>SQL Queries Used</h3> 

1.Show all customer records.

    SELECT * FROM customers; 
    
2.Show total number of customers.

    SELECT count(*) FROM customers;
    
3.Show transactions for Chennai market (market code for chennai is Mark001).

    SELECT * FROM transactions where market_code='Mark001'; 
 
4.Show distrinct product codes that were sold in chennai.

    SELECT distinct product_code FROM transactions where market_code='Mark001';
 
5.Show transactions where currency is US dollars.

    SELECT * from transactions where currency="USD";

6.Show transactions in 2020 join by date table.

    SELECT transactions.*, date.* FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020;
    
7.Show total revenue in year 2020.

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.currency="INR\r"     or transactions.currency="USD\r";
    
8.Show total revenue in year 2020, January Month.

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and date.month_name="January"     and (transactions.currency="INR\r" or transactions.currency="USD\r");

9.Show total revenue in year 2020 in Chennai.

    SELECT SUM(transactions.sales_amount) FROM transactions INNER JOIN date ON transactions.order_date=date.date where date.year=2020 and transactions.market_code="Mark001";
    



    
    
    
    
    
    
