# Property `Au.csvTable.Rows`

Gets the internal `List` containing rows as string arrays.

```
public List<string[]> Rows { get; }
```

##### Property Value

`List<string[]>`

#### Remarks

It's not a copy; changing its content will change content of this `Au.csvTable` variable. You can do anything with the `List`. For example, sort it, find rows containing certain field values, get/set field values directly, add/remove rows directly. All row arrays have `Length` equal to `Au.csvTable.ColumnCount`, and it must remain so; you can change `Length`, but then need to call `ColumnCount=newLength`.

#### Examples

```
x.Rows.Sort((a,b) => string.CompareOrdinal(a[0], b[0]));
```