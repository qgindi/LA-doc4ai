# Method `Au.Types.TreeBase<T>.Descendants`

Gets all descendant nodes (direct children, their children and so on).

```
public IEnumerable<T> Descendants(bool andSelf = false, Func<T, bool> stepInto = null)
```

##### Parameters

- *andSelf*  (`bool`):
    Include this node. Default `false`.
- *stepInto*  (`Func<T, bool>`):
    If not `null`, called for each descendant node that has children. Let it return `false` to skip descendants of that node.

##### Returns

`IEnumerable<T>`