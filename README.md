# `saitm` Database SQL Dumps

This document provides an overview of the two SQL dump files: `saitm_groups_studentds.sql` and `saitm_dep1.sql`. Both files are MySQL dumps for a database named `saitm`.

## 🗂️ Files Included

1.  **`saitm_groups_studentds.sql`**: Contains the table structure and data for the `groups_studentds` table.
2.  **`saitm_dep1.sql`**: Contains the table structure and data for the `dep1` table.

## ⚙️ How to Restore

You can restore this database using the following MySQL commands:

1.  **Create the database** (if it doesn't already exist):
    ```sql
    CREATE DATABASE saitm;
    ```
2.  **Use the database**:
    ```sql
    USE saitm;
    ```
3.  **Import the SQL files** (run these from your command line):
    ```sh
    mysql -u [your_username] -p saitm < saitm_groups_studentds.sql
    mysql -u [your_username] -p saitm < saitm_dep1.sql
    ```

## Database Schema

The database `saitm` contains two tables. Both tables share an identical structure.

### Table Structure (for `groups_studentds` and `dep1`)

| Column | Type |
| :--- | :--- |
| `name` | `varchar(30)` |
| `rollno` | `int` |
| `class` | `varchar(30)` |
| `grade` | `varchar(10)` |
| `marks` | `int` |

## 📊 Data Overview

### `groups_studentds` Table

  * This table contains **8 student records**.
  * All students are in the `ds-a` class.
  * The data includes names, roll numbers, marks, and grades ('A' or 'B+').
  * Example students include 'manik' (rollno 131), 'harsh' (rollno 105), and 'aakriti' (rollno 100).

### `dep1` Table

  * This table contains **9 student records**.
  * It includes a **duplicate entry** for the student 'manik' (rollno 131).
  * Similar to the other table, all students are in the `ds-a` class.
  * In this table, **all students** are listed with an 'A' grade.
