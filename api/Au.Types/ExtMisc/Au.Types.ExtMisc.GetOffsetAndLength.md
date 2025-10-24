# Method `Au.Types.ExtMisc.GetOffsetAndLength`

If this is `null`, returns `(0, length)`. Else calls `System.Range.GetOffsetAndLength`.

```
public static (int Offset, int Length) GetOffsetAndLength(this Range? t, int length)
```

##### Parameters

- *t*  (`Range?`)
- *length*  (`int`)

##### Returns

`(int start, int end)`

##### Exceptions

- `ArgumentOutOfRangeException`