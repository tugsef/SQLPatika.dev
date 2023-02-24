# Homework11

**1.QUERY**

  actor ve customer tablolarında bulunan first_name sütunları 
 için tüm verileri sıralayalım.
```
	(SELECT first_name FROM actor)
	UNION
	(SELECT first_name FROM customer)
	ORDER BY first_name;
```

 *1.1.QUERY*

  actor ve customer tablolarında bulunan first_name sütunları 
 için tüm verileri sıralayalım.
```
	(SELECT first_name FROM actor)
	UNION ALL
	(SELECT first_name FROM customer)
	ORDER BY first_name;
```

 **2.QUERY**

  actor ve customer tablolarında bulunan first_name sütunları 
  için kesişen verileri sıralayalım.
```
	(SELECT first_name FROM actor)
	INTERSECT
	(SELECT first_name FROM customer)
	ORDER BY first_name;
 ```
 
  *2.1.QUERY*

  actor ve customer tablolarında bulunan first_name sütunları 
  için kesişen verileri sıralayalım.
```
	(SELECT first_name FROM actor)
	INTERSECT ALL
	(SELECT first_name FROM customer)
```

 **3.QUERY**

  actor ve customer tablolarında bulunan first_name sütunları 
  için kesişen verileri sıralayalım.
```
	(SELECT first_name FROM actor)
	EXCEPT
	(SELECT first_name FROM customer)
	ORDER BY first_name;
```

 *3.1.QUERY*

  actor ve customer tablolarında bulunan first_name sütunları 
  için kesişen verileri sıralayalım.
```
	(SELECT first_name FROM actor)
	EXCEPT ALL
	(SELECT first_name FROM customer)
	ORDER BY first_name;
```
