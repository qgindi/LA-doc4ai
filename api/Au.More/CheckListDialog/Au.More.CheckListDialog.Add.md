# Method `Au.More.CheckListDialog.Add`

## Overload 1

Adds a checkbox.

```
public CheckBox Add(string text, bool check = false, string tooltip = null)
```

##### Parameters

- *text*  (`string`)
- *check*  (`bool`)
- *tooltip*  (`string`)

##### Returns

`CheckBox`

The checkbox.

* * *

## Overload 2

Adds multiple checkboxes.

```
public void Add(IEnumerable<string> items, bool check = false)
```

##### Parameters

- *items*  (`IEnumerable<string>`):
    Array, `List`, etc containing text strings for checkboxes.
- *check*  (`bool`):
    Whether to check all checkboxes.