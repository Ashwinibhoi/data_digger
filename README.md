# 🗄️ Data Digger – SQL Database Project

## 📌 Project Overview

**Data Digger** is a SQL-based database management project developed using MySQL. The project demonstrates fundamental and intermediate SQL operations for managing customer information, orders, products, and order details.

The main objective of this project is to practice database creation, table management, data manipulation, data retrieval, aggregate functions, subqueries, and joins.

## 🎯 Project Objectives

- Create and manage a relational database using MySQL.
- Store and manage customer information.
- Maintain order and product records.
- Perform CRUD operations (Create, Read, Update, Delete).
- Analyze sales and revenue using aggregate functions.
- Retrieve meaningful information using filtering, sorting, and grouping.
- Establish relationships between tables using primary and foreign keys.
- Combine data from multiple tables using SQL joins.

## 🛠️ Technologies Used

- **Database:** MySQL
- **Language:** SQL
- **Concepts:** DDL, DML, DQL, Aggregate Functions, Subqueries, Joins, Constraints

## 🗂️ Database Structure

**Database Name:** `DataDigger2`

The project contains four tables:

### 1. Customers

Stores customer information.

| Column | Data Type | Description |
|---|---|---|
| CustomerID | INT | Unique customer ID and primary key |
| Name | VARCHAR(50) | Customer name |
| Email | VARCHAR(100) | Customer email address |
| Address | VARCHAR(100) | Customer address |

### 2. Orders

Stores order information for customers.

| Column | Data Type | Description |
|---|---|---|
| OrderID | INT | Unique order ID and primary key |
| CustomerID | INT | References the Customers table |
| OrderDate | DATE | Date of the order |
| TotalAmount | DECIMAL(10,2) | Total order amount |

### 3. Products

Stores product details and stock information.

| Column | Data Type | Description |
|---|---|---|
| ProductID | INT | Unique product ID and primary key |
| ProductName | VARCHAR(100) | Product name |
| Price | DECIMAL(10,2) | Product price |
| Stock | INT | Available stock quantity |

### 4. OrderDetails

Stores individual product details associated with orders.

| Column | Data Type | Description |
|---|---|---|
| OrderDetailID | INT | Unique order detail ID and primary key |
| OrderID | INT | References the Orders table |
| ProductID | INT | References the Products table |
| Quantity | INT | Quantity of the product ordered |
| SubTotal | DECIMAL(10,2) | Subtotal for the order detail |

## 🔗 Database Relationships

- **Customers → Orders:** One customer can have multiple orders.
- **Orders → OrderDetails:** One order can contain multiple order detail records.
- **Products → OrderDetails:** One product can appear in multiple order detail records.

Primary keys uniquely identify records, while foreign keys establish relationships between tables.

## ⚙️ SQL Operations Performed

### 1. Database and Table Creation
- Created the `DataDigger2` database.
- Created four relational tables.
- Defined primary key and foreign key constraints.

### 2. Data Insertion
- Inserted sample customer records.
- Added order and product information.
- Inserted order details with product quantities and subtotals.

### 3. Data Manipulation
- Updated customer addresses.
- Modified order amounts and product prices.
- Deleted customers, orders, and products based on specified conditions.

### 4. Data Filtering and Sorting
- Retrieved customers by name.
- Filtered orders by customer ID and date.
- Sorted products by price in descending order.
- Used `BETWEEN` to find products within a price range.

### 5. Aggregate Functions
Used the following functions to analyze data:

- `MAX()` – Finds the highest order amount or product price.
- `MIN()` – Finds the lowest order amount or product price.
- `AVG()` – Calculates the average order amount.
- `SUM()` – Calculates total revenue or product quantities.
- `COUNT()` – Counts matching order detail records.

### 6. Grouping and Subqueries
- Used `GROUP BY` to calculate total quantities by product.
- Used `ORDER BY` and `LIMIT` to identify the top three products by quantity ordered.
- Used subqueries to find the highest-priced and lowest-priced products.

### 7. Joins
Used `JOIN` operations to combine related information from multiple tables.

**Customer Order Details:** Displays customer names, order IDs, order dates, and order amounts.

**Product Order Details:** Displays order IDs, product names, quantities, and subtotals.

## 📊 Key Features

- Customer information management
- Order tracking and amount updates
- Product price and stock management
- Sales and revenue calculations
- Product quantity analysis
- Highest- and lowest-priced product identification
- Relational data retrieval using joins
- Date-based order filtering

## ▶️ How to Run the Project

1. Install MySQL Server and a MySQL client, such as MySQL Workbench.
2. Open MySQL Workbench and connect to your database server.
3. Create a new SQL query tab.
4. Copy the SQL script into the query editor.
5. Execute the script in sequence.
6. Run the `SELECT` queries to view the results.

**Important:** The script begins with `DROP DATABASE DataDigger2;`. Running it will delete the existing database and its data if that database exists. Remove this statement if you want to preserve existing data.

## 📚 Learning Outcomes

Through this project, I practiced:

- Writing SQL queries for database management.
- Designing relational database tables.
- Using primary and foreign keys.
- Performing CRUD operations.
- Applying aggregate functions and subqueries.
- Filtering and sorting records.
- Grouping data for analysis.
- Joining multiple tables to retrieve meaningful information.

## 🚀 Future Improvements

- Add customer registration and order entry workflows.
- Calculate order totals automatically from order details.
- Add stock validation and inventory updates.
- Introduce views and stored procedures.
- Generate monthly sales reports.
- Add more sample data for advanced analysis.

## 👩‍💻 Author
      ashwini bhoi
**Project:** PR.1 – Data Digger  
**Technology:** MySQL / SQL  
**Project Type:** Database Management and SQL Practice Project

---

⭐ If you find this project useful, consider giving the repository a star on GitHub.
