CREATE DATABASE database_name
\c => SQL command to connect to a db
\l => list all db
 drop DATABASE db_name; to delete a database


tables are created inside a specific
database

- Tables are where we stored out data
- the SQL keywords should be optonally
capitalized
- create a table
- table colums are holds the data
- the type of data expected in a 
column should be specified

CREATE TABLE table_name(
colum_name column_data_type
);

e.g
CREATE TABLE table_name(
_id int,
name VARCHAR
);

CREATE TABLE movies(
movie_id int,
movie_name VARCHAR
);

to list all the column in a table together with the data;
SELECT * form table_name;
e.g 
SELECT * from movies;


SELECT A DATA FROM A colum_name

SELECT column_to_select(i.e returned) FROM table_name WHERE colum_identifier(operator e.g =, >)colum_identifier_value;
e.g
SELECT movie_name FROM movies WHERE movie_id= 4; this will return the movie name


drop table tb_name

Adding data into table
- INSERT into table_name(columA, columnB)
VALUES (value_A, value_B);
e.g
INSERT into movies(movie_id,
movie_name) VALUES (3, 'merlin');

- You can choose to write into few columns instead of all

e.g
INSERT into movies(movie_id) VALUES (1)


to see a table description
\d table_name

- UPDATING TABLE
UPDATE table_name SET colum_name_to_be_updated =  new_column_value 
WHERE column_identification_or_row_identificatio =value_of_column_identification_or_row_identificatio ;
e.g
UPDATE movies SET movie_name='good doctor' WHERE movie_id=4;


DELETE FROM A TABLE
DELETE FROM table_name_to_delete_from WHERE colum_name = the_value_of_row_to_delete;
e.g
DELETE FROM movies WHERE movie_id=4; this will delete the record of movie_id=4 from the table