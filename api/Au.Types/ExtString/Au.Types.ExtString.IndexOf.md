# Method `Au.Types.ExtString.IndexOf`

## Overload 1

Finds character *c* in this span, starting from *startIndex*.

```
public static int IndexOf(this ReadOnlySpan<char> t, int startIndex, char c)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *startIndex*  (`int`)
- *c*  (`char`)

##### Returns

`int`

Character index in this span, or -1 if not found.

##### Exceptions

- `ArgumentOutOfRangeException`

* * *

## Overload 2

Finds character *c* in *range* of this span.

```
public static int IndexOf(this ReadOnlySpan<char> t, Range range, char c)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *range*  (`Range`)
- *c*  (`char`)

##### Returns

`int`

Character index in this span, or -1 if not found.

##### Exceptions

- `ArgumentOutOfRangeException`

* * *

## Overload 3

Finds string *s* in this span, starting from *startIndex*.

```
public static int IndexOf(this ReadOnlySpan<char> t, int startIndex, ReadOnlySpan<char> s, bool ignoreCase = false)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *startIndex*  (`int`)
- *s*  (`ReadOnlySpan<char>`)
- *ignoreCase*  (`bool`)

##### Returns

`int`

Character index in this span, or -1 if not found.

##### Exceptions

- `ArgumentOutOfRangeException`
- `ArgumentNullException`:
    *s* is `null`.

* * *

## Overload 4

Finds string *s* in *range* of this span.

```
public static int IndexOf(this ReadOnlySpan<char> t, Range range, ReadOnlySpan<char> s, bool ignoreCase = false)
```

##### Parameters

- *t*  (`ReadOnlySpan<char>`)
- *range*  (`Range`)
- *s*  (`ReadOnlySpan<char>`)
- *ignoreCase*  (`bool`)

##### Returns

`int`

Character index in this span, or -1 if not found.

##### Exceptions

- `ArgumentOutOfRangeException`
- `ArgumentNullException`:
    *s* is `null`.