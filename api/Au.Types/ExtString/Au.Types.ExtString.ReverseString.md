# Method `Au.Types.ExtString.ReverseString`

Reverses this string, like `"Abc"` -> `"cbA"`.

```
public static string ReverseString(this string t, bool raw)
```

##### Parameters

- *t*  (`string`)
- *raw*  (`bool`):
    Ignore `char` sequences such as Unicode surrogates and grapheme clusters. Faster, but if the string contains these sequences, the result string is incorrect.

##### Returns

`string`

The result string.