# Method `Au.wpfBuilder.Skip`

Adds one or more empty cells in current row of current grid.

```
public wpfBuilder Skip(int span = 1)
```

##### Parameters

- *span*  (`int`):
    Column count.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    In non-grid panel.

#### Remarks

Actually just changes column index where next element will be added.