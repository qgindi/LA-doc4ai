# Property `Au.folders.ThisAppImages`

Gets or sets path of folder "images of this application".

```
public static FolderPath ThisAppImages { get; set; }
```

##### Exceptions

- `InvalidOperationException`:
    Thrown by the `set` function if this property is already set.

##### Property Value

`Au.Types.FolderPath`

#### Remarks

Default is `ThisAppBS + "Images"`.

Used by functions of these classes: `Au.icon`, `Au.popupMenu`, `Au.toolbar`, `Au.uiimage`, possibly some other. This function does not auto-create the folder; usually it is created when installing the application; the script editor does not use and does not install it.