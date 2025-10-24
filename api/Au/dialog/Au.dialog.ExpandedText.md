# Method `Au.dialog.ExpandedText`

Adds text in expander control.

```
public dialog ExpandedText(DText text, bool showInFooter = false)
```

##### Parameters

- *text*  (`Au.Types.DText`):
    Text. Can be string, or string with links like `new("Text <a>link</a> text.", e => { print.it("link"); })`, or `null`.
- *showInFooter*  (`bool`):
    Show the text at the bottom of the dialog.

##### Returns

`Au.dialog`