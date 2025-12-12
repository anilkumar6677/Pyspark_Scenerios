# Pyspark_Scenerios


✅ Scenario-1: Find employees with duplicate salaries

🔹 Input
```
+----------+-----------+----------+--------+---------------------+---------+
| workerid | firstname | lastname | salary |     joiningdate     | depart  |
+----------+-----------+----------+--------+---------------------+---------+
|   001    | Monika    | Arora    |100000  |2014-02-20 09:00:00 | HR      |
|   002    | Niharika  | Verma    |300000  |2014-06-11 09:00:00 | Admin   |
|   003    | Vishal    | Singhal  |300000  |2014-02-20 09:00:00 | HR      |
|   004    | Amitabh   | Singh    |500000  |2014-02-20 09:00:00 | Admin   |
|   005    | Vivek     | Bhati    |500000  |2014-06-11 09:00:00 | Admin   |
+----------+-----------+----------+--------+---------------------+---------+
```

🔹 Output

```
+----------+-----------+----------+--------+---------------------+---------+
| workerid | firstname | lastname | salary |     joiningdate     | depart  |
+----------+-----------+----------+--------+---------------------+---------+
|   002    | Niharika  | Verma    |300000  |2014-06-11 09:00:00 | Admin   |
|   003    | Vishal    | Singhal  |300000  |2014-02-20 09:00:00 | HR      |
|   004    | Amitabh   | Singh    |500000  |2014-02-20 09:00:00 | Admin   |
|   005    | Vivek     | Bhati    |500000  |2014-06-11 09:00:00 | Admin   |
+----------+-----------+----------+--------+---------------------+---------+

```

✅ Scenario-2: Get highest salary employee in each department


🔹 Input

```
+--------+----------+---------+--------+---------+
| emp_id | name     | dept    | salary | city    |
+--------+----------+---------+--------+---------+
| 1      | Mohan    | IT      | 60000  | Pune    |
| 2      | Rohan    | HR      | 45000  | Delhi   |
| 3      | Sohan    | IT      | 75000  | Mumbai  |
| 4      | Karan    | HR      | 55000  | Delhi   |
| 5      | Varun    | Sales   | 30000  | Chennai |
+--------+----------+---------+--------+---------+

```

🔹 Output

```
+---------+----------+--------+
| dept    | name     | salary |
+---------+----------+--------+
| HR      | Karan    | 55000  |
| IT      | Sohan    | 75000  |
| Sales   | Varun    | 30000  |
+---------+----------+--------+
```
✅ Scenario-3: Count employees city-wise


🔹 Input
```
+--------+---------+--------+
| emp_id | name    | city   |
+--------+---------+--------+
| 1      | Arun    | Pune   |
| 2      | Kiran   | Pune   |
| 3      | Mohit   | Delhi  |
| 4      | Ramu    | Delhi  |
| 5      | Ravi    | Pune   |
+--------+---------+--------+
```

🔹 Output
```
+--------+-------------+
| city   | emp_count   |
+--------+-------------+
| Pune   | 3           |
| Delhi  | 2           |
+--------+-------------+

```

✅ Scenario-4: Find second highest salary

🔹 Input

```
+--------+--------+
| emp_id | salary |
+--------+--------+
| 1      | 50000  |
| 2      | 75000  |
| 3      | 60000  |
| 4      | 75000  |
| 5      | 30000  |
+--------+--------+

```
🔹 Output

```
+--------------+
| second_high  |
+--------------+
| 60000        |
+--------------+


```
✅ Scenario-5: Find employees who joined after 2020

🔹 Input

```
+--------+----------+---------------------+
| emp_id | name     | joining_date        |
+--------+----------+---------------------+
| 1      | Varun    | 2019-03-10          |
| 2      | Mohan    | 2021-05-13          |
| 3      | Priya    | 2020-11-23          |
| 4      | Simran   | 2022-02-18          |
+--------+----------+---------------------+

```
🔹 Output

```
+--------+--------+---------------------+
| emp_id | name   | joining_date        |
+--------+--------+---------------------+
| 2      | Mohan  | 2021-05-13          |
| 4      | Simran | 2022-02-18          |
+--------+--------+---------------------+

```


Join Scenario 1 — inner Join Employees & Departments

Input: Employees
```
+------+--------+--------+
|emp_id|name    |dept_id |
+------+--------+--------+
|1     |Amit    |10      |
|2     |Riya    |20      |
|3     |Karan   |30      |
+------+--------+--------+
```
Input: Departments
```
+--------+-----------+
|dept_id |dept_name  |
+--------+-----------+
|10      |IT         |
|20      |HR         |
+--------+-----------+
```
Expected Output
```
+------+--------+--------+-----------+
|emp_id|name    |dept_id |dept_name  |
+------+--------+--------+-----------+
|1     |Amit    |10      |IT         |
|2     |Riya    |20      |HR         |
+------+--------+--------+-----------+
```


join Scenario 2 — Left Join to Find Employees Without Departments

Input: Employees
```
+------+--------+--------+
|emp_id|name    |dept_id |
+------+--------+--------+
|1     |Amit    |10      |
|2     |Riya    |20      |
|3     |Karan   |30      |
+------+--------+--------+
```
Input: Departments
```
+--------+-----------+
|dept_id |dept_name  |
+--------+-----------+
|10      |IT         |
|20      |HR         |
+--------+-----------+
```


Expected Output
```
+------+--------+--------+-----------+
|emp_id|name    |dept_id |dept_name  |
+------+--------+--------+-----------+
|1     |Amit    |10      |IT         |
|2     |Riya    |20      |HR         |
|3     |Karan   |30      |NULL       |
+------+--------+--------+-----------+
```
Join Scenario 3 — Right Join: List all Departments Even If No Employees


Input: Employees
```
+------+--------+--------+
|emp_id|name    |dept_id |
+------+--------+--------+
|1     |Amit    |10      |
|2     |Riya    |20      |
|3     |Karan   |30      |
+------+--------+--------+
```
Input: Departments
```
+--------+-----------+
|dept_id |dept_name  |
+--------+-----------+
|10      |IT         |
|20      |HR         |
|30      |Finance    |
+--------+-----------+
```
Output
```
+------+--------+--------+-----------+
|emp_id|name    |dept_id |dept_name  |
+------+--------+--------+-----------+
|1     |Amit    |10      |IT         |
|2     |Riya    |20      |HR         |
|NULL  |NULL    |30      |Finance    |
+------+--------+--------+-----------+
```
Join Scenario 4 — Full Outer Join
Input: Employees
```
+------+--------+--------+
|emp_id|name    |dept_id |
+------+--------+--------+
|1     |Amit    |10      |
|2     |Riya    |20      |
|3     |Karan   |30      |
+------+--------+--------+
```
Input: Departments
```
+--------+-----------+
|dept_id |dept_name  |
+--------+-----------+
|10      |IT         |
|20      |HR         |
+--------+-----------+
```

Output
```
+------+--------+--------+-----------+
|emp_id|name    |dept_id |dept_name  |
+------+--------+--------+-----------+
|1     |Amit    |10      |IT         |
|2     |Riya    |20      |HR         |
|3     |Karan   |30      |NULL       |
|NULL  |NULL    |40      |Support    |
+------+--------+--------+-----------+
```
Join Scenario 5 — Anti Join: Find Employees Without Department

Input: Employees
```
+------+--------+--------+
|emp_id|name    |dept_id |
+------+--------+--------+
|1     |Amit    |10      |
|2     |Riya    |20      |
|3     |Karan   |30      |
+------+--------+--------+
```
Input: Departments
```
+--------+-----------+
|dept_id |dept_name  |
+--------+-----------+
|10      |IT         |
|20      |HR         |
+--------+-----------+
```
Output

```
+------+--------+--------+
|emp_id|name    |dept_id |
+------+--------+--------+
|3     |Karan   |30      |
+------+--------+--------+
```


Window Functions — 5 Scenarios
Window Scenario 1 — Rank Employees by Salary

Input
```
+------+--------+--------+
|emp_id|name    |salary  |
+------+--------+--------+
|1     |Amit    |70000   |
|2     |Riya    |90000   |
|3     |Karan   |70000   |
+------+--------+--------+
```
Output
```
+------+--------+--------+------+
|emp_id|name    |salary  |rank  |
+------+--------+--------+------+
|2     |Riya    |90000   |1     |
|1     |Amit    |70000   |2     |
|3     |Karan   |70000   |2     |
+------+--------+--------+------+
```
Window Scenario 2 — Dense Rank by Salary

Input
```
+------+--------+--------+
|emp_id|name    |salary  |
+------+--------+--------+
|1     |Amit    |70000   |
|2     |Riya    |90000   |
|3     |Karan   |70000   |
+------+--------+--------+
```
Output
```

+------+--------+--------+-----------+
|name  |salary  |dense_rank          |
+------+--------+--------+-----------+
|Riya  |90000   |1                  |
|Amit  |70000   |2                  |
|Karan |70000   |2                  |
+------+--------+--------+-----------+
```
Window Scenario 3 — Row Number per Department

Input
```
+------+--------+--------+
|emp_id|name    |salary  |
+------+--------+--------+
|1     |Amit    |70000   |
|2     |Riya    |90000   |
|3     |Karan   |70000   |
+------+--------+--------+
```
Output
```
+------+--------+--------+-----------+
|name  |dept    |salary  |row_number |
+------+--------+--------+-----------+
|Amit  |IT      |70000   |1          |
|Karan |IT      |65000   |2          |
|Riya  |HR      |90000   |1          |
+------+--------+--------+-----------+
```
Window Scenario 4 — Running Total (Cumulative Sum)
Input
```
+------+--------+--------+
|emp_id|name    |salary  |
+------+--------+--------+
|1     |Amit    |70000   |
|2     |Riya    |90000   |
|3     |Karan   |70000   |
+------+--------+--------+
```
Output
```
+--------+-------+--------------+
|month   |sales  |running_total |
+--------+-------+--------------+
|Jan     |1000   |1000          |
|Feb     |2000   |3000          |
|Mar     |3000   |6000          |
+--------+-------+--------------+
```

Window Scenario 5 — Lag: Compare Salary with Previous Month
Input
```
+------+--------+--------+
|emp_id|name    |salary  |
+------+--------+--------+
|1     |Amit    |70000   |
|2     |Riya    |90000   |
|3     |Karan   |70000   |
+------+--------+--------+
```

```
+--------+--------+--------+
|month   |sales   |prev    |
+--------+--------+--------+
|Jan     |1000    |NULL    |
|Feb     |2000    |1000    |
|Mar     |3000    |2000    |
+--------+--------+--------+

```


Complex Scenario  — Explode Array Column

Input
```
+--------+---------------+
|name    |skills         |
+--------+---------------+
|Amit    |[Java, Scala]  |
|Riya    |[Python]       |
+--------+---------------+
```
Output
```
+--------+--------+
|name    |skill   |
+--------+--------+
|Amit    |Java    |
|Amit    |Scala   |
|Riya    |Python  |
+--------+--------+
```

Complex Scenario  — JSON Parse Column

Input
```
+----------+--------------------------+
|emp_id    |info                      |
+----------+--------------------------+
|1         |{"age":30,"city":"Pune"}  |
+----------+--------------------------+
```
Output
```
+----------+-----+-------+
|emp_id    |age  |city   |
+----------+-----+-------+
|1         |30   |Pune   |
+----------+-----+-------+

```


Complex Scenario — Grouped Collect List

Input
```
+--------+--------+
|dept    |name    |
+--------+--------+
|IT      |Amit    |
|IT      |Karan   |
|HR      |Riya    |
+--------+--------+
```
Output
```
+--------+------------------+
|dept    |employees         |
+--------+------------------+
|IT      |[Amit, Karan]     |
|HR      |[Riya]            |
+--------+------------------+

```
