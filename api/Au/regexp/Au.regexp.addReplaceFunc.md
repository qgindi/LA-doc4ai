# Method `Au.regexp.addReplaceFunc`

Adds or replaces a function that is called when a regular expression replacement string contains `${+name}` or `${+name(g)}` or `${+name(g, v)}`, where *g* is group number or name and *v* is any string.

```
public static void addReplaceFunc(string name, Func<RXMatch, int, string, string> replFunc)
```

##### Parameters

- *name*  (`string`):
    A string used to identify the function. Can contain any characters except `'}'`, `'('` and `')'`.
- *replFunc*  (`Func<Au.Types.RXMatch, int, string, string>`):

    Callback function. Called for each found match. Returns the replacement. Parameters:

    - current match.
    - group number *g*, if replacement is like `${+name(g)}` or `${+name(g, v)}`; else 0.
    - string *v*, if replacement is like `${+name(g, v)}`; else `null`.

    In the callback function you can use `Au.Types.RXMatch.ExpandReplacement`.

#### Remarks

Useful when there is no way to use `Au.regexp.Replace` overloads with a *replFunc* parameter. For example in Find/Replace UI.

#### Examples

Create new script in editor and add this code. In **Properties** set role `editorExtension`. Run. Then in the **Find** panel in the replacement field you can use `${+Lower}`, `${+Lower(1)}`, `${+Lower(2)}` etc.

```
regexp.addReplaceFunc("Lower", (m, g, v) => m[g].Value.Lower()); //make lowercase
```

Another example. Replacement could be like `${+mul(1, 10)}`.

```
regexp.addReplaceFunc("mul", (m, g, v) => (m[g].Value.ToInt() * v.ToInt()).ToString()); //multiply by v
```