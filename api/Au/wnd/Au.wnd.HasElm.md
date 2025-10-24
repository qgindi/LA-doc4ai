# Method `Au.wnd.HasElm`

Returns `true` if this window contains the specified UI element. Calls `Au.elmFinder.Exists`.

```
public bool HasElm(elmFinder f)
```

##### Parameters

- *f*  (`Au.elmFinder`)

##### Returns

`bool`

##### Exceptions

- `Au.Types.AuWndException`

#### Examples

Find window that contains certain UI element, and get the UI element too.

```
var f = new elmFinder("BUTTON", "OK");
wnd w = wnd.find(cn: "#32770", also: t => t.HasElm(f));
print.it(w);
print.it(f.Result);
```

The same with parameter *contains*.

```
var f = new elmFinder("BUTTON", "OK");
wnd w = wnd.find(cn: "#32770", contains: f);
print.it(w);
print.it(f.Result);
```