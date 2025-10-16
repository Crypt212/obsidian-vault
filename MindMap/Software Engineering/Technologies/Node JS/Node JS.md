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
- In [[Node JS]], each file is treated as a seperate [[Modules|module]].
## History
- At the time [[Node JS]] was created, there was no built-in [[Modules|module]] system in [[Javascript]].
- [[Node JS]] defaulted to [[Modules|CommonJS]] as its [[Modules|module]] system.
- As of ES2015, [[Javascript]] does have a standardised module system as part of the language itself.
- That new [[modules|module]] system is called the [[Modules|EcmaScript Modules]], ES Modules, or ESM.
- The [[Modules|ES Modules]] is now supported by [[Node JS]].
## Types of Modules
- Local modules - [[Modules]] that we create in our application.
- Built-in modules - [[Modules]] provided by the [[Node JS]] out of the box.
- Third party [[modules]] - [[Modules]] provided by other developers.
## Built-in Modules
- `path`
- `events`
- `fs`
- `stream`
- `http`