# Method `Au.Types.TreeBase<T>.IsDescendantOf`

## Overload 1

Returns `true` if this node is a descendant of node *n*.

```csharp
public bool IsDescendantOf(T n)
```

##### Parameters

- *n*  (`T`):
  Can be `null`.

##### Returns

`bool`

* * *

## Overload 2

Returns `true` if this node is a descendant of nearest ancestor node for which *predicate* returns `true`.

```csharp
public bool IsDescendantOf(Func<T, bool> predicate)
```

##### Parameters

- *predicate*  (`Func<T, bool>`)

##### Returns

`bool`