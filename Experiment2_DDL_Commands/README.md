# Experiment 2: DDL Commands
```
NAME: HARI NIVEDHAN P
REG.NO: 212224220031
```
## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
---
<img width="920" height="420" alt="image" src="https://github.com/user-attachments/assets/8280588c-faa3-42d1-be63-242446205841" />


```sql
Create TABLE Customers(
CustomerID INTEGER,
Name TEXT,
Email TEXT,
JoinDate DATETIME);
```

**Output:**
<img width="1267" height="446" alt="image" src="https://github.com/user-attachments/assets/da12464e-a259-4f74-a6c6-50cfd4d06c0f" />


**Question 2**
---
<img width="870" height="422" alt="image" src="https://github.com/user-attachments/assets/ef56bca8-0caf-40f4-9f99-71e0263c7828" />


```sql
CREATE TABLE Employees(
EmployeeID INTEGER,
FirstName TEXT,
LastName TEXT,
HireDate DATE);
```

**Output:**
<img width="1264" height="361" alt="image" src="https://github.com/user-attachments/assets/045eb54f-bb53-4126-a293-61b683f4528d" />


**Question 3**
---
<img width="998" height="237" alt="image" src="https://github.com/user-attachments/assets/f2969fa2-4e81-442c-998f-69a860534c90" />


```sql
INSERT INTO Products(ProductID,Name,Category,Price,Stock) VALUES (101,'Laptop','Electronics',1500,50);
```

**Output:**
<img width="1260" height="281" alt="image" src="https://github.com/user-attachments/assets/ac2da9c2-083e-46b1-bb1c-edde278929de" />


**Question 4**
---
<img width="875" height="378" alt="image" src="https://github.com/user-attachments/assets/9eaffddd-13f5-4375-8e31-c66d06421e55" />


```sql
CREATE TABLE Events(
EventID INTEGER,
EventName TEXT,
EventDate DATE);
```

**Output:**
<img width="1263" height="429" alt="image" src="https://github.com/user-attachments/assets/8d9d12b0-18fa-4e52-b01c-96e85da36c8b" />


**Question 5**
---
<img width="972" height="543" alt="image" src="https://github.com/user-attachments/assets/0c3c34ae-9b7e-4767-8c9d-923c425fe39c" />


```sql
ALTER TABLE Student_details
ADD Mobilenumber number
```

**Output:**
<img width="1272" height="396" alt="image" src="https://github.com/user-attachments/assets/e5b28c0e-db8b-4dd9-9be6-34411f4cd61a" />


**Question 6**
---
<img width="1132" height="228" alt="image" src="https://github.com/user-attachments/assets/22945a4e-9747-4d07-95d3-b6bf6ebdaa38" />


```sql
INSERT INTO Products(PRODUCTID ,Name, Category, Price, Stock) VALUES (104, 'Tablet', 'Electronics',100,50);
```

**Output:**
<img width="1260" height="300" alt="image" src="https://github.com/user-attachments/assets/3f818bda-f9f5-462d-b517-82cf7d0cc33d" />


**Question 7**
---
<img width="1258" height="386" alt="image" src="https://github.com/user-attachments/assets/57813611-71a9-4676-91ff-3999361263c1" />


```sql
CREATE TABLE Products (
    ProductID INTEGER PRIMARY KEY,
    ProductName TEXT UNIQUE NOT NULL,
    Price REAL CHECK (Price > 0),
    StockQuantity INTEGER CHECK (StockQuantity >= 0)
);

```

**Output:**
<img width="1260" height="334" alt="image" src="https://github.com/user-attachments/assets/de3a4fb9-2a47-43b5-92f2-ba1dff3b8e56" />


**Question 8**
---
<img width="878" height="361" alt="image" src="https://github.com/user-attachments/assets/53c8e7dd-85d0-4cb1-9359-c41995bf9db0" />


```sql
CREATE TABLE Tasks (
    TaskID INTEGER,
    TaskName TEXT,
    DueDate DATE
);

```

**Output:**
<img width="1256" height="423" alt="image" src="https://github.com/user-attachments/assets/085fc26a-b85c-4881-9aaa-7acbf404e5e4" />


**Question 9**
---
<img width="822" height="446" alt="image" src="https://github.com/user-attachments/assets/cf09cbeb-065c-42ee-a92b-7d68ee645283" />


```sql
INSERT INTO Student_details (RollNo, Name, Gender, Subject, MARKS)
SELECT RollNo, Name, Gender, Subject, MARKS
FROM Archived_students;
```

**Output:**
<img width="1251" height="319" alt="image" src="https://github.com/user-attachments/assets/37a9228c-d024-4dc0-80cb-48eb9b08357c" />


**Question 10**
---
<img width="1236" height="325" alt="image" src="https://github.com/user-attachments/assets/5f24d225-6648-41c1-a363-7779c3560de8" />


```sql
ALTER TABLE Student_details
ADD COLUMN email TEXT NOT NULL DEFAULT 'Invalid';

```

**Output:**
<img width="1261" height="292" alt="image" src="https://github.com/user-attachments/assets/f70c5eec-3a7e-4d0a-bf14-b4198dd7619c" />



## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
