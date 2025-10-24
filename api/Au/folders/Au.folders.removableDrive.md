# Method `Au.folders.removableDrive`

## Overload 1

Gets removable/external/USB drive path, like `@"F:\"`.

```
public static FolderPath removableDrive(int driveIndex = 0)
```

##### Parameters

- *driveIndex*  (`int`):
    0-based removable drive index.

##### Returns

`Au.Types.FolderPath`

`null` if unavailable.

#### Remarks

Calls `System.IO.DriveInfo.GetDrives` and counts drives of type `System.IO.DriveType.Removable`.

* * *

## Overload 2

Gets removable/external/USB drive name (like `@"F:\"`) by its volume label.

```
public static FolderPath removableDrive(string volumeLabel)
```

##### Parameters

- *volumeLabel*  (`string`):
    Volume label. You can see it in drive **Properties** dialog; it is not the drive name that is displayed in File Explorer.

##### Returns

`Au.Types.FolderPath`

`null` if unavailable.