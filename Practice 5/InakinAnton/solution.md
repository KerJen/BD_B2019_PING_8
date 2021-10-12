# Янкин Антон Дмитриевич БПИ 191
# Задача 1

1. SELECT Title, PubName FROM Book;
2. SELECT ISBN, MAX(PagesNum) FROM Book;
3. SELECT Author FROM Book GROUP BY Author HAVING count(*) > 5;
4. SELECT * FROM Book WHERE PagesNum > (SELECT AVG(PagesNum) FROM Books) * 2;
5. SELECT DISTINCT c2.name  FROM Category c1 JOIN Category c2 ON c1.ParentCat = c2.CategoryName
6. SELECT Author, COUNT(Author) AS AuthorCount FROM Book GROUP BY Author ORDER BY AuthorCount DESC LIMIT 1;
7. SELECT DISTINCT r.ID, r.LastName, r.FirstName, r.Address, r.BirthDate FROM Reader r, Borrowing br, Book b WHERE b.Author = 'Марк Твен' AND br.ISBN = b.ISBN AND br.ReaderNr = r.ID;
8. SELECT ISBN FROM Copy GROUP BY ISBN HAVING count(*) > 1;
9. SELECT * FROM Book ORDER BY PubYear LIMIT 10;
10. ?

# Задача 2

1. INSERT INTO Borrowing ('ReaderNr', 'ISBN', 'CopyNumber') VALUES('')
2. DELETE FROM Book WHERE PubYear > 2000;
3. UPDATE Borrowing b, BookCat bc SET b.ReturnDate=b.ReturnDate+30 WHERE bc.CategoryName="Базы данных" AND b.ReturnDate > '01/01/2016';

# Задача 3
1. Берет два поля студента, таблицы студентов, у которых нет оценок >= 4
2. Все кредиты профессора, если он проводил лекции, иначе кол-во кредитов будет нулевым
3. Самая высокая оценка большая или равное 4 каждого студента из каждой посещеной ими лекции
