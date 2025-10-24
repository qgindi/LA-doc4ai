# Method `Au.wpfBuilder.BindingContext`

Sets `System.Windows.FrameworkElement.DataContext` property of the last added element. Then with `Au.wpfBuilder.Bind` of this and descendant elements don't need to specify data source object because it is set by this function.

```
public wpfBuilder BindingContext(object source)
```

##### Parameters

- *source*  (`object`):
    Data source object.

##### Returns

`Au.wpfBuilder`