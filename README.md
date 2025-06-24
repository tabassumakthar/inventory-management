# inventory-management
# Inventory Management System (DBMS Project - MySQL)

Inventory is the backbone of any product-based business. This system ensures that stock levels are efficiently managed, suppliers are tracked, and customer orders are fulfilled accurately and on time. By using a structured MySQL database, this project supports seamless tracking of inventory across suppliers, warehouses, and customers.

---

## Introduction

Inventory management involves tracking the movement of products from suppliers to warehouses and finally to customers. This project focuses on:

- Monitoring product levels in real time  
- Managing multiple warehouses  
- Maintaining supplier and customer records  
- Executing SQL queries for data analysis and transactions  

> *Note: The product names, suppliers, and customers in this project are inspired by characters and items from the TV show* **F.R.I.E.N.D.S**, *used here creatively to make the database more engaging and relatable.*

---

## Features

- Centralized inventory database  
- Product, supplier, and customer tracking  
- Real-time stock updates  
- MySQL-based implementation  
- Use of joins, subqueries, and aggregate functions  
- Set operations and view generation  

---

## Technologies Used

- **Database**: MySQL  
- **Query Language**: SQL (Structured Query Language)  
- **Concepts Applied**: ER Diagrams, Joins, Subqueries, Aggregates, DDL/DML  

---

## Database Schema Overview

### Product Table
- ProductID (Primary Key)  
- Name  
- Description  
- Category  
- Price  
- QuantityAvailable  
- Discount (optional)

### Supplier Table
- SupplierID (Primary Key)  
- Name  
- ContactInfo  
- Address  

### Warehouse Table
- WarehouseID (Primary Key)  
- Location  
- Capacity  
- Manager  
- ContactInfo  

### Customer Table
- CustomerID (Primary Key)  
- Name  
- ContactInfo  
- ShippingAddress  

### Orders Table
- OrderID (Primary Key)  
- CustomerID (Foreign Key)  
- OrderDate  
- Status  
- DeliveryAddress  

### Transaction Table
- TransactionID (Primary Key)  
- TransactionDate  
- Quantity  
- Amount  
- ProductID (Foreign Key)  

### Employee Table
- EmployeeID (Primary Key)  
- Name  
- Position  
- ContactInfo  
- WarehouseID (Foreign Key)  

###  Future Improvements

- Mobile app integration for real-time inventory tracking  
- Role-based user authentication and access control  
- Smart alerts for low stock and automated restocking  
- Dashboard and analytics for better decision-making

##  Sample SQL Commands

###  Table Creation (DDL)

```sql
CREATE TABLE Product (
  ProductID INT PRIMARY KEY,
  Name VARCHAR(50),
  Description VARCHAR(100),
  Category VARCHAR(50),
  Price DECIMAL(10,2),
  QuantityAvailable INT
);

CREATE TABLE Supplier (
  SupplierID INT PRIMARY KEY,
  Name VARCHAR(50),
  ContactInfo VARCHAR(100),
  Address VARCHAR(100)
);

-- Similarly create Warehouse, Customer, Orders, Transaction, and Employee tables

