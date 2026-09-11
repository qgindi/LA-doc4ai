# Method `Au.More.MouseCursor.GetCurrentVisibleCursor`

Gets current global mouse cursor.

```csharp
public static bool GetCurrentVisibleCursor(out nint cursor)
```

##### Parameters

- *cursor*  (`nint`):
  Receives native handle. Don't destroy.

##### Returns

`bool`

`false` if cursor is hidden.