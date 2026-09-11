# Markdown

Library info: [Markdig](🔗). NuGet: Markdig.

```csharp
/*/ nuget -\Markdig; /*/

var md = """
## Header
Text.
""";
var s = Markdig.Markdown.ToHtml(md);
print.it(s);
```