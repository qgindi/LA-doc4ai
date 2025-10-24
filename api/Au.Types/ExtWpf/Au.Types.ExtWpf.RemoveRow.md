# Method `Au.Types.ExtWpf.RemoveRow`

## Overload 1

Removes row and adjusts row indices of children that are in other rows.

```
public static void RemoveRow(this Grid t, int index, bool removeChildren)
```

##### Parameters

- *t*  (`Grid`)
- *index*  (`int`)
- *removeChildren*  (`bool`):
    Remove children that are in that row.

* * *

## Overload 2

Removes a child element and its row from this grid. Adjusts row indices of children that are in other rows.

```
public static void RemoveRow(this Grid t, UIElement e, bool removeOtherElements)
```

##### Parameters

- *t*  (`Grid`)
- *e*  (`UIElement`)
- *removeOtherElements*  (`bool`):
    Also remove other elements that are in that row.