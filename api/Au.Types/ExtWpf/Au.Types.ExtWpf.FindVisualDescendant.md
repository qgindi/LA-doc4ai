# Method `Au.Types.ExtWpf.FindVisualDescendant`

Enumerates visual descendant objects, including parts of composite controls, and calls callback function *f* for each. When *f* returns `true`, stops and returns that object. Returns `null` if *f* does not return `true`.

```
public static DependencyObject FindVisualDescendant(this DependencyObject t, Func<DependencyObject, bool> f, bool orSelf = false)
```

##### Parameters

- *t*  (`DependencyObject`)
- *f*  (`Func<DependencyObject, bool>`)
- *orSelf*  (`bool`)

##### Returns

`DependencyObject`