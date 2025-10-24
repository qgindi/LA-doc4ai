# Method `Au.elm.fromMouse`

Gets UI element from mouse cursor (pointer) position.

```
public static elm fromMouse(EXYFlags flags = 0)
```

##### Parameters

- *flags*  (`Au.Types.EXYFlags`)

##### Returns

`Au.elm`

##### Exceptions

- `Au.Types.AuException`:
    Failed. For example, window of a higher [UAC](../articles/UAC.html) integrity level process.

#### Remarks

Uses API `AccessibleObjectFromPoint`.