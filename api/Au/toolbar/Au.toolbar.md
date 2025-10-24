# Class `Au.toolbar`

Floating toolbar. Can be attached to windows of other programs.

```
public class toolbar : MTBase
```

##### Remarks

To create toolbar code can be used menu **TT > New toolbar**.

Not thread-safe. All functions must be called from the same thread that created the `Au.toolbar` object, except where documented otherwise. Note: item actions by default run in other threads; see `Au.Types.MTBase.ActionThread`.

##### Inheritance

`object` → `Au.Types.MTBase` → `toolbar`

### Constructors

`toolbar(string, TBCtor, string, int, string, string)`

### Properties

`Anchor`, `AutoSize`, `AutoSizeWrapWidth`, `Background`, `Border`, `BorderColor`, `DisplayText`, `DpiScaling`, `FirstTime`, `Font`, `Hidden`, `Hwnd`, `IsOpen`, `IsOwned`, `this[string, MTImage, int, string]`, `Items`, `Last`, `Layout`, `MaximizedWindowTopPlus`, `Metrics`, `MiscFlags`, `Name`, `NoContextMenu`, `NoDefaultImage`, `Offsets`, `OwnerWindow`, `Satellite`, `SatelliteOwner`, `Sizable`, `Size`, `TextColor`, `Transparency`, `defaultMetrics`

### Methods

`Add`, `AutoHide`, `AutoHideScreenEdge`, `AutoHideScreenEdge`, `Close`, `Group`, `Hide`, `Menu`, `Menu`, `Separator`, `Show`, `Show`, `Show`, `Show`, `ToString`, `find`, `getSettingsFilePath`, `toolbarsDialog`

### Events

`Closed`

### Members inherited from other types of this library
`MTBase.ExtractIconPathFromCode`, `MTBase.ActionThread`, `MTBase.ActionException`, `MTBase.PathInTooltip`, `MTBase.ImageSize`