# Assignment One

## Answers

### Question 1

- (TURKISH) film tablosunda bulunan tüm sütunlardaki verileri replacement cost değeri 12.99 dan büyük eşit ve 16.99 küçük olma koşuluyla sıralayınız ( BETWEEN - AND yapısını kullanınız.)
- Arrange the data in all columns of the film table with the condition that the replacement cost value is greater or equal to 12.99 and less than 16.99. ( use BETWEEN - AND clause. )

```sql
SELECT * FROM film
WHERE replacement_cost BETWEEN 12.99 and 16.98;
```

### Question 2

- (TURKISH) actor tablosunda bulunan first_name ve last_name sütunlardaki verileri first_name 'Penelope' veya 'Nick' veya 'Ed' değerleri olması koşuluyla sıralayınız. ( IN operatörünü kullanınız.)
- Arrange the data in first_name and last_name columns of the actor table with the condition that the first_name value is 'Penelope', 'Nick' or 'Ed'. ( use IN clause. ) 

```sql
SELECT first_name, last_name FROM actor
WHERE first_name IN ('Penelope','Nick','Ed');
```

### Question 3

- (TURKISH) film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99, 2.99, 4.99 VE replacement_cost 12.99, 15.99, 28.99 olma koşullarıyla sıralayınız. ( IN operatörünü kullanınız.)
- Arrange the data in all columns of the film table with the conditions that the rental rate is either 0.99, 2.99 or 4.99 and the replacement cost is either 12.99, 15.99 or 28.99. ( use IN clause. ) 

```sql
SELECT * FROM film
WHERE rental_rate IN (0.99, 2.99, 4.99) AND replacement_cost IN (12.99, 15.99, 28.99);
```