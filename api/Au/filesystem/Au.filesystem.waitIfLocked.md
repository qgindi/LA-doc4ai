# Method `Au.filesystem.waitIfLocked`

## Overload 1

This function can be used to safely open a file that may be temporarily locked (used by another process or thread). Waits while the file is locked.

```
public static T waitIfLocked<T>(Func<T> f, int millisecondsTimeout = 2000)
```

##### Parameters

- *f*  (`Func<T>`):
    Lambda that calls a function that creates, opens or opens/reads/closes a file.
- *millisecondsTimeout*  (`int`):
    Wait max this number of milliseconds. Can be `System.Threading.Timeout.Infinite` (-1).

##### Returns

`T`

The return value of the lambda *f*.

##### Exceptions

- `ArgumentOutOfRangeException`:
    *millisecondsTimeout* less than -1.
- `Exception`:
    Exceptions thrown by the called function.

##### Type Parameters

- `T`

#### Remarks

Calls the lambda and handles `System.IO.IOException`. If the exception indicates that the file is locked, waits and retries in loop.

#### Examples

```
var s1 = File.ReadAllText(file); //unsafe. Exception if the file is locked.

var s2 = filesystem.waitIfLocked(() => File.ReadAllText(file)); //safe. Waits while the file is locked.

using(var f = filesystem.waitIfLocked(() => File.OpenText(file))) { //safe. Waits while the file is locked.
	var s3 = f.ReadToEnd();
}

using(var f = filesystem.waitIfLocked(() => File.Create(file))) { //safe. Waits while the file is locked.
	f.WriteByte(1);
}
```

* * *

## Overload 2

This function can be used to safely open a file that may be temporarily locked (used by another process or thread). Waits while the file is locked.

```
public static void waitIfLocked(Action f, int millisecondsTimeout = 2000)
```

##### Parameters

- *f*  (`Action`):
    Lambda that calls a function that creates, opens or opens/reads/closes a file.
- *millisecondsTimeout*  (`int`):
    Wait max this number of milliseconds. Can be `System.Threading.Timeout.Infinite` (-1).

##### Exceptions

- `ArgumentOutOfRangeException`:
    *millisecondsTimeout* less than -1.
- `Exception`:
    Exceptions thrown by the called function.

#### Remarks

Calls the lambda and handles `System.IO.IOException`. If the exception indicates that the file is locked, waits and retries in loop.

#### Examples

```
File.WriteAllText(file, "TEXT"); //unsafe. Exception if the file is locked.

filesystem.waitIfLocked(() => File.WriteAllText(file, "TEXT")); //safe. Waits while the file is locked.
```