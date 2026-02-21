# freeCodeCamp Celestial Bodies Database

PostgreSQL database dump for the **Celestial Bodies** project  
(part of the freeCodeCamp **Relational Database** Certification)

## Project Overview

This project consists of a PostgreSQL database named `universe` that models celestial objects with proper relationships using primary keys and foreign keys.

### Completed Requirements

- At least **5 tables**:  
  - `galaxy`  
  - `star`  
  - `planet`  
  - `moon`  
  - One additional table  `asteroid`

- Foreign keys implemented correctly between tables  
  - star → galaxy  
  - planet → star  
  - moon → planet  

- Minimum number of rows:  
  - `galaxy`: ≥ 6 rows  
  - `star`: ≥ 6 rows  
  - `planet`: ≥ 12 rows  
  - `moon`: ≥ 20 rows  
  - `asteroide`: ≥ 3 rows  

- Each table has at least 3 rows 
- Appropriate data types used (`SERIAL`, `VARCHAR`, `INTEGER`, `NUMERIC`, `TEXT`, `BOOLEAN`)  
- Constraints: `PRIMARY KEY`, `FOREIGN KEY`, `UNIQUE`, `NOT NULL` where appropriate

## Database Dump

The file **`universe.sql`** contains:
- `CREATE DATABASE` statement
- All `CREATE TABLE` statements with constraints
- All `INSERT` statements with sample data

## How to Restore the Database 

```bash
# Create an empty database
createdb universe

# Or with user 
# createdb -U postgres universe

# Restore the dump
psql -d universe -f universe.sql

# Or with user:
# psql -U postgres -d universe -f universe.sql
