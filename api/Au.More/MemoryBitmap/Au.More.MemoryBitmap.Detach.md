# Method `Au.More.MemoryBitmap.Detach`

Deletes memory DC, clears this variable and returns its bitmap (native bitmap handle). The returned bitmap is not selected into a DC. Will need to delete it with API `DeleteObject`.

```
public nint Detach()
```

##### Returns

`nint`