# Assignment Seven

## Answers

### Question 1

- (TURKISH) film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.
- Group the films of the film table by their ratings.

```sql
SELECT rating FROM film
GROUP BY rating;
```

### Question 2

- (TURKISH) film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.
- Sort the film count and the replacement_cost value where we group all films by their replacement_cost column and when the film count is greater than 50.

```sql
SELECT replacement_cost, COUNT(*) as movie_count
FROM film
GROUP BY replacement_cost
HAVING COUNT(*) > 50;
```

### Question 3

- (TURKISH) customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?
- What are the customer numbers for the store_id values of the customer table?

```sql
SELECT store_id, COUNT(*) as member_count
FROM customer
GROUP BY store_id;
```

### Question 4

- (TURKISH) city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.
- Share the country_id info and the city count with most cities after grouping the city data of the city table by the country_id column.

```sql
SELECT COUNT(*) as city_count, country_id
FROM city
GROUP BY country_id
ORDER BY COUNT(*) DESC
LIMIT 1;
```
