# Method `Au.Types.TreeBase<T>.AncestorsFromRoot`

Gets ancestor nodes. The order is from the root node towards this node.

```
public T[] AncestorsFromRoot(bool andSelf = false, bool noRoot = false)
```

##### Parameters

- *andSelf*  (`bool`):
    Include this node. Default `false`.
- *noRoot*  (`bool`):
    Don't include `Au.Types.TreeBase<T>.RootAncestor`.

##### Returns

`T[]`