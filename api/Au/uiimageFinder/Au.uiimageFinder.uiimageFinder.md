# Constructor of `Au.uiimageFinder`

Stores image/color data and search settings in this object. Loads images if need. See `Au.uiimage.find`.

```
public uiimageFinder(IFImage image, IFFlags flags = 0, int diff = 0, Func<uiimage, IFAlso> also = null)
```

##### Parameters

- *image*  (`Au.Types.IFImage`):
    Image or color to find. Or array of them. More info: `Au.Types.IFImage`.
- *flags*  (`Au.Types.IFFlags`)
- *diff*  (`int`):
    Maximal allowed color difference. Can be 0 - 100, but should be as small as possible. Use to find images with slightly different colors than the specified image.
- *also*  (`Func<Au.uiimage, Au.Types.IFAlso>`):

    Callback function. Called for each found image instance and receives its rectangle, match index and list index. Can return one of `Au.Types.IFAlso` values. 
Examples:

    - Skip 2 matching images: `also: o => o.Skip(2)`
    - Skip some matching images if some condition is `false`: `also: o => condition ? IFAlso.OkReturn : IFAlso.FindOther`
    - Get rectangles etc of all matching images: `also: o => { list.Add(o); return IFAlso.OkFindMore; }`
    - Do different actions depending on which list images found: `var found = new BitArray(images.Length); uiimage.find(w, images, also: o => { found[o.ListIndex] = true; return IFAlso.OkFindMoreOfList; }); if(found[0]) print.it(0); if(found[1]) print.it(1);`

##### Exceptions

- `ArgumentException`:
    An argument is/contains a `null`/invalid value.
- `FileNotFoundException`:
    Image file does not exist.
- `Exception`:
    Exceptions of `Au.More.ImageUtil.LoadGdipBitmap`.