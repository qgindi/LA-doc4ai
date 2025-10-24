# Method `Au.Types.ExtXml.Elem`

Gets the first found direct child element that has the specified attribute or value.

```
public static XElement Elem(this XElement t, XName name, XName attributeName, string attributeValue = null, bool ignoreCase = false)
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

`XElement`

`null` if not found.