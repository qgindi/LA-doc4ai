# Method `Au.pathname.getNameNoExt`

Gets filename without extension.

```
public static string getNameNoExt(string path)
```

##### Parameters

- *path*  (`string`):
    Path or filename (then just removes extension). Can be `null`.

##### Returns

`string`

Returns `""` if there is no filename. Returns `null` if *path* is `null`.

#### Remarks

The same as `Au.pathname.getName`, just removes extension. Similar to `System.IO.Path.GetFileNameWithoutExtension`. Some differences: if ends with `'\\'` or `'/'`, gets part before it, eg `"B"` from `@"C:\A\B\"`.

Supports separators `'\\'` and `'/'`. Also supports URL and shell parsing names like `@"::{CLSID-1}\0\::{CLSID-2}"`.

Examples:

| *path* | result |
| --- | --- |
| `@"C:\A\B\file.txt"` | `"file"` |
| `"file.txt"` | `"file"` |
| `"file"` | `"file"` |
| `@"C:\A\B"` | `"B"` |
| `@"C:\A\B\"` | `"B"` |
| `@"C:\A\B.B\"` | `"B.B"` |
| `@"C:\aa\file.txt:alt.stream"` | `"file.txt:alt"` |
| `"http://a.b.c"` | `"a.b"` |