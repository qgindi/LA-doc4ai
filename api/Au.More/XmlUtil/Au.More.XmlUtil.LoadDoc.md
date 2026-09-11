# Method `Au.More.XmlUtil.LoadDoc`

Loads XML file in a safer way.
Uses`System.Xml.Linq.XDocument.Load` and `Au.filesystem.waitIfLocked`.

```csharp
public static XDocument LoadDoc(string file, LoadOptions options = LoadOptions.None)
```

##### Parameters

- *file*  (`string`):
  File. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`.
  If starts with`'<'`, loads from XML string instead.
- *options*  (`LoadOptions`):
  Enum: value__, None, PreserveWhitespace, SetBaseUri, SetLineInfo, .ctor.

##### Returns

`XDocument`

##### Exceptions

- `ArgumentException`:
  Not full path.
- `Exception`:
  Exceptions of `System.Xml.Linq.XDocument.Load`.

#### Remarks

Unlike `System.Xml.Linq.XDocument.Load`, does not replace `\r\n` with `\n`.