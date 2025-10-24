# Method `Au.Types.ExtXml.ElemOrAdd`

## Overload 1

Gets the first found direct child element. If not found, adds new empty child element.

```
public static XElement ElemOrAdd(this XElement t, XName name)
```

##### Parameters

- *t*  (`XElement`)
- *name*  (`XName`)

##### Returns

`XElement`

The found or added element.

* * *

## Overload 2

Gets the first found direct child element that has the specified attribute. If not found, adds new child element with the attribute. More info: `Au.Types.ExtXml.Elem`

```
public static XElement ElemOrAdd(this XElement t, XName name, XName attributeName, string attributeValue = null, bool ignoreCase = false)
```

##### Parameters

- *t*  (`XElement`)
- *name*  (`XName`)
- *attributeName*  (`XName`)
- *attributeValue*  (`string`)
- *ignoreCase*  (`bool`)

##### Returns

`XElement`

The found or added element.