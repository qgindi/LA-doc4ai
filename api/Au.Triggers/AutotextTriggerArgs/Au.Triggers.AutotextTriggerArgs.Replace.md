# Method `Au.Triggers.AutotextTriggerArgs.Replace`

Replaces the user-typed text with the specified text or/and HTML.

```
public void Replace(string text, string html = null)
```

##### Parameters

- *text*  (`string`):
    The replacement text. Can be `null`. Can contain `[[|]]` to move the text cursor (caret) there with the `Left` key; not if *html* specified.
- *html*  (`string`):
    The replacement HTML. Can be full HTML or fragment. See `Au.clipboardData.AddHtml`. Can be specified only *text* or only *html* or both. If both, will paste *html* in apps that support it, elsewhere *text*. If only *html*, in apps that don't support HTML will paste *html* as text.

#### Remarks

Options for this function can be specified when adding triggers, in the *flags* parameter. Or before adding triggers, with `Au.Triggers.AutotextTriggers.DefaultFlags`.

#### Examples

```
Triggers.Autotext["#exa"] = o => o.Replace("<example>[[|]]</example>");
```

More examples: `Au.Triggers.ActionTriggers`.