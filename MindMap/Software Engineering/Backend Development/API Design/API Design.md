2025-07-23 18:46
Tags:

- Is an interface/mechanism that allow two software components to communicate under a set of definitions and protocols. The requesting software is called client, the responding one is called server.
- Before designing, you choose the *communication paradigm* (Request\response, Real-Time, Bidirectional streaming, ... etc) first, leading to determining the protocol ([[HTTP]], [[WebSocket]], [[SSE]], ... etc), and finally choosing the architectural style.
# Architectural Styles
- There are many **Architectural Styles** for APIs.

| API Style     | Primary Use Case                                                 | Key Characteristics                                                                                                                        |
| ------------- | ---------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| **REST**      | General-purpose web APIs.                                        | Uses HTTP methods (GET, POST, etc.), stateless, returns data (often in JSON). **The most common web API.**                                 |
| **GraphQL**   | Querying complex data, client-specific needs.                    | Lets the client ask for _exactly_ the data it needs in a single request. Avoids over-fetching and under-fetching.                          |
| **gRPC**      | High-performance internal microservices.                         | Uses HTTP/2 for speed, uses **Protocol Buffers** (a binary format) for efficient serialization. Great for server-to-server communication.  |
| **SOAP**      | Enterprise-level, high-security systems (e.g., banking).         | A strict protocol using XML. Very formal with built-in error handling and security (WS-Security).                                          |
| **WebSocket** | Real-time, bidirectional communication (e.g., chat, live feeds). | Provides a persistent, full-duplex connection between client and server. Unlike others, it's for constant streaming, not request-response. |
# API Types
1. **Open/Public APIs:** Available for any developer to use. Often require an API key. (e.g., Twitter API, Google Maps API).

2. **Partner APIs:** Not publicly available; access is granted specifically to business partners.

3. **Internal/Private APIs:** Used within a single company for its internal systems to talk to each other. Not exposed to the outside world. (e.g., a front-end web app talking to a back-end service).

4. **Composite APIs:** APIs that bundle multiple API requests (often to different endpoints or services) into a single call. This is useful for performance in micro-services architectures.
# Design Principles
## Consistency
## Simplicity
## Security
## Performance