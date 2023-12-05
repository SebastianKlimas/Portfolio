## Kilka zadań związanych z SQLem.

```sql
SELECT * FROM Production.ProductCategory
Order by Name
```
![Screenshot_2](https://github.com/SebastianKlimas/Portfolio/assets/68077439/8bfb1e66-5370-43c9-98ce-077499715e49)

### 1. Napisz zapytanie SQL zwracające Tytuł filmu i rok premiery filmu.
```sql
SELECT mov_title, mov_year
FROM movie;
```
!![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/ba28b6d7-64fd-4fb0-9544-0bf53dfe304c)

### 2. Napisz zapytanie SQL, aby dowiedzieć się, kiedy ukazał się film „American Beauty”. Zwróć rok premiery filmu.
```sql
SELECT mov_year FROM movie 
WHERE mov_title='American Beauty'
```
!![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/4bb040c2-a3c8-4597-9397-2892de68a71c)

### 3. Napisz zapytanie SQL, aby znaleźć film wydany w 1999 roku. Zwróć tytuł filmu.
```sql
SELECT mov_title, mov_year
FROM movie
WHERE mov_year = '1999'
```
!![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/f31461c9-2381-4036-bdbe-66bfa1bc353c)

### 4. Napisz zapytanie SQL, aby znaleźć filmy wydane przed 1999 rokiem. Zwróć tytuł filmu
```sql

