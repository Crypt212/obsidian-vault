- **Cookies** are small pieces of data sent from a website and stored on the user's computer by the web browser.
- They are *automatically* sent back to the server with every [[HTTP]] request.
- They are accessible by both **client** and **Server**.
- They are set by the **server** using `Set-Cookie` [[HTTP]] header.
- If they are set with expiration date, they will presist until that date (even after closing the browser).
- If no expiration date is set, they will last only for the **session**.
- For the same website, every opened tab has its own **session storage**.
- It's capacity is around *4KB*.
- **Scope**: Tied to a specific domain. Can be scoped to a subdomain (e.g., blog.example.com).

# Primary Use Cases:
- **Session Management**: Logging in to a website. The server sends a session cookie to identify you on subsequent page loads.
- **Personalization**: Storing user preferences like theme, language, or font size.
- **Tracking**: Analyzing user behavior across a site or even across different sites (third-party cookies).
