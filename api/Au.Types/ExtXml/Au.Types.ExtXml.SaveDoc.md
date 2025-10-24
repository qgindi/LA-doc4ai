# Method `Au.Types.ExtXml.SaveDoc`

Saves XML to a file in a safer way. Uses `System.Xml.Linq.XDocument.Save` and `Au.filesystem.save`

```
public static void SaveDoc(this XDocument t, string file, bool backup = false, SaveOptions? options = null)
```

##### Parameters

- *t*  (`XDocument`)
- *file*  (`string`)
- *backup*  (`bool`)
- *options*  (`SaveOptions?`)

##### Exceptions

- `Exception`:
    Exceptions of `System.Xml.Linq.XDocument.Save` and `Au.filesystem.save`.