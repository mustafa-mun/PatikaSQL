# Assignment Six

## Answers

### Question 1

- (TURKISH) film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?
- What is the average of the values on the rental_rate column of the film table ?

```sql
SELECT AVG(rental_rate)
FROM film;
```

The answer is 2.98.

### Question 2

- (TURKISH) film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?
- How many films of the film table starts with character 'C' ?

```sql
SELECT COUNT(*)
FROM film
WHERE title LIKE 'C%';
```

The answer is 92.

### Question 3

- (TURKISH) film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?
- What is the length of the longest film that belongs to film table whose rental rate value equals to 0.99 ?

```sql
SELECT MAX(length)
FROM film
WHERE rental_rate = 0.99;
```

The answer is 184.

### Question 4

- (TURKISH) film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?
- How many diffrent replacement_cost values are there for the films of the film table whose length is greater than 150 minutes ?

```sql
SELECT COUNT(DISTINCT replacement_cost)
FROM film
WHERE length > 150;
```

The answer is 21.
