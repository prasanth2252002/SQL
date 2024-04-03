create database trig
use trig

/* after Delete*/
create table currentStudents(id int,name varchar(30),studyingyear int,dept varchar(30),passingyear int)
create table passedoutstudents(id int,name varchar(30),dept varchar(30),passingyear int)

select*from currentStudents
select *from passedoutstudents


drop table passedoutstudents


insert into currentStudents values(121,'sathish',4,'eee',2023)
insert into currentStudents values(12312,'dev',4,'ece',2022)
insert into currentStudents values(423,'mani',4,'mech',2021)
insert into currentStudents values(1281,'rajkumar',4,'ece',2023)
insert into currentStudents values(5645,'chandru',3,'it',2024)
insert into currentStudents values(86578,'santhosh',2,'civil',2025)
insert into currentStudents values(7686,'guna',1,'mech',2021)
insert into currentStudents values(45,'mark',4,'eee',2025)

create trigger delete_AfterTrigger on currentStudents 
for delete as
insert into passedoutstudents(id,name,dept,passingyear) select del.id,del.name,del.dept,del.passingyear from deleted del
print'trigger deleted'

drop trigger delete_AfterTrigger
delete from currentstudents where passingyear=2023

----/After Insert/
create table orginal(id int,name varchar(30),email varchar(30))
create table backupdb(id int,name varchar(30),email varchar(30))

create trigger insert_trigger on orginal
for insert as
insert into backupdb (id,name,email) select i.id,i.name,i.email from inserted  as i
print 'inserted successfull'

insert into orginal values(121,'sathish','sathishskvnr@gmail.com')

select* from orginal
select* from backupdb

/* Instead of Update*/

create table students(id int,name varchar(20),dept varchar(30),sportsid int)
create table sports(sportsid int,event varchar(20),prizes int)

insert into students values(121,'sathish','EEE',23)
insert into students values(122,'madesh','MECH',26)
insert into students values(123,'rahul','CIVIL',203)
insert into students values(124,'david','IT',20)
insert into students values(125,'kishore','ECE',216)
insert into students values(126,'chandru','EEE',225)
insert into students values(127,'Deepak','ECE',223)

insert into sports values(216,'football',2)
insert into sports values(223,'Volley ball',3)
insert into sports values(23,'Tennis',0)
insert into sports values(225,'football',1)
insert into sports values(20,'cricket',5)
insert into sports values(203,'Carom',7)
insert into sports values(26,'Chess',2)

select* from students
select* from sports


create view studentdetails
as
select st.id,st.name,st.dept,st.sportsid,sp.event,sp.prizes
from students st join sports sp on st.sportsid=sp.sportsid


create trigger  studentdetails_trigger on studentdetails
instead of update as
declare @id int, @name varchar(20),@event varchar(20),@spid int
select @name=st.name from students st join inserted i on st.sportsid=i.sportsid
select @event=i.event from students st join inserted i on st.sportsid=i.sportsid
select @id=sportsid from students where name=@name 
update sports set event=@event where sportsid=@id
print'updated'

select * from studentdetails


update studentdetails set event='chess' where name='rahul'

/* instead of delete*/

create trigger delete_trigger on studentdetails
instead of delete as 
declare @id int, @name varchar(20),@dept varchar(30),@sportsid int,@event varchar(20),@prize int
select @id=deleted.id from deleted
select @name=deleted.name from deleted
select @DEPT=deleted.dept from deleted
select @sportsid=deleted.sportsid from deleted
select @event=deleted.event from deleted
select @prize=deleted.prizeS from deleted
delete  from studeNTS where id=@id
DELETE FROM sports where event=@event
print 'deleted'

delete from  studentdetails where event='chess'
delete from studentdetails where name='madesh'

drop trigger delete_trigger
