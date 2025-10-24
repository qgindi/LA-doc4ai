# Class `Au.sqlite`

A SQLite database connection. Creates/opens/closes database file or in-memory database. Executes SQL, etc.

```
public class sqlite : IDisposable
```

##### Remarks

This class wraps a SQLite API object `sqlite3*` and related `sqlite3_x` functions. They are documented in the SQLite website.

To correctly close the database file, at first need to dispose all child objects, such as `Au.sqliteStatement`, then dispose the `sqlite` object. To dispose a static `sqlite` variable, you may want to use `Au.process.thisProcessExit` event. Although this class has a finalizer that disposes the object (closes database), you should always dispose explicitly. Finalizers don't run on process exit.

##### Examples

```
//open database file
using var db = new sqlite(@"C:\test\sqlite.db");
//create table
db.Execute("CREATE TABLE IF NOT EXISTS test(id INTEGER PRIMARY KEY, name TEXT, x INT, guid BLOB, array BLOB)");

//add 2 rows of data
using(var trans = db.Transaction()) { //optional, but makes much faster when making multiple changes, and ensures that all or none of these changes are written to the database
	using(var p = db.Statement("INSERT OR REPLACE INTO test VALUES(?, ?, :x, ?, ?)")) {
		//assume we want to add values of these variables to the database table
		int id = 1; string name = "TEXT"; long x = -10; Guid guid = Guid.NewGuid(); int[] arr = new int[] { 1, 2, 3 };
		//add first row
		p.Bind(1, id);
		p.Bind(2, name).BindStruct(4, guid).Bind(5, arr);
		p.Bind(":x", x);
		p.Step();
		//add second row
		p.Reset().Bind(1, 2).Bind(":x", 123456789012345).Step(); //unbound columns are null
	}
	//update single row
	db.Execute("UPDATE test SET name=?2 WHERE id=?1", 2, "two");
	//write all this to database
	trans.Commit();
}

//get data
using(var p = db.Statement("SELECT * FROM test")) {
	while(p.Step()) { //for each row of results
		print.it(p.GetInt(0), p.GetText(1), p.GetLong(2));
		print.it(p.GetStruct<Guid>("guid"));
		print.it(p.GetArray<int>("array"));
		print.it("----");
	}
}
//get single value
if(db.Get(out string s1, "SELECT name FROM test WHERE id=?", 1)) print.it(s1); else print.it("not found");
if(db.Get(out int i1, "PRAGMA page_size")) print.it(i1);
```

##### Inheritance

`object` → `sqlite`

### Constructors

`sqlite(string, SLFlags, string)`

### Properties

`Changes`, `Handle`, `IsInTransaction`, `LastInsertRowid`

### Methods

`Any`, `Dispose`, `Dispose`, `Execute`, `Execute`, `Execute`, `Get`, `Get`, `Get`, `Get`, `Get`, `GetStruct<T>`, `Get<T>`, `Get<T>`, `Statement`, `Statement`, `TableExists`, `Transaction`

### Operators

`implicit operator nint(sqlite)`

### See Also

`Au.sqliteStatement`