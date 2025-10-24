# Other conversions

To convert simple types such as `int` to `double` or vice versa, use implicit or explicit cast.

```
int i = 5;
double d4 = i; //implicit cast
//int i1 = d4; //error, can't convert implicitly (because the double type is larger than int)
int i1 = (int)d4; //explicit cast
```

Or use class [Convert](https://www.google.com/search?q=System.Convert+class).

```
i1 = Convert.ToInt32(d4);
```

In some cases you may need `BitConverter`.

```
var b = new byte[] { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };
print.it(BitConverter.ToString(b));
```