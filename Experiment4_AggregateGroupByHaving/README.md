# Experiment 4: Aggregate Functions, Group By and Having Clause
~~~
NAME: HARI NIVEDHAN P
REG NO: 212224220031
~~~

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
<img width="822" height="373" alt="image" src="https://github.com/user-attachments/assets/e6a8bb5f-d594-48d7-a5f8-d71390fedfff" />


```sql
select name,max(income)
from employee
where city = 'California';
```

**Output:**

<img width="623" height="245" alt="image" src="https://github.com/user-attachments/assets/36bd9e2a-0a9e-4eee-b130-6839d90c00aa" />



**Question 2**
---
<img width="687" height="397" alt="image" src="https://github.com/user-attachments/assets/ccf73caf-20f4-482f-99d0-67871057a35e" />



```sql
SELECT COUNT(DISTINCT customer_id)
AS COUNT
FROM customer
WHERE grade IS NOT NULL;
```

**Output:**

<img width="418" height="242" alt="image" src="https://github.com/user-attachments/assets/738c08f2-b4ea-4a2e-a9b8-71ef2567b3f5" />



**Question 3**
---
<img width="865" height="395" alt="image" src="https://github.com/user-attachments/assets/f736e2bc-10b9-4577-952e-1dd739a65db2" />



```sql
SELECT MAX(age) - MIN(age) AS
age_difference
from employee

```

**Output:**

<img width="460" height="223" alt="image" src="https://github.com/user-attachments/assets/2e339448-f65f-4782-a479-1ca7c26caa2f" />


**Question 4**
---
<img width="660" height="467" alt="image" src="https://github.com/user-attachments/assets/26f8fa8e-bc38-47b6-a220-88b85f48ccea" />



```sql
select patientID, count(*) as TotalAppointments
from Appointments
group by PatientID;

```

**Output:**


<img width="650" height="487" alt="image" src="https://github.com/user-attachments/assets/aa389368-950e-46d4-90a9-0d4fcc146de1" />


**Question 5**
---

<img width="561" height="507" alt="image" src="https://github.com/user-attachments/assets/4f7cd516-1849-432c-8cf3-c6579a6e9f64" />



```sql
select InsuranceCompany , count(*) as TotalPatients
from Insurance
group by InsuranceCompany;
```

**Output:**


<img width="678" height="533" alt="image" src="https://github.com/user-attachments/assets/5b1b06bd-d800-408c-8b9c-9813117452a1" />


**Question 6**
---

<img width="860" height="363" alt="image" src="https://github.com/user-attachments/assets/3e6f6d46-8fb0-4da3-9461-e5cece675549" />



```sql
select Gender , count(*) as TotalPatients
from Patients
group by Gender;
```

**Output:**


<img width="571" height="272" alt="image" src="https://github.com/user-attachments/assets/cd466798-0e15-4781-bcb2-10f237c600a2" />


**Question 7**
---

<img width="1286" height="372" alt="image" src="https://github.com/user-attachments/assets/b09b40b9-9171-4a61-9487-9ab3f93fefae" />



```sql
select (age/5)*5 as age_group,
SUM(salary)
from customer1
group by (age/5)*5
having SUM(salary) >5000;
```

**Output:**

<img width="549" height="278" alt="image" src="https://github.com/user-attachments/assets/cffab107-048c-4235-9ed1-15d0f50bcabe" />


**Question 8**
---

<img width="957" height="376" alt="image" src="https://github.com/user-attachments/assets/6122eaec-9ddc-4cc2-8009-564e4cdc71c5" />



```sql
select address,
AVG(salary)
from customer1
group by address
having AVG(salary) > 5000;
```

**Output:**


<img width="482" height="326" alt="image" src="https://github.com/user-attachments/assets/9e0d6df2-bef7-4a7e-800b-4e2db28be1f8" />


**Question 9**
---

<img width="816" height="457" alt="image" src="https://github.com/user-attachments/assets/d85e8207-2a36-4594-b9b3-2ff2e7b377e8" />



```sql
select address, AVG(salary)
from customer1
group by address
having AVG(salary) < 15000;
```

**Output:**


<img width="512" height="463" alt="image" src="https://github.com/user-attachments/assets/d77c2b5d-36bc-4d12-82c3-91ecd87eaf84" />


**Question 10**
---

<img width="1256" height="361" alt="image" src="https://github.com/user-attachments/assets/bb71b72f-d11d-48f0-b68c-7d3f1d7e7b3e" />


```sql
select (age/5)*5 as age_group,
MIN(age)
from customer1
group by (age/5)*5
having MIN(age) < 25;
```

**Output:**


<img width="477" height="230" alt="image" src="https://github.com/user-attachments/assets/e39ea231-3ccb-4a6b-8eba-1deecd8afcc3" />



## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
