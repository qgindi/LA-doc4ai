# Method `Au.Types.TreeBase<T>.Ancestors`

Gets ancestor nodes. The order is from this node towards the root node.

```
public IEnumerable<T> Ancestors(bool andSelf = false, bool noRoot = false)
```

##### Parameters

- *andSelf*  (`bool`):
    Include this node.
- *noRoot*  (`bool`):
    Don't include `Au.Types.TreeBase<T>.RootAncestor`.

##### Returns

`IEnumerable<T>`