- **HTTP** (HyperText Transfar Protocol) is a protocol that defines the structure of *messages* transferred between *server* and *client*, it follows the [[Web Architecture]] rules.

- The *messages* transferred are:
	- **Requests**: Messages sent by the *client* to the *server*, wishing some changes to the data on the server or requiring some data back.
	- **Responses**: Messages sent back to the *client* after processing the request, having the resulting state.

- **HTTP** *requests/responses* are have some rules, they are sent using **data serialization formats** (like [[MindMap/Software Engineering/Languages/Serialization Format/JSON]], [[XML]], ...etc).
# HTTP Versions
| Version                              | Key Features & Differences                                                                                                                                                                                                                                                                                                                                                                                        | Impact                                                                                                              |
| ------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| **HTTP/0.9** (1991)                  | - The simplest. Only `GET` method.  <br>- No headers, no status codes, only HTML.                                                                                                                                                                                                                                                                                                                                 | Obsolete. Historical only.                                                                                          |
| **HTTP/1.0** (1996)                  | - **Added headers** (for meta-data).  <br>- **Status codes** (e.g., 200 OK, 404 Not Found).  <br>- **Other methods** (`POST`, `HEAD`).  <br>- **Could transfer other files** (images, scripts).                                                                                                                                                                                                                   | **Major improvement.** But: opened a **new TCP connection for every request**, which was very slow and inefficient. |
| **HTTP/1.1** (1997, updated in 1999) | - **Persistent Connections:** Reused a single TCP connection for multiple requests, reducing latency.  <br>- **Pipelining:** Sent multiple requests without waiting for responses (was problematic and often disabled).  <br>- **Chunked Transfer Encoding:** Allowed streaming of content.  <br>- **New Methods:** `PUT`, `PATCH`, `DELETE`, `OPTIONS`, `TRACE`.                                                 | **The workhorse of the web for over 20 years.** It solved the biggest inefficiencies of 1.0.                        |
| **HTTP/2** (2015)                    | - **Binary Protocol:** Instead of text, it's binary, making it faster to parse and more efficient.  <br>- **Multiplexing:** Sends multiple requests and responses **simultaneously over a single connection**, solving head-of-line blocking.  <br>- **Header Compression:** (HPACK) Reduces overhead.  <br>- **Server Push:** Allows the server to send resources to the client before the client asks for them. | **Major performance boost** for modern websites, which often require hundreds of resources.                         |
| **HTTP/3** (2022)                    | - **Uses QUIC instead of TCP:** QUIC is a transport protocol built on UDP. It solves TCP's head-of-line blocking at the transport layer.  <br>- **Connection Migration:** If you switch networks (Wi-Fi to 5G), the connection can continue without re-handshaking.  <br>- **Faster Handshake:** QUIC combines TLS encryption and transport handshakes into a single step, reducing latency.                      | The next evolution, focused on **reducing latency** even further, especially on mobile and unstable networks.       |
- **Key Evolution:** The driving force has been **performance**. Reducing the number of connections (1.1), then making the single connection vastly more efficient (2), and finally reworking the underlying transport protocol for lower latency (3).
# Structure
- The **HTTP** *response or request* has a **start-line**, **headers**, a blank line, and an optional **body**.
## Start Line
-
## Header
- contains information about the request/response.
- headers could be divided into categories:
### General Headers
- Apply to both requests and responses.
#### `Connection`
- controls connection persistence.
#### `Cache-Control` 
- caching directives.
#### `Date` 
- Date of the request/response.
#### `Content-Type`
- The content type using [[MIME]] types.
### Request Headers
- Provide more information about the resource to be fetched or the client itself.
#### `Host`
- mandatory in HTTP/1.1 
#### `User-Agent`
- client ID
#### `Accept`
- what content types the client understands.
#### `Authorization`
- credentials
### Response Headers
- Provide additional information about the response.
#### `Server`
- server software
#### `Set-Cookie`
- sends a cookie to the client
#### `Age`
- how long the object was in a cache
### Entity/Representation Headers
- Describe the content (body) of the message.
#### `Content-Type`
- MIME type of the body, e.g., `text/html`
#### `Content-Length`
- size of the body in bytes
#### `Content-Encoding`
- compression used, e.g., `gzip`
## Body
- Contains the data transferred.
## HTTP Methods (Verbs)

- `GET`: Retrieve a resource.
- `POST`: Submit data to be processed (create a new resource).
- `PUT`: Replace a resource.
- `PATCH`: Partially update a resource.
- `DELETE`: Remove a resource.
- `HEAD`: Get the headers for a resource (like GET but without the body).
- `OPTIONS`: Ask the server which methods are supported for a resource.
	
## Status Code Classes

- `1xx` (**Informational**): Request received, continuing process.
- `2xx` (**Success**): Action was successfully received, understood, and accepted. (`200 OK`, `201 Created`).
- `3xx` (**Redirection**): Further action needs to be taken to complete the request. (`301 Moved Permanently`, `304 Not Modified`).
- `4xx` (**Client Error**): The request contains bad syntax or cannot be fulfilled. (`400 Bad Request`, `403 Forbidden`, **`404 Not Found`**).
- `5xx` (**Server Error**): The server failed to fulfill a valid request. (**`500 Internal Server Error`**, `502 Bad Gateway`, `503 Service Unavailable`).

# [[HTTPS]]
- HTTP **Secure**. It is simply HTTP running over [[SSL]]/[[TLS]] encryption. It provides privacy, integrity, and authentication. The communication is encrypted, preventing eavesdropping.