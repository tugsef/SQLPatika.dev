# Homework8

*1.QUERY*

 test veritabanınızda employee isimli sütun bilgileri 
 id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) 
 olan bir tablo oluşturalım.
```SQL
    CREATE TABLE employee (
	    id SERIAL PRIMARY KEY,
	    name VARCHAR(50) NOT NULL,
	    email VARCHAR(100),
	    birthday DATE
	
    );
```

*2.QUERY*

```SQL
insert into employee (name, email, birthday) values ('Cece', 'ctitterton0@wsj.com', '2014-09-24');
insert into employee (name, email, birthday) values ('Goldia', 'gyerby1@wikimedia.org', '1987-08-24');
insert into employee (name, email, birthday) values ('Lela', 'lkingsbury2@bbc.co.uk', '1991-01-13');
insert into employee (name, email, birthday) values ('Dulci', 'dtysall3@aol.com', '2019-04-01');
insert into employee (name, email, birthday) values ('Randall', 'rbente4@skype.com', '1964-05-19');
insert into employee (name, email, birthday) values ('Henrie', 'hflagg5@skyrock.com', '1986-03-31');
insert into employee (name, email, birthday) values ('Sherill', 'sgreenland6@shareasale.com', '1988-02-05');
```


*3.QUERY*
```SQL
UPDATE employee
SET name = 'UPDATE'
WHERE id =1
RETURNING*;
```
```SQL
UPDATE employee
SET name = 'Eric',
    email = 'eric@kd.com',
    birthday = '2000-05-01'
WHERE name = 'Langston'
RETURNING*;
```
```SQL
UPDATE employee
SET name = 'Eric',
    email = 'eric@kd.com',
	birthday = '2000-05-01'
WHERE name = 'Langston'
RETURNING*;
```
```SQL
UPDATE employee
SET name = 'Eric',
    email = 'eric@kd.com',
	birthday = '2000-05-01'
WHERE name LIKE '%ny'
RETURNING*;
```
```SQL
UPDATE employee
SET name = '404',
    email = 'eric@kd.com',
	birthday = '2000-05-01'
WHERE name != 'Eric'
RETURNING*;
```

*4.QUERY*
```SQL
DELETE FROM employee
WHERE name = '404'
RETURNING*;
```
```SQL
DELETE FROM employee
WHERE id NOT BETWEEN 20 AND 45
RETURNING*;
```
```SQL
DELETE FROM employee
WHERE name LIKE 'M%a'
RETURNING*;
```
```SQL
DELETE FROM employee
WHERE id > 125
RETURNING*;
```
```SQL
DELETE FROM employee
WHERE id > 110 AND name LIKE 'A%'
RETURNING*;
```
