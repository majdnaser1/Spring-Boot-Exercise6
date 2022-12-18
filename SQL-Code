# DDL - Create
create database bank;

create table customer (
    id varchar(25)  primary key ,
    username varchar(20)  not null ,
    email varchar(255)  unique ,
    password varchar(20)  not null ,
    role varchar(5) check( role='admin' or role = 'user' )
);

create table  account (
    id varchar(10) primary key ,
    balance int default 0 ,
    customer_id varchar(25) ,
    foreign key (customer_id) references customer(id)
);

create table  loan (
    id varchar(10) primary key ,
    loanAmount int default 100 check ( loanAmount >= 100 ),
    isPaid boolean default false,
    account_id varchar(10) ,
    foreign key (account_id) references  account(id)
);

# DDL - Drop

drop database bank;
drop table loan;
drop table account;
drop table customer;

# DDL - Alter
alter table  customer add column age int;
alter table  customer drop  column  age;


# DDL - Truncate
truncate  table  loan;


# ---------------------

# DQL - Select
select  * from customer;
select  * from loan;
select  * from account;


# ---------------------

# DML - Insert

insert  into customer values  ('1','saleh','s@s.com','123456','admin');
insert  into customer values  ('2','ali','ali@ali.com','123456','admin');
insert into  account values ('1',1000,'1');
insert into  loan values ('1',100000,false,'1');


# DML - Update

update  customer set  email='saleh@saleh.com' where id='1';

# DML - Delete

delete from  customer where id='1';
