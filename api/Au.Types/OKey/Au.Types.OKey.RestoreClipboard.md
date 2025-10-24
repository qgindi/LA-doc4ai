# Property `Au.Types.OKey.RestoreClipboard`

Whether to restore clipboard data when copying or pasting text. Default: `true`. By default restores only text. See also `Au.Types.OKey.RestoreClipboardAllFormats`, `Au.Types.OKey.RestoreClipboardExceptFormats`.

```
public bool RestoreClipboard { get; set; }
```

##### Property Value

`bool`

#### Examples

```
opt.key.RestoreClipboard = true;
```