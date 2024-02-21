### WHERE CLAUSE IN PqSQL
- The PostgreSQL WHERE clause is used to filter results returned by the SELECT statement.
- The condition evaluates to true, false, or unknown. It can either be a Boolean expression or a combination of Boolean expressions where AND and OR operators are used.
- The WHERE clause can also be used with the UPDATE and DELETE statement to specify rows to be updated or deleted.


#### Below table provides us with the list of comparison operators valid in PostgreSQL:
Operator	Description
- =	Equal
- >	Greater than
- <	Less than
- >=	Greater than or equal to
- <=	Less than or equal to
- <> or =!	Not equal
- AND	Logical AND operator
- OR	Logical OR operator

- Example 1: Using WHERE clause with the equal (=) operator. Here we will be using the equal operator in the “customer” table of our sample database.
SELECT
    last_name,
    first_name
FROM
    customer
WHERE
    first_name = 'Kelly';


- Example 2: Using the WHERE clause with the AND operator. Here we will be using the AND operator in the “customer” table of our sample database.
SELECT
    last_name,
    first_name
FROM
    customer
WHERE
    first_name = 'Kelly'
AND last_name = 'Knott';

SELECT
    last_name,
    first_name
FROM
    customer
WHERE
    age between 9 AND 20;