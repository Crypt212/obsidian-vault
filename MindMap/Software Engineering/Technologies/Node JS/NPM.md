# Module Caching
- when modules are imported using [[CommonJS]] modules system, imports done by `require` are saved in `require.cache`, they are cached so that when requiring them again they don't reload them from start.
