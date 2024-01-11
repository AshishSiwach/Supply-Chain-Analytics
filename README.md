# Supply-Chain-Analytics
Supply Chain Analytics for Atliq Mart an FMCG manufacturer.
## Problem Statement
AtliQ Mart is a growing FMCG manufacturer headquartered in Gujarat, India. It is currently operational in three cities Surat, Ahmedabad and Vadodara. They want to expand to other metros/Tier 1 cities in the next 2 years.

AtliQ Mart is currently facing a problem where a few key customers did not extend their annual contracts due to service issues. It is speculated that some of the essential products were either not delivered on time or not delivered in full over a continued period, which could have resulted in bad customer service. Management wants to fix this issue before expanding to other cities and requested their supply chain analytics team to track the ’On time’ and ‘In Full’ delivery service level for all the customers daily basis so that they can respond swiftly to these issues.

The Supply Chain team decided to use a standard approach to measure the service level in which they will measure ‘On-time delivery (OT) %’, ‘In-full delivery (IF) %’, and OnTime in full (OTIF) %’ of the customer orders daily basis against the target service level set for each customer.

## Meta data
This file contains all the meta information regarding the columns described in the CSV files. we have provided 3 CSV files:
1. dim_customers.csv
2. dim_products.csv
3. dim_date
4. dim_targets_orders
5. fact_order_lines.csv
6. fact_orders_aggregate.csv

---------------------------------------------------------------------------------------------

Column Description for dim_customers:

This table contains all the information about customers

1. customer_id: Unique ID is given to each customer
2. customer_name: Name of the customer
3. city: It is the city where the customer is present

---------------------------------------------------------------------------------------------------

Column Description for dim_products:
This table contains all the information about the products

1. product_name: It is the name of the product
2. product_id: Unique ID is given to each of the products
3. category: It is the class to which the product belongs

---------------------------------------------------------------------------------------------------

Column Description for dim_date:
This table contains the dates at daily, monthly level and week numbers of the year

1. date: date at the daily level
2. mmm_yy: date at the monthly level
3. week_no: week number of the year as per the date column

---------------------------------------------------------------------------------------------------

Column Description for dim_targets_orders:
This table contains all target data at the customer level

1. customer_id: Unique ID that is given to each of the customers
2. ontime_target %: Target assigned for Ontime % for a given customer
3. infull_target %: Target assigned for infull % for a given customer
4. otif_target %:   Target assigned for otif % for a given customer

---------------------------------------------------------------------------------------------------

Column Description for fact_order_lines:
This table contains all information about orders and each item inside the orders.

1. order_id: Unique ID for each order the customer placed
2. order_placement_date: It is the date when the customer placed the order
3. customer_id: Unique ID that is given to each of the customers
4. product_id: Unique ID that is given to each of the products
5. order_qty: It is the number of products requested by the customer to be delivered
6. agreed_delivery_date: It is the date agreed between the customer and Atliq Mart to deliver the products
7. actual_delivery_date: It is the actual date Atliq Mart delivered the product to the customer
8. delivered_qty: It is the number of products that are actually delivered to the customer


---------------------------------------------------------------------------------------------------

Column Description for fact_orders_aggregate:
This table contains information about OnTime, InFull and OnTime Infull information aggregated at the order level per customer

1. order_id: Unique ID for each order the customer placed
2. customer_id: Unique ID that is given to each of the customers
3. order_placement_date: It is the date when the customer placed the order
4. on_time: '1' denotes the order is delviered on time. '0' denotes the order is not delivered on time.
5. in_full: '1' denotes the order is delviered in full quantity. '0' denotes the order is not delivered in full quantity.
6. otif:    '1' denotes the order is delviered both on time and in full quantity. '0' denotes the order is either not delivered on time or not in full quantity.

## Key Insights and Finding
1. OT % vs Target OT %
   
   ![image](https://github.com/AshishSiwach/Supply-Chain-Analytics/assets/84501246/fc072cc6-056d-457b-bdd4-34993368b626)
2. IF % vs Target IF %

   ![image](https://github.com/AshishSiwach/Supply-Chain-Analytics/assets/84501246/32df22c4-be53-4427-a671-dc13411c7361)
3. OTIF % vs Target OTIF %

   ![image](https://github.com/AshishSiwach/Supply-Chain-Analytics/assets/84501246/1a4eed1f-614d-4650-92b2-560bb2db7db7)
4. Line Fill Rate %(LIFR %) and Volume Fill Rate %(VOFR %)

   ![image](https://github.com/AshishSiwach/Supply-Chain-Analytics/assets/84501246/bec1ffb4-6151-4d91-a30b-3b691148baaa)
5. OT %, IF % and OTIF % with their targets split by cities

   ![image](https://github.com/AshishSiwach/Supply-Chain-Analytics/assets/84501246/a6c6157f-dbef-4739-b906-371192c753a5)
6. OT %, IF % and OTIF % split by customers

   ![image](https://github.com/AshishSiwach/Supply-Chain-Analytics/assets/84501246/2db86377-bbef-45c8-a3c2-f4ddecb7f048)

7. Metrics Performance Over time

   ![image](https://github.com/AshishSiwach/Supply-Chain-Analytics/assets/84501246/7b8de339-1d7f-473a-b542-5155ef8a12e5)
8. LIFR % and VOFR % by products

   ![image](https://github.com/AshishSiwach/Supply-Chain-Analytics/assets/84501246/c7c91218-a861-49b3-a97c-6830ff82ee69)
9. Approximately 29% orders were delivered late.
10. On an average orders have been 1.69 days late from the agreed delivery date.
11. On an average it takes 2.42 days to ship the product from the day order was placed.














