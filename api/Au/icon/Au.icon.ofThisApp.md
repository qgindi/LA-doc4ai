# Method `Au.icon.ofThisApp`

Gets icon from unmanaged resources of this program.

```
public static icon ofThisApp(int size = 16, int resourceId = 32512)
```

##### Parameters

- *size*  (`int`):
    Icon width and height. Default 16.
- *resourceId*  (`int`):
    Native resource id. Default `IDI_APPLICATION` (C# compilers add app icon with this id).

##### Returns

`Au.icon`

`null` if not found.

#### Remarks

If role `miniProgram` (default), at first looks in main assembly (`.dll`); if not found there, looks in `.exe` file. Else only in `.exe` file.

The icon is cached and protected from destroying. Don't need to destroy it, and not error to do it.