- `Promise` is a class in [[Javascript]] that provides methods to wait for asynchronous code and do stuff after it.
- We can make an instance that takes a callback holding the *asynchronous code*, and `resolve` and `reject` callback functions as parameters that we can call, allowing us to indicate success or failure to the code to the promise object.
- A promise has a state
# Important Methods
1. `.then(acceptCallback, rejectCallback)`: 