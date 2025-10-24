# Method `Au.wnd.HasChild`

Returns `true` if this window contains the specified control. Calls `Au.wndChildFinder.Exists`.

```
public bool HasChild(wndChildFinder f)
```

##### Parameters

- *f*  (`Au.wndChildFinder`)

##### Returns

`bool`

##### Exceptions

- `Au.Types.AuWndException`

#### Examples

Find window that contains certain control, and get the control too.

```
var cf = new wndChildFinder("Password*", "Static");
wnd w = wnd.find(cn: "#32770", also: t => t.HasChild(cf));
print.it(w);
print.it(cf.Result);
```

The same with parameter *contains*.

```
var cf = new wndChildFinder("Password*", "Static");
wnd w = wnd.find(cn: "#32770", contains: cf);
print.it(w);
print.it(cf.Result);
```