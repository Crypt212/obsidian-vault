- **Local Storage** is a key-value storage mechanism available in the user's browser. It is part of the [[Web Storage API]] and is designed for storage that persists beyond the current session.

# Characteristics
- For the same website, **local storage** is the same across all tabs and windows.
- **Lifetime**: Lasts forever.
- **Accessiblity**: It's accessible only by client-side.
- **Capacity**: It is around *5~10MB*.
- **Scope**: It is scoped to the protocol + domain + port. For example, http://example.com and https://example.com have different local storage.

# Primary Use Cases
- Storing non-sensitive data that needs to persist between sessions.
- Caching static content or user data to improve performance on subsequent visits.
- Saving a draft of a form or a blog post locally.
