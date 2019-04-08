## Wrapper Class around sqlite3
* In sqlite3 after connecting to the database, for every read execute statement the data needs to be fetched and for evey write execute statement the data needs to be committed. But this class eliminates these requirements and make it simple to read and write to the database.

# Files:
* palsql/__init__.py

## Usage Examples:
* import palsql
* db = palsql.db("db-filename")  ##-connect to the database
* db.read("sql statement")  ##-returns the read data from database
* db.write("sql statement")  ##-writes the data and commits to the database
* db.read("select item from table", flat=False)  ##-returns the raw read data 
* db.read(f"select item from table where item = {Variable}")  ##-read with string substitution
* db.read1("select item from table where id = 1") ##-returns the data for one item

## For other sqlite3 cursor commands use the cursor class
* db.cur.execute(.....)
* db.cur.fetchall()
