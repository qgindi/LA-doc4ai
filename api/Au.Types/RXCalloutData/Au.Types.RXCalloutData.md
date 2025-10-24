# Struct `Au.Types.RXCalloutData`

Managed version of PCRE API struct `pcre2_callout_block`. When you set `Au.regexp.Callout`, your callout function's parameter is of this type.

```
public struct RXCalloutData
```

##### Remarks

More info in PCRE help topic [pcre2callout](https://www.pcre.org/current/doc/html/pcre2callout.html). Most properties are `pcre2_callout_block` fields as documented in PCRE help. Other properties and methods are easier/safer versions of unsafe fields like `offset_vector`.

### Properties

`LastGroup`, `LastGroupValue`, `Result`, `callout_flags`, `callout_number`, `callout_string`, `callout_string_offset`, `capture_last`, `capture_top`, `current_position`, `mark`, `next_item_length`, `pattern_position`, `start_match`

### Methods

`Group`, `GroupValue`