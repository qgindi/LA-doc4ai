# Property `Au.Types.MTItem.File`

Gets file or script path extracted from item action code (see `Au.Types.MTBase.ExtractIconPathFromCode`) or sets path as it would be extracted.

```
public string File { get; set; }
```

##### Property Value

`string`

#### Remarks

Can be used to set file or script path when it cannot be extracted from action code. When you set this property, the menu/toolbar item uses icon of the specified file, and its context menu contains **Find file** or **Open script**.