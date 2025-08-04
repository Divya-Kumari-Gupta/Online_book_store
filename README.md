# 📚 Online Bookstore SQL Project

This project is a mini-database system for managing an online bookstore. It includes table creation, data import from CSV files, and a wide range of SQL queries to analyze books, customers, and orders.

## 🧾 Database Structure

- **Books** – Stores information about books (title, author, genre, price, stock, etc.)
- **Customers** – Stores customer details (name, email, city, country)
- **Orders** – Stores order data (which customer bought which book, quantity, total amount)

## 📂 Data Import

CSV files (`Books.csv`, `Customers.csv`, `Orders.csv`) are imported using `COPY` commands.

```sql
COPY Books(Book_ID, Title, Author, Genre, Published_Year, Price, Stock) 
FROM 'path_to/Books.csv' CSV HEADER;

COPY Customers(Customer_ID, Name, Email, Phone, City, Country) 
FROM 'path_to/Customers.csv' CSV HEADER;

COPY Orders(Order_ID, Customer_ID, Book_ID, Order_Date, Quantity, Total_Amount) 
FROM 'path_to/Orders.csv' CSV HEADER;
