# Method `Au.clipboardData.AddHtml`

Adds HTML text. Uses clipboard format `Au.Types.ClipFormats.Html` (`"HTML Format"`).

```
public clipboardData AddHtml(string html)
```

##### Parameters

- *html*  (`string`):
    Full HTML or HTML fragment. If full HTML, a fragment in it can be optionally specified. See examples.

##### Returns

`Au.clipboardData`

this.

##### Exceptions

- `ArgumentNullException`

#### Examples

```
d.AddHtml("<i>italy</i>");
d.AddHtml("<html><body><i>italy</i></body></html>");
d.AddHtml("<html><body><!--StartFragment--><i>italy</i><!--EndFragment--></body></html>");
```