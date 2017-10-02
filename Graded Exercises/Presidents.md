#ISTA-420
##Chetana Adhikari
###Presidents graded Exercise

CREATE TABLE T1
( President nchar(100),
  Tookoffice nchar(100),
  Leftoffice nchar(100),
  Party nchar(100),
  Homestate nchar(100));

  Bulk INSERT T1 FROM 'C:\users\chetana\President.csv'
  WITH
  (
  DaTAFILETYPE ='char',
  FIELDTERMINATOR = ',',
  ROWTERMINATOR ='\n'
  );


using Presidents;
select * from T1;

Delete from T1
Where President = 'President';


ALTER TABLE T1
ADD PRIMARY KEY (ID);

Select * from T1;

ALTER TABLE T1
    ADD RowId int NOT NULL IDENTITY (1,1);

	ALTER TABLE T1
ADD PRIMARY KEY (RowID);

UPDATE T1
SET Leftoffice = '01/20/2017'
WHERE President = 'Barack Obama';

INSERT INTO T1
VALUES ('Donald Trump', '01/20/2017', 'Current', 'Republican', 'Newyork');

SELECT * FROM T1
ORDER BY Party, Homestate;

SELECT COUNT (Party)
FROM T1
WHERE Party = 'Democratic';

SELECT COUNT (Party)
FROM T1
WHERE Party = 'Republican';

Select COUNT (Party)
FROM T1
Where Party = 'Whig';

SELECT distinct e.city
FROM hr.Employees e
inner join sales.Customers c
on e.city = c.city;

SELECT distinct e.city
FROM hr.Employees e
left join sales.Customers c
on e.city = c.city
where c.city is null;



