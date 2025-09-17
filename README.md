
# Coffee Shop 

Coffeee-Shop

Get the posisible reresults for coffee shop

The Coffee Shop is not doing well for the past 6 month 
The setuation leaded the CEO to step down due to poor performence 
The new CEO want to fix the conflict that will upgrade sale 
gets all the insight of the shop

# Aim
To find analytical result that will assist to grow sales
To possible result that will have great impect on the sale
to find permanent solutions for the Coffee shop

#Objective
The tools i used to get the result

Microsoft Excel to retrive data

Snowflakes for Data processing

Excel Pivot table Groups and chats

Googlelooker developing an interective dashoboard


# EDA  ----checking column on my database
SELECT
    DISTINCT *
FROM
    "COFFEE"."PUBLIC"."SHOP"
limit
    5;
---- checking number of product Id
SELECT
    count (DISTINCT product_id)
FROM
    "COFFEE"."PUBLIC"."SHOP";
---checking number of qty
SELECT
    count (DISTINCT transaction_qty) AS number_of_transactions
FROM
    "COFFEE"."PUBLIC"."SHOP";
---checking min date
SELECT
    MIN (TRANSACTION_DATE) AS Start_date
FROM
    "COFFEE"."PUBLIC"."SHOP";
----checking max date
SELECT
    Max (TRANSACTION_DATE) AS last_date
FROM
    "COFFEE"."PUBLIC"."SHOP";
---checking store opening time
SELECT
    MIN (TRANSACTION_TIME) AS opening_time
FROM
    "COFFEE"."PUBLIC"."SHOP";
---checking store closing time
SELECT
    MAX (TRANSACTION_TIME) AS closing_time
FROM
    "COFFEE"."PUBLIC"."SHOP";
----checking number of shops
SELECT
    DISTINCT (store_location)
FROM
    "COFFEE"."PUBLIC"."SHOP";
--- check number of catergory
SELECT
    DISTINCT (PRODUCT_CATEGORY)
FROM
    "COFFEE"."PUBLIC"."SHOP";
---- Checking product type
SELECT
    DISTINCT (PRODUCT_TYPE)
FROM
    "COFFEE"."PUBLIC"."SHOP";
---checking price list
SELECT
    DISTINCT UNIT_PRICE
FROM
    "COFFEE"."PUBLIC"."SHOP";
-----checking min price
SELECT
    Min (DISTINCT UNIT_PRICE)
FROM
    "COFFEE"."PUBLIC"."SHOP";
----checking min price
SELECT
    MAX (DISTINCT UNIT_PRICE)
FROM
    "COFFEE"."PUBLIC"."SHOP";
SELECT
    PRODUCT_CATEGORY,
    product_type
FROM
    "COFFEE"."PUBLIC"."SHOP";
----date

# CODE 
SELECT DISTINCT product_category,

SUM(PRODUCT_ID) AS Total_Number_Of_Id_Per_Cartegory,
COUNT (PRODUCT_TYPE) AS Product_available,
SUM (TRANSACTION_QTY) AS Total_Transaction_Quantity,
SUM (UNIT_PRICE) AS Total_amount_Purchase_Per_Cartegory,
COUNT(PRODUCT_CATEGORY) AS Total_Number_Of_Cartegoty,
COUNT(PRODUCT_CATEGORY) AS Total_Number_Of_Cartegoty,
COUNT(TRANSACTION_TIME) AS Total_Number_Purchase,
DAYNAME (TRANSACTION_DATE) AS Day_of_Transaction,
TO_DATE (TRANSACTION_DATE) AS Purchase_Date,

 CASE   
        WHEN TRANSACTION_DATE BETWEEN '2023-01-01' AND '2023-01-30' THEN 'January'
        WHEN TRANSACTION_DATE BETWEEN '2023-02-01' AND '2023-02-28' THEN 'February'
        WHEN TRANSACTION_DATE BETWEEN '2023-03-01' AND '2023-03-30' THEN 'March'
        WHEN TRANSACTION_DATE BETWEEN '2023-04-01' AND '2023-04-30' THEN 'April'
        WHEN TRANSACTION_DATE BETWEEN '2023-05-01' AND '2023-05-30' THEN 'May'
        ELSE 'June'
        END AS Transaction_By_Month,

CASE    
        WHEN TRANSACTION_TIME BETWEEN '07:00:00' AND '11:59:00' THEN 'Morning'
        WHEN TRANSACTION_TIME BETWEEN '12:00:00' AND '16:59:00' THEN 'Afternoon'
        ELSE 'Evening' 
        END Day_time
FROM COFFEE.PUBLIC.SHOP

GROUP BY ALL;



