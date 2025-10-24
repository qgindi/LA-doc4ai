# Method `Au.More.WndUtil.GetClassLong`

Calls API `GetClassLongPtr`.

```
public static nint GetClassLong(wnd w, int index)
```

##### Parameters

- *w*  (`Au.wnd`)
- *index*  (`int`)

##### Returns

`nint`

#### Remarks

Supports `Au.lastError`. For *index* can be used constants from `Au.Types.GCL`. All values are the same in 32-bit and 64-bit process. In 32-bit process actually calls `GetClassLong`, because `GetClassLongPtr` is unavailable.