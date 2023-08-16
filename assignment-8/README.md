# Assignment Eight

## Answers

### Question 1

- (TURKISH) test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.
- Create an employee table with columns id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100)

```sql
CREATE TABLE employee(
  id INTEGER PRIMARY KEY,
  name VARCHAR(50),
  birthday DATE,
  email VARCHAR(100)
);
```

### Question 2

- (TURKISH) Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.
- Add 50 data to the table we create(employee) using service 'Mockaroo'.

The data is generated using the [Mackaroo Service](https://www.mockaroo.com/).

### Question 3

- (TURKISH) Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.
- Do 5 UPDATE operations that is goint to update other columns according to each of the collumns.

```sql
UPDATE employee
SET name = 'Alex Johenson'
Where id = 3
```

```sql
UPDATE employee
SET birthday = '2019-06-30'
  email = 'erandalston5@usgs.gov'
Where id = 29
```

```sql
UPDATE employee
SET email = 'lcheverell3@canalblog.com'
Where id = 18
```

```sql
UPDATE employee
SET birthday = '1970-06-06'
  name = 'Sharleen Crangle'
Where id = 44
```

```sql
UPDATE employee
SET birthday = '1999-10-08'
  email = 'twestfield2@ning.com'
  name = 'Thorin Westfield'
Where id = 12
```

### Question 4

- (TURKISH) Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.
- Do 5 DELETE operations that will delete the relevant row according to each of the columns.

```sql
DELETE FROM employee
WHERE id = 12
```

```sql
DELETE FROM employee
WHERE email = 'twestfield2@ning.com'
```

```sql
DELETE FROM employee
WHERE email = 'twestfield2@ning.com' AND birthday = '1999-10-08'
```

```sql
DELETE FROM employee
WHERE birthday = '1999-10-08' AND name = 'Thorin Westfield'
```

```sql
DELETE FROM employee
WHERE AND email = 'twestfield2@ning.com' birthday = '1999-10-08' AND name = 'Thorin Westfield'
```
