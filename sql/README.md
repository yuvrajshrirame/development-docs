# SQL

> Class notes of SQL taken from PWSkills by Yuvraj Shrirame.

## Types of Languages:

### 1. Imperative Language

    Ex: Ruby, C, C++, Java, JavaScript

### 2. Declarative Language

    Ex: SQL

# SQL

- SQL → Structured Query Language
- SQL is a Declarative Language and is used to interact with the Relational Database
- SQL is case-insensitive

# SQL Commands

## Clear Console

```sql
SYSTEM CLS;
```

## Listing Existing Databases

```sql
SHOW DATABASES;
```

## Creating Database

```sql
CREATE DATABASE DB_NAME;
```

## Selecting Database (For Performing Operations within it)

```sql
USE DB_NAME;
```

## Deleting Database

```sql
DROP DATABASE DB_NAME;
```

## Creating Tables

```sql
CREATE TABLE TABLE_NAME (COL_1 VARCHAR(100), COL_2 INTEGER);
```

Ex:

```sql
CREATE TABLE PRODUCT (Name VARCHAR(100), Rating INTEGER);
```

## Adding/Inserting Data into Tables

```sql
INSERT INTO TABLE_NAME (COL_1, COL_2) VALUES ("VALUE1", "VALUE2");
```

Ex:

```sql
INSERT INTO TABLE_NAME (Name, Rating) VALUES ("Avengers Endgame", 5);
```

## Listing Tables in a Database

```sql
SHOW TABLES;
```

## Listing Table Content

```sql
SELECT COL_1, COL_2 FROM TABLE_NAME;
/* To select all the columns, we use asterisk (*) */
SELECT * FROM TABLE_NAME;
```

Ex:

```sql
SELECT Name, Rating FROM movies_db;
/* OR we can use (*) to select all the columns */
SELECT * FROM movies_db;
```

## Adding Multiple Items into Table at Once

```sql
INSERT INTO TABLE_NAME (COL_1, COL_2) VALUES (VALUE1, VALUE2), (VALUE3, VALUE4), (VALUE5, VALUE6);
```

Ex:

```sql
INSERT INTO moviesTable (Name, Actor) VALUES ("Iron Man", "Downey JR"), ("Thor", "Chris H."), ("Wednesday", "Jenna Ortega");
```

## Where Clause & Conditions

```sql
SELECT * FROM TABLE_NAME WHERE CONDITION;
```

Ex:

```sql
SELECT * FROM MOVIES_TABLE WHERE ACTORS_GENDER = "Male";
SELECT * FROM MOVIES_TABLE WHERE ACTORS_NETWORTH >= 1500;
SELECT * FROM MOVIES_TABLE WHERE ACTORS_NETWORTH >= 1500 OR ACTORS_NETWORTH <= 1000;
/* AND, OR can also be used in the MySQL to apply multiple conditions */
```

## Like Keyword (For Prefix, Suffix Matching)

```sql
// SUFFIX MATCHING
SELECT * FROM TABLE_NAME WHERE COL_NAME LIKE "%ABC";
// PREFIX MATCHING
SELECT * FROM TABLE_NAME WHERE COL_NAME LIKE "ABC%";
// SUBSTRING MATCHING (IN-BETWEEN)
SELECT * FROM TABLE_NAME WHERE COL_NAME LIKE "%ABC%";
```

Ex:

```sql
// SUFFIX MATCHING
SELECT * FROM ACTORS WHERE FirstName LIKE "%Ch";
// PREFIX MATCHING
SELECT * FROM ACTORS WHERE FirstName LIKE "Ch%";
// SUBSTRING MATCHING (IN-BETWEEN)
SELECT * FROM ACTORS WHERE FirstName LIKE "%A%";
```

## Sorting using ORDER BY

```sql
// ASCENDING SORTING
SELECT * FROM TABLE_NAME ORDER BY COL_NAME ASC;
// DESCENDING SORTING
SELECT * FROM TABLE_NAME ORDER BY COL_NAME DESC;
```

Ex:

```sql
SELECT * FROM MOVIES_TABLE ORDER BY NETWORTH ASC;
SELECT * FROM MOVIES_TABLE ORDER BY NETWORTH DESC;
// MORE COMPLEX COMBINATIONS DO SUPPORT SORTING
SELECT * FROM ACTORS WHERE FirstName LIKE "%A%" ORDER BY NETWORTH ASC;

// SORTING STRINGS
SELECT * FROM ACTORS ORDER BY FirstName ASC;
SELECT * FROM ACTORS WHERE FirstName LIKE "%A%" ORDER BY FirstName ASC;
```

## Pagination using LIMIT and OFFSET

NOTE: You’ll have to use both LIMIT and OFFSET to perform Pagination

```sql
SELECT * FROM TABLE_NAME LIMIT 5 OFFSET 0;
// THE ABOVE STATEMENT MEANS: IT WILL SHOW 5 ROWS STARTING FROM 0 (0 -> FIRST ROW)
SELECT * FROM TABLE_NAME LIMIT 5 OFFSET 5;
// THE ABOVE STATEMENT WILL LIST THE NEXT 5 ROWS (I.E. PAGINATION)
```

## Updating Values/Records

```sql
UPDATE TABLE_NAME SET COL = VAL WHERE CONDITION;
```

Ex:

```sql
UPDATE ACTORS SET NETWORTH = 500 WHERE FirstName = "Chadwick";
```

## Deleting Values/Records

```sql
DELETE FROM TABLE_NAME WHERE CONDITION;
```

Ex:

```sql
DELETE FROM ACTORS WHERE FIRSTNAME = "Chris";
```

## DESC Command

```sql
// DESC COMMAND IS USED TO DESCRIBE THE TABLE
DESC TABLE_NAME;
```

## Primary Key

- Primary key is an UNIQUE ID given to the rows

```sql
CREATE TABLE CUSTOMERS (
   ID INT NOT NULL,
   NAME VARCHAR (20) NOT NULL,
   AGE INT NOT NULL,
   ADDRESS CHAR (25),
   SALARY DECIMAL (18, 2),
   PRIMARY KEY (ID) // Primary Key
);
```

## Joins

- Combines two or more tables to access the records from both the tables
- Joins can be used till any extent

```sql
SELECT COL_of_TABLE_1, COL_of_TABLE_2 FROM TABLE_1 JOIN TABLE_2 ON TABLE_1.COL_of_TABLE_1 = TABLE_2.COL_of_TABLE_2;
```

## Aliases

- Alias is basically a nickname for any column or anything

```sql
SELECT FIRST_NAME AS FST, LAST_NAME AS LST FROM TABLE_NAME;
```

## Conditionals in SQL

- It is used to perform IF-ELSE type of queries

```sql
SELECT
    CASE
        WHEN A + B > C AND B + C > A AND A + C > B THEN
            CASE
                WHEN A = B AND B = C THEN 'Equilateral'
                WHEN A = B OR B = C OR C = A THEN 'Isosceles'
                ELSE 'Scalene'
            END
        ELSE 'Not A Triangle'
    END
FROM TRIANGLES;
```

## Count

- It is used to count the elements

```sql
SELECT COUNT(*) FROM ACTORS WHERE CITY = "TEXAS";
// IT WILL PRINT THE NO. OF ACTORS THAT LIVE IN TEXAS
```

## Distinct

- It is used to refine the records which aren’t repeated

```sql
SELECT DISTINCT DISTRICT FROM ACTORS;
```

## Group By

- It is used to return a single row which is present at multiple places

```sql
SELECT COUNT(*), DISTRICT FROM ADDRESS GROUP BY ADDRESS;
// HERE, GROUP BY RETURNS ALL THE UNIQUE DISTRICTS WITH ITS COUNT
```
