# Assignment One

## Answers

### Question 1

- (TURKISH) film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.
- Sort the data in the title and description columns found in the film table.

```sql
SELECT title, description
FROM film;
```

### Question 2

- (TURKISH) film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.
- Sort the data in all columns of the film table with the condition that the film length (length) is greater than 60 and less than 75.

```sql
SELECT * FROM film
WHERE length > 60 AND length < 75;
```

### Question 3

- (TURKISH) film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.
- Sort the data in all columns of the film table with the conditions that the rental rate is 0.99 and the replacement cost is either 12.99 or 28.99.

```sql
SELECT * FROM film
WHERE rental_rate = 0.99 AND (replacement_cost = 12.99 OR replacement_cost = 28.99);
```

### Question 4

- (TURKISH) customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?
- What is the value in the last_name column for the customer whose value in the first_name column in the customer table is 'Mary'?

Smith.

### Question 5

- (TURKISH) film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.
- Sort the data that does not have a length (length) greater than 50 and also does not have a rental_rate value of 2.99 or 4.99 in the film table.

```sql
SELECT * FROM film
WHERE NOT length > 50 AND NOT (rental_rate = 2.99 OR rental_rate = 4.99);
```
