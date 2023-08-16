# Assignment Eleven

## Answers

### Question 1

- (TURKISH) 'film' tablosunda film uzunluğu length sütununda gösterilmektedir. Uzunluğu ortalama film uzunluğundan fazla kaç tane film vardır?
- Film length is shown on the length column in the film table. How many films are there which length is greater than average film length of film table ?

```sql
SELECT COUNT(*) FROM film
WHERE length >
(
  SELECT AVG(length) FROM film
);
```

### Question 2

- (TURKISH) film tablosunda en yüksek rental_rate değerine sahip kaç tane film vardır?
- How many film are there on the film table which has the maximum rental rate value ?

```sql
SELECT COUNT(*) FROM FILM
WHERE rental_rate =
(
  SELECT MAX(rental_rate) FROM film
);
```

### Question 3

- (TURKISH) film tablosunda en düşük rental_rate ve en düşük replacement_cost değerlerine sahip filmleri sıralayınız
- Sort the films of the film table with the lowest rental_rate and the lowest replacement_cost.

```sql
SELECT rental_rate, replacement_cost
FROM FILM
ORDER BY rental_rate, replacement_cost ASC;
```

### Question 4

- (TURKISH) payment tablosunda en fazla sayıda alışveriş yapan müşterileri(customer) sıralayınız.
- Sort the customers by their purchase count.

```sql
SELECT customer_id, COUNT(*) AS payment_count
FROM payment
GROUP BY customer_id
ORDER BY COUNT(*) DESC;
```
