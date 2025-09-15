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
# Module Systems
## CommonJS
## Ecmascript Modules

## Module Caching
- when modules are imported using [[CommonJS]] modules system, imports done by `require` are saved in `require.cache`, they are cached so that when requiring them again they don't reload them from start.
# Core Node Modules
- `OS` module for dealing with operating system.
- ``