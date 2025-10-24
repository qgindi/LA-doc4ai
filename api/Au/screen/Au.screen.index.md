# Method `Au.screen.index`

Gets screen at the specified index of the `Au.screen.all` array.

```
public static screen index(int index, bool lazy = false)
```

##### Parameters

- *index*  (`int`):
    0-based screen index. Index 0 is the primary screen. If index too big, gets the primary screen.
- *lazy*  (`bool`):
    Create variable with `Au.screen.LazyFunc` that later will get screen handle.

##### Returns

`Au.screen`

##### Exceptions

- `ArgumentOutOfRangeException`:
    Negative *index*.