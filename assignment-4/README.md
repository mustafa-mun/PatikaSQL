# Assignment Four

## Answers

### Question 1

- (TURKISH) film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.
- Sort the distinc values ​​in the replace_cost column in the film table.

```sql
SELECT DISTINCT replacement_cost
FROM film;
```

### Question 2

- (TURKISH) film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
- How many different data are there in the replacement cost columns in the film table ?

```sql
SELECT COUNT(DISTINCT replacement_cost)
FROM film;
```

The answer is 21.

### Question 3

- (TURKISH) film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
- How many movie names (title) are starts with character 'T' and at the same time rating equals to 'G' in the film table ?

```sql
SELECT COUNT(*)
FROM film
WHERE title LIKE 'T%' AND rating = 'G';
```

The answer is 9.

### Question 4

- country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
- How many country names contains exactly five characters in the country table ?

```sql
SELECT COUNT(*)
FROM country
WHERE country LIKE '_____';
```

The answer is 13.

### Question 5

- city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?
- How many city names ends with character 'R' or 'r' in the city table ?

```sql
SELECT COUNT(*)
FROM city
WHERE city ILIKE '%r';
```

The answer is 33.
