1. Create a db called company consist of the following tables.
1.Emp (eno,ename, job,hiredate,salary,commission,deptno,) 
2.dept(deptno,deptname,location) 
eno is primary key in emp 
deptno is primary key in dept 
create table Emp(eno int(10),ename varchar(10),job varchar(10), hiredate date,salary varchar(10),commision varchar(10),deptno varchar(20));
create table dept(deptno varchar(20),deptname varchar(20),location varchar(20));
ALTER TABLE Emp ADD PRIMARY KEY (eno);
ALTER TABLE dept ADD PRIMARY KEY (deptno);

insert into Emp(eno,ename,job,hiredate,salary,commision,deptno) values (01,'ABC','manager',2022/01/02,'5000','2000','10');
insert into Emp(eno,ename,job,hiredate,salary,commision,deptno) values (02,'PQR','salesman',2022/01/02,'1001','500','20');
insert into Emp(eno,ename,job,hiredate,salary,commision,deptno) values (03,'XYZ','manager',2022/01/02,'1000','2500','10');
insert into Emp(eno,ename,job,hiredate,salary,commision,deptno) values (04,'LMN','salesman',2022/01/02,'500','2500','20');
insert into dept (deptno,deptname,location) values ('10','production','Pune');
insert into dept (deptno,deptname,location) values ('20','Marketing','Mumbai');







Solve Queries by SQL

 1. List the maximum salary paid to salesman

SELECT MAX(salary)FROM Emp where job = 'salesman' ;

 2. List name of emp whose name start with ‘I’ 

select * from Emp where ename like 'I%'

3. List details of emp who have joined before ’30-sept-81’ 

select * from Emp where hiredate < 30/09/1981;

4. List the emp details in the descending order of their basic salary 

select * from Emp order by salary desc;

5. List of no. of emp & avg salary for emp in the dept no ‘20’ 

SELECT COUNT(ename)from Emp;

SELECT AVG(salary)from Emp where deptno = '20'

6. List the avg salary, minimum salary of the emp hiredatewise for dept no ‘10’. 

SELECT AVG(salary) from Emp where deptno = '10' ;

SELECT MIN(salary) from Emp where deptno = '10' ;

7. List emp name and its department 

select Emp.ename,dept.deptno from Emp inner join dept on Emp.deptno = dept.deptno;

8. List total salary paid to each department 

SELECT SUM(salary) from Emp where deptno = '10';

SELECT SUM(salary) from Emp where deptno = '20';

9. List details of employee working in ‘Dev’ department 

SELECT Emp.ename, dept.deptname from Emp inner join dept on Emp.deptno = dept. deptno where deptname = 'Dev';

10. Update salary of all employees in deptno 10 by 5 %.

update Emp set salary = salary + 5 where deptno = '10';

select * from Emp;
