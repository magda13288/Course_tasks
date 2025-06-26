Skorzystaj z bazy `simple_library.db`

---

1. Podaj listę wszystkich książek w bibliotece
SELECT DISTINCT(Title) FRom simple_library ORDER By title;

2. Podaj listę książek napisanych przez Stanisława Lema
SELECT DISTINCT(Title), author_surname FRom simple_library WHERE author_surname = 'Lem' ORDER By title;

3. Podaj listę książek zarejestrowanych w 2015 r.

SELECT DISTINCT(title), author_surname, registration_date FROM simple_library 
WHERE registration_date = '2015' 
ORDER By title;

4. Oblicz liczbę książek w bibliotece

SELECT COUNT(ID) FROM simple_library;

5. Oblicz, ilu różnych autorów stworzyło książki przechowywane w bibliotece

SELECT COUNT(DISTINCT(author_surname)) AS liczba_autorow FROM simple_library;

6. Dla każdego autora oblicz liczbę egzemplarzy książek przechowywanych w bibliotece

SELECT Author_surname, COUNT(Title) FROM simple_library GROUP BY Author_surname;

7. Oblicz liczbę książek starszych niż 10 lat



8. Dla każdego autora podaj liczbę tytułów przez niego napisanych

