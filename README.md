# Alter Table Modify
- It is used to modify the existing columns in a table, multiple columns can also be modified at once
- Syntax (for oracle and MySQL)
    ```sql
    ALTER TABLE TABLE_NAME
    MODIFY COLUMN_NAME COLUMN_TYPE
    ```
- Syntax Only for Oracle
    ```sql
    ALTER TABLE TABLE_NAME
    ALTER COLUMN COLUMN_NAME COLUMN_TYPE
    ```

# DML
The SQL command that deals with manipulation with ata present in the database belongs to DML or data and includes most of the SQL 

## List of SQL Commands
- ### select 
    - It is used to retrieve the data from database
    - Syntax
        ```sql
        SELECT col1, col2, col3 FROM TABLE WHERE condition
        ```
    - Syntax for all columns
        ```sql
        - SELECT * FROM TABLE;
        - SELECT * FROM TABLE WHERE MARKS>50;
        ```
- ### insert 
    - It is used to insert data into a table.
    - first method is specify only the value of data to be inserted without the columns names
        - Syntax
            ```sql
            - INSERT INTO table_name VALUES(value1, value2, value3, ...)
            ```
    - Columns name and VALUES
        - In the which we want to fill and their corresponding values as shown below -
            ```sql
            INSERT INTO TABLE_NAME(COL1, COL2, COL3, ...) VALUES (VAL, VAL2, VAL3, ...)
            ```
    - Using SELECT i
        - we can use select statement with `insert into` statement to copy rows from one table and the into another table. The use of this table is similar to that of the insert into statement. The difference is that the select statement is used to select the data from a different table. The different ways of using insert statement -
        1. INSERT INTO SELECT - INSERTING ALL
            ```sql
            INSERT INTO FIRST_TABLE SELECT * FROM SECOND_TABLE
            ```
        2. 
            - WE CAN COPY ONL THOSE COLUMNS WHICH WE WANT INSERT INTO DIFFERENT TABLE
                ```sql
                INSERT INTO FIRST_TABLE (NAMES_OF_COLUMNS) SELECT NAMES_OF_COLUMNS FROM SECOND TABLE
                ```
        3. Copy specify - we can copy specific rows from table to insert into another table by using where clause with the select statement
            ```sql
            INSERT INTO TABLE_1 SELECT * FROM TABLE_2 WHERE CONDITION
            ```
        4. To insert multiple rows into table using single
            ```sql
            INSERT INTO TABLE_NAME (COL1, COL2, COL3 ...)
            VALUES (VAL1, VAL2, VAL3, ...),
            (VAL1, VAL2, VAL3, ...) ...
            ```
- ### update 
    - It is used to update the data from existing table
- ### delete
    - It is used to delete records from database table

### Q1. You have a table student (NAME, ROLLNO, FATHERNAME, ADD, MARKS)
- Display the details of student whose name **Alok**
- Display the name and Roll.No of the student whose name is Amit and father's name Ragav
- Display the name and Roll.No of the student whose marks > 50
- display the name and address of the student whose  no. is 10203005060
- Display the name, and father's name and Roll.No whose marks > 50 and name is Amit

```sql
SELECT * FROM STUDENT WHERE NAME='ALOK';
SELECT NAME, ROLLNO FROM STUDENT WHERE NAME='AMIT' AND FATHERNAME='RAGAV';
SELECT NAME, ROLLNO FROM STUDENT WHERE MARKS>50;
SELECT NAME, ADD FROM STUDENT WHERE ROLLNO=10203005060;
SELECT NAME, FATHERNAME, ROLLNO FROM WHERE MARKS>50 AND NAME=AMIT;
```


```sql
SELECT * FROM STUDENT WHERE NAME='ALOK';
```

### Q2. You have a table student (NAME, ROLLNO, FATHERNAME, ADD, MARKS)
2. display the details of the student whose name starts with A.
3. display the details of the student whose name ends with Q.
4. display the details of the student having exactly 5 characters in the name and the character name is 4.
5. display the details of the student having DOB ending with 01.
6. display the details of the student whose DOB start with 11.

### Ans :
```sql
SELECT * FROM STUDENT WHERE NAME='%A';
SELECT * FROM STUDENT WHERE NAME='Q%';
SELECT * FROM STUDENT WHERE NAME='Q%';
SELECT * FROM STUDENT WHERE NAME='Q%';
SELECT * FROM STUDENT WHERE NAME='Q%';
```





### 
- Where we can use NULL values 
in the same way we can also use not NULL in the where clause