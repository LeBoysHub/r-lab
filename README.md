https://www.geeksforgeeks.org/how-to-execute-sql-server-stored-procedure-in-sql-developer/amp/


https://www.geeksforgeeks.org/sql-procedures/amp/

https://www.codeproject.com/Articles/25600/Triggers-SQL-Server




# dbms-lab-2
create table employ(Empid numeric(5),
					FirstName varchar(20),
					LastName varchar(30),
					Email varchar(30),
					PhoneNo numeric(10),
					Salary integer);
insert into employ values(901,'siva','kumar','csk@gmail.com',9966338855,25000), 
						 (902,'mahi','reddy','mahireddy@gmail.com',8855228855,25000),
						 (903,'sumanth','godari','sumanth@gmail.com',7744117744,25000);
insert into employ(FirstName,LastName,Email,PhoneNo) values ('sai','segji','sai@gamil.com',1122334455);
insert into employ(Empid,Email)values('911','911@gmail.com');
select * from employ;
exec sp_help employ;
alter table employ add constraint PK_employ primary key(Empid,Email);
alter table employ 
alter column Empid numeric(6) NOT NULL;
alter table employ alter column Email varchar(25) NOT NULL;
alter table employ add  primary key(Email);
truncate table employ;
drop table employ;



create table depart(DeptNo int,DeptName varchar(20),Location varchar(20),designation varchar(30));
insert into depart values(500,'CSE','kalikir','des'),
						 (400,'CIV','kalikiri','des1'),
						 (300,'EEE','lalaikiri','dd');
insert into depart(DeptNo,DeptName,Location) values (400,'EEE','KKKK');
exec sp_help depart;
select * from depart;
drop table depart;
alter table depart alter column DeptNo int NOT Null;
alter table depart alter column DeptName varchar(20) NOT NULL;
alter table depart add constraint PK_depart unique(DeptName);
alter table depart add constraint PK_depart primary key(DeptNo);
