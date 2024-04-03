

/*#1*/



use dbname
CREATE TABLE academics (student_id INT PRIMARY KEY,name VARCHAR(50),department VARCHAR(50),year INT,percentage FLOAT)
create table extracirrucular(id int,symposiom int ,internship varchar(20),certification int)
create table sports(id int,event varchar(20),prizes int)

insert into academics values(001,'deepak','ECE',1, 90.9)
insert into academics values(002,'sathish','EEE',2, 88.4)
insert into academics values(003,'prasanth','CSE',3, 87.7)
insert into academics values(004,'parthiban','ECE',4, 98.4)
insert into academics values(005,'benito','IT',3, 95.2)
insert into academics values(006,'gowtham','EEE',2, 94.1)
insert into academics values(007,'arunab','ECE',3, 91.6)
insert into academics values(008,'karan','EEE',1, 93.8)






insert into extracirrucular values(1,0,'yes',4)
insert into extracirrucular values(2,3,'No',2)
insert into extracirrucular values(3,2,'yes',8)
insert into extracirrucular values(4,2,'no',4)
insert into extracirrucular values(5,0,'yes',3)
insert into extracirrucular values(6,3,'no',4)
insert into extracirrucular values(7,1,'yes',2)
insert into extracirrucular values(8,7,'yes',2)

insert into sports values(1,'cricket',3)
insert into sports values(2,'football',1)
insert into sports values(3,'chess',7)
insert into sports values(4,'carom',2)
insert into sports values(5,'badmition',1)
insert into sports values(6,'kabadi',4)
select * from academics
select * from extracirrucular
select * from sports
/*##############################################11111111111*/
SELECT   a.student_id,   a.name,   a.department,   a.year,   a.percentage,   e.symposiom,   e.internship,   e.certification,   s.event,   s.prizes FROM academics a LEFT JOIN extracirrucular e ON a.student_id = e.id LEFT JOIN sports s ON a.student_id = s.id;


/*#2*/

CREATE TABLE customerdetails (customer_id INT PRIMARY KEY,customer_name VARCHAR(100) ,city VARCHAR(50))

create table ordertable(order_id int  , orderdate date, orderamount money)

create table sales (salesid int  ,salespersonname varchar(25), comission int)


select * from customerdetails
select * from ordertable
select * from sales



update sales set city = 'chennai' where salespersonname ='Alice';

update sales set city = 'salem' where salespersonname ='Bob';

update sales set city = 'chennai' where salespersonname ='Eva';

update sales set city = 'salem' where salespersonname ='John';

update sales set city = 'chennai' where salespersonname ='Davis';

insert into customerdetails values(1,'arun','chennai')
insert into customerdetails values(2,'varun','salem')
insert into customerdetails values(3,'tharun','madurai')
insert into customerdetails values(4,'code','chennai')
insert into customerdetails values(5,'ram','salem')
insert into customerdetails values(6,'ajay','salem')
insert into customerdetails values(7,'vijay','chennai')
insert into customerdetails values(8,'jay','madurai')


INSERT INTO ordertable VALUES
    (1, '2023-07-20', 100.50),
    (2, '2023-07-21', 250.75),
    (3,  '2023-07-21', 75.20),
    (4,  '2023-07-22', 300.00),
    (5, '2023-07-23', 150.25);


	INSERT INTO sales VALUES
    (1, 'Alice', 5.00),
    (2, 'Bob ', 4.50),
    (3, 'Eva ', 6.25),
    (4, 'John ', 3.75),
    (5, 'Davis', 4.00);

	alter table sales add city varchar(25)

		select * from customerdetails
			select * from ordertable
	select * from sales


	/*##############################################222222222222222*/

	SELECT cd.customer_id,cd.customer_name,cd.city,ot.orderdate,ot.orderamount,s.salespersonname,s.comission FROM customerdetails cd LEFT JOIN ordertable ot ON cd.customer_id = ot.order_id LEFT JOIN
    sales s ON cd.customer_id = s.salesid;
	

	/*#3*/
	/*##############################################333333333333*/


	SELECT
    s.salespersonname AS "Salesperson Name", cd.customer_name AS "Customer Name", cd.city AS "City" FROM customerdetails cd INNER JOIN
    ordertable ot ON cd.customer_id = ot.order_id INNER JOIN sales s ON cd.customer_id = s.salesid WHERE
    cd.city = s.city;


/*#4*/

CREATE TABLE product (id INT PRIMARY KEY, name VARCHAR(100), price DECIMAL(10, 2),company_id INT)


select * from product

INSERT INTO product (id, name, price, company_id)
VALUES
 (122, 'iphone 14 pro max', 145000.00, 3),
    (123, 'Pixel 6', 72000.00, 5),
    (134, 'OnePlus 9T', 62000.00, 4),
    (145, 'Redmi Note 11 Pro', 24000.00, 2),
    (156, 'Sony Xperia 5 III', 92000.00, 6),
    (167, 'Airpods', 28000.00, 3),
    (178, 'Galaxy Buds Pro', 21000.00, 1),
    (189, 'Surface Laptop 4', 87000.00, 7)





    (101, 'Galaxy s23', 75000.00, 1),
    (102, 'iphone 14 pro max', 130000.00, 3),
    (103, 'Pixel 6', 69999.00, 5),
    (104, 'OnePlus 9T', 59999.00, 4),
    (105, 'Redmi Note 11 Pro', 22999.00, 2),
    (106, 'Sony Xperia 5 III', 89999.00, 6),
    (107, 'Airpods', 26799.00, 3),
    (108, 'Galaxy Buds Pro', 18999.00, 1),
    (109, 'Surface Laptop 4', 84999.00, 7),
    (110, 'MacBook Pro M1', 109999.00, 8),
    (111, 'Dell XPS 15', 99999.00, 9),
    (112, 'Asus ROG Phone 5', 54999.00, 10);

   



	CREATE TABLE company (
    companyid INT PRIMARY KEY,
    name VARCHAR(100) NOT NULL)


select * from company




INSERT INTO company (companyid, name)
VALUES
    (1, 'Samsung'),
    (2, 'Nokia'),
    (3, 'Apple'),
    (4, 'OnePlus'),
    (5, 'Google'),
    (6, 'Sony'),
    (7, 'Microsoft'),
    (8, 'Apple Inc.'),
    (9, 'Dell'),
    (10, 'Asus'),
    (11, 'Xiaomi'),
    (12, 'Lenovo');



		/*##############################################444444444444*/

SELECT p.id AS product_id, p.name AS product_name, p.price, c.name AS company_name FROM product p INNER JOIN company c ON p.company_id = c.companyid
INNER JOIN (
    SELECT company_id, MAX(price) AS max_price
    FROM product
    GROUP BY company_id
) max_prices ON p.company_id = max_prices.company_id AND p.price = max_prices.max_price;
