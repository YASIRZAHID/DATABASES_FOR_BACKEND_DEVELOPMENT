This guide contains OPERATORS and SORTING?FILTERING methods
# SQL OPERATORS
## Airthmatic operators
+
-
*
/
%

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
=
<
>
>+
<=
<> - not equal to

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
