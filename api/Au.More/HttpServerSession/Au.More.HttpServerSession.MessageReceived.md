# Method `Au.More.HttpServerSession.MessageReceived`

Called when the server receives a HTTP request message.

```
protected abstract void MessageReceived(HSMessage m, HSResponse r)
```

##### Parameters

- *m*  (`Au.Types.HSMessage`):
    Contains request info and content.
- *r*  (`Au.Types.HSResponse`):
    Allows to set response info and content.

#### Remarks

Not called if failed to read the message.

The server uses try/catch when calling this. Prints unhandled exceptions if `Au.More.HttpServerSession.Verbose` `true`. On unhandled exception sends error 500 (`InternalServerError`) and closes the connection.