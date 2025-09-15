# [[AJAX]]
- [[AJAX]] stands for **Asynchronous JavaScript and XML**, it's a set of web development techniques that allows a web page to communicate with a server **without reloading the entire page**.
- This creates a much faster and smoother user experience, similar to a desktop application.
- The process relies on a JavaScript object called the *[[XHR]]* or the newer, more powerful [[Fetch API]].
> Note that it supports [[XML]], [[MindMap/Software Engineering/Languages/Serialization Format/JSON|JSON]] and many more, the name is just historical.
# [[XHR]] (`XMLHttpRequest`)
- The **`XMLHttpRequest`** object (often called **XHR**) is a built-in tool in [[JavaScript]] that allows your web page to **talk to a server** using [[HTTP]] protocol.
# [[Fetch API]]
- The **`fetch`** method is a *modern* built-in tool in [[JavaScript]] that allows your web page to **talk to a server** using [[HTTP]] protocol, it uses [[promises]].
# [[MindMap/Software Engineering/Languages/Javascript/JSON|JSON]] in JavaScript
- A class to deal with [[MindMap/Software Engineering/Languages/Serialization Format/JSON|JSON]] data.
## Important Methods
1. `JSON.stringify()`: Converts [[Javascript]] object to [[MindMap/Software Engineering/Languages/Serialization Format/JSON|JSON]] data.
2. `JSON.parse()`: Converts [[MindMap/Software Engineering/Languages/Serialization Format/JSON|JSON]] data to [[Javascript]] object.

# Asynchronous Javascript
- JavaScript is single-threaded → it runs one task at a time (on the *call stack*).
- We can utilize the browser (or *[[Node JS]]* environment) to run our code asynchronously, since these environments provide:
	- Web APIs.
	- *Callback Queue* (*Task Queue*) that contains functions waiting to be executed after the *call stack* finishes, there are 2 types of queues with the provided priorities:
		- **1st**: *Microtask Queue* containing callbacks from promises.
		- **2nd**: *Macrotask Queue* containing callbacks from Web APIs.
	- *Event Loop*, a constantly running process that checks if the *call stack* is empty. If it is, it moves the first function from the *callback queue* to the *call stack*.
	
- *asynchronous* code is code that runs without blocking code after it.
## [[Promises]]
- `Promise` is a class in [[Javascript]] that provides methods to wait for asynchronous code and do stuff after it.
## `async`/`await`
