# Method `Au.wpfBuilder.End`

Ends adding controls etc to the window or nested panel (`Au.wpfBuilder.StartGrid` etc).

```csharp
public wpfBuilder End()
```

##### Returns

`Au.wpfBuilder`

#### Remarks

Always call this method to end a nested panel. For root panel it is optional if using `Au.wpfBuilder.ShowDialog`.