use dbname

/create a table/

create table employee(id int, firstname varchar(25), lastname varchar(25), mobno bigint , emailid varchar(25), department varchar(25), designation varchar(25), salary int)
alter table employee alter column mobno bigint

/insert 8  values/
ALTER TABLE employee ADD takehome int;

insert into employee values(001,'s','deepak',3500190463,'depak@gmail.com','finance','data analyst', 550000)
insert into employee values(002,'r','sathish',7500196463,'sk@gmail.com','sales','senior developer', 660000)
insert into employee values(003,'n','prasanth',0500490463,'ps@gmail.com','marketing','software trainee', 560000)
insert into employee values(004,'m','parthiban',5200190463,'pb@gmail.com','legal','software trainee', 590000)
insert into employee values(005,'o','benito',1500190063,'bo@gmail.com','marketing','software trainee', 780000)
insert into employee values(006,'s','gowtham',9577190463,'go@gmail.com','R&D','software trainee', 900000)
insert into employee values(007,'k','arunab',9500190460,'ar@gmail.com','finance','software trainee', 880000)
insert into employee values(008,'v','karan',2500190463,'kn@gmail.com','marketing','software trainee', 544000)


select * from employee

/alter  table by adding dob and joining date/

alter table employee add dob date, dateofjoining date

/update values/

update employee set dateofjoining = '2022/12/1' where department ='marketing';

update employee set dateofjoining = '2020/11/11' where department ='sales';

update employee set dateofjoining = '2021/10/9' where department ='finance';

update employee set dateofjoining = '2021/10/28' where department ='R&D';

update employee set dateofjoining = '2021/1/28' where department ='legal';

update employee set dob = '2002/01/3 ' where id = 1;

update employee set dob = '2001/02/3 ' where id = 2;

update employee set dob = '2002/03/9 ' where id = 3;

update employee set dob = '2002/04/2 ' where id = 4;

update employee set dob = '2002/05/9 ' where id = 5;

update employee set dob = '2001/06/3 ' where id = 6;

update employee set dob = '2002/07/5 ' where id = 7;

update employee set dob = '2002/08/9 ' where id = 8;

update employee set dob = '2002/09/13 ' where id = 9;

update employee set dob = '2001/11/23 ' where id = 10;


/show vales of emp > 1 exp/

select * from employee where salary >= 600000 and datediff(year,dateofjoining,cast(getdate() as date)) >= 1

/show exp/

select datediff(year,dateofjoining,cast(getdate() as date)) as date from employee

/expenditure/

select sum(salary) from employee where department = 'marketing'


/delete the highest salary/

DELETE FROM employee WHERE salary = (select max(salary) from employee )

/calculate takehome ctc by salary/

UPDATE employee SET takehome = salary - (salary * 0.2)

/sort by vsalary from least to high/


SELECT id, firstname, lastname, department, designation, salary, takehome FROM employee ORDER BY takehome
