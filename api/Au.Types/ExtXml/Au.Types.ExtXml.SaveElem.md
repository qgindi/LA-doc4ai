# Method `Au.Types.ExtXml.SaveElem`

Saves XML to a file in a safer way. Uses `System.Xml.Linq.XElement.Save` and `Au.filesystem.save`.

```
public static void SaveElem(this XElement t, string file, bool backup = false, SaveOptions? options = null)
```

##### Parameters

- *t*  (`XElement`)
- *file*  (`string`)
- *backup*  (`bool`)
- *options*  (`SaveOptions?`)

##### Exceptions

- `Exception`:
    Exceptions of `System.Xml.Linq.XElement.Save` and `Au.filesystem.save`.