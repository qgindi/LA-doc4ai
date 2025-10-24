# Property `Au.toolbar.Metrics`

Sets some metrics of this toolbar, for example button padding.

```
public TBMetrics Metrics { get; set; }
```

##### Property Value

`Au.Types.TBMetrics`

#### Remarks

Cannot be changed after showing toolbar window.

#### Examples

```
t.Metrics = new(4, 2);
```

### See Also

`Au.toolbar.defaultMetrics`