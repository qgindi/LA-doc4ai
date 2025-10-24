# Method `Au.Types.TreeBase<T>.XmlSave`

## Overload 1

Saves tree of nodes (this and descendants) to an XML file.

```
protected void XmlSave(string file, TreeBase<T>.XmlNodeWriter nodeWriter, XmlWriterSettings sett = null, IEnumerable<T> children = null)
```

##### Parameters

- *file*  (`string`):
    XML file. Must be full path. Can contain environment variables etc, see `Au.pathname.expand`.
- *nodeWriter*  (`Au.Types.TreeBase<T>`.`Au.Types.TreeBase-1.XmlNodeWriter`):
    Callback function that writes node's XML start element (see `System.Xml.XmlWriter.WriteStartElement`) and attributes (see `System.Xml.XmlWriter.WriteAttributeString`). Must not write children and end element. Also should not write value, unless your reader knows how to read it.
- *sett*  (`XmlWriterSettings`):
    XML formatting settings. Optional.
- *children*  (`IEnumerable<T>`):
    If not `null`, writes these nodes as if they were children of this node.

##### Exceptions

- `ArgumentException`:
    Not full path.
- `Exception`:
    Exceptions of `System.Xml.XmlWriter.Create` and other `System.Xml.XmlWriter` methods.

#### Remarks

Uses `Au.filesystem.save`. It ensures that existing file data is not damaged on exception etc.

#### Examples

`Au.Types.TreeBase<T>`

* * *

## Overload 2

Writes tree of nodes (this and descendants) to an `System.Xml.XmlWriter`.

```
protected void XmlSave(XmlWriter x, TreeBase<T>.XmlNodeWriter nodeWriter, IEnumerable<T> children = null)
```

##### Parameters

- *x*  (`XmlWriter`)
- *nodeWriter*  (`Au.Types.TreeBase<T>`.`Au.Types.TreeBase-1.XmlNodeWriter`):
    Callback function that writes node's XML start element (see `System.Xml.XmlWriter.WriteStartElement`) and attributes (see `System.Xml.XmlWriter.WriteAttributeString`). Must not write children and end element. Also should not write value, unless your reader knows how to read it.
- *children*  (`IEnumerable<T>`):
    If not `null`, writes these nodes as if they were children of this node.

##### Exceptions

- `Exception`:
    Exceptions of `System.Xml.XmlWriter` methods.

#### Examples

`Au.Types.TreeBase<T>`