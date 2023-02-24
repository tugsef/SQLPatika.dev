# Homework10

*1.QUERY*

  city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) 
  isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.
  
```
	SELECT city.city , country.country FROM city
	LEFT OUTER JOIN country ON city.country_id = country.country_id;
```

*2.QUERY*

  customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki 
  first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.
```
	SELECT payment.payment_id , customer.first_name , customer.last_name FROM payment
	RIGHT OUTER JOIN customer ON customer.customer_id = payment.customer_id;
```

*3.QUERY*

  customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki 
  first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.
```
	SELECT rental.rental_id , customer.first_name , customer.last_name FROM rental
	FULL OUTER JOIN customer ON customer.customer_id = rental.customer_id;
```
