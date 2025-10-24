# Method `Au.More.PrintServer.GetMessage`

Gets next message and removes from the queue.

```
public bool GetMessage(out PrintServerMessage m)
```

##### Parameters

- *m*  (`Au.Types.PrintServerMessage`)

##### Returns

`bool`

`false` if there are no messages.

#### Remarks

Messages are added to an internal queue when clients call `Au.print.it` etc. They contain the text, time, etc. This function gets the oldest message and removes it from the queue.