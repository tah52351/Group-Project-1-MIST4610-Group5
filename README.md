# Group 5 Mist 4610 Project 1

# Team Name:

39217 Group 5

# Team Members:

1. Becca Paden @beccapaden
2. Charlotte Moore @cem62831
3. Gabe Hanes @
4. Tyler Haleblian @
5. Logan Carras @lgc52432

# Scenario Description:

The database is well-suited for managing clothing e-commerce orders and tracking the specific clothes customers buy, when they buy them, and how those products are categorized. Like a real clothing store, the database maintains basic information from each customer in order to maintain a clientele record. It also keeps track of the orders from each customer, when it was ordered, where it is going to, and to what customer it is being sent to. 

In real clothing stores, every time a customer orders there will be an address, order date, and an order ID attached to a customer’s ID. This is shown in the database, and it is used to ensure successful delivery of the item. The database opens opportunities to sell a variety of clothing items that are specific in the name of the item, the price, size, color, and category (type). Categories (like Shirts, Hats, Dresses, Pants, etc) and subcategories (T-shirts, Long-sleeved shirts, tank tops, etc) are used to specify items for the consumer so they know exactly what they are ordering.

# Data Model

Explanation of data model:

The Clothes entity represents the clothing items that will be sold at the store. Each clothing item belongs to one category but a category can (in a one-to-many relationship with the Categories table), and will contain a name, price, size, and color. For example, some clothing items may fall under the “Shirts” category or the “Sweatshirts” category. A specific clothing item can be included in many orders (many-to-many relationship with the Orders table) which mimics inventory styles of real clothing stores. 

The Clothes_Orders table is the join table that manages the many-to-many relationship between Orders and Clothes. It tracks which clothing items are included in each order and their respective quantities. This is done by tracking the order ID and the cloth ID from the Clothes and Orders tables respectively. This is similar to commerce in modern clothing stores where each clothing item has its own ID, every order is processed by its ID, and the corresponding clothing items are matched with their respective order IDs to successfully send them to the right customer.

The Category table is used to specify the types of items that are sold at the store. Each category can contain many clothing items, but each clothing item only belongs to one category, establishing a one-to-many relationship between Categories and Clothes. The Category entity also has a one-to-many recursive relationship between sub_category_id and category_id, where each category has multiple subcategories. For example, the “Shirts” category can have “T-shirts” or “Long sleeve shirts” categories, or the “Pants” category can have “Jeans”, “Sweatpants”, or “Khakis” categories. 

The Customer table is pretty straightforward, tracking first and last names and the customer’s email address. Like a real e-commerce site, each customer can place multiple orders which is displayed by a one-to-many relationship with the Orders table. This is to ensure that customers are not just limited to ordering only once.

The Orders table is used to ensure each item ordered is tracked and dated. The table also includes order addresses to ensure delivery of the product to the customer. Each clothing item can be ordered multiple times, and an order can contain multiple clothing items, forming a many-to-many relationship with the Clothes table via the Clothes_Orders join table. The entity uses order_id, order_date, and order_address as a composite primary key to uniquely identify each order to a customer (customer_id) through the one-to-many relationship with the Customers table.

The Transaction table is used to represent a transaction in the clothing store. It has a transaction_id primary key and a credit_card_number attribute. It is in a one to one relationship with the Orders entity where one order is accompanied by one transaction. The entity is a useful record of customer’s payment information for recurring payments and management can use it to track the total number of transactions.

<img width="530" alt="Screenshot 2024-10-04 at 1 15 00 PM" src="https://github.com/user-attachments/assets/e23e074d-aa6f-4bf7-940b-0bd35d0e2473">

# Data Dictionary:

<img width="637" alt="Screenshot 2024-10-06 at 9 13 34 AM" src="https://github.com/user-attachments/assets/057226b7-8e8f-4081-9d46-2c311c6a4188">

<img width="715" alt="Screenshot 2024-10-06 at 9 14 51 AM" src="https://github.com/user-attachments/assets/b8872602-b011-41d5-8d0d-23006cfadd47">

<img width="715" alt="Screenshot 2024-10-06 at 9 15 12 AM" src="https://github.com/user-attachments/assets/5bf93c8e-e0b4-40c4-a70d-a95b4fb1deaf">

<img width="617" alt="Screenshot 2024-10-06 at 9 16 46 AM" src="https://github.com/user-attachments/assets/a9c54651-a7af-4746-8edf-1ed35729282a">

<img width="710" alt="Screenshot 2024-10-06 at 9 17 00 AM" src="https://github.com/user-attachments/assets/8d758c5f-b9e2-4b4f-8eea-9adb7b068308">

<img width="708" alt="Screenshot 2024-10-06 at 9 17 21 AM" src="https://github.com/user-attachments/assets/6b3ef8cf-63ac-4423-9a05-62c4d24c5f56">

# Queries:

<img width="779" alt="Screenshot 2024-10-14 at 4 29 58 PM" src="https://github.com/user-attachments/assets/4507c887-da85-4dd6-9c3c-cbe8ae8d716a">

1. Query 1 shows the total number of orders placed from the store.

<img width="1313" alt="Screenshot 2024-10-08 at 4 17 23 PM" src="https://github.com/user-attachments/assets/a13f6f40-fd69-4c46-ab8d-b911761bf792">

Query 1 allows managers to monitor the number of overall sales to gauge business performance. Monitoring this number shows the manager when their store has reached sales and performance goals. 

2. Query 2 shows the products offered by the store and their in descending order.

<img width="1313" alt="Screenshot 2024-10-08 at 4 17 50 PM" src="https://github.com/user-attachments/assets/eaa9a488-a6e8-4ebd-b772-0cb5b32aa923">

Query 2 allows managers to see the range of prices in their products and to know which products are more or less expensive. This is important to know if the store is selling more of the higher priced or lower priced items to see how much the customers the store is reaching is likely to spend.

3. Query 3 lists the information for all customers, including name and email.

<img width="1313" alt="Screenshot 2024-10-08 at 4 17 57 PM" src="https://github.com/user-attachments/assets/e5284ebf-adc5-41a1-aad8-7530fe7709b8">

Query 3 allows management to easily reach customers with targeted email marketing campaigns, promoting new products, special offers, and seasonal sales. Managers can also use this information to solicit feedback through surveys sent via email, gaining insights into customer preferences, satisfaction levels, and areas for improvement.

4. Query 4 lists the order numbers and addresses.
   
<img width="1313" alt="Screenshot 2024-10-08 at 4 18 11 PM" src="https://github.com/user-attachments/assets/9ffee375-4a0b-43df-93ef-528dc9d03fd0">

Query 4 allows managers to analyze order addresses to optimize shipping routes and reduce delivery times, leading to more efficient logistics operations.

5. Query 5 lists the customers that ordered 2 or more pieces of clothing in their order.
   
<img width="1313" alt="Screenshot 2024-10-08 at 4 31 30 PM" src="https://github.com/user-attachments/assets/4851f40e-b01c-4948-be60-899b9ce393fe">

Query 5 allows managers to view someone who ordered multiple items and target marketing towards them because they may be more likely to buy more clothing. 

6. Query 6 lists what types of items that each customer has purchased, and how many of each that person bought.
   
<img width="1313" alt="Screenshot 2024-10-08 at 4 31 40 PM" src="https://github.com/user-attachments/assets/127145ce-2303-41cd-878f-287decd48c61">

Query 6 allows managers to determine which customers primarily purchase each type of clothing. Then they can effectively market to each person more efficiently.

7. Query 7 lists customers who have spent over $80 and how much they spent. 

<img width="1313" alt="Screenshot 2024-10-08 at 4 31 50 PM" src="https://github.com/user-attachments/assets/630656f7-48cb-418f-a142-055d5af790cc">

Query 7 allows managers can identify customers who have spent $80 or more in the clothing store. This data can help identify high-value customers who may be more likely to buy even more in the future. 

8. Query 8 lists the average price of items bought by a customer, ordered by their size.
   
<img width="1313" alt="Screenshot 2024-10-08 at 4 32 06 PM" src="https://github.com/user-attachments/assets/d69bdb78-e0d4-4212-93e4-ff29d4a14ac8">

Query 8 gives details about the customer as well as the amount and type of product they ordered. One can change the size and price to find what sizes are ordered by what demographic of customers. This information would be useful for business operations as management will be able to demand forecast for different sizes, target their marketing promotions, and order products that line up with the highest spending customers. 

9. Query 9 lists clothing id, product name, and quantity ordered in descending order. 

<img width="1313" alt="Screenshot 2024-10-08 at 4 32 18 PM" src="https://github.com/user-attachments/assets/5df0e717-4e69-4205-9b86-a54fcbd9b3dc">

Query 9 allows managers to know which items are ordered the most so they can ensure popular products are adequately stocked, preventing stock outs and lost sales. It helps in balancing inventory levels, ensuring that best-sellers are prioritized while minimizing excess stock of less popular items.

10. Query 10 lists order that costs over $30 and had 2 or more items in the order.
    
<img width="1313" alt="Screenshot 2024-10-08 at 4 32 25 PM" src="https://github.com/user-attachments/assets/4853e482-25d2-4f07-a145-a87edce4f103">

Query 10 allows managers to figure out what size boxes they need to buy to ship orders, and how often people place big orders. The $30 constraint is to ensure small items like stickers are not being purchased, so managers know that these orders therefore require the larger box. 

# Database information:

Name of the database: 
ha_group5
