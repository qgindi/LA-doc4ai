# Property `Au.Types.MTBase.ExtractIconPathFromCode`

Extract file path or script path from item action code (for example `Au.run.it` or `Au.script.run` argument) and use icon of that file or script. This property is applied to items added afterwards; submenus inherit it.

```
public bool ExtractIconPathFromCode { get; set; }
```

##### Property Value

`bool`

Default: `Au.toolbar` `true`, `Au.popupMenu` with *name* `true`, `Au.popupMenu` without *name* `false`.

#### Remarks

Gets path from code that contains a string like `@"c:\windows\system32\notepad.exe"` or `@"%folders.System%\notepad.exe"` or URL/shell or `@"\folder\script.cs"`. Also supports code patterns like `folders.System + "notepad.exe"`, `folders.shell.RecycleBin`.

If extracts path, also in the context menu adds item **Find file** which selects the file in Explorer or **Open script** which opens the script in editor.