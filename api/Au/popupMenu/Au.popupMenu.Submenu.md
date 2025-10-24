# Method `Au.popupMenu.Submenu`

## Overload 1

Adds menu item that opens a submenu. Used like `m.Submenu("Example", m => { /* add submenu items */ });`.

```
public PMItem Submenu(string text, Action<popupMenu> opening, MTImage image = default, bool disable = false, int l_ = 0, string f_ = null)
```

##### Parameters

- *text*  (`string`):
    Item text. Can include hotkey, tooltip and underlined character, like `"Te&xt\t Hotkey\0 Tooltip"`; more info: `Au.popupMenu`.
- *opening*  (`Action<Au.popupMenu>`):
    Action called whenever opening the submenu and should add items to it.
- *image*  (`Au.Types.MTImage`):
    Item image. Read here: `Au.Types.MTBase`.
- *disable*  (`bool`):
    Disabled state.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.Types.PMItem`

#### Remarks

The submenu is other `Au.popupMenu` object. It inherits many properties of this menu; see property documentation.

#### Examples

```
m.Submenu("Example", m => {
	m["A"] = o => { print.it(o); };
	m["B"] = o => { print.it(o); };
});
```

This code shows dynamically created menu of files in a folder and subfolders. Subfolder files are retrieved when opening the submenu.

```
var m=new popupMenu();
_Dir(m, new DirectoryInfo(@"C:\"));
m.Show();

static void _Dir(popupMenu m, DirectoryInfo dir) {
	foreach (var v in dir.EnumerateFileSystemInfos()) {
		if(v.Attributes.Has(FileAttributes.System|FileAttributes.Hidden)) continue;
		if(v.Attributes.Has(FileAttributes.Directory)) {
			m.Submenu(v.Name, m=> _Dir(m, v as DirectoryInfo));
		} else {
			m[v.Name]=o=>print.it(v.FullName);
		}
		m.Last.File = v.FullName;
	}
}
```

* * *

## Overload 2

Adds menu item that opens a reusable submenu.

```
public PMItem Submenu(string text, Func<popupMenu> opening, MTImage image = default, bool disable = false, int l_ = 0, string f_ = null)
```

##### Parameters

- *text*  (`string`):
    Item text. Can include hotkey, tooltip and underlined character, like `"Te&xt\t Hotkey\0 Tooltip"`; more info: `Au.popupMenu`.
- *opening*  (`Func<Au.popupMenu>`):
    Func called whenever opening the submenu and should return the submenu object. Can return `null`.
- *image*  (`Au.Types.MTImage`):
    Item image. Read here: `Au.Types.MTBase`.
- *disable*  (`bool`):
    Disabled state.
- *l_*  (`int`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)
- *f_*  (`string`):
    [Caller info parameter](../articles/Caller%20info%20parameter.html)

##### Returns

`Au.Types.PMItem`

#### Remarks

The caller creates the submenu (creates the `Au.popupMenu` object and adds items) and can reuse it many times. Other overload does not allow to create `Au.popupMenu` and reuse same object. The submenu does not inherit properties of this menu.

#### Examples

```
var m2 = new popupMenu(); m2.AddCheck("C1"); m2.AddCheck("C2");
m.Submenu("Submenu", () => m2);
```