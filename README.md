# Inventory & Sales Management System

A console-based Inventory & Sales Management System developed using **Python** and **MySQL**.

## Project Overview

This project helps manage products, inventory stock, and sales records through a simple command-line interface.

The application connects Python with a MySQL database to store and manage product and sales information.

## Features

* Add new products
* View all products
* Search products
* Update product price and quantity
* Delete products
* Sell products and automatically update stock
* Low stock alerts
* View sales report
* MySQL database integration
* Input validation for price, quantity, and product ID

## Technologies Used

* Python
* MySQL
* MySQL Connector/Python
* Git & GitHub

## Database

The project uses a MySQL database named:

`inventory_db`

CREATE DATABASE inventory_db;

USE inventory_db;

CREATE TABLE products (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100) NOT NULL,
    category VARCHAR(50),
    price DECIMAL(10,2),
    quantity INT DEFAULT 0
);

CREATE TABLE sales (
    id INT PRIMARY KEY AUTO_INCREMENT,
    product_id INT,
    quantity INT,
    sale_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

### Tables

**products**

* id
* name
* category
* price
* quantity

**sales**

* id
* product_id
* quantity
* sale_date

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/deveshtiwari9794/Inventory-Sales-Management.git
```

### 2. Open the project folder

```bash
cd Inventory-Sales-Management
```

### 3. Install MySQL Connector


pip install mysql-connector-python


### 4. Create the database

Open MySQL and create:


CREATE DATABASE inventory_db;


Then create the required tables.

### 5. Configure MySQL

Update the MySQL connection details in `main.py` according to your local MySQL setup.

### 6. Run the application

python main.py

## Main Menu
1. Add Product
2. View Products
3. Search Product
4. Update Product
5. Delete Product
6. Sell Product
7. Low Stock Alert
8. Sales Report
9. Exit


## Learning Outcomes

Through this project, I practiced:

* Python programming
* MySQL database operations
* CRUD operations
* SQL queries
* Python-MySQL connectivity
* Input validation
* Git and GitHub
* Basic inventory and sales management logic

## Future Improvements

* GUI-based interface
* User login and authentication
* Product categories and filters
* Dashboard with sales statistics
* Export sales reports
* Web-based version
