## Kilka zadań związanych z SQLem.

### Baza danych
![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/df3bfdf0-ac20-4df0-987f-82583fc01f9a)



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
![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/ba28b6d7-64fd-4fb0-9544-0bf53dfe304c)

### 2. Napisz zapytanie SQL, aby dowiedzieć się, kiedy ukazał się film „American Beauty”. Zwróć rok premiery filmu.
```sql
SELECT mov_year FROM movie 
WHERE mov_title='American Beauty'
```
![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/4bb040c2-a3c8-4597-9397-2892de68a71c)

### 3. Napisz zapytanie SQL, aby znaleźć film wydany w 1999 roku. Zwróć tytuł filmu.
```sql
SELECT mov_title, mov_year
FROM movie
WHERE mov_year = '1999'
```
![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/f31461c9-2381-4036-bdbe-66bfa1bc353c)

### 4. Napisz zapytanie SQL, aby znaleźć filmy wydane przed 1999 rokiem. Zwróć tytuł filmu i rok.
```sql
SELECT mov_title, mov_year
FROM movie WHERE mov_year < 1999
```
![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/601ed250-bf9b-4f8c-aefe-e93a7190936b)

### 5. Napisz zapytanie SQL w celu znalezienia nazwy wszystkich filmów i recenzentów na jednej liście.
```sql
SELECT reviewer.rev_name
FROM reviewer UNION
(SELECT movie.mov_title
FROM movie);
```
![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/b002d5b3-6e01-436f-a0d3-09baa10e6cb0)


### 6. Napisz zapytanie SQL, aby znaleźć recenzentów, którzy ocenili film na conajmniej 7 gwiazdek. Zwróć nazwę recenzenta oraz ocenę.
```sql
SELECT reviewer.rev_name, rating.rev_stars
FROM reviewer, rating
WHERE rating.rev_id = reviewer.rev_id
AND rating.rev_stars>=7
AND reviewer.rev_name is not null;
```
![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/7cdc0fec-44bb-48de-bf60-0053b92b1c38)


### 7. Napisz zapytanie SQL aby znaleźć filmy bez żadnej oceny. Zwróć wartość filmu.
```sql
SELECT mov_title
FROM movie
WHERE mov_id NOT IN 
(SELECT mov_id  FROM rating);
```
![image](https://github.com/SebastianKlimas/Portfolio/assets/68077439/248a7e0a-b731-4cd3-bfa4-cc3eb2f70288)

### 8. Napisz zapytanie SQL, aby znaleźć filmy o identyfikatorze 905, 907 lub 917. Zwróć tytuł filmu.
```sql
...
```

### 9. Napisz apytanie SQL, aby znaleźć tytuły filmów zawierające słowo „Boogie Nights”. Posortuj zestaw wyników w kolejności rosnącej według roku filmu. Zwróć identyfikator filmu, tytuł filmu i rok premiery filmu.
```sql
...
```

### 10. Napisz zapytanie SQL, aby znaleźć aktorów o imieniu „Woody” i nazwisku „Allen”. Zwróć identyfikator aktora.
```sql
...
```
