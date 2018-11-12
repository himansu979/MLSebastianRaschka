#### 1. Connect to sqlite3 database
```
import sqlite3
con = sqlite3.connect("data.db")
cursor = con.cursor()

#### 2. create table users
##create_table = "CREATE TABLE users (id int, username text, password text)"
create_table = "CREATE TABLE IF NOT EXISTS users (id INTEGER PRIMARY KEY, username text, password text)"
cursor.execute(create_table)

#### 3. insert data into the table : execute and executemany()
user = (1, "jose", "asdf")
insert_query = "INSERT INTO users VALUES (?, ?, ?)"
cursor.execute(insert_query, user)

#### 4. insert many entries in a single command
users = [
    (2, "rolf", "asdf"),
    (3, "anne", "xyz"),
    (4, "Himansu", "abc")
]
cursor.executemany(insert_query, users)


#### 5. select query
query = "SELECT * from users"
first_row = result.fetchone()
[i for i in cursor.execute(query)]

#### 6. where keyword
get_name = ("food", )
query2 = "SELECT * FROM users where username=?"
result2 = cursor.execute(query2, get_name)
row2 = result2.fetchone()
print(row2)


con.commit()
con.close()
```

### SQLite3 from command line
```
>sqlite3
SQLite version 3.23.1 2018-04-10 17:39:29
Enter ".help" for usage hints.
Connected to a transient in-memory database.
Use ".open FILENAME" to reopen on a persistent database.

>.databases
>.tables
> select * from users;

>.exit
```


