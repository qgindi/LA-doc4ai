# Method `Au.Types.ExtMisc.AsSpan`

Gets a `System.Span<T>` view over the data in a list. Items should not be added or removed from the `System.Collections.Generic.List<T>` while the `System.Span<T>` is in use.

```
public static Span<T> AsSpan<T>(this List<T> t)
```

##### Parameters

- *t*  (`List<T>`)

##### Returns

`Span<T>`

A `System.Span<T>` instance over the `System.Collections.Generic.List<T>`.

##### Type Parameters

- `T`:
    The type of items in the list.