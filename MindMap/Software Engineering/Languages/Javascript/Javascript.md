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
- The **`XMLHttpRequest`** object (often called **XHR**) is a built-in tool in JavaScript that allows your web page to **talk to a server**.
- You can *ask for* data (fetch information).
- You can *send* data (like form details).
- And all this happens *without reloading the entire page*.
- This was one of the first ways to make web pages dynamic and is the foundation of [[AJAX]].
> Note that it supports [[XML]], [[JSON]] and many more, the name is just historical.
## Important Properties
1. `readyState`: Shows the 