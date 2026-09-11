# Property `Au.toolbar.Metrics`

Sets some metrics of this toolbar, for example button padding.

```csharp
public TBMetrics Metrics { get; set; }
```

##### Property Value

`Au.Types.TBMetrics`

#### Remarks

Cannot be changed after showing toolbar window.

#### Examples

```csharp
t.Metrics = new(4, 2);
```

### See Also

`Au.toolbar.defaultMetrics`