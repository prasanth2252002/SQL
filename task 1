

use student

create table task2(id int , firstname varchar(25), lastname varchar(25), mobno bigint , emailid varchar(25), department varchar(25), designation varchar(25), salary money)

insert into task2 values(001,'s','deepak',3500190463,'depak@gmail.com','finance','data analyst', 990000)
insert into task2 values(002,'r','sathish',7500196463,'sk@gmail.com','sales','senior developer', 660000)
insert into task2 values(003,'n','prasanth',0500490463,'ps@gmail.com','marketing','software trainee', 560000)
insert into task2 values(004,'m','parthiban',5200190463,'pb@gmail.com','legal','software trainee', 590000)
insert into task2 values(005,'o','benito',1500190063,'bo@gmail.com','marketing','software trainee', 780000)
insert into task2 values(169,'s','gowtham',9577190463,'go@gmail.com','R&D','software trainee', 900000)
insert into task2 values(007,'k','arunab',9500190460,'ar@gmail.com','finance','software trainee', 880000)
insert into task2 values(008,'v','karan',2500190463,'kn@gmail.com','marketing','software trainee', 544000)

drop procedure Updatedetails

select * from task2

CREATE PROCEDURE Updatedetails
    @id int,
    @mail varchar(23)
  
  as begin 
 
update  task2 set emailid=@mail where id=@id


end

exec Updatedetails 003,'fouth@gmail.com'
-------------------------------------------------------------


 create procedure delete_student
 (@id int)
 
as

begin 
delete from task2  where id=@id

end

exec delete_student 3

--------------------------------------------------------------


CREATE TABLE Students (
    student_id INT PRIMARY KEY,
    name VARCHAR(50),
    marks INT
);

select * from students


INSERT INTO Students (student_id, name, marks) VALUES 
(1, 'deapak', 80),
(2, 'sathish', 90),
(3, 'parthiban', 70),
(4, 'karan', 60),
(5, 'prasanth', 85),
(6, 'gowtham', 95),
(7, 'benito', 75),
(8, 'raj', 65),
(9, 'kumar', 55),
(10, 'arun', 100);


alter table students drop column marks


drop function calculate_grade

CREATE FUNCTION calculate_grade(@marks INT) 
RETURNS VARCHAR(1)


BEGIN
    DECLARE @grade VARCHAR(1);
    IF @marks >= 90 
	begin
	SET @grade = 'A';
	end

   IF @marks >= 80 and @marks >= 90 
	begin
	SET @grade = 'B';
	end

   IF @marks >= 70 and @marks <= 80
	begin 
	SET @grade = 'C';
	end

    IF @marks >= 60 and @marks <= 70
	begin
	 SET @grade = 'D';
	 end
    RETURN @grade;
END

---------------------------------------------------------------



update tblmarks set grade=dbo.calculate_grade(marks)


select dbo.calculate_grade(marks) from tblmarks

--------------------------------------------------------------



------------------------------------------------------------
delete from tblmarks where  dbo.calculate_grade(marks) = 'c'
--------------------------------------------------------------



CREATE TABLE tblmarks (ids int foreign key references Students(student_id) ,marks INT);

INSERT INTO tblmarks VALUES 
(1, 80),
(2,90),
(3,  70),
(4, 60),
(5, 85),
(6, 95),
(7,  75),
(8, 65),
(9,  55),
(10, 100);


select * from tblmarks

------------------------------------------------------------------------------------------------
create view prodetails
as
select ids,marks,name,grade from Students s join tblmarks t on s.student_id=t.ids
------------------------------------------------------------------------------------------------
select * from prodetails

drop view prodetails
------------------------------------------------------------------------------------------------
alter table tblmarks add  grade varchar(1)

------------------------------------------------------------------------------------------------


drop table Employeedetails

 CREATE TABLE EmployeeDetails (
    id INT PRIMARY KEY,
    employee_name VARCHAR(100),
    date_of_birth DATE)
INSERT INTO EmployeeDetails (id, employee_name, date_of_birth) VALUES
    (1, 'deepak', '1990-05-15'),
    (2, 'sathish', '1985-09-21'),
    (3, 'prasanth', '1992-11-10'),
    (4, 'benito', '1988-03-06'),
    (5, 'rdj', '1997-07-30'),
    (6, 'leo', '1994-12-12'),
    (7, 'gowtham', '1987-08-25'),
    (8, 'arnab', '1993-02-14'),
    (9, 'taylor', '1991-10-18'),
    (10, 'swift', '1989-04-05');

	select * from EmployeeDetails

drop function CalculateAge

CREATE FUNCTION CalculateAge(@birthdate DATE)
RETURNS INT
AS
BEGIN
    DECLARE @age INT;
    SET @age = DATEDIFF(YEAR, @birthdate, cast(getdate() as date))


    RETURN @age;
END;

delete from EmployeeDetails  where  dbo.CalculateAge(date_of_birth) >30 

alter table EmployeeDetails add  ageofemployee int

alter table EmployeeDetails drop column age 


--------------------------------------11--------------------------------------------------
update EmployeeDetails set ageofemployee=dbo.CalculateAge(date_of_birth)
------------------------------------------------------------------------
select dbo.CalculateAge(date_of_birth) from EmployeeDetails
drop table EmployeeDetails
------------------------------------------------------------------------------------------




-- Create the table EmployeeDetails
CREATE TABLE EmployeeDetails (
    id INT PRIMARY KEY,
    employee_name VARCHAR(100),
    date_of_birth DATE
);

-- Insert data into the table EmployeeDetails
INSERT INTO EmployeeDetails (id, employee_name, date_of_birth) VALUES
    (1, 'deepak', '1990-05-15'),
    (2, 'sathish', '1985-09-21'),
    (3, 'prasanth', '1992-11-10'),
    (4, 'benito', '1988-03-06'),
    (5, 'rdj', '1997-07-30'),
    (6, 'leo', '1994-12-12'),
    (7, 'gowtham', '1987-08-25'),
    (8, 'arnab', '1993-02-14'),
    (9, 'taylor', '1991-10-18'),
    (10, 'swift', '1989-04-05');

-- Create the function CalculateAge
CREATE FUNCTION CalculateAge(@birthdate DATE)
RETURNS INT
AS
BEGIN
    DECLARE @age INT;
    SET @age = DATEDIFF(YEAR, @birthdate, CAST(GETDATE() AS DATE));
    RETURN @age;
END;

-- DeleteEmployeesAbove30
CREATE FUNCTION DeleteEmployeesAbove30()
RETURNS TABLE
AS
RETURN
    SELECT *
    FROM EmployeeDetails
    WHERE dbo.CalculateAge(date_of_birth) <= 32;

-- Delete
DELETE FROM EmployeeDetails
WHERE id IN (SELECT id FROM DeleteEmployeesAbove30());

-- 
DROP FUNCTION DeleteEmployeesAbove30;

ALTER TABLE EmployeeDetails ADD ageofemployee INT;

-- Update
UPDATE EmployeeDetails SET ageofemployee = dbo.CalculateAge(date_of_birth);


select * from EmployeeDetails
