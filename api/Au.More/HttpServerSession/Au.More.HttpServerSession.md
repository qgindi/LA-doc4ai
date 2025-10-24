# Class `Au.More.HttpServerSession`

Simple HTTP 1.1 server. Can be used for communicating between two scripts or apps on local network, internet or same computer. Also can receive requests from web browsers etc.

```
public abstract class HttpServerSession
```

##### Remarks

To receive HTTP messages, create a class with base `HttpServerSession` and add function `Au.More.HttpServerSession.MessageReceived`. Example in `Au.More.HttpServerSession.Listen<TSession>`.

##### Inheritance

`object` → `HttpServerSession`

### Properties

`Client`, `ClientIP`, `KeepAliveTimeout`, `Verbose`

### Methods

`Auth`, `Listen<TSession>`, `MessageReceived`, `Run`