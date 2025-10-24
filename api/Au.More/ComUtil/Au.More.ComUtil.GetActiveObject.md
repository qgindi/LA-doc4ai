# Method `Au.More.ComUtil.GetActiveObject`

## Overload 1

Gets a COM object existing in other process and registered in ROT.

```
public static object GetActiveObject(string progID, bool dontThrow = false)
```

##### Parameters

- *progID*  (`string`):
    ProgID of the COM class. Example: `"Excel.Application"`.
- *dontThrow*  (`bool`):
    If fails, don't throw exception but return `null`.

##### Returns

`object`

##### Exceptions

- `COMException`:

    - *progID* not found in the registry. Probably it is incorrect, or the program isn't installed.
    - An object of this type currently is unavailable. Probably the program is not running, or running with a different UAC integrity level.

#### Remarks

Calls API `GetActiveObject`.

This process must have the same [UAC](../articles/UAC.html) integrity level as the target process (of the COM object). In script **Properties** select **uac user**.

#### Examples

```
/*/ uac user; com Outlook 9.6 #ed6988d3.dll; /*/
using Outlook = Microsoft.Office.Interop.Outlook;
var app = (Outlook.Application)ComUtil.GetActiveObject("Outlook.Application");
print.it(app.ActiveExplorer().CurrentFolder.Name);
```

### See Also

`System.Runtime.InteropServices.Marshal.BindToMoniker`

* * *

## Overload 2

```
public static object GetActiveObject(in Guid clsid, bool dontThrow = false)
```

##### Parameters

- *clsid*  (`Guid`)
- *dontThrow*  (`bool`)

##### Returns

`object`

##### Exceptions

- `COMException`:
    An object of this type currently is unavailable. Probably its program is not running, or running with a different UAC integrity level.