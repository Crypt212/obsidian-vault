- AJAX stands for **Asynchronous JavaScript and XML**, it's a set of web development techniques that allows a web page to communicate with a server **without reloading the entire page**.
- This creates a much faster and smoother user experience, similar to a desktop application.
- The process relies on a JavaScript object called the *[[XHR]]* or the newer, more powerful *[[Fetch API]]*.
> Note that it supports [[XML]], [[MindMap/Software Engineering/Languages/Serialization Format/JSON]] and many more, the name is just historical.
# How it works
1. **An Event Occurs:** Something happens on your web page.
2. **Create an AJAX Request:** JavaScript creates an *[[XHR]]* object or uses the `fetch()` function.
3. **Send the Request:** The request is sent to a web server.
4. - **Server Processes the Request:** The server receives the request, does something, and prepares a response, usually in **[[MindMap/Software Engineering/Languages/Serialization Format/JSON]]** or **[[XML]]** format.
5. **Server Sends a Response Back**.
6. **The Page is Updated**: JavaScript uses the **[[DOM]]** to dynamically update _only the specific part_ of the page that needs to change.