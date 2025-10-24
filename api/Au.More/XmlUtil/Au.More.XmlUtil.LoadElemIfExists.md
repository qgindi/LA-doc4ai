# Method `Au.More.XmlUtil.LoadElemIfExists`

If XML file exists, loads it (calls `Au.More.XmlUtil.LoadElem`), else creates new element or returns `null`.

```
public static XElement LoadElemIfExists(string file, string elemName = null, LoadOptions options = LoadOptions.None)
```

##### Parameters

- *file*  (`string`)
- *elemName*  (`string`):
    Element name to use if *file* does not exist. If `null`, returns `null` if *file* does not exist.
- *options*  (`LoadOptions`)

##### Returns

`XElement`

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Exception`:
    Exceptions of `System.Xml.Linq.XElement.Load`.