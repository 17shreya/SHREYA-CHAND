# SHREYA-CHAND

CREATE DATABASE ORG;
USE ORG;

CREATE TABLE Worker (
		WORKER_ID INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
        FIRST_NAME CHAR(25),
        LAST_NAME CHAR(25),
        SALARY INT(15),
        JOINING_DATE datetime,
        DEPARTMENT CHAR(25)
);
INSERT INTO Worker (WORKER_ID, FIRST_NAME, LAST_NAME, SALARY, JOINING_DATE, DEPARTMENT) VALUES
(001,'MONIKA','ARORA',100000,'14-02-20 09.00.00','HR'),
(002,'NIHARIKA','VERMA',80000,'14-06-11 09.00.00','ADMIN'),
(003,'VISHAL ','SINGHAL',300000,'14-02-20 09.00.00','HR'),
(004,'AMITABH','SINGH',500000,'14-02-20 09.00.00','ADMIN'),
(005,'VIVEK','BHATI',500000,'14-02-11 09.00.00','ADMIN'),
(006,'VIPUL','DIWAN',200000,'14-06-11 09.00.00','ACCOUNT'),
(007,'SATISH','KUMAR',100000,'14-01-20 09.00.00','ACCOUNT'),
(008,'GEETIKA','CHAUHAN',90000,'14-04-11 09.00.00','ADMIN');


ERRORS

 SALARY INT(15), — — — — SALARY INT,
  SHOULD NOT WRITE WORKER_ID AS IT IS PRIMARY KEY AND AUTO INCREMENTED.
SELECT * FROM Worker1; IS NOT PRESENT

Answer the following questions with writing the appropriate queries.
Question 1:
Write an SQL query to fetch “FIRST_NAME” from the Worker table using the alias name
<WORKER_NAME>.

SELECT FIRST_NAME AS WORKER_NAME FROM Worker1;



Question 2:
Write an SQL query to fetch unique values of DEPARTMENT from the Worker table.

SELECT DISTINCT DEPARTMENT FROM Worker1;


Question 3:
Write an SQL query to print the first three characters of FIRST_NAME from the Worker table.

SELECT LEFT(FIRST_NAME, 3) AS First_Three_Characters FROM Worker1;

Question 4:
Write an SQL query that fetches the unique values of DEPARTMENT from the Worker table and
prints its length.

SELECT DISTINCT DEPARTMENT, LENGTH(DEPARTMENT) AS DPTT_Len FROM Worker1;

Question 5:
Write an SQL query to print all Worker details from the Worker table order by FIRST_NAME
Ascending and DEPARTMENT Descending.

SELECT * FROM worker1 ORDER BY FIRST_NAME ASC, DEPARTMENT DESC;

Question 6:
Write an SQL query to print details of Workers with DEPARTMENT name as “Admin”.

SELECT * FROM Worker1 WHERE DEPARTMENT = 'Admin';


Question 7:
Write an SQL query to print details of the Workers whose SALARY lies between 100000 and
500000.

SELECT * FROM Worker1 WHERE SALARY BETWEEN 100000 AND 500000;

Question 8:
Write an SQL query to fetch worker names with salaries >= 50000 and <= 100000.

SELECT * FROM Worker1 WHERE SALARY>=50000 and  SALARY<= 100000;

Question 9:
Write an SQL query to show only even rows from the WORKER table.

SELECT * FROM Worker1 WHERE MOD(WORKER_ID, 2) = 0;

Question 10:
Write an SQL query to print details of the Workers who joined in Feb’2014.

SELECT * FROM Worker1 WHERE MONTH(JOINING_DATE) = 2 AND YEAR(JOINING_DATE) = 2014;


