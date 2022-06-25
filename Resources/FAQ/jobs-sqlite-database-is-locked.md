# FAQ - The database file is locked

<topMenu>

---

## org.sqlite.SQLiteException: \[SQLITE_BUSY\] The database file is locked (database is locked)

SQLite is just a library that reads and writes to a regular file, not a full SQL database. Therefore, sqlite3 databases can be busy or locked when used by an existing long query, another query that's hanging, or when another plugin is already using it (it is a bad practice to use multiple connections when connecting to SQLite). You can try restarting the server or /stop it, copying the original .db file to a new one, backing up your .db file, deleting the original and then renaming the copy to the original name and starting the server again.

Reading threads might not be closing. Or maybe the Jobs plugin doesn't properly close after insert/update queries. You could consider trying to move to the MySQL database type.

More info about [sqlite3/locking](http://www.sqlite.org/draft/matrix/lockingv3.html)

