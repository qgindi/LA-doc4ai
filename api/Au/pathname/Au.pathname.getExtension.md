# Method `Au.pathname.getExtension`

## Overload 1

Gets filename extension, like `".txt"`.

```
public static string getExtension(string path)
```

##### Parameters

- *path*  (`string`):
    Path or filename. Can be `null`.

##### Returns

`string`

Returns `""` if there is no extension. Returns `null` if *path* is `null`.

#### Remarks

Supports separators `'\\'` and `'/'`.

* * *

## Overload 2

Gets filename extension and path part without the extension. More info: `Au.pathname.getExtension(string)`.

```
public static string getExtension(string path, out string pathWithoutExtension)
```

##### Parameters

- *path*  (`string`):
    Path or filename. Can be `null`.
- *pathWithoutExtension*  (`string`):
    Receives path part without the extension. Can be the same variable as *path*.

##### Returns

`string`