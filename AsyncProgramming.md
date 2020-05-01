### What is Async programming
Its programming paradigm used to provide flawless user experience because user is free to do other task without waiting for current task to be finished.
### Multithreading vs Async Programming
>| Traditional | Current |
>| ------ | ----------- |
>|   Threading (Low-Level)   | Task & Parallel Library |
>| Background Worker (Event Based Async Pattern) | Async & Await |
### How to make async call
calling method should be marked with `async` keyword. Inside calling method those methods call which takes long time to process must be decorated with `await` keyword
### Example of long running codes.
- I/O Operation (disk)
- Memory 
- External service call (http, tcp, socket)
- Databse call
### What is the significance of `await` keyword
- The `await` keyword will pause execution of attached method until result is available without blocking current/UI thread
- `await` keyword validate the success of asychronous operation.
- After successfull operation returns potential result.
> The Only time `async` method returns `void` when its a `Event Handler`

___
- Method Marked `async task` will automatically return task without explicitly having to return anything.
- Exception occured in `async void` method are uncaught leads to application crash.
___
### Dos and Donts
>| DO NOTs | DOs |
>| ------ | ----------- |
>|  Never use `async void` unless it's an event handler or delegate | Always use `async` and `await` together|
>|Never block async operation by calling `Result` or `Wait()`|Always return as `Task` from an async method| 
>||Always await an async method to validate operation|






