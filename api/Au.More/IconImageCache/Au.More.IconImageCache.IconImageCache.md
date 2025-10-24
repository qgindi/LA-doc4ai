# Constructor of `Au.More.IconImageCache`

```
public IconImageCache(int imageSize = 16, string directory = null)
```

##### Parameters

- *imageSize*  (`int`):
    Width and height of images. Min 16, max 256.
- *directory*  (`string`):
    Path of cache directory. If `null`, will be used only memory cache.

##### Exceptions

- `ArgumentException`:
    Not full path.