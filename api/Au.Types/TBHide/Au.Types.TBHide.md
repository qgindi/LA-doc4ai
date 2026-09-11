# Enum `Au.Types.TBHide`

Reasons to hide a toolbar. Used with `Au.toolbar.Hide`.

```csharp
[Flags]
public enum TBHide
```

## Fields

### `FullScreen`

A full-screen window is active. See flag `Au.Types.TBFlags.HideWhenFullScreen`.

### `Owner`

Owner window is hidden, minimized, etc.

### `User`

This and bigger flag values can be used by callers for any purpose. Value 0x10000.