# Assignment Five

## Answers

### Question 1

- (TURKISH) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en uzun (length) 5 filmi sıralayınız.
- Sort the longest 5 film of the film table with the condition that the movie title ends with character 'n'.

```sql
SELECT * FROM film
WHERE title LIKE '%n'
ORDER BY length DESC
LIMIT 5;
```

### Question 2

- (TURKISH) film tablosunda bulunan ve film ismi (title) 'n' karakteri ile biten en kısa (length) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.
- Sort the shortest 5 films(6,7,8,9,10) of the film table with the condition that title ends with the character 'n'.

```sql
SELECT * FROM film
WHERE title LIKE '%n'
ORDER BY length ASC
OFFSET 5
LIMIT 5;
```

### Question 3

- (TURKISH) customer tablosunda bulunan last_name sütununa göre azalan yapılan sıralamada store_id 1 olmak koşuluyla ilk 4 veriyi sıralayınız.
- Sort the first 4 data in the last_name column of the customer table with descending order where store_id equals to 1.

```sql
SELECT * FROM customer
WHERE store_id = 1
ORDER BY last_name DESC
limit 4;
```
