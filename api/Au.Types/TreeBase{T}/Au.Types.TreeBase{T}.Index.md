# Property `Au.Types.TreeBase<T>.Index`

Returns 0-based index of this node in parent. Returns -1 if no parent.

```
public int Index { get; }
```

##### Property Value

`int`

#### Remarks

Can be slow if there are many siblings. This class does not have an "index" field and therefore has to walk the linked list of siblings.