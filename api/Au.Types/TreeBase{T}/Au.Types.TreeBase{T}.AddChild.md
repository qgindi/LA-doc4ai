# Method `Au.Types.TreeBase<T>.AddChild`

Adds node *n* to this node as a child.

```
public void AddChild(T n, bool first = false)
```

##### Parameters

- *n*  (`T`)
- *first*  (`bool`):
    Insert *n* as the first child node. If `false` (default), appends to the end.

##### Exceptions

- `ArgumentException`:
    *n* is `null`, or has parent (need to `Au.Types.TreeBase<T>.Remove` at first), or is this node, or an ancestor of this node.