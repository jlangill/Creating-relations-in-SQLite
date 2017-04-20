# Creating-relations-in-SQLite
Using Python (Jupyter Notebooks) to create relational tables in SQLite
Let's first get everything you need setup.
Import sqlite3 into the environment.
Connect to nominations.db and assign the Connection instance to conn.
Let's now write and run some queries to explore the data.
Return the schema using pragma table_info() and assign to schema.
Return the first 10 rows using the SELECT and LIMIT statements and assign to first_ten.
Since both schema and first_ten are lists, use a for loop to iterate over each element and print each element. This makes our output easier to understand.

Create the ceremonies table with the following schema:
id: integer, primary key.
Year: integer.
Host: text.
Create the list of tuples, years_hosts, that contains the values for the rows we want to insert into the ceremonies table.
Use the Connection method executemany to insert the values into the ceremonies table.
To verify that the ceremonies table was created and populated correctly, run the following queries:
Return the first 10 rows using the SELECT and LIMIT statements.
Return the schema using pragma table_info().

Turn on foreign key constraints by writing and running the following query:
PRAGMA foreign_keys = ON;

Write and run the query to create the nominations_two table with the schema specified above.
Write and run the query we discussed above that returns the records from the nominations table and assign the results set to joined_nominations.
Write a placeholder insert query that can insert values into nominations_two and assign this query to insert_nominations_two. Make sure the ordering of the columns matches the ordering from joined_nominations.
Use the Connection method executemany to insert the records in joined_nominations using the placeholder insert query insert_nominations_two.
Verify your work by returning the first 5 rows from nominations_two.

Write and run the query that deletes the nominations table from the database.
Write and run the query that renames nominations_two to nominations.

Create the 3 tables we need to model the relationship between movies and actors. You need to create the movies and actors tables before creating the movies_actors table for the foreign key references to work.
Create the movies table using the following schema:
id: primary key, integer type.
movie: movie name, text type.
Create the actors table using the following schema:
id: primary key, integer type.
actor: actor's full name, text type.
Create the movies_actors join table using the following schema:
id: primary key, integer type.
movie_id: foreign key reference to movies.id column.
actor_id: foreign key reference to actors.id column.

What other datasets can we add to the database?
Based on what you know, brainstorm how you would populate the join table and the linked tables using data from nominations.
