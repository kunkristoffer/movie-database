# movie-database
Group project in SQL @ kodehode.

## Schema Structure
![Alt text](assets/visualization.jpg?raw=true "Visualization of projects schema structure")

## Assignment tasks
- [x] Create the database and tables according to instructions and image given
- [x] Insert the data given in excel/csv file in to respective tables
####
- [x] From Movie Table, write a SQL query to find the name and year of the movies. Return movie title, movie release year.
- [x] From Movie Table, write a SQL query to find when the movie 'American Beauty' released. Return movie release year.
- [x] From Movie Table, write a SQL query to find the movie that was released in 1999. Return movie title.
- [ ] From Movie Table, write a SQL query to find those movies, which were released before 1998. Return movie title.
- [ ] From Movie Table & Reviewer table, write a SQL query to find the name of all reviewers and movies together in a single list.
- [ ] From Rating Table & Reviewer table, write a SQL query to find all reviewers who have rated seven or more stars to their rating. Return reviewer name.
- [ ] From Rating Table & Movie table, write a SQL query to find the movies without any rating. Return movie title.
- [ ] From Movie Table, write a SQL query to find the movies with ID 905 or 907 or 917. Return movie title.
- [ ] From Movie Table, write a SQL query to find the movie titles that contain the word 'Boogie Nights'. Sort the result-set in ascending order by movie year. Return movie ID, movie title and movie release year.
- [ ] From actor Table, write a SQL query to find those actors with the first name 'Woody' and the last name 'Allen'. Return actor ID.

## Self-imposed challenges
- [ ] Incorporate C# with Linq (@Jorgen)
  - [ ] Create a gui to access data
  - [ ] Support crud operations
- [ ] ~~ Parse excel/csv file for automatic import/export ~~


## Assesment criteria
Work in the group to create the tables and answering the queries. So that everyone in the group create same kind of tables.
You can maintain your own document to save the queries which you answered. Try to answer these queries by next class.

## Todo's & links
- https://learn.microsoft.com/en-us/dotnet/csharp/linq/
- https://learn.microsoft.com/en-us/dotnet/api/system.data.sqlclient?view=net-8.0
- https://www.w3schools.com/sql/sql_join.asp

CREATE TABLE movie (
  mov_id integer NOT NULL,
  mov_title char(50) NOT NULL,
  mov_year integer NOT NULL,
  mov_time integer NOT NULL,
  mov_lang char(50) NOT NULL,
  mov_dt_rel date NOT NULL,
  mov_rel_country char(5) NOT NULL,
  PRIMARY KEY (mov_id)
)