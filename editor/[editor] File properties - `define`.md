# File properties - `define`

Symbols that can be used with `#if`. Example: `ONE,TWO,d:THREE,r:FOUR`.

A symbol here can have a prefix:

- `r:` - define the symbol only if `optimize true` (checked).
- `d:` - define the symbol only if no `optimize true`.

If no `optimize true`, symbols `DEBUG` and `TRACE` are added implicitly.

See also [C# #define](https://www.google.com/search?q=site:microsoft.com+C%23+%23define).