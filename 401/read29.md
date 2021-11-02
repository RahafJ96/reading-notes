# Room

## [Saving data with Room](https://developer.android.com/training/data-storage/room)
- Is like when to cache data so that when the device cannot access the network, the user can still browse that content while they are offline.

- With room we use SQL queries.


### Setup
- To use Room in your app, add the following dependencies to your app's build.gradle file:

```
dependencies {
    def room_version = "2.3.0"

    implementation "androidx.room:room-runtime:$room_version"
    annotationProcessor "androidx.room:room-compiler:$room_version"

    // optional - RxJava2 support for Room
    implementation "androidx.room:room-rxjava2:$room_version"

    // optional - RxJava3 support for Room
    implementation "androidx.room:room-rxjava3:$room_version"

    // optional - Guava support for Room, including Optional and ListenableFuture
    implementation "androidx.room:room-guava:$room_version"

    // optional - Test helpers
    testImplementation "androidx.room:room-testing:$room_version"

    // optional - Paging 3 Integration
    implementation "androidx.room:room-paging:2.4.0-alpha04"
}
```

### Primary components
- **The three major components in Room:**
1. The database class that holds the database and serves as the main access point for the underlying connection to your app's persisted data.
2. Data entities that represent tables in your app's database.
3. Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.

### Sample implementation

1. **Data entity**
```java
@Entity
public class User {
    @PrimaryKey
    public int uid;

    @ColumnInfo(name = "first_name")
    public String firstName;

    @ColumnInfo(name = "last_name")
    public String lastName;
}
```
2. **Data access object (DAO)**

```java
@Dao
public interface UserDao {
    @Query("SELECT * FROM user")
    List<User> getAll();

    @Query("SELECT * FROM user WHERE uid IN (:userIds)")
    List<User> loadAllByIds(int[] userIds);

    @Query("SELECT * FROM user WHERE first_name LIKE :first AND " +
           "last_name LIKE :last LIMIT 1")
    User findByName(String first, String last);

    @Insert
    void insertAll(User... users);

    @Delete
    void delete(User user);
}
```

3. **Database**
DataBase class must be like this:

```java
@Database(entities = {User.class}, version = 1)
public abstract class AppDatabase extends RoomDatabase {
    public abstract UserDao userDao();
}
```

## [Defining entities in Room](https://developer.android.com/training/data-storage/room/defining-data)
- Room entities to define your database schema(table), 
and each instance of an entity represents a row of data in the corresponding table.

```java
@Entity(tableName = "users")
public class User {
    @PrimaryKey
    public int id;

    @ColumnInfo(name = "first_name")
    public String firstName;

    @ColumnInfo(name = "last_name")
    public String lastName;
}
```

### Define a composite primary key

```java
@Entity(primaryKeys = {"firstName", "lastName"})
public class User {
    public String firstName;
    public String lastName;
}
```

### Ignore fields

```java
@Entity
public class User {
    @PrimaryKey
    public int id;

    public String firstName;

    @Ignore
    Bitmap picture;
}
```
OR
```java
@Entity(ignoredColumns = "picture")
public class RemoteUser extends User {
    @PrimaryKey
    public int id;

    public boolean hasVpn;
}
```


## [Related entities in Room](https://developer.android.com/training/data-storage/room/relationships)
### Create embedded objects
- use the @Embedded annotation to represent an object that you'd like to decompose into its subfields within a table. 

```java
public class Address {
    public String street;
    public String state;
    public String city;

    @ColumnInfo(name = "post_code") public int postCode;
}

@Entity
public class User {
    @PrimaryKey public int id;

    public String firstName;

    @Embedded public Address address;
}
```

### Define one-to-one relationships
```java
public class UserAndLibrary {
    @Embedded public User user;
    @Relation(
         parentColumn = "userId",
         entityColumn = "userOwnerId"
    )
    public Library library;
}
}
```

### Define one-to-many relationships

```java
public class UserWithPlaylists {
    @Embedded public User user;
    @Relation(
         parentColumn = "userId",
         entityColumn = "userCreatorId"
    )
    public List<Playlist> playlists;
}
```
```java
@Transaction
@Query("SELECT * FROM User")
public List<UserWithPlaylists> getUsersWithPlaylists();
```
### Define many-to-many relationships

```java
public class PlaylistWithSongs {
    @Embedded public Playlist playlist;
    @Relation(
         parentColumn = "playlistId",
         entityColumn = "songId",
         associateBy = @Junction(PlaylistSongCrossref.class)
    )
    public List<Song> songs;
}

public class SongWithPlaylists {
    @Embedded public Song song;
    @Relation(
         parentColumn = "songId",
         entityColumn = "playlistId",
         associateBy = @Junction(PlaylistSongCrossref.class)
    )
    public List<Playlist> playlists;
}
```

```java
@Transaction
@Query("SELECT * FROM Playlist")
public List<PlaylistWithSongs> getPlaylistsWithSongs();

@Transaction
@Query("SELECT * FROM Song")
public List<SongWithPlaylists> getSongsWithPlaylists();
```

### Define nested relationships
```java
@Entity
public class User {
    @PrimaryKey public long userId;
    public String name;
    public int age;
}

@Entity
public class Playlist {
    @PrimaryKey public long playlistId;
    public long userCreatorId;
    public String playlistName;
}
@Entity
public class Song {
    @PrimaryKey public long songId;
    public String songName;
    public String artist;
}

@Entity(primaryKeys = {"playlistId", "songId"})
public class PlaylistSongCrossRef {
    public long playlistId;
    public long songId;
}
```
```java
public class PlaylistWithSongs {
    @Embedded public Playlist playlist;
    @Relation(
         parentColumn = "playlistId",
         entityColumn = "songId",
         associateBy = Junction(PlaylistSongCrossRef.class)
    )
    public List<Song> songs;
}
```
```java
public class UserWithPlaylistsAndSongs {
    @Embedded public User user;
    @Relation(
        entity = Playlist.class,
        parentColumn = "userId",
        entityColumn = "userCreatorId"
    )
    public List<PlaylistWithSongs> playlists;
}
```
```java
@Transaction
@Query("SELECT * FROM User")
public List<UserWithPlaylistsAndSongs> getUsersWithPlaylistsAndSongs();
```

## [Accessing data with Room](https://developer.android.com/training/data-storage/room/accessing-data#java)

- DAOs make it easier for you to mock database access when you test your app.

### Anatomy of a DAO

- You can define each DAO as either an **interface** or an **abstract** class. 

- The following code is an example of a simple DAO that defines methods for inserting, deleting, and selecting User objects in a Room database:

```java
@Dao
public interface UserDao {
    @Insert
    void insertAll(User... users);

    @Delete
    void delete(User user);

    @Query("SELECT * FROM user")
    List<User> getAll();
}
```

- **There are two types of DAO methods that define database interactions:**

1. Convenience methods that let you insert, update, and delete rows in your database without writing any SQL code.
2. Query methods that let you write your own SQL query to interact with the database.

### Convenience methods

Room provides convenience annotations for defining methods that perform simple **inserts**, **updates**, and **deletes** without requiring you to write a SQL statement.

- **for more complex inserts, updates, or deletes, or if you need to query the data in the database, use a query method instead.**

- The **@Insert** annotation allows you to define methods that insert their parameters into the appropriate table in the database. 

- The **@Update** annotation allows you to define methods that update specific rows in a database table. 

- The **@Delete** annotation allows you to define methods that delete specific rows from a database table.

### Query methods
- The **@Query** annotation allows you to write SQL statements and expose them as DAO methods. 

#### Simple queries


```java
@Query("SELECT * FROM user")
public User[] loadAllUsers();

//And 

@Query("SELECT first_name, last_name FROM user")
public List<NameTuple> loadFullName();

```

#### Pass simple parameters to a query
```java
@Query("SELECT * FROM user WHERE age > :minAge")
public User[] loadAllUsersOlderThan(int minAge);

//And

@Query("SELECT * FROM user WHERE age BETWEEN :minAge AND :maxAge")
public User[] loadAllUsersBetweenAges(int minAge, int maxAge);

@Query("SELECT * FROM user WHERE first_name LIKE :search " +
       "OR last_name LIKE :search")
public List<User> findUserWithName(String search);
```

#### Pass simple parameters to a query
```java
@Query("SELECT * FROM user WHERE region IN (:regions)")
public List<User> loadUsersFromRegions(List<String> regions);
```

#### Query multiple tables
```java
@Query("SELECT * FROM book " +
       "INNER JOIN loan ON loan.book_id = book.id " +
       "INNER JOIN user ON user.id = loan.user_id " +
       "WHERE user.name LIKE :userName")
public List<Book> findBooksBorrowedByNameSync(String userName);
```