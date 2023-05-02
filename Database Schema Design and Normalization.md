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
1. Conceptual/Logical Schema- Defines entities, attributes and relationships.
2. Internal/Physical Schema- Defines the actual storage of data and access paths.
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
