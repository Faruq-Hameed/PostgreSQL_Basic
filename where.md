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


- Example 3: Using the WHERE clause with the OR operator. Here we will be using the OR operator in the “customer” table of our sample database.
SELECT
    first_name,
    last_name
FROM
    customer
WHERE
    last_name = 'Cooper' OR 
    first_name = 'Jo';


- Example 4: Using the WHERE clause with the IN operator. The IN operator is used for string matching. Here we will be using the IN operator in the “customer” table of our sample database.
SELECT
    first_name,
    last_name
FROM
    customer
WHERE 
    first_name IN ('Kelly', 'Jo', ' Alexander');

- Example 5: Using the WHERE clause with the LIKE operator. The LIKE operator is used to find string matching a particular pattern. Here we will be using the LIKE operator in the “customer” table of our sample database.
SELECT
    first_name,
    last_name
FROM
    customer
WHERE 
    first_name LIKE 'Kath%'; last_name and Last_name that has first_name that conatins 'Kath' will be returned
    

- Example 7: Using the WHERE clause with the not equal operator (<>). Here we will be using the <> operator in the “customer” table of our sample database.
SELECT 
    first_name, 
    last_name
FROM 
    customer 
WHERE 
    first_name LIKE 'Bra%' AND 
    last_name <> 'Motley';