# Method `Au.More.FastBuffer<T>.GetStringFindLength`

Finds length of `'\0'`-terminated UTF-16 string in buffer and converts to C# string. This function can be used when `T` is `char`. Use when length is unknown.

```
public string GetStringFindLength()
```

##### Returns

`string`

#### Remarks

If there is no `'\0'` character, gets whole buffer, and the string probably is truncated.