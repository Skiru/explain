Table link
https://dev.mysql.com/doc/index-other.html 
WORLD

### Jak działą indeksy (DLA PRIMARY, lub UNIQUE)?
````
SELECT * FROM TABELA WHERE USER_ID=100;
````
1. Silnik SQL przeszukuje indeks w poszukiwaniu wartości 100
2. Znajduje wartość w indeksie i odczytuje przypisany do tej wartości rowid.
3. Poprzez rowid (adres fizyczny wiersza na dysku) silnik sql dostaje się do wiersza w tabeli.

### Tworzenie indeków
Index B-tree gdy mamy zróżnicowane dane
````
CREATE INDEX NAZWAINDEKSU ON NAZWATABELI(NAZWAKOLUMNY)
````

Index złożony na więcej niż jedną kolumnę, np gdy w WHERE, JOIN lub GROUP BY jest wiele tabel
````
CREATE INDEX NAZWAINDEKSU ON NAZWATABELI(NAZWAKOLUMNY1, NAZWAKOLUMNY2)
````

Unikalne - zakładane na te kolumny w których wartości są unikalne. Umożliwiają stosowanie <b>unique scan</b>.
````
CREATE UNIQUE INDEX NAZWAINDEKSU ON NAZWATABELI(NAZWAKOLUMNY)
````



