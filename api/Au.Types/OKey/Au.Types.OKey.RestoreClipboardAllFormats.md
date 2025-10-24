# Property `Au.Types.OKey.RestoreClipboardAllFormats`

When copying or pasting text, restore clipboard data of all formats that are possible to restore. Default: `false` - restore only text.

```
public static bool RestoreClipboardAllFormats { get; set; }
```

##### Property Value

`bool`

#### Remarks

Restoring data of all formats set by some apps can be slow or cause problems. More info: `Au.Types.OKey.RestoreClipboardExceptFormats`.

This property is static, not thread-static. It should be set (if need) at the start of script and not changed later.

#### Examples

```
OKey.RestoreClipboardAllFormats = true;
```

### See Also

`Au.Types.OKey.RestoreClipboard`

`Au.Types.OKey.RestoreClipboardExceptFormats`