#Name: second.sql
##Author: Chetana Adhikari
###Date: August 8, 2017

.echo on
.headers on

drop table if exists family;

create table family (
  id int, 
  name text,
  sex int,
  role text
);

insert into family values (1, "Donald", 1, "parent");
insert into family values (2, "Melania", 0, "parent");
insert into family values (3, "Ivanka", 0, "child");
insert into family values (4, "Baron", 1, "child");

select * from family;
select * from family where role = "parent";
select * from family where sex = 0;
