# Operator `Au.wildex.implicit operator`

Creates new `Au.wildex`from wildcard expression string.
If the string is`null`, returns `null`.

```csharp
public static implicit operator wildex(string wildcardExpression)
```

##### Parameters

- *wildcardExpression*  (`string`):
  [Wildcard expression](🔗).

##### Returns

`Au.wildex`

##### Exceptions

- `ArgumentException`:
  Invalid `"**options "` or regular expression.