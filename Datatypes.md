# Datatype
Tells Dtabase hoe to interpret the value of the column

# Numerical Datatypes
TINYINT 0-255
INT upto 4 billion
## Task 1
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

