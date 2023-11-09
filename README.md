# MongoDB-Exercise

1.Create a Database called movies.
use movies

 use movies
switched to db movies
movies> 

2.Create a collection called moviedetails..
db.createCollection("moviedetails")

{ ok: 1 }
movies> 




3.Create above 5 movie documents into a moviedetails collection.
movies> db.moviedetails.insertMany([{ "Movie-Title": "Jurassic Park" },{ "Movie-Title": "Forrest Gump" },{ "Movie-Title": "Titanic"},{ "Movie-Title": "The Dark Knight" },{ "Movie-Title": "Avatar" }])

{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("654c7ec3d200188bf7133fa2"),
    '1': ObjectId("654c7ec3d200188bf7133fa3"),
    '2': ObjectId("654c7ec3d200188bf7133fa4"),
    '3': ObjectId("654c7ec3d200188bf7133fa5"),
    '4': ObjectId("654c7ec3d200188bf7133fa6")
  }
}
movies> db.moviedetails.insertMany([{"Genre/Type": "Adventure"},{"Genre/Type": "Drama"},{"Genre/Type": "Romance "},{"Genre/Type":"Action"},{"Genre/Type":"Science Fiction"}])

{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("654c81e7d200188bf7133fb2"),
    '1': ObjectId("654c81e7d200188bf7133fb3"),
    '2': ObjectId("654c81e7d200188bf7133fb4"),
    '3': ObjectId("654c81e7d200188bf7133fb5"),
    '4': ObjectId("654c81e7d200188bf7133fb6")
  }
}

db.moviedetails.insertMany([{"Director": "Steven Spielberg"},{"Director":"Robert Zemeckies"},{"Director":"James Cameron"},{"Director":"Christopher Nolan"},{"Director":"James Cameron"}])

{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("654c85ea8f3a24e34a1ba9b2"),
    '1': ObjectId("654c85ea8f3a24e34a1ba9b3"),
    '2': ObjectId("654c85ea8f3a24e34a1ba9b4"),
    '3': ObjectId("654c85ea8f3a24e34a1ba9b5"),
    '4': ObjectId("654c85ea8f3a24e34a1ba9b6")
  }
}

db.moviedetails.insertMany([{"Release Year":"1993"},{"Release Year":"1994"},{"Release Year":"1997"},{"Release Year":"2008"},{"Release Year":"2009"}])

{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("654c883a8f3a24e34a1ba9b7"),
    '1': ObjectId("654c883b8f3a24e34a1ba9b8"),
    '2': ObjectId("654c883b8f3a24e34a1ba9b9"),
    '3': ObjectId("654c883b8f3a24e34a1ba9ba"),
    '4': ObjectId("654c883b8f3a24e34a1ba9bb")
  }
}


4.List all documents created.
db.moviedetails.find()

[
  {
    _id: ObjectId("654c7ec3d200188bf7133fa2"),
    'Movie-Title': 'Jurassic Park'
  },
  {
    _id: ObjectId("654c7ec3d200188bf7133fa3"),
    'Movie-Title': 'Forrest Gump'
  },
  {
    _id: ObjectId("654c7ec3d200188bf7133fa4"),
    'Movie-Title': 'Titanic'
  },
  {
    _id: ObjectId("654c7ec3d200188bf7133fa5"),
    'Movie-Title': 'The Dark Knight'
  },
  {
    _id: ObjectId("654c7ec3d200188bf7133fa6"),
    'Movie-Title': 'Avatar'
  },
  {
    _id: ObjectId("654c7f0cd200188bf7133fa7"),
    'Movie-Title': 'Jurassic Park'
  },
  {
    _id: ObjectId("654c7f0cd200188bf7133fa8"),
    'Movie-Title': 'Forrest Gump'
  },
  {
    _id: ObjectId("654c7f0cd200188bf7133fa9"),
    'Movie-Title': 'Titanic'
  },
  {
    _id: ObjectId("654c7f0cd200188bf7133faa"),
    'Movie-Title': 'The Dark Knight'
  },
  {
    _id: ObjectId("654c7f0cd200188bf7133fab"),
    'Movie-Title': 'Avatar'
  },
  {
    _id: ObjectId("654c80b6d200188bf7133fac"),
    'Genre/Type': 'Adventure'
  },
  { _id: ObjectId("654c80b6d200188bf7133fad"), 'Genre/Type': 'Drama' },
  {
    _id: ObjectId("654c80b6d200188bf7133fae"),
    'Genre/Type': 'Romance '
  },
  {
    _id: ObjectId("654c80ead200188bf7133faf"),
    'Genre/Type': 'Adventure'
  },
  { _id: ObjectId("654c80ead200188bf7133fb0"), 'Genre/Type': 'Drama' },
  {
    _id: ObjectId("654c80ead200188bf7133fb1"),
    'Genre/Type': 'Romance '
  },
  {
    _id: ObjectId("654c81e7d200188bf7133fb2"),
    'Genre/Type': 'Adventure'
  },
  { _id: ObjectId("654c81e7d200188bf7133fb3"), 'Genre/Type': 'Drama' },
  {
    _id: ObjectId("654c81e7d200188bf7133fb4"),
    'Genre/Type': 'Romance '
  },
  { _id: ObjectId("654c81e7d200188bf7133fb5"), 'Genre/Type': 'Action' }
]
Type "it" for more



5.List James Cameron’s movies.

List  James Cameron’s movies released in 2009.
Delete the movie which you don’t like.
Add the movie which is your favourite. 
List movie Directed  by Christopher Nolan in 1994.
  10.  List out the Director’s Name in your document. 
