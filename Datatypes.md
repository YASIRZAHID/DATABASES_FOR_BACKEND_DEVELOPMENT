This article inludes 
Datatypes
Item Navigation/Editing

# Datatype
Tells Dtabase hoe to interpret the value of the column

## Numerical Datatypes
TINYINT 0-255
INT upto 4 billion
DECIMAL

### Task 1
```
CREATE DATABASE cm_devices; 
```

```
USE cm_devices;
```

```
CREATE TABLE devices (deviceID int, deviceName varchar(50), price decimal);
```

```
SHOW tables;
```

```
SHOW columns FROM devices;
```

Optional
```  
CREATE TABLE stock (deviceID int, quantity int, totalPrice decimal);
```

## String Datatypes
CHAR      -Characters of fixed length (predetermined) e.g CAHR(50) occupies 50 char length
VARCHAR   -Characters of variable length e.g VARCHAR(50) Occupies max 50 or less 
TINYTEXT  -When less than 255 chars used (e.g PARAGRAPHS)
TEXT      -Upto 65000 chars (e.g ARTICLE)
MEDIUMTEXT-upto 16.7 million chars (e.g BOOK)
LONGTEXT  -upto 4GB text data.

### TASK 1
```
CREATE DATABASE cm_devices;
```
```
USE cm_devices
```
```
CREATE TABLE customers (username CHAR(9), fullName VARCHAR(100), email VARCHAR(255)); 
```
```
SHOW tables;
```
```
SHOW columns FROM customers; 
```
Optional
```
CREATE TABLE feedback(feedbackID CHAR(8), feedbackType VARCHAR(100), comment TEXT(500));
```
## Database Constaraints
Used to limit the type of data that can be stored in a Table.

- Columns level constraints apply to a Column
- Table level constraints apply to a table

Most commonly used constraints
**NOT NULL** - to prevent empty fields

```
CREATE TABLE FRUITS(
NAME VAR(50) NOT NULL,
QUANTITY INT NOT NULL
);
```

**DEFAULT** - Assigns default values to a field
```
CREATE TABLE FRUITS(
NAME VAR(50) NOT NULL,
QUANTITY INT NOT NULL DEFAULT 0
);
```
### Task 1
```
CREATE DATABASE cm_devices;
```

```
USE cm_devices;
```

```
CREATE TABLE address(id int not null, street varchar(255), postcode varchar(10), town varchar(30) default "Harrow");
```

```
SHOW columns FROM address;
```

Optional
```
CREATE TABLE Address (id int NOT NULL,  street VARCHAR(255), postcode VARCHAR(10) DEFAULT "HA97DE", town VARCHAR(30) DEFAULT "Harrow"); 
```

## Choosing correct Datatype

```
CREATE DATABASE cm_devices;
```

```
USE cm_devices;
```

```
CREATE TABLE invoice (customerName VARCHAR(50), orderDate DATE, quantity INT, price DECIMAL); 
```

```
SHOW tables;
```

```
SHOW columns FROM invoice; 
```

# ITEM NAVIGATION

## Creating/Deleting Database

### Creating a Database
Name of a database must be
max 63 chars and unique

```
CREATE DATABSE DATABASE_NAME;
```

### Deleting a Database
```
DROP DATABASE DATABSE_NAME;
```

## Creating/Editing/Deleting a table

### Creating a Table

```
CREATE TABLE TABLE_NAME (COLUMN1_NAME DATATPE...);
```

### Altering a TABLE

For example here we want to add another column to the table
```
ALTER TABLE table_name ADD(column_name DATATYPE);
```

For example here we want to remove a column from the table
```
ALTER TABLE table_name DROP COLUMN COLUMN_NAME;
```

For example here we are changing the previously set datatype of a column to VARCHAR(100)
```
ALTER TABLE TABLE_NAME MODIFY COLUMN_NAME VARCHAR(100);
```

### Inserting data in a table

For example here we are inserting the values in a previously created datatable
```
INSERT INTO TABLE_NAME (COLUMN1_NAME, COLUMN2_NAME, COLUMN3_NAME)
VLAUES (value1, value2, value3);
```

Here is how to add multiple rows
```
INSERT INTO TABLE_NAME (COLUMN1_NAME, COLUMN2_NAME, COLUMN3_NAME)
VLAUES (value1a, value2a, value3a),
VLAUES (value1b, value2b, value3b),
VLAUES (value1c, value2c, value3c),
VLAUES (value1d, value2d, value3d);
```

### Task 1
```
CREATE DATABASE bookshop;
```

```
USE bookshop; 
```

```
CREATE TABLE customers (customerID int, customerName varchar(50), customerAddress varchar(255));
```

```
SHOW tables;
```

```
INSERT INTO customers (customerID, customerName, customerAddress) VALUES (1, "Jack", "115 Old street Belfast");
```

```
INSERT INTO customers(customerID, customerName, customerAddress) VALUES (2, "James", "24 Carlson Rd London") ;
```

```
SELECT * FROM customers;
```

### Selecting data from a table
To get a single attribute
```
SELECT COLUMN_NAME FROM TABLE_NAME;
```
To get a multiple attributes
```
SELECT COLUMN_NAME1,COLUMN_NAME2 FROM TABLE_NAME;
```

To get all attributes
```
SELECT * FROM TABLE_NAME;
```

#### INSERT INTO SELECT
```
INSERT INTO TARGET_TABLE (TARGET_COLUMN_NAME)
SELECT SOURCE_COLUMN_NAME
FROM SOURCE_TABLE
```
##### TASK 1

```
CREATE DATABASE football_club
```

```
USE football_club; 
```

```
CREATE TABLE players (playerID int, playerName varchar(50), age int);
```

```
CREATE TABLE games(gameID INT, gameDate DATE, score INT);
```

```
SHOW tables;
```
#### SELECT tasks 
Most used select tasks include math calculations, date and time queries, concatenation functions.

### Updating data in the table
Here we are updating the column1 and column2 values
```
UPDATE TABLE_NAME
SET COLUMN_NAME1 = "VALUE1" ,COLUMN_NAME2 = "VALUE2"
WHERE PRIMARY_KEY = VALUE;
```

If we have to change values for multiple students for multiple columns then
```
UPDATE TABLE_NAME here we changed where to include all column names with similar column value
SET COLUMN_NAME1 = "VALUE1" ,COLUMN_NAME2 = "VALUE2"
WHERE COLUMN_NAME = VALUE;
```

### DELETING DATA FROM TABLE
Deletion of selective records 
```
DELETE FROM TABLE_NAME
WHERE COLUMN_NAME='VALUE'
```
Deletion of all records
```
DELETE FROM TABLE_NAME;
```

```
TRUNCATE TABLE customers;
```

```
INSERT INTO customers (customerID, customerName, customerAddress) VALUES (1, "Jack", "115 Old street Belfast"),(2, 'James', '24 Carlson Rd London'),(4, 'Maria', '5 Fredrik Rd, Bedford'),(5, 'Jade', '10 Copland Ave Portsmouth '),(6, 'Yasmine', '15 Fredrik Rd, Bedford'),(3, 'Jimmy', '110 Copland Ave Portsmouth');
```

```
DELETE FROM customers WHERE customerID = 3;
```

```
SELECT * FROM customers;
```

