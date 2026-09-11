# Constructor of `Au.wildex`

```csharp
public wildex(string wildcardExpression, bool matchCase = false, bool noException = false)
```

##### Parameters

- *wildcardExpression*  (`string`):
  [Wildcard expression](🔗).
  Cannot be`null`(throws exception).
  `""` will match `""`.
- *matchCase*  (`bool`):
  Case-sensitive even if there is no `**c`.
- *noException*  (`bool`):
  If *wildcardExpression* is invalid, don't throw exception; let `Au.wildex.Match` always return `false`.

##### Exceptions

- `ArgumentNullException`
- `ArgumentException`:
  Invalid `"**options "` or regular expression.