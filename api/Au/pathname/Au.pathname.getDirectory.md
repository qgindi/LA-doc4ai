# Method `Au.pathname.getDirectory`

Removes filename part from *path*. By default also removes separator (`'\\'` or `'/'`) if it is not after drive name (eg `"C:"`).

```
public static string getDirectory(string path, bool withSeparator = false)
```

##### Parameters

- *path*  (`string`):
    Path or filename. Can be `null`.
- *withSeparator*  (`bool`):
    Don't remove separator character(s) (`'\\'` or `'/'`). See examples.

##### Returns

`string`

Returns `""` if the string is a filename. Returns `null` if the string is `null` or a root (like `@"C:\"` or `"C:"` or `@"\\server\share"` or `"http:"`).

#### Remarks

Similar to `System.IO.Path.GetDirectoryName`. Some differences: skips `'\\'` or `'/'` at the end (eg from `@"C:\A\B\"` gets `@"C:\A"`, not `@"C:\A\B"`); does not replace `'/'` with `'\\'`.

Parses raw string. You may want to `Au.pathname.normalize` it at first.

Supports separators `'\\'` and `'/'`. Also supports URL and shell parsing names like `@"::{CLSID-1}\0\::{CLSID-2}"`.

Examples:

| *path* | result |
| --- | --- |
| `@"C:\A\B\file.txt"` | `@"C:\A\B"` |
| `"file.txt"` | `""` |
| `@"C:\A\B\"` | `@"C:\A"` |
| `@"C:\A\/B\/"` | `@"C:\A"` |
| `@"C:\"` | `null` |
| `@"\\network\share"` | `null` |
| `"http:"` | `null` |
| `@"C:\aa\file.txt:alt.stream"` | `"C:\aa"` |
| `"http://a.b.c"` | `"http:"` |
| `"::{A}\::{B}"` | `"::{A}"` |
| `""` | `""` |
| `null` | `null` |

Examples when *withSeparator* `true`:

| *path* | result |
| --- | --- |
| `@"C:\A\B"` | `@"C:\A\"` (not `@"C:\A"`) |
| `"http://x.y"` | `"http://"` (not `"http:"`) |