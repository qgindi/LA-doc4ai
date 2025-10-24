# Method `Au.filesystem.more.emptyRecycleBin`

Empties the Recycle Bin.

```
public static void emptyRecycleBin(string drive = null, bool progressUI = false)
```

##### Parameters

- *drive*  (`string`):
    If not `null`, empties the Recycle Bin on this drive only. Example: `"D:"`.
- *progressUI*  (`bool`):
    Show progress dialog if slow. Default `true`.