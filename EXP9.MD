# <CENTER> EXPERIMENT 09

## Q1. Display the name of employee who earns highest salary.
```sql
SELECT ENAME
FROM EMPLOYEE
WHERE SAL = (SELECT MAX(SAL) FROM EMPLOYEE);
```

## Q2. Display the employee number and name of employee working as clerk and earning highest salary among clerks.
```sql
SELECT EMPNO, ENAME
FROM EMPLOYEE
WHERE JOB = 'CLERK'
AND SAL = (
SELECT MAX(SAL) FROM EMPLOYEE WHERE JOB = 'CLERK' );
```

## Q3. Display the names of the salesman who earns a salary more than the highest salary of any clerk.
```sql
SELECT ENAME
FROM EMPLOYEE
WHERE JOB = 'SALESMAN'
AND SAL > (
SELECT MAX(SAL)  FROM EMPLOYEE  WHERE JOB = 'CLERK' );
```

## Q4. Display the names of clerks who earn salary more than that of JAMES and salary less than that of SCOTT.
```sql
SELECT ENAME
FROM EMPLOYEE
WHERE JOB = 'CLERK'
AND SAL > (SELECT SAL FROM EMPLOYEE WHERE ENAME = 'JAMES')
AND SAL < (SELECT SAL FROM EMPLOYEE WHERE ENAME = 'SCOTT');
```

## Q5. Display the names of employees who earn a salary more than that of JAMES or salary greater than that of SCOTT.
```sql
SELECT ENAME
FROM EMPLOYEE
WHERE SAL > (SELECT SAL FROM EMPLOYEE WHERE ENAME = 'JAMES')
OR SAL > (SELECT SAL FROM EMPLOYEE WHERE ENAME = 'SCOTT');
```

## Q6. Display the names of the employees who earn highest salary in their respective departments.
```sql
SELECT ENAME
FROM EMPLOYEE E
WHERE SAL = ( SELECT MAX(SAL)  FROM EMPLOYEE  WHERE DEPTNO = E.DEPTNO );
```

## Q7. Display the names of employees who earn highest salaries in their respective job groups.
```sql
SELECT ENAME
FROM EMPLOYEE E
WHERE SAL = (SELECT MAX(SAL) FROM EMPLOYEE  WHERE JOB = E.JOB);
```

## Q8. Display the employee names who are working in accounting dept.
```sql
SELECT ENAME
FROM EMPLOYEE
WHERE DEPTNO = (
SELECT DEPTNO FROM DEPARTMENT  WHERE DNAME = 'ACCOUNTING' );
```

## Q9. Display the employee names who are working in MUMBAI.
```sql
SELECT ENAME
FROM EMPLOYEE
WHERE DEPTNO = (
SELECT DEPTNO FROM DEPARTMENT  WHERE LOCATION = 'MUMBAI' );
```

## Q10. Display the job groups having total salary greater than the maximum salary for managers.
```sql
SELECT JOB, SUM(SAL) AS TOTAL_SALARY
FROM EMPLOYEE
GROUP BY JOB
HAVING SUM(SAL) > (
SELECT MAX(SAL) FROM EMPLOYEE  WHERE JOB = 'MANAGER' );
```
