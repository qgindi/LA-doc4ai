# Method `Au.elm.fromMouse`

Gets UI element from mouse cursor (pointer) position.

```csharp
public static elm fromMouse(EXYFlags flags = 0)
```

##### Parameters

- *flags*  (`Au.Types.EXYFlags`):
  Enum: NotInProc, UIA, PreferLink, TrySmaller, OrUIA.

##### Returns

`Au.elm`

##### Exceptions

- `Au.Types.AuException`:
  Failed. For example, window of a higher [UAC](🔗) integrity level process.

#### Remarks

Uses API `AccessibleObjectFromPoint`.