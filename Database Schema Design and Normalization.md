# DATABASE SCHEMA
Blueprint of how your data looks like (this process is also known as **Data Modelling**)
Generally its referred to as organization of information and its relationship
In MYSQL its a collection of data structures within a database
In SQL server its a collection of individual but related components
In Posgre SQL its a namespace with named database objects
In Oracle its a propert of each respective database user

Working however remains the same **Organization of data in form of tables** and **Relationships between the tables **

Schema objects are tables, row, columns ....

Database Schema includes:
1. Data Relationships
2. Unique Object Keys
3. Name and Datatypes

Advantages of Schema
1. Management - provides logical grouping for projects.
2. Accessibility - Enables greater accessibility to objects.
3. Security - offers a range of useful security features.
4. Ownership - permits ownership transfers between users.

## TYPES OF SCHEMA
1. Conceptual/Logical Schema- Defines entities, attributes and relationships. (Entity relationship modelling)
2. Internal/Physical Schema- Defines the actual storage of data and access paths.(the actual code)
3. External/View Schema- Defines diffrent user views.

Creating a simple table
```
create table table_name(
FIELD DATATYPE...,
PRIMARY KEY (PRIMARY_KEY_FIELD),
)
```

Here's another table linking to other tables primary key
```
create table table_name(
FIELD DATATYPE...,
PRIMARY KEY (PRIMARY_KEY_FIELD),
FOREIGN KEY (FOREIGN_KEY_FIELD) REFRENCES OTHER_TABLE(FOREIGN_KEY_FIELD);
)
```
### TASK

```
CREATE TABLE tbl( 

    table_id INT, 

    location VARCHAR(255), 

    PRIMARY KEY (table_id) 

); 
```

```
CREATE TABLE waiter( 

    waiter_id INT, 

    name VARCHAR(150), 

    contact_no VARCHAR(10), 

    shift VARCHAR(10), 

    PRIMARY KEY (waiter_id) 

); 
```

```
CREATE TABLE table_order( 

    order_id INT, 

    date_time DATETIME, 

    table_id INT, 

    waiter_id INT, 

    PRIMARY KEY (order_id), 

    FOREIGN KEY (table_id) REFERENCES tbl(table_id), 

    FOREIGN KEY (waiter_id) REFERENCES waiter(waiter_id) 

); 
```

```
CREATE TABLE customer( 

    customer_id INT, 

    name VARCHAR(100), 

    NIC_no VARCHAR(12), 

    contact_no VARCHAR(10), 

    PRIMARY KEY (customer_id) 

); 
```

```
CREATE TABLE reservation( 

    reservation_id INT, 

    date_time DATETIME, 

    no_of_pax INT, 

    order_id INT, 

    table_id INT, 

    customer_id INT, 

    PRIMARY KEY (reservation_id), 

    FOREIGN KEY (order_id) REFERENCES table_order(table_id), 

    FOREIGN KEY (table_id) REFERENCES tbl(table_id), 

    FOREIGN KEY (customer_id) REFERENCES customer(customer_id) 

); 
```

```
CREATE TABLE menu( 

    menu_id INT, 

    description VARCHAR(255), 

    availability INT, 

    PRIMARY KEY (menu_id) 

); 
```

```
CREATE TABLE menu_item( 

    menu_item_id INT, 

    description VARCHAR(255), 

    price FLOAT, 

    availability INT, 

    menu_id INT, 

    PRIMARY KEY (menu_item_id), 

    FOREIGN KEY (menu_id) REFERENCES menu(menu_id) 

); 
```

```
CREATE TABLE order_menu_item( 

    order_id INT, 

    menu_item_id INT, 

    quantity INT, 

    PRIMARY KEY (order_id,menu_item_id), 

    FOREIGN KEY (order_id) REFERENCES table_order(order_id), 

    FOREIGN KEY (menu_item_id) REFERENCES menu_item(menu_item_id) 

); 
```
## Table Relationships
### ER(Entity Relationship) DIAGRAM
Square (column) links to Diamond links to Square (destination column)
Crow foot for one to many and many to one

### Primary Key
**Degree is the number of columns/attributes**
**Cardinality is the number of records**
**Candidate key is the one that is unique for each record**
**Candidate key not selected as primary key becomes secondary key**

### Foreign Key
Create table 1
```
CREATE TABLE vehicle( vehicleID varchar(10), ownerID varchar(10), plateNumber varchar(10), phoneNumber INT);
```
Create table2
```
CREATE TABLE Owner(ownerID VARCHAR(10), ownerName VARCHAR(50), ownerdrerss  VARCHAR(255), PRIMARY KEY (ownerID));
```
Add foreign key in table 1
```
ALTER TABLE vehicle ADD FOREIGN KEY (ownerID) REFERENCES owner (ownerID);
```
### Finding Entities
**Atributes can be Derived, Multi-valued or Key**

# Database Normalization
Process of structuring tables that minimizes challenges in batabase systems by reducing
**Data duplcation, avoiding data modifcation implications and helping to simplify data queries from database**
Multipurpose tables cause problems some of them being **Insert anomally, Update Anomally,Deletion Anomally **

## Problems

### Insert Anomally
When one of the fields is not yet available however required to fill the table.

### Update Anomally
One update requires further updates in one or multiple other other columns.

### Deletion Anomally
Deletion of a record results in deletion of some other necessary/required data.

## Solution
Break the multipupose into multiple single purpose tables.
### First Normal Form 1NF
Enforces data atomicity and eliminates unnecessary repeating groups of data in database tables.
**Data Atomicity means that there can only be one single instance value per column field(one value per field) this reduces data redundancy and in accuracy**


