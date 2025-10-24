# Callback functions, lambda, delegate, event

Note: callback functions and events are widely used. Without this knowledge you can't write or read many scripts and other codes.

The second argument in the first example is a callback function, also known as [lambda](https://www.google.com/search?q=C%23+lambda). It is passed to `Func1`, and then `Func1` calls it.

```
Func1(5, i => { print.it(i); });
Func1(5, i => print.it(i)); //the same. Don't need { } if there is single statement.

//or the callback function can be defined elsewhere; then it can be used in multiple places.
Func1(2, Func2);
Func1(3, Func2);

//or use a delegate variable
Action<int> a1 = i => { print.it(i); };
Func1(4, a1);
Func1(5, a1);

Func3(() => {  });
Func4((a, b) => {  });

Func5(i => i != 0); // { return i != 0; }

void Func1(int n, Action<int> a) {
	for (int i = 0; i < n; i++) {
		a(i);
	}
}

void Func2(int i) {
	print.it(i);
}

void Func3(Action a) {
	a();
}

void Func4(Action<int, string> a) {
	a(1, "TEXT");
}

void Func5(Func<int, bool> a) {
	bool r = a(1);
}
```

The above examples use generic function types [Action\[\[lt\]\]T\[\[gt\]\]](https://www.google.com/search?q=System.Action%3CT%3E+delegate) and [Func\[\[lt\]\]T, TResult\[\[gt\]\]](https://www.google.com/search?q=System.Func%3CT%2C+TResult%3E+delegate). Function types can be defined with the `delegate` keyword.

In the above examples we pass lambdas etc as function parameters. Actually we pass *delegates* - auto-created objects that can call the function.

Another way is *events*. An event can have multiple subscribed functions. When raised, it calls all them. Subscribe with operator +=. Unsubscribe (if need) with operator -=. [More info](https://www.google.com/search?q=C%23+event).

```
var c = new Class1();
c.Event1 += i => print.it("event handler lambda", i);
c.Event1 += EventHandler;
c.Func1(1);
c.Event1 -= EventHandler;
c.Func1(2);

void EventHandler(int i) {
	print.it("event handler method", i);
}

class Class1 {
	//Declare an event. 
	public event Action<int> Event1;
	
	public void Func1(int x) {
		//Raise the event. It calls all subscribed functions.
		Event1?.Invoke(x); //? means "do nothing if the event is null, ie there are no subscribers"
	}
}
```

Events are very useful in custom dialog windows. Examples in recipe [Dialog - events](Dialog%20-%20events.html).