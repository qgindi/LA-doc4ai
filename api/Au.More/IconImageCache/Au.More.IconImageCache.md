# Class `Au.More.IconImageCache`

Gets images as `System.Drawing.Bitmap` of same logical size to be displayed as icons. Can get file icons or load images from files etc.

```
public sealed class IconImageCache : IDisposable
```

##### Remarks

Uses memory cache and optionally file cache to avoid loading same image multiple times. Getting images from cache is much faster.

`Bitmap` objects retrieved by this class are stored in memory cache. Don't dispose them before disposing the `IconImageCache` object. Usually don't need to dispose these `Bitmap` objects explicitly (GC will do it).

Thread-safe.

##### Inheritance

`object` → `IconImageCache`

### Constructors

`IconImageCache(int, string)`

### Properties

`Common`, `ImageSize`

### Methods

`Clear`, `ClearAll`, `CommonOfSize`, `Dispose`, `Get`

### Events

`Cleared`