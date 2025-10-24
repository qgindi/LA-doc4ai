# Method `Au.Types.ExtXml.Descs`

Finds all descendant elements that have the specified attribute or value.

```
public static IEnumerable<XElement> Descs(this XElement t, XName name, XName attributeName, string attributeValue = null, bool ignoreCase = false)
```

##### Parameters

- *t*  (`XElement`)
- *name*  (`XName`):
    Element name. If `null`, can be any name.
- *attributeName*  (`XName`):
    Attribute name. If `null`, uses the `Value` property of the element.
- *attributeValue*  (`string`):
    Attribute value (or `Value`). If `null`, can be any value.
- *ignoreCase*  (`bool`):
    Case-insensitive *attributeValue*.

##### Returns

`IEnumerable<XElement>`

`null` if not found.