# Constructor of `Au.Types.HSContentPart`

```
public HSContentPart(int Index, Dictionary<string, string> Headers, byte[] Content)
```

##### Parameters

- *Index*  (`int`):
    0-based index of this part in the list of parts.
- *Headers*  (`Dictionary<string, string>`):
    Headers of this part.
- *Content*  (`byte[]`):
    Raw content of this part. For example UTF-8 text.