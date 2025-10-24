# Property `Au.More.FileWatcher.Paused`

When your app writes, creates, deletes, moves or renames the file, it must set this property = `true` during the file operation. It helps to distinguish internal and external changes. Example: `Au.More.FileWatcher`.

```
public bool Paused { get; set; }
```

##### Property Value

`bool`