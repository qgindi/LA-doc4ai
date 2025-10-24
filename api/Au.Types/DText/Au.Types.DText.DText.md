# Constructor of `Au.Types.DText`

```
public DText(string text, params Action<DEventArgs>[] links)
```

##### Parameters

- *text*  (`string`):
    Text. Links can be specified like `"Text <a>link</a> text."`.
- *links*  (`Action[]<Au.Types.DEventArgs>`):
    Link click handlers like `e => { print.it("link"); }`.