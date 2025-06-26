Skorzystaj z bazy `library.db`

---

Dodatkowe informacje:
  
  * maksymalny czas wypożyczenia - 25 dni
  * opłata za każdy dzień zwłoki - 0,50 PLN

---

1. Oblicz liczbę użytkowników biblioteki

SELECT Count(users.ID) AS 'User count' FROm users;

2. Oblicz liczbę użytkowników biblioteki aktywnych w 2018 r.

SELECT Count(user_id) AS 'User count' FROm borrowings WHERE STRFTIME('%Y', borrow_date) = '2018';

3. Podaj listę użytkowników, którzy w 2010 r. pożyczyli więcej niż 3 książki

SELECT COUNT(user_id)
FROM (
    SELECT user_id
    FROM borrowings
    WHERE STRFTIME('%Y', borrow_date) = '2010'
    GROUP BY user_id
    HAVING COUNT(book_id) > 3
) AS filtered_users;


4. Oblicz liczbę książek pożyczonych przez każdego z użytkowników.



5. Oblicz liczbę książek pożyczonych przez każdego z użytkowników w 2017 r.

---

6. Podaj łączną liczbę wypożyczeń każdego egzemplarza
7. Podaj łączną liczbę wypożyczeń każdego tytułu
8. Podaj 10 najpopularniejszych tytułów w 2016 r.

---

9. Podaj listę pozycji (tytuł, ID egzemplarza, imię i nazwisko użytkownika) oddanych po terminie
10. Podaj listę pozycji (tytuł, ID egzemplarza, imię i nazwisko użytkownika, liczba dni) oddanych po terminie
11. Podaj listę pozycji (tytuł, ID egzemplarza, imię i nazwisko użytkownika) nieoddanych

---

12. Podaj 20 najdłużyszych zakończonych wypożyczeń
13. Podaj 10 najdłuższych niezakończonych wypożyczeń

---

14. Oblicz średnią liczbę dni wypożyczenia dla każdego użytkownika
15. Oblicz łączną liczbę dni wypożyczenia ponad termin dla każdego użytkownika
16. Oblicz średnią liczbę dni wypożyczenia ponad termin dla każdego użytkownika

---

17. Podaj 10 tytułów, które średnio są wypożyczane na największą liczbę dni
18. Podaj 10 tytułów, które były najdłużej wypożyczone
19. Podaj 10 tytułów, które były najdłużej wypożyczone (uwzględnij wypożyczenia, które nadaj trwają)

---

20. Oblicz łączną kwotę zapłaconą przez każdego z użytkowników
21. Oblicz łączną kwotę, który każdy użytkownik powinien był zapłacić

~~22. Podaj listę użytkowników zalegających z opłatami~~

~~23. Oblicz dług każdego użytkownika zalegającego z opłatami~~

---

24. Podaj średnią liczbę wypożyczeń egzemplarzy każdego z tytułów
25. Podaj średnią liczbę wypożyczeń tytułów każdego z autorów
26. Podaj średnią liczbę wypożyczeń egzemplarzy każdego z autorów

---

27. Podaj najpopularniejszego autora dla każdego użytkownika
28. Podaj najaktywniejszego użytkownika dla każdego autora

---

29. Podaj listę użytkowników, którzy przez cały okres działalności biblioteki pożyczyli więcej książek niż przeciętny użytkownik
30. Podaj listę użytkowników, którzy w 1995 r. pożyczyli więcej książek niż przeciętny użytkownik
31. Dla każdego użytkownika podaj rok, w którym pożyczył najwięcej książek

---

32. Oblicz dług każdego użytkownika zalegającego z opłatami
