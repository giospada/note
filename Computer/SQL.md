---
tags: [Computer]
title: SQL
created: '2020-04-04T20:09:21.253Z'
modified: '2020-05-30T17:01:48.867Z'
---

  
# SQL Notes

## Source: http://techcitynews.com/2013/10/24/why-you-should-learn-some-sql/ 

"Once you can write SQL there are literally no questions you cannot ask of your data."

"When you use SQL to ask questions of a database that you control you can ask any question you want."

**Basic exmaple:**

A simple query that gives me a list of users and their sign in accounts:

```
select email, name, nickname, sign_in_count from people
order by sign_in_count desc limit 200
```

## Source: http://www.sqlteaching.com/

**Create table:**

**Inner joins:**

Say we start with three tables - character, character_tv_show and character_actor.

To get each character name with his/her TV show name, we can write:

```
SELECT character.name, character_tv_show.tv_show_name
FROM character 
INNER JOIN character_tv_show
ON character.id = character_tv_show.character_id;
```
The above puts together every row in character with the corresponding row in character_tv_show, or vice versa.

This next inner join pairs each character name with the actor who plays them:

```
SELECT character.name, character_actor.actor_name
FROM character 
INNER JOIN character_actor
ON character.id = character_actor.character_id;
```
```
name	actor_name
Doogie Howser	Neil Patrick Harris
Barney Stinson	Neil Patrick Harris
Lily Aldrin	Alyson Hannigan
Willow Rosenberg	Alyson Hannigan

```

**Left joins:**

An inner join can only return rows where there is data for both the character name and the actor.

Sometimes you may want to get all of the character names, even if there isn't corresponding data for the actor.

A left join returns all data from the first, or left table, and puts NULL in columns where there is no data from the right table.

Using left joins between character names and TV shows would look like this:

```
SELECT character.name, tv_show.name
FROM character 
LEFT JOIN character_tv_show
ON character.id = character_tv_show.character_id
LEFT JOIN tv_show
ON character_tv_show.tv_show_id = tv_show.id; 

```

The below uses a left join to match character names with the actors they play them:

```
SELECT character.name, actor.name
FROM character
LEFT JOIN character_actor
ON character.id =  character_actor.character_id
LEFT JOIN actor
ON character_actor.actor_id = actor.id

```
```
name	name
Doogie Howser	Neil Patrick Harris
Barney Stinson	Neil Patrick Harris
Lily Aldrin	Alyson Hannigan
Willow Rosenberg	Alyson Hannigan
Steve Urkel	null
Homer Simpson	null
```

**Group by:**

Example table:

```
friends_of_pickles
id	name	gender	species	height_cm
1	Dave	male	human	180
2	Mary	female	human	160
3	Fry	male	cat	30
4	Leela	female	cat	25
5	Odie	male	dog	40
6	Jumpy	male	dog	35
7	Sneakers	male	dog	55
```

This query returns the number of rows for each species:
```
SELECT COUNT(*), species FROM friends_of_pickles GROUP BY species
```

A note on COUNT: You can specify which columns you want to count, if some columns have nothing in them the count is different, which is why count(*) is common because it just counts all the rows in the table. For example you could do COUNT(name) or COUNT(id) and they would return different results if not all table rows had a name.

This query return the tallest height for each species:
```
SELECT MAX(height_cm), species FROM friends_of_pickles GROUP BY species
```

Other GROUP BY functions include SUM, AVG,and MIN.

**Order by:**

ORDER BY is used to sort the rows by an attribute.

For example, to sort the friends_of_pickles table by name:

```
SELECT * FROM friends_of_pickles ORDER BY name;
```

adding DESC at the end of the query would put them in descending order.

The below query sorts the same table by height_cm in descending order:

```
SELECT * FROM friends_of_pickles ORDER BY height_cm DESC
```

## Source: Code School http://campus.codeschool.com/courses/try-sql/contents

### Level 1

**1.1  Introducing SQL**

The columns are the first place to look inside the database.

Next is to search by row.

We search the columns from left to right, and then the rows from top to bottom.

**1.10 SQL Language:**

SQL is written in statements that ask the database to perform many things.

SQL talks to the database.

The browser sends out a request which is the SQL code, This code goes to the database, the databse sends the result back to SQl, and then SQL sends it back to the browser.

Note all SQL statements must have a semi colon at the end to complete the statement.

```
SELECT ___ - the column or columns to be searched
FROM ____; the table the data is in
```

Say for example we want to do the following things:

- Retreive a list of all movie titles

```
SELECT title
FROM movies;
```

- Retrieve all movies and all of their infomation

```
SELECT id, title, genre, duration
FROM movies;
```

OR, use the asterisk to select all columns

```
SELECT * 
FROM movies;
```

The above retreives all matching data as if we had listed out all of the columns.

- Retreive the title of the movie with id 2

```
SELECT title
FROM movies
WHERE id = 2;
```

- Retreive all movies with title The Kid

```
SELECT *
FROM movies
WHERE title = 'The Kid';
```

**1.19 Guiding Data Criteria:**

- Retrieve the title of the movies sorted by duration

```
SELECT title
FROM movies
ORDER BY duration;
```

The film titles are then returned in ascending order, lowest to highest.

To return in descending order we can do the following:

```
SELECT title
FROM movies
ORDER BY duration DESC;
```

- Find films which have a duration of more than 100 minutes

To do this, we use multiple comparison fields in the WHERE statement.

```
SELECT ___
FROM ___
WHERE ___ > ___;
```

Selects all records from movies table where the duration is longer than 100 minutes:

```
SELECT *
FROM movies
WHERE duration > 100;
```

- Films which do not have a genre of horror

```
SELECT *
FROM movies
WHERE genre <> 'Horror';
```

- All records which have both an id of 1 and a genre of comedy


```
SELECT ___
FROM ___
WHERE ___
AND ___;
```
```
SELECT title
FROM movies
WHERE id = 1
AND genre = 'Comedy';
```

In the above example, both the WHERE and the AND conditions must be met.

- Movies where id is 1 or genre is comedy

```
SELECT ___
FROM ___
WHERE ___
OR ___;
```
```
SELECT title
FROM movies
WHERE id = 1
OR genre = 'Comedy';

```

In the above example, either the WHERE or the OR criteria can be met to return results.

Statements written in the challenges:

```
SELECT id, title
FROM movies
WHERE duration >= 86
AND genre = 'Horror'
ORDER BY duration;
```

```
SELECT item, price, size
FROM concessions
WHERE item = 'Popcorn'
OR item = 'Soda'
ORDER BY price DESC;
```

### Level 2

**2.1: Adding data**

- Adding a fifth record to the movies table
```
INSERT INTO movies (id, title, genre, duration)
VALUES (5, 'The Circus', 'Comedy', 71);
```

Note this can also be done without entering the column names, if all fields are being entered:

```
INSERT INTO movies 
VALUES (5, 'The Circus', 'Comedy', 71);
```

Note that we don't have to inset into every column:

```
INSERT INTO movies (id, title)
VALUES (5, 'The Circus');
```

```
INSERT INTO movies (title, duratiojn)
VALUES ('The Fly', 80);
```

In the above example, the id gets set, even though we didn't set it.

This is because the id column is acting as our primary key. It is unique. This field will never be blank or empty.

SQL automatically increments the primary key for a table when a new record is inserted into the table.

So the id, being the primary key, will be automaically incremented each time a new record is inserted into the table.

A NULL value is used to represent a field with missing or unknown data. 

SQL statemenets from the challenges:

```
INSERT INTO concessions (item, size)
VALUES ('Nachos', 'Regular');

INSERT INTO concessions (item, price, id)
VALUES ('Pizza', '2.00', 8);
```

**2.8: Changing current data**

- Changing the genre 

```
UPDATE ____ - the table the data is in
SET ___ = ___ - the column to be changed followed by the column name, the value needed to change the column to 
(WHERE clause) - optional, condition to help indicate where the change will take place
```

Example:

```
UPDATE movies
SET genre = 'Romance'
WHERE id = 5;
```

- Changing multiple columns within a row

For example:

```
UPDATE movies
SET genre = 'Romance', duration = 70
WHERE id = 5;
```

- Making mutiple changes to different rows at the same time

```
UPDATE movies 
SET genre = 'Romance'
WHERE id = 3 OR id = 5;
```

In the challenges:

```
UPDATE concessions
SET price = 1.00
WHERE item = 'Popcorn'
OR item = 'Candy';
```

**2.15: Removing data**

DELETE recipe

```
DELETE FROM ___ (WHERE clause);
```
```
DELTE FROM movies WHERE id = 5;
```
```
DELETE FROM movies WHERE duration < 100;
```

Note: If we did not use the where clause in DELETE, it would have removed all records of movies from the database.

Some more delete statements from the challenges:

```
DELETE FROM movies
WHERE genre = 'Comedy';

DELETE FROM movies
WHERE duration > 120 
OR title = 'Nosferatu';
```

### Level 3

**Creating and removing databases and tables**

- Create new database with four tables

```
CREATE DATABASE _____; - the name of the database
```

```
CREATE DATABASE Chaplin Theatres;
```

- Remove a database, or dropping a databse 

```
DROP DATABASE _____;
```
```
DROP DATABASE Chaplin Theatres;
```

This would completely remove hte Chaplin Theatres database.

- Create table inside newly created database

```
CREATE TABLE ____
(
column_name1 datatype,
column_name2 datatype,
column_name3 datatype,
);
```

From the spreadsheet, we can see four columns of data.

Each column has a different type of data.

The id column is numbers, so the type can be int.

```
CREATE TABLE movies
(
id int,
title varchar(50), - varchar means letters or numbers and no longer than 50 characters
genre varchar(15), 
duration int,
);
```

- Remove a table from the database

```
DROP TABLE _____;
```
```
DROP TABLE movies;
```

From the challenges:

varchar(10) would best relate to a price field

```
CREATE TABLE advertisements 
(
  id int,
	ad_type varchar(20),
  mode varchar(20),
  number int
);

INSERT INTO advertisements
VALUES (1, 'Poster', 'Paper', 20);
```

```
UPDATE advertisements
SET category = 'Television'
WHERE name = 'Commercial';

DROP TABLE advertisements;
```

**3.7: Manipulating Tables**

- The ALTER TABLE command is used to add, modify and remove columns in a table.

```
ALTER TABLE ____ - table name 
ADD COLUMN ______ ______; - column name, data type of new column 
```

```
ALTER TABLE movies
ADD COLUMN ratings int;
```

- Adding some data to the ratings column

```
UPDATE movies
SET ratings = 8
WHERE title = 'Don Juan';
```

The new ratings column now has some data.

- Removing a column from a table 

```
ALTER TABLE movies
DROP COLUMN ratings;
```

From the challenges:

```
ALTER TABLE concessions
ADD COLUMN inventory int;

UPDATE concessions
SET inventory = 100
WHERE item = 'Candy'
OR item = 'Hot Dog';

ALTER TABLE concessions
ALTER COLUMN inventory 
TYPE varchar(10);

UPDATE concessions
SET inventory = 'Full'
WHERE item = 'Popcorn';

UPDATE concessions
SET inventory = 'Half'
WHERE item = 'Soda';

UPDATE concessions
SET inventory = 'Empty'
WHERE item = 'Hot Dog'
OR item = 'Candy';

ALTER TABLE concessions
DROP COLUMN inventory;

```

**Link to CodeSchool slides: http://courseware.codeschool.com/try_sql/trysql-slides.pdf**

## Source - http://www.w3schools.com/sql/sql_join_left.asp

**Left joins:**

The LEFT JOIN keyword returns all rows from the left table (table1), with the matching rows in the right table (table2). The result is NULL in the right side when there is no match.

Syntax:

```
SELECT column_name(s)
FROM table1
LEFT JOIN table2
ON table1.column_name=table2.column_name;
```

The following SQL statement will return all customers, and any orders they might have:

```
SELECT Customers.CustomerName, Orders.OrderID
FROM Customers
LEFT JOIN Orders
ON Customers.CustomerID=Orders.CustomerID
ORDER BY Customers.CustomerName;
```

**Postgres:**

postgres can keep lots of different databases at the same time

so connect to your database with psql, then do \l

it lists all the databases

you can connect to a specific database by typing: \c <database name>

CREATE DATABASE dbname;

will create you a new database

then you can "connect" to it with \c <dbname>

you can list all available databases with \l (lowercase L)

oh \d tablename shows one table

if you are half-way through a statement it uses the -# prompt to let you know

ctrl c to escape back to ansa=#

SELECT * 
FROM tablename;

to show the entire contents of the table

## Source: http://sqlzoo.net/wiki/SQL_Tutorial

### Select basics 

```
SELECT name, gdp/population FROM world
 WHERE area > 50000
 
SELECT name, continent FROM world
 WHERE area < 2000
  AND gdp > 5000000

SELECT name, population FROM world
 WHERE name IN ('Finland', 'Norway', 'Sweden')
 
//in allows you to search in a list 

SELECT name FROM world
 WHERE name LIKE 'G%'

//like permits a pattern
//% is the wildcard 
```

### Select name

```
//selecting a name that contains the letter x

SELECT name FROM world
  WHERE name LIKE '%x%'

//select countries that end with land

SELECT name FROM world
  WHERE name LIKE '%land'

//Finds the countries that have "t" as the second character.
SELECT name FROM world
 WHERE name LIKE '_t%'
ORDER BY name

//Finds the countries that have "t" as the third character.
SELECT name FROM world
 WHERE name LIKE '__t%'
ORDER BY name

//Finds the countries that have two "o" characters separated by two others.
SELECT name FROM world
 WHERE name LIKE '%o__o%'

//Finds a country with exactly four characters 
SELECT name FROM world
 WHERE name LIKE '____'
```

### SELECT from WORLD Tutorial

```
SELECT name, population/1000000 FROM world
 WHERE continent = 'South America'
```

### SELECT within SELECT Tutorial

```
//List each country name where the population is larger than 'Russia'.

SELECT name FROM world
  WHERE population >
     (SELECT population FROM world
      WHERE name='Russia')

//Show the countries in Europe with a per capita GDP greater than 'United Kingdom'.
SELECT name FROM world 
 WHERE continent='Europe' AND gdp/population >
  (SELECT gdp/population FROM world
    WHERE name='United Kingdom')


//List the name and continent of countries in the continents containing 'Belize', 'Belgium'.
SELECT name, continent FROM world
 WHERE continent IN
  ((SELECT continent FROM world
   WHERE name='Belize'),
  (SELECT continent FROM world WHERE name='Belgium'))

//Which country has a population that is more than Canada but less than Poland? Show the name and the population.
SELECT name, population FROM world
 WHERE population  > 
  (SELECT population FROM world
   WHERE name='Canada')
  AND population <
   (SELECT population FROM world
    WHERE name='Poland')

//Which countries have a GDP greater than every country in Europe? [Give the name only.] (Some countries may have NULL gdp values)
SELECT name FROM world
  WHERE gdp > ALL
    (SELECT gdp FROM world
        WHERE continent='Europe' 
          AND gdp<>'NULL')

//Find the largest country (by area) in each continent, show the continent, the name and the area:
SELECT continent, name, area FROM world x
  WHERE area >= ALL
    (SELECT area FROM world y
        WHERE y.continent=x.continent
          AND area>0)


//Find the continents where all countries have a population <= 25000000. Then find the names of the countries associated with these continents. Show name, continent and population.//

///The inner query creates a list of populations on the continent it's looking at, this list is checked by the 25000000 >= ALL to see if all of them are less than 25million.///

SELECT name, continent, population FROM world x
WHERE 25000000 >= ALL
   (SELECT population FROM world y
       WHERE y.continent=x.continent)

```

### SUM and COUNT tutorial 

Aggregate functions such as COUNT, SUM and AVG take many values and delivers just one value.

```
//Show the total population of the world.
SELECT SUM(population)
FROM world

//List all the continents - just once each.
SELECT DISTINCT(continent) FROM world

//Give the total GDP of Africa
SELECT SUM(gdp) FROM world WHERE continent = "Africa"

//How many countries have an area of at least 1000000
SELECT COUNT(name) FROM world WHERE area >= 1000000

//What is the total population of ('France','Germany','Spain')
SELECT SUM(population) FROM world WHERE name IN ('France','Germany','Spain')

//For each continent show the continent and number of countries.
SELECT continent, COUNT(name) FROM world GROUP BY continent

//For each continent show the continent and number of countries with populations of at least 10 million.
SELECT continent, COUNT(name) FROM world WHERE population >= 10000000 GROUP BY continent

//List the continents that have a total population of at least 100 million.
SELECT DISTINCT continent FROM world x 
WHERE 100000000 <= (SELECT SUM(y.population) FROM world y WHERE x.continent = y.continent GROUP BY continent)


```

### The JOIN operation
http://sqlzoo.net/wiki/The_JOIN_operation

```
SELECT player,teamid, mdate
  FROM game JOIN goal ON (id=matchid) WHERE teamid='GER'
```

```
SELECT team1, team2, player 
FROM goal 
JOIN game ON (matchid = id) 
WHERE player LIKE 'Mario%'
```

```
SELECT player, teamid, coach, gtime
  FROM goal JOIN eteam ON (teamid=id)
   WHERE gtime<=10
```

```
SELECT mdate, teamname 
FROM game JOIN eteam ON (game.team1 = eteam.id)
WHERE eteam.coach = 'Fernando Santos'
```

```
SELECT player
FROM goal
JOIN game ON (goal.matchid = game.id)
WHERE stadium = 'National Stadium, Warsaw'
```

**More difficult questions:**

returns one too many rows - need to fix:
```
SELECT player
FROM goal
JOIN game ON matchid = id
WHERE ( (goal.teamid != 'GER') AND (game.team1 = 'GER' || game.team2 = 'GER'))

```

  
