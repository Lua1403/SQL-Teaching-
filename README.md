# SQL-Teaching-
1. SELETC all rows from family members
   ```
   SELECT *
   FROM family_members

2. Can you return just the name and species columns?
   ```
   SELECT name, species
   FROM family_members

3. Can you run a query that returns all of the rows that refer to dogs?
   ```
   SELECT *
   FROM family_members
   WHERE species = 'dog'

4. Can you run return all rows of family members whose num_books_read is greater than 190?
   ```
   SELECT *
   FROM family_members
   WHERE num_books_read > 190

5. Can you return all rows in family_members where num_books_read is a value greater or equal to 180?
   ```
   SELECT *
   FROM family_members
   WHERE num_books_read >= 180

6. Can you find all of Pickles' friends that are dogs and under the height of 45cm?
   ```
   SELECT *
   FROM Friends_Of_Pickles
   Where species = 'dog' AND height_cm < 45
   ```
7. Can you find all of Pickles' friends that are dogs or under the height of 45cm?
   ``` 
   SELECT *
   FROM Friends_Of_Pickles
   WHERE species = 'dog' OR height_cm < 45
   ```
8. Can you run a query that would return the rows that are not cats or dogs?
   ```
   SELECT *
   FROM friends_of_pickles
   WHERE species NOT IN ('cat', 'dog')
   ```
9. Can you return a list of the distinct species of animals greater than 50cm in height?
   ```
   SELECT DISTINCT species
   FROM friends_of_pickles
   WHERE height_cm > 50
   ```
10. Can you run a query that sorts the friends_of_pickles by height_cm in descending order?
    ```
    SELECT * 
    FROM friends_of_pickles 
    ORDER BY height_cm DESC
    ```
11. Can you return the single row (and all columns) of the tallest friends_of_pickles?
    ```
    SELECT *
    FROM friends_of_pickles
    ORDER BY height_cm DESC LIMIT 1
    ```
12. returns the total number of rows in the table friends_of_pickles.
    ```
    SELECT COUNT (*)
    FROM friends_of_pickles
    ```
13. Can you return the number of rows in friends_of_pickles where the species is a dog?
    ```
    SELECT COUNT (*)
    FROM friends_of_pickles
    WHERE species = 'dog'
    ```
14. Can you find the total num_books_read made by this family?
    ```
    SELECT SUM (num_books_read)
    FROM family_members
    ```
15. Can you find the average num_books_read made by each family member?
    ```
    SELECT AVG (num_books_read)
    FROM family_members
    ```
16. Can you find the highest num_books_read that a family member makes?
    ```
    SELECT MAX (num_books_read)
    FROM family_members
    ```
17. Can you return the tallest height for each species? Remember to return the species name next to the height too, like in the example query.
    ```
    SELECT MAX (height_cm), species
    FROM friends_of_pickles 
    GROUP BY species
    ```
 18. Can you return the family members that have the highest num_books_read?
     ```
     SELECT *
     FROM family_members
     WHERE num_books_read = (SELECT MAX(num_books_read)
     FROM family_members)
     ```
19. Can you return all of the rows of family_members where favorite_book is not null?
    ```
    SELECT *
    FROM family_members
    WHERE favorite_book IS NOT NULL
    ```
20. Can you return a list of celebrities that were born after September 1st, 1980?
    ```
    SELECT *
    FROM celebs_born
    WHERE birthdate > '1980-09-01'
    ```
21. Can you use an inner join to pair each character name with the actor who plays them? Select the columns: character.name, character_actor.actor_name
    ```
    
    ```
     
