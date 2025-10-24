# Method `Au.Types.TreeBase<T>.AddSibling`

Inserts node *n* before or after this node as a sibling.

```
public void AddSibling(T n, bool after)
```

##### Parameters

- *n*  (`T`)
- *after*  (`bool`):
    Insert *n* after this node. If `false` (default), inserts before this node.

##### Exceptions

- `ArgumentException`:
    See `Au.Types.TreeBase<T>.AddChild`.
- `InvalidOperationException`:
    This node does not have parent (`Au.Types.TreeBase<T>.Parent` is `null`).