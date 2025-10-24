# Method `Au.icon.trayIcon`

## Overload 1

Gets icon of tray icon size from unmanaged resources of this program or system.

```
public static icon trayIcon(int resourceId = 32512)
```

##### Parameters

- *resourceId*  (`int`):
    Native resource id. Default `IDI_APPLICATION` (C# compilers add app icon with this id).

##### Returns

`Au.icon`

#### Remarks

Calls API `LoadIconMetric`.

The icon can be in main assembly (if role `miniProgram`) or in the program file (`.exe`). If not found, loads standard icon, see API `LoadIconMetric`.

* * *

## Overload 2

Loads icon of tray icon size from `.ico` file.

```
public static icon trayIcon(string icoFile)
```

##### Parameters

- *icoFile*  (`string`)

##### Returns

`Au.icon`

`null` if not found.

#### Remarks

Calls API `LoadIconMetric`.