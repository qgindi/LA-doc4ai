# Method `Au.More.HttpServerSession.Run`

Executes the session: reads requests, calls your `Au.More.HttpServerSession.MessageReceived`, writes responses, implements keep-alive.

```
protected virtual void Run()
```

#### Remarks

The server uses try/catch when calling this. Prints unhandled exceptions if `Au.More.HttpServerSession.Verbose` `true`. On unhandled exception closes the connection.