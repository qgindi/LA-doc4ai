# Method `Au.Types.IOcrEngine.GetBitmapData`

Gets image pixels.

```
protected static byte[] GetBitmapData(Bitmap b)
```

##### Parameters

- *b*  (`Bitmap`)

##### Returns

`byte[]`

#### Remarks

The pixel format is either `Format32bppRgb` (if it's *b* format) or `Format32bppArgb`.