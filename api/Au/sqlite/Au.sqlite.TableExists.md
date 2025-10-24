# Method `Au.sqlite.TableExists`

Returns `true` if the table exists.

```
public bool TableExists(string table)
```

##### Parameters

- *table*  (`string`):
    Table name.

##### Returns

`bool`

#### Remarks

This function is slower than `"CREATE TABLE IF NOT EXISTS..."`.