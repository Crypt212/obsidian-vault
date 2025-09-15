# AJAX
- AJAX stands for **Asynchronous JavaScript and XML**, it's a set of web development techniques that allows a web page to communicate with a server **without reloading the entire page**.
- This creates a much faster and smoother user experience, similar to a desktop application.
- The process relies on a JavaScript object called the *[[XHR]]* or the newer, more powerful [[Fetch API]].
> Note that it supports [[XML]], [[MindMap/Software Engineering/Languages/Serialization Format/JSON|JSON]] and many more, the name is just historical.
## XHR (`XMLHttpRequest`)
- The **`XMLHttpRequest`** object (often called **XHR**) is a built-in tool in [[JavaScript]] that allows your web page to **talk to a server** using [[HTTP]] protocol.
## Fetch API
- The **`fetch`** method is a *modern* built-in tool in [[JavaScript]] that allows your web page to **talk to a server** using [[HTTP]] protocol, it uses [[promises]].
# JSON in JavaScript
- [[JSON]] can be used in [[Javascript]] to hold data, we have a class to deal with [[JSON]] data called, guess what, `JSON` class.
## Important Methods
1. `JSON.stringify()`: Converts [[Javascript]] object to [[JSON]] data.
2. `JSON.parse()`: Converts [[JSON]] data to [[Javascript]] object.

# Asynchronous Javascript
- JavaScript is single-threaded → it runs one task at a time (on the *call stack*).
- We can utilize the browser (or *[[Node]]* environment) to run our code asynchronously, since these environments provide:
	- Web APIs.
	- Callback Queue (Task Queue) that contains functions waiting to be executed
- For slow tasks it uses asynchronous programming.
- *asynchronous* code is code that runs without blocking code after it.{}
## Promises
- promise is a block of code that will start running *asynchronously* (without blocking )
## `async`/`await`
