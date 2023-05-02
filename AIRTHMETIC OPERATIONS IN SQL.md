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

### TASK 1

```
CREATE DATABASE Chinook;
```

```
USE Chinook;
```

```
CREATE TABLE Customer (CustomerId INT NOT NULL, FirstName VARCHAR(40) NOT NULL, LastName VARCHAR(20) NOT NULL, Company VARCHAR(80), Address VARCHAR(70), City VARCHAR(40), State VARCHAR(40), Country VARCHAR(40), PostalCode VARCHAR(10), Phone VARCHAR(24), Fax VARCHAR(24), Email VARCHAR(60) NOT NULL, SupportRepId INT, CONSTRAINT PK_Customer PRIMARY KEY (CustomerId));
```

```
  INSERT INTO Customer (CustomerId, FirstName, LastName, Company, Address, City, State, Country, PostalCode, Phone, Fax, Email, SupportRepId) VALUES (1, 'Muhammad', 'Ali', 'Pakistan International Airlines', 'Jinnah International Airport', 'Karachi', 'Sindh', 'Pakistan', '75200', '+92 (21) 9903-3633', '+92 (21) 9903-3634', 'muhammad.ali@pia.com.pk', 3),(2, 'Yasir', 'Zahid', 'Pakistan State Oil', 'PSO House, Khayaban-e-Iqbal', 'Islamabad', 'Islamabad Capital Territory', 'Pakistan', '44000', '+92 (51) 111 111 PSO', '+92 (51) 920 1524', 'yasir.zahid@psopk.com', 4),(3, 'Fatima', 'Nawaz', 'National Bank of Pakistan', 'I.I. Chundrigar Road', 'Karachi', 'Sindh', 'Pakistan', '74000', '+92 (21) 99221100', '+92 (21) 99221111', 'fatima.nawaz@nbp.com.pk', 5),(4, 'Imran', 'Khan', 'Pakistan Tourism Development Corporation', 'Flashman's Hotel', 'Rawalpindi', 'Punjab', 'Pakistan', '46000', '+92 (51) 9272016', '+92 (51) 9272017', 'imran.khan@ptdc.com.pk', 3),(5, 'Saba', 'Haider', 'Mobilink Jazz', 'Mobilink House, 1- A, Kohistan Road, F-8 Markaz', 'Islamabad', 'Islamabad Capital Territory', 'Pakistan', '44000', '+92 (51) 111300300', '+92 (51) 2652960', 'saba.haider@mobilink.net', 5),(6, 'Ayesha', 'Javed', 'Telenor Pakistan', '345, Plot # 55، Huma Block', 'Lahore', 'Punjab', 'Pakistan', '54000', '+92 (42) 111 345 100', '+92 (42) 111 345 700', 'ayesha.javed@telenor.com.pk', 3);
```

```
SELECT CustomerID, FirstName, LastName, City, State, Country FROM Customer;
```

```
SELECT CustomerID, FirstName, LastName, City, State, Country FROM Customer ORDER BY FirstName;
```

```
SELECT * FROM Customer WHERE Country = "Pakistan"; 
```

```
SELECT * FROM Customer  WHERE Country = "Pakistan" ORDER BY FirstName; 
```



