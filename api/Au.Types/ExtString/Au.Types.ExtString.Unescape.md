# Method `Au.Types.ExtString.Unescape`

## Overload 1

Replaces C# escape sequences to characters in this string.

```
public static bool Unescape(this string t, out string result)
```

##### Parameters

- *t*  (`string`):
    This string.
- *result*  (`string`):
    Receives the result string. It is this string if there are no escape sequences or if failed.

##### Returns

`bool`

`false` if the string contains an invalid or unsupported escape sequence.

#### Remarks

Supports all escape sequences of `Au.Types.ExtString.Escape`: `\\`, `\"`, `\t`, `\n`, `\r`, `\0`, `\uXXXX`. Does not support `\a`, `\b`, `\f`, `\v`, `\e`, `\'`, `\xXXXX`, `\UXXXXXXXX`.

* * *

## Overload 2

Replaces C# escape sequences to characters in this string.

```
public static string Unescape(this string t)
```

##### Parameters

- *t*  (`string`):
    This string.

##### Returns

`string`

New string if replaced, else this string. Does not replace if the string does not contain escape sequences or if some escape sequences are invalid or unsupported.

#### Remarks

Supports all escape sequences of `Au.Types.ExtString.Escape`: `\\`, `\"`, `\t`, `\n`, `\r`, `\0`, `\uXXXX`. Does not support `\a`, `\b`, `\f`, `\v`, `\e`, `\'`, `\xXXXX`, `\UXXXXXXXX`.