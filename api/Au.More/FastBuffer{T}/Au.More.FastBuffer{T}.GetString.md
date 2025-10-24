# Method `Au.More.FastBuffer<T>.GetString`

Gets API result as string, or allocates bigger buffer if old buffer was too small. This function can be used when `T` is `char`.

```
public bool GetString(int r, out string s, BSFlags flags = 0, string sDefault = null)
```

##### Parameters

- *r*  (`int`):
    The return value of the called Windows API function, if it returns string length or required buffer length. Or you can call `Au.More.FastBuffer<T>.FindStringLength`.
- *s*  (`string`):
    Receives the result string if succeeded, else *sDefault* (default `null`).
- *flags*  (`Au.Types.BSFlags`):

    Use if the API function isn't like this:

    - If succeeds, returns string length without the terminating `'\0'` character.
    - If buffer too small, returns required buffer length.
    - If fails, returns 0.
- *sDefault*  (`string`):
    Set *s* = this string if buffer too small or *r* \< 1 or if the retrieved string == this string (avoid creating new string).

##### Returns

`bool`

If *r* > `Au.More.FastBuffer<T>.n`, calls `More(r);` and returns `false`. Else creates new string of *r* length and returns `true`.