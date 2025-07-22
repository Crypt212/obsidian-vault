is an interface/mechanism that allow two software components to communicate under a set of definitions and protocols. The requesting software is called client, the responding one is called server.

### There are 4 current ways to configure and create APIs:

- [[SOAP API]]: is a less flexible API that provides messages exchange between client and server using XML, it is considered outdated.

- [[RCP API]]: client has a function that computes on the servers, then the server returns its output back to the client.

- [[WebSocket API]]: is a modern API that uses JSON objects to pass data. A WebSocket API supports two-way communication between client apps and the server. The server can send callback messages to connected clients, making it more efficient than [[REST API]].

- [[REST API]]: is the most popular and flexible API, today. The client sends requests to the server as data. The server uses this client input to start internal functions and returns output data back to the client.

### API Integrations

- software components that automatically update data between client and server, like data and time automatically sync on your machine when you travel to another time zone.