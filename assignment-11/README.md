# Assignment Eleven

## Answers

### Question 1

- (TURKISH) actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.
- Sort all the data for the first_name colummns of actor and customer tables.

```sql
( SELECT first_name  FROM customer
)
UNION
(
SELECT first_name FROM actor
);
```

### Question 2

- (TURKISH) actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.
- Sort all the common data for the first_name colummns of actor and customer tables.

```sql
( SELECT first_name  FROM customer
)
INTERSECT
(
SELECT first_name FROM actor
);
```

### Question 3

- (TURKISH) actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.
- Sort the data for the first_name columns of actor and customer tables which exists on first table but not on second.

```sql
( SELECT first_name  FROM actor
)
EXCEPT
(
SELECT first_name FROM customer
);
```

### Question 4

- (TURKISH) İlk 3 sorguyu tekrar eden veriler için de yapalım.
- Do the first 3 query again for the duplicate datas.

```sql
( SELECT first_name  FROM customer
)
UNION ALL
(
SELECT first_name FROM actor
);
```

```sql
( SELECT first_name  FROM customer
)
INTERSECT ALL
(
SELECT first_name FROM actor
);
```

```sql
( SELECT first_name  FROM actor
)
EXCEPT ALL
(
SELECT first_name FROM customer
);
```
