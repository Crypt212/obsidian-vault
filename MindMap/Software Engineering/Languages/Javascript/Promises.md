- `Promise` is a class in [[Javascript]] that provides methods to wait for asynchronous code and do stuff after it.
- We can make an instance that takes a callback holding the *asynchronous code*, and `resolve` and `reject` callback functions as parameters that we can call, allowing us to indicate success or failure to the code to the promise object.
- A promise has a `state` property that could have values `pending`, `resolved`, `rejected`.
- When resolved, a promise will have a `value` property holding the data passed to the `resolve` callback function.
- When rejected, a promise will have a `reason` property holding the error passed to the `reject` callback function, or any thrown error.
# Important Methods
1. `.then(acceptCallback, rejectCallback)`: 