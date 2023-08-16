# Assignment Ten

## Answers

### Question 1

- (TURKISH) city tablosu ile country tablosunda bulunan şehir (city) ve ülke (country) isimlerini birlikte görebileceğimiz LEFT JOIN sorgusunu yazınız.
- Write a LEFT JOIN query where we can see the city and country names of the city and country tables together.

```sql
SELECT city.city, country.country
FROM CITY
LEFT JOIN country ON country.country_id = city.country_id;
```

### Question 2

- (TURKISH) customer tablosu ile payment tablosunda bulunan payment_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz RIGHT JOIN sorgusunu yazınız.
- Write a RIGHT JOIN query where we can see the payment id of payment table and the first_name and last_name columns of the customer table together.

```sql
SELECT payment.payment_id, customer.first_name, customer.last_name
FROM customer
RIGHT JOIN payment ON payment.customer_id = customer.customer_id;
```

### Question 3

- (TURKISH) customer tablosu ile rental tablosunda bulunan rental_id ile customer tablosundaki first_name ve last_name isimlerini birlikte görebileceğimiz FULL JOIN sorgusunu yazınız.
- Write a FULL JOIN query where we can see the rental id of rental table and the first_name and last_name columns of the customer table together.

```sql
SELECT rental.rental_id, customer.first_name, customer.last_name
FROM customer
FULL JOIN rental ON rental.customer_id = customer.customer_id;
```
