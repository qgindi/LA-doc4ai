# Method `Au.perf.next`

Stores current time in next element of an internal array.

```
public static void next(char cMark = '\0')
```

##### Parameters

- *cMark*  (`char`):
    A character to mark this time in the results string, like `"A=150"`.

#### Remarks

Don't call `next` more than 16 times after `Au.perf.first`, because the array size is fixed.