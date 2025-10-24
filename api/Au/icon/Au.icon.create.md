# Method `Au.icon.create`

Creates icon at run time.

```
public static icon create(int width, int height, Action<Graphics> drawCallback = null)
```

##### Parameters

- *width*  (`int`)
- *height*  (`int`)
- *drawCallback*  (`Action<Graphics>`):
    Called to draw icon. If `null`, the icon will be completely transparent.

##### Returns

`Au.icon`