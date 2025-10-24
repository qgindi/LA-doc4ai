# Field `Au.pathname.maxFilePathLength`

Maximal file (not directory) path length supported by all functions (native, .NET and this library). For longer paths need `@"\\?\"` prefix. It is supported by most native kernel API (but not shell API) and most functions of this library and .NET.

```
public const int maxFilePathLength = 259
```