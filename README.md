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

Query #2: Give a monthly breakdown of the total number of transactions and total sales for each store. Make this a stored procedure so that each store can be called for, then call up “Boba Bliss”.

Query #3: List all customers along with their loyalty program details, including customers who may not have a loyalty program and loyalty programs that are not linked to any customer. For each customer, show their ID, first name, last name, loyalty program ID, and total points. Show in descending order.

Query #4: List all drinks that have been sold, and then list drinks that have not been sold. Show in descending order. 

Query #5: 

## Three Visualizations:

Visualization #1:

Visualization #2:

Visualization #3:


