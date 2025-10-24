# Property `Au.Types.TreeBase<T>.Previous`

Gets previous sibling node, or `null` if none.

```
public T Previous { get; }
```

##### Property Value

`T`

#### Remarks

Can be slow if there are many siblings. This class does not have a "previous" field and therefore has to walk the linked list of siblings.