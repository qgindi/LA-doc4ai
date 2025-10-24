# Method `Au.Types.ExtWpf.FindVisualAncestor`

## Overload 1

Calls callback function *f* for each visual ancestor (`System.Windows.Media.VisualTreeHelper.GetParent`), and returns the ancestor for which *f* returns `true`. Also can return *last* or `null`.

```
public static DependencyObject FindVisualAncestor(this DependencyObject t, bool andThis, Func<DependencyObject, bool> f, object last, bool andLast)
```

##### Parameters

- *t*  (`DependencyObject`)
- *andThis*  (`bool`):
    Include this object.
- *f*  (`Func<DependencyObject, bool>`)
- *last*  (`object`):
    When found this ancestor, stop and return *last* if *andLast* `true` or `null` if `false`.
- *andLast*  (`bool`):
    If *last* found, return *last* instead of `null`.

##### Returns

`DependencyObject`

### See Also

`System.Windows.Controls.ItemsControl.ContainerFromElement`

* * *

## Overload 2

Returns the nearest visual ancestor (`System.Windows.Media.VisualTreeHelper.GetParent`) of type *T*. Also can return *last* or `null`.

```
public static DependencyObject FindVisualAncestor<T>(this DependencyObject t, bool andThis, object last, bool andLast) where T : DependencyObject
```

##### Parameters

- *t*  (`DependencyObject`)
- *andThis*  (`bool`):
    Include this object.
- *last*  (`object`):
    When found this ancestor, stop and return *last* if *andLast* `true` or `null` if `false`.
- *andLast*  (`bool`):
    If *last* found, return *last* instead of `null`.

##### Returns

`DependencyObject`

##### Type Parameters

- `T`

### See Also

`System.Windows.Controls.ItemsControl.ContainerFromElement`