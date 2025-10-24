# Method `Au.pathname.getName`

Gets filename from *path*. Does not remove extension.

```
public static string getName(string path)
```

##### Parameters

- *path*  (`string`):
    Path or filename. Can be `null`.

##### Returns

`string`

Returns `""` if there is no filename. Returns `null` if *path* is `null`.

#### Remarks

Similar to `System.IO.Path.GetFileName`. Some differences: if ends with `'\\'` or `'/'`, gets part before it, eg `"B"` from `@"C:\A\B\"`.

Supports separators `'\\'` and `'/'`. Also supports URL and shell parsing names like `@"::{CLSID-1}\0\::{CLSID-2}"`.

Examples:

| *path* | result |
| --- | --- |
| `@"C:\A\B\file.txt"` | `"file.txt"` |
| `"file.txt"` | `"file.txt"` |
| `"file"` | `"file"` |
| `@"C:\A\B"` | `"B"` |
| `@"C:\A\B\"` | `"B"` |
| `@"C:\A\/B\/"` | `"B"` |
| `@"C:\"` | `""` |
| `@"C:"` | `""` |
| `@"\\network\share"` | `"share"` |
| `@"C:\aa\file.txt:alt.stream"` | `"file.txt:alt.stream"` |
| `"http://a.b.c"` | `"a.b.c"` |
| `"::{A}\::{B}"` | `"::{B}"` |
| `""` | `""` |
| `null` | `null` |