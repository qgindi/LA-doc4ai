# Method `Au.More.XmlUtil.LoadElem`

## Overload 1

Loads XML file in a safer way. Uses `System.Xml.Linq.XElement.Load` and `Au.filesystem.waitIfLocked`.

```
public static XElement LoadElem(string file, LoadOptions options = LoadOptions.None)
```

##### Parameters

- *file*  (`string`):
    File. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`. If starts with `'<'`, loads from XML string instead.
- *options*  (`LoadOptions`)

##### Returns

`XElement`

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Exception`:
    Exceptions of `System.Xml.Linq.XElement.Load`.

#### Remarks

Unlike `System.Xml.Linq.XElement.Load`, does not replace `\r\n` with `\n`.

* * *

## Overload 2

Loads XML file with a namespace.

```
public static XElement LoadElem(out XNamespace ns, string file, LoadOptions options = LoadOptions.None)
```

##### Parameters

- *ns*  (`XNamespace`):
    Receives the default namespace. Use it to get elements, like `var x2 = x1.Element(ns + "name")`.
- *file*  (`string`):
    File. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`. If starts with `'<'`, loads from XML string instead.
- *options*  (`LoadOptions`)

##### Returns

`XElement`

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Exception`:
    Exceptions of `System.Xml.Linq.XElement.Load`.

#### Remarks

Unlike `System.Xml.Linq.XElement.Load`, does not replace `\r\n` with `\n`.