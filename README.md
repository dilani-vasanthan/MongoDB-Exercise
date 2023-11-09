# MongoDB-Exercise

**1.Create a Database called movies.**
``use movies

 use movies
switched to db movies
movies> ``

**2.Create a collection called moviedetails**
``db.createCollection("moviedetails")

{ ok: 1 }
movies>`` 




**3.Create above 5 movie documents into a moviedetails collection.**
``movie> db.moviedetails.insertMany([{MovieTitle:"Jurassic Park",GenreType:"Adventure",Director:"Steven Spielberg",ReleaseYear:1993},{MovieTitle:"Forrest Gump",GenreType:"Drama",Director:"Robert Zemeckies",ReleaseYear:1994},{MovieTitle:"Titanic",GenreType:"Romance",Director:"James Cameron",ReleaseYear:1997},{MovieTitle:"The Dark Knight",GenreType:"Action",Director:"Christopher Nolan",ReleaseYear:2008},{MovieTitle:"Avatar",GenreType:"Science Fiction",Director:"James Cameron",ReleaseYear:2009}])

{
  acknowledged: true,
  insertedIds: {
    '0': ObjectId("654c9db67d1937f1690a9255"),
    '1': ObjectId("654c9db67d1937f1690a9256"),
    '2': ObjectId("654c9db67d1937f1690a9257"),
    '3': ObjectId("654c9db67d1937f1690a9258"),
    '4': ObjectId("654c9db67d1937f1690a9259")
  }
}


4.List all documents created.
db.moviedetails.find()

[
  {
    _id: ObjectId("654c9db67d1937f1690a9255"),
    MovieTitle: 'Jurassic Park',
    GenreType: 'Adventure',
    Director: 'Steven Spielberg',
    ReleaseYear: 1993
  },
  {
    _id: ObjectId("654c9db67d1937f1690a9256"),
    MovieTitle: 'Forrest Gump',
    GenreType: 'Drama',
    Director: 'Robert Zemeckies',
    ReleaseYear: 1994
  },
  {
    _id: ObjectId("654c9db67d1937f1690a9257"),
    MovieTitle: 'Titanic',
    GenreType: 'Romance',
    Director: 'James Cameron',
    ReleaseYear: 1997
  },
  {
    _id: ObjectId("654c9db67d1937f1690a9258"),
    MovieTitle: 'The Dark Knight',
    GenreType: 'Action',
    Director: 'Christopher Nolan',
    ReleaseYear: 2008
  },
  {
    _id: ObjectId("654c9db67d1937f1690a9259"),
    MovieTitle: 'Avatar',
    GenreType: 'Science Fiction',
    Director: 'James Cameron',
    ReleaseYear: 2009
  }
]``


**5.List James Cameron’s movies.**
``movie> db.moviedetails.find({Director:"James Cameron"})

[
  {
    _id: ObjectId("654c9db67d1937f1690a9257"),
    MovieTitle: 'Titanic',
    GenreType: 'Romance',
    Director: 'James Cameron',
    ReleaseYear: 1997
  },
  {
    _id: ObjectId("654c9db67d1937f1690a9259"),
    MovieTitle: 'Avatar',
    GenreType: 'Science Fiction',
    Director: 'James Cameron',
    ReleaseYear: 2009
  }
]``


**6.List  James Cameron’s movies released in 2009.**
``movie> db.moviedetails.find({Director:"James Cameron",ReleaseYear:2009})

[
  {
    _id: ObjectId("654c9db67d1937f1690a9259"),
    MovieTitle: 'Avatar',
    GenreType: 'Science Fiction',
    Director: 'James Cameron',
    ReleaseYear: 2009
  }
]``
**7.Delete the movie which you don’t like.**
``movie> db.moviedetails.remove({ MovieTitle:"Avatar" })

DeprecationWarning: Collection.remove() is deprecated. Use deleteOne, deleteMany, findOneAndDelete, or bulkWrite.
{ acknowledged: true, deletedCount: 1 }``


**8.Add the movie which is your favourite.**
``movie> db.collection_name.insertOne({ MovieTitle:"Leo",GenreType:"comedy",Director:"Dilani",ReleaseYear:2022})
{
  acknowledged: true,
  insertedId: ObjectId("654ca2b27d1937f1690a925b")
}``
**9.List movie Directed  by Christopher Nolan in 1994.**
``movie> db.moviedetails.find({Director:"Christopher Nolan",ReleaseYear:2008})
[
  {
    _id: ObjectId("654c9db67d1937f1690a9258"),
    MovieTitle: 'The Dark Knight',
    GenreType: 'Action',
    Director: 'Christopher Nolan',
    ReleaseYear: 2008
  }
]``
 **10.  List out the Director’s Name in your document.**

``movie> db.moviedetails.distinct("Director")
[
  'Christopher Nolan',
  'James Cameron',
  'Robert Zemeckies',
  'Steven Spielberg'
]``

