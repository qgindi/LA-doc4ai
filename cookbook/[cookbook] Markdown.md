# Markdown

Library info: [Markdig](https://github.com/xoofx/markdig). NuGet: Markdig.

```
/*/ nuget -\Markdig; /*/

var md = """
## Header
Text.
""";
var s = Markdig.Markdown.ToHtml(md);
print.it(s);
```