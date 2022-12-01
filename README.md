Just some SQL notes taken during practice. 

( mainly used MySQL )

---

- **ON**  : Add condition
```
    SELECT <> FROM <> 
    ON <table name A>.<Col name A> = <table name B>.<Col name B>
```

- **AS** : Change the title of table 
```
    SELECT <> AS <> FROM <> 
    // doesn't change the database
```

- **OFFSET** : Choose the certain row 
```
    LIMIT 1 OFFSET 1
    // the output would be 2nd row 
```

- **CREATE FUNCTION** : Use function 
```
    CREATE FUNCTION SomeFunction(N INT) RETURN INT
    BEGIN
    RETURN ( ... ); 
    END
```

- **SET** : Change number in function 
```
    DECLARE A INT; 
    SET A = N - 1; 
```

- **RANK**
```
    SELECT <>, 
    RANK() OVER(
        ORDER BY <>
    ) <rank name>
    FROM <>
    // rank: 1 2 2 4 ...
```

- **DENSE_RANK**
```
    SELECT <>, 
    DENSE_RANK() OVER(
        ORDER BY <>
    ) <rank name>
    FROM <>
    // rank: 1 2 2 3 4 ...
```

- **PARTITION BY** : Partition order
```
    SELECT <>, 
    DENSE_RANK() OVER(
        PARTITION BY <>
        ORDER BY <>
    ) <rank name>
    FROM <>
    // rank: 1 2 2 3 4 1 2 1 2 3 ...
```

- **TRUNCATE TABLE**
```
    TRUNCATE TABLE <table name>
    // delete all row in table quickly
```

- ** 


