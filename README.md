# DATABASES_FOR_BACKEND_DEVELOPMENT
NOTES FOR FUTURE REFRENCING

# TYPES OF DATABASES
RELATIONAL DATABASES
OOP DATABASES >> DATA:OBJECTS >>
GRAPH DATABASES >> DATA:NODES >> RELATION:EDGES
DOCUMENT DATABASES >> DATA:JSON >> ORGNIZED IN TABLES

# HOSTING
DEDICATED MACHINE
CLOUD

CLOUD IS PREFFERED BECAUSE IT ALLOWS TO
STORE MANAGE RETRIEVE DATA
ACCESS DATA VIA INTERNET
LOW COST OPTION

# HOW TO CREATE RELATION DATA:
EACH INSTANCE SHOULD HAVE UNIQUE IDENTIFIERS i.e: PRIMARY KEYS

# TYPES OF CHARTS USED TO PRESENT DATA
BAR CHARTS
BUBBLE CHARTS
LINE CHARTS
PIE CHARTS
DUAL AXIS CHARTS
GANTT CHARTS
HEAT MAPS
SCATTER PLOT CHARTS

GRAPH IS CHOOSEN ON BASES OF TAGET AUDIENCE, INFORMATION, GOAL.

# ALTERNATIVE TYPES OF DATABASES
RELATIONAL DATABASES MOSTLY STORE STRUCTURAL DATA SO THERE IS LIMITATION TO TYPE OF DATA THEY CAN STORE.SO FOR NON STRUCTURA DATABASES NOSQL DATABASES ARE USED BECAUSE THEY PROVIDE FLEXIBLE AND SCALABLE DATA STRUCTURE.(CURRENTLY USED BY AI SOCIAL MEDIA IOT DEVICES)
## TYPES OF NOSQL DATABASES
DOCUMENT DATABASES
KEY-VALUE DATABASES
GRAPH DATABASES

## DIG DATA
COMPLEX DATA THAT INCREASES IN VOLUME WITH TIME
includes variety of data types
more powerful than traditional data
provides unique insight

e.g used by manufacturing sector, retail, telecommunication

## cloud hosting
requires no infrastructure, maintenance, storage costs
many providers
more affordble

## BUSSINESS INTELLIGENCE
analyze the data to perform informed decissions

# Evolution of databases
## Flat files
Simple text files one line contains one record 
Separated by comma white space tabs

## Hierarichal databases
Hierarichally arranged

## Network Databases
This database allows multiple parent child relationships
a member can have multiple owners

## Relational Databases
Most used batabase system 
Data is stored in a table 
Each column holds one attribute
Each row is a record with unique ID i.e Primary Key
Access/Linking to other database is granted using Foreign Key

## Object Oriented DataBases
Work in frameworks of real programming languages.
Data is presented as an Object

## NoSQL databases
Used For Unstructured data
Data can be stored in adhoc manner
Data can be of different types
Can handle Bigdata

### diffeent types of NoSQL databases
Document Databases
Key-Value databases
Wide-Column Databases
Graph databases

# Atomicity Consistency Isolation Durability(ACID)
these are the properties every transaction must posses

# What is Structured Query Language
used to interact with databases

## relational databases SQL can interact with
MySQL
PostgreSQL
Oracle
Microsoft SQL Server

## how database interprets instructions given using SQL
Using database management system(DBMS)

## CRUD
Create Read Update Delete are most common operations

# Categorization of SQL on usage basses i.e: subsets
DDL Data Definition Language
DML Data Manipulation Language
DQL Data Query Language
DCL Data Control Language

## Data Definition Language
Helps you define data in your database
Command to create tables
    Create
Command to alter tables
    Alter
Command to remove existing column/object
    Drop

## Data Manipulation Language
Helps you manipulate data most CRUD operations are done here
Command to insert data to a field
    Insert
Command to update existing data 
    Update
Command to delete existing data
    Delete
## Data Query Language
Used to read and retrieve data
Command to get preffered data row/column
    Select

## Data Control Language
To control who can access database
Command to give access 
    Grant
Command to block access
    Revoke
