# Method `Au.wpfBuilder.SpanRows`

Sets row span of the last added element.

```
public wpfBuilder SpanRows(int rows)
```

##### Parameters

- *rows*  (`int`):
    Row count.

##### Returns

`Au.wpfBuilder`

##### Exceptions

- `InvalidOperationException`:
    In non-grid panel.

#### Remarks

In next row(s) use `Au.wpfBuilder.Skip` to skip cells occupied by this element. Often it's better to add a nested panel instead. See `Au.wpfBuilder.StartGrid`.