# Assignment Three

## Answers

### Question 1

- (TURKISH) country tablosunda bulunan country sütunundaki ülke isimlerinden 'A' karakteri ile başlayıp 'a' karakteri ile sonlananları sıralayınız.
- Sort the data in all columns of the country table with the condition that the country name starts with the character 'A' and ends with character 'a'.

```sql
SELECT * FROM country
WHERE country LIKE 'A%a';
```

### Question 2

- (TURKISH) country tablosunda bulunan country sütunundaki ülke isimlerinden en az 6 karakterden oluşan ve sonu 'n' karakteri ile sonlananları sıralayınız.
- Sort the data in all columns of the country table with the condition that the country name is at least 6 characters and ends with character 'n'.

```sql
SELECT * FROM country
WHERE country LIKE '_____%n';
```

### Question 3

- (TURKISH) film tablosunda bulunan title sütunundaki film isimlerinden en az 4 adet büyük ya da küçük harf farketmesizin 'T' karakteri içeren film isimlerini sıralayınız.
- Sort the data in title columns of the film table with the condition that the film title contains at least 4 case insensitive 'T' characters.

```sql
SELECT * FROM film
WHERE title ILIKE '%t%t%t%t%';
```

### Question 4

- film tablosunda bulunan tüm sütunlardaki verilerden title 'C' karakteri ile başlayan ve uzunluğu (length) 90 dan büyük olan ve rental_rate 2.99 olan verileri sıralayınız.
- Sort the data in all columns of the film table with the condition that the film title starts with character 'C', length is greater than 90 and rental rate is 2.99.

```sql
SELECT * FROM film
WHERE title LIKE 'C%' AND length > 90 AND rental_rate = 2.99;
```