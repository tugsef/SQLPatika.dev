# Homework12

*1.QUERY*

  film tablosunda film uzunluğu length sütununda gösterilmektedir. 
  Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
```SQL
	SELECT COUNT(*) FROM film
	WHERE length > 
	(
		SELECT AVG(length) FROM film
		);
```

*2.QUERY*

  film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
```SQL
	SELECT COUNT(*) FROM film
	WHERE  rental_rate =
	(SELECT MAX(rental_rate) FROM film);
```

*3.QUERY*

  film tablosunda en düşük rental_rate ve en düşük replacement_cost değerlerine sahip filmleri sıralayınız.
```SQL
	SELECT * FROM film
	WHERE rental_rate = (SELECT MIN(rental_rate) FROM film) AND 
	replacement_cost = (SELECT MIN (replacement_cost) FROM film);
```

*4.QUERY*

 payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
```SQL
	CREATE VIEW customer_amount AS
	SELECT customer.customer_id , customer.first_name , customer.last_name , COUNT(customer.customer_id) , SUM(payment.amount) AS amount FROM customer
	INNER JOIN payment ON customer.customer_id = payment.customer_id
	GROUP BY customer.customer_id;

	SELECT * FROM customer_amount
	WHERE amount = (
	SELECT MAX(amount) FROM customer_amount
	);

```
