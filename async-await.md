# Async/Await

`Note: await accepts “thenable” objects` https://javascript.info/async-await
Async wraps the returned value into a Promise regardless whether it is a Promise or any other value.

The fundamental difference between await and vanilla promises is that await X() suspends execution of the current function, while promise.then(X) continues execution of the current function after adding the X call to the callback chain. In the context of stack traces, this difference is pretty significant. Enable JavaScript engines to handle stack traces in a more performant and memory-efficient manner by following these recommendations
https://mathiasbynens.be/notes/async-stack-traces