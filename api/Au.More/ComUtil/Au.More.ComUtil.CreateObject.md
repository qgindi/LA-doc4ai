# Method `Au.More.ComUtil.CreateObject`

## Overload 1

Creates COM object using ProgID.

```
public static object CreateObject(string progID)
```

##### Parameters

- *progID*  (`string`):
    The programmatic identifier (ProgID) of the COM type.

##### Returns

`object`

##### Exceptions

- `Exception`

#### Remarks

Use this function when you don't have the COM interface definition or the interop assembly. Else use code like `var x = new InterfaceType();` or `var x = new CoclassType() as InterfaceType`.

#### Examples

```
dynamic app = ComUtil.CreateObject("Excel.Application");
app.Visible = true;
3.s();
app.Quit();
```

* * *

## Overload 2

Creates COM object using CLSID.

```
public static object CreateObject(in Guid clsid)
```

##### Parameters

- *clsid*  (`Guid`)

##### Returns

`object`

##### Exceptions

- `Exception`