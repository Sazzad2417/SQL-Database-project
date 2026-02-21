# SQL Database Project (SQLite)

## Overview

This project implements a relational database using **SQLite** to model
a simple inventory management system.

The database includes: - 3 related tables - 1000+ records in one table -
Foreign key relationships - A composite key - Nominal, ordinal,
interval, and ratio data types - Fully synthetic (randomly generated)
data

------------------------------------------------------------------------

## Database Tables

### 1. product_category

Stores product categories.

### 2. product_information

Stores product details and links to product_category.

### 3. product_purchase_details

Stores batch-level purchase records and links to product_information.

Relationships: product_category (1) → product_information (1) →
product_purchase_details (many)

------------------------------------------------------------------------

## Dataset Summary

  Table                      Records
  -------------------------- ---------
  product_category           5
  product_information        50
  product_purchase_details   1040

------------------------------------------------------------------------

## How to Run (SQLite)

1.  Open Command Prompt\
2.  Navigate to folder: cd C:`\sqlite`{=tex}
3.  Start SQLite: sqlite3 inventory.db
4.  Enable foreign keys: PRAGMA foreign_keys = ON;
5.  Load the file: .read pms_sqlite.sql

------------------------------------------------------------------------

## Sample Queries

Count records: SELECT COUNT(\*) FROM product_purchase_details;

Find oldest expiry date: SELECT MIN(expire_date) FROM
product_purchase_details;

------------------------------------------------------------------------

## Ethical Considerations

-   No real personal data used\
-   All data is synthetic\
-   No external datasets downloaded

------------------------------------------------------------------------

Developed for SQL Database Project Assignment by Md Sazzad Hosen Khan.
