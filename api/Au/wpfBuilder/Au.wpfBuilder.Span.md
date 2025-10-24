# Method `Au.wpfBuilder.Span`

Sets column span of the last added element.

```
public wpfBuilder Span(int columns)
```

##### Parameters

- *columns*  (`int`):
    Column count. If -1 or too many, will span all remaining columns in current row. If 0, will share 1 column with next element added in current row; to set element positions use `Au.wpfBuilder.Margin`, `Au.wpfBuilder.Width` and `Au.wpfBuilder.Align`; see also `Au.wpfBuilder.And`.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    In non-grid panel.