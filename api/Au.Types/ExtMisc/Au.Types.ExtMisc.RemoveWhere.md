# Method `Au.Types.ExtMisc.RemoveWhere`

Removes items based on a predicate. For example, all items that have certain value.

```
public static void RemoveWhere<TKey, TValue>(this Dictionary<TKey, TValue> t, Func<KeyValuePair<TKey, TValue>, bool> predicate)
```

##### Parameters

- *t*  (`Dictionary<TKey, TValue>`)
- *predicate*  (`Func<KeyValuePair<TKey, TValue>, bool>`)

##### Type Parameters

- `TKey`
- `TValue`