# Method `Au.More.ComUtil.GetWindowObject`

Gets COM object from a window using API `AccessibleObjectFromWindow(OBJID_NATIVEOM, IID_IDispatch`).

```
public static object GetWindowObject(wnd w, string cnChild = null, bool dontThrow = false)
```

##### Parameters

- *w*  (`Au.wnd`):
    Window or control.
- *cnChild*  (`string`):
    Child window class name. Format: [wildcard expression](../articles/Wildcard%20expression.html). If used, gets COM object from the first found child or descendant window where it succeeds. If `null`, gets COM object from *w*.
- *dontThrow*  (`bool`):
    If fails to get COM object, don't throw exception but return `null`.

##### Returns

`object`

##### Exceptions

- `Au.Types.AuWndException`:
    *w* 0 or invalid.
- `Au.Types.AuException`:
    Failed.

#### Examples

Microsoft Excel.

```
/*/ com Excel 1.9 #9fdf46bf.dll; /*/
using Excel = Microsoft.Office.Interop.Excel;
var w = wnd.find(0, null, "XLMAIN", "EXCEL.EXE");
Excel.Workbook book = ((Excel.Window)ComUtil.GetWindowObject(w, "EXCEL7")).Parent;
print.it(book.Name);
```

Microsoft Word.

```
/*/ com Word 8.7 #6a6b0205.dll; /*/
using Word = Microsoft.Office.Interop.Word;
var w = wnd.find(0, null, "OpusApp", "WINWORD.EXE");
Word.Document doc = ((Word.Window)ComUtil.GetWindowObject(w, "_WwG")).Parent;
print.it(doc.Name);
```

Microsoft PowerPoint.

```
/*/ com PowerPoint 2.12 #fdf81915.dll; /*/
using PowerPoint = Microsoft.Office.Interop.PowerPoint;
var w = wnd.find(0, "*PowerPoint", null, "POWERPNT.EXE");
PowerPoint.Presentation doc = ((PowerPoint.DocumentWindow)ComUtil.GetWindowObject(w, "**m mdiClass||paneClassDC")).Parent;
print.it(doc.Name);
```

Microsoft Access.

```
/*/ com Access 9.0 #cdda93ea.dll; /*/
using Access = Microsoft.Office.Interop.Access;
var w = wnd.find(0, null, "OMain", "MSACCESS.EXE");
Access.Application app = (Access.Application)ComUtil.GetWindowObject(w);
print.it(app.CurrentProject.Name);
```

To get COM object from Microsoft Outlook or Publisher, use `Au.More.ComUtil.GetActiveObject`.