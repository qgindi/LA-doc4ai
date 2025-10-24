# File read (load), write (save)

There are many ways to read and write files of various formats. Class [File](https://www.google.com/search?q=System.IO.File+class) reads/writes simple text or raw binary data.

```
string file = @"C:\Test\test.txt";
```

Read all text to a string.

```
string text = File.ReadAllText(file);
print.it(text);
```

Read if file exists.

```
string text2 = File.Exists(file) ? File.ReadAllText(file) : null;
```

Write all text from a string.

```
File.WriteAllText(file, text); //creates new file or overwrites existing file
```

Read text lines.

```
string[] lines = File.ReadAllLines(file);
foreach (var s in lines) {
	print.it(s);
}
```

Write text lines from `List`.

```
var a = new List<string>();
for (int i = 1; i <= 10; i++) a.Add("line " + i);
File.WriteAllLines(file, a);
```

Usually text in files is Unicode, encoded as UTF-8 or UTF-16. The `ReadX` functions can read both. The `WriteX` functions write UTF-8 by default. Let's write UTF-16:

```
File.WriteAllText(file, text, Encoding.Unicode);
```

If the file already exists, the `WriteX` functions overwrite (replace) it, else they create new file. The `AppendX` functions append to existing file or create new file.

```
File.AppendAllText(file, "line\r\n"); //append a string

File.AppendAllLines(file, a); //append a list or array
```

Read/write binary (non-text) data.

```
byte[] b = File.ReadAllBytes(file);
File.WriteAllBytes(file, b);
```

All above functions immediately fail if the file is locked at that time (eg an app is writing the file). Also the write functions can corrupt the file in some cases. To read and write in a safer way, use `Au.filesystem` functions.

```
text = filesystem.loadText(file); //waits max 2 s if locked
text = filesystem.waitIfLocked(() => File.ReadAllText(file), 10_000); //waits max 10 s if locked
```

See also `Au.filesystem.saveText` and similar functions. They write in a safer way and can create a backup file.