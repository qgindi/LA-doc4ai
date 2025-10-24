# Enum `Au.Types.BRFilter`

Used with `Au.Types.ExtMisc.Resize`

```
public enum BRFilter
```

### Fields

| Name | Description |
| --- | --- |
| Bicubic | Produces image similar to `Graphics.DrawImage` with `InterpolationMode.HighQualityBicubic`. |
| CatmullRom | Produces slightly sharper image (less blurry) than `Graphics.DrawImage` with `InterpolationMode.HighQualityBicubic`. |
| Lanczos3 | Produces sharper image (less blurry) than `Graphics.DrawImage` with `InterpolationMode.HighQualityBicubic`. |