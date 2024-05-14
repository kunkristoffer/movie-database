// Use DBML to define your database structure
// Docs: https://dbml.dbdiagram.io/docs

Table actor {
  act_id interger [primary key]
  act_fname char(20)
  act_lname char(20)
  act_gender char(1)
}

Table genres {
  gen_id integer [primary key]
  gen_title char(20)
}

Table director {
  dir_id integer [primary key]
  dir_fname char(20)
  dir_lname char(20)
}

Table movie {
  mov_id integer [primary key]
  mov_title char(50)
  mov_year integer
  mov_time integer
  mov_lang char(50)
  mov_dt_rel date
  mov_rel_country char(5)
}

Table movie_genres {
  mov_id integer
  gen_id integer
}

Table movie_directors {
  dir_id integer
  mov_id integer
}

Table reviewer {
  rev_id integer [primary key]
  rev_name char(30)
}

Table rating {
  mov_id integer
  rev_id integer
  rev_stars integer
  num_o_ratings integer
}

Table  movie_cast {
  act_id integer
  mov_id integer
  role char(30)
}

Ref: movie_cast.act_id > actor.act_id
Ref: movie_cast.mov_id > movie.mov_id
Ref: movie_directors.dir_id > director.dir_id
Ref: movie_directors.mov_id > movie.mov_id
Ref: movie_genres.mov_id > movie.mov_id
Ref: movie_genres.gen_id > genres.gen_id
Ref: rating.mov_id > movie.mov_id
Ref: rating.rev_id > reviewer.rev_id


