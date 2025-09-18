#framework
- **Express** is a **web framework** and [[Node JS]] package used to build [[Web Server|web servers]] with [[HTTP]] protocol in [[Javascript]].
- Other [[Node JS]] frameworks for beckend development: [[Fastify]], [[Koa]], [[Nest JS]], [[Hapi]].
- Differences between version 4 and 5 are negligible.
# How it works
- The **server app** instance is created using `express()` factory function.
- The **app** instance is setup to listen on a specific *port* for requests using `listen(port, callback)` method, the *callback function* runs after listening is set up.
- The **app** instance has methods to handle [[HTTP]] requests and return responses, these methods take the `url` and callback function that takes `request` and `response` parameters of type [[Request]] and [[Response]] objects (ex. `get(url, callback)`).
- [[Request]] 
# Middlewares
## Built-in Middlewares
- `express.static(filepath)`: Sets a file to be public so that it's content can be accecced