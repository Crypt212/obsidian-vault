- The **`XMLHttpRequest`** object (often called **XHR**) is a built-in tool in [[JavaScript]] that allows your web page to **talk to a server** using [[HTTP]] protocol.
- You can *ask for* data (fetch information).
- You can *send* data (like form details).
- And all this happens *without reloading the entire page*.
- This was one of the first ways to make web pages dynamic and is the foundation of [[AJAX]].
> Note: XHR supports [[XML]], [[MindMap/Software Engineering/Serialization Format/JSON]] and many more, the name is just historical.
> Note: XHR is the old way to request data in [[JavaScript]], now we use [[Fetch API]].
# Important Properties
1. `readyState`: Shows the progress of request:
	- `0`: **UNSENT**: Request is created but not opened yet.
	- `1`: **OPENED**: Request is opened and ready to be sent.
	- `2`: **HEADERS_RECEIVED**: Server responded with headers.
	- `3`: **LOADING**: Response is loading.
	- `4`: **DONE**: Request is finished and response is ready.
2. `status`: Shows the **result** of your request ([[HTTP]] status code).
3. `responseText`: The actual data the server sends back, in **plain text** (could be [[HTML]], [[MindMap/Software Engineering/Serialization Format/JSON]], or [[XML]].)
# Important Methods
1. `open(method, url, async)`: Prepares a request (opens it).
	- `method`: The `HTTP` request method.
	- `async`: Boolean defines whether the `xhr.send` method is *non-blocking* (`true`) or *blocking* (`false`), default is `true`. It is always better to set it to `true`, since, sync function will freeze the browser until request is done (bad user experience).
2. `send(data)`: Sends the request to the server.
	- `data`: Optional. The data to be sent, if any.
3. `setRequestHeader(header, value)`:  Sets `HTTP` headers for the request.
# Important EventHandlers
1. `noreadystatechange`: Runs when `readyState` changes.
2. `onload`: Runs when the request is done and successful (`status == 200`).
3. `onerror`: Runs when something goes wrong.
