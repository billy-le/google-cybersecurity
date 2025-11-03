# Apply filters to SQL queries

### Project description

The project has two MariaDB tables, `log_in_attempts` and `employees`, which I will use SQl to query against. This project is to practice using SQL filters and operators like WHERE, LIKE, AND, etc. to get the data I need to work as a security analysts.

A snippet of the table of `log_in_attempts` is shown below:

| event_id | username | login_date | login_time | country | ip_address      | success |
| -------- | -------- | ---------- | ---------- | ------- | --------------- | ------- |
| 1        | jrafael  | 2022-05-09 | 04:56:27   | CAN     | 192.168.243.140 | 1       |
| 2        | apatel   | 2022-05-10 | 20:27:27   | CAN     | 192.168.205.12  | 0       |
| 3        | dkot     | 2022-05-09 | 06:47:41   | USA     | 192.168.151.162 | 1       |
| 4        | dkot     | 2022-05-08 | 02:00:39   | USA     | 192.168.178.71  | 0       |
| 5        | jrafael  | 2022-05-11 | 03:05:59   | CANADA  | 192.168.86.232  | 0       |
| 6        | arutley  | 2022-05-12 | 17:00:59   | MEXICO  | 192.168.3.24    | 0       |
| 7        | eraab    | 2022-05-11 | 01:45:14   | CAN     | 192.168.170.243 | 1       |

And a snippet of the table `employees` is shown below:
| employee_id | device_id | username | department | office |
|-------------|--------------|----------|------------------------|-------------|
| 1000 | a320b137c219 | elarson | Marketing | East-170 |
| 1001 | b239c825d303 | bmoreno | Marketing | Central-276 |
| 1002 | c116d593e558 | tshah | Human Resources | North-434 |
| 1003 | d394e816f943 | sgilmore | Finance | South-153 |
| 1004 | e218f877g788 | eraab | Human Resources | South-127 |
| 1005 | f551g340h864 | gesparza | Human Resources | South-366 |
| 1006 | g329h357i597 | alevitsk | Information Technology | East-320 |
| 1007 | h174i497j413 | wjaffrey | Finance | North-406 |
| 1008 | i858j583k571 | abernard | Finance | South-170 |
| 1009 | NULL | lrodriqu | Sales | South-134 |

### Retrieve after hours failed login attempts

The task was to perform a query to get all failed attempts after business hours. To complete this task, I will need to use the `>` greater than operator paired with the `AND` logical operator to perform a query after business hours and when `success` is FALSE.

```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00' AND success = FALSE;
```

### Retrieve login attempts on specific dates

This task was to perform a query to get login attempts on two specific dates. So in this query, we will use the `OR` query but we can also use the `BETWEEN` as well.

```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
```

```sql
SELECT *
FROM log_in_attempts
WHERE  login_date BETWEEN '2022-05-08' AND '2022-05-09';
```

### Retrieve login attempts outside of Mexico

The task was to perform a query for log in attempts originating from outside of Mexico.

```sql
SELECT * FROM log_in_attempts WHERE NOT country LIKE 'MEX%';
```

### Retrieve employees in Marketing

The task was to perform a query to get all employees from the Marketing department.

```sql
SELECT * FROM employees WHERE department = 'Marketing';
```

### Retrieve employees in Finance or Sales

The task was to perform an `OR` query to get employees from the Finance or Sales Department;

```sql
SELECT * FROM employees WHERE department = 'Finance' OR departmenting = 'Sales';
```

### Retrieve all employees not in IT

The task was to use the `NOT` operator to get all Departments not IT.

```sql
SELECT * FROM employees WHERE NOT department = 'Information Technology';
```

### Summary

As a security analyst, I will need to perform queries on a database. This exercise was to get familiar with working with SQL queries and filtering so I can extract the data that I needed.
