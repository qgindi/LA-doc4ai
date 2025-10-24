# Method `Au.icon.winStoreAppImage`

## Overload 1

Gets image of a Windows Store App.

```
public static Bitmap winStoreAppImage(string shellString, int size = 16)
```

##### Parameters

- *shellString*  (`string`):
    String like `@"shell:AppsFolder\Microsoft.WindowsCalculator_8wekyb3d8bbwe!App"`.
- *size*  (`int`):
    Desired width and height.

##### Returns

`Bitmap`

`Bitmap` object, or `null` if failed. Its size may be != *size*; let the caller scale it when drawing.

* * *

## Overload 2

Gets image of a Windows Store App. This overload accepts a `Au.Types.Pidl` instead of a shell string.

```
public static Bitmap winStoreAppImage(Pidl pidl, int size = 16)
```

##### Parameters

- *pidl*  (`Au.Types.Pidl`)
- *size*  (`int`)

##### Returns

`Bitmap`

`Bitmap` object, or `null` if failed. Its size may be != *size*; let the caller scale it when drawing.