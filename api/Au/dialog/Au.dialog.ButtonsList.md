# Method `Au.dialog.ButtonsList`

Sets custom buttons to be displayed as a list.

```
public dialog ButtonsList(Strings buttons = default, bool asCommandLinks = true)
```

##### Parameters

- *buttons*  (`Au.Types.Strings`):
    List of button names. Can be string like `"One|Two|..."` or `string[]` or `List<string>`. Button ids will be 1, 2, ... . Default button will be 1, unless changed with `Au.dialog.Default`. Unlike `Au.dialog.Buttons`, this function does not allow to specify button ids; also all specified buttons will be custom buttons, even if named like `"OK"`.
- *asCommandLinks*  (`bool`):
    The style of custom buttons. If `false` - row of classic buttons. If `true` - column of command-link buttons that can have multiline text.

##### Returns

`Au.dialog`

#### Remarks

You can call `Au.dialog.Buttons` too, to add common buttons (like **OK**, **Cancel**); use negative button ids. Both functions set the style (classic or command link) of custom buttons; wins the one called last.