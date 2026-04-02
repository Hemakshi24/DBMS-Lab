Microsoft Windows [Version 10.0.26200.7840]
(c) Microsoft Corporation. All rights reserved.

C:\Users\user>cd ../../

C:\>cd xampp/mysql/bin

C:\xampp\mysql\bin>mysql -uroot
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 8
Server version: 10.4.32-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> use hemakshi_30116_2cse14
Database changed
MariaDB [hemakshi_30116_2cse14]> SELECT ENAME FROM EMPLOYEE;
+--------+
| ENAME  |
+--------+
| SMITH  |
| ALLEN  |
| WARD   |
| JONES  |
| MARTIN |
| BLAKE  |
| CLARK  |
| SCOTT  |
| KING   |
| TURNER |
| ADAMS  |
| JAMES  |
| FORD   |
| MILLER |
+--------+
14 rows in set (0.014 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT DNAME FROM EMPLOYEE;
ERROR 1054 (42S22): Unknown column 'DNAME' in 'field list'
MariaDB [hemakshi_30116_2cse14]> SELECT DNAME FROM DEPARTMENT;
+------------+
| DNAME      |
+------------+
| RESEARCH   |
| ACCOUNTING |
| SALES      |
| OPERATIONS |
+------------+
4 rows in set (0.019 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT D.ENAME, E.DNAME FROM EMPLOYEE JOIN DEPARTMENT;
ERROR 1054 (42S22): Unknown column 'D.ENAME' in 'field list'
MariaDB [hemakshi_30116_2cse14]> SELECT*FROM EMPLOYEE;
+--------+--------+-----------+------+------------+------+------+--------+
| EMP_NO | ENAME  | JOB       | MGR  | HIREDATE   | SAL  | COMM | DEPTNO |
+--------+--------+-----------+------+------------+------+------+--------+
|   7369 | SMITH  | CLERK     | 7902 | 1980-12-17 |  880 | NULL |     20 |
|   7499 | ALLEN  | SALESMAN  | 7698 | 1981-02-20 | 1600 |  300 |     30 |
|   7521 | WARD   | SALESMAN  | 7698 | 1981-02-22 | 1250 |  300 |     30 |
|   7566 | JONES  | MANAGER   | 7839 | 1981-04-02 | 3273 | NULL |     20 |
|   7654 | MARTIN | SALESMAN  | 7698 | 1981-09-28 | 1250 | 1400 |     30 |
|   7698 | BLAKE  | MANAGER   | 7839 | 1981-05-01 | 3135 | NULL |     30 |
|   7782 | CLARK  | MANAGER   | 7839 | 1981-06-09 | 2695 | NULL |     20 |
|   7788 | SCOTT  | ANALYST   | 7566 | 1982-12-09 | 3300 | NULL |     40 |
|   7839 | KING   | PRESIDENT | NULL | 1981-11-17 | 5500 | NULL |     20 |
|   7844 | TURNER | SALESMAN  | 7698 | 1981-09-08 | 1500 |    0 |     30 |
|   7876 | ADAMS  | CLERK     | 7788 | 1983-01-12 | 1210 | NULL |     20 |
|   7900 | JAMES  | CLERK     | 7698 | 1981-12-03 | 1045 | NULL |     30 |
|   7902 | FORD   | ANALYST   | 7566 | 1981-12-03 | 3300 | NULL |     20 |
|   7934 | MILLER | CLERK     | 7782 | 1982-01-23 | 1430 | NULL |     10 |
+--------+--------+-----------+------+------------+------+------+--------+
14 rows in set (0.000 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT*FROM DEPARTMENT;
+--------+------------+
| DEPTNO | DNAME      |
+--------+------------+
|     10 | RESEARCH   |
|     20 | ACCOUNTING |
|     30 | SALES      |
|     40 | OPERATIONS |
+--------+------------+
4 rows in set (0.000 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT E.ENAME, D.DNAME FROM EMPLOYEE E INNER JOIN DEPARTMENT D ON E.DEPT_NO = D.DEPT_NO;
ERROR 1054 (42S22): Unknown column 'E.DEPT_NO' in 'on clause'
MariaDB [hemakshi_30116_2cse14]> SELECT E.ENAME, D.DNAME FROM EMPLOYEE E INNER JOIN DEPARTMENT D ON E.DEPTNO = D.DEPTNO;
+--------+------------+
| ENAME  | DNAME      |
+--------+------------+
| SMITH  | ACCOUNTING |
| ALLEN  | SALES      |
| WARD   | SALES      |
| JONES  | ACCOUNTING |
| MARTIN | SALES      |
| BLAKE  | SALES      |
| CLARK  | ACCOUNTING |
| SCOTT  | OPERATIONS |
| KING   | ACCOUNTING |
| TURNER | SALES      |
| ADAMS  | ACCOUNTING |
| JAMES  | SALES      |
| FORD   | ACCOUNTING |
| MILLER | RESEARCH   |
+--------+------------+
14 rows in set (0.001 sec)

MariaDB [hemakshi_30116_2cse14]>

Microsoft Windows [Version 10.0.26200.8039]
(c) Microsoft Corporation. All rights reserved.

C:\Users\user>cd ../../

C:\>cd xampp/mysql/bin

C:\xampp\mysql\bin>mysql -uroot
Welcome to the MariaDB monitor.  Commands end with ; or \g.
Your MariaDB connection id is 8
Server version: 10.4.32-MariaDB mariadb.org binary distribution

Copyright (c) 2000, 2018, Oracle, MariaDB Corporation Ab and others.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

MariaDB [(none)]> use hemakshi_30116_2cse14
Database changed
MariaDB [hemakshi_30116_2cse14]> SELECT e.ENAME, d.DNAME FROM Employee e JOIN Department d ON e.DEPTNO = d.DEPTNO;
+--------+------------+
| ENAME  | DNAME      |
+--------+------------+
| SMITH  | ACCOUNTING |
| ALLEN  | SALES      |
| WARD   | SALES      |
| JONES  | ACCOUNTING |
| MARTIN | SALES      |
| BLAKE  | SALES      |
| CLARK  | ACCOUNTING |
| SCOTT  | OPERATIONS |
| KING   | ACCOUNTING |
| TURNER | SALES      |
| ADAMS  | ACCOUNTING |
| JAMES  | SALES      |
| FORD   | ACCOUNTING |
| MILLER | RESEARCH   |
+--------+------------+
14 rows in set (0.034 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT e.ENAME AS employee, m.ENAME AS manager FROM Employee e JOIN Employee m ON e.MGR = m.EMP_NO WHERE m.ENAME = 'JONES';
+----------+---------+
| employee | manager |
+----------+---------+
| SCOTT    | JONES   |
| FORD     | JONES   |
+----------+---------+
2 rows in set (0.003 sec)

MariaDB [hemakshi_30116_2cse14]> CREATE TABLE SALGRADE (
    -> GRADE INT,
    -> LOSAL INT,
    -> HISAL INT
    -> );
Query OK, 0 rows affected (0.011 sec)

MariaDB [hemakshi_30116_2cse14]> INSERT INTO SALGRADE VALUES
    -> (1,700, 1200),
    -> (2, 1201, 1400),
    -> (3, 1401, 2000),
    -> (4, 2001, 3000),
    -> (5, 3001, 9999);
Query OK, 5 rows affected (0.008 sec)
Records: 5  Duplicates: 0  Warnings: 0

MariaDB [hemakshi_30116_2cse14]> SELECT e.ENAME,e.JOB, d.DNAME AS Manager, s.grade FROM Employee e JOIN DEPARTMENT d ON e.DEPTNO = d.DEPTNO LEFT JOIN Employee m ON e.MGR = m.EMPNO JOIN SALGRADE s ON e.SAL BETWEEN s.LOSAL AND s.HISAL ORDER BY d.DNAME;
ERROR 1054 (42S22): Unknown column 'm.EMPNO' in 'on clause'
MariaDB [hemakshi_30116_2cse14]> SELECT * FROM SALGRADE;
+-------+-------+-------+
| GRADE | LOSAL | HISAL |
+-------+-------+-------+
|     1 |   700 |  1200 |
|     2 |  1201 |  1400 |
|     3 |  1401 |  2000 |
|     4 |  2001 |  3000 |
|     5 |  3001 |  9999 |
+-------+-------+-------+
5 rows in set (0.001 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT E.ENAME, E.JOB, D.DNAME, M.ENAME AS MANAGER, S.GRADE FROM Employee E JOIN DEPARTMENT D ON E.DEPTNO = D.DEPTNO LEFT JOIN Employee M ON E.MGR = M.EMP_NO JOIN SALGRADE S ON E.SAL BETWEEN S.LOSAL AND S.HISAL ORDER BY D.DNAME;
+--------+-----------+------------+---------+-------+
| ENAME  | JOB       | DNAME      | MANAGER | GRADE |
+--------+-----------+------------+---------+-------+
| SMITH  | CLERK     | ACCOUNTING | FORD    |     1 |
| ADAMS  | CLERK     | ACCOUNTING | SCOTT   |     2 |
| KING   | PRESIDENT | ACCOUNTING | NULL    |     5 |
| JONES  | MANAGER   | ACCOUNTING | KING    |     5 |
| FORD   | ANALYST   | ACCOUNTING | JONES   |     5 |
| CLARK  | MANAGER   | ACCOUNTING | KING    |     4 |
| SCOTT  | ANALYST   | OPERATIONS | JONES   |     5 |
| MILLER | CLERK     | RESEARCH   | CLARK   |     3 |
| WARD   | SALESMAN  | SALES      | BLAKE   |     2 |
| MARTIN | SALESMAN  | SALES      | BLAKE   |     2 |
| TURNER | SALESMAN  | SALES      | BLAKE   |     3 |
| BLAKE  | MANAGER   | SALES      | KING    |     5 |
| JAMES  | CLERK     | SALES      | BLAKE   |     1 |
| ALLEN  | SALESMAN  | SALES      | BLAKE   |     3 |
+--------+-----------+------------+---------+-------+
14 rows in set (0.002 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT E.ENAME, E.JOB, E.SAL, S.GRADE, D.DNAME FROM EMPLOYEE E JOIN DEPARTMENT D ON E.DEPTNO = D.DEPTNO JOIN SALGRADE S ON E.SAL BETWEEN S.LOSAL AND S.HISAL WHERE E.JOB <> 'CLERK' ORDER BY E.SAL DESC;
+--------+-----------+------+-------+------------+
| ENAME  | JOB       | SAL  | GRADE | DNAME      |
+--------+-----------+------+-------+------------+
| KING   | PRESIDENT | 5500 |     5 | ACCOUNTING |
| FORD   | ANALYST   | 3300 |     5 | ACCOUNTING |
| SCOTT  | ANALYST   | 3300 |     5 | OPERATIONS |
| JONES  | MANAGER   | 3273 |     5 | ACCOUNTING |
| BLAKE  | MANAGER   | 3135 |     5 | SALES      |
| CLARK  | MANAGER   | 2695 |     4 | ACCOUNTING |
| ALLEN  | SALESMAN  | 1600 |     3 | SALES      |
| TURNER | SALESMAN  | 1500 |     3 | SALES      |
| MARTIN | SALESMAN  | 1250 |     2 | SALES      |
| WARD   | SALESMAN  | 1250 |     2 | SALES      |
+--------+-----------+------+-------+------------+
10 rows in set (0.001 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT E.ENAME AS EMPLOYEE, E.JOB, IFNULL(M.ENAME, 'NO MANAGER') AS MANAGER FROM EMPLOYEE E LEFT JOIN EMPLOYEE M ON E.MGR = M.EMP_NO;
+----------+-----------+------------+
| EMPLOYEE | JOB       | MANAGER    |
+----------+-----------+------------+
| SCOTT    | ANALYST   | JONES      |
| FORD     | ANALYST   | JONES      |
| ALLEN    | SALESMAN  | BLAKE      |
| WARD     | SALESMAN  | BLAKE      |
| MARTIN   | SALESMAN  | BLAKE      |
| TURNER   | SALESMAN  | BLAKE      |
| JAMES    | CLERK     | BLAKE      |
| MILLER   | CLERK     | CLARK      |
| ADAMS    | CLERK     | SCOTT      |
| JONES    | MANAGER   | KING       |
| BLAKE    | MANAGER   | KING       |
| CLARK    | MANAGER   | KING       |
| SMITH    | CLERK     | FORD       |
| KING     | PRESIDENT | NO MANAGER |
+----------+-----------+------------+
14 rows in set (0.001 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT E.ENAME, E.JOB, (E.SAL*12) AS ANNUAL_SAL, E.DEPTNO, D.DNAME, S.GRADE FROM EMPLOYEE E JOIN DEPARTMENT D ON E.DEPTNO = D.DEPTNO JOIN SALGRADE S ON E.SAL BETWEEN S.LOSAL AND S.HISAL WHERE (E.SAL*12 = 36000) OR (E.JOB <> 'CLERK');
+--------+-----------+------------+--------+------------+-------+
| ENAME  | JOB       | ANNUAL_SAL | DEPTNO | DNAME      | GRADE |
+--------+-----------+------------+--------+------------+-------+
| ALLEN  | SALESMAN  |      19200 |     30 | SALES      |     3 |
| WARD   | SALESMAN  |      15000 |     30 | SALES      |     2 |
| JONES  | MANAGER   |      39276 |     20 | ACCOUNTING |     5 |
| MARTIN | SALESMAN  |      15000 |     30 | SALES      |     2 |
| BLAKE  | MANAGER   |      37620 |     30 | SALES      |     5 |
| CLARK  | MANAGER   |      32340 |     20 | ACCOUNTING |     4 |
| SCOTT  | ANALYST   |      39600 |     40 | OPERATIONS |     5 |
| KING   | PRESIDENT |      66000 |     20 | ACCOUNTING |     5 |
| TURNER | SALESMAN  |      18000 |     30 | SALES      |     3 |
| FORD   | ANALYST   |      39600 |     20 | ACCOUNTING |     5 |
+--------+-----------+------------+--------+------------+-------+
10 rows in set (0.001 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT E.ENAME, E.JOB, (E.SAL*12) AS ANNUAL_SAL, E.DEPTNO, D.DNAME, S.GRADE FROM EMPLOYEE E JOIN DEPARTMENT D ON E.DEPTNO = D.DEPTNO JOIN SALGRADE S ON E.SAL BETWEEN S.LOSAL AND S.HISAL WHERE (E.SAL*12 = 30000) AND (E.JOB <> 'CLERK');
Empty set (0.001 sec)

MariaDB [hemakshi_30116_2cse14]>  SELECT E.EMP_NO, E.ENAME, IFNULL(M.EMP_NO, 'NO MANAGER') AS MANAGER_NO, IFNULL(M.ENAME, 'NO MANAGER') AS MANAGER_NAME FROM EMPLOYEE E LEFT JOIN EMPLOYEE M ON E.MGR = M.EMP_NO;
+--------+--------+------------+--------------+
| EMP_NO | ENAME  | MANAGER_NO | MANAGER_NAME |
+--------+--------+------------+--------------+
|   7788 | SCOTT  | 7566       | JONES        |
|   7902 | FORD   | 7566       | JONES        |
|   7499 | ALLEN  | 7698       | BLAKE        |
|   7521 | WARD   | 7698       | BLAKE        |
|   7654 | MARTIN | 7698       | BLAKE        |
|   7844 | TURNER | 7698       | BLAKE        |
|   7900 | JAMES  | 7698       | BLAKE        |
|   7934 | MILLER | 7782       | CLARK        |
|   7876 | ADAMS  | 7788       | SCOTT        |
|   7566 | JONES  | 7839       | KING         |
|   7698 | BLAKE  | 7839       | KING         |
|   7782 | CLARK  | 7839       | KING         |
|   7369 | SMITH  | 7902       | FORD         |
|   7839 | KING   | NO MANAGER | NO MANAGER   |
+--------+--------+------------+--------------+
14 rows in set (0.002 sec)

MariaDB [hemakshi_30116_2cse14]> SELECT D.DNAME, D.DEPTNO, SUM(E.SAL) AS TOTAL_SAL FROM EMPLOYEE E JOIN DEPARTMENT D ON E.DEPTNO = D.DEPTNO GROUP BY D.DNAME, D.DEPTNO;
+------------+--------+-----------+
| DNAME      | DEPTNO | TOTAL_SAL |
+------------+--------+-----------+
| ACCOUNTING |     20 |     16858 |
| OPERATIONS |     40 |      3300 |
| RESEARCH   |     10 |      1430 |
| SALES      |     30 |      9780 |
+------------+--------+-----------+
4 rows in set (0.002 sec)

MariaDB [hemakshi_30116_2cse14]> MariaDB [hemakshi_30116_2cse14]> SELECT E.ENAME, D.DNAME FROM EMPLOYEE E JOIN DEPARTMENT D ON E.DEPTNO = D.DEPTNO;
+--------+------------+
| ENAME  | DNAME      |
+--------+------------+
| SMITH  | ACCOUNTING |
| ALLEN  | SALES      |
| WARD   | SALES      |
| JONES  | ACCOUNTING |
| MARTIN | SALES      |
| BLAKE  | SALES      |
| CLARK  | ACCOUNTING |
| SCOTT  | OPERATIONS |
| KING   | ACCOUNTING |
| TURNER | SALES      |
| ADAMS  | ACCOUNTING |
| JAMES  | SALES      |
| FORD   | ACCOUNTING |
| MILLER | RESEARCH   |
+--------+------------+
14 rows in set (0.002 sec)

MariaDB [hemakshi_30116_2cse14]>
