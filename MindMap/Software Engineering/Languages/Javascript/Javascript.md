# AJAX
- AJAX stands for **Asynchronous JavaScript and XML**, it's a set of web development techniques that allows a web page to communicate with a server **without reloading the entire page**.
- This creates a much faster and smoother user experience, similar to a desktop application.
- The process relies on a JavaScript object called the *[[XHR]]* or the newer, more powerful *[[Fetch API]]*.
> Note that it supports [[XML]], [[JSON]] and many more, the name is just historical.
## How it works
1. **An Event Occurs:** Something happens on your web page.
2. **Create an AJAX Request:** JavaScript creates an *[[XHR]]* object or uses the `fetch()` function.
3. **Send the Request:** The request is sent to a web server.
4. - **Server Processes the Request:** The server receives the request, does something, and prepares a response, usually in **[[JSON]]** or **[[XML]]** format.
5. **Server Sends a Response Back**.
6. **The Page is Updated**: JavaScript uses the **[[DOM]]** to dynamically update _only the specific part_ of the page that needs to change.
# XHR (`XMLHttpRequest`)
- The **`XMLHttpRequest`** object (often called **XHR**) is a built-in tool in JavaScript that allows your web page to **talk to a server** using [[HTTP]] protocol.
- You can *ask for* data (fetch information).
- You can *send* data (like form details).
- And all this happens *without reloading the entire page*.
- This was one of the first ways to make web pages dynamic and is the foundation of [[AJAX]].
> Note that it supports [[XML]], [[JSON]] and many more, the name is just historical.
## Important Properties
1. `readyState`: Shows the progress of request:
	- `0`: **UNSENT**: Request is created but not opened yet.
	- `1`: **OPENED**: Request is opened and ready to be sent.
	- `2`: **HEADERS_RECEIVED**: Server responded with headers.
	- `3`: **LOADING**: Response is loading.
	- `4`: **DONE**: Request is finished and response is ready.
2. `status`: Shows the **result** of your request ([[HTTP]] status code).
3. `responseText`: The actual data the server sends back, in **plain text** (could be [[HTML]], [[JSON]], or [[XML]].)
## Important Methods
1. `open(method, url, async)`: Prepares a request (opens it).
	- `method`: The `HTTP` request method.
	- `async`: Boolean defines whether the `xhr.send` method is *non-blocking* (`true`) or *blocking* (`false`), default is `true`. It is always better to set it to `true`, since, sync function will freeze the browser until request is done (bad user experience).
2. `send(data)`: Sends the request to the ser