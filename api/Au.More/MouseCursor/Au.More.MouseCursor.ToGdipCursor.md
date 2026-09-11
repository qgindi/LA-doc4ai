# Method `Au.More.MouseCursor.ToGdipCursor`

Creates `System.Windows.Forms.Cursor` object that shares native cursor handle with this object.

```csharp
public Cursor ToGdipCursor()
```

##### Returns

`Cursor`

`null` if `Au.More.MouseCursor.Handle` is `default(IntPtr)`.