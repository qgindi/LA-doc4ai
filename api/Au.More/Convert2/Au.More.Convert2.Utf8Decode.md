# Method `Au.More.Convert2.Utf8Decode`

Converts `'\0'`-terminated UTF-8 string to C# string (UTF-16).

```
public static string Utf8Decode(byte* utf8)
```

##### Parameters

- *utf8*  (`byte*`):
    UTF-8 string. If `null`, returns `null`.

##### Returns

`string`

#### Remarks

Finds `'\0'` and calls `System.Text.Encoding.GetString`. Don't use this function when UTF-8 string length is known; call `Encoding.UTF8.GetString` directly.