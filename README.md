# Travel Booking Management System

## Overview

The **Travel Booking Management System** is a SQL-based database project designed to simulate the core operations of a travel booking platform. The system manages customers, bookings, payments, transportation, destinations, and related travel information through a structured relational database.

The project focuses on applying core and advanced SQL concepts such as **DDL, DML, constraints, joins, subqueries, views, aggregate functions, and database normalization**.

## Project Highlights

* Designed and normalized **10 interlinked relational tables** to maintain data consistency and reduce redundancy.
* Worked with **8+ interconnected datasets** representing different components of a travel booking ecosystem.
* Developed **25+ SQL queries** covering basic to advanced database operations.
* Implemented customer booking, payment processing, transport availability, and revenue analysis.
* Added **50+ sample records** to simulate real-world travel booking scenarios.
* Integrated multiple transportation modes within a single database system.
* Applied primary keys, foreign keys, unique constraints, and other integrity constraints to maintain reliable relationships between tables.

## SQL Concepts Used

### DDL — Data Definition Language

Used SQL commands to design and manage the database structure.

```sql
CREATE TABLE
ALTER TABLE
DROP TABLE
TRUNCATE TABLE
```

### DML — Data Manipulation Language

Used DML commands to insert, update, delete, and retrieve data.

```sql
INSERT
UPDATE
DELETE
SELECT
```

### Constraints

Implemented database constraints to maintain data integrity.

* PRIMARY KEY
* FOREIGN KEY
* UNIQUE
* NOT NULL
* CHECK
* DEFAULT

### Joins

Used different types of joins to retrieve information distributed across multiple tables.

```sql
INNER JOIN
LEFT JOIN
RIGHT JOIN
SELF JOIN
```

Example use cases include:

* Retrieving customers along with their booking information
* Displaying booking and payment details
* Finding available transportation for destinations
* Connecting customers, bookings, destinations, and transport details

### Subqueries

Implemented nested queries for retrieving complex information such as:

* Customers with specific booking conditions
* Transportation options based on availability
* Bookings above average cost
* Destination-based travel analysis
* Customer and payment-based filtering

### Aggregate Functions

Used SQL aggregate functions for data analysis.

```sql
COUNT()
SUM()
AVG()
MAX()
MIN()
```

These were used for operations such as:

* Calculating total revenue
* Finding average booking cost
* Counting bookings per customer
* Finding popular destinations
* Analyzing transportation usage

### Views

Created SQL views to simplify frequently required queries and provide reusable representations of complex data.

Views were used for:

* Booking summaries
* Customer travel history
* Payment information
* Revenue analysis

## Database Design

The database contains **10 normalized and interconnected tables** representing major components of the travel system.

The logical database modules include:

* Customer Management
* Booking Management
* Destination Management
* Payment Management
* Transportation Management
* Travel Availability
* Accommodation / Travel Services
* Booking History

Relationships between the tables are maintained using **Primary Keys and Foreign Keys**.

## Database Normalization

The database schema was normalized to reduce data redundancy and maintain data consistency.

Normalization helps:

* Avoid duplicate records
* Maintain data integrity
* Simplify database updates
* Improve database organization
* Establish meaningful relationships between entities

## Major Functionalities

### Customer Management

Stores and manages customer information required for travel bookings.

### Travel Booking

Allows customer bookings to be connected with destinations, transport services, and related travel information.

### Payment Processing

Maintains payment details associated with customer bookings.

### Transport Management

Supports multiple modes of transportation and manages their availability.

### Booking Analysis

SQL queries can be used to analyze booking patterns and retrieve detailed customer travel information.

### Revenue Analytics

Aggregate queries are used to analyze revenue generated through bookings and payments.

## Sample Query

Example of retrieving booking information along with customer details:

```sql
SELECT
    c.customer_id,
    c.customer_name,
    b.booking_id,
    b.booking_date
FROM Customer c
JOIN Booking b
ON c.customer_id = b.customer_id;
```

Example of revenue calculation:

```sql
SELECT SUM(amount) AS total_revenue
FROM Payment;
```

Example using a subquery:

```sql
SELECT *
FROM Booking
WHERE amount > (
    SELECT AVG(amount)
    FROM Booking
);
```

> Table and column names may vary depending on the final database schema.

## Project Statistics

| Component           | Details                                                       |
| ------------------- | ------------------------------------------------------------- |
| Database            | SQL                                                           |
| Tables              | 10                                                            |
| Datasets / Entities | 8+                                                            |
| SQL Queries         | 25+                                                           |
| Sample Records      | 50+                                                           |
| Key Concepts        | DDL, DML, Constraints, Joins, Subqueries, Views, Aggregations |
| Domain              | Travel & Booking Management                                   |

## How to Run

1. Clone the repository.

```bash
git clone <repository-url>
```

2. Open your SQL environment such as:

* MySQL Workbench
* MySQL Command Line
* PostgreSQL
* Oracle SQL Developer
* VS Code with SQL extensions

3. Create the database.

```sql
CREATE DATABASE TravelBookingManagement;
```

4. Execute the table creation / schema SQL file.

5. Execute the sample data insertion file.

6. Run the SQL query file to explore the implemented operations and analytics.

## Possible Repository Structure

```text
Travel-Booking-Management-System/
│
├── README.md
├── schema.sql
├── data.sql
├── queries.sql
├── views.sql
└── database-design/
```

## Key Learnings

Through this project, I gained practical experience in:

* Designing relational databases
* Database normalization
* Creating relationships using primary and foreign keys
* Writing complex SQL joins
* Implementing nested queries and subqueries
* Creating reusable SQL views
* Performing aggregate and analytical queries
* Maintaining data consistency using constraints
* Translating real-world business requirements into relational database structures

## Conclusion

The Travel Booking Management System demonstrates how a relational database can be used to model a real-world travel ecosystem. By integrating customer information, bookings, payments, destinations, and multiple transportation modes, the project provides practical experience with database design and advanced SQL querying.

The project serves as a comprehensive implementation of fundamental and advanced SQL concepts while demonstrating their application to a realistic business use case.
