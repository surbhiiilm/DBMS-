# Experiment 1

## DEPARTMENT TABLE

```
+--------+------------+
| DEPTNO | DNAME      |
+--------+------------+
|     10 | ACCOUNTING |
|     20 | RESEARCH   |
|     30 | SALES      |
|     40 | OPERATIONS |
+--------+------------+
```

## EMPLOYEE TABLE
```
+-------+--------+-----------+------+------------+------+------+--------+
| EMPNO | ENAME  | JOB       | MGR  | HIREDATE   | SAL  | COMM | DEPTNO |
+-------+--------+-----------+------+------------+------+------+--------+
|  7369 | SMITH  | CLERK     | 7902 | 1980-12-17 |  800 | NULL |     20 |
|  7499 | ALLEN  | SALESMAN  | 7698 | 1981-02-20 | 1600 |  300 |     30 |
|  7521 | WARD   | SALESMAN  | 7698 | 1981-02-22 | 1250 |  300 |     30 |
|  7566 | JONES  | MANAGER   | 7839 | 1981-04-02 | 2975 | NULL |     20 |
|  7654 | MARTIN | SALESMAN  | 7698 | 1981-09-28 | 1250 | 1400 |     30 |
|  7698 | BLAKE  | MANAGER   | 7839 | 1981-05-01 | 2850 | NULL |     30 |
|  7782 | CLARK  | MANAGER   | 7839 | 1981-06-09 | 2450 | NULL |     20 |
|  7788 | SCOTT  | ANALYST   | 7566 | 1982-12-09 | 3000 | NULL |     40 |
|  7839 | KING   | PRESIDENT | NULL | 1981-11-17 | 5000 | NULL |     20 |
|  7844 | TURNER | SALESMAN  | 7698 | 1981-09-08 | 1500 |    0 |     30 |
|  7876 | ADAMS  | CLERK     | 7788 | 1983-01-12 | 1100 | NULL |     20 |
|  7900 | JAMES  | CLERK     | 7698 | 1981-12-03 | 3000 | NULL |     30 |
|  7902 | FORD   | ANALYST   | 7566 | 1981-12-03 | 3000 | NULL |     20 |
|  7934 | MILLER | CLERK     | 7782 | 1982-01-23 | 1300 | NULL |     10 |
+-------+--------+-----------+------+------------+------+------+--------+
```
## 1. Create Employee_master table with data using Employee table.
```
+-------+--------+-----------+------+------------+------+------+--------+
| EMPNO | ENAME  | JOB       | MGR  | HIREDATE   | SAL  | COMM | DEPTNO |
+-------+--------+-----------+------+------------+------+------+--------+
|  7369 | SMITH  | CLERK     | 7902 | 1980-12-17 |  968 | NULL |     20 |
|  7499 | ALLEN  | SALESMAN  | 7698 | 1981-02-20 | 1600 |  300 |     30 |
|  7521 | WARD   | SALESMAN  | 7698 | 1981-02-22 | 1250 |  300 |     30 |
|  7566 | JONES  | MANAGER   | 7839 | 1981-04-02 | 3600 | NULL |     20 |
|  7654 | MARTIN | SALESMAN  | 7698 | 1981-09-28 | 1250 | 1400 |     30 |
|  7698 | BLAKE  | MANAGER   | 7839 | 1981-05-01 | 2850 | NULL |     30 |
|  7782 | CLARK  | MANAGER   | 7839 | 1981-06-09 | 2965 | NULL |     20 |
|  7788 | SCOTT  | ANALYST   | 7566 | 1982-12-09 | 3000 | NULL |     40 |
|  7839 | KING   | PRESIDENT | NULL | 1981-11-17 | 6050 | NULL |     20 |
|  7844 | TURNER | SALESMAN  | 7698 | 1981-09-08 | 1500 |    0 |     30 |
|  7876 | ADAMS  | CLERK     | 7788 | 1983-01-12 | 1331 | NULL |     20 |
|  7900 | JAMES  | CLERK     | 7698 | 1981-12-03 | 3630 | NULL |     30 |
|  7902 | FORD   | ANALYST   | 7566 | 1981-12-03 | 3630 | NULL |     20 |
|  7934 | MILLER | CLERK     | 7782 | 1982-01-23 | 1300 | NULL |     10 |
+-------+--------+-----------+------+------------+------+------+--------+
```

## 2. Delete all record into Employee_master whose DeptNo is 10
```
+-------+--------+-----------+------+------------+------+------+--------+
| EMPNO | ENAME  | JOB       | MGR  | HIREDATE   | SAL  | COMM | DEPTNO |
+-------+--------+-----------+------+------------+------+------+--------+
|  7369 | SMITH  | CLERK     | 7902 | 1980-12-17 | 1065 | NULL |     20 |
|  7499 | ALLEN  | SALESMAN  | 7698 | 1981-02-20 | 1600 |  300 |     30 |
|  7521 | WARD   | SALESMAN  | 7698 | 1981-02-22 | 1250 |  300 |     30 |
|  7566 | JONES  | MANAGER   | 7839 | 1981-04-02 | 3960 | NULL |     20 |
|  7654 | MARTIN | SALESMAN  | 7698 | 1981-09-28 | 1250 | 1400 |     30 |
|  7698 | BLAKE  | MANAGER   | 7839 | 1981-05-01 | 2850 | NULL |     30 |
|  7782 | CLARK  | MANAGER   | 7839 | 1981-06-09 | 3262 | NULL |     20 |
|  7788 | SCOTT  | ANALYST   | 7566 | 1982-12-09 | 3000 | NULL |     40 |
|  7839 | KING   | PRESIDENT | NULL | 1981-11-17 | 6655 | NULL |     20 |
|  7844 | TURNER | SALESMAN  | 7698 | 1981-09-08 | 1500 |    0 |     30 |
|  7876 | ADAMS  | CLERK     | 7788 | 1983-01-12 | 1464 | NULL |     20 |
|  7900 | JAMES  | CLERK     | 7698 | 1981-12-03 | 3630 | NULL |     30 |
|  7902 | FORD   | ANALYST   | 7566 | 1981-12-03 | 3993 | NULL |     20 |
+-------+--------+-----------+------+------------+------+------+--------+
```
## 3. Update 10% in his salary of DEPTNO 20 into Employee_Master.
```
+-------+--------+-----------+------+------------+------+------+--------+
| EMPNO | ENAME  | JOB       | MGR  | HIREDATE   | SAL  | COMM | DEPTNO |
+-------+--------+-----------+------+------------+------+------+--------+
|  7369 | SMITH  | CLERK     | 7902 | 1980-12-17 | 1065 | NULL |     20 |
|  7499 | ALLEN  | SALESMAN  | 7698 | 1981-02-20 | 1600 |  300 |     30 |
|  7521 | WARD   | SALESMAN  | 7698 | 1981-02-22 | 1250 |  300 |     30 |
|  7566 | JONES  | MANAGER   | 7839 | 1981-04-02 | 3960 | NULL |     20 |
|  7654 | MARTIN | SALESMAN  | 7698 | 1981-09-28 | 1250 | 1400 |     30 |
|  7698 | BLAKE  | MANAGER   | 7839 | 1981-05-01 | 2850 | NULL |     30 |
|  7782 | CLARK  | MANAGER   | 7839 | 1981-06-09 | 3262 | NULL |     20 |
|  7788 | SCOTT  | ANALYST   | 7566 | 1982-12-09 | 3000 | NULL |     40 |
|  7839 | KING   | PRESIDENT | NULL | 1981-11-17 | 6655 | NULL |     20 |
|  7844 | TURNER | SALESMAN  | 7698 | 1981-09-08 | 1500 |    0 |     30 |
|  7876 | ADAMS  | CLERK     | 7788 | 1983-01-12 | 1464 | NULL |     20 |
|  7900 | JAMES  | CLERK     | 7698 | 1981-12-03 | 3630 | NULL |     30 |
|  7902 | FORD   | ANALYST   | 7566 | 1981-12-03 | 3993 | NULL |     20 |
+-------+--------+-----------+------+------------+------+------+--------+
```

## 4. Alter SAL with size 10,2 in Employee_Master.
```
+----------+---------------+------+-----+---------+-------+
| Field    | Type          | Null | Key | Default | Extra |
+----------+---------------+------+-----+---------+-------+
| EMPNO    | int(11)       | NO   |     | NULL    |       |
| ENAME    | varchar(20)   | YES  |     | NULL    |       |
| JOB      | varchar(20)   | YES  |     | NULL    |       |
| MGR      | int(11)       | YES  |     | NULL    |       |
| HIREDATE | date          | YES  |     | NULL    |       |
| SAL      | decimal(10,2) | YES  |     | NULL    |       |
| COMM     | int(11)       | YES  |     | NULL    |       |
| DEPTNO   | int(11)       | YES  |     | NULL    |       |
+----------+---------------+------+-----+---------+-------+
```
## 5. Drop Employee master Table.
```
+----------------+
| Tables_in_iilm |
+----------------+
| department     |
| employee       |
+----------------+
```




