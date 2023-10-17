1 - SELECT * FROM students WHERE date_of_birth LIKE '1990-%';
2 - SELECT * FROM courses WHERE cfu > 10;
3 - SELECT * FROM students WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURRENT_DATE) > 30;
4 - SELECT * FROM courses WHERE period LIKE 'I %' AND year = 1;