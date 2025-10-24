# Method `Au.Types.ExtWpf.VisualAncestors`

Gets visual ancestors (`System.Windows.Media.VisualTreeHelper.GetParent`).

```
public static IEnumerable<DependencyObject> VisualAncestors(this DependencyObject t, bool andThis = false, object last = null)
```

##### Parameters

- *t*  (`DependencyObject`)
- *andThis*  (`bool`):
    Include this object.
- *last*  (`object`):
    Last ancestor to get.

##### Returns

`IEnumerable<DependencyObject>`