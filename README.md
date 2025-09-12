[Coffee_Shop (1).pdf](https://github.com/user-attachments/files/22068677/Coffee_Shop.1.pdf)
# Coffee Shop 

Coffeee-Shop

Get the posisible reresults for coffee shop

The Coffee Shop is not doing well for the past 6 month that leads previous CEO to desmissed the company due to poor performence 
The new CEO want to fix the conflict that will upgrade sale 

# Aim
To find analytical result that might assist to grow sales
To possible result that will have great impect on the sale
to find permanent solutions to sales 

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

# Presentation

https://www.canva.com/design/DAGysCwf0hI/oQVJL746WNQ7BSagQzLgQQ/edit

links: https://lookerstudio.google.com/s/idIx6vriyPw

links: utm_content=DAGxljIbu94&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton
[COFFEE SHOP CSV DATA BASE.xlsx](https://github.com/user-attachments/files/22068196/COFFEE.SHOP.CSV.DATA.BASE.xlsx)[COFFEE SHOP CSV DATA BASE.xlsx](https://github.com/user-attachments/files/22068379/COFFEE.SHOP.CSV.DATA.BASE.xlsx)
<img width="1848" height="870" alt="Miro diagram" src="https://github.com/user-attachments/assets/1b11db71-6eba-4cb9-8910-0d94be036331" />
[COFFEE SHOP CSV DATA BASE.xlsx](https://github.com/user-attachments/files/22068367/COFFEE.SHOP.CSV.DATA.BASE.xlsx)
![rough scatch](https://github.com/user-attachments/assets/76d58e93-747c-4882-b58a-0c8502505d03)
[Coffee shop data in 6 M (1).csv](https://github.com/user-attachments/files/22068388/Coffee.shop.data.in.6.M.1.csv)
