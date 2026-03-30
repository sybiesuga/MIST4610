# SQL-Grocery-DataBase
UGA MIST 4610 Spring 2026 Group Project Repository 

TEAM MEMBERS:
1. Andrew Yancey, - https://github.com/AndyY-64
2. Kristina Lam, - https://github.com/sybiesuga
3. Bryan Yang, - https://github.com/BryanYangUGA
4. Shivani Menon, - https://github.com/shivanimenon 
5. Andrew Pruitt, - https://github.com/andrewpruitt033


PROBLEM DESCRIPTION:

Our mission is to design and implement a relational database that models a regional grocery store chain operating across multiple locations in the southeastern United States. The central entity in the model is the StoreLocation, identified by a unique locationId, which represents each physical store.

The business operates:

5 store locations

3 suppliers

50 customers

50 employees

50 products

8 sections per store

Each store offers a variety of products organized into sections (e.g., produce, dairy, frozen goods), with products sourced from third-party suppliers. The system is designed to support core business operations, including inventory tracking, employee management, customer transactions, and order processing.

Using generated sample data, the database will enable meaningful queries that help managers and executives analyze sales performance, monitor inventory levels, evaluate supplier relationships, and improve overall store profitability.

DATA MODEL:

The data model is designed to accurately represent the relationships between key entities within a grocery store chain while maintaining data integrity through normalization and the use of primary and foreign keys.

At the core of the model are StoreLocations (5), which serve as the operational hubs where inventory is stocked, employees are assigned, and customer transactions occur. Each store is linked to its inventory through a many-to-many relationship with Products, illusrated by the Inventory table, which tracks the quantity of each product available at each location.

Products are associated with both a Supplier and a Section. Each product is supplied by exactly one supplier and categorized into one section, while suppliers and sections can each be linked to multiple products. This structure allows for efficient tracking of product sourcing and organization within stores.

Customer purchases are represented through the Order table, where each order is placed by a single customer and processed by a single employee. The relationship between orders and products is handled by the OrderItem table, which records the specific items included in each transaction along with their quantities and prices. This design enables detailed analysis of purchasing behavior and sales performance.

Employees are handled through the StoreEmployee table, which assigns each employee to a specific store location. This ensures that employees are properly associated with a single store while allowing each store to maintain a team of multiple employees.

Overall, the model supports both operational functionality and analytical capabilities by clearly defining relationships between entities and ensuring consistency through enforced constraints. This structure enables efficient querying for business insights such as inventory distribution, sales patterns, and employee utilization.

<img width="947" height="738" alt="Screenshot 2026-03-29 at 4 38 04 PM" src="https://github.com/user-attachments/assets/32922529-8462-4a1f-acf2-5d27df8e2a1d" />



DATA DICTIONARY:


<img width="717" height="183" alt="Screenshot 2026-03-29 at 4 30 53 PM" src="https://github.com/user-attachments/assets/7474ee89-f73a-4736-be66-3cbf0b727d75" />


<img width="723" height="310" alt="Screenshot 2026-03-29 at 4 32 42 PM" src="https://github.com/user-attachments/assets/11cfb53c-4f30-4d89-8f1c-cad947d042a1" />


<img width="680" height="193" alt="Screenshot 2026-03-29 at 4 33 02 PM" src="https://github.com/user-attachments/assets/9eb2603b-0403-44bd-b8f1-8035e055ea55" />


<img width="682" height="392" alt="Screenshot 2026-03-29 at 4 33 21 PM" src="https://github.com/user-attachments/assets/d6fb5a12-f46b-4e00-b658-d723c5277fc0" />


<img width="680" height="225" alt="Screenshot 2026-03-29 at 4 33 42 PM" src="https://github.com/user-attachments/assets/4bdd9bbe-da16-43f8-bd73-727965ec43b7" />


<img width="684" height="225" alt="Screenshot 2026-03-29 at 4 33 59 PM" src="https://github.com/user-attachments/assets/2448c68a-e41c-48fd-9f2e-3a6d5c6b32a7" />


<img width="684" height="174" alt="Screenshot 2026-03-29 at 4 35 22 PM" src="https://github.com/user-attachments/assets/558a033c-958b-4a53-81cd-583e823b8896" />


<img width="678" height="338" alt="Screenshot 2026-03-29 at 4 35 46 PM" src="https://github.com/user-attachments/assets/a4731bb0-5f44-463d-8411-0f152ecdcf64" />


<img width="683" height="401" alt="Screenshot 2026-03-29 at 4 36 03 PM" src="https://github.com/user-attachments/assets/00ac7ab0-d459-438e-84e6-dcdfe30fb904" />


QUERIES:

<img width="664" height="289" alt="Screenshot 2026-03-28 at 12 01 13 PM" src="https://github.com/user-attachments/assets/04164bbd-a64c-4f1c-a668-bdda6af93027" />

Query #1 (Total Sales per Store)
     What are the total sales for each individual store?
     This query calculates the sum of total sales for each individual store, and this helps managers analyze which stores are performing well or need improvement. 

   <img width="818" height="525" alt="Screenshot 2026-03-28 at 12 04 31 PM" src="https://github.com/user-attachments/assets/d456577c-ff2c-416f-893c-af52dacce7e1" />
  
Query #2 (Products Below Reorder Level)
     What items are low in stock?
     This query notifies the manager when certain items' stock is low, and that helps managers restock before they run out of an item.

<img width="818" height="525" alt="Screenshot 2026-03-28 at 12 07 15 PM" src="https://github.com/user-attachments/assets/6ee42a74-d548-4169-bbe0-91e50eee6e98" />

Query #3 (Top 5 Best Selling Products)
     What items are top-selling in the company?
     This query identifies the top-selling products of the company, which allows managers to figure out what to promote and what to keep when cycling out inventory to maintain high sales.  
     
<img width="814" height="520" alt="Screenshot 2026-03-28 at 12 09 34 PM" src="https://github.com/user-attachments/assets/21540657-e8b1-4f21-8582-ac5c6b9d85ac" />

Query #4 (Average Transaction Value)
     What is the average amount a customer spends in the store?
This query summarizes how much the average customer spends in a store, which allows managers to analyze how much the average customer spends and how it contributes to the overall sales of the company. 

<img width="815" height="516" alt="Screenshot 2026-03-28 at 12 10 30 PM" src="https://github.com/user-attachments/assets/2ea6c2f3-a4d0-42fb-9058-0eabe66787b7" />

Query #5 (Suppliers with Above Average Costs)
     What suppliers have higher than average prices? The query identifies suppliers whose average price is above the mean price of all products. This helps managers to look at supplier cost and see if any replacement in supplier is needed
  <img width="815" height="512" alt="Screenshot 2026-03-28 at 12 11 09 PM" src="https://github.com/user-attachments/assets/6917dc86-4813-42b4-9251-5bccea96ab86" />
  
Query #6 (Stores That Have Never Sold a Certain Category)
     This query can check which stores have not sold product from a certain section. It helps manager detect gaps in customer preference in different locations. Then each store can have their own items and matches the customers interest. 
 
 <img width="814" height="509" alt="Screenshot 2026-03-28 at 12 13 07 PM" src="https://github.com/user-attachments/assets/d5165194-9454-43e6-86d9-2f6018fd1379" />
  
Query #7 (Customers Who Spent More Than $500)
     This query identifies customers who spend more than 500 dollars. This helps managers to recognize high value customers and possibly have them become loyal customers by offering promotions, discounts and loyalty programs.

<img width="814" height="520" alt="Screenshot 2026-03-28 at 12 13 49 PM" src="https://github.com/user-attachments/assets/38831165-0516-4c9c-b8f5-38e994bad902" />

Query #8 (The 5 most recent Orders)
     What are the most recent orders made in the system? This query can track the latest orders based on the order date limited to the five recent transactions. This can help managers quickly and efficiently review sales activity and track performance.

<img width="816" height="515" alt="Screenshot 2026-03-28 at 12 14 18 PM" src="https://github.com/user-attachments/assets/dd6f05da-2b83-4b7b-a4a7-e28532fa7d6a" />

Query #9 (Customers with the Most Transactions) 
What customers have made the most transactions?
This query calculates the total number of transactions made by each customer by counting their orders, helping managers identify the most active or valuable customers.

<img width="813" height="516" alt="Screenshot 2026-03-28 at 12 14 52 PM" src="https://github.com/user-attachments/assets/24254594-b7c8-41a2-b0bf-70b296715bd2" />

Query #10 (Product Cost Above Average Price in Their Category) 
Which products are priced above the average price within their category?
This query identifies products whose prices are higher than the average price in their section, helping managers evaluate pricing strategies and identify premium or overpriced items.

<img width="812" height="505" alt="Screenshot 2026-03-28 at 12 15 36 PM" src="https://github.com/user-attachments/assets/aedbd0e4-eb50-49b5-aa5d-71d426f1f252" />

DATABASE INFORMATION: 

Database Name: al_Group_21482_G1

Additonal Information:
  - Database created using MySQLWorkbench 8.0C
  -  - Each query listed above is a store procedure which can be called using: CALL TP_Q#();
