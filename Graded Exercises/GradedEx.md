#Name: first.sql
##Author: Chetana Adhikari
###Date: August 8, 2017

.echo on
.headers on

drop table if exists text;

create table text (
  id int,
  name text,
  role text,
  sex int
);

insert into text values (1, "Charles", "parent", 1);
insert into text values (2, "Bonnie", "parent", 0);
insert into text values (3, "Casie", "child", 0);
insert into text values (4, "Jackson", "child", 1);
insert into text values (5, "Midnight", "pet", 0);


select * from text;
select * from text where role = "child";
select * from text where sex = 1;
select * from text where sex = 1 and role ="parent";
