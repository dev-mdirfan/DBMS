# Alter Table Modify
- It is used to modify the existing columns in a table, multiple columns can also be modified at once
- Syntax (for oracle and MySQL)
    - alter table table_name
    - modify column_name column_type

- Only for Oracle
    - alter table table_name
    - alter column column_name column_type

# DML
The SQL command that deals with manipulation with ata present in the database belongs to DML or data and includes most of the SQL 

- List of SQL Commands
    - select 
        - It is used to retrieve the data from database
        - Syntax
            - select column1, column2, column3 from table where condition
        - Syntax for all columns
    - insert 
        - It is used to insert data into a table
    - update 
        - It is used to update the data from existing table
    - delete
        - It is used to delete records from database table

### Q1. You have a table student (NAME, ROLLNO, FATHERNAME, ADD, MARKS)
- Display the details of student whose name Alok
- Display the name and Roll.No of the student whose name is Amit and father's name Ragav
- Display the name and Roll.No of the student whose marks > 50
- display the name and address of the student whose  no. is 10203005060
- Display the name, and father's name and Roll.No whose marks > 50 and name is Amit

<pre>
SELECT * FROM STUDENT WHERE NAME='ALOK';
SELECT NAME, ROLLNO FROM STUDENT WHERE NAME='AMIT' AND='RAGAV';
SELECT NAME, ROLLNO FROM STUDENT WHERE MARKS>50;
SELECT NAME, ADD FROM STUDENT WHERE ROLLNO=10203005060;
SELECT NAME, FATHERNAME, ROLLNO FROM WHERE MARKS>50 AND NAME=AMIT;
</pre>