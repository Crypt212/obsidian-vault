#runtime-environment
- is a **runtime environment** to run and execute [[Javascript]] *outside the browser*, usually for development on the server.
- **Node JS** includes:
	- The **V8 Javascript Engine** (same as Chrome).
	- Tools (called *core modules*) for working with: Files, Network, OS, [[Web Server|Web Servers]], Modules and Packages.
- **Node JS** is built using **[[C++]]** and **[[Javascript]]**.
- Uses **modules** to organize code.
- It has no access to [[DOM]].
# Benefits
- Use one language everywhere.
- Build fast backend servers (in development, and good performance).
- It's exceptionally fast and efficient for **I/O-bound** tasks (networking, databases) due to its non-blocking, event-driven architecture.
- Real-time apps like chats, games and collaborative tools are well handled.
- Supported package management [[NPM]] (Node Package Manager).
# Limitations
- **CPU-bound Tasks.** If you give the single-threaded Event Loop a task that requires a lot of calculation (e.g., complex mathematical computations, sorting huge arrays, image/resize processing, synchronous CPU-intensive logic), it will **block** the loop.
# Modules
- Modules are encapsulated and reusable chunks of code that has its own context
- In [[Node JS]], each file is treated as a seperate module.

## Types of Modules
- Local modules - Modules that we create in our application.
- Built-in modules - Modules provided by the [[Node JS]] out of the box.
- Third party modules - Modules provided by other developers.
## Supported Module Systems
- CommonJS modules.
- Ecmascript modules.
## Module Scope
- When modules are imported, each module has its own scope for its variables, isolating them from the environment they are called in, here is an example:
```javascript
// foo.js
const a = 'foo';
console.log(a);

// boo.js
const a = 'boo'; // same constant name
console.log(a);

// index.js
import 'foo.js';
import 'boo.js';

// output
// foo
// boo
```
- This is achieved by using ***module wrapper***.
## Module Wrapper
- under the hood, every module (including the starting main/index module) is wrapped in an [[IIFE]] function call, it looks something like this:
```javascript
(function(exports, require, module, __filename, __dirname) {
})
```
- `__filename`: is the name of the filename of the current module.
- `__dirname`: is the name of the directory in which the current module exists.
- `require`: is the function used to import other modules, it has some important properties like the `cache` that holds a map from cached imported module paths to its `Module` instances.
- `exports`: is a reference to the `module.exports` property.
- `module`: is a `Module` instance that holds information for the current module, one example is the `exports` property which holds the exported data from the current module.
### Favour `module.exports` over `exports`
- `exports` is a reference to the object `module.exports`, if we set data to `exports.x`, that sets it to the property  `module.exports.x`.
- **The Proplem**: if we assign an object (containing our exported functions for example) to `exports`, [[Javascript]] will interpret that as breaking the reference and setting the new object for `exports` only, meaning `exports` will not be a reference to `module.exports` anymore.
## Module Caching
- When modules are imported using *CommonJS* modules system, imports done by `require` are saved in `require.cache`, they are cached so that when requiring them again they don't reload them from start.
- When modules are imported using 