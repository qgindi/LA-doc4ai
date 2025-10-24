# Method `Au.Types.TreeBase<T>.XmlLoad`

## Overload 1

Loads XML file and creates tree of nodes from it.

```
protected static T XmlLoad(string file, TreeBase<T>.XmlNodeReader nodeReader)
```

##### Parameters

- *file*  (`string`):
    XML file. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`.
- *nodeReader*  (`Au.Types.TreeBase<T>`.`Au.Types.TreeBase-1.XmlNodeReader`):
    Callback function that reads current XML element and creates/returns new node. See example.

##### Returns

`T`

the root node.

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Exception`:
    Exceptions of `System.Xml.XmlReader.Create`.
- `XmlException`:
    An error occurred while parsing the XML.

#### Examples

`Au.Types.TreeBase<T>`

* * *

## Overload 2

Reads XML and creates tree of nodes.

```
protected static T XmlLoad(XmlReader x, TreeBase<T>.XmlNodeReader nodeReader)
```

##### Parameters

- *x*  (`XmlReader`)
- *nodeReader*  (`Au.Types.TreeBase<T>`.`Au.Types.TreeBase-1.XmlNodeReader`):
    Callback function that reads current XML element and creates/returns new node.

##### Returns

`T`

the root node.

##### Exceptions

- `XmlException`:
    An error occurred while parsing the XML.

#### Examples

`Au.Types.TreeBase<T>`