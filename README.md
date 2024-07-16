

Input dataset contains all the information regarding the columns described in the CSV files.
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

customer_id: Unique ID that is given to each of the customers
ontime_target %: Target assigned for Ontime % for a given customer
infull_target %: Target assigned for infull % for a given customer
otif_target %:   Target assigned for otif % for a given customer

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
6: otif:    '1' denotes the order is delviered both on time and in full quantity. '0' denotes the order is either not delivered on time or not in full quantity.

# Steps:

1.Data Loading

2.Data Preprocessing & Transformation

3.Data Modelling 
![WhatsApp Image 2024-07-16 at 1 53 29 PM](https://github.com/user-attachments/assets/69516d7b-d13f-4dd4-8bc1-33afa63179de)


4.Creating DAX queries for columns and measures

    Total Order Lines =Count of all order lines in fact_orders table
    
    Line Fill Rate(LIFR %) =Number of order lines shipped In Full Quantity / Total Order Lines
    
    Volume Fill Rate(VOFR %) =Total Quantity shipped / Total Quantity Ordered
    
    Total Orders =Total orders from fact aggregate table
    
    On Time Delivery(OT %) =Number of orders delivered On Time / Total Number of Orders

    In Full Delivery(IF %) =Number of orders delivered in Full quantity / Total Number of Orders





5.Data Visualization

6.Report Generation



![Screenshot_16-7-2024_23926_](https://github.com/user-attachments/assets/8c32a525-ea7a-41e6-8fdd-e7d8a79c07b2)
![Screenshot_16-7-2024_23940_](https://github.com/user-attachments/assets/06f7894e-64c1-4dd6-9910-3f95a96b7b5a)
![Screenshot_16-7-2024_23954_](https://github.com/user-attachments/assets/4f985115-200e-4328-abf9-c95e6194b662)
![Screenshot_16-7-2024_24025_](https://github.com/user-attachments/assets/53a8318e-d6b0-4bad-b40d-8b97feb50f4a)
![Screenshot_16-7-2024_24037_](https://github.com/user-attachments/assets/34bfbdc4-f40f-4e6f-8d0c-5b8418cd4e61)
