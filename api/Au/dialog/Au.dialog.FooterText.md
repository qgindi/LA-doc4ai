# Method `Au.dialog.FooterText`

Adds footer text.

```
public dialog FooterText(DText text)
```

##### Parameters

- *text*  (`Au.Types.DText`):
    Text. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`, or `null`.

##### Returns

`Au.dialog`