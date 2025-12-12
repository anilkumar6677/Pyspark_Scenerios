# Pyspark_Scenerios


✅ Scenario-1: Find employees with duplicate salaries
🔹 Input
+----------+-----------+----------+--------+---------------------+---------+
| workerid | firstname | lastname | salary |     joiningdate     | depart  |
+----------+-----------+----------+--------+---------------------+---------+
|   001    | Monika    | Arora    |100000  |2014-02-20 09:00:00 | HR      |
|   002    | Niharika  | Verma    |300000  |2014-06-11 09:00:00 | Admin   |
|   003    | Vishal    | Singhal  |300000  |2014-02-20 09:00:00 | HR      |
|   004    | Amitabh   | Singh    |500000  |2014-02-20 09:00:00 | Admin   |
|   005    | Vivek     | Bhati    |500000  |2014-06-11 09:00:00 | Admin   |
+----------+-----------+----------+--------+---------------------+---------+

🔹 Output
+----------+-----------+----------+--------+---------------------+---------+
| workerid | firstname | lastname | salary |     joiningdate     | depart  |
+----------+-----------+----------+--------+---------------------+---------+
|   002    | Niharika  | Verma    |300000  |2014-06-11 09:00:00 | Admin   |
|   003    | Vishal    | Singhal  |300000  |2014-02-20 09:00:00 | HR      |
|   004    | Amitabh   | Singh    |500000  |2014-02-20 09:00:00 | Admin   |
|   005    | Vivek     | Bhati    |500000  |2014-06-11 09:00:00 | Admin   |
+----------+-----------+----------+--------+---------------------+---------+

✅ Scenario-2: Get highest salary employee in each department
🔹 Input
+--------+----------+---------+--------+---------+
| emp_id | name     | dept    | salary | city    |
+--------+----------+---------+--------+---------+
| 1      | Mohan    | IT      | 60000  | Pune    |
| 2      | Rohan    | HR      | 45000  | Delhi   |
| 3      | Sohan    | IT      | 75000  | Mumbai  |
| 4      | Karan    | HR      | 55000  | Delhi   |
| 5      | Varun    | Sales   | 30000  | Chennai |
+--------+----------+---------+--------+---------+

🔹 Output
+---------+----------+--------+
| dept    | name     | salary |
+---------+----------+--------+
| HR      | Karan    | 55000  |
| IT      | Sohan    | 75000  |
| Sales   | Varun    | 30000  |
+---------+----------+--------+
