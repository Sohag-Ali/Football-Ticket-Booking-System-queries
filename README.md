# SQL Queries Assignment

A PostgreSQL database project demonstrating table creation, relationships, and SQL queries using JOINs, Aggregate Functions, Subqueries, and Constraints.

## ERD Desing Link 
https://drawsql.app/draw?t=41b89096-e5ec-4da2-84b8-484439bcccd9&view=1

## 📌 Project Overview

This project is designed to practice and demonstrate SQL database concepts including:

- Database Creation
- Table Creation
- Primary Key & Foreign Key
- Data Insertion
- Data Retrieval
- JOIN Operations
- Aggregate Functions
- Filtering & Sorting
- Grouping Data

## 🗄️ Database Schema

### Users Table

| Column | Type |
|----------|----------|
| user_id | SERIAL PRIMARY KEY |
| full_name | VARCHAR(100) |
| email | VARCHAR(100) |

### Bookings Table

| Column | Type |
|----------|----------|
| booking_id | SERIAL PRIMARY KEY |
| user_id | INTEGER (FK) |
| booking_date | DATE |

## 🛠️ Technologies Used

- PostgreSQL
- Beekeeper Studio
- SQL

## 📋 Queries Implemented

### 1. Retrieve all users

```sql
SELECT * FROM Users;
```

### 2. Retrieve all bookings

```sql
SELECT * FROM Bookings;
```

### 3. LEFT JOIN Example

```sql
SELECT
    u.user_id,
    u.full_name,
    b.booking_id
FROM Users u
LEFT JOIN Bookings b
ON u.user_id = b.user_id;
```

### 4. Count Total Bookings

```sql
SELECT COUNT(*) AS total_bookings
FROM Bookings;
```

### 5. Group By Example

```sql
SELECT
    user_id,
    COUNT(*) AS booking_count
FROM Bookings
GROUP BY user_id;
```

## 🚀 How to Run

1. Install PostgreSQL
2. Create a database
3. Execute the schema.sql file
4. Execute the queries.sql file
5. Verify results in Beekeeper Studio

## 📂 Files

- schema.sql
- insert_data.sql
- queries.sql
- README.md

## 👨‍💻 Author

Sohag Ali