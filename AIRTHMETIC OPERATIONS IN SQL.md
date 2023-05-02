This guide contains OPERATORS and SORTING?FILTERING methods
# SQL OPERATORS
## Airthmatic operators
```
+
-
*
/
%
```

### REAL LIFE EXAMPLES
```
SELECT column_name1 + column_name2 FROM table_name; 
```
To get total salary we can use
```
SELECT salary + allowance FROM employee; 
```
Getting Employees with 25000 salary
```
SELECT * FROM employee WHERE salary + allowance = 25000; 
```


```
SELECT column_name1 - column_name2 FROM table_name;  
```
Salary excluding tax
```
SELECT salary - tax FROM employee; 
```




## Comparison operators
```
=
<
>
>=
<=
<> - not equal to
```

### Examples
Record of employee ID=1
```
SELECT * FROM employee WHERE employee_id = 1; 
```
Record of employee named Yasir
```
SELECT * FROM employee WHERE employee_name = 'Yasir'; 
```
Employees with salary not 24000
```
SELECT *  FROM employee WHERE salary <> 24000; 
```

## Sorting and Filtering of Data

### ORDER BY clause
Used to sort data in ascendng / descending order (applicable for numerical and string type data)
For ascending order based on column name we can write (if not specified ASC is default order by setting)
```
SELECT COLUMN_NAME1, COLUMN_NAME2, COLUMN_NAME3, COLUMN_NAME4 FROM TABLE_NAME ORDER BY COLUMN_NAME ASC;
```
For descending order based on column name we can write
```
SELECT COLUMN_NAME1, COLUMN_NAME2, COLUMN_NAME3, COLUMN_NAME4 FROM TABLE_NAME ORDER BY COLUMN_NAME DESC;
```
Order by for multiple columns
```
Select * FROM table_name ORDER BY column_name1, column_name2 ASC|DESC; 
```

### WHERE clause
Used to filter data that satisfy a specific condition
Mostly used with 
-Comparison operator
-Logical operators
--BETWEEN
  Used to filter records between specific numeric, date, time  range.
--LIKE
  Specify pattern within the search criteria.
--IN
  Used to specify multiple possible values for column.
Others include 
```
ALL
AND
ANY
EXISTS
NOT
OR 
IS NULL
UNIQUE
```

```
SELECT * FROM employee WHERE salary + allowance = 25000; 
```

```
SELECT * FROM students WHERE department = 'engineering'; 
```
#### BETWEEN example
Filtering out same age slot students
```
SELECT * FROM students WHERE DOB = BETWEEN "01-12-2010" AND "01-12-2011";
```

#### LIKE example
Filtering out values starting with 'Sc' followed by any number of keywords
```
SELECT * FROM students WHERE faculty LIKE 'sc%';
```

#### IN example
FILTERING OUT STUDENTS STUDYING IN PAKISTAN AND TURKEY
```
SELECT * FROM students WHERE country IN ('PAKISTAN','TURKEY');
```

These can also be used in update and delete statements....









