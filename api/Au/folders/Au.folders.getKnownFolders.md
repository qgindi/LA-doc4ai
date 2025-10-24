# Method `Au.folders.getKnownFolders`

Gets canonical names and paths of all known folders, including custom known folders registered by applications. These names can be used with `Au.folders.getFolder`.

```
public static Dictionary<string, string> getKnownFolders()
```

##### Returns

`Dictionary<string, string>`

#### Remarks

Paths of virtual and unavailable folders are returned as `"<virtual>"` and `"<unavailable>"`.