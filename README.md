# Women-in-SQL-Project-2

# BobaShop

## Team Name: 
Women In SQL

## Team Members:
Alicia Pirani [@aliciapirani](https://github.com/aliciapirani)

Alekhya Seelam [@alekhyaseelam](https://github.com/alekhyaseelam)

Diya Tahliani [@diyatahliani](https://github.com/diyatahliani)

Linzey Nguyen [@linzeynguyen](https://github.com/linzeynguyen)

Lancey Charles [@lanceycha](https://github.com/lanceycha)

## Scenario Description: 
The objective is to design and implement a relational database that effectively captures the operations of a boba shop. At the core of this model is the Store entity, which interacts with various related components, including employees, transactions, drinks, and more. We aim to accurately represent these relationships, generate sample data, and populate the entities with relevant attributes. Additionally, we seek to execute meaningful queries on this data to gain valuable insights into the boba shop's performance and operations.

## Data Model:
### Explanation of data model: 

Our data model is based on the structure of a hypothetical boba shop. It tracks employees, stores, drinks, transactions, payments, customer information, loyalty programs, and inventory.

### One-to-Many Relationships:

Store - Employee: One store has many employees, but many employees can only work at one store.

Store - Transaction: One store can have many transactions, but many transactions link back to one store.

Store - Inventory: One store can have multiple inventory items, but many inventory items link back to one store.

Vendor - Inventory: One vendor can supply multiple products, but multiple products can only come from one vendor.

Customer - Transaction: One customer can make many transactions, but many transactions link back to one customer. 

Transaction - Payment: One transaction can have many payments, but payments can only link back to one transaction.

Transaction - TransactionItem: One transaction can have multiple transaction items, but many transaction items link back to one transaction.

Drink - TransactionItem: A drink can be in many transaction items, but many transaction items link back to one drink.

### One-to-One Relationship:

Customer - LoyaltyProgram: One customer can have one loyalty program and one loyalty program can only link back to one customer.


### Many-to-Many Relationship:

Drink - Transaction: One drink can be involved in multiple transactions, and one transaction can include multiple drinks.

### One-to-Many Recursive Relationship: 

Employee's Boss - Employee: An employee who is a boss can look over many employees, but many employees report to one boss.

<img width="867" alt="Screenshot 2024-10-02 at 9 08 16 PM" src="https://github.com/user-attachments/assets/41b00d58-8f7c-412a-a1a7-00d7ed489242">

## Data Dictionary: 

### Table: Store 

<img width="885" alt="store " src="https://github.com/user-attachments/assets/a887b708-0c07-4753-a645-a372c8d2d42f">

### Table: Employee

<img width="882" alt="employee" src="https://github.com/user-attachments/assets/34210ffb-188f-43b8-beab-5aaf4e21b95d">

### Table: Payment
<img width="918" alt="payment" src="https://github.com/user-attachments/assets/e4b28b40-1fec-4608-9bc3-31974d9865b9">

### Table: Transaction
<img width="882" alt="transaction" src="https://github.com/user-attachments/assets/103c44e7-7f7a-4b92-8471-539dad18b67c">

### Table: Transaction Item
<img width="973" alt="transaction item" src="https://github.com/user-attachments/assets/616491d8-e761-470e-8176-29c059e4ee0f">

### Table: Vendor 
<img width="973" alt="vendor" src="https://github.com/user-attachments/assets/60c3975b-70e5-4d00-bd2c-a787e5b0e8a9">

### Table: Customer
<img width="973" alt="customer" src="https://github.com/user-attachments/assets/09f74b81-063c-446d-88e4-8f48bcce07fa">

### Table: Loyalty Program
<img width="973" alt="loyalty program" src="https://github.com/user-attachments/assets/0ad7eaa1-ceea-42f3-9f5a-48b9d82e30f4">

### Table: Drink 
<img width="973" alt="drink" src="https://github.com/user-attachments/assets/b8d62343-8362-4fb9-b571-49359cf035b5">

### Table: Inventory
<img width="973" alt="inventory" src="https://github.com/user-attachments/assets/dd880c5b-023e-43d9-94d9-3e8fd51c6a0e">

## Five Queries:

Query #1: Generate a report that shows the total sales for each store. At the end of the list, include a row showing the grand total sales across all stores.

This report displays the total sales for each store along with the grand total sales across all stores. It can help a manager analyze individual store performance and make data-driven decisions.

<img width="385" alt="Screenshot 2024-11-27 at 4 13 35 PM" src="https://github.com/user-attachments/assets/9cbca2a0-b7ea-47a0-9f10-1a82df495769">
<img width="135" alt="Screenshot 2024-11-27 at 4 12 16 PM" src="https://github.com/user-attachments/assets/92457a60-b19d-4c23-b6b8-898e6c7ec742">

Query #2: Give a monthly breakdown of the total number of transactions and total sales for each store. Make this a stored procedure so that each store can be called for, then call up “Boba Bliss”.

This query is relevant for a manager because it provides actionable insights into the sales performance of individual stores on a monthly basis. It helps the manager to identify performance trends, optimize operations, and make strategic decisions regarding staffing, inventory, and marketing. The stored procedure also makes each store's information easily accessible. 

<img width="402" alt="Screenshot 2024-11-27 at 4 15 26 PM" src="https://github.com/user-attachments/assets/fd95af64-a3fd-4e33-86f8-c721956e5f28">
<img width="213" alt="Screenshot 2024-11-27 at 4 15 39 PM" src="https://github.com/user-attachments/assets/8d2ff4b7-849b-4b40-aa39-6e1b2ae8121e">
<img width="505" alt="Screenshot 2024-11-27 at 4 16 14 PM" src="https://github.com/user-attachments/assets/318ee7b9-dd0b-4fdf-9415-17eba0fc842b">
<img width="281" alt="Screenshot 2024-11-27 at 4 16 30 PM" src="https://github.com/user-attachments/assets/6d525d37-2594-47e8-9039-a028680af113">

Query #3: List all customers along with their loyalty program details, including customers who may not have a loyalty program and loyalty programs that are not linked to any customer. For each customer, show their ID, first name, last name, loyalty program ID, and total points. Show in descending order.

This query is valuable for a manager as it provides a complete view of customer engagement with loyalty programs. It highlights both active and inactive participants, as well as loyalty programs with no customers. This data helps the manager assess program effectiveness, identify opportunities for customer retention, and make informed decisions about marketing and loyalty initiatives.

<img width="312" alt="Screenshot 2024-11-27 at 4 17 46 PM" src="https://github.com/user-attachments/assets/120d52d5-e813-471a-9d91-f845c1e78868">
<img width="139" alt="Screenshot 2024-11-27 at 4 18 06 PM" src="https://github.com/user-attachments/assets/79613235-f100-4fd2-b6da-6643104e1f83">

Query #4: List all drinks that have been sold, and then list drinks that have not been sold. Show in descending order. 

This query helps the manager track drink sales and identify both popular and underperforming products. It enables informed decisions regarding inventory, menu changes, and marketing strategies, ultimately driving sales and customer satisfaction.

<img width="310" alt="Screenshot 2024-11-27 at 4 18 45 PM" src="https://github.com/user-attachments/assets/9e750b24-2dab-4628-b756-a49f6e36d502">
<img width="125" alt="Screenshot 2024-11-27 at 4 18 56 PM" src="https://github.com/user-attachments/assets/6954c3e3-9722-43fc-b1c2-6cc4ff1a767d">

Query #5: List all the customers’ first and last name  (even if they did not make a transaction) with the total amount they spent in stores in ascending order. 

This query is useful for a manager as it provides a comprehensive view of customer spending, enabling better segmentation, targeted marketing, and customer retention strategies. By identifying both high-value and low/no-spend customers, the manager can optimize sales efforts, improve customer engagement, and drive overall business growth.

<img width="471" alt="Screenshot 2024-11-27 at 4 19 39 PM" src="https://github.com/user-attachments/assets/713c9870-d42c-4f63-a8bd-c8d7049accc4">
<img width="105" alt="Screenshot 2024-11-27 at 4 19 54 PM" src="https://github.com/user-attachments/assets/ae064127-9ff7-48d1-8ea6-83b984166012">

## Three Visualizations:

Visualization #1: Show drink performance by total profit, total quantity sold, and total revenue for each drink. Highlight the best performer and list in descending order.

A visualization of drink performance based on total profit, total quantity sold, and total revenue provides a powerful tool for managers to monitor and analyze the success of their product offerings. It allows for quick identification of best-performing drinks, informs strategic decisions regarding marketing, inventory, and sales, and ultimately helps maximize profitability and customer satisfaction.

<img width="528" alt="Screenshot 2024-11-27 at 4 21 41 PM" src="https://github.com/user-attachments/assets/14541687-9848-4685-b759-357ffe85bccb">

Visualization #2: Show store performace by revenue and list in descending order from most generated revenue to least generated revenue. 

This store performance visualization helps managers identify top-performing stores and optimize sales strategies. It provides insights for improving underperforming locations, managing resources effectively, and making informed decisions to drive revenue growth.

<img width="640" alt="Screenshot 2024-11-27 at 6 16 56 PM" src="https://github.com/user-attachments/assets/40c7ca7b-ddad-4686-b921-4eac644cc158">

Visualization #3: Show the quantity of drinks ordered per flavor.

This visualization enables managers to identify top-performing and underperforming drink flavors, helping them make data-driven decisions on inventory, promotions, and menu adjustments. It provides clear insights into customer preferences, allowing for better alignment of offerings with market demand.

<img width="458" alt="Screenshot 2024-11-27 at 6 17 32 PM" src="https://github.com/user-attachments/assets/7620c891-339c-4b1f-ae71-281a2ea4c013">

## Database Information:



Name of the database: cs_asp54028

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Qx; (where x is to be replaced by the query number).

