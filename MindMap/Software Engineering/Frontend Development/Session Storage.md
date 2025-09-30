- **Session Storage** is a key-value storage mechanism available in the user's browser. It is part of the [[Web Storage API]].

# Characteristics
- **Lifetime**: Data is cleared when the page session ends. A page session lasts as long as the browser is open, and survives over page reloads and restores. However, closing the browser tab or window ends the session and clears the storage.
- **Accessiblity**: It's accessible only by client-side.
- **Capacity**: It is around *5~10MB*.
- **Scope**: It is scoped to the browser tab. If you open the same site in two tabs, each tab will have its own separate session storage.

# Primary Use Cases
- Storing information for a single workflow or task, like the contents of a multi-step form.
- Storing data that should not persist after leaving the page.
