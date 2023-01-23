# tietokannat_K2023
Koulutehtäviä

mysql> CREATE TABLE pet(name VARCHAR(20),
    -> owner VARCHAR(20),
    -> species VARCHAR(20),
    -> sex CHAR(1),
    -> birth date,
    -> death date);

mysql> INSERT INTO PET VALUES( 'Whistler','Gwen','bird',NULL,'1997-12-09',NULL);

+----------+--------+---------+------+------------+------------+
| name     | owner  | species | sex  | birth      | death      |
+----------+--------+---------+------+------------+------------+
| Fluffy   | Harold | cat     | f    | 1993-02-04 | NULL       |
| Claws    | Gwen   | cat     | m    | 1994-03-17 | NULL       |
| Buffy    | Harold | dog     | f    | 1989-05-13 | NULL       |
| Fang     | Benny  | dog     | m    | 1990-08-27 | NULL       |
| Bowser   | Diane  | dog     | m    | 1979-08-31 | 1995-07-29 |
| Chirpy   | Gwen   | bird    | f    | 1998-09-11 | NULL       |
| Whistler | Gwen   | bird    | NULL | 1997-12-09 | NULL       |
| Slim     | Benny  | snake   | m    | 1996-04-29 | NULL       |
+----------+--------+---------+------+------------+------------+

1.
mysql> DELETE FROM pet where name='Puffball';
mysql> UPDATE pet SET birth = '1998-08-31' WHERE name = 'Bowser';
mysql> UPDATE pet SET death = '2000-09-15' WHERE name = 'Chirpy';
mysql> SELECT * FROM pet WHERE birth >= '1990-01-01' ;
mysql> SELECT * FROM pet WHERE sex = 'm' ;
SELECT name FROM pet WHERE sex = 'm' AND species = 'dog'
SELECT name, owner FROM pet WHERE sex = 'm' AND species = 'dog'

2. 
mysql> SELECT owner FROM pet;
mysql> SELECT name FROM pet ORDER BY name ASC;
mysql> SELECT name, species FROM pet WHERE death IS NULL;
mysql> SELECT owner FROM pet WHERE owner LIKE 'H%'
mysql> SELECT name, species FROM pet WHERE name LIKE '%ff%';
mysql> SELECT name, species FROM pet WHERE LENGTH(name) = 4;
