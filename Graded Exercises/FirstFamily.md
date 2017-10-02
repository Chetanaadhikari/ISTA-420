#First Family
##ISTA-420
###Chetana Adhikari

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
id|name|sex|role
1|Donald|1|parent
2|Melania|0|parent
3|Ivanka|0|child
4|Baron|1|child
select * from family where role = "parent";
id|name|sex|role
1|Donald|1|parent
2|Melania|0|parent
select * from family where sex = 0;
id|name|sex|role
2|Melania|0|parent
3|Ivanka|0|child
