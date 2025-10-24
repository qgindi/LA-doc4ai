# Method `Au.Types.ExtWpf.RemoveColumn`

## Overload 1

Removes column and adjusts column indices of children that are in other columns.

```
public static void RemoveColumn(this Grid t, int index, bool removeChildren)
```

##### Parameters

- *t*  (`Grid`)
- *index*  (`int`)
- *removeChildren*  (`bool`):
    Remove children that are in that column.

* * *

## Overload 2

Removes a child element and its column from this grid. Adjusts column indices of children that are in other columns.

```
public static void RemoveColumn(this Grid t, UIElement e, bool removeOtherElements)
```

##### Parameters

- *t*  (`Grid`)
- *e*  (`UIElement`)
- *removeOtherElements*  (`bool`):
    Also remove other elements that are in that column.